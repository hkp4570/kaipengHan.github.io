---
title: react中引入rc-tree和rc-tree-select库之后样式覆盖问题
date: 2021-11-05 13:40:05
categories: 
- 解决方案
tags: 
- react
- rc-tree
- rc-tree-select
---

## 问题
在项目中同时引入rc-tree和rc-tree-select库之后，同时在全局样式文件global.less中分别引入两个库的样式文件
<!-- more -->
![文件引入](1.png)
这时我们打开页面之后会发现rc-tree的样式没有正常显示，而且无法展开树结构
![不正常显示](2.png)
可是下面这样才是正常显示
![正常显示](3.png)
而此时rc-tree-select组件库却能够正常显示
![正常显示](4.png)
当我们调整全局样式文件中两个库的样式引入顺序，会发现谁后引入谁就可以正常显示。猜测可能是发生了样式覆盖
## 解决
![解决](5.png)
![解决](6.png)
同样也可以在使用rc-tree-select的组件中这样做
