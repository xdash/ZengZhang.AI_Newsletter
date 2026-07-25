### 「模型行为工程师」这个混合角色（数据科学 + 产品管理 + 提示工程）比任何单一角色都重要。

[

![范冰 XDash's avatar](https://substackcdn.com/image/fetch/$s_!gLs0!,w_36,h_36,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F55cb259b-c4c4-4c79-8bfe-a4a47eef9d1a_940x940.jpeg)

](https://substack.com/@xdash)

[范冰 XDash](https://substack.com/@xdash)

Apr 23, 2026

1/ 前一阵子一打开候选内容库，满屏的「小龙虾」；最近风向转了，都在明里暗里讨论「蒸馏某人/职能」（尤其今天早上看到 **[小扎演都不演了](https://mp.weixin.qq.com/s/XBu7KrhqZlmvfIJqmFbyFg)**）。此情此景，让我很想化用经典，吟诗一首——

> 开始他们蒸馏翻译、运营、程序员、打字员，我没说什么，因为我不是干这行的；
> 后来他们蒸馏产品经理、分析师、设计师、编剧、作家、演员、销冠，我还是没说什么，因为我觉得与我无关；
> 接着他们蒸馏教师、律师、医生、会计、记者，我依然没说什么，因为我暂时还能站着；
> 最后他们来蒸馏我时，环顾四周，已经没有人能替我说话了。
> —— 只剩下 Agent 对我冷冷嗤笑。

2/ 最近基友开发的笔记产品 **flomo 迎来了六周年**，近期相继推出了（或即将推出）认知地图、随机漫步 3.0、主题回顾、AI 洞察、记忆档案、MCP 接口等强力功能。感兴趣的可以 **[看这篇了解下](https://mp.weixin.qq.com/s/rVYCMTPTVdTXxkVtfQ13zQ)**。

顺带推荐创始人之一 Light 自己的小报童专栏（小报童也是他们做的）：**[SmallTalk·第三季](https://xiaobot.net/p/smalltalk2025?refer=af038a9b-c8fe-4429-9eee-f96a3211eec4) 。**主要写对创业、投资和人生的偏见，预计更满 100 篇。这年头好的商人都是哲学家。

OK，以下是本期的内容 ——

* * *

##### ▪️CASE 案例

### **[Notion’s Token Town: 5 Rebuilds, 100+ Tools, MCP vs CLIs and the Software Factory Future — Simon Last & Sarah Sachs of Notion](https://podwise.ai/dashboard/episodes/7761465) （附 YouTube 视频）**

##### via Simon Last & Sarah Sachs

Notion 正在用「软件工厂」模式构建 AI 智能体，目标只有一个：**成为企业工作的核心记录系统。**

他们踩了 5 次坑才明白：构建可靠 AI 智能体的关键，不是写越来越复杂的提示词，而是让工具定义**从「僵化的少量示例」转向「目标导向」**。这意味着工具所有权可以分散到不同产品团队，而不是集中在一个神秘团队手里。

（Notion 最近的 PR 很多嘛，除了这篇以外，Colossus 给它们也 **[写了篇深度内部报道《Inside Noteion》](https://colossus.com/article/inside-notion/)**，懒得看长文可 **[看我的 Quick Memo](https://mp.weixin.qq.com/s/F_VSTI7jDDpbBI9LbkKzeA)**；以及还有个 YouTube **[探访新办公室的视频](https://youtu.be/4qkyxm4jppc?si=rQpG7oLgESpjL7_T)**也给我刷到了。）

几条经验：

-   最有效的工程领导力，是培养团队**乐于删除自己代码**的文化；

-   产品开发**优先「演示而非备忘录」**，用内部使用发现边缘情况；

-   「模型行为工程师」这个混合角色（**数据科学 + 产品管理 + 提示工程**）比任何单一角色都重要；

-   **渐进式披露**是智能体系统的关键架构要求，一次性暴露过多工具会损害模型性能并增加 Token 成本；

-   最成功的 AI 驱动工作流，**让产品本身成为记录系统，智能体通过读写共享数据库协调**，而非依赖自定义消息协议

评估也需要分层：**单元测试用于持续集成，「成绩单」评估用于发布准备，30% 通过率的「上限」评估用于识别未来能力**。

对企业 AI 而言，最高杠杆活动不是训练定制基础模型，而是**优化外部循环——即工具质量、验证系统和框架**。

**智能体系统应设计为「为顶尖学生授课」，优先考虑高级用户能力和可解释性，而非过度简化的界面**。

**延伸阅读：**

-   **[Notion Custom Agents 复盘：三年重写 5 次，Notion 历史上最成功的新功能之一](https://mp.weixin.qq.com/s?__biz=Mzg5NTc0MjgwMw==&mid=2247523808&idx=1&sn=0a6aea0c1f3f9c5c6e86eff9592fd30b)**

* * *

### **[Slax Note AI Coding 产品重构的复盘（整理版 v2）](https://mp.weixin.qq.com/s?__biz=Mzg5NDY4ODM1MA==&mid=2247486037&idx=1&sn=5244a718cc5b59d433b0518c9b49ee84&chksm=c154f12d8a669530997283c4489300ddb94c43530ecb0ecd13d8f30a1edccbd6f48db67a4b8e&mpshare=1&scene=1&srcid=0422Icj84btRmQfCYyLMxmza&sharer_shareinfo=c486fbf73cfed9e3a5c44624ee77e656&sharer_shareinfo_first=c486fbf73cfed9e3a5c44624ee77e656)**

##### via 吴鲁加

[

![](https://substackcdn.com/image/fetch/$s_!SObE!,w_1456,c_limit,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faf4efafb-cc03-4c12-88d9-f859d100f258_639x632.heic)

](https://substackcdn.com/image/fetch/$s_!SObE!,f_png,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faf4efafb-cc03-4c12-88d9-f859d100f258_639x632.heic)

知识星球创始人，分享了最近一次用 AI 重构项目 Slax Note 的过程复盘。

这不是一次轻松的胜利。团队经历从兴奋、怀疑、受挫到调整方法并重建信心的过程。他们的起点是探索一种激进的新开发方式：由产品或设计师借助 AI 直接生成代码并验收，而非层层转交研发。

**成功的关键前提是「spec 驱动」的 AI coding——研发工程师先将复杂系统的知识提炼为结构化规格文件，使 AI 的生成行为有据可依，从而降低幻觉与非技术角色的门槛**。（工程师不抵触/焦虑吗，这不就是被萃取了吗，哈哈..）

真正的价值在于验证了产品角色可深度参与实现。AI 擅长快速搭建框架与界面修补，但在涉及真实业务链路与复杂环境时，对规格、验证与代码审查的要求反而更高。**后期拉开差距的是发现根因与控制回归的能力。**

这次实验的本质不是 AI 替代研发，而是将研发经验沉淀为可协作的流程。

**延伸阅读：**

-   来自该团队员工视角的另一篇：**[完全不懂编程的我们，通过 Vibe coding 重写了一个 App（感受篇）](https://mp.weixin.qq.com/s?__biz=MzA4OTA3ODA1Mg==&mid=2648684287&idx=1&sn=011302bd8ef35a980d6412d5c22ddff3&chksm=8989d76dd0f8c97419f7488af7f02e9dced545856766e5ec316a04543a907bf5a9ab18103069&mpshare=1&scene=1&srcid=0423ZduRgWFkTzDxRMq4fti7&sharer_shareinfo=4396268834a166cc1527b1b70850845f&sharer_shareinfo_first=1df3d74da13b45cc95025c6ca2e471c6)**

* * *

### **[孩子王 CTO 王海龙：我们只用 AI 做「脏活累活」，就狂赚 30 亿](https://mp.weixin.qq.com/s?__biz=MzIxNTAzNzU0Ng==&mid=2654904869&idx=2&sn=aa67cbe432e673bec25752f4f5f4c060)**

##### via 混沌学园

一篇孩子王 CTO 的分享，肯定有 PR/卖货的成分，但即便如此，篇幅还是挺长，里面能启发实业和创业的细节还是有一些的。

比如，孩子王的思路很清晰：**企业落地 AI 需遵循三大底层逻辑——寻找「大齿轮」场景、将私有数据作为护城河、培养懂技术与业务的 AI 架构师。他们通过「数字训战官」AI Agent 高频考核上万名员工，并利用「销冠人脑蒸馏」将隐性经验显性化。**

他们自称成功根基是十年构建的「单客经济」数字化底座——利用**母婴行业高度可建模的数据预判用户需求**，服务 9600 万会员的全生命周期。

* * *

##### ▪️OPINION 观点

### **[Multi-Agents: What’s Actually Working](https://x.com/walden_yan/status/2047054401341370639)**

##### via walden\_yan

[

![Image](https://substackcdn.com/image/fetch/$s_!judM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F838bf580-c280-4064-9204-4ceef94867f6_768x593.png "Image")

](https://substackcdn.com/image/fetch/$s_!judM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F838bf580-c280-4064-9204-4ceef94867f6_768x593.png)

多智能体系统经过十个月的发展，已从「普遍不实用」转向「在特定协作模式下真正可行」。

作者分享了一些对行业的观察预测、数据调研和实战心得。

* * *

### **[关于 AI 硬件出海，他们讲了点不写进 BP 的实话](https://mp.weixin.qq.com/s?__biz=MzU5Mjg5MjQ5Ng==&mid=2247521046&idx=2&sn=db82a8f0be0847796e21e65adb5d16b8)**

##### via 非凡产研

AI 硬件全球化的成败关键，往往不在炫酷的模型参数，而在于对物理世界复杂性的务实应对。

四个不同赛道的 CEO 讲了实话：

-   Demeter Robot 为规避国内农业非标场景的改造难题，直接出海欧美利用其标准化农场。本质是**「用中国的 PPI 对标欧美的 CPI」**；

-   ALLTIME 万物时 发现欧美用户**对治愈系「赛博盘串」的接受度超预期，产品定位在跨文化中自然分化为「宠物陪伴」或「解压美学」**；

-   Wavenote 为追求极简体验，不惜投入高昂成本将两个按键合而为一，揭示了硬件为抹平用户体验门槛所付出的残酷取舍；

-   Sipeed 矽速科技 直面供应链现实，指出**「内存比金子还贵」的地缘政治与成本压力**，迫使团队加快透明化开源以应对猜忌。

贯穿这些案例的潜台词是：技术决定上限，而**中国成熟的供应链体系与灵活的本土化策略，才是支撑 AI 硬件出海活下去的生存底线**。

* * *

### 随便看看：

-   **[《GEO 行业数据造假手册：一个卧底交付员的自述》](https://mp.weixin.qq.com/s?__biz=MzA4MTc3NzY0Mg==&mid=2652350634&idx=1&sn=3aceb92b1c7da92fe2f217fa2a6a30a0&chksm=85fd2936404025cec929ef53adaacdc7cc105b97f672be728cdd06fcc4e02ac6344b247c9e30&mpshare=1&scene=1&srcid=0423RswG2tMMShiZNo7Z0Bmk&sharer_shareinfo=2c094a6d9b89d4339ba7d176e49804d4&sharer_shareinfo_first=2c094a6d9b89d4339ba7d176e49804d4)：**GEO 行业如何通过操纵数据计算标准来系统性美化效果报告？两个关键骗术：其一是**推荐率的邪修算法**，将同一词包内各关键词的推荐率简单相加而非求平均，使 1% 的真实推荐率在报告中呈现为 100% 甚至更高；其二是**用设备数偷换搜索次数**，通过模糊分母定义将极低的真实曝光率放大为可观的推荐率。

-   **[《爱奇艺热搜背后，揭秘「买脸」这门生意》](https://mp.weixin.qq.com/s?__biz=MzkyNjU2ODM2NQ==&mid=2247627962&idx=3&sn=1e3b89b2d546f6e22e2057afc258b396&chksm=c3ed677b9f82e28b5f18df4484072bd0abb04df4d85bfb28723cd912a67ad7c5cf7c6622d978&mpshare=1&scene=1&srcid=0423A5huXNov2KfGftu7qB7w&sharer_shareinfo=08637b88d7e471faf593e47fc0407057&sharer_shareinfo_first=08637b88d7e471faf593e47fc0407057)：**讲了 AI 视频行业从盗用肖像到购买授权的商业化转型及其伴随的复杂乱象。原来**买个脸的授权是 200 元/剧**。

-   **[《一个 「龙虾技能市场」，凭什么拿下 AI 增速第一？》](https://mp.weixin.qq.com/s?__biz=MzU5Mjg5MjQ5Ng==&mid=2247520955&idx=1&sn=75e1d0d8a1f30258b497e7776861f2e0)**：增长最快的产品普遍在推进 AI **从「回答问题」到「直接交付结果」**，比拼的是能否一站式完成工作。Web 增长越来越依赖「产品力 + 分发力 + SEO/内容引流」的三件套组合，许多上榜产品同时扮演着工具、内容站和流量入口的角色。

### 适合个人上手的教程/评测/资源：

-   **[《单篇 100 万阅读文章，如何用 AI 做好内容创作？》](https://mp.weixin.qq.com/s?__biz=MjM5NDI4MTY3NA==&mid=2257499594&idx=1&sn=17e88fef7b93351862192177da19ae6c&chksm=a42ba4e3dfc6339ff2f41fa3675ad88813d20cfc863f98c0a0c97bb0b40dfe00ace92ec439ac&mpshare=1&scene=1&srcid=0416zougfkJCeilLcSs8tJvP&sharer_shareinfo=e6a3d12aa13a2d094334d3ef6e8925e4&sharer_shareinfo_first=e6a3d12aa13a2d094334d3ef6e8925e4)：**好内容有明确标准且可量化，流量权重公式为：**选题占 50%，标题占 20%，开头占 10%，正文占 20%**。六条标准：逻辑需层层递进而非平铺；开头须反常识制造冲突；正文需持续设置阅读钩子；信息密度要高；要提供可操作的解决方案；整体需有独特的节奏与风格。

-   **[《神级 CLI 写作大法》](https://mp.weixin.qq.com/s?__biz=MjM5ODU1MzQzOQ==&mid=2451429482&idx=1&sn=94d7761944d4616fd9805ac28ebd0214)：**将创作者内在的认知与审美通过命令行工具转化为一条可执行的内容生产线。这套方法将单篇文章的创作时间从 120-240 分钟压缩至 25-40 分钟，本质是将时间从「与 AI 拉扯」重新分配到「注入个人判断」上。

-   **[《我挖到了 Kimi K2.6+Hermes 的六个神技巧，这下多 Agent 24h 组队干活真成了》](https://mp.weixin.qq.com/s?__biz=Mzg3MTk3NzYzNw==&mid=2247506550&idx=1&sn=2b47083a68ffa57f3120f41615916e55)：**作者通过实践验证了 Kimi K2.6 模型与 Hermes Agent 框架的结合，能够构建稳定、高效的多智能体协作系统，从而替代 Claude 等成本高昂的方案。

-   **[《实测 Claude Design：小白也能做出专业级设计｜附最全玩法+官方实用技巧》](https://www.ifanr.com/1662860?utm_source=rss&utm_medium=rss&utm_campaign=)：**最近该工具的发布直接冲击了 Figma 等传统设计工具的市场地位，关键在于实现了从提示词到可交付方案的端到端输出，无需人工干预。

-   **[《拿虚构产品，测真实 AI｜K2.6 加持后，Kimi Agent 能干到哪一步》](https://mp.weixin.qq.com/s?__biz=MzAxMDMxOTI2NA==&mid=2649107353&idx=1&sn=5741cda209ad0c4dd87c93a5b7a77f7c)：**通过虚构产品 iShout 的测试案例，评估 K2.6 模型升级后 Kimi Agent 在复杂商业任务中的真实能力上限。

-   **[《给龙虾装上八爪鱼 MCP 后，我把亚马逊选品流程全跑通了》](https://mp.weixin.qq.com/s?__biz=MzI5Mzk5MzA5Mg==&mid=2247487301&idx=1&sn=a35f0f2f6a41cd1bed883c8e73f0a519&chksm=ed31291d26c19afa913f67cd2214f191360c22d9e9b64ce610db81df3f4cf510b2b1043d583b&mpshare=1&scene=1&srcid=0420CL84aCcfgbw0Kb0pNcsj&sharer_shareinfo=f79ea8eacb190cfe279c92aedba3f977&sharer_shareinfo_first=f79ea8eacb190cfe279c92aedba3f977)：**通过将八爪鱼采集器的 MCP 服务接入 AI 工作流，解决跨境电商亚马逊选品的数据抓取与分析难题。

-   **[《我给 Claude Code 做了个 AI 硬件监工》](https://mp.weixin.qq.com/s?__biz=MzU0MDk3NTUxMA==&mid=2247496535&idx=1&sn=a1bb9ae0c6cde5f915410b1cdeb580e4)：**通过模块化硬件为 AI 编程助手构建一个物理交互界面，实现了多会话状态墨水屏看板、物理按键审批带来的仪式感与审慎，以及蓝牙远程控制带来的空间自由。

[

![Mia's avatar](https://substackcdn.com/image/fetch/$s_!lwgR!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa5a6a3ad-d871-45f2-b6a2-8631abf35fce_1280x1706.jpeg)

](https://substack.com/profile/342765327-mia)

1 Like

[](https://substack.com/note/p-195210688/restacks?utm_source=substack&utm_content=facepile-restacks)
