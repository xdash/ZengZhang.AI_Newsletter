# From Tool to Teammate: How AI is Reshaping Front-End Development — A First-Person Perspective from Google I/O

> 原链: https://aicraftlab.substack.com/p/from-tool-to-teammate-how-ai-is-reshaping  
> 来源: aicraftlab.substack.com · 归档自 EP.21 · 抓取于 2026-08-06  

---

# From Tool to Teammate: How AI is Reshaping Front-End Development — A First-Person Perspective from Google I/O

*There is **a Chinese version** of this article after the English version.*

本文英文版之后附有中文版，请下拉查看。

A few days ago, I attended the Google I/O conference. Ever since, one thought has been echoing in my mind: the Web development we once knew is undergoing a seismic shift.

No longer are developers limited to calling “cloud-based LLMs” via REST APIs. Much like JavaScript and CSS, AI is becoming a *native layer inside the browser itself*, woven directly into our daily workflows.

After exploring the key booths in the Web section and attending a hands-on workshop, I witnessed four transformative forces reshaping our work:

- **Web AI**
- **Developer Experience & Modern CSS**
- **Privacy & Data**
- **Multi-Agent Orchestration**

# Revolution 1: Browsers as Powerful AI Platforms

In the Web AI section, two distinct yet complementary approaches to on-device AI emerged:

## Approach 1: “Built-in Brain” with Gemini Nano

Gemini Nano is an API **built directly into Chrome**, allowing developers to invoke it with zero setup. Its advantages are compelling:

- **Zero latency** : Runs directly on the user’s device with no server round-trip.
- **Privacy-preserving** : All data stays local—nothing goes to the cloud.
- **Offline-capable** : Works even without an internet connection.

Already-integrated APIs include:

