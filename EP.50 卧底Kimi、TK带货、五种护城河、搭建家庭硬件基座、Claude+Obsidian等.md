### 真正的护城河已从「难做的事」转向「难得到的东西」。

[

![范冰 XDash's avatar](https://substackcdn.com/image/fetch/$s_!gLs0!,w_36,h_36,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F55cb259b-c4c4-4c79-8bfe-a4a47eef9d1a_940x940.jpeg)

](https://substack.com/@xdash)

[范冰 XDash](https://substack.com/@xdash)

Apr 03, 2026

最近各家都开始出官方 CLI 了，我也开始陆续把自己常用的CLI（/MCP）整合进我自己的贾维斯了，包括 Podwise、飞书、滴答清单、flomo 等。

在此特别推荐 **[Podwise](https://podwise.ai?s_aff=XDash)** 新出的 CLI（[Github 主页](https://github.com/hardhackerlabs/podwise-cli)）。

以防你不知道：**Podwise 是我一直在用的「信息套利」工具，可以专门用来压榨那些有信息量的硬核播客/YouTube 视频的价值。**转录文字稿、总结洞察、信息可视化、同步笔记。推荐出去，用了都说好（[我之前录制过一期 YouTube 视频来介绍它](https://www.youtube.com/watch?v=9dl5ZKvDdMI)）。

我用它的 CLI 做了几个 skills，譬如直接将常听常看的节目的最新一期的文字稿（包括其他 AI 精炼内容），拉取到本地，经过我的信息系统处理后，整合到各种任务流中。

[

![](https://substackcdn.com/image/fetch/$s_!plqv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbee23bab-8bf5-4fed-9e67-e53c8c722f65_540x421.jpeg)

](https://substackcdn.com/image/fetch/$s_!plqv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbee23bab-8bf5-4fed-9e67-e53c8c722f65_540x421.jpeg)

你可以用我的专属优惠码 **XDash** 或点击这个链接（[https://podwise.ai?s\_aff=XDash](https://podwise.ai?s_aff=XDash)）获得 Podwise 的首充和续费会员的锁定惠率。

订购会员套餐后，就获取了正式的 AI 和 API 使用额度。你既可以在浏览器的赏心悦目的界面中，可视化地快速跳读原本的音视频内容，也能像我一样直接在 CLI 里撬动它内置的 AI 能力，而不用自己开发。简直不要太爽。墙裂推荐。

（这周我还是过滤掉了大部分的龙虾内容，所以本期内容体量有所减少）

OK，以下是本期的内容 ——

* * *

##### ▪️CASE 案例

### [Agent 的家：如何在 AI 时代搭建个人家庭硬件基座（硬核）](https://sspai.com/post/108064)

##### via 张立行

[

![](https://substackcdn.com/image/fetch/$s_!G4zf!,w_1456,c_limit,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1b39e932-cfe5-4a9e-9bfd-4497825bf588_1858x1022.heic)

](https://substackcdn.com/image/fetch/$s_!G4zf!,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1b39e932-cfe5-4a9e-9bfd-4497825bf588_1858x1022.heic)

作者军火展示一般地介绍了自己为 AI 配备的那些硬件设备，包括存储、调用、唤醒的等，并充分说明了各种设备的缘起、场景、体验评测、价格清单等，看得我津津有味。

比如，作者**经历过一次 NAS 崩溃的教训后，果断把数据存储和核心服务彻底分开。**之前图省事搞的 All-in-One 方案虽然方便，但数据安全实在伤不起。这本质上是用便利性换了可靠性。

他的桌面级硬件全景长这样：一台专管存储的 NAS，一台跑 PVE 和 Debian 容器的小主机承担所有自动化工具，作为局域网算力中心的 Mac Studio，以及一台 5,500 块收来的二手 x86 主机，显卡是 RTX 3060。这台机器被虚拟化切割成三块：跑本地多模态模型、24 小时在线的云端开发机、相对安全的公用 AI 实例。**最容易被忽视但至关重要的是软路由——整个架构的网络基石。**

AI 冲击传统行业的同时，反而创造了新的硬件机会和二手市场红利。那台高性能主机就是从倒闭的视频工作室淘来的。

这套架构让他能做到：纯语音指挥 AI，完成从构思、编码到部署调试的全流程。这不是设备堆砌，而是一次面向 AI 原生工作方式的硬件基座重构。

* * *

### [我用 AI 做了一条 TK 带货视频，成本 3 块钱，卖了 5 万美金](https://mp.weixin.qq.com/s?__biz=MzI5Mzk5MzA5Mg==&mid=2247487152&idx=1&sn=454fa6b944c0adaea7a44e93b0bcd28f&chksm=ed9dd31dafb200f41ee30971610f94945fdf258269b835536800a404f485d55c0875b6d7f045&mpshare=1&scene=1&srcid=0402iwMpI3D56Izo3BOcMpsb&sharer_shareinfo=032a28a5ff3450cad5c6ec075dbc405f&sharer_shareinfo_first=032a28a5ff3450cad5c6ec075dbc405f)

##### via 饼干哥哥

[

![](https://substackcdn.com/image/fetch/$s_!jK-b!,w_1456,c_limit,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0edbd009-c4c3-49c5-80a4-1f0c3d40fad7_687x356.heic)

](https://substackcdn.com/image/fetch/$s_!jK-b!,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0edbd009-c4c3-49c5-80a4-1f0c3d40fad7_687x356.heic)

作者的团队大半年烧了二十几万，跑出七位数 GMV，踩坑换来的核心洞察就一句话：**在 TikTok 上，像素级的产品一致性是个陷阱，用户下单的关键是 20 秒内的情绪冲击、身份投射和价格锚定，产品像不像根本不重要。**

他们用真金白银测试出的模型选型公式：品牌片用 Veo，种草用 Sora，投流用 Grok，故事用 Seedance，长片用 Kling。选错模型成本能差 30 倍。最贵的 Veo 3 废片率高达 80%，这你敢信？

另一个反常识的结论：TikTok 底层逻辑是「货带人」而非「人带货」。团队花两个月打造 AI 人设号，粉丝涨三千，零出单。转做产品种草视频，第一周就爆单。还有一个常见死法是照搬国内直播模式——数据显示，AI 短视频的长尾效应远超直播，一条视频发两个月还在出单。

AI 在电商领域的应用已进入精细化运营阶段。烧钱试错换来的不是炫技，而是一套剔除幻想、直指转化的务实方法论。

* * *

##### ▪️OPINION 观点

### [当 AI 可以做一切，剩下的护城河只有这 5 种](https://www.huxiu.com/article/4847018.html?f=rss)

##### via 虎嗅

Michael Bloch 指出一个反直觉的洞察：当 AI 让构建软件变得轻而易举时，传统的技术壁垒正在快速失效。**真正的护城河已从「难做的事」转向「难得到的东西」**。

**五种 AI 无法压缩形成时间的核心资产：**

1.  **持续复利增长的专有「活数据」**

2.  **需要多年积累的网络效应**

3.  **受政治进程而非技术影响的监管许可**

4.  **部署于物理世界所需的大规模资本**

5.  **受物理规律限制的基础设施**

「时间」本身成为了元护城河。这些优势都需要数年甚至数十年的现实时间沉淀，AI 无法并行加速。

* * *

### [如何在 AI 时代，找回你被埋没的创造力](https://mp.weixin.qq.com/s?__biz=MzIyMzA5NjEyMA==&mid=2647681166&idx=1&sn=aa7bbb97a0efb2a95828bd0d73ce0fa2&chksm=f18e7985e42c0534ef102c025f2d49eb20e8470a665ab68e29a6ec02628d9f7e5c0b4a1ce3a6&mpshare=1&scene=1&srcid=0331WDxL9dEh9XqlZVp5XhbA&sharer_shareinfo=40f707e695e632347d8495451c8a660a&sharer_shareinfo_first=40f707e695e632347d8495451c8a660a)

##### via 数字生命卡兹克

从 OpenClaw 到各种 AI 创作工具，人们兴奋地安装，然后对着闪烁的光标陷入空白。不是工具没用，而是我们被规训太久，忘了自己本来就有创造欲望。

AI 工具不是答案本身，而是放大器。它能把那个被掩埋的、属于每个人的创造天性重新点燃并赋能，前提是你先找回那个对世界「不满意」的、最原始的自己。

为此作者在文中给出了几个具体原则和建议，有一些还是能击中我，引导我反思的。

* * *

### 随便看看：

-   **[《「卧底」Kimi 的 100 小时》](https://mp.weixin.qq.com/s?__biz=MjEwMzA5NTcyMQ==&mid=2653247814&idx=1&sn=b1dd98d6293e532b5f673ecd83dbd401&chksm=4f957af0c7c3ce1aedbd6891275e4f0d45689d3d64bf20ca529be148bedbf4fd9fb39d0e17a9&mpshare=1&scene=1&srcid=0402ctEGsFLrC6jN6uFSIwwa&sharer_shareinfo=c4e4420d968299fc37c3bafe84e85553&sharer_shareinfo_first=eaa42d44ab291b4ca4227fd885f10482)** 罕见地揭开了月之暗面这家估值超 1200 亿人民币、却极度神秘的 AI 公司的内部生态。300 多名平均年龄不到 30 岁的员工，每人扛着近 4 亿估值，80% 是内倾人格。Kimi 要上市了，类似的公关稿基本是正面论述，有些甚至褒奖得过于露骨了，看个热闹吧。

-   **[《华语乐坛里，到底还剩多少活人？》](https://mp.weixin.qq.com/s?__biz=MzA5NDc1NzQ4MA==&mid=2654649691&idx=1&sn=b52147235265516adfea8a08cf412c6c)** 重新审视了 AI 对音乐产业的冲击。最近周杰伦新专辑发了，我听了完全不是那味儿。但是通过一堆二创（尤其推荐 AI 升 key 类、周杰伦年轻音色类），慢慢觉得这张专辑有些歌还不错。这让我对音乐行业的现状更感兴趣了，于是推荐这篇。文章通过一位职业作曲人沐花音的真实境遇，揭示了 Suno 等模型突飞猛进后，行业坍塌的速度与血腥程度。

-   **[《追了一年 AI 工具，产出为零：一个连续创业者的反思》](https://www.huxiu.com/article/4846922.html?f=rss)** 精准地刺破了科技圈里最普遍的幻觉：人们误以为「先看到未来就等于先赢」，结果却陷入不断测试新工具、却毫无实际产出的怪圈。反思一下我身上也多少有这问题。

-   **[《凌晨三点，我在排队等一个 AI》](https://www.ifanr.com/1660385?utm_source=rss&utm_medium=rss&utm_campaign=)** 开篇很有意思：Seedance 2.0 爆火，导致下游公司员工需要凌晨三点错峰上班。作者用大量细节勾勒出一个拧巴的供需结构：一边是 200 万美元的优先访问权和千万级的入场券，将中小公司挤出牌桌；另一边是平台方转向基于 Token 消耗的精细计费，用夜间优惠等价格杠杆疏导流量。

-   **[《医生说没救了，但亿万富翁不信，用 AI 战胜了癌症并开源全部诊疗数据》](https://www.mittrchina.com/news/detail/16170)** 展示了一个顶尖创业者如何将商业逻辑移植到生死战场。GitLab 创始人西德·西布兰迪杰在 2023 年确诊罕见骨肉瘤，经历毁灭性治疗后于 2024 年复发，被医生宣告无计可施。他随即辞任 CEO，以「创始人模式（Founder Mode）」自救：亲力亲为组建私人医疗团队，建立高达 25 TB 的个人生物数据库，并像管理代码库一样开源全部诊疗数据。 最终取得了抗癌成功。非常振奋人心，比上周那个自制药物救自家狗狗的更令人暖心。

### 适合个人上手的教程/评测/资源：

-   **[《Claude + Obsidian Solving The Memory Issue! (Walkthrough)Claude + Obsidian：解决记忆问题！（完整指南）》](https://x.com/intheworldofai/status/2039255561280057794)**：作者提出了一个「三层复合记忆堆栈」的架构，其核心是严格区分「工作区」与「大脑区」的双轨文件结构，将 AI 生成的高频但可能杂乱的「工作」内容，与人类精选、高信噪比的「知识」永久记录分离开来，以此保护 Obsidian 知识图谱的纯净与可搜索性。

-   **[《OpenCLI：万物皆可 CLI》](https://mp.weixin.qq.com/s?__biz=MzA4NzgzMjA4MQ==&mid=2453481700&idx=1&sn=377e4c26de698584d065dff8e6a675bf&chksm=86eefd3b2f26583c6342135e00d47e99dae3cbbd7df8c16bbab6c73b99d27263fac7e09c1dad&mpshare=1&scene=1&srcid=04022CfJ6cfoC8U4zVGumm0g&sharer_shareinfo=70ed7d10a9e2cd1bbd106decc0c1f8d5&sharer_shareinfo_first=70ed7d10a9e2cd1bbd106decc0c1f8d5)**：介绍了用 CLI+浏览器插件，来更快进行浏览器操作的方式，非常适合 Claude Code 等命令行玩家。

-   **[《从飞书文档到发布公众号，只需要几秒！我做了一个 CLI 工具帮你丝滑发文》](https://sspai.com/post/108059)：**作者做了一个名为 feishu-wechat-cli 的命令行工具，将整个流程压缩为一条命令和几秒钟。

-   **[《即梦 CLI 体验指南 - Feishu Docs》](https://bytedance.larkoffice.com/wiki/FVTwwm0bGiishxkKOoScdHR2nsg)** ：即梦也出 CLI 了。

-   **[《E73. AI 的不焦虑用法:你不需要再多学一个工具，你需要搞清楚 AI 能帮你解决什么问题》](https://www.web3brand.io/p/e72-ai-anti-anxiety)**：最让我感兴趣的是 Ruby 那个在 GitHub 上获得 600 多个 Stars 的科技股财报分析 Skill，它不仅能进行多维度估值，更核心的是提供了「变异观点」和反偏见框架，旨在发现市场共识盲点。

[

![Katelyn's avatar](https://substackcdn.com/image/fetch/$s_!i9GT!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack.com%2Fimg%2Favatars%2Fpurple.png)

](https://substack.com/profile/442985395-katelyn)[

![ben's avatar](https://substackcdn.com/image/fetch/$s_!ZrMU!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8ebdf5e3-fa08-4a7b-a943-5e91811785a1_144x144.png)

](https://substack.com/profile/479376429-ben)[

![游白's avatar](https://substackcdn.com/image/fetch/$s_!aadA!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2e4de0f4-8be2-4cc2-91e2-0d0c41d51b89_144x144.png)

](https://substack.com/profile/367105818-6e38767d)[

![Ruby Wang's avatar](https://substackcdn.com/image/fetch/$s_!d44m!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F29336479-aa06-4e42-823c-d32a76ce8b72_1130x1130.png)

](https://substack.com/profile/42543259-ruby-wang)[

![Justin's avatar](https://substackcdn.com/image/fetch/$s_!AqNR!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff52f32c7-c392-4cc9-8def-bfb0b396522b_1614x2451.jpeg)

](https://substack.com/profile/23543850-justin)

6 Likes

[](https://substack.com/note/p-193033118/restacks?utm_source=substack&utm_content=facepile-restacks)
