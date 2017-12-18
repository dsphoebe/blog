---
title: CSS优先级别
date: 2017-12-12 14:54:22
tags: [CSS]
---
有人问我，CSS优先级是怎么样的？
然后我答说，内嵌Style > ID > Class > Element tag。
人又问，为什么了？
我说，不知道。
从我接触CSS已经有很多年了，它的优先级，有接触过它的优先级算法，但并没有记下来，只是由于使用中一直在头脑里重复这套 内嵌Style > ID > Class > Element tag。

我觉得我有必要深入了解下它

### CSS优先级是讲的什么？
CSS的各种选择器运用到一个HTML标签上后，这些选择器的样式的运用的优先级决定了这个HTML标签最后在浏览器的展示

### CSS选择器有哪些了？
除了在HTML标签上直接加的style属性，就是在.css文件里面的用到的了，
有：
|id选择器|#id|
|class选择器|.class|
|属性选择器||
|伪类选择器||
标签选择器，
伪元素选择器，
通配符选择器，
子元素选择器，
相邻兄弟选择器，
组合类选择器

0. !import
1. 内嵌样式style 1000
2. id选择器      0100
3. class选择器/属性选择器/伪类选择器 0010
4. 标签选择器/伪元素选择器 0001
5. 通配符选择器
6. 子选择器(>)， 相邻选择器(+, ~)

相关文章：
- [CSS选择器笔记](http://www.ruanyifeng.com/blog/2009/03/css_selectors.html)
- [CSS 选择器参考手册](http://www.w3school.com.cn/cssref/css_selectors.ASP)
- [优先级是如何计算的](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Specificity)
- [CSS 的优先级机制[总结]](http://www.cnblogs.com/xugang/archive/2010/09/24/1833760.html)
