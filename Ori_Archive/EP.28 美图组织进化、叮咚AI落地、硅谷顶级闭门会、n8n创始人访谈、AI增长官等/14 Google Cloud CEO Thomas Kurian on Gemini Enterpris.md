# Google Cloud CEO Thomas Kurian on Gemini Enterprise, AI's Labor Implications, Investment Frenzy

> 原链: https://www.bigtechnology.com/p/google-cloud-ceo-thomas-kurian-on-ecd  
> 来源: www.bigtechnology.com · 归档自 EP.28 · 抓取于 2026-08-06  

---

Google just introduced a version of its Gemini chatbot built for business use cases. The new product, Gemini Enterprise, connects with enterprise data and includes an agent builder, customer service tools, and more.

The initiative comes amid a flood of new AI investment, which has ramped pressure on the technology to deliver returns for business, and reports that enterprises have struggled to implement AI effectively. Google Cloud Platform is well positioned in this regard. The unit has surged amid the generative AI wave, and the company’s Gemini 2.5 Pro model currently sits atop the LLM Arena leaderboard.

Thomas Kurian, Google Cloud Platform’s CEO, spoke with me about the rollout of Gemini Enterprise this week. Here’s our conversation — edited lightly for length and clarity — where we cover the fundamentals of a successful enterprise AI implementation, AI’s likely impact on white collar work, and what Kurian makes of the AI investment frenzy.

Alex Kantrowitz: Why do businesses need a separate version of Gemini?

Thomas Kurian: It’s the same Gemini model. But it connects Gemini to two important things. One is all the bespoke data sources and applications like your Microsoft Office 365, your JIRA project management system, your ERP or CRM apps. It provides connectivity so that you can understand the information in those systems. Secondly, it also understands your personal context: Who do you work with? What information are you looking for? What meetings do you have coming up so I can prepare the information for you, and what task can I do on your behalf?

Have you heard the recent conversations about how AI has not been working well for enterprises?

Yes

From a technical standpoint, what is the most difficult thing to do when it comes to building AI for enterprise?

There are three elements. First, you need to have a model that’s world class in not hallucinating, and is using the right tools to do the right job. Gemini 2.5 gives people that. The quality of the model is really important.

Second is just giving you a model by itself is not useful. If you’re building an agent — let’s say you’re doing financial analysis for your CFO — that agent needs to look up financial results from your ERP system. It needs to look at contracts you have in your Microsoft Office system. So it needs to be able to reason across all of that enterprise context. But in doing so, it should maintain your security, meaning it shouldn’t say, ‘Well, now that I have all this data, I’m going to publish it to the whole company.’ So it needs to manage your security and permissions the right way. And it needs to be able to understand the information as it changes, because in enterprises, information changes all the time.

Third, when you build agents, you need to have a central place to govern and manage. Because organizations are worried about a million agents happening in their company and not having a central place to manage what permissions, what tasks they’re given permissions to do, etc.

So that’s the three pieces: A great system that understands the enterprise. Feeding it with the context to have agents operate. And a central place to govern and manage. And Gemini Enterprise is designed to address all three.

Let’s talk about agents. Do you think they’re underhyped, have the right amount of hype, or has the industry overhyped them?

I think there’s a lot of hype.

So many people have swept many of the problems that agents need to do correctly under the rug, Take, as a practical example, you want to have an agent monitor all supplier contracts and determine which ones have indemnification warranties for you, a very mundane thing, The agent needs to be accurate in flagging these things. It needs to understand the details of what a contract is and also be able to reason on things like indemnification and warranties. It may need to access your supply chain system to understand how much exposure you have to these guys, because if you have exposure to a big supplier that’s not giving you indemnification, it’s a big issue.

So when you look at agents, what we’re really trying to do is to give people the ability to build agents, to have those agents be able to use tools to access information from the company systems and reason on it, and then to have a central framework to manage this so that somebody doesn’t say, oh my god, an agent looked up all my supplier information and someone else got access to that information.

it seems like the industry has used ‘agent’ as a fancy term for something that uses a tool and comes back to you with an answer in the chatbot vs. something that’s going out there, and does a full job, Do you think that’s a fair criticism?

I think that’s a fair criticism. That’s not how we define an agent.

How do you define an agent?

An agent for us is an autonomous system that understands the user, can perform multi-step interactions, can generate multiple potential answers, can use tools to critique those answers, and has a high degree of accuracy in performing these multiple steps.

So for instance, to your question on chat as the front end, a lot of times, people say, ‘I’m delegating a task to an agent.’ It goes out, generates a single step response, and because you don’t trust the answer, because it’s such poor quality, you don’t delegate anything to it. It’s just a fancy word for chatbot doing asynchronous things for you. That’s not what we’re talking about.

You consider Deep Research an agent. But it’s also effectively, to me, a function that happens within a chat window. Am I just not comprehending the complexity on the back end?

It’s how you can chain it along with other things. Let’s take a super simple example, I am being asked to go to a customer site and repair a modem. Just hypothetically. That task has many different things. It has the need to schedule me. It has a need to ensure that I have sufficient repair equipment. It needs to have an accurate diagnosis of what might be broken. That’s typically many, many steps from scheduling my time, making sure I have the skills to actually do the repair, ensuring there is inventory that’s going to be dispatched along with me, et cetera,

