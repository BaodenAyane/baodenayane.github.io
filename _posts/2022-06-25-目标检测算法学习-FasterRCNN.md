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
        
              step0:生成区域集R，具体参见论文《Efficient Graph Based image Segmentation》
              
              step1:计算区域集R里每个相邻区域的相似度S={s1，s2...}
              
              step2：找出相似度最高的两个区域，将其合并为新集，添加进R
              
              step3：从S中移除所有与step2有关的子集
              
              step4：计算新集与所有子集的相似度
              
              step5：跳至step2，直至S为空
        
        2.对于每一个区域：修正区域为CNN的输入，利用网络对候选框提取到特征
        
