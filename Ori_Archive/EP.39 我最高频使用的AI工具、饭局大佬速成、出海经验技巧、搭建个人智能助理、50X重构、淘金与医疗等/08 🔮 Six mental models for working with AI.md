# 🔮 Six mental models for working with AI

> 原链: https://www.exponentialview.co/p/six-mental-models-for-working-with  
> 来源: Exponential View · 归档自 EP.39 · 抓取于 2026-08-05  

---

# 🔮 Six mental models for working with AI

### Plus a stack of 50+ AI tools we use at Exponential View

The question of whether AI is “good enough” for serious knowledge work has been answered. The models crossed that threshold this year. What’s slowing organizations down now isn’t capability, but the need to redesign work around what these systems can do.

We’ve spent the past 18 months figuring out how. We made plenty of mistakes but today I want to share what survived. Six mental models that can genuinely change the quality of work you get from generative AI. Together with the [seven lessons we shared earlier in the year](https://www.exponentialview.co/p/seven-lessons-from-automating-our?utm_source=publication-search), this is the operating manual we wish we had all along.

**At the end, you’ll also get access to our internal stack of 50+ AI tools. We’ve documented everything we’re actively using, testing or intend to test, to help you decide what tools might work for you.**

Enjoy!

### 1. The 50x reframe

Most people start working with AI by asking something along the lines of: how do I speed up what I’m already doing?

That question is comfortable and wrong. I find that it anchors me to existing constraints.

A more useful question is:

What would I do if I had 50 people working on this?


Then work backwards.

The 50x reframe forces you to imagine the ideal outcome unconstrained by time or labor. Only then do you ask which parts of that hypothetical organization can be simulated with software. I now encourage our team members to think of who they would hire, what work that person would do, how they’d know if they were successful.

If you’ve not had the experience of hiring fifty people on a project (fair enough!), use this prompt to get you started to identify what it is that you may need:

##### A prompt you could use:

`I currently [describe your task/process]. Walk me through what this would look like if I had a team of 50 people dedicated to doing this comprehensively and systematically. What would each role focus on? What would the ideal output look like? Then help me identify which parts of that hypothetical team’s work could be automated or assisted by AI tools.`
For example, we use this approach for podcast guest prospecting and research. We used to rely on network and serendipity to identify 20-30 strong candidates for each season; a mix of the right expertise, timing and editorial fit that consistently delivered good conversations – but left too much to chance. Instead, 50x thinking asks what if we could systematically evaluate the top 1,000 potential guests? What if we could track the people we’re interested in so they surface when they’re most relevant? We built a workflow that researches each candidate, classifies expertise, identifies timely angles, and suggests the most relevant names for any given week’s news cycle.

### 2. Adversarial synthesis

Even experienced operators have blind spots. We internalize standards of “good” based on limited exposure. No one has seen great outputs across every domain but the models, collectively, have come closer to it than anyone else.

To make the most of this superpower, I give Gemini, Claude and ChatGPT the same task – and make them argue. Then have each critique the others. You’ll quickly surface gaps in your framing, assumptions you didn’t realise you were making, and higher quality bars than you expected.

![](https://substackcdn.com/image/fetch/$s_!zg5A!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faa30a739-743d-492a-82d4-ffada9480b49_1024x1024.png)

When models disagree, it’s usually a sign that the task is underspecified, or that there are real trade-offs you haven’t surfaced yet. Which brings us to the next point.

### 3. Productize the conversation

If you’re having the same conversation with AI repeatedly, turn it into a tool. Every repeated prompt is a signal. Your workflow is basically telling you that this (t)ask is valuable enough to formalize.

I found that when I productize a conversation by turning it into a dedicated app or agentic workflow, my process gets better at the core and my tool evolves over time. So the benefits of the original conversation end up compounding in a completely new way.

##### A prompt you could use:

```
## Context
I have a recurring [FREQUENCY] task: [BRIEF DESCRIPTION].
Currently I do it manually by [CURRENT PROCESS - 1-2 sentences]. 
Here’s an example of this task in action:
<example>
Input I provided: [PASTE ACTUAL INPUT]
Output I needed: [PASTE ACTUAL OUTPUT OR DESCRIBE]
</example>
## What I Need
Turn this into a reusable system with:
1. **Input specification**: What information must I provide each time?
2. **Processing instructions**: What should the AI do, step by step?
3. **Output structure**: Consistent format for results
4. **Quality criteria**: How to know if the output is good
## Constraints
- Time/effort budget: [e.g., “should take <5 min to run”]
- Depth: [e.g., “verify top 10 claims, not exhaustive”]
- Tools available: [e.g., “has web search” or “no external lookups”]
- Error handling: [e.g., “flag uncertain items vs. skip them”]
## Desired Format
Deliver this as a: [CHOOSE ONE]
- [ ] System prompt I can paste into Claude/ChatGPT
- [ ] Zapier/Make automation spec
- [ ] Python script (Replit-ready)
- [ ] Lindy/agent configuration
- [ ] All of the above with tradeoffs explained
## Success Looks Like
A good output will: [2-3 bullet points describing what “done well” means]
```
I kept asking LLMs for editorial feedback multiple times a week, for weeks. After some fifteen hours of repeat prompting, I built a virtual editor panel in Replit and Lindy.
