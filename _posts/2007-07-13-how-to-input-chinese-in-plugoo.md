---
title: 如何在 Plugoo 中输入中文
author: esperisto
layout: post
archive: true
comments: true
categories:
  - 经验之谈
tags:
  - plugoo
  - web服务
  - 中文
  - 技巧
---
[Plugoo][1] 是一个可以让您在自己的站点、电子邮件、论坛文章等等中和您的读者聊天的工具。支持流行的即时聊天软件：Google Talk、MSN Messenger、AIM、Yahoo! Messenger、ICQ 及 Jabber。

但是在默认情况下，在 Plugoo 的 Widget 插件上是没法直接输入中文的，只能通过在其他地方写好后粘贴进去。

其实要想在其中直接输入中文很简单，只需要做一件事：删除 Plugoo HTML 代码中的 `<param name="wmode" value="transparent" />` 就可以了。

 [1]: http://www.plugoo.com