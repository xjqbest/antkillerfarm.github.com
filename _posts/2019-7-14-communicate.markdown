---
layout: post
title:  通信协议, 传感器
category: resource 
---

* toc
{:toc}

# 通信协议

## HTTPS

https://mp.weixin.qq.com/s/C68icGtwh3IzuUbANaRXEg

也许，这样理解HTTPS更容易

https://mp.weixin.qq.com/s/ewI7sHDFj1AHaNAtBDM8uA

HTTPS到底加密了什么？

https://mp.weixin.qq.com/s/IcpaoCU6WXYRTqOuC4AmKQ

用信鸽来解释HTTPS

https://mp.weixin.qq.com/s/Yn2yJ-tQOIvwr1YJZabFuw

HTTPS协议

https://mp.weixin.qq.com/s/oydBIAEqAswppme6ku70fQ

https加密那点事

https://mp.weixin.qq.com/s/iN8NQd8SuWL4gCWhRbY6tg

图解基于HTTPS的DNS

https://mp.weixin.qq.com/s/Yj5NqRJG48kKX2kNnmj9yw

20张图彻底弄懂HTTPS的原理！

https://segmentfault.com/a/1190000023936425

为什么HTTPS是安全的

https://mp.weixin.qq.com/s/BIPbe_jJr3Xm0tBi-YEAEQ

可怕，原来HTTPS也没用

## TCP

所谓粘包就是连续给对端发送两个或者两个以上的数据包，对端在一次收取中可能收到的数据包大于1个，大于1个，可能是几个（包括一个）包加上某个包的部分，或者干脆就是几个完整的包在一起。当然，也可能收到的数据只是一个包的部分，这种情况一般也叫半包。

https://mp.weixin.qq.com/s/sbBhBowAfhnaydErmoTxDg

TCP协议如何解决粘包、半包问题

----

https://mp.weixin.qq.com/s/zU1Mw3yaNmk4D5pP9vxxaw

TCP三次握手和SYN攻击

https://mp.weixin.qq.com/s/3VqdjEK4QkER4Q05JgfjhQ

详解TCP之滑动窗口

https://mp.weixin.qq.com/s/yH3PzGEFopbpA-jw4MythQ

TCP三次握手原理，你真的理解吗？

https://mp.weixin.qq.com/s/ct3wknW9b9oZBoXwZTh-Fg

面试官问我：一个TCP连接可以发多少个HTTP请求？我竟然回答不上来...

https://zhuanlan.zhihu.com/p/101702312

详解TCP超时与重传机制

https://mp.weixin.qq.com/s/dPgA9HKkkqDo_W7Q1qVCoQ

肝完这篇TCP/IP，我就去面试去

https://mp.weixin.qq.com/s/bt0vGltG9OAIWMk8iEQzew

15张图，把TCP/IP讲得一清二楚！

https://mp.weixin.qq.com/s/q6WWwNoXMDA3UI8XacYsBQ

TCP：一个悲伤的故事

## DNS

https://mp.weixin.qq.com/s/DDk5YZv9Q7CaqdiKvQxZGQ

从理论到实践，全方位认识DNS（理论篇）

https://mp.weixin.qq.com/s/rZU35kVTXs5ebf7k6lnheQ

从理论到实践，全方位认识DNS（实践篇）

https://mp.weixin.qq.com/s/dVY0tPgkUq3W5waVtITFUA

一文看懂：网址，URL，域名，IP地址，DNS，域名解析

https://mp.weixin.qq.com/s/cSWjUlO-TaBrqnkt-IK6hA

一文讲懂什么是vlan、三层交换机、网关、DNS、子网掩码、MAC地址

https://mp.weixin.qq.com/s/1x1tUuPJ0fkiPj0G_uTSmg

美国如果把根域名服务器封了，中国会从网络上消失？

## URI

URI = Universal Resource Identifier

URL = Universal Resource Locator

URN = Universal Resource Name

个人的身份证号就是URN，个人的家庭地址就是URL，URN可以唯一标识一个人，而URL可以告诉邮递员怎么把货送到你手里。

参考：

https://blog.csdn.net/koflance/article/details/79635240

URL和URI的区别

## QUIC

Quic全称quick udp internet connection，“快速UDP互联网连接”，是由google提出的使用udp进行多路并发传输的协议。

Quic相比现在广泛应用的http2+tcp+tls协议有如下优势：

1.减少了TCP三次握手及TLS握手时间。

2.改进的拥塞控制。

3.避免队头阻塞的多路复用。

4.连接迁移。

5.前向冗余纠错。

参考：

https://mp.weixin.qq.com/s/vpz6bp3PT1IDzZervyOfqw

QUIC协议原理分析

https://mp.weixin.qq.com/s/Bm_4M-QCcWYRqv1V8a-J-A

QUIC协议原理浅解

https://mp.weixin.qq.com/s/_RAXrlGPeN_3D6dhJFf6Qg

让互联网更快的协议，QUIC在腾讯的实践及性能优化

