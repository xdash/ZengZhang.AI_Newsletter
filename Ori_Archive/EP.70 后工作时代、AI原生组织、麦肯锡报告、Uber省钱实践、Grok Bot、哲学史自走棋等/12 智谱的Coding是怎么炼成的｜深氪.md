# 智谱的Coding是怎么炼成的｜深氪

> 原链: https://mp.weixin.qq.com/s?__biz=MzkwMDQ2NDU2Nw==&mid=2247518056&idx=1&sn=d3842dad7d317bdded408d05127ff686  
> 来源: mp.weixin.qq.com · 归档自 EP.70 · 抓取于 2026-09-17  

---

![图片](https://mmbiz.qpic.cn/sz_mmbiz_jpg/q1LBRhFZOGOwnk81Ks9EwicVAnD1OKxicGZaJqmbqpNZJscddI7qVwpzKibzSwjOWPtFocxNjicV72RKbZWgRicwLZy5EiaMWcO9zMcDYtLibQwicQY/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1#imgIndex=0)![图片](https://mmbiz.qpic.cn/sz_mmbiz_png/q1LBRhFZOGM0hXA55PZA6Sj4rRGYrWbNy4MW2VRHHdnBaJDTJayfq2wibr7NTlWvUI9KlYwaVFwZuTicKaHaXhUwbuZFAXvibjkFkkDO9Mdx70/640?wx_fmt=png&from=appmsg&tp=webp&wxfrom=5&wx_lazy=1#imgIndex=1)文｜周鑫雨 张雨忻编辑｜张雨忻 杨轩

GLM 5.3发布后不到一小时，智谱一名销售的电话和微信都爆了：十几个来询问API上线时间的，以及吸取了Kimi K3教训，想提前锁定智谱推理算力的客户也不少。这种状况一直持续了整个周末。

8月14日下午，智谱突然发布了新一代模型，在测评榜单上再次刷新国产模型的Coding表现，与不久前发布的Kimi K3并列开源第一，与Claude Fable 5、GPT-5.6 Sol等闭源旗舰模型处于同一水平。这瞬间引爆了客户们的热情。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

△来源：智谱公众号

周末过去，消息和电话并没有停——原定8月18日要上线的GLM 5.3 API推迟了，销售再一次被客户“围攻”。“客户在电话里对我喊：内部预算和开发运维都到位了，delay一天我们的管理成本就多好几万！”

上述销售回忆，如此这般的“API哄抢”大概是从2026年2月开始的——这是智谱发布大版本更新模型GLM 5的时间，当时多家外媒都评价其“第一次真正把中国开源模型推到全球前沿模型附近”。在那以后的GLM 5.1来到全球第一模型梯队，GLM 5.2拿到全球开源模型SOTA（最佳）。可以说，每一个版本都在显著提升。

这期间，越来越多人开始问，这些模型背后的智谱，是一家怎样的公司？

其实，在中国2023年开始兴起的大模型浪潮中，智谱原本是一个“不够主流叙事”的存在：

它不够年轻——2019年就已经成立，在推崇“小天才”的气氛下看起来不够酷；

它不够“公司化”——几乎完全脱胎于清华，带着鲜明的学院派和实验室气质；

它的商业化路径看起来不够性感——长期给政企客户做模型私有化部署，不是互联网的“可复制、规模化”逻辑。

但是，如果你是近一年才关注到这家公司，对它的认知大概率会是：全球大模型第一股，最高曾摸到1.3万亿港元市值，堪比好几个美团；拥有开源SOTA的模型，口碑全球出圈；ARR（年度经常性收入）目前在中国模型厂里位列第一......

这种大转变的核心，就在模型的Coding能力上——当全球大模型都沉浸在Anthropic带来的Coding狂欢中时，智谱是中国最早拿到Coding门票的大模型公司，靠着足够好的Coding模型迎来口碑爆发和收入激增，并且一定程度上推高了过去半年国内大语言模型的竞争烈度。

智谱做了什么？率先拿到Coding门票的，为什么会是智谱？

要解答这些问题，需要先回到2025年5月，“智谱押中Coding”的前两个月。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

## 背水一战，和意外的Coding爆发

2025年5月，智谱紧急召开了一次战略会。“只有核心高管和少数股东参与了，核心议题之一是，智谱下一阶段的模型要往哪个方向走。”一位知情者告诉36氪。

这个议题，在那个时间点几乎决定了智谱的接下来的命运。

一方面，**在2025年春节横空出世的DeepSeek R1几乎一刀悬在了智谱的商业化大动脉上。** 这个性能比肩OpenAI o1，但价格只有o1 1/30的模型，冲击了当时整个B端市场，而面向B端做定制化模型部署是智谱当时最重要的商业化方向。

一位智谱做商业交付的员工告诉36氪，他就没能过个好年：“一天接5、6个客户的电话，但大部分是来问能不能部署DeepSeek的。”他心里有些五味杂陈，“DeepSeek一夜之间全民知晓，不少客户的老板都交代下面的人改用DeepSeek。”另有智谱员工告诉36氪，“保守估计，当时智谱近30%的客户流向了DeepSeek，对公司打击很大。”他提到，为了留住客户，智谱给一些客户开出了非常低的折扣。

而另一方面，国内的大模型市场也在悄然转向。Chatbot的热度褪去，当时与智谱同为“六小虎”成员的月之暗面、MiniMax都在押注以调用工具、执行复杂任务能力见长的旗舰模型。

**面对危机和变化，智谱的这次战略会做出了一个扭转命运的决定：****改变原****本针对****文本、多模态****、编程等****能力****各自做垂直模型的路线****，押注****Reasoning（推理）、****Coding****（编程）、Agentic（智能体）三类数据融合的大参数、三合一模型。**

智谱意识到，必须走出舒适区，寻找属于下一阶段的新机会，而新机会只会从效果足够好的、能解决更复杂的生产力需求的大模型里长出来。

这个决定对智谱来说并不容易。“不少股东都反对继续scale up模型（即推高模型参数），因为投入太高了。”一位知情者告诉36氪。智谱的财务压力一直都不小——2025年财报显示，智谱净亏损高达47.18亿元，仅研发一项就花费了31.82亿元，是当年总营收的4倍。

另一个原因则在于，**多数据融合的模型，与智谱****走****B端定制****的****商业模式****天然****相悖。** 一名智谱B端业务人士告诉我们，为了匹配客户的具体业务场景，智谱此前将模型能力做了很清晰的垂直场景划分——对话、生图、生视频、Coding等各有对应的模型和产品。若用一个融合模型匹配所有场景，那么部署成本会变得非常高。

**这个“三合一”模型，就是在2025年7月上线的GLM 4.5** 。“原本4月就要上线的，但因为临时调整了模型方向，硬生生拖到了7月。”一位知情人士告诉36氪。

这是智谱的背水一战。为了训练“三合一”的模型，**智谱准备了15万亿Token的通用数据，以及8万亿Token的Coding、Reasoning和Agentic数据，总训练数据量几乎是同期模型的1.5倍** 。

焦虑几乎弥漫在所有人身上。多位智谱员工告诉36氪，GLM 4.5发布前的几个月，AI院（智谱的技术和产研部门）的所有算法几乎住在公司，“4.5发布那天，我凌晨下班，早上上班的时候，算法那边坐的整整齐齐，和昨晚我走的时候几乎一模一样。”还有市场侧员工在发布日通宵到早上8点，“太焦虑了，不知道GLM 4.5的市场反响会怎么样。”

后来的故事人尽皆知：**GLM 4.5成为了智谱第一个在Coding上收获口碑的大模型，也让智谱成了国内最早押中Coding赛道的大模型公司之一。它真的帮智谱找到了属于下一竞争阶段的新机会——Coding。**

其实在国内，不少大模型公司在2024年6月Claude 3.5 Sonnet发布时就已经关注到了Coding的苗头，但却没敢入局。

**MiniMax创始人闫俊杰两年前就曾问过DeepSeek创始人梁文锋：“你们要不要做AI Coding。”梁给出了否定的答案。** “当时大家的共识是，全中国会写代码的人可能只有100-200万，这似乎不是一个足够大的市场。”闫俊杰在一场活动上回忆道。但他们没想到的是，当AI Coding成为改变生产方式的变量，200万人的市场也可以变成2000万人。

不过，智谱的率先押中，也并非是“一切尽在计划中”。

一名智谱员工告诉我们，“三合一”刚开始训的时候，Reasoning、Coding和Agentic之间的优先级没有明显差别，**模型最终聚焦到Coding上，一个直接的诱因是，用户的选择。**

据36氪了解，研发过程中团队内部反复讨论提到，模型要贴近用户的真实需求，不要围着榜单来，模型真正的能力需要在真实任务中得到验证。所以算法团队会频繁参考用户/客户反馈，了解他们的需求点。其中，**“提高研发效率”，是一个被高频提及的需求。** 而恰好，这也与管理层所强调的“追求更高智能上限”方向一致。

GLM 4.5发布后，一位销售记得，当时不断有KA客户提需求，将GLM 4.5接入程序员的工作流。社交媒体上，“Claude平替”的声音也开始出现——毕竟，GLM 4.5的Coding能力逼近Claude Sonnet 4，价格却只要后者的1/7。

**Coding成了GLM 4.5市场反响最好的能力** 。2025年9月，智谱推出了“GLM Coding Plan”，**成为国内第一个推出Coding Plan的大模型公司** 。10月，“GLM Coding Plan企业版”上线，同月推出的新模型GLM 4.6，据官方说法，特别强化了Coding能力。

**到这里，智谱的新故事线逐渐清晰——在又重又难以复制的B端模型部署生意之外，抓住了能规模化、且商业价值较高的Coding生意。**

“Chatbot的故事，从DeepSeek出来后，就已经结束了。我们应该思考的是下一个bet是什么。”在2025年初的一场活动上，智谱创始人唐杰曾提到。现在回头看，这个bet就是Coding。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

## GLM 5.2和万亿市值

智谱今年1月在香港挂牌上市、成为“全球大模型第一股”这天，CEO张鹏给每位员工发了200元的红包。但这份喜悦只维持了一天——一天后，MiniMax上市，股价首日暴涨109%，市值突破千亿元，几乎是智谱的两倍。

当两家基因完全不同的大模型公司被同一时间放到公开市场上被审视，智谱在市值上暂时落了下风。“在国内，当时MiniMax聚焦的C端市场被认为有更大的想象力，被贴上toB、toG标签的智谱看上去就没那么性感。”一名大模型投资人对36氪说。

**但仅过了5个月，智谱用一个开源的SOTA模型再次扭转局势，而这一次，比GLM 4.5那次更为彻底：收入、口碑、股价，迎来全面爆发。**

2026年6月13日，智谱发布了新一代旗舰模型GLM 5.2 。这个依旧以Coding为最主要能力的模型在Artificial Analysis综合榜单上位列开源模型SOTA，仅次于闭源的Claude Fable 5、Claude Opus 4.8（max），以及GPT 5.5（xhigh）。

用户的钱包是最诚实的。**GLM 5.2让智谱的API收入快速攀升。**

智谱股东告诉36氪，2026年5月，智谱的ARR还在5-6亿美元左右，对年底ARR的预期为10-15亿美元。而在GLM 5.2发布后一个月，36氪再度独家获悉，**7月智谱的ARR已飙升至10亿美元，相较2个月前几乎翻倍，而年底的ARR预期也提升至25亿美元。** 针对这一数据，智谱暂无回应。

能够从销售第三方模型里获得分成的云厂商们也快速捕捉到了GLM 5.2带来的机会。一名智谱人士告诉36氪，阿里云、火山引擎、甚至小米和金山云，“推销GLM 5.2比智谱自己都狠”，因为“客户都是来问GLM 5.2的”。阿里云一名销售也证实了这件事：由于下游需求太旺盛，到了7月，阿里云“直接给客户推GLM 5.2”。

**智谱迎来了自己的“DeepSeek时刻”。**

不仅国内，海外影响力也因GLM 5.2被快速打开。云端部署与托管平台Vercel的监测显示，**GLM 5.2调用量的增长速度是2026年以来所有模型中最快的，超过了4月发布的DeepSeek V4。**

“智谱没多少营销预算，我们的做法就是免费给潜在KA和KOL early access（试用名额），让他们直观感受模型能力。”一位销售告诉36氪。另有市场推广业人士告诉我们，**在GLM 5.2发布前，智谱的中高层一有机会就飞去海外见KA客户和科技KOL，邀请他们参与内测。** “当时不少海外客户用过之后发现，GLM 5.2的综合能力超过了DeepSeek V4，海外口碑就是这么逆转的。”

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

△GLM 5.2发布后，智谱总部搜狐网络大厦外墙的LOGO，从汉字“智谱”，换成了“Z”。图源：作者拍摄

股价也飞升了。

**GLM 5.2发布后的第一个交易日，智谱股价大涨32%，并在一周后，达成万亿市值。** 在这个时间点下，智谱的市值大约是2.5个美团，和3.5个京东。

回溯到年初股价节节攀升的时期，智谱在商业化上就做了一个决定：**大幅提升MaaS业务的优先级。实际上，****不少股东都认为，****智谱****原有****的（B端）****定制****化生意****，撑不起****太高的市值****。**

一方面，定制化业务没有规模效应，想接更多单子，就必须加更多人。**据一位智谱员工的测算，B端业绩每年稳定在1.5倍的增长幅度——稳健，但天花板就在那。** 并且，每一笔订单都是高度非标的。“有时候为了尽快拿到验收单，我们工作之余还要付出很多额外的情绪和体力劳动：替客户开会，帮他们制作汇报PPT，甚至帮他们接孩子......说白了，就是要付出大量人力把客户服务好。”

另一方面，现在模型的迭代速度太快，可能一个模型在开始部署时还是行业内最领先，但花几个月部署完之后已经被别的模型远远超过。越来越多客户也认为购买MaaS服务是更灵活的方式。

其实早在2021年，智谱内部就讨论过未来的商业模式，当时内部已经认为，应该对标（彼时的）OpenAI，把重点放在API调用收费上。但由于当时国内MaaS市场太早期，也没有真正能打的模型，所以没有条件推下去。

5年后的现在，张鹏选择把对标对象明确为了Anthropic。但对比Anthropic来看，智谱的MaaS业务还有巨大的收入鸿沟需要填补。根据最新的公开数据，智谱的市销率高达Anthropic的5倍多。**基于Anthropic的市销率，智谱的市值若想稳定在万亿港元，ARR要达到487.8亿港元，约62.2亿美元。** 而当下，智谱的ARR刚刚达到10亿美元。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

## 取舍的胜利，“不犯错”的胜利

“为什么是智谱？”当智谱用GLM 4.5踢开Coding的大门，并以GLM 5.2一飞冲天后，不少人开始问出这个问题。

36氪也向多位智谱员工抛出了这个问题，得到的答案几乎一致：**克制地聚焦、没犯错、****每一步****基本****做对****了** ——“把每一步都做对，模型几乎不可能差”这个结论，在字节的Seedance的成功上也被验证过。

这些看起来偏“稳健”的风格和做法，与智谱这家公司的基因息息相关。回溯智谱在一些关键时刻做过的对的选择，有一个因素非常重要，那就是——尊重自己的基因。

**张鹏曾这样评价智谱：“就像清华的理工男一样，很聪明****、****很能干，你让他干什么事情，他能干得很漂亮，但是就是没有太多的情绪价值。”这符合一直以来外界对智谱的印象：有技术、有视野，但看起来不够有趣，不够性感。**

而张鹏关于智谱“没有太多情绪价值”的评价，与智谱的模型和产品之间，形成了有趣的互文。

2024年，智谱曾与一家硬件厂商合作，将GLM接入产品。当时，智谱拿出了GLM“情商最高的系列”。但在内部测评中，当员工输入“我的心情有点down”时，接入了GLM的产品的回复竟是：“打开空调”。

张鹏曾在媒体访谈中提到：“（杨）植麟（月之暗面创始人）知道怎么去理解普通人的需求和想法，我们在这方面可能做得没有那么好，这跟我们的定位有关系。”智谱在这方面的弱势，使它**在toC产品上存在短板。**

两个典型案例是Chatbot“智谱清言”和视频生成模型“智谱清影”。根据“AI产品榜”数据，截至2025年3月，Chatbot大战约一年半后，智谱清言App端月活为1043万；同时期，豆包的月活是9736万。而“清影”的销售情况则可以用“惨淡”来形容，一位智谱销售告诉我们，“客户大多是从事艺术领域工作的，看不上清影的审美。”

不擅长聊天、不擅长视觉类审美这样的市场反馈，并没有让智谱失去战斗力。相反，**意识到自己的短板后，智谱****果断将资源****从这些方向上撤出，****聚焦****到了****自己擅长的方向****上****。****“智谱是一个非常理工科气质的公司，Coding就是最适合他们的方向。”一位业内人士评价。**

目前，**在智谱AI院中，负责多模态模型训练的算法降缩减10人左右；而聚焦文本、Coding方向的算法则有百人。** 一名知情人士透露，**智谱****有较高的预算做****Coding、Agentic****的RL环境搭建和数据工程。**

在当下算力资源、模型容量、模型数据量等现实掣肘下，模型厂商们都不可避免地要做选择题，为不同的模型能力排优先级。**如果既要又要，可能导致哪方能力面都不够突出的结果。**

“模型每一种后训练目标都会占用其他目标的能力。把提升Coding能力作为训练目标，意味着训练数据要少废话、高精度，这和正常人之间带有情感的交流是相悖的。”智谱一名前算法员工举了个例子：GPT-5和DeepSeek V4发布时，都因为提升了Coding和Reasoning能力，而被用户评价“情商变低”。

还有一个例子是MiniMax。模型M3发布后，一名参与训练的算法反思，M3各项能力都不突出，就在于训练目标没有收敛：“MiniMax的优势业务都是toC的，虽然老板们知道Coding和Agentic重要，但也放不下模型的情商优化工程。”最后的结果就是，M3发布后行业反响平平。

**不过近期，36氪独家获悉MiniMax在6月底解散了后训练团队中的“泛娱乐组”，将人力和资源投入到了Reasoning和办公场景。**

**做对方向的取舍之后，在接下来模型训练的每一个关键环节中，智谱也基本做到了“不犯错”。****一个核心原因在于，智谱搭建了精细的A/B Test体系。** 一名智谱员工告诉我们，“遇到关键技术选型时，智谱会分两三波人马做A/B Test，每个测试组放两三个研究员，就像实验室一样。”

另有员工提到，**智谱将训练阶段和训练路线拆得很细致，一旦无法确定技术选型，算法就会将每一条路线下的训练结果去测试集上跑一跑，择优而取。**

另一个不犯错的原因，则来源于“经验”。早在2021年，唐杰就主导了智源研究院发起的万亿参数大模型“悟道2.0”的训练。在一众大模型公司的创始人中，做过这个参数量模型的只有唐杰和杨植麟。

**经验带给智谱的，是对数据****和后训练****的重视** 。目前业界的共识是，提升Coding能力的关键，是做好SFT（监督微调）和Agentic RL（基于Agent任务环境做强化学习）。在这两个后训练环节，“**至少对于一些前端任务，数据的作用比算法大。** ”一位大模型行业人士判断。

然而，制定数据策略有相当高的经验壁垒。“用哪些query去问，基于哪些task跑，合成的数据用来做SFT还是RL，是用来生成训练的模拟环境，还是直接用于训练，这些决策都离不开经验。”一名MiniMax算法告诉我们，M3发布后，MiniMax内部开了场反思会，内部得出的一个结论就是：数据策略没做好。

早在2024年，智谱就在海外投入了一个团队，从事数据的采购。**在内部，****负责模型训练和数据的****张笑涵主导搭建了一个数据标注平台，名为“狂标”。在语言模型和多模态模型****两个组****轮训期间，待训组的核心任务，就是标数据。**

**另外，自GLM 4.5起，算法团队开始愈发重视下游客户的反馈。** 一位智谱员工记得，AI院常常与销售和交付团队的负责人们开会，从而收集KA客户的反馈。**模型发版前，内部****会设置****两道测评** ：一道在AI院，做通用能力测试；另一道则在交付团队，基于目标用户高频场景做测评。“所以，GLM的Coding能力在开发者群体中口碑很好。”

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

## 人才壁垒：师门下的组织

这套“不犯错”的体系背后，是智谱AI院的数百名算法人员。“**智谱的算法用钱挖不动** 。”一名从事高招的猎头告诉36氪，“有大厂愿意开数千万元薪资包挖智谱AI院的核心算法，但最后以失败告终。”

一方面，智谱的核心算法确实很贵——公司市值快速攀升，核心算法手里的期权都值十几亿了。但更重要的原因是，**智谱与它的核心人才之间形成了一种金钱之外的深度关系，这是其它大模型公司难以复制的。**

这种关系是怎么建立的？

在国内一众大模型公司里，智谱是一个鲜明的存在：从创始人到各个岗位上的核心成员，几乎都来自清华，其中不乏大量同门和师生关系。很多行业人士在提到智谱的组织时都会提到几个词：学院派、清华系、唐杰和他的门徒......

“它是一个公司、学校、研究院的结合体”，一名投资人如此评价智谱。

作为以模型训练为核心的组织，这个组织绕不开的人物，是它的创始人兼首席科学家唐杰。作为清华计算机系教授，唐杰是中国最早做机器学习、NLP（自然语言处理）的学者之一。多位投资人和FA评价，当他们在2022年底找对标OpenAI的标的时，脑海中最先跳出的清华学者是：唐杰、孙茂松、黄民烈。

在不少智谱员工看来，“唐杰热情、有信服力、执行力也强”，但同时对待技术和业务又要求极高。一名智谱AI院的算法记得，智谱Agent产品AutoGLM 2.0的训练结果不理想，唐杰直接推迟了上线时间。

这家公司的核心团队带有强烈的清华系人际羁绊。负责商业化的CEO张鹏，清华本、硕、博出身，与唐杰同属计算机系；负责政府关系的智谱总裁王绍兰和董事长刘德兵，也都毕业于清华，与创始团队在清华数据科学研究院大数据研究中心共事过。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

△智谱港交所挂牌上市当天，张鹏（左二）、王绍兰（左一）、刘德兵（发言者）等智谱核心成员到场。图源：智谱

而智谱的心脏——负责模型训练的AI院，**数百位位研究员中****70%以上都是清华计算机系的本科生、硕士生或博士生** 。

**庞大清华师生构成的智谱形成了一个相对稳固的算法组织，被师门关系所包裹，“学院”文化鲜明。**

学院文化一方面体现在工作方式上：**AI院层级扁平，比起公司，更像一个实验室** 。据智谱员工，很多关键方向都是从一个技术问题或一次实验结果的讨论开始的，不同背景的研究人员会很自然地参与进来。对年轻研究员来说，有比较大的空间来提出问题、验证想法。

并且，不少学生都表示，出于对自己老师、学长的尊重和情感，不会轻易选择离开。“想在唐老师门下读硕士博士的学生里，有一些也会选择先来智谱工作。”一位前智谱算法告诉我们。

**源源不断的人才供给，加上较低的流失率，智谱的算法人才壁垒就这样形成。** 据36氪了解，GLM 5发布后，有智谱的算法实习生一天之内就收到近10通猎头的电话；字节的猎头曾对着GLM论文上的署名，一个个打电话；腾讯混元愿意开两倍的底薪，去挖一个智谱的硕士。而以上种种，成功率都不高。

大模型公司之间的竞争，只会越来越激烈。

8月19日，唐杰在X上发帖，阐述他对Scaling Law的理解：模型能力已经不再单纯由参数量决定，它更像是一个控制变量的实验，而变量包括“用了多少数据”、“准备把算力花在哪里”、“模型最终由谁、在什么条件下运行”等。这个论述指向GLM 5.3相较于上一代，实际是在后训练环节下功夫，而非卷预训练参数。

而大比例推高模型参数的几乎是剩下的所有头部大模型。过去一个月，月之暗面、DeepSeek、阿里都相继发布了新版旗舰模型，参数在1.6亿-2.8亿之间，是GLM 5.3的2-4倍。其中，月之暗面在7月17日发布的K3，取代了GLM 5.2维持了一个月的开源SOTA之位；而仅过了20多天，智谱又用GLM 5.3再次夺回。

模型方向、训练路线、数据质量、算法人才......围绕大模型各个维度的争论和竞速，远没有到可以分出胜负的时候。

（36氪作者邓咏仪、李炤峰对本文亦有贡献）

图片来源｜********企业供图、作者拍摄、 电影《黑客帝国》********

  


![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)[![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)](https://mp.weixin.qq.com/s?__biz=MzkwMDQ2NDU2Nw==&mid=2247517958&idx=1&sn=9a0c17af364ee245d20bbb7d2d1c7721&scene=21#wechat_redirect)[![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)](https://mp.weixin.qq.com/s?__biz=MzkwMDQ2NDU2Nw==&mid=2247517949&idx=1&sn=e828ca8ee154dc74762f734a00b46197&scene=21#wechat_redirect)![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)
