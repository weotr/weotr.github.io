---
title: "Markdown语法"
description: vscode编写
date: 2022-05-17T19:46:18+08:00
image: 
math: 
license: 
hidden: false
comments: true
draft: false
categories: ['markdown']
tags: ['markdown','vscode']
lastmod: '2022-05-18'
---

直接看[这篇教程](https://kz16.top/md/)，下边是我自己用vscode写markdown文件的一些留意事项


## markdown基本使用(vscode)

### 配合插件（vscode）
* Markdown Preview Enhanced
* Markdown TOC
* Excel to Markdown
* Paste Image

### 插入图片

* 使用paste image插件直接复制黏贴（不推荐）

这种方法插入的图片不能直接黏贴到博客页上，最好使用下面base64码转换的方法，可以任意复制黏贴全文
*webp用格式工厂转换下*（base64码好长一段，虽然能收起来，非必要不用）
[把图片转换成base64代码](http://www.jsons.cn/img2base64/)
代码太长vscode中可使用折叠方案，用标签```<!-- #region -->图片地址<!-- #endregion -->```

### 禅模式 更注重sematics
**我要抄单词啦** crtl+i斜体；crtl+b加粗加黑

### 公式
$$
[学一下Latex公式的使用](https://blog.csdn.net/fengxinlinux/article/details/86547402)
$$

### 表格
|电磁学|理论力学|量子力学|
|---|---|---|
|12|13|14|
|合格|良好|优秀|

|电磁学|理论力学|量子力学|
|---|---|---|
|12|13|14|
|合格|良好|优秀|

（这里不知道为什么用Preview content渲染出的表格没有边框线qwq,hexo渲染raw部分没有对齐）

### 链接
这是一个[链接](https://www.baidu.com/?tn=49055317_hao_pg)
复制链接，crtl+v到相应的文字上

### 输出为pdf
在Preview content中右击，选择Open in Browser,crtl+P

### 添加代码块
用```加代码表示
用hexo写博客，建议用下边这种。
{% codeblock %}
{% endcodeblock %}

参考教程：[markdown终极教程]()