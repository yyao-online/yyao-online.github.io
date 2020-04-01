---
layout: article
title: 使用jekyll在github上搭建个人博客（三）
key: 2020-04-01-jekyll-github-pages-3
tags: jekyll github 博客
pageview: true
---

> 本文中我将介绍如何在[github](https://github.com/)上搭建个人博客，其中会涉及到一些命令行操作，可能对于编程小白会有一些难懂。

### 使用主题

本文使用TeXt主题来美化博客

**GitHub地址：**[https://github.com/kitian616/jekyll-TeXt-theme](https://github.com/kitian616/jekyll-TeXt-theme)

主题的作者提供了多种方式安装主题，笔者采用的是最简单直接的方式。

#### 1. 下载

[<i class="fas fa-download"></i>下载TeXt主题](https://github.com/kitian616/jekyll-TeXt-theme/archive/master.zip){:.button.button--success.button--rounded.button--lg}

#### 2. 安装

- 清空你的仓库，并将主题包解压至仓库根目录

<span><font color="red">注意下载的主题压缩包内部还有一层目录，需要将此目录中的内容释放至仓库根目录下</font></span>

- 安装依赖（若不需要本地调试，可以跳过）
```shell
> bundle install
```

- 本地调试
```shell
> jekyll serve
```

![Jekyll-TeXt-Theme本地服务](https://blog-yyao-online.oss-cn-hangzhou.aliyuncs.com/2020-04-01-jekyll-github-pages-3/Jekyll-TeXt-Theme%E6%9C%AC%E5%9C%B0%E6%9C%8D%E5%8A%A1.jpg)

#### 3. 站点设置

**参考文档**

- 英文：[https://tianqi.name/jekyll-TeXt-theme/docs/en/quick-start](https://tianqi.name/jekyll-TeXt-theme/docs/en/quick-start)
- 中文：[https://tianqi.name/jekyll-TeXt-theme/docs/zh/quick-start](https://tianqi.name/jekyll-TeXt-theme/docs/zh/quick-start)