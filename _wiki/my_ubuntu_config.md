---
layout: wiki
title: 个人 ubuntu16.04 常用软件工具安装配置
categories: ubuntu
description: 常用软件工具安装配置。
keywords: ubuntu
---
 

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


  


<span style="color: red;">*转载注明出处，这样我就更能坚持写作了*<span>  
**[随心的个人博客](https://jinbooooom.github.io) >> [人类简史简摘](https://jinbooooom.github.io/2018/12/15/my_ubuntu16_config/)**  




















　　
