# Cherry Studio 复盘：从 Chat 到 Agent，一款「套壳」开源产品如何推倒重来？

> 原链: https://mp.weixin.qq.com/s?__biz=MzY5ODQwMTkxNA==&mid=2247516610&idx=1&sn=3a5f267d9580c01610be5bd389ff18c6&chksm=f524ee4587be60d7fd349819e293be621ec677b9d2c48a572563577729406bfcd6f8ec8702ab  
> 来源: 公众号 · 归档自 EP.69 · 抓取于 2026-08-27  

---

![图片](https://mmbiz.qpic.cn/sz_mmbiz_gif/5icxfcvT9Umj7xQFlVRNLVdicYzwKh4W3eaKCopIyU3gzLxhELh1qyS8CwlNlgpOmPia1SlAMOXSju1HmQ8kdQzB8QGpflkgVxtA82AoIVJBbk/640?wx_fmt=gif&from=appmsg&tp=webp&wxfrom=5&wx_lazy=1#imgIndex=0)「套壳」是 Cherry Studio 最大的标签。但这个「壳」，在过去一年成了 GitHub 上增长最快的 AI 桌面应用之一。Cherry Studio 最初的目标很明确，就是帮用户在不同大模型之间自由切换，做一个更好用的聊天客户端。

但当行业从 Chat 转向 Agent，团队发现原本这套为聊天设计的架构，撑不起任务执行的未来，于是决定推倒重来。

Cherry Studio 2.0 不是一次简单的版本升级。它的产品定位从「更好用的 AI 聊天工具」转向「个人 Agent 平台」，底层架构也全部重写。与此同时，原来的 1.x 版本还得照常运转，每天仍有大量用户在线使用。团队把这个过程形容为「边开飞机边换发动机」。

围绕 Agent 重新做一遍产品，该从哪里开始？在 Cherry Studio 创始人 Yinsen 看来，2.0 更像是一次重新定义自己的过程，比起单纯连接模型的工具，Cherry Studio 希望逐渐成为个人和组织使用 AI 的基础设施。

他认为，Agent 的核心价值是替用户管理复杂度。系统内部可以越来越复杂、具备越来越多能力，但用户面对的产品应该更简单。这意味着，Cherry Studio 的改变必须贯穿整个产品，从底层架构、交互方式，再到 Agent 之间的协作机制。

以下是 Yinsen 对这次产品重构的完整复盘，经 Founder Park 编辑整理。

  


⬆️关注 Founder Park，最及时最干货的创业分享  


* * *

Founder Park 正在持续寻找值得被看见的 AI 团队与项目。

我们将通过「AI 产品市集」、内容报道、社群分发等方式，帮你触达早期用户、获得真实反馈，以及建立关键连接。

如果你正在做 AI 相关的事，欢迎和我们聊聊。 ![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

* * *

## 01

## Chat 只是过渡阶段，

## Agent 开始完成任务

Cherry Studio 最开始诞生的时候，其实没有想得那么复杂。

2024 年，AI 产品的主要形态还是 Chat。无论是 ChatGPT、Claude，还是各种国内大模型应用，本质上都是围绕一个聊天窗口展开。用户提出问题，模型生成答案，这是一种非常自然、也非常容易理解的交互方式。

所以 Cherry Studio 最初的目标很明确，做一个更好用的 AI 模型客户端。

我们希望用户可以更自由地选择模型，不被限制在某一个平台中。不同模型有不同特点，有些擅长代码，有些擅长推理，有些更适合中文场景，有些在速度和成本方面更有优势。用户应该能够根据自己的需求，选择最适合自己的模型。

我们也希望降低多模型使用的门槛。Cherry Studio 出现之前，如果用户想体验多个模型，通常得打开不同网站、注册不同账号、适应不同交互。对技术用户可能不算什么，但对大量普通用户来说，这本身就是很高的使用成本。

早期 Cherry Studio 解决的问题很简单，让用户更方便地使用 AI。架构设计也是围绕 Chat 展开的，聊天记录、模型配置、会话管理，是产品最核心的数据。这套设计在当时完全合理，因为它解决的就是一个聊天客户端的问题。Cherry Studio 1.x 的很多选择，都是在这个阶段形成的。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

但随着 AI 能力的快速发展，我们逐渐意识到，Chat 可能只是 AI 应用的一个过渡阶段。聊天最大的特点，是由用户主动驱动。用户知道自己想问什么，然后向 AI 提出问题，等待它给出回答。但真实工作中，很多需求是一件需要完成的事情，并不是一个明确的问题。

比如，「帮我整理一下公司的历史资料，分析市场趋势，然后生成一份报告」。这不是一次回答就能完成的。AI 需要理解目标、读取资料、搜索信息、调用工具，再根据中间结果不断调整方向，最后才能形成一个可用的结果。

这就是 Agent 和 Chat 的区别。Chat 的核心是生成一个答案，Agent 的核心是完成一个目标。

**当 AI 开始承担任务执行的角色，软件的设计方式也必须发生变化。** 过去的软件更多围绕功能展开，用户找到功能、点击按钮、完成操作。Agent 软件则围绕目标展开，用户表达需求，Agent 理解目标，再调用各种能力完成任务。

未来软件的竞争点不一定是谁提供了更多按钮，而在于谁能够更好地理解用户意图，并组织各种能力完成工作。

过去一年，Cherry Studio 加入了知识库、MCP、联网搜索、文件处理、绘图和翻译等能力。表面上看，它们是不同的功能模块，但背后的方向是一致的，就是让 AI 获得更多完成任务的能力。

当然，回头看 Cherry Studio 1.x，我们也必须承认一个问题。随着能力不断增加，产品复杂度也在不断上升。用户看到的是越来越多的入口、配置项和概念，但我们真正希望实现的，是让 Agent 帮助用户管理这些复杂能力，减少用户学习和掌握新工具的负担。

这也是为什么 Cherry Studio 必须进入 2.0。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

  


## 02

## 旧架构支撑不起 Agent，

## 必须边开飞机边换发动机

很多用户看到 Cherry Studio 2.0，最直接的感受是界面变了。但实际上，这次最大的变化在底层架构。

原因很简单，原来的架构是为 Chat 设计的，未来我们需要支撑 Agent，两者对数据的要求完全不同。

在 Chat 场景中，一条消息基本就是用户输入和模型输出。系统主要保存聊天记录，管理不同会话。但 Agent 场景下，一次任务可能涉及非常复杂的数据关系。用户提出需求之后，Agent 可能需要调用多个工具、读取多个文件、查询知识库、执行多个步骤，并根据执行结果决定下一步行动。

整个过程从一次性的「输入」和「输出」，变成一个持续运行的任务。系统既要记录最终结果，也要保存执行过程、上下文关系、工具状态、任务状态以及恢复能力。缺少可靠的数据基础，Agent 就很难稳定运行。

Cherry Studio 1.x 早期的数据架构很符合当时的需求。那个阶段，我们主要解决聊天问题，数据模型相对简单，很多状态管理方式更偏向客户端应用。但随着产品逐渐演进，数据越来越多，模块间的关系越来越复杂，功能之间的耦合也越来越明显。继续在旧架构上增加功能，短期可能更快，长期却一定会越来越困难。

所以，Cherry Studio 2.0 进行了底层重构。我们重新设计了数据存储方式，引入数据库，也重新规划了数据生命周期和模块之间的关系。用户可能不会直接看到这些变化，但它决定了 Cherry Studio 未来能不能成为一个真正的 Agent 平台。在 Agent 时代，数据本身就是能力的一部分。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

这次 Cherry Studio 2.0 最大的挑战，其实并不在技术本身，是在一个已经拥有用户、生态、历史包袱的开源项目中，完成一次底层重构。

我们经常用一句话来形容这个过程，边开飞机边换发动机。

如果是一个没有用户的新项目，重新设计架构并不困难。工程团队可以停下来，把所有问题重新梳理一遍，再按照理想状态重新开始。但 Cherry Studio 已经不是一个实验项目。每天都有大量用户在使用，有人在工作中依赖它，也有人持续向我们反馈问题。我们不能简单地停掉旧版本，把所有精力投入新架构。

与此同时，我们又很清楚，如果继续沿着旧架构堆叠功能，未来一定会遇到越来越大的问题。

这是一个很典型的工程矛盾。一方面，产品需要快速响应用户需求，需要持续增加新的能力。另一方面，底层架构又得足够稳定，才能支撑未来的发展。很多时候，软件项目的问题不是某一个功能设计错了。**随着产品目标变化，早期正确的选择逐渐不再适合新的阶段。**

Cherry Studio 1.x 的架构没有错，它很好地支撑了我们从一个聊天客户端成长起来。但当目标从 Chat 变成 Agent，系统面对的问题已经发生了变化，我们只能选择承担这次重构的成本。

这几个月，我们一边维护 1.x 用户体验，一边建设 2.0 新体系。旧的问题要解决，新能力要开发，底层架构还在不断调整。有些时候，工程团队会感觉像是在同时维护两个产品。

也正是在这个过程中，我们越来越明确接下来要解决的问题。不再只是「如何让用户更方便地使用 AI」，还有「如何让 AI 主动帮助用户完成事情」。这两个阶段看似连续，但背后的产品理念已经发生了变化。

  


## 03

## 产品越来越复杂，

## 用户应该越用越简单

过去一段时间，不少用户问过我们，Cherry Studio 为什么不专注做一个简单、稳定、轻量的 Chat 客户端？还有一种更直接的反馈是，Cherry Studio 是不是越来越「臃肿」了？

从用户体验角度来看，这个反馈是成立的。随着一年多的发展，Cherry Studio 从最开始的模型聊天工具，逐渐增加了知识库、MCP、联网搜索、翻译、绘图、Agent 和代码能力。如果把这些能力全部直接展示给用户，产品自然会越来越复杂。1.x 中越来越多的入口、配置项和概念，也说明我们在能力建设和产品整合之间，还没有完全找到平衡。

但我们认为，解决这个问题的方向并不是简单地减少功能。如果未来 AI 的方向确实是 Agent，那么 AI 软件内部承载的能力只会越来越多。一个真正强大的 Agent，不可能只连接一个模型、一个工具或者一种数据。

未来的方向应该是，**系统内部越来越复杂，但****用户体验****越来越简单** 。我们非常认可 Codex 等产品的演进方式，好的产品是在内部能力增强的同时，让外部交互越来越简单。用户看到的是更少的操作，系统完成的是更多事情。

这也是我们认为 Agent 最重要的价值之一，Agent 本身就是复杂度管理层。过去，用户需要自己理解什么时候用搜索，什么时候用知识库，什么时候调用工具，什么时候切换模型。未来，这些决策应该由 Agent 完成。

对于技术用户来说，选择不同软件、配置不同工具、理解不同系统之间的关系，可能不是太大的问题。但大量普通用户不想学什么是 MCP、什么是 Embedding、不同 Agent 框架又有什么区别。他们只希望告诉 AI，「帮我完成这件事。」

「一个程序只做一件事」这个原则没有过时，但它的实现方式在变化。未来可能依然需要大量专业工具，一个负责搜索，一个负责代码执行，一个负责图片处理。区别在于，人不再需要亲自组合它们，Agent 来负责组合。工具应该越来越专注，Agent 应该越来越通用。

Cherry Studio 做了很多事情，同时也明确不做一些事情。我们没有做视频生成社区，没做情感陪伴，没做群聊，也没做类似酒馆的角色社区。不是因为这些方向没有价值，是它们不符合 Cherry Studio 当前的核心定位。

我们的目标是成为一个能够最大化 AI 能力的工作入口，不是一个装下所有 AI 功能的大杂烩。知识库、搜索、工具和 Agent 是围绕这个目标的自然延伸，其他的不属于当前想解决的问题。

Cherry Studio 和很多商业 AI 产品还有一个重要区别。很多商业产品可以把复杂基础设施隐藏起来，用户注册账号就能直接使用。但是 Cherry Studio 选择的是开源和 BYOK，允许用户选择自己的模型、连接不同服务商、管理自己的数据。这带来了自由，也带来了选择模型、配置 API、处理 Embedding、安装依赖和运行 Agent 等复杂性。

如果我们只是把这些复杂性原样暴露给用户，开源的价值反而会降低。Cherry Studio 要做的是，保持开放的同时降低使用门槛。让用户拥有选择权，但不必承担所有技术成本。

  


## 04

## 围绕 Agent，

## 重新思考产品应该长什么样

当我们重新思考 Cherry Studio 的未来，另一个重要问题是，Agent 到底应该是什么？

很多产品会把 Agent 理解为一个更聪明的聊天机器人，或者在聊天窗口里增加一个自动执行按钮。但我们认为，这不是 Agent 的核心。Agent 真正重要的地方，是它改变了软件和用户之间的关系。

过去的软件大多由用户驱动。用户打开软件、寻找功能、填写参数，然后等待结果。软件提供能力，但用户必须知道如何使用这些能力。Agent 的目标，是让用户从「操作软件」变成「委托任务」。用户提出目标，Agent 理解目标，然后决定如何完成。

这背后需要的不只是一个模型，是一整套能力体系，包括模型、工具、上下文、执行环境和任务管理。因此，Cherry Studio 2.0 对 Agent 的建设，远不止简单增加一个聊天入口，它在重新构建整个 AI 工作流。

我们也不认为 Agent 应该绑定在某一个模型或某一个框架上。过去，很多 Agent 方案主要围绕 Anthropic 生态展开，因为 Claude 在工具调用、代码执行、任务规划等方面做了很多探索。但就像今天的软件不会绑定某一个数据库一样，未来的 Agent 生态也应该是开放的。

所以 Cherry Studio 2.0 开始**支持不同的 Agent 框架** 。包括轻量、灵活，更适合日常任务场景的 Pi Agent。我们也会支持 Claude Agent SDK 这样的成熟框架，用于更复杂、更强大的任务场景。不同框架有不同优势，Cherry Studio 更希望成为承载这些能力的平台，不限制用户只能使用某一种实现方式。

除了通用 Agent，我们也一直在探索 Coding Agent 方向。最初 Cherry Studio 中的代码工具叫 Code Two。在 2.0 中，我们将它升级为 Code Mate。我们希望它能从代码工具变成编码搭档。

第一阶段，Code Mate 可以让 Cherry Studio 成为统一的模型入口。很多用户已经在使用 Claude Code、Codex CLI、OpenClaw 等 Coding Agent，但这些工具通常需要单独配置模型、管理环境。Cherry Studio 可以作为统一入口，把已经接入的模型能力提供给这些 Agent，减少重复配置。

Code Mate 更大的价值在未来。**除了给 Agent 提供模型，Cherry Studio 更应该成为 Agent 的管理中心。** 用户可以在 Cherry Studio 中提出一个任务，由不同 Agent 分别分析需求、编写代码、测试和审查结果，Cherry Studio 负责协调，让它们形成完整的工作流。

这也是我们对于未来软件形态的一个判断。未来的软件不一定是用户打开很多应用，再亲自完成信息流转。更多时候，**用户面对的是一个统一入口，由 Agent 调度背后的模型和工具。**

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

在 Cherry Studio 2.0 的设计讨论中，我们也重新思考了一个很具体的交互问题。输入框中的 @，到底应该关联什么？

过去很多聊天软件习惯 @ 会话，因为在 Chat 时代，聊天记录就是核心资产。用户想引用之前的讨论，把上下文传递给当前对话。

但进入 Agent 时代，会话会越来越多，Agent 却相对稳定。用户真正想调用的，通常是某一种能力，不是某一次历史聊天。例如让代码 Agent 处理一个问题，让研究 Agent 调查一个主题，让写作 Agent 修改一篇文章。所以**未来更自然的交互，可能是 @Agent。**

传统助手切换和 Agent 调度不是一回事。聊天模式下切换助手，本质上是在当前会话里更换一个回答者。真正的 Agent 应该拥有自己的上下文和工作空间。如果用户让另一个 Agent 接手任务，合理的方式是当前 Agent 整理任务信息，把必要上下文交接给另一个 Agent。另一个 Agent 在自己的环境中继续工作，最后返回结果。

这更像现实世界中的团队协作。两个人合作，不是一个人跑到另一个人的电脑前继续操作。他们需要整理资料、完成交接，再各自在自己的环境里推进工作。

这也是 Cherry Studio 未来需要完善 Agent 间通信机制的原因。不同 Agent 有独立会话，同时能通过消息协作。2.0 重新建立的数据库体系，为这种多 Agent 协作打下了基础。未来我们可以管理 Agent 的 session、搜索历史任务、发送消息，让不同 Agent 之间完成任务交接。

  


## 05

## 本地模型用来补齐基础能力，

## 不是云端模型的简单替代

在 Cherry Studio 的发展过程中，本地模型一直是很多用户关注的话题。不少用户通过 Cherry Studio 连接 Ollama 使用本地模型。对他们来说，这代表了一种自由、可控和隐私保护的方式。

但我对本地大语言模型的判断一直比较谨慎。不是说本地模型没有价值，是需要区分不同类型的模型，以及它们在 AI 产品中承担的角色。

目前，如果希望在普通设备上运行一个能够媲美 GPT、Claude 等先进的大语言模型，仍然存在现实限制。模型能力依赖大量参数和计算资源，云端背后庞大的算力基础设施是普通个人设备很难匹配的。

其次是使用成本。较大的本地模型需要更高性能的硬件支持，包括更大的内存、更强的 GPU、更好的散热能力。这意味着很多用户为了运行一个模型，需要购买额外硬件，还得接受设备性能下降和功耗增加。

如果普通用户只是想要更好的 AI 助手体验，本地运行一个大语言模型目前未必是最优选择。换句话说，**本地大语言模型短期内并不是云端先进模型的简单替代。**

但这并不意味着本地模型没有价值。相反，我们认为本地模型在 AI 产品中有非常重要的位置，只是它承担的角色可能和很多人的预期不同。

随着 Cherry Studio 的发展，我们开始把问题从「能不能在电脑上运行一个本地大模型」，换成「哪些 AI 能力应该放在本地」。

很多影响 AI 使用体验的关键能力，并不需要几十亿、几百亿参数的大模型。Embedding、OCR、ASR、数据脱敏等能力，规模更小，更像 AI 产品的基础设施，但它们对产品是否易用影响很大。

以知识库为例。很多用户第一次接触知识库时，会遇到一个理解门槛：为什么聊天模型不能直接读取文件？为什么还需要一个叫 Embedding 的模型？

知识库背后涉及文本向量化。系统需要先通过 Embedding 模型把用户文档转换成可供检索的数据结构，再根据问题找到相关内容，交给语言模型生成回答。

目前很多云端服务商都提供 Embedding API，比如 BGE-M3、Qwen3 Embedding 等模型服务。理论上用户可以直接调用，但实际使用中存在不少问题。

首先是理解成本。对于普通用户来说，大语言模型是一个容易理解的概念，它负责聊天、写作、回答问题。但 Embedding 是更底层的概念，用户需要理解为什么知识库需要额外模型、不同模型有什么区别、怎么配置 API。这都增加了产品使用门槛。

其次，不是所有模型服务商都提供完整能力。很多用户使用 DeepSeek 官方 API，它提供非常强大的语言模型能力，但目前并没有对应的 Embedding 服务。这意味着用户即使已经配置好了模型，也可能无法顺畅使用知识库。

更重要的是，知识库是长期数据资产。用户积累的知识库内容不应该依赖一个随时可能变动的外部服务。我们已经遇到过类似情况，比如某些服务商调整 API 参数或者更换模型版本，就可能导致用户原来的知识库出现异常。因为向量数据和 Embedding 模型之间存在关联，模型不可用或接口变了，用户可能没法重新生成自己的知识库。对于基础能力来说，这种不确定性并不理想。

所以，Cherry Studio 2.0 选择提供离线 Embedding 模型。用户可以下载模型，在本地完成知识库创建，不依赖第三方服务，模型版本更稳定，数据也更可控。我们使用的 Embedding 模型规模大约是 0.6B，不需要高端 GPU，也不会明显影响现代设备的性能。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

这也体现了我们对于本地模型价值的重新理解。我们不希望用户在电脑上运行一个庞大的语言模型，去替代云端 GPT 或 Claude，而是**通过一些轻量模型，把 AI 产品中关键但容易被忽视的基础能力补齐。**

OCR 也是一个典型例子。在 Cherry Studio 2.0 里我们优先用系统能力，比如 macOS 新版本就提供了一些系统级模型服务，可以直接做 OCR。系统不具备的话，我们再用离线模型补充。比如在 Windows 环境下使用 Paddle OCR 等开源模型，用户不用注册第三方服务、申请 API Key 或充值，下载模型就能获得对应能力。

类似的思路，未来还会继续扩展到数据脱敏和 ASR。

经过这些探索，我们对本地模型的定位越来越清晰。本地模型未来不会简单替代云端大模型，更可能成为 AI 产品中的基础设施。云端大模型负责复杂推理和高智能任务，本地小模型负责稳定、低成本、隐私、安全的基础能力。两者是互补而非竞争关系。

因此，Cherry Studio 未来引入本地模型会坚持几个原则：模型规模尽量小、资源消耗尽量低、普通设备可以运行、跨平台稳定。我们不会为了展示「本地 AI」，强行让用户运行一个庞大的模型。对大多数用户来说，真正重要的是 AI 能不能帮他完成工作，不是电脑里装了多少参数的模型。

  


## 06

## 让 Coding Agent 帮忙多写几行代码，

## 还不等于 AI 原生开发

除了产品本身的变化，Cherry Studio 2.0 还有一个非常重要的变化，我们的研发方式也在发生变化。

过去的软件开发，本质上是人与人的协作。产品经理定义需求，设计师设计方案，工程师实现功能，测试人员验证质量。这是过去几十年软件行业形成的一套成熟流程。但随着 AI Coding 和 Agent 的发展，软件开发正在进入一个新的阶段。AI 不再只是辅助工具，它开始参与软件生产过程。

在 Cherry Studio 内部，我们已经大量使用 AI 辅助开发，包括代码生成、代码 Review、问题分析和测试辅助。但比起「让 AI 帮我们写更多代码」，更重要的变化是让软件项目本身变得更容易被 AI 理解。

过去，一个新人加入项目，需要通过阅读代码、文档和沟通，逐渐建立对项目的理解。未来，一个 Agent 加入项目，也需要类似的上下文。它需要知道这个项目解决什么问题，代码结构是什么，设计原则是什么，哪些地方可以修改，哪些边界不能破坏。

所以我们重新整理了项目里的 Agent.md、Contributor 文档和工程架构说明。这些文档不仅是写给人看的，也是未来给 Agent 看的。

我们认为，未来的软件开发不会简单变成「AI 替代程序员」。更可能出现的是一种新的协作方式，人类负责目标、判断和创造，Agent 负责执行、分析和协作。软件工程师的价值，也会逐渐从编写每一行代码，转向设计系统、定义边界和判断结果。

在我们的理解里，使用几个 Coding Agent 还不足以称为 AI 原生开发，它指向的是整个软件生产方式的变化。

这种变化也在推动 Cherry Studio 从社区驱动走向更体系化的维护。项目早期的快速发展，很大程度上得益于开源社区。大量用户参与测试、提交问题、贡献代码，给项目带来了很强的生命力。但项目快速增长之后，代码质量的一致性、长期维护的稳定性、不同贡献者之间的理解差异也在逐渐显现。

随着团队逐渐稳定，我们开始在社区贡献之外建立更体系化的开发流程，包括更明确的架构规范、更完善的测试体系、更稳定的问题反馈机制，以及更持续的工程投入。2.0 的底层重构也解决了一部分历史包袱，很多旧模块在这次过程中重新设计甚至重新实现。

Cherry Studio 2.0 还会探索产品反馈 Agent。对于一个多模型、多平台、多 Agent 的产品来说，Bug 和兼容问题很复杂。过去，用户知道「哪里不能用」，开发团队却经常不知道「为什么不能用」，因为系统、模型、接口、错误信息和操作步骤等关键上下文没有被完整收集。

未来用户遇到问题，不一定需要自己收集日志、复制报错、整理环境描述。他可以直接告诉 Agent：「这里出问题了。」Agent 帮助收集相关信息、分析可能原因，再整理成开发团队可以直接处理的问题报告。这也是 Agent 在产品生命周期中的另一种应用。在帮助用户工作的同时，也帮助产品团队理解用户。

  


## 07

## 重做一遍之后，

## Cherry Studio 想成为人与 AI 协作的入口

回顾 Cherry Studio 的发展，我们其实经历了几个阶段。

最开始，我们解决的是如何让用户更方便地使用不同 AI 模型。后来，我们开始探索如何让 AI 理解用户自己的知识。再后来，我们开始思考如何让 AI 主动完成任务。

这三个阶段，对应了 AI 应用的三个入口：模型入口、知识入口和任务入口。Agent 正是连接它们的关键。

Cherry Studio 2.0 之后，我们不会停止探索。GitHub roadmap 上还有大量功能等待实现。未来我们会继续完善 Agent 能力、多 Agent 协作、移动端体验、企业能力、更多本地模型支持，以及更强的数据和知识管理。

但更重要的是，我们希望保持一个原则：不要为了增加功能而增加功能。每一次迭代，都应该降低用户的负担。

过去的软件演进，很多时候意味着不断增加能力。未来优秀的软件，或许是在能力越来越强的同时，让用户看到的东西越来越少。用户不需要知道背后有多少模型、调用了多少工具、任务经过了多少步骤。只要表达目标，然后得到结果。这也是 Cherry Studio 2.0 最核心的意义。

过去，我们是在做一个 AI 聊天工具。现在，我们希望打造一个真正的 Agent 平台。未来，我们希望 Cherry Studio 成为人与 AI 协作的新入口，让 AI 从回答问题走向真正帮助用户完成工作。Cherry Studio 还在路上。但我们相信，Agent 时代的软件形态，才刚刚开始。

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

![图片](data:image/svg+xml,%3C%3Fxml version='1.0' encoding='UTF-8'%3F%3E%3Csvg width='1px' height='1px' viewBox='0 0 1 1' version='1.1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg stroke='none' stroke-width='1' fill='none' fill-rule='evenodd' fill-opacity='0'%3E%3Cg transform='translate\(-249.000000, -126.000000\)' fill='%23FFFFFF'%3E%3Crect x='249' y='126' width='1' height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)**更多阅读**

# [ Evolvent AI 胡梦康：Agent 可能会被模型吃掉，但帮助 Agent 进化不会](https://mp.weixin.qq.com/s?__biz=MzY5ODQwMTkxNA==&mid=2247516586&idx=1&sn=49d174cee784f32c86e9fafd5338a62e&scene=21#wechat_redirect)

# [Stripe 花 100 亿买 OpenRouter，模型 Router 会成为一个新赛道吗？](https://mp.weixin.qq.com/s?__biz=MzY5ODQwMTkxNA==&mid=2247516581&idx=1&sn=b28218c04da5f5fb3543b6cddf1850fb&scene=21#wechat_redirect)

# [DeepSeek V4 Flash 可以交付结果了，Agent 开始拼 Harness 了](https://mp.weixin.qq.com/s?__biz=MzY5ODQwMTkxNA==&mid=2247516565&idx=1&sn=979f8c13c2d392310fcdd3226e226d5d&scene=21#wechat_redirect)

# [MiniMax 怎么做 Agent：Model-Harness 协同只是第一步，还有 Inference-Harness 协同](https://mp.weixin.qq.com/s?__biz=MzY5ODQwMTkxNA==&mid=2247516541&idx=1&sn=a31f3207b86e3c5a439572fb10263138&scene=21#wechat_redirect)

# [Manus 重新独立：这七个月一直没停下，但通用 Agent 的牌桌已经挤满了玩家](https://mp.weixin.qq.com/s?__biz=MzY5ODQwMTkxNA==&mid=2247516533&idx=1&sn=83693ec130ad7dc066121c4a8b335b87&scene=21#wechat_redirect)

  
转载原创文章请添加微信：founderparker
