**model.named_parameters():**

如果print(model.named_parameters()) ,输出为：<class 'generator'>

```
for k, v in dict(model.named_parameters()).items():
    print(k)
for k, v in model.named_parameters():
    print(k)
两者没啥区别    
module_list.0.Conv2d.weight	
module_list.0.BatchNorm2d.weight
module_list.0.BatchNorm2d.bias
module_list.1.Conv2d.weight
module_list.1.BatchNorm2d.weight
module_list.1.BatchNorm2d.bias
module_list.2.Conv2d.weight
module_list.2.BatchNorm2d.weight
module_list.2.BatchNorm2d.bias

module_list.0.Conv2d.weight
module_list.0.BatchNorm2d.weight
module_list.0.BatchNorm2d.bias
module_list.1.Conv2d.weight
module_list.1.BatchNorm2d.weight
module_list.1.BatchNorm2d.bias
module_list.2.Conv2d.weight
module_list.2.BatchNorm2d.weight
module_list.2.BatchNorm2d.bias
```



以yolov3-spp-voc.cfg为例

**model.named_parameters()只显示可学习参数**

```
for k, v in model.named_parameters():
    print(k)
```

输出：

```
module_list.0.Conv2d.weight
module_list.0.BatchNorm2d.weight
module_list.0.BatchNorm2d.bias
module_list.1.Conv2d.weight
module_list.1.BatchNorm2d.weight
module_list.1.BatchNorm2d.bias
module_list.2.Conv2d.weight
module_list.2.BatchNorm2d.weight
module_list.2.BatchNorm2d.bias
module_list.3.Conv2d.weight
module_list.3.BatchNorm2d.weight
module_list.3.BatchNorm2d.bias
module_list.5.Conv2d.weight
module_list.5.BatchNorm2d.weight
module_list.5.BatchNorm2d.bias
module_list.6.Conv2d.weight
module_list.6.BatchNorm2d.weight
module_list.6.BatchNorm2d.bias
module_list.7.Conv2d.weight
module_list.7.BatchNorm2d.weight
module_list.7.BatchNorm2d.bias
module_list.9.Conv2d.weight
module_list.9.BatchNorm2d.weight
module_list.9.BatchNorm2d.bias
module_list.10.Conv2d.weight
module_list.10.BatchNorm2d.weight
module_list.10.BatchNorm2d.bias
module_list.12.Conv2d.weight
module_list.12.BatchNorm2d.weight
module_list.12.BatchNorm2d.bias
module_list.13.Conv2d.weight
module_list.13.BatchNorm2d.weight
module_list.13.BatchNorm2d.bias
module_list.14.Conv2d.weight
module_list.14.BatchNorm2d.weight
module_list.14.BatchNorm2d.bias
module_list.16.Conv2d.weight
module_list.16.BatchNorm2d.weight
module_list.16.BatchNorm2d.bias
module_list.17.Conv2d.weight
module_list.17.BatchNorm2d.weight
module_list.17.BatchNorm2d.bias
module_list.19.Conv2d.weight
module_list.19.BatchNorm2d.weight
module_list.19.BatchNorm2d.bias
module_list.20.Conv2d.weight
module_list.20.BatchNorm2d.weight
module_list.20.BatchNorm2d.bias
module_list.22.Conv2d.weight
module_list.22.BatchNorm2d.weight
module_list.22.BatchNorm2d.bias
module_list.23.Conv2d.weight
module_list.23.BatchNorm2d.weight
module_list.23.BatchNorm2d.bias
module_list.25.Conv2d.weight
module_list.25.BatchNorm2d.weight
module_list.25.BatchNorm2d.bias
module_list.26.Conv2d.weight
module_list.26.BatchNorm2d.weight
module_list.26.BatchNorm2d.bias
module_list.28.Conv2d.weight
module_list.28.BatchNorm2d.weight
module_list.28.BatchNorm2d.bias
module_list.29.Conv2d.weight
module_list.29.BatchNorm2d.weight
module_list.29.BatchNorm2d.bias
module_list.31.Conv2d.weight
module_list.31.BatchNorm2d.weight
module_list.31.BatchNorm2d.bias
module_list.32.Conv2d.weight
module_list.32.BatchNorm2d.weight
module_list.32.BatchNorm2d.bias
module_list.34.Conv2d.weight
module_list.34.BatchNorm2d.weight
module_list.34.BatchNorm2d.bias
module_list.35.Conv2d.weight
module_list.35.BatchNorm2d.weight
module_list.35.BatchNorm2d.bias
module_list.37.Conv2d.weight
module_list.37.BatchNorm2d.weight
module_list.37.BatchNorm2d.bias
module_list.38.Conv2d.weight
module_list.38.BatchNorm2d.weight
module_list.38.BatchNorm2d.bias
module_list.39.Conv2d.weight
module_list.39.BatchNorm2d.weight
module_list.39.BatchNorm2d.bias
module_list.41.Conv2d.weight
module_list.41.BatchNorm2d.weight
module_list.41.BatchNorm2d.bias
module_list.42.Conv2d.weight
module_list.42.BatchNorm2d.weight
module_list.42.BatchNorm2d.bias
module_list.44.Conv2d.weight
module_list.44.BatchNorm2d.weight
module_list.44.BatchNorm2d.bias
module_list.45.Conv2d.weight
module_list.45.BatchNorm2d.weight
module_list.45.BatchNorm2d.bias
module_list.47.Conv2d.weight
module_list.47.BatchNorm2d.weight
module_list.47.BatchNorm2d.bias
module_list.48.Conv2d.weight
module_list.48.BatchNorm2d.weight
module_list.48.BatchNorm2d.bias
module_list.50.Conv2d.weight
module_list.50.BatchNorm2d.weight
module_list.50.BatchNorm2d.bias
module_list.51.Conv2d.weight
module_list.51.BatchNorm2d.weight
module_list.51.BatchNorm2d.bias
module_list.53.Conv2d.weight
module_list.53.BatchNorm2d.weight
module_list.53.BatchNorm2d.bias
module_list.54.Conv2d.weight
module_list.54.BatchNorm2d.weight
module_list.54.BatchNorm2d.bias
module_list.56.Conv2d.weight
module_list.56.BatchNorm2d.weight
module_list.56.BatchNorm2d.bias
module_list.57.Conv2d.weight
module_list.57.BatchNorm2d.weight
module_list.57.BatchNorm2d.bias
module_list.59.Conv2d.weight
module_list.59.BatchNorm2d.weight
module_list.59.BatchNorm2d.bias
module_list.60.Conv2d.weight
module_list.60.BatchNorm2d.weight
module_list.60.BatchNorm2d.bias
module_list.62.Conv2d.weight
module_list.62.BatchNorm2d.weight
module_list.62.BatchNorm2d.bias
module_list.63.Conv2d.weight
module_list.63.BatchNorm2d.weight
module_list.63.BatchNorm2d.bias
module_list.64.Conv2d.weight
module_list.64.BatchNorm2d.weight
module_list.64.BatchNorm2d.bias
module_list.66.Conv2d.weight
module_list.66.BatchNorm2d.weight
module_list.66.BatchNorm2d.bias
module_list.67.Conv2d.weight
module_list.67.BatchNorm2d.weight
module_list.67.BatchNorm2d.bias
module_list.69.Conv2d.weight
module_list.69.BatchNorm2d.weight
module_list.69.BatchNorm2d.bias
module_list.70.Conv2d.weight
module_list.70.BatchNorm2d.weight
module_list.70.BatchNorm2d.bias
module_list.72.Conv2d.weight
module_list.72.BatchNorm2d.weight
module_list.72.BatchNorm2d.bias
module_list.73.Conv2d.weight
module_list.73.BatchNorm2d.weight
module_list.73.BatchNorm2d.bias
module_list.75.Conv2d.weight
module_list.75.BatchNorm2d.weight
module_list.75.BatchNorm2d.bias
module_list.76.Conv2d.weight
module_list.76.BatchNorm2d.weight
module_list.76.BatchNorm2d.bias
module_list.77.Conv2d.weight
module_list.77.BatchNorm2d.weight
module_list.77.BatchNorm2d.bias
module_list.84.Conv2d.weight
module_list.84.BatchNorm2d.weight
module_list.84.BatchNorm2d.bias
module_list.85.Conv2d.weight
module_list.85.BatchNorm2d.weight
module_list.85.BatchNorm2d.bias
module_list.86.Conv2d.weight
module_list.86.BatchNorm2d.weight
module_list.86.BatchNorm2d.bias
module_list.87.Conv2d.weight
module_list.87.BatchNorm2d.weight
module_list.87.BatchNorm2d.bias
module_list.88.Conv2d.weight
module_list.88.Conv2d.bias
module_list.91.Conv2d.weight
module_list.91.BatchNorm2d.weight
module_list.91.BatchNorm2d.bias
module_list.94.Conv2d.weight
module_list.94.BatchNorm2d.weight
module_list.94.BatchNorm2d.bias
module_list.95.Conv2d.weight
module_list.95.BatchNorm2d.weight
module_list.95.BatchNorm2d.bias
module_list.96.Conv2d.weight
module_list.96.BatchNorm2d.weight
module_list.96.BatchNorm2d.bias
module_list.97.Conv2d.weight
module_list.97.BatchNorm2d.weight
module_list.97.BatchNorm2d.bias
module_list.98.Conv2d.weight
module_list.98.BatchNorm2d.weight
module_list.98.BatchNorm2d.bias
module_list.99.Conv2d.weight
module_list.99.BatchNorm2d.weight
module_list.99.BatchNorm2d.bias
module_list.100.Conv2d.weight
module_list.100.Conv2d.bias
module_list.103.Conv2d.weight
module_list.103.BatchNorm2d.weight
module_list.103.BatchNorm2d.bias
module_list.106.Conv2d.weight
module_list.106.BatchNorm2d.weight
module_list.106.BatchNorm2d.bias
module_list.107.Conv2d.weight
module_list.107.BatchNorm2d.weight
module_list.107.BatchNorm2d.bias
module_list.108.Conv2d.weight
module_list.108.BatchNorm2d.weight
module_list.108.BatchNorm2d.bias
module_list.109.Conv2d.weight
module_list.109.BatchNorm2d.weight
module_list.109.BatchNorm2d.bias
module_list.110.Conv2d.weight
module_list.110.BatchNorm2d.weight
module_list.110.BatchNorm2d.bias
module_list.111.Conv2d.weight
module_list.111.BatchNorm2d.weight
module_list.111.BatchNorm2d.bias
module_list.112.Conv2d.weight
module_list.112.Conv2d.bias
```



