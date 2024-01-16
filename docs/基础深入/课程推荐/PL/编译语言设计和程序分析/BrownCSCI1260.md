# Brown CSCI 1260 : Compilers and Program Analysis

- 开设学校：Brown，UC Berkeley([CS164](https://inst.eecs.berkeley.edu/~cs164/))
- 涉及语言：OCaml，x86 assembly，Lisp等
- 课程官网：[Brown CSCI 1260](https://browncs1260.github.io/)
- 课程视频：(不公开，但有录屏，在某处)

---

PS: UCB和Brown在最近的授课中，内容和作业很相近，因此综合在一起介绍。在做hw时，可以提供参考

- Prerequisites:
    - CS 61B. Data Structures
    - CS 61C. Machine Structures

## 课程介绍

> Have you ever wondered why C programs seem to run faster than Python programs? Have you ever been confused by an error message and wondered why Java couldn't understand your program? In CSCI 1260, we'll learn how compilers read in code in one language and produce code in another; in particular, we'll learn how to translate high-level languages to code that your computer's processor can understand. We will get hands-on practice developing compilers for a series of increasingly complex languages. Along the way, we'll learn some general best practices for developing and testing complex software systems.

你是否想过为什么 C 语言程序时常比 Python 程序运行得更快？你是否曾对错误信息感到困惑，并想好奇为什么 Java 无法理解你的程序？在 CSCI 1260 中，我们将学习编译器如何读入一种语言的代码并生成另一种语言的代码；我们将学习如何将高级语言翻译成计算机处理器能够理解的代码。我们将亲身实践，为一系列日益复杂的语言开发编译器。同时，我们还将学习一些开发和测试复杂软件系统的技巧。

## 内容梳理

这门课的安排很像一篇paper ["An Incremental Approach to Compiler Construction"](http://scheme2006.cs.uchicago.edu/11-ghuloum.pdf)，它基于scheme实现了Intel x86架构上的一个编译器，源语言是scheme的子集(是不是很怪qaq)。这篇paper有很多值得拓展与深入讲解的地方，与其配套的还有tutorial及源代码，可以在[这个仓库](https://github.com/namin/inc)里找到。

这门课则基于 OCaml 实现了一个类似的编译器，每节课 Professor 都会现场扩展编译器的功能，并进行讲解，提供的notes也很详细，每年都有一个代码仓库进行课后的代码更新，比如[class-compiler-2023](https://github.com/BrownCS1260/class-compiler-2023)
(实现上还借助C语言实现了runtime.c，诸如打印值之类的操作被简化了)

你或许并不熟悉OCaml，但这门课也会引导你进行语法的学习，并且通过assignment进行练习。在后期完成有关编译器的作业时，你需要自己补充测试(没有公开太多测试)，这或许是个缺陷，但也是个挑战，如果你习惯了面向公开测试debug，经历一下这样子的历练也是不错的选择～(这门课可以面向 Interpreter debug)

在课程中，还介绍并实现了一些编译上的优化(作业也会让我们实现)，比如尾调用(Tail Call)优化，常数折叠，公共子表达式消除(Common subexpression elimination)，寄存器分配等等。

## 碎碎念

这门课除了最后optimization的hw没写，其他应该都做完了～ 

最初学习这门课的私心是再熟练用一用OCaml，写到最后发现也没用到太多高级语法，便跑去读了[RWO](https://realworldocaml.org/)，这门课的学习也不一定那么轻松，对OCaml代码的debug没有直接使用肉眼看汇编和gdb调试来的方便(偶尔会用到utop)

- [What is difference between tail calls and tail recursion?](https://stackoverflow.com/questions/12045299/what-is-difference-between-tail-calls-and-tail-recursion)
