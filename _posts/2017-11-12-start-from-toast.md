---
layout: post
title: Android 源码分析 —— 从 Toast 出发
categories: Android
description: Android 源码分析，深入解析 Toast。
keywords: RTFSC, Android, Toast
---

本系列文章在 <https://github.com/mzlogin/rtfsc-android> 持续更新中，欢迎有兴趣的童鞋们关注。

![](/images/posts/android/toast.png)

（图 from Android Developers）

Toast 是 Android 开发里较常用的一个类了，有时候用它给用户弹提示信息和界面反馈，有时候用它来作为辅助调试的手段。用得多了，自然想对其表层之下的运行机制有所了解，所以在此将它选为我的第一个 RTFSC Roots。

本篇采用的记录方式是先对它有个整体的了解，然后提出一些问题，再通过阅读源码，对问题进行一一解读而后得出答案。

本文使用的工具与源码为：Chrome、插件 insight.io、GitHub 项目 [aosp-mirror/platform_frameworks_base][3]

**目录**

<!-- vim-markdown-toc GFM -->

* [Toast 印象](#toast-印象)
* [提出问题](#提出问题)
* [解答问题](#解答问题)
    * [Toast 的超时时间](#toast-的超时时间)

<!-- vim-markdown-toc -->

## Toast 印象

首先我们从 Toast 类的 [官方文档](1) 和 [API 指南](2) 中可以得出它具备如下特性：

1. Toast 不是 View，它用于帮助创建并展示包含一条小消息的 View；

2. 它的设计理念是尽量不惹眼，但又能展示想让用户看到的信息；

3. 被展示时，浮在应用界面之上；

不知道你看到这个列表，是否学到了新知识或者明确了以前不确定的东西，反正我在整理列表的时候是有的。

## 提出问题

根据以上特性，再结合平时对 Toast 的使用，提出如下问题来继续本次源码分析之旅（大致由易到难排列，后文用 小 demo 或者源码分析来解答）：

1. Toast 的超时时间具体是多少？

2. 能不能弹一个时间超长的 Toast？





<div align="center"><img width="192px" height="192px" src="https://mazhuang.org/assets/images/qrcode.jpg"/></div>

[1]: https://developer.android.com/reference/android/widget/Toast.html

