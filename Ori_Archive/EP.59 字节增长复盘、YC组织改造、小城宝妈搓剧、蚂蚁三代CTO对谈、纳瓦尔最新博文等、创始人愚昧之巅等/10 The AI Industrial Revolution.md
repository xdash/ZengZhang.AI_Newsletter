# The AI Industrial Revolution

> 原链: https://naval.substack.com/p/industrial  
> 来源: naval.substack.com · 归档自 EP.59 · 抓取于 2026-08-05  

---

# The AI Industrial Revolution

### Build your own factory

*Also on [nav.al](http://nav.al/industrial) · [Apple](https://apple.co/4x7TT0y) · [Spotify](https://open.spotify.com/episode/3Xo3RttsOvD3vm2qv7uAJ7?si=ad10562d54554bdf) · [YouTube](https://youtu.be/v6MWNrVbM4E) · [X](https://x.com/navalpodcast/status/2062583301270040581?s=20)*

[Naval](http://x.com/naval) with three frontier founders on the new means of production: [Guillermo Rauch](https://x.com/rauchg) (Vercel), [Blake Scholl](https://x.com/bscholl) (Boom Supersonic), and [Max Hodak](https://x.com/maxhodak_) (Science).

# **Part 1: Waste Tokens, Save Time**

**[Nivi](http://x.com/nivi):** Welcome. You’re listening to [Naval Podcast](https://x.com/navalpodcast), your authoritative source for new knowledge. We’re trying something new today. I have three frontier founders with us—three good-looking guys, actually, and a fourth good-looking guy, Naval.

Let me just introduce everybody.

[Guillermo “the G” Rauch](https://x.com/rauchg). He’s building [Vercel](https://vercel.com/) into an AI cloud for the world of agents and whatever comes after that.

[Blake Scholl](https://x.com/bscholl). He’s building [Boom Supersonic](https://boomsupersonic.com/)—supersonic aircraft, in his own factory, and jet engines as well.

And [Max Hodak](https://x.com/maxhodak_) from [Science](https://science.xyz/). He’s building a biohybrid brain interface that grows living neurons on silicon to restore sensory functions like sight—but eventually to explore new parts of the brain and new senses.

All three of these guys are not composing their products with off-the-shelf parts. They’re building their own factories. And we don’t care as much about what they’re building exactly as we do about what they’re learning about how they’re building.

What’s the new knowledge they’re generating?

What’s their alpha?

What principles are they discovering that other founders can learn from?

What are they trying to figure out right now?

Naval, any reactions before I jump in to Guillermo?

**Naval:** Yeah, let’s just have fun.

**Nivi:** You guys should just jump in.

## **AI Software Factories**

**Guillermo Rauch:** I can’t remember my exact quote, but I’ve been really pilled with this idea of software factories. The job of the engineer being something where you just show up to work, you ship the output directly, and everything inside the company was—“how good is person A at shipping output B?”

And now what’s happening is, the way I’m judging you as an engineer is, “are you producing the factory that will produce multiplicative outputs B through Z?”

That’s a pretty significant change. We used to believe—and it used to be somewhat controversial—that there are 10x engineers.

Now clearly there’s 100x or 1,000x engineers, and the world hasn’t fully adjusted to this.

**Naval:** I used to get flamed on Twitter for saying there are 10x engineers, because it flies in the face of so much equality philosophy that everyone’s equal. But the reality is, when you’re operating in idea domains, in intellectual and virtual digital domains, it’s not even 10x—it’s 100x or 1,000x, and it always has been.

Satoshi. Notch. The guy who invented JavaScript, the Brendan Eichs of the world. John Carmack. These are 1,000x programmers.

Not to even mention—if you choose the right thing to work on versus the wrong thing to work on, that’s an infinity difference. And it could just be not necessarily a better programmer, just one who had better judgment on what to work on in the first place.

And now obviously it’s less controversial because of AI leverage.

**Guillermo:** What’s controversial is the token leaderboards. People are still getting a little confused—“Well, I have a bunch of 100x engineers. Look at all these tokens that I’m paying for.”

I’m curious if you guys have seen the same—how do you measure ROI?

**Blake Scholl:** It’s like the old measuring of lines of code. Token consumption and lines of code feel like similarly not direct paradigms.

**Max Hodak:** My observation has been that Claude or ChatGPT is basically as good as you are in a domain. If you’re a really capable developer, these things are really powerful. If you’re a junior developer, you’ll find it to be more of a junior developer. The feedback you give them sporadically seems to be incredibly important—these little updates seem to totally determine the types of performance you get out of them.

**Guillermo:** There’s a new kind of support I give now—you come to me, you didn’t get good output out of the model, and I tell you what to prompt the model with. The quality of the reprompting is extremely important.

**Max:** To be clear, I think this will become less important over time. As the models get much smarter, you’ll be able to put in less and get more out. But at this stage, it really seems to reflect back the judgment that the user brings in.

## **Waste Tokens, Save Time**

**Naval:** I’ve kind of resisted learning all the tricks and tips. “Use [Ralph Wiggum](https://ghuntley.com/ralph). Use [OpenClaw](https://openclaw.ai/). Use [Hermes](https://github.com/nousresearch/hermes-agent). Use this prompt engine. Use this scaffolding. Plug in this piece. Always use plan mode.”

I just ignored all of that. I assumed the model is going to get better faster than I would figure out how to use it. It would figure out how to use me faster than I would figure out how to use it. So I’ve just been completely ham-fisted with them.

I get frustrated at them and have found myself typing less and less information, doing less and less work as time goes on, because I just assume I can brute-force my way through it. I’ll throw Codex, Claude, and Gemini at the same problem over and over and just waste tokens to save time. No matter how expensive these models might seem, they’re still way cheaper than a human. So I would say—just waste tokens, save time. Don’t look at the tokens either as inputs or outputs. Just look at your time, and look at the final output.

Even if they’re writing low-quality code—which I know in many cases they are—when the time comes and I want to ship to production, I’ll just throw more tokens at it. “Go through, look at it, rewrite it.”

They’re just going to get better every generation. I don’t see where this necessarily stops. As long as we have verifiable domains and solved problems, they’re going to resolve those problems. Now in the unsolved problems domain—maybe you’re [Terence Tao](https://terrytao.wordpress.com/), at the cutting edge of creativity—you need to be working very collaboratively and carefully and closely with the model. But I’m not at that level in software engineering.

## **Models Instructing Humans**

**Naval:** Guillermo, you’re probably the most extreme software engineer on the team. How are you finding these models at the edge of their capability?

**Guillermo:** There’s one thing that’s happened recently that resonates strongly with what you’re saying. It used to be that you’d give a prompt to the model and it kind of does a classic next-token prediction thing and runs away with your idea. Models now have been doing this intuitive planning mode—without you even having to ask them to plan—where it comes back to you and says, “Look, what you’re asking me for, there are these three routes we can take. Here’s the set of trade-offs.”

That’s the moment where people on X do the whole thing—“Now we have a PhD-level engineer model.”

The models at some point graduated. They used to be junior engineers. Now they’re principal engineers, because they come back to you with a set of trade-offs. And obviously, sometimes they bullshit, which is hilarious—it tells you “this is going to take three weeks” and “this many tokens.” It makes really bad predictions. But I respect the models a lot more as a peer that I’m going back and forth intellectually with.

There are still a lot of gaps. If you’re a really proficient engineer or architect, you’re still extracting more juice.

So the question Max was positing—if you’re junior, do you get junior back?

Clearly not, because a junior gets more advanced knowledge in code than they would have been able to write by themselves. But doesn’t an experienced architect get 10x where a junior engineer gets 2x? That’s what I’m trying to figure out.

**Max:** There are architectural decisions. I’m seeing this now with some of our junior software engineers on the team—what’s the next step in their career progression? It’s going from writing implementation for a feature to picking technologies. Choosing between Postgres versus some other database. Picking between [ZeroMQ](https://zeromq.org/) versus some other queuing system. The models can suggest them, but that’s the thing—you’ll see it and you’ll go, “No, no, I want to use this other thing.”

That’s the type of little feedback that really matters and the types of output you seem to get at this point.

**Naval:** It’s taste and judgment, right? That said—you can ask the models “which one should I use and why,” and they know everything. They’ll give you a really good trade-offs matrix.

**Guillermo:** That’s the change that’s happened recently. You’d say, “Hey, go put this super-high-cardinality telemetry data into Postgres.” And it goes, “No, no, bro. We don’t put that kind of data into Postgres. You should consider [ClickHouse](https://clickhouse.com/) or [Athena](https://aws.amazon.com/athena) or whatever.”

That’s happened to me a lot. Really impressive.

The thing I’m still struggling with is—clearly the human is still completing the model. At what point is it the other way around? The human is the one starting to get the instructions back: “Go get me this API key, because it’s something only you can do.”

Or “Get me this amount of capital for my next set of investments.” You just watch. Clearly we’re still not there yet.

**Naval:** That’s a temporary aberration. Pretty soon every good SaaS company or hosting provider will have a CLI and API interface the models can use directly. They don’t even necessarily need an API. As long as it’s text-based, Unix-based—the agent can hack its own API. And the money part—you insert crypto tokens, put in Bitcoin, put in whatever, and the model goes and pays for whatever it needs. People are working on this.

## **Is Pure Software Dead?**

**Naval:** The thing I’m now thinking through is—is pure software dead? Is pure software engineering an obsolete thing? It’s like saying speaking English. The models now speak English. We had to learn code to communicate with them. Now the models speak English—fuzzy, sloppy English, like a human—and they understand things. So where’s the moat for a founder? Hardware? It’s a boon. You had to build hardware, and it was hard to build a software company alongside. Patrick Collison says, “Software is art, and it’s hard to hire artists.”

Now, as a hardware founder—great, you can have really good software developed fairly quickly.

If you’re creating models, maybe that’s the new software engineering—training, tweaking, post-training, fine-tuning. But classic software engineering—is that dead? Is pure software investable? Is pure software something you can organize a company and a team around, and try to get some leverage?

**Guillermo:** Did you guys see—there was an article on X by Mitchell Hashimoto called “[The Building Block Economy](https://mitchellh.com/writing/building-block-economy)”? His argument is that the most useful thing for agents to have now is really powerful reusable building blocks. To Max’s example, you wouldn’t expect your clanker to reinvent a queue infrastructure system every time it needs to send an email. It needs to bring in the right building block, right-sized for the task—“Okay, for this one it’s [BullMQ](https://bullmq.io/).”

I challenge the notion that I’d want the agent to reinvent the entire universe from first principles in a way that’s incompatible with the rest of society and civilization. It’s almost like reinventing highways, laws, policies—just for you. Even if there’s potential for extra optimization, there’s still cooperation-at-large-scale value of saying “we’re both depending on Postgres 13.2.”

The category of infrastructure software and building blocks these agents are going to use is—obviously in bias, this is what we’re building—extremely valuable. I don’t see the agent reinventing all of that any time soon.

Another metaphor I’ve been using: anything that’s already been created that the models can reuse is like a token cache. You don’t want to churn through a trillion tokens to reproduce what’s already existing. There’s always a starting point the model can fork off from. It’s going to change things quite profoundly.

**Naval:** So these are like libraries and dependencies, but for models.

**Guillermo:** Yes—for agents specifically.

## **You Don’t Get Stuck Anymore**

**Max:** To Naval’s question, though—I learned to program when I was really little. Through all of being a teenager and in my twenties, I’d get sucked into it and code for like twenty hours. It was super fun. I knew all this stuff about different programming languages.

I haven’t written a single line of code in quite a while now. Partly that’s because my job is different. But also—since December, I’ve built a huge amount of software that I now use every day. All these projects I’d kind of fantasized about for years that I’m now using—that I’ve actually built. I didn’t write any of that. And I just can’t imagine going back to actually writing code by hand. I have a hard time seeing that as part of the future.

**Guillermo:** What’s really cool is that you understand how the pieces click together. Anyone who understands what an API is, how data flows, inputs and outputs, performance—because you have to orient the model around “this is the level of expectation I have out of this operation.” That has always been infinitely more useful than writing code. A really proficient engineering leader has been quote-unquote vibe coding through people on Slack or one-on-ones—you’re transmitting your will, your intent, your experience, and letting others run with it. Now we do the same, but with agents. That’s why you’ve been successful with it. I don’t know that everyone sees the same level of success.

**Naval:** I went from not having written code in twenty years to coding all the time now—through agents. Building tons of software. It turns out that just understanding the basic principles of software engineering and algorithms gets you a long way. The reason I stopped coding was that I didn’t have time to figure out the latest language, the latest architecture, the infrastructure pieces to plug into. And Vercel makes it a lot easier, but even then—just getting started was a bear. Plugging pieces together, assembling infrastructure was just so annoying.

**Max:** The thing that really changed is—it used to be you could build a lot, a lot would go straightforward, but then you’d hit some random thing and you could spend an indefinite period of time debugging some narrow thing. Now, with agents, you just don’t get stuck anymore. Which is pretty amazing. Relatively quickly they can find the right way to do things. It used to be that—I remember when other friends would try to learn to program, it was like—“Nope, it’s intrinsically frustrating. That’s part of the deal. That’s how you learn.”

And that just isn’t true anymore.

# **Part 2: Vibe Coding Hardware**

## **Vibe Coding a Turbine Blade**

**Nivi:** Hey Blake, how are you applying all this at [Boom Supersonic](http://boomsupersonic.com)?

**Blake Scholl:** It completely changes the role of software and hardware developers. From day one we tried to take a lot of traditional engineering workflows—hardware engineering workflows—and turn them into software. If you haven’t been around hardware engineering, let me try to make this clear. A lot of hardware engineering happens in Excel spreadsheets on engineers’ laptops in a silo. Very complex spreadsheets, sometimes with VBScript code. All of this is actually software, but it’s treated as if it’s not. There’s no source control, no automated testing. If you want to hand something off from an aerodynamicist to a structures engineer, that’s done manually with a spreadsheet over email. It’s the nineteen-nineties. It’s terrible.

So we started building software frameworks to automate and make repeatable hardware engineering flows, with the idea that we could reduce the cost of iteration. But it was slow going—we could never afford enough software engineers. What we’ve gotten into now is a mind-blowingly different model: the software engineers create the architectures, because they understand systems, algorithms, and division of concerns. Then the hardware engineers can vibe-code their pieces because they know hardware engineering. The result is mind-blowingly different productivity for small teams.

Example. If you’re designing a turbine blade—classically, a turbine blade starts cold, but when it runs it gets hot, so it gets bigger. You have to design both the aerodynamics and the structural design to work in its cold shape and its hot shape. You have to convert between cold and hot, between structures and aerodynamics. This takes one engineer one day for one blade for one piece of the analysis. There are about a thousand blades in a jet engine. You can’t do much. Now, with a combination of software and hardware people creating the solution, you can change blade geometry and see in real time the structures and aerodynamics results. Two engineers can design an entire jet engine. Wildly different.

**Guillermo Rauch:** One of the things you mentioned is that software engineers are creating the tools and architectures for the rest of the engineers. To me, that’s the biggest cataclysm of enterprise software—there’s no startup that builds hardware collaboration tools that can sell you anything anymore. Internally, you’re just coding the right thing you need at any given time. Even spreadsheets are kind of cooked. The reason spreadsheets were successful is that no one could build custom software. The thing that approximates custom software the most is a spreadsheet with a bunch of VBScript functions.

**Naval:** Right—they’re lightweight programming.

**Max Hodak:** I’ve personally moved almost entirely from Excel to [Python](https://www.python.org/) models, where I can get believable simulations of things. The thing AI hasn’t come to yet, but I think it will within the next year—probably within 2026—and that will be very exciting: right now it can generate software, but soon it will generate [STEP files](https://en.wikipedia.org/wiki/ISO_10303-21) and PCB layouts. When it comes for mechanical and electrical engineering, that’s a whole other thing we haven’t seen yet. Very cool.

## **Open Source Compounds China’s Advantage**

**Naval:** On the hardware side, this is a boon for all these little gadget companies and part companies that write really bad software because they can’t make great software. Now they’re going to be able to make good-enough software. Or it may not even be software with a human front end—it might just be completely agentic, an agent accessing it, and you talk to it through voice to control hardware.

This is one of the reasons China is big into open-source models. They’re going all in on it because they have hardware superiority. They have these very complex supply chains and component chains. They’re basically saying—“hey, if I can just generate software on demand, then I don’t have this disadvantage anymore against Silicon Valley.”

That’s not the only reason they’re doing open source. They’re also behind, they’re distilling models, they’re catching up, they’re collaborating on resources. But the Chinese government has a history of funding efforts that help their entire ecosystem along, especially in network-effect businesses. They want to pool all their resources, catch up on AI, and use it to give their hardware stuff an advantage.

Ironically, they’re doing all the open-source stuff because [OpenAI](https://openai.com/) is not open. [Grok](https://x.ai/) publishes models, but they’re a model or two behind. Google has some local models, nothing really competitive. [Anthropic](https://anthropic.com/), to my knowledge—I don’t even know of any open-source models from them. So all the open-source heft is coming from China. It helps our hardware founders, but it helps their hardware founders and factories that much more. All the crappy little software that goes with all the random knickknacks and thingamajigs you buy off Amazon to tinker with on a lazy Saturday afternoon—that software’s getting a lot better very quickly.

**Guillermo:** Everyone’s had the wake-up call that without great frontier coding models, you don’t have self-improvement. Imagine China as a whole not having the ability to produce frontier everything. It’s not just about producing software—in any piece of this hardware pipeline, like Blake was saying, you need to generate software. If you fall behind in your ability to generate software, you fall behind in your ability to generate everything.

## **You Always Want the Smartest Model**

**Guillermo:** One thing I’m curious about: everyone loves to talk about Chinese models. Do you guys use Chinese models? Do you know anybody who uses Chinese models?

**Naval:** No. This is an argument I had yesterday at dinner. One person at the table was claiming you’ll just use [DeepSeek](https://deepseek.com/) for 97% of things because it’s so cheap, and if you need more intelligence you’ll just run it over and over again—the same problem. You’ll only use OpenAI, Anthropic, etc. for the most advanced tasks. I was kind of like, “I don’t know.” I think intelligence is an unalloyed good. You always want more intelligence. When these models make a mistake, you don’t know it. And it’s always cheaper than a real person, and real-time.

So you’ll just use the most intelligent model available. Which isn’t great news, because it means you’ll end up creating a monopoly or oligopoly situation in AI. But I always want the most intelligent programmer. I always want the most correct answer. I always want the best judgment. Given the amount of leverage I’m going to pour into it—through capital and code and people and marketing—I want to make the right decision every time. When I have two models, one I know is a little smarter than the next, and they both give me answers, often I don’t actually know which is the correct answer. So if I know one model is a little smarter, I’m going to go with that answer, and eventually I’m going to stop asking the model I think is less intelligent. Have you guys found a use for these so-called less intelligent models?

**Guillermo:** We see uses. We have AI Gateway data—basically every application agent goes through it. There’s definitely usage of open models, but the top is heavily dominated by frontier intelligence.

There’s a caveat: frontier intelligence at reasonable cost and performance *slaps* at scale. [Gemini](https://gemini.google.com/)—people don’t get really excited about Gemini, but they put out models that are super smart at the right performance-cost combination. For a lot of tasks other than coding, interestingly enough, they’re the best industrial production models. You can throw them at support tasks or browser automation. I’d always put a Gemini model there, and I’d look to Chinese models for those kinds of things.

But any time I’m working to push the frontier, you need the best possible coding model. That’s basically two or three models. The Chinese are certainly not in it.

## **Software Still Needs Hands**

**Nivi:** Max, you’re pushing pretty hard into vertical integration and extreme urgency. Want to talk about that?

**Max:** For many things, you can’t buy it, so you have to make it somehow. We obviously don’t do this on things like frontier models—I have an Anthropic subscription. We actually do use some of the Chinese models, to Naval’s point. We use some [Qwen](https://qwen.ai/) models and DeepSeek models. We have a big internal fine-tune of 3.2 that I use for a bunch of things—we’re going to look into porting to 4 soon. But that’s on the personal side, not on the company side.

Our preference would always be to buy something. If there’s a vendor that offers a service at a great price—for example, PCBs. We don’t make PCBs. Those are basically free. You can buy them in unlimited quantity from Asia. But the closer our products get to being a single block of covalently bonded matter, the better they’ll be. Lower power, smaller, higher performance, longer lasting. The components aren’t available. In order to do that type of integration—to actually innovate beyond just piecing together things you can buy off the shelf, which is really very limiting—you have to learn to do it yourself. That shows up as vertical integration. So we own a captive [MEMS](https://en.wikipedia.org/wiki/Microelectromechanical_systems) foundry on the East Coast. There was no other way to do the type of packaging and assembly we wanted to do.

All of this is going to be affected heavily by AI over the next few years. It’s not quite there yet. Ironically, one of the biggest impacts we’ve seen of AI inside the company is in regulatory interactions. If we can generate documentation, or if we can ask—“we want to evolve this product, there are thousands of [ISO standards](https://www.iso.org/) that might apply, which ones do we have to comply with, trace this through”—that used to require a whole regulatory and quality team for several months. Now the AI just kind of knows.

When I think about stuff like the surgical program or the MEMS fab—ultimately the software still needs hands. It’s going to be smarter than us, but if it can’t make things, those are real boundaries. We’ve instrumented our foundry as well as many other parts of the company in ways where, as these models get better, that should show up pretty immediately in things like the cell engineering we’re doing and the material science we’re developing. Our protein engineering group really uses deep learning a lot—I think we’re probably state of the art there. But it’s very application-specific. It means different things in different parts of the company. There’s not one answer.

## **Humans Are Becoming Verifiers**

**Naval:** What Max was talking about with regulatory stuff makes me realize—it’s been a while since I generated a basic legal document using a lawyer. I stopped asking lawyers for NDAs, agreements for this, sign that, research this. All the basic legal tasks are gone too. There’s the old joke that law is like spaghetti code—very complicated code they try to put in English. It contradicts this code over here, has to fit into that code over here. There are no real [APIs](https://en.wikipedia.org/wiki/API) for it.

For junior engineers and junior engineering—junior engineers basically got a promotion to senior engineer, and junior engineering got taken over by agents. The same way, in law, you can say “paralegals just got fired,” or you can say “paralegals just got promoted to senior lawyers, and now they can spend their time thinking about the law.”

**Guillermo:** It’s actually interesting to think about the parallels between how software engineering is evolving and lawyers. You never know exactly what lawyers put into these documents—you just trust them. “Hey, lawyer, can you look at this document? Can you tell me if it’s legit? Can you do red lines?” What you’re valuing in the relationship with a lawyer is that they’re a trusted authority. They went to law school. They’re putting their reputation on the line.

There’s a parallel with software engineering. The biggest problem today is this mountain of slop that ends up as a [PR](https://docs.github.com/en/pull-requests). There are all these memes on Twitter—“way back in the day we used to read every line of code of a PR.” Well, in my world—infrastructure—I want engineers to be able to say “I understand” every line of that PR. That doesn’t necessarily mean you’ve read every line. It means you can say “I understand the consequences of this PR. I’m signing off on understanding the consequences.” Or, “I wrote the test harness, the simulations, the proofs, the type-checkers—even without reading this, I have confidence I can sign off that it’ll be safe in production.”

There’s a world in which we embrace that everything is going to be spaghetti code we don’t fully understand, but we write the evaluators that give us confidence, and we rely on people—the infrastructure production engineers—to say, “Okay, I’m fine sending this into prod.” Someone is going to get paged if your systems go down. Another thing people are underestimating: creating software is really easy, zero to one. But think about a thousand days from now. What does your software look like? Is it secure? Is it tested? Is it production-grade? Is it performant? And are you still motivated to invest all those tokens in maintaining it in prod?

**Naval:** Humans are becoming verifiers. That’s how we train these models—with good verification data—and now we need human verifiers. A lot of the old function of people, lawyers, engineers, operations people, moves to verifying the stack and saying, “Yeah, this is roughly correct, I’ll roughly stand behind it, I’ll support you if it goes wrong.”

# **Part 3: The Regulatory Frontier**

## **The Regulatory Red Queen Race**

**Blake:** One of the things we’ve seen related to regulatory—it massively reduces change aversion and improves iteration. Example: let’s say you’re going to certify an airplane. One of the zillions of things you have to do is prove it can withstand a lightning strike. The regulatory documentation for the test plan stretches on for, say, 200 pages. What you would classically do is hire a—let’s be honest—not super-bright engineer who’s willing to be there, monkey at keyboard, writing 200 pages of regulatory compliance documentation. It takes a couple of months. And by the way, if you *change* the airplane, now you want to cry, because there’s another two months of rework of this rote compliance documentation.

What we’ve found is we can build a [RAG](https://en.wikipedia.org/wiki/Retrieval-augmented_generation) that will enable us to basically prompt our way through all of that work in—let’s call it minutes. The first-order effect is you save a lot of time. The second-order effect is, if you change the specification of the airplane, it now takes minutes, not months. So you can actually be *willing* to change. And the third-order effect is you can get rid of the not-very-great engineers and have a small number of really creative ones who can iterate rapidly, because the cost of change goes down. In a certain sense, the entire regulatory burden—which really hurts the ability to iterate—drops away.

**Max:** This is a really undersold story in AI right now. The consensus in Silicon Valley is that regulation sucks—we want to go faster, we want to realize this amazing future, we want abundance, prosperity, and stuff that slows down that future is to be avoided. Certainly we’ve over-regulated. We’ve made it impossible to build stuff. It’s totally crazy what goes into building any physical thing in a lot of places.

But a lot of the regulations themselves are not the problem. If you’ve actually read a lot of these things—having non-smog-choked cities is great. Being able to swim in many rivers is great. A lot of these things were progress. The problem is that it’s really difficult for humans to deal with understanding and complying with this, and every time you have to exchange a letter with the government, you wait months. If you could take a lot of the things we’ve learned and make them totally frictionless, that would be pretty cool. I think that’s an under-sold story.

**Naval:** Until the regulator starts spewing tokens back at us. Then you start getting huge amounts of documents from the regulators that you have to comply with, and it’s agent-on-agent wars. But at least it’s a fair fight.

**Max:** That’s basically what we have now.

**Blake:** I’d actually argue that would be an improvement from where we are now. One of the terrible things right now is, if you’re going to build anything physical, you have to get a building permit. You’re guilty until proven innocent. The worst thing we’ve run into is the fire department, because they have the moral imprimatur of *people pulling people out of burning buildings*—and yet what they actually do is just screw with your design for buildings for months. If we could replace the fire marshal with an agent that would critique your building plan quickly—even if its feedback were overdone—it would be massively better than the delays that exist today.

**Guillermo:** When Max was talking about this potentially being a good thing—that we have all this regulation—my head went to: the thing that makes agents successful is humans or other agents setting up the right testing guardrails. People are really excited about slash goal, or Ralph loops, where you tell the model, “Go do this, and this is your exit criteria.” I’m telling Blake, “Go make us all supersonic. Your exit criteria is that you’ve complied with all of these regulations.” There’s totally a world where we say the regulations are great—they’re like our test suite. As long as passing them doesn’t incur contradictions, and the regulations are actually reasonable, they’re an awesome guardrail. Otherwise we’d be shipping slop directly into the air.

**Naval:** This is going to turn into a [Red Queen’s race](https://en.wikipedia.org/wiki/Red_Queen_hypothesis). They’re going to have agents, we’re going to have agents. I think we might have better agents—that’s good, as opposed to human-versus-human. But their cycle time, their response time, may get longer. The App Store is drowning in spam right now. I’m sure the patent office is drowning in spam. These agencies are going to be slow adopters of AI. They’re going to get DDoSed by clever entrepreneurs just overloading them with documents. It’s possible the approval time for this stuff may extend out as it suddenly gets flooded.

## **Why There’s No Innovation in Healthcare**

**Blake:** It creates an opportunity to really shift the regulatory model. Imagine if we drove around a city the way we build things today. Before you could go anywhere, you’d have to write a plan, ship it to some regulator, and wait. Your plan would have to specify, “We’re going to take such-and-such a route, drive this speed limit, use our blinker, stop at every stop sign, never run a red light,” blah blah blah. Three months later you get a critique back: “We think you should drive on this other street.” Eventually you get approval and you go drive somewhere. It’s insane—you can never go anywhere. And yet that is absolutely the way we build physical infrastructure in this country. We should actually make more of these things enforcement-based, rather than pre-approval-based.

**Max:** I don’t want to be under too much—if I ship a medical device to a lot of people, there needs to be—there are unknowns. We were responsible, we did clinical trials, we reported all the data, but—

**Naval:** Max, this is why there’s so little innovation in medical right now. The FDA approval process is a nightmare. In fact, the two biggest advancements in tech in Silicon Valley in the last decade—AI and, before that, crypto—they’re both in the math domain, because that’s the last unregulated domain. When they start regulating frontier models and start regulating GPUs, that stops as well. Peter Thiel laments that there’s no innovation in the physical domain. Well, it’s been held back by huge regulatory barriers.

You can always find a scary case—a vaccine, or a famous medical disaster—but the regulations spread everywhere, the tentacles are everywhere, and there are all these contradictory regulatory bodies. [SpaceX got sued](https://www.justice.gov/opa/pr/justice-department-sues-spacex-discriminating-against-asylees-and-refugees-hiring) for not having enough—I forget what—migrants or refugees or whatever, but they’re not *allowed* to hire them, by government regulation on the other side, because they’re not citizens. This is not like logical code that has to compile in one place. These are made-up random regulations all over the place. You might comply with one state and violate another, violate federal over here, annoy this guy over here, that guy chooses to prosecute one out of fifty people who are his friend. It’s arbitrary. It’s capricious.

**Blake:** And the idea that this makes things safer is a complete mythology. Watch Boeing. They certified the [737 MAX](https://en.wikipedia.org/wiki/Boeing_737_MAX_groundings), which had a single sensor that had complete authority over the nose-up, nose-down attitude of that airplane. No intern is dumb enough to think that’s a good idea. Yet it got all the way through the certification system. This stuff doesn’t actually make us safer, it just makes us slower.

**Max:** Well, there’s definitely dysfunction here. I think some of this makes us safer in the sense that the [NRC](https://www.nrc.gov/) makes us safer—which is that their job was to make sure nuclear energy was safe, and they did this by permitting zero plants from the seventies until I think a year ago. It will be perfectly safe if we never build any of it.

I want to be really clear—I’m on the side of deregulation on a lot of this. I agree with Blake that a lot of this can be done more efficiently. But I also think it’s a little too dismissive to say, “This is just the FDA, the agencies.” The problem is deeper. If the FDA approves ten really important drugs, they don’t get any credit. One patient dies, and they get hauled before Congress and yelled at. They have very negatively-biased incentives. The reality is that this is reflective of the beliefs of the American people. There’s a trade-off between the perception of risk taken in human-subjects research, and the rate at which we get new medicines.

**Blake:** It’s totally asymmetric. If you approve a bad thing, your career is over. If you block a good thing, nobody notices. It creates an asymmetric slowdown. I think that is the most important problem to solve in the regulatory state.

**Max:** This is a very deep problem because it is where the voters are. We poll some of the stuff we’re working on in the future to understand where the American people are on it. If you push too hard, you can work around it—go to [Próspera](https://en.wikipedia.org/wiki/Pr%C3%B3spera), all kinds of ways to try to go faster. But if you’re seen as being a bad actor, you’re rejected from the society we live in. That’s the thing you need an answer for. That’s deeper than just saying, “We need regulatory reform.”

## **We Need a True 50-State Experiment**

**Naval:** You have a deep point there, Max—it’s where the voters, the citizens, are. We like to blame politicians. You’ll see this on X all the time—people are like, “This politician, that politician, the other politician.” They’re elected, by majority vote. This is where the people literally are. That’s the package, that’s the bundle they’ve chosen. You may not like this instantiation, but if you removed this one, something very similar would take its place, because the voters would just vote them right back in.

Culturally it’s very hard for most people to understand what we lost, what we missed. France—there’s a French entrepreneur on X lamenting that 57% of GDP gets sucked up by the government, so you can’t create companies. But to the average French citizen, that’s not visible. They don’t notice what they’re missing. They just know they’re slightly poorer than the US.

[The Economist](https://www.economist.com/leaders/2026/05/21/americas-economy-is-soaring-even-with-the-maga-tax) [just did a little piece](https://www.economist.com/leaders/2026/05/21/americas-economy-is-soaring-even-with-the-maga-tax)—economists are finally coming back around to being capitalists after thirty years—on how the US is outstripping everybody, growing faster, getting bigger. But they immediately turn around and say, “It’s because of the oceans, because of natural resources”—everything but capitalism. They don’t want to say the dirty C-word, because for some reason all these magazines became Marxists at some point. They can’t envision or imagine what could have been if we had just been a little more laissez-faire, a little more open.

I would love to see a true experiment among the fifty states. Different regulations, different tax structures. Right now federal tax structure and federal regulations dominate everything. But imagine you could go to some small state if you had cancer, and you could try every drug everyone was cooking up. *Caveat emptor*—you’ve got to do your research. This is known as the experimental zone. Same for drones. Same for aircraft—a little harder, because you’ve got to cross a lot of areas—but yeah.

**Blake:** There’s something magical in there—the notion of innovation zones. We have a huge [NIMBY](https://en.wikipedia.org/wiki/NIMBY) problem. But if you create opt-in [YIMBY](https://en.wikipedia.org/wiki/YIMBY) zones, they create that experimentation framework. By definition, it happens where people are consenting. You can try different rules, or no rules, or different ways of enforcing—innocent until proven guilty—and see what actually happens. What are the innovation consequences? What are the safety consequences? Then the successes can spread.

**Max:** To Naval’s point, an innovation zone would not solve the problem in drug discovery. The [Right to Try Act](https://en.wikipedia.org/wiki/Right_to_Try_Act) passed a little while ago. We’ve had this pathway called [Single Patient IND](https://www.fda.gov/about-fda/center-drug-evaluation-and-research-cder/physician-request-single-patient-ind-compassionate-or-emergency-use) for a lot longer than that. If your doctor calls the FDA and says, “I want to give my patient an unapproved drug,” they approve over 99% of those. They can even grant them over the phone.

The problem is that to dose a patient you still need clinical-grade drug. The only entity with that is typically the IP owner who’s in the middle of running a clinical trial—they’re investing hundreds of millions of dollars into making this thing. The FDA will draw an adverse inference if something bad happens to your patient who’s probably really sick to begin with, and that’s seen as a property of the drug, which is global—not related to your innovation zone. So there are two problems. One, you need to get the IP owner to give you some of their drug—they’re not going to do that. Two, you need to prevent the global regulator from casting doubt on what might happen with their clinical trial if they give you some.

**Blake:** How would you address that in medicine?

**Max:** This is inside baseball. The FDA has to be prohibited from drawing adverse inferences across different users of a [capsid](https://en.wikipedia.org/wiki/Capsid), for example. There are specific ways you could really accelerate innovation with a relatively light regulatory touch by just preventing this paranoia from driving our decisions.

## **China’s FDA Is Beating Ours**

**Guillermo:** Is there anything better than the FDA out there? What are we benchmarking these regulators against?

**Naval:** Everyone follows the FDA. Everyone copies the FDA.

**Max:** Two expansions. First, Europe—not really better than the FDA, but they have a different system. They’ve got these [notified bodies](https://en.wikipedia.org/wiki/Notified_body)—basically private businesses blessed by their host governments to certify things. Trains, planes, medical devices. The notified-body system creates slightly better incentives at the review layer because they can hire people, they can grow, there’s competition. They themselves have to be compliant with conditions placed by host governments, but it means there can be many thousands more reviewers than in the US.

Second—there actually is one approved, getting-paid implantable [BCI](https://en.wikipedia.org/wiki/Brain%E2%80%93computer_interface) today, which is in China. The [CFDA](https://en.wikipedia.org/wiki/National_Medical_Products_Administration) is thinking for itself. They have a system that I think is going to give us a run for our money if we’re not careful. The costs to bring a drug or device to market are just much lower. You can try things in humans and try things on market.

Here’s the thing I’ve been spending a lot of time thinking about. Twenty years ago we were buying far fewer laptops and phones; each one was much more expensive. Now they’re cheaper, there are far more of them, we buy more of them, total spending has gone up. This is great. Stock prices of Qualcomm and Samsung and Apple are way up. Everybody’s happy. They’re using the excess wealth generated by phones and laptops to buy more phones and laptops.

This doesn’t happen in healthcare. Because of the reimbursement mechanism—there’s this enterprise sale happening—the bucket of money we use to buy healthcare is basically fixed. It is not increasing as there’s more stuff producing better healthcare outcomes, the way we see in technological growth industries. The rate of spending on healthcare grows at roughly the rate of growth of tax receipts. If AI is booming and there are major advances, and two years from now we’re spending ten times as much on AI, this could be great. But if in two years we’re spending ten times as much on healthcare, this would be a catastrophe. This is fundamentally at odds with being a technological growth industry.

There’s this omni-problem in healthcare, all related to the same thing: it’s just too expensive to bring these things to market. That’s what China is getting at. The way out of this is not single-payer or some revision to health insurance. It’s to bring down the costs so that someone can buy this with a credit card, finance it, maybe like a car, worst case—and then you charge them in the transaction. To do that, we have to make it cheaper to bring these things to market. China is doing that. That will allow them to sell these things for $10,000 instead of $100,000. That is deregulation.

## **Healthcare Is a Communist Society Inside Capitalism**

**Naval:** Fundamentally, there’s no private market in healthcare. The analogy people make sometimes—imagine that instead of going to restaurants and paying, you’d go to all the restaurants, and at the end of the month you’d send all the receipts and bills to your insurer or to the government, and they would reimburse you. There’d be a line outside every good restaurant. Every bad restaurant would be available. The waits would be terrible. The product wouldn’t improve. You’re basically running a small communist society inside a larger capitalist society. That’s what we’re doing in healthcare.

**Blake:** It’s also what we’re doing on roads, which is why we have traffic. There’s no variable pricing for getting on the highway, which is why it’s always clogged.

**Naval:** If you want to step on the third rail of healthcare for a moment, think about this plan. Tell me what’s wrong with it. Imagine that the first 20% of your annual income was your healthcare deductible. If you’re broke and homeless, it’s zero. If you’re rich, it’s millions of dollars. Whatever your annual income is, the first 20% is your healthcare deductible. The rest is paid by the government and the insurance system, up to the usual caps they have today.

You’d create a private market pretty quickly. In dental, plastic surgery, a lot of optional medical procedures, you’d get a competitive situation. You get improvement. Look at optometry with LASIK. Look at dental with veneers and braces and dental surgery. Look at plastic surgery. Those fields do seem to be advancing because they’re private payers—people voting with their money.

We need to do some equivalent of that in the normal healthcare system. But people lose their minds. They don’t even want to think one step ahead. “No, no, no, what about the broke person?” The broke person has no income. “Twenty percent is too much for some people.” Okay, you can put some deductible in there. But generally, if you don’t have some private market where people are paying out of pocket for what are medical procedures, you’re just not going to get this feedback loop. You’re not going to get this ability to spend more money into the system.

Right now, very wealthy people can spend voluntarily into the system. But the prices aren’t anywhere. The rate cards aren’t anywhere. The system’s not designed for it. If you go shopping for medical care and you want to pay out of pocket, sometimes they’ll quote you a price that’s 10x what they charge the insurance company.

## **Sid’s Story: N-of-1 Medicine**

**Max:** Have you heard Sid’s story from GitLab? He had a massively successful IPO, then was diagnosed with a rare cancer. He has lived way past the prognosis. He really took it into his own hands. He did frontline chemo, then there was one alternative available, he exhausted it, and the doctors were like, “We’ve got nothing for you.” Since then, six or seven companies have come out of it. There are now twenty or thirty drugs in his escalation ladder. He’s still alive.

**Guillermo:** He’s doing great. I saw him the other day. He basically created his own personalized medicine and treatment plan.

**Max:** There are a handful of these anecdotes I’ve heard now. It is really clear to me that at the high end—if you’re not dealing with insurance, you have the resources, you’re like, “I want the full toolbox of modern science”—outcomes are possible that are crazy. If you go ask your doctor, “What will happen if I do this?” they will start shouting and throwing things. But crazy things are possible at the high end. This type of N-of-1 medicine is going to end up being a really rich source of research for understanding how to build more translatable things.

**Guillermo:** It requires a ton of agency from the patient in a moment where they’re at their weakest, which is pretty ironic. My friend passed away from cancer, and the last thing he wanted to do was research N-of-1 medicine—he was dying by the week. This is where AI should really shine, and democratize what you can actually do when you find yourself in that situation. It’s kind of crazy how few people get access to this, just from a knowledge perspective, not just monetarily.

# **Part 4: The Autonomous Company**

## **Autonomous Infrastructure**

**Nivi:** How much autonomous software do you have in your organizations that’s running on its own, or near-autonomous and improving on its own?

**Guillermo:** A lot of our infrastructure is already autonomous. We have a capability that fires off upon finding anomalies—I recommend everyone create a version of this, or Vercel offers one. Today most engineering organizations respond to anomalies by setting up alarms or monitoring thresholds by hand, which is pretty insane, but that’s how the entire industry works.

We’ve automated a lot of the [SRE](https://en.wikipedia.org/wiki/Site_reliability_engineering) job—Site Reliability Engineering. Any metric that slows down, speeds up, or changes throughput fires an anomaly alert, an agent investigates, and the agent can decide to create an incident. If an incident is filed, people get looped in and the agent begins remediation. We’re doing everything except giving the agent the tools to change prod—we’re serving solutions on a silver platter to engineers.

The other thing working really well: autonomous optimization and autonomous security research. We open-sourced a tool called [deepsec](https://vercel.com/blog/introducing-deepsec-find-and-fix-vulnerabilities-in-your-code-base). It’s incredible—like Mythos, but you get it today. We run it against our entire monorepo using ten thousand concurrent agents in the cloud. It found several quarters’ worth of security-research progress in a couple of days, for fourteen thousand dollars of tokens—months of red-teaming, entire teams of people.

Cybersecurity is becoming a nightmare: too many vulnerabilities, too much work, adversaries too powerful. You have to invest proactively. You’ve probably seen people on Twitter translating codebases from one language to another—once you’ve done the work to get a working program, optimizing or rewriting it in a native language is now quite doable with frontier models.

**Naval:** Just from my own vibe-coded app—I built a bug-reporting queue for my [TestFlight](https://developer.apple.com/testflight/) users. They report bugs from inside the app; it uploads the logs and a screenshot. Of course they use it for feature requests too. A simple daemon compiles all the bug reports, proactively analyzes and fixes them in the background, then ships me a TestFlight build to try before I ship it to the testers. I could see an app in the future literally built by its users. I’m not saying that’s a good idea—it might be a mess.

**Guillermo:** We should ship that, just to see what happens.

**Naval:** As a social experiment. You’d end up with a [Homer Simpson car](https://en.wikipedia.org/wiki/The_Homer)—an umbrella, a flashlight, a clown horn, every feature. But for bug-fixing, you could definitely do it.

## **Your Job Is to Train the Agent**

**Blake:** We did a version of that experiment. I stopped all project work across the entire company for a week and said, “Everybody, from the receptionist to the engineers, build whatever you think is the most important thing to build. Your only requirements: you have to use AI, and you have to demo it for the whole company when you’re done.” I expected a large number of silly projects and a small number of needle-movers. We got the opposite—a large number of needle-movers and very few silly projects. Two or three were trajectory-changing; they’d absolutely change the direction of the company.

What surprised me most: the receptionist—the ship-and-receive associate whose job was to take packages off a truck and email people when their stuff hit inventory—built an automation for that. We’re actually using it.

The conclusion I came to: everybody has some idea of what could exist that would make the world better, but their first-order ideas are often stupid, and they can’t project that out and see it. But if they can go from idea to an actual thing, they can react and iterate. Give them a week, and by the end they’ve built something that makes sense.

**Guillermo:** Imagine if all work was like that. How do you set up a workforce that doesn’t do the work directly—all they do is train the agent that does it for them? You have to remind people, create hackathons. There’s a culture change happening: a lot of people coming in intuitively know their job isn’t to work on the thing, it’s to train the agent that works on the thing.

**Naval:** It could get a lot crazier. Maybe you just turn on all the cameras, and the agent watches everything happening, sees that the shipping-and-receiving process is inefficient, and writes the app and presents it.

**Guillermo:** We’re likely going to ship a feature into AI Gateway that lets people opt in to preserving inputs and outputs. Then you can say, “For all my inputs and outputs, extract the skills—learn from my work and dump it as skills I can download for myself.”

You could imagine people in companies wanting to share and pool this together.

**Naval:** It’s funny—for me that’s unimaginable, because my own work isn’t repetitive. I look for things to automate, and there’s almost nothing left to automate in my own work. I hope that’s where everybody ends up: you work in your maximum zone of creativity and interest at all times. If there’s anything left to automate, automate it—get it out of your life, it’ll free you to be creative, and that’s where you generate all the value.

That’s hard to see in the job-career mindset, because you hire people to do the same thing over and over, and that’s going away. It’s scary—people ask, “What am I going to do?” You’re going to do creative things. You don’t have to come up with a new thing every day—that’s impossible—but once in a while you come up with a new thing that creates a point of leverage.

## **The Next Lord of the Rings**

**Max:** Historically the returns were maybe 70% intelligence, 30% agency. Now it’s going to be 70% agency, 30% intelligence—and that’ll shift further as the models get better.

**Naval:** I’ll take the counterpoint, Max. I think it’s 99% intelligence and 1% agency—because the agents will exercise the agency. You’ll literally say, “Hey agent, I’m making smart decisions and thinking big thoughts; just go implement stuff.” Sometimes I want to build a feature on an app I’m vibe-coding, and I’ll ask the agent, “What feature should I build next? Go look at the logs.”

**Max:** To be clear, I’m talking about the returns *to humans*. The humans best fit for the future are the ones who are more agentic—the ones who can open Claude and think, “What should I build?” instead of watching YouTube.

**Naval:** Here’s a fun experiment. We all know a lot of people now who are coding who weren’t before—including, in many cases, ourselves. The percentage of coders has probably gone up 10x.

**Guillermo:** It’s why our sign-up numbers are through the roof—a whole new class of people who aren’t engineers.

**Naval:** But the majority of people still aren’t creating code. I tell people, “Vibe coding is so much fun.” I had a gaming group I used to play first-person shooters with to blow off steam; I completely stopped. That time went to vibe coding instead. It’s more entertaining, you get something real out of it, and the feedback loop is just as tight or better.

I tell my friends, “You should be vibe coding instead,” and they give me a blank look. To them it was always a black box—they assume you’re just talking to the computer. They don’t realize it’s a lot easier now. So we might’ve gone from 0.01% of the population writing code to maybe 1%—call it 100x—but 99% still never will.

**Max:** It’s crazy. It’s like a video game—a great video game—but real stuff comes out.

**Naval:** The normies have gotten a little more into it, but through media models—video models. More people have fooled around making videos and images than writing code and apps. But video has its own issues—someday “make me a great movie about X” spits out a good documentary, but right now they don’t have the taste or the judgment.

**Max:** This is a bet I have with Andrej Karpathy: what year can you dump in a book and get a movie out? I think it’s close—he’s come down substantially on his timeline. By 2030 we’re going to have dozens of Lord of the Rings—some fan saying, “He did it wrong, I’m making my own take.”

One of my benchmarks: I’m a huge fan of *[The Expanse](<https://en.wikipedia.org/wiki/The_Expanse_%5C(novel_series%5C)>)*. There’s a TV series and nine books; they made the first six books but not the last three, and there are meaningful divergences. I’m looking forward to dumping in the last three books, conditioned on the TV series, and saying, “Generate the last three seasons.”

**Guillermo:** That’s a great feature. When you said, “Get me the next Lord of the Rings,” I got excited—because we haven’t had a breakthrough in imagination, in culture, the likes of Harry Potter and Lord of the Rings.

## **What’s Your Definition of Art?**

**Naval:** So what can humans uniquely do? This gets to the core issue. Max, you’re an AGI maximalist—so for you it’s nothing; agents will do everything.

**Max:** I’m not anti-human, but if your identity is how smart and creative you are, you’re going to have a bad time.

**Naval:** I’m still on the other side of that. Creativity is the thing that surprises you—you step out of the system and do something that wasn’t even imaginable within it. It’s outside the training data, out of the distribution that was fed into the system. There’ll always be room for that.

**Guillermo:** Have you noticed every Claude website looks the same? People dial in what a Claude website looks like—serif font, brown and cream, monospace with a certain spacing. After a while you get a distribution, and you say, “This isn’t creative. This is slop that came out of Claude.”

**Max:** To be clear, I don’t think it’s human versus computer—it’s human *with* computer versus *just* computer. But the computer’s going to produce crazy super-stimuli; it’s going to make the entertainment. We see a weak form of this in TikTok. My personal definition of art is meaningful out-of-distribution behavior—something surprising, like you’re moving in the Z-axis. And “meaningful” means it changes your future trajectory through the universe—your life is somehow different for having thought it and reflected on it.

**Max:** My definition is broad. There can be military maneuvers you’d call art. We’re going to see [Move 37s](https://en.wikipedia.org/wiki/AlphaGo_versus_Lee_Sedol#Game_2) all over the place. What’s your definition of art?

**Naval:** I have multiple definitions. I think of art as conveying emotion—something you felt, transmitted to another person; you create an object that captures an emotion you felt inside. By that definition a computer is almost incapable of it: the exact same piece of art without intent behind it is meaningless. You can argue nature is art—a sunset—but that’s pure intelligence working without motive, so no ego gets involved, and your brain recognizes the complex system. Art in the human sense is: someone felt something and wanted you to feel it. So the identity of who created it matters.

**Max:** So a beautiful photo—if a person takes it versus AI generating the exact same photo down to the last pixel, the person taking it has more meaning for you.

**Guillermo:** Do you remember [ControlNet](https://en.wikipedia.org/wiki/ControlNet), a year or two ago? There was a medieval-village scene with a swirl in it—AI-generated. That was one of the first times I looked at this and thought it was really cool.

**Naval:** But doesn’t that break your premise? A human came up with the training and the prompt to arrive at that riddle. It’s possible AI does that itself in the future, but I give whoever came up with that optical-illusion ControlNet idea the credit.

The bar is going to be raised massively—it’ll take more and more to surprise you. Like Studio Ghibli: OpenAI destroyed Studio Ghibli for everybody. Nobody wants to see another Studio Ghibli work again. It’s been done.

**Naval:** Right, but art has to be out of distribution. Once you’ve seen tons of Studio Ghibli everywhere, it’s in distribution—no longer surprising, and the art value is gone. Humans are the ones who generate surprise completely out of the data distribution, and they do it with intent—and intent matters for meaning. Take an AI trained to be perfect at mathematics, within the formal system. Then [Kurt Gödel](https://en.wikipedia.org/wiki/G%C3%B6del%27s_incompleteness_theorems) comes along with something completely outside the system—the incompleteness theorem—stepping outside it to break it. That kind of thing I don’t think an AI can get to. The meaning comes from the fact that a human did it for a purpose and conveyed something.

## **Can AI Have New Ideas?**

**Max:** The really deep question: is it possible for an LLM or transformer to go out of distribution—to have a new idea that wasn’t present in the training set?

**Naval:** The training sets are so large it’s hard to imagine ideas that aren’t in them somewhere. But if they exist, they probably lie in the natural domain—physics, interaction, feeling, emotion, evolution—things language isn’t subject to. There are still things outside of language, though language is a great compressor of a lot of it.

**Max:** I think the question is how you go out of distribution without randomness. In [reinforcement learning](https://en.wikipedia.org/wiki/Reinforcement_learning) you can sample an action from a distribution and get randomness that walks you into new territory. Can humans go out of distribution—where does any new idea come from? Are we also dependent on randomness?

**Naval:** We’re not dependent on *pure* randomness. Natural selection works through pure randomness—mutate a gene and see what happens. But humans seem able to cut through infinite space, eliminate huge swaths, so our creativity makes sense within the larger scheme. That’s one of our unique capabilities. Maybe AI is starting to do that at the edges, as we’re seeing with some math problems—but math is a very bounded domain. At the moment, truly stepping outside and surprising people is still the domain of humans. Human plus AI is where it’s all moving. Human without AI, forget it; pure AI isn’t there yet—but human plus AI, we’re in that era, and I’m betting we stay there longer than people think.

## **A Very Large Number of Small Teams**

**Naval:** Humans will have an enormous amount of value—more value. Everyone here, our productivity has gone through the roof. Basic economics says that when productivity is higher, you’re wealthier and you hire *more* people, not fewer. If someone’s really good with AI and really smart and creative, I want to hire them more than ever, for the leverage.

**Guillermo:** That’s a new requirement. We’re hiring juniors and super-seniors, as long as they’re really good with agents and quick to adapt. My hypothesis is we end up with a larger number of smaller teams. The number of people required for any given task drops a lot. People who only see first-order effects say, “All the jobs disappear—I can do a jet engine with two people, not a thousand; 998 jobs gone.”

But what it actually means is you can create a lot of *different* jet engines. We’ll get an explosion of entrepreneurship, an explosion of founders, and a very large number of very small teams.

**Naval:** AI provided base-level intelligence and domain knowledge and cut through the jargon; now agents provide a lot of agency. So what’s left is creativity, taste—and yes, you need enough agency to get started and to stick with it, but you don’t need to spend twenty years learning one thing before you can contribute. That barrier going down means generalists are having a field day.

At the end of the day we’re all generalists—we like to think about everything. Max is here talking about consciousness and the FDA and brain science and creativity. The people on Twitter fond of saying “experts, credentials, sources” are the ones getting hurt, because the expertise matters less now.

You spend five or ten years getting a PhD—hopefully it developed your creativity, instincts, taste, and judgment, because if all it did was help you memorize jargon and scaffolding, AI cuts right through that. It’s a bicycle for the mind, accelerated. So it’s people with AI versus people without AI—and the single best thing you can do for yourself is get really good with these tools, and always know the edges of what they can and can’t do. And that’s a moving target.

Amazing read!

Thaaanks! It's amazing to really get the recent insights from Naval.