# ckpt['model']

```
for k, v in ckpt['model'].items():
    print(k)
```

```
module_list.0.Conv2d.weight
module_list.0.BatchNorm2d.weight
module_list.0.BatchNorm2d.bias
module_list.0.BatchNorm2d.running_mean
module_list.0.BatchNorm2d.running_var
module_list.0.BatchNorm2d.num_batches_tracked
module_list.1.Conv2d.weight
module_list.1.BatchNorm2d.weight
module_list.1.BatchNorm2d.bias
module_list.1.BatchNorm2d.running_mean
module_list.1.BatchNorm2d.running_var
module_list.1.BatchNorm2d.num_batches_tracked
module_list.2.Conv2d.weight
module_list.2.BatchNorm2d.weight
module_list.2.BatchNorm2d.bias
module_list.2.BatchNorm2d.running_mean
module_list.2.BatchNorm2d.running_var
module_list.2.BatchNorm2d.num_batches_tracked
module_list.3.Conv2d.weight
module_list.3.BatchNorm2d.weight
module_list.3.BatchNorm2d.bias
module_list.3.BatchNorm2d.running_mean
module_list.3.BatchNorm2d.running_var
module_list.3.BatchNorm2d.num_batches_tracked
module_list.5.Conv2d.weight
module_list.5.BatchNorm2d.weight
module_list.5.BatchNorm2d.bias
module_list.5.BatchNorm2d.running_mean
module_list.5.BatchNorm2d.running_var
module_list.5.BatchNorm2d.num_batches_tracked
module_list.6.Conv2d.weight
module_list.6.BatchNorm2d.weight
module_list.6.BatchNorm2d.bias
module_list.6.BatchNorm2d.running_mean
module_list.6.BatchNorm2d.running_var
module_list.6.BatchNorm2d.num_batches_tracked
module_list.7.Conv2d.weight
module_list.7.BatchNorm2d.weight
module_list.7.BatchNorm2d.bias
module_list.7.BatchNorm2d.running_mean
module_list.7.BatchNorm2d.running_var
module_list.7.BatchNorm2d.num_batches_tracked
module_list.9.Conv2d.weight
module_list.9.BatchNorm2d.weight
module_list.9.BatchNorm2d.bias
module_list.9.BatchNorm2d.running_mean
module_list.9.BatchNorm2d.running_var
module_list.9.BatchNorm2d.num_batches_tracked
module_list.10.Conv2d.weight
module_list.10.BatchNorm2d.weight
module_list.10.BatchNorm2d.bias
module_list.10.BatchNorm2d.running_mean
module_list.10.BatchNorm2d.running_var
module_list.10.BatchNorm2d.num_batches_tracked
module_list.12.Conv2d.weight
module_list.12.BatchNorm2d.weight
module_list.12.BatchNorm2d.bias
module_list.12.BatchNorm2d.running_mean
module_list.12.BatchNorm2d.running_var
module_list.12.BatchNorm2d.num_batches_tracked
module_list.13.Conv2d.weight
module_list.13.BatchNorm2d.weight
module_list.13.BatchNorm2d.bias
module_list.13.BatchNorm2d.running_mean
module_list.13.BatchNorm2d.running_var
module_list.13.BatchNorm2d.num_batches_tracked
module_list.14.Conv2d.weight
module_list.14.BatchNorm2d.weight
module_list.14.BatchNorm2d.bias
module_list.14.BatchNorm2d.running_mean
module_list.14.BatchNorm2d.running_var
module_list.14.BatchNorm2d.num_batches_tracked
module_list.16.Conv2d.weight
module_list.16.BatchNorm2d.weight
module_list.16.BatchNorm2d.bias
module_list.16.BatchNorm2d.running_mean
module_list.16.BatchNorm2d.running_var
module_list.16.BatchNorm2d.num_batches_tracked
module_list.17.Conv2d.weight
module_list.17.BatchNorm2d.weight
module_list.17.BatchNorm2d.bias
module_list.17.BatchNorm2d.running_mean
module_list.17.BatchNorm2d.running_var
module_list.17.BatchNorm2d.num_batches_tracked
module_list.19.Conv2d.weight
module_list.19.BatchNorm2d.weight
module_list.19.BatchNorm2d.bias
module_list.19.BatchNorm2d.running_mean
module_list.19.BatchNorm2d.running_var
module_list.19.BatchNorm2d.num_batches_tracked
module_list.20.Conv2d.weight
module_list.20.BatchNorm2d.weight
module_list.20.BatchNorm2d.bias
module_list.20.BatchNorm2d.running_mean
module_list.20.BatchNorm2d.running_var
module_list.20.BatchNorm2d.num_batches_tracked
module_list.22.Conv2d.weight
module_list.22.BatchNorm2d.weight
module_list.22.BatchNorm2d.bias
module_list.22.BatchNorm2d.running_mean
module_list.22.BatchNorm2d.running_var
module_list.22.BatchNorm2d.num_batches_tracked
module_list.23.Conv2d.weight
module_list.23.BatchNorm2d.weight
module_list.23.BatchNorm2d.bias
module_list.23.BatchNorm2d.running_mean
module_list.23.BatchNorm2d.running_var
module_list.23.BatchNorm2d.num_batches_tracked
module_list.25.Conv2d.weight
module_list.25.BatchNorm2d.weight
module_list.25.BatchNorm2d.bias
module_list.25.BatchNorm2d.running_mean
module_list.25.BatchNorm2d.running_var
module_list.25.BatchNorm2d.num_batches_tracked
module_list.26.Conv2d.weight
module_list.26.BatchNorm2d.weight
module_list.26.BatchNorm2d.bias
module_list.26.BatchNorm2d.running_mean
module_list.26.BatchNorm2d.running_var
module_list.26.BatchNorm2d.num_batches_tracked
module_list.28.Conv2d.weight
module_list.28.BatchNorm2d.weight
module_list.28.BatchNorm2d.bias
module_list.28.BatchNorm2d.running_mean
module_list.28.BatchNorm2d.running_var
module_list.28.BatchNorm2d.num_batches_tracked
module_list.29.Conv2d.weight
module_list.29.BatchNorm2d.weight
module_list.29.BatchNorm2d.bias
module_list.29.BatchNorm2d.running_mean
module_list.29.BatchNorm2d.running_var
module_list.29.BatchNorm2d.num_batches_tracked
module_list.31.Conv2d.weight
module_list.31.BatchNorm2d.weight
module_list.31.BatchNorm2d.bias
module_list.31.BatchNorm2d.running_mean
module_list.31.BatchNorm2d.running_var
module_list.31.BatchNorm2d.num_batches_tracked
module_list.32.Conv2d.weight
module_list.32.BatchNorm2d.weight
module_list.32.BatchNorm2d.bias
module_list.32.BatchNorm2d.running_mean
module_list.32.BatchNorm2d.running_var
module_list.32.BatchNorm2d.num_batches_tracked
module_list.34.Conv2d.weight
module_list.34.BatchNorm2d.weight
module_list.34.BatchNorm2d.bias
module_list.34.BatchNorm2d.running_mean
module_list.34.BatchNorm2d.running_var
module_list.34.BatchNorm2d.num_batches_tracked
module_list.35.Conv2d.weight
module_list.35.BatchNorm2d.weight
module_list.35.BatchNorm2d.bias
module_list.35.BatchNorm2d.running_mean
module_list.35.BatchNorm2d.running_var
module_list.35.BatchNorm2d.num_batches_tracked
module_list.37.Conv2d.weight
module_list.37.BatchNorm2d.weight
module_list.37.BatchNorm2d.bias
module_list.37.BatchNorm2d.running_mean
module_list.37.BatchNorm2d.running_var
module_list.37.BatchNorm2d.num_batches_tracked
module_list.38.Conv2d.weight
module_list.38.BatchNorm2d.weight
module_list.38.BatchNorm2d.bias
module_list.38.BatchNorm2d.running_mean
module_list.38.BatchNorm2d.running_var
module_list.38.BatchNorm2d.num_batches_tracked
module_list.39.Conv2d.weight
module_list.39.BatchNorm2d.weight
module_list.39.BatchNorm2d.bias
module_list.39.BatchNorm2d.running_mean
module_list.39.BatchNorm2d.running_var
module_list.39.BatchNorm2d.num_batches_tracked
module_list.41.Conv2d.weight
module_list.41.BatchNorm2d.weight
module_list.41.BatchNorm2d.bias
module_list.41.BatchNorm2d.running_mean
module_list.41.BatchNorm2d.running_var
module_list.41.BatchNorm2d.num_batches_tracked
module_list.42.Conv2d.weight
module_list.42.BatchNorm2d.weight
module_list.42.BatchNorm2d.bias
module_list.42.BatchNorm2d.running_mean
module_list.42.BatchNorm2d.running_var
module_list.42.BatchNorm2d.num_batches_tracked
module_list.44.Conv2d.weight
module_list.44.BatchNorm2d.weight
module_list.44.BatchNorm2d.bias
module_list.44.BatchNorm2d.running_mean
module_list.44.BatchNorm2d.running_var
module_list.44.BatchNorm2d.num_batches_tracked
module_list.45.Conv2d.weight
module_list.45.BatchNorm2d.weight
module_list.45.BatchNorm2d.bias
module_list.45.BatchNorm2d.running_mean
module_list.45.BatchNorm2d.running_var
module_list.45.BatchNorm2d.num_batches_tracked
module_list.47.Conv2d.weight
module_list.47.BatchNorm2d.weight
module_list.47.BatchNorm2d.bias
module_list.47.BatchNorm2d.running_mean
module_list.47.BatchNorm2d.running_var
module_list.47.BatchNorm2d.num_batches_tracked
module_list.48.Conv2d.weight
module_list.48.BatchNorm2d.weight
module_list.48.BatchNorm2d.bias
module_list.48.BatchNorm2d.running_mean
module_list.48.BatchNorm2d.running_var
module_list.48.BatchNorm2d.num_batches_tracked
module_list.50.Conv2d.weight
module_list.50.BatchNorm2d.weight
module_list.50.BatchNorm2d.bias
module_list.50.BatchNorm2d.running_mean
module_list.50.BatchNorm2d.running_var
module_list.50.BatchNorm2d.num_batches_tracked
module_list.51.Conv2d.weight
module_list.51.BatchNorm2d.weight
module_list.51.BatchNorm2d.bias
module_list.51.BatchNorm2d.running_mean
module_list.51.BatchNorm2d.running_var
module_list.51.BatchNorm2d.num_batches_tracked
module_list.53.Conv2d.weight
module_list.53.BatchNorm2d.weight
module_list.53.BatchNorm2d.bias
module_list.53.BatchNorm2d.running_mean
module_list.53.BatchNorm2d.running_var
module_list.53.BatchNorm2d.num_batches_tracked
module_list.54.Conv2d.weight
module_list.54.BatchNorm2d.weight
module_list.54.BatchNorm2d.bias
module_list.54.BatchNorm2d.running_mean
module_list.54.BatchNorm2d.running_var
module_list.54.BatchNorm2d.num_batches_tracked
module_list.56.Conv2d.weight
module_list.56.BatchNorm2d.weight
module_list.56.BatchNorm2d.bias
module_list.56.BatchNorm2d.running_mean
module_list.56.BatchNorm2d.running_var
module_list.56.BatchNorm2d.num_batches_tracked
module_list.57.Conv2d.weight
module_list.57.BatchNorm2d.weight
module_list.57.BatchNorm2d.bias
module_list.57.BatchNorm2d.running_mean
module_list.57.BatchNorm2d.running_var
module_list.57.BatchNorm2d.num_batches_tracked
module_list.59.Conv2d.weight
module_list.59.BatchNorm2d.weight
module_list.59.BatchNorm2d.bias
module_list.59.BatchNorm2d.running_mean
module_list.59.BatchNorm2d.running_var
module_list.59.BatchNorm2d.num_batches_tracked
module_list.60.Conv2d.weight
module_list.60.BatchNorm2d.weight
module_list.60.BatchNorm2d.bias
module_list.60.BatchNorm2d.running_mean
module_list.60.BatchNorm2d.running_var
module_list.60.BatchNorm2d.num_batches_tracked
module_list.62.Conv2d.weight
module_list.62.BatchNorm2d.weight
module_list.62.BatchNorm2d.bias
module_list.62.BatchNorm2d.running_mean
module_list.62.BatchNorm2d.running_var
module_list.62.BatchNorm2d.num_batches_tracked
module_list.63.Conv2d.weight
module_list.63.BatchNorm2d.weight
module_list.63.BatchNorm2d.bias
module_list.63.BatchNorm2d.running_mean
module_list.63.BatchNorm2d.running_var
module_list.63.BatchNorm2d.num_batches_tracked
module_list.64.Conv2d.weight
module_list.64.BatchNorm2d.weight
module_list.64.BatchNorm2d.bias
module_list.64.BatchNorm2d.running_mean
module_list.64.BatchNorm2d.running_var
module_list.64.BatchNorm2d.num_batches_tracked
module_list.66.Conv2d.weight
module_list.66.BatchNorm2d.weight
module_list.66.BatchNorm2d.bias
module_list.66.BatchNorm2d.running_mean
module_list.66.BatchNorm2d.running_var
module_list.66.BatchNorm2d.num_batches_tracked
module_list.67.Conv2d.weight
module_list.67.BatchNorm2d.weight
module_list.67.BatchNorm2d.bias
module_list.67.BatchNorm2d.running_mean
module_list.67.BatchNorm2d.running_var
module_list.67.BatchNorm2d.num_batches_tracked
module_list.69.Conv2d.weight
module_list.69.BatchNorm2d.weight
module_list.69.BatchNorm2d.bias
module_list.69.BatchNorm2d.running_mean
module_list.69.BatchNorm2d.running_var
module_list.69.BatchNorm2d.num_batches_tracked
module_list.70.Conv2d.weight
module_list.70.BatchNorm2d.weight
module_list.70.BatchNorm2d.bias
module_list.70.BatchNorm2d.running_mean
module_list.70.BatchNorm2d.running_var
module_list.70.BatchNorm2d.num_batches_tracked
module_list.72.Conv2d.weight
module_list.72.BatchNorm2d.weight
module_list.72.BatchNorm2d.bias
module_list.72.BatchNorm2d.running_mean
module_list.72.BatchNorm2d.running_var
module_list.72.BatchNorm2d.num_batches_tracked
module_list.73.Conv2d.weight
module_list.73.BatchNorm2d.weight
module_list.73.BatchNorm2d.bias
module_list.73.BatchNorm2d.running_mean
module_list.73.BatchNorm2d.running_var
module_list.73.BatchNorm2d.num_batches_tracked
module_list.75.Conv2d.weight
module_list.75.BatchNorm2d.weight
module_list.75.BatchNorm2d.bias
module_list.75.BatchNorm2d.running_mean
module_list.75.BatchNorm2d.running_var
module_list.75.BatchNorm2d.num_batches_tracked
module_list.76.Conv2d.weight
module_list.76.BatchNorm2d.weight
module_list.76.BatchNorm2d.bias
module_list.76.BatchNorm2d.running_mean
module_list.76.BatchNorm2d.running_var
module_list.76.BatchNorm2d.num_batches_tracked
module_list.77.Conv2d.weight
module_list.77.BatchNorm2d.weight
module_list.77.BatchNorm2d.bias
module_list.77.BatchNorm2d.running_mean
module_list.77.BatchNorm2d.running_var
module_list.77.BatchNorm2d.num_batches_tracked
module_list.84.Conv2d.weight
module_list.84.BatchNorm2d.weight
module_list.84.BatchNorm2d.bias
module_list.84.BatchNorm2d.running_mean
module_list.84.BatchNorm2d.running_var
module_list.84.BatchNorm2d.num_batches_tracked
module_list.85.Conv2d.weight
module_list.85.BatchNorm2d.weight
module_list.85.BatchNorm2d.bias
module_list.85.BatchNorm2d.running_mean
module_list.85.BatchNorm2d.running_var
module_list.85.BatchNorm2d.num_batches_tracked
module_list.86.Conv2d.weight
module_list.86.BatchNorm2d.weight
module_list.86.BatchNorm2d.bias
module_list.86.BatchNorm2d.running_mean
module_list.86.BatchNorm2d.running_var
module_list.86.BatchNorm2d.num_batches_tracked
module_list.87.Conv2d.weight
module_list.87.BatchNorm2d.weight
module_list.87.BatchNorm2d.bias
module_list.87.BatchNorm2d.running_mean
module_list.87.BatchNorm2d.running_var
module_list.87.BatchNorm2d.num_batches_tracked
module_list.88.Conv2d.weight
module_list.88.Conv2d.bias
module_list.91.Conv2d.weight
module_list.91.BatchNorm2d.weight
module_list.91.BatchNorm2d.bias
module_list.91.BatchNorm2d.running_mean
module_list.91.BatchNorm2d.running_var
module_list.91.BatchNorm2d.num_batches_tracked
module_list.94.Conv2d.weight
module_list.94.BatchNorm2d.weight
module_list.94.BatchNorm2d.bias
module_list.94.BatchNorm2d.running_mean
module_list.94.BatchNorm2d.running_var
module_list.94.BatchNorm2d.num_batches_tracked
module_list.95.Conv2d.weight
module_list.95.BatchNorm2d.weight
module_list.95.BatchNorm2d.bias
module_list.95.BatchNorm2d.running_mean
module_list.95.BatchNorm2d.running_var
module_list.95.BatchNorm2d.num_batches_tracked
module_list.96.Conv2d.weight
module_list.96.BatchNorm2d.weight
module_list.96.BatchNorm2d.bias
module_list.96.BatchNorm2d.running_mean
module_list.96.BatchNorm2d.running_var
module_list.96.BatchNorm2d.num_batches_tracked
module_list.97.Conv2d.weight
module_list.97.BatchNorm2d.weight
module_list.97.BatchNorm2d.bias
module_list.97.BatchNorm2d.running_mean
module_list.97.BatchNorm2d.running_var
module_list.97.BatchNorm2d.num_batches_tracked
module_list.98.Conv2d.weight
module_list.98.BatchNorm2d.weight
module_list.98.BatchNorm2d.bias
module_list.98.BatchNorm2d.running_mean
module_list.98.BatchNorm2d.running_var
module_list.98.BatchNorm2d.num_batches_tracked
module_list.99.Conv2d.weight
module_list.99.BatchNorm2d.weight
module_list.99.BatchNorm2d.bias
module_list.99.BatchNorm2d.running_mean
module_list.99.BatchNorm2d.running_var
module_list.99.BatchNorm2d.num_batches_tracked
module_list.100.Conv2d.weight
module_list.100.Conv2d.bias
module_list.103.Conv2d.weight
module_list.103.BatchNorm2d.weight
module_list.103.BatchNorm2d.bias
module_list.103.BatchNorm2d.running_mean
module_list.103.BatchNorm2d.running_var
module_list.103.BatchNorm2d.num_batches_tracked
module_list.106.Conv2d.weight
module_list.106.BatchNorm2d.weight
module_list.106.BatchNorm2d.bias
module_list.106.BatchNorm2d.running_mean
module_list.106.BatchNorm2d.running_var
module_list.106.BatchNorm2d.num_batches_tracked
module_list.107.Conv2d.weight
module_list.107.BatchNorm2d.weight
module_list.107.BatchNorm2d.bias
module_list.107.BatchNorm2d.running_mean
module_list.107.BatchNorm2d.running_var
module_list.107.BatchNorm2d.num_batches_tracked
module_list.108.Conv2d.weight
module_list.108.BatchNorm2d.weight
module_list.108.BatchNorm2d.bias
module_list.108.BatchNorm2d.running_mean
module_list.108.BatchNorm2d.running_var
module_list.108.BatchNorm2d.num_batches_tracked
module_list.109.Conv2d.weight
module_list.109.BatchNorm2d.weight
module_list.109.BatchNorm2d.bias
module_list.109.BatchNorm2d.running_mean
module_list.109.BatchNorm2d.running_var
module_list.109.BatchNorm2d.num_batches_tracked
module_list.110.Conv2d.weight
module_list.110.BatchNorm2d.weight
module_list.110.BatchNorm2d.bias
module_list.110.BatchNorm2d.running_mean
module_list.110.BatchNorm2d.running_var
module_list.110.BatchNorm2d.num_batches_tracked
module_list.111.Conv2d.weight
module_list.111.BatchNorm2d.weight
module_list.111.BatchNorm2d.bias
module_list.111.BatchNorm2d.running_mean
module_list.111.BatchNorm2d.running_var
module_list.111.BatchNorm2d.num_batches_tracked
module_list.112.Conv2d.weight
module_list.112.Conv2d.bias
```



