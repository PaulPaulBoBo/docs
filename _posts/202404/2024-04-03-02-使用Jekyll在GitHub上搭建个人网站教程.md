---
title:      使用Jekyll在GitHub上搭建个人网站教程
date:       2024-04-03
tags:
- Github
- Jekyll
--- 

## 一、前言

Jekyll是一个简单的、博客感知的、静态站点生成器。它使用Markdown（或其他标记语言）来格式化文本，然后通过Liquid模板引擎来布局网站，最后生成一个完整的静态网站。GitHub Pages则允许你在GitHub上直接托管你的网站，并且可以与Jekyll完美结合。下面我们就来详细介绍一下如何使用Jekyll在GitHub上搭建个人网站。

## 二、准备工作

在开始之前，你需要确保已经安装了以下工具：

1. **Git**：一个分布式版本控制系统，用于与GitHub进行交互。
2. **Ruby**：Jekyll的运行需要Ruby环境。

## 三、安装Jekyll

打开命令行工具，输入以下命令来安装Jekyll：


```bash
gem install jekyll bundler
```
这将安装Jekyll和Bundler。Bundler是Ruby的一个依赖管理工具，可以帮助我们管理Jekyll的插件和主题。

## 四、创建并初始化项目

在命令行中，导航到你想要创建网站的目录，然后输入以下命令来初始化一个新的Jekyll项目：


```bash
jekyll new my-awesome-site
cd my-awesome-site
```
这将在当前目录下创建一个名为`my-awesome-site`的新目录，并初始化一个新的Jekyll项目。

## 五、配置网站

进入项目目录后，你会看到一个名为`_config.yml`的文件。这是Jekyll的配置文件，你可以在这里设置网站的标题、描述、URL等基础信息。例如：


```yaml
title: My Awesome Site
description: > # this means to ignore newlines until "baseurl:"
  A blog about my awesome life.
baseurl: "" # the subpath of your site, e.g. /blog
url: "https://example.com" # the base hostname & protocol for your site, e.g. http://example.com
```
## 六、编写博客文章

在Jekyll中，博客文章通常放在`_posts`目录下。每个文章都是一个Markdown文件，文件名遵循`YEAR-MONTH-DAY-title.MARKUP`的格式。例如，`2023-07-18-hello-world.md`。

在Markdown文件中，你可以使用Markdown语法来格式化文本。例如：


```markdown
---
layout: post
title:  "Hello World"
date:   2023-07-18 10:18:00 +0800
categories: jekyll update
---

You'll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.
```
## 七、本地预览

在命令行中，输入以下命令来启动Jekyll的本地服务器：


```bash
bundle exec jekyll serve
```
这将启动一个本地服务器，并在浏览器中打开你的网站。你可以在浏览器中看到网站的实时预览，并在修改文件后自动刷新。

## 八、将网站推送到GitHub

首先，你需要在GitHub上创建一个新的仓库，并将你的项目与这个仓库关联起来。然后，你可以使用Git命令将你的项目推送到GitHub：


```bash
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/your-username/your-repo.git
git push -u origin master
```
请将上述命令中的`your-username`和`your-repo`替换为你的GitHub用户名和仓库名。

## 九、启用GitHub Pages

在GitHub上，进入你的仓库设置，找到"GitHub Pages"部分，选择"master branch"作为源，然后保存更改。现在，你的网站就已经在GitHub Pages上上线了！

## 十、总结

以上就是使用Jekyll在GitHub上搭建个人网站的完整教程。当然，这只是一个基础的入门教程，Jekyll还有很多高级功能和插件等待你去探索。希望这个教程能对你有所帮助，祝你搭建出一个属于自己的、独一无二的网站！