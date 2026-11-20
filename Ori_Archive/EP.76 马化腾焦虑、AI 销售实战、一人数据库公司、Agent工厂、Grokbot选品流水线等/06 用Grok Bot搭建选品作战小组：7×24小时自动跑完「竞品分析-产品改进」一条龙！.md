# 用Grok Bot搭建选品作战小组：7×24小时自动跑完「竞品分析-产品改进」一条龙！

> 原链: https://mp.weixin.qq.com/s?__biz=MzA3MDA3NzI1Nw==&mid=2455089892&idx=1&sn=2bf4fd31f1734c6471efb852d0edb26f  
> 来源: 公众号 · 归档自 EP.76 · 抓取于 2026-11-20  

---

Hello，大家好，我是Bulus lan

我在国庆回来后写了一篇[用Grok Bot搭建5个跨境电商数字员工，实现自动化经营（附部署教程）](https://mp.weixin.qq.com/s?__biz=MzA3MDA3NzI1Nw==&mid=2455089554&idx=1&sn=0c0ddd23850e7878731f48f2c31c4145&scene=21#wechat_redirect)，一开始阅读量还挺惨淡。

当时我还纳闷这么好用趁手的Agent怎么没人在意，没想到最近Grok Bot越来越火。

GB满足了我们跨境卖家对“数字员工”的想象：有岗位身份，能分工协作，配备一台7×24 小时不关机的云电脑，能在人类睡觉的时候持续工作。

今天这篇文章继续分享：怎么用【Grok Bot + 卖家精灵MCP】组建一个亚马逊选品作战小队，把从竞品情报到需求洞察的流程一次性跑通。

每一步都附上了要用到的提示词和Skill工具，方便大家开箱即用

![图片](https://mmbiz.qpic.cn/mmbiz_png/gKFw3mzo9hqDjNjXJwrEJia6VZwLqrsNnJAia515ic509xTT04Rb7Seucqia0FEQSJia4MLjKHret9EhoC6netHZpxLXTkQxmk4narxEeaOS6iaWs/640?wx_fmt=png&from=appmsg&tp=webp&wxfrom=5&wx_lazy=1#imgIndex=0)

先赞后看，人生灿烂！

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

欢迎跨境电商从业者来我们「[MBG跨境AI实战圈](https://mp.weixin.qq.com/s?__biz=MzA3MDA3NzI1Nw==&mid=2455088782&idx=1&sn=72cae31e67be599f3b88f91b06c3230d&scene=21#wechat_redirect)」玩耍，探索AI+商业的最佳实践和真实边界，多个跨境大卖、AI专家已在热聊中。

  


## 架构设计：1个总助+3个专业岗位Bot

很多卖家好奇这套数字员工组合到底是怎么跑起来的，其实核心就在几个Grok Bot功能的配合：

  * 云电脑负责把工作环境和分析资料沉淀在云端，关掉窗口也不丢进度

  * 不同 Bot 拥有明确分工，可以在群聊中通过消息直接交换资料

  * 挂载的 Skill 负责把业务规程固化为可复用的工作方法

  * Routine（定时任务） 则用来安排后续的定时监控




这也决定了我们这次的分工设计：只需要一个总助 Bot 来维护共用的业务背景、统一派工与交接，减少反复交代。

相当于招了个总经理助理，由他来指挥竞品情报Bot、用户反馈Bot、产品研究Bot来执行具体任务和反馈进度。

完完全全解放人类生产力！

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

### 第一段提示词：建队、配齐 Skill 与业务启动

在侧栏新建一个主控 Bot 作为总助，直接把下面这段话发给它，只需替换方括号里的产品信息：

  *   *   *   *   *   *   *   *   *   * 

    
    
    你是本项目的总助Bot，是我交代业务背景和总任务的主要入口。    
    一、你的主要职责 你负责统筹整个竞品与产品开发项目，整理背景、分派任务、检查专业工具与Skill的实际安装状态、跟进真实回执和汇总交付，不替专业岗位重做完整分析。维护同一份业务背景卡和简明任务记录。  二、当前业务背景与研究目标 1. 目标产品：美国站参考ASIN ［填写对标ASIN，如 XXX］，品类是［填写品类，如抽屉收纳盒］，它不是我的在售产品。 2. 研究目标：先研究竞品的产品组合、卖点和场景，再核查买家需求与真实痛点，汇总成果与待研究问题交由我确认；后续结合我方条件交付《产品机会与改进判断》，说明究竟是改产品、改组合、改信息表达或适配提示，还是暂不改，并附上依据、反证和验证条件。 3. 我方条件：［填写你的目标成本、现有供应链能力与工艺限制，未知的写未知］。 4. 已排除方向：［填写明确不考虑的方向，如不做大尺寸、不做木质等］。 5. 输出位置：/workspace/项目目录。  三、你要协同的三个专业岗位（在同一个群聊中推进） 1. 竞品情报Bot： - 必须安装并挂载Skill：amazon-competitor-radar（竞品狙击手Skill） - Skill完整包来源：GitHub项目 buluslan/amazon-competitor-radar - 准备要求：读取仓库入口说明，检查包是否完整、当前宿主支持的加载方式，补齐运行条件。不要只复制名称就报告已安装。 - 岗位职责：从参考ASIN出发，摸清对手的规格变体、套装配比、价格带、核心卖点与场景，输出《竞品观察表》。  2. 用户反馈Bot： - 必须安装并挂载Skill：review-analyzer-skill（评论深度分析Skill） - Skill完整包来源：GitHub项目 buluslan/review-analyzer - 准备要求：检查Python环境与数据工具依赖，结合卖家精灵MCP拉取真实留评。 - 岗位职责：按22个维度给好评和差评打标，输出《需求证据表》，明确区分评论提及、客服与退货。  3. 产品研究Bot： - 无需安装第三方分析Skill。当前等待我根据前两步成果指定具体问题并另行启动，后续由我单独发送完整分析规范。届时复用竞品情报与用户反馈两侧沉淀的证据，结合我方条件开展研究。   
    四、推进与确认规则 1. 执行顺序为：竞品研究 → 买家反馈 → 成果汇总。 2. 竞品研究与买家反馈为固定流程，由你自动接续推进；两步完成后汇总阶段成果与待研究问题交给我，由我决定何时启动产品研究及具体研究方向，不预先决定研发方向。 3. 遇到关键条件缺失、研究范围变化、新增费用或权限时，汇总向我确认。我可以直接在群里穿透追问专业Bot。  请先整理共用背景卡，检查两个专业Skill的安装与可用状态，复述团队分工和当前所需条件，等待我确认后启动第一阶段。

### 第二段提示词：接入卖家精灵 MCP

我们做市场洞察、竞品分析和选品，必须要接入市场数据，才能得出有理有据的判断结论。

还是非常推荐大家接入卖家精灵的MCP，让 Bot 具备直接调取亚马逊商品Listing、评论、品类市场数据的能力。

接入也很方便，到卖家精灵MCP上开通APIKey后，直接替换下面【APIkey】部分，发送给你的总助Bot即可。

  *   *   *   *   *   * 

    
    
    请帮我把【卖家精灵 MCP】接入到当前云电脑环境，配置如下： 服务名称：ss_mcp 传输协议：Streamable HTTP 服务地址：https://mcp.sellersprite.com/v2/mcp鉴权方式：请求头 secret-key: 【你的APIkey】接入完成后，先发起一个针对本次目标 ASIN 的只读查询，验证接口是否能够正常返回 Listing 基础信息和评论样本，确认连通后再向我汇报。

这样就大功告成啦！![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

 

## 第一步：竞品情报 Bot 拆解对手怎么卖

收到开工确认后，总助会自动唤起竞品情报 Bot，调取buluslan自研的竞品狙击手Skill：amazon-competitor-radar 

竞品狙击手 Skill 并不是简单浏览商品页面，而是把一套严谨的竞品调研规程封装成了连续动作。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

首先Bot 会从我们提供的基准 ASIN出发，通过卖家精灵MCP，反查核心搜索词，圈定真实的流量重叠池，锁定真正争夺核心搜索流量的10～20个候选竞品ASIN。

然后再从价格带分布、变体配比、卖点结构、标题词布局和生命周期阶段五个维度综合评估，最终筛选出，最值得我们去参考对标的1～2个ASIN 。

关于这个Skill的更多介绍，大家可以看之前这篇文章：[5套提示词，用WorkBuddy跑出亚马逊竞品精准狙击最佳实践（附教程/资料包）](https://mp.weixin.qq.com/s?__biz=MzA3MDA3NzI1Nw==&mid=2455089347&idx=1&sn=45b45106e94d626b622da68a7ae9b635&scene=21#wechat_redirect)

总助Bot会全程指挥竞品情报Bot，然后跟你进行汇报进展。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

在完成标准化分析后，竞品情报 Bot 会把数据沉淀为一张具体的竞品观察表。

这次我拿一个美国站的透明收纳盒套装做案例，它跑出的竞品观察表主要回答三个核心问题： 

对手到底是按什么比例配套装的？主要卖点承诺了什么？它主打哪些具体的使用场景？

表内详细拆解了 25 件套里的 4 种尺寸配比、长宽高、对应价格区间，以及五点描述里主打的浴室梳妆台、办公桌、厨房抽屉等场景。

同时理清了父子变体关系，避免把不同颜色和包装当成了多个独立对手。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

在总助把结果汇总交给你查看时，如果你想对竞品情报做更深度的核验，可以直接在群里向竞品情报 Bot 发出这段承接提示词：

  *   *   *   *   *   * 

    
    
    竞品情报Bot，请基于已生成的竞品观察表与原始页面快照，对本次竞品分析做深化核验： 1. 明确本次筛选核心对标链接的流量依据，核查父子变体关系，剔除同款重复计算的干扰； 2. 严格按单件规格尺寸、套装组合配比、每件折算价格与标称场景，拉出逐项对照矩阵； 3. 严格区分对手页面宣传的卖点承诺与实际交付推断，标注哪些属于主观宣传、哪些有明确参数支撑； 4. 评估对手打法中值得借鉴的具体动作，并逐条列出我方借鉴所需的前提条件与当前未知缺项； 5. 整理出一份附带页面来源依据的对照清单，并将需买家原声进一步核实的痛点与疑问单列交由总助。

整个找竞品到输出报告的过程，都非常丝滑，我全职只需要跟总助Bot沟通就好了。

  


## 第二步：用户反馈 Bot 验证买家怎么用

第一步的竞品情报分析工作，并没有包含具体的竞品VOC评论分析。

我一直有个观点：评论区里，蕴含着巨大的金矿！

产品Lisiting宣传得再好，买家买回去用得爽不爽，有没有槽点和可改进方向，才是真实机会所在。

接下来，总助Bot会把竞品观察表流转给用户反馈 Bot，调用bulus lan自研的VOC评论深度分析Skill：review-analyzer-skill

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

这里的分析并不是让 AI 泛读一遍评论然后写几句心得。

用户反馈 Bot 会先核对样本所属的变体版本与去重情况，按照人群、场景、功能、质量、服务、体验、市场、情感等 22 个维度对每条评论逐条打标。

随后统计不同痛点和卖点的出现频次与样本基数，再回到买家原话解释这些统计数字，形成一份结构化的需求证据表。

这样才能从最大程度上，避免AI产生的幻觉。

关于这个Skill的更多介绍，大家可以看之前这篇文章：[电商VOC深度分析Skill 2.0升级：可以一键直出专家级洞察报告了!](https://mp.weixin.qq.com/s?__biz=MzA3MDA3NzI1Nw==&mid=2455088448&idx=1&sn=4895a53e1ba56b2879f0dfe795c31ff8&scene=21#wechat_redirect)

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

很多卖家容易在这里踩坑：看到几条一星差评骂尺寸不对，就以为发现了超级痛点，冲动地想去开新模具。

针对收纳盒这个案例，打标系统很快提炼出两条针锋相对的真实原声：

正面原声：尺寸组合完美，正好塞满我的新书桌抽屉。 

负面原声：完全放不进我的梳妆台抽屉，高度太高了，根本合不上。

这时候用户反馈 Bot 必须给出客观的样本基数：在被分析的 500 条留评样本里，抱怨高度不匹配的实际只有 14 条（占比不足 3%），而夸赞容量合适、分类清晰的则有 180 条。

把两条评论放在一起看，事实非常清晰：收纳盒本身的尺寸没有变，变的是不同买家手里的抽屉环境。

这往往不是注塑质量缺陷，而是购买前的预期与实际使用环境不匹配，本质是 Listing 页面未能做好充分的适用范围提示与防退货指引。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

当你审阅完整份报告，想要进一步探索某个产品问题的真实性时，可以直接发这段承接提示词：

  *   *   *   *   *   * 

    
    
    用户反馈Bot，请基于已有留评样本与需求证据表，对本次买家原声做深度交叉核验： 1. 针对抽屉高度与尺寸不匹配问题进行回查，同时全面检索样本中对尺寸组合的正面夸赞，正反证据同步呈现； 2. 核实样本的变体覆盖、留评时间跨度与去重情况，明确每一类反馈的提及次数与有效样本分母； 3. 提取具有代表性的买家原话并注明留评位置或ID，仅记录真实买家表述，不脑补或编造具体的抽屉尺寸数值； 4. 严格辨析买家原声属性，分清真实使用缺陷、购买尺寸不符与页面预期误差，不将公开评论提及率等同于客服排障与退货率； 5. 整理输出包含“问题-使用场景-买家原话-频次分母-相反证据-已知缺口”的结构化需求证据，提交总助备查。

到这一步，在产品研究前的所有情况已经全部扒清楚了。

你会知道你想入场的这个品类，你值得对标的竞品ASIN都有哪些，他们Listing的质量如何，我们可以如何参考，评论里的买家是否满意，哪里是产品改进机会.....

如果发现当前竞品打法成熟且无明显机会，也可以在此选择暂不继续，重复这个竞品探索->评论分析的工作流循环。  


把精力留给下一个潜在品类。

  


## 第三步：产品研究 Bot 决策改动动作

产品研究是一门深厚的学问，而且我觉得产品开发上一件非常吃专业度的事情，方法也因人而异。

因此我暂时没有去做一个所谓的“产品开发Skill”，所以这一步，我更多是总结了一套产品研究的规范，帮助我们做进一步的推演。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

可以优化下提示词发给你产品研究Bot。

  *   *   *   *   *   *   *   *   *   *   *   * 

    
    
    产品研究Bot，请实际读取共用业务背景卡、竞品观察表和需求证据表，复用前两岗的证据和我方条件，按以下规范开展产品研究并交付《产品机会与改进判断报告》：  一、本次研究任务与输入核对 1. 本次研究问题/关注方向：［填写你从上游汇总中选出的具体攻坚问题，如抽屉收纳盒高度不匹配与套装配比问题］。 2. 上游资料实际位置：［填写竞品观察表、需求证据表与原始快照的存储路径，如 /workspace/项目目录］。 3. 我方条件更新：［填写本次是否有更新的目标成本、模具底线或供应链限制；若无变化直接复用共用背景卡］。 4. 依据核对：实际读取上游沉淀的证据，交叉核对数据与买家原话，未知项保持未知，不脑补条件；不重复全网选品，也不重复爬取评论。  二、研究与分析规范 1. 辨析真伪需求：区分真实使用需求、产品质量缺陷、购买不匹配和预期误差，绝不把单条差评直接翻译成新功能。 2. 核对现有供给：回查竞品各变体、关联型号及同类成熟产品，核实该痛点是否已被其他产品解决；未查到供给不等于市场空白。 3. 动作四选一决策：针对每个核心问题，在【改产品】、【改组合】、【改信息表达与适配提示】、【暂不改】四类动作中权衡取舍，必须明确写出为什么选择该动作、为什么排除其他三类。 4. 反证与代价推演：检索相反买家反馈与替代方案，结合我方供应链限制，测算潜在新增成本与副作用。  三、成果交付格式 请输出结构化的《产品机会与改进判断报告》，每项判断写清： - 人群与使用场景 - 具体痛点与现有供给对照 - 动作类别与改进假设 - 正反两方面证据 - 我方条件匹配度与新增代价 - 下一步验证清单（具体验证动作、资料/样品需求、继续与放弃条件）  先整理分析逻辑，等待我审核确认；未获授权不推导最终采购与开模。

针对收纳盒的高度问题，产品研究 Bot 结合我们在背景卡里填写的模具成本限制，做出了冷静的权衡：

不建议为了迎合少数矮抽屉差评，去单独开模做超矮款。

美国家庭抽屉内高普遍在两寸半到三寸之间，现有尺寸能覆盖绝大多数场景

一旦把高度压得过扁，单盒容积缩水会丧失实用价值，还会增加开模与备货负担。

当前最推荐的动作是改信息表达：在主图补充一张抽屉深度测算与场景对照指南，把买错预期的买家在下单前劝退。

至于改组合（比如调整不同尺寸盒子的套装配比），它与高度问题不同，是我们后续可以探索的产品优化方向。

而且我还让每个Bot相互讨论了两轮，交叉验证了一下。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

如果说，大家跑出来了一些潜在新品方向，还可以继续做一个【1688盘品Bot】，让他去帮你到1688上找供应链，哈哈哈。

这个Bot的模版我放在我之前的做的Grok Bot模版库里面的了，大家可以自己去搜。

指路：mbgai.vip/bots

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

到这里，单次研究就全部闭环了。

这次的真实案例跑下来，几个Bot给我的最终结论，其实并不是让我做新品研发，而是告诉我如果要做类似的产品，可能更需要注意产品特点和Listing表达的一致性。

我觉得，也挺真实的。

  


## 第四步：用Routine（定时任务）建立盯盘哨兵

单次分析做完了，以往大家往往就把文档丢进文件夹吃灰。

但电商竞争是动态的，对手下个月可能就改了价格或配件。

这时候，我们可以让竞品情报 Bot 挂上Routine定时任务。

所谓最小 Routine，就是坚决不要让 AI 每天去重新跑全网选品，那纯粹是在空耗 token。

最小监控必须极其克制： 针对我们确认的这几个核心 ASIN，设定每周固定时段自动通过卖家精灵MCP/网页采集获取最新信息、数据。

建议看三个核心字段：价格是否有超过 10% 的变动、主图和五点描述是否有新增功能或尺寸声明、在售变体组合是否有增减。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

发给竞品情报 Bot 的监控提示词非常简单：

  *   *   *   *   *   *   * 

    
    
    请为基准 ASIN ［填写目标ASIN］ 设定最小 Routine 监控方案： 每周二上午 10 点检查一次。 调用卖家精灵MCP，只监控三个核心字段：价格是否有超过 10% 的变动、主图和五点描述是否有新增功能或尺寸声明、在售变体组合是否有增减。  若无变动，记录简要日志，不要打扰我； 若检测到实际变化，将新旧快照与差异点整理成简报发到群聊： -若此前已输出产品研究结论，由总助转交产品研究 Bot 评估该变化对既有结论的影响； -若此前尚未启动产品研究，先提醒我关注变动，由我决定是否开展专项研究。

Grok Bot会在右侧动态这里生成定时任务，我们也可以随时关闭。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

一套流程下来，你在云端拥有的不是一个冷冰冰的问答框，而是一个 7×24 小时替你站岗的竞品情报哨兵。

  


## 写在最后

从竞品拆解、买家原声提炼，到产品动作的权衡与自动化盯盘，AI 从来不是替代我们的思考，而是把繁琐的手工活沉淀为标准的工作流。

把业务想清楚，把岗位边界定好，把判断权收在自己手里，这才是使用 Agent 真正舒服的状态。

上面分享的完整提示词、背景卡规范和配置细节，我都整理在配套资料里了，新手小白也能按照我的流程一步步配置好。

大家还想了解Grok Bot哪些玩法和实践？欢迎评论交流，下次选题内容或许就是为你定制的工作流！

* * *

欢迎跨境电商从业者来我们「[MBG 跨境AI实战圈](https://mp.weixin.qq.com/s?__biz=MzA3MDA3NzI1Nw==&mid=2455088782&idx=1&sn=72cae31e67be599f3b88f91b06c3230d&scene=21#wechat_redirect)」玩耍，探索AI+商业的最佳实践和真实边界，多个跨境大卖、AI专家已在热聊中

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)