# model.state_dict()

state_dict相当于一个字典

```
for name in model.state_dict():
	print(name)
打印名字

如果要参数：
for name,parameter in model.state_dict().items():
    print(parameter)

```



以yolov3-spp-voc为例

```
for name in model.state_dict():
	print(name)
```



```
module_list.0.Conv2d.weight
module_list.0.BatchNorm2d.weight
module_list.0.BatchNorm2d.bias
module_list.0.BatchNorm2d.running_mean
module_list.0.BatchNorm2d.running_var
module_list.0.BatchNorm2d.num_batches_tracked
module_list.1.Conv2d.weight
module_list.1.BatchNorm2d.weight
module_list.1.BatchNorm2d.bias
module_list.1.BatchNorm2d.running_mean
module_list.1.BatchNorm2d.running_var
module_list.1.BatchNorm2d.num_batches_tracked
module_list.2.Conv2d.weight
module_list.2.BatchNorm2d.weight
module_list.2.BatchNorm2d.bias
module_list.2.BatchNorm2d.running_mean
module_list.2.BatchNorm2d.running_var
module_list.2.BatchNorm2d.num_batches_tracked
module_list.3.Conv2d.weight
module_list.3.BatchNorm2d.weight
module_list.3.BatchNorm2d.bias
module_list.3.BatchNorm2d.running_mean
module_list.3.BatchNorm2d.running_var
module_list.3.BatchNorm2d.num_batches_tracked
module_list.5.Conv2d.weight
module_list.5.BatchNorm2d.weight
module_list.5.BatchNorm2d.bias
module_list.5.BatchNorm2d.running_mean
module_list.5.BatchNorm2d.running_var
module_list.5.BatchNorm2d.num_batches_tracked
module_list.6.Conv2d.weight
module_list.6.BatchNorm2d.weight
module_list.6.BatchNorm2d.bias
module_list.6.BatchNorm2d.running_mean
module_list.6.BatchNorm2d.running_var
module_list.6.BatchNorm2d.num_batches_tracked
module_list.7.Conv2d.weight
module_list.7.BatchNorm2d.weight
module_list.7.BatchNorm2d.bias
module_list.7.BatchNorm2d.running_mean
module_list.7.BatchNorm2d.running_var
module_list.7.BatchNorm2d.num_batches_tracked
module_list.9.Conv2d.weight
module_list.9.BatchNorm2d.weight
module_list.9.BatchNorm2d.bias
module_list.9.BatchNorm2d.running_mean
module_list.9.BatchNorm2d.running_var
module_list.9.BatchNorm2d.num_batches_tracked
module_list.10.Conv2d.weight
module_list.10.BatchNorm2d.weight
module_list.10.BatchNorm2d.bias
module_list.10.BatchNorm2d.running_mean
module_list.10.BatchNorm2d.running_var
module_list.10.BatchNorm2d.num_batches_tracked
module_list.12.Conv2d.weight
module_list.12.BatchNorm2d.weight
module_list.12.BatchNorm2d.bias
module_list.12.BatchNorm2d.running_mean
module_list.12.BatchNorm2d.running_var
module_list.12.BatchNorm2d.num_batches_tracked
module_list.13.Conv2d.weight
module_list.13.BatchNorm2d.weight
module_list.13.BatchNorm2d.bias
module_list.13.BatchNorm2d.running_mean
module_list.13.BatchNorm2d.running_var
module_list.13.BatchNorm2d.num_batches_tracked
module_list.14.Conv2d.weight
module_list.14.BatchNorm2d.weight
module_list.14.BatchNorm2d.bias
module_list.14.BatchNorm2d.running_mean
module_list.14.BatchNorm2d.running_var
module_list.14.BatchNorm2d.num_batches_tracked
module_list.16.Conv2d.weight
module_list.16.BatchNorm2d.weight
module_list.16.BatchNorm2d.bias
module_list.16.BatchNorm2d.running_mean
module_list.16.BatchNorm2d.running_var
module_list.16.BatchNorm2d.num_batches_tracked
module_list.17.Conv2d.weight
module_list.17.BatchNorm2d.weight
module_list.17.BatchNorm2d.bias
module_list.17.BatchNorm2d.running_mean
module_list.17.BatchNorm2d.running_var
module_list.17.BatchNorm2d.num_batches_tracked
module_list.19.Conv2d.weight
module_list.19.BatchNorm2d.weight
module_list.19.BatchNorm2d.bias
module_list.19.BatchNorm2d.running_mean
module_list.19.BatchNorm2d.running_var
module_list.19.BatchNorm2d.num_batches_tracked
module_list.20.Conv2d.weight
module_list.20.BatchNorm2d.weight
module_list.20.BatchNorm2d.bias
module_list.20.BatchNorm2d.running_mean
module_list.20.BatchNorm2d.running_var
module_list.20.BatchNorm2d.num_batches_tracked
module_list.22.Conv2d.weight
module_list.22.BatchNorm2d.weight
module_list.22.BatchNorm2d.bias
module_list.22.BatchNorm2d.running_mean
module_list.22.BatchNorm2d.running_var
module_list.22.BatchNorm2d.num_batches_tracked
module_list.23.Conv2d.weight
module_list.23.BatchNorm2d.weight
module_list.23.BatchNorm2d.bias
module_list.23.BatchNorm2d.running_mean
module_list.23.BatchNorm2d.running_var
module_list.23.BatchNorm2d.num_batches_tracked
module_list.25.Conv2d.weight
module_list.25.BatchNorm2d.weight
module_list.25.BatchNorm2d.bias
module_list.25.BatchNorm2d.running_mean
module_list.25.BatchNorm2d.running_var
module_list.25.BatchNorm2d.num_batches_tracked
module_list.26.Conv2d.weight
module_list.26.BatchNorm2d.weight
module_list.26.BatchNorm2d.bias
module_list.26.BatchNorm2d.running_mean
module_list.26.BatchNorm2d.running_var
module_list.26.BatchNorm2d.num_batches_tracked
module_list.28.Conv2d.weight
module_list.28.BatchNorm2d.weight
module_list.28.BatchNorm2d.bias
module_list.28.BatchNorm2d.running_mean
module_list.28.BatchNorm2d.running_var
module_list.28.BatchNorm2d.num_batches_tracked
module_list.29.Conv2d.weight
module_list.29.BatchNorm2d.weight
module_list.29.BatchNorm2d.bias
module_list.29.BatchNorm2d.running_mean
module_list.29.BatchNorm2d.running_var
module_list.29.BatchNorm2d.num_batches_tracked
module_list.31.Conv2d.weight
module_list.31.BatchNorm2d.weight
module_list.31.BatchNorm2d.bias
module_list.31.BatchNorm2d.running_mean
module_list.31.BatchNorm2d.running_var
module_list.31.BatchNorm2d.num_batches_tracked
module_list.32.Conv2d.weight
module_list.32.BatchNorm2d.weight
module_list.32.BatchNorm2d.bias
module_list.32.BatchNorm2d.running_mean
module_list.32.BatchNorm2d.running_var
module_list.32.BatchNorm2d.num_batches_tracked
module_list.34.Conv2d.weight
module_list.34.BatchNorm2d.weight
module_list.34.BatchNorm2d.bias
module_list.34.BatchNorm2d.running_mean
module_list.34.BatchNorm2d.running_var
module_list.34.BatchNorm2d.num_batches_tracked
module_list.35.Conv2d.weight
module_list.35.BatchNorm2d.weight
module_list.35.BatchNorm2d.bias
module_list.35.BatchNorm2d.running_mean
module_list.35.BatchNorm2d.running_var
module_list.35.BatchNorm2d.num_batches_tracked
module_list.37.Conv2d.weight
module_list.37.BatchNorm2d.weight
module_list.37.BatchNorm2d.bias
module_list.37.BatchNorm2d.running_mean
module_list.37.BatchNorm2d.running_var
module_list.37.BatchNorm2d.num_batches_tracked
module_list.38.Conv2d.weight
module_list.38.BatchNorm2d.weight
module_list.38.BatchNorm2d.bias
module_list.38.BatchNorm2d.running_mean
module_list.38.BatchNorm2d.running_var
module_list.38.BatchNorm2d.num_batches_tracked
module_list.39.Conv2d.weight
module_list.39.BatchNorm2d.weight
module_list.39.BatchNorm2d.bias
module_list.39.BatchNorm2d.running_mean
module_list.39.BatchNorm2d.running_var
module_list.39.BatchNorm2d.num_batches_tracked
module_list.41.Conv2d.weight
module_list.41.BatchNorm2d.weight
module_list.41.BatchNorm2d.bias
module_list.41.BatchNorm2d.running_mean
module_list.41.BatchNorm2d.running_var
module_list.41.BatchNorm2d.num_batches_tracked
module_list.42.Conv2d.weight
module_list.42.BatchNorm2d.weight
module_list.42.BatchNorm2d.bias
module_list.42.BatchNorm2d.running_mean
module_list.42.BatchNorm2d.running_var
module_list.42.BatchNorm2d.num_batches_tracked
module_list.44.Conv2d.weight
module_list.44.BatchNorm2d.weight
module_list.44.BatchNorm2d.bias
module_list.44.BatchNorm2d.running_mean
module_list.44.BatchNorm2d.running_var
module_list.44.BatchNorm2d.num_batches_tracked
module_list.45.Conv2d.weight
module_list.45.BatchNorm2d.weight
module_list.45.BatchNorm2d.bias
module_list.45.BatchNorm2d.running_mean
module_list.45.BatchNorm2d.running_var
module_list.45.BatchNorm2d.num_batches_tracked
module_list.47.Conv2d.weight
module_list.47.BatchNorm2d.weight
module_list.47.BatchNorm2d.bias
module_list.47.BatchNorm2d.running_mean
module_list.47.BatchNorm2d.running_var
module_list.47.BatchNorm2d.num_batches_tracked
module_list.48.Conv2d.weight
module_list.48.BatchNorm2d.weight
module_list.48.BatchNorm2d.bias
module_list.48.BatchNorm2d.running_mean
module_list.48.BatchNorm2d.running_var
module_list.48.BatchNorm2d.num_batches_tracked
module_list.50.Conv2d.weight
module_list.50.BatchNorm2d.weight
module_list.50.BatchNorm2d.bias
module_list.50.BatchNorm2d.running_mean
module_list.50.BatchNorm2d.running_var
module_list.50.BatchNorm2d.num_batches_tracked
module_list.51.Conv2d.weight
module_list.51.BatchNorm2d.weight
module_list.51.BatchNorm2d.bias
module_list.51.BatchNorm2d.running_mean
module_list.51.BatchNorm2d.running_var
module_list.51.BatchNorm2d.num_batches_tracked
module_list.53.Conv2d.weight
module_list.53.BatchNorm2d.weight
module_list.53.BatchNorm2d.bias
module_list.53.BatchNorm2d.running_mean
module_list.53.BatchNorm2d.running_var
module_list.53.BatchNorm2d.num_batches_tracked
module_list.54.Conv2d.weight
module_list.54.BatchNorm2d.weight
module_list.54.BatchNorm2d.bias
module_list.54.BatchNorm2d.running_mean
module_list.54.BatchNorm2d.running_var
module_list.54.BatchNorm2d.num_batches_tracked
module_list.56.Conv2d.weight
module_list.56.BatchNorm2d.weight
module_list.56.BatchNorm2d.bias
module_list.56.BatchNorm2d.running_mean
module_list.56.BatchNorm2d.running_var
module_list.56.BatchNorm2d.num_batches_tracked
module_list.57.Conv2d.weight
module_list.57.BatchNorm2d.weight
module_list.57.BatchNorm2d.bias
module_list.57.BatchNorm2d.running_mean
module_list.57.BatchNorm2d.running_var
module_list.57.BatchNorm2d.num_batches_tracked
module_list.59.Conv2d.weight
module_list.59.BatchNorm2d.weight
module_list.59.BatchNorm2d.bias
module_list.59.BatchNorm2d.running_mean
module_list.59.BatchNorm2d.running_var
module_list.59.BatchNorm2d.num_batches_tracked
module_list.60.Conv2d.weight
module_list.60.BatchNorm2d.weight
module_list.60.BatchNorm2d.bias
module_list.60.BatchNorm2d.running_mean
module_list.60.BatchNorm2d.running_var
module_list.60.BatchNorm2d.num_batches_tracked
module_list.62.Conv2d.weight
module_list.62.BatchNorm2d.weight
module_list.62.BatchNorm2d.bias
module_list.62.BatchNorm2d.running_mean
module_list.62.BatchNorm2d.running_var
module_list.62.BatchNorm2d.num_batches_tracked
module_list.63.Conv2d.weight
module_list.63.BatchNorm2d.weight
module_list.63.BatchNorm2d.bias
module_list.63.BatchNorm2d.running_mean
module_list.63.BatchNorm2d.running_var
module_list.63.BatchNorm2d.num_batches_tracked
module_list.64.Conv2d.weight
module_list.64.BatchNorm2d.weight
module_list.64.BatchNorm2d.bias
module_list.64.BatchNorm2d.running_mean
module_list.64.BatchNorm2d.running_var
module_list.64.BatchNorm2d.num_batches_tracked
module_list.66.Conv2d.weight
module_list.66.BatchNorm2d.weight
module_list.66.BatchNorm2d.bias
module_list.66.BatchNorm2d.running_mean
module_list.66.BatchNorm2d.running_var
module_list.66.BatchNorm2d.num_batches_tracked
module_list.67.Conv2d.weight
module_list.67.BatchNorm2d.weight
module_list.67.BatchNorm2d.bias
module_list.67.BatchNorm2d.running_mean
module_list.67.BatchNorm2d.running_var
module_list.67.BatchNorm2d.num_batches_tracked
module_list.69.Conv2d.weight
module_list.69.BatchNorm2d.weight
module_list.69.BatchNorm2d.bias
module_list.69.BatchNorm2d.running_mean
module_list.69.BatchNorm2d.running_var
module_list.69.BatchNorm2d.num_batches_tracked
module_list.70.Conv2d.weight
module_list.70.BatchNorm2d.weight
module_list.70.BatchNorm2d.bias
module_list.70.BatchNorm2d.running_mean
module_list.70.BatchNorm2d.running_var
module_list.70.BatchNorm2d.num_batches_tracked
module_list.72.Conv2d.weight
module_list.72.BatchNorm2d.weight
module_list.72.BatchNorm2d.bias
module_list.72.BatchNorm2d.running_mean
module_list.72.BatchNorm2d.running_var
module_list.72.BatchNorm2d.num_batches_tracked
module_list.73.Conv2d.weight
module_list.73.BatchNorm2d.weight
module_list.73.BatchNorm2d.bias
module_list.73.BatchNorm2d.running_mean
module_list.73.BatchNorm2d.running_var
module_list.73.BatchNorm2d.num_batches_tracked
module_list.75.Conv2d.weight
module_list.75.BatchNorm2d.weight
module_list.75.BatchNorm2d.bias
module_list.75.BatchNorm2d.running_mean
module_list.75.BatchNorm2d.running_var
module_list.75.BatchNorm2d.num_batches_tracked
module_list.76.Conv2d.weight
module_list.76.BatchNorm2d.weight
module_list.76.BatchNorm2d.bias
module_list.76.BatchNorm2d.running_mean
module_list.76.BatchNorm2d.running_var
module_list.76.BatchNorm2d.num_batches_tracked
module_list.77.Conv2d.weight
module_list.77.BatchNorm2d.weight
module_list.77.BatchNorm2d.bias
module_list.77.BatchNorm2d.running_mean
module_list.77.BatchNorm2d.running_var
module_list.77.BatchNorm2d.num_batches_tracked
module_list.84.Conv2d.weight
module_list.84.BatchNorm2d.weight
module_list.84.BatchNorm2d.bias
module_list.84.BatchNorm2d.running_mean
module_list.84.BatchNorm2d.running_var
module_list.84.BatchNorm2d.num_batches_tracked
module_list.85.Conv2d.weight
module_list.85.BatchNorm2d.weight
module_list.85.BatchNorm2d.bias
module_list.85.BatchNorm2d.running_mean
module_list.85.BatchNorm2d.running_var
module_list.85.BatchNorm2d.num_batches_tracked
module_list.86.Conv2d.weight
module_list.86.BatchNorm2d.weight
module_list.86.BatchNorm2d.bias
module_list.86.BatchNorm2d.running_mean
module_list.86.BatchNorm2d.running_var
module_list.86.BatchNorm2d.num_batches_tracked
module_list.87.Conv2d.weight
module_list.87.BatchNorm2d.weight
module_list.87.BatchNorm2d.bias
module_list.87.BatchNorm2d.running_mean
module_list.87.BatchNorm2d.running_var
module_list.87.BatchNorm2d.num_batches_tracked
module_list.88.Conv2d.weight
module_list.88.Conv2d.bias
module_list.91.Conv2d.weight
module_list.91.BatchNorm2d.weight
module_list.91.BatchNorm2d.bias
module_list.91.BatchNorm2d.running_mean
module_list.91.BatchNorm2d.running_var
module_list.91.BatchNorm2d.num_batches_tracked
module_list.94.Conv2d.weight
module_list.94.BatchNorm2d.weight
module_list.94.BatchNorm2d.bias
module_list.94.BatchNorm2d.running_mean
module_list.94.BatchNorm2d.running_var
module_list.94.BatchNorm2d.num_batches_tracked
module_list.95.Conv2d.weight
module_list.95.BatchNorm2d.weight
module_list.95.BatchNorm2d.bias
module_list.95.BatchNorm2d.running_mean
module_list.95.BatchNorm2d.running_var
module_list.95.BatchNorm2d.num_batches_tracked
module_list.96.Conv2d.weight
module_list.96.BatchNorm2d.weight
module_list.96.BatchNorm2d.bias
module_list.96.BatchNorm2d.running_mean
module_list.96.BatchNorm2d.running_var
module_list.96.BatchNorm2d.num_batches_tracked
module_list.97.Conv2d.weight
module_list.97.BatchNorm2d.weight
module_list.97.BatchNorm2d.bias
module_list.97.BatchNorm2d.running_mean
module_list.97.BatchNorm2d.running_var
module_list.97.BatchNorm2d.num_batches_tracked
module_list.98.Conv2d.weight
module_list.98.BatchNorm2d.weight
module_list.98.BatchNorm2d.bias
module_list.98.BatchNorm2d.running_mean
module_list.98.BatchNorm2d.running_var
module_list.98.BatchNorm2d.num_batches_tracked
module_list.99.Conv2d.weight
module_list.99.BatchNorm2d.weight
module_list.99.BatchNorm2d.bias
module_list.99.BatchNorm2d.running_mean
module_list.99.BatchNorm2d.running_var
module_list.99.BatchNorm2d.num_batches_tracked
module_list.100.Conv2d.weight
module_list.100.Conv2d.bias
module_list.103.Conv2d.weight
module_list.103.BatchNorm2d.weight
module_list.103.BatchNorm2d.bias
module_list.103.BatchNorm2d.running_mean
module_list.103.BatchNorm2d.running_var
module_list.103.BatchNorm2d.num_batches_tracked
module_list.106.Conv2d.weight
module_list.106.BatchNorm2d.weight
module_list.106.BatchNorm2d.bias
module_list.106.BatchNorm2d.running_mean
module_list.106.BatchNorm2d.running_var
module_list.106.BatchNorm2d.num_batches_tracked
module_list.107.Conv2d.weight
module_list.107.BatchNorm2d.weight
module_list.107.BatchNorm2d.bias
module_list.107.BatchNorm2d.running_mean
module_list.107.BatchNorm2d.running_var
module_list.107.BatchNorm2d.num_batches_tracked
module_list.108.Conv2d.weight
module_list.108.BatchNorm2d.weight
module_list.108.BatchNorm2d.bias
module_list.108.BatchNorm2d.running_mean
module_list.108.BatchNorm2d.running_var
module_list.108.BatchNorm2d.num_batches_tracked
module_list.109.Conv2d.weight
module_list.109.BatchNorm2d.weight
module_list.109.BatchNorm2d.bias
module_list.109.BatchNorm2d.running_mean
module_list.109.BatchNorm2d.running_var
module_list.109.BatchNorm2d.num_batches_tracked
module_list.110.Conv2d.weight
module_list.110.BatchNorm2d.weight
module_list.110.BatchNorm2d.bias
module_list.110.BatchNorm2d.running_mean
module_list.110.BatchNorm2d.running_var
module_list.110.BatchNorm2d.num_batches_tracked
module_list.111.Conv2d.weight
module_list.111.BatchNorm2d.weight
module_list.111.BatchNorm2d.bias
module_list.111.BatchNorm2d.running_mean
module_list.111.BatchNorm2d.running_var
module_list.111.BatchNorm2d.num_batches_tracked
module_list.112.Conv2d.weight
module_list.112.Conv2d.bias
```