https://zhuanlan.zhihu.com/p/68012355

HTTP/3竟然基于UDP，HTTP协议这些年都经历了啥？（HTTP/3之前名为HTTP-over-QUIC）

https://mp.weixin.qq.com/s/fy84edOix5tGgcvdFkJi2w

一文读懂HTTP/1 HTTP/2 HTTP/3

https://mp.weixin.qq.com/s/unzge23Aw0jrvBST-iW0Qw

HTTP/3的过去、现在和未来

https://mp.weixin.qq.com/s/MHYMOYHqhrAbQ0xtTkV2ig

HTTP/3原理实战

https://mp.weixin.qq.com/s/DiaruzlgPPKmJCiBg19_og

为什么HTTP3.0使用UDP协议

https://mp.weixin.qq.com/s/uNXxyPZ5IssZfgFFD-m5dQ

什么是HTTP简史

https://mp.weixin.qq.com/s/A4OYoKFVu2nZCyDJcoFrQA

从HTTP到HTTP/3的发展简史

https://mp.weixin.qq.com/s/Mwom82Wwzo4pK9uGSNdfSQ

xxxxHub都用上了HTTP/2，它牛逼在哪？

https://mp.weixin.qq.com/s/E4H3iQRoH0baybSPuGS7Fw

我的HTTP/1.1好慢啊！

## 参考

https://www.cnblogs.com/maybe2030/p/4781555.html

计算机网络基础知识总结

https://mp.weixin.qq.com/s/_bWOYpZNjA4p7ZWM1J_4mw

通信协议之序列化

https://mp.weixin.qq.com/s/CP_Egs4LUx7I8BXSqrS_dQ

互联网协议入门（一）

https://mp.weixin.qq.com/s/KoqN7Dq1aLhqEFAJP8V0KA

66条计算机网络的知识点

https://mp.weixin.qq.com/s/Lee4DRNCQuGCTTAsSYR8ng

高性能网络编程之accept建立连接

https://mp.weixin.qq.com/s/PAuijOCx8TLCsyU_RGs11w

从TCP协议的原理来谈谈rst复位攻击

https://mp.weixin.qq.com/s/W_JjnDuinmLrahIpPY8h-g

tcp服务端一直sleep，客户端发送数据问题总结

https://mp.weixin.qq.com/s/bUrTDj1atJSZvFeWA8H-SA

正向代理和反向代理

https://mp.weixin.qq.com/s/YQfk9lqHbepG2om7mEGTSg

如何给女朋友解释什么是反向代理？

https://zhuanlan.zhihu.com/p/32615963

什么是IPFS?(一)

https://zhuanlan.zhihu.com/p/32633235

什么是IPFS?(二)

https://zhuanlan.zhihu.com/p/32651288

什么是IPFS?(三)

https://mp.weixin.qq.com/s/F6hZpIDqxSCs0ZZ5_6fsMg

HTTP/2协议的优点解析

https://mp.weixin.qq.com/s/3-6T0YS0UsbWndu1xgrW_A

白话Session与Cookie：从经营杂货店开始

https://mp.weixin.qq.com/s/JyPuFauAycot6bvvaunNlw

把cookie聊清楚

https://mp.weixin.qq.com/s/Btlj2A329KUbRU9It79OKQ

面试环节：在浏览器输入URL回车之后发生了什么？

https://mp.weixin.qq.com/s/Mc7vpJw5r_vcbsxLXwfeNA

看完这篇HTTP，跟面试官扯皮就没问题了

https://mp.weixin.qq.com/s/LKB66Ap_L4LedJ72DcXZig

图解ARP协议（一）

https://mp.weixin.qq.com/s/5J_8hD0DnCaX4ksgsgTjHA

大量的TIME_WAIT状态连接怎么处理？

https://mp.weixin.qq.com/s/urwS1dFAZsBG0Kyl8YgLpQ

GET和POST请求的本质区别是什么

https://mp.weixin.qq.com/s/o9zxzklBOFyNkOPMR4gdnA

想避免重复请求/并发请求？这样处理才足够优雅

https://mp.weixin.qq.com/s/_wUoGwcSlJeaMH0JSjNbeA

直接用IP访问知乎，我发现了一个秘密···

# 传感器

这里主要讨论自动驾驶方面的传感器，但也包括了一些非自动驾驶类的传感器知识。

## 激光雷达

https://mp.weixin.qq.com/s/biiTHllmpsKSgMiaZbBYrQ

激光雷达科普文

https://mp.weixin.qq.com/s/4HNaS8Dpi9pcPzE_nN-BvA

全球12家顶级激光雷达公司解读：谁有机会撼动Velodyne

https://mp.weixin.qq.com/s/Ef6aWgs9xkHaAwTX4rxjKA

用激光雷达感知世界

https://mp.weixin.qq.com/s/mlwDZ1DUDbHIn4hQvkumAw

自动驾驶感知神器——激光雷达概述

https://mp.weixin.qq.com/s/hVhutvHeXsZOvJZfG1xaFw

自动驾驶车载激光雷达技术现状分析

