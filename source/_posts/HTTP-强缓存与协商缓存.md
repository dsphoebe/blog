---
title: HTTP 强缓存与协商缓存
tags:
  - HTTP
date: 2019-01-07 14:11:54
---


强缓存：向浏览器缓存查找该请求结果，并根据该结果的缓存规则来决定是否使用该缓存结果的过程。

强缓存是根据客户的保留的服务器端的 response header 中的字段：expires、cache-control 来控制的。

cache-control 是过期的一个时间长度，expires 是过期的时间点。cache-control 的优先级高于 expires。在无法确定客户端时间是否与服务器端时间同步的情况下，cache-control 相比 expires 是更好的选择，所以如果同时存在时，只有 cache-control 会生效。

Expires 是 HTTP/1.0 控制网页缓存的字段，其值为服务器返回请求结果缓存的到期时间，即再次发起该请求时，如果客户端的时间小于 expires 值，则直接返回缓存结果。

Cache-Control 是在 HTTP/1.1 用于控制网页缓存的字段，常见值：

- public：所有内容都缓存 客户端和代理服务器都可缓存（一般都是设置为这个）
- private：所有内容都缓存 客户端可缓存，默认值
- no-cache：客户端缓存内容，但是是否使用缓存则需要经过协商缓存来验证决定
- no-store：所有内容都不缓存，既不强制缓存也不协商缓存
- max-age=xxx：缓存在 xxx 秒后失效

缓存失效时间计算公式：expirationTime = responseTime + freshnessLifetime - currentAge

协商缓存：在强制缓存失效后，浏览器携带缓存标识向服务器发送请求，由服务器根据缓存标识决定是否使用缓存的过程。

协商缓存的标识 response header 中的字段：Last-Modified / If-Modified-Since、Etag / If-None-Match 来控制的。

Etag / If-None-Match 的优先级高于 Last-Modified / If-Modified-Since。

Last-Modifed 是服务器响应请求时，返回该资源文件在服务器最后被修改的时间

Etag 是服务器响应请求时，返回当前资源文件的一个唯一标识（有服务器生成），客服端再次发起请求时，If-None-Match 携带上次请求返回的唯一标识 Etag 值，If-None-Match 与该资源在服务器的 Etag 值做比较，一致则返回 304，代表资源无更新，继续使用缓存文件；不一致则重新返回资源文件，状态码 200

强制缓存不会发请求到服务器，而协商缓存会发请求到服务器，所以说它两都不会从服务器加载资源数据。