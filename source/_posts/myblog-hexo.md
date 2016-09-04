---
title: 利用 hexo + github 搭建个人博客
date: 2016-09-04 02:59:07
categories:
  - 其它
tags: [hexo, github]
---

Hexo是一个开源的静态博客生成器， GitHub Pages免费的静态站点，利用两者可以方便搭建简单的个人博客。

# 准备条件
1. hexo
2. git

## 安装 hexo
1. 安装node.js
2. 校验node.js 

``` sh
$ node -v
$ npm -v
```

3. 安装hexo

``` sh
$ npm install hexo-cli -g
$ npm install hexo --save
$ hexo -v
$ hexo init & npm install
$ hexo g
$ hexo s
```

## 安装 git

## 配置_config.yml

``` javascript
deploy:
  type: git
  repo: git@github.com:yourname/yourname.github.io.git
  branch: master
```

## 部署（上传）到github

``` sh
$ npm install hexo-deployer-git --save
$ hexo d 
```




