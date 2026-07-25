### 「未来最可怕的颠覆者可能不是竞争对手，而很可能就是你的用户。」

[

![范冰 XDash's avatar](https://substackcdn.com/image/fetch/$s_!gLs0!,w_36,h_36,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F55cb259b-c4c4-4c79-8bfe-a4a47eef9d1a_940x940.jpeg)

](https://substack.com/@xdash)

[范冰 XDash](https://substack.com/@xdash)

Jan 22, 2026

##### ▪️PREFACE 卷首语

花里胡哨的各种 AI 编程产品满天飞，但我最近回归了命令行界面（CLI，Command Line Interface），转向 Claude Code / Codebuddy 这类工具。

黑漆漆的命令行里，字符串的跳跃、闪动，很有《黑客帝国》的既复古又未来的科技感（BTW，「字节跳动」这名字怎么来的，想必老程序员张一鸣也是很有共鸣）。大概也是因为我到了容易怀旧的中登年纪，看到小时候自己在学习机 / DOS / QBasic 界面里玩的那一套界面，又文艺复兴了，有点熟悉有点兴奋。

起初契机，是我意识到，现在 AI 写代码已经太强大、太迅捷了。唯一拖累它的，是我操作的速度——我得在多窗口间切换，我得精准地用鼠标指针戳到页面上某个细小的按钮，我得克服种种推荐算法的诱惑。到头来，忘了自己一开始要干嘛，原本是在做什么任务。我才是那个拖累 AI 写代码的元凶。

而在命令行的终端里，

-   我可以更聚焦地输入、等待、接收。没有标签页切换的视觉噪音，没有突然弹出的通知干扰，更没有「你可能感兴趣」的推荐算法投喂；

-   让命令行里的 Claude Code / Codebuddy 自动去做任务，也能空出我的鼠标键盘。我可以用它们做别的事，而不是鼠标停了、任务就断了（自动化脚本 / RPA 工具，比如影刀，也有这个问题，会占用鼠标键盘）；

-   最近 Claude Code / Codebuddy / Trae 相继推出的 Skill，也很强力，外挂在 CLI 里，直接将操作效率倍增。我直接吹爆。

以前 RAG、MCP（包括需要拖拽节点的工具，比如 n8n）这些，我都只是看看，笑而不语，根本没花力气折腾。因为一早已经做出了判断：都是 AI 大模型本身能力还不够强阶段的中间产物，是混沌的、不稳定的、前期投入 ROI 很低的、需要一整个生态来共创的，且迟早被模型进化迭代掉（今天看果然如此）。但 Skill 则更扎实、强悍、可复用、一个人也能做一整套闭环技能。
追求纯粹效率的朋友（比如我这样要在限定时间内完成任务，然后带娃的奶爸）试一把 CLI 吧，不会让你失望滴。

（这期没广告 lol，我憋个大的）

OK，以下是本期的正式内容——

* * *

##### ▪️CASE 案例

### [火爆全网的《卢浮宫小猫》AI 视频万字创作心得分享，这可能是他们最毫无保留的一次。](https://mp.weixin.qq.com/s?__biz=MzIyMzA5NjEyMA==&mid=2647678972&idx=1&sn=d42663a7ea0cf4881ce4c5f5fdcb7bb6)

##### via 数字生命卡兹克

[

![](https://substackcdn.com/image/fetch/$s_!-dJ-!,w_1456,c_limit,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd396e2eb-a5fe-46fe-83ea-9d4ecd8c26ab_655x368.heic)

](https://substackcdn.com/image/fetch/$s_!-dJ-!,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd396e2eb-a5fe-46fe-83ea-9d4ecd8c26ab_655x368.heic)

数字艺术家海辛和阿文，凭「故宫猫上班记」登上 TED 2025 主会场，与 Sam Altman 同台。这次他们为浦东美术馆创作官方 AI 宣传片，毫无保留地拆解了完整流程。

顶级 AI 创作并非始于技术或脚本，而是「先定调，再执行」。他们用一个镜像画面的「暴改」案例，揭示了如何将复杂的商业需求（浦东美术馆、卢浮宫、上海、巴黎）转化为清晰、高雅且具传播力的视觉语言。

-   **选角即战略。**主角猫的颜色并非随意。他们最初从美术馆黑白主题色选了奶牛猫，但为配合两支片子的长宣传周期与调性统一，果断弃用追车剧情，最终调整为「一白一橘」。白猫代表法国，橘猫延续其「上海代言」属性，这背后是精准的用户定位与品牌符号的深度绑定。

-   **定调决定成败。**在画分镜前，他们优先确定了影片的「画面影调」和「音乐」。他们发现镜厅的格子结构像钢琴键盘，水波纹倒影质感呼应钢琴和弦，于是主乐器定为钢琴。音乐先决定了剪辑节奏，再反向指导镜头是快是慢——这让商业短片脱离了素材堆砌，拥有了电影级的情绪弧线。

-   **镜像叙事构建高级感。**他们将卢浮宫与浦东美术馆、上海与巴黎、两只猫处理成镜像关系。早期探索是简单的分屏，但阿文一次关键「暴改」，将卢浮宫置于上方，浦东美术馆作为倒影放在下方，画面瞬间变得透气、高雅。这种「镜像」思维，是把复杂的文化对撞，简化成了观众一眼能感知的优雅对比。

AI 是笔，但创意是手。最强的工具在高手那里，是用来实现精准商业意图和艺术品味的。

* * *

### [腾讯悄悄内测「上头蛙」，比短剧更上头，比陪聊更克制，这或许是微信 AI 生态的真底牌](https://mp.weixin.qq.com/s?__biz=MzA3NzUxMzM5MQ==&mid=2453897281&idx=1&sn=b3fc426c86c4cf36a3c8d184afddea0a)

##### via Z Finance

[

![](https://substackcdn.com/image/fetch/$s_!gh1S!,w_1456,c_limit,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0f3fa0fa-8d7c-4426-b5e9-a243c67c751c_636x434.heic)

](https://substackcdn.com/image/fetch/$s_!gh1S!,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0f3fa0fa-8d7c-4426-b5e9-a243c67c751c_636x434.heic)

腾讯在微信生态内测的「上头蛙」，不是简单的聊天机器人，而是一个瞄准结构化内容生产的「AI 剧本工厂」。它试图在微信内跑通一个从消费、创作到分享的闭环，这背后是腾讯对 AI 应用商业化的深层考量。

反直觉的路径选择：在众多 AI 产品追逐「赛博恋爱」和开放式对话的虚火时，「上头蛙」却选择了一条更克制、但也更具确定性的路——做互动叙事。**它把爆款短剧的「强冲突、快节奏」叙事逻辑，与 AI 的无限分支能力结合，创造出一种「可消费、可复玩、可分享」的内容单元。用户每做一个选择，AI 就精准抛出一个剧情小高潮，用连续的多巴胺刺激死死拽住用户。**

更深的商业逻辑藏在微信的生态策略里。微信正在系统性扶持 AI 小程序，提供算力、云资源和流量激励，本质上是在为「生态内原生 AI 应用」铺路。「上头蛙」这样的内容产品，就成了一个完美的试验田：**用低门槛的小程序形态吸引用户，用结构化故事便于平台管理和推荐，再用极短的分享链路在微信社交圈里自然裂变。**

它的目标不是漫无边际的陪聊，而是打造一个可持续的「内容消费-用户创作」引擎，把上头的用户直接变成内容供给侧的发动机。这或许就是微信 AI 生态握在手里的那张真底牌：放弃追逐通用对话的幻觉，在自身最擅长的「内容+社交」土壤里，种出能开花结果的 AI 应用。

* * *

### [首席助教详尽复盘哈佛最受欢迎的 AI 安全课](https://www.lesswrong.com/posts/gcFB2RT5vpKHbH4ic/reflections-on-ta-ing-harvard-s-first-ai-safety-course)

##### via LessWrong

作者是哈佛首门 AI 安全课程的首席教学助理（TA）。课程最吸引人的地方，在于它用一套「真金白银」驱动的实战模式，把学生直接推到了 AI 安全研究的最前线。

这篇复盘文章，不只是学术分享，更像一份为其他大学复刻此类课程准备的「开源操作手册」。

-   **用「入场券」和「研究经费」筛选并激励顶尖人才。**课程不是谁都能上，设置了「作业 0」作为筛选门槛，要求学生复现一篇关于「突发错位」的 AI 安全论文，从 274 名申请者中精准挑出约 70 人。教授为每个小组的迷你项目提供 50 美元，为最终项目提供高达 500 美元的报销额度——这可不是象征性的补贴，而是实实在在的研究启动资金，虽然大多数学生用得比这少，但这种「投资式」教学法，瞬间把学术项目拉升到了接近创业孵化的层面。

-   **「研究研讨会」模式：**从复现到创造。课程结构摒弃传统授课，定位为研究研讨会。核心是让学生先「复现」重要的 AI 安全论文结果，再产出原创研究。最终成果是一篇 5-10 页的 NeurIPS 风格论文和一场海报展示，约 23 个最终项目直接指向可发表的学术产出。这相当于在校园里搭建了一个微型 AI 安全实验室，教学过程即研究过程。

-   **资源全公开与「客座讲师」驱动。**所有课程大纲、讲座录像全部公开，构建了强大的知识公共品。每周 3 小时的课程，大量依赖客座讲师，并穿插由 4 人小组准备的 15 分钟主题报告。这种模式既保证了前沿视野的输入，又通过高频、小团队的输出练习，强化了学生的研究和表达能力。

这门课的成功秘诀在于：它用严格的筛选确保人才密度，用真实的资金和项目模拟研究环境，再用完全开放的资源降低复制门槛。它证明，顶尖的 AI 安全人才培养，可以像运营一个高潜力的初创项目那样，通过精心设计的激励体系和实战框架来实现。

* * *

### [92 年，33 岁，做了十年猎头，我用 AI 把自己猎掉，开了家一人公司](https://mp.weixin.qq.com/s?__biz=MjM5NjE3NjYzMw==&mid=2247495351&idx=1&sn=fd89c66d5afe0ab212c3a120b47a52a1&chksm=a7fc4518ec40b2e9ae1ec07118445b225422b3eb575dec3d00b09ff546a20a7db3dafc0c8ab7&mpshare=1&scene=1&srcid=0120cdoGCb44MNFjBFCjzUdg&sharer_shareinfo=4cf267649c50af3308abf07ba13c07f8&sharer_shareinfo_first=4cf267649c50af3308abf07ba13c07f8)

##### via 纵所周知101

[

![](https://substackcdn.com/image/fetch/$s_!rQqc!,w_1456,c_limit,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9e0dc5ba-35cb-471c-8f14-0801cab5cb8b_639x243.heic)

](https://substackcdn.com/image/fetch/$s_!rQqc!,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9e0dc5ba-35cb-471c-8f14-0801cab5cb8b_639x243.heic)

故事从减肥开始。一位资深猎头，用 Claude 制定减肥计划，拿到的不是「少吃多动」这种废话，而是一份具体到每日饮食、运动强度、瓶颈期调整的个性化方案。就是这套「拆解目标→生成行动」的方法，支撑他一年减重 80 斤。这

减肥成功让他意识到，AI 能干的远不止这些。他开始系统性地把 AI 融入核心能力圈。4 个月消化 60 本书，用「读书笔记智能体」形成可复用的知识资产；更关键的是，他开始思考如何将十年猎头经验转化为 AI 工作流，探索「猎头智能体」的可能性。

最终他离开稳定的高管职位，用 AI 将自己从原有角色中「猎掉」。

底层逻辑是什么？通过 AI 工具矩阵承担大量信息处理、方案生成和流程管理工作，极大扩展了个体能力的边界。单兵作战也能具备过去小型团队才有的产出效率与专业深度。

* * *

##### ▪️OPINION 观点

### [All in AI 的第一个三年](https://mp.weixin.qq.com/s?__biz=MzIyMDE5OTYyMw==&mid=2651051471&idx=1&sn=e72fb5a5e738a02d5307b043824140ef)

##### via 42章经

投资机构绿洲在 2023 年曾有机会以约 8 亿美金估值投资美国机器人公司 Figure AI，却因「未来属于中国」的判断而放弃；如今该公司估值已达 400 亿美金，错过超 50 倍增长。

「在 AI 这种全球性技术浪潮中，过早的地域性预判可能成为代价高昂的认知盲区。」这成为了它们深刻的一课。AI 的本质是连接全人类的智力革命，因此「开放」比「精准」更重要。

除此之外，他们还意识到：

-   资产形态上，未来硬通货可能是「算力」而非货币。因为算力是支配 AI 智力的钥匙，未来甚至可能出现「算力配额」与「算力慈善」。若能回到三年前，顶级策略将是「把钱全换成算力，再用算力去投人」。

-   竞争格局上，巨头的反应速度远超预期。Google、微软等大厂凭借信心、投入与聚才能力，快速压低了创业公司的天花板，这让早期投资必须更注重生态位而非单纯的技术优势。

-   无论参与还是观望 AI，个体的终极策略都是「活出自己」。AI 会极度放大个人独特的审美或能力点，让其能服务全球；而即使不用 AI，专注所爱、成为「无法被替代的部分」，也是在 AI 时代创造价值的方式。

可能在未来，一部分人通过 AI 放大自我服务大众，另一部分人则通过深耕自我成为独特存在，两者共同构成了人机共存的新生态。

* * *

### [姚顺雨最新访谈：AI 下半场，机会在这一点](https://mp.weixin.qq.com/s?__biz=MzIxNTAzNzU0Ng==&mid=2654902492&idx=1&sn=4fd57334957297cd71bedc5180d4cdd3)

##### via MIT Technology Review

OpenAI 前研究员、现任腾讯首席 AI 科学家姚顺雨，提出了一个反直觉的洞察：AI 下半场最大的机会，竟在于「设计不同于 ChatGPT 的交互方式」。

上半场大家拼的是算法和算力，焦虑于「如何训练出更强的模型」；**下半场的瓶颈变成了「如何定义有价值的任务」。**这就像你拥有了一位天才，但若只让他陪你闲聊，无疑是巨大的浪费。真正的胜负手，在于谁能设计出激发 AI 潜能的「考题」和「战场」。

Agent 是通往 AGI 的必经形态。姚顺雨将能行动的 AI 称为「Language Agent」（语言智能体）。它的本质不是聊天，而是通过语言进行推理，再通过推理实现泛化。这就像人面对新游戏时，会观察、思考、制定策略，而不是盲目试错百万次。语言模型提供的「强先验」，让 AI 拥有了这种跨任务推理的可能。

未来格局是「单极多元」。我们或许会有一个类似 Google 的超级 AI 平台，但世界不会被单一模型垄断。最终的智能边界，由「交互方式」决定。这意味着，创业公司不必在巨头的模型赛道上硬拼，而是可以转身成为「任务设计师」和「环境构建师」，在定义「如何与 AI 协作」的新战场上开辟蓝海。

**AI 的下半场，英雄将从「炼丹师」变为「导演」和「编剧」。**机会不在于做出另一个更聪明的聊天大脑，而在于为这个大脑设计出能改变世界的精彩剧本和舞台。

* * *

### [当牙医开始自己做工具：Claude Cowork 把「写代码」变成按钮，软件护城河还能剩多少？](https://mp.weixin.qq.com/s?__biz=MzA3MDU4ODkyNg==&mid=2247511932&idx=1&sn=35d38492fd6735370abbb0d244794dc3)

##### via 硅谷科技评论

风投大佬 Fred Wilson 十年前讲过一个「牙医软件寓言」。现在这个寓言有了续集：

一位普通牙医，用 AI 编程工具 Claude Code，没写一行代码就为自己诊所「捏」出了完美适配的软件，彻底抛弃了所有软件供应商。这标志着一个根本性转变：软件的护城河，正从「写代码的能力」转向「懂业务的深度」。

当牙医开始「Vibecoding」（直觉式编程），就像用乐高积木一样，通过对话和提示词就能组合出所需功能，这意味着**「领域知识」成了新的核心竞争力。软件公司引以为傲的「最佳实践」，在用户自己「完美定制」的需求面前，变得不堪一击。未来最可怕的颠覆者可能不是竞争对手，而很可能就是你的用户。**

这场变革直接动摇了 SaaS 的命脉——订阅制收入。如果软件可以像写备忘录一样「随用随生成」，用户为什么还要每年支付 5000 美元甚至 2.5 万美元的订阅费？定制化的边际成本几乎归零，通用型软件的市场空间被急剧压缩。

更残酷的现实是，传统软件巨头展现了惊人的进化速度。Salesforce 用 6 个月完成核心重构，Notion 也在 6 个月内革新 AI 架构。这形成了一个前后夹击的战场：后方是「武装起来」的用户，前方是「突然开窍」的巨头，留给中间层创业公司的生存空间正在消失。

* * *

### 随便看看：

-   **[《AI 用 512 种特征辨认猫狗，帮助 17 万只走失宠物回家》](https://mp.weixin.qq.com/s?__biz=MjM5NjAxOTU4MA==&mid=3009365433&idx=2&sn=675becf4d279957b8f11d6f62f15e17e)**讲述了一个非营利组织如何将 AI 面部识别技术，变成一个高效整合社会资源的宠物寻回生态系统。

-   **[《最早用上 AI 的山村小学，八年后怎么样了？》](https://mp.weixin.qq.com/s?__biz=MzA3NTc2NDY5MA==&mid=2653094620&idx=1&sn=282d12f2d368451393d035e014485c01)**带我们走进安徽大别山深处的一所小学，看看八年前就引入 AI 智慧课堂的试点，如今变成了什么样。

-   **[《字节扣子 2.0 发布，我们深挖了它这两年的生长真相》](https://mp.weixin.qq.com/s?__biz=MTMwNDMwODQ0MQ==&mid=2653097480&idx=1&sn=a8ef5c0fe2a0e8e2acc38f8e0cef47f8)**深扒了字节跳动旗下 AI 产品「扣子」从 2023 年诞生到 2026 年升级 2.0 的野生成长史。它并非大厂战略规划的产物，反而像一个在字节内部拿到投资的早期创业团队，经历了从对话 Bot 到工作流，再到如今定位「职场 AI」与「Vibe Coding」的多次战略腾挪。一个看似不性感的「工作流」功能，竟成了决定产品生死的关键转折。

-   **[《We’ve Built 12+ Vibe Coded Apps Used 800,000+ Times. I Love It. But I Still Have To Maintain Them Every Single Day.》](https://www.saastr.com/weve-built-12-vibe-coded-apps-used-800000-times-i-love-it-but-i-still-have-to-maintain-them-every-single-day/)**来自 SaaS 领域的知名人物 Jason Lemkin，他分享了自己用「氛围编程」快速打造出 12 个以上、总使用量超 80 万次的 AI 应用后，却不得不面对一个鲜少被提及的残酷现实：真正的产品需要日复一日的维护。氛围编程带来的并非一劳永逸，而是一份需要每日耕耘的「园艺合同」。

-   **[《当 AI 成为了「杀猪盘」的新外衣》](https://mp.weixin.qq.com/s?__biz=Mzk0MDYyMDA0NQ==&mid=2247491006&idx=1&sn=7252211290ba78e591ecec2113737c3f)**通过一个名为「芯光云」的 AI 投资骗局案例，揭示了技术狂热如何被包装成收割普通人的陷阱。最高级的骗局，卖的从来不是技术，而是人性对暴富的渴望和从众的安全感。

-   **[《重生之我在「青椒模拟器」做导师，一路飞升到院士》](https://mp.weixin.qq.com/s?__biz=MzA3NTc2NDY5MA==&mid=2653094645&idx=1&sn=e2cd6bf27a03262b6c460273832dcada)**通过一款意外爆火的高校模拟游戏，揭示了当下科研与职场生态的镜像世界。两位在读博士生用「摸鱼」时间创造的这款游戏，竟在高峰时一天涌入九万人次，它巧妙地将大模型技术变成了一个社会实验场，让玩家在虚拟的「非升即走」压力下，提前预演自己的人生选择。游戏的核心吸引力并非娱乐，而是「照镜子」。

-   **[《「Claude Cowork 杀死了我的创业公司」》](https://mp.weixin.qq.com/s?__biz=MzAxMDMxOTI2NA==&mid=2649103764&idx=1&sn=38a547891595b9ee8c111f6d905e821f)**讲述了一个反直觉的商业故事：AI 巨头 Anthropic 发布 Claude Cowork，竟意外「杀死」了一家做类似多智能体平台的创业公司 Eigent，而后者却因此爆火。当巨头免费内置了你的核心功能，创业公司该怎么办？Eigent 的 CEO 李国豪给出了一个教科书级的回应：开源。

-   **[《谁来给桌面 Agent 的转正签字？》](https://www.huxiu.com/article/4828329.html?f=rss)**通过作者亲身测试一款 MiniMax 新上线的桌面 AI 助手，揭示了当前 AI 工具在宣传的无所不能与实际使用体验之间的巨大落差。

### 适合个人上手的教程/评测/资源：

-   **[《我的 AI 工具日常使用与工作流是怎样的？》](https://wangshuyi.substack.com/p/ai-ba0)**是作者对自己庞杂 AI 工具箱和工作流的一次深度揭秘。核心观点是「重器轻用」—— 不迷信全能选手，而是像管理公司员工一样，让每个工具在最擅长的领域发光发热，实现高效协同。

-   **[《火爆全网的 Skills，终于有了最简单的打开方式。》](https://mp.weixin.qq.com/s?__biz=MzIyMzA5NjEyMA==&mid=2647679068&idx=1&sn=6b3ae5770982ec685d57fe8a006e6317)**介绍了 AI 工具「扣子」2.0 版本如何通过内置「Skills」功能，让普通用户也能轻松创建和使用 AI 技能，从而将复杂的专业工具平民化。作者如何用「口喷式开发」把开源项目 FFmpeg 和 ImageMagick 打包成一个视频图片处理 Skill。延伸阅读：**[《字节全球首发 AI 技能商店：一句话生成 Coze Skills，你的经验直接卖钱》](https://mp.weixin.qq.com/s?__biz=MzI3MTA0MTk1MA==&mid=2652665717&idx=1&sn=f78729105732a364aca2372a32ee16bc)**

-   **[《实测夸克「千问划词快捷指令」，这 7 个邪修 Prompt，建议收藏》](https://mp.weixin.qq.com/s?__biz=MzA3MzI4MjgzMw==&mid=2651012094&idx=1&sn=88dcd9a32e04ef66230aaa0f6259477e)**通过实测夸克 AI 浏览器的「千问划词」功能，揭示了如何通过预设「邪修」Prompt 来彻底改变与 AI 的协作效率，让 AI 从「听话的助手」变成「主动的伙伴」。

-   **[《千问打通阿里生态后，会发生什么？》](https://mp.weixin.qq.com/s?__biz=MzAxMDMxOTI2NA==&mid=2649103832&idx=1&sn=c233ff29f4c197c965bd35cc277b810b)**深入实测了阿里千问 App 在打通淘宝、高德、飞猪、支付宝等核心服务后的真实能力。它揭示了一个关键转变：AI 正从一个「回答问题的对话框」，进化成能直接处理「真实生活任务」的行动入口。最吸引人的深度案例，是千问如何像一个「超级生活助理」，通过「办公助手」模块处理复杂、多步骤的团餐订购任务。

-   **[《小白 Vibe Coding 发行全平台 & 可变现应用指南》](https://mp.weixin.qq.com/s?__biz=MzU0MDk3NTUxMA==&mid=2247495440&idx=1&sn=8bc7a55a17d51b85491dd873c27b9dd8)**以作者用 Youware 开发一款名为「Vibe Diary」的 AI 日记应用为深度案例，揭示了如何利用最新的「Coview」和「YouBase」功能，将 AI 编程门槛「拉低一万倍」，并构建出真正能分发和变现的完整产品。

[

![早ao's avatar](https://substackcdn.com/image/fetch/$s_!ryS2!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack.com%2Fimg%2Favatars%2Fyellow.png)

](https://substack.com/profile/432822386-ao)[

![王鑫星's avatar](https://substackcdn.com/image/fetch/$s_!X3VX!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F94854790-89fd-468d-b680-b885670c755c_1206x1206.png)

](https://substack.com/profile/421654501-738b946b661f)[

![Cedric's avatar](https://substackcdn.com/image/fetch/$s_!DgTc!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff26b52e8-a406-487b-b39b-c7faafb89ad9_640x640.png)

](https://substack.com/profile/438735210-cedric)[

![MindBro's avatar](https://substackcdn.com/image/fetch/$s_!X9o_!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3e203178-8b6a-4c3b-9da3-8c116f6e3f85_288x288.png)

](https://substack.com/profile/439445599-mindbro)[

![DeepRead|深度阅读's avatar](https://substackcdn.com/image/fetch/$s_!cmS2!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5778a8bf-1a94-431d-9b59-b9b293ad071e_900x1296.jpeg)

](https://substack.com/profile/408766993-deepread)

5 Likes

[](https://substack.com/note/p-185326081/restacks?utm_source=substack&utm_content=facepile-restacks)
