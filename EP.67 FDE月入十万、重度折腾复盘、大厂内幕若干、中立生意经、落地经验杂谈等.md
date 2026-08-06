##### ▪️卷首语

  * 最近一周继续用 Kimi K3 优化我这个 Newsletter。基于过往运营一年多、产出 66 期内容所沉淀的数万篇内容+机器打标+我人工打标，做了一次全量回归，调整了各项评分参数和 prompt。现在效果明显进步了，这一周筛出我感兴趣且高质量的长文，明显更多了，一下子都有点看不完。所以这期的篇幅整体也变长了。不知道大家是更满足了，还是更焦虑了？我会根据数据结果和各位的反馈继续打磨。

  * 想体验 Kimi K3，但是被官方的会员售罄告示卡住了？可以 **[用我的邀请链接注册](https://kimi-bot.com/activities/zh-cn/invite/share?scenario=invite&from=share_poster&invitation_code=EVAFWM) **Kimi 新账号，就可以获得一次抽奖机会，赢得 3 天 ~ 365 天对应的会员资格配额奖励。100% 中奖，亲测成功，我这个月又多白嫖了不少算力。

  * 上周免费开源到 Github 的 **[《前线部署工程师：人工智能时代的客户价值交付秘籍》](https://github.com/xdash/FDE-the-Guidance-Book-of-Forward-Deployed-Engineer)** 一周来已经获得了 3k+ stars，感谢大家的支持。我还在继续润色和增补，现在可读性整体更好一些了，但还有提升空间。这是个开源项目，会持续维护。也欢迎 follow 我的 Github 主页。

[Subscribe now](https://www.zengzhang.ai/subscribe?)

* * *

##### ▪️OPINION 观点

### 📈 **[硅谷工程师眼中的 AI 创业下半场](https://mp.weixin.qq.com/s?__biz=MzkyNDEzOTAzNg==&mid=2247487925&idx=1&sn=0f257c001dbb27ee9d22343600883592)**

##### **[原链 * 公众号 * 约 17 分钟读完](https://mp.weixin.qq.com/s?__biz=MzkyNDEzOTAzNg==&mid=2247487925&idx=1&sn=0f257c001dbb27ee9d22343600883592)**

硅谷 AI 工程师马培元在最近一篇专访里给出 10 个判断，覆盖人才、组织、行业和投资，核心就一句话：**野 蛮生长阶段过去了，所有共识都在迅速过期。**

  * 人才市场正在重写规则。通才碾压专才，兼具 AI、全栈与 iOS 经验的「六边形战士」最抢手；AI 原生技能可以短期碾压资历，他自己靠 AI 辅助，两年做到资深。

  * 招聘也变了：算法题权重下降，流行在线笔试加 work trial，用 AI 和禁用 AI 的考察轮次并存。

  * 组织层面，「更好地使用 AI」实质是组织转型问题。AI 能把数天的 Bug 修复压到两三个小时，倒逼架构扁平化；People manager 正在消亡，管理者必须自己写代码----**Cognition 60 多人的工程团队，只有 1 个纯管理岗**。

  * 行业判断上，Token 狂热开始退潮。大公司被 AI 账单吓到，**Uber 四个月就烧完了全年预算**，转而限制用量；Cognition 顺势推出「AI 生产力保证」，效率不达标最高赔 1000 万美元。

  * 模型崇拜也被推翻，融合调度多个便宜模型与顶尖模型成了新做法。

**投 资机会在两头：新的 AI infra（监测 agent 输出质量、沙盒隔离），以及 vertical agent----垂直行业存在大量「不可训练」的复杂流程，能带来 20-100 倍的稳健回报。**

AI 时代，任何判断的保鲜期可能不足一个月，非共识里正孕育新生意。

* * *

### ⚠️ **[AI应用的「二房东」困局](https://mp.weixin.qq.com/s?__biz=MzkyNjU2ODM2NQ==&mid=2247631326&idx=1&sn=246cd251e4dabe91570a79a1ea9d23a4)**

##### **[原链 * 公众号 * 约 29 分钟读完](https://mp.weixin.qq.com/s?__biz=MzkyNjU2ODM2NQ==&mid=2247631326&idx=1&sn=246cd251e4dabe91570a79a1ea9d23a4)**

AI 视频公司 OiiOii 年底要向火山引擎支付 5000 万元，买 Seedance 2.0 的「纯血版」API----这种采购往往不是业务需要，而是为了抢首发权和并发资源。

这篇文章顺着这笔钱往下挖，挖出了 AI 应用公司的集体尴尬：**商 业模式沦为一条持续亏本的 token 周转链。**

顶级模型的能力决定应用上限，模型厂商用 token 价格卡脖子，应用公司只能当「二房东」，**毛 利率普遍只有 10%-25%，甚至出现「毛亏率」**。

文中提到的最典型的是演语科技旗下 LibTV：以年框 5000 万购入 Seedance 2.0，再以低于采购价 10% 的价格把 token 转卖给友商，只为推高 ARR 融资叙事。**用 户消耗 token 越多，平台亏得越多；用不完的额度又变成清仓甩卖的库存。官方打击「逆向工程」转卖，实质是在和用户争夺转售资格。**

成本被后置结算放大，应用公司被迫四处寻找低价 token：上游倾销、同行甩卖、政府补贴，乃至「中转站」泛滥。传统 SaaS 是用户越多越便宜，AI 应用却是**用 户越多越亏**----边际成本跟着使用量回来了。除非找到定价权、或彻底改变成本结构，这套游戏里的创业公司只能在毛亏率中挣扎。

* * *

### ⚔️ **[大厂 AI 办公换战场的内幕若干](https://mp.weixin.qq.com/s?__biz=MzU3Mjk1OTQ0Ng==&mid=2247537832&idx=1&sn=d9a795ebff15c009b503ee63ae9c8d2f&chksm=fd050b7a278dd4927f777c875cfc608ff18bbfa1332a379ebf6108e75758e5b6b2fd8000131c)**

##### **[原链 * 公众号 * 约 21 分钟读完](https://mp.weixin.qq.com/s?__biz=MzU3Mjk1OTQ0Ng==&mid=2247537832&idx=1&sn=d9a795ebff15c009b503ee63ae9c8d2f&chksm=fd050b7a278dd4927f777c875cfc608ff18bbfa1332a379ebf6108e75758e5b6b2fd8000131c)**

2025 年 DeepSeek R1 发布后，腾讯、阿里、字节重新押注 AI 办公智能体----钉钉、飞书、企业微信都被视为上一代产物，三家站回同一起跑线。这篇内幕稿梳理了三家的变阵路径。

腾讯把资源归拢到 WorkBuddy，打通混元大模型与多条业务线，**日 活已达百万量级，超过所有国内对手**。阿里在赛马中快速整合：1992 年出生的陈宇森接手钉钉，把 QoderWork、悟空、MuleRun 合并为「千问办公」，八月初公测并打通钉钉。字节动作最大：飞书产品团队并入豆包，销售与客服归入火山引擎，飞书负责人谢欣承认调整仓促。

为什么推倒重来？此前巨头受 OpenAI 影响，集中押注通用聊天机器人和超级入口，结果春节大战集体碰壁----元宝、千问日活冲高回落，**豆 包日耗算力数千万元，收入却不足百万**。to B 和智能体成了唯一坚定的方向。

文章的潜台词值得咀嚼：旧产品的功能、组织与商业模式已经固化，AI 入口救不了它们，必须从头做 AI 原生办公产品；飞书、钉钉最大的价值，可能只是多年积累的企业组织上下文数据。一位阿里人士的反问点破了这层关系：是豆包、千问更需要飞书、钉钉，还是反过来？这场近十年没分出胜负的战争，换了个战场重开。

* * *

##### ▪️CASE 案例

### ⚡ **[21个定时雷达、5000 篇自建库：一个重度用户的两个月 AI 折腾复盘](https://mp.weixin.qq.com/s?__biz=MzIzMzM2Mjk5OQ==&mid=2247484756&idx=1&sn=7f99ce91d735f07f35b9fb1a145e012b&chksm=e9227be73dcda345038afe92a0e82f1ff5bad6dd2dd189eef4cdbaa3b566fb2fa522c777bd07)**

##### **[原链 * 公众号 * 约 11 分钟读完](https://mp.weixin.qq.com/s?__biz=MzIzMzM2Mjk5OQ==&mid=2247484756&idx=1&sn=7f99ce91d735f07f35b9fb1a145e012b&chksm=e9227be73dcda345038afe92a0e82f1ff5bad6dd2dd189eef4cdbaa3b566fb2fa522c777bd07)**

[![](https://substackcdn.com/image/fetch/$s_!Oeu6!,w_1456,c_limit,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faa63bb2e-3b92-417d-b197-fd50132e6b30_1554x1054.heic)](https://substackcdn.com/image/fetch/$s_!Oeu6!,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faa63bb2e-3b92-417d-b197-fd50132e6b30_1554x1054.heic)

来自我们社群小伙伴 @马奇诺 的分享。

他把自己六七月两个月的 AI 实践写成了流水账，密度很高。工具按机器分工：公司电脑跑 Claude Code，家里电脑跑 Codex，配合网易 UU 远程异地操控。三端同步弃用 iCloud，改用三个 git 仓库加坚果云分层存储，cron 兜底。VPS 加 Claude Code 加飞书机器人组成 24 小时在线助理，**承 载 21 个定时雷达**。

踩坑经验也实在：DeepSeek V4 迁移要显式关闭思考模式；动态日期别进 system prompt，否则缓存全失。知识沉淀上，他的自建库已存 5000 多篇数据，通过 review 漏斗筛出 30 条，**其 中 9 条即时落地**。

还提到：把 AI 嵌进飞书社群运营的「元宝派」构想；反馈上瘾引发的异步工作与睡眠管理；AI 自媒体在品味与流量之间的矛盾等。

* * *

### 💰 **[呼兰当「临时 CEO」：用 AI 把月亏 12 万的脱口秀俱乐部做到盈利 7 万](https://mp.weixin.qq.com/s?__biz=MzA4MDMwNjcxNg==&mid=2648348730&idx=1&sn=80b71ad7170e4845c7fa8d02a13e41ea)**

##### **[原链 * 公众号 * 约 21 分钟读完](https://mp.weixin.qq.com/s?__biz=MzA4MDMwNjcxNg==&mid=2648348730&idx=1&sn=80b71ad7170e4845c7fa8d02a13e41ea)**

脱口秀演员呼兰（前程序员、精算硕士）以「临时 CEO」身份接手深圳开花俱乐部时，账上是月亏 9-12 万，客流惨淡。

他先做产品重构：砍掉每日开放麦，固定为周二练习场、周四粤语之夜等专场，引入投票器和演员排行榜。但真正扭转局面的是 AI 系统 Accio Work。呼兰用它快速搭起数据看板：自动接入多个售票平台，清洗、去重、关联，半小时生成可视化经营数据----以前这是人工逐个平台统计的粗放活。更典型的是灯牌采购：AI 自主完成设计选型、比价、联系工厂、准备谈判话术，**两 天走完原本需要数天的流程**。

两个月后，俱乐部**从 月亏 9 万转为盈利 7 万**。这个案例的价值在于可复制：AI 承接重复性低效工作，人回归创作和决策----放在任何一家线下小剧场、乃至更多小微企业身上，逻辑都成立。

* * *

### 🧭 **[硅谷 pitch 现场：不吹模型，全在讲自己行业落地之痛](https://mp.weixin.qq.com/s?__biz=Mzg3NDc2MjQxMg==&mid=2247495025&idx=1&sn=92d7d6498b9669ceaf27092f46d41c50)**

##### **[原链 * 公众号 * 约 17 分钟读完](https://mp.weixin.qq.com/s?__biz=Mzg3NDc2MjQxMg==&mid=2247495025&idx=1&sn=92d7d6498b9669ceaf27092f46d41c50)**

[![](https://substackcdn.com/image/fetch/$s_!2QLt!,w_1456,c_limit,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6bb3d788-29e9-46cd-b47f-0a44936617fc_1542x1144.heic)](https://substackcdn.com/image/fetch/$s_!2QLt!,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6bb3d788-29e9-46cd-b47f-0a44936617fc_1542x1144.heic)

作者在旧金山一场 pitch 活动上观察到一个明显转向：8 个团队里，大多数不再展示模型优势，而是讲业务痛点和自身经历。AI 工具商品化之后，硅谷创业公司的竞争壁垒正从技术转向行业理解。

几个样本很有说服力。做房地产的 Realty AI 用 AI 协调交易流程，已有 10 个真实经纪人完成 12 笔交易；做二手配送的 RAACT 拍照自动匹配配送方案，在湾区积累 2800 个用户；做楼宇能源管理的 Zoya 覆盖 900 多万平方英尺建筑，帮客户省下近 20 万美元。当晚第一名 Cure Money 瞄准信用合作社市场，花一年和 6000 个用户研究建立知识图谱，已拿到 NSF 资助。还有团队**把 动漫制作成本从每集 15-30 万美元压到 1-2 万美元**。

投资人关心的问题很一致：壁垒在哪、谁付费，强调数据、架构或分发的差异化。作者顺手点了早期项目的常见病：定价过低、TAM 计算脱离实际、竞争分析过于乐观、低估 AI 的生产稳定性。结论可以当金句用：**AI 让「实现」变便宜了，但没有让「判断」变便宜**----来自行业内部的理解，才是难以复制的护城河。

* * *

### 💻 **[被 A 厂封禁，月活反而从 250 万暴涨到 1300 万：OpenCode 的中立生意经](https://mp.weixin.qq.com/s?__biz=Mzg5NTc0MjgwMw==&mid=2247525470&idx=1&sn=205576340ca805cc94f0d4e3f04b105f)**

##### **[原链 * 公众号 * 约 34 分钟读完](https://mp.weixin.qq.com/s?__biz=Mzg5NTc0MjgwMw==&mid=2247525470&idx=1&sn=205576340ca805cc94f0d4e3f04b105f)**

开源 Coding Agent 的崛起一定要靠技术碾压吗？OpenCode 的故事给出另一个答案。这篇整理了 CEO Jay V 与联合创始人 Dax Raad 近半年播客访谈的文章，核心词是「定位博弈」：在 Claude Code、Codex 主导的市场里，占据开放、中立、不锁定用户的位置，让所有模型公司互相竞争时都愿意借力于它。

2026 年 1 月，Anthropic 封禁用户通过 OpenCode 调用 Claude 订阅----这反而成了增长拐点。OpenCode 顺势拿到 OpenAI 官方支持，**月 活从 250 万暴涨到 6 月的 1300 万，每日处理 7 万亿 token**；推理业务年化收入约 4000 万美元，订阅再贡献 1800 万。Dax Raad 对开源价值的解释也实在：社区能帮忙适配 Gemini 等各类模型，覆盖长尾需求，这是闭源产品复制不了的护城河。

关于模型竞争，Jay V 的判断是开源模型已从「追求最聪明」转向「足够聪明＋成本/速度优势」----Kimi 曾因 token 速度远超 Opus 带动订阅增长，GLM 5.2 也因前端能力吸引用户。至于竞争策略，他们说得很坦白：选择一个暂时的「坏人」，团结整个行业对抗它，Anthropic 不幸成了那个靶子。给创业者的启示：当市场上有一两个主导玩家时，站在它们对立面的开放生态位，可能比正面竞争更有爆发力。

* * *

### 🛠️ **[FDE月入十万的主要工作：告诉老板「世界上已经有汽车了」](https://mp.weixin.qq.com/s?__biz=MzkxNzUwMTk5NQ==&mid=2247500406&idx=1&sn=1c505df4efbe8ca6bf1ff7e298ca83e6)**

##### **[原链 * 公众号 * 约 14 分钟读完](https://mp.weixin.qq.com/s?__biz=MzkxNzUwMTk5NQ==&mid=2247500406&idx=1&sn=1c505df4efbe8ca6bf1ff7e298ca83e6)**

FDE（前线部署工程师）成了 AI 落地最热的新岗位，个人接单者月入十万。这篇文章通过三位转行者的故事，讲了这份钱到底好不好赚。

26 岁的 Lawted，北邮计算机毕业、进过阿里，AI 浏览器创业失败后转接单，给深圳一家货代公司做 AI 化改造。驻场后他发现，三十多名员工手动处理货运 PDF，流程极度落后，但系统切换风险巨大：**公 司毛利率仅 8%，一单出错全年白干**；老系统安全运行六年，而被替代的员工月薪四千，token 费反而更贵。他感叹，FDE 一大半工作是告诉老板「世界上已经有汽车了」。

27 岁的 Jolie Ni 从硅谷程序员转行，成了 Anthropic 的 Claude Partner，**平 均月收入超 10 万元**。她学到的最重要一课是「教育客户」：企业只说「提效率」，却说不清痛点，甚至抗拒流程重组。她判断个人 FDE 只是过渡，企业最终会设立内部岗位，因此计划转型培训企业内部 FDE。

24 岁文科生小唐因焦虑被 AI 替代而学 vibe coding，低价接单练手，帮一家预约平台用 AI 数字人接管客服和客户经理，真人参与度降到 5%。但新问题随之而来：老板要求可视化、需求变化快，每换一个行业就得重新摸索，无法产品化。

FDE 的困境在于人力成本高、需求太具体，降本空间有限，项目往往是一锤子买卖。三位受访者不约而同转向培训或社群，把「赚焦虑钱」变成可持续的生意。或许真正的机会不在个人单干，而在教会企业自己养 FDE。

* * *

### 🎮 **[不卷角色卷「小镇」：这款 AI 陪伴产品月流水 98 万美元](https://mp.weixin.qq.com/s?__biz=MzYzNTkyMTI2Ng==&mid=2247575405&idx=1&sn=f7020fa433ae373534b0f0405fded71e)**

##### **[原链 * 公众号 * 约 14 分钟读完](https://mp.weixin.qq.com/s?__biz=MzYzNTkyMTI2Ng==&mid=2247575405&idx=1&sn=f7020fa433ae373534b0f0405fded71e)**

[![](https://substackcdn.com/image/fetch/$s_!-6JA!,w_1456,c_limit,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff991c2d1-d8cb-464c-91f7-c2be6026996c_1596x866.heic)](https://substackcdn.com/image/fetch/$s_!-6JA!,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff991c2d1-d8cb-464c-91f7-c2be6026996c_1596x866.heic)

AI 陪伴这个品类，商业化前景一直不明朗，Enjoy-AI Town 却做到了**月 流水 98 万美元**。白鲸出海编辑部张凯然拆解了它的打法。

产品借鉴斯坦福论文和开源 AI Town，把「人观察 AI 社交」变成「人和 AI 一起社交」：场景成为对话的上下文，UGC 机制让体验维度指数级增加，多角色关系网络提供了 1v1 聊天给不了的剧情厚度。

真正的引爆点，在变现设计和深度体验的化学反应。银币与红心双货币分别对应「建设」与「叙事」，三档订阅形成梯度付费墙；用户从早期功利性购买加速道具，转向购买货币搭建小镇、培育关系----**RPD 从 1 月的 1.15 美元升到 6 月的 2.15 美元**，加速道具 Magic 的销售额占比从第二跌到第五，建设性货币销量大幅上升。

张凯然的洞察是：同质化产品都在卷对话质量和角色精度时，**用 「地理变量」把单一关系变成多节点网络，靠节点间的随机碰撞制造惊喜，反而走出新路。**与其在既有维度内卷，不如重构产品的基本单位----从「角色」转向「场景」和「关系网络」，让用户从付费「逃课」转而为叙事深度买单。

* * *

### 随便看看：

  * **[《深度 | 外宾 Genspark》](https://mp.weixin.qq.com/s?__biz=MzkyNjU2ODM2NQ==&mid=2247631520&idx=1&sn=040eaafcab32ba3cfeeac0390760b802&chksm=c3f61b13a679c7a7a0b4ec36de42d2921f163bbe33dd9ef598ea4d4f1b1479eb0eefef577116)**自称美国硅谷公司的 Genspark，实际是百度前高管景鲲和朱凯华创立，对外叙事刻意淡化中国背景。

  * **[《AI 正导致一场知识的转基因危机，多数人将沦为认知肉鸡？》](https://mp.weixin.qq.com/s?__biz=MzU4NDQwMTc3MQ==&mid=2247493298&idx=1&sn=76c0f386d66c349ebb8368034df0bb34)**互联网超 50% 新内容由 AI 生成，检索池污染率达 67% 时，用户有超 80% 概率接触 AI 内容。

  * **[《梁文锋青年往事：八万本金、一台菲亚特和一个人的长征》](https://mp.weixin.qq.com/s?__biz=MzkyMTczNjE3Nw==&mid=2247491841&idx=1&sn=a248ac7f6bb9129ce83d798d9bfc4ca6&chksm=c0379407df80de918c3b5b2b52a5290f9fe7f48f0013370444b715fb3b7352c7b22e6981e222)**幻方量化和 DeepSeek，都是这条「慢」路线的回报。

  * **[《AI 终于带来了新职业 FDE，这个活阿里是怎么干的》](https://mp.weixin.qq.com/s?__biz=MjM5ODQ2MDIyMA==&mid=2650735339&idx=1&sn=05ec00ffa82e1ed7a12c1816784b9a46)**文章聚焦阿里瓴羊 FDE 团队：雅迪客服项目里，FDE 坐进客服席位，把人的判断拆解成 AI 能执行的步骤。

  * 三篇大厂有关的（顺便推荐刚上映的《年会不能停2》，挺好笑的）：**[《我在大厂，四处「活水」》](https://mp.weixin.qq.com/s?__biz=MjEwMzA5NTcyMQ==&mid=2653253396&idx=1&sn=9c4527802f7b6e84993bd6e191e9ccb0)**、**[《AI 来了，大厂中层不好混了》](https://www.huxiu.com/article/4879898.html?f=rss)、[《最近的大厂人，恨透了它》](https://mp.weixin.qq.com/s?__biz=MjM5ODMzMDMyMw==&mid=2654907059&idx=3&sn=71d75c753338aa59b820104449e5a64a)**。

  * **[《瞄准家庭协作痛点，两个前大厂员工用三周做出日程管理小程序》](https://mp.weixin.qq.com/s?__biz=MzU1Mjc4NjM4Mg==&mid=2247590945&idx=1&sn=2a7041b6ff16575095d2bc396a6543ba)**前大厂员工张坤的前同事因孩子接送问题和妻子争吵，两人干脆动手做了个小程序「卷了么」。

  * **[《我用 AI 谈恋爱》](https://mp.weixin.qq.com/s?__biz=MzkzMTI3MTUyMw==&mid=2247523671&idx=1&sn=2845ef04292cdd0bc6e624b9dba05cbf)**作者 Y 自述和男友 L 各自借助 AI 处理亲密关系。

  * **[《为了和 AI 谈恋爱，她们给 AI 手搓身体、开发长期记忆系统，甚至发展到了「见家长」》](https://mp.weixin.qq.com/s?__biz=MzA3NzUxMzQ5Mw==&mid=2648145785&idx=1&sn=da3844b6841bcba24a12acd44341df8f)**人机恋玩家早已不满足于聊天。

  * **[《Karpathy's Pelican》](https://twitter.com/karpathy/status/2083749667410727319)**Karpathy 花约 10 美元、1M token 预算，让 Opus 5 把《指环王》开篇生成 three.js 3D 渲染。

### 适合个人上手的教程/评测/资源：

  * **[《用 Vercel Eve 构建 AI 代码审查机器人》](https://www.youtube.com/watch?v=cmATJGbA8bI)**How I AI 频道主持人 Claire 演示用 Vercel Eve 框架构建 PR 风险评分机器人「Merge Mommy」。

  * **[《每日 UI 改进自动 PR 系统》](https://note.com/dorisukeone/n/n1a6b193c560e)**一位日本开发者用 Claude Code 搭了套每日自动改进代码机制，每天早 8 点 GitHub Actions 触发。

  * **[《代码库知识图谱化工具解析》](https://note.com/ai_arai_ally/n/n61b17529176a)**日本作者用 graphify 把自己 407 个文件、约 1800 万词的「散乱工厂」项目转成知识图谱，全程本地，token 成本为 0。

  * **[《重构经济收益：Token 消耗降 83%》](https://martinfowler.com/articles/exploring-gen-ai/refactoring-economic-benefit.html)**经过 15 步重构后，让智能体执行同一变更的输入 token 从 159,564 降到 27,360，节省 83%。

  * **[《开源活人感写作技能》](https://mp.weixin.qq.com/s?__biz=MzIyMzA5NjEyMA==&mid=2647684946&idx=1&sn=ae7edcc572b998dc4e1ac3591977aa85)**数字生命卡兹克开源了「活人感写作.skill」。

  * **[《Skill 上下文瘦身技巧》](https://mp.weixin.qq.com/s?__biz=Mzg3MTk3NzYzNw==&mid=2247509161&idx=1&sn=bd9aa077bbc46a6049ad66af6d15af0f)**作者卡尔给 Codex 和 Claude Code 里 300 多个 Skill 做了次「瘦身」，单个 Skill 可省约 89% 启动上下文。

  * **[《固定规则让 AI 输出更简洁》](https://note.com/ai_arai_ally/n/n21325e43ccfe)**日本作者发现 GitHub 周榜第二的项目 ayghri/i-have-adhd 让 AI 输出既有目的性也有下一步建议。

  * **[《ima 高配英语词典提效 5 倍》](https://mp.weixin.qq.com/s?__biz=Mzk0MDg0MTkzOA==&mid=2247503352&idx=1&sn=066b690aee3d086776a22b0279b8825c)**把 ima 当「高配英语词典」的三个用法。

  * **[《人工智能三种用法的七个案例》](https://mp.weixin.qq.com/s?__biz=Mzk0MDg0MTkzOA==&mid=2247503276&idx=1&sn=6e8a0d186d2a4043f9c6ac289bb9eaf5)**腾讯官方从 100 多份用户投稿里挑出 7 个案例，归纳出 ima × WorkBuddy 的打开方式。

  * **[《CodeX 重构我的旅行攻略》](https://mp.weixin.qq.com/s?__biz=MzAwMzc4MTQxNA==&mid=2247488727&idx=1&sn=3b3d385453fc3a1e2fa9ce246de3866e)**产品犬舍主理人纯银 uncle 用 CodeX 重构了旅行攻略工作流。

  * **[《AI 接管 80% 视频剪辑》](https://mp.weixin.qq.com/s?__biz=MzkyNzU0MzQwOQ==&mid=2247485343&idx=1&sn=8f6f78b09994c7133bcad3dcdb2bc1a9)**作者黄益贺用自制 AI Skill 接管了口播视频 80% 的剪辑。

  * **[《我用 AI 做出诗经山河图》](https://sspai.com/post/112730)**一位不会编程的作者花 20 天向 Codex 描述需求，做出可交互的《诗经》历史地图，又用 MiniMax-Music 为 305 首诗生成歌谣。太喜欢这个了，很有美感，发到了我们的 AI x 育儿社群，反应热烈。
