##### ▪️PREFACE 卷首语

Hi 各位，无预警地停更一个月后，我回来了！

诸多因素导致停更。既有国庆假期想陪伴家人、远离工作的考虑，也有秋冬换季身体抱恙的因素。小小休整一下，便于日后更轻快出发。此外还有两个重要的理由：

1/ 第一个理由是，在过去数月中，我一度陷入自我怀疑：这个每周免费更新的 newsletter，有价值吗？甚至写了篇小作文，发在自媒体上（[X](https://x.com/XDash/status/2111033764021473637)、[即刻](https://m.okjike.com/originalPosts/6ad1f44abd0563695bb89d09)、[公众号](https://mp.weixin.qq.com/s/vDFielWE4OXAQ9jRwah70Q)）。这几处数据都小爆了一下，看来有共鸣的朋友挺多的。

我不想为了维持更新，就强行给读者灌输没营养的内容。而在断更开始的那一周，恰好我的内容库里并没有冒出足够多让我感到兴奋的、足够储备一期的内容。于是在靠「推荐垃圾」、「断更」这两害里，我选择了后者，起码自己和读者的负担更小些。

这期间我也想通了两件事----1）如果我自己不兴奋，哪怕离钱再近、市场声量再大的领域，我也不再推荐了，比如 AI 短剧制作、GEO。我只先主观推荐我自己感兴趣的内容，再考虑大众的口味。2）每周肉眼筛选 AI 内容，除了发 Newsletter 分享外，我也找到了其他的价值突破口，让做这件事的动力有了延续。

2/ 第二个理由是，我在忙一本新书。之前我发在 Github 的开源小册子**《 前线部署工程师（FDE）》，在这一个月完成了所有出版立项和印刷上架工作，目前已经可购买现货。**

[![](https://substackcdn.com/image/fetch/$s_!GAYR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F713867cf-22bd-4c13-8eb5-e9ca964548a0_723x704.png)](https://substackcdn.com/image/fetch/$s_!GAYR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F713867cf-22bd-4c13-8eb5-e9ca964548a0_723x704.png)

我坦承，这本书是我全程用 Claude Code 辅助写完的，原本是用开源形式（[Github 地址](https://github.com/xdash/FDE-the-Guidance-Book-of-Forward-Deployed-Engineer)）免费提供（目前 5.1k stars）。有很多朋友之前已经读过，给出了好评。

后被人民邮电出版社关注，对方派出编辑做了许多修正、校对、优化的工作，最终以纸质版形式上市，以面向更广阔且有需求的读者人群。

但这里不是卖书，是告诉您，您完全可以免费获取免费开源版。如果你是微信读书的会员，也可以直接搜索「FDE」阅读（作者是范冰的那本）。

当然，如果您想收藏一本纸质版，或者想向下属/合作伙伴安利，也欢迎去各大网店搜索「FDE」购买（黄色封面）。

[京东](https://item.jd.com/10237748982809.html) | [淘宝天猫](https://detail.tmall.com/item.htm?abbucket=16&id=1092101882413&skuId=6313004570173) | [当当](https://product.dangdang.com/30119055.html)

这里我只求个免费的赞。如果您读完觉得不错，可以到[ 豆瓣来给个四/五星好评](https://book.douban.com/subject/38676682/)。Thx~

3/ 篇末，推荐个最新发现的 B站 宝藏 AI 短剧 up 主----[「红楼原语」](https://space.bilibili.com/3747566497827606/)。

它正致力于用 AI 方式还原红楼梦脂批本的每一章节，有画面意境也有原文批注。从没完整读下来红楼的文盲如我有救了。

[Subscribe now](https://www.zengzhang.ai/subscribe?)

OK，以下是本周正刊内容，Enjoy----

* * *

##### ▪️OPINION 观点

### 💡 **[利不在器：论为何 AI 应用都不赚钱](https://mp.weixin.qq.com/s?__biz=MzU2MTgzMjQyMA==&mid=2247485185&idx=1&sn=d6baf9dc75704fd21b72c1a07f344d30&chksm=fdb54145c5e8301d33283a58340d44f1984468c978e76d200eabef48d7900fbe15d34386de01&mpshare=1&scene=1&srcid=1005Z5MB0e7olnlgEDZXQDuU&sharer_shareinfo=37128bb4affa0b7b64e3dc5810be741e&sharer_shareinfo_first=7ac1988e2ce3085b9d58508711d1ee51)**

##### **[原链 * 公众号 * 约 7 分钟读完](https://mp.weixin.qq.com/s?__biz=MzU2MTgzMjQyMA==&mid=2247485185&idx=1&sn=d6baf9dc75704fd21b72c1a07f344d30&chksm=fdb54145c5e8301d33283a58340d44f1984468c978e76d200eabef48d7900fbe15d34386de01)**

AI infra 在赚钱，AI 应用却被碾平。

作者参加完中科大校友会活动，把这个反差拆成了**「 利不在器」：写代码、做图、翻译这些单点能力供给多、壁垒低，利润必然趋近于零。**

**传 统企业买 AI infra 改造供应链，是在创造增量；而 AI app for AI users 更容易陷入零和博弈。**Anthropic、智谱、OpenAI Codex、字节 Seedance 的集体选择，也都指向 to B。**真 正能收到钱的，是 workflow capture----接管完整业务流程，交付明确的营收增长。**

客户愿意长期付费的 KPI，只有一条：绑定真实 P&L 的垂直 ROI。作者的算账公式是「替人率 × 人数」，所以电商、直播、游戏公会、保险销售这些雇佣纯低端白领的生意，都是 AI workflow capture 最好的靶场。

* * *

### 🧠 **[谈判、选书、管健康，Chamath 把 AI 攒成一套「生活模型」](https://www.youtube.com/watch?v=iI9uVDF0R4s)**

##### **[原链 * youtube.com * 约 29 分钟看完](https://www.youtube.com/watch?v=iI9uVDF0R4s)**

投资人 Chamath Palihapitiya 在 YouTube 发了个视频，介绍自己的 AI 用法，起了个名字：生活模型。

**他 让一串个人代理各管一摊。高风险谈判交给纳什均衡代理，商业和心理学书籍先过一遍心理过滤器，另有投资组合优化和健康管理系统。教育方面，他的建议是学工程和物理，理解世界如何运作；再学哲学、政治和经济学，培养品味。**

在他看来，AI 创造的工作会比取代的更多，但个人得先培养品味和判断力，才能有效利用它。选完基础模型，你还得持续建微服务、持续改，并筛选编排 AI 的输出。

他把这些工具攒出来的能力叫作「仿生能力」。与此同时他也提醒，别把 AI 当成超级智能。

眼下还处在信息混乱周期，AI 的影响远未确定。个人能做的，是尽早动手构建工具，在变化里长出自己的能力。

（怎么搭建？可以看一下我之前录制的 [「我如何打造私人 AI 贾维斯」（https://diy-jarvis.com/）视频课程](https://diy-jarvis.com/)。

* * *

### 🌱 **[Meshy破 1 亿美金后，胡渊鸣用 48 条反思划出了创始人的边界](https://mp.weixin.qq.com/s?__biz=MzkyNTE1MjYzNg==&mid=2247484262&idx=1&sn=14628187e5f8beaf1a26456ecd2636ef&chksm=c035ba4833ce452932328cdacdf26fa0f004de3f03498a798727d289f2c48c690a2867852809&mpshare=1&scene=1&srcid=1007yjuIB6F9RjtWwObOK5vl&sharer_shareinfo=1ebb0208735e04edea8aa01516e7c077&sharer_shareinfo_first=d4e0b3db2ec4bf83fb827876151dd956)**

##### **[原链 * 公众号 * 约 32 分钟读完](https://mp.weixin.qq.com/s?__biz=MzkyNTE1MjYzNg==&mid=2247484262&idx=1&sn=14628187e5f8beaf1a26456ecd2636ef&chksm=c035ba4833ce452932328cdacdf26fa0f004de3f03498a798727d289f2c48c690a2867852809)**

Meshy 的 ARR 突破 1 亿美金后，创始人胡渊鸣花一个月写下 48 条反思。

他想回答三个问题：**哪 些事希望提前知道，创始人性格如何影响团队相处，自己还有哪些不足。**

文章分成温度与原则、时间与 Founder mode、AI 与人、团队与管理、战略与执行五个板块，讲的是公司从 10 到 100 阶段的认知迭代。（成功者复盘难免带着事后归因，但关于管理边界和自我消耗的部分，仍值得对照自查。）

* * *

### 🤖 **[开口之前就把事做完：Today AI 押注长程记忆和主动 Agent](https://mp.weixin.qq.com/s/KGkqa0y-DLGMNC9Zu1C9SA)**

##### **[原链 * 公众号 * 约 10 分钟读完](https://mp.weixin.qq.com/s/KGkqa0y-DLGMNC9Zu1C9SA)**

[![记忆如何围绕工作、健康、旅行和学习组织（产品示例）](https://substackcdn.com/image/fetch/$s_!Eisi!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Feee3766d-6115-4441-b381-6c3b9a76da25_1080x608.webp)](https://substackcdn.com/image/fetch/$s_!Eisi!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Feee3766d-6115-4441-b381-6c3b9a76da25_1080x608.webp)

最近 Personal Agent 在大肆炒作，也跑出几个阶段性的爆款产品。

在国内，Today AI 的齐俊元早在 2014 年就买下 today.ai 域名，想做 AI 个人助理，如今海外版已经上线，并且 PR 说融了两亿美金。

本文作者走访了 Today 办公室，聊了一个多小时。我因为也在搭建自己的 AI 贾维斯，很感兴趣，于是读了一下，想取取经，看看有什么可以 ~~抄 袭~~ 借鉴的。

  * 团队认为，记忆系统必须针对具体场景设计：收集哪些信息、怎样理解人的行为、什么值得记下来，都要放进对场景的理解里。只用通用提示词让模型「记重要的事」，效果通常很差。

  * **Today 的北极星指标是 DAU，用户主动发起 query 的次数优先级反而很低。** 团队最关心 Agent 主动解决了哪些问题。

  * Today 的 PM Suki 还分享了自己用 Today 替代外教的经历。Today 先做测试，再建 scheduled tasks 安排每天学什么，根据反馈调整课程计划，还把生活里的熟人编进课程当角色。

  * 作者由此给了一条找需求的路：看人们原来在为什么花钱。1 对 1 外教和健身教练都是先了解水平、安排课程、跟进学习、根据反馈调整，恰好是 Agent 现在就能干的。

个人 Agent 面对的是开放世界，充满主观判断。比如「帮我给邻居发邮件让他别再吵了」，邮件发出去了，task 就算成功吗？未必，真实需求是「让他别吵」。

联合创始人高策给出的答案仍然**落 回 Memory 和 Proactive：用户长期以来是什么样的人、最近发生了什么、什么事值得主动去做，都需要产品持续组织和使用相关信息，不能只靠模型当下的 working memory。**

BTW，这赛道纯应用层这能跑通吗？我觉得创业团队要活下来，避免跟巨头正面竞争，**还 是得走硬件路线，推出自己的 Context 收集产品。**但，这又是另一个深水区和能量圈的故事了。

* * *

##### ▪️CASE 案例

### ⚡ **[YC让智能体每晚读员工对话，把技能越养越准](https://mp.weixin.qq.com/s?__biz=MzA3MDQyNDUzMA==&mid=2649928931&idx=1&sn=5a4ae835015a5f660c46b07f6c1b1d4a&chksm=869608cc9834c82302ff63f81b12bf64a95227236d889b0b8917ac4af274bbd5b395a51cab1a&mpshare=1&scene=1&srcid=0924rjlMJHWTF2PCi10KGNqp&sharer_shareinfo=7e6d872d61387ce8fcb8a068a72dc961&sharer_shareinfo_first=7e6d872d61387ce8fcb8a068a72dc961)**

##### **[原链 * 公众号 * 约 23 分钟读完](https://mp.weixin.qq.com/s?__biz=MzA3MDQyNDUzMA==&mid=2649928931&idx=1&sn=5a4ae835015a5f660c46b07f6c1b1d4a&chksm=869608cc9834c82302ff63f81b12bf64a95227236d889b0b8917ac4af274bbd5b395a51cab1a)**

YC 普通合伙人 Pete Koomen 在播客里讲了内部的 AI 原生组织实践：把 AI 当成一切工作的构建层，并记录所有产物，形成共享的组织大脑。

  * 第一步是集中上下文。**YC 运行在自研软件上，所有重要信息都在同一个 Postgres 数据库里。** 智能体用只读 SQL 查询就能回答复杂业务问题，人们愿意提的问题随之变多、变复杂，形成杰文斯悖论。数据分散的组织，可以把数据反规范化到为智能体优化的 schema 里，做成类似 Karpathy 风格的知识 wiki。

  * 第二步是组织自我改进。YC 的通用智能体每晚读取员工与智能体的对话，寻找改进点，还会读会议记录，把人和公司的信息写回内部数据库，形成「梦境循环」。「两句话描述技能」就是典型案例。合伙人 Tom 写了初始技能，小组 office hours 的会议记录又被智能体学进去，技能明显变好，Pete 认为它已经超过自己。

  * 第三步是开放、信任和共享。YC 默认让全职员工看到智能体对话，并广播到 Slack 频道，既促进学习，也形成社会控制。

  * Pete 认为，真正智能体化、效率提升千倍的组织，必须具备相对平等和默认信任这两个特征，也要愿意每年花一万到十万美元买 token。

今天花十万或一百万美元一年做的事，两年后会变成常见配置。创业公司因此有一次性的时间跃迁机会，可以跨越现有巨头。（这套经验出自 YC：全员高密度、老板就在隔壁。搬进两百人的公司，先得看看自己有没有那个信任基础。）

* * *

### 🍷 **[11名员工撑起 14 城数百张酒桌：AI 盲盒酒局是不是好生意](https://mp.weixin.qq.com/s?__biz=MzI2NDk5NzA0Mw==&mid=2248906422&idx=1&sn=c4e30d859a02d3b3218fbbb7d43a9bb1)**

##### **[原链 * 公众号 * 约 17 分钟读完](https://mp.weixin.qq.com/s?__biz=MzI2NDk5NzA0Mw==&mid=2248906422&idx=1&sn=c4e30d859a02d3b3218fbbb7d43a9bb1)**

[![Image](https://substackcdn.com/image/fetch/$s_!0A_e!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6289c843-d2ec-4cde-887f-0eb7ad245970_1080x720.webp)](https://substackcdn.com/image/fetch/$s_!0A_e!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6289c843-d2ec-4cde-887f-0eb7ad245970_1080x720.webp)

AI 社交产品 Table for Six（T46）已获得 BAI Capital 和某游戏公司累计数百万美元天使轮融资，累计付费用户超过 4 万人。

T46 由前麦肯锡同事 Jeff 和白菜创立，从喝酒卡牌和快闪酒馆起步，后来转向六人盲盒酒局。用户支付 88 元或 118 元，得到一杯饮品和一场由 AI 匹配的陌生人聚会。

AI 在后台接下了传统主理人的核心工作：从报名问卷提炼匹配准则，平衡年龄、性别、内外向和社交能量，为每桌生成专属卡牌，甚至用六个 Agent 模拟参与者，预演对话气氛。

运营端也由 5 个主 Agent 及其子 Agent 跑完整流程：排桌、选场地、生成打印文件、对接印厂、核对装盒、下闪送订单。**11 名都在上海的员工，就这样撑起 14 座城市的数百张酒桌。**

我身边有朋友实际参与了这个活动。结果 6 人报名，实到 4 人。看来这类产品要应对的不确定性和非标性，并不是来自线上的 AI，更多就像剧本杀一样，来自线下一个个始终只追寻新鲜刺激的年轻人呀。

* * *

### 💰 **[从 19.9 元教程到 30 万元企业课：教别人用 AI，我赚翻了](https://mp.weixin.qq.com/s?__biz=MjM5ODMzMDMyMw==&mid=2654912867&idx=2&sn=ca0eafe6bc4de656ed8518a237007cdd)**

##### **[原链 * 公众号 * 约 17 分钟读完](https://mp.weixin.qq.com/s?__biz=MjM5ODMzMDMyMw==&mid=2654912867&idx=2&sn=ca0eafe6bc4de656ed8518a237007cdd)**

当 AI 让越来越多技能变得廉价，教别人用 AI 反而成了一门生意。五位从业者的自述，把价格从 19.9 元一直拉到 30 万元。

  * 北京梦镜惊鸣创始人王甜以 3000 元一门课教 AI 视频制作，学员不到二十人。她没打算把培训做成长久生意，因为「AI 变化越来越快」。

  * AI 应用顾问张羽明用 AI 生成课程内容，已经排到 33 门大课、400 多节。个人课程月费 19800 元，**企 业培训单堂可达 30 万元**，团队每月 API 费用也要 3000 到 5000 美元。

  * 南京法律顾问林舟专教律师用 AI，线下小课一堂收入 3 万到 5 万元，线上课月入两三万元，已经超过他做律师时的收入。但他清楚：「这种信息差能维持多久，我并没有把握。」

  * 徐州 AIGC 导演杨波拒掉 48 万元的包就业大单，自己定价 12800 元，两个月包吃包住包算力。他强调培训要有真实订单和利他思维。

  * 北京科技公司行政周琳把接单经验整理成 19.9 元教程，三个月卖出 300 多份、收入 6000 多元。卖教程反而比接单更赚钱。

付费者买的其实是行业经验、客户资源、真实商单机会，以及缓解被 AI 取代的焦虑。

AI 一边消灭信息差，一边制造新信息差。这门生意的窗口期可能只有一两年，等 AI 真正变成日常工具，很多东西自然没人需要再花钱学。

* * *

### 🏢 **[卡兹克的 30 多人公司花了 5 天进行 AI 化改造中台](https://mp.weixin.qq.com/s?__biz=MzIyMzA5NjEyMA==&mid=2647686948&idx=1&sn=d43b6d924d339092f96e3ba826119f6c)**

##### **[原链 * 公众号 * 约 17 分钟读完](https://mp.weixin.qq.com/s?__biz=MzIyMzA5NjEyMA==&mid=2647686948&idx=1&sn=d43b6d924d339092f96e3ba826119f6c)**

[![](https://substackcdn.com/image/fetch/$s_!2S2C!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7443b991-acbd-41b4-a81d-4946463cc118_660x537.png)](https://substackcdn.com/image/fetch/$s_!2S2C!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7443b991-acbd-41b4-a81d-4946463cc118_660x537.png)

一个 30 多人的小公司，人人都在用 AI，接下来还差什么？

数字生命卡兹克在国庆期间花 5 天做了一场公司改造，想让每个员工都能创造产品、改变流程。

他用 Claude Opus 5.5 等工具，从品牌 VI、UI 组件、PPT 模板一路做到 Skill 封装，搭起一个以 Agent 为原生操作、以飞书数据为基建的企业中台。

公司里其实已经冒出不少自发实践，比如财务给商务 Vibe Coding 了开票助手。但应用部署、权限管理和 Skill 分发，始终是痛点。

卡兹克租了一台服务器，把中台包装成 MCP。**员 工只要把一段 Prompt 发给自己的 Agent，就能自动安装 MCP、发布应用、分配子域名和权限。**

中台复用了飞书的权限体系和数据同步，还支持千人千面的首页定制----每个员工的首页，都由 Agent 根据账号 ID 自动生成。

他把数据、Context 以及由此建立的协同关系，看作企业未来最核心的资产。Agent 甚至暴力推演了所有数据规则，清理过去人工录入留下的屎山。

他期待的场面很具体：新员工入职第一天发现流程蠢，同事自然地说「那你让 Agent 改一下呗」，第二天新应用就上线，全公司都用上。（自己公司的改造，效果难免往好里说，但「把中台包成 MCP 再分发」这个动作，别家公司可以直接照搬。）

过去是员工适应公司系统，接下来，公司系统可以开始适应每一个活生生的人。

* * *

### 随便看看：

  * **[《中国工厂生死分野：AI 点燃的无声暴裂》](https://mp.weixin.qq.com/s?__biz=MjM5NjAxNDE2MA==&mid=2651119803&idx=1&sn=4ddc37747ee615493d73402ceca32339)**：1688 上超 20% 的采购需求已由 AI 智能体发起，今年预计超 40%。有 200 人团队跑出过去 1000 人的产值，也有传统打样厂订单缩水近一半。

  * **[《疯狂水世界进入广告业，仿佛龙卷风摧毁停车场。》](https://mp.weixin.qq.com/s?__biz=MzA5NDc1NzQ4MA==&mid=2654703104&idx=1&sn=5008ebf4cd3e65bfab81c82a00b02e90)**：一条 3D 广告从 10 万到 20 万元、耗时一两周，降到一两天和几十元 token 成本。效率上来了，抄袭和互诉也跟着泛滥。

  * **[《AI「入侵」影视业》](https://mp.weixin.qq.com/s?__biz=MjM5NDAzMjk2MA==&mid=2653628965&idx=1&sn=92981263760b721ade55774f3168684d)**：第一财经的调研显示，AI 短剧成本不到真人剧的十分之一，单集模型成本 500 元。2026 年一季度 AI 微短剧 12.2 万部，占总量 95%，红果日活也破了 1 亿。

  * **[《中国 AI 的年轻掌权者们》](https://mp.weixin.qq.com/s?__biz=MzU3Mjk1OTQ0Ng==&mid=2247539314&idx=1&sn=5dfbab5aca1b10bceb11401de540d12b)**：晚点 LatePost 拆解杨植麟、罗福莉、姚顺雨等人的上位路径：技术判断力正在取代商业战果，把三十岁上下的研究员推向权力中心。

  * **[《2026 年小天才崩投资人实操指南》](https://mp.weixin.qq.com/s?__biz=Mzk4ODkwMTE5Nw==&mid=2247484154&idx=1&sn=b471eefbfe9dce74bdd44b17fb560384&chksm=c41c809e4cd6ac96d7ff5c283477b323a5d7a14b236d512b928fd6eeaa5eff7a9a42c55f1f8b&mpshare=1&scene=1&srcid=1009Gj3vGJOzosybmQD2ypgu&sharer_shareinfo=15195986455ba708089f6247d9bcd28d&sharer_shareinfo_first=15195986455ba708089f6247d9bcd28d)**：一篇反讽的一级市场定价指南：年龄要小、理想够大、商业化最好别太早；蓝驰上午交流、下午就发 TS。融资是资源配置，不是诺贝尔奖。

  * **[《导演陆川写了 3 个 AI 工具：我想弄清楚人到底哪儿不可替代》](https://mp.weixin.qq.com/s?__biz=MzI2NDk5NzA0Mw==&mid=2248904001&idx=1&sn=9ea48cf157ba2679dfc7e343d3bc9ad9)**：陆川用 57 天、近一万行代码写出剧本医生「情书」，又做了「上镜」和「积木」。他的判断是数据比算力重要：没有 1000 张卡，就先用两张卡训一个小模型。

  * **[《职场版「奇迹暖暖」：年轻人开始做起 AI 模特搭配师》](https://www.huxiu.com/article/4892802.html?f=rss)**：AI 模特搭配师在一二线城市月薪多为 1 万到 2 万元，跨行者每天可完成约 40 套造型。工具换了，审美和整体搭配能力仍是门槛。

  * **[《45 岁失业后，他向 AI「问」出一份工作》](https://mp.weixin.qq.com/s?__biz=Mzk0MDYyMDA0NQ==&mid=2247494492&idx=1&sn=9c7a16e35b450d07cccd5c3cab9c5f5f)**：镜相工作室记录的样本：45 岁的孟建军用支付宝 AI 就业助手「晓叶」，两天完成求职到入职，月薪约 4000 元、包吃包住。后来转做骑手，第一天挣了 112 元。

### 适合个人上手的教程/评测/资源：

  * **[《463 条 AI 视频提示语开源》](https://mp.weixin.qq.com/s?__biz=Mzg3MTk3NzYzNw==&mid=2247511621&idx=1&sn=18b1f7fccaba22417ae7767d669e6bcf)**：作者卡尔重新跑通 463 条 AI 视频提示语，蒸馏成 14 个模版和 25 个 Skills，全部开源。项目含打斗、手持 UGC vlog 等配方，适合直接临摹。

  * **[《AI 给商品拍 MV 教程》](https://mp.weixin.qq.com/s?__biz=MzA4NzMyNzU5Mg==&mid=2453083106&idx=1&sn=54f73fa271588c8a1ec6a831acd42b2b)**：MVLAND 上传产品图、选模特和曲风，就能生成 30 秒商品 MV。作者实测炸鸡、塑料板凳和耳机等案例，可换语言、模特与场景测试不同市场。

  * **[《一句话生成原理科普视频》](https://mp.weixin.qq.com/s?__biz=MzIyMzA5NjEyMA==&mid=2647687109&idx=1&sn=032fd9f6aab5ee20ea5d14f97bf48a86)**：数字生命卡兹克实测开源 Skill Anatomy：一句话生成带讲解和配音的原理科普视频。5 分钟视频约消耗 Claude Max 周额度 1%，Opus 5.5 生成约 1 个半小时。

  * **[《QBS 三步法：陌生领域快速成 skill》](https://mp.weixin.qq.com/s?__biz=Mzg3MTk3NzYzNw==&mid=2247511489&idx=1&sn=dcb0e5f18a5263fd5fa0fa166a055c05)**：卡尔开源 QBS 方法：Question、Book、Skill，让 GPT-6 找书、读章节、提炼规则，再用新任务测试。附时间管理示例和生成的 skill。
