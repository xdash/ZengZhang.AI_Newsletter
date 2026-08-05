# My biggest takeaways from my conversation with GitLab's first-ever CIO, Manu Narayan

> 原链: https://mattpaige68.substack.com/p/my-biggest-takeaways-from-my-conversation  
> 来源: mattpaige68.substack.com · 归档自 EP.66 · 抓取于 2026-08-05  

---

# My biggest takeaways from my conversation with GitLab's first-ever CIO, Manu Narayan

### Past the productivity ceiling: rebuilding the enterprise from first principles. Why efficiency gains flatline, why skills (not agents) are how AI scales, and why context is the new moat.

60% of DevSecOps professionals say the ROI from AI coding is exceeding expectations.

73% of the same group are worried about the long-term maintainability of the code it produces.

Same survey. Same people. ([GitLab’s new AI Accountability Report](https://about.gitlab.com/resources/ai-accountability-survey-2026/), 1,500 DevSecOps professionals.)

That contradiction is the enterprise AI story right now. Teams are shipping faster than they ever have, and they’re quietly nervous about what they’re accumulating. Most companies respond by optimizing harder: more speed, more volume, more lines of code.

[Manu Narayan](https://www.linkedin.com/in/manunarayan/) thinks that’s aiming at the wrong target.

Manu is GitLab’s first-ever CIO. The company where software gets created (NVIDIA, Lockheed Martin, and Barclays all build on it) decided that internal AI transformation needed its own seat at the executive table, and brought Manu in to run it. His job is everything internal-facing: how GitLab uses GitLab, and how every team member from sales to support gets real leverage from AI.

I had him on [Talking AI](https://hatchworks.com/talking-ai/productivity-ceiling/) this week, and his core argument has been rattling around my head since: efficiency gains alone drive you into a productivity ceiling you can’t engineer your way out of. 

A faster version of a pre-AI workflow is still a pre-AI workflow. The way past the ceiling is rebuilding the workflow from first principles.

Here are my top 8 takeaways.

*(Each quote has a timestamp, so you can jump straight to that moment in the episode.)*

## 1. Incremental gains are table stakes. Hunt the nonlinear ones.

Most AI programs celebrate the 15% efficiency bump. Manu’s team treats those as the baseline, worth capturing, never the goal.

“We’re not really interested in just the nominal gains or incremental efficiency gains that somebody can get. Those are important. We wanna capture those. We wanna enable our team members to have access to all these great tools. But we really wanna see where can we find outsized gains, or nonlinear benefits.” — Manu Narayan (~18:30)


Nonlinear looks like 5-10x’ing development team productivity through agentic development, or collapsing support resolution times, measured through innovation velocity and delivery timelines rather than activity. And his first move to get there wasn’t a tool rollout. It was executive alignment:

“We are not looking for incremental gains. We’re looking for a wholesale transformation.” — Manu Narayan (~43:00)


That alignment turned into a tight partnership with GitLab’s Chief People Officer on evolving roles, AI literacy, and enablement. Which tracks with what [PwC’s Chief AI Officer told me](https://open.substack.com/pub/mattpaige68/p/i-just-sat-down-with-pwcs-chief-ai?r=57u8oy&utm_campaign=post-expanded-share&utm_medium=post%20viewer) a few months back: AI value is 80% business transformation, 20% tech, and most companies invert the ratio. 

If your executive team still thinks AI is an IT project, you’ve already chosen the ceiling.

## 2. “All politics is local.” The org model is hub, spoke, hub.

Manu’s diagnosis of why AI adoption stalls inside companies is the most humane one I’ve heard:

“You have this idea of the AI haves and the have-nots. You have people who have embraced the technology, understand how it works, have incorporated it into their workflows. And then you have the people that haven’t, and that’s not by their own fault. It’s really a mix of their enablement.” — Manu Narayan (~3:55)


His fix is a hub-spoke-hub model. A centralized team owns governance, technology choices, and the deep technical builds. Then every department gets an embedded **AI transformation owner**: someone who knows the workflows, the processes, and the people well enough to be the bridge between functional and technical. 

Those owners build a center of excellence of champions inside their division, surface the best bottom-up ideas, and route the ones with real scale potential back to the hub for investment.

“I’m a believer of the saying all politics is local. The best way to drive meaningful transformation is more localized to the personas and roles that ultimately need transformation.” — Manu Narayan (~5:00)


The have-nots don’t need a mandate. They need someone local who can translate.

## 3. The full-stack employee is emerging, and the job is becoming “manager of agents”

This one matches what I’m seeing inside [HatchWorks AI](https://hatchworks.com/) almost exactly. Domain boundaries are bleeding (our copywriters design, our designers write, our strategy teams run AI-led stakeholder interviews at a scale we never could before). Manu is engineering that on purpose:

“Having people operate more in this full stack manner, meaning end-to-end ownership across a certain process. Where maybe you used to have four or five people that all did a sliver of it, really expanding that scope of role and capability. It shortens the cycle, it increases that end-to-end accountability, removing some of the internal handoffs that often slow things down.” — Manu Narayan (~7:30)


His example: internal Salesforce development used to touch six or seven roles (BSA, product owner, admin, developer, QA). AI lets individuals stretch across more of that lifecycle.

And the stretching doesn’t stop at adjacent roles. It goes up a level of abstraction:

“You’re really looking at how a team of agents is working and operating, and you’re helping orchestrate them. It’s a bit of the role of almost like a manager of agents as opposed to the doer of a task.” — Manu Narayan (~30:45)


Human-in-the-loop isn’t disappearing; it’s moving. A year ago the human reviewed every AI-generated line. Now [agents work in loops](https://open.substack.com/pub/mattpaige68/p/stop-prompting-ai-start-writing-loops?r=57u8oy&utm_campaign=post-expanded-share&utm_medium=post%20viewer), other agents oversee them, and the human decides *where* judgment enters: maybe you’re fine with an AI summary of code reviews, but a person always signs off on security scans. 

Deciding those checkpoints is becoming a core organizational skill.

## 4. Skills are how AI actually scales in the enterprise

I went deep on this one with him, because [skills are my whole operating system](https://open.substack.com/pub/mattpaige68/p/how-to-turn-claude-skills-into-your?r=57u8oy&utm_campaign=post-expanded-share&utm_medium=post%20viewer). His definitional line is the cleanest I’ve heard from an enterprise leader:

“A skill often is enhancing what a human does. An agent is something that, while you may have a human in the loop as part of the process, ultimately is running a bit autonomously.” — Manu Narayan (~10:30)


Human-invoked versus autonomous. Simple, and it immediately clarifies what belongs where.

But the bigger insight is what skills solve at company scale. The AI haves have already built their reusable prompts and workflows. Skills codify that advantage and make it transferable:

“The skill helps codify that, which is really important. But moreover, it actually lets us scale that out really easily to other people in similar roles. It’s a way that you can enable without needing to fully teach around all the fundamentals.” — Manu Narayan (~11:15)


And here’s the idea to steal.

GitLab runs an internal skill library: anyone in the company can submit a skill to a GitLab repo, a review process promotes the good ones into the official library, and skills get distributed to people by persona. Team members iterate on and build off each other’s skills along the way, promoting the strongest ones so the best rise to the top.

Bottom-up creativity, top-down quality control, and the library compounds instead of collecting dust.

Their account-research skill (which pulls internal systems, external sources, and support tickets into a consistent pre-call brief for every field-facing role) is exactly the pattern I’ve written about with [chaining and nesting](https://open.substack.com/pub/mattpaige68/p/how-to-chain-and-nest-claude-skills?r=57u8oy&utm_campaign=post-expanded-share&utm_medium=post%20viewer): small, composable, shared skills.

Manu runs a personal one too: a daily to-do skill that reads his conversations, email, and prior list, and briefs him every morning. (I told him about mine. It once told me, after a late event night, “Drinks win. Get somebody to cover the training.” That’s AGI, honestly.)

## 5. Token maxing measures the wrong thing

Token maxing (gamifying AI adoption by celebrating whoever burns the most tokens) is having a moment. Manu isn’t buying:

“It’s really easy to gamify, and there’s a direct cost associated at the end, which makes it really difficult as you start to think about that being the means of driving your productivity.” — Manu Narayan (~16:10)


Six months ago GitLab tracked raw usage stats too (weekly actives across their five or six enterprise AI platforms). They still watch tokens, but for cost control. The measures that matter now are business KPIs, by role and persona:

“We’re not thinking just about things like lines of code. We’re thinking about innovation velocity. We’re thinking about release cadences. We’re really thinking about how does delivery to the end customer change.” — Manu Narayan (~16:45)


In support: time to first response, time to resolution, the number of turns a ticket takes. Boring, established metrics. Manu’s own words: “It sounds a little quaint, but it’s actually that simple.” Usage tells you people showed up. Business KPIs tell you the work changed.

(He also expects model-specific spend caps to become standard internally. “Almost unavoidable.” The CFO era of AI is coming.)

PS. If you are looking to reduce token spend with out reducing token usage, you need to check out [how Coinbase’s CEO cut token spend in half as token usage grew](https://open.substack.com/pub/mattpaige68/p/coinbase-cut-its-ai-bill-nearly-in?r=57u8oy&utm_campaign=post-expanded-share&utm_medium=post%20viewer).

## 6. Freedom in the sandbox. Governance on the repo side.

The tension every IT leader is living: lock things down and people route around you; open things up and you’re a public company with regulated customers shipping ungoverned code. Manu’s resolution is an architectural one:

“There’s a lot that happens client side today, whether you’re using Codex or Claude or even open source models. But when you think about what’s happening repo side, that’s ultimately where you can put in assurance and governance and guardrails and the things that make you really comfortable about what’s being developed.” — Manu Narayan (~24:30)


Develop however you want, locally, in whatever tool. The governance lives where the code lands: AI-generated code reviews, auto-remediation of security vulnerabilities, auto-remediation of pipeline failures. That matters because the bottleneck has moved.

[Per the report](https://about.gitlab.com/resources/ai-accountability-survey-2026/), **85% of DevSecOps professionals say AI shifted the bottleneck from writing code to reviewing and validating it.** The after-code part of the lifecycle is now the whole game, and it’s exactly the part you can’t govern from a laptop.

Same philosophy on shadow AI. Anyone can build an agent in their own sandbox; the moment it touches enterprise context, it gets reviewed and optimized before publishing. And the real defense against shadow AI isn’t policing:

“The official means of getting something approved, of being able to do a POC, of being able to deploy a vibe-coded app, those can’t be more painful than going on your own.” — Manu Narayan (~41:00)


That’s the whole shadow IT playbook in one sentence. Make the happy path the easy path.

## 7. Speed is commoditizing. Context is the moat.

The report’s headline argument is that context and traceability are the new differentiators, and Manu’s explanation of *why* is the sharpest thing in the episode:

“The capabilities of the different frontier LLMs have increased and improved so dramatically. The ability to access context itself has not.” — Manu Narayan (~32:15)


Models got better faster than your ability to feed them. So the constraint moved again (bottlenecks always move), from model quality to context quality.

His support-engineering example makes it concrete: everyone says customer support is a solved AI problem. But a senior support engineer carries years of undocumented experience with deployment types, OS versions, and past failures. Where rich context exists, AI takes the work. Where the context lives only in a person, the person wins. The frontier of what AI can do in your company is drawn by what you’ve made legible to it.

That’s also the pitch behind GitLab Orbit, their knowledge graph: stitch the code base together with pipeline failures, security scans, and review comments, and agents consume fewer tokens while producing more accurate output, faster. It’s the enterprise version of what I’ve been building personally with [my AI second brain](https://open.substack.com/pub/mattpaige68/p/andrej-karpathy-just-showed-us-how?r=57u8oy&utm_campaign=post-expanded-share&utm_medium=post%20viewer): compound your context in one connected place and every AI task downstream gets better.

## 8. The SaaS-pocalypse is overstated. The last 20% is why.

I gave him my [Bring-Your-Own-Agent](https://open.substack.com/pub/mattpaige68/p/welcome-to-the-bring-your-own-agent?r=57u8oy&utm_campaign=post-expanded-share&utm_medium=post%20viewer) take (nobody wants 30 agents in 30 tools) and asked whether SaaS survives the era. His answer, from a man whose company both sells SaaS and vibe-codes internally:

“It’s really easy to get to that proof of concept that’s 80, 90% of the way there. It has bells and whistles and features that people love. But that remaining 20%, as you start to layer in role-based access control, versioning, immutable versus non-immutable records, the things that are actually really deep problems, those end up being this really long tail.” — Manu Narayan (~38:10)


Systems of record, governance, compliance, SOX controls: none of that gets vibe-coded away. What changes is the interface. Manu sees agent sprawl as a real problem (every agent wants context from every system, which turns into a data sovereignty headache fast), so GitLab concentrates on a handful of agent platforms and pipes context in through MCP connectors.

And a prediction worth logging: he doesn’t think MCP is the endgame. “I’m not sure MCP is the be-all, end-all protocol. I think we’ll see agent-to-agent communication protocols emerging” (~39:30). Your agent talking to the SaaS vendor’s agent. Exactly where I think this goes.

## The lightning round

Four quick ones worth keeping:

- **Most important superpower right now** : “Intellectual curiosity. Your ability to access information, to become a pseudo expert on things, is unparalleled to any time in history. If you have curiosity and a little bit of intellectual horsepower, you can pretty much do anything now.” (~42:30)
- **Most overhyped thing vendors sell** : “A lot of AI vendors are simply selling essentially wrappers on a model... there’s nominal value in that. We really need true agentic capabilities that get work done.” (~43:40)
- **Best AI dollar spent this year** : Glean, as internal enterprise search plus an agent and knowledge platform. Manu called it “the enterprise knowledge LLM” (~44:15). (Full disclosure: HatchWorks AI partners with Glean, so I smiled at that one.)
- **Advice to his pre-AI self** : “The AI era is like living in dog years.” GitLab has iterated its AI program three times in his ten months. “What doesn’t work is the traditional way of RFPs and POCs. You’re gonna make a call, and maybe next year it’s not gonna be the right call anymore. Speed is probably the more important metric.” (~44:50)

## The through-line

If you’re a solo builder rather than a 2,000-person enterprise, the playbook scales down cleanly: capture the incremental gains but hunt the nonlinear ones, keep your experiments in a sandbox with one honest gate before they touch anything real, and invest in your context layer before your tool layer.

But the through-line of the whole conversation is the ceiling. Every company is getting the efficiency gains right now. They’re real, they’re everywhere, and they’re about to be table stakes. The separation happens when someone stops asking “how do we do this faster” and starts asking “why does this workflow exist at all.”

A faster version of a pre-AI workflow is still a pre-AI workflow.

🎧 The full conversation goes deeper on all of this: [listen to the episode here](https://hatchworks.com/talking-ai/productivity-ceiling/). Manu is active on [LinkedIn](https://www.linkedin.com/in/manunarayan/) and worth a follow, and the GitLab blog’s agentic orchestration coverage is genuinely good.

*If this was useful, share it with the person at your company quietly fighting the productivity ceiling. And subscribe if you haven’t: I break down conversations like this, plus tactical AI guides, every week.*

Point 6 is the one worth underlining for anyone rolling this out. Moving governance to where the code lands instead of the laptop is what makes "develop in whatever tool" actually safe. The 85% stat is the quiet tell: if reviewing and validating is the whole game now, that's exactly where the controls belong, not client-side where you just push people to route around you. Manu's "make the happy path the easy path" line is the same insight from the culture angle. Curious how the hub-spoke-hub model holds up when a department's embedded owner disagrees with a central governance call.
