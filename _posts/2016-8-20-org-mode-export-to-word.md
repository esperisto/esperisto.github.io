---
layout: post
title: Org-mode 导出为 Word 的技巧
categories: 经验之谈
tags:
  - org-mode
  - word
  - xml
---

[Org Mode](http://www.orgmode.org) 是个大杀器。为了这个大杀器我也学习了 Emacs 的基本操作方法。

Org mode 的文件可以导出为各种文件格式，比如 pdf、html、iCalendar、LateX、ODT。

在使用中，有时需要转换到 Word 文档。但是并没有这个功能。怎么办呢？Org mode 虽然能够转换到 ODT 文档，但是 Word 却无法打开转换出的 ODT 文件。原因未知，我猜测也可能是文件头的问题。

我们可以借助 Word 可以打开 html 文件的功能，迂回一下，将 org 文件转换为 html 文件再由 Word 打开就可以了。

但是呢，直接转换的 html 打开后是乱码！

打开 html 查看源代码，为什么文件头不是 `html` 而是 `xml`？不是说好的导出 html 吗？

找到了如下的方法：

在 init.el 中添加以下内容，把 xml 文件头去掉：

```elisp 
(setq org-html-xml-declaration (quote (("html" . "")
                                       ("was-html" . "<?xml version=\"1.0\" encoding=\"%s\"?>")
                                       ("php" . "<?php echo \"<?xml version=\\\"1.0\\\" encoding=\\\"%s\\\" ?>\"; ?>"))))
```

之后导出的 html 文件就可以直接在 Word 打开了。

