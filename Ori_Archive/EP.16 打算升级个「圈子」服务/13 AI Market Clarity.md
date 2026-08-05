# AI Market Clarity

> 原链: https://blog.eladgil.com/p/ai-market-clarity  
> 来源: blog.eladgil.com · 归档自 EP.16 · 抓取于 2026-08-06  

---

# AI Market Clarity

### A subset of AI markets have crystalized in the last 12 months, with the likely market leaders for the next year or two suddenly clear

## **AI Markets Have Crystalized**

AI markets have evolved significantly over the last 4 years. When GPT-3 came out and scaling laws were openly discussed in the AI literature, it seemed clear that you could extrapolate the rate of progress from GPT-2 to GPT-3 onwards through GPT-4, 5 etc and realize a revolution was going to happen.

4 years ago, I started looking for Generative AI companies to back or help start given this curve. I ended up leading or participating in early rounds in companies like [Harvey](https://www.harvey.ai/), [Perplexity](https://www.perplexity.ai/), [Character.AI](https://blog.character.ai/our-next-phase-of-growth/), [BrainTrust](https://www.braintrust.dev/), and others. At the time it was clear to just “back all the best people working on all the biggest problems” because very few people were actually starting generative AI companies. OpenAI seemed to be the only clear foundation model company (with Anthropic pre-launch and promising, Llama non-existent, and Google clearly someone who could (and would eventually) aggressively innovate but was stymied at the time by its own internal processes).

As more people outside of the core AI community woke up to this opportunity, or researchers and engineers from the main labs left to start new companies in AI, the world of AI became murkier. I used to say that [the more I learn about AI, the less I knew about AI](https://blog.eladgil.com/p/things-i-dont-know-about-ai) – because it was unclear in many early markets who the likely winners would be and the underlying models and tech were changing so fast. For example in 2022, it was clear code / AI driven software engineering was going to be important, but it was unclear who the winners would be (for example Cursor was not launched until 2023, Codium launched [Windsurf in GA](https://windsurf.com/blog/windsurf-launch) about 9 months ago, and Cognition launched [Devin](https://cognition.ai/blog/introducing-devin) in limited release a bit over a year ago).

We have now entered an era where the first set of AI markets have solidified and a likely set of winners have emerged. This does not mean others won’t show up over time to compete in these markets or that current leaders won’t get acquired or eventually die (just as Stripe launched over a decade after PayPal and 4 or so years after Braintree, and Facebook launched a few years after Friendster and Myspace). We will also see a new set of markets crystalize in the coming few years and these markets today seem quite uncertain.

## Markets with more clarity

### 1. Foundation Models- LLMs

There are many types of foundation models including large language models (LLMs), as well as models for voice, images, video, music, chemistry, biology, materials, physics and other areas. Foundation models are often driven by scale (of data, compute, certain types of post training and feedback, etc). Scale means capital, so to win in the LLM market you need high availability of capital now entering the many billions.

In the LLM market, a core set of companies have clearly emerged as the ongoing players of the future. They are often partnered with hyperscalers (Amazon with Anthropic, Google GCP with Gemini, Microsoft Azure with OpenAI and its own efforts) as these companies have an economic incentive (cloud spend on AI via AI adoption) to fund these companies that is independent of whether these companies are good investments or not (they often are). Revenue ramps for foundation model companies are rumored to be in the $0 to many $billions range in just 3 or so years, while cloud spend on “AI” has been reported to have reached [a few billion per quarter for some of the main clouds](https://www.reuters.com/business/microsoft-beats-quarterly-revenue-estimates-ai-shift-bolsters-cloud-demand-2025-04-30/).

The core players in the LLM world are now Anthropic, Google, Meta (via Llama), Microsoft, Mistral, OpenAI, X.AI. Three or four of these companies are the [clear winners on various benchmarks](https://artificialanalysis.ai/models) and most broadly adopted by developers and enterprise, and are also driving most of the spend in the industry. There are newer entrants like SSI and Thinking Machine Labs driven by brilliant AI researchers, which may either come up with innovative approaches or raise ongoing money to compete, or end up in a few years as acquisitions for companies wishing to enter the market or double down on talent.

![](https://substackcdn.com/image/fetch/$s_!QXsK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F96de5704-be21-4218-b8d5-5f7c5dd17af5_1734x796.png)

![](https://substackcdn.com/image/fetch/$s_!g8cN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F36c15560-9a55-4b88-be8a-61e3d42818ad_2440x1634.png)

In parallel, Chinese companies have launched new open source efforts such as [Deepseek](https://www.deepseek.com/), [Alibaba Qwen](https://www.alibabacloud.com/en/solutions/generative-ai/qwen?_p_lc=1), and more recently [Kimi](https://github.com/MoonshotAI/Kimi-K2), that perform well on benchmarks. There is a lot to say on Chinese open source LLMs, that might be best covered in a separate post.

In the future, it is unlikely that many new core LLM companies will get started due to capital moats, barring some new breakthrough that somehow doesn’t spread quickly.

Other foundation model markets are still lacking the clear winner or winners although promising companies exist in multiple segments.

### 2. Code

Code is one of the earliest and clearest large-scale applications of generative AI and LLMs. For example, [Github copilot was launched in October 2021](https://en.wikipedia.org/wiki/GitHub_Copilot) and was already well adopted and useful despite more limited functionality and fidelity of its day. Code has all sorts of properties that make it especially amendable to generative AI approaches. Revenue ramps in code are rumored to be in the $0 to $50 up to [$500M in the first 2 years](https://techcrunch.com/2025/06/05/cursors-anysphere-nabs-9-9b-valuation-soars-past-500m-arr/) of some of the players live product lifetime – an insanely fast pace.

Like foundation model companies, the core likely winners in code are evident, with a handful of companies seeming to be interesting over time. Large incumbents may still enter the coding market, and products to date do not seem especially sticky but moats tend to come with time. However, this handful of companies will play an important role in the next few years of code barring the unexpected and includes Anthropic’s Claude Code, [Cognition / Windsurf](https://x.com/cognition_labs/status/1944819486538023138), Cursor, [Google / Windsurf](https://techcrunch.com/2025/07/11/windsurfs-ceo-goes-to-google-openais-acquisition-falls-apart/), Microsoft/Github, OpenAI, potentially startups like Magic or Poolside, and then vibe coding companies like Lovable, Replit, and others. Intriguingly, both Figma and Canva have launched vibe coding tools and one can imagine lots more coming. 

A number of questions continue to exist for code (and other markets) including agentic vs IDE-based work flows and their eventual overlap (they will undoubtedly converge), as well as the degree to which the foundation model companies will integrate or subsume more of the coding companies functionality directly given both large economic value, as well as code being a bootstrap path to AGI / SI. These core questions will drive who the final winners in code will be.

### 3. Legal

The core players in core legal markets have solidified with [Harvey](https://www.harvey.ai/blog/harvey-raises-series-e) (both law firms and enterprise) and [CaseText](https://legal.thomsonreuters.com/en/c/cocounsel-core/complete-legal-tasks-faster) as the current leaders. Other startups working in either overlapping ([Legora](https://legora.com/)) or new areas ([Crosby](https://crosby.ai/)) are starting to emerge. [EvenUp](https://www.evenuplaw.com/) moved in the post AI era into personal injury and related areas, while [Eve](https://www.eve.legal/) and [Supio](https://www.supio.com/) are focused on plaintiff work flows. We are still very early in full workflow automation but startups like Harvey and EvenUp have started to take core legal workflows and build systems to complete the work start from finish. With the centrality of legal, companies like Harvey may be able to naturally integrate  into other professional services workflows over time

Given the breadth of legal across vertical areas (patents, contracts, etc.) and type (law firms, enterprise, SMB, consumer) there may be new legal areas yet to explore.

### 4. Medical Scribing

Physician tools and scribing is another area with a clear set of main players that markets have consolidated against include [Abridge](https://www.abridge.com/blog/series-e), [Ambience](https://www.ambiencehealthcare.com/product), [Commure](https://www.commure.com/) / Athelas, and Nuance (Microsoft). Some international players have also emerged in this area and may either end up as stand alone, or consolidated into the main players.

The key next step for these players is to expand products into other areas of the healthcare stack.

### 5. Customer service / experience

The customer experience market in the US appears to have consolidated in the short term into a few core startup players – Decagon and Sierra, while incumbents like [Intercom](https://www.intercom.com/drlp/ai-agent), [Zendesk](https://www.zendesk.com/service/ai/) and others work to add and cross-sell generative AI capabilities. Other startups of interest include Forethought, Maven, Parahelp, Wonderful, and others. Like many of the markets above, customer experience has the characteristic that generative AI is displacing or augmenting humans strongly with agentic work, versus another seat-based workflow tool. 

We are starting to see the shift from selling seats, to selling units of cognition. This is an underdiscussed aspect of AI companies in general.

Reasoning model advancements and agentic infrastructure products will only accelerate this shift.

### 6. Search and IR re-invention

Players focused here include Google, OpenAI (chatGPT), Perplexity, and Meta. [Perplexity](https://www.perplexity.ai/) is notably the main startup in this market, while most of the other players are incumbents. This may end up being true for other consumer and prosumer markets as well, although there is a lot of room for new consumer use cases.

Perplexity and the other players are moving quickly into the agentic future (see section below), both through tools like Deep Research, but also more recently via entry into the browser market. For example, [Perplexity’s Comet browser](https://x.com/PerplexityComet/status/1943328926232907911) already incorporates agentic actions for shopping on the web and other actions.

## Future markets that will be important

3 years ago it was clear foundation models / LLMs, code, healthcare, customer service and other areas would be important AI markets, but it was much less clear who would win or be important. Today the market leaders that are likely to play a short term role are clear (although as mentioned often new startups or incumbents launching products can still join later in the game).

The next set of markets that seem highly interesting and tractable to generative AI include, but are not limited to the below. **I and my team are highly interested in investing behind companies in these areas**:

- **Accounting.** People are both building software here and in some cases doing rollups.
- **Compliance.** Lots of different forms of compliance. Pharma compliance is one example with early players like[Blue Note Health](https://www.bluenotehealth.com/) .
- **Financial tools.** Tools to help financial analysts or others. There are a number of great teams and early companies working in this area.
- **Sales tooling and agents.** Lots to do here – from AI agents doing SDR work to tools to augment enterprise sales.
- **Security.** An enormous number of potential applications here, particularly in areas of high service utilization or large team complexity. There will separately emerge security companies focused on AI-end points, agents, or foundation model usage that could lead to data leaks or other exploits.
- **Other markets TBD.** Lots to do!
- **What have I missed?** Let me know on[X.com](https://x.com/eladgil) or directly.

There are a set of exciting companies in each of these areas, and which of them will pull ahead or win will likely crystalize in the coming months or quarters. In some cases models may not yet be good enough to address these markets well, in others a broader workflow tool or better GTM approach needs to be developed. In some cases it might just be a matter of time – it takes time to fully understand a customer, build against their needs, and see product-market pull and fit.

**I (and my team) am actively looking to invest in all these areas – so please ping if working on it. :)**

### Model vs GTM vs Team?

For the “new” market segments above, one core question is what has been preventing market crystalization?

Part of it for some markets is the models need to advance in reasoning or fidelity. For example, legal workflows did not work on GPT 3.5 but with GPT4 really took off and Harvey benefited from this plus custom model work. Similarly, coding tools like Cursor benefited from Claude 3.5 (launched June 2024) and were just not as useful until the models used crossed some tipping point of fidelity. Building early against customers pre-model fidelity allows you to capture market share once the models get better.

This leads to the concept of the GPT Ladder - at a certain level of GPT (or Claude, or Gemini, or Grok, or Llama) release, specific new markets will open up. For example, GPT-5 (or Claude X, or Gemini Y) should support an entirely new market that simply was not tractable technologically in the absence of the model.

![](https://substackcdn.com/image/fetch/$s_!4PLh!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F73ef3064-38c9-484c-822f-08cfa2ea7b88_1778x1194.png)

Beyond models, other things that may prevent adoption of generative AI in a market may include:

- **Go-to-market, buying behavior & competition** .
  - Startups may be getting go-to-market wrong (selling to the wrong customers in the wrong way)
  - There may be too much incumbent lock in (or ability to counter startups quickly with worse product or cross sell against an existing UI or workflow owned by the incumbent).
  - Buyers in the market may just be slow to move and adopt and will get there over time.
- **Teams.** Perhaps the right team has not shown up yet, or the founders are new to the market and will take a bit of time to learn and iterate what customers need.
- **Time to build.** It takes time to build and ship useful products. Sometimes activity in a market is just too nascent and in 6-12 months a big enough product footprint will exist for winner(s) to emerge.

### Agents everywhere

One big ongoing shift is moving from pure tooling “AI chat” to agentic workflows. Agents are AI software that do actions on your behalf. It is the difference between looking up information about travel to Spain on Google, and having Google spawn an AI agent that goes and books the travel for you and takes actions on your behalf. Coding tools like Devin and customer service tools like Decagon/Sierra seem the earliest B2B adopters of agentic workflows, while informational tools like chatGPT, Gemini, and Perplexity are adding agents to do deep research for their users.

As reasoning models and agents proliferate, new infrastructure to support agentic deployment & workflows is accelerating. A number of startups are working on agentic frameworks or infrastructure, while consulting or large-scale deployment firms are also adding agents to their roster of tools to deploy in enterprises.

We are starting to see the shift from selling seats, to selling units of cognition or human equivalent labor.

### AI Roll Ups

I have been talking about, and investing in, generative [AI driven roll ups for 3 years or so](https://techcrunch.com/2025/06/01/early-ai-investor-elad-gil-finds-his-next-big-bet-ai-powered-rollups/). From the earliest days of generative AI it was clear that this new form of scaled transformer-based AI was very good at human knowledge work – which is much of the white collar services economy. In AI driven roll ups, buying a company versus just selling them software can lead to outsized faster adoption and economics than just selling software. 

Often, adoption of AI is not a technology problem – it is an organization, process, and people issue. Can you rework an entire organization or its way of doing things around the AI tooling? This is often a much harder problem than just the AI tooling itself and requires owning the actual company to be able to rework organizational processes on a short enough time frame to matter (at least for a startup – incumbents often take a long time).

I have funded 2 AI driven buyouts to date and am excited to back more- reach out if you are working in this area!

## Market ending moves

In another [post](https://blog.eladgil.com/p/market-ending-moves), I talk about “[market ending moves](https://blog.eladgil.com/p/market-ending-moves)” – what big strategic play can you do (M&A? Enormous capital scale and investment? Other?) can you do to just win first place in a market. 

As markets consolidate, the strategic moves to just win a market become clear. This will likely lead to various forms of M&A, partnership, channel lock in, or other strategies as the handful of players per market consolidate down into one or a small handful.

We should see a lot of consolidation and M&A coming quite soon due to the ability to win a market by combining the two main startup leaders (often hard to negotiate but worth doing) or incumbent/startup pairs (distribution + tech = winning).

Very exciting times are ahead.

## Summary - AI markets have crystalized 

AI markets are now the clearest they have been in a few years. The leaders in a given segment are clear for many of the earlier generative AI markets like Code and Legal, while new markets are ripe for disruption. Exciting times ahead.

## **OTHER POSTS**

**My book:** High Growth Handbook. [Amazon](https://www.amazon.com/High-Growth-Handbook-Elad-Gil/dp/1732265100). [Online](https://growth.eladgil.com/).

**Markets:**

**Firesides & Podcasts**

**Startup life**

**Co-Founders**

- [How To Choose A Co-Founder](http://blog.eladgil.com/2012/02/how-to-choose-co-founder.html)
- [Unequal Cofounders](http://blog.eladgil.com/2017/08/unequal-cofounders.html)
- [How To Fire A Co-Founder](http://blog.eladgil.com/2013/01/how-to-fire-co-founder.html)
- [Founders Should Divide and Conquer](http://blog.eladgil.com/2014/12/founders-should-divide-and-conquer.html)

**Raising Money**
