# CSCI 0300: Fundamentals of Computer Systems

- 开设学校：Brown University
- 涉及语言：C, C++
- 课程页面：[CSCI 0300](https://cs.brown.edu/courses/csci0300)

---

## 介绍

正如首页所说，这门课将会从硬件层到网络层，讲述计算机系统背后的“魔法”
> This is a great class for students who are interested in learning **what** systems programming is, **how** systems work, and **why** these systems are so critical to modern technology.

通过这门课的学习，我们可以：

- 了解真实的计算机工作原理：理解程序运行的过程
- 利用现代的编程工具进行学习(C/C++)
- 通过课程设计的每个项目，实现操作系统的核心，实现一个分布式系统...
- ...

整个课程分为四个Block：

1. **Computer Systems Basics**
2. **Fundamentals of Operating Systems**
3. **Concurrency and parallel programming**
4. **Distributed systems**

选用的参考教材及介绍如下

-   **The C Programming Language** by Brian W. Kernighan and Dennis M. Ritchie (also known as "K&R"; Prentice Hall PTR, ISBN 0-13-110362-8) is _the_ classic textbook for programming in C.
-   **Computer Systems: A Programmer's Perspective, Third Edition** (also knows as "CS:APP3e") by Randal E. Bryant and David R. O'Hallaron (Pearson, 2015, ISBN 978-0134092669). This is a long, comprehensive textbook, and provides a background reference for the lecture material. If you would like to read about the same concepts explained in different words, or read beyond what we talk about in lectures, this will be a good starting point.

## 配套资源

- 全网没有公开的视频资源，但是每节课所配套的note都含括了知识要点(有没有视频都不会影响这门课的学习)
- 几乎所有的Lab和Project都拥有本地测试。Lab0会指引配置统一的学习环境(支持Arm架构，苹果用户大喜)。
- 每个Lab所设置的内容也十分有趣，Makefile的配置；学会使用检测内存泄漏的工具，使用gdb；学习x86-64汇编；了解多线程的编程，认识并使用一些简化网络服务和分布式系统的编程工具(如Protobuf,gRPC)...
- 当然，最有趣的还是设置的6个project，熟悉C语言编程，制作一个内存管理工具，实现缓存的I/O，深入虚拟内存及进程的学习，加深对多线程编程的理解，实现一个分布式系统。
- 当然，有趣归有趣，其难度也是较大的，这是门比较“冷门”的课程，且配置lab及project时会自动完成Github Classroom的配置，全网几乎没有公开答案。有时候一个Lab的学习可以用上一天，更别说Project了，在完成Project的时候需要正确的判断，否则会陷入题目的陷阱，认认真真学习这些内容对自己的代码能力绝对能有提升。
- 在首页点击Resource还可以浏览对应Topic下的习题及解析，灵活考察了所学的内容，可以作为复习的材料

## 建议

- 希望你有一定的体系结构基础(阅读过或准备阅读CSAPP，或者学习过CS61C...)
- 你需要有勇气与时间来学习这门课程，因为你可能会因为第一个Project就被劝退
- 灵活运用一些库函数，多多查阅相关文档
- 你还可以参考哈佛的[CS61](https://cs61.seas.harvard.edu/)进行学习
- 有任何问题，可以在这里交流，[Q群:923303787](https://qm.qq.com/cgi-bin/qm/qr?k=sU0ssPHZKh3C_NccUczFhBiPyPKhq6ph&authKey=YTGoicI3MKLNMmQKh08P0fTWkKUrv7gNz4ABi/CdcOatILb9YKC+0rR1Zy8gFBrL&noverify=0)
