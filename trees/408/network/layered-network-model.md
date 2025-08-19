
---
title: 三种体系结构
---

$\gdef\str#1{\footnotesize{#1}}$
$\gdef\hint#1{{\color{gray}{\str{#1}}}}$

| OSI 的体系结构 [^osi] | TCP/IP 的体系结构 | 五层协议的体系结构 |
| - | - | - |
| 7	[应用层][application] | 4 [应用层][application] [^application-example] | 5 [应用层][application] |
| 6 [表示层][presentation] |
| 5 [会话层][session] |
| 4 [传输层][transport] | 3 [传输层][transport] (TCP 或UDP) | 4 [传输层][transport] |
| 3 [网络层][network] | 2 [网际层][network] IP | 3 [网络层][network] |
| 2 [数据链路层][data-link] |  | 2 [数据链路层][data-link]
| 1 [物理层][physical] | 1 [物理层][physical] [^network-access] | 1 [物理层][physical] |

[application]: ./application-layer.md
[presentation]: ./presentation-layer.md
[session]: ./session-layer.md
[transport]: ./transport-layer.md
[network]: ./network-layer.md
[data-link]: ./data-link-layer.md
[physical]: ./physical-layer.md

[^osi]: OSI 低三层统称为 "通信子网", 它是为了联网而附加的通信设备, 完成数据的传输功能; 高三层统称为 "资源子网", 相当于计算机系统, 完成数据的处理等功能. 传输层承上启下. 

[^application-example]: 应用层协议如 DNS, HTTP, TELNET, SMTP, FTP, RTP 等. 

[^network-access]: 此处有时也用 "网络接口层" 占位, 但这一层并没有具体内容. 和 TCP/IP 的应用层一样, "网络接口层" 涵盖了 OSI 协议中多层的功能. 