# model.load_state_dict(ckpt['model'], strict=False)

如果不添加参数strict=False，而model中有ckpt['model']没有的参数，会触发报错 。

加上strict=False，就是ckpt['model']有多少，就向model加载多少。



在上面的示例中，model.state_dict和ckpt['model'] 是完全对应的，所以在此项目中，即使是不添加strict=False，也不影响





# optimizer加载参数

```
optimizer.load_state_dict(ckpt['optimizer'])
```

查看ckpt['optimizer'] 内容

ckpt['optimizer']本身是一个字典



```
for k,v in ckpt['optimizer'].items():
	for x in v:
		print(k,x)

```

k有两类 state 与 param_groups

state:

```
state 0
state 1
state 2
state 3
state 4
state 5
state 6
state 7
state 8
state 9
state 10
state 11
state 12
state 13
state 14
state 15
state 16
state 17
state 18
state 19
state 20
state 21
state 22
state 23
state 24
state 25
state 26
state 27
state 28
state 29
state 30
state 31
state 32
state 33
state 34
state 35
state 36
state 37
state 38
state 39
state 40
state 41
state 42
state 43
state 44
state 45
state 46
state 47
state 48
state 49
state 50
state 51
state 52
state 53
state 54
state 55
state 56
state 57
state 58
state 59
state 60
state 61
state 62
state 63
state 64
state 65
state 66
state 67
state 68
state 69
state 70
state 71
state 72
state 73
state 74
state 75
state 76
state 77
state 78
state 79
state 80
state 81
state 82
state 83
state 84
state 85
state 86
state 87
state 88
state 89
state 90
state 91
state 92
state 93
state 94
state 95
state 96
state 97
state 98
state 99
state 100
state 101
state 102
state 103
state 104
state 105
state 106
state 107
state 108
state 109
state 110
state 111
state 112
state 113
state 114
state 115
state 116
state 117
state 118
state 119
state 120
state 121
state 122
state 123
state 124
state 125
state 126
state 127
state 128
state 129
state 130
state 131
state 132
state 133
state 134
state 135
state 136
state 137
state 138
state 139
state 140
state 141
state 142
state 143
state 144
state 145
state 146
state 147
state 148
state 149
state 150
state 151
state 152
state 153
state 154
state 155
state 156
state 157
state 158
state 159
state 160
state 161
state 162
state 163
state 164
state 165
state 166
state 167
state 168
state 169
state 170
state 171
state 172
state 173
state 174
state 175
state 176
state 177
state 178
state 179
state 180
state 181
state 182
state 183
state 184
state 185
state 186
state 187
state 188
state 189
state 190
state 191
state 192
state 193
state 194
state 195
state 196
state 197
state 198
state 199
state 200
state 201
state 202
state 203
state 204
state 205
state 206
state 207
state 208
state 209
state 210
state 211
state 212
state 213
state 214
state 215
state 216
state 217
state 218
state 219
state 220
state 221
state 222
state 223
state 224
```



