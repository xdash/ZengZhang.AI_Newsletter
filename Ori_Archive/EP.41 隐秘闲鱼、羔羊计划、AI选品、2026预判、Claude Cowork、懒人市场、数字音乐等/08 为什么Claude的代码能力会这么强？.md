# 为什么Claude的代码能力会这么强？

> 原链: https://www.zhihu.com/question/1914086301076029991  
> 来源: 知乎热榜 · 归档自 EP.41 · 抓取于 2026-08-05  

---

[AI代码](//www.zhihu.com/topic/26433641)

[代码生成器](//www.zhihu.com/topic/27246714)

[Claude3.5](//www.zhihu.com/topic/30171670)

# 为什么Claude的代码能力会这么强？

[圆桌收录Coding with AI](https://www.zhihu.com/roundtable/vibecoding)

有采用什么特别的技术吗？达到这个水平的难度在哪里？显示全部 ​

关注者

**1,180**

被浏览

**1,431,940**

关注问题​写回答

​邀请回答

​好问题 23

​2 条评论

​分享

​

#### 101 个回答

默认排序

[![彼岸樱](https://picx.zhimg.com/v2-b73e1c8adf4ba5b84871aac181d361d7_l.jpg?source=1def8aca)](//www.zhihu.com/people/qiujiangkun)

[彼岸樱](//www.zhihu.com/people/qiujiangkun)

港校学生 量化开发

​ 关注

870 人赞同了该回答

一个原因是砸钱，招人洗数据，测试模型，质量要求很高  
在某平台上，时薪能开到85美元

[https://t.mercor.com/eFal8t.mercor.com/eFal8](https://link.zhihu.com/?target=https%3A//t.mercor.com/eFal8)

声明：以上链接有我的邀请码，可以支持我，不影响自己的收入

[编辑于2026-03-27 11:49](//www.zhihu.com/question/1914086301076029991/answer/2017936113961018930)

​赞同 870​​37 条评论​1161 ​27 

​分享

​

​

[![独元殇](https://picx.zhimg.com/v2-4764145505b1580cae0589fc69cc8c7e_l.jpg?source=1def8aca)](//www.zhihu.com/people/du-yuan-shang)

[独元殇](//www.zhihu.com/people/du-yuan-shang)

www.ccgxk.com 站长（永不用AI写文章，只手打）

​ 关注

航海家 程墨Morgan 等 1098 人赞同

因为 Claude 和其他美国三大模型（Gemini ChatGPT [Grok](https://zhida.zhihu.com/search?content_id=765002961&content_type=Answer&match_order=1&q=Grok&zhida_source=entity)）不一样，不走泛能力，谁都能用，而是将更大的精力，研究怎么砸自己 程序员 的饭碗，研究编码。术业有专攻，所以在 2025 年用它编码，一直是很顺滑。

为了能早日砸的彻底，Anthropic 煞费苦心不少。因此这个 Claude 模型一直被引以为傲的就是写代码了！它里面内置了很多很多东西，比如代码评审、安全评审等等.... 也以编码为核心，推广了很多概念，比如 MCP 等等。

为了让 诸位 更深入感受【为什么Claude的代码能力会这么强？】，我今天使用一个单线故事，来讲一下 Claude 在背后做的几个大事件级的努力。

它是一个很优秀的编码工具，可惜大部分人都 浅尝辄止。更多关于它的玩法，还得去阅读官方文档：

[](https://link.zhihu.com/?target=https%3A//code.claude.com/docs)

* * *

## 提示词仓库

最开始 Claude 依然是在网页上对话框对话。和其他大模型没什么两样。

但是这个办法不行，因为逐渐我们会发现我们会不断重复发相同的提示词，比如 部署的步骤、替换某个文件、根据某某规范评审代码、新加一个 class.... 做这么多重复工作是没必要的。

于是 Claude 整了个【提示词仓库】，也就是 Slash Commands 斜杠命令，把我们事先写好的一个个提示词，放到一个 markdown 文件里。复用，之后我们在用的时候，直接在对话框里 斜杠 ，然后输入命令名称和参数。

![](https://picx.zhimg.com/50/v2-93a0b86bca5053fc6370e28f8db7b236_720w.jpg?source=1def8aca)

![](data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='778' height='840'></svg>)

这对于一个常年敲代码的人，真的友好不少啊！

## 主会话与子代理 sub-agents

后来，我们的 AI Claude 写的代码多了，需要各种评审测试，性能评估，OK ，这个过程会占用很多很多时间，20分钟、1 个小时都绰绰有余。

于是天才们又引入了一个新概念，【主会话 与 子代理】，也就是 sub-agents，就是 你干你的，我干我的，我们互不干扰！

我们甚至可以一种事，多个协助来做，比如一个评审安全、一个评审规范、一个评审性能.... 或者一个负责一个文件夹，这样效率大大提高，多线齐下，10 分钟搞定过去 3 个小时的活。更重要的是，这个不影响主会话的事儿，不受干扰。而这些「小兵」把活儿干完，会把干活儿的结果汇总发给主会话，很有那种老板在办公室里指挥作战一样的感觉。

多任务并行、上下文隔离！

（要注意一件事，子代理 sub-agents 里不能调用 sub-agents，也不能调用 Commands，否则会套娃。 ）

* * *

代码规范，也会一直在更新。而代码规范一般是一个工程项目的核心！一动，其他都得跟着动，各种命令提示词也会跟着动，而且由于提示词都是自然语言写的，维护起来比维护代码还要吃力！现在我们把麻烦移到了提示词维护工程上。

怎么解决这个问题？

## 大模型上下文协议 MCP

天才们又发明了 MCP 这个玩意儿！这样 AI 能从文档系统里自己去查找最新的规范。你只需要部署一个 MCP Server 就可以！

> **MCP（[Model Context Protocol](https://zhida.zhihu.com/search?content_id=765002961&content_type=Answer&match_order=1&q=Model+Context+Protocol&zhida_source=entity)）是一种基于 HTTP 的 JSON-RPC 协议，也就是我们常定义的 JSON 结构的后端接口。**设计好 MCP Server 后，AI 就能通过 Server 接口获取到最新的数据。

当然，MCP 的发明初衷是做这个的，而现在已经发展成了 AI 和各个各界形色各异的软件打交道的工具！不仅可辅助查询规范，还能辅助评审，比如把结果发到 飞书 或者外企更喜欢的 slack 里！

MCP 主要用于接口鉴权的通知推送、少量数据的拉取。

然而，我们又无法确定 MCP 返回的内容，是否会「超载」？或者说浪费大量的 token 数，导致 上下文膨胀事件的发生？

怎么搞？天才想到，把内容先下载下来，先不急着去读，而是分次按需去阅读。

## 特定领域专家 Agent Skills 

这便是【[渐进式披露](https://zhida.zhihu.com/search?content_id=765002961&content_type=Answer&match_order=1&q=%E6%B8%90%E8%BF%9B%E5%BC%8F%E6%8A%AB%E9%9C%B2&zhida_source=entity)】 Agent Skills ！我们下载 规范 是使用 curl 这个纯粹的拉取命令，先把规范下载到 tmp 目录，然后分段读取。

这个 Agent Skills 非常适合 复杂任务处理，大量的上下文处理。当然，它的初衷是解决 MCP 的这个问题，但后台它索性就是啥都能做了，能帮你干活，MCP 当手和脚，剪视频、发文章、发评论、制作各种垃圾东西..... 一种初代 AGI。

Skills 起来后，我个人明显感受到各行各界业界的产能在10倍 ヽ(；´Д｀)ﾉ，甚至100倍增长。 网络的帖子开始海量增加，产研团队的产能开始十倍百倍增长。产能翻百倍，产出的垃圾也翻了百倍。skills有很强的泛化继承能力，而且易迁移，领域专家转化为 skill， 一下就放大了，现在是需要更多领域专家来构建 skill。

* * *

## 插件市场

然而现在你的工作流给搞的非常完美（额... 其实就是整理调试了一大堆可用的 markdown 提示词），能够去用 AI 写很多很多项目了，但如果现在你想搞一个新项目，怎么办？从 0 开始搞吗？

天才们又想到了【提示词共享】这个概念，也就是打包 提示词 成一个插件 plugin。发布到 plugin 市场里，学名叫 [Plugin Marketplace](https://zhida.zhihu.com/search?content_id=765002961&content_type=Answer&match_order=1&q=Plugin+Marketplace&zhida_source=entity)。

用户如果需要最新的提示词，就可以直接在市场里拿到最新的提示词。虽然吧，这些所谓插件，本质是就是一大堆文本文件，但确实好用！

送礼物

还没有人送礼物，鼓励一下作者吧

[编辑于2026-01-17 21:47](//www.zhihu.com/question/1914086301076029991/answer/1993823682188039336)

​赞同 1098​​49 条评论​1773 ​22 

​分享

​

​

收起​

[![小雅](https://picx.zhimg.com/v2-d39b5c31a1f3c7f97afbaa1f3db7ec06_l.jpg?source=1def8aca)](//www.zhihu.com/people/85-22-20-80)

[小雅](//www.zhihu.com/people/85-22-20-80)

学习科学的生活方式

848 人赞同了该回答

Claude Code 用过的都说好，丝滑、懂你，甚至让你写码都感觉上头，国内的DeepSeek v3.1，[Qwen](https://zhida.zhihu.com/search?content_id=747605496&content_type=Answer&match_order=1&q=Qwen&zhida_source=entity), Kimi k2, 智谱GLM-4.5都已经支持了Claude Code的调用，但为什么CC如此好，背后的原因是什么？以及该如何在自己的 Agent/工作流里复刻Claude Code 的体验

分享一篇来自大神博主[Vivek Aithal](https://zhida.zhihu.com/search?content_id=747605496&content_type=Answer&match_order=1&q=Vivek+Aithal&zhida_source=entity) 的好文，这篇文章给出了非常详细的分析和解读，全是干货

![](https://pic1.zhimg.com/50/v2-c50948be49583635ccec6c8d4f5a1d9c_720w.jpg?source=1def8aca)

![](data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='1080' height='936'></svg>)

  


过去几个月，作者抓包分析了 Claude Code 的所有请求，写了篇几千字的硬核指南

文章的核心要点 ：

1.可调试性 >>> 其他一切。 大部分的魔力在于设计出好的（底层和高阶）工具和提示词，让模型自己去发挥。记住，保持简单

2.保持单一循环。 说真的，99% 的场景根本不需要什么框架或多智能体协作。Claude Code 就只有一个主循环，最多带一个分支（而且分支也是它自己）

  1. 3\. [LLM 搜索](https://zhida.zhihu.com/search?content_id=747605496&content_type=Answer&match_order=1&q=LLM+%E6%90%9C%E7%B4%A2&zhida_source=entity) >>> RAG



让模型自己思考怎么搜，而不是简单粗暴地把 RAG 和 LLM 两个系统绑在一起，那种设计太 low 了

要设计好用的底层工具（Bash, Edit, ToDo）和高阶工具（比如 Grep——尽管模型本来也能用 Bash 实现）

  1. 4\. 引导模型主动干活，效果拔群。但尴尬的是，想让它听话，最有效的办法还是在 Prompt 里大喊 “PLEASE THIS IS IMPORTANT”……没错，就这么朴实无华



注意：这篇博文并非 Claude Code 的架构揭秘（市面上已经有一些不错的了）。这篇文章旨在成为构建优秀 LLM 智能体的指南，其基础是作者过去几个月使用和捣鼓 Claude Code 的个人经验

**正文**

Claude Code 是我迄今为止用过的最令人愉悦的 AI 智能体/工作流。它不仅让针对性修改或凭感觉写点一次性工具这类事变得不那么烦人，使用 Claude Code 本身就让我感到快乐。它有足够的自主性来做一些有趣的事情，同时又不会像其他一些工具那样，带来突兀的失控感。当然，大部分的重活儿都是由新的 Claude 4 模型（尤其是其多模态思维能力）完成的。但我发现，即便与同样使用底层模型的 Cursor 或 Github Copilot 智能体相比，Claude Code 在客观上也确实没那么烦人！到底是什么让它这么好用？如果你正在一边读一边点头，那么我将尝试给出一些答案

Claude Code (CC) 的使用体验之所以很棒，是因为它**就是好用** 。CC 的构建基于对 LLM 擅长什么和不擅长什么的深刻理解。它的提示词和工具弥补了模型的不足之处，并帮助它在自己擅长的领域大放异彩。它的控制循环非常简单，易于理解和调试。

CC 一发布，我们 MinusX 就开始使用了。为了探究其内部机制，同事Sreejith 写了一个记录器，可以拦截并记录每一个网络请求。接下来的分析来自我过去几个月的广泛使用经验。这篇文章试图回答这个问题 —— **“是什么让 Claude Code 如此出色，以及你如何在自己的基于聊天的 LLM 智能体中提供类似 CC 的体验？”** 我们已经在 MinusX 中集成了其中大部分经验，也很期待看到你将它们付诸实践！

## **如何构建一个像 Claude Code 一样的智能体**

如果说这篇文章只有一个核心要点，那就是 —— 保持简单，傻瓜原则（Keep Things Simple, Dummy）。LLM 的调试和评估已经够头疼的了。你引入的任何额外复杂性（如多智能体、智能体间的交接、或复杂的 RAG 搜索算法）只会让调试难度增加 10 倍。如果这样一个脆弱的系统侥幸能跑起来，你之后也会因为害怕破坏它而不敢做任何大的改动。所以，把所有东西都放在一个文件里，避免过度复杂的样板代码，并且至少要把它推倒重来几次 :)

以下是从 Claude Code 中学到的，可以在你自己的系统中实现的主要经验：

**Claude Code 在每一个关键节点都选择了架构上的简洁 —— 单一主循环、简单的搜索、简单的待办事项列表等等。抵制过度设计的冲动，为模型构建好约束框架，然后就让它自己“大展身手”吧！这不就是端到端自动驾驶的翻版吗？惨痛的教训，不是吗？**

### **1\. 控制循环设计**

1.1.保持一个主循环

可调试性远远大于复杂的手动调优、多智能体、langchain-graph-node 那一套复杂的玩意儿。

尽管多智能体系统现在非常流行，Claude Code 只有一个主线程。它会周期性地使用几种不同类型的提示词来总结 git 历史、将消息历史合并成一条，或者搞出一些有趣的 UX 元素。但除此之外，它维护的是一个扁平的消息列表。它处理层级任务的一个有趣方式是，通过生成一个自身的克隆作为子智能体来处理，但这个子智能体无法再生成更多的子智能体。这里最多只有一个分支，其结果会作为一个“工具响应”被添加回主消息历史中。

如果问题足够简单，主循环就通过迭代式地调用工具来处理。但如果有一个或多个复杂任务，主智能体就会创建自己的克隆。这种“最多单分支”和待办事项列表的结合，确保了智能体既有能力将问题分解为子问题，又能始终关注最终期望的结果。

我非常怀疑你的应用是否真的需要一个多智能体系统。每增加一层抽象，都会让你的系统更难调试，更重要的是，这会让你偏离通用模型改进的康庄大道。

1.2.在所有事情上都用小模型

CC 发出的所有重要的 LLM 调用中，超过 50% 是发给 `claude-3-5-haiku` 的。它被用来读取大文件、解析网页、处理 git 历史和总结长对话。它甚至被用来生成那个用于提示正在处理中的单词标签——毫不夸张地说，每次按键都会调用！这些小模型比标准模型（如 Sonnet 4, GPT-4.1）便宜 70-80%。所以，大胆地用吧！

### **2\. 提示词**

Claude Code 的提示词极其详尽，充满了启发式规则、示例和那种“敲黑板”式的重点提醒。系统提示词本身约有 2800 token，而工具定义部分则更是占据了高达 9400 token 的惊人篇幅。用户提示词总是包含 `[claude.md](https://zhida.zhihu.com/search?content_id=747605496&content_type=Answer&match_order=1&q=claude.md&zhida_source=entity)` 文件的内容，这通常又有 1000-2000 个 token。系统提示词包含了关于语气、风格、主动性、任务管理、工具使用策略和执行任务等部分。它还包含了日期、当前工作目录、平台和操作系统信息，以及最近的 git 提交记录。

Claude Code 完整提示词：

[https://minusx.ai/blog/decoding-claude-code/#appendix:~:text=Main%20Claude%20Code-,System,-Prompt](https://link.zhihu.com/?target=https%3A//minusx.ai/blog/decoding-claude-code/%23appendix%3A~%3Atext%3DMain%2520Claude%2520Code-%2CSystem%2C-Prompt)

2.1.使用 `claude.md` 来协同处理用户上下文和偏好

大多数代码智能体的开发者都已经形成了一个共识模式，那就是使用上下文文件（也叫 Cursor Rules / `claude.md` / `agent.md`）。Claude Code 在有和没有 `claude.md` 的情况下，其表现有天壤之别。这是一种让开发者传递代码库中无法推断的上下文，以及明确所有严格偏好的绝佳方式。例如，你可以强制 LLM 跳过某些文件夹，或使用特定的库。CC 会在每次用户请求时，发送 `claude.md` 的全部内容。

2.2.特殊的 XML 标签、Markdown 和大量示例

使用 XML 标签和 Markdown 来结构化提示词已经是公认的有效方法。CC 两者都广泛使用。以下是 Claude Code 中一些值得注意的 XML 标签：

`<system-reminder>`：这通常用在许多提示词部分的末尾，用来提醒 LLM 一些它大概率会忘记的事情。例如：
    
    
    <system-reminder>提醒你，你的待办事项列表当前是空的。不要向用户明确提及此事，因为他们已经知道了。如果你正在处理的任务可以从待办事项列表中受益，请使用 TodoWrite 工具来创建一个。如果不需要，请忽略此消息。再次强调，不要向用户提及此消息。</system-reminder>

`<good-example>`, `<bad-example>`：这些标签用来固化启发式规则。当模型面临一个十字路口，有多个看似合理的路径/工具调用可以选择时，它们特别有用。示例可以用来对比不同情况，并清楚地指明哪条路径是更可取的。例如：
    
    
        请通过使用绝对路径来维持当前工作目录的稳定，避免使用 `cd` 命令。只有在用户明确要求时，你才可以使用 `cd`。
        <good-example>
        pytest /foo/bar/tests
        </good-example>
        <bad-example>
        cd /foo/bar && pytest tests
        </bad-example>

CC 也使用 Markdown 来划分系统提示词中的不同部分。示例性的 Markdown 标题包括：

  * • 语气和风格
  * • 主动性
  * • 遵循惯例
  * • 代码风格
  * • 任务管理
  * • 工具使用策略
  * • 执行任务
  * • 工具



### **3\. 工具**

完整的工具提示词 —— 足足有 9400 个 token！

[https://minusx.ai/blog/decoding-claude-code/#appendix:~:text=Claude%20Code%20Tools-,Show,-Related%20Articles](https://link.zhihu.com/?target=https%3A//minusx.ai/blog/decoding-claude-code/%23appendix%3A~%3Atext%3DClaude%2520Code%2520Tools-%2CShow%2C-Related%2520Articles)

3.1. LLM 搜索 >>> 基于 RAG 的搜索

CC 与其他流行的代码智能体的一个显著区别在于它抛弃了 RAG。Claude Code 搜索你的代码库的方式和你自己一样，使用非常复杂的 `ripgrep`、`jq` 和 `find` 命令。由于 LLM 对代码的理解能力非常强，它可以使用复杂的正则表达式来找到任何它认为相关的代码块。有时，它甚至会用一个小模型来读取整个文件。

RAG 理论上听起来不错，但它引入了新的（而且更重要的是，隐藏的）失败模式。该用什么相似度函数？用什么重排器？如何对代码进行分块？如何处理大的 JSON 或日志文件？而使用 LLM 搜索，它只需要看 10 行 JSON 文件就能理解其结构。如果需要，它还可以再看 10 行——就像你一样。最重要的是，这是可以通过强化学习（RL）来优化的——这正是那些大模型公司已经在做的事情。模型完成了大部分的重活儿——理应如此，这极大地减少了智能体中活动部件的数量。另外，将两个复杂的智能系统以这种方式连接起来本身就很丑陋。我最近和一个朋友开玩笑说，这是 LLM 时代的摄像头与激光雷达之争，而且我不是在开玩笑。

3.2 如何设计好工具？（底层工具 vs. 高级工具）

这个问题让每一个构建 LLM 智能体的人夜不能寐。你应该给模型通用的任务（比如有意义的动作），还是应该给它底层的任务（比如打字、点击和 bash 命令）？答案是：看情况（而且你应该两者都用）

Claude Code 既有底层工具（`Bash`, `Read`, `Write`），也有中级工具（`Edit`, `Grep`, `Glob`）和高级工具（`Task`, `WebFetch`, `exit_plan_mode`）。CC 可以用 bash，那为什么还要单独给一个 Grep 工具呢？这里的真正权衡在于，你期望智能体使用该工具的频率 vs. 智能体使用该工具的准确性。CC 使用 [grep](https://zhida.zhihu.com/search?content_id=747605496&content_type=Answer&match_order=2&q=grep&zhida_source=entity) 和 glob 非常频繁，以至于将它们做成单独的工具是合理的，但同时，它也可以为特殊场景编写通用的 bash 命令。

类似地，还有像 `WebFetch` 或 `mcp_ide_getDiagnostics` 这样更高级的工具，它们的功能非常确定。这避免了 LLM 需要执行多个底层的点击和输入操作，让它能保持在正轨上。工具描述中有详尽的提示词和大量示例。系统提示词中还有关于“何时使用某个工具”或如何在两个可以完成相同任务的工具之间进行选择的信息。

**Claude Code 中的工具：**

  * • Task
  * • Bash
  * • Glob
  * • Grep
  * • LS
  * • ExitPlanMode
  * • Read
  * • Edit
  * • MultiEdit
  * • Write
  * • NotebookEdit
  * • WebFetch
  * • TodoWrite
  * • WebSearch
  * • mcp_ide_getDiagnostics
  * • mcp_ide_executeCode



3.3 让智能体管理一个待办事项列表

这样做有很多好处。上下文退化是长时运行的 LLM 智能体中的一个常见问题。它们一开始满怀热情地解决一个难题，但随着时间的推移，它们会迷失方向，最终输出一堆垃圾。

目前智能体设计中有几种方法来解决这个问题。许多智能体尝试过明确的待办事项（一个模型生成待办事项，另一个模型实现它们），或者多智能体交接+验证（PRD/PM 智能体 → 实现者智能体 → QA 智能体）。

我们已经知道，由于种种原因，多智能体交接不是一个好主意。CC 使用了一个明确的待办事项列表，但这个列表是由模型自己维护的。这让 LLM 保持在正轨上（它被强烈提示要频繁参考待办事项列表），同时给予模型在实现过程中随时修正路线的灵活性。这也有效地利用了模型的多模态思维能力，可以即时拒绝或插入新的待办事项

### **4\. 可引导性**

4.1 语气和风格

CC 明确地尝试控制智能体的美学行为。系统提示词中有关于语气、风格和主动性的部分——充满了指令和示例。这就是为什么 Claude Code 在其注释和积极性方面让人感觉很有品味。我建议直接将这部分的大段内容复制到你的应用中
    
    
    > # 一些关于语气和风格的示例
    > - 重要：除非用户要求，否则你不应该在回答中添加不必要的开场白或结尾（比如解释你的代码或总结你的行为）。
    > - 除非用户要求，否则不要添加额外的代码解释摘要。
    >
    > - 如果你不能或不会帮助用户做某件事，请不要解释为什么或者这可能导致什么，因为这会显得说教味太浓，很烦人。
    >
    > - 只有在用户明确要求时才使用表情符号。在所有其他交流中避免使用表情符号。

4.2 “这个很重要” 仍然是顶尖技术

不幸的是，在要求模型不要做某件事方面，CC 并没有更高明的办法。`IMPORTANT`, `VERY IMPORTANT`, `NEVER` 和 `ALWAYS` 似乎仍然是引导模型避开雷区的最佳方式。我期望模型未来会变得更具可引导性，从而避免这种粗暴的方式。但就目前而言，CC 大量使用这种方法，你也应该如此。一些例子：
    
    
    > - 重要：除非被要求，否则不要添加 ***任何*** 注释。
    >
    > - 非常重要：你必须避免使用像 `find` 和 `grep` 这样的搜索命令。请改用 Grep、Glob 或 Task 工具进行搜索。你必须避免使用像 `cat`、`head`、`tail` 和 `ls` 这样的读取工具，请使用 Read 和 LS 工具来读取文件。\n 如果你 _仍然_ 需要运行 `grep`，请停止。总是优先使用 `rg` 来执行 ripgrep。
    >
    > - 重要：你绝不能为用户生成或猜测 URL，除非你确信这些 URL 是为了帮助用户编程。你可以使用用户在消息或本地文件中提供的 URL。

4.3 写下算法（附带启发式规则和示例）

识别出 LLM 需要执行的最重要任务，并为其写出算法，这是极其重要的。尝试角色扮演成 LLM，通过示例进行推演，识别出所有的决策点并明确地写下来。如果能以流程图的形式呈现会更有帮助。这有助于结构化决策过程，并辅助 LLM 遵循指令。一定要避免的是，写一大堆杂乱的“该做”和“不该做”。它们很难被追踪，而且容易相互矛盾。如果你的提示词长达几千个 token，你很可能会无意中写下相互冲突的“该做”和“不该做”。在这种情况下，LLM 会变得极其脆弱，并且无法融入新的用例。

Claude Code 系统提示词中的 `Task Management`、`Doing Tasks` 和 `Tool Usage Policy` 部分，清晰地阐述了需要遵循的算法。这也是一个可以添加大量启发式规则和 LLM 可能遇到的各种场景示例的地方

### **one more thing ：为什么要关注大模型公司的提示词？**

在引导 LLM 方面，很多工作其实是在尝试逆向工程它们的后训练/[RLHF](https://zhida.zhihu.com/search?content_id=747605496&content_type=Answer&match_order=1&q=RLHF&zhida_source=entity) 数据分布。应该用 JSON 还是 XML？工具描述应该放在系统提示词里还是直接放在工具定义里？你应用当前的状态信息呢？

看看它们在自己的应用中是怎么做的，并以此来指导你自己的设计，是很有帮助的。Claude Code 的设计非常有主见，借鉴它有助于形成你自己的设计思路

再次强调，核心要点是**保持简单** 。那些过度封装的脚手架框架弊大于利。Claude Code 真正让我相信，一个Agent可以既简单又极其强大

[发布于2025-09-17 22:47](//www.zhihu.com/question/1914086301076029991/answer/1951779221312627388)

​赞同 848​​26 条评论​1933 ​27 

​分享

​

​

收起​

[Qwen3.8-Max首发尝鲜，个企双版超值优惠低至39元/月起Qwen3.8-Max 首发尝鲜、上新 deepseek-v4-flash，更多模态和旗舰模型共享额度，个企双版本超值优惠低至 39 元/月起，高效开启 AI 生产力查看详情](https://click.qianwenai.com/m/20000000790/?cb=https%3A%2F%2Fsugar.zhihu.com%2Fplutus_adreaper_callback%3Fsi%3D8d4a13b8-1407-4d8b-a432-dd36d2d74f8d%26os%3D3%26zid%3D236%26zaid%3D3777575%26zcid%3D3789508%26cid%3D3789507%26event%3D__EVENTTYPE__%26value%3D__EVENTVALUE__%26score%3D__EVENTSCORE__%26ts%3D__TIMESTAMP__%26cts%3D__TS__%26mh%3D7492365d72e10bec9fe0718b0ca42ec3%26adv%3D645640%26ocg%3D0%26cp%3D0%26ocs%3D0%26aic%3D0%26atp%3D0%26ct%3D0%26ed%3DGiBNJgVzfCMmUW9XFyEvRA8xBGxJICwkOhh0FlwxKw1ZY0gnWzUoISkYf1UXISFcCiIEeh4yNyw9GGJBRCUlVFZ0DHMIc2h3fRVrVwZgfwdZY1YkXSo-fX4DPhIMZ3wEXHYNeQntjUMcdG7cxQ%3D%3D&spu=biz%3D0%26ci%3D3789508%26si%3D602c1410-2363-4dcf-8082-315fbf2f2fa5%26ts%3D1785943280%26zid%3D236)

阿里云的广告 · 3.2 万人浏览

[![Simon Zhang](https://picx.zhimg.com/v2-0adb73ac29a5278ae43136b73da1f81c_l.jpg?source=1def8aca)](//www.zhihu.com/people/simon-zhang-14)

[Simon Zhang](//www.zhihu.com/people/simon-zhang-14)

[​![](https://picx.zhimg.com/v2-27bfcba90e66db79ce8768ab807e017e_l.png?source=32738c0c)](https://www.zhihu.com/question/48509984)

建筑学话题下的优秀答主

[谢邀 @代码蜂巢x](https://www.zhihu.com/people/f1d8b5f7c721127f2f08e88d5cbc8484)[收录于 · 赛萌君的AI笔记](https://www.zhihu.com/column/c_1853351007855190018)

航海家 程墨Morgan 等 388 人赞同

单说模型的话没那么强，至少体感上Opus 4.6并没有显著强于GPT-5.4 High，但A社的产品从设计角度看很有前瞻性。

在那个还是RAG为王的背景下，Claude Code + Sonnet 3.7最先具有相对完备的agent特征，尤其在25年上半年，A社在编程自主性这一块可以说是遥遥领先。

Claude Code的出现很大程度上改变了AI编程的可用性，是第一家在产品上体现了“好马配好鞍”并且获得成功的公司。在CC出来之前，大多数人还只是听说过Cursor这类的AI编程IDE，少数人用过。用过的感受基本是小型项目还行，大型项目根本hold不住，无论是性能还是token消耗上都hold不住。

彼时围绕VS Code生态搭建的一系列插件以及另起炉灶的变种们，面临一个很重要的问题：**你如何让一个大模型能精准地在一个本地代码库里去做搜索定位，并且基于定位去做增删改。**

传统的RAG是条死路，撇开向量化大型代码库需要耗费的漫长时间，光是把原本代码库的层级结构切片，就很难去重构一个高效的搜索空间（因为就算你匹配到了片段，往往它也并不能解决问题，代码库里的文件大多不是独立存在的，而是还有依赖关系）。但同时你又不可能把整个代码库全都灌进当时普遍在64k-128k之间的上下文窗口里，然后指望大模型每次都能完美地执行大海捞针。

那么其中一种解决思路是索引+深度定制的RAG架构。比如Cursor背后的团队没有选择死磕本地算力，而是基于团队代码库高度同源的特点（平均92%相似度），设计了一套基于云端的安全索引复用机制。

在日常编码的增删改查中，Cursor摒弃了全局刷新。它通过默克尔树进行精准的增量比对，每次同步只传输和更新哈希值产生变化的分支，极大减少了数据传输的负担。同时，发生变更的代码会被切分为“语法分块”并在后台异步转化为向量；而未修改的代码块则直接命中缓存，免去了重复的推理计算开销。这套创新的底层架构，成功让AI大模型终于拥有了在复杂企业级代码海洋中精准“捞针”的能力。（对，Cursor虽然不是传统RAG但本质上还在死磕大海捞针）

![](https://pic1.zhimg.com/50/v2-d6fd88dddb332d1204a4a92c34091f21_720w.jpg?source=1def8aca)

![](data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='1920' height='1080'></svg>)

图源：https://cursor.com/blog/secure-codebase-indexing

当开发者在大型项目中启动Cursor时，客户端会通过计算代码库的默克尔树（Merkle tree）生成一个“相似度哈希（simhash）”。服务器端利用这个特征向量，匹配并直接复用团队内部已存在的最佳索引，同时允许客户端在这个后台拷贝的过程中立刻发起语义搜索。

为了解决复用别人索引可能带来的代码泄露与越权访问风险，Cursor创造性地引入了内容访问证明（[Proving access](https://zhida.zhihu.com/search?content_id=773784921&content_type=Answer&match_order=1&q=Proving+access&zhida_source=entity)）机制：客户端必须上传完整的哈希树，服务器在返回搜索结果前会进行严格的比对校验；如果客户端无法通过哈希值证明本地实际拥有该文件，包含该文件的搜索结果就会被直接拦截并丢弃。

![](https://pic1.zhimg.com/50/v2-25c24b504c5b237fd4d34d32f276cd96_720w.jpg?source=1def8aca)

![](data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='1920' height='1080'></svg>)

图源：https://cursor.com/blog/secure-codebase-indexing

这一套打法确实从某种程度上让AI编程工具达到了可用的标准，在工程实践上也很有巧思，但它更像是一套严谨的工作流框架，而非依靠大模型本身的自主和智能。当时我用Cursor的体验就是模型只是在既定的框架下做有限的动作，而驾驭这辆马车不跑偏不翻车还需要高强度的人机交互，我需要看diff，要review和approve，并且每次都是这样，在心力消耗上并不小。

相比之下，A社推出的 Claude Code 则走了一条截然不同的道路。它放弃了在 IDE 里做重度定制的“微操”与“死磕”，而是选择回归开发者最初始、也最硬核的形态——命令行（CLI），从而真正将大模型的能力推向了“agent”的完全体。

![](https://picx.zhimg.com/50/v2-2698fd61c685996266d1cd6d10aa65b2_720w.jpg?source=1def8aca)

![](data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='1920' height='1080'></svg>)

图源：https://www.anthropic.com/news/claude-3-7-sonnet

形态上的差异，直接带来了自主性的云泥之别。

在 Cursor 里，出于对大模型胡乱改代码的担忧，开发者往往不敢轻易开启完全放任的模式，只能手动逐一审查并批准每一个动作。 Claude Code 极其聪明地设计了“渐进式授权”机制。当它提出要执行命令或修改时，不只有“是”和“否”，还有一个极其关键的选项——“是，并且下次执行此类操作时不再询问”。

![](https://pic1.zhimg.com/50/v2-3072e8e8dfd4cddca12e77b60cb47e13_720w.jpg?source=1def8aca)

![](data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='3840' height='2161'></svg>)

图源：https://www.anthropic.com/engineering/claude-code-sandboxing

这种设计让大模型像一个真实的人类实习生一样：刚开始你盯着它做，随着它一次次展示出正确的操作，它就在“赚取”你的信任 。最终，你可以彻底放权，让它真正实现完全的自主运行，而不是让你持续充当一个微观管理者。

在跑测试和进行版本控制时，Claude Code 的终端原生属性让它如鱼得水。它能极度自然地运行终端命令来执行测试，并根据测试反馈毫无摩擦地自主迭代修复代码。

除了写代码，Claude Code 的设计格局远超传统编码工具——它允许使用者将 AI 从“一问一答的问答机”变成“可复用的系统”。用户可以用极其轻量的 Markdown 文件为它设定上下文和指令，并自定义专属的斜杠命令。

至于后面更新版本里的sub-agents多路并行更是又往前了一大步。每个 agent 都有独立的上下文窗口，互不干扰且同速推进。这直接将原本线性的开发时间降维压缩，实现了效率的成倍增长。

* * *

agentic coding的成功不能只归功于模型的进步，它背后是运行环境、工具调用、权限管理等多个因素叠加带来的胜利。

![](https://picx.zhimg.com/50/v2-4230dc5e3ff794b53116d942261d26ac_720w.jpg?source=1def8aca)

![](data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='1356' height='644'></svg>)

图源：https://russellluo.com/2025/09/demystifying-claude-code-agentic-coding

今天A社能在编程领域拥有如此出众的声誉成为诸多友商的对标竞品，离不开它的产品背后的设计思维一直在尝试推动模型之外的边界，Claude Code是这样，[Claude Cowork](https://zhida.zhihu.com/search?content_id=773784921&content_type=Answer&match_order=1&q=Claude+Cowork&zhida_source=entity)上也有类似的影子。

送礼物

还没有人送礼物，鼓励一下作者吧

[发布于2026-03-19 15:54](//www.zhihu.com/question/1914086301076029991/answer/2017992237389232094)

​赞同 388​​25 条评论​499 ​11 

​分享

​

​

收起​

[![一直很懒的小强](https://picx.zhimg.com/v2-bf1f7ff64679fefa04a8c41c859406ae_l.jpg?source=1def8aca)](//www.zhihu.com/people/45-73-72-24)

[一直很懒的小强](//www.zhihu.com/people/45-73-72-24)

[谢邀 @代码蜂巢x](https://www.zhihu.com/people/f1d8b5f7c721127f2f08e88d5cbc8484)

444 人赞同了该回答

Claude的代码能力强,不是因为Anthropic用了更多的算力或更大的数据集。

说句实话,在这两个维度上,OpenAI和Google都不会落后。

真实的原因其实更有意思，Anthropic做了一个大多数模型公司都不愿意做的选择:放弃做"全能型选手",反而把所有的注意力都砸到了编程这一个领域。  
  
术业有专攻。这句老话在AI时代有了全新的含义。

这个差异体现在三个层面上。  
  
首先是定位。Claude从一开始就不是想要成为一个"你什么都能问"的通用AI。

OpenAI和Google做产品的时候,心里装的是:我怎么让全球10亿人都用上我的AI。

Claude的逻辑完全不同:我怎么让100万程序员离不开我。

这看似是个小数字,但这个选择改变了一切——当你只需要服务一个高度专业化的用户群体时,你可以对他们的需求进行极致的理解。  
  
其次是训练数据的处理逻辑。

一般的LLM训练,从GitHub爬下来的代码就拿来用。

但Anthropic显然经历过一个认知的转变:GitHub上的代码质量参差不齐。

他们可能建立了一套复杂的内部评估系统,不仅判断代码能否运行,还要评估代码的架构合理性、风格规范性,甚至可维护性。

这等同于在训练数据层面就进行了一次严格的筛选和净化。这个选择的代价很高,但效果也很高。  
  
方向确定了,技术就是窗口。Claude的代码能力不是基于某一个卖点或某项技术来告诉你的,而是多项设计决策协同作用的结果。  
  
上下文窗口是最直观的那个。Claude现在为上一个体验提供100万token起步,最新的两个版本甚至逼近到了少说也得200万token起。很多人一看这个数字就想:这就是内存比较大。但对于程序员来说,这是一个完全不一样的存在。  
  
想象一下重构一个大型系统的场景。今天的云原生微服务架构,一个单一业务模块、一套依赖、配置文件、API文档、数据库schema,简简单单就是几十万token。

以前用旧模型的时候,这种条件下我们得自己去裁剪每一个文件、每一个函数,辛苦地拼接这个、拼接那个,战战兢兢地诌求一个AI会看到全局。

Claude的优势是:你的整个[monorepo](https://zhida.zhihu.com/search?content_id=767481510&content_type=Answer&match_order=1&q=monorepo&zhida_source=entity)、数据库schema、API文档、五周的git日志,我一次性全部丢给你。  
  
还有一个就是目前最好的编程工具，Claude code，是的，它已经火出地球了，并且这个工具还对Claude的模型做了额外的优化，如果大家用的是Claude 模型，效果会好很多，就拿现在大厂的模型一一去适配就会发现。

而且现在使用Claude code本身也不是很难，CC中转或用国内的模型，都可以，也可以自己去订阅会员。

相关阅读：

[](https://zhuanlan.zhihu.com/p/2004613207357158833)

[](https://zhuanlan.zhihu.com/p/1992313721415046720)

贴一个具体案例。上周我们组里一个资深后端在整修一个老旧的业务系统。Java 8写的，整个项目拉下来就是一个贝博洞。他想把它迁移到Go，并且上云原生。  
  
以前需要两个月。他直接用了Claude Code。

我要特别说一下，这是Anthropic推的终端工具。如果说Cursor是IDE上的神，那Claude Code就是终端里的上帝。  
  
他直接在终端敲了一条命令，让Claude Code扫描整个Java项目，理解业务逻辑，然后生成Go代码生成、打包、[Dockerfile](https://zhida.zhihu.com/search?content_id=767481510&content_type=Answer&match_order=1&q=Dockerfile&zhida_source=entity)和Kubernetes的yaml文件。  
  
最离谱的是，整个过程中遇到一个依赖库在Go里没有对应的版本，Claude Code没有瞎编，而是自己在GitHub搜了一个功能类似的库，用适配器模式重新兼容接口。  
  
这体现的正是核心能力：代理工作流。  
  
Claude的强，在于它好像会深度遣好程序员的思维。一起设计、然后编程、最后审查。

Claude Opus 4.5搭配[Computer Use](https://zhida.zhihu.com/search?content_id=767481510&content_type=Answer&match_order=1&q=Computer+Use&zhida_source=entity)功能，现在已经可以像人一样操作电脑了。

它能自己开浏览器查文档、自己跑测试用例、自己看报错日志、然后自己修bug。

[编辑于2026-02-10 18:04](//www.zhihu.com/question/1914086301076029991/answer/2000259488280756921)

​赞同 444​​30 条评论​422 ​10 

​分享

​

​

收起​

[![广告](https://pic1.zhimg.com/v2-cde2d2b5b191c7b00fcf9572d74ca7cb_720w.webp?source=d6434cab)](https://www.volcengine.com/activity/ark?utm_source=7&utm_medium=zhihu&utm_term=vg_zhihu_libao_webjx_dmx19k9&utm_campaign=0&utm_content=dbdmx_19k9&spu=biz%3D0%26ci%3D3634141%26si%3Ddf912b09-3d4d-48fb-81ad-4732330d6b42%26ts%3D1785943282%26zid%3D3)

相关问题

[大家都说 Claude 4.6 写代码远超竞品，国内开发者怎么才能低成本、稳定地用上？](/question/2020818929019299208) 3 个回答

[有没有不需要折腾网络，直接能用原版 Claude 写代码的工具？](/question/2020131577192034927) 1 个回答

[程序中文件如何安排和给代码文件起名字？](/question/23863699) 1 个回答

大家都在搜

换一换

[笔试第一称被第二名花钱劝弃考442 万](/search?q=%E7%AC%94%E8%AF%95%E7%AC%AC%E4%B8%80%E7%A7%B0%E8%A2%AB%E7%AC%AC%E4%BA%8C%E5%90%8D%E8%8A%B1%E9%92%B1%E5%8A%9D%E5%BC%83%E8%80%83&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)热

[鸿蒙智行回应「竹知了」事件363 万](/search?q=%E9%B8%BF%E8%92%99%E6%99%BA%E8%A1%8C%E5%9B%9E%E5%BA%94%E3%80%8C%E7%AB%B9%E7%9F%A5%E4%BA%86%E3%80%8D%E4%BA%8B%E4%BB%B6&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)热

[DeepSeek 被称为大模型「斩杀线」354 万](/search?q=DeepSeek+%E8%A2%AB%E7%A7%B0%E4%B8%BA%E5%A4%A7%E6%A8%A1%E5%9E%8B%E3%80%8C%E6%96%A9%E6%9D%80%E7%BA%BF%E3%80%8D&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)热

[婚外胚胎案丈夫称已销毁胚胎349 万](/search?q=%E5%A9%9A%E5%A4%96%E8%83%9A%E8%83%8E%E6%A1%88%E4%B8%88%E5%A4%AB%E7%A7%B0%E5%B7%B2%E9%94%80%E6%AF%81%E8%83%9A%E8%83%8E&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)新

[人生选择模拟器347 万](https://event.zhihu.com/renshengxuanze/)活动

[周杰伦 刘若雪346 万](/search?q=%E5%91%A8%E6%9D%B0%E4%BC%A6+%E5%88%98%E8%8B%A5%E9%9B%AA&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)新

[长鑫拒绝苹果降价要求345 万](/search?q=%E9%95%BF%E9%91%AB%E6%8B%92%E7%BB%9D%E8%8B%B9%E6%9E%9C%E9%99%8D%E4%BB%B7%E8%A6%81%E6%B1%82&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)新

[同济大学取消教师长期聘任345 万](/search?q=%E5%90%8C%E6%B5%8E%E5%A4%A7%E5%AD%A6%E5%8F%96%E6%B6%88%E6%95%99%E5%B8%88%E9%95%BF%E6%9C%9F%E8%81%98%E4%BB%BB&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)热

[患癌妻子申请销毁婚外胚胎遭拒329 万](/search?q=%E6%82%A3%E7%99%8C%E5%A6%BB%E5%AD%90%E7%94%B3%E8%AF%B7%E9%94%80%E6%AF%81%E5%A9%9A%E5%A4%96%E8%83%9A%E8%83%8E%E9%81%AD%E6%8B%92&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)热

[美国拟禁止进口中国光模块314 万](/search?q=%E7%BE%8E%E5%9B%BD%E6%8B%9F%E7%A6%81%E6%AD%A2%E8%BF%9B%E5%8F%A3%E4%B8%AD%E5%9B%BD%E5%85%89%E6%A8%A1%E5%9D%97&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)热

[![广告](https://picx.zhimg.com/v2-e83a36f123c337da1a596ccbe236d786_720w.webp?source=d6434cab)](https://www.zhihu.com/topic/2060805443815830388/hot?spu=biz%3D0%26ci%3D3794853%26si%3D1e506336-df93-42bc-9257-2d90c0af9729%26ts%3D1785943282%26zid%3D4)

 

帮助中心

服务热线：400-919-0001[帮助与客服](/help-center)[联系我们](/contact)更多

 

举报中心

违法和不良信息举报：010-82716601[我的举报](/community?source=zhihu_default)更多

 

关于知乎

[知乎个人信息保护指引](/term/privacy)[知乎协议](/term/zhihu-terms)[下载知乎](https://www.zhihu.com/app/)[Investor Relations](https://ir.zhihu.com)网站资质信息更多

* [京ICP证110745号](https://tsm.miit.gov.cn/dxxzsp/) · [京ICP备13052560号-1](https://beian.miit.gov.cn/) · [京公网安备 11010802020088 号](http://www.beian.gov.cn/portal/registerSystemInfo?recordcode=11010802020088) · [京网文[2025]0422-132 号](https://www.zhihu.com/certificates) · [药品医疗器械网络信息服务备案（京）网药械信息备字（2022）第00334号](https://picx.zhimg.com/80/v2-7475facab3f2d2eda6faddaca4901d20_720w.png)

![本站提供适老化无障碍服务](https://pica.zhimg.com/80/v2-ccdb7828c12afff31a27e51593d23260_720w.png)
