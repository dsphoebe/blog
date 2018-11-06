---
title: 浏览器解析 URL
date: 2017-12-11 23:05:41
tags: [浏览器, URL, BOM]
---
一个 URL 输入后是不是通过浏览器的BOM对象来解析的 URL 了？
一个 URL 也就是BOM的location对象
location对应包含了
- 协议名称protocol: http, https, ftp...
- 用户名: username
- 密码: password
- 主机名: hostname
- 端口: port
- 路径名: pathname
- 查询串: search
- 书签名: hash