---
title: "Hugo基础"
description: 
date: 2022-05-17T19:37:00+08:00
image: 
math: 
license: 
hidden: false
comments: true
categories: ['hugo']
tags: ['hugo']
draft: false
lastmod: '2022-05-18'
---
## 常用命令 
`hugo new site "$mysite"`创建新站点

`hugo version`查看版本
 
`hugo env`版本和环境详细信息
 
`hugo new post/index.md`创建文章

`hugo`编译生成静态文件,Hugo将编译所有文件并输出到public目录

`hugo server`编译生成静态文件并启动web服务

## hugo+github手动推送流程
`hugo`生成静态文件，将public文件夹下内容复制到本地xxx.github.io文件夹下

进入xxx.github.io文件夹下

`git add .`提交全部内容到xxx.github.io文件夹下(注意空格)

`git commit -m '提交信息(必填)'`

`git push`

## iframe+obsidian在hugo中插入幕布
hugo不支持iframe嵌入，需要使用shortcode方式设置：
[参考](https://github.com/ericswpark/hugo-iframe）

``{{/</iframe url="https://music.163.com/outchain/player?type=2&id=25638827&auto=1&height=66">}}``(前面两处斜杠防止被渲染)

使用obsidian中convert url to iframe插件：`Alt+I`快捷键到网址上




