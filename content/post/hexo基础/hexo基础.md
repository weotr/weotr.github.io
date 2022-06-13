---
title: "Hexo基础"
description: butterfly主题
date: 2022-04-19T13:33:08+08:00
image: 
math: 
license: 
hidden: false
comments: true
draft: false
categories: ['hexo']
tags: ['hexo']
lastmod: '2022-05-18'
---
###  · 相关工具

##### 1、安装node.js

##### 2、安装npm

##### 3、安装git

##### 4、检测安装成功

打开cmd命令行，分别执行，

```npm -v```

```git --version```
如果出现版本信息就安装成功
##### 5、安装hexo
打开cmd，执行

```npm install hexo-cli -g```

等待安装完成，输入
```hexo -v```
出现版本号则安装成功


### · 配置远程仓库

##### 1、注册github账户，add a new repository
格式为"用户名.github.io"，此地址即为网站域名
pulic类型

创建之后，点setting设置远程库，找到Github Pages 点击Automatic page generator

##### 2、本地生成ssh并与仓库绑定
```$ cd ~/.ssh #查看本机已存在的ssh```
如果没有，
```ssh-keygen -t rsa -C ''邮件地址''```
3次回车，
生成一个ssh公钥，找到.ssh文件夹，记事本打开复制.pub文件内容
github->设置->ssh->将公钥内容复制到key，title随便，保存
测试是否成功
```$ ssh -T git@github.com #邮件地址不用改```
输入yes，出现''hi ***,You're successfully~''则配置成功

配置
```$ git config --global user.name ''github用户名''```

```$ git config --global user.email ''邮箱''```

附：git其他操作（跳过）
```git add```
```git conmmit -m '提交信息'```
```git checkout -b hexo```创建并切换到新分支hexo，默认的master用来部署更新项目
```git push origin hexo```提交后到github把hexo分支设置默认

### ·  将hexo模板放到github
创建一个文件夹用于存放hexo，进入此文件夹右键git bush here
使用
```$ npm install hexo --save```
```$ hexo init```
```$ npm install```
```$ hexo g```
```$ hexo s```打开http://localhost:4000即可看到内容
修改_config.yml

langurage: ZH-hans
deploy:
    type: git
    repo: github上仓库ssh的链接
    branch：main

```$ npm install hexo-deployer-git -save```  安装远程部署插件

```$ hexo clean``` 清除public及_deploy缓存文件

```$ hexo d -g``` 生成静态页面并部署到GitHub
