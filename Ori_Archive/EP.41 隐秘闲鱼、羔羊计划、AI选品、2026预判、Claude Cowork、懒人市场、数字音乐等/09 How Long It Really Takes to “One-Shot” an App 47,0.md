# How Long It Really Takes to “One-Shot” an App: 47,000 Lines of Code Later

> 原链: https://www.saastr.com/how-long-it-really-takes-to-one-shot-an-app-47000-lines-of-code-later/  
> 来源: SaaStr · 归档自 EP.41 · 抓取于 2026-08-05  

---

The vibe coding hype cycle has a narrative problem.

Every week, someone posts “I built a SaaS in 4 hours!” And technically, they’re not lying. You can absolutely scaffold something that looks like a product in an afternoon.

But there’s a canyon-sized gap between a demo and something people will actually use. I just learned exactly how wide that canyon is. I’ve vibe coded a dozen apps now used 800,000+ times.

My latest?  A complex game.  A start-up simulator, **[Founderscape.ai](http://www.founderscape.ai)**.  OK it’s not a B2B app.  But how long it took to truly get it into production is instructive.

![](https://i0.wp.com/www.saastr.com/wp-content/uploads/2026/01/founderscape2-scaled.jpeg?resize=1000%2C734&quality=70&ssl=1)


## The Project: Founderscape.ai

I set out to build something I’d never attempted before: a full startup simulator game. Not a landing page. Not a prototype. A real game where you:

- Go from founding to YC to Series A to IPO
- Raise from Sequoia, Benchmark, Founders Fund — with realistic dilution math
- Build a team and poach from your AI rivals
- Manage burn rate, runway, NRR, and churn
- Race to a trillion-dollar valuation before you run out of cash

Think of it as “what if someone turned 15 years of SaaStr content into a game you could actually play.”

The result? **Founderscape.ai** — a cyberpunk-styled founder simulation with real VCs, real accelerators, real mentors, and an AI competitor that scales with you.

## The Numbers Nobody Talks About

Here’s the development data:

![](https://i0.wp.com/www.saastr.com/wp-content/uploads/2026/01/Screenshot-2026-01-05-at-9.17.11-AM-scaled.png?resize=1000%2C447&quality=70&ssl=1)


That’s not “one-shot.” That’s a month of focused building.


## The Myth of “I Built It in a Weekend”

Here’s what actually happens when you try to ship something real:

**Days 1-3: The honeymoon.** Everything works. You’re a genius. The AI understands you perfectly. You post screenshots and people are impressed.

**Days 4-7: The reckoning.** Edge cases appear. The AI starts “helping” by changing things you didn’t ask it to change. You realize your data model is wrong. You rebuild core systems.

**Days 8-12: The grind.** You’re not building new features anymore. You’re fixing what broke when you built the last feature. You’re in the debugging phase that consumes 60% of actual development time.

**Days 13-16: The polish.** The game works. Now you need it to feel good. UI tweaks. Balance adjustments. Performance optimization. This phase never ends — you just decide to ship.

3,158 commits over 16 days means I was pushing changes roughly 200 times per day. That’s not “prompt and forget.” That’s constant iteration, testing, breaking, and fixing.

## What Actually Took the Time

Building Founderscape required systems that don’t exist in any tutorial:

![](https://i0.wp.com/www.saastr.com/wp-content/uploads/2026/01/founderscape1-scaled.jpeg?resize=1000%2C738&quality=70&ssl=1)


**Financial modeling that’s actually accurate.** NRR calculations, dilution math, burn rate, runway — these need to work exactly like they do in real startups. Get the math wrong and the whole game feels fake.

**A living competitive ecosystem.** AI rivals that grow alongside you, make strategic decisions, and can actually beat you. This isn’t a static opponent — it’s a system that adapts.

**Three distinct visual environments.** A headquarters view, an office management view, and a city map with your competitors. Each needs its own UI, its own interactions, its own state management.

**Real-world data.** Actual VCs with accurate check sizes. Real accelerators with realistic equity takes. Mentor buffs based on what those people actually bring to a cap table.

**Post-IPO gameplay.** Most games end at the exit. Founderscape continues — stock price management, secondary offerings, the path to trillion-dollar status.

None of this is impossible with vibe coding. All of it takes time.

## One Shotting Works. In A Sense. Sort Of. It Gets You Maybe 40% Of The Way, If You Do It Right.

If you’re evaluating whether to vibe code something substantial, here’s the real calculus:

**Simple landing page:** 2-4 hours. The hype is real here.

**Information-based web app:** 10-20 hours. Still fast, still worth it.

**Complex interactive product:** 40-100+ hours. This is where the gap lives.

**Production-ready at scale:** Add 30-60 minutes per day, forever. Maintenance isn’t optional.

My game took 40-55 hours over 16 days. That’s 2.5-3.5 hours per day of focused work. Not a weekend project. Not a lunch break experiment. A real time commitment.

## Would I Do It Again?

Absolutely.

Here’s the thing: 40-55 hours to build a game with 47,000 lines of code is still insanely fast. A traditional game studio would scope this as a 6-month project with a team.

I did it solo, over winter break, while doing everything else I normally do.

The leverage is real. The speed is real. But “one-shot” is a lie we tell ourselves to feel like wizards.

## What I Actually Learned

**Domain expertise matters more than technical skill.** I knew exactly what I wanted because I’ve lived this stuff for 15 years. The AI handled the how. I provided the what.

**Vibe coding is not “no work.” It’s “different work.”** You’re not writing code, but you’re debugging constantly, testing every change, and making thousands of micro-decisions.

**The main game file was 6,122 lines.** A single file. That’s what “rapid iteration” looks like in practice — giant files that accumulate complexity because refactoring takes time you don’t have.

**3,158 commits is not an exaggeration.** Every prompt, every test, every fix. This is what real vibe coding looks like when you’re building something that needs to work.

## And Here’s the Kicker: We’re Not Done

Those 16 days and 47,000 lines of code? That’s just what it took to get into production.

To make it *great*? So, so much more.

The game is live. People are playing it. I’m already getting feedback, bug reports, feature requests. The MMORPG version is on the roadmap. Balance needs tuning. New content needs building. The mobile experience needs rethinking entirely.

Production is not the finish line. Production is the starting line.

This is the part nobody talks about when they post “shipped in a weekend!” The weekend gets you to launch. The next six months get you to good. The next year gets you to great.

Every single day, I’ll be in there. Tweaking. Fixing. Improving. Adding. That’s not a burden — that’s what building something real looks like.

The 40-55 hours got Founderscape into players’ hands. The next 400 hours will make it something they can’t stop playing.

## One Shot-ting Prototypes Works. But That’s Just The Start.

“How long does it take to one-shot an app?”

- If you mean a prototype: hours.
- If you mean something people will actually use: weeks.
- If you mean something you’re proud of: longer than you think, but still faster than you’d believe.
- If you mean something truly great: you’re never done.

Founderscape.ai took 16 days, 3,158 commits, and 47,000 lines of code to ship. It’s live. People are playing it. An MMORPG version is coming.

That’s not “one-shot.” That’s vibe coding at scale. And we’re just getting started.

*Try Founderscape.ai for free: [Founderscape.ai](https://founderscape.ai/)*

*Go from startup to YC to IPO. Raise from the best VCs. Build your team. Beat your rivals. See if you can hit a trillion-dollar valuation before you run out of runway.*

![](https://i0.wp.com/www.saastr.com/wp-content/uploads/2026/01/Screenshot-2026-01-05-at-9.19.14-AM-scaled.png?resize=1000%2C643&quality=70&ssl=1)