https://mp.weixin.qq.com/s/zX2Jy5a32AVnhOUeLgS_wA

摄像头、雷达、激光雷达——自动驾驶几大传感器系统大揭秘

https://mp.weixin.qq.com/s/ecqeQdOo3xUV-PvL_T48eA

一文读懂三角法和TOF激光雷达

https://mp.weixin.qq.com/s/kO5yy7x0r3LhttBhLVpT5w

固态激光雷达研究进展

https://mp.weixin.qq.com/s/1MAb4tZfY4qQPaodo3xHoA

激光雷达原理

https://mp.weixin.qq.com/s/4zW8ZW90v6pLYb6B8RurMg

聊传感器激光雷达

## 参考

https://mp.weixin.qq.com/s/Ee18sjKXNGMowKwqLB0jVg

给自动驾驶一双"通天眼"——环境感知器篇

https://mp.weixin.qq.com/s/dusPUCjKUzhfmTRhzXte-A

新的图像传感器给汽车装上眼睛

https://mp.weixin.qq.com/s/45xNWa_32DAsKdlfYY_QfA

Uber自动驾驶撞死行人视频公布：无人车环境感知解决方案该如何优化？

https://mp.weixin.qq.com/s/VBpOwGrTPs0nlmTyXvqDwA

为什么只用摄像头和光学雷达是不够的：我们能从Uber的自动驾驶车致死事件中学到什么

https://mp.weixin.qq.com/s/WiS-iJHA1zoIyb1cvKiuZQ

自动驾驶传感器“一哥之争”，这事儿你怎么看？

https://mp.weixin.qq.com/s/WWm1tkCXVJgdlVbsXCTYIg

自动驾驶汽车硬件系统概述

https://mp.weixin.qq.com/s/C77q2LEA-lMEabtsO30LxQ

自动驾驶需要几个camera

https://mp.weixin.qq.com/s/2-PB-5tTNeGPLPHQBdRwBA

40张动态图详解全部传感器工作原理

https://mp.weixin.qq.com/s/oCEeIM_DhmQ67zT_KLVb7Q

Face ID与3D传感技术科普

https://blog.csdn.net/carson2005/article/details/72972414

光纤陀螺简介

https://mp.weixin.qq.com/s/ZRakGZWXlQaUgtMfe2c2aw

不要轻易碰我，不然我就知道你有多软了

>鲍哲南，女，1970年生，芝加哥大学博士（1995）。现为Stanford教授，美国工程院院士。

https://mp.weixin.qq.com/s/NwptdxWiN4SadjUQafA5rw

高端MEMS固体波动陀螺的发展与应用

https://blog.csdn.net/richard_liujh/article/details/49615395

光学心率测量原理

https://mp.weixin.qq.com/s/NrNojDc9gEU3F_GybKA67Q

三大屏下指纹技术方案对比

https://mp.weixin.qq.com/s/g5VKcxcp6QWesfegcU_GuQ

手机指纹解锁和密码解锁，哪个更安全？

https://mp.weixin.qq.com/s/2TKkoWZcYVVvlEKvA6iNyA

近年值得关注的新兴MEMS和传感器技术

https://mp.weixin.qq.com/s/elSezCSBPnuEqOFmHACLVg

24GHz雷达的应用案例

https://mp.weixin.qq.com/s/SgUcLH3kfRVha661PLyMeg

体声波(BAW)是什么？

https://mp.weixin.qq.com/s/FohJ81sPT_Zk7s1qLuP1-A

动态视觉传感器（DVS）：高级自动驾驶的“超眼”

https://mp.weixin.qq.com/s/ya-CHw572C2nnk8XraEMqQ

功率半导体器件现状及未来

https://mp.weixin.qq.com/s/bNhd7owOIdCdzO2xOtBMRw

谈谈超结功率半导体器件

https://mp.weixin.qq.com/s/0K595c2GdhPrdWBgpvU-Gw

超声波雷达在汽车上的应用

https://mp.weixin.qq.com/s/j0-Lj8lOyDP0RArB7NzUNw

特斯拉的整车传感器配置方案

https://mp.weixin.qq.com/s/WIjbYMvMis-YBr_ev_wjmQ

霍尔元件及其应用

https://mp.weixin.qq.com/s/vbTR1A0rgzCQY8XG70SNPQ

了不起的MEMS发明人

https://mp.weixin.qq.com/s/ns8riNkUILB-y07VMtGhSw

MEMS培训讲义

https://mp.weixin.qq.com/s/gHvvMG7D_W0M2RFntyRaDw

车载抬头显示AR HUD成像技术大解密

https://mp.weixin.qq.com/s/qOnMNbA9C7bcwZ6IvOxyCA

一组动图看懂3D打印原理

https://mp.weixin.qq.com/s/oN6n7GXnqASKBbVS54rfGg

陀螺仪工作原理及其厂家

https://mp.weixin.qq.com/s/iMHYjOyF7MiAEqhwLwqRYA

日本的传感器之王（基恩士）
