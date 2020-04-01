---
layout: article
title: 使用jekyll在github上搭建个人博客（二）
key: 2020-04-01-jekyll-github-pages-2
tags: jekyll github 博客
pageview: true
---

> 本文中我将介绍如何在[github](https://github.com/)上搭建个人博客，其中会涉及到一些命令行操作，可能对于编程小白会有一些难懂。

### 创建GitHub仓库

首先登录到GitHub，新建一个新的仓库：[https://github.com/new](https://github.com/new)

![GitHub创建仓库](https://blog-yyao-online.oss-cn-hangzhou.aliyuncs.com/2020-04-01-jekyll-github-pages-2/GitHub%E5%88%9B%E5%BB%BA%E4%BB%93%E5%BA%93.jpg)

**注意：**
- 仓库名称是`YOURNAME.github.io`，`YOURNAME`是你的GitHub的用户名，笔者是`yyao-online`，这样命名的仓库，部署后访问地址是`http://yyao-online.github.io`
- 仓库名称也可以是别的任意值，这样命名的仓库，部署后访问地址是`http://yyao-online.github.io/xxxxxxx`，`xxxxxxx`为仓库名，**这样可能会造成一些资源文件的丢失**。
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
```的大多数dd

本地运行
```shell
> jekyll serve
```

使用浏览器访问[http://127.0.0.1:4000](http://127.0.0.1:4000)即可查看效果。

![Jekyll本地服务](https://blog-yyao-online.oss-cn-hangzhou.aliyuncs.com/2020-04-01-jekyll-github-pages-2/Jekyll%E6%9C%AC%E5%9C%B0%E6%9C%8D%E5%8A%A1.jpg)

### 部署到GitHub Pages

部署过程很简单，将本地仓库`push`到GitHub即可。

部署后可以为你的博客自定义域名，在`GitHub > 你的仓库 > Settings`下设置

另外需要给你的域名增加一条`CNAME`类型的解析记录，该记录值对应的GitHub Pags默认生成的域名`YOURNAME.github.io`

![GitHub Pages设置](https://blog-yyao-online.oss-cn-hangzhou.aliyuncs.com/2020-04-01-jekyll-github-pages-2/GitHub%20Pages%E8%AE%BE%E7%BD%AE.jpg)

_GitHub Pages的主页：[https://pages.github.com/](https://pages.github.com/)，如有兴趣可以看看。_