![](https://substackcdn.com/image/fetch/$s_!Qdt6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F80a18941-0b15-4e46-8669-a7d99c3b10f7_1834x616.png)

🔗 Dev Docs: [https://developer.chrome.com/docs/ai/built-in-apis](https://developer.chrome.com/docs/ai/built-in-apis)*(Some APIs are still in limited preview and require early access.)*

🔗 To enable Gemini Nano in Chrome:

- Go to `chrome://flags/#optimization-guide-on-device-model` , enable`BypassPerfRequirement` .
- To enable Summarization API, visit `chrome://flags/#summarization-api-for-gemini-nano`

Quick test result:

![](https://substackcdn.com/image/fetch/$s_!Cb-8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9010d9ab-bf35-486e-9610-b238f30a7b28_1702x670.png)

**Limitation**: The model is general-purpose and cannot be fine-tuned.

## Approach 2: “Tailor-Made Brain” with Gemma + WebGPU

For developers needing customization, Google offers the **Gemma + WebGPU** stack. Gemma is an open lightweight model family by Google, and WebGPU is the browser-native engine that powers it.

**What is WebGPU?**

WebGPU is a modern browser API that allows JavaScript to directly tap into the GPU for high-performance parallel computing—critical for running AI models efficiently. It’s the performance bridge between LLMs and the web.


This setup lets you download Gemma models, fine-tune them with your own data, and build domain-specific multimodal AI apps—all within the browser.

🔗 Guide: [LLM Inference in the Browser](https://ai.google.dev/edge/mediapipe/solutions/genai/llm_inference/web_js)

## Harmony: Convenience Meets Customization

These two approaches are not mutually exclusive—they complement each other beautifully:

- Use **Gemini Nano** as a plug-and-play “convenience store” for 80% of tasks.
- Use **Gemma + WebGPU** as a “custom kitchen” to build your competitive edge for the other 20%.

# Revolution 2: DevTools + Modern CSS — Developer Experience Reimagined

If Gemini Nano and Gemma are giving browsers their “brains,” then **DevTools + Modern CSS APIs** are giving developers superpowers to work more efficiently and creatively.

## 1. DevTools: Your AI Pair Programmer

Old debugging workflows were clunky:

Edit code in IDE → Refresh browser → `console.log()` spam → Sometimes use Playwright screenshots.

Now, with **Gemini integrated directly into Chrome DevTools**, that workflow is radically improved.

You can:

- Select any HTML element visually.
- Have a conversation with the AI assistant about it.

**Example interaction:**

**You (clicking a square** `div` **that should be a wheel):**

“I’ve selected this element. It’s currently a square, but it should be a perfect circle. Can you help?”

**AI Assistant:**

“Sure. To make it a circle, you’ll need to set `border-radius` to 50%…”


With one click, the suggestion can be applied—and even **saved back to the local source file**!

🔗 Example: [cinemai.devtools.hangar](https://chrome.dev/cinemai/devtools/hangar)

![](https://substackcdn.com/image/fetch/$s_!ANpw!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F579bd5a0-0285-4e1c-a0a3-b075fce25729_2314x1434.png)

## 2. Modern CSS APIs: From Styling to Interaction

This complements DevTools beautifully. Since the AI assistant modifies mostly **HTML and CSS**, the modern CSS APIs now offer far greater expressiveness, enhancing both development speed and UI elegance.

Key APIs:

- **View Transitions API** : Smooth page-to-page transitions.
- **Scroll-driven Animations** : Animations that sync directly with scroll behavior.

These enable interactions that once required JavaScript, now achievable purely with CSS—more performant, cleaner, and aligned with **progressive enhancement** principles.

🔗 Docs:

**Takeaway**: The golden trio of **DevTools + AI + Modern CSS** is reshaping front-end workflows:

- CSS is more powerful
- DevTools helps you apply it intelligently

# Revolution 3: The Future of Privacy and Data

This revolution is about **trust and data responsibility** at the heart of the web.

## Privacy Sandbox: Building a Cookie-less Future

At the booth, I explored the **Privacy Sandbox**, Google’s initiative to replace traditional third-party cookies in response to growing privacy concerns.

It’s not a single product, but a **suite of browser APIs** that enable attribution, interest-based targeting, and personalization **without compromising user privacy**.

🔗 Developer Site: [privacysandbox.com](https://privacysandbox.com/intl/en_us/open-web/)

This lays the foundation for a **healthier and more trustworthy web** over the next decade.

# Multi-Agent Orchestration Made Simple with Google ADK

I also joined a hands-on **Multi-Agent Workshop** powered by Google’s **Agent Development Kit (ADK)**. We explored agent orchestration with minimal code and live browser dashboards:

- **Sequential Agents** :
  - Agent 1 (Researcher): Pulls info from Wikipedia.
  - Agent 2 (Writer): Writes a short story.
  - Agent 3 (Critic): Reviews the output.
- **Parallel Agents** :
  - Each agent performs a unique task simultaneously and merges the result.

🔗 Docs: [Google ADK Intro](https://developers.googleblog.com/en/agent-development-kit-easy-to-build-multi-agent-applications/)

I also compared it to LangGraph:

![](https://substackcdn.com/image/fetch/$s_!m3z6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8af0e58c-a049-4baa-a0d5-73adb103fcac_1222x1108.png)

# Final Thoughts: The AI-Powered Web Is Taking Shape

Each of these revolutions pushes the boundaries of the Web:

- **AI-integrated browsers** make intelligent capabilities instantly accessible.
- **DevTools + CSS** redefine how we craft experiences.
- **Privacy Sandbox** guards the foundation of trust.
- **Multi-agent frameworks** make orchestrating intelligence easier than ever.

These are not isolated events—they are coming together to shape a future where **everyone can orchestrate, and everyone can use AI**.

I left Google I/O with one core question:

As the lines between Web and AI blur, **how should we redefine “programming” and reimagine the new developer workflow**?


**以下是中文版**

前几天，我参加了Google I/O大会，结束之后，脑子里只有一个念头：我们所熟知的 Web 开发正在经历一场根本性的变革。开发者不一定只能通过 REST API 远程调用的“云端大语言模型”，正像 JavaScript 和 CSS 一样，AI成为浏览器内核的一部分，成为我们日常开发工作流中触手可及的伙伴。

在逛了 Web 展区的几个核心 Booths，并参加了一场 Workshop 后，我看到了三股正在发生、并将彻底改变我们工作的力量：**Web AI**、**开发者体验与现代 CSS**、**隐私与数据的未来**、**多智能体编排**。

# 革命一：浏览器成为强大的 AI 平台

在 Web AI 展区，我看到了两种截然不同却又相辅相成的端侧 AI 实现路径。

## 路径一：开箱即用的“内置大脑” — Gemini Nano

这是一种可以直接调用的、内置在 Chrome 中的 Gemini Nano API。它的优势显而易见：

- **零延迟** ：模型在用户设备本地运行，无需服务器往返。
- **保护隐私** ：用户数据保留在本地，不发送到云端。
- **离线可用** ：即使没有网络连接，AI 功能依然可以工作。

目前已经集成的 API 一览：

![](https://substackcdn.com/image/fetch/$s_!sIWZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5c1a67c3-0e43-40b3-a7a9-fa821fe1e517_2122x1102.png)

开发者文档：[https://developer.chrome.com/docs/ai/built-in-apis?hl=zh-cn](https://developer.chrome.com/docs/ai/built-in-apis?hl=zh-cn) （部分功能仍在内测阶段，需要申请权限）

另外，使用前需要先在 Chrome 中开启相关配置，详情可参考：[chrome configuration setting instructions](https://browserai.danduh.me/?utm_source=medium&utm_medium=post&utm_id=initial)

示例操作：

- 启用 Gemini Nano, 打开 `chrome://flags/#optimization-guide-on-device-model` ，启用`BypassPerfRequirement` 。
- 启用 Summarization API: 打开 `chrome://flags/#summarization-api-for-gemini-nano` ，并启用。

快速测试了一下：

![](https://substackcdn.com/image/fetch/$s_!36Re!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2c121af4-70d1-4391-bc3a-3e221349aa04_1674x666.png)

当然，它的限制也很明显：这是一个预训练的通用模型，开发者无法进行个性化微调（Fine-tune）。

## 路径二：量身定制的“专属大脑” — Gemma & WebGPU

对于需要更强定制能力的场景，Google 提供了 **Gemma + WebGPU** 技术栈。Gemma 是 Google 推出的开放、轻量级模型系列，而 WebGPU 则是让其在浏览器中高效运行的关键引擎。

**什么是 WebGPU？**

简单来说，WebGPU 是一个现代浏览器 API，允许网页代码直接高性能地访问 GPU（图形处理器）。AI 模型需要海量并行计算，而这正是 GPU 的专长。WebGPU 就是那座桥，让 JavaScript 可以直接利用 GPU 硬件加速，是端侧 AI 的性能引擎。


通过该技术栈，开发者可以下载 Gemma 模型，用自己的数据微调，打造真正懂业务的多模态 AI 应用。

参考：《适用于 Web 的 LLM 推理指南》：[https://ai.google.dev/edge/mediapipe/solutions/genai/llm_inference/web_js?hl=zh-cn](https://ai.google.dev/edge/mediapipe/solutions/genai/llm_inference/web_js?hl=zh-cn)

## 相辅相成：便利与定制的完美结合

这两种方式并非对立，而是互补的。开发者可以在同一个应用中结合使用：用“便利店”般的 Gemini Nano API 解决 80% 的通用需求，再用“专业厨房”般的 Gemma + WebGPU 打造 20% 的核心竞争力。

# 革命二：AI 辅助开发 + 现代 CSS 的完美结合

如果说 **Gemini Nano** 和 **Gemma** 是让浏览器本身拥有“大脑”，那么 **DevTools + 现代 CSS API** 则让开发者的日常工作更高效、更顺畅。

## 1. DevTools：AI 变身你的结对程序员

过去调试流程低效：IDE 改代码 → 浏览器刷新 → `console.log()` 调试，甚至要借助 **Playwright** 做截图对比，开发者需要在多个工具间反复切换。

现在，Google 在 Chrome DevTools 中深度集成了 **Gemini AI 助手**，彻底改变了这一工作流。你可以直接用元素选择器点选页面上的任意元素，然后和 AI 助手对话。

**交互示例：**

**你（选中一个方形的** `div`**，它本应是个轮子）：**`> 我已经选中了这个元素。它现在是方的，但它应该是个轮子。帮我改成完美的圆形。`

**AI Assistant:**`> 好的。要将这个 div 变成圆形，需要把 border-radius 设置为 50%...`


确认无误后，AI 生成的修改建议可以一键应用，并**直接保存回本地源文件**，真正打通了从调试到修复的闭环。

例子参考：[https://chrome.dev/cinemai/devtools/hangar](https://chrome.dev/cinemai/devtools/hangar)

![Pasted image 20250820125730.png Pasted image 20250820125730.png](https://substackcdn.com/image/fetch/$s_!8OzV!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd12950c2-6f62-48b4-835c-4340930db0da_2976x1812.png)

## 2. 现代 CSS API：从样式到交互的跃升

这里与 DevTools 恰好形成呼应。因为 DevTools 的 AI 助手主要修改 **HTML 和 CSS**，而 **现代 CSS API** 让 CSS 本身的表现力大大增强，开发与调试效率的提升因此更加显著。

- **View Transitions API** ：轻松实现页面不同状态间的平滑过渡。
- **Scroll-driven Animations** ：将动画进度与用户的滚动操作直接关联。

这意味着，很多过去必须依赖 JavaScript 的复杂交互，现在只需 CSS 就能实现。性能更好、代码更简洁，并且符合“**渐进增强 (Progressive Enhancement)**”原则：在现代浏览器中提供流畅体验，在老旧浏览器中则优雅降级为基础版本。

开发者文档：

- [https://developer.chrome.com/docs/css-ui/scroll-driven-animations?hl=zh-cn](https://developer.chrome.com/docs/css-ui/scroll-driven-animations?hl=zh-cn)
- [https://developer.chrome.com/docs/web-platform/view-transitions?hl=zh-cn](https://developer.chrome.com/docs/web-platform/view-transitions?hl=zh-cn)

小 tips：通过 **DevTools + AI 助手** 与 **现代 CSS API** 的结合，前端开发正在形成一个新的“黄金组合”：

- CSS 本身更强大
- DevTools 能智能地帮助修改和应用 CSS

# 革命三：隐私与数据的未来

第三场革命关乎 Web 的核心信任与数据使用方式。

## Privacy Sandbox：为无 Cookie 的未来铺路

在展区，我还看到了 **隐私沙盒 (Privacy Sandbox)** 的介绍。随着公众对隐私的关注不断增强，传统依赖第三方 Cookie 的用户追踪与广告投放方式，正逐渐暴露出其固有的问题与局限。

Privacy Sandbox 并非单一产品，而是一系列浏览器 API，旨在取代第三方 Cookie 的功能。它允许网站在不侵犯用户隐私的前提下，实现广告归因、兴趣定向等关键业务。可以说，这是在为未来十年的 Web 奠定一个更健康、更值得信赖的基础。

开发者文档：[https://privacysandbox.com/intl/en_us/open-web/](https://privacysandbox.com/intl/en_us/open-web/)

# Google的 ADK框架 - 多智能体的编排的门槛正在降低

那天下午，我还参加的一场 **Multi-Agent Workshop** ，使用 Google 的 **Agent Development Kit (ADK)** 来编排多智能体应用：

- **顺序智能体 (Sequential Agent)** ：
  - **Agent 1 (研究员)** ：抓取维基百科信息
  - **Agent 2 (作家)** ：根据信息写小说.
  - **Agent 3 (评论家)** ：评估小说
- **并行智能体 (Parallel Agent)** ：多个 Agent 同时执行不同任务，再汇总结果。

整个框架的抽象层次很高，用极少的代码即可定义复杂流程，还能通过 Web 界面实时监控 Agent 的动态。

开发者指路：[https://developers.googleblog.com/en/agent-development-kit-easy-to-build-multi-agent-applications/](https://developers.googleblog.com/en/agent-development-kit-easy-to-build-multi-agent-applications/)

过程中我联想到和 langgraph 的区别，所以顺便一起做了一个梳理如下：

![](https://substackcdn.com/image/fetch/$s_!rCq4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc61684b5-de1a-4496-8cb6-fa129b614eea_1530x1198.png)

这三场革命各自推动着 Web 的边界：**AI 内嵌浏览器**让能力触手可及，**DevTools + CSS**让开发体验前所未有地高效顺滑，而 **Privacy Sandbox** 则守护了信任与数据底线。最后的多智能体 Workshop 更让我意识到，这些变革并非孤立，而是逐步拼合出一个新的图景：一个人人都能编排、人人都能使用 AI 的未来。

我带着这样的问题离开 Google I/O：当 Web 与 AI 的边界逐渐消融，我们作为开发者该如何重新定义“编程”的含义并梳理新的编程流程？
