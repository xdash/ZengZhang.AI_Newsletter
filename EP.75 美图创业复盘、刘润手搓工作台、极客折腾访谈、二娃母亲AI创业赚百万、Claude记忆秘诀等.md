##### ▪️PREFACE 卷首语

1/ 下午在即刻 [发了条动态](https://web.okjike.com/u/160F8D03-E580-4799-8D02-B86B1A6FBF64/post/6af6c31166b4f61307719d9e)，大意是说我在给自家内网的贾维斯找了个师傅 ---- 个人算力蒸馏不了最前沿的大模型，那就去蒸馏别的 Personal Agent 产品：复杂任务先让 Grokbot 跑通一遍，再让它教给内网的贾维斯，省得我手动调教。Grokbot 你就是奥创，是严父，是童虎，是我爹。

2/ 这期收了 29 条内容，读下来发现差不多三分之一在讲同一件事：怎么给 AI 派活，又怎么验收它干得对不对。这都是我近期关注的重点。因为我发现，折腾有意义的任务固然重要，从折腾的快乐中长出值钱的生意这个路径似乎更长期主义。特别喜欢鸭哥的播客，听了两遍，又学到了折腾的新玩法。

3/ **[《AI 写作工程学：如何用智能体快速创作出版级的内容》](https://zerodaybook.mikecrm.com/rEgDmgL)**11/11 正式上线了，双十一那晚也直播讲了一场。

[![](https://substackcdn.com/image/fetch/$s_!pfik!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1edb9f42-d67e-48d1-bc74-c80170ed94e4_2362x1408.png)](https://substackcdn.com/image/fetch/$s_!pfik!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1edb9f42-d67e-48d1-bc74-c80170ed94e4_2362x1408.png)

这门课讲的是怎么把想法或经验，快速高品质地用 AI 写出来。背后是借鉴计算机里的软件研发的相关思路。我连纸质书出版都跑通了，做其他比如自媒体、写论文简直是降维打击。2小时，八个主要章节模块，有 prompt、有参考截图、有理念有技术。

不管你是想出书建立专家身份，把过往作品打包成一本物理纪念，还是想批量写书赚快钱、写策划写论文，应该都能有所收获。

早鸟价已经结束，恢复正价 299 元（但买过我其他产品的老朋友照例可以加我微信领 100 元红包的）：<https://zerodaybook.mikecrm.com/rEgDmgL>

OK，以下是本周正刊内容，Enjoy----

* * *

##### ▪️OPINION 观点

### 🧠 **[Anthropic公布 Claude 内部记忆架构：Fable 5 如何用 10 个记忆文件秒了 Sonnet 的 413 个](https://mp.weixin.qq.com/s?__biz=MzIyNjM2MzQyNg==&mid=2247729895&idx=1&sn=6e486687100696a37703dcb9effd5115)**

##### **[原链 * 公众号 * 约 15 分钟读完](https://mp.weixin.qq.com/s?__biz=MzIyNjM2MzQyNg==&mid=2247729895&idx=1&sn=6e486687100696a37703dcb9effd5115)**

[![Image](https://substackcdn.com/image/fetch/$s_!0K69!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb67716ca-210b-443d-aa84-f2e9ff11a0d0_1080x493.webp)](https://substackcdn.com/image/fetch/$s_!0K69!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb67716ca-210b-443d-aa84-f2e9ff11a0d0_1080x493.webp)

Anthropic 在官方长文里第一次把 Claude 的内部记忆架构讲清楚，结论有点反常识：**长 期记忆要做精巧的减法，存得越多反而越拖垮它。**

他们先拿外挂记忆开刀。事无巨细地记，会拖垮模型；笔记本身记错了，还会引发级联崩溃。

宝可梦红版那个实验最能说明问题：Sonnet 3.7 记了 413 个文件，只拿到 1 枚徽章；Fable 5 只用了 10 个文件，拿到 4 枚。

所以真正的长期记忆只该装隐性规则，不装易变的事实。

架构是四层金字塔，自底向上：原始执行流水、记忆笔记、知识 Wiki、注入上下文。Wiki 这层最省，Stainless 的案例里**平 均每个问题少花约 2 万 Token**。

顶层还有个「离线梦境」，模仿人的睡眠----拿底层流水回头校对笔记、修错。月见山那个任务里，修正组穿过去了，没修的组没过。

到了 Claude Code 上，只加载前 200 行当目录索引，剩下的按需检索。

最后附上三条法则：保留原始底账；顶层做目录，底层做仓库；给强模型目标，而不是死板规则。

* * *

### 💰 **[ChatGPT能搞定 70% 的场景，美图的选择是先绕开](https://mp.weixin.qq.com/s?__biz=Mzg5Mjc3MjIyMA==&mid=2247588470&idx=1&sn=03698b92a7200086523b9c952a84e9d2&chksm=c15372fe4b418607d7210ebc583ad4d1ef54824fd28eaa8dfdf2824271ba999db90a69dba3c2&mpshare=1&scene=1&srcid=1112mKbKei66941l1RtLSQh7&sharer_shareinfo=adf099ebcc0ca7a3eefe8e69d4f8ef6c&sharer_shareinfo_first=adf099ebcc0ca7a3eefe8e69d4f8ef6c)**

##### **[原链 * 公众号 * 约 15 分钟读完](https://mp.weixin.qq.com/s?__biz=Mzg5Mjc3MjIyMA==&mid=2247588470&idx=1&sn=03698b92a7200086523b9c952a84e9d2&chksm=c15372fe4b418607d7210ebc583ad4d1ef54824fd28eaa8dfdf2824271ba999db90a69dba3c2)**

[![Image](https://substackcdn.com/image/fetch/$s_!xcOV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F85c801d5-1797-47d1-9228-a79a0a3db233_1080x962.webp)](https://substackcdn.com/image/fetch/$s_!xcOV!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F85c801d5-1797-47d1-9228-a79a0a3db233_1080x962.webp)

被加密坑惨了的美图，算是接着 AI 又活过来了，还很滋润。美图 CEO 吴欣鸿在一场播客里，把 AI 应用创业的坑摊开讲了一遍。

这篇作者听完，结合自己的困惑提炼出六条。

  * 第一条是别跟模型硬碰。**ChatGPT 能搞定 70% 的场景就先绕开，去啃行业里那些模型还接不住的脏活**，靠 Know-how 建墙。美图自己就把提词器单独拎出来做成「开拍」，又在保险、房产经纪这类行业里往深里做。

  * 第二条是敢撤。美图砸钱做过视频大模型，发现资源悬殊太大，干脆收缩回图像模型。承认打不过，比押对方向更难。

  * 第三条：核心场景自己练模型。美图的模型有 96.5% 自研，同等效果下成本只有外部模型的二十分之一，人像修图这种活儿还能针对性磨到八九十分。

  * 第四条讲组织。美图照着 Supercell 的样子，拆出十几个十人以内的工作室，用 AI Coding 三天做出 Demo，分阶段验证，不行就砍。

  * 第五条讲收钱。基础订阅照留，另外把 AI 能力封装成「直接交付结果」的服务----用户愿意为省下几天时间多付钱。

  * 第六条讲出海，也最容易被忽略。生产力应用从第一天就该面向全球，市场按文化圈切，不按地理位置切。

别一味追用户增长，先看肯不肯付钱、留不留得住；本地团队做运营，研发留在中国；创始人得自己飞出去调研。

感兴趣的建议去听听原播客。

（这套经验带着明显的幸存者视角，美图的家底也不是谁都拿得出来；但「绕开模型最强的地方，去做它做不好的事」这一条，对单人团队一样成立。）

* * *

### 💡 **[用 AI 十倍提效的人，为什么反而更难升职](https://www.ximalaya.com/sound/1031626765)**

##### **[原链 * ximalaya.com * 约 93 分钟读完](https://www.ximalaya.com/sound/1031626765)**

超线性学院联合创始人鸭哥在播客里聊了几个折腾的例子，我挺喜欢。

比如他调教 AI 帮忙写稿，不是反复调教提示词，而是在发现这条路很难之后，直接做更高维度的事情----先让 AI 把原文改写成 AI 味，再拿 AI 文当输入、原文当输出做微调，**一 张 RTX 5090 上一两个小时就能跑完，盲测下几乎分不出谁写的**。酷炫。

当然他作为一个在名司做过的学霸，也聊了关于职场的思考。比如借助 AI，效率是上去了，被派来的活也跟着变多、变零散，最后变成一头「模范老黄牛」。不想当老黄牛，就得往上挪一步：把验收标准和关键决策攥在自己手里，让别人按你定的标准交活。

此外，对技术名词他保持警惕：LangChain 是模型还不行时的补丁，jev 也是过度营销，真正该练的是出题、写 Eval、当 Manager 带 AI 干活。

播客里还夹了个睡眠实验：主播用几百个变量跑回归，发现预测睡眠最强的变量是「当天最后一次用 AI 的时间」。照 AI 自己的建议少用之后，**平 均睡眠多了 1.4 小时**。

* * *

##### ▪️CASE 案例

### 🗂️ **[二娃母亲调动九个 Agent 做出百万美金生意](https://mp.weixin.qq.com/s/NcXNkWqeNY5esVmvbCT06g)**

##### **[原链 * 公众号 * 约 10 分钟读完](https://mp.weixin.qq.com/s/NcXNkWqeNY5esVmvbCT06g)**

ChatPRD 创始人 Claire Vo 在 Lenny 播客里讲了自己的公司：九个专门的 AI 智能体，2026 年初年收入约 140 万美元，自筹资金。

九个业务岗分得很细：日程管理（Polly）、销售跟进（Sam）、播客数据分析（Howie）、家庭事务（Finn），再加增长研究、计费运营、客服分诊、内容和法务审阅，外加两位工程副驾。全部跑在几台 Mac mini 和旧笔记本上。

她强调的重点很简单：**每 个 AI 岗上岗前，先写一条 30 秒内能判断对错的验收标准**。

她也划了三条绝不交给 AI 的线：对外承诺（合同、报价、交付时间）、资金动作（付款、退款、改价）、判断一个需求是不是假需求。理由是责任没法代理、错误不可逆，而 AI 擅长回答被问出来的问题，不擅长判断这个问题值不值得问。

所以她把自己的工作概括成从「做事」变成「审事」，而这需要一整套把人组织起来的手艺----那正是二十年经验最该变现的部分。

她还建议攒两笔资产：受众从五年前开始攒，专业从二十年前开始攒。AI 让这两笔资产的变现效率翻倍，但它不生产资产本身。

文末还有一组 Stripe 2026 年二季度的数据：通过 Atlas 注册的股份公司里，63% 是单一创始人，创历史新高----**但 注册主体不等于实际经营主体**。

她最后给了张九岗四列的表，建议先挑一个岗、把验收标准写死跑两周，跑通再加第二个。

  * 延伸阅读：[Spawn 创始人写了篇长文](https://x.com/jsnnsa/status/2115623382721126826?rw_tt_thread=True)，讲一家做多人游戏创作引擎的十人公司怎么把 AI 用到骨子里：人类团队很小，旁边站着一支永久性的 AI 代理舰队。

* * *

### 🛠️ **[刘润手搓 AI 工作台为短视频团队减负](https://mp.weixin.qq.com/s?__biz=MjM5NjM5MjQ4MQ==&mid=2651789819&idx=1&sn=038314d31cdf6ec973542c1a73d7b03d&chksm=bca42133abc15dfbbfca57f2b1e12ba6b83c55c6e58aed6d557000e6648eabd7a47f5c1a8ed2)**

##### **[原链 * 公众号 * 约 16 分钟读完](https://mp.weixin.qq.com/s?__biz=MjM5NjM5MjQ4MQ==&mid=2651789819&idx=1&sn=038314d31cdf6ec973542c1a73d7b03d&chksm=bca42133abc15dfbbfca57f2b1e12ba6b83c55c6e58aed6d557000e6648eabd7a47f5c1a8ed2)**

[![Image](https://substackcdn.com/image/fetch/$s_!LgRB!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe9946041-e851-435a-80ec-afea7b804409_1080x509.webp)](https://substackcdn.com/image/fetch/$s_!LgRB!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe9946041-e851-435a-80ec-afea7b804409_1080x509.webp)

刘润写了自己给小媒体公司手搓的自动剪辑工作台，起点很朴素：同事加班太多。

他以脚本为起点，让 AI 按流程把配音、分镜、素材匹配、字幕调整一路跑下来，削掉剪辑同学的重复劳动。

第一条，他觉得得先找出流程里那个决定后面所有环节的节点，然后围绕它组织功能。

第二条是让修改只影响该改的地方。字幕之所以不必留到最后做，就是因为工作台把字幕和配音、分镜放在同一页，改一处不会牵动别处。

第三条是判断哪部分在耗脑力，就把它交给工具。自动规划分镜、给素材打标签检索这类活，最适合让 AI 先跑一版。

这套工具他自己也说不上专业，但内部用着顺手。

结尾那句挺实在：你完全可以按自己的流程，手搓一个只服务自己的生产工具。

* * *

### 🚀 **[Grok Bot当指挥官，二十个 AI 员工跑五个跨境团队](https://mp.weixin.qq.com/s?__biz=MjM5NDI4MTY3NA==&mid=2257501548&idx=1&sn=b047ccbfc9bfbbf21208d2fae73315cc)**

##### **[原链 * 公众号 * 约 18 分钟读完](https://mp.weixin.qq.com/s?__biz=MjM5NDI4MTY3NA==&mid=2257501548&idx=1&sn=b047ccbfc9bfbbf21208d2fae73315cc)**

[![Grok Bot 跨设备 AI 指挥官架构](https://substackcdn.com/image/fetch/$s_!6QtI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb6538cb6-e887-451d-b533-1239bf0a2b15_1080x608.webp)](https://substackcdn.com/image/fetch/$s_!6QtI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb6538cb6-e887-451d-b533-1239bf0a2b15_1080x608.webp)

饼干哥哥用 Grok Bot 这个 Agent 拉了五个跨境团队、二十个 AI 员工。这个数字本身没啥可抄的，真正可复制的是他给 Grok Bot 找的位置：不当执行者，当指挥官。

Grok Bot 背后的模型已经从 Opus 5.5 降到 Grok 4.6，直接写长文或复杂代码容易翻车。但云电脑加多终端协同让它能远程操作本地电脑，于是架构变成：手机端当指挥官，本地机器干重活，Notion 当共享数据库，Cloudflare Worker 当免费网关。

五个团队各有分工。

  * TikTok 那组由增长总监带爆款猎手、脚本编导和投流盯盘手，巡检同行爆款、诊断广告异常。

  * SEO 与 GEO 那组用情报捕手去 Reddit 和 X 挖真实提问，远程唤醒 Claude 写深度英文长文，正文里埋结构化对比表。

  * VOC 那组采集亚马逊差评和 Reddit 吐槽，按使用场景、高频槽点、未被满足的爽点、原声黑话四个维度打标，反哺产品微创新和营销选题。

  * 飞书那组最省钱：用免费网关把 VPS 监控从每月 8640 次压到 40 至 60 次，还让全员在飞书里 @ 机器人调用小语种翻译。

  * 内部产品那组串起 Notion 需求池、GitHub 仓库和两台编码电脑，从 PRD 生成到 QA 自动验收跑成一条线。

另外是：别一上来把 Bot 拆太细；重要规则存进共用记忆或 Skill；装上 Wake on Done；切本机执行时关掉 Mac 的 App Nap。

**单 任务能跑多远看模型，多任务能跑多远看架构**。

* * *

### 随便看看：

  * **[《2026，AI 应用的钱都流向了哪里？》](https://mp.weixin.qq.com/s?__biz=MzkyNjU2ODM2NQ==&mid=2247635261&idx=2&sn=2b0ca6dd9705063c2140e39d1e1ad9d0)**：视频、图像、3D 拿走大额资金，医疗教育这类垂直行业融资更频但单笔小。别盯融资额，盯验证路径：PixVerse ARR 超 4000 万美元，演语科技 ARR 3 亿美元。

  * **[《短剧凶猛，三次洗牌｜封面故事》](https://mp.weixin.qq.com/s?__biz=MTI3NTQ1MTY0MQ==&mid=2650678262&idx=1&sn=bf7a15470b8093ae53ae53a38baf974f)**：三次洗牌改的都是钱从哪来：流量定价、平台当付款人、AI 时代的算力与版权账单。2026 年前九个月上线 49 万部微短剧，只有 1.3% 的 AI 剧跨过 5000 万播放的盈亏线。

  * **[《AI 面试逼疯打工人》](https://mp.weixin.qq.com/s?__biz=MzkzODUxNTM2OA==&mid=2247543127&idx=1&sn=9a27b234794ef8626170501f236a7c4a)**：机械工程师被追问 C++，求职者被要求上传全身照，面完只收到一句「未通过」。有人投 600 份简历、面了 15 场 AI 面试仍是 0 offer。企业省下筛选成本，压力全转给求职者。

  * **[《无班可上，年轻人正在被逼着直接当老板｜不懂经网站》](https://mp.weixin.qq.com/s?__biz=MzU4NDQwMTc3MQ==&mid=2247493773&idx=1&sn=251bd63fa3ae48b4845b98d07b256166)**：美国 20 岁出头的名校毕业生，融到 200 万美元比找份 5 万美元的工作更容易：文件准备岗一年少 17%，应届生空缺跌 33%。打工不再提供安全感，创业就成了防御性下注。

  * **[《日薪 180，在「流水线」上给机器人当老师》](https://mp.weixin.qq.com/s?__biz=MzkyNDEzOTAzNg==&mid=2247488627&idx=1&sn=c003ac125deef43999f83e03a62b6a3b)**：机器人要达到类人能力约需一亿小时数据，全球有效数据只有几十万小时，缺口由近百万兼职采集员填。作者亲身体验的另一面是：多层外包、无劳动保障、偷工减料照样达标。

  * **[《AI 产业爆发前夜，深圳迭代调研实录｜《财经》特别报道》](https://mp.weixin.qq.com/s?__biz=MjM5NDU5NTM4MQ==&mid=2653741546&idx=1&sn=eecc7e261930b39551d1eeb6764c7978)**：深圳 AI 核心产业规模 2200 亿元，对着近 4 万亿 GDP 还只是先导。华强北从档口转成 AI 硬件选品中心，模力营用三级算力缩短打样，但机器人落地仍少。作者看到的是：深圳在试着把产业优势写成亚太规则。

  * **[《网友用 AI 搓出来的「App」，可以直接在小红书玩起来了？》](https://mp.weixin.qq.com/s?__biz=MzA5NDc1NzQ4MA==&mid=2654707082&idx=1&sn=48ae1946f4a700b29abbaeed7d96090e)**：70% 的小工具创作者不是专业开发者，开蚌直播间人气超 231 万，一位从阿里离职的创作者一周涨粉近 1 万。小红书正在变成 AI 时代的 App Store，变现内测 11 月开启。

### 适合个人上手的教程/评测/资源：

  * **[《Antigravity 上手全流程指南》](https://mp.weixin.qq.com/s?__biz=Mzk0NzQzOTczOA==&mid=2247528434&idx=1&sn=cdced5eca5093ff8d8a640fedc2e50a9)**：Google 的 Antigravity，权限四档里 Turbo 自主性最高、隔离最弱，不熟先别开；远程 Agent 跑在隔离云端，电脑休眠也能继续。

  * **[《agent-desktop 实测：不截图不抢鼠标》](https://mp.weixin.qq.com/s?__biz=Mzk0ODM5NTEyNA==&mid=2247507536&idx=1&sn=27cf065aab52cec826b8c0b3cc28906e)**：Vercel Labs 的 agent-desktop 接 MCP 后靠无障碍树给按钮编号，不截图不抢鼠标。15 笔账单加总实测 55 次按键 0 失误，代价是单步约 1.5 秒。

  * **[《dbskill 三件套去除 AI 味》](https://mp.weixin.qq.com/s?__biz=MzA5MDg2MzQ5NQ==&mid=2247490949&idx=1&sn=765a106c58a4bee72973291f2480c73a&chksm=91cb8837982f0fddbff166392f2b06833930317024330aee84ac02ab34cc20135d4bbd772cd4)**：dontbesilent 把去 AI 味拆成三个 Skill：ai-check 扫 22 种 AI 写作特征，speak-human 改对话语气，plain-writing 按简化英语规范改产品说明。

  * **[《国产模型去 AI 味四类实战》](https://mp.weixin.qq.com/s?__biz=Mzg3MTk3NzYzNw==&mid=2247512876&idx=1&sn=d16f3ee7b6de41c40c63c38a81b5a73c)**：卡尔实测商汤 SenseNova-6.8-Flash，把代码动画、UI、3D、SVG 海报四类产物的 AI 味都压下去了。最通用的两条：先定色号与字号层级，删掉没必要的英文小字说明。

  * **[《三工具流水线造动态吉祥物》](https://mp.weixin.qq.com/s?__biz=MjM5NDI4MTY3NA==&mid=2257501560&idx=1&sn=5cd92b1ec4618ef24e1201c9878badf7&chksm=a4598caf76dda3d4ff305e322ea7c4015b18f3c572296306b576ec1e7904291c8e8b9ef9ebf2)**：饼干哥哥用三个工具拼出流水线，拿 16 张静态表情半小时跑完全套：Logo 定稿、全身母版、12 款微信循环 GIF，还有一只会跟着鼠标转眼睛的网页角色。

  * **[《浏览器手搓实时语音大肥鱼》](https://mp.weixin.qq.com/s?__biz=MzIyNjM2MzQyNg==&mid=2247729612&idx=1&sn=d803aaa8822b68be423132ecbf39ebc4)**：基于声网实时互动工具包，四步在浏览器搭出一只能实时对话、嘴型随声音张合、支持插话打断的「大肥鱼」。实测端到端 28ms，静音判停窗口从 480ms 放宽到 900ms 才好使。

  * **[《错题本变多用户学习系统》](https://mp.weixin.qq.com/s/qGK3zVc6Eb-qLqAy6jw7fg)**：程序员爸爸把只服务自家孩子的错题本改成多用户系统：登录隔离数据，知识图谱覆盖人教版全学科 3297 个知识点、4868 条先修关系，错题按 1-3-7-14 节奏复习。

  * **[《flomo 更新：视频笔记与 AI 连接》](https://mp.weixin.qq.com/s?__biz=MzI0MDA3MjQ2Mg==&mid=2247490876&idx=1&sn=c425953f61821aed6481df541fa35fca&chksm=e8b0ac6efaaab6a15e74dccd3148a202ca241ed8835c67befda636758a712f7024367051d48a&scene=0&xtrack=1)**：新增视频上传，文字和图片接不住的真实场景也能留住。同时在 WorkBuddy 和豆包上架连接器，AI 能检索笔记、也能把新想法写回来，连接随时可断。

  * **[《22 款生产力工具分级排名》](https://www.youtube.com/watch?v=uRCskQbL1KY)**：Ali Abdaal 把在用的 22 款工具从 F 级排到 S 级，标准是自己的 GPS 方法：有目标、有计划、有系统。同一个 Slack，对团队管理者是 S 级，对他这个 maker 是 F 级。

  * **[《Token 羊毛监控站免费开放》](https://mp.weixin.qq.com/s?__biz=MzIyMzA5NjEyMA==&mid=2647688203&idx=1&sn=830360dc6103e7fa745c116a5d84e54a&chksm=f1720a7d5f107c89932a4cbd26f1465efb77ade5731461dfdc27493efa3940b9a480f5df7c26)**：卡兹克把 AIHOT 的监控引擎反过来用：原本用来剔广告的规则，现在专门找免费 Token 福利。按日、周、月列出可领额度，还给每份羊毛配了张卡，领了就点亮、升级。

  * **[《用 AI 定时巡检证监会新规》](https://mp.weixin.qq.com/s?__biz=Mzk0MzEwODgzMQ==&mid=2247527284&idx=1&sn=8e56321af323cadbf389bd3e1581751f)**：大刘把查法规做成定时任务，一份提示词给证监会官网七条硬约束：只用一级信源、条款号必须对得上、找不到旧版就如实留空、拿不准写「需查完整规则」。每周跑一次，出对照报告。

  * **[《AI 出海 40 个工具六站打通》](https://mp.weixin.qq.com/s?__biz=MzAxMjUyNDQ5OA==&mid=2653588414&idx=1&sn=b1ce17db9a6eddd78c74e11fe93af42a)**：橙哥把自己从程序员做到收美刀的路径拆成六站：调研选品、建站开发、设计与内容、AI 引擎、自动化增长、收款换汇，40 个工具按顺序排进去。工具是枪，扣扳机的是你自己。

  * **[《零代码跑通量化全流程》](https://mp.weixin.qq.com/s?__biz=MzAxMjUyNDQ5OA==&mid=2653588428&idx=1&sn=52c9045feffd3f609d051db327eb1cb0)**：橙哥在 Minara 上用对话走完行情研究、价格告警、策略、回测、自动执行。功能本身不算稀奇，有用的是它给出的读法：聪明钱在扫货 meme，但单笔只有几千美金，真正的大户在撤。
