---
layout: post
title:  linux学习心得（三）
category: linux 
---

* toc
{:toc}

# Linux参考资源

# 环境变量

设置环境变量的方法：

1）临时的：使用export命令声明即可，变量在关闭shell时失效。示例如下：

`export PATH=/home/xyz/bin:$PATH;`

2）永久的：需要修改配置文件，变量永久生效。

在/etc/profile文件中添加变量（对所有用户生效）。修改文件后要想马上生效，还要运行`source /etc/profile`，不然只能在下次重进此用户时生效。

在用户目录下的.bash_profile文件中增加变量（对该用户生效）。同样需要source才能马上生效。

重要的环境变量：

PATH：可执行文件路径。

LD_LIBRARY_PATH：动态链接库文件路径

## tldr

tldr是一个采用示例说明的简化版的man。

官网：

http://tldr.sh/

该项目原生支持node.js，但也提供了其他多种语言的支持。

参考：

https://linuxtoy.org/archives/tldr.html

tldr: 简读Manpage

## 下载工具

wget和curl是最常见的下载工具。这里推荐使用axel，该工具支持多路http下载。

示例：

`wget -c <URL>`

`curl -C -o <file name> <URL>`

`axel <URL>`

参考：

http://os.51cto.com/art/201605/511423.htm

Linux用户宝典：用于下载的十大命令行工具

### NFS

#### 客户端

`mount -t nfs 192.168.0.1:/tmp /mnt/nfs`

挂载NFS。挂载点（即上例中的/mnt/nfs）必须事先创建。

`mount: /bak: bad option; for several filesystems (e.g. nfs, cifs) you might need a /sbin/mount.<type> helper program`

出现上面的问题，需要：

`sudo apt install nfs-common libnfs-utils`

#### 服务器端

```bash
sudo apt install nfs-server
cd /
sudo mkdir nfs-server
sudo chmod 777 nfs-server
sudo chmod 666 /etc/exports
echo "/nfs-server *(rw,sync,no_root_squash)">>/etc/exports
sudo service nfs-server restart
```

参考：

https://www.cnblogs.com/tu13/p/ubuntu_nfs.html

ubuntu18.04搭建NFS服务器

## OpenGrok

OpenGrok是一个阅读源码的Web系统。

官网：

http://oracle.github.io/opengrok/

代码：

https://github.com/oracle/opengrok

参考：

http://mazhuang.org/2016/12/14/rtfsc-with-opengrok/

搭建大型源码阅读环境——使用OpenGrok

## ELF & PE

![](/images/img4/exe.png)

https://zhuanlan.zhihu.com/p/254882216

深入浅出ELF

https://mp.weixin.qq.com/s/vnqANjTMNqdjkHXl203eRg

逆向工程基础：从PE文件到进程地址空间

https://mp.weixin.qq.com/s/_RD_jY-gJFxlT9DX2jGDAA

只有170字节，最小的64位Hello World程序这样写成

## 同步锁

read-write lock、RCU lock、spin lock

对于悲观锁，开发者认为数据发送时发生并发冲突的概率很大，所以每次进行读操作前都会上锁。

对于乐观锁，开发者认为数据发送时发生并发冲突的概率不大，所以读操作前不上锁。

到了写操作时才会进行判断，数据在此期间是否被其他线程修改。如果发生修改，那就返回写入失败；如果没有被修改，那就执行修改操作，返回修改成功。

乐观锁一般采用Compare And Swap（CAS）算法进行实现。

比较并交换(compare and swap, CAS)，是原子操作的一种，可用于在多线程编程中实现不被打断的数据交换操作，从而避免多线程同时改写某一数据时由于执行顺序不确定性以及中断的不可预知性产生的数据不一致问题。

https://mp.weixin.qq.com/s/mTOzcdjaak-z6ypL9MR2Lw

小白科普：悲观锁和乐观锁

https://mp.weixin.qq.com/s/t-jZ9GoqW46rU3t9ahHqCQ

mysql悲观锁总结和实践

https://mp.weixin.qq.com/s/6MRi_UEcMybKn4YXi6qWng

操作系统中锁的实现原理

https://mp.weixin.qq.com/s/yHSraIAYsjYWPaGXA3PijA

一张图读懂非公平锁与公平锁

https://mp.weixin.qq.com/s/qnZL4ENAbTvVMVcImVTtYw

深入浅出CAS

https://mp.weixin.qq.com/s/T_z2_gsYfs6A-XjVTVV_uQ

说说无锁(Lock-Free)编程那些事（上）

