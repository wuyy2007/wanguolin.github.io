---
layout: post
title: '在 Github 上搭建自己的博客系统'
category: 文档
tags: 折腾
---


本来是准备用wordpress写一点读书笔记的，结果在找可以将wordpress备份到Github插件或脚本的时候，才发现早就有成熟的方案可以在Github直接搭建自己的博客系统了。

对于程序员来说，这样做的好处是显而易见的：

1、发布博客的过程就是git push的过程，于是天然具备了博客的版本管理和分布式备份。

2、整个博客完全由代码所生成，内容和展现完全分离，可以比较容易的更换主题，以及升级维护、增加功能插件……各种折腾，完了一键编译就好。

3、服务器的维护成本摊给了Github，如果愿意使用username.github.io的话，连域名都省下了。

我在搭建这个系统的过程中，阅读了不少指导性的文章，其中最有帮助的要属[Github](http://help.github.com/categories/20/articles/)和[Jekyll的官方文档](http://jekyllrb.com/docs/home/)，但是如果你觉得中文更加亲近一些，加上我走过的弯路兴许能够对你有帮助，你就可以考虑读下去。



一、基本原理

1、我们之所以有机会能够图文茂的在Github上面书写博客，还要得益于Github的Page.Github,（现在更名为username.github.io）功能。这个功能可以让开发者或者企业host一些静态页面在指定的地点，他的工作原理是通过Jekyll（下面介绍）来编译放在指定repo的模板，从而生成静态的html页面再展现在（和指定repo位置）对应的url位置。

2、Jekyll是一个建站工具（Transform your pain text into static websites and blogs），其本质是一个模板引擎，可以根据模板和配置文件，生成博客或是网站。
    
Jekyll的开发环境是Ruby，这就意味着高度建议你在Linux或是Mac系统下完成环境的搭建工作。


2. 环境搭建

1、安装ruby和ruby-dev。ruby-dev中存在一些gem install所需要的依赖。

2、gem install jekyll

3、为了维持ruby jekyll等一系列工具链的版本一致性，强烈建议gem install bundler,然后建立一个如下的Gemfile來共bundle update的时候读取。

`
source 'https://rubygems.org'
gem 'github-pages'
`


3. ***；

二、“绿色”迁移

1. 拷贝 /Applications/Adobe Photoshop CC；

2. 拷贝 /Library/Application Support/Adobe 以及 ~/Library/Application Support/Adobe;

3. 运行 PS，提示“Adobe Application Support 文件夹中缺少运行 Photoshop 所需的一个或多个文件。请运行 Photoshop 安装程序，并重新安装 Photoshop。”，网上非常多人反映此问题，但没有解决方案。突然转念一想，换成英文关键字搜索，发现 [Adobe 官网有篇文章](http://helpx.adobe.com/photoshop/kb/error-one-or-files-application.html)，内容比较长，说白了就是还要拷贝 /Library/ScriptingAdditions/Adobe Unit Types.osax

4. 再次运行，一切搞定收工。

终于全部软件都是“绿色”啦……
