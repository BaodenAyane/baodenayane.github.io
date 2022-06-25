---
redirect_from: /_posts/2022-06-25-%E7%9B%AE%E6%A0%87%E6%A3%80%E6%B5%8B%E7%AE%97%E6%B3%95%E5%AD%A6%E4%B9%A0-FasterRCNN/
title: 目标检测算法学习-FasterRCNN
tags:
  -机器学习
---
[`目标检测算法视频`](https://www.bilibili.com/video/BV1mU4y1m7dN)

## RCNN介绍：
步骤一：训练分类网络（AlexNet）

步骤二：模型做fine-tuning

        1.类别1000改为20
        
        2.去掉FC
        
步骤三：特征提取

        1.提取候选框（选择性搜索）
        
        2.对于每一个区域：修正区域为CNN的输入，利用网络对候选框提取到特征
        
