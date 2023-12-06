# CS3110:OCaml Programming
  - 开设学校: Cornell University
  - 课程页面: [CS3110](https://cs3110.github.io/textbook/chapters/preface/about.html)
  - 课程视频：[20年公开课程](https://www.youtube.com/watch?v=MUcka_SvhLw&list=PLre5AT9JnKShBOPeuiD9b-I4XROIJhkIU)
  - 对应教程下载: [CS3110 TextBook](https://github.com/cs3110/textbook)

----------------------------


## 内容介绍

> This course is about making you a better programmer.

CS3110是康奈尔大学教授函数式编程的一门课程，使用的语言为OCaml，课程的资源都是公开的，可以在网上找到对应的视频、textbook和对应的答案。

这门课通过学习OCaml,从而学习函数式编程的思想。OCaml将函数式、指令式和面向对象编程统一于类ML的类型系统之下。因此学习这门课程不需要为了使用OCaml而非常熟悉纯函数式编程范型。
所以课程内容适用于各种语言，不必说课程使用的是很老的语言就觉得上了没用，这门课程的核心在于思想，而非语言。

### 函数式编程的特点
- Immutability：函数式编程具有具有函数不变性和数据不变性，函数不变性即函数不能改变其状态，数据不变性即数据不能改变。
- First-Class Functions: 函数可以作为参数传递给其他函数，也可以被赋值为变量，好处是其灵活性高，允许高度的抽象和代码重用，减少冗余代码。
- Pure Functions：与函数不变性对应，即意味着函数的输出只与输入ru有关，不与外界有任何交互。(如修改全局状态或外部变量)
- Higher-Order Functions： 在这门课程可以看到频繁使用的高阶函数，其是接受其他函数组为参数或者返回函数作为结果的函数。通过高阶函数可以和First-Class Functions思想来构建抽象和复用代码。

### OCaml的特点
- 静态类型检查：OCaml是静态类型检查的语言，在编译期时检查类型是否匹配。
- 模式匹配: **Pattern Matching**是OCaml一个显著特性。模式匹配允许程序员以一种声明式的方式检查数据结构，并根据数据的结构和内容执行不同的代码分支
- 类型推论： 编译器可以自动推断变量的数据类型和函数签名，也可以自己指定类型。
- 类型安全: OCaml有个很特别的的一点，就是会在运行时编译器会检查模式匹配是否穷尽了所有可能的情况，从而避免在运行时出现未匹配的情况。

## 个人感想
这门课的内容难度不大，每个单元知识点都有对应的视频观看，同时textbook里的内容也比较详细，我喜欢看textbook的内容来学，但是有的知识点可能只在视频里提到，所以我还是补回了视频的。

我一开始学习OCaml的时候，对其语法有点不适应，然后用多了Pattern Matching语法就发现很神奇，感觉OCaml的语法很简洁，然后通过做OCaml每个章节的Exercises来熟悉。我觉得Exercises是值得去做的，当然如果时间不够的话，可以去看官方提供的[答案](https://github.com/cs3110/textbook-solutions)来看

这门课还教了随机测试的内容，记忆最深的就是Crrectness章节的Black-bbox和Glass-box testing，还有对函数式编程思想非常重要的数学归纳法。有兴趣的朋友可以多看看下这个部分

