# 如何评价Karpathy提出的个人知识库的架构？

> 原链: https://www.zhihu.com/question/2024197832765128929  
> 来源: www.zhihu.com · 归档自 EP.51 · 抓取于 2026-08-05  

---

[知识库](//www.zhihu.com/topic/19553061)

[构建知识框架](//www.zhihu.com/topic/23581813)

[个人知识库](//www.zhihu.com/topic/27865119)

# 如何评价Karpathy提出的个人知识库的架构？

Andrej Karpathy再一次发表了高热度推文，他描述了一个依靠LLM打造个人知识库的系统架构。这篇推文阅读量高达1700万，而后他又补充了一条…显示全部 ​

关注者

**1,642**

被浏览

**295,997**

关注问题​写回答

​邀请回答

​好问题 41

​3 条评论

​分享

​

#### 118 个回答

默认排序

[![程墨Morgan](https://picx.zhimg.com/v2-50aea4b87aeed8dd361b39ec3e3a2c33_l.jpg?source=1def8aca)](//www.zhihu.com/people/morgancheng)

[程墨Morgan](//www.zhihu.com/people/morgancheng)

[​![](https://pica.zhimg.com/v2-4a07bc69c4bb04444721f35b32125c75_l.png?source=32738c0c)](https://zhuanlan.zhihu.com/p/344234033)

新知答主

​ 关注

[收录于 · 进击的人工智能](https://www.zhihu.com/column/c_1801290451342454787)

航海家 温戈 等 771 人赞同

[Karpathy](https://zhida.zhihu.com/search?content_id=776253192&content_type=Answer&match_order=1&q=Karpathy&zhida_source=entity)发了条长推，说他最近搞了个『[LLM Knowledge Base](https://zhida.zhihu.com/search?content_id=776253192&content_type=Answer&match_order=1&q=LLM+Knowledge+Base&zhida_source=entity)』，用来管理自己的研究资料。

核心思路其实一句话就能讲清楚：**别用[向量数据库](https://zhida.zhihu.com/search?content_id=776253192&content_type=Answer&match_order=1&q=%E5%90%91%E9%87%8F%E6%95%B0%E6%8D%AE%E5%BA%93&zhida_source=entity)了，让LLM直接读Markdown文件，而且让LLM自己维护这些文件。**

![](https://pica.zhimg.com/50/v2-de6ea9805749bc4d730f150a311d4378_720w.jpg?source=1def8aca)

![](https://pica.zhimg.com/80/v2-de6ea9805749bc4d730f150a311d4378_1440w.webp?source=1def8aca)

就这点东西吗？

真的就这些，但是，Devils are in details，细节中挺多可圈可点之处。

* * *

传统知识库管理都用RAG，RAG大家应该都熟——把文档切成碎片，转成向量(embedding)，存进向量数据库，查的时候做相似度搜索，结果用LLM来整合。

这套架构在企业级场景里曾经被吹上了天，但Karpathy觉得，对于个人研究者来说，这玩意儿纯属杀鸡用牛刀。

他的方案分三步走：

**第一步，喂料：** 把论文、代码仓库、网页文章统统扔进一个`raw/`目录（这个目录名不重要，只不过Karpathy用的是raw)，这个过程中保证raw里的文本都是markdown文本，为了达到这个目的，Karpathy用Obsidian的[Web Clipper](https://zhida.zhihu.com/search?content_id=776253192&content_type=Answer&match_order=1&q=Web+Clipper&zhida_source=entity)工具把网页下载转成Markdown，连图片都下载本地化存储。

**第二步，编译：** 这是核心，LLM上场了，对raw中的文件进行编译和索引，把第一步获得的markdown编撰成一个结构化的wiki，生成摘要，识别关键概念，撰写百科式词条，当然也要建立反向链接，把相关概念串起来——**这就是人工可以做，但是AI做的更快的苦力活** 。

**第三步，体检：** LLM定期对整个wiki做检查，修补前后矛盾的地方，补充缺失的信息，也就是打造一个**会自我修复的活的知识库** 。

打个比方，就是Karpathy请了一个AI图书管理员，这个管理员不只负责上架图书，还会自己写新书来解释旧书之间的关系，隔三差五还巡查一遍书架，把放错位置的书归位。

你可能会问——这和我往Obsidian里丢一堆笔记有什么区别？

区别大了。

你看我的Obsidian，最大的目录就是Knowledge，看到什么新知识，我就在Knowledge里建一个markdown文件，现在都积累上千个markdown文件了，但是这些markdown就是一个信息孤岛，如果我主动去编辑，就没有关联。

![](https://picx.zhimg.com/50/v2-0997f6e53a1afd42d151bdd65dc87fe4_720w.jpg?source=1def8aca)

![](data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='1282' height='1206'></svg>)

当我需要获得历史上所有某个主题的知识时，我只能用搜索，但是搜索出来的内容非常多，而且碎片化，我还要动脑子去总结，比如我要搜agent相关知识，得到一大堆笔记，还要我现场去过滤。

![](https://picx.zhimg.com/50/v2-fdf22801d7882653be3ea600d201c755_720w.jpg?source=1def8aca)

![](data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='1284' height='1404'></svg>)

总之，Obsidian天生是死的，要人去主动操作才能盘活。

而Karpathy的个人知识库天生是活的，每一次加入新增资料，都会被LLM整合进现有的知识网络，知识在这里是复利增长的。

而且，他选markdown不选向量数据库，有个非常实际的好处，**每一条AI给出的结论都能追溯到具体的`.md`文件**，不像RAG那样，你问AI一个问题，它从黑盒里捞出几个向量碎片拼成答案，你根本不知道它为什么这么说。

Karpathy的方案里，所有证据链都是明文可读的，当然Obsidian创始人Steph Ango对此大加赞赏，可以理解，毕竟Karpathy等于给他们做了广告。

* * *

我个人认为，Karpathy这套用来搞『个人』知识库没问题，但是作为『团体』知识库，行不通。

首先是体量问题，Karpathy自己也承认，这套系统的适用规模是大约100篇文章40万字，超出这个量级，靠`index.md`和[grep](https://zhida.zhihu.com/search?content_id=776253192&content_type=Answer&match_order=1&q=grep&zhida_source=entity)搜索就开始力不从心了，当然，这些技术问题都不是大问题，利用层级管理，就可以支持更大体量的内容。

相比于体量问题，更大的问题是，**这套方法对使用者的判断力和自律性要求极高** 。

Karpathy能玩得转，是因为他是Karpathy啊，他Karpathy什么人，头脑很清楚，知道哪些资料值得喂给LLM，知道LLM编译出来的东西哪些靠谱哪些扯淡，知道什么时候该手动介入纠偏。

但是，如果使用者判断力没那么强，自律性没那么高，以为架起一个系统就无脑接受一切了，肯定要翻车。

你把这套东西交给一个团队试试？

我们都知道，团队会让能力广度增加，但是深度下降。

我最近就接触过一个团队，他们全面拥抱[AI Coding](https://zhida.zhihu.com/search?content_id=776253192&content_type=Answer&match_order=1&q=AI+Coding&zhida_source=entity)之后，连续线上出大bug，解决得也手忙脚乱。

原来，团队感受到AI Coding爽之后，代码和文档几乎全都自动生成，连[Code Review](https://zhida.zhihu.com/search?content_id=776253192&content_type=Answer&match_order=1&q=Code+Review&zhida_source=entity)都无脑使用AI，一开始效率飞升，皆大欢喜，然后线上出了bug，他们去debug的时候，找到出问题的那一行，却没人能解释当初为啥改这一行，git blame追查到改这一行的那个人，那人对改了这一行毫无印象，因为都是AI改的嘛，无脑信任AI，就是这个结果。

知识库也是一样的道理啊。

一个人用的时候，只要你自律有判断力，你对自己负责，觉得哪部分不对会追问，用的就好。

十个人用的时候呢？一个人往里面喂了一篇有问题的论文，LLM把它编译进了[维基](https://zhida.zhihu.com/search?content_id=776253192&content_type=Answer&match_order=1&q=%E7%BB%B4%E5%9F%BA&zhida_source=entity)，其他九个人基于这条错误信息继续构建，幻觉就这么滚雪球了。

当然，有人在尝试解决这个问题。一个叫jumperz的开发者搞了个Swarm Agent架构，让多个Agent协作来管理知识库。

![](https://pic1.zhimg.com/50/v2-88e967d8c7868125a056031771bcca6f_720w.jpg?source=1def8aca)

![](data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='1492' height='1108'></svg>)

Swarm Agent

其中还有一个独立的评审员[Hermes](https://zhida.zhihu.com/search?content_id=776253192&content_type=Answer&match_order=1&q=Hermes&zhida_source=entity)，它来做QA，每篇AI生成的Wiki都要过审，合格了才能进入正式知识库，不合格的停留在草稿区自生自灭。

我觉得这个有独立QA的思路很棒，值得仔细探究。

* * *

Karpathy发的这条推下面，很多人都有这样一个问题：**您能不能做一期油管视频来讲讲？**

![](https://picx.zhimg.com/50/v2-a01ee22d74711cae5321e525d3e2d9d1_720w.jpg?source=1def8aca)

![](data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='1786' height='674'></svg>)

有意思，Karpathy这个推文是用Markdown+Wiki就能管理知识，而大家的第一反应是——**我还是想看你真人出镜，对着镜头给我讲一遍** 。

这就是智人啊，视觉动物。

知识库可以是Markdown的，但人类获取知识的偏好不是阅读，而是看别人讲，难怪知乎玩不过抖音呢:-)

Karpathy用实际行动证明了**LLM可以当图书管理员** ，Karpathy的粉丝们用实际回应证明了，**比起去图书馆翻书，大家更想听馆长直接的宣讲** 。

送礼物

还没有人送礼物，鼓励一下作者吧

[编辑于2026-04-06 10:34](//www.zhihu.com/question/2024197832765128929/answer/2024431529238036773)

​赞同 771​​49 条评论​1472 ​39 

​分享

​

​

收起​

[![wangleineo](https://pic1.zhimg.com/v2-8c2de28ae2740a09f3efc66d5707b2e5_l.jpg?source=1def8aca)](//www.zhihu.com/people/wonglei)

[wangleineo](//www.zhihu.com/people/wonglei)

[​![](https://pic1.zhimg.com/v2-27bfcba90e66db79ce8768ab807e017e_l.png?source=32738c0c)](https://www.zhihu.com/question/48509984)​![](https://picx.zhimg.com/v2-4812630bc27d642f7cafcd6cdeca3d7a.jpg?source=88ceefae)

AI编程开发话题下的优秀答主

[收录于 · AI时代](https://www.zhihu.com/column/c_1896267381921280342)

航海家 icon-meh 等 381 人赞同

传统的知识库系统基于RAG：把原文切成小段（chunk），然后计算其[Embedding](https://zhida.zhihu.com/search?content_id=776194002&content_type=Answer&match_order=1&q=Embedding&zhida_source=entity)，存入向量数据库。当用户提问时，把问题也转换成向量，到向量数据库查询，找到语义最接近的一些chunks，和问题一起放入[LLM](https://zhida.zhihu.com/search?content_id=776194002&content_type=Answer&match_order=1&q=LLM&zhida_source=entity)的上下文，让LLM根据引用资料回答问题。这是RAG最简单的形式，复杂一些的系统会增加全文索引和搜索、Reranker等等组件，甚至启用多轮查询来找到需要的文字资料。

Andrej的知识库构想，本质上将知识库系统划分为三个层次：

  * 原始数据层：可导入多种格式的数据，数据导入引擎会将其转换为 [Markdown](https://zhida.zhihu.com/search?content_id=776194002&content_type=Answer&match_order=1&q=Markdown&zhida_source=entity) 格式并存储于特定目录。
  * 知识图谱层：也是 Markdown 文件形式。但由大语言模型生成，按概念组织，并通过概念间的关系相互连接。这些 Markdown 文件还可引用原始数据文件。
  * 用户界面层：在向用户呈现信息时，系统可支持多种格式：纯文本、幻灯片、思维导图、音频、网页动画等。大语言模型负责查询知识图谱层与原始数据，以构建相应格式。



我的猜测是，[NotebookLM](https://zhida.zhihu.com/search?content_id=776194002&content_type=Answer&match_order=1&q=NotebookLM&zhida_source=entity) 的运作方式就是如此，只是它不公开展示中间层（知识图谱层）。

![](https://pic1.zhimg.com/50/v2-9518d9eb73e841fbcd4ab3913a8a96e5_720w.jpg?source=1def8aca)

![](data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='1114' height='1170'></svg>)

我一直用[Obsidian](https://zhida.zhihu.com/search?content_id=776194002&content_type=Answer&match_order=1&q=Obsidian&zhida_source=entity)打造自己的笔记系统，现在累积了上千条笔记。既有自己写的，也有收集的网文。关于如何组织它们，的确有点头疼，一开始用目录结构来组织，发现不够灵活；于是放在同一个层次上，用Tag来管理，安装了一个AI打Tag的插件，但是发现AI很不擅于给文本写Tag，要自己手动维护Tag又很麻烦。Andrej用LLM来构建一个知识Wiki层这个设计，可以把分散在各个笔记中的概念组织起来，倒是很值得尝试一下。

关于第三层，用户界面层，我以前也有过类似的想法： [AI阅读应用的三个维度](https://www.zhihu.com/pin/1975889702021243711) 。可以根据用户的喜好以各种形式来展示知识：

  1. 文本形式。
  2. Slides：Karpathy提到了一个[Marp](https://zhida.zhihu.com/search?content_id=776194002&content_type=Answer&match_order=1&q=Marp&zhida_source=entity)的方案，还有[slidev](https://zhida.zhihu.com/search?content_id=776194002&content_type=Answer&match_order=1&q=slidev&zhida_source=entity)等也可以用。
  3. [Mindmap](https://zhida.zhihu.com/search?content_id=776194002&content_type=Answer&match_order=1&q=Mindmap&zhida_source=entity)或者其他的[mermaid](https://zhida.zhihu.com/search?content_id=776194002&content_type=Answer&match_order=1&q=mermaid&zhida_source=entity)静态图表形式。
  4. 配合[TTS模型](https://zhida.zhihu.com/search?content_id=776194002&content_type=Answer&match_order=1&q=TTS%E6%A8%A1%E5%9E%8B&zhida_source=entity)，做成语音播客形式。
  5. 如果不在乎成本，可以调用AI图片视频模型生图、视频来讲解概念。
  6. 用Html内的[SVG](https://zhida.zhihu.com/search?content_id=776194002&content_type=Answer&match_order=1&q=SVG&zhida_source=entity)动画展示动态过程，就像Claude一样：[Claude的动画功能简直炫爆了！](https://www.zhihu.com/pin/2015582636697998099)



Lex Fridman在评论区留言，他就采用了第6种格式来和知识库交互：

![](https://pic1.zhimg.com/50/v2-289d4efaa0d5f35f879ee87d496b1845_720w.jpg?source=1def8aca)

![](data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='865' height='538'></svg>)

Andrej的这个设计主要有两方面的创新。一是用AI来完成知识图谱的动态构建；二是知识库的三层架构。

构建知识图谱是对文本数据的结构化（或者说半结构化），Andrej用程序代码的编译（Compile）来形容，很贴切。Compile可以理解成一个伞式术语，不仅包含常用的总结（summarize），还包含概念抽取、分类、对比、归纳、联想等等对文本的智能加工。具体做什么，完全取决于你写给LLM的引导性提示词。原始文本在第二层被编译成一个半结构化的表示，又在第三层映射成用户友好的展示界面。

这个三层架构可能会成为知识库产品的一个通用架构。其中每一层都可以用各种不同的实现。比如第二层，可以用AI维护一组markdown的形式来实现（Andrej的设计），也可以引入一个图数据库（[GraphRAG](https://link.zhihu.com/?target=https%3A//github.com/microsoft/graphrag)的设计），甚至可以用纯手工画Canvas，或者通过Tag Network来构建知识图谱。

只要三个层次之间定义好接口，每一个层次就可以容纳各种可替换的方案：

  * 第一层是各种数据源的ingestion engine，导出成通用文本格式，构成第二层的接口。
  * 第二层就是上面说的各种知识图谱实现，为上层提供索引、查询接口。
  * 第三层利用AI模型，生产各种形式的用户界面。



Andrej这条推文，定义的不只是知识库的一种实现方案，它定义的可能是一种生态。三个层次的各种组件方案可以随意组合，搭建自己的知识库。

再深一层，这种架构的意义可能不仅限于知识库。在Andrej的idea文件中，有这样一行：

> I have the LLM agent open on one side and Obsidian open on the other. The LLM makes edits based on our conversation, and I browse the results in real time — following links, checking the graph view, reading the updated pages.   
> **Obsidian is the IDE; the LLM is the programmer; the wiki is the codebase.**

这个应用可以看成是“非代码项目的集成开发环境”。想想，所有的知识类工作，它们的本质不就是整理信息，把信息转换成新的形式交付吗？

  * 文员：把邮件、会议纪要、项目文档整理汇总，做一个PPT。
  * 科研工作：把领域内某个方向的相关论文通读一遍，总结成一个综述论文。
  * 新闻、自媒体：把最近的热点新闻相关的文章综合整理，写一个播客稿，然后录音频节目。
  * 分析师：收集某个行业的各公司财报、新闻事件、统计数据，写一份研究报告。
  * 作者（非虚构类）：写大纲，根据大纲收集资料，汇总整理，按章节写作。
  * 教师：把教材和相关材料加工整理，产出课件、作业、考试题。



所有这些工作，就是把一系列的文本数据用人的智能Compile一下，变成另一种形式输出。这些过程都可以用上述知识库的方式来完成。这样看的话，它就不仅是一个知识库，而是一个知识类工作的通用Agent，也就是[Claude Cowork](https://zhida.zhihu.com/search?content_id=776194002&content_type=Answer&match_order=1&q=Claude+Cowork&zhida_source=entity)的生态位了。

* * *

Andrej这两条推文没少给Obsidian带货，Obsidian都感受到压力了，大幅扩张工程团队，从3个人增加到了4个人。

![](https://pica.zhimg.com/50/v2-cee90940e62c6c06d5fd5d5ec5602460_720w.jpg?source=1def8aca)

![](data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='1170' height='943'></svg>)

对自己技术自信的小伙伴可以试试，不限地理位置远程办公哦。

* * *

🚀 **我的[知识星球](https://zhida.zhihu.com/search?content_id=776194002&content_type=Answer&match_order=1&q=%E7%9F%A5%E8%AF%86%E6%98%9F%E7%90%83&zhida_source=entity)「AI Engineer」正式开放:** [AI Engineer](https://link.zhihu.com/?target=https%3A//t.zsxq.com/XctMe)

如果你热衷AI技术，想用AI Agent、RAG、大模型做出实用产品，这个星球就是为你准备的。

**加入后你将获得：**

**🔥 深度实战内容**

  * AI Agent架构设计、提示词工程、落地避坑指南
  * 每周工具测评 & 产品拆解（不是理论，是能跑的代码）



📖 **新书抢先读**

我正在撰写《AI Agent实战指南》，全书章节**优先在星球连载** （大纲已完成，早鸟可第一时间追更）。

💬 **交流 & 答疑**

与同好一起从0到1打磨AI产品，我也会定期回答你的具体问题。

🎁 **首批限时优惠**

原价 **199元/年** ，领券立减 **100元** → **仅需99元**  
⏰ **6月1日恢复原价** ，仅限前50名

**立即加入：**  
👉 点击领取优惠券：[下载图片在微信里扫码](https://link.zhihu.com/?target=https%3A//raw.githubusercontent.com/RealHacker/system-prompts-visualizer/refs/heads/main/planet%2520coupon.png)。如果失效，星球小程序搜索“AI Engineer”。

送礼物

还没有人送礼物，鼓励一下作者吧

[编辑于2026-05-09 19:52](//www.zhihu.com/question/2024197832765128929/answer/2024214594608964286)

​赞同 381​​19 条评论​992 ​9 

​分享

​

​

收起​

[![平凡](https://pic1.zhimg.com/v2-9f81432bb5f397e14ec2c65e949eb0d3_l.jpg?source=1def8aca)](//www.zhihu.com/people/jzwa)

[平凡](//www.zhihu.com/people/jzwa)

[​![](https://picx.zhimg.com/v2-4a07bc69c4bb04444721f35b32125c75_l.png?source=32738c0c)](https://www.zhihu.com/question/510340037)

新知答主

[收录于 · 人工智能AI知识库](https://www.zhihu.com/column/c_1867989249418211328)

航海家 温戈 等 418 人赞同

[Karpathy](https://zhida.zhihu.com/search?content_id=776351105&content_type=Answer&match_order=1&q=Karpathy&zhida_source=entity) 这条推文，技术上没有什么新东西。

没有新模型，没有新算法，没有新工具。

但它 1700 万阅读量背后有一件事值得认真回答：这个架构的本质是什么？它和 RAG 的区别，究竟是技术层面的，还是认知模型层面的？

我认为是后者。

## **先说结论**

Karpathy 的方案和 RAG 的核心差异，可以用一对计算机科学里的经典概念来描述：

**RAG = 解释器模式（Interpreter）**

**[LLM](https://zhida.zhihu.com/search?content_id=776351105&content_type=Answer&match_order=1&q=LLM&zhida_source=entity) Wiki = 编译器模式（Compiler）**

你先看下面这个图，很直白的区别。

![](https://pica.zhimg.com/50/v2-ff4681d70a2aa37f9b355af7682c956f_720w.jpg?source=1def8aca)

![](data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='1229' height='847'></svg>)

如果你写过代码，你会立刻明白这意味着什么。

简单来说，就三句话

  1. 解释器是每次运行时现场翻译代码，慢但灵活。 
  2. 编译器是提前一次性把代码翻译好，运行时直接执行，快且高效，但需要预处理时间。
  3. RAG 每次查询，都让 LLM 现场去原始文档里"找"信息，临时合成答案，用完即丢。 



Karpathy 的 Wiki，是提前让 LLM 把所有文档"编译"成一个结构化百科，查询时 LLM 翻的是自己写的笔记。

这个框架可以推演出几乎所有你想问的问题。

## **为什么 RAG 是"解释器"**

RAG 的工作流程是这样的：

你把文档切成小块（chunk），给每个块生成一个向量（embedding）。用户提问时，系统找到最相似的几个块，拼给 LLM，LLM 基于这些块生成回答。

这里面有一个根本性的问题：每次查询，LLM 都是在"现场读原文"。

你今天问"XX 的核心架构是什么"，LLM 读了三段文本，给了你答案。明天你问"XX 的优缺点"，LLM 再读三段文本，又给了你一个答案。这两次回答之间，没有任何积累发生——它每次都从零开始。

你问了 100 次，它就综合了 100 次。

**知识没有复利。**

而且更深的问题是：chunk 本身是人为切割的，丢失了原始语境。向量 embedding 是黑盒，一个文档和另一个文档的关联是通过数学相似度建立的，不是通过语义理解。溯源很难，修改更难。

## **Karpathy 方案的核心机制：知识编译**

他的系统有三层：

第一层：Raw原始文档，LLM 只读不改，保持不可变。

第二层是 Wiki：LLM 读完所有原始文档后，写出来的结构化 Markdown 文件集合。包含概念页、来源摘要、实体条目，以及页面间的交叉引用（backlinks）。这层才是真正的知识库。

第三层是 [Schema](https://zhida.zhihu.com/search?content_id=776351105&content_type=Answer&match_order=1&q=Schema&zhida_source=entity)：一个配置文件（Gist 里建议用 CLAUDE.md），定义 Wiki 的组织结构、格式约定、操作流程。Schema 把通用 LLM 变成了有纪律的知识管理员。

日常操作只有三种：

**Ingest** ：加入新的原始资料，LLM 读完后更新 Wiki。一份新资料通常会触及 10-15 个已有页面，建立新连接。

**Query** ：提问，LLM 翻自己写的 Wiki 回答，有价值的回答本身也归档进 Wiki——知识开始复利。

**[Lint](https://zhida.zhihu.com/search?content_id=776351105&content_type=Answer&match_order=1&q=Lint&zhida_source=entity)** ：定期健康检查，LLM 扫描 Wiki，找矛盾、孤立页面、过时内容。

Karpathy 自己的研究 Wiki，在单个话题上已经积累到了 100 篇文章、40 万字——比一篇博士论文还长。他没有亲自写一个字。

**这个框架真正有趣的地方在哪**

你可能会问：Wiki 文件多了，不也需要检索吗？那不就还是 RAG 吗？

还真不是。

区别在于**检索的对象是什么** 。

RAG 检索的是原始文档的片段，文档本身没有经过理解，语义结构是由检索算法临时决定的。

LLM Wiki 检索的是 LLM 已经理解过、整理过的笔记——语义结构是在 [ingest](https://zhida.zhihu.com/search?content_id=776351105&content_type=Answer&match_order=1&q=ingest&zhida_source=entity) 阶段提前建立好的，查询时只是取出结果。

用编译器类比：RAG 是每次把源码跑一遍；Wiki 是编译好的二进制，直接执行。

Karpathy 在 Gist 里也提到了支撑这个系统的核心工具：qmd（本地 Markdown 搜索，支持 [BM25](https://zhida.zhihu.com/search?content_id=776351105&content_type=Answer&match_order=1&q=BM25&zhida_source=entity) \+ 向量 + LLM reranking）、[Obsidian](https://zhida.zhihu.com/search?content_id=776351105&content_type=Answer&match_order=1&q=Obsidian&zhida_source=entity)（浏览 Wiki 的 IDE）、[Web Clipper](https://zhida.zhihu.com/search?content_id=776351105&content_type=Answer&match_order=1&q=Web+Clipper&zhida_source=entity)（自动把网页转为 Markdown 存入 raw/）。

整个技术栈的特点是：简单、可控、可溯源。没有向量数据库，没有外部 API 依赖，全是本地 Markdown 文件。

**Obsidian 的 CEO Steph Ango 本人也参与了这个话题的讨论，他建议维护两个独立[Vault](https://zhida.zhihu.com/search?content_id=776351105&content_type=Answer&match_order=1&q=Vault&zhida_source=entity)：一个放人工整理的知识，一个放 AI 编译的内容，防止 AI 幻觉污染人工高质量笔记。这个建议很实用，也直接指向了这个方案最大的未解问题。**

## **这个方案的真实边界**

说清楚它好在哪，也要说清楚它的边界。

第一，**规模限制** 。这套方案在个人知识库规模下非常好用：100-500 篇文章，用 index.md + 上下文窗口就够了。如果你有数十万份文档，上下文窗口装不下，还是需要 RAG 辅助检索。Karpathy 本人也没说这是企业级方案。

第二，**幻觉传播风险** 。如果 LLM 在 ingest 阶段写了一个错误的连接，这个错误会通过 backlinks 扩散到越来越多的页面。RAG 至少可以回头看原文，Wiki 里的错误可能更难发现。Lint 操作可以缓解，但不能完全消除。

第三，**上手门槛** 。现在这套工具链对非技术用户还是偏程序员友好，需要配置 CLAUDE.md、理解文件夹结构、会用 Coding Agent 执行操作。

这个架构的价值不在于它有多新颖，而在于它把一个"显而易见但没人认真做"的想法清晰化了：

在个人知识管理这个规模，LLM 够聪明，没必要用 RAG 的复杂度。

Markdown + LLM + 纪律，就够了。

对于做研究、整理信息量大的人来说，这个方案现在就值得认真试一试。不一定要搭完整版，哪怕先用最简单的形式，一个 raw/ 文件夹、一个 wiki/ 文件夹、一个配置文件，跑起来的感觉会告诉你这件事有没有价值。

送礼物

还没有人送礼物，鼓励一下作者吧

[发布于2026-04-07 04:54](//www.zhihu.com/question/2024197832765128929/answer/2024711510899922921)

​赞同 418​​21 条评论​958 ​16 

​分享

​

​

收起​

[Qwen3.8-Max首发尝鲜，个企双版超值优惠低至39元/月起Qwen3.8-Max 首发尝鲜、上新 deepseek-v4-flash，更多模态和旗舰模型共享额度，个企双版本超值优惠低至 39 元/月起，高效开启 AI 生产力查看详情](https://click.qianwenai.com/m/20000000790/?cb=https%3A%2F%2Fsugar.zhihu.com%2Fplutus_adreaper_callback%3Fsi%3D76d75fc0-ce8a-4301-b27e-eee0b513ce07%26os%3D3%26zid%3D236%26zaid%3D3777575%26zcid%3D3789508%26cid%3D3789507%26event%3D__EVENTTYPE__%26value%3D__EVENTVALUE__%26score%3D__EVENTSCORE__%26ts%3D__TIMESTAMP__%26cts%3D__TS__%26mh%3D7492365d72e10bec9fe0718b0ca42ec3%26adv%3D645640%26ocg%3D0%26cp%3D0%26ocs%3D0%26aic%3D0%26atp%3D0%26ct%3D0%26ed%3DGiBNJgVzfCMmUW9XFyEvRA8xBGxJICwkOhh0FlwxKw1ZY0gnWzUoISkYf1UXISFcCiIEeh4yNyw9GGJBRCUlVFZ0DHMIc2h3fRVrVwZgfwdZY1YkXSo-fX4DPhIMZ3wEXHYNeQntjUMcdG7cxQ%3D%3D&spu=biz%3D0%26ci%3D3789508%26si%3D8575d7ff-e788-4b94-a9b8-6ba01dd76f34%26ts%3D1785941257%26zid%3D236)

阿里云的广告 · 3.2 万人浏览

[![Simon Zhang](https://pica.zhimg.com/v2-0adb73ac29a5278ae43136b73da1f81c_l.jpg?source=1def8aca)](//www.zhihu.com/people/simon-zhang-14)

[Simon Zhang](//www.zhihu.com/people/simon-zhang-14)

[​![](https://pica.zhimg.com/v2-27bfcba90e66db79ce8768ab807e017e_l.png?source=32738c0c)](https://www.zhihu.com/question/48509984)

建筑学话题下的优秀答主

[收录于 · 赛萌君的AI笔记](https://www.zhihu.com/column/c_1853351007855190018)

283 人赞同了该回答

“xx就是你的第二大脑”这阵风还是吹到了[karpathy](https://zhida.zhihu.com/search?content_id=776274189&content_type=Answer&match_order=1&q=karpathy&zhida_source=entity)的推文里……

这是一个极大增加了管理维护复杂度，极大程度上增加token消耗，同时只适用于一小撮播客或者自媒体博主的知识管理方案。

如果去掉Agentic的部分，纯粹是很多年前企业内部Wiki项目限时返场。当年有些人把结构化思考的期望寄托在结构化文档上面。

![](https://pica.zhimg.com/50/v2-c1c726eefadc712f1832729a36555ee8_720w.jpg?source=1def8aca)

![](data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='1080' height='269'></svg>)

图源：https://developer.volcengine.com/articles/7535837333141061683

事后只证明了两件事：

  1. 结构化的思考来源于使用者本身的mindset，再好的文档也会有组织内部的人看起来一头雾水。所以最终决定一个组织能否最大化结构思考的共识取决于每一个成员的素质和组织内的管理水平，反例可以参考前几个月火起来的OpenClaw，上月末本月初的几次重大更新有种不管其他人死活的美感。
  2. 结构化文档的维护在长期来看是不可持续的，除非这个知识库是一个很有限的静态知识库（内容不随着时间而变化）。只有打磨静态知识才有所谓的“复利”，在一个动态知识库里昨天的洞察可以是今天的噪音，前期知识之间的关系连接越精细后期就越难迭代。在[LLM](https://zhida.zhihu.com/search?content_id=776274189&content_type=Answer&match_order=1&q=LLM&zhida_source=entity)还不能很好handle大型代码库的当下，你让它去更新大型知识库也会遇到一样的问题。



然后他那个llm-wiki.md里最后写灵感源泉是1945年Vannevar Bush的Memex[1]……

![](https://pic1.zhimg.com/50/v2-e490b1b9c9ed413b91830eb7f611291c_720w.jpg?source=1def8aca)

![](data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='597' height='399'></svg>)

图源：https://www.reddit.com/r/Futurism/comments/z6bd4a/do_you_think_we_have_already_created_any_memex/#lightbox

> Memex 被设想为一种“个人图书馆”或“记忆辅助工具”。Bush 将其描述为一个类似写字台的设备，内部存储了大量书籍、记录和通讯内容，并且能以极高的速度和灵活性进行检索。  
> 基于当时的技术，Bush 设想它使用微缩胶片来存储信息，并配有屏幕、键盘和按钮进行操作。

Memex 最核心的贡献在于它对信息组织方式的重构。Bush 认为，人类的大脑不是通过“分类目录”运作的，而是通过联想。Memex 允许用户建立“迹线”（Trails）。当你阅读一篇文章时，可以点击一个开关，将它与另一篇相关的文章永久性地“链接”在一起。这种在不同文档间跳转的能力，直接启发了后来的超文本（Hypertext）和万维网（World Wide Web）。

这一概念被应用在现在几乎所有主流的个人知识管理（[PKM](https://zhida.zhihu.com/search?content_id=776274189&content_type=Answer&match_order=1&q=PKM&zhida_source=entity)）工具上，问题是这些产品几乎无一例外地把关联知识的重担推到了用户身上，自己本身只提供低阻力的分类功能。

然后现在有个人跳出来说：没关系，花token就好了。我不太明白为什么要用大量的[LLM token](https://zhida.zhihu.com/search?content_id=776274189&content_type=Answer&match_order=1&q=LLM+token&zhida_source=entity)去给一个很古老的思维工具模式擦屁股，这种行为像是什么呢，就好比你用光刻机的零件拼出了一台效率x100的[珍妮纺纱机](https://zhida.zhihu.com/search?content_id=776274189&content_type=Answer&match_order=1&q=%E7%8F%8D%E5%A6%AE%E7%BA%BA%E7%BA%B1%E6%9C%BA&zhida_source=entity)，然后指着上面连着的线说：看，我给自己织了一件新衣服！

BBC：But at what cost?

* * *

今年很多概念造得都让人无语，Markdown is all you need这种垃圾话听听得了，我甚至有些怀疑[Karpathy](https://zhida.zhihu.com/search?content_id=776274189&content_type=Answer&match_order=1&q=Karpathy&zhida_source=entity)是不是已经和Peter看齐，成了大厂卖token的二道贩子了，你看他原帖怎么说的：

> **[LLM 知识库](https://zhida.zhihu.com/search?content_id=776274189&content_type=Answer&match_order=1&q=LLM+%E7%9F%A5%E8%AF%86%E5%BA%93&zhida_source=entity)**  
>  最近我发现一件非常有用的事：利用 LLM 为各种感兴趣的研究课题构建**个人知识库** 。这样一来，我最近大部分的 Token 消耗不再是用于处理代码，而是用于处理知识（以 Markdown 和图像的形式存储）。最新的 LLM 非常擅长处理这些。具体流程如下：  
> **数据摄入：** 我会将原始文档（文章、论文、代码库、数据集、图像等）索引到一个 `raw/` 目录下，然后使用 LLM 增量式地“编译”出一个 Wiki，这其实就是一个存放在目录结构中的 `.md` 文件集合。这个 Wiki 包含了 `raw/` 目录下所有数据的摘要、反向链接，并能将数据归类为不同的概念、撰写相关文章并将它们关联起来。为了将网页文章转换为 `.md` 文件，我喜欢使用 **[Obsidian](https://zhida.zhihu.com/search?content_id=776274189&content_type=Answer&match_order=1&q=Obsidian&zhida_source=entity) Web Clipper** 扩展，并使用快捷键将所有相关图像下载到本地，以便我的 LLM 能够轻松引用。  
> **IDE：** 我使用 **Obsidian** 作为“前端 IDE”，在这里我可以查看原始数据、编译后的 Wiki 以及生成的各种可视化图表。需要注意的是，Wiki 的所有数据都由 LLM 编写和维护，我很少直接改动它。我还尝试了一些 Obsidian 插件来以其他方式渲染和查看数据（例如用 **[Marp](https://zhida.zhihu.com/search?content_id=776274189&content_type=Answer&match_order=1&q=Marp&zhida_source=entity)** 制作幻灯片）。  
> **问答（Q &A）：** 有趣的地方在于，一旦你的 Wiki 规模足够大（例如我最近关于某项研究的 Wiki 约有 100 篇文章，共 40 万字），你就可以向你的 [LLM 智能体](https://zhida.zhihu.com/search?content_id=776274189&content_type=Answer&match_order=1&q=LLM+%E6%99%BA%E8%83%BD%E4%BD%93&zhida_source=entity)提出各种针对该 Wiki 的复杂问题，它会自动去进行研究、寻找答案等。我原以为需要用到复杂的 RAG（检索增强生成），但在这种中小规模下，LLM 在自动维护索引文件和文档简要概述方面表现得非常好，阅读所有重要的相关数据也相当轻松。  
> **输出：** 比起在终端获取文本答案，我更喜欢让它为我渲染 Markdown 文件、幻灯片（Marp 格式）或 matplotlib 图像，然后我再次在 Obsidian 中查看。根据查询需求，你可以想象出许多其他的视觉输出格式。通常，我会将这些输出重新“归档”回 Wiki 中，以增强它处理后续查询的能力。因此，我自己的探索和查询总是在为知识库增值。  
> **优化（Linting）：** 我会对 Wiki 运行一些 LLM “健康检查”，例如查找不一致的数据、补全缺失信息（通过网页搜索）、发现有趣的新文章关联点等，以此增量式地清理 Wiki 并提升其整体数据完整性。LLM 非常擅长建议进一步探索的问题。  
> **额外工具：** 我发现自己还在开发一些额外的工具来处理数据，比如我“氛围写码”（vibe coded）了一个运行在 Wiki 上的小型朴素搜索引擎，我既会直接使用它（通过 Web UI），也经常通过命令行将其作为工具交给 LLM 来处理更大规模的查询。  
> **进一步探索：** 随着仓库规模的增长，自然而然的想法是考虑“合成数据生成 + 微调”，让 LLM 通过权重直接“记住”这些数据，而不仅仅是依靠上下文窗口。  
> **总结（TLDR）：** 从给定数量的来源收集原始数据，由 LLM 编译成 `.md` 格式的 Wiki，随后由 LLM 通过各种命令行工具进行问答和增量增强，所有内容均可在 Obsidian 中查看。你几乎不需要手动编写或编辑 Wiki，那是 LLM 的领地。我认为这里有巨大的空间去打造一款令人惊叹的新产品，而不仅仅是一堆简陋的脚本集合。

搞了半天是把token消耗从coding放到了数据转化（Anything2md）上……弄一堆链接把这些Markdown文件串成一个Graph。

用脚趾头想都知道随着后期文档越来越多，无论是新增内容还是维护使用，你不依赖[Embedding](https://zhida.zhihu.com/search?content_id=776274189&content_type=Answer&match_order=1&q=Embedding&zhida_source=entity)/Indexing一定会面临海量的token消耗（按照Karpathy原文的说法即便是增量更新对于token的消耗最少是线性增长）。从性价比上来说Embedding Model的token价格只有LLM token价格的几分之一甚至更少。

而且纵观当年的Evernote到现在的[Notion](https://zhida.zhihu.com/search?content_id=776274189&content_type=Answer&match_order=1&q=Notion&zhida_source=entity)和Obsidian，问题从来不是知识库有多么结构化，而是本地文件分类和关联到最后一定会失效。因为越到后面无论是人还是LLM都会被困在自己创造出的系统里疲于奔命，要么是人得花精力去管理要么是舍得花Token让LLM去持续维护。

![](https://picx.zhimg.com/50/v2-b0f9f071730de96d835714d06c736735_720w.jpg?source=1def8aca)

![](data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='666' height='463'></svg>)

图源：https://postimg.cc/8fmkhxVp

从低维护的角度来看，扁平无状态才是最好的管理方式。作为前Evernote用户和现Obsidian用户，我现在最常用的知识库一个是[notebookLM](https://zhida.zhihu.com/search?content_id=776274189&content_type=Answer&match_order=1&q=notebookLM&zhida_source=entity)，另一个是ima。前者把数据格式转换压榨到极致，source转音视频、转PPT、转脑图、转文档等功能一应俱全，后者真就是直接往里丢文件，用Chrome端插件采集网页内容，然后问问题即可。

我完全无法想象notebookLM这样的产品要是让我自己在本地维护那得多肉疼token消耗，也就是现在的谷歌套餐包含了才能毫无心理负担地去使用。而像ima这类的知识库目前最大的优势是多端同步，管理成本也很低，我基本上不去做细致分类，大类上分错了也不要紧，一共没几个知识库，全@ 上也很方便。当然你也可以质疑后者作为一个产品没什么壁垒，从我这个用户角度来说RAG还真就是很多[笔记类软件](https://zhida.zhihu.com/search?content_id=776274189&content_type=Answer&match_order=1&q=%E7%AC%94%E8%AE%B0%E7%B1%BB%E8%BD%AF%E4%BB%B6&zhida_source=entity)的救星，要是[GenAI](https://zhida.zhihu.com/search?content_id=776274189&content_type=Answer&match_order=1&q=GenAI&zhida_source=entity)时代来得早个五六年，我也许不会弃用Evernote。

* * *

言归正传，karpathy的这套架构技术上是可行的，但是分层架构和连接关系都很常规，也依旧没有解决维护更新方面的痛点，烧token属于是厂商乐开花用户流出泪的解法。我个人觉得PKM工具在GenAI出现以后面临的问题是它需要管理的内容是爆炸式增长的，同样知识之间的关联关系也是在上述基础上的 O(n*m) 。

一个普通人花这么多精力去管理维护知识库，最好产出回报是能对冲投入的时间经济成本，否则最省力的办法还是搭模型能力的顺风车。讲道理这两年环境和工具调用上的提升应该足以抹平非结构化本地文件带来的不便。

别人我不知道，我自己不信什么知识库炼出金子的童话故事，可能自媒体大师们有这个需求。

## 参考

  1. ^Vannevar Bush 在 1945 年发表的文章《As We May Think》中提出的 Memex（Memory Extender 的缩写），被认为是现代个人电脑、互联网以及超文本系统的概念鼻祖。 <https://en.wikipedia.org/wiki/Memex>



送礼物

还没有人送礼物，鼓励一下作者吧

[发布于2026-04-06 13:12](//www.zhihu.com/question/2024197832765128929/answer/2024474561505140848)

​赞同 283​​24 条评论​317 ​10 

​分享

​

​

收起​

[![AI解码师](https://picx.zhimg.com/v2-fdac6de0add53a6c59762650c399ff7e_l.jpg?source=1def8aca)](//www.zhihu.com/people/ferrarizrw)

[AI解码师](//www.zhihu.com/people/ferrarizrw)

[​![](https://pic1.zhimg.com/v2-2ddc5cc683982648f6f123616fb4ec09_l.png?source=32738c0c)](https://www.zhihu.com/question/48510028)

互联网行业 技术专家

[收录于 · AI来时的路：记录AI发展的历程](https://www.zhihu.com/column/c_1903807394905031339)

122 人赞同了该回答

先说背景：4月2号[Karpathy](https://zhida.zhihu.com/search?content_id=776252654&content_type=Answer&match_order=1&q=Karpathy&zhida_source=entity)在X上发了一条帖子，随后又放出了一个gist文档。内容其实不复杂：搞了一套用**LLM主动编写和维护[Markdown Wiki](https://zhida.zhihu.com/search?content_id=776252654&content_type=Answer&match_order=1&q=Markdown+Wiki&zhida_source=entity)**的个人知识库系统，三层架构——`raw/`原始素材层、`wiki/`编译层、`schema`约束层。用[Obsidian](https://zhida.zhihu.com/search?content_id=776252654&content_type=Answer&match_order=1&q=Obsidian&zhida_source=entity)做前端浏览，LLM做后端维护，人负责丢素材和提问。

刷了下相关的文章，全网讨论主要集中在两个方向：一是“这是不是RAG的替代品？”，二是“这能不能做成产品？”

* * *

先说第一个问题，跟RAG的区别，大多数人用LLM的方式是通过对话的方式。你问一句，它答一句。**token被消耗在即时生成上，用完就没了。** 下次你再来，一切从零开始，你还得重新描述背景、重新解释上下文。

跟LLM长时间协作过的人一定有过这种体验：一个复杂项目搞到一半，session断了或者context满了，你得花大量时间和token把之前的“记忆”重建回来。Karpathy自己也提到了这个痛点。

他的做法是：**把相当一部分token不再花在“直接回答问题”上，而是花在“整理和维护一个持久化的知识结构”上。**

举个具体的例子，往`raw/`里扔了一篇新论文，传统RAG的做法是把它切片、向量化、存起来，等你问问题的时候再检索。Karpathy的做法是让LLM立刻读这篇论文，然后：

  * 写一页摘要存进wiki
  * 更新`index.md`目录
  * 遍历现有的实体页面和概念页面，找到相关的全部更新
  * 标注新论文和旧结论之间的矛盾
  * 在`log.md`里记一笔



**一份素材进来，可能触发10到15个wiki页面的修改。**

这些token花在了**知识的结构化沉淀** 上，下次再问问题的时候，LLM只需要读`index.md`找到相关页面，读完直接给你带引用的回答。回答需要的信息不再试临时检索拼凑出来的，而是早就被编译好了——交叉引用已经存在，矛盾已经标记，综合结论已经成型。

也就是说**从传统的“花token生成答案”转变到了到“花token维护知识”上。** 传统方式是用token换即时回报，Karpathy的方式是用token换**长期增值** （跟这阵子爆火的龙虾的思路挺像）。

* * *

这个思路早在1945年[Vannevar Bush](https://zhida.zhihu.com/search?content_id=776252654&content_type=Answer&match_order=1&q=Vannevar+Bush&zhida_source=entity)就在那篇著名的文章里提出了**[Memex](https://zhida.zhihu.com/search?content_id=776252654&content_type=Answer&match_order=1&q=Memex&zhida_source=entity)** 的概念——一种个人化的知识存储系统，文档之间有关联路径，人可以沿着路径跳转浏览。七八十年过去了，Wiki、笔记软件、知识图谱搞了一轮又一轮。

问题一直卡在同一个地方：**谁来做维护？**

任何维护过个人wiki或者[Notion](https://zhida.zhihu.com/search?content_id=776252654&content_type=Answer&match_order=1&q=Notion&zhida_source=entity)笔记库的人都知道，一开始热情满满，三个月后更新频率断崖式下降。因为维护的**认知负担** 太重了——你得判断新素材应该归到哪个分类，得检查旧条目要不要更新，得手动创建交叉链接。这些工作枯燥、琐碎、收益滞后，人受不了。

**LLM不觉得无聊。** 它不会忘记更新交叉引用，也不会懒得检查旧页面和新素材之间的冲突。一次操作可以同时修改15个文件，**维护成本接近于零** 。

另一个成立的条件是**上下文窗口的扩大** 。Karpathy的wiki规模是大约100篇文章、40万字。现在支持128K以上context的模型有几百个，支持1M以上的也有几十个。40万字的编译后wiki可以完整塞进[context window](https://zhida.zhihu.com/search?content_id=776252654&content_type=Answer&match_order=1&q=context+window&zhida_source=entity)，不需要做任何检索——LLM直接看全文，recall是100%。

如果放在两年前，8K context的时代，这套思路根本跑不起来。

* * *

也看到很多讨论在争论“Karpathy是不是在否定RAG”。这是个伪命题。

他否定其实是**在中等规模知识库上用RAG是过度工程** 。一套标准的RAG pipeline要搞向量数据库、embedding pipeline、chunk策略、top-k调参、[re-ranking](https://zhida.zhihu.com/search?content_id=776252654&content_type=Answer&match_order=1&q=re-ranking&zhida_source=entity)——对于个人研究项目或者部门级知识库来说，这些基础设施引入的复杂度和延迟，往往比它解决的问题更大。

而Karpathy的**编译式方案** 有一个RAG做不到的根本优势：**知识在存储层面就已经被结构化了。**

RAG检索回来的是“和你的问题语义相似的文本碎片”。这些碎片之间没有显式关联。你问“A和B有什么关系”，RAG可能分别找到讲A的chunk和讲B的chunk，但恰好漏掉了那段明确描述AB关系的内容——因为那段文字可能跟你的query向量距离较远。

Karpathy的wiki里，A和B的关系在**编译阶段** 就已经被LLM识别并写进了对应页面，以**backlink** 的形式显式存在。查询的时候，LLM看到A页面上有指向B的链接，自然就能顺着路径把关系说清楚。

当然，这套方案也有清晰的边界。当知识库膨胀到百万级文档、跨团队多来源数据汇入的时候，纯Markdown + context window的方案就扛不住了。那时候你确实需要向量检索、需要RAG。

**两者不是互斥关系，是不同规模下的不同选择。**

维度| RAG| Karpathy编译式  
---|---|---  
数据格式| 不透明的向量| 人可读的Markdown  
关联逻辑| 语义相似度| 显式backlink和索引  
可审计性| 低| 高——每个claim可追溯到具体.md文件  
适用规模| 百万级文档| 百到万级高信号文档  
维护方式| 静态（需要重新索引）| 主动式（LLM定期lint自愈）  
  
* * *

自己试了下。按照Karpathy的gist搭了一个简易版，用来整理最近在跟的一个开源项目的技术文档。

几个不成熟的结论：**编译阶段的prompt设计是核心壁垒。** Karpathy在gist里只给了high-level的思路，但实际操作中，你告诉LLM“读这篇文档然后更新wiki”远远不够。你得在`[schema](https://zhida.zhihu.com/search?content_id=776252654&content_type=Answer&match_order=2&q=schema&zhida_source=entity)`（也就是`[CLAUDE.md](https://zhida.zhihu.com/search?content_id=776252654&content_type=Answer&match_order=1&q=CLAUDE.md&zhida_source=entity)`或`AGENTS.md`）里非常明确地规定：新页面的标准格式是什么、什么情况下创建新实体页面、什么情况下合并到现有页面、冲突怎么标注、索引怎么分类。这个`schema`文件需要你和LLM反复迭代，搞个两三轮才能稳定。

在我大概攒了30多篇素材之后跑了一次health check，LLM找出了3处页面间的矛盾说法（同一个API参数在不同页面描述不一致）、2个孤儿页面、4个被频繁提及但没有专属页面的概念。这些问题如果是我自己维护，不知道什么时候才能发现，所以**[Lint](https://zhida.zhihu.com/search?content_id=776252654&content_type=Answer&match_order=1&q=Lint&zhida_source=entity) 操作的代价被严重低估了**。

**存在一定的幻觉，** 编译阶段LLM偶尔会在摘要里加入原始素材中没有的推断。目前的缓解方式是在每个页面强制要求source attribution，lint的时候交叉验证。不算完美，但够用。

* * *

Karpathy在gist末尾提了一个方向：当wiki经过长期lint变得足够“干净”之后，可以拿它做**fine-tuning的训练数据** ，把知识从context window搬到模型weights里。

这其实是一条很清晰的路径：**原始素材 → 编译成结构化wiki → wiki作为训练集 → fine-tune出领域专用小模型** 。

如果这条路跑通，意味着你的个人知识库最终可以“**内化** ”成一个专属于你的小模型。不需要每次查询都把整个wiki塞进context，模型本身就“知道”你的知识体系。

还还挺让人期待的。

* * *

Karpathy的这篇分享，技术上没什么特别高深的（他自己也说就是“hacky collection of scripts”）。他提出了一种**分配LLM算力的新思路** ——把token从一次性消耗转向**持久化知识投资** ，让LLM从无状态的聊天对象变成你**知识库的全职维护员** 。这个思路在**长context模型普及 + LLM维护成本趋近于零** 的条件下是成立的，而且可能会催生出一批新的个人知识管理工具。

至于能不能规模化到企业，那是另一个故事了。光是多人协作时的**幻觉传播** 问题，就够业界啃一阵子的。

送礼物

还没有人送礼物，鼓励一下作者吧

[编辑于2026-04-06 12:57](//www.zhihu.com/question/2024197832765128929/answer/2024430416518498208)

​赞同 122​​9 条评论​311 ​11 

​分享

​

​

收起​

[![广告](https://pic1.zhimg.com/v2-cde2d2b5b191c7b00fcf9572d74ca7cb_720w.webp?source=d6434cab)](https://www.volcengine.com/activity/ark?utm_source=7&utm_medium=zhihu&utm_term=vg_zhihu_libao_webjx_dmx19k9&utm_campaign=0&utm_content=dbdmx_19k9&spu=biz%3D0%26ci%3D3634141%26si%3D1946f1a5-b681-40fb-b3f9-3254555dd0b9%26ts%3D1785941259%26zid%3D3)

相关问题

[能否设计一个好的算法，实现智能的自我涌现？](/question/58755259) 1 个回答

[从机器学习角度，如果数据样本足够支撑，你会如何优化你的项目？ ?](/question/330540064) 1 个回答

大家都在搜

换一换

[笔试第一称被第二名花钱劝弃考428 万](/search?q=%E7%AC%94%E8%AF%95%E7%AC%AC%E4%B8%80%E7%A7%B0%E8%A2%AB%E7%AC%AC%E4%BA%8C%E5%90%8D%E8%8A%B1%E9%92%B1%E5%8A%9D%E5%BC%83%E8%80%83&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)热

[鸿蒙智行回应「竹知了」事件362 万](/search?q=%E9%B8%BF%E8%92%99%E6%99%BA%E8%A1%8C%E5%9B%9E%E5%BA%94%E3%80%8C%E7%AB%B9%E7%9F%A5%E4%BA%86%E3%80%8D%E4%BA%8B%E4%BB%B6&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)热

[DeepSeek 被称为大模型「斩杀线」354 万](/search?q=DeepSeek+%E8%A2%AB%E7%A7%B0%E4%B8%BA%E5%A4%A7%E6%A8%A1%E5%9E%8B%E3%80%8C%E6%96%A9%E6%9D%80%E7%BA%BF%E3%80%8D&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)热

[婚外胚胎案丈夫称已销毁胚胎349 万](/search?q=%E5%A9%9A%E5%A4%96%E8%83%9A%E8%83%8E%E6%A1%88%E4%B8%88%E5%A4%AB%E7%A7%B0%E5%B7%B2%E9%94%80%E6%AF%81%E8%83%9A%E8%83%8E&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)新

[人生选择模拟器346 万](https://event.zhihu.com/renshengxuanze/)活动

[周杰伦 刘若雪345 万](/search?q=%E5%91%A8%E6%9D%B0%E4%BC%A6+%E5%88%98%E8%8B%A5%E9%9B%AA&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)新

[长鑫拒绝苹果降价要求345 万](/search?q=%E9%95%BF%E9%91%AB%E6%8B%92%E7%BB%9D%E8%8B%B9%E6%9E%9C%E9%99%8D%E4%BB%B7%E8%A6%81%E6%B1%82&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)新

[同济大学取消教师长期聘任344 万](/search?q=%E5%90%8C%E6%B5%8E%E5%A4%A7%E5%AD%A6%E5%8F%96%E6%B6%88%E6%95%99%E5%B8%88%E9%95%BF%E6%9C%9F%E8%81%98%E4%BB%BB&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)热

[患癌妻子申请销毁婚外胚胎遭拒329 万](/search?q=%E6%82%A3%E7%99%8C%E5%A6%BB%E5%AD%90%E7%94%B3%E8%AF%B7%E9%94%80%E6%AF%81%E5%A9%9A%E5%A4%96%E8%83%9A%E8%83%8E%E9%81%AD%E6%8B%92&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)热

[妈妈罚男孩一次性吃30袋魔芋爽314 万](/search?q=%E5%A6%88%E5%A6%88%E7%BD%9A%E7%94%B7%E5%AD%A9%E4%B8%80%E6%AC%A1%E6%80%A7%E5%90%8330%E8%A2%8B%E9%AD%94%E8%8A%8B%E7%88%BD&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)热

[![广告](https://pic1.zhimg.com/v2-8ebbc9b6201827235d9f8ada638b1b51_720w.webp?source=d6434cab)](https://zhuanlan.zhihu.com/p/2065803984070079183?plugcb=https%3A%2F%2Fsugar.zhihu.com%2Fplutus_adreaper_callback%3Fsi%3D02f9f358-c58c-46d7-bca2-63c2fe880926%26os%3D3%26zid%3D4%26zaid%3D3780426%26zcid%3D3796362%26cid%3D3796362%26event%3D__EVENTTYPE__%26value%3D__EVENTVALUE__%26score%3D__EVENTSCORE__%26ts%3D__TIMESTAMP__%26cts%3D__TS__%26mh%3D7492365d72e10bec9fe0718b0ca42ec3%26adv%3D19403%26ocg%3D1%26cp%3D100%26ocs%3D0%26aic%3D0%26atp%3D0%26ct%3D2%26ed%3DGiBNJgVzfCMmUW9XFyEvRA8xBGxJICwkOhh0FlwxKw1ZY0gnWzUoISkYf1UXISFcCiIEeh4yNyw9GGJBRCUlVFZ0DnsMcG14fBZnUAhpegZSY1YkXSo-fX4DPhIMZ3wEXHYNeQkSzp5O_hupPw%3D%3D&spu=biz%3D0%26ci%3D3796362%26si%3D07e13362-02bb-453f-8f36-7a8ea77fee96%26ts%3D1785941260%26zid%3D4)

 

帮助中心

服务热线：400-919-0001[帮助与客服](/help-center)[联系我们](/contact)更多

 

举报中心

违法和不良信息举报：010-82716601[我的举报](/community?source=zhihu_default)更多

 

关于知乎

[知乎个人信息保护指引](/term/privacy)[知乎协议](/term/zhihu-terms)[下载知乎](https://www.zhihu.com/app/)[Investor Relations](https://ir.zhihu.com)网站资质信息更多

* [京ICP证110745号](https://tsm.miit.gov.cn/dxxzsp/) · [京ICP备13052560号-1](https://beian.miit.gov.cn/) · [京公网安备 11010802020088 号](http://www.beian.gov.cn/portal/registerSystemInfo?recordcode=11010802020088) · [京网文[2025]0422-132 号](https://www.zhihu.com/certificates) · [药品医疗器械网络信息服务备案（京）网药械信息备字（2022）第00334号](https://picx.zhimg.com/80/v2-7475facab3f2d2eda6faddaca4901d20_720w.png)

![本站提供适老化无障碍服务](https://pica.zhimg.com/80/v2-ccdb7828c12afff31a27e51593d23260_720w.png)
