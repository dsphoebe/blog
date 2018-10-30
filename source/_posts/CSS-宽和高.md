---
title: CSS 宽和高
tags:
  - CSS
  - 文档流
  - 多行居中
date: 2018-10-29 23:45:07
---

## 块状元素的宽高如何确定？

**单行文字高度由字体的行高决定**。字体设计师会在字体文件里写一个建议行高，所以如果开发者没有设置 line-height，则这个块状元素内部的元素行高就是字体设计师定的建议行高。

虽然可以用 `&nbsp;` (no break space) 来实现多个空格，但是由于空格的宽度也是由字体设计师控制的，比如有的设计师定的空格是 2 个字符，有的设计师定的可能是 2.2 个字符，所以咱们不能用它来实现对齐布局。那咱们如何来实现不同个数的字体对齐了？

如下实现两个字和四个字对齐：

<p data-height="265" data-theme-id="dark" data-slug-hash="zmQqxm" data-default-tab="css,result" data-user="dsphoebe" data-pen-title="两行不同个数字体左右对齐" class="codepen">See the Pen <a href="https://codepen.io/dsphoebe/pen/zmQqxm/">两行不同个数字体左右对齐</a> by dsphoebe (<a href="https://codepen.io/dsphoebe">@dsphoebe</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

HTML 会把内联文本之外的空格删掉，之间的全部空格合并显示为一个空格。如果给元素定义 display:inline-block; 或者 display:inline; 表现出来的效果和上面一样，**HTML 元素之间空格都是显示为一个空格，元素之外的空格不显示**。

如果内联文本很多时，就会到第二行，显示为从左到右，从上到下的排列方式，这种文本流动的方式就称为文档流。

如果在文档流中遇到太长的字符时，会因为过长而另启一行，而且可能太长而导致超出块状元素的宽度。限制它超出可以在合适的位置加上连字符 -，或者定义它的样式为 word-break: break-all;，意思为按照块状元素的宽度切断字符。

### 块状元素内部文本溢出问题

#### 单行文本溢出

<p data-height="265" data-theme-id="dark" data-slug-hash="MPdyVP" data-default-tab="css,result" data-user="dsphoebe" data-pen-title="单行文本溢出" class="codepen">See the Pen <a href="https://codepen.io/dsphoebe/pen/MPdyVP/">单行文本溢出</a> by dsphoebe (<a href="https://codepen.io/dsphoebe">@dsphoebe</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

#### 多行文本溢出

<p data-height="265" data-theme-id="dark" data-slug-hash="EdzKoz" data-default-tab="css,result" data-user="dsphoebe" data-pen-title="多行文本超出部分变成省略号" class="codepen">See the Pen <a href="https://codepen.io/dsphoebe/pen/EdzKoz/">多行文本超出部分变成省略号</a> by dsphoebe (<a href="https://codepen.io/dsphoebe">@dsphoebe</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
