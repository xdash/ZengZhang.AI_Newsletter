# Sometimes the Best AI Solution Is the One You Don't Build Yourself

> 原链: https://every.to/working-overtime/how-i-successfully-failed-at-my-first-ai-operations-project  
> 来源: every.to · 归档自 EP.21 · 抓取于 2026-08-06  

---

![Sometimes the Best AI Solution Is the One You Don't Build Yourself](/_next/image?url=https%3A%2F%2Fd24ovhgu8s7341.cloudfront.net%2Fuploads%2Fpost%2Fcover%2F3734%2Fhandevery.png&w=3840&q=75)

[Working Overtime](/working-overtime)

![](https://d24ovhgu8s7341.cloudfront.net/uploads/publication/logo/100/Screenshot_2024-11-22_at_9.33.36_AM.png)

# Sometimes the Best AI Solution Is the One You Don't Build Yourself

How I successfully failed at my first AI operations project

[Katie Parrott](/@katie.parrott12)

![](https://d24ovhgu8s7341.cloudfront.net/uploads/user/avatar/47943/v6nzzAut_400x400.jpg)

Aug 21, 2025 · 10 min readUpdated Jul 25, 2026

*Was this newsletter forwarded to you? __[Sign up](https://every.to/account)__ to get it in your inbox.*

Minutes into our weekly AI editorial operations call, I shared my screen and held my breath.

The AI editing application I’d been building for weeks—the one I’d promised was ready, not once, but twice—errored out.

I clicked “Analyze” again. More errors. One more time. Errors again.

This was the last chance for my first official project as Every’s AI editorial ops lead. I’d been at this for weeks—tinkering with prompts, debugging code, and migrating from platform to platform like a Dickensian orphan looking for a meal—only to watch our team struggle more with the system I’d built than they would have with editing the piece themselves. Either the AI editor worked today and we rolled it out, or we would cut our losses and move the whole thing into Claude Teams—shared Claude workspaces where everyone inside the organization can access the same projects.

I kept the Zoom patter going while I willed the system to load the beautifully formatted high-resolution editorial feedback that had been there when I’d tested it half an hour earlier. The output—what should have been a detailed analysis of an essay draft measured against Every’s editorial principles and best practices—stubbornly refused to appear. When I stopped talking, the silence told me what I already knew.

![Just an hour after it was working fine, my Every AI Editor app refuses to cooperate. (All images courtesy of the author.)](/_next/image?url=https%3A%2F%2Fd24ovhgu8s7341.cloudfront.net%2Fuploads%2Feditor%2Fposts%2F3734%2Foptimized_d4d71023-6bc3-4d27-8bfd-d0cf62283b96.png&w=1200&q=75)

By the time the call ended, I was finally ready to admit what everyone else could see: I was solving the wrong problem. We needed a solution that worked reliably, every time, without me playing whack-a-mole with bugs that multiply faster than I can squash them. My failed demo taught me to let go of the builder's impulse long enough to see the solution waiting in someone else's infrastructure. Six weeks of debugging taught me what we needed. More importantly, it taught me what we didn't.

![](/_next/image?url=https%3A%2F%2Fd24ovhgu8s7341.cloudfront.net%2Fuploads%2Feditor%2Fadvertisements%2F807%2Foptimized_coraad.png&w=1200&q=75)

**Make email your superpower**

Not all emails are created equal—so why does our inbox treat them all the same? [Cora](https://cora.computer/?utm_source=standalonead) is the most human way to email, turning your inbox into a story so you can focus on what matters and getting stuff done instead of on managing your inbox. Cora drafts responses to emails you need to respond to and briefs the rest. 

## **Why Every needs an AI editor**

When I started in the __[AI operations role](https://every.to/working-overtime/ai-doesn-t-care-about-your-resume)__ at Every this past June, I knew right away what I wanted to build first: an AI‑powered editor. One of our guiding principles for automation at Every is ["](https://every.to/chain-of-thought/the-mantra-of-this-ai-age-don-t-repeat-yourself)[Don't repeat yourself](https://every.to/chain-of-thought/the-mantra-of-this-ai-age-don-t-repeat-yourself)[."](https://every.to/chain-of-thought/the-mantra-of-this-ai-age-don-t-repeat-yourself) If you notice yourself making the same edits over and over, that's your cue to call in AI for help.

And there are plenty of edits we make again and again. Where's the lead? Is it at the top where it belongs, or buried in paragraph five? Do the headline, subheading, and introduction work together to draw readers in? Are the stakes clear? Is the writer's credibility established? These aren't small notes—they're the core of how Every thinks about good writing. Because they repeat across every draft, they're exactly the kind of work an AI assistant can excel at: Surface patterns, enforce standards, and leave the final creative judgment to humans.

The goal is to cut down on the revision cycles our writers and editors go through to get a piece publication-ready. Every publishes daily with a small team. Many of the team members who write have jobs that are *not* writing, and many of them aren’t professional writers, so editing cycles are easily our biggest bottleneck. Writers average 3-4 revision rounds per piece, with each round taking 2-3 days—meaning a single essay often takes two weeks from draft to publication.

I'd built a system for my own pieces that worked beautifully. Each week, the Every editorial team talks through how the week’s pieces could have been stronger—buried leads, abstract language, missing stakes. I combined those patterns with Every's style guide, examples of our best-performing pieces, and a taxonomy of common issues we see in drafts. All of that went into a Claude project—a dedicated workspace where you can store documents, instructions, and context that carry over across every chat you initiate inside of it**.** 

With all of that context, plus every piece I’ve written for __[my own column](https://every.to/working-overtime)__, uploaded to the project’s “knowledge,” the project behaved like an editorial assistant built just for me. 

Whenever I wrote a piece, I'd run it through this editor first. It caught the stuff I was blind to—my tendency to hedge statements with “maybe” or “just,” my weakness for correlative conjunctions (those “not X, but Y” constructions that AI loves so much), the way I'd forget to insert a “so what” early in the piece. I thought I could package up this system and hand it to other writers like a gift.

I was, to be kind to my former self, naive.

There's an entire constellation of considerations in making AI useful in an organization that have very little to do with vibe coding jam sessions. There’s education—how do you inform the team about an available solution, and how to use it? There's reliability—it has to work every time, not just when you're there to debug it. And there's change management—convincing writers to paste their precious drafts into yet another tool when they're already juggling five different platforms.

It doesn’t matter if *I* find my creations useful. What matters is whether other people can use it, want to use it, and get value from it when they do. That's a completely different bar—one that, as we’re about to see, was alternately tricky and incredibly simple to clear. 

## **There and back again: A builder’s tale** 

What came next felt like being trapped in an escape room made up of errors, maintenance nightmares, and confused co-workers. Here it is, a tragedy in five parts:

**Become a [paid subscriber to Every](https://every.to/subscribe) to unlock this piece and learn about:**

1. Why custom-built solutions failed
2. Why the asset is standards, not code
3. Four failed approaches before finding the right solution
4. Know when to build versus when to leverage existing tools

## Create a free account, or log in.

Every members live and work at the edge of AI. Join now.

By continuing, you agree to the [Terms of Sale](/terms), [Terms of Service](/terms), and [Privacy Policy](/privacy).

Enjoy unlimited access to all of Every.

[See subscription options](/pricing-all-plans)