```
param_groups {'lr': 0.009999739554486183, 'momentum': 0.9246547504025765, 'dampening': 0, 'weight_decay': 0.0, 'nesterov': True, 'initial_lr': 0.01, 'params': [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 70, 71, 72]}
param_groups {'weight_decay': 0.0003331723027375201, 'lr': 0.009999739554486183, 'momentum': 0.9246547504025765, 'dampening': 0, 'nesterov': True, 'initial_lr': 0.01, 'params': [73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 84, 85, 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100, 101, 102, 103, 104, 105, 106, 107, 108, 109, 110, 111, 112, 113, 114, 115, 116, 117, 118, 119, 120, 121, 122, 123, 124, 125, 126, 127, 128, 129, 130, 131, 132, 133, 134, 135, 136, 137, 138, 139, 140, 141, 142, 143, 144, 145, 146, 147, 148]}
param_groups {'lr': 0.009999739554486183, 'momentum': 0.9246547504025765, 'dampening': 0, 'weight_decay': 0.0, 'nesterov': True, 'initial_lr': 0.01, 'params': [149, 150, 151, 152, 153, 154, 155, 156, 157, 158, 159, 160, 161, 162, 163, 164, 165, 166, 167, 168, 169, 170, 171, 172, 173, 174, 175, 176, 177, 178, 179, 180, 181, 182, 183, 184, 185, 186, 187, 188, 189, 190, 191, 192, 193, 194, 195, 196, 197, 198, 199, 200, 201, 202, 203, 204, 205, 206, 207, 208, 209, 210, 211, 212, 213, 214, 215, 216, 217, 218, 219, 220, 221, 222, 223, 224]}
```

