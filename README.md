# iot-drawer
微信小程序的抽屉菜单

## 概述
基于微信小程序（weapp）开发的抽屉菜单

## 更新日志



### 0.1

`2017.11.12`

-   更新readme和第一版代码

## 下载
``` bash
git clone https://github.com/Shino161/iot-drawer.git
```
## Api
   `Method:`
   openIotDrawer() //打开菜单
   closeIotDrawer() //关闭菜单
   
## 组件用法

组件样式推荐在`app.wxss`直接引入`path/to/components/drawer-menu/index.wxss`。

~~~html

<import src="path/to/components/drawer-menu/index.wxml" />

<template is="iot-drawer" data="{{ pageData, iotDrawerOpen}}"></template>
~~~

将js文件引用到页面js后，合并到page

~~~js

var iotDrawer = require('path/to/components/drawer-menu/index.js');

Page(Object.assign({}, iotDrawer, {
  //点击菜单项后的回调
  selectItem: function(event){
    ...
    this.closeIotDrawer()
  },
  ...
}));

~~~
