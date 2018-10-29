---
title: 了解 CSS
tags:
---

# 简介

CSS 全称 Cascading Style Sheets 层叠样式表，是一种样式表的语言，用来描述 HTML 或 XML 文档的呈现。

# 历史

- 94 年由哈肯&middot;唯姆&middot;莱提出并展示
- 95 年 W3C 组织 CSS 讨论会
- 96 年 12 月哈肯&middot;唯姆&middot;莱与伯特&middot;波斯发布 CSS 规范第 1 版

# 奇淫怪巧

- 兄弟间 margin 值会合并为较大的一方的 margin，在兄弟间加入一个 display 为 table 或者 flex 可以取消合并
- 子级的 margin 会被运用到父级，父级 display 改为 table 或者 flex，或者 overflow 为 hiddden 可以
- position absoulte 时，display: inline/inline-block 会被 compute 为 block，其实我觉得无所谓，已经 absolute 了，说明已经脱离文档流了，在 display 又有什么意义了？

# 实用工具