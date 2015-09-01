---
title: Ubuntu 6.06 安装备忘
author: esperisto
layout: post
archive: true
comments: true
categories:
  - 经验之谈
tags:
  - installation
  - linux
  - ubuntu
---
  * 安装完毕后先改变为cn99的源，更新、升级到6.06.1。
  * 然后安装显卡驱动程序 nvidia-glx。
  * 再进行中文美化：安装文泉驿点阵字体及Windows中的宋体、仿宋体、黑体。（其实系统以安装好后中文显示就很不错了，只是不习惯uming字体）

　　一个完整美化过的系统就绪了。

  * 然后再安装一些 firefox 扩展: performancing、fasterfox、flashplayer、del.icio.us、雅虎收藏+。
  * Blog客户端还可选择Deepest Sender（用了一下，觉得还是没有performancing来的顺手，如果blog是LiveJournal的话还要好一点）。 
  * 多媒体方面mplayer，w32codec。

更新：由于Ubuntu 6.06没有预先安装gstreamer 0.10，所以导致totem和Rhythmbox无法播放mp3音乐，只需 sudo apt-get install gstreamer0.10*