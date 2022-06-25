---
redirect_from: /_posts/2022-06-25-%E7%9B%AE%E6%A0%87%E6%A3%80%E6%B5%8B%E7%AE%97%E6%B3%95%E5%AD%A6%E4%B9%A0-FasterRCNN%E5%BA%94%E7%94%A8%E4%BA%8EADAS/
title: 目标检测算法学习-FasterRCNN应用于ADAS
tags:
  -机器学习
---
[`目标检测算法视频`](https://www.bilibili.com/video/BV1mU4y1m7dN)

## ADAS业务场景综述

先进驾驶辅助系统（Advanced Driver Assistance System），简称ADAS，是利用安装于车上的各式各样的传感器，在第一时间收集车内外的环境数据，进行静，动态物体的辨识，侦测与追踪等技术
上的处理，从而能让驾驶者在最快的时间察觉可能发生的危险，以引起注意和提高安全性的安全技术

## KITTI数据集

KITTI数据集由德国卡尔斯鲁厄理工学院和丰田美国技术研究院联合创办，是目前国际上最大的自动驾驶场景下的计算机视觉算法评测数据集。该数据集用于评测立体图像(stereo)，光流(optical flow)，视觉测距(visual odometry)，3D物体检测(object detection)和3D跟踪(tracking)等计算机视觉技术在车载环境下的性能。KITTI包含市区、乡村和高速公路等场景采集的真实图像数据，每张图像中最多达15辆车和30个行人，还有各种程度的遮挡与截断。整个数据集由389对立体图像和光流图，39.2 km视觉测距序列以及超过200k 3D标注物体的图像组成，以10Hz的频率采样及同步。总体上看，原始数据集被分类为’Road’, ’City’, ’Residential’, ’Campus’ 和 ’Person’。对于3D物体检测，label细分为car, van, truck, pedestrian, pedestrian(sitting), cyclist, tram以及misc组成。

[`本次学习所使用的KITTI数据集`](http://www.cvlibs.net/datasets/kitti/eval_object.php?obj_benchmark=2d)

使用的是其中的Download left color images of object data set (12 GB)和Download training labels of object data set (5 MB)数据集

## KITTI数据集打包成VOC格式数据集