https://mp.weixin.qq.com/s/h75n7sHnrmoLJ4DVAW5AUQ

说说无锁(Lock-Free)编程那些事（下）

https://blog.csdn.net/zqz_zqz/article/details/70233767

java中的锁--偏向锁、轻量级锁、自旋锁、重量级锁

https://mp.weixin.qq.com/s/muSUJuE1A45UTXpWTeFxOA

24张图带你彻底理解Java中的21种锁

https://mp.weixin.qq.com/s/gbCshU5eEn4Gefduk1zdCQ

浅谈Java并发下的乐观锁

## 参考

https://mp.weixin.qq.com/s/n6D5_6K9TrnuXg3h6AiFNA

华为“鸿蒙”所涉及的微内核到底是什么？一文带你认识微内核

![](/images/img3/Monolithic_vs_Micro.jpg)

![](/images/img3/UNIX.jpg)

----

https://mp.weixin.qq.com/s/I7C7cXFgxO7RO0Wpjjj3xQ

一篇文章带你“重新认识”线程上下文切换怎么玩儿

https://www.cnblogs.com/liqiuhao/p/9450093.html

关于TOCTTOU攻击的简介

https://mp.weixin.qq.com/s/2QAm6F109LV2koC64xIpqA

简直不要太硬了！一文带你彻底理解文件系统

https://mp.weixin.qq.com/s/0jR4Y3sT8RRW7FYEOmBsXg

一口气搞懂文件系统，就靠这25张图了

https://mp.weixin.qq.com/s/Y_GYtL9m3zmY-5VZMbCfWg

Linux中用户的简介与管理

https://linux.cn/article-8290-1.html

漫画赏析：Linux内核到底长啥样

https://mp.weixin.qq.com/s/IucIsbJPo4eUUopV8xNN9w

图解Linux程序的链接原理

https://mp.weixin.qq.com/s/zBtdhjAOjwcJbGluccwOlA

我和面试官之间关于操作系统的一场对弈！写了很久，希望对你有帮助！

https://mp.weixin.qq.com/s/3Pp7wkDO6Rnxb5aZP0sacw

一文了解操作系统I/O

https://mp.weixin.qq.com/s/xM8uvYbX6VY8MVZrYkvCUg

链接选项rpath的原理和应用

https://juejin.im/post/5e8844996fb9a03c6675b9d6

我们按下电脑开机键的背后发生了什么？

https://mp.weixin.qq.com/s/DCqkgksOHa81EI-I0oaZvg

Linux下9种优秀的代码比对工具推荐

https://zhuanlan.zhihu.com/p/162366167

Linux下C++so热更新

https://mp.weixin.qq.com/s/rH7WqriomFTA55ecacV8Gw

键盘敲入A字母时，操作系统期间发生了什么...

https://mp.weixin.qq.com/s/vDlWCVK8knxPf5HoqmtZyQ

从创建进程到进入main函数，发生了什么？

https://mp.weixin.qq.com/s/4ZdnacKuqkpWTso6P1Rmjg

如何调试多线程程序

https://mp.weixin.qq.com/s/8DNyicMcycUL3RRAiKAz8g

Linux进程必知必会

https://mp.weixin.qq.com/s/EkScI-WCdjLz1g2ec6nkhQ

理解格式化原理

https://mp.weixin.qq.com/s/Sqpp82FhZEC8HkeVHzk9QA

5万字、97张图总结操作系统核心知识点

https://mp.weixin.qq.com/s/SYlaIkuXBqFrbZ-gDMYqtA

高并发高性能服务器是如何实现的

https://mp.weixin.qq.com/s/73eaj0qvhUFWGbDA4H2MNQ

读取文件时，程序经历了什么？

https://mp.weixin.qq.com/s/Y8YZzkuzVr_ti6skHpd1NA

Linux网络包接收过程的监控与调优

https://mp.weixin.qq.com/s/4tAxQ0auQfv5x7Dh3B-85g

Linux内存管理

https://mp.weixin.qq.com/s/jDPxu6IVo3_VpK5l6_-jdQ

Linux系统内存知识

http://www.ruanyifeng.com/blog/2013/04/processes_and_threads.html

进程与线程的一个简单解释

https://mp.weixin.qq.com/s/zVi45pZka_kPpKIoNXNVBA

当初我要是这么学习“进程和线程”就好了

https://mp.weixin.qq.com/s/A8TnhOFLQOhEqphE760yvw

15个相见恨晚的Linux神器，你可能一个都没见过

