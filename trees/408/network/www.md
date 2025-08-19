
---
title: 万维网与 HTTP 协议
---

万维网 [WWW, World Wide Web], 是一个信息系统, 在这个系统中, 文档和其他资源通过统一资源标识符 [URI, Uniform Resource Identifiers] [^url] 进行标识和互相链接. 用户可以使用网络浏览器访问万维网上的资源. URI 的语法由五个按从左到右重要性递减的组件组成. 

```
URI = scheme ":" ["//" authority] path ["?" query] ["#" fragment]

authority = [userinfo "@"] host [":" port]
```

#### 组成结构

URL (统一资源定位符): 每个网页或资源都有一个唯一的地址, 称为 URL, 它定义了资源的位置和如何访问它.
HTTP/HTTPS (超文本传输协议 / 安全超文本传输协议): 这是用于从服务器传输网页到浏览器的协议.
HTML (超文本标记语言): 大多数网页使用 HTML 编写, 它是用于描述和呈现超文本的标准标记语言.
HTTP 协议

[^url]: 另外, URL [Uniform Resource Locator] 按定义是 URI 的子集, 多见于网页链接. 而 URI 也包括像 ISBN 这样的标识符. URI 方案可以是协议、规范或指定, 如 HTTP、文件或数据. 

#### HTTP 协议

超文本传输协议 [HTTP, Hypertext Transfer Protocol] 是互联网上应用最为广泛的一种网络协议. 它是一个属于应用层的协议, 常基于 TCP/IP 协议通信. HTTP 用于客户端和服务器之间的数据传输, 特别是在万维网 (WWW) 中, 用于传输网页 (HTML 文件) 以及与其关联的资源 (如图片、音频、视频等).

- 无状态. HTTP 本身不保持用户的状态信息, 每个请求都是独立的, 服务器无法识别是不是同一个用户发送的多个请求. 这一点在现实中通常通过 Cookie 和 Session 技术来弥补.

- 组成部分. 
    1. 请求和响应. HTTP 通信通常包括客户端向服务器发送请求, 然后服务器返回响应的过程. 
    1. 方法. HTTP 定义了一组请求方法, 用于表示对资源的不同操作. 
        - `GET`: 请求指定资源. 
        - `POST`: 提交数据以供处理.
        - `PUT`: 更新指定资源.
        - `DELETE`: 删除指定资源.
        - `HEAD`: 与 `GET` 相似, 但只请求资源的头部信息.
        - `OPTIONS`: 获取可以应用于目标资源的通信选项.
        - `PATCH`: 对资源进行部分修改.
        - 其他方法还包括 `CONNECT`, `TRACE` 等.
    1. [状态码](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Status). 响应返回一个状态码, 用于表示请求的结果. 
        - `200 OK`: 请求成功.
        - `400 Bad Request`: 错误请求. 
        - `403 Forbidden`: 客户端无访问权限.  
        - `404 Not Found`: 资源未找到.
        - `500 Internal Server Error`: 服务器内部错误. 
        - 及其他状态码, 用于表示不同的响应状态.
    1. 头部字段: HTTP 请求和响应都包含头部信息, 提供有关请求或响应的元数据, 例如内容类型 [Content-Type] 或 用户代理 [User-Agent].
        - 消息体: 请求或响应的主体部分, 通常包含要传输的数据. 如 `POST` 请求的数据或服务器返回的网页内容. 

#### 长连接和短连接

HTTP 根据首部的 `keepalive` 选项是否被设置被分为长连接和短连接. 

- 长连接 / 持久连接 [persistant connection]. 通过设置 `keepalive` 选项, 可以在一个 TCP 连接中发送多个 HTTP 请求.
- 短连接 / 非持久连接 [multiple connection]. 没有设置 `keepalive` 选项, 那么每一次发送 HTTP 请求都必须单独建立一个 TCP 连接.

在 HTTP/1.0 中, 持久连接不是默认行为. 要在 HTTP/1.0 中启用它, 必须在请求头部添加 `Connection: keep-alive`. 
在 HTTP/1.1 中及之后, 持久连接是默认行为. 如果想关闭它, 必须在请求或响应头部添加 `Connection: close`. 

#### 流水线和非流水线

- 流水线 [pipelining]: HTTP 客户端在未等待前一个请求的响应的情况下, 连续发送多个 HTTP 请求.
- 非流水线 [non-pipelined]: HTTP 客户端必须接收到上一个请求的响应, 才能发送下一个请求.

在 HTTP/1.0 中, 流水线 的功能并不支持.在 HTTP/1.1 中, 引入了 HTTP 流水线 的支持, 但由于使用中队头阻塞 [^head-of-line-blocking] 的问题, 应用并不广泛.在 HTTP/2 中, 进一步改进了请求处理机制, 允许多个请求和响应在同一个连接中并行进行, 解决了队头阻塞的问题.

#### Cookie

HTTP 协议是无状态的, 这意味着每个请求都是独立的, 服务器默认情况下无法知道两个请求是否来自同一客户端或用户. Cookie 的引入使得服务器能够跨多个请求 "识别" 和 "记住" 用户.

HTTP 服务器通过 `Set-Cookie` 首部字段来设置每一个客户端的 Cookie 值, 当浏览器接收到带有 `Set-Cookie` 字段的 HTTP 响应时, 就会存储该 Cookie 字段, 并在下次向对应的服务器发送 HTTP 请求时自动将 Cookie 字段添加在 HTTP 首部. 当 HTTP 服务器接收到带有 Cookie 的请求时, 它就可以区分这个请求是来自于那个客户端的了. 

[^head-of-line-blocking]: 即一列的第一个数据包 (队头) 由于延迟、丢包或慢速响应等原因受阻而导致整列数据包受阻. 在 HTTP/2.0 之前, 只有在完成上一个 HTTP 请求后, 才能发送下一个请求. 但是在 HTTP/2.0 中, 可以并发地发送多个 HTTP 请求, 这些请求被并发地处理. 
