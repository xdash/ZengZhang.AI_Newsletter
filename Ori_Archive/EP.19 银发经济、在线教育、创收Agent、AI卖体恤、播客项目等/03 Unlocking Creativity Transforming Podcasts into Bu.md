# Unlocking Creativity: Transforming Podcasts into Business Ideas

> 原链: https://thebootstrappedfounder.com/the-podscan-ideas-vault-engineering-as-marketing/  
> 来源: thebootstrappedfounder.com · 归档自 EP.19 · 抓取于 2026-08-06  

---

Today I’ll be talking about a successful marketing project within my software business that turned out to be so successful that it spawned a business built on top of that business. And when this episode is released, it’ll be one day since the platform has been live, so I’ll be sharing the most raw and most timely insight into what happened, what the story is, how it happened, and how I went about building this particular project.

This episode is sponsored by [Paddle.com](http://Paddle.com), my Merchant of Record payment provider of choice who has been helping me focus on Podscan — and the project I’ll be sharing with you, quite literally from day one. They’re taking care of all things related to money so founders like you and me can focus on building the things only we can build. Paddle handles the rest. Sales tax, credit cards failing, all of that. I highly recommend it, so please check out [Paddle.com](http://Paddle.com).

## The Birth of an Idea

The thing I built is called the Podscan Ideas newsletter, and on top of that newsletter now sits the Podscan Ideas Vault, which is a platform that tracks, scores, ranks and analyzes business ideas that it pulls from the full transcripts of fresh episodes of around 500 podcasts of all kinds – mainly focused on entrepreneurial, business, finance, philosophy, and science podcasts.

Now, it isn’t a novel idea to extract information from other media, right? The whole idea of travel guides or rewatch podcasts is pretty much an indicator that there is value just by extracting things from existing content created by people. But Podscan in particular has been extremely well set up to extract information from a whole industry’s worth of insights and content in a very, very easy way.

## The Customer Who Sparked Everything

In fact, I have several customers that have lists of podcasts set up on Podscan with a webhook. Whenever a new episode comes out, it sends it over to their servers, and they send it through a lot of cleaning up. They take the transcript, analyze it, summarize it, and do a lot of stuff with it, and then they generate some kind of content from this and send that out to their own customers.

Imagine – I have a couple people just taking podcasts and summarizing them and turning that into a newsletter. But here’s the really interesting one: I have a particular customer that works in the medical field who summarizes very specific podcasts in a very specific subfield – like a subdivision of one particular kind of surgery. He takes all the podcasts that are run by experts in that field, extracts the most relevant information and even translates that into a foreign language, so that people who operate in that field, in that particular country, are able to get all the information from these many hundreds of hours of podcasts that come out every week at a glance. He even has the capacity to only show the episodes relevant to that particular person.

And that inspired me.

## From Inspiration to Implementation

I recently thought about what a success story that is – that somebody is pulling all this information through the Podscan API, through our webhook, real-time webhooks that are activated whenever a new episode comes out and we transcribe it. We immediately send the full transcripts over to anybody who has an account and is tracking that particular show.

I was like, “Well, this is a great example of how Podscan can be used, so why don’t I tell my audience, and why don’t I tell the world about this particular use case?” Which I did a couple of weeks ago. I started working on sharing not only that the story exists, which is cool, but also promising that I would build an automation using the existing automation tools out there – things like Zapier or n8n or Make – to show how this can be done reliably using the platform. Because I wanted to show “Hey, Podscan can be easily integrated,” and I wanted to reach more customers. So why not do development or coding or integrating as marketing?

## Building the Automation

I started building this automation on n8n, which is a very highly flexible but more technical platform to build integrations in. I took my webhook that came from my podcast list, where I just added a couple hundred podcasts from all kinds of interesting industries, took the webhook, generated a summary for each of these episodes and saved that in a Google Sheet.

It was really simple. I just used tools that I already had active. I didn’t have a service, a backend, a database. I just used Google Sheets, OpenAI’s APIs, and everything else that n8n offered was more just logic.

I wanted to create a newsletter out of the data from these podcasts. And I thought, “Well, my audience is entrepreneurial. Why not take all the good ideas that come from all these podcasts?” People talk about “Oh, I wish this would exist” or “Hey, this industry has these problems. Somebody should really solve it.” Whenever that comes up, an AI can find these occurrences and take out the idea and flesh it out a little bit.

It could turn it into “Well, this could be a solution here. You could build an AI-powered marketplace that sells these things to these people, because they both are trying to look for sellers and buyers.” Or “You could turn this into an info product, because people say ‘I want to read about this.’ Well, why don’t you build something that facilitates that and gives people that information?”

## The Technical Process

So in my workflow, I took my webhook and generated an idea-based summary through OpenAI – just posting the full transcript and asking it to take the three best ideas out of it. Then I would write those ideas to a Google Sheet. Once a week or once a day – that was the idea – I would take all of the items in my Google Sheet, rank them in some way, take the top 10 and turn that into an email, turn that into a markdown document, and feed that markdown document into [Kit.com](http://Kit.com) (formerly ConvertKit), and just create a new broadcast and send it out to everybody who’s subscribed to it.

Kit has a really wonderful integration, so you can have a landing page where people can easily sign up. I thought that must be automatable, and it was. I very quickly got something working that just created a really nice list of the top 10 ideas and had additional information for each idea – like how feasible is it? How much money would you need to spend to get in there? What are the challenges? What are the opportunities? How can you potentially measure if the idea is implemented right? All of this into a newsletter.

A couple hours later, I had a fully working workflow.

## The Community Response

I shared a screenshot of that on Twitter and got a lot of positive feedback. Meanwhile, people were signing up for Podscan to begin with, just to see if they could themselves build something without knowing exactly how to do it. I got a lot of DMs on Twitter about people that would really like to see me walk them through it so they can set up something like this in their own industry.

So I decided to make a video out of it. I recorded myself explaining the already set-up process in the n8n workflow, step by step. Here’s where the webhook comes in. Here’s the fields you can expect. Here’s how you can create a summary. I even shared the prompts for each of the steps – both the summary and the newsletter generation. I shared which APIs I use, what the [Kit.com](http://Kit.com) API looks like, what the API for Google Sheets looks like. Obviously, anybody could use whatever they want, but I just shared how I approached this in a video.

I shared that video on Twitter as well to great success. A lot of people signed up for Podscan just to see if they could build something themselves. But – and here was the thing – a lot of people were interested in the actual outcome of that newsletter. It wasn’t just an experiment to show how Podscan worked. People wanted to actually get the business ideas.

## From Newsletter to Platform

So I doubled down and made the newsletter generation tool better and better, refined the prompts and all of that. But it was still just a newsletter. And just a newsletter is great because it will always be a great way for me to advertise Podscan being the source of all the information in the newsletter. But there’s so much missing.

In 500-plus podcasts that I currently look into, there are a lot of ideas. I get hundreds of ideas a day, but only a couple of them make it into the email, because 10 is already a lot. But what do I do with the other ideas? People wouldn’t be able to get them because I just take the top 10, but the others might still be interesting.

So I thought, “How about I build a software as a service platform, or just a platform where I save all these other ideas and I make them available to anybody who’s interested?” And obviously this being an extension of Podscan, because it’s sitting on top of Podscan APIs and the Podscan data, I could probably monetize that a little bit. The newsletter should always be free. Cool ideas should be out there, but 10 of them for free a day is great. How about I make everything free that happened over the last 24 hours? But if it’s older than that, if it’s an archived idea, if it’s something that came up last week and you want to look at it, I make it available for a fee through a subscription to the platform.

## The Ideas Vault Vision

Once I started thinking about this, I very quickly came up with the idea of the newsletter vault. Because a vault would be a place where all the good ideas are stored and stashed, where you can search for them, search for ones that are related, do a deeper analysis. Maybe you could even chat with an idea to see what the potential problems are beyond the couple of paragraphs that are in the newsletter. You could do a deep analysis where you could really go have a really smart system look into all the potential pitfalls, all the potential little challenges along the way.

You might even have an opportunity to click a button and have the idea be built by tools like Lovable or Bolt or v0 – any of these tools that allow you to prompt your way into a product. Well, I have the prompt because I have the idea, and I have a system that could easily make this available.

## Building with AI

So I built a software as a service platform on [ideas.podscan.fm](http://ideas.podscan.fm) that facilitates exactly this – the Podscan Ideas Vault. It’s a really simple Laravel 12 project that has been completely coded by Claude. I wrote maybe two lines of code in this and everything else was fully automatically prompted into existence.

It uses the Laravel Spark tool that allows me to integrate Paddle, my payment provider of choice. I use the default Tailwind design because it’s very data-focused, so I don’t need to have fancy graphics or anything. We just focus really on the ideas, the concepts that I’m interested in. And I integrated a couple of webhook endpoints where, instead of saving data into Google Sheets, this application would now host all the ideas. It would host all the newsletter episodes. It would be an archive of the newsletters as well.

My n8n automation could slowly be turned into either a completely internal process or use these endpoints of the Ideas Vault to store and fetch information from.

## The Launch

I built this over two or three days. I created a new account on Paddle, which was verified a couple days after, and then I started integrating all the relevant secrets into the project. And now it’s a fully functioning software platform that hosts, at this point, almost 1,500 ideas extracted from individual podcast episodes – with quotes where they were mentioned, with the actual location in the conversation where the idea comes from, and the kind of idea for what founder it’s for, how much it might take to get to any revenue, and what the initial investment is. All of this constantly, automatically extracted from podcast episodes as they are being released in hundreds of shows.

I added a function for people to suggest new podcasts to track that I can add to the system. I added functions for people to chat with ideas, to favorite ideas. You can see past newsletter episodes. And all of this is pretty much available for free for anything that was added in the last 24 hours. Any idea, any newsletter episode that is 24 hours and younger is completely available to anybody who’s interested – both logged-in users and non-logged-in users. Everybody can see this. And the moment they want to go to an idea or a newsletter that is older than that, they are asked to purchase a subscription.

It has been very simple to build because Claude is highly capable of building these kind of CRUD applications – the create, read, update, delete apps that really just interact with the database and show things from a database, and then you can add your comments to it and stuff. Claude is really good at that.

## The Results and Future

This has been operating for a week now, just testing the system, and yesterday, as of this episode being released, the newsletter contains a link to the ideas platform, and I started sharing it on Twitter. I’ll see where this is going, but it will be an interesting source of revenue for Podscan, which it likely is, because this is a database that just keeps growing in terms of the value of the content. I have vector search happening in there, so people will find ideas for keywords that aren’t even really mentioned in those ideas.

It’s a really interesting project just to source information from what’s already out there, but it also has the capacity to show people how easy it is to set up something that sits on top of the Podscan API. All these podcasts, all these episodes, all these transcripts have so much valuable data in there. This is just one way of showing how this can be used.

## A Business on Top of a Business

So it’s a business on top of a business. I think I’ll look into building other ones just like it over the next couple of weeks. But because this is also so heavily automated, and it’s such a daily injection of fresh ideas into the community, I think this is a really helpful little tool to pull information from podcasts out there.

In my own numbers, in my own prospects on Podscan itself, this has already shown an uptick. The idea of sharing – the whole concept of taking podcast content and reworking it into condensed, extracted information that you then share periodically – that’s not just my doctor customer’s idea. That’s not just what the Podscan Ideas Vault is about. That is a generally applicable concept that can be used for podcasts in almost any industry.

If you have experts in your industry, you can pull all this information that they have, that they share on podcasts, out, compress it, and share it with the yet-to-be experts in your industry. Any industry can benefit from this because you can turn it into any shape of content you want. You could turn it into YouTube video scripts. You could turn it into automated TikToks. You could turn it into newsletters, obviously. You could turn it into individual emails that you send out to individual people. It doesn’t really matter. The data source is the same, and that’s the Podscan API with all these podcasts.

## Engineering as Marketing

So that is what I’m trying to do – it’s engineering as marketing and business building as marketing that is both an opportunity to get people to have a subscription to an Ideas Vault and see the power of Podscan.

That’s my latest project. I think it’s really fun. It has been really fun to build. Please do check it out at [ideas.podscan.fm](http://ideas.podscan.fm). You’ll see all the latest ideas for free there. If you are looking for a business idea, these are really cool and all of them link to the podcast where the idea was discussed so you can check it out. They’re scored, they’re analyzed. Might be really interesting. I’ve seen a couple really interesting ones.

Of course, there have been challenges, technical challenges to make this tool work, to make it interesting. I think I’ll share more about this over time. I already had to implement quite a lot of things to make the ideas pop, to make them really valuable, which is, I guess, a trade secret at this point. But I’ll share more over the next couple of weeks, seeing where this goes.

Let me know what you think. I’m always excited to hear, particularly in this super early stage, where this could go, where you could see this going and all of that. So I’m excited about the Podscan Ideas Vault and the power of Podscan being shown in a real project sitting on top of the API.
