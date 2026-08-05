# Builder.ai did not “fake AI with 700 engineers”

> 原链: https://blog.pragmaticengineer.com/builder-ai-did-not-fake-ai/  
> 来源: blog.pragmaticengineer.com · 归档自 EP.12 · 抓取于 2026-08-06  

---

# Builder.ai did not “fake AI with 700 engineers”

*Originally published* *in The Pragmatic Engineer Newsletter.*

An eye-catching detail widely reported by media and on social media about the bankrupt business [__Builder.ai__](http://builder.ai/?ref=blog.pragmaticengineer.com) last week, was that the company faked AI with 700 engineers in India:

- “Microsoft-backed AI startup chatbots revealed to be human employees” – [__Mashable__](https://mashable.com/article/microsoft-backed-ai-startup-chatbot-human-employees?ref=blog.pragmaticengineer.com)
- “Builder.ai used 700 engineers in India for coding work it marketed as AI-powered” – [__MSN__](https://www.msn.com/en-in/news/other/builder-ai-used-700-engineers-in-india-for-coding-work-it-marketed-as-ai-powered-after-hype-now-goes-bust/ar-AA1FZ65K?ref=blog.pragmaticengineer.com)
- “Builder.ai faked AI with 700 engineers, now faces bankruptcy and probe” – India’s [__Business Standard__](https://www.business-standard.com/companies/news/builderai-faked-ai-700-indian-engineers-files-bankruptcy-microsoft-125060401006_1.html?ref=blog.pragmaticengineer.com)

**In the past week, I’ve been talking with several engineers who worked at Builder.ai, and can confirm that this detail was untrue.** But let’s hold that thought for a second, and do a thought experiment about how we could make this headline be true! Something like it has been attempted before…

#### Design challenge: a system with 700 devs pretending to be an AI

Okay, we’ve put on our “evil hacker” villain mask and put ethical considerations in the bin: our goal is to build a system where 700 engineers pretend to be a working AI system, all without using any artificial intelligence. Also, it’s the year 2024 in this experiment. So, how would we pull it off?

The naive approach: have the devs write code and assume there will never be more than 700 parallel sessions in play:

![](https://storage.ghost.io/c/39/f8/39f85cc7-8637-40fc-a57c-f45754453717/content/images/2025/06/AD_4nXccoBChOXb8aXvp1ZKqtWk4oyfGFziSF8w4IYT_aF1IMgIHwz3g9LbEqO6KePMFc2kOHKwzck_3DTkAI3t-SifxjVcAuqJyTe5sf4Bmaw5EEexTdODyLajnf4XP0lq1TtUxf_DNwA.png)


*First attempt at a system where 700 devs can pretend to be an AI*
There is one immediate, major problem: latency. No user will believe it’s a working AI if it takes 10-30 minutes to provide a response. In that scenario, the deception is likely to be quickly exposed. What’s needed is faster response times, so customers could be fooled into believing they’re interacting with a machine. Basically, what’s called for is something akin to the [__Mechanical Turk__](https://en.wikipedia.org/wiki/Mechanical_Turk?ref=blog.pragmaticengineer.com):

“The Mechanical Turk, also known as the Automaton Chess Player, or simply The Turk, was a fraudulent chess-playing machine constructed in 1770, which appeared to be able to play a strong game of chess against a human opponent. For 84 years, it was exhibited on tours by various owners as an automaton. 

The machine survived and continued giving occasional exhibitions until 1854, when a fire swept through the museum where it was kept, destroying the machine. Afterwards, articles were published by a son of the machine's owner revealing its secrets to the public: that it was an elaborate hoax, suspected by some, but never proven in public while it still existed.”

The Automaton Chess Player concealed a person inside the machine, which went unnoticed for more than 80 years:


*The Automaton Chess Machine in action*
Back to the current problem, and applying the inspiration of the 18th century chess machine containing a concealed human. To improve latency – and decrease users’ suspicion – we could perhaps stream what the “assigned developer” typed:


*Reducing latency of the system by streaming typing*
This is better, but it remains a giveaway that the system is slow to complete basic tasks. So what about incentivizing our developers with a bonus for completing tasks under 3 minutes, and allowing them to use any tool they want? Incentives are powerful, so it’s likely the following would be observed:


*Devs complete tasks much faster when they can use their tools!*
We did it! We managed to fake a good enough AI.

But wait… how exactly did the devs complete their tasks within the arbitrary time frame of 3 minutes? To find out, questions are asked, and this what we see (remember, it’s 2024):


*How the “700 devs pretending to be AI” would actually work in 2024*
Wait… what?! “Devs pretending to be an AI would use an AI to deliver the outputs in time? This is a logical approach for 2024, when LLMs were already more than capable of generating high-quality code. And this is why it would be irrational to hire 700 developers to pretend to be AI last year, when there were already LLMs that did this much better.

If you hired a competent engineer in 2024 to design a system that takes a prompt and pretends to be an AI, and they could use any tool they liked, and there were 700 devs for the project, what they built would look something like this:

Spoiler: Builder.ai did exactly this as well!

#### Natasha’s tech stack

Builder.ai [__first showcased__](https://www.youtube.com/watch?v=s4YrQsZ03Vg&ref=blog.pragmaticengineer.com) the idea of Natasha in 2021, well before ChatGPT was announced. Back then, Natasha was positioned as a “personal app builder,” and it was clear that the solution worked with a “network of geeks” who built apps to spec:


*“You tell us your idea, and me [Natasha] and my network of geeks build it, using building blocks that really work.” Source:*

*Builder.ai*

*in 2021*
The product promised a cost estimate up front, and a schedule. The idea was that by taking on thousands of projects, the team behind Natasha could create reusable building blocks that speed up building websites and mobile apps.

In December 2023, one year after ChatGPT was released, Builder.ai [__announced__](https://www.builder.ai/blog/natasha-everywhere?ref=blog.pragmaticengineer.com) Natasha CodeGen as “your always-on software development partner”. In April 2024, the company demoed Natasha CodeGen in [__a series of videos__](https://www.builder.ai/blog/codegen-with-natasha?ref=blog.pragmaticengineer.com), which show code generation happening, as well. In the video, there’s a cut, and the video returns when the React code is generated. I’ve confirmed with former engineers at the company that behind the scenes, the system ran for a few minutes before finishing code generation:


*Natasha’s log output in April 2024. Source:*

*Builder.ai*
Natasha was aimed to be an AI tool for the whole software development cycle:

- **Idea** : refine an idea with a visual UI of what the app’s UI could look like
- **Planning** : create user stories (tasks) inside a dedicated UI. Tasks include creating acceptance criteria.
- **Code generation planning** : feed the task into an LLM to plan steps for code generation
- **Testing** : have the AI add tests first, following a test driven development (TDD) approach, and create a PR only if the tests pass
- **Generate code:** create the code, and run them against the tests
- **Create a PR** : only do this if all the tests pass

**A team of 15 engineers worked on Natasha Codegen.** Most engineers were based in the UK, with around 3 in India. At its peak, Builder.ai’s AI team was circa 30 people. On top of building Natasha, the team was building and maintaining many AI products and services. One ex-engineer there told me they thought a lack of focus contributed to the company’s demise.

The tech stack behind Natasha:

- **Python** : for the orchestrator that lines up steps that the agents took
- **Ruby on Rails** : for parts of the backend and frontend
- **React** : for a good part of the frontend
- **GPT** and**Claude** for LLMs integrated for the code generation step


*The web components for Natasha were built using Ruby on Rails. Source:*

*Builder.ai*
The team built a set of coding benchmarks that they ran whenever a new model came out, and chose the model that worked best for their use cases.

Natasha had a grander vision than to just be a code generator tool: it was the codename for all AI projects inside [__Builder.ai__](http://builder.ai/?ref=blog.pragmaticengineer.com), like Microsoft using “Copilot” for all its AI projects, not only GitHub Copilot. Other products using the Natasha brandname:

- **A chatbot** that customers and developers at Builder.ai could talk to about their codebase, or instruct to implement certain features
- **A knowledge graph** : a vector database storing relationships between features, the blocks that implement them and customer use cases
- **ML models:** to predict how long it would likely take to implement a specification requested by a customer

#### What about the 700 developers?

Builder.ai had a working code generator platform built by around 15 engineers, so why did it need to hire hundreds more more in India? For one thing, Builder hired 300 internal engineers and kicked off building internal tools, all of which could have simply been purchased, including:

- **Builder Home** (dashboard for customers)
- **Builder Meet** (similar to Zoom)
- **Builder Tracker** (similar to JIRA)
- **Builder Whiteboard** (inspired based on Figma: designers would import Figma designs to Whiteboard, and then use these designs to create clickable wireframes and prototypes. Later, Whiteboard exported React code and components to the working folder of customer projects.)
- **Builder Chat** (similar to Slack)
- **SenseiBot** (review and merge PRs and deploy apps to Test/Staging/Prod environments)

One reason Builder.ai failed to grow revenue as quickly as investors were told it was doing, was likely due to this lack of focus and rebuilding tools that already existed without building anything novel.

**Builder.ai also sold an “external development network”, on top of Natasha.** There were around 500-1,000 engineers employed through outsourcing companies like Globant, TatvaSoft, and others. These devs were based in places like Vietnam, Romania, Ukraine, Poland, and other countries, as well as India. Last year, the company was working on more than 500 client apps. *This number of outsourced devs is likely to be the origin of the “700 developers in India” claim that went viral.*

Former engineers at Builder.ai told me there was internal conflict about what was the *main* product: was it the Natasha ecosystem, including the code generator, or the bespoke software development service that Builder.ai offered to customers?

The company built **Builder IDE** with a team of internal 20 devs and Natasha to help the hundreds of outsourced developers build apps for customers. Builder IDE included facial recognition to verify that the developer matched the profile in the system. It also had a fraud detection system that monitored usage. That system flagged cases where contractors billed for 8 hours, but had been active in the IDE for less.

Fraud around developer hours worked vs recorded was rampant for two years, according to Yash Mittal, former associate product director at [__Builder.ai__](http://builder.ai/?ref=blog.pragmaticengineer.com). He wrote:

“The primary bottleneck [of scaling the business] was with our external developer network. Another pioneering effort by Builder.ai involved onboarding developers globally to customize solutions on our platform using our IDEs. However, we didn't anticipate the significant fraud that would ensue, leading to a prolonged and resource-intensive ‘cat and mouse’ game lasting nearly two years before we finally got it under control.”

#### Downfall

[__Builder.ai__](http://builder.ai/?ref=blog.pragmaticengineer.com) went bust after the emergence of allegations of accounting fraud. The Financial Times [__reported__](https://www.ft.com/content/926f4969-fda7-4e78-b106-4888c8704bda?ref=blog.pragmaticengineer.com) that lenders to the company seized remaining funds once a financial audit revealed the company had apparently misled investors about revenue:

“Builder.ai submitted provisional accounts to its auditor showing large reductions to prior revenue estimates, according to people familiar with the matter. 

These figures showed that a prior $220mn estimate for 2024 revenues had been revised to around $55mn, while a previously reported 2023 total sales figure of $180mn would be restated to roughly $45mn, the people added.”

Lenders withdrawing their capital blew a hole in the accounts, and the fraud allegations ensured no new investors wanted to sink money into the business. The company’s fate was sealed.

**I’ve spoken with engineers who worked at** __Builder.ai__**, and they feel disappointed and a bit bitter about the experience.** I talked with three engineers who were incredibly disappointed at the company’s collapse, and said they didn’t spot any warning signs. After all, Builder.ai raised money from Microsoft [__in April 2024__](https://www.builder.io/blog/builder-closes-20-million-funding-m12-microsoft?ref=blog.pragmaticengineer.com) – which itself showed a strong vote of confidence. One dev told me he trusted [__Builder.AI__](http://builder.ai/?ref=blog.pragmaticengineer.com)’s leadership because former CEO Sachin Dev Duggal [__won__](https://www.ey.com/en_gl/weoy/class-of-2024/united-kingdom?ref=blog.pragmaticengineer.com) Ernst and Young’s “World Entrepreneur of the Year” award as recently as last year.


*A journey: entrepreneur of the Year in 2024, accused of misleading investors in 2025. Source:*

*Ernst and Young*
These engineers did solid work, created an AI system that felt like it was on par in capability terms with the likes of Devin and Factory. Unfortunately, the viral claim that Builder.ai used human devs to pretend to be an AI, has them fearing an impact upon their career prospects.

*This is why I want to share the truth about Builder.ai’s tech stack: that there was no conspiracy to deceive users into interacting with 700 devs in the mistaken belief they were working with a cutting-edge AI. The devs did solid work, and the company’s demise was totally unrelated to their efforts.* 

Also, I find it hard to believe that devs joining the then-high flying AI company could have had knowledge of machinations taking place at the executive management level of the business.

**So, where did the viral claim about 700 devs pretending to be AI, originate.** The Financial Times [__tracked it down__](https://www.ft.com/content/16ee837a-1d89-448b-8a33-9741025334d6?ref=blog.pragmaticengineer.com) to this post from an account on X:


*This post*

*from a self-proclaimed crypto enthusiast with no reporting history turned out to be false*
The fake claim in this post caught people’s attention, including finance newsletter writer Linas Beliūnas, who shared it with his more than 500,000 LinkedIn followers, and many publications quoted that post:


*Shocking claims travel fast, even when untrue. Source: Linas Beliūnas on*

*LinkedIn*
This is a good reminder of the importance of checking sources, and to be extra sceptical about social media posts. This also applies to me because last week this publication was among those which reported the claim. This is why I consider it important to recognise the error, and to go get the full story by talking with people who worked at [__Builder.ai__](http://builder.ai/?ref=blog.pragmaticengineer.com).

If your team is looking to hire engineers with experience building real AI systems, the Builder.ai alumni group is likely a great source of such hires. It’s sad to see a startup implode in the AI space over fraud allegations, and good luck to engineers who worked at Builder.ai in finding their next role!

This was one of four sections from The Pulse #137. [The full edition](https://newsletter.pragmaticengineer.com/p/the-pulse-137?ref=blog.pragmaticengineer.com) additionally covers:

- **Industry pulse.** A big push to repeal Section 174, Meta throws money at fixing its AI problems, Google might be preparing for job cuts, ChatGPT could be eating Google Search market share, and Arc launches “AI-browser”, Dia.
- **Stock vesting changes at NVIDIA and Anthropic.** Stock grants at NVIDIA are becoming front-loaded, while Anthropic has gone from options to double-trigger RSUs.
- **A reminder of vibe coding’s security risks.** Readers of this publication proved vibe-coded apps are a security nightmare, by bypassing the upvoting fingerprinting on a simple “vibe coded” app which I instructed an AI to make secure.

              [Subscribe to my weekly newsletter](https://newsletter.pragmaticengineer.com/about) to get articles like this in your inbox. It's a pretty good read - and the [#1 software engineering newsletter](https://substack.com/top/technology) on Substack.
