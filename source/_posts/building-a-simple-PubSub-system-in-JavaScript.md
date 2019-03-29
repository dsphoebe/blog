---
title: 译：EventTarget 到 PubSub
date: 2019-03-30 01:27:42
tags:
---

> 原文链接：[Building a simple PubSub system in JavaScript](https://paul.kinlan.me/building-a-pubsub-api-in-javascript/)

最近在开发一个 Web push 服务项目，需要让 UI 响应应用程序级别的事件。因为有几个组件需要来自系统的信息，又不互相依赖。我希望他们能独立于"业务逻辑"管理自己。

我查看了很多工具，但是我是一个严重的 NIH 综合症患者，最后我决定写一个简单的发布订阅模式来完成我的需求，嗯，我发现它非常符合我的需求。

我在想我是否应该使用 DOM 事件，这个DOM 已经提供给开发这的基本属性：用 addEventListener 来监听事件。
但是有一个问题是：必须把事件绑定到 DOM 元素或者 window 上。因为 JavaScript 没有提供给你其他继承自 EventTarget 的模型。

思考：将 EventTarget 作为一个对象可以不用创建自定义 PubSub 系统。🤔

跟着这个思路，一个初略大致的代码如下（ps：先不考虑代码的可执行性）

```js
/* When a user added, do something useful like update UI */
EventManager.subsribe('useradd', function(user) {
    console.log(user);
});

/* The UI submits the data, lets publish the event. */
form.onsubmit(function(e) {
    e.preventDefault();
    
    // do something with user fields.
    
    EventManager.publish('useradd', user);
});
```

Redux 和其他一些系统也是用这个思路来做的，在许多情况下来帮助我们管理 state。
我并不是需要一个状态隔离的模型的 state。

我自己实现一个，对我来说它实现起来很简单：

```js
    var EventManager = new (
        function() {
            var events = {};
            
            this.publish = function(name, data) {
                var handlers = events[name];
                if (!!handlers === false) return;
                handlers.forEach(function(handler) {
                    handlers.forEach(function(handler) {
                        handler.call(this, data);
                    });
                });
            };
            
            this.subscribe = function(name, handler) {
                var handlers = events[name];
                if (!!handlers === false) {
                    handlers = events[name] = [];
                }
                handlers.push(handler);
            };
            
            this.unsubscribe = function(name, handler) {
                var handlers = events[name];
                if (!!handers === false) return;
                
                var handlerIdx = handlers.indexOf(handler);
                handlers.splice(handlerIdx);
            };
        }
    );
```

看起来会有很多 bug，但我喜欢。如果你感兴趣的话，我已经 push 到 [GitHub](https://github.com/PaulKinlan/EventManager) 上了。