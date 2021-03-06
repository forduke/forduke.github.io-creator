---
title: "HTTP 相关"
date: 2019-11-05T14:37:36+08:00
draft: false
---

### HTTP (HyperText Transfer Protoco)

超文本传输协议（HTTP）是一个用于传输超媒体文档（例如 HTML）的应用层协议。

### URL 概览

以百度搜索 hello 为例

https://www.baidu.com/s?wd=hello&rsv_spt=1#5

协议+域名或 IP+端口号+路径+查询参数+锚点
![URL地址](/image/http/url-1.png)

- **协议：** http:// 是协议。它表明了浏览器必须使用何种协议。它通常都是 HTTP 协议或是 HTTP 协议的安全版，即 HTTPS。Web 需要它们二者之一，但浏览器也知道如何处理其他协议，比如 mailto:（打开邮件客户端）或者 ftp:（处理文件传输）。
- **域名：** www.baidu.com 是域名。它表明正在请求哪个 Web 服务器。
- **端口：** HTTP 协议的标准端口（HTTP 为 80，HTTPS 为 443）通常都不用写，也不会展示。
- **路径：** 上图没有展示，是网络服务器上资源的路径。
- **查询参数：** ?wd=hello&rsv_spt 是提供给网络服务器的额外参数。参数用 & 符号分隔的键/值对列表。
- **锚点** 锚点表示资源中的一种“书签”，给浏览器显示位于该“加书签”位置的内容的方向。**注意！**＃后面的部分（也称为片段标识符）从来没有发送到请求的服务器。

---

### DNS

域名系统（服务）协议（DNS）是一种分布式网络目录服务，主要用于域名与 IP 地址的相互转换，以及控制因特网的电子邮件的发送。DNS 使用 TCP 和 UDP 端口 53。对于每一级域名长度的限制是 63 个字符，域名总长度则不能超过 253 个字符。

---

### nslookup

我查了下这个命令有点多，暂时用不上，如果查网站 IP 就直接
nslookup baidu.com
![nslookup](/image/http/url-2.png)

---

### IP

细节暂时未深入研究~后面学习了再补上

---

### 域名

- com 是顶级域名
- baidu.com 是二级域名（俗称一级域名）
- www.baidu.com 是三级域名（俗称二级）
- 上到下依次是父子关系
