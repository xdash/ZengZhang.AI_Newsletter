# 对话 Today AI

> 原链: https://mp.weixin.qq.com/s/KGkqa0y-DLGMNC9Zu1C9SA  
> 来源: 公众号 · 归档自 EP.72 · 抓取于 2026-10-23  

---

Today.ai 是齐俊元的新作品，定位：**下一代 Personal Agent** 而早在 2014 年，他便买下 today.ai 这个域名，想做一个 AI 个人助理  


[![图片](https://mmbiz.qpic.cn/sz_mmbiz_jpg/jXSGuwJvpdgMfRFyqAprmKm8S7lkqRkicVbkNdanraHicGxMRwlzzFJhpUF6vagZ6h7W2UmqkrYwAibDTWzzDWfBUib6lv87gc7cbbczzq1D2dM/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1#imgIndex=0)](https://mp.weixin.qq.com/mp/appmsg/show?__biz=MjM5OTY1NTgyMg==&appmsgid=10014306&itemidx=1&sign=9f50f66121180bd04596ae0de938b2f3&mpshare=1&scene=21&srcid=0820z1TVYemKV81Sj9uZHB2M&sharer_shareinfo=68eb06569f4d84dacbe822b9e7c76a68&sharer_shareinfo_first=bca4da611d51bfc42b3bacb80a359460#wechat_redirect)

今天 Today AI 海外版已上线，而国内版也将正式发布

![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/jXSGuwJvpdhcVD5pCmHdXBRqvCEAV3IFrYrWvoDiaDXdTa2tGeE6qHPdBQoc906deRXp63CiaCzCeAUtepndDxsMjichKjgPLdeJqOVcfQPBcI/640?wx_fmt=png&from=appmsg&tp=webp&wxfrom=5&wx_lazy=1#imgIndex=1)

  


今天我恰好来了西岸梦中心，便在中午去了他们的办公室，和团队聊了一个多小时，想知道他们是如何构建这套 Agent 的

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)Today 办公室入口

我最想知道的是，Today 对 Personal Agent 的理解，跟其他产品有什么不同？团队给出的答案是：**长程 Memory 和 主动性 Proactive**

很多 Agent 的使用从一个具体任务开始：我提出需求，它调用工具，交付结果。Today 想让助理长期围绕同一个人工作，对你的了解会随着使用不断积累，影响后面的安排，也帮助它判断下一件值得做的事  


这次交流，我们主要聊了两个问题：它怎样了解一个人，又怎样利用这些了解去主动提供帮助

本文【不涉及任何实测】，只是我从 Today 团队的取经

  


## Agent 如何更懂你

“拿到日历和邮箱权限之后，一个 Agent 就了解你了吗？”这个问题是 Today 团队问我的

收到一封邮件，很多时候意味着别人想让你做什么，比如要卖给你东西、约你见面、让你处理事情；而你主动发出去的邮件，则更可能在介绍自己、表达需求、作出承诺，是自己的意图

这些东西，都是 Agent 能获得到的明面信息

但如果是一个人类秘书，也会同时关心到邮箱里的行为信息，比如某个来源的邮件，你一直不读，这也是信息。但没读未必就是不感兴趣，过去的兴趣也未必一直有效

“如果只是写一个很通用的提示词，让模型把它认为重要的事情记下来，通常效果很差。”即便拿到同一个邮箱，两个 Agent 形成的记忆和建议，仍然可能很不一样

Today 团队有个判断：**记忆系系统需要针对具体场景设计** ，收集哪些信息、怎样理解人的行为、什么值得记下来，都要把对场景的理解放进去Today 会把这些对用户的了解整理在 Memories 里，记录个人背景和偏好。后续的交互与反馈会继续修正这份记忆，再影响下一次的建议和行动

![记忆如何围绕工作、健康、旅行和学习组织（产品示例）](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)记忆如何围绕工作、健康、旅行和学习组织（产品示例）

听到这，我会好奇：“我看到这里有很多先验经验，人只负责给反馈，我们会不会越来越像一家数据标注公司？”对于我的这个猜测，Today 团队并不认同，并跟我说：“这依然是产品经理的工作：你很懂一个领域，就把这种理解放进产品，让更多用户受益”比如，发件箱里的信息值得多看一些，阅读行为也值得记录。这些观察会影响系统收集什么、怎样组织记忆，最后怎样使用它

于是我换了一个说法：**先验经验之于 harness，如同数据之于模型** 他们觉得这个说法更接近：**模型可以一样，对人的理解不一样，做出来的助理就会有差别**

  


##  北极星指标

我问他们，如果从产品运营的视角，Persoal Agent 的北极星指标会是什么？答案是 DAU

用户主动发起 query 的次数，优先级会放得非常低。他们最关心的是，Agent 主动帮用户解决了哪些问题  


“我们做的是主动性的 Agent，希望用户在开口之前，Agent 就直接把事情做了”如果助理已经了解我的日程、偏好和正在推进的事情，这些了解就应该用起来，减少我每天重新交代的部分  


我一直觉得：对时间的感知，是 Personal Agent 很重要的一部分。它得知道你原本准备做什么，也得知道今天发生了什么变化

Today 的产品示例里有这样一个场景：你昨晚睡了不到六小时，上午十点又有品牌评审，它会问，要不要把今天的长距离散步挪到晚上，先准备评审文档

Memory 给 Proactive 提供了依据

这里用到的既有原来的计划，也有新发生的情况。Today 也会提前整理当天的简报，让用户打开产品时，就能看到今天要处理的事情

  


![主动帮助与持续任务（产品示例）](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)主动帮助与持续任务（产品示例）

  


## 用 Today 替代自己的外教

Suki 是 Today 的 pm，她与我分享了自己学外语的过程“比如我的 Today 给我做了个性化外语课程，完全根据我现在的水平来。我们先做一轮测试，测试完，它给我建很多 scheduled tasks，告诉我星期一学什么、星期二和星期三学什么。”“它会根据我的反馈调整课程计划。比如我说最近不想学这些单词，想难度更高一点，或者换一个 topic，第二天课程计划就会调整。它个性化的地方，是这个教程完全 for 我一个人”

而在日常中，Suki 也会让 Today 把生活里的熟人编进课程，成为里面的角色。后来发现自己更喜欢互动学习，又让它做了一个拼词游戏“我觉得整个过程完全替代了我的外教老师”

你会发现，这其实也是一个找需求的思路：**看人们原来在为什么花钱** 就比如我们找 1v1 的教练，无论是英语外教，亦或是健身教练，他们都会先了解你的水平、再安排课程、跟进学习，再根据反馈调整，这点恰好也是 Agent 现在就能干的

一个 Personal AI 要参与到普遍生活，可以从一个具体需求开始获取人的习惯，用户再逐渐扩大自己的使用范围。比如用户可能是为了学外语来的，后来又让它帮忙安排旅行。旅行要去哪里，什么时候出发，会影响前面的学习计划；原来对这个人的了解，也就有了更多用处

  


## 路在何方

对于工作 Agent 来说，代码写得能不能跑是很容易评估的但对于个人 Agent 来说，情况就大不一样

生活场景是开放世界的问题，而且有很多主观判断，比如这个例子：“帮我给邻居发邮件，让他别再吵了”假定邮件发出去了，这个 task 算成功了吗？或许未必。我的真实需求并非「发出邮件」，而是「让他别吵」

对于这个事情的处理，人的喜好、双方关系...等等一系列因素会影响 Agent 的行动路径，**这又回到了我们前面聊的先验经验**

我这两年一直有一种虚无感，便也将这个问题抛给了 Today 团队：今天做一个东西，可能还没走完产品周期，就被下一轮能力变化颠覆了，那产品团队今天应该把力气花在哪里？

Today 的联合创始人高策老师给出的答案，依然是 Memory 和 Proactive

在他看来，一个用户长期以来是什么样的人，最近发生了什么，什么事情值得主动去做，都需要产品持续组织和使用相关信息，不能只靠模型当下的 working memory

  


## 附：12 年前的畅想

下面这些内容，是齐俊元在 2014 年写下的，摘录在此  


  


移动互联网对人们生活的改变确实巨大

产品经理离开了电子日历 就会忘记自己一天要参加的会议

妈妈离开了代办事项应用 就会忘记缴水电费

媒体编辑离开了电子阅读器 就会疏忽一天最重要的新闻

  


但这么多的应用 真的让我们的生活更轻松吗

以我自己为例 我的代办事项清单已经堆了满满几百项 连点开的勇气都没有

待阅软件更是连数字都已经没法显示 直接是一个无穷大的符号

原因却很简单 这是事没有在我应当处理的时候去做 后来就不断拖延 日复一日 终于成为再也无法撬动的巨大石阵

  


所以 我们的团队开始打造一款产品

希望它能够比你更了解一天要做的所有事情

从琐碎的代办事项到重要的工作任务

从轻松的个人约会到严肃的公司会议

甚至是需要阅读的每一篇文章

然后由它 温柔地提醒你 眼下你该处理什么事

  


我们对它的期待很简单 就是它应当足够简单易用

无论是谁第一次见到它 都能够不假思索地创建一个日程 添加一个任务

  


我们对它有一个基本的要求 它要适应你既有的习惯

如果你习惯于使用谷歌日历 它能够和谷歌日历同步 并且按时提醒你

如果你习惯于使用 Teambition 进行项目管理 那么它不仅让你看到项目中所有的任务 并且能让你和项目成员共同讨论

如果你习惯于使用 Pocket 存储希望仔细阅读的文章 它理应提供一样的阅读体验 并且更加专注

  


我们对它有一个美好的期待 希望它不仅让你的生活变得有效率 而且还更精彩

当日的科技要闻 周末的设计沙龙 当月的创业者活动 等等

只要简单的订阅 它就会自动地在合适的时候提醒你参加

  


我们对它有一个远大的梦想 希望它如此聪明 能够成为你的助手

  


经过几个月的设计研发 它已初具形态 并成为了我自己每天早晨第一个查看的应用

所以我们给它起名 「今天」 希望它可以让你的今天不同于昨天
