---

title: 【入门系列】CSS 入门
tags: 
  - CSS
---

## 介绍

CSS 全称 Cascading Style Sheets 层叠样式表，是一种样式表的语言，用来描述 HTML 或 XML 文档的呈现。CSS 描述了在屏幕、纸质、音频等媒体上的元素应该如何渲染。



### 优势

- 避免重复
- 更容易维护
- 为不同目的，使用不同的样式而内容相同

!import 是为用户提供的，相对于开发者的样式，浏览器的样式，用户自定义的样式级别最高。



## CSS 声明

![css è¯­æ³ - å£°æ](https://mdn.mozillademos.org/files/16188/css_syntax_-_declaration.png)

![img](https://mdn.mozillademos.org/files/3667/css%20syntax%20-%20declarations%20block.png)

![img](https://mdn.mozillademos.org/files/3668/css%20syntax%20-%20ruleset.png)



## 其他 CSS 语句 

@-规则（At-rules）在 CSS 中被用来传递元数据、条件信息或其他描述信息。

### @media

screen，print，projection，all

@page

### @document 

```css
@document url(https://www.example.com) {
    body {
        background: red;
    }
}
```



### @supports

```css
@supports (条件语句) 检测是否支持某个 CSS 属性，条件语句有3个关键字：or，and，not
```



## 选择器

简单选择器：id，class，tag，*

### 属性选择器

- 存在和值：[attr]，[attr=val]，[attr~=val]
- 子串值：[attr|=val]，[attr^=val]，[attr$=val]，[attr*=val]

### 伪类和伪元素

### 基于关系的选择器

### 组合器 和 多重选择器

### CSS 选择器的优先级



## CSS 是如何工作的？

当浏览器显示文档时，它必须将文档的内容与其样式信息结合。它分为两个阶段：

1. 浏览器先将标 HTML 和 CSS 转化成 DOM，DOM 代表了计算机内存中的相应文档，因为它已经融合了文档内容和相应的样式表。
2. 浏览器显示 DOM 的内容。

![img](https://mdn.mozillademos.org/files/11781/rendering.svg)