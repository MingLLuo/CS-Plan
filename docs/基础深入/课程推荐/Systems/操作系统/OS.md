# 操作系统专题

学习操作系统推荐什么路径，我觉得最合适的配方是 MIT6.S081 + OSTEP，有空可以看 jyy 的 OS 系列的授课材料（[B 站](https://space.bilibili.com/202224425)），从绿导师的课中能获得很多骚操作，但当时直接上手 PA 有点描述不清的怪感，写了两个 mini lab 就溜了。记得从 23 年开始，南大很多老师都主动在 B 站分享了他们的授课视频，在此致以敬意。

在看 CLRS 时还跟着[Par4g0N](https://space.bilibili.com/390606417)的算法设计与分析视频学习，动态之前分享的航拍视频好像消失了？

跑题了跑题了

MIT6.S081 的代码量不大，难度主要体现在几个 hard 部分，以及选做的 topics，蛮多朋友在博客与 B 站分享他们实现的思路，在这无法一一列出。我认为仔细了解 xv6 的执行过程，分析源码更有意义，不要刷完就跑。记得 jyy 的 OS 课有带着[学习 xv6](https://www.bilibili.com/video/BV1DY4y1a7YD)，还讲了如何配 VSCode 来 Debug，很有用，评论区也有人分享 solution，可以关注。

相较于 xv6 的 lab 设计，Pintos 会“强迫”你研读源码，很多设计都需要你来会翻看代码，理解源码的实现。提供的注释都很直接，理解起来没什么障碍。

愿意花时间和精力，建议直接冲 CS162，如果有 xv6 的底子，会轻松一些

国内很出名的“银杏书”第二版可以买来当拓展看一看，个人读起来没有阅读国外这些书的顺畅，暂时总结不出原因，如果要读，建议看完 CSAPP，有一些 OS 基础再读

额外可以拓展的有：

- 清华的 rCore
- 以及国外指导操作系统实现的文档
	- [Writing an OS in Rust Philipp Oppermann's blog](https://os.phil-opp.com/)
- ...

还有一本书[《计算机系统开创性经典文献选读与解析》](https://book.douban.com/subject/36470622/)，还专门蹲便宜的时候下单，虽然还是小贵。我个人完全读不下去这类论文解析，选择的论文很经典，但扯来扯去，完全看不懂想要干啥，最近不知道有没有更新，至少当时的感觉就是完全读不下去
