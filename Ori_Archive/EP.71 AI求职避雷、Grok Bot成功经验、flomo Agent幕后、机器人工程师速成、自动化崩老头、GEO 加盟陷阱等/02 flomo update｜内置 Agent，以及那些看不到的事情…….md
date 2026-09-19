# flomo update｜内置 Agent，以及那些看不到的事情……

> 原链: https://mp.weixin.qq.com/s?__biz=MzI0MDA3MjQ2Mg==&mid=2247490716&idx=1&sn=1ab57e48792a6889becaf5d95cb3e0af&chksm=e81efe09e9c9d9cd29371a3857706af108214cceb5d8ebafb4021c006480b5b7909be8de2784  
> 来源: 公众号 · 归档自 EP.71 · 抓取于 2026-09-20  

---

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

过去，flomo 只能以文字承载我们注意力的结果。

但许多让我们有共鸣的事情，是在被追问，被反驳，被联想时形成的。

  


德国社会学家罗萨说过，共鸣是一种自己和世界的关系：**有东西触动你，你能回应，双方都因此变了一点，而且这件事无法强求。**

**  
**

就像我们不经意间听到了一首过去的歌曲，或者在某个时刻想起了某本书中未曾理解的句子一样。或许也可以有一种新的记录方法，把自己尚未清晰的，模糊的想法，和 Agent 探讨，探寻其中的共鸣究竟在何处。

  


在经历了许多波折之后，我们把 Agent 带到了 flomo 里。它记着你过往记录的一切，去追问，去反驳，去联想。

  


我们希望通过它，让那些触动，变成自己具体的行动；让浅显的体验，因共鸣而变成具体的经验；让我们弄清楚自己经历的每件事之间的联系。

  


人生是一连串的事件，当我们知晓事件之间的联系，便不易被风吹散。

  


# **Agent 迭代**

内置 Agent ，在首页输入框旁边（没看到的朋友偏好设置看一眼哦）。

  


不仅可以随时@过往的笔记，或调用技能进行讨论，**还可以识别图片**  —— 试试把你的认知地图分享图发给它，看看有什么惊喜。

  


另外还有全套的定时任务，也已经内置进来。给 flomo 开启手机的推送（Push）功能，就不会错过 Agent 给你发来的提醒啦。

  


对了，别忘了在设置中给它起个名字。以及，拍拍（双击）它的头，看看会有什么表情。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

电脑端 Agent

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

手机端 Agent

  


但这次想讲的，是一些背后的事情，也是最近我们「看起来没什么更新」的主要原因。

  


先说一下 Clawbot 的问题。过去几个月，经它投递的定时任务失败率接近 99%，还有一部分用户的 Clawbot 被静默，连对话都无法响应。

  


我们排查、打听、尝试了各种办法，毫无头绪；开发者社区里同样的反馈，一片沉默。

  


于是我们决定不再等待，**让 Agent 内置在 flomo —— 定时任务的结果直接在 App 里通知你，通知也重新设计过，更醒目 —— 记得去应用市场更新～**

**  
**

另一件事，就是点数消耗问题。前一阵 DeepSeek 涨价让人猝不及防，高峰期消耗会变成原来的 12 倍之多，让已经开发完的模型切换功能只得搁置。

  


但我们并不想涨价，或把成本都转嫁在大家头上。经过一个月的各种努力，我们终于把成本又控制到了涨价前，并且抹平了峰谷计价，开发了重置卡等等……

  


简单来说就是：**不管外面怎么涨价，大家看到这篇文章时，点数和涨价前一样耐用。** 不过有几个细节要交代下：

  1. 记得新建对话（微信内输入 /新建，App 内点新建入口）。

  2. 第一天建立缓存时消耗会略多，之后就好了。

  3. 已经给所有用 Agent 的朋友发了一张重置卡，可用来重置当日额度。入口在购买扩展额度的界面，记得在有效期前使用（消息通知看一眼啊喂）。


![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

重置卡可在购买扩展额度的界面找到

  


未来的，如果服务商继续降价，我们也会持续跟进。

以及，若因为升级模型 & 系统功能导致缓存失效的，我们会继续免费赠送大家重置卡。

  


PS：国庆长假之前，应该能体验到「洞察之后继续追问」了。

  


# **Agent 之外**

在 AI 加持下，flomo 基础功能迭代比之前更快。这里讲几个各平台大家容易感受到的变化，更多的细节会罗列在文末。

  


### Android

我们几乎重新打磨了 Android 的界面，解决了 Android 长期碎片化的问题，并增加了类似玻璃效果的透明质感。让许多不统一的地方（如菜单、按钮、动画等）有了统一的设计语言。这些变化乍一看变化不大，但在许多细节上会更加顺手。

  


之前在 iOS 和 Web 上线的认知地图的 3D 版本，也经过优化呈现在大家面前。即使几年前的手机，用起来也会相当丝滑。

  


对了，不太会看认知地图的话，看看上面 Agent 那段写的小技巧。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

###   


### iOS

除了**全面支持 iOS 27 的液体玻璃** 效果之外，我们也重塑了 iPad 上的体验：

  * 输入框不再小小一块，可以铺满全屏了；

  * 侧边栏也有了自己的「分寸」，不会横屏竖屏时打架；

  * 后续等大家升级到 iOS 27 时，还能在新建笔记时，创建手写笔记（预计本月稍后发布）；




![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

  


iPhone 上则有这些变化：

  * 每日回顾支持了实时活动，可以在锁屏上看到更多文字；也能自由调整小组件文字大小；

  * 长按笔记时，可以连续朗读笔记。试试在每日回顾中朗读一下？

  * 查看相关笔记时，能基于这条笔记继续随机漫步。


![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

###   


### 桌面端

桌面端迎来了不少变化，之前大家反馈许久的宽屏利用率问题，已经在新版本得到了改善，并且支持把 Agent 设置为第三栏。

  


但这次的重点，是我们重写了独立窗口的相关功能：

  * Agent 对话支持单独打开窗口（也支持快捷键哦），这样可以在桌面上随时和它聊天；

  * 新建笔记界面大幅简化，增加草稿提示。并且发布后，笔记可以保持在桌面反复修改；

  * 单独设置为独立窗口的笔记，单击就能进入编辑状态，不用点点了；


![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

  


以及，对许多人来说复杂的多级标签编辑功能，也尝试进行了改善：

  * 可以直接把某个标签向上移动一级；

  * 也可以选择直接把某标签移动到另一个标签下；




这些操作全是图形界面，点点鼠标就能完成。后续，我们也会在其他端部署。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

### 全局体验

  * 历史版本支持恢复附件，图片也不用怕丢了；

  * 复制粘贴全面统一格式，web/桌面菜单支持一键复制了（这个小东西真的很难 🤯）；

  * 编辑器内有序列表超过 100.  时的错位问题，以及各种缩进问题，排版更优雅；

  * AI 洞察支持异步洞察，点了之后关闭 App 也没事；

  * MCP 优化连接稳定性，支持从笔记中读图；

  * 高级搜索功能重塑，操作更简单；

  * PS：鸿蒙版本稍后都会跟进




  


更多可能还有近百项修复，就不一一罗列了。

毕竟这篇文章每个字都是手工敲的，没有复制粘贴。

虽然能看到这里的人不多，但这可能是一种执拗吧 ——

毕竟当你真心对待一件事情的时候，其他人是能感受到的。

  


那么，很期待下次的，见字如面。
