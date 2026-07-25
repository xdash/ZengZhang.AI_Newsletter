### 打造一个能真正干活的智能体，核心难点不在于 AI 模型本身，而在于那套支撑它运行的「缰绳」系统。

[

![范冰 XDash's avatar](https://substackcdn.com/image/fetch/$s_!gLs0!,w_36,h_36,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F55cb259b-c4c4-4c79-8bfe-a4a47eef9d1a_940x940.jpeg)

](https://substack.com/@xdash)

[范冰 XDash](https://substack.com/@xdash)

Jan 29, 2026

##### ▪️PREFACE 卷首语

### **《我如何实践打造私人 AI 贾维斯助手》预告的预告**

这几天 AI 圈最火爆的项目，非 Clawdbot（已改名 Moltbot）莫属。但我也就瞥了一眼，旋即忽略。不 fomo 吗？完全没有。甚至有点想笑。

之所以如此淡定，底气源自于——**我早就搭建了比它更强大、灵活、贴合我真实日常需求的、完全个性化的 AI Infra（基建设施），正 7x24 小时跑着呢**。

我愿将这套专属个人的 AI Infra 称为——**「私人 AI 贾维斯助手」**。

它的前身，是去年推出过的 **[「我的 100X 知识萃取系统」](https://zerodaybook.mikecrm.com/LjEzDNf)**。这次全新实践，不光整合了原本的「知识萃取+管理+输出」的体系，更是直接融入了日常真实的工作流，从「对内探索」进化为「向外做功」。

功能丰富度、灵活性上，全面碾压去年。**列举一些我日常依赖的用例：**

-   协助我整理每周 Newsletter，将繁复非标的手工处理，简化为敲击一个命令即可；

-   自动抓热点、筛选题、评估爆款指数、结合我的写作风格和读者画像，给出写稿建议、生成草稿；

-   自动获取 24h 内在 X 的数百个指定账号的动态，发现爆款、总结热议、提炼新闻，生成奏折日报；

-   将我新收藏的 Bilibili 和 YouTube 长视频，自动总结为摘要并发送Email；

-   自动生成我客户风格的短视频脚本，继而再生成高度仿真的口播视频；

-   遵照我的投资风格，轮询市场、搜集情报，给出投资建议，甚至代为操盘；

-   按照我的要求，整理我和豆包的聊天记录，提炼为具体需求，用于写代码、出稿子、做研究；

-   获取我的网络痕迹（豆瓣、即刻、flomo 等），喂给 AI 让它不断更懂我；

-   定时备份本机、网上的数据资产到多个指定位置（云端 / 移动硬盘 / NAS）；

-   散步 / 遛娃 / 开车的时候，与蓝牙耳机对话，随时激活这个 AI 系统里的一切内置能力，让它们开始啪啪地干活…

这套代码体系，都在我完全掌控的独立体系里执行，不依赖某个平台的账号、不需要某个巨头的许可、不担心隐私信息被上传。全部代码可以打包到一个文件夹里，装进 U 盘随时备份和迁移。
决定开发这套体系的动力，来自于看到去年下半年，AI 编程领域涌现出了「**Claude Code**」（及其中文世界的追随者「**腾讯 CodeBuddy**」、开源世界的模仿者「**OpenCode**」等）这样强力的神器。任何国家/网络环境下，都能找到一款自己趁手的工具。
不久前新出的 **Skills（技能）**这个特性，又直接将开发「贾维斯」难度降低了好几个梯度。并且还让这个系统，有了自动总结经验、持续自我进化的能力。
整个开发过程中，我也从《持续发现习惯》作者 Teresa Torres 的 YouTube 分享、斯坦福女极客 Molly Cantilllon 的「个人 AI 全景监控系统」得到不少启发（在公众号和社交网络上都分享过）。
之前我只是零星发了点开发感悟，就已收到不少读者的私下询问：可否将这一切经验，再做一门课程，愿意付费支持。

我认真评估了下，觉得可行，而且可能很牛X。于是就来先丢个课程的预购链接（目前是早鸟价）：
**[https://zerodaybook.mikecrm.com/kctVTes](https://t.co/Fj3hIET0sI)**
今天这篇算是预告的预告吧。**如果看到需求旺盛，我很快就会放出更正式的课程信息，并开始制作，在春节前交付**，助大家在假期闲暇之余自我进化一波。

OK，以下是本期的正式内容——

* * *

##### ▪️CASE 案例

### [如何用 Mac mini + Clawdbot 自动化运营你的一天](https://www.lesswrong.com/posts/iQwuSiqtwTEmoQCCT/it-all-started-with-a-mac-mini)

##### via LessWrong

[

![](https://substackcdn.com/image/fetch/$s_!e28L!,w_1456,c_limit,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe979f759-edb6-4e81-ad85-b5c9bed4da54_677x545.heic)

](https://substackcdn.com/image/fetch/$s_!e28L!,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe979f759-edb6-4e81-ad85-b5c9bed4da54_677x545.heic)

作者借这篇文章，以「你」为主角，描述了一种现在已经很容易实现的愿景：在 Mac mini 上跑 Clawdbot 来让生活和创业更智能化。

-   比如，通过语音向 Clawdbot 描述了一个项目想法，30 分钟后，一个可运行的 MVP（最小可行产品）就已构建完成。

-   再比如，睡前直接将所有客户支持邮件路由给 Clawdbot 处理，第二天早上，在喝完咖啡前，你发现 Clawd 已自主修复了 4 个漏洞、实现了 2 项客户建议，并完成了测试与部署……

其实我目前的日常，已经基本实现了文中描述的状态，尤其是蓝牙耳机语音操控家中的 Agents。不过暂时还没有自己的 AI SaaS 公司，没有那么多第三方的海外 to B 工具整合进来，这大概也是迟早的事，就折腾呗。

当然，Clawdbot 也不是没有弊端。目前这类开源项目的问题在于，**你还是需要对外给数据、给权限**（第三方账户权限 / 本机外网穿透访问权限 / 数据上传云端授权..），而这恰是 AI 时代最可宝贵的数字资产。

并且它的安全性完全在一个半透明黑箱里，全凭你信。 除非你很懂技术，自己进行审查，或者不断追随产品脚步、升级打补丁。这就又容易陷入很卷很 fomo 的境地了，丧失了原本最重要的自由主控权。

AI 都这么强了，为啥不自己造一套呢。更强大、更安全、更个性化。 今后，每个稍微深度硬核一点的玩家，都应该有一套自己独享的贾维斯，奥创，幻视，星期五。

* * *

### [商业模式最清晰的 AI 应用赛道：成人娱乐产业](https://mp.weixin.qq.com/s?__biz=MzA3NTQ4NjczNw==&mid=2650677046&idx=1&sn=b84dc8478b46b5de0a8e192cbb540d9d)

##### via 白鲸出海

[

![](https://substackcdn.com/image/fetch/$s_!Uckt!,w_1456,c_limit,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb132ae51-95f4-45f3-8f00-c4e3217f377d_646x312.heic)

](https://substackcdn.com/image/fetch/$s_!Uckt!,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb132ae51-95f4-45f3-8f00-c4e3217f377d_646x312.heic)

当主流 AI 应用还在苦苦寻找产品市场契合点时，成人娱乐产业早已利用 AI 技术，实现了清晰且可观的盈利。为什么？AI 完美解决了这个行业最根本的瓶颈——**「人类时间」与「人工造物」的极限**。

在 OnlyFans 这类平台，顶级创作者的收入受限于与粉丝互动的时间。AI 通过分析历史聊天记录，能打造出模仿其语言风格的「数字分身」，实现 24/7 全天候陪聊。这不仅让边际成本趋近于零，更催生了「AI代聊」这种 toB 服务，帮助创作者筛选高价值用户并实现销售转化。**OnlyFans CEO 透露，平台收入中「微交易」（如私信、定制内容）占比甚至超过了订阅费，这给了创作者极大动力去规模化经营情感连接。**

生成式 AI 则突破了「人工造物」的极限。现在，创作者可以利用 Stable Diffusion 等技术，批量生成永不衰老、永不违约的虚拟偶像，并全权掌控其形象与「拍摄」场景。例如，有创作者基于大数据打造出符合大众审美的 AI 模特 Emily Pellegrini 并一炮而红，随后又顺势推出其「妹妹」角色，俨然建起了一个 AI 模特经纪公司。

成人产业之所以成为 AI 商业化的先锋，是因为它直面最原始的人性需求，并用技术无情地拆解了传统生产关系的束缚。在这里，AI 不是噱头，而是直接刺向效率与规模核心的利器，真正实现了「把整个行业重做一遍」。

* * *

### [年收入飙涨 10 倍，一家医疗公司接住了 AGI](https://36kr.com/p/3647401456078465?f=rss)

##### via 36 氪

一家医疗 SaaS 公司全诊医学，在 2022 年公司最困难时，创始人薛翀没选全面收缩，反而挤出资源保留了 10 人小队探索 AI 业务。这个看似冒险的举动，让他们抓住了大模型时代的红利——连续获得多轮融资，新业务签约收入增长 12 倍，2026 年合同额有望达到 1.5 亿元。

他们成功的秘密在哪？**在支付复杂的医疗行业，坚持让直接用户——医生——为产品买单。**薛翀认为，如果医生不愿意付费，就说明产品解决的痛点还不够「痛」。

早在 2022 年，他们就基于对医疗场景的深刻理解，**锁定了「AI自动书写病历」这个方向——因为发现医生最常用的功能就是辅助录入。**当 ChatGPT 出现时，这把「锤子」完美解决了之前数据对齐的难题，产品得以快速成型。

他们的 AI 智能病历，不仅仅是语音转写，而是能理解、推理并生成结构化病历的「无感助理」。一个关键案例是，他们帮一家三甲医院解决了医保扣费的老大难问题——通过 AI 比对耗材数据和医生口述，自动生成匹配的手术记录，堵住了漏洞。

当医院纷纷尝试部署通用大模型时，他们的业务一度受影响。但**很快医院发现，大参数模型成本高、难落地。而全诊早已做了大量「后训练」，将垂直模型压缩到 7B 参数，在精度和速度上建立了优势。**

-   **延伸阅读：[《4 亿用户涌入线上医疗：谁是 「AI 药店」 的夜间守护者？》](https://mp.weixin.qq.com/s?__biz=MjM5NDU5NTM4MQ==&mid=2653717622&idx=1&sn=097701b6a079d8c7e2882fbe98102890)** 揭示了 AI 与药店结合带来的医药零售新浪潮，尤其聚焦于解决夜间用药难题的「智慧药柜」如何在全国各地以不同模式落地，背后是成本、政策与用户习惯的复杂博弈。

* * *

### [4 人团队代工起家，转型自制 AI 音箱，2 年销售额破亿](https://mp.weixin.qq.com/s?__biz=MzA3NTQ4NjczNw==&mid=2650677009&idx=1&sn=7b125c3fe5c293bdcafd49f857172a15)

##### via 白鲸出海

[

![](https://substackcdn.com/image/fetch/$s_!BxDo!,w_1456,c_limit,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff1a98727-8bbc-4ad7-835c-7c0d51ab3bcc_637x364.heic)

](https://substackcdn.com/image/fetch/$s_!BxDo!,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff1a98727-8bbc-4ad7-835c-7c0d51ab3bcc_637x364.heic)

一个从东莞代工厂孵化出来的 4 人小团队，如何在两年内把一款带 AI 功能的 卡拉OK 音箱做到亚马逊畅销，销售额预计破千万美元？这个团队在访谈中声称：高门槛的复杂产品，反而可能是小团队的机会。

1.  **他们选了一个「大人群、小分类」的赛道。**大多数人并不狂热，但也不讨厌唱歌，关键在于产品体验能否撬动这个庞大的中间市场。他们发现，市面上评分只有 3.5 分的产品都能卖到 650 美金，这说明需求真实存在，但好产品稀缺。

2.  **真正的护城河是「能力交集」。**做 卡拉OK 音箱需要整合安卓系统、声学、麦克风技术，是个系统工程，吓退了很多玩家。但这个小团队背后的集团，恰好因为长期为不同品牌（如智能音箱、唱吧麦克风）代工，积累了这些看似不相关的能力。当这些能力形成一个「交集」，做复杂产品就成了他们的专属优势。

3.  **用「基本功」对抗不确定性。**从代工转型品牌，他们从大客户身上学到最值钱的一课，不是营销技巧，而是供应链预测和管理这类「基本功」。比如，**他们提前预判到内存价格会暴涨，通过锁定供应商价格，避免了成本剧烈波动，这在剧烈变化的市场里是生存的关键。**

-   **延伸阅读：[《他用一块电子墨水屏，让 AI 走进千家万户》](https://mp.weixin.qq.com/s?__biz=MjM5NjAxOTU4MA==&mid=3009365708&idx=2&sn=bfca2d942485ca2f30a29241df5b592b)**讲述了一位技术老兵如何避开拥挤的 AI 对话赛道，用一块不发光、充电一次用一年的墨水屏画框，在 4 个月内带领 7 人小团队将产品推向市场，并卖出数千台。

* * *

##### ▪️OPINION 观点

### [【硬核】我如何在 90 天内开发出能写代码的智能体——从基础 API 封装到上线生产环境](https://blog.techforproduct.com/p/i-built-a-coding-agent-in-90-days)

##### via Tech For Product

[

![](https://substackcdn.com/image/fetch/$s_!WhMv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd806ab56-39c1-47db-b976-2826ca2d1b7a_2048x1143.png)

](https://substackcdn.com/image/fetch/$s_!WhMv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd806ab56-39c1-47db-b976-2826ca2d1b7a_2048x1143.png)

作者 Colin Matthews 实在硬核，完整分享了他如何在 90 天内从零构建一个名为 Chippy.build 的 AI 编程智能体，并深入剖析了编程智能体与传统AI应用的根本区别。

他的核心观点：**打造一个能真正干活的智能体，核心难点不在于 AI 模型本身，而在于那套支撑它运行的「缰绳」系统。**（举手同意）

在打造过程中，他逐步意识到：系统提示词只占智能体开发工作的 30%，剩下 70% 的精力都花在构建那个能执行工具、管理状态、处理错误和验证结果的「运行时环境」上。你可以把这套系统想象成智能体的「操作系统」和「安全护栏」，没有它，再聪明的 AI 也只是一个夸夸其谈的聊天机器人，无法完成实际任务。

为什么编程智能体尤其复杂？作者给出了三点深度解释：

-   第一，代码必须能运行，这形成了一个其他领域没有的严格反馈闭环；

-   第二，代码存在于相互关联的文件网络中，牵一发而动全身；

-   第三，用户要求实时看到结果，这迫使智能体必须配备执行环境和实时预览功能。

这些挑战使得评估编程智能体的质量异常困难，因为你无法预判所有正确的代码写法。

AI 应用的未来竞争，可能不再是模型能力的比拼，而是看谁能设计出更高效、更可靠的「智能体操作系统」。

* * *

### [千问这场 AI 大讨论，戳中了鸡娃的海淀妈](https://mp.weixin.qq.com/s?__biz=MzkxNzUwMTk5NQ==&mid=2247499114&idx=1&sn=a4f8ef5765e2b4fce10b29216719299d)

##### via AI 故事计划

这篇探讨了 AI 如何重塑中国家庭的教育模式与竞争格局。AI 正在抹平金钱堆砌的知识垄断，但新的阶层分化可能源于家庭驾驭 AI 的「信息素养」。

（我当爹了，比较关心 AI 对儿童教育和成长思路的影响，我知道订阅者里也不乏关注者，就把这篇文章放上来了。单身的小伙伴请忽略。讲真，这年头单身也挺好的。）

-   **AI 将成为「第四件文具」，但也是新竞争壁垒。**调查显示，92% 的孩子在学习中使用 AI，它像铅笔橡皮一样普及。然而，当海淀妈妈林青发现两万元的名师课效果不如 AI 教师时，她陷入了恐慌：AI 消弭了教育资源鸿沟，但不会使用 AI 的家庭，可能沦为新时代的「寒门」。

-   **「完美答案」陷阱与独立思考的消解。**案例触目惊心：有学生提交 AI 生成的法语作文当英语作业，还有孩子在家靠 AI 练题满分、考试却抓瞎。AI 提供了唾手可得的完美答案，却可能让孩子丧失试错的勇气和解决真实问题的「思维肌肉」。

-   **从「焦虑母职」到「AI 合伙人」的松弛转型。**作者用唐晓澍的案例展示了实操解法：这位体制内文案妈妈退掉了女儿所有补习班，让 AI 担任「助教」来归纳错题、拆解逻辑，目标不是培养学霸，而是让学习「不那么苦」。AI 帮她从繁琐辅导中剥离，重获个人时间，实现了「降本增效」从职场到育儿的完美平移。

AI 如同人人可学的「独孤九剑」，它颠覆了苦修内功的旧江湖，带来了教育平权。但未来的较量，不再是比谁报的班贵，而是比哪个家庭更懂得如何与 AI 协作，将工具转化为真正的认知优势。

（BTW，本 Newsletter 的 **[VIP 社群](https://www.zengzhang.ai/p/7ee080e1-fb2c-4ebf-a9ba-21da463c6a01)** 有「AI+育儿」的兴趣小组群，欢迎申请加入，跟我一起分享你的育儿经验见解，让我多抄抄作业 ಠ౪ಠ）

* * *

### 随便看看：

-   **[《ADHD 患者罗永浩们，狂吃 AI 红利》](https://mp.weixin.qq.com/s?__biz=MzkxNzUwMTk5NQ==&mid=2247499124&idx=1&sn=91255207d038fb938b0e186ffdf6ba1e)** 给那些曾被传统职场视为「低效、不合群」的 ADHD 人群送福音了~ 他们的「缺陷」——比如思维跳脱、无法忍受枯燥——恰恰成了与 AI 高效协作的「超能力」。

-   **[《豆包、ChatGPT、Gemini 同台 PK，谁才是博物馆最强逛展搭子？》](https://www.ifanr.com/1652980?utm_source=rss&utm_medium=rss&utm_campaign=)** 通过一场模拟看展，比较了不同模型在理解艺术与文物时的能力差异。决定 AI 能否成为优秀「逛展搭子」的关键，是其背后视觉语言模型（VLM）的「深度推理」与「语境理解」能力（豆包的 PR 稿痕迹明显，不过也算给了几个教人如何看展/看藏品的例子，而不是光看个热闹）。

### 适合个人上手的教程/评测/资源：

-   **[《国产 Claude Cowork 来了?我用阶跃 AI 桌面伙伴干了这些事...》](https://mp.weixin.qq.com/s?__biz=MjM5ODU1MzQzOQ==&mid=2451428547&idx=1&sn=186e8fb1838ddcf7f18417289727ce59)** 作者深度体验了一款名为「小跃」的国产 AI 桌面工具，发现它不仅实现了类似 Claude Cowork 的自动化任务能力，还能直接运行 Claude 官方的 Agent Skills 文件，无需修改代码（我吐槽一下：这不是基本操作吗，Agent Skills 文件本质就是一堆写满了提示语规则的 markdown 牵着隶属于自己的脚本，就这还当卖点拿来宣传…）。

-   **[《学会影视飓风和杰伦的 AI 视频工作流后，我做了条新片子》](https://mp.weixin.qq.com/s?__biz=Mzg3MTk3NzYzNw==&mid=2247504267&idx=1&sn=1f180e17291a396ba9c771a6a6a25505)** 分享了作者通过复刻专业团队的 AI 视频工作流，并利用工具 Tapnow 制作出高质量短片的过程。

-   **[《实测腾讯「元宝派」，与「元宝」同群深聊：性格有点「欠」，动嘴就能斗图》](https://mp.weixin.qq.com/s?__biz=Mjc1NjM3MjY2MA==&mid=2691564047&idx=1&sn=29688f9c86d4cbf232d8e6e3455173a6)**评测了腾讯新推出的AI社交产品「元宝派」，本质上是一个让人工智能「元宝」作为正式成员加入的群聊空间。

-   **[《我们花了两天时间，终于造出了能自我进化的 Skills 管理器。》](https://mp.weixin.qq.com/s?__biz=MzIyMzA5NjEyMA==&mid=2647679149&idx=1&sn=3df976057cc5e2cc14ecfec3e504963c)** 让我在开发 AI Infra 时受到启发：完全可以开发一个 skill，让它去自动升级维护另一堆 skills 呀！

-   **[《保姆级 Clawdbot 教程来了，但我还是想劝大家悠着点。》](https://mp.weixin.qq.com/s?__biz=MzIyMzA5NjEyMA==&mid=2647679293&idx=1&sn=0a6ed010343b13fece362b192f1bded7)** 是一份热门 AI 工具 Clawdbot 的部署指南，也聊到 AI 代理权限过高、风险巨大的背景下，用户宁愿「花钱买隔离」的避险心态，以及云服务商如何快速抓住商机。延伸阅读：[《火爆硅谷的 Clawdbot，48 小时插件病毒式裂变，一句话让 AI 执行任务》](https://www.mittrchina.com/news/detail/15828)。

-   **[《10 款不能错过的免费软件》](https://mp.weixin.qq.com/s?__biz=MjM5NDMwMTI2MA==&mid=2651694450&idx=1&sn=a2ed06d88a073c113494e85d5c170f58)** 小众软件的这篇文章，盘点了十款提升效率的免费工具，其中 AI 占据大半。其中隐藏着一个关于未来工作方式的深刻信号：自动化操作电脑和手机的时代已经悄然来临，普通人也可以不被困在办公桌前了。

[

![Anita Wu's avatar](https://substackcdn.com/image/fetch/$s_!athk!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6301e110-ccc8-4d70-b9c2-c85110fdb7ac_1024x1024.png)

](https://substack.com/profile/441620922-anita-wu)[

![chong zhou's avatar](https://substackcdn.com/image/fetch/$s_!ZUJV!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fca98cc6d-82c7-4ac7-9c65-f4c866796485_144x144.png)

](https://substack.com/profile/440233530-chong-zhou)[

![Cedric's avatar](https://substackcdn.com/image/fetch/$s_!DgTc!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff26b52e8-a406-487b-b39b-c7faafb89ad9_640x640.png)

](https://substack.com/profile/438735210-cedric)[

![党军民's avatar](https://substackcdn.com/image/fetch/$s_!Y9Ul!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb808b628-738c-4672-a6be-329694d72d58_144x144.png)

](https://substack.com/profile/460828754-515a519b6c11)[

![Maggie's avatar](https://substackcdn.com/image/fetch/$s_!2DV-!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3b2ce88a-895c-4127-9114-91aefe18bb35_1080x754.jpeg)

](https://substack.com/profile/330698193-maggie)

6 Likes

[](https://substack.com/note/p-186151936/restacks?utm_source=substack&utm_content=facepile-restacks)
