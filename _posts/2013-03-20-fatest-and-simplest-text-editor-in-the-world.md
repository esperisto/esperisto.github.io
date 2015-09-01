---
title: 世界最快速最简单的文本编辑器
author: esperisto
layout: post

categories:
  - 经验之谈
tags:
  - HTML5
  - 技巧
  - 浏览器
  - 笔记本
  - 编辑器
archive: false
comments: true  
---
最近不知道在哪里突然发现了一个 HTML5 绝妙的技巧，可以把浏览器弄成一个编辑器。以前在用电脑的时候突然要记一个东西，不得不打开一个文本编辑器来，在 Windows 上我一般用 SciTE，一个小巧的文本编辑器。在 Ubuntu 上一般用 gedit。但是再小的编辑器，与打开一个浏览器标签页相比打开速度也是很慢的。现在不愁了。  
只需在浏览器（Firefox、Chrome、Opera）中，打开一个新标签页，在地址栏中输入：

```
    data:text/html, <html contenteditable>`
```

新标签页就变成一个记事本了。把这个标签页放到书签工具栏里，每次需要记个什么东西的时候，鼠标中键单击，瞬间出来记事本。方便快捷。  
这简单的一句话，在 [Jose Jesus Perez Aguinaga][1] 的博客里大家完善了好多出来。

这里记两个我使用的：

```
data:text/html;charset=utf-8,<title>TextEditor</title> <style>html,body{margin:0;padding:0;}</style><textarea style="font-size:2rem;font-family:monaco;line-height:1.4;width: 100%; height:100%;border:none;outline:none;margin:0; padding:90px;"autofocus placeholder="在此处输入文字" />`
```

这个是用 textarea 而不是 contenteditable 做的。  
下面这个，作者 [vladocar][2]，弄成了时髦的 [Writability &#8211; Minimal Distractions Free Browser Text Writing Tool][3]：

```
data:text/html;charset=utf-8, <title>Writability</title><body OnLoad='document.body.focus();'  contenteditable style="font-size:21px;line-height:1.6;font-family:'Chaparral Pro',Georgia;max-width:21em;margin:0 auto;padding:3rem;background-color:rgb(233,233,225);color:rgb(68,68,68);" spellcheck="false">`
```

这篇文章就是我用 Writability 写好复制到 WordPress 里的。

 [1]: https://coderwall.com/p/lhsrcq
 [2]: https://coderwall.com/vladocar
 [3]: http://www.vcarrer.com/2013/01/writability-write-in-your-browser.html