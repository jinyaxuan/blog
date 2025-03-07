---
title: "不要让脑袋里只剩 0 和 1 —— 避免思维固化"
date: 2017-10-15 13:39:52
id: the-world-isnt-only-true-or-false
categories: Documents
tags: []
---

## 0x00 前言

曾经和一位不做技术、但与技术人员有合作的朋友聊天，他作为一名小领导，常和外包程序员打交道。我问他：你觉得做程序员最忌讳什么？他的回答是：

> 不要让脑袋里只剩下是与非、零和一。
>
> 作者：孙伟喆／2017-10-15

## 0x01 问题

那时候不懂这句话的我一心只顾钻研技术，于是追问：何出此言？

> 好多程序员做久了技术，习惯了面对代码，有时候可以明显感觉到他（们）缺乏了一些基本的感性思维。比方说，客户提出的需求，给出的答复总是：我只想要你明确的逻辑，不要跟我讲太多；又或是对于产品经理口中的某个效果，只有两条路：可以实现／实现不了；这让我难以接受。

是啊！世界上的事情怎么会有明确的分界线，人的思维是曲线的，最怕思维固化、一根筋。

## 0x02 分析

回到朋友提出的两个例子：

### 客户构想的需求

*   首先要明白，客户是普通人，不懂代码。
*   其次，客户提出的需求永远只是脑袋中的构想，如何把构想变成现实是你的事情，而不是客户需要思考的东西。
*   作为乙方，我们应该主动协助不懂代码的“小白”客户确定他想要的是什么，客户思维所及只能停留在与技术无关的层次上，那么接下来就需要你带领客户去分析，理清他的逻辑，同时也要思考在技术层面上如何实现。客户不了解在软件行业此类“构想”是如何实现，而我们不懂客户行业内的规则，在你主动带领客户分析需求、对需求“具体化”的时候，客户可以跟得上你的思维，及时修正你所说的是否有所偏差，甚至有可能打开了思路，主动说出某一模块的细节；而这时候，疯狂的记笔记就好了。

关于上面这条理论，有个很典型又类似的例子：

> People don't know what they want until you show it to them. - Steve Jobs
>
> 消费者并不知道自己想要什么，直到我们拿出自己的产品。——史蒂夫·乔布斯

**有兴趣可以看看《乔布斯传》。**

### 上级布置的任务

1.  领导要什么？`结果`。
2.  领导要你干什么？`实现结果的过程`。

常有人和我说：我已经尽力了啊，但是有时候我真的不会，真的完不成，他（Boss）怎么还是训我。

的确，做开发难免遇到实在解决不掉的“坑”，但你有没有想过是自己的问题？我们不妨换个角度，用医生和病人来描述这件事。

> 假设你是一名患者，来医院经过一系列的诊断，医生只告诉你：你没救了。你会转头就走，放弃治疗么？
>
> 同样，老板安排你去做一件事情，你遇到问题只反馈一句：这个我们做不了。那老板是不是也该反问一句：所以我们这个项目就这样不做了？
>
> 作为患者，你一定会继续追问：为什么没救了？医生做了哪些诊断？有没有其他方案可以缓解？……
>
> 而作为医生，也同样有义务提供完善的诊断报告，至少让不懂医学的你，知道自己身体是哪里出了毛病。

回到现实。

老板想要的是结果，你没有达到 Boss 的预期，难道还要他反过来询问你事情的详细经过吗？你是不是应该给出一份报告（哪怕是口头形式），用以说明：

1.  做了哪些尝试？
2.  遇到怎样的困难？
3.  是否还有其他方案？
4.  ……

当有了这样详细的报告，或许老板、甚至团队中的同事，就可以通过你没有的资源、人脉等方方面面，解决掉你尝试过、但行不通的方案。

若是依旧解决不掉，那你也应该提出“缓解”方案。这时候，就需要你明确老板给你安排的工作，背后想要达到的目的是怎样的、他的“刚需”是什么。

所谓条条大路通罗马，目标是死的，人是活的；从“刚需”的角度出发，思考是否有其他“通向罗马”的路。

通常，此时的解决方案目标已经不再是圆满达到预期，而不得不有一定的舍弃，只要舍弃的不是影响大局、刚需、核心利益的东西，都可以列在你的报告里：

1.  是否有“圆滑”的解决方案？
2.  能达到怎样的效果？
3.  所带来的成本多少？代价如何？
4.  ……

至于如何选择，决策权已经全部在老板手里，他只要做个简单的**选择题**即可，而不是**问答题**。

此时，优劣代价已经全部在 Boss 心中有数，接下来你所做的，就是执行老板选择的方案就好。

这才是真正的：“我尽力了”。

**有兴趣可以看看《说话的艺术》。**

## 0x03 拓展

由此，又回到了我平时常常挂在嘴边的理论：

> 立足程序员，眼界高于程序员。

**_立足程序员_**指的是着手当下，把自己应该做的事做好、所要承担的责任承担起来，保证自己写的代码不出问题。

**_高于程序员_**指的是放眼全局，在做程序员的同时多思考：

1.  从同事角度想，自己的代码和别人对接是否方便？有没有可能产生的误会？
2.  从高级程序员角度想，某条代码是不是可以再优化得更完善、更优雅？
3.  从架构师角度想，某块代码是不是可以进行快速重构使其具有更高的扩展性、健壮性、可维护性等等？
4.  从老板角度想，这套系统有没有潜在风险、额外成本或是不确定因素？
5.  从客户角度想，我们的产品是否好用？细节体验是否完美？有没有解决目前核心问题？

这样，才有机会从程序员中脱颖而出，成为受到老板、甚至客户青睐的佼佼者。

## 0x04 思考

为什么会出现这样的问题？

是国内死板的开发流程造就了这样一批不会动脑筋的程序员？

还是从最初的模板式教育就固化了孩子原本多彩多样的思维。

> 文采有限，欢迎批评指正。
