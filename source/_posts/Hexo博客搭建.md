---
title: Hexo博客搭建
date: 2017-02-13 01:25:25
tags:
---
简单记录一下Hexo博客的搭建

## Hexo

### 安装Hexo Cli

``` bash
$ npm install hexo-cli -g
```

### 生成Hexo项目

``` bash
$ hexo init blog
$ cd blog
$ npm install
$ hexo server
```

### Hexo个性化设置

[官方配置说明(英文)](https://hexo.io/docs/configuration.html)

``` 
项目根目录下的 _config.yml 文件
```

## Hexo主题 Fexo

[Fexo Github](https://github.com/forsigner/fexo)

### Fexo使用

``` bash
hexo项目根目录下themes文件夹下克隆主题项目
$ cd themes
$ git clone https://github.com/forsigner/fexo.git
修改hexo项目根目录下的配置文件_config.yml
theme: fexo
```

### Fexo个性化设置

[Fexo文档](http://forsigner.com/2016/03/10/fexo-doc-zh-cn/)

```
项目根目录下 themes\fexo
详细见fexo官方文档
```

## 其它

### 上传至Github

``` bash
Github上新建一个仓库
仓库名为
Github用户名.github.io
hexo项目根目录下安装发布工具
$ npm install hexo-deployer-git --save
修改hexo项目根目录下的配置文件_config.yml
deploy:
  type: git
  repo: github仓库地址
  branch: master
  message: 提交本次修改信息(github commit message)
发布
$ hexo generate
$ hexo deploy
本地效果浏览
$ hexo server
服务器效果浏览
Github用户名.github.io  
```

### 绑定域名

```
hexo项目根目录下source文件夹
新建文件CNAME (无文件名后缀)
内容 为待绑定域名 (无http://www:前缀)
域名提供商处修改DNS解析
增加对Github服务器的解析
主机记录@, 记录值192.30.252.153
主机记录www, 记录值192.30.252.154
主机记录@, 记录值192.30.252.154
主机记录www, 记录值192.30.252.153
等待DNS刷新后即可正常解析(一般为10分钟左右)
```