### 「没有人性」是数字员工最大的优势。

1/ 不知是谁最先把「AI 语音输入」呼作「口喷」的，我至今都觉得过于粗俗，难以接受，透着一股老登感，看到这样讲的都想立马关掉。 那么问题来了，还能叫什么呢？口输？口敲？口谕？语控？舌灿？吟唱…？

2/ 最近愈发觉得「观点」不值钱，分享自己真实做（出）了什么才值钱。 于是写了脚本帮我过滤社媒信息（有图，发在 [即刻的](https://m.okjike.com/originalPosts/6a0a7de1af7695b4cfa858a9)、[X 的](https://x.com/XDash/status/2056205552120971718)）。从每天混迹的社媒抓来的几千条数据中，排除掉上面链接的图 1 所示例的干扰项，仅保留图 2 的。 拿最近两周的几万条数据实际跑了下，最终噪音比例高达 99.2%。可谓「他人即地狱」的数据具象化。

3/ 老同事为了女儿学英文，做了个专注英系合称自然拼读的项目：[拼读树](https://www.pindushu.com/)。友情推荐一下，适合 3-8 岁小朋友。

Subscribed

以下是本期正文，Enjoy:

* * *

##### ▪️CASE 案例

### **[制造豆包：一个 AI 超级入口的形成与转向](https://mp.weixin.qq.com/s?__biz=MzU3Mjk1OTQ0Ng==&mid=2247536071&idx=1&sn=e7dccce6e8f01599c27aa131f2cb3d23)**

##### via 郑可书

晚点最新一篇值得看的深度报道，讲了字节跳动做的豆包，幕后一些发展历程中的坎坷故事。它的增长正面临一个根本矛盾：**用户越多，推理成本越高，收入却没同步涨。**

豆包的成功延续了今日头条和抖音验证过的方法论：**顺应人性、依赖数据、极速迭代。**

负责人朱骏把「拟人化」定义为「类似人的温度」，从品牌名到图标都强调亲密感。

但行业信念正在动摇——「AI 聊天机器人将成为一切入口」的判断可能被改写。Anthropic 在编程和智能体上的突破，已经威胁到 OpenAI 的地位。

此外，它的投放成本远低于腾讯元宝和阿里千问，这让它迅速起量。但问题也随之而来——开启付费订阅计划后，用户吐槽「笨还收费」，复杂任务处理不行，团队不得不紧急修复。

这场仗没那么好打。字节的方法论惯性很强，但似乎 AI 技术迭代的速度更残酷。

* * *

### **[我把多 Agent 协作搬进 Hermes Kanban，才发现群聊派活真的不够用了](https://mp.weixin.qq.com/s?__biz=Mzk0ODM5NTEyNA==&mid=2247505962&idx=1&sn=6322706214ec38fcfec146aa666e0df2)**

##### via 孟健的 AI 编程认知

[![](https://substackcdn.com/image/fetch/$s_!WpQL!,w_1456,c_limit,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9112489d-9608-4386-96cd-d9c3661dae37_1200x649.heic)](https://substackcdn.com/image/fetch/$s_!WpQL!,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9112489d-9608-4386-96cd-d9c3661dae37_1200x649.heic)

多 Agent 协作最难的不是让它们跑起来，而是便于追踪进展，以及让任务不丢。

作者孟健把整套流程从聊天窗口搬进 Hermes Kanban 看板后，才意识到之前的「群聊派活」有多脆弱——状态不可见，恢复成本高，长链路协作随时可能断掉。

于是，他尝试采用了 Hermes Kanban 这个工具体系，任务终于不再是聊天里的一次函数调用，而是**看板里一张持久化的卡片：包含描述、状态、产物路径和阻塞原因** 。

看板作为事实源，Telegram 仅做可见性。每个 Agent 只看自己 lane 里的 ready 任务，执行后必须写清交付物路径、关键结论和下一棒。推不动了？明确标记 blocked，而不是一直显示 running。

他举了个视觉返工的例子：设计 Agent 在卡片里记录失败原因与 fallback 方案，产品验收 Agent 核对后创建前端任务卡，前端 Agent 严格按合同执行不擅自优化，QA 按严重程度报告问题并创建修复卡。人类仅在关键节点介入。

* * *

### **[如何创建一套可商用的 AI 上下文体系](https://writewithai.substack.com/p/full-guide-how-to-create-a-master)**

##### via Dickie Bush

作者 Dickie Bush 过去几个月 AI 使用时间增加了 100%，但产出提升了超过 500%。关键做法是构建了一套让 AI 深度理解其业务的文档集。

这 8 份文档分别是：**Money Model Builder（定价与盈利模型）、Perfect Avatar Map（目标客户画像与痛点）、Belief Ladder（客户购买前的信念链）、Acquisition Blueprint（获客漏斗）、North Star Brief（使命与运营原则）、Org Chart Builder（组织架构）、Tech Stack Inventory（技术栈清单）以及「What Good Looks Like」Vault（最佳内容与语气范例）** 。

他强调，这套系统让每次输出所需的编辑和修正工作量大幅减少。一小时内可以按此框架搭建自己的上下文文件夹。

* * *

### **[重生之我是崇祯，但满朝文武皆 AI](https://mp.weixin.qq.com/s?__biz=MzkyNjU2ODM2NQ==&mid=2247628785&idx=1&sn=24140ee834b510c6b29aa649186ed3a9)**

##### via 董道力

[![](https://substackcdn.com/image/fetch/$s_!gCbl!,w_1456,c_limit,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb3173772-8872-4506-a9dd-53a49a6fde51_1100x551.heic)](https://substackcdn.com/image/fetch/$s_!gCbl!,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb3173772-8872-4506-a9dd-53a49a6fde51_1100x551.heic)

这篇介绍了个很有意思的 AI 独立游戏。

制作人追青是独立开发者，没有大厂背景。他做的《历史模拟器：崇祯》中，玩家扮演崇祯帝，通过调整财政（税收政策）、民心（民间疾苦）、军心（军队士气）这些可量化数值来影响历史走向——**不是通过预设剧本，是 AI 实时推演** 。

团队不到 10 人，从立项到上线用了 6 个月。**核心壁垒是自研的推演系统：约束大模型将玩家圣旨翻译成具体状态变量，并引发连锁危机，而不是简单喂史料。**

游戏定价 48 元，玩家需购买额外 AI 推演额度。上线一周收到 700 多条评测，评价「褒贬不一」——玩家认可新鲜度，但集中吐槽稳定性与扣费问题。

**追青给「AI 原生游戏」下了个定义：剥离 AI 模块后核心玩法无法运行。** 他选择明末，是因为史料丰富且具话题度。他判断，随着模型性能提升，约束条件可以更宽泛，但当前仍需工程架构来保障推演效果。

* * *

##### ▪️OPINION 观点

### **[用 AI 构建一家能自我进化的公司](https://mp.weixin.qq.com/s?__biz=MzI1MTUxNzgxMA==&mid=2247502112&idx=1&sn=a2199493b978a80574f985a8738bdc15)**

##### via 刘小排

YC 出了两门课，讲同一个观点：AI 时代公司应该从第一天起就按「AI 原生」的方式搭建。但中美创业者的理解，完全不在一个频道上。

  * 硅谷前沿创业者强调 Capability——「AI 在很多能力上远比我厉害」，目标是最大化发挥 AI 的全部能力。

  * 国内创业者仍停留在 Productivity——琢磨「如何用 AI 提效 20%」，隐含假设是「我比 AI 厉害」。

**YC 的激进判断是「1 个人 + AI = 1000 个谷歌工程师」。** 这意味着公司不再需要那么多人类节点转发信息，而应重组为一组递归、自我改进的 AI 闭环——信息被捕获进入公司大脑，被 Agent 理解、调用、修复、更新，甚至能在创始人睡觉时继续变好。

刘小排用两个比喻展开：旧公司像罗马军团，靠人类层级传递信息，中层本质上充当人肉路由器。Copilot 是错误的心智模型，只看到蒸汽机让马车跑快，却没看到铁路即将到来。

* * *

### **[Anthropic 创始人手册：如何打造一家 AI Native 公司](https://mp.weixin.qq.com/s?__biz=MzIyNjM2MzQyNg==&mid=2247722768&idx=1&sn=dcd8f2ecd4308b8b6c1e2026282534fb)**

##### via Anthropic 团队

Anthropic 出了份创始人手册，教你怎么做 AI Native 公司。这篇文章是个导读（完整中文翻译/英文原版见下方）。

手册将 AI 带来的变化划分为四个阶段：**创意、MVP、发布和规模化。** 核心判断是：**AI 降低的是执行门槛，而非判断门槛。最危险的不是做不出产品，而是太快做出了没人需要的东西。**

小团队正借助 AI 获得过去大公司的组织能力。未来竞争的差异将不再是人数多寡，而是谁更会指挥 AI。

但护城河已经变了。它不再只是模型能力，而是**领域知识、用户数据飞轮和工作流锁定** 这三者的结合。尤其是工作流锁定——能让切换成本从换工具，变成重建一套工作方式。

**延伸阅读：**

  * **[完整中文翻译](https://mp.weixin.qq.com/s?__biz=MzkzNDQxOTU2MQ==&mid=2247517029&idx=1&sn=cd8a2ed31807452cd30035a9054221e7&poc_token=HMxjDmqjd0rT3pJ-ZXSGpLuwpScbM5mza27L8Aun)**

  * **[英文原版](http://claude.com/blog/the-founders-playbook)**

* * *

### **[「我有 10 个 AI 员工」，提供的不是生产力，是当老板的爽感，和对权力的幻想](https://mp.weixin.qq.com/s?__biz=MzI2OTkzMjQxMw==&mid=2247492798&idx=1&sn=f6b5b6d80588e0dc3824525e7b41b795)**

##### via 李自然

有人给 AI 包装了一层「数字员工」的概念，听起来很爽。但李自然说：这本质上是在满足人的控制欲和拟人化本能，不是解决真实的工程问题。

他认为，真正高效的 AI 使用方法是把 Agent 视为函数调用——核心在于上下文隔离、用完即弃、按模型能力档位分工。**一个干净的上下文包，远比岗位描述重要。Agent 干完活就应返回结果并释放资源，主线程必须保持清醒的决策权。**

他用「赛博朝廷」项目举例：720 行 Python 代码模拟朝堂议政很有趣，但多个 Agent 指向同一模型，无法产生真正的多视角制衡——**只会制造氛围感，而不是生产力** 。

简单任务用便宜模型，复杂判断用 SOTA 模型，才是真正的分工。想用 AI 干正事，应专注于任务打包和上下文流向控制，而不是沉迷于当老板的权力幻想。

* * *

### **[上周做了场内部分享，关于我做 AI 这三年来总结的内容创作方法论](https://mp.weixin.qq.com/s?__biz=MzIyMzA5NjEyMA==&mid=2647682309&idx=1&sn=aa02004fb326c8311493fd3ed24a5294)**

##### via 数字生命卡兹克

数字生命卡兹克是三年从零做到百万粉的内容创作者。他刚做了场内部分享，总结了做内容的核心方法论：三步——获取信息、找角度、创作。

关键在于第一步。他强调，获取信息不能只局限在 AI 领域，**要像投资组合一样跨领域配置，从综艺、电影、历史中汲取叙事技巧和视角。** 真正的创新发生在不同领域的交叉点上。

怎么找角度？他举了个例子：有个金融从业者把自己研究陌生领域的方法论整理成了一个 Prompt，用了两年。这本质上是把「如何获取信息」本身给系统化了。

他还提出，将原始信息加工成能打动人的故事，才是内容的价值所在。否则只是没有灵魂的信息搬运。创作者应以广度拓宽武器库，以垂直深度建立专业壁垒。

* * *

### 随便看看：

  * **[《Coding 的中场战事》](https://mp.weixin.qq.com/s?__biz=MzkxOTAyNjAwOA==&mid=2247555207&idx=1&sn=28e4daa6cd26c7395a78c7361e6aa7cf)** ：几家 AI 编程产品截至目前的发展历史梳理。

  * **[《「养虾」两个月，我卖出五个数字员工》](https://mp.weixin.qq.com/s?__biz=MzU2MzQzOTg1Nw==&mid=2247522962&idx=1&sn=5ff5c18fbf853720e16403b2969f682a)** ：有个矿业公司数据分析师，用 OpenClaw 训练了五个数字员工，卖给律所、期货公司、水务公司、电商企业。

  * **[《FA 眼中的 AI 人才战：2000 投资人蹲路演，700 万年薪抢应届生》](https://mp.weixin.qq.com/s?__biz=Mzk0MDYyMDA0NQ==&mid=2247492394&idx=1&sn=713eadc315fe8a514716516caaad8187)** ：2000 个投资人蹲在路演现场，应届生年薪总包从 300 万被抬到 700 万。这是 AI 创投圈的现状。

  * **[《一个作家患上了 AI 依赖症》](https://mp.weixin.qq.com/s?__biz=MzAwMjE1NjcxMg==&mid=2654840713&idx=2&sn=2008c02351e70966965f47be0c8490f5)** ：作者燕草是职业撰稿人，写了十年商业报道。她在创作中逐渐把 AI 当成深度对话伙伴，发现它在理论分析、定制化表达和倾听能力上远超预期。

  * **[《连测 91 天：豆包爱引用什么内容？答案有点反常识》](https://mp.weixin.qq.com/s?__biz=MzAwMjE1NjcxMg==&mid=2654840779&idx=2&sn=68da2f8d7b50b9031771d340219d657b)** ：新榜智汇通过 91 天连续监测「6000 元游戏笔记本」这个问题，共收集 3925 篇信源，发现引用次数前 10 的信源中，无一篇来自抖音或今日头条。排名第一的是一篇技术社区文章。

  * **[《抖快红 B 上最火的 AI 博主，在赚钱了吗？》](https://mp.weixin.qq.com/s?__biz=MzI0MjM2NTY4Mw==&mid=2247592364&idx=1&sn=7fbadc7bf0e8eba3c0c6478a9df7953e)** ：抖音、快手、小红书、B 站的 AI 博主，格局初步形成。AI 工具测评与科普类（秋芝 2046）踩中「流量快」和「变现稳」两个商业逻辑；AIGC 创作类（荒蛋记录员、WAI-你听）以创意为灵魂，能承载情感共鸣，具备破圈传播和品牌合作潜力；AI 虚拟博主类（鹅娘、Yuri 尤栗）通过人设养成获得商业确定性，Yuri 已获得官方身份认证并接到品牌合作；硬核技术与开发类由专业人士主导。能打动大众情感的内容天然具备商业想象空间。

### 适合个人上手的教程/评测/资源：

  * **[《.4k Stars！用 Claude Code 写论文的全套流水线，有人打包开源了》](https://www.36kr.com/p/3812800346742274)** ：学术研究场景里，幻觉和谄媚是系统性问题。一套名为 ARS 的 Claude Code 技能包，通过 4 个 skill 将学术研究从研究、写作、审稿到定稿串成全自动流水线。

  * **[《40 分钟学会 Codex！「零基础」终级教程》](https://podwise.ai/dashboard/episodes/8031872)** ：秋芝最新的 Codex 使用教程。

  * **[《我宣布：Codex 比 ChatGPT 还好用！》](https://mp.weixin.qq.com/s?__biz=MjgzMTAwODI0MA==&mid=2652452485&idx=1&sn=e19436cda48459fb8f50090d7f3898c3)** ：OpenAI 将 Codex 从桌面端扩展至手机端，使其成为能远程控制电脑的 Agent 产品，而不仅仅是写代码工具。iOS 和 Android 用户可预览使用，通过手机即可查看实时运行环境、审阅输出、批准命令、切换模型、发起新任务，所有实际操作均在本地或远程服务器上运行。

  * **[《刚刚，微信聊天记录能喂给 AI 了，我让它爬楼、砍价、整理信息》](https://www.36kr.com/p/3807409070398976)** ：腾讯推出了将微信聊天记录一键转发至元宝 AI 的功能。

  * **[《分享一个 Skill：如何找到值得做的创业 idea》](https://mp.weixin.qq.com/s?__biz=MzA4NzgzMjA4MQ==&mid=2453484238&idx=1&sn=ad64ad290131dc64af4117c9e0b3e474)** ：作者 J0hn 为高效扫描赚钱信号，使用 AI 浏览器 Tabbit，并创建了「每日机会扫描」Skill，让 AI 代理自动规划策略、搜索、提取信息并输出结构化的机会评估报告。

  * **[《踢飞信息焦虑找回阅读快乐，我给微信读书 Skill 做个大升级》](https://mp.weixin.qq.com/s?__biz=Mzg3MTk3NzYzNw==&mid=2247507153&idx=1&sn=1b5e804355bd86b824c0209820b9f0b3)** ：卡尔·AI 沃茨基于微信读书 Skill 开发了开源项目「carl-weread」，核心思路不是推荐整本书，而是根据用户当前的工作与困惑，从书架上精准推荐一个章节。

  * **[《LibTV 团队版上线 开启视频团队合作模式降维打击》](https://mp.weixin.qq.com/s?__biz=MzkzMTcyMTgxNg==&mid=2247510663&idx=1&sn=1d2f079373e22c3e3047205d83b5ed18)** ：LibTV 上线团队版，关键突破在于共享画布：导演、抽卡师、剪辑师可同时在一个项目内操作，分镜调整实时同步，抽卡师无需等待文件传输即可开始生成，剪辑师能提前使用已完成的镜头片段，三人并行推进效率大幅提升。
