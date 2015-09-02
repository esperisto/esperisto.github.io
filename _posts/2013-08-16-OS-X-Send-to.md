---
title: 在 Mac OS X 上实现类似 Windows 发送到（Send To）功能
author: esperisto
layout: post

categories:
  - 经验之谈
tags:
  - Automator
  - Mac OS X
  - Windows
  - 服务
archive: false
comments: true
---
刚买了一台 MacBook Air 2013 款电脑，用着还挺舒服的。终于见识了苹果在笔记本方面的能力。话说这款电脑搭载的 Mac OS X Mountain Lion 是目前世界最先进的操作系统，怎么他的文件管理器 Finder 没有像 Windows 资源管理器的“发送到”功能呢？要知道这是一个很方便的功能，可以自己向 Sendto 文件夹添加文件夹快捷方式，以后在其他文件或文件夹上点右键就可以讲其复制过去。还可以快捷发邮件和发送到 U 盘里。比如下图：

![<Windows Send To](/assets/images/macsendto1.png)

其实在 Mac OS X 上，也还是能够实现类似的方法的。不过呢，现在我只能弄出发送到文件夹的功能。没法作出发送邮件。不过呢，这个发邮件的功能在其他地方是有的。下面就是具体办法：

  1. 我们需要打开 Automator：在 Launchpad 里面选择“其他”-›“Automator”。
  2. 在打开后出现的“选取文稿类型”中，单击“服务”，然后单击“选取”。这里我们就是要利用 Mac OS X 的“服务”功能来实现“发送到”。
  3. 在左侧窗格中的资料库里，选择“文件和文件夹”，然后在右边找到“拷贝 Finder 项目”。（刚从 Windows 换过来的朋友需要注意这里是“拷贝”，不是“复制”。Mac 上的复制和 PC 上的复制不是一个概念。按说英文版界面上，拷贝是 Copy，复制是 Duplicate。Mac 里的复制，在 Windows 上说成是创建副本）。
  4. 将找到的“拷贝 Finder 项目”拖到右侧窗格的空白处。然后在上方的“服务收到选定的”后面选中“文件或文件夹”。这个表示我们操作的输入是什么。后边的“位于”选择“Finder”。
  5. 在“拷贝 Finder 项目”中，将“至：”选成你需要发送到的文件夹。
  6. 按 Command + S 保存。保存的时候写一个明白易懂的名字。比如我用的是“发送到……文件夹”。

![Automator](/assets/images/macsendto2.png)

保存后，在 Finder 中随便选择一个文件单击右键，就会出来一个新的项目，单击就可以将文件或文件夹拷贝到设置的位置。试试吧！