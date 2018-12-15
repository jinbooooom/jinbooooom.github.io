---
layout: wiki
title: 个人 ubuntu16.04 常用软件工具安装配置
categories: ubuntu
description: 常用软件工具安装配置。
keywords: ubuntu
---
 
## 深度学习

### nvidia 显卡驱动

法一:
添加新 nvidia 官方驱动源
```shell
sudo add-apt-repository ppa:graphics-drivers/ppa
sudo apt-get update
```
安装驱动(对应我的笔记本 GTX1060 显卡，驱动是 410)
```shell
sudo apt-get install nvidia-410 nvidia-settings
```
[华硕笔记本(GTX 1060显卡)安装Ubuntu16.04+Nvidia显卡驱动+Cuda8.0+cudnn6.0+ROS+Opencv3.2+Caffe+Tensorflow](https://blog.csdn.net/Sparta_117/article/details/73739980)

法二：
打开 **设置>>软件和更新>>附加驱动**

### Anaconda

```shell
bash Anaconda*.sh
```

## 常用工具

### teamviewer

```shell
sudo dpkg -i teamviewer*.deb
```
不出意外会出现一些错误，需要安装一些依赖。使用下面的修复依赖关系的命令：
```shell
sudo apt-get install -f
```
再次执行命令:
```shell
sudo dpkg -i teamviewer*.deb
```
参考链接：
[Ubuntu16.04 安装Teamviewer](http://www.cnblogs.com/wmr95/p/7574615.html)


  


<span style="color: red;">*转载注明出处，这样我就更能坚持写作了*<span>  
**[随心的个人博客](https://jinbooooom.github.io) >> [人类简史简摘](https://jinbooooom.github.io/2018/12/15/my_ubuntu16_config/)**  




















　　
