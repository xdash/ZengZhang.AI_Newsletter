### 当 AI 能替人消费时，品牌不主动嵌入 Agent 工具箱，就会被 Agent 忽略。

##### ▪️卷首语

[![](https://substackcdn.com/image/fetch/$s_!U2La!,w_1456,c_limit,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd77bf7ca-bfbd-4aaa-b477-da2fe6f4338e_1034x670.heic)](https://substackcdn.com/image/fetch/$s_!U2La!,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd77bf7ca-bfbd-4aaa-b477-da2fe6f4338e_1034x670.heic)

我的新课程 **[《我如何用 AI 开发内容商品（经验和复盘）》](https://zerodaybook.mikecrm.com/LZtJIOB) **已于今天正式如期上线！

**总共 3 万多字逐字稿、68 页 PPT、两小时足额时长** ，满满都是我的实践经历/踩坑经验/工具资源分享。购买后自动发货，可通过国内外网盘或 YouTube 观赏和查收课件资源（附赠 PDF）。

请预购的朋友们检查您的邮箱，查收课程链接（如收件箱看不到，先查一下是否误判进了垃圾箱）。

没能赶上早鸟的朋友，以及只买「现货」的朋友，也有上车机会。**目前我的所有课程，都在 6.18 大促进行中（截止 6.20），全部原价 299 → 特惠价 99** 。希望能帮端午假期宅家精进的朋友，在节假日期间有个愉快的学习体验。

  * **《我如何用 AI 打造 100X 知识萃取系统》** ：<https://zerodaybook.mikecrm.com/LjEzDNf>

  * **《我如何实践打造私人 AI 贾维斯助手》：**<https://zerodaybook.mikecrm.com/kctVTes>

  * **《我如何用 AI 开发内容商品（经验和复盘）》：**

<https://zerodaybook.mikecrm.com/LZtJIOB>

Subscribed

OK，以下是本期正文，Enjoy:

* * *

##### ▪️CASE 案例

### **[全网订阅第一的 AI 股神，看多 167 家、看空 56 家，我全给标了](https://mp.weixin.qq.com/s?__biz=MzAxMDMxOTI2NA==&mid=2649109181&idx=1&sn=46dfe6c80bd7ebe603829cc220c39773)**

##### via 十字路口 Crossing

[![](https://substackcdn.com/image/fetch/$s_!h6jK!,w_1456,c_limit,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F24973914-ed4a-4344-967a-6dbb01e342a1_649x331.heic)](https://substackcdn.com/image/fetch/$s_!h6jK!,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F24973914-ed4a-4344-967a-6dbb01e342a1_649x331.heic)

最近 X 平台上有个付费订阅排名第一的 AI 分析师，叫**「白毛股神」Serenity** 。她有多猛呢，一天能发几十条，从台积电的 CoWoS 产能，到某家光模块小厂的良率，到 CPO 到底什么时候上量，密度高到离谱。

终于有个人实在受不了了，自己动手开发了个工具站叫「白毛速报」，专门把 Serenity 的碎片化观点整理成可查询的多空地图。功能包括：

  * 第一，把 786 家公司按提及次数摊开，首次量化出看多 167 家、看空 56 家的比例。

  * 第二，每家公司交由 DeepSeek 生成带日期的观点摘要，一次点击调阅全部原文。

  * 第三，打上「看多/看空/中性」立场标签，避免被单条推文带偏。

  * 第四，把 CPO、HBM 这些黑话做成可点击入口，用大白话解释。

  * 第五，按提及频率排序，分组展示多空标的——被念叨 729 次的云厂 Nebius 位居看多榜首位。

用 AI 炒股还是很有搞头呀，难怪我社群里最活跃的是「AI+投资」兴趣小组呢。

* * *

### **[我花 7 万 token 点了杯咖啡：瑞幸上线 AI 开放平台，野心何在？](https://mp.weixin.qq.com/s?__biz=MzA3NzUxMzQ5Mw==&mid=2648143744&idx=1&sn=42518c8849736730569013de0b37e50f)**

##### via AI 新榜

[![](https://substackcdn.com/image/fetch/$s_!s4jn!,w_1456,c_limit,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F606fcf37-5ba1-468c-9e47-969ae404eee1_641x360.heic)](https://substackcdn.com/image/fetch/$s_!s4jn!,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F606fcf37-5ba1-468c-9e47-969ae404eee1_641x360.heic)

来看看擅长搞营销的瑞幸，最近折腾出个啥——**竟然推出 CLI，允许 Agent 点咖啡了** 。

然而，作者实测了一下用 CLI 点单，发现整个流程并不顺畅——安装、登录、绑定大模型 API Key、查询门店，每一步都有坑。门店名称不精确、定位有偏差，折腾了好几轮才终于下单。价格呢？优惠券不同，最终价格也会浮动。

7.4 万 token，折合不到 1 块钱——如果你用便宜模型的话。用贵的模型，成本直接跳到 6 块钱。第一次体验的 token 消耗，远高于后续。

瑞幸其实不是第一个吃螃蟹的。**麦当劳早就上线了 MCP 服务，场景还更多。** 瑞幸这步棋，是把内部 AI 能力通过标准协议对外开放，抢占「Agent 代劳消费」的入口。

这倒是挺有意思的一个尝试，除了凑近 AI 概念可以在资本市场好好讲故事之外，我倒真的是希望更多现实世界的实体商家，能够开放出它们的业务或能力，让我自家 AI 接进去，延伸使用场景。

* * *

### **[爆火的低成本创业赛道「AI 漫剧」，到底谁赚到钱了？](https://mp.weixin.qq.com/s?__biz=MTc5MTU3NTYyMQ==&mid=2651585931&idx=1&sn=5c79c41fac6ded01eee44deefbd0460b)**

##### via 三联生活周刊

AI 漫剧感觉才火了没几个月，就频繁被曝出正在经历一场残酷的洗牌。

三联生活周刊的这篇调查文章，披露了两组数据：3 月还有近百人团队的南昌公司，现在收缩到 5 人；而另一边，头部公司拿着千万级预存算力、50-100 人的投流团队，还在持续扩大产能。针对小团队的报价，从每分钟 800-3000 元，直接给干暴到了 50 元。

主要原因还是平台规则变化：**分成系数下调、审核周期拉长，那些靠平台分账「打工」的人，突然发现工资发不出来了。** 但有 IP、付费平台和投流策略的头部玩家，照样能多端口分发、精准出价，把收益装进口袋。

再看看出海，也是听起来很美，但门槛比你想象的高。版权授权、声音归属、音乐使用——每一个都是坑。**有人已经开始提供这类合规服务了，而且这门生意，可能比做内容本身更赚钱。**

* * *

##### ▪️OPINION 观点

### **[AI for Science 的拐点到了吗？](https://mp.weixin.qq.com/s?__biz=MzIzMDAzMTgzOA==&mid=2650861925&idx=1&sn=ee63da699f8bd2cb8c19ba96e4948670)**

##### via 峰瑞资本

「AI for Science」正在从小众赛道，变成全球资本和药企集中下注的方向。

峰瑞资本在 AI 制药领域已经有多家被投企业成功上市。他们主办的一场沙龙里，科学家 CEO 们聊了几个核心话题：**AI 极大提升了研发效率，在拓扑蛋白质、天然产物、AI 虚拟细胞领域都有突破性进展。** 投资人马睿列了五个拐点信号，说对未来五年 AI4S 非常乐观。

但挑战也很实在。创业公司最大的坑是身份转变——从技术导向转市场导向，从「我能做什么」到「市场要什么」。**下一个技术突破的关键，在于加速数字世界与物理世界的对齐。**

话说上海最近推了个大动作，要促进科研范式演进，目标是培育出下一个诺奖级成果。这事儿能不能成另说，但信号是明确的。

* * *

### **[92 年极客掌舵钉钉：陈宇森的产品审美与 AI 哲学](https://mp.weixin.qq.com/s?__biz=MjM5NjAxNDE2MA==&mid=2651117032&idx=2&sn=2c324a77b32180f383112cc5947324f8)**

##### via 未知来源

钉钉换 CEO 了。新掌门叫陈宇森，92 年生，前长亭科技创始人，纯技术极客。

这篇文章是对他的专访，聊到了对产品和 AI 哲学的观点。

他有个挺有意思的判断：**衡量 AI 产品好坏，不看低付费用户规模，而看大额付费用户的续费率。** 他的产品 MuleRun 上线两个月，月付费超 200 美金的用户几乎零流失。这被他视为达到 PMF 的早期信号。

关于 AI Native 转型，他的观点很直接：**组织必须「放手」。人参与流程，恰恰是给 AI 降速的原因。传统研发团队一周的活，甩手给 AI 干只要两三天，效率差十几倍。**

市场竞争方面，他认为当前 Agent 市场极其广阔，**真正的对手不是同类产品，而是客户愿不愿意采用先进工具。** 一旦客户体验了好用的 Agent，就会快速下单；拒绝使用的企业，将被更高效的 AI Native 竞争者碾压。

他的预言：当 AI 干活速度远超人类提出需求的速度时，生产力的瓶颈将变成人本身。

* * *

### 随便看看：

  * **[《我做了个紫微人生报告，一眼看出你什么时候走大运!「AI 赛博命理」》](https://www.bilibili.com/video/BV1e4zMB5E7m)** ：南派三合星情论命法，被一个团队做成了 AI 产品。输入出生信息，输出终生盘总结、十二宫位解读、财富格局等八个核心模块，外加十年大限趋势。

  * **[《离职后 30 天入职，一个中年打工人的靠谱「找工作指南」》](https://mp.weixin.qq.com/s?__biz=MTc5MTU3NTYyMQ==&mid=2651586282&idx=2&sn=c61e4d9e9fec799a0333c5035c930983)** ：崔若冲 30 天面试了 19 家公司，最终在 AI 工具的辅助下，拿到 4 个 offer 入职一家 AI 公司。

  * **[《让 AI 推荐它们觉得好听的歌！品味能否吊打真人？》](https://www.bilibili.com/video/BV18sEi6qEoX)** ：作者做了 10 年人工音乐推荐，现在让豆包、DeepSeek、T-ME、Z-Lot 和 ChatGPT 五个 AI 来 PK。

### 适合个人上手的教程/评测/资源：

  * **[《我的一人公司品牌部是怎么运转的？Lovart 制作爆款封面图教学！》](https://mp.weixin.qq.com/s?__biz=Mzg2OTA1OTAxNA==&mid=2247490855&idx=1&sn=4d8b4afcdf5328de2b0c074e642ed948)** ：内容创作者应尽早为自己攒一套可调用的人像资产，让观众一眼认出你，而不是淹没在精致的同质化封面里。

  * **[《我花 300 块，让 Claude Fable 5 开发桌面 APP，值么？》](https://juejin.cn/post/7650134533661032475)** ：程序员鱼利用 Claude Fable 5 模型，在 Cursor 中自主开发了一套包含桌面端、服务端和 Web 管理后台的完整系统。 约 50 分钟开发加 20 分钟修复，费用 300 元。

  * **[《我薅了美图 7 天会员，结果发现它已经进化成我不知道的样子了》](https://mp.weixin.qq.com/s?__biz=MzkxNTUwODgzNA==&mid=2247541131&idx=1&sn=1982db178e3e0826060ac5c63cea80aa)** ：介绍了美图开发出来的的 AI 功能。

  * **[《Codex 操控电脑的三种方案》](https://mp.weixin.qq.com/s?__biz=MzE5ODY5MDU4Mw==&mid=2247485986&idx=1&sn=c7c017796bb280c31ef193806bc56358)** ：OpenAI 内部负责 Codex 桌面体验的 Jason 拆解了三种方案的适用场景。

  * **[《AI 没法直出 UI？GPT+Figma 这样搭才管用！》](https://mp.weixin.qq.com/s?__biz=MjM5OTEwNjI2MA==&mid=2651928131&idx=3&sn=24274cf8d45270bf10d515462b60130b)** ：不要指望 AI 直接生成可交付的 Figma 设计稿。 更稳妥的方式是先用 image2 探索视觉方向，再回到 Figma 中整理结构，最后由设计师落地。

  * **[《Codex 不得不装的 12 个插件，都在这了 》](https://juejin.cn/post/7649738148373725225)** ：Codex 的真正价值不在于模型本身，而在于插件生态。

  * **[《为了让你搞懂 Loop Engineering，我搭了个让 Agent 持续帮你找工作的最佳实践》](https://mp.weixin.qq.com/s?__biz=MjM5OTEwNjI2MA==&mid=2651928067&idx=2&sn=a6b904899a5f90459818875745777919)** ：讲了最近冒出来的 Loop Engineering，这是围绕长期任务设计的一套 Agent 之外的循环系统，让 Agent 能够稳定地被触发、干活、交付、蛰伏。

  * **[《靠 11 个 SEO 大神 + Grok 任务，每天 5 分钟追完一手 SEO 情报》](https://mp.weixin.qq.com/s/cZGmqWp0pXse26U209NMww)** ：做 SEO 最怕信息差。 作者将这件事自动化：用 Grok 预设任务，每天自动搜索总结 11 位 SEO 大神的推文，通过邮件发送。
