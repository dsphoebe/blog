---
title: cookie sessionStorage localStorage
date: 2017-12-12 14:46:27
tags: [cookie, sessionStorage, localStroage]
---
Cookie, Session storage, Local Storage都是存储在客户端本地机器上的数据。
常常被用来进行比较。

前端通过document.cookie获取/设置，Cookie的设置/获取以及cookie的属性值（path，domain，expires，secure）的设置都是键值对的字符串进行修改更新；关闭浏览器后就失效了。
服务器端设置，通过HTTP头与客户端进行交互，确定用户。还有一点时如果服务器设置了http only，前端是无法通过document.cookie获取到的。
Cookie的最大存储空间很小，最多可设置50个键值对，各浏览器不同，数据量一共不能超过4kb。
如果前端操作cookie，可以用已经封装好了的小型库，比如 [cookie操作简易库]。(https://developer.mozilla.org/en-US/docs/Web/API/Document/cookie/Simple_document.cookie_framework)

Session storage和Local Storage都是H5新出来的，它们能存储的数据量比Cookie要大，能存储5mb的数据。当键值修改或者clear时，会触发storage事件。

localStorage是永久保存的，除非覆盖/清除
sessionStorage是关闭会话或者浏览器就会被清除

sessionStorage场景？

相关文章
- [HTTP cookies 详解](http://blog.csdn.net/lijing198997/article/details/9378047)
- [Document.cookie](https://developer.mozilla.org/zh-CN/docs/Web/API/Document/cookie)
- [详说 Cookie, LocalStorage 与 SessionStorage](http://jerryzou.com/posts/cookie-and-web-storage/)