# ckpt['']与ckpt.get('')

效果相同

如

```
ckpt['optimizer']
ckpt.get['optimizer']
```

























model.module_defs      是一个list

```
[{'type': 'convolutional', 'batch_normalize': 1, 'filters': 32, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 64, 'size': 3, 'stride': 2, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 32, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 64, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 3, 'stride': 2, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 64, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 64, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 3, 'stride': 2, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 3, 'stride': 2, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 1024, 'size': 3, 'stride': 2, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 1024, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 1024, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 1024, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 1024, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'size': 3, 'stride': 1, 'pad': 1, 'filters': 1024, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'maxpool', 'stride': 1, 'size': 5}, {'type': 'route', 'layers': [-2]}, {'type': 'maxpool', 'stride': 1, 'size': 9}, {'type': 'route', 'layers': [-4]}, {'type': 'maxpool', 'stride': 1, 'size': 13}, {'type': 'route', 'layers': [-1, -3, -5, -6]}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'size': 3, 'stride': 1, 'pad': 1, 'filters': 1024, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'size': 3, 'stride': 1, 'pad': 1, 'filters': 1024, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 0, 'size': 1, 'stride': 1, 'pad': 1, 'filters': 75, 'activation': 'linear'}, {'type': 'yolo', 'mask': [6, 7, 8], 'anchors': array([[         10,          13],
       [         16,          30],
       [         33,          23],
       [         30,          61],
       [         62,          45],
       [         59,         119],
       [        116,          90],
       [        156,         198],
       [        373,         326]]), 'classes': 20, 'num': 9, 'jitter': '.3', 'ignore_thresh': '.7', 'truth_thresh': 1, 'random': 1}, {'type': 'route', 'layers': [-4]}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'upsample', 'stride': 2}, {'type': 'route', 'layers': [-1, 61]}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'size': 3, 'stride': 1, 'pad': 1, 'filters': 512, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'size': 3, 'stride': 1, 'pad': 1, 'filters': 512, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'size': 3, 'stride': 1, 'pad': 1, 'filters': 512, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 0, 'size': 1, 'stride': 1, 'pad': 1, 'filters': 75, 'activation': 'linear'}, {'type': 'yolo', 'mask': [3, 4, 5], 'anchors': array([[         10,          13],
       [         16,          30],
       [         33,          23],
       [         30,          61],
       [         62,          45],
       [         59,         119],
       [        116,          90],
       [        156,         198],
       [        373,         326]]), 'classes': 20, 'num': 9, 'jitter': '.3', 'ignore_thresh': '.7', 'truth_thresh': 1, 'random': 1}, {'type': 'route', 'layers': [-4]}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'upsample', 'stride': 2}, {'type': 'route', 'layers': [-1, 36]}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'size': 3, 'stride': 1, 'pad': 1, 'filters': 256, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'size': 3, 'stride': 1, 'pad': 1, 'filters': 256, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'size': 3, 'stride': 1, 'pad': 1, 'filters': 256, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 0, 'size': 1, 'stride': 1, 'pad': 1, 'filters': 75, 'activation': 'linear'}, {'type': 'yolo', 'mask': [0, 1, 2], 'anchors': array([[         10,          13],
       [         16,          30],
       [         33,          23],
       [         30,          61],
       [         62,          45],
       [         59,         119],
       [        116,          90],
       [        156,         198],
       [        373,         326]]), 'classes': 20, 'num': 9, 'jitter': '.3', 'ignore_thresh': '.7', 'truth_thresh': 1, 'random': 1}]
[{'type': 'convolutional', 'batch_normalize': 1, 'filters': 32, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 64, 'size': 3, 'stride': 2, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 32, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 64, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 3, 'stride': 2, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 64, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 64, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 3, 'stride': 2, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 3, 'stride': 2, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 1024, 'size': 3, 'stride': 2, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 1024, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 1024, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 1024, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 1024, 'size': 3, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'shortcut', 'from': [-3], 'activation': 'linear'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'size': 3, 'stride': 1, 'pad': 1, 'filters': 1024, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'maxpool', 'stride': 1, 'size': 5}, {'type': 'route', 'layers': [-2]}, {'type': 'maxpool', 'stride': 1, 'size': 9}, {'type': 'route', 'layers': [-4]}, {'type': 'maxpool', 'stride': 1, 'size': 13}, {'type': 'route', 'layers': [-1, -3, -5, -6]}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'size': 3, 'stride': 1, 'pad': 1, 'filters': 1024, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 512, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'size': 3, 'stride': 1, 'pad': 1, 'filters': 1024, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 0, 'size': 1, 'stride': 1, 'pad': 1, 'filters': 75, 'activation': 'linear'}, {'type': 'yolo', 'mask': [6, 7, 8], 'anchors': array([[         10,          13],
       [         16,          30],
       [         33,          23],
       [         30,          61],
       [         62,          45],
       [         59,         119],
       [        116,          90],
       [        156,         198],
       [        373,         326]]), 'classes': 20, 'num': 9, 'jitter': '.3', 'ignore_thresh': '.7', 'truth_thresh': 1, 'random': 1}, {'type': 'route', 'layers': [-4]}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'upsample', 'stride': 2}, {'type': 'route', 'layers': [-1, 61]}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'size': 3, 'stride': 1, 'pad': 1, 'filters': 512, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'size': 3, 'stride': 1, 'pad': 1, 'filters': 512, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 256, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'size': 3, 'stride': 1, 'pad': 1, 'filters': 512, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 0, 'size': 1, 'stride': 1, 'pad': 1, 'filters': 75, 'activation': 'linear'}, {'type': 'yolo', 'mask': [3, 4, 5], 'anchors': array([[         10,          13],
       [         16,          30],
       [         33,          23],
       [         30,          61],
       [         62,          45],
       [         59,         119],
       [        116,          90],
       [        156,         198],
       [        373,         326]]), 'classes': 20, 'num': 9, 'jitter': '.3', 'ignore_thresh': '.7', 'truth_thresh': 1, 'random': 1}, {'type': 'route', 'layers': [-4]}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'upsample', 'stride': 2}, {'type': 'route', 'layers': [-1, 36]}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'size': 3, 'stride': 1, 'pad': 1, 'filters': 256, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'size': 3, 'stride': 1, 'pad': 1, 'filters': 256, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'filters': 128, 'size': 1, 'stride': 1, 'pad': 1, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 1, 'size': 3, 'stride': 1, 'pad': 1, 'filters': 256, 'activation': 'leaky'}, {'type': 'convolutional', 'batch_normalize': 0, 'size': 1, 'stride': 1, 'pad': 1, 'filters': 75, 'activation': 'linear'}, {'type': 'yolo', 'mask': [0, 1, 2], 'anchors': array([[         10,          13],
       [         16,          30],
       [         33,          23],
       [         30,          61],
       [         62,          45],
       [         59,         119],
       [        116,          90],
       [        156,         198],
       [        373,         326]]), 'classes': 20, 'num': 9, 'jitter': '.3', 'ignore_thresh': '.7', 'truth_thresh': 1, 'random': 1}]

```







