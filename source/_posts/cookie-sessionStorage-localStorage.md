---
title: cookie sessionStorage localStorage三者差别
date: 2017-12-12 14:46:27
tags: [cookie, sessionStorage, localStroage]
---
Cookie, Session storage, Local Storage都是存储在客户端本地机器上的数据
常常被用来进行比较。

所以了，它们三者的区别或者说使用场景是：
当客户端需要与服务器端进行交互时，就用Cookie，就是服务器端设置Cookie，客户端会存储，当客户端再次访问这个接口时，带着Cookie，服务器端就知道了，哦，是你哦，熟人，然后就能顺利拿到接口的相关数据了。

Session storage和Local Storage都是H5新出来的，它们能存储的数据量比Cookie要大，
