# CS 161: Computer Security

- 开设学校：UC Berkeley
- 涉及语言：C, Go, SQL
- 课程页面：[CS161](https://cs161.org)

---

## 主要内容

这门课可划分为操作系统安全，密码安全，网络安全，还有一些扩展

- 操作系统安全主要聚焦于内存安全，学习x86汇编和堆栈相关的概念，它的[Cheat Sheet](https://sp23.cs161.org/assets/projects/1/cheatsheet.pdf)真的很爱

- 密码安全介绍了基本的密码模型范式，一些模型的应用(加密，认证，验证...)，最后一节还介绍了比特币

- 网络部分(分为Web Security和Network Security)介绍了基本的网络模型、协议以及攻击手段

- 还补充了软件安全相关内容，病毒、入侵检测...

## 学习建议

1. 直接看slides的效果可能高于看Recording，每一次Lecture都应该阅读Textbook对应的章节（阅读Slides是个不连续的过程，没有人在旁讲述学习可能不连贯，Textbook就可以很好的帮助你学习）
2. 说了这么多，Textbook值得读
3. Discussion有空可以做完，没空也应该挑一点写
4. HW都开放了就把握住吧～
5. Project2的Ag和Project3是不对外开放，Proj1/2都会有个故事背景，做起来还是挺有趣的？
    - Project1的体量比较小，半天一天就能写完了，学完之后GDB水平大增(然后没用又忘了)
    - Project2需要你设计一个“安全”的文件系统，提供的本地测试不太够，即使是enroll了这门课：`Due to the nature of computer security, the majority of these tests are hidden.`建议找几个朋友一起设计完成这个Project，相互讨论

## 学习心得

- 系统安全的内容很好的巩固了CSAPP中所学的汇编知识，完成Project时还需要参考阅读一篇关于ASLR(Address space layout randomization)的论文，这部分的学习很有趣～
- 密码安全作为这里可能较难的topic，劝退了很多人？(主要是觉得有数学吧hh)我认为这块的知识很有必要了解，哈希/签名/证书等概念是CS人必备的吧，不过这里还是比较浅的，想要深入学习可以找其他资料，[CSCI1515](../密码学/BrownCSCI1515.md)就是一个不错的选择(我们老师说这门课还是很有难度的)。
    - Project2是自己一个人写的，一开始码量不大，基本功能实现的也差不多，但是在细细斟酌之后，就开始了补洞之旅，写测试和代码得有几千行了，最后测试还是有些细节没考虑到。这个Project还是建议合作完成，前期设计时能多考虑到一些内容，这个Project并不会用到Go的太多特性，学习一下语法就可以开始上手了(用的GoLand，体验挺好)
- Web部分的学习倾向于网页及其服务上的攻击，有SQL注入，CSRF(一种伪造手段)...
- 网络部分的学习可以配合着课内的《计算机网络》，不过这里的网络更偏向网络协议，也会介绍关于他们的攻击手段

## 资源分享

- Summer23开放了Spring2023的HW，邀请码为：`G2DR3D`，虽然没有开放lab以及project的autograder，但这个作业的质量整的很好，在你做对时还有解析
- Textbook在介绍DNS时推荐了一个漫画，顺着摸发现了整个[漫画系列](https://dnsimple.com/comics)，主要介绍DNS/HTTPS，跟着看还是很有趣的(还有彩蛋🥲)

### Project2测试范围节选

主要是我在ag上看到的测试要求，供参考

- Design Requirements
    - Keystore Abuse Test: number of public keys (in Keystore) should not depend on the number of files stored, or the length of any file. 
    - Collision Resistance Test: Check for collisions in designs using separators/concats. Designs must use H(a) + "/" + H(b), not H(a + "/" + b), or similar. 
- Functionality [RevokeAccess]
    - Revoke access before a top-level child accepts an invite. 
    - Revoke access before a sub-level child accepts an invite. 
    - A complicated chain of shares & revokes. 
    - Create three different invitations, and then accept the second one that we created. Then, revoke and attempt to re-accept any of the earlier invites. All of the AcceptInvitation calls should fail. 
    - A revoked user's LoadFile should fail. 
- 不列了，相信你们可以考虑到🙃