Now, when we look at that, it’s a chain of activities that can be a collection of individual agents. It can have an inventory agent, it can have a scheduling agent, and it could have the deep research agent to say — If I don’t have this part, can you go and research the supply chain to see if there’s an alternate part, because this one’s in short supply, and the customer needs a solution tomorrow afternoon.

So that chain of reasoning requires an accuracy in every step, because if any one of them is wrong, the output can be wrong by a large amount.

If each individual step in a change sequence can be off by 2% or 3% the outcome can be wrong by 50%. And so there’s a lot of things that we’ve done with our agent framework, for example, to have the system correct itself, be able to generate multiple responses, to actually test those responses. And all those elements are what we talk about as actually constituting a multi-step agent.

In the Gemini Enterprise release, you talk about a data science agent that can automate data wrangling, accelerate detailed data exploration, find patterns, and streamline complex model development. What’s left for a data scientist to do?

The data scientist still has to explain to Gemini what problem to go look for. We’re taking care of the mundane elements of what people used to call data engineering.

That data engineering was often the lion’s share of a data scientist’s work. What do you expect to happen to the data science field?

Think about a practical example. I want to do exploration of a clinical trial and the efficacy of the clinical trial. So there’s a number of steps involved with it. The results of the trial could be in one system, the parameters of the trial and the demographics and population could be in another system. So the first step is ingest the data from these two or three different systems into one system. And as part of ingesting, normalize it. Then tokenize it. If it’s healthcare data, you have to tokenize it so that people don’t see my information. Then catalog that information. This tool can help automate a lot of that.

On the front end, you can ask it, for example, ‘I want to run a statistical sampling of this set cohort of people, and I want to run an exploration across X number of tests we did on them.’ So that can be expressed in a high level language. Behind the scenes it will generate code for you to say, ‘Okay, this is the sample you want to run,’ And you can also say, run it only against this subset of the information from the trial. It can subset it and run it against it. Hopefully, it gives you a sense of what the agent itself does.

Now, how does it help people? It helps open up the door for a lot of teams that don’t have data engineers associated with them to go faster and do it a bit easier than they had before.

But, again, the question was about what happens to the data scientist?

What happens to data scientists? They can run a lot more experiments than they could before, because you can create a lot more synthetic tests or scenarios using the model, and you can run these ML experiments much, much faster than you can before.

When people see this technology, there’s a couple reactions. One is, I’m not sure if it works. Another is, it’s going to automate all work. Is there a middle ground between the two?

Yes, I think there is definitely a middle ground. And I think partly it’s because people are reacting to hype on one end and also not thinking rationally on the other end.

Take one of the products we’re announcing, something called Customer Engagement Suite. This is the ability to do chat and voice based interactions from a web or mobile app to be able to respond to customer service and sales and other questions. Now this product is being used widely by many, many companies.

When we first introduced it, people said, ‘Does that mean we don’t need any customer service agents anymore?; You know, the reality is, in almost all our clients, they have not let go anybody

And so what is the value of this customer engagement suite? It answers questions that many people never bothered to call the company about, because they were like, ‘Hey, I have to wait forever in line on the phone. The company doesn’t understand my native language, so I’m afraid to call them because they don’t have somebody in my native language’ It’s helping answer a lot of questions that people could never solved before, and so never bothered to ask. So sometimes when technology vendors put forward something, people extrapolate to outcomes that may or may not be true.

Thinking about the future of the interface, is there going to be one universal interface on top of all business software platforms, or is there some combination of chats and then traditional software?

It’s a great question. We see it evolving very quickly. We see a couple of things. One is, we definitely see the interface becoming multimodal, not just chat. There’s so many solutions where the input and output is no longer chat. They want to just take video in, video out, or or image in, image out. And it’s becoming incredibly powerful to be able to do that.

Here’s an example: reimbursing you for an accident on your vehicle. You chat with me, and then you say, let me show you what the damage on my car is. I take a picture, and you take a picture and upload it, and you want to hear back, you know, over voice, for example, we can reimburse you, and we’re just debited your bank account X amount of money as a credit for you. Do you see what I mean now? That’s interface, as we see the multi modality becoming super streamlined with our tools. More and more organizations in many, many industries are changing from just chat to multi modal.

Yes, but we have this entire business software industry. If the agent does its job, do we need those programs anymore?

You will need those because they also manage business rules for the company. For example, if you have a general ledger, it’s managing your accounting, and there’s a set of financial rules it manages. There are professionals who just use that interface. There’ll be others who go through an agent for self service tasks. We’re not saying nothing will change over time, it might change.

One last quick one for you, the AI industry, there’s so much money flowing around lots of circular investments. Is this healthy?

If you don’t create wealth, and you just pass wealth from one pocket to another sooner or later that you know how that ends. We’re focused on providing customers real value. I think you’ve seen our growth, and because we have our own chips and our own models, we’re not just redistributing other people’s stuff, and so I think over time, you’ll see it in our financial results.

This week on Big Technology Podcast: Anthropic Chief Product Officer on Why AI Model Development Is Accelerating

Mike Krieger is the chief product officer at Anthropic and co-founder of Instagram. Krieger joins Big Technology Podcast to discuss Anthropic’s Sonnet 4.5 launch and how the company’s been able to speed up AI model development. Tune in to hear how Anthropic is using internal tools to move fast, where the next generations of model improvements will look like, and whether model orchestration will be the core differentiator between labs. We also cover how AI development compares to social media, whether AI content will ever take off, and enterprise AI’s path ahead.
