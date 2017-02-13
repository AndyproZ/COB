---
title: Angular2.0学习笔记
date: 2017-02-13 13:55:50
tags:
---
该笔记整理自 大漠穷秋 的视频教程, 个别细节处进行补充。
[Angular2.0中文视频教程](https://my.oschina.net/mumu/blog/834254)

## 快速上手 

[Npm](https://nodejs.org/en/download/)
### npm代理配置
因为在校园网下，访问外网速度较慢，故需要设置镜像。
正常网络环境下推荐使用VPN。
方法一(CMD运行以下命令)
```
设置镜像
npm config set registry https://registry.npm.taobao.org 
npm info underscore
删除镜像
npm config delete registry
```
方法二(安装淘宝npm镜像工具cnpm)
``` bash
安装
$ npm install -g cnpm --registry=https://registry.npm.taobao.org
使用
cnpm用法与npm使用方法相同
卸载
$ npm uninstall cnpm
```
### Angular-Cli

Angular-Cli的安装
```
(管理员权限运行cmd)
$ npm install -g node-gyp
$ npm install --global windows-build-tools
$ npm install -g angular-cli
```
Angular-Cli的使用
```
查看版本
$ ng --version 
查看帮助
$ ng help 
创建新angular项目
$ ng new project-name (project-name为项目名,任意英文字符)
本地运行该项目
$ ng serve
生成类
$ ng generate class
$ ng g cl
模板名称缩写(使用方法同上)
cl:class
c:component
d:directive
e:enum
m:module
p:pipe
s:service
设置预编译(发布前使用该方法)
$ ng  serve --prod --aot
```
### Angular2最核心的3个概念

Component组件
[单向数据流例子](https://github.com/modern-javascript/angular2-data-flow)
[ngd组件树生成器](https://github.com/compodoc/ngd)

NgModule根模块
[@NgModule常见问题](https://angular.cn/docs/ts/latest/cookbook/ngmodule-faq.html)

Router路由
静态路由
异步路由
[路由与导航](https://angular.cn/docs/ts/latest/guide/router.html)

### Angular架构思想
DI依赖注入
[对比Angular1和Angular2中的依赖注入](https://my.oschina.net/mumu/blog/775695)

DataBinding数据绑定
[ANGULAR CHANGE DETECTION EXPLAINED](https://blog.thoughtram.io/angular/2016/02/22/angular-2-change-detection-explained.html)
[ANGULAR 2CHANGE DETECTION EXPLAINED](http://pascalprecht.github.io/slides/angular-2-change-detection-explained/#/)

### UI库
[ng2-bootstrap](https://github.com/valor-software/ng2-bootstrap) 
[PrimeNG](http://www.primefaces.org/primeng/#/)
[Angular-Material2](https://github.com/angular/material2)
[Ionic](https://ionic.io/)

### 其它
[Angular2思维导图](https://github.com/TeamStuQ/skill-map/tree/master/data/designbyStuQ/png-Angular2-by-StuQ.png)

[Tilt火狐插件，3D形式展现页面元素关系](https://addons.mozilla.org/zh-CN/firefox/addon/tilt/)
