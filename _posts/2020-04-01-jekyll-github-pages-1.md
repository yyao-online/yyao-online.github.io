---
layout: article
title: 使用jekyll在github上搭建个人博客（一）
key: 2020-04-01-jekyll-github-pages-1
tags: jekyll github 博客
pageview: true
---

> 本文中我将介绍如何在[GitHub](https://github.com/)上搭建个人博客，其中会涉及到一些命令行操作，可能对于编程小白会有一些难懂。

### 工具简介

1. **GitHub** [https://github.com/](https://github.com/)

    全球最大的社交编程及代码托管网站，并且支持将`Jekyll`项目免费部署在`GitHub Pages`上，支持自定义域名。

2. **Jekyll** [http://jekyllcn.com/](http://jekyllcn.com/)

    可以将文本转换成静态博客。

    **简单**

    不再需要数据库，不需要开发评论功能，不需要不断的更新版本——只用关心**你的博客内容**。

    **静态**

    Markdown（或 Textile）、Liquid 和 HTML & CSS 构建可发布的静态网站。

    **博客支持**

    支持自定义地址、博客分类、页面、文章以及自定义的布局设计。

3. **Git**

    安装及使用方法不会在本文中多做赘述，需要详细了解的，可以参考：[Git教程 - 廖雪峰的官方网站](https://www.liaoxuefeng.com/wiki/896043488029600)

4. **VS Code**

    微软开发的一款跨平台的文本编辑器，

### 环境搭建

这一步是为了你能在本地预览你的网站，如果你不需要在本地预览，可以跳过此步骤。

<span><font color="red">注：本文的所有内容基于Win10操作系统</font></span>

#### 1. 安装Jekyll

参考：[http://jekyllcn.com/docs/installation/](http://jekyllcn.com/docs/installation/)，本文的Jekyll都是参照此步骤。

需要注意的是，当前的Jekyll版本是`4.0.0`，已经不需要Python环境的支持，所以不用安装Python。而笔者在搭建博客环境之前，已经安装了NodeJs环境，后面也没有验证NodeJs对于Jekyll是否必须，大家可以试试不安装NodeJs是否可以运行Jekyll。

##### 1.1 安装Ruby

Ruby的Windows安装包下载地址 [https://rubyinstaller.org/downloads/](https://rubyinstaller.org/downloads/)

![Ruby下载](https://blog-yyao-online.oss-cn-hangzhou.aliyuncs.com/2020-04-01-jekyll-github-pages-1/Ruby%E4%B8%8B%E8%BD%BD.jpg)

这里我们直接下载推荐的版本 `Ruby+Devkit 2.6.5-1 (x64)`，下载下来是个`.exe`文件，直接运行即可。
        
**验证Ruby**

```shell
> ruby -v
ruby 2.6.5p114 (2019-10-01 revision 67812) [x64-mingw32]
```

##### 1.2 安装RubyGems

下载地址 [https://rubygems.org/pages/download](https://rubygems.org/pages/download)

![RubyGems下载](https://blog-yyao-online.oss-cn-hangzhou.aliyuncs.com/2020-04-01-jekyll-github-pages-1/RubyGems%E4%B8%8B%E8%BD%BD.jpg)

Windows操作系统下推荐下载`ZIP`，任意文件夹下解压后，进入对应目录，运行命令（需要以管理员身份运行命令）

```shell
> ruby setup.rb
```

**验证RubyGems**

```shell
> gem -v
3.1.2
```

##### 1.3 安装NodeJs

下载地址 [https://nodejs.org/en/](https://nodejs.org/en/)

![NodeJs下载](https://blog-yyao-online.oss-cn-hangzhou.aliyuncs.com/2020-04-01-jekyll-github-pages-1/NodeJs%E4%B8%8B%E8%BD%BD.jpg)

下载当前最新的LTS（Long Term Support 长期支持版）版本，下载下来是个`.msi`文件，直接运行即可。

**验证NodeJs**
```shell
> node -v
v12.16.1
> npm -v
6.13.4
```

#### 2. 安装Jekyll

```shell
> gem install jekyll
```

**验证Jekyll**

```shell
> jekyll -v
jekyll 4.0.0
```
