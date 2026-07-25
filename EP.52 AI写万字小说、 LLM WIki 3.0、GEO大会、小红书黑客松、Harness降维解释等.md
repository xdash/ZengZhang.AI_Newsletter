### 「找到和 AI 正交的因素去 compounding。」

[

![范冰 XDash's avatar](https://substackcdn.com/image/fetch/$s_!gLs0!,w_36,h_36,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F55cb259b-c4c4-4c79-8bfe-a4a47eef9d1a_940x940.jpeg)

](https://substack.com/@xdash)

[范冰 XDash](https://substack.com/@xdash)

Apr 16, 2026

1/ 一晃这个周更 Newsletter 都写到 EP #52 了。算上中间偶尔停更的那一两期，满打满算也是写满一年了。目前也仍是最大的中文 AI 商业类 Newsletter。

期间 AI 光速发展，我的技术栈也迭代了好几版。从最开始希望逐渐全自动完成，到现在坚定了用**机器帮我半自动分拣 + 最终人工精拣筛**，也算摸出了固定套路。

域名注册为 ZengZhang.ai，原本还是想从老本行的「商业增长」视角切入，不采编纯技术向（却没结合实际应用场景落地的）内容。但发现即便是聚焦在商业领域，市面上公开披露的案例，仍会有大量浅薄重复的，观点也不乏空泛的宏大叙事或孱弱的未来预测。

所以现在我完全按我主观标准，剔除掉自己懒得看的东西——哪怕它们发布在名号响亮的（自）媒体，哪怕原始的点击量很高。我尤其不喜欢制造 FOMO 却不给解药、只为博眼球的内容，它们在我的系统里打分被降权是最厉害的。

至于坚持更新的动力，除了自己有强意愿去追 AI 最新的真·干货，还是偶尔会放点广告推荐和知识售卖，作为补贴持续运营的零花钱。我看到推上虽有人吐槽，却也话锋一转旋即表示理解，并继续热情推荐他人来订阅。爱你们哟。

2/ 今天这期的广告环节（这不就来了），推荐一下抖音 460+ 万粉丝的 @姜胡说 推出的小报童付费专栏**《从素人到百万大v，老伙计们的闭门课》**，分享他做短视频的方法论（原则、经验、技巧），赚钱的思路，以及如何完成一本书的尝试。

已更新了 15 万字，有 6000+ 人购买。感兴趣的可以通过 **[这个链接](https://xiaobot.net/p/jhs20250718?refer=af038a9b-c8fe-4429-9eee-f96a3211eec4)** 到微信中购买订阅，价格是 168 元，我会从中获取佣金，并且看到支持者的微信昵称。

OK，以下是本期的内容 ——

* * *

##### ▪️CASE 案例

### **[我用 Claude Code 写了一部 5 万字小说，投稿七猫，被拒了](https://mp.weixin.qq.com/s?__biz=MzU3MTcxOTg4OQ==&mid=2247484438&idx=1&sn=f2f6dde9baf3d2b024f0a44063b97abe&chksm=fdea919c578db4ca95f6bc59ac294f1e5a88724ee7ae021c14b20f80dd31f1e5fce71a917a58&mpshare=1&scene=1&srcid=0410YzM0kKGD0ssYa7dUUwo8&sharer_shareinfo=cba1a6f90bd51aaf6038aaa4c052ab2b&sharer_shareinfo_first=cba1a6f90bd51aaf6038aaa4c052ab2b)**

##### via 月月鸟

我一直有个疑问：用 AI 写网络小说赚稿费，有没有搞头？作者实际尝试了下，用 Claude Code 写完一部五万字小说，结果投出去两天就被拒了。

他复盘了整个流程：**用一个专为中文小说设计的 Skill，解决了 AI 长文本中人物状态丢失的核心痛点，通过章节摘要自动追踪机制，**写出的稿子质量居然达到了及格线。

但进入真实商业场景后，短板暴露了。七猫小说网两天就拒稿，理由是什么？**节奏把控、爽点设计、情绪感染力都不到位**——网文市场最看重的这些维度，他没写出来。

整个投稿流程倒是很丝滑：从选平台、分析投稿要求到撰写申请书，全由 AI 代劳。我觉得作者再钻深一点，把前面提到的拒稿理由再悉心打磨到位一番，或许真能形成 SOP，骗过七猫的审核 AI 呢..

* * *

### **[一篇文章卖了 20 万，开源 CC+Obsidian 打造的 LLM Wiki 内容创作 3.0 系统](https://mp.weixin.qq.com/s?__biz=MjM5NDI4MTY3NA==&mid=2257499566&idx=1&sn=36b9fee6ac54e6b61f91120b0e74ba9e&chksm=a49e23d181bac400c4d65135dbc1deab459217e32152502184fd3eefe5446b71fd11e91109d2&mpshare=1&scene=1&srcid=0415zmBE80S85EpQbbM3icmf&sharer_shareinfo=9cc6ac3b5288bf3ae7c355712fa9a25a&sharer_shareinfo_first=932b39e24dd02c3438f85a9af609aa19)**

##### via 饼干哥哥AGI

[

![](https://substackcdn.com/image/fetch/$s_!U8Bn!,w_1456,c_limit,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe92b475f-85eb-4e9d-b8ac-c1eef342f4b5_673x425.heic)

](https://substackcdn.com/image/fetch/$s_!U8Bn!,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe92b475f-85eb-4e9d-b8ac-c1eef342f4b5_673x425.heic)

作者借鉴近期很火的 Karpathy 的 LLM Wiki 方法论，并增加了自己的独特迭代，升级到 3.0 知识编译——让 AI 从临时检索者变成知识资产的持续维护者。具体三步：**新内容自动编译整合、Wiki 页面持续更新、沉淀成可复用的资产。**全文图文并茂，十分详尽，也给了我新的启发。

这套方案为依赖 AI 进行深度内容创作的从业者，提供了一条从工具自动化迈向知识系统化的可行路径。

* * *

### **[程序员养龟有多离谱？我让 Claude Code 每天给我发乌龟行为报告](https://www.huxiu.com/article/4849810.html?f=rss)**

##### via 叶水水

[

![](https://substackcdn.com/image/fetch/$s_!NE6t!,w_1456,c_limit,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0fe6aed0-9857-4e3f-87ab-8df1c6af2da6_767x964.heic)

](https://substackcdn.com/image/fetch/$s_!NE6t!,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0fe6aed0-9857-4e3f-87ab-8df1c6af2da6_767x964.heic)

养龟这件事，被一个程序员玩出了花——水温监控、行为分析、录像推送，全是 AI 在跑。很喜欢这类极客实操的复盘内容。

他通过自然语言与 Claude Code 对话，零代码构建了一套智能宠物监护系统：直接配置 Home Assistant 仪表盘与自动化规则，实现水温、加热棒功率等数据的集中监控与异常告警；活动监测环节，AI 自主完成从录像抽帧对比、生成精华视频到调用本地大模型 Gemma 进行行为分析的全套流程。

这里面有几个关键性能优化判断：**传文件头而非整个视频、用 ffmpeg 直接裁切。整个系统架构整合了 HA、NAS 与闲置 Mac，以近乎零成本运行。**

作者的角色由此从程序员转变为提出需求、验收效果的产品经理。AI 编程助手已能深度理解复杂需求并做出合理的技术选型，将对话直接转化为可运行的系统——但并未消解对问题拆解与架构设计能力的需求。

* * *

##### ▪️OPINION 观点

### **[从 SEO 到 GEO，从流量到 Agent，真正的变化才刚刚开始](https://x.com/yaojingang/status/2043206958610801126)**

##### via yaojingang

北京首场 GEO 大会上，几位专家分享了关键洞察，被总结这篇成了长推文。例如：

-   阎志涛指出，AI 时代的核心从 ranking 转向 AI visibility，流量可能下跌但业绩未必，因为 AI 先影响用户心智；原创数据成为独特资产，而 GEO 最终越来越像做品牌。

-   张凯的实验数据揭示，官网仍是 AI 引用的核心资产（占比约 50%），内容需结构化、事实导向，1000 到 3000 词为佳；ChatGPT 优化需做深单页，Google 优化需做多页面。

-   拔刀刘强调数据是 GEO 优化的起点，品牌在 AI 中的可见度是一个需要数据破解的黑盒；AI 搜索转化率更高源于用户意图表达更完整，移动端是关键战场。

从业者需从流量思维转向信任与品牌思维，从理解算法黑盒转向基于自身业务构建独特的数据与内容体系。

* * *

### **[一文带你看懂，火爆全网的 Harness Engineering 到底是个啥。](https://mp.weixin.qq.com/s?__biz=MzIyMzA5NjEyMA==&mid=2647681527&idx=1&sn=27dfac445fe88042e182ab3f3c6388b0&chksm=f1274993a629284dad7296661777c495c678fb94540ff927b229264eb7449c2e82a48245f02d&mpshare=1&scene=1&srcid=04156eFz7fakVHQT1nSp4Ftw&sharer_shareinfo=3baca4df46f479777a40a432d46acb1f&sharer_shareinfo_first=3baca4df46f479777a40a432d46acb1f)**

##### via 卡兹克

[

![](https://substackcdn.com/image/fetch/$s_!VKkj!,w_1456,c_limit,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5bcaea79-b2b6-4a71-9ee7-ee6af0ef686a_650x369.heic)

](https://substackcdn.com/image/fetch/$s_!VKkj!,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5bcaea79-b2b6-4a71-9ee7-ee6af0ef686a_650x369.heic)

**AI 行业催生了三次跃迁：Prompt Engineering → Context Engineering → Harness Engineering。**这本质上映射了人类对 AI 认知与控制方式的根本转变。

作者用游戏做类比：三个阶段分别对应《只狼》的手动操作、《金铲铲之战》的前期配置、《全面战争》的系统驾驭——控制粒度从精细到宏观，AI 自主性从低到高。

**Harness Engineering 的核心在于构建一套系统性的规则与约束来驾驭高度自主的 AI 智能体。**其兴起反映了模型能力已超越单点提示或上下文管理的阶段。对于从业者而言，理解这一脉络是把握未来人机协作范式的基础。这篇文章将 Harness 讲解得深入浅出，不懂的看这篇基本够了。

**延伸阅读：**

-   **《[Harness 刚火，可能就要成为过去时了](https://mp.weixin.qq.com/s?__biz=Mjc1NjM3MjY2MA==&mid=2691566996&idx=1&sn=c8d313585dfd940a2e6a7a37783c8aeb&chksm=a8ef761f45c0367feafcbd0a0351ce6133d2b7e8f3340d0e5321e90177fa7861d133a5e677b5&mpshare=1&scene=1&srcid=0414P3S6U44sz5P6bBDuVbeY&sharer_shareinfo=1bf3b79a1b2eddefaa47bedd03cb17ef&sharer_shareinfo_first=96885eaf801fe32839b2789e72197757)》：**模型性能下降并非因为能力不足或信息丢失，而是模型在长上下文中主动选择了「偷懒」。未来的方向或许不是更复杂的工程管控，而是需要引导或激励模型进行更深层、更耗能的「分析式」推理。

* * *

### **[Reid Hoffman says leaders need to update their AI strategy. His advice: weekly check-ins.](https://www.businessinsider.com/reid-hoffman-leaders-fix-ai-strategy-2026-4)**

##### via Ben Shimkus

LinkedIn 创始人/ 「Paypal 黑帮」核心成员的 Reid Hoffman 指出了一个老派思维的陷阱：**许多高管仍在沿用「小范围测试-形成概念验证-全面推广」的旧有软件部署模式，这完全不适合 AI**。

他认为正确的做法是，鼓励员工在全公司范围内快速探索 AI 工具的实际效用，并建立每周例会机制，让团队定期分享个人及集体在提升生产力方面的新尝试与心得。

此外，Hoffman 本人对当前 AI 在投资决策上的应用持怀疑态度，认为其建议仅是「商学院水平的平庸答案」，无法真正创造风险投资回报。

* * *

### 随便看看：

-   **[《看完小红书黑客松的 59 个热血团队，我们想推荐这 6 个》](https://mp.weixin.qq.com/s?__biz=MzkyNjU2ODM2NQ==&mid=2247627426&idx=1&sn=56590ff8f6451d64286431412de3a299&chksm=c3dc98b9e9154a481a9173c88d276c4ea8caaea31c3c3504243c88c76ceaf53d5a08c9efd8ec&mpshare=1&scene=1&srcid=0412Si9ijSVSDozpJSdUj8dD&sharer_shareinfo=689d685752e94842d7ecc1b58f75d706&sharer_shareinfo_first=45d2077d396ca86f51d52476c7cebdbd)**：小红书办了场 AI 黑客松，59 个团队参加。看完之后挑了 6 个有意思的。

-   **[《AI 高维向量空间里，「觉悟」的邻居是谁？一次跨越东西方的语义探索》](https://mp.weixin.qq.com/s?__biz=MjM5MzM4MzQwMw==&mid=2652889905&idx=1&sn=edbf24783d4d410e858c014b9abdfe19&chksm=bcf89ded5f205bddebe9dad985e114750134f90eac15fe44688499f730bf8a5fa2ec25ba470f&mpshare=1&scene=1&srcid=0413Hk3iP2LTybi4ru34NirE&sharer_shareinfo=680c1bc697dab53dbae955dea0844986&sharer_shareinfo_first=680c1bc697dab53dbae955dea0844986)**：把「觉悟」丢进 AI 的向量空间里，它的邻居是谁？答案是死亡、疯狂、孤独、虚无、痛苦等存在主义核心概念。

-   **[《1.2 亿观众，见证 AI 漫剧从狂热到崩塌》](https://www.huxiu.com/article/4850549.html?f=rss)：**极致的效率追求催生了「文化垃圾」——从业者用爬虫扒剧本、偷脸生成角色、充斥擦边与恶俗桥段，导致爆款率从 0.18% 跌至 0.12%。

-   **[《月薪 3000 的人，正在批量生产价值 243 亿的爆款。》](https://mp.weixin.qq.com/s?__biz=MzA5NDc1NzQ4MA==&mid=2654652931&idx=1&sn=94dfc4f2ec6e89e27742a4546a737871)：**AI 短剧这行，有一批人天天就是对着 AI 抽卡，他们工作枯燥、加班频繁且报酬低廉，实习生月薪仅 2-3k，社招平均 4-6k。但爆款率极低，2025 年上线超 6 万部作品，播放量破亿的不足百部。

-   **[《被网友吹上天的名人 AI，一开口我就知道是个水货。》](https://mp.weixin.qq.com/s?__biz=MzA5NDc1NzQ4MA==&mid=2654653260&idx=3&sn=cd8683856e8b73ca706dbe3306a900c7)：**名人数字分身的本质是缺乏灵魂的拟像，其深度与可靠性远被高估。这类 skill 通过喂食公开的传记、演讲等二手资料生成，只能模仿名人的表面语气和几个标志性案例，却无法触及决定其成功的默会知识与真实灵魂。

-   **[《IDG 李骁军最新的 52 条箴言》](https://mp.weixin.qq.com/s?__biz=MzYzNTA3NTgwNQ==&mid=2247484097&idx=1&sn=a939fdd8097d8a17ac4acb2b592e9989&scene=21&poc_token=HArB3WmjJeijZvo44kvbAesXHaxbr5GsScf5H6jH)**：提到了一些对 AI 的思考观点。

### 适合个人上手的教程/评测/资源：

-   **[《分享一个我用了 2 年的深度研究 Prompt，半小时帮你搞懂任何陌生领域。》](https://mp.weixin.qq.com/s?__biz=MzIyMzA5NjEyMA==&mid=2647681493&idx=1&sn=76f444ffcb134e6e8763d03fe03ae5ca&chksm=f1064cf8570d823db34578fcd7194141acef8d3e6085f465fdf9551b5a7ba2b0e5775006ef98&mpshare=1&scene=1&srcid=0413uLuKXYp2ANISTcFeRx6w&sharer_shareinfo=c8b9f5b3d4364b8abdecc949d7cf182b&sharer_shareinfo_first=c8b9f5b3d4364b8abdecc949d7cf182b)：**核心在于两条轴的交叉：纵向轴追溯事物从诞生至今的完整历史与因果链条，理解其演变轨迹；横向轴则在当下时间点进行赛道内的竞品对比，厘清市场定位与差异化优势。

-   **[《达尔文.skill 正式发布，一个无限进化的 skill 系统！》](https://x.com/AlchainHust/status/2043709317296361851)：**作者在手动维护超过 50 个 skill 后陷入瓶颈，受 Karpathy 的 autoresearch 项目启发，将「随机变异-自然选择」的进化逻辑迁移到 skill 优化领域，开发出达尔文.skill。该系统通过自动评估、修改、验证并借助 git 实现「棘轮机制」，确保 skill 质量只升不降。

-   **[《我怎么用 AI 辅助写作》](https://mp.weixin.qq.com/s?__biz=Mzg5NDY4ODM1MA==&mid=2247486011&idx=1&sn=66f7c5701ab2f61ab23c68c819050be3&chksm=c1c7f1ee024c81296f06e16fe1b3dacae09b17235c493ed090a76f5af2ea4a78fcae4c1c92df&mpshare=1&scene=1&srcid=0414qy0hFysoLUQEKpiVzJPC&sharer_shareinfo=baa33f6130a2af053f50ed41a83f0188&sharer_shareinfo_first=974be99c709c5637335d497ed7ae87ce)**：知识星球创始人分享了他的五步法：有所感（记录灵感）→ 和 AI 讨论（借助知识广度激发新想法）→ 提炼自己的观点 → 梳理结构 → AI 辅助整理与润饰。

-   **[《10 Open Projects for AI Security》](https://www.turingpost.com/p/aisecuritytools)**：十个保护 AI 安全的开源项目推荐，包括 NVIDIA NeMo Guardrails 用于控制模型行为并防御越狱和提示注入；Promptfoo 将 AI 安全转化为自动化测试与报告流程；LLM Guard 提供模块化交互安全工具包，专注净化、有害语言检测和数据防泄漏等。

-   **[《看不懂 Agent？我让 AI 花了一下午写了个 mini-OpenClaw》](https://www.huxiu.com/article/4849919.html?f=rss)：**OpenClaw 太复杂，于是有人让 AI 花了一下午，自己写了个简化版。

-   **[《AI 結合卡片盒筆記法，人不再操作軟體，用對話流程讓 Codex 搭建資料整理系統：我的兩個月實測心得》](http://www.playpcesor.com/2026/04/ai-codex.html)：**作者利用 ChatGPT Codex 等 AI Agent，通过对话指令自动抓取网页与视频内容、建立参考文献摘要、生成暂时与永久笔记、构建笔记间的链接和知识架构图，所有产出以 markdown 文件存于本地文件夹，实现了「工具即 AI 本身」，人无需操作传统笔记软件界面。

-   **[《量化基本面研究团队的 CLAUDE.md、Skills 和 Hooks 实战配置指南》](https://mp.weixin.qq.com/s?__biz=MzkxMTIxNzgyMw==&mid=2247489627&idx=1&sn=e9fdcfeea61876c2bdb10d55000d152b&chksm=c0f50cc8049c06f8d2b54479c36610ea1208cb4620cb5edbd45d2d80f7c384011826c46bba70&mpshare=1&scene=1&srcid=0412ky6ZK3ofay1MomVqHIOz&sharer_shareinfo=bee3fdeff61f0fad1bf7cb62bff50b1c&sharer_shareinfo_first=bee3fdeff61f0fad1bf7cb62bff50b1c)：**团队通过项目级 CLAUDE.md 为 AI 植入统一的「团队 DNA」，相当于共享的代码规范与工作流手册；利用 Skills 和 Hooks 构建类似量化策略框架的 AI 基础设施，将成员从重复性数据处理中解放出来。
