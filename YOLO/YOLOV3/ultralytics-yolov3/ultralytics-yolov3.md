# ultralytics-yolov3 源码阅读

## 源码地址

archive:https://github.com/TNTWEN/yolov3/tree/archive

# 文件结构

|-- cfg

​	|-- yolov3-spp.weights

|-- data

​	|-- coco2017.data

​	|-- coco.names

|-- utils

​	|-- adabound.py

​	|-- datasets.py

​	|-- google_utils.py

​	|-- layers.py

​	|-- parse_config.py

​	|-- torch_utils.py

​	|-- utils.py

|-- weights

​	|-- yolov3-spp.weights

|-- models.py

|-- [train.py](###train.py)

|-- test.py

|-- detect.py

## 源码解析

## train.py

[argparse](###argparse)

[apex](###apex)

[glob](###glob)



**可选项：超参数的替换**

```
import numpy as np
'''
a.txt内容：
1
2
3

'''
hyp = {'giou': 3.54,  # giou loss gain
       'cls': 37.4,  # cls loss gain
       'cls_pw': 1.0} # cls BCELoss positive_weight

for k, v in zip(hyp.keys(), np.loadtxt("a.txt")):
    hyp[k] = v

print(hyp)

输出：
{'giou': 1.0, 'cls': 2.0, 'cls_pw': 3.0}

```

**梯度累计次数**

```
accumulate = max(round(64 / batch_size), 1)
```

[round](###round)

GPU资源首先时，梯度累计一定程度上缓解batchsize小带来的问题（为什么只是一定程度上？因为batchsize越大，批归一化效果会更好） 实际使用时，batchsize依旧是设得越大越好

若batchsize >64,那它就是实际的batchsize

若batchsize=16，accumulate=4，累积四次的梯度后再反向传播，一定程度上相当于batchsize为64



[math.fmod与%](###math.fmod 与%)



**init_seeds()**

代码在运行过程中会存在许多的随机性，比如参数的随机初始化等，这会导致每次运行的结果不能完全一样，导致实验结果不可复现。在以下几处设定好统一的随机数种子即可

- python 自带的 random.seed(seed)

- numpy : np.random.seed(seed)

- pytorch : torch.manual_seed(seed)

- CUDNN库 ：

  - torch.backends.cudnn.benchmark
    设置这个flag可以让内置的cuDNN的auto-tuner自动寻找最适合当前配置的高效算法，来达到优化运行效率的问题。但是由于噪声和不同的硬件条件，即使是同一台机器，benchmark都可能会选择不同的算法。为了消除这个随机性，只需要disable它即可。

  ```
    torch.backends.cudnn.benchmark = False
  ```

  - torch.backends.cudnn.deterministic
    CUDA中的一些运算，如对sparse的CUDA张量与dense的CUDA张量调用torch.bmm()，它通常使用不确定性算法。为了避免这种情况，就要将这个flag设置为True，让它使用确定的实现。

    ```
    torch.backends.cudnn.deterministic = True
    ```

在ultralytics-yolov3中：

-- train.py

```
from utils.utils import *
init_seeds()
```

-- utils/utils.py

```
import random
import numpy as np
from . import torch_utils 

def init_seeds(seed=0):
    random.seed(seed)#√
    np.random.seed(seed)#√
    torch_utils.init_seeds(seed=seed)
```

-- utils/torch_utils.py

```
def init_seeds(seed=0):
    torch.manual_seed(seed)

    # Reduce randomness (may be slower on Tesla GPUs) # https://pytorch.org/docs/stable/notes/randomness.html
    if seed == 0:
        cudnn.deterministic = False
        cudnn.benchmark = True
```

此处`cudnn.deterministic = False  cudnn.benchmark = True`的设置与上面介绍的相反

https://github.com/ultralytics/yolov3/issues/679  关于NMS速度的讨论，涉及到了``cudnn.deterministic cudnn.benchmark`在不同取值时速度情况的对比



在yolov5源码中：

```
def init_torch_seeds(seed=0):
    # Speed-reproducibility tradeoff    https://pytorch.org/docs/stable/notes/randomness.html
    torch.manual_seed(seed)
    if seed == 0:  # slower, more reproducible
        cudnn.benchmark, cudnn.deterministic = False, True
    else:  # faster, less reproducible
        cudnn.benchmark, cudnn.deterministic = True, False
```

seed=0时 `cudnn.benchmark, cudnn.deterministic = False, True`更容易复现，但速度会慢一些。

**data_dict = parse_data_cfg(data)**

[parse_data_cfg(data)](###parse_data_cfg(data))



**初始化model**

-- train.py 

```
model = Darknet(cfg).to(device)
```

-- [models.py](##models.py)

​	--class Darknet

​		[parse_model_cfg(cfg)](###parse_model_cfg(cfg))

**optimizer**

使用add_param_group(),不同层使用不同的lr和weight decay

```
if opt.adam:
    # hyp['lr0'] *= 0.1  # reduce lr (i.e. SGD=5E-3, Adam=5E-4)
    optimizer = optim.Adam(pg0, lr=hyp['lr0'])
    # optimizer = AdaBound(pg0, lr=hyp['lr0'], final_lr=0.1)
else:
    optimizer = optim.SGD(pg0, lr=hyp['lr0'], momentum=hyp['momentum'], nesterov=True)
optimizer.add_param_group({'params': pg1, 'weight_decay': hyp['weight_decay']})  # add pg1 with weight_decay
optimizer.add_param_group({'params': pg2})  # add pg2 (biases)
print(optimizer)
print('Optimizer groups: %g .bias, %g Conv2d.weight, %g other' % (len(pg2), len(pg1), len(pg0)))
del pg0, pg1, pg2
```

print(optimizer) 输出

```
SGD (
Parameter Group 0
    dampening: 0
    lr: 0.01
    momentum: 0.937
    nesterov: True
    weight_decay: 0

Parameter Group 1
    dampening: 0
    lr: 0.01
    momentum: 0.937
    nesterov: True
    weight_decay: 0.0005

Parameter Group 2
    dampening: 0
    lr: 0.01
    momentum: 0.937
    nesterov: True
    weight_decay: 0
)
```



**模型加载**

1. 从.pt加载

```
ckpt = torch.load("weights/last.pt", map_location=device)
```

ckpt的组成部分：



```
for k,v in ckpt.items():
    print(k)
```

epoch     <class 'int'>
best_fitness <class 'numpy.ndarray'>
training_results   <class 'str'>
model          <class 'dict'>
optimizer    <class 'dict'>



加载的参数model  optimizer best_fitness



2. 从darknet.weights 加载

models.py->函数 load_darknet_weights(self, weights, cutoff=-1)





**余弦退火**

```
import torch.optim.lr_scheduler as lr_scheduler

# Scheduler https://arxiv.org/pdf/1812.01187.pdf 余弦退火
    lf = lambda x: (((1 + math.cos(x * math.pi / epochs)) / 2) ** 1.0) * 0.95 + 0.05  # cosine
    scheduler = lr_scheduler.LambdaLR(optimizer, lr_lambda=lf)
    scheduler.last_epoch = start_epoch - 1  # see link below
    # https://discuss.pytorch.org/t/a-problem-occured-when-resuming-an-optimizer/28822
```



## parse_config.py

### parse_data_cfg(data)

解析data文件，读取至字典

例如：coco2017.data

```
classes=80
train=C:\Project\data\coco2017\train2017.txt
valid=C:\Project\data\coco2017\val2017.txt
names=data\coco.names
```

函数：parse_data_cfg(data)

```
def parse_data_cfg(path):
	#路径支持 data/*.data 或者*.data
    # Parses the data configuration file
    if not os.path.exists(path) and os.path.exists('data' + os.sep + path):  # add data/ prefix if omitted
        path = 'data' + os.sep + path

    with open(path, 'r') as f:
        lines = f.readlines()

    options = dict()
    for line in lines:
        line = line.strip()
        if line == '' or line.startswith('#'):
            continue
        key, val = line.split('=')
        options[key.strip()] = val.strip()

    return options
```

### parse_model_cfg(cfg)









## models.py



## 知识点详解

### argparse

命令行解析的标准模，这个库可以让我们直接在命令行中就可以向程序中传入参数并让程序运行。

以train.py为例，其使用模板为：

```
import argparse
 parser = argparse.ArgumentParser()
    parser.add_argument('--epochs', type=int, default=300)  # 500200 batches at bs 16, 117263 COCO images = 273 epochs
    parser.add_argument('--batch-size', type=int, default=64)  # effective bs = batch_size * accumulate = 16 * 4 = 64
    parser.add_argument('--cfg', type=str, default='cfg/yolov3-spp-voc.cfg', help='*.cfg path')
    parser.add_argument('--data', type=str, default='data/voc.data', help='*.data path')
    parser.add_argument('--multi-scale', action='store_true', help='adjust (67%% - 150%%) img_size every 10 batches')
    parser.add_argument('--img-size', nargs='+', type=int, default=[416, 416], help='[min_train, max-train, test]')
    parser.add_argument('--rect', action='store_true', help='rectangular training')
    parser.add_argument('--resume', action='store_true', help='resume training from last.pt')
    parser.add_argument('--nosave', action='store_true', help='only save final checkpoint')
    parser.add_argument('--notest', action='store_true', help='only test final epoch')
    parser.add_argument('--evolve', action='store_true', help='evolve hyperparameters')
    parser.add_argument('--bucket', type=str, default='', help='gsutil bucket')
    parser.add_argument('--cache-images', action='store_true', help='cache images for faster training')
    parser.add_argument('--weights', type=str, default='weights\last.pt', help='initial weights path')
    parser.add_argument('--name', default='', help='renames results.txt to results_name.txt if supplied')
    parser.add_argument('--device', default='', help='device id (i.e. 0 or 0,1 or cpu)')
    parser.add_argument('--adam', action='store_true', help='use adam optimizer')
    parser.add_argument('--single-cls', action='store_true', help='train as single-class dataset')
    parser.add_argument('--freeze-layers', action='store_true', help='Freeze non-output layers')
    opt = parser.parse_args()
```

随后就可以用opt.调用参数

如opt.cfg  ,opt.weights

### apex

APEX是英伟达开源的，完美支持PyTorch框架，用于改变数据格式来减小模型显存占用的工具。其中最有价值的是amp（Automatic Mixed Precision），将模型的大部分操作都用Float16数据类型测试，一些特别操作仍然使用Float32。并且用户仅仅通过三行代码即可完美将自己的训练代码迁移到该模型。实验证明，使用Float16作为大部分操作的数据类型，并没有降低参数，在一些实验中，反而由于可以增大Batch size，带来精度上的提升，以及训练速度上的提升。

https://github.com/NVIDIA/apex

https://blog.csdn.net/c9Yv2cf9I06K2A9E/article/details/100135729

```
O0：纯FP32训练，可以作为accuracy的baseline；
O1：混合精度训练（推荐使用），根据黑白名单自动决定使用FP16（GEMM, 卷积）还是FP32（Softmax）进行计算。
O2：“几乎FP16”混合精度训练，不存在黑白名单，除了Batch norm，几乎都是用FP16计算。
O3：纯FP16训练，很不稳定，但是可以作为speed的baseline；
```

以yolov3-spp，VOC数据集为例，只有o3最后保存的.pt文件变小了，o0,o1,o2都是按单精度保存的。最后转化为darknet权重（.weights)时，会统一保存精度。   不过日常使用时用o1即可。

​           .pt                 .weights

O0:490098KB    245037KB

O1:490098KB    245037KB

O2:490098KB    245037KB

O3:367685KB    245037KB

注：.pt文件保存了如epoch，优化器等信息，大小一般为.weights文件的2倍。

```
mixed_precision = True
try:  # Mixed precision training https://github.com/NVIDIA/apex
    from apex import amp
except:
    print('Apex recommended for faster mixed precision training: https://github.com/NVIDIA/apex')
    mixed_precision = False  # not installed
    
if mixed_precision:
	model, optimizer = amp.initialize(model, optimizer, opt_level='O1', verbosity=0)
	
if mixed_precision:
    with amp.scale_loss(loss, optimizer) as scaled_loss:
        scaled_loss.backward()
```

### glob

匹配所有的符合条件的文件，并将其以list的形式返回。

![image-20210219200842179](assets/image-20210219200842179.png)

```
import glob
f=glob.glob("hyp*.txt")
print(f)

>>>['hyp.txt', 'hyp2.txt']
```

glob.glob()的返回值时一个list   ，可以用+来合并多个glob.glob

```
# Remove previous results
for f in glob.glob('*_batch*.jpg') + glob.glob(results_file):
	os.remove(f)
```



### round

**round()** 方法返回浮点数 x 的四舍五入值，准确的说保留值将保留到离上一位更近的一端（四舍六入）。

精度要求高的，不建议使用该函数。

# 

```
>>> round(10.0/3, 2)
3.33
>>> round(20/7)
3
```

第一个参数是一个浮点数，第二个参数是保留的小数位数，可选，如果不写的话默认保留到整数。

在python3中

 如果距离两边一样远，会保留到偶数的一边。比如round(0.5)和round(-0.5)都会保留到0，而round(1.5)会保留到2。

round(2.675, 2) 的结果，不论我们从python2还是3来看，结果都应该是2.68的，结果它偏偏是2.67，为什么？这跟浮点数的精度有关。我们知道在机器中浮点数不一定能精确表达，因为换算成一串1和0后可能是无限位数的，机器已经做出了截断处理。那么在机器中保存的2.675这个数字就比实际数字要小那么一点点。这一点点就导致了它离2.67要更近一点点，所以保留两位小数时就近似到了2.67。

除非对精确度没什么要求，否则尽量避开用round()函数。近似计算我们还有其他的选择：

- 使用math模块中的一些函数，比如math.ceiling（天花板除法）。
- python自带整除，python2中是/，3中是//。

### math.fmod与%

公式相同
y%x = y - (y/x)\*x
math.fmod(y,x) = y - (y/x)*x
两种运算方法的公式相同，区别在于y/x的取值方法不同：
y%x中的y/x倾向于向下取整（**在为负数时候，远离0的方向**），而math.fmod中的y/x倾向于向0的方向取整

例如：

-3%2=-3-(-3/2)*2=-3- (-2)\*2=1

math.fmod(-3,2)=-3-(-3/2)*2=-3-(-1)\*2=-1.0(float)   虽为float类型，但并不影响`math.mod(x,y)==0` 的逻辑判断



