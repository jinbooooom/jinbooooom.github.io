---
layout: post
title: 数据处理工具
summary: 深度学习模型训练前的一些数据处理需要用到的工具
featured-img: tools
---

深度学习模型训练前的一些数据处理需要用到的工具。

开源工具：[数据处理](https://github.com/jinbooooom/data-processing)
这里面大部分程序用于数据增广

- ### 镜像变换
  - augmented_data/mirror.py   

  ![mirror](https://jinbooooom.github.io/sources/cat.jpg)

- ### 仿射变换
  - augmented_data/warp.py  

    对于已标注的图像，通过旋转变换来增广数据集，并且算出增广的数据的坐标，取代低效的人工手动标注。

  - augmented_data/showBBox.py  

    将计算出的标注框，显示在增广后的图像上。

  ![warp_show](https://jinbooooom.github.io/sources/warp_show.jpg)

- ### 生成新图片
  - augmented_data/createNewImg.py

  对数字仪表图片，将里面的数字都裁剪出来，随机缩放、旋转、噪声处理等，然后将不同的数字粘贴到某一个模板的显示屏上，以扩展数据集。  
  ![create_led](https://jinbooooom.github.io/sources/create_led.jpg)

- ### 标签信息 YOLO 格式转 VOC2007格式
- yolo2voc.py

- ### 其他工具
  - tools/BaiduImageSpider/index.py：输入关键字，就爬百度图片下该关键字的图片，用来弥补数据量不充足时，补充数据集。

  - tools/extract_frames/\*：用于对视频抽帧。当数据量不足时，可以通过拍视频的方式，然后设置每隔多久抽一帧图像作为数据集。