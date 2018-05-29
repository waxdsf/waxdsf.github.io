---
layout: post
title: 基于GitHub Pages和jekyll搭建个人博客
tags: [build]
---

#### 搭建过程

- 创建一个新项目，项目名须为username.github.io格式

  **备注：** 此处username为GitHub账号用户名

- 找一个Jekyll模版，可以参考[模版网站](http://jekyllthemes.org/)，拷贝下来放入项目里

- 将项目推到GitHub就大功告成了，现在你拥有一个个人博客了，只需要使用markdown撰写内容并放入相应目录并push，博客内容就会自动更新



#### 使用自定义域名

你可能还想要定义自己的域名，只需要以下两步：

- 添加域名解析

  记录类型选择CNAME，记录值填username.github.io

  **备注：** 此处username为GitHub账号用户名

- 配置GitHub

  有两种方式：

  - 在GitHub项目的Settings->GitHub Pages->Custom domain设置中填写要设置的域名
  - 在项目根目录创建一个名为CNAME的文件，在其中添加要解析的域名

需要注意的是如果使用一级域名，即www.domain.com，那么配置GitHub时只能填写domain.com，不能带有www，如果使用二级域名，如blog.domain.com，那么配置GitHub时需要填写整体域名，即blog.domain.com



#### 配置Jekyll本地环境

- 安装Ruby、RubyGems

- 安装Jekyll

  ```
  gem install jekyll bundler
  ```

- 本地运行

  在项目目录下执行

  ```
  bundler install
  jekyll serve
  ```

  

#### 参考

[GitHub帮助文档](https://help.github.com/articles/using-a-custom-domain-with-github-pages/)

[Jekyll官网](https://jekyllrb.com/docs/home/)