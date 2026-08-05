# How to use Deep Research for GTM

> 原链: https://www.growthunhinged.com/p/deep-research-for-gtm  
> 来源: www.growthunhinged.com · 归档自 EP.19 · 抓取于 2026-08-06  

---

👋 *Hi, it’s* *Kyle Poyar* *and welcome to* *Growth Unhinged**, my weekly newsletter exploring the hidden playbooks behind the fastest-growing startups.*

*I’m totally hooked on Deep Research mode within ChatGPT and Perplexity. I can’t tell you how much time it has saved me when compiling information for this newsletter or, honestly, for any research-intensive GTM project. It’s one of the most powerful, yet underused AI functions that exists today. Let’s change that.* 

*For help I turned to* [Torsten Walbaum](https://www.linkedin.com/in/torsten-walbaum/) *who’s built and led strategy and analytics teams at companies like Uber, Meta and Rippling. Torsten now writes the fantastic Operator’s Handbook newsletter, which I cannot recommend highly enough.* *True to form, Torsten shares an immensely practical guide for turning Deep Research into your own personal McKinsey-caliber analyst.* 

Deep Research is the first AI feature that truly blew my mind.

It’s the first time that AI is able to solve complex non-engineering tasks end-to-end, from developing a plan to gathering relevant context and then producing a high-quality deliverable. I’m usually hesitant to make bold claims with regards to AI, but Deep Research has literally condensed tasks that took me 10+ hours into minutes (once I figured out how to use it correctly).

Despite this, there seem to be fewer Deep Research power users than I expected, and I think it has to do with the name. “Research” makes it sound like it’s mostly a tool for academics and investors, but that only scratches the surface; in reality, it’s a game changer for any task that involves reviewing lots of information and distilling practical insights from it.

And, as it turns out, that’s almost any project in GTM.

That’s the first reason I teamed up with Kyle to write this article: **By walking through real-world GTM use cases, I want to show what the tool is capable of and inspire more people to use it creatively.**

The other reason is that despite its enormous potential, Deep Research isn’t perfect, and you need to provide a lot of handholding to the AI if you want top-tier results. In contrast to many other AI use cases, how you write the prompt actually still matters a lot here, and the context you provide can make or break the result.

In the rest of this post, we’ll cover:

- Actionable tips on how to get the best outputs from Deep Research
- What an effective Deep Research prompt looks like
- Which tool (ChatGPT, Gemini, Claude, Perplexity, Grok) is best for what
- Five practical GTM use cases with prompt examples you can try right now (plus more ideas for inspiration)

## How to get the best results from Deep Research

Regardless of which AI tool you use (more on that below), there are a few key limitations you should be aware of.

**Don’t worry, though:** All of them can be addressed, and we’ll go through the exact workflows and prompting techniques that will get you the best results.

### **1. Point the research agent to high-quality sources**

The quality of the output you get from Deep Research is heavily dependent on the sources the agents use. Unfortunately, they often show bad judgment here: They’ll treat social media opinions as facts, over-index on individual sources, or use outdated data. It can be extremely frustrating to notice this after the report is done because you’ll have to re-do the whole thing and lose 15 minutes plus valuable research credits in the process.

There are two simple ways to fix this, though:

- **Option 1:** Specify in the prompt what*kind* of sources to prioritize (e.g. primary sources like government data over secondary ones like news articles)
- **Option 2:** Use an AI model like GPT-5 or Claude Opus to create a list of specific high-quality sources and then feed that into Deep Research (you’ll see this in action in example #5 below)

In addition, if you want more transparency, you can also ask the research agent to:

1. Always provide in-text citations for any claim it makes
2. Add a table to the report that lists all sources and shows which source was used for what, what type of source it is, what year the data is from, etc.
3. Outline where different sources disagree (esp. when it comes to data) and what the reason might be (e.g. differences in methodology)

![](https://media.beehiiv.com/cdn-cgi/image/fit=scale-down,quality=80,format=auto,onerror=redirect/uploads/asset/file/d688b09a-4a9e-4676-849d-0005eabacfda/23a618ec-2aa7-4026-8a41-8b920e431fc1_860x516.jpg)

This only adds one minute to your workflow, but will save you lots of headaches down the road.

### 2. Provide context to get customized insights

Getting an in-depth overview of a topic at the click of a button is already kind of neat; but it’s not actually that useful. To really get value out of it, you need something that’s tailored to *your particular situation*.

![](https://media.beehiiv.com/cdn-cgi/image/fit=scale-down,quality=80,format=auto,onerror=redirect/uploads/asset/file/72e5607d-6554-4007-a018-561e936e2e81/c2e5ff4c-fcb7-4dae-8980-34c6e2ab6860_590x170.jpg)

Unfortunately, most Deep Research tools are not in the habit of asking for the context they need. So if you don’t proactively provide relevant information, they’ll either make assumptions or keep things generic.

To avoid this, you’ll need to provide all the context that a human team member would need as well. What exactly that is depends on the situation, but here are a few common things you’ll likely want to touch on:

💼 **Where you work and how your company operates**

This is especially important if you want the AI to come up with concrete recommendations for what to do and/or tactical guidance for how to implement the suggestions.

If your company has a large online presence, it’s often enough to just mention where you work; but if you’re at a small startup, it’s better to briefly outline what the company does, how big it is, plus anything else relevant for the specific task (e.g. how your GTM motion works etc.).

🎯 **What exactly you’re trying to achieve**

Often, when I see people use Deep Research, they give the AI a *task* (e.g. “*Pull together a report comparing these tools*”) without sharing the motivation and ultimate goal (e.g. “*We’re trying to get better visibility into campaign performance for planning and budget allocation”*).

The more transparent you are about your goal and where the AI fits in, the more impactful the result will be. And if the request is part of a larger project, make sure you share any work that has been done up to that point.

🚧 **[If applicable] What constraints you’re facing**

If there are hard constraints that will rule out certain options, share this to get a more targeted report:

- How much budget and headcount do you have for implementing this project?
- Are there any deadlines you’re working towards?
- Anything leadership or legal won’t approve based on past experience?

**Pro tip:** If you don’t want to provide context every time you prompt Deep Research, create a *Project*. That way, you only need to upload the initial context once, and every research report adds to the joint knowledge between you and the AI.

![](https://media.beehiiv.com/cdn-cgi/image/fit=scale-down,quality=80,format=auto,onerror=redirect/uploads/asset/file/b7248e9a-0752-499b-a754-4352da3b9c0c/f346e8d4-b69c-4de8-86c9-4751d4744c9e_1528x741.jpg)

The above is a good start, but I’ve noticed that it can be pretty difficult to brainstorm exactly what you should be sharing, especially when you’re trying to move fast.

To make things easier, I’ve started asking AI for its take (GPT-5 and Claude Opus both do a great job):

*I'm planning to generate a Deep Research report on [X] in order to [Y]. What context should I provide so that I get a customized, actionable report? Pretend you have no context from any prior conversations.*

Lastly, if you want to be sure you didn’t miss anything, ask the Deep Research agent directly to get additional context from you:

![](https://media.beehiiv.com/cdn-cgi/image/fit=scale-down,quality=80,format=auto,onerror=redirect/uploads/asset/file/c1020b52-86fb-49fe-9a28-86fdfd890a83/460d4933-9540-4016-a04b-52f63783bbe1_574x264.jpg)

### 3. Ask for a research plan before getting started

The biggest advantage of Gemini Deep Research is that it always shares a plan before it gets going; that way, you can make adjustments in advance instead of waiting 20 minutes only to find that you disagree with the methodology or the report focuses on the wrong thing.

![](https://media.beehiiv.com/cdn-cgi/image/fit=scale-down,quality=80,format=auto,onerror=redirect/uploads/asset/file/4ef15b21-7d1a-40df-9d5b-a0ff84470ea9/cb9712e8-8369-4460-9a3b-0198c273dadd_1600x567.jpg)

None of the other tools do that; instead, you need to explicitly ask for the research plan in your prompt:

![](https://media.beehiiv.com/cdn-cgi/image/fit=scale-down,quality=80,format=auto,onerror=redirect/uploads/asset/file/6d31efee-9842-4b2c-9ff4-0214d9ad7fd1/083f7913-4320-4756-8e9e-b508592049fc_552x69.jpg)

**Note:** Make sure you repeat the request if you’re answering any questions after your initial prompt. Otherwise, the tools sometimes forget about it.

A few questions to ask yourself as you’re reviewing the research plan:

- Does it cover everything you’re interested in? Would you like any additional outputs (e.g. templates, code snippets, etc.)?
- Do you agree with the methodology and focus areas (e.g. how the agent plans to evaluate different options)?
- Does the AI seem to be making any assumptions, or do any parts seem generic? If so, you need to provide additional context.

### 4. Specify an easy-to-digest report format

The default reports you get back are often hard to read, especially if you want to skim them for the most important insights.

It’s easy to change that with the right prompt, though. Just ask to:

- Include a summary at the beginning of the document and every individual section
- Start with the key insights or recommendations before going into details
- Use overview tables or visuals instead of text blocks where appropriate

![](https://media.beehiiv.com/cdn-cgi/image/fit=scale-down,quality=80,format=auto,onerror=redirect/uploads/asset/file/b36a74c7-88a3-4d57-b68d-da4cbc891631/e9dffd35-7cd6-413c-89e8-aa0cdccd1ff3_1600x752.jpg)

## How to write a good Deep Research prompt

Putting all of the tips from above together and adding a few optional ones, this is what an effective Deep Research prompt looks like.

Just copy this and plug in your own information (the comments marked with “#” are there to explain each section and should not be included in the prompt):
