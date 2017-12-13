---
title: CSS优先级别
date: 2017-12-12 14:54:22
tags:
---
0. !import
1. 内嵌样式style 1000
2. id选择器      0100
3. class选择器/属性选择器/伪类选择器 0010
4. 标签选择器/伪元素选择器 0001
5. 通配符选择器
6. 子选择器(>)， 相邻选择器(+)

相关文章：
- [优先级是如何计算的](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Specificity)
- [CSS 的优先级机制[总结]](http://www.cnblogs.com/xugang/archive/2010/09/24/1833760.html)