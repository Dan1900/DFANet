# DFANet
This repo is an unofficial pytorch implementation of DFANet:Deep Feature Aggregation for Real-Time Semantic Segmentation
# log
* 2019.4.16  Afater 483 epoches it rases RuntimeError: value cannot be converted to type float without overflow: (9.85073e-06,-3.2007e-06).According to the direcation of stackoverflow the error can be fixed by modifying "self.scheduler.step()" to "self.scheduler.step(loss.cpu().data.numpy())" in train.py.But the loss and iou become very bad descriped on "curvs on CityScape set"。 


### Installation

* pytorch==1.0.0
* python==3.6
* numpy
* torchvision
* matplotlib
* opencv-python
* tensorflow
* tensorboardX

### Dataset and pretrained model

Download CityScape dataset and unzip the dataset into `data` folder.Then run the command 'python utils/preprocess.py' to create labels.

### Train the network without pretrained model.
Modify your configuration in `main.py`.

```
run the command  'python main.py'
```

### curvs on CityScape set

![](https://github.com/huaifeng1993/DFANet/blob/master/results/DeepinScreenshot_select-area_20190418170943.png)

### To do

- [ ] Train the backbone xceptionA on the ImageNet-1k.

- [ ] Modify the network and improve the accuracy.

- [ ] Debug and report the performance.

- [x] Schedule the lr

under construction...

### Thanks

