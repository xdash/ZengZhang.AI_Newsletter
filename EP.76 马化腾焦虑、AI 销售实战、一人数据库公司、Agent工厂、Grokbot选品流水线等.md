##### ▪️PREFACE 卷首语

1/ 推荐个新发现的 B站 账号 [@GrokBot打工日记](https://space.bilibili.com/3747573145800217) 。挺有意思，幕后主使全程让 Grokbot 自己去开账号、跟评论区互动、收集想法、开发出来、制作视频演示、做每日数据复盘，如此循环往复。这个号自己就养起来了。从开号到今天，不到一个月，已经 1.7 万粉了，最近每天涨粉大几百。

2/ 本人出售两个手头 AI 域名： Ray-Ban.AI（雷朋）、 XiaoLv.ai（效率）。前者可用于智能眼镜相关，后者可用于效率类产品或导航。欢迎接洽。自己用不上，价格很好商量。联系： [i@TonyStark.AI](mailto:i@TonyStark.AI) （这真的是我的邮箱，新启用）。

3/ 这期收了 23 条，读下来发现有条共同的暗线：大家都在给 Agent 装「中控台」。

上周卡兹克给 Autoloop 加了可视化面板，每一单的状态、耗时、费用都看得见，才敢放手，这周有人延续它的做法跑通了多 Agent 状态管理；Steve Yegge 用 22 个 Claude Max 账号养 Agent 工厂，四个月完成了号称 100 年的开发量；冯若航对一人 AI Naitive 公司的经验也比较翔实。

最近在给一些知名企业做 AI Native 和内部 AI FDE 的咨询和培训，比较关注这块。恰好能将我过去两年搭建 Agent 的经验和用在公司提效、运营增长上的经验用上。我现在不讲流量、不做运营/营销口的分享，主要兴趣还是集中在 AI Native ---- 形象地说，怎么让一个人带着几十个 Agent 管好组织内部的一摊经营活动。这是我的兴趣所在。有需要的朋友也可以联系我洽询哈（还是联系： [i@TonyStark.AI](mailto:i@TonyStark.AI)）。

[Subscribe now](https://www.zengzhang.ai/subscribe?)

OK，以下是本周正刊内容，Enjoy----

* * *

##### ▪️OPINION 观点

### 🐧 **[马化腾在焦虑什么](https://mp.weixin.qq.com/s?__biz=MzkwNDQ5MjM1Mw==&mid=2247495988&idx=1&sn=b81dba5d14e99b5c59a2f8dbba4f6ffe)**

##### **[原链 * 公众号 * 约 16 分钟读完](https://mp.weixin.qq.com/s?__biz=MzkwNDQ5MjM1Mw==&mid=2247495988&idx=1&sn=b81dba5d14e99b5c59a2f8dbba4f6ffe)**

腾讯 11 月 18 日发了三季报。收入同比增长 8%，到 2073.36 亿元。但经营盈利降了 7%，**自 由现金流从 -138 亿元扩大到 -691 亿元**，钱主要砸进了算力采购。

往前一周，11 月 11 日腾讯 28 周年庆，马化腾把话挑明了：过去做的是轻资产，这是第一次做重资产。「很多核心业务觉得自己似乎有险可守」，但「远处浪潮已经吞没一个个山丘」。他的安排是「用一半人守传统业务，一半人打新战役」，原话是「现在已经是生死存亡的时候了」。

短期的仗确实打赢了，可账面上有几笔硬的。

模型上，下半年国内和 GPT、Claude 的差距重新拉大。前沿数学测评里，GPT-6.1-Sol 拿 97.5 分，混元 Hy4 只有 13 分----13 分这个数字，挺扎眼。参数规模上，Fable 和 Astra 约 10 万亿，国内过万亿的只有 Kimi、Qwen、DeepSeek 三家，腾讯 Hy4 是 7700 亿。

算力更紧：中国训练芯片总量不到美国的 1/10，三大厂里腾讯囤得最少。

业务侧，WorkBuddy 日活 1000 万、7 天年化收入超 5 亿美元，单看是不错的战果。但对照腾讯 7000 多亿元的年收入仍是零头，Token 成本还高企。

另外还有两层隐忧。微信里的「小微」日活 3000 万，却因为数据安全顾虑读不了聊天记录，只能先做「更好的微信搜索」。姚顺雨用不到一年把混元带回第一梯队，验证了年轻化路线，但他带的是 800 人，腾讯是 11 万人，换血难度不在一个量级。

结尾落在财报会上那句：「AI 肯定会带来重组，企业可以用更少的人。」

* * *

### ⚡ **[601.8小时转写、253 条会议记录：Dify 商业化负责人用 AI 重做销售的一年](https://mp.weixin.qq.com/s?__biz=Mzg2NDA3NTExMA==&mid=2247487795&idx=1&sn=dab6cc704e3ba04f79713f56a960297b&chksm=cff656dd21b9b6bf4e1763960fd00e228a8c76454f08979b7d5da8a78605ba2881d871357d50&mpshare=1&scene=1&srcid=11139jdoTLS623zgNbOvwOK4&sharer_shareinfo=4b62faa0baa771933380d381e6d19a73&sharer_shareinfo_first=4b62faa0baa771933380d381e6d19a73)**

##### **[原链 * 公众号 * 约 14 分钟读完](https://mp.weixin.qq.com/s?__biz=Mzg2NDA3NTExMA==&mid=2247487795&idx=1&sn=dab6cc704e3ba04f79713f56a960297b&chksm=cff656dd21b9b6bf4e1763960fd00e228a8c76454f08979b7d5da8a78605ba2881d871357d50)**

[![会议、邮件、协作文档和商机记录怎样汇到同一份客户档案](https://substackcdn.com/image/fetch/$s_!T5_y!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd11335f8-8d77-43b8-ab47-a3e5add7edb8_1080x608.webp)](https://substackcdn.com/image/fetch/$s_!T5_y!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd11335f8-8d77-43b8-ab47-a3e5add7edb8_1080x608.webp)

Dify 的商业化负责人在崔牛会 AI 实践者峰会上做了场分享，讲从用 AI 到卖 AI，销售这活儿到底变了多少。

过去一年她接触约 100 家企业，攒下 **253 条会议记录、672 条录音、601.8 小时转写**，再用 Codex 追溯记录、找回承诺、起草回信。

  * 她自己用 AI 做销售，养成了三个习惯。接到活先问「为什么这件事要我做」；AI 第一次做得不好，先回头检查是自己没说明白、还是它没看到会议记录；每次模型更新，最想试的是手里一直没解决的那个问题。

  * 见客户也有讲究。遇到已经在用社区版的客户，她先问对方用到哪一步、今天为什么想聊，而不是急着开演示会。谈伙伴合作，她要能回答三件事：一起做什么、回去能推动哪一步、最快能办成哪件小事。

  * 她对销售的定义很新鲜：销售是一台现实世界的采集器。每天约人、出门、听客户说话，有些信息帮判断单子能不能关，有些应该让产研同事直接听到原话。

* * *

### 🤖 **[22个 Claude Max 账号养一座 Agent 工厂：Steve Yegge 4 个月清掉 60 年积压](https://mp.weixin.qq.com/s?__biz=MzIwNjM2NjQyNg==&mid=2247498409&idx=1&sn=e1f2ed1f268c950c105aa6ac32c85a75)**

##### **[原链 * 公众号 * 约 15 分钟读完](https://mp.weixin.qq.com/s?__biz=MzIwNjM2NjQyNg==&mid=2247498409&idx=1&sn=e1f2ed1f268c950c105aa6ac32c85a75)**

[![Image](https://substackcdn.com/image/fetch/$s_!Oal4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0219cd6f-6354-45e8-9651-d77b89ff1882_1080x608.webp)](https://substackcdn.com/image/fetch/$s_!Oal4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0219cd6f-6354-45e8-9651-d77b89ff1882_1080x608.webp)

Steve Yegge 是亚马逊和谷歌的双料老兵，在技术圈写过多篇刷屏长文。他在 AIE CODE 2026 大会上的演讲，主题是给自己运行了 30 年的游戏 Wyvern 搭一座软件工厂。

配置很夸张：**22 个 Claude Max 账号**，每天上线 50 到 100 个功能，4 个月清掉了 60 年的积压工作量。

但他重点不在速度。他把难点拆成五个问题：工作流转、燃料管理、上下文管理、人事管理和模型福利----他反复强调，最难的不是代码，是人，工厂越大，需要的人越多。

给开发者的建议也很反常：别再盯着 SaaS 和工具，去做体验。

* * *

##### ▪️CASE 案例

### 🛠️ **[把 Autoloop 接进公司真实业务](https://mp.weixin.qq.com/s?__biz=MjM5ODQ3MDk0Mg==&mid=2448912486&idx=1&sn=1c624db5497bc833722f1808d2bbd546&chksm=b3f10d8880c08bb0ecb1b353de4eb8e863b7f59f5789c7ab1e01168445a86cbcefb253d61588&mpshare=1&scene=1&srcid=1116rv2LTZsJzm6Nkwf54mUb&sharer_shareinfo=c72c128193f68b83ce47ed1bbf90dd3e&sharer_shareinfo_first=c72c128193f68b83ce47ed1bbf90dd3e)**

##### **[原链 * 公众号 * 约 7 分钟读完](https://mp.weixin.qq.com/s?__biz=MjM5ODQ3MDk0Mg==&mid=2448912486&idx=1&sn=1c624db5497bc833722f1808d2bbd546&chksm=b3f10d8880c08bb0ecb1b353de4eb8e863b7f59f5789c7ab1e01168445a86cbcefb253d61588)**

[![Image](https://substackcdn.com/image/fetch/$s_!BmxM!,w_1456,c_limit,f_auto,q_auto:good,fl_lossy/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe739fb67-053f-4cd4-843c-f363656f86fe_1000x606.gif)](https://substackcdn.com/image/fetch/$s_!BmxM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe739fb67-053f-4cd4-843c-f363656f86fe_1000x606.gif)

作者学习了卡兹克的 Agent-Autoloop（前两周分享过），将自己的系统做了两项升级。一是加中控台，每一单的状态、耗时、费用、交接点全部可视化。二是换入口：从群聊一句话改成飞书多维表格，测试同事按原来的方式提问题，Agent 自动接单、修改、回写状态。

试验田是一个真实的支付 SaaS 项目，7 条问题跑下来：1 单关闭、3 单待复验、2 单待推送、1 单被判断为非问题。

他还给出两单的完整时间线：从接单到验收共 37 分钟，**Agent 实际干活约 10 分钟，模型费用分别是 1.14 和 2.35 美元**。

三条体会值得抄：入口要选团队本来就在用的东西；看得见才敢放手；给 Agent 眼睛，但别给手。

最后一句可以当这期的注脚：架子一旦搭起来，加人、加项目、加环节都比想象中容易----框架一行没改，改的都是规则、脚本和约定。

* * *

### 💻 **[5000亿 Token 原价 300 万、实花 7 万：冯若航的一人数据库公司怎么跑](https://mp.weixin.qq.com/s?__biz=MzU5ODAyNTM5Ng==&mid=2247494237&idx=1&sn=262d5d82c3a97c41c1a07e4542d1946d)**

##### **[原链 * 公众号 * 约 31 分钟读完](https://mp.weixin.qq.com/s?__biz=MzU5ODAyNTM5Ng==&mid=2247494237&idx=1&sn=262d5d82c3a97c41c1a07e4542d1946d)**

[![Image](https://substackcdn.com/image/fetch/$s_!Lerg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa7db7024-47c1-4df7-ac07-4d544a40a342_1080x608.webp)](https://substackcdn.com/image/fetch/$s_!Lerg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa7db7024-47c1-4df7-ac07-4d544a40a342_1080x608.webp)

冯若航在清华大学软件论坛做了个分享，主题很狂：一人公司借助 AI Agent 舰队，在数据库这种硬核基础软件赛道，能跑出百人级的产出。

证据是他自己的两个项目。一个是 Pigsty，他独立维护的开源 PostgreSQL 发行版：横跨 16 个 Linux 发行版，管理 600 多个扩展、3 万多个编译目标，GitHub 近 6000 星。另一个是 Silo，接盘 MinIO 社区版做的，不到一年 4600 星、下载近 800 万次，240 多个下游项目完成迁移。

他算的那笔账很有意思：**四 个月消耗 5000 亿 Token，按 API 原价值 300 万，走订阅制只花了 7 万，成本 2.5%**。他管这叫「健身房原理」----个人订阅补贴机制，让重度用户拿到数十倍算力杠杆。

方法上他提出「AI 工程管理学」：人是主刀医生，只做宏观决策，执行全交给 Agent。他的模型配比是 10 个 Codex、3 个 Claude、1 个 Gemini、1 个 GLM，调度底座就是一张 PostgreSQL 任务队列表。

工程实践三句话：设计靠文档驱动（ADR、架构蓝图），编码靠赛马与对抗（多模型互审），测试靠暴力测试----饱和式测试挖出过 100 多个深层 Bug。

最值得琢磨的是他解释「为什么组织级 AI 提效远不如超级个体」：阿姆达尔定律、沟通税、流程损耗三层漏斗，能把效率蒸发掉两个数量级。

收尾他很直接：现在是创业黄金时间，门槛降了，但竞争也加剧，快鱼吃慢鱼。

* * *

### 💰 **[一个总助带三个 Bot：跨境卖家把选品跑成了 7×24 自动流水线](https://mp.weixin.qq.com/s?__biz=MzA3MDA3NzI1Nw==&mid=2455089892&idx=1&sn=2bf4fd31f1734c6471efb852d0edb26f)**

##### **[原链 * 公众号 * 约 18 分钟读完](https://mp.weixin.qq.com/s?__biz=MzA3MDA3NzI1Nw==&mid=2455089892&idx=1&sn=2bf4fd31f1734c6471efb852d0edb26f)**

[![Image](https://substackcdn.com/image/fetch/$s_!cp5k!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc343adb5-c871-4a4f-8299-6cc9b461d953_1080x717.webp)](https://substackcdn.com/image/fetch/$s_!cp5k!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc343adb5-c871-4a4f-8299-6cc9b461d953_1080x717.webp)

选品分析做一次不难，难的是持续做。作者 Bulus lan 用 Grok Bot 搭了个「选品作战小组」，把这条流水线跑成了 7×24 自动运转。

配置是一个总助 Bot 统筹，下面三个兵：竞品情报 Bot、用户反馈 Bot、产品研究 Bot。靠着 Grok Bot 的云电脑、群聊协作、Skill 和 Routine 功能，从竞品拆解到产品改进决策，全程自动跑完。

他以美国站的透明收纳盒套装为案例演示：通过卖家精灵 MCP 接入真实市场数据，再用自研的 amazon-competitor-radar 和 review-analyzer-skill 两个 Skill，分别产出竞品观察表和需求证据表。

几个判断很老练：竞品分析要区分宣传卖点和实际交付；评论分析要结合样本基数，别被少数差评带偏；产品改进优先考虑信息表达调整，而不是上来就开模。

最后一步是 Routine 定时任务：竞品情报 Bot 每周自动监控核心 ASIN 的价格、主图和变体变化，变成一个 7×24 小时站岗的竞品情报哨兵。

他的收尾态度我喜欢：AI 不是替代思考，而是把繁琐手工活沉淀成标准工作流----把判断权收在自己手里，才是使用 Agent 的舒服状态。

（案例绑在 Grok Bot 上，但这套分工思路搬到任何带定时任务和 Skill 的 Agent 框架上都成立。）

* * *

### 随便看看：

  * **[《9.6 元就能生成一个的「AI 探店博主」，正在把多少人骗进难吃餐馆》](https://mp.weixin.qq.com/s?__biz=MzAwMjE1NjcxMg==&mid=2654846752&idx=2&sn=03eebf533f3b0e2e0a94ee2804c030ea)**：商家上传门店照片、充值 9.6 元算力，几分钟就能生成一条逼真探店视频；找代做团队做，要价 300 到 800 元，产业链上游公司月流水可达 800 万。大众点评半年处罚 500 多名虚假作者，杭州中院首例 AI 种草不正当竞争案判赔 10 万。

  * **[《AI 行业里，被高薪叙事平均掉的人》](https://www.huxiu.com/article/4906379.html?f=rss)**：高薪只属于塔尖少数人，塔下的人承受薪资落差与超负荷：校招变成社招，中层率先崩塌。麻省理工分析 300 多个企业 AI 项目，95% 没有可量化的利润影响。有人退向 AI infra 或国央企求稳，慢下来成了新选择。

  * **[《Claude 破解千页哥德尔手稿：80 年前他差一步拿菲尔兹奖》](https://mp.weixin.qq.com/s?__biz=MzIzNjc1NzUzMw==&mid=2247944324&idx=2&sn=aa3eb0414935136d02e8999ce363f0b1)**：哥德尔 1009 页手稿用的是全球仅约六人能读懂的失传速记，人类团队一年只能处理 50 页。Claude 几天交出 650 页解析、663 个定理，约 400 个通过 Coq 验证，还补全了一份当年可能值菲尔兹奖的未竟证明。

  * **[《在快 AI 时代，我是怎么把 Mole 做成一款「慢产品」的？》](https://sspai.com/post/118512)**：Tw93 做 Mac 清理工具 Mole 的笨功夫：让 AI Agent 装 853 款软件测卸载残留，补 13 类规则和 90 多条清理路径；逐一登录 30 多款 AI 工具记录占用。产品差距就藏在这些细节里。

  * **[《这些 AI 手搓的几百 K 的 3D 世界，正在让 HTML 再次伟大。》](https://mp.weixin.qq.com/s?__biz=MzIyMzA5NjEyMA==&mid=2647688394&idx=1&sn=a5db5eb7ca3dcd61d0774f97f3c2a5aa)**：数字生命卡兹克拆解一个 1.4M 的 HTML 游戏：700KB 是 Three.js 库，其余全靠代码现场生成模型贴图音效----文件里存的是菜谱，不是成品菜。附实操模板和 AI 自审迭代技巧。

### 适合个人上手的教程/评测/资源：

  * **[《微信同步 Obsidian 的 WXLink 插件实践》](https://mp.weixin.qq.com/s?__biz=MzIyMzk3MTEwNQ==&mid=2247488542&idx=1&sn=b942da31ca358d88cdb135ee611d62b7&chksm=e95fb8690fa36c529bd123a8c9a7cca3059326ce1ac18cee704901ab9ef8d8982a00776422ef&mpshare=1&scene=1&srcid=1116S8MhEBAlrwkcTtqjTxyW&sharer_shareinfo=fc067e27dab29dbef50f41974e230728&sharer_shareinfo_first=fc067e27dab29dbef50f41974e230728)**：Next 蔡蔡开源的 Obsidian 插件，基于腾讯官方 ilink 协议直连，不经过个人服务器，比服务号方案更稳。微信里发文字或链接，自动落进 Obsidian 的 inbox；离线消息下次打开时补收。

  * **[《腾讯员工用 Skill 生成器打造 AI 学习闭环》](https://mp.weixin.qq.com/s?__biz=MzYzODgxODMzNQ==&mid=2247496992&idx=1&sn=78d79a24ebc6b496f79291718cad5aac&chksm=f17ee366347981b1e02d71da69d5b06a56aaf4726b06f71c117aad04f41db806810888070250&mpshare=1&scene=1&srcid=1116A5mml2IymyE45ufnZLfQ&sharer_shareinfo=4f5d269f78ba2debd053ad3a6ae6f457&sharer_shareinfo_first=4f5d269f78ba2debd053ad3a6ae6f457)**：腾讯产品经理 Balance Li 把学习流程固化成 Skill：输入、学习、确认、验收、沉淀五步，每个学习点先定可验收的目标（能画出 RAG 流程，而非了解 RAG），进度存进项目文件，下次对话能续学。

  * **[《用 Grok Bot 白嫖 Twitter RSS》](https://mp.weixin.qq.com/s?__biz=MzIzOTY0OTQ2MA==&mid=2247486677&idx=1&sn=9660c2e88373182f312aa96cef482d63)**：潦草学者的邪修：让 Grok Bot 用 X 官方读取工具定时抓 49 个账号，生成静态 feed.xml 挂到 Vercel 免费托管。不买付费 API，不用 Cookie，每天两次刷新约占每日额度的 3%。局限是只收原创帖、非实时。

  * **[《实测 DeepSeek 四个接口只花一毛七》](https://mp.weixin.qq.com/s?__biz=Mzk0NzQzOTczOA==&mid=2247528783&idx=1&sn=2f35373ae9e8c3e24aa6efd5ace0dbda&chksm=c2bb0c60929ec19d77b43ec8b13408a30fc124bf2692e40f22c59d4e25f5bb49cec6f015ccc5&mpshare=1&scene=1&srcid=1115v3zlmKBjkAwlUg1jH2Y4&sharer_shareinfo=c2b2408aef36dc145de7e32c850a3ee6&sharer_shareinfo_first=c2b2408aef36dc145de7e32c850a3ee6)**：把 DeepSeek 的语音合成、语音识别、联网搜索、版面识别四个接口接成本地脚本：做双人播客、语音记待办、念早报、抠图表，20 笔计费请求合计 0.17 元。文中附几处暗坑，比如 MP3 会被拒收，得先转 Ogg Opus。

  * **[《省 token 提示词：让 Agent 不空转》](https://mp.weixin.qq.com/s?__biz=Mzg3MTk3NzYzNw==&mid=2247513929&idx=1&sn=279024d9066f57473a93d0fcebf30191)**：卡尔发现 Grok Bot 的定时任务吃掉 75% 额度：没更新也完整跑一遍。他把 Anthropic 常驻 Agent 指南翻成一段提示词：按版本去重、无变化只回「无更新」、不自行加戏。三天后 Bot 用量从 75% 降到 30%，总用量降 55%，一年省 840 刀。

  * **[《自动领 Token 开源工具实测》](https://mp.weixin.qq.com/s?__biz=MzkzMTQ0NDUxOA==&mid=2247484280&idx=1&sn=727ea55b8e45f246a9ee994fd035a2dd)**：向明开源的 agent-auto-signin，让 Agent 自动每日签到领免费额度：WorkBuddy、Qoder、豆包、TRAE、WPS 灵犀等合计每天约 900 单位。登录由用户自己完成，工具不存敏感信息，目前仅 Mac 实测通过。

  * **[《智能体私有部署选型指南》](https://mp.weixin.qq.com/s?__biz=Mzk2NDQ4MjExMQ==&mid=2247484533&idx=1&sn=6c6f42eb206d980057d9b77dcb1cc827)**：以 CRM 厂商上线销售智能体为例，推演全托管、混合、私有三种部署方式的差异。核心提醒：出域的不是数据库而是上下文，授权单位从角色变成任务。附客户安全评审必问的 6 个问题。

  * **[《开源项目 terminal-mac 让 AI Agent 拥有独立 Mac》](https://mp.weixin.qq.com/s?__biz=MzYyMTY1NDA0Nw==&mid=2247522920&idx=1&sn=18e8833c93b30df1d175730713e400f4)**：基于苹果官方 Virtualization 框架，给 AI Agent 一台完全隔离的 macOS 虚拟机，画面渲染进终端，内置 MCP 供 Claude Code 等直接截图点击。隔离解决了焦点抢占和误操作风险。

  * **[《播客剪辑 AI 工作流实战》](https://mp.weixin.qq.com/s?__biz=MzAxMzMxMjQxNg==&mid=2453122858&idx=1&sn=ef54e9655fb22c6442ebb8919e7e9818)**：沉思 Lu 把播客后期做成一套 Skill：转写盘选题、粗剪、字幕、插图动画、封面导出，已迁移到 Codex 上独立产出一条 84 秒视频。附双人同框的三种呈现方案、降噪参数经验，以及可直接抄的 30-60 秒试剪提示词。

  * **[《国产 MG 动画新工具：代码写视频，支持深度编辑》](https://mp.weixin.qq.com/s?__biz=MzY5NzMwNTczNg==&mid=2247489260&idx=1&sn=d08465f923d582f71c66fd50aec74c51)**：Fotor Agent 走「代码写视频」路线，大白话对话即可生成 MG 动画，交付的不是焊死的 MP4 而是可修改的视频工程：元素精修、多轨道时间轴、原生 4K 输出。适合高频更新的知识科普类自媒体。

  * **[《TapNow 语音指挥 AI 做视频全流程实测》](https://mp.weixin.qq.com/s?__biz=Mzk4ODYxNDE2OQ==&mid=2247489813&idx=1&sn=3bf5205e831727f6fd05117a67a16bf2)**：罗子马实测 TapNow：口述故事自动出提案和分镜，生成报错时 AI 自己做控制变量实验定位问题；Cinemap 搭 3D 白模、Monta 口嗨剪辑，全程不用打字。他的提醒也实在：模型厂随时可能吞噬应用层。

  * **[《MovieClaw：NAS 影音 Agent 新工具》](https://mp.weixin.qq.com/s?__biz=MzA4NzMyNzU5Mg==&mid=2453083871&idx=1&sn=a4d698d95284083d8a3096961536639d)**：NAS 影音 Agent，一句话完成找片、下载、刮削全流程，接入 PT 站、下载器和 TMDB 刮削，支持订阅轮播热门影视。Docker 部署，内置几十个工具还能通过 MCP 开放给外部 Agent 调用。
