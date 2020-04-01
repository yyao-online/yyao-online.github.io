---
layout: article
title: 使用jekyll在github上搭建个人博客（二）
key: 2020-04-01-jekyll-github-pages-2
tags: jekyll github 博客
---

> 本文中我将介绍如何在[github](https://github.com/)上搭建个人博客，其中会涉及到一些命令行操作，可能对于编程小白会有一些难懂。

### 创建GitHub仓库

首先登录到GitHub，新建一个新的仓库：[https://github.com/new](https://github.com/new)

![GitHub创建仓库](https://blog-yyao-online.oss-cn-hangzhou.aliyuncs.com/2020-04-01-jekyll-github-pages-2/GitHub%E5%88%9B%E5%BB%BA%E4%BB%93%E5%BA%93.jpg)

**注意：**
- 仓库名称是`YOURNAME.github.io`，`YOURNAME`是你的GitHub的用户名，笔者是`yyao-online`
- 无论是公有库还是私有库都可以，就算是私有库，使用了GitHub Pages也是公开的，我们做博客不就是给人看的么，哈哈~~~

经过以上步骤，仓库就创建好了。

### 创建第一个Jekyll项目

将仓库克隆到本地
```shell
> git clone https://github.com/YOURNAME/YOURNAME.github.io.git
```

进入克隆的仓库
```shell
> cd YOURNAME.github.io
```

创建Jekyll项目，因为当前文件夹是个Git仓库，并不是空文件夹，所以要加上`--force`参数
```shell
> jekyll new . --force
```

本地运行
```shell
> jekyll serve
```

使用浏览器访问[http://127.0.0.1:4000](http://127.0.0.1:4000)即可查看效果。

### 部署到GitHub Pages

部署过程很简单，将本地仓库`push`到GitHub即可。

_GitHub Pages的主页：[https://pages.github.com/](https://pages.github.com/)，如有兴趣可以看看。_