https://mp.weixin.qq.com/s/ejGjsGA1ijPP--j3BLcEFA

Linux并发与同步

https://mp.weixin.qq.com/s/CAPU8bjJWobQs6JHHMasvQ

Linux服务端最大并发数是多少？

http://www.ruanyifeng.com/blog/2016/03/systemd-tutorial-part-two.html

Systemd入门教程：实战篇

https://mp.weixin.qq.com/s/bPqnaMqhi_4p1mwjmvyoIw

多图详解10大高性能开发核心技术

https://mp.weixin.qq.com/s/wmzwvnOToqCkKJz5yw-USQ

低调的Linux文件系统家族

https://mp.weixin.qq.com/s/ESLO1RH6Q8udwI13Z2Pz_w

详解linux io flush

https://mp.weixin.qq.com/s/LLlzPB2emr9Hqr7gql0B4Q

为什么Linux需要Swapping

https://mp.weixin.qq.com/s/fzLcAkYwKhj-9hgoVkTzaw

CPU飙高，系统性能问题如何排查？

https://mp.weixin.qq.com/s/IcEP-JGQbWA7s7yPdIC9vA

80%时间屏蔽了中断，实时性还有救么？

https://mp.weixin.qq.com/s/iKfWSfzauzNjcAvXPNhq0Q

这些算法都不会还学什么操作系统

https://mp.weixin.qq.com/s/gj6Zw8SvOdSZqRx8KP9wWw

20张图揭开内存管理的迷雾，瞬间豁然开朗

https://mp.weixin.qq.com/s/IQYUNzVgSOFUHB9c1SM0Bw

10张图22段代码，万字长文带你搞懂虚拟内存模型和malloc内部原理

http://www.ruanyifeng.com/blog/2016/03/systemd-tutorial-commands.html

Systemd入门教程：命令篇

https://mp.weixin.qq.com/s/xOqXM5kFi0CzilDg0EXFKg

Linux内核源码规范解析

https://mp.weixin.qq.com/s/QB-IHiCIWEu3bALm2Dp46Q

操作系统课程知识结构

https://www.zhihu.com/answer/460715569

生产力应用大汇总

https://mp.weixin.qq.com/s/QsgoONKwI7ds8Hnx2Wer6A

Linux从程序到进程

https://mp.weixin.qq.com/s/tguC-WOleKRWLfTmGdJlQg

Linux文件系统的实现

https://www.cnblogs.com/biyeymyhjob/archive/2012/07/20/2601655.html

Linux写时拷贝技术(copy-on-write)

https://zhuanlan.zhihu.com/p/296207162

Linux I/O原理和Zero-copy技术全面揭秘

https://mp.weixin.qq.com/s/cudK2dhw4jNr7I34luVKVw

终于有人把零拷贝Zero-Copy讲懂了

https://mp.weixin.qq.com/s/MNzSES3dlMuiwkffLWJGIg

文件系统：隐匿在Linux背后的机制

https://mp.weixin.qq.com/s/1JiXL1f3SSjsBojlJSNOpQ

Linux的启动流程

https://mp.weixin.qq.com/s/ZfprFQjVANuCE2N693gZBQ

用户空间和内核空间

https://mp.weixin.qq.com/s/oKtu3AA9D3y--xMDQ8EARw

携程一次Dubbo连接超时问题的排查

https://mp.weixin.qq.com/s/4o_cSzWeJdLJMObJBhaZlw

计算机系统中的内存

https://www.jianshu.com/p/fad3339e3448

浅析Linux中的零拷贝技术

https://mp.weixin.qq.com/s/6R8UcLLjm9gdWud-eNHztw

中断及其初始化

https://mp.weixin.qq.com/s/qwouMWc4CFtqG_jra4xbIg

IDT及中断处理的实现

https://mp.weixin.qq.com/s/pRsXWAv7wgYcN_jlzcA2YA

内存都没了，还能运行程序？

https://mp.weixin.qq.com/s/snQ3T86usv4rXz0MMQvFfQ

如何回答性能优化的问题，才能打动阿里面试官？

https://www.cnblogs.com/zhouyu629/p/3734494.html

一次心惊肉跳的服务器误删文件的恢复过程

https://mp.weixin.qq.com/s/5iyWeSeDzuA2cY7YBMhk7w

MMU那些事儿

https://mp.weixin.qq.com/s/0OeeYUgBBVVMtxscvzgJHw

i++是线程安全的吗？

https://mp.weixin.qq.com/s/U0qr1oZYXBBmZnC5vsKYLQ

浅谈linux IO