---
layout: wiki
title: ubuntu16.04 常用软件安装
categories: ubuntu
description: 软件安装。
keywords: ubuntu，软件
---


### 网易云音乐

```shell
sudo dpkg -i netease-cloud-music*ubuntu.deb
```
显示安装错误，因为缺少依赖,使用如下命令安装相关依赖：
```shell
sudo apt-get install -f 
```
再重复安装命令:
```shell
sudo dpkg -i netease-cloud-music*ubuntu.deb
```
启动客户端：
```shell
netease-cloud-music
```



参考链接：
[网易云安装](https://blog.csdn.net/zz531987464/article/details/83050067)

<span style="color: red;">*转载注明出处，这样我就更能坚持写作了*<span>  
**[随心的个人博客](https://jinbooooom.github.io) >> [ubuntu16.04 常用软件安装](https://jinbooooom.github.io/wiki/ubuntu16.04_config/)**  
