##### ▪️PREFACE 卷首语

[![](https://substackcdn.com/image/fetch/$s_!-ffg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd0cf409c-6193-4aea-8468-91b1cb1130a6_1672x941.jpeg)](https://substackcdn.com/image/fetch/$s_!-ffg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd0cf409c-6193-4aea-8468-91b1cb1130a6_1672x941.jpeg)

1/ 我的新书《前线部署工程师（FDE）》，**电 子版已经在京东、多看、微信读书、当当上线**。这是之前那本开源书的精编，出版社做了校正、优化、配图等工作，让它的品质更优。感兴趣的可以去支持下。

纸质版预计国庆后问世，采用 32 开本，方便携带和随手查阅，这样能最大程度发挥这本偏实操性工具书的价值。拿来收藏、祭拜（？）也是极好的。上市了我再告知大家。

2/ 最近线下跟很多从业者聊 FDE。头一回干的，或是摩拳擦掌准备入场的，普遍在交付环节有困惑和卡点。尤其是甲方老板想做一套自己内部的 Agent，稍微懂行点的，会追问：项目效果怎么评测？失败怎么处理？权限怎么分配？隐私安全能保证吗？

对此我统一建议，还是系统地先补一下课。

极客邦科技新做了一期**「 AI Agent 全栈工程师训练营」**，用 14 周、一条项目主线，带大家完整走一遍 6 大企业级 Agent 项目的开发链路----从统一模型和工具调用底座开始，逐步做到诸如 Codebase Agent、RAG、多 Agent 协作与自动评测，再把日志、监控、灰度、成本治理都补齐，最后要有一个基于 DeerFlow 的综合大项目。

想学习 AI Agent 开发 / 做 FDE / 在企业内部推动 AI 转型的朋友，可以先领如下资料看看。里面有 2 小时试听课、六大项目学习路线和 AI Agent 知识库。先看清学习什么，再决定要不要报名。

[![](https://substackcdn.com/image/fetch/$s_!uneG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2f4eb877-2f61-4cec-9e78-853f8d5adca2_883x266.png)](https://substackcdn.com/image/fetch/$s_!uneG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2f4eb877-2f61-4cec-9e78-853f8d5adca2_883x266.png)

[Subscribe now](https://www.zengzhang.ai/subscribe?)

OK，以下是本周正刊内容，Enjoy----

* * *

##### ▪️OPINION 观点

### 🧩 **[AI正把文化变成黑暗森林：谁先暴露想法，谁先被狩猎](https://mp.weixin.qq.com/s?__biz=MzU4NDQwMTc3MQ==&mid=2247493501&idx=1&sn=aeed54d2f92101af8a7f442911386cea)**

##### **[原链 * 公众号 * 约 24 分钟读完](https://mp.weixin.qq.com/s?__biz=MzU4NDQwMTc3MQ==&mid=2247493501&idx=1&sn=aeed54d2f92101af8a7f442911386cea)**

纽约大学数学家特里斯坦*巴克马斯特和供职于 Anthropic 的合作者莱文特*阿尔珀格，借助 Claude、Codex 在纳维尔－斯托克斯千禧年问题上推进了很久。而 **OpenAI 听到传闻后，调动约一万个并发智能体，只用约 88 小时就完成解答并做了形式验证**。

双方随即陷入署名争执。

专栏作家埃里克*霍尔由此提出：AI 正把文化变成黑暗森林----**暴 露未完成的方向，等于向更强的竞争者发出狩猎信号。知识可以共享，但声誉和回报不会按贡献自动分配。当 AI 能独立做出相似成果时，保密只能保护时间差，保不住价格。**

作者给的出路很实际：**掌 握真实需求、参与持续合作、留下可验证记录、争取合理收益安排，并保留换工具、换渠道、换合作方式的余地。**

对普通人来说，这种变化先伤害学习，再拉大问题本身的差距。霍尔的答案是变成面壁者，但代价是切断知识生长的根、降低思考质量。毕竟过去隐藏是个人选择，今天你藏不住----吸收的成本归零了。

* * *

##### ▪️CASE 案例

### 🧠 **[定时任务失败率 99%、DeepSeek 涨价 12 倍：flomo 内置 Agent 背后的硬仗](https://mp.weixin.qq.com/s?__biz=MzI0MDA3MjQ2Mg==&mid=2247490716&idx=1&sn=1ab57e48792a6889becaf5d95cb3e0af&chksm=e81efe09e9c9d9cd29371a3857706af108214cceb5d8ebafb4021c006480b5b7909be8de2784)**

##### **[原链 * 公众号 * 约 9 分钟读完](https://mp.weixin.qq.com/s?__biz=MzI0MDA3MjQ2Mg==&mid=2247490716&idx=1&sn=1ab57e48792a6889becaf5d95cb3e0af&chksm=e81efe09e9c9d9cd29371a3857706af108214cceb5d8ebafb4021c006480b5b7909be8de2784)**

[![](https://substackcdn.com/image/fetch/$s_!ytSp!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb1701318-2a78-4db2-aa16-6cbb68a2b84e_978x612.png)](https://substackcdn.com/image/fetch/$s_!ytSp!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb1701318-2a78-4db2-aa16-6cbb68a2b84e_978x612.png)

笔记工具 flomo 最近大升级，把 Agent 内置进了应用，方便你去追问、去反驳、去联想，让触动变成具体行动。

Agent 就在首页输入框旁，可以随时 @ 过往笔记、调用技能讨论、识别图片，还自带全套定时任务，开启推送后不会错过提醒。

本文除了是对新功能的图文介绍，也披露了开发背后的部分隐情。比如，过去几个月 Clawbot 投递的定时任务**失 败率接近 99%**，部分用户的 Clawbot 被静默，排查无果后开发团队决定不再等待----把 Agent 内置进 flomo，定时任务结果直接在 App 内通知。

另一场硬仗是成本。DeepSeek 涨价后，**高 峰期消耗变成原来的 12 倍**，已经开发完的模型切换功能只得搁置。团队花了一个月把成本控制回涨价前的水平，抹平峰谷计价，还开发了重置卡。承诺是：不管外面怎么涨价，点数和涨价前一样耐用。

* * *

### 🎮 **[Dota国服前 100 的网吧老板，现在一个人管 700 台电脑](https://mp.weixin.qq.com/s?__biz=MzkxNzUwMTk5NQ==&mid=2247500642&idx=1&sn=f5f320226f676a05a1022a7683cf6e39)**

##### **[原链 * 公众号 * 约 13 分钟读完](https://mp.weixin.qq.com/s?__biz=MzkxNzUwMTk5NQ==&mid=2247500642&idx=1&sn=f5f320226f676a05a1022a7683cf6e39)**

[![](https://substackcdn.com/image/fetch/$s_!vH34!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F934503c2-6408-4ef7-9f0a-7860d0688aa5_966x546.png)](https://substackcdn.com/image/fetch/$s_!vH34!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F934503c2-6408-4ef7-9f0a-7860d0688aa5_966x546.png)

郭剑楠，浙大物理系毕业，Dota2 打到国服前 100。2021 年他在兰溪开出第一家屁屁猫网吧，五年后扩到 7 家，散在浙江四个城市，近 700 台电脑、42 名员工，年营收 1500 万元。

但管理一直是他的瓶颈。屋顶漏水、灯箱起火、厕所堵塞，所有事最后都找到他。

**想 看一遍完整经营数据，要在不同平台间切账号、登后台 28 次**，**光 月报就要花七八天。零食过期一次清掉 3000 多元的货；设备故障从发现到确定维修方案，要 7 到 15 天。**

转折点是一次小实验：他让店长用 AI 生成周报，**AI 发现了女性顾客占比上升的趋势，他据此添了香氛、提了卫生标准。**今年夏天，经朋友推荐他用上千问办公（看到这里知道是广告，但不妨碍了解这个非常具体的 use case），把收银系统、美团、抖音的账号授权接入，AI 每天早上自动发来经营日报、分析总结和营销建议。

变化最明显的是运维。CPU 温度、显卡负载实时监测，异常自动生成钉钉工单，**维 修周期从一两周缩到一天**；清灰也从全量拆机变成精准定位 20 台过热设备。

零食由 AI 读销售记录，提醒补货或下架。员工培训做成了游戏技能树，新人最快一天上岗；绩效拆成每日可领的积分任务，完成清洁约 5 元积分，一天额外拿 20 到 50 元。

现在 7 家店每月省下两三万元，他每天花一两个小时就能管完所有店。他还做了一张决策时间轴，把每次采纳 AI 建议的执行结果和门店数据挂钩，过一两个月回头看成效。

省下的时间干嘛了？每周打 Dota，东南亚服 500 名上下。

* * *

### 💰 **[AI社交的尽头是温柔乡：日本用户为什么甘愿掏钱](https://www.huxiu.com/article/4889564.html?f=rss)**

##### **[原链 * 虎嗅 * 约 15 分钟读完](https://www.huxiu.com/article/4889564.html?f=rss)**

[![](https://substackcdn.com/image/fetch/$s_!3fEk!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb55c1db4-d6ad-4a96-b07f-ebb3ed3d823f_792x409.png)](https://substackcdn.com/image/fetch/$s_!3fEk!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb55c1db4-d6ad-4a96-b07f-ebb3ed3d823f_792x409.png)

这两年很多 AI 社交项目被证伪关停，这个曾经让媒体竞相报道的赛道，也变得默默无闻。资本也退潮了。但这个方向真的偃旗息鼓了吗？

其实，被投资人/大厂叫停的 AI 社交，在日本成了吸金机器，有不少闷声发财的例子。

霞光社拆了 Zeta、キャラぷ 等产品，结论是日本市场有独特土壤：**二 次元文化加孤独经济，用户要的是情绪价值和温柔乡。成功产品的打法普遍激进----用 KOL 营销和从众心理，直接击穿用户的信任门槛。**

文章有个判断值得记住：**AI 社交的底层是叙事内容，不是技术交互，所以产品得围绕内容生成和消费场景来设计。韩国公司在粉丝内容运营上的优势（比如 KPOP 模式）可以迁移过来，未来方向则是「消费即生成」和低门槛的多模态体验。**

最后一句话很狠：**从 业者得先相信 AI 内容能打败抖音，才有可能在竞争里胜出。**

* * *

### 💻 **[先手动 onboarding 300 个用户、再拼命删功能：Grok Bot 一个月封神的笨办法](https://mp.weixin.qq.com/s?__biz=Mzg3NDc2MjQxMg==&mid=2247495217&idx=1&sn=ebb07d8a4c70889e76ed6ea750cb65dd)**

##### **[原链 * 公众号 * 约 16 分钟读完](https://mp.weixin.qq.com/s?__biz=Mzg3NDc2MjQxMg==&mid=2247495217&idx=1&sn=ebb07d8a4c70889e76ed6ea750cb65dd)**

Roman Ugarte 在 Lenny's Podcast 里复盘了（马斯克家新出的）Grok Bot 的爆发：一个月从零做到最热 AI 产品，靠的是两个反直觉决定----所有东西跑在云端，每个 bot 有自己的计算机（这是成功者的事后归因，并且肯定掩藏了不少真实想法，所以听听就好）。

团队刻意保持小而隔离，一个月做出原型，然后**手 动 onboarding 了近 300 个早期用户**，逐个观察真实用法。接着是大量删功能，把产品语言从「有」改成「能做到」，让用户用自然语言直接建立自动化任务。SpaceXAI 内部招聘团队的用法也提供了样板：用 bot 自动追踪论文作者并引荐。

Roman 有句话点透了体验差异：**能 100% 完成工作的 AI 和只能做 90% 的 AI，感觉完全不同**----后者依然占用用户心智。

真正的 AI-native 产品得从根上为 AI 设计，让用户把 AI 当成有电脑的同事，而不是一个聊天窗口。

* * *

### 随便看看：

  * **[《一线销售们所亲历的 AI 办公大战》](https://mp.weixin.qq.com/s?__biz=MzkxNzUwMTk5NQ==&mid=2247500565&idx=1&sn=e9ebd8f4325cbaff5a954747dc92f6aa&chksm=c0f2c8baafc2c2c7500ab23894af261acff872edcdfd1618ba3a6b8eadc426807c79db4981b1)**：腾讯 WorkBuddy、字节豆包、阿里千问办公贴身肉搏。一线销售的真实体感：客户买不买取决于现有办公系统而非模型能力，单卖席位利润微薄，赚钱靠的是后续转型服务和 token 消耗。

  * **[《围绕 AI 重建公司的实战手册》](https://mp.weixin.qq.com/s?__biz=MzA3MDQyNDUzMA==&mid=2649928659&idx=1&sn=48f40bdd248d45a838c1684832ae3c54)**：这期 a16z 播客中，二手车公司 Kavak 创始人分享转型 AI 原生：每天跑 10 万到 20 万个智能体，96% 客户互动由智能体处理，转化率达人类 2.1 倍，还在墨西哥试了 AI CEO，利润提升 50%。

  * **[《GEO 加盟堪比诈骗》](https://mp.weixin.qq.com/s?__biz=MzA4MTc3NzY0Mg==&mid=2652351009&idx=1&sn=b1ef2564fc89ae3083641db5096a2f96)**：GEO 最先跑通的生意，是向普通人招城市代理收钱。「零加盟费」背后，首次进货、算力预存、保证金总有一个名字负责把钱收走；而代理商能触达的小商户，恰恰最不适合做 GEO。

  * **[《日薪千元的 AI 实习生，在焦虑什么？》](https://mp.weixin.qq.com/s?__biz=MzkzODUxNTM2OA==&mid=2247542162&idx=1&sn=2afa2e8d605a3e530a97cc6c6b964b61)**：大厂 AI 实习，普通岗位日薪 500 到 1000 元，博士生最高 6000 元，但高薪集中在极少数人身上，门槛一年比一年高。五位实习生的共同焦虑：不知道稀缺能持续多久。

  * **[《苦等上岸，AI 职业培训班里的年轻人》](https://mp.weixin.qq.com/s?__biz=MzkxNzUwMTk5NQ==&mid=2247500602&idx=1&sn=1f8bbf1e4859f8469150bc18d454515f&chksm=c069b87d579da71da1bdf11bc65357a5483ec72cf972ebaa1023c54d718695efc3fa33c3d250)**：销售话术是「零基础转型，半年上岸，挑战 25W+ 年薪」，合同小字却是「不承诺就业」。多数学员只学会了包装简历，就业率靠试用期连环跳槽兑现。有学员自嘲：我们可能都只是 AI 时代的炮灰。

  * **[《外企员工成了第一波 AI 难民》](https://mp.weixin.qq.com/s?__biz=MzIwNzM2MjA4OA==&mid=2247596222&idx=1&sn=5b3db0c1fd7c0c21a771fe08ab336c40&chksm=96226efec7da7bdec125741cc2c11a7bcea60203dc864f4b942050f8580830f83d3d0985c0eb)**：国产 AI 不在总部采购清单，境外工具又怕数据出境，外企员工两头不靠。微软 Copilot 配额稀缺，1800 人的公司里供应链部门只抢到 3 个账户；有小组争取名额时，三名提效不明显的同事先被裁了。

  * **[《批量自动化崩老头，一个 AI 搞定了》](https://mp.weixin.qq.com/s?__biz=Mzg5ODU4OTU3MQ==&mid=2247502366&idx=1&sn=07d845ffa276a6eb68edd0a82cf0ac5b)**：约会 App 把大模型塞进匹配池冒充女性，两周跑出 4700 多个 AI 人格、处理 236 万条消息，AI 与真人比例约 4:1。「三聊一崩」行规：聊三次要一次钱，单笔 20 到 50 元，老手月入两三万。

  * **[《Corgi Girls 与硅谷 AI 圈的「辣妹复兴」》](https://mp.weixin.qq.com/s?__biz=MzkyMTczNjE3Nw==&mid=2247493267&idx=1&sn=0fbb8d6c1d483ad5fcea3b50ad3253a8)**：Corgi Insurance 的社区负责人把外貌、生活方式和销售能力整合成个人品牌。AI 拉低技术门槛后，注意力成了稀缺资源，销售与营销能力重新升值。

  * **[《情况又变，35 岁成香饽饽了》](https://mp.weixin.qq.com/s?__biz=MzI2NDk5NzA0Mw==&mid=2248901419&idx=2&sn=98acc3ebb3efafefefdc3722ded6284c)**：斯坦福研究：AI 暴露高的职业里，年轻人就业下滑 19%，41 岁以上群体反而增长。可编码知识被 AI 吃掉，隐性知识与 AI 互补----前提是别把经历只熬成工龄。

### 适合个人上手的教程/评测/资源：

  * **[《开源 Mac 操控 skill，让 agent 高效办公》](https://mp.weixin.qq.com/s?__biz=Mzg2OTA1OTAxNA==&mid=2247492082&idx=1&sn=8bd0094afaec0208069ad1c50a6cc12c)**：花叔开源的 Mac 操控 skill：探测 app 四种可操控层，读写分离不抢用户焦点，每次操作后回读验证。Claude Code 实测 33 分钟用 Blender 建出邮轮模型。

  * **[《花叔开源 Huashu-Report 报告 skill》](https://mp.weixin.qq.com/s?__biz=Mzg2OTA1OTAxNA==&mid=2247492170&idx=1&sn=64f9df6b6a646e523817563d8e34a058)**：花叔开源的报告 skill：数字必须先进数据表，能写成代码的规则全进编译器，最后逐页人工扫版式。跑了 19 个 agent 拆解 42 份顶级机构报告校准品位，MIT 协议，装上即用。

  * **[《用 TraeCode 搭建 LLM Wiki 知识库》](https://mp.weixin.qq.com/s?__biz=MzkxMTY4NTAyNQ==&mid=2247520153&idx=1&sn=c5d44a247c80e79d96d055c2815570db)**：从 Karpathy 的 LLM Wiki 推文出发，演示用 TraeCode 从零搭个人知识库：三层架构，提取、查询、巡检三大操作。和 RAG 的区别在于知识编译一次、持续积累，而非每次重新检索拼凑。

  * **[《公众号文章一键转 AI 知识库教程》](https://mp.weixin.qq.com/s?__biz=MzkxNTUwODgzNA==&mid=2247543756&idx=1&sn=811fdb5483f0014eee2bf9ab89b8f0b1)**：阿虚同学开发的小工具：任意一篇文章链接即可采集整个公众号的历史文章，导出 JSON 导入腾讯 ima 知识库，增量采集可同时跑几十个账号。需下全文可配合 wechatDownload。

  * **[《GPT-6 Astra 操控 Blender 建模教程》](https://mp.weixin.qq.com/s?__biz=MzIyMzA5NjEyMA==&mid=2647686056&idx=1&sn=c1710404c08cf3201da27f4d53f94940)**：数字生命卡兹克的保姆级教程：Computer Use 口述建天坛祈年殿（4 小时、约 100 美元）、MCP 做摩托车动画、CLI 跑脚本。规则几何体效果良好，生物模型还得靠 Tripo 生成再导入。

  * **[《Typeless 平替网易叭哥体验》](https://mp.weixin.qq.com/s?__biz=Mzk0NzQzOTczOA==&mid=2247526946&idx=1&sn=4f995a4ba47b6c1ed6a139e92f863eba)**：Typeless 免费额度从每周 8000 字砍到 2000 字后，作者试了网易叭哥：小声说话识别不错，支持 100 多种语言翻译，承诺云端不留存数据；但识别率略差，非流式输入缺实时反馈。

  * **[《6 个月机器人工程师速成指南》](https://mp.weixin.qq.com/s?__biz=MzA4ODg0NDkzOA==&mid=2247515233&idx=1&sn=30fe5c6069d890fbff38275d76e5bfd1)**：机器人是当下最不拥挤的高价值技能。路线图假设零电子基础，每月一个主题：焊接、Arduino 与 ESP32、ROS 2、仿真、控制理论，六个月做出能展示的机器人，附三档硬件预算。

  * **[《AI 时代求职避雷指南》](https://sspai.com/post/114461)**：被「倒序名单」裁员后，作者用 AI 三步写简历：念叨全部工作细节、提炼总结、按心仪 JD 定稿。避雷清单包括四种猎头（靠谱的极少）、算法推荐失效，以及海外博彩等诈骗职位。