**model.module_list**       可以像list一样读取    model.module_list [0]

```
ModuleList(
  (0): Sequential(
    (Conv2d): Conv2d(3, 32, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(32, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (1): Sequential(
    (Conv2d): Conv2d(32, 64, kernel_size=(3, 3), stride=(2, 2), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(64, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (2): Sequential(
    (Conv2d): Conv2d(64, 32, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(32, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (3): Sequential(
    (Conv2d): Conv2d(32, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(64, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (4): WeightedFeatureFusion()
  (5): Sequential(
    (Conv2d): Conv2d(64, 128, kernel_size=(3, 3), stride=(2, 2), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(128, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (6): Sequential(
    (Conv2d): Conv2d(128, 64, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(64, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (7): Sequential(
    (Conv2d): Conv2d(64, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(128, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (8): WeightedFeatureFusion()
  (9): Sequential(
    (Conv2d): Conv2d(128, 64, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(64, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (10): Sequential(
    (Conv2d): Conv2d(64, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(128, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (11): WeightedFeatureFusion()
  (12): Sequential(
    (Conv2d): Conv2d(128, 256, kernel_size=(3, 3), stride=(2, 2), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(256, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (13): Sequential(
    (Conv2d): Conv2d(256, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(128, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (14): Sequential(
    (Conv2d): Conv2d(128, 256, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(256, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (15): WeightedFeatureFusion()
  (16): Sequential(
    (Conv2d): Conv2d(256, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(128, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (17): Sequential(
    (Conv2d): Conv2d(128, 256, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(256, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (18): WeightedFeatureFusion()
  (19): Sequential(
    (Conv2d): Conv2d(256, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(128, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (20): Sequential(
    (Conv2d): Conv2d(128, 256, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(256, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (21): WeightedFeatureFusion()
  (22): Sequential(
    (Conv2d): Conv2d(256, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(128, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (23): Sequential(
    (Conv2d): Conv2d(128, 256, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(256, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (24): WeightedFeatureFusion()
  (25): Sequential(
    (Conv2d): Conv2d(256, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(128, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (26): Sequential(
    (Conv2d): Conv2d(128, 256, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(256, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (27): WeightedFeatureFusion()
  (28): Sequential(
    (Conv2d): Conv2d(256, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(128, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (29): Sequential(
    (Conv2d): Conv2d(128, 256, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(256, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (30): WeightedFeatureFusion()
  (31): Sequential(
    (Conv2d): Conv2d(256, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(128, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (32): Sequential(
    (Conv2d): Conv2d(128, 256, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(256, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (33): WeightedFeatureFusion()
  (34): Sequential(
    (Conv2d): Conv2d(256, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(128, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (35): Sequential(
    (Conv2d): Conv2d(128, 256, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(256, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (36): WeightedFeatureFusion()
  (37): Sequential(
    (Conv2d): Conv2d(256, 512, kernel_size=(3, 3), stride=(2, 2), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(512, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (38): Sequential(
    (Conv2d): Conv2d(512, 256, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(256, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (39): Sequential(
    (Conv2d): Conv2d(256, 512, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(512, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (40): WeightedFeatureFusion()
  (41): Sequential(
    (Conv2d): Conv2d(512, 256, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(256, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (42): Sequential(
    (Conv2d): Conv2d(256, 512, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(512, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (43): WeightedFeatureFusion()
  (44): Sequential(
    (Conv2d): Conv2d(512, 256, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(256, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (45): Sequential(
    (Conv2d): Conv2d(256, 512, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(512, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (46): WeightedFeatureFusion()
  (47): Sequential(
    (Conv2d): Conv2d(512, 256, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(256, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (48): Sequential(
    (Conv2d): Conv2d(256, 512, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(512, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (49): WeightedFeatureFusion()
  (50): Sequential(
    (Conv2d): Conv2d(512, 256, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(256, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (51): Sequential(
    (Conv2d): Conv2d(256, 512, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(512, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (52): WeightedFeatureFusion()
  (53): Sequential(
    (Conv2d): Conv2d(512, 256, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(256, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (54): Sequential(
    (Conv2d): Conv2d(256, 512, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(512, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (55): WeightedFeatureFusion()
  (56): Sequential(
    (Conv2d): Conv2d(512, 256, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(256, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (57): Sequential(
    (Conv2d): Conv2d(256, 512, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(512, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (58): WeightedFeatureFusion()
  (59): Sequential(
    (Conv2d): Conv2d(512, 256, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(256, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (60): Sequential(
    (Conv2d): Conv2d(256, 512, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(512, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (61): WeightedFeatureFusion()
  (62): Sequential(
    (Conv2d): Conv2d(512, 1024, kernel_size=(3, 3), stride=(2, 2), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(1024, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (63): Sequential(
    (Conv2d): Conv2d(1024, 512, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(512, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (64): Sequential(
    (Conv2d): Conv2d(512, 1024, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(1024, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (65): WeightedFeatureFusion()
  (66): Sequential(
    (Conv2d): Conv2d(1024, 512, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(512, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (67): Sequential(
    (Conv2d): Conv2d(512, 1024, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(1024, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (68): WeightedFeatureFusion()
  (69): Sequential(
    (Conv2d): Conv2d(1024, 512, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(512, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (70): Sequential(
    (Conv2d): Conv2d(512, 1024, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(1024, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (71): WeightedFeatureFusion()
  (72): Sequential(
    (Conv2d): Conv2d(1024, 512, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(512, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (73): Sequential(
    (Conv2d): Conv2d(512, 1024, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(1024, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (74): WeightedFeatureFusion()
  (75): Sequential(
    (Conv2d): Conv2d(1024, 512, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(512, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (76): Sequential(
    (Conv2d): Conv2d(512, 1024, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(1024, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (77): Sequential(
    (Conv2d): Conv2d(1024, 512, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(512, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (78): MaxPool2d(kernel_size=5, stride=1, padding=2, dilation=1, ceil_mode=False)
  (79): FeatureConcat()
  (80): MaxPool2d(kernel_size=9, stride=1, padding=4, dilation=1, ceil_mode=False)
  (81): FeatureConcat()
  (82): MaxPool2d(kernel_size=13, stride=1, padding=6, dilation=1, ceil_mode=False)
  (83): FeatureConcat()
  (84): Sequential(
    (Conv2d): Conv2d(2048, 512, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(512, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (85): Sequential(
    (Conv2d): Conv2d(512, 1024, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(1024, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (86): Sequential(
    (Conv2d): Conv2d(1024, 512, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(512, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (87): Sequential(
    (Conv2d): Conv2d(512, 1024, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(1024, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (88): Sequential(
    (Conv2d): Conv2d(1024, 75, kernel_size=(1, 1), stride=(1, 1))
  )
  (89): YOLOLayer()
  (90): FeatureConcat()
  (91): Sequential(
    (Conv2d): Conv2d(512, 256, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(256, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (92): Upsample(scale_factor=2.0, mode=nearest)
  (93): FeatureConcat()
  (94): Sequential(
    (Conv2d): Conv2d(768, 256, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(256, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (95): Sequential(
    (Conv2d): Conv2d(256, 512, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(512, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (96): Sequential(
    (Conv2d): Conv2d(512, 256, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(256, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (97): Sequential(
    (Conv2d): Conv2d(256, 512, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(512, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (98): Sequential(
    (Conv2d): Conv2d(512, 256, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(256, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (99): Sequential(
    (Conv2d): Conv2d(256, 512, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(512, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (100): Sequential(
    (Conv2d): Conv2d(512, 75, kernel_size=(1, 1), stride=(1, 1))
  )
  (101): YOLOLayer()
  (102): FeatureConcat()
  (103): Sequential(
    (Conv2d): Conv2d(256, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(128, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (104): Upsample(scale_factor=2.0, mode=nearest)
  (105): FeatureConcat()
  (106): Sequential(
    (Conv2d): Conv2d(384, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(128, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (107): Sequential(
    (Conv2d): Conv2d(128, 256, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(256, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (108): Sequential(
    (Conv2d): Conv2d(256, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(128, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (109): Sequential(
    (Conv2d): Conv2d(128, 256, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(256, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (110): Sequential(
    (Conv2d): Conv2d(256, 128, kernel_size=(1, 1), stride=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(128, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (111): Sequential(
    (Conv2d): Conv2d(128, 256, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1), bias=False)
    (BatchNorm2d): BatchNorm2d(256, eps=0.0001, momentum=0.03, affine=True, track_running_stats=True)
    (activation): LeakyReLU(negative_slope=0.1, inplace=True)
  )
  (112): Sequential(
    (Conv2d): Conv2d(256, 75, kernel_size=(1, 1), stride=(1, 1))
  )
  (113): YOLOLayer()
)

```

