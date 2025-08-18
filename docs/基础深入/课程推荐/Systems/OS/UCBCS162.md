# CS162: Operating Systems and Systems Programming

- 开设院校：UC Berkeley
- 涉及语言：C, Rust(选做)
- 课程页面：[cs162.org](https://cs162.eecs.berkeley.edu)

---

不愧是 Pintos...

## 前备知识

- 数据结构：数组、链表、二叉树和散列
- 汇编语言程序设计
- C 语言、GDB 调试
- CPU 缓存、内存层次结构、虚拟内存（CS61C）
- CPU 流水线和基本数字逻辑设计 （CS61C/EECS151）
- 随机变量和概率分布的基本知识（CS70）

## 课程介绍

> The purpose of this course is to teach the design of operating systems and operating systems concepts that appear in other computer systems. Topics we will cover include concepts of operating systems, systems programming, networked and distributed systems, and storage systems, including multiple-program systems (processes, interprocess communication, and synchronization), memory allocation (segmentation, paging), resource allocation and scheduling, file systems, basic networking (sockets, layering, APIs, reliability), transactions, security, and privacy.

本课程的目的是教授操作系统的设计和其他计算机系统中出现的操作系统概念。内容包括操作系统、系统编程、网络和分布式系统以及存储系统的概念，包括多程序系统（进程、进程间通信和同步）、内存分配（分段、分页）、资源分配和调度、文件系统、基本网络（套接字、分层、API、可靠性）、事务、安全和隐私。

能有什么收获？实际操作与设计底层代码，配上很好的教学资源，在 MIT6.S081 的基础上，更加深入地了解操作系统的设计与实现。但性价比高不高，还是要看个人的学习目标，不是所有人愿意抽一周时间写一个 Project，更何况这门课的 Project 有三个。（我能因为几行 typo 坐在电脑前调试一天，是浪费吗？

## 学习建议

~~（一个人自学的话快跑！！！~~

因为不是课内要求，组队完成 Pintos 项目也要考虑契合度。一开始拉人来学（结果没人来，后面发现自己一个人设计，Debug 排错可能还方便一点，毕竟没有学业压力，全靠自觉，线上合作可能变量有点大

CS162 在 Spring2024 最大的变化就是把比较旧的 Vagrant 环境换成了 [Docker](https://github.com/Berkeley-CS162/cs162-workspace)，想起我以前配的环境还有点残留，抽空得把它处理干净，Docker 赛高！

### 排坑

- 正常的 Lecture 等材料一定要重点关注，Discussion 有时候能提供一点设计上的参考
- Lecture 和 OSPP 这本书的内容相搭，如果看课觉得有点不好消化，去看看书就好

#### Homework

- hw-list 和 hw-shell 没有完整的本地测试，可以手工测试
- 关于前三个 hw，我设计了一套[测试框架](https://github.com/MingLLuo/CS162HW-TestScript)（捣鼓了至少半天），hw-http 以及 hw-memory 有本地测试，便没有设计；测试用例参考了 ucb 内部的测试脚本
- hw-http 玩玩 Rust 挺好，至今学不会 Rust，lol
- hw-mapreduce 可以直接跑去看 MIT6.5840 的 lab，之前实现过，这边就撒手没写了
- homework 的进度可以稍微提前，对 Project 设计有很大帮助
- 这一块的难度不大，拿 List 来说，就是想让你了解在 Pintos 中 List 这个模块如何使用，指导你能快速上手（陷入魔掌

#### Project

相较于 xv6，Pintos 更像是提供了个基本框架，写足了测试，剩下的扔给你来实现，像个霸道总裁？现在的 Pintos 还是基于 x86，倒也不用太在意是不是 RISCV。

很推荐大家尝试完成 Pintos，难度会比 MIT6.S081 高一些，但这个经历和收获很宝贵

一个人写项目的精神状态如下：

好诶，开始新的 Project，看看文档，看看源码，打个草稿，直接开工；写完代码，测试没过；面向测试 Debug，开始至暗时刻；测试通过，如沐春风，感觉自己是个奇才 hh，要好好奖励自己；一段时间后，新的 Project 发布....（x2）

（测试通过之后真的可能会很中二的自夸一番，心境真的会有变化，感觉很奇妙。

- CS162 目前有三个 Project（User Programs, Threads, File System）取消了 VM 这个部分，不过 hw-memory 会让你实现 sbrk
- 建议环境选择 Docker SSH + VSCode，Pintos 在 VSCode 的配置可以参考 HW0 的文档，至少代码跳转没有问题，真的很重要。我将 shell 改成了 zsh，配上了 ohmyzsh，如果你选择更换终端，记得复制 bashrc 中的环境变量
- gdb 有些魔法，阅读 Pintos/GDB 专栏，`loadusersymbols`和`dumplist`会是你的好朋友(/home/workspace/.bin/gdb-macros)，printf 和 ASSERT 也是
- Project Thread 中可能会多 smfs 的测试，可以直接删去（src/tests/threads/Make.tests），我暂时没找到实现 smfs 的文档描述，直接换成了 mlfqs（选做），在 Stanford 课上关于实现这部分的[参考](https://web.stanford.edu/~ouster/cgi-bin/cs140-spring20/pintos/pintos_2.html)，一起做了（给自己浇了把油，Debug++
- 选择适合自己的同步原语比较重要，semaphore 和 lock 的选择感觉可以纠结很久，可以到源码中看他们的实现来决定，读写锁我倒是没怎么用过
- C 语言有 goto，在实现 filesys 扩展文件打下，撤销扩展失败申请的 free_map 块会很方便，至今觉得我实现那部分代码很美丽

- 完成部分模块，想要批量测试某个 module，如 filesys/base，你可能会直接删掉其他 TEST_SUBDIRS，虽然编译能成功，但会因为没有初始化模块而报错，我是直接用一些骚操作处理，懒得写一个脚本或者深入探查原因（可能是 userprog 或者 kernel 的初始化模块需要载入磁盘，但删去就没有预先创建，导致报错
- 运行测试时，可能会提示你语言地区设置的问题，可以添加环境变量`export LC_ALL=C.UTF-8`，或者直接在`~/.bashrc` `~/.zshrc`中添加

- 合并测试的测试文件可以参考如下样例，能进行完整的测试

```makefile
# -*- makefile -*-
kernel.bin: DEFINES = -DFILESYS -DTHREADS -DUSERPROG
KERNEL_SUBDIRS = threads devices lib lib/kernel userprog filesys tests/threads tests/userprog/kernel
TEST_SUBDIRS = tests/threads tests/userprog tests/userprog/kernel tests/filesys/base tests/filesys/extended tests/userprog/multithreading
SIMULATOR = --qemu
```

## 资源

- 课程视频大多没有太新，也有朋友提供了 2024Spring 的视频，可以去看看
- [Stanford CS140 Pintos Documentation](https://web.stanford.edu/class/cs140/projects/pintos/pintos.pdf)：去看在线文档排版好一些，这份可以下载的 pdf 信息和 162 的 Pintos Doc 差不多
- 直接按照 CS162 课程的 schedule 学习，配置环境即可，整个过程没有什么障碍
- 每学期结束，CS162 staff 会在某个时间段删除 student0/group0 仓库，最好提前备份完整的，想学又不能学很难受哒 😋
