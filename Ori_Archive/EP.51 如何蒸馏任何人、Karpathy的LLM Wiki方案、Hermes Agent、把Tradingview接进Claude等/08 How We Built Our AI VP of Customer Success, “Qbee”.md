# How We Built Our AI VP of Customer Success, “Qbee” — And How You Can Build Yours

> 原链: https://www.saastr.com/how-we-built-our-ai-vp-of-customer-success-qbee-and-how-you-can-build-yours/  
> 来源: Jason Lemkin · 归档自 EP.51 · 抓取于 2026-08-05  

---

We’ve now built 20+ AI agents and 12+ vibe coded apps used 800,000+ times at SaaStr. We’ve shared how we rolled out our AI SDRs, and how we built / vibe’d our AI VP of Marketing as well as a bunch of AI-powered VC tools that have done almost a million startup valuations.

But Qbee is the best thing we’ve built so far.

Qbee is our AI VP of Customer Success. He manages all 100+ sponsors **[for SaaStr AI Annual (May 12-14, come!](http://www.saastrannual.com)**), sends every one of them hyper-personalized weekly emails, tracks 13 core tasks with subtasks per customer, follows up without drama, identifies gaps in real time, and pushes a Slack + email update to our team every single day.

And he was built with zero engineers, on Replit, for less than a thousand dollars. Our AI token costs across *all* of our vibe coded apps haven’t hit $200/month yet.

Here’s what matters: **he reduced our human hours on customer management by more than 70%.**  Customer logins and on-time task submissions went up more than 10x compared to our old tool. And customers didn’t even realize most of the communication was coming from an AI until we told them on a webinar.

I want to walk through exactly how Amelia (our Chief AI Officer) and I built this, how it evolved, and how you can build your own version. Because if we built it, you can build your own, too.

## It Didn’t Start This Way

Qbee did not start as an AI VP of Customer Success. That was never the plan.

For the past two years, we’d been paying for an off-the-shelf portal tool for our sponsors. Zero AI functionality. Zero. It was a static customer portal where people could log in and submit things to us. No single sign-on. No way to track unique deliverables across customers. No analytics. We couldn’t even tell if someone had logged in unless they submitted something.

Amelia’s original goal in January was simple: vibe code a better project management tool on Replit. Replace the thing that wasn’t working. The initial spec was basic — assign people tasks, add single sign-on, build in some light automations so sponsors would know what to do next and get reminders.

That’s all Qbee did for the first couple of weeks. And it was already better than what we had.

Then we deployed to production with real customers and real data started flowing in. We could see who was logging in, who wasn’t, what they were doing at certain times of day, what they weren’t doing. We had granularity we’d never had before. And that’s when we realized Qbee could do a lot more than manage tasks.

## The “Oh Wait” Moment

A few weeks after launch, Amelia was sitting down on a Sunday night to write the weekly sponsor email. Same thing she’d done for years — a newsletter-style blast to all sponsors with a generic list of what they needed to do. Same links for everyone. Same deadlines. No personalization.

She looked at Qbee and the data he had on every single sponsor — their tier, their specific contract deliverables, which tasks they’d completed, which they hadn’t, whether they had speaking sessions or custom activations or lanyard sponsorships — and realized: why am I writing this generic email when Qbee already knows everything about every single customer?

So she built the email capability. Qbee sent 100 personalized sponsor emails in 10 minutes. Each one with that sponsor’s specific task status, their unique registration codes, their unique discount codes, what they’d completed, what was still due, and details specific to their sponsorship tier. All at 11:11 AM, 11:12 AM, boom, done.

Previously, getting a human to do this took a week. And I mean a full week of someone’s time. We had tried for years to get our agencies and production teams to send individualized emails. Here’s the math: 100 sponsors, each with at least four registration codes. That’s 400 links someone has to go find. Then check if each person has logged into the portal. Then figure out their specific deliverables. Then write the email.

Nobody wanted to do it. We literally could not find people willing to do this work. When it did happen, maybe once, it took a full week and was still incomplete.

Qbee does it every week, perfectly, in minutes.

## What Qbee Actually Does Now

For our customers (sponsors), Qbee:

- Assigns deliverables and deadlines unique to their contract and tier
- Organizes all their inputs and uploads in one place
- Tracks timelines and automates next steps
- Sends personalized reminders and follow-ups using their actual data (login status, tasks completed, contract specs, etc.)
- Provides their unique registration codes, discount codes, and ticket links
- Handles speaker session submissions with real-time slot management (when four sponsors picked the same time slot, Qbee grayed it out for the fifth)
- Manages booth graphics submissions and deadline enforcement

For our team, Qbee:

- Gives us a real-time dashboard showing every sponsor’s task completion status
- Sends daily Slack and email updates on who’s behind, who’s at risk, who hasn’t logged in
- Completely automates the personalization that used to require manual hours
- Flags submissions so we can review them (Amelia now uses Claude Cowork with Illustrator to check booth graphics instead of doing it manually)
- Even started handling collections on overdue payments this week

The TikTok example tells the story well. When TikTok sponsored SaaStr London previously, they were painfully slow to submit anything. Big company, lots of approvals, nothing came in on time. Amelia remembers going to London and not having their logos or booth graphics.

This year, TikTok completed 11 of 13 tasks in a single day. Qbee made it so easy that a sponsor who’d been a pain to work with turned into one of the fastest to complete everything. The friction was gone.

![](https://i0.wp.com/www.saastr.com/wp-content/uploads/2026/04/AI-WW-How-we-Built-Our-AI-VP-of-Customer-Success-_Qbee_-1.jpg?resize=960%2C540&quality=70&ssl=1)


## The Real Unlock: Personalization + Coverage

The core CSM problem has always been the tension between personalization and coverage. You want every customer to feel like they’re your only customer. But you have 200 customers and a team of 4 CSMs. Something has to give, and it’s always personalization.

AI agents break that tension.

We went from reactive customer success — same email blasts to everyone, routing issues to someone else, hoping people would do their tasks — to proactive, agentic customer success. Real time. 24/7. Not once a quarter.

And this is where the QBR comparison matters. “QB” is partially a play on QBR, but QBRs have always been frustrating. Why am I waiting once a quarter for super generic stats? Everything in a QBR has already happened. It’s retrospective by definition.

Qbee operates in real time. He knows what’s happening now. He’s not waiting for some magical quarterly window to pass before surfacing insights. He has all the data, all the time, and acts on it as often as customers can absorb it.

If you measured output on the specific dimension of proactive, accurate, personalized operational outreach at scale, the agent wins. Almost always.

## How We Built It (And How You Can Too)

### Step 1: Write a Spec First

Before opening Replit, write a spec. Amelia’s original spec was pretty basic — user flows, a dashboard, checklists, an asset library, upload functionality, single sign-on. She wrote it up front and it covered maybe 60% of what Qbee does today.

If writing a spec from scratch seems intimidating, start in Claude. Just say “I need help writing a spec for a customer success portal” and iterate with it. You don’t need to be a prompt engineer in 2026. Those days are behind us. Just talk to Claude, describe what you want, iterate until you understand everything in the spec, then give it to your vibe coding platform.

The more granular your spec, the less you’ll iterate later (and the lower your costs). But don’t let perfectionism stop you. Amelia’s first spec wasn’t that detailed, and Qbee still turned out great. The bigger goal is getting to production, not having a perfect spec.

We’ve shared both the original spec and the current V2 spec (which is significantly more detailed after three months of iteration). You can use them as templates. You can literally give saastrsponsors.com to your vibe coding agent and say “I want something like this for my business.”

### Step 2: Load Your Spec Into Your Vibe Coding Platform

Take your spec to Replit, Lovable, v0, or whatever you prefer. Give the agent your spec plus some design references — websites you like the look of, customer portals you’ve seen that work well. Then:

- Tweak the designs
- Test every single function — every button, every upload, every form field
- Hook up email capabilities (we use Resend)
- Create your database
- Port over any content and knowledge your agent needs (FAQs, guidelines, etc.)
- Test everything again

Amelia tested literally every input and output in Qbee before sending it to a single customer. Her biggest fear was something breaking in production. The testing phase took the longest of any step, and it should. Your agent has to actually work.

### Step 3: Set Up Authentication

We used Clerk for single sign-on. We needed different members of the same customer organization to access shared data securely. One organization = one sponsor company. Users within that org get Owner/Admin/Member roles.

This was the hardest part for someone new to vibe coding. SSO is legitimately tricky. But it’s gotten easier — Lovable and v0 have built-in auth now. And if you don’t need multi-user org access, it’s much simpler.

One thing we learned the hard way: build in session timeouts. Our first version didn’t have one. A sponsor logged in and stayed logged in for five days straight. When they finally tried to upload something, it broke because the session had expired on the back end without reauthenticating them. We added a 15-minute timeout and the problem went away.

### Step 4: Deploy to a Few First, Then Expand

We didn’t roll Qbee out to all 100 sponsors at once. Amelia picked one customer at each sponsorship tier (Diamond, Platinum, Gold, Silver) and deployed to them first. Things broke. The Salesforce integration kept disconnecting. Some edge cases around pending users in Clerk caused emails to not go out to everyone on a team.

But we learned what broke, fixed it, and expanded. Every week, customers told us what they wanted added. They asked for email marketing copy. They wanted a networking information section. They wanted to submit activations through the portal instead of emailing us. They wanted a full speaker submission flow.

We added all of it. Qbee today is not how he was in January. He won’t be the same next week either, because customers keep requesting features. And here’s the part that matters: when a customer asks for something, instead of saying “that’s not on our roadmap,” we go into Replit and build it. Sometimes the same day. We’re not engineers. That’s a superpower you don’t get with off-the-shelf software.

### Step 5: Leverage Your Data to Go Agentic

This is how Qbee graduated from a project management tool to an AI VP of Customer Success. Once you have real customer data flowing through your app — logins, task completions, usage patterns — you can start automating actions based on that data.

Are you sending customers unique links during onboarding? Let the agent do it. Want to send reminders based on what they have or haven’t done? Let the agent do it. CSMs not checking in regularly? Let the agent do it. The agent will do it every time, without drama, at whatever frequency you set.

We evolved Qbee’s agentic capabilities one layer at a time:

1. First, personalized weekly emails to each sponsor
2. Then, triggered actions when customers did or didn’t complete tasks
3. Then, internal team reporting with real-time visibility and gap analysis
4. Then, proactive outreach for deadline enforcement, collections, and more

### Step 6: Agent Hop for Security

Never store sensitive customer data directly in your vibe coded agent. We call this “agent hopping” — segmenting data across different systems so nothing lives in one place.

Qbee’s customer database lives in Salesforce. Contracts, contacts, deal details — all in Salesforce. Qbee has to call the Salesforce API to get that data. He doesn’t have 100 contracts sitting in his knowledge base. User data lives in Clerk. Registration links come from Misbo. The agent hops between systems to assemble the full picture.

Amelia built a custom Salesforce Connected App to make this work. Had she done that before? No. She asked Claude and the Replit agent how to do it, got it working in about 20 minutes, and now the integration doesn’t break.

The more sensitive data you store directly in your agent, the more you need to become a security expert — constant audits, penetration testing, trying to break things. Most people don’t want that burden. To the extent you can keep sensitive data in established, secure systems and have your agent call out to them, do it.

### Step 7: Build the Agentic Piece One Layer at a Time

Don’t try to make your agent fully autonomous from day one. That wasn’t even our goal — we just wanted a better portal. The agentic capabilities emerged over time as we saw what was possible with the data we were collecting.

Start simple. Get the core functionality working. Deploy to real users. See what data you’re generating. Then ask: what can I automate with this? Layer by layer.

## The Maintenance Reality

Every time we share one of these, we say the same thing: there is no set-and-forget. These agents require daily attention.

You have to check in on them every single day. You have to review their outputs. As you add features, things that used to work might break (regressions are real — adding a new page might break the upload button for no obvious reason). Our Slack integration today sent triple updates instead of one. We know why it happens. We fix it. It’s life.

Our hack: have the agent send you an email status update every single day. You’ll see stuff break in the email before customers tell you. Build that in from day one.

Between Amelia and me, we’re checking on Qbee every day. Just like you’d manage a human VP of CS — you’d check in daily, review their work, course correct. Same deal.

## But Humans Still Matter at $100K Deals

One thing I want to be clear about: we didn’t dump our customers solely onto an AI. At a $100K average deal size, this is still a bespoke process. Amelia, David, and I are all still involved. We’re copied on every Qbee email. When customers reply, sometimes we reply back. I was on 10 sponsor calls last week and will be on another 10 this week. Amelia still does weekly sponsor webinars.

Our top-tier diamond sponsors have weekly calls with us. Some of them work in our Slack. The Google team prefers Google Meet and Google Chat. Salesforce likes Slack (of course). We go where the customer wants.

Qbee handles the 95% of stuff that can be automated — the personalized task emails, the deadline reminders, the status tracking, the gap analysis. That frees us up to actually respond faster to the strategic questions, the creative booth discussions, the nuanced problems that need a human.

Customers like this mix. They want to reach a human when they need one. They also appreciate that for 90% of operational stuff, there’s an agent that’s faster, more accurate, and available 24/7. Very rarely has anyone been frustrated. They get it.

And the fact that Qbee freed up our time means we can be more flexible about *how* we work with customers. Before, we were stretched too thin and had to force everyone through the same process. Now we can meet each customer where they are.

## The Real Challenge For You

I’ve done a lot of investments. I work with a lot of high-growth B2B + AI companies. Very few people do customer success well. When I meet a VP of CS who tells me everything is perfect, they’re always gone in six months. 100% of the time, customer success is not as good as you think it is.

There is something broken in your onboarding, retention, follow-up, or customer education process right now. Find it. Go through your flow. See where only 50% of your customers are covered. Or 30%. Or 20%.

Then think about what you would build to get that to 100% coverage. Even one CSM managing 50 accounts isn’t viable alone. But one CSM plus an agent? That’s viable. You don’t drop the human. You augment them with an agent that handles the operational coverage gap.

If your current off-the-shelf CS software is working great and you’re at 100% coverage with full personalization — don’t build this. The 90/10 rule applies. Buy 90%, vibe 10% at most.

But if you have gaps — and you almost certainly do — this is low-hanging fruit for vibe coding. The off-the-shelf software in this category is mediocre, hard to configure, and dated. You can build something better, customized to your exact business, and ship features the same day customers ask for them.

We’ve shared the specs, the slides, and the live app at saastrsponsors.com. Use them. Give the URL to your vibe coding agent. Copy the format. Make your own version.

And if you want to see this built live, come to SaaStr Annual on May 12-14. Amelia is doing a session where she rebuilds an AI VP of Marketing in real time with a Replit engineer on stage. All the major vibe coding platforms — Replit, Lovable, v0, Vercel — will be there. Anthropic will be there. The goal of Deploy Day on Tuesday is that you walk out with your own working AI agent.

Because if we built it with zero engineers, you can too. It just takes someone who cares enough to manage the agent every day. That’s the real unlock.
