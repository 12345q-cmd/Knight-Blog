---
title: 前端开发学习
cover: https://ts2.tc.mm.bing.net/th/id/OIP-C.D-4N9gpG64E4fBCiAN8WvQHaEK?rs=1&pid=ImgDetMain&o=7&rm=3
date: 2024-03-11 14:30:00
tags:
  - 教程
categories: 技术
---
## 前端开发学习
前端开发首先要熟悉html，css，JavaScript这几个技术

- <!DOCTYPE html> 声明使用html5版本来显示网页
- lang语言种类：en定义语言为英文，zh-CN为中文 ``<html lang=“en”>``
- 字符集（Character set）
 - eg：``<meta charset="UTF-8"/>``规定html文档使用的字符编码
 charset常用的有GB2312，BIG5，GBK，UTF-8(万国码)

- **加粗``<strong></strong>``或者``<b></b>``**
- **倾斜 ``<em></em>``或者``<i></i>``**  ``<i></i>``斜体
- 删除线``<del></del>``或者``<s></s>``
- 下划线``<ins></ins>``或者``<u></u>``

- ``<div> ``标签用来布局,但是现在一行只能放一个``<div>``｡ 

  ``<span>`` 标签用来布局,一行上可以多个 ``<span>``｡

- 图像标签和路径
 - ``<img src="图像URL"/>``
   - src图片路径
   - alt替换文本
   - title提示文本
   - width设置图像宽度
   - height设置图像高度
   - border 设置边框粗细
- 链接语法
  - ``<a href="跳转目标" target="目标窗口的弹出方式"> 文本或图像 </a>``
  href用来指定链接目标的url地址
  target用于指定链接页面的打开方式，_self为默认值，_blank为在新窗口中打开方式


- css用于外观美化和布局定位
`` <head>
         <style>
            p{
                属性名: 属性值;
                属性名：属性值;
            }
            </style>
 </head>``


css引用方法，有三种方式：内部样式，行内样式，外部样式
- 内部样式（内嵌样式）页面头部style标签定义
- 行内样式（嵌入样式）：html标签的style属性
- 外部样式：使用独立``.css``文件定义，然后在页面中使用``link标签``或者
 ``<link rel="stylesheet" type="text/css" href="CSS样式文件的路径">``
 ``@import``指令导入外部样式文件
``
<style>
    @import url("css文件路径");
</style>
``
- 选择器：
  - 基础选择器：id选择器，类选择器，标签选择器，通配符选择器
  - 复杂选择器：复合选择器，组合选择器，嵌套选择器，伪类选择器
  - link 未访问的链接
    - visited 已访问的链接
    - hover 鼠标悬浮到连接上，即移动在连接上
    - active 选定的链接，被激活

- 选择器优先级：行内样式>ID选择器>类选择器>标签选择器
- 用！important可是某个样式有最高优先级 
常见css属性
font-size 字体大小
font-weight 字体粗细
font-family 字体
font-style 字体样式 norma普通italic斜体
font 简写

em倍数

- color 颜色
 line-height 行高
 text-align 文本对齐
 vertical-align 垂直对齐
 vertical
！[文本属性](C:\Desktop\my-hexo-blog\public\images\2025-08-13 023336.png)
<img src="C:\Desktop\my-hexo-blog\public\images\2025-08-13 023336.png" alt="文本属性" width="500" height="300">
