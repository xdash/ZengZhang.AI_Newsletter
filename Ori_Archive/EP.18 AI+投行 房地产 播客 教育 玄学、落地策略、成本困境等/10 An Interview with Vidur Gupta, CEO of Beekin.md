# An Interview with Vidur Gupta, CEO of Beekin

> 原链: https://artificialinvestment.substack.com/p/an-interview-with-vidur-gupta-ceo  
> 来源: artificialinvestment.substack.com · 归档自 EP.18 · 抓取于 2026-08-06  

---

This week, I did an interview with Vidur Gupta, founder & CEO of Beekin, a real‑estate analytics platform that blends public, spatial and asset‑level data with machine‑learning and (increasingly) generative‑AI. Beekin’s core products forecast asset values, rents and resident behavior—especially the likelihood that a tenant will renew—so that multifamily and single‑family rental owners can boost retention, reduce vacancy downtime and fine‑tune pricing. In the simplest terms, they have a bot that tells landlords how to set the rent (among other things).

Here are some key takeaways:

- **GenAI-powered guidance** : They are using GenAI to help convert data into clear recommendations such as changing the rent on a specific unit. They are helping even people who “hate data” make more informed decisions
- **Agents on the loose:** Prototype agents aim to automate key tasks for property managers and owners, working with existing software stacks
- **Pricing:** Beekin avoids per seat pricing by having fees scale with the number of units, rather than to user counts.
- **Agent collaboration** : Rather than becoming the “über‑agent,” Beekin wants to be the trusted intelligence agent that other agents call for rent or renewal decisions
- **Token‑cost debate** : We debated whether in the future LLMs will stop lowering token costs
- **Data syndication:** We discussed whether it’s a good idea for data companies to let customers put their data into models, and I got a little spicy with some of our vendors

Please check out the lightly edited video or transcript below:

**Richard Lichtenstein:** Hello. I am Richard Lichtenstein. I am the host of Artificial Investment, a Substack and occasional podcast. I'm joined by Vidur Gupta, who is the CEO of Beekin. And he's going to have a lot of really interesting stuff to tell us about GenAI today.

Vidur, nice to meet you. Why don't you introduce yourself and tell us about Beekin and what it is?

**Vidur Gupta:** Absolutely. Thanks again, Richard. Good to meet everyone, and thanks for having me here. So my name is Vidur. I founded Beekin after working in banking and at a $70 billion private equity firm where I accidentally invested in $2 billion of real assets.

And as an investor, I realized how inefficient private markets were. And how a lot of alpha was created through information arbitrage. So at Beekin what we do is we harness a lot of public data, spatial data and asset level data to predict asset valuations, rent, nowcasting and forecasting. We also predict renter behavior, how likely renters are to renew their lease. And we provide that to equity investors in apartments and single family rental to optimize their portfolios.

So the business is primarily a software company which leverages a lot of machine learning, supervised and unsupervised. And increasingly we are finding quite amazing GenAI use cases in, in what we do.

**Richard Lichtenstein:** I think it's a super interesting business. So before we get into all the Gen AI stuff, just would love to just understand a little more about exactly how it works. So how do you predict that someone who's renting an apartment is gonna not renew their lease?

**Vidur Gupta:** That's a great question. If you think about people who rent it's no different to consumer behavior in e-commerce or any kind of transaction. Where there's a lot of rich history or breadcrumbs of the consumer's prior interactions with the product. And what we do is we compartmentalize it into three buckets.

First is the actual SKU or the rental property, how expensive or cheap the property is. Obviously that's a big predictor. The second is financial attributes of the renter affordability and how regular they are with payments and things like that. And the third part is satisfaction or interaction within the built environment, which is information we extract from general ledgers or systems of record.

And that's messy stuff like repair requests, and then the last piece of course: neighborhoods have a lot of spatial insight through demographics, density of schools, distance tools, jobs which govern whether people stay there for long or don't stay there for long. So I think that that provides a composite kind of understanding of behavior.

**Richard Lichtenstein:** Great. Let's get into the GenAI aspect of it, right? So is GenAI involved in some of that feature extraction? If somebody calls up and complains about something, is GenAI able to interpret that complaint and the resolution of it and say did it work or not?

**Vidur Gupta:** Exactly. I think there are two constraints to that. One is the quality of the data and how it is stored and normalized in these systems, which is always a challenge. And the other aspect is responsibility. If you think about it and you zoom out a little bit, we are using machine learning to make decisions on people, and these are renters who are not very homogenous.

So we are a bit careful about feature engineering, feature extraction and making sure there's not implicit correlation with factors that might start to discriminate against certain groups. But yes, I think GenAI has a big role to play in how some of these features can be understood. Because they're meta features, right? People use some of these rules to make sense of renters, right? If someone's young, they're gonna move. If someone's making a bunch of money, they have a lot of money to spend. All of these are heuristic, which people use for making day-to-day decisions. So we want to make sure as we make this industry leapfrog to the next level, we don't wanna compound those biases.

**Richard Lichtenstein:** That makes sense. To me a lot of this feels very intuitive, right? If somebody calls and complains that there's no hot water 20 times, they're more likely to leave.

If they're young and have a lot of money, they're more likely to look around. A lot of this seems very intuitive. So what's the value add of Beekin given that a lot of this is kind of intuition anyway?

**Vidur Gupta:** That's a good point. I think there is two parts. One is a model at scale, which is, battle-tested is less biased than people. Two: making these decisions by looking at all these factors or columns or meta analysis is time consuming. And if you scale all the way down to the leasing agent or someone who's doing the day-to-day job of making these decisions is time consuming and it's costly.

So a model which is accurate and predictive can be used to empower these agents to do higher value stuff, right? So to your point, if someone is angry or gonna leave and you have that intelligence, 80, 100 days before their lease is coming up for renewal, there's things you can do about it.

So what you've done is with that single tweak you've made the leasing agent a true customer service person. Where they can, reach out. And the value to a landlord is very simple. When people leave, it costs money to fix the property. The property is empty for typically two to four weeks.

And what we are seeing now in this weak market, renters just can't afford to pay more money. So it's likely that you will not be able to push rent a lot on anyone coming in. So mathematically it doesn't make sense to let people leave, and therefore the industry is moving to this service driven economy.

Very similar to what hotels and airlines have done exceptionally well with loyalty, where they're trying to make sure that they can save every renewal that is possible.

**Richard Lichtenstein:** The landlord actually, really wants to keep the tenants there and keep them happy.

Sounds great. I think to everyone listening to this who has a landlord, it's good to hear that you're using data, but it sounds like the decisions the data is leading to are things that are pro-tenant and generally probably good for everyone, which is nice.

**Vidur Gupta:** Yeah. And there's a perfect equilibrium, right? And the problem is even the landlord doesn't necessarily reach that equilibrium because, they are too lopsided. But I think, you're absolutely right. There is value to both parties in reaching that efficiency.

**Richard Lichtenstein:** Now let's get to the GenAI. How are you using GenAI in this product?

**Vidur Gupta:** Yeah, that's a great point. Two ways. One, of course, like most data companies, we are a model data output company. We are obviously using a lot of Gen AI for reports, for serving up these insights to the end customer so that they can interpret and make sense of a lot of messy information in a storytelling manner, and they can understand and embrace the output.

We are working with groups who are testing, creating agents on top of this. So imagine an agent which could, from a landlord standpoint, identify renters, reach out to them, intervene, remediate problems, and then essentially close a renewal, and all of that sounds simple right now.

The entire food chain is fairly broken. There are people involved in each of these steps inside a property company. So you're not just unlocking revenue for or value for the landlord, you are also unlocking efficiency for whoever's doing this job. So I think those are the two ways we think GenAI is most impactful in just this food chain.

**Richard Lichtenstein:** So if I think about the couple of use cases you mentioned, I think the reporting one makes a lot of sense. I've looked at a lot of data companies and one thing I've heard over and over is we can use GenAI to take that data and make it easier for people to draw insights from it.

That's a great use case. So let's start with that. Let's dig into that one more click before we go to the agents. What do the reports say, right? What is the AI able to extract from the data and pull up, and how are people using those insights to make decisions?

**Vidur Gupta:** Yeah, that's a great point. So I think if you triangulate, there is a renter, there is the asset, which is the property and the market. There's a couple of roles. One, someone who's operationally involved in leasing and retaining and all of that.

And then there's an investor who wants to interpret this and connect different factors, right? So what's happening to the market? What's happening to the asset? And then depending on what's happening with the residents or renters, how can I change or improve it? Because it's not never like a linear correlation, right?

It's winter in Manhattan, people don't really move. Your property isn't necessarily doing great, but it's not doing too badly based on historical performance. There are all these folks who are on the fence about likelihood to renew predominantly based on this reason, which could be price.

Your property is just too expensive for Brooklyn. Gotta figure it out, right? If you drop rate by 50 bucks on average, you are likely to go from whatever, 60% renewal retention to 65% renewal. Retention, right? Which will save you about, I'm just making this up, about $700,000 in cost, which is meaningful, right?

So all of that meta-analysis is possible thanks to GenAI. Which wasn't possible before because it's just connecting too many dots.

**Richard Lichtenstein:** I love that you're giving them specific recommendations about what the rent should be.

That feels very practical. I like to hear about people using AI for things that are pragmatic. So that's great. Let's turn to the agents for a minute.

Who are the humans that the agents are interacting with, what are the systems they're interacting with? How is that all gonna work? Are you using MCP or other protocols? 'Cause I think a lot of people are very interested in agents. But there are very few of them in the wild, so we'd love to understand more about what you're actually doing there.

**Vidur Gupta:** And remember, some of this is obviously, not in production, so I'm giving you the low down on what we are learning too, right?

We've all seen from customer support that there are benefits and drawbacks to having a purely agentic approach to supporting customers. Particularly when some of the challenges are like really tier three problems or slightly more advanced issues.

With this, I think there are two roles. One is usually someone internal. So you go from, a tiered kind of service approach, right? Where there's someone managing the property, someone who's their boss and their super boss. You compress that to one person who faces off with an agent.

The agent does all the work, they monitor it. And then the system reports on outcomes, right? Outcomes being how much money did the landlord make, or how many people stayed or did not stay as a result of an experiment, right?

Yes, MCP is involved. Obviously the whole industry is moving towards it and starting to use it more actively. And I think the systems are involved are too. First are a system of record. I'm not naming any names, but think of a Salesforce equivalent or like a true system of record.

And quite a few of those systems of record have started building their own agents. In other industries, I'm sure you've seen where they recognize that they'll have a bunch of native agents and then they'll have third party. So yeah, that's high level. I'm happy to go into details.

**Richard Lichtenstein:** The thing that I think is interesting is where you were going at the end of that answer, which is I think a lot of agents are gonna be flying around, and what you're describing is, to be honest, a bit of transition for your company, right?

Where I think today, if I understand correctly, your company is a data company, right? Your company is providing data and helping make data decisions and what you're describing with agents is going a little further than that, right? You're starting to get into some of the actual property management pieces, which obviously as you say, there are other systems that exist that are doing that.

So how do you think about where Beekin's specific role in that ecosystem is? And by the way, the answer could be you're gonna try to displace some of those existing systems that are old and outdated. But how do you see yourself fitting into what is already a fairly complex technical landscape?

**Vidur Gupta:** Absolutely. So first off, we already have a lot of workflow in addition to our math. So the way we deliver, keep in mind, like most of our customers are mid-market property management companies, they have no way to consume abstract models if you cannot use the models to do certain work, right?

Particularly when you scale all the way down to a property manager who's not a quant, they're not a data scientist. They sometimes hate data. So for them, data is a path to doing a job. So we've built a fair amount of workflow for our pricing engines, how we deliver pricing recs, how they connect with systems.

This is one way to serve up the outcome, right? If you think about is a system integration, either it's an API or it's a Snowflake instance, or it is an agent inside the ecosystem of whatever property management company they're using, right? And you're absolutely right. There will be multiple agents.

And the way we want to work with them is collaborate with them. There is value to collaboration. And for us, the agent is just another experience outside our SaaS workflow, right? It's a little more native, it's a little more embedded versus saying, "Hey, you gotta come to my dashboard, click on these five buttons, and only then will the magic happen."

**Richard Lichtenstein:** The idea that everybody's building their own dashboard and everyone's gonna go to a different dashboard is not gonna work.

The idea of people who hate data is my worst nightmare. I can't even imagine such a person but I believe you that such people exist and that they're users of your product. And so that's why I think something that's just very direct and recommendation driven that just says "raise the price here, lower the price here" is got to be the kind of thing that's going to be effective. But I think about this future with agents. You're headed for a similar problem where everybody's got an agent, and there's bots everywhere flying around and nobody knows what to do.

And so one of the things I think is likely to happen at some point the next say five years is there will be some sort of über agent that sits on top of all of the individual agents that different software is providing. And if that happens where do you see Beekin fitting in? Are you gonna try to be the sort of single point for the property managers, or you're one piece of that broader system?

**Vidur Gupta:** I think we'd like to be one piece of the system because if there is an über agent we'd like to plug into the über agent where they call us for a specific solution or a specific problem.

We like to continue to be best of breed in just that problem. What I would rather do is, if someone wants to lend to a property or wants to finance a property or buy a property, we can harness some of the same intelligence we have to help create agents for that workflow. Because I'm sure there's a lot of friction in there.

So that's our direction of travel versus wanting to own all of these agents by being the über agent, because to your point, who knows who that will be and who knows where that will come from? Will it be the systems of record who will go and create something? Will it be a third party who's just agentic by DNA and has taken leapfrog?

I personally feel the power still resides, particularly in real estate with a lot of legacy companies who have, vast majority of data and more importantly the belief that they have the best data or the most amount of data and they understand the operations workflow. Or if they're a lending business, they understand the lending workflow or the investment workflow far better than what any data company like us can ever do.

**Richard Lichtenstein:** I think that’s a healthy attitude as well because there is a lot of room for people to play in that middle layer with successful agents that are helping to drive good outcomes.

And I think that's where a lot of companies are gonna be. And I think if they're realistic about it you're going to end up being successful in that layer. And if you say, I got to be that top layer, I got to be the agent everyone talks to. You might not be, and then you've wasted a lot of time and money on something that's not going to work.

Now let me ask you about how you think about pricing. You can decide how much about your own pricing information you wanna reveal, but one, are you pricing on a per seat basis today? And if you are, how do you think about pricing in an agent world?

**Vidur Gupta:** Yeah, it's a good one. It's a great question. Right now we price on a per asset basis because fundamentally we are improving the health or the outcome for the individual unit or property or apartment. And my belief is some of that pricing framework should persist because if we do our job well in an agent world, some of the value will accrete directly to the asset.

Because we people will spend less time on the asset and deliver better outcomes on the asset. So we will be able to monitor the improvement in performance of the asset. I think there'll be pricing compression. There'll be some sort of commoditization, right? The wild card here is token cost.

I don't quite know how that'll evolve ' cause that's our COGS. Because we are in the asset based pricing model for some medium term outlook, because it is not linked to a seat. So we are not being measured in how many seats did we save? How many bodies did we save?

We are being measured in how much profit did the asset generate? Or how healthy is the asset, right? And so long as we can do a better job of an AB test or measurement of the asset value, we should be able to extract value out of it. I don't see medium term pricing model change from an asset based pricing model.

But again, I don't know if the quantum will be able to be the same because as agents become more pervasive clients might start to solve some of the intermediate problems through other things.

**Richard Lichtenstein:** Interesting. First of all, I think you've got the right idea.

Obviously any kind of pricing the more it's tied to outcomes, the better. Per asset, as you say, has that correlation. That's good. And I agree to avoid some of the issues here. I'm curious about what you said about token costs though.

I do hear people say token costs are high. This is why we got to charge extra for AI features and stuff. But in general, I feel like the token costs are cheap enough and keep coming down so much that I feel like that argument is just an excuse for raising price.

It's not actually a real thing. So I'm curious when you said that. Are you seeing token costs as something you're spending a lot of money on, or are you more anticipating that?

**Vidur Gupta:** I think it's more a future anticipation, right? We saw this with all the cloud costs, right?

The promise was significant savings going to cloud. But as you start storing more data, running more models, more instances, the cloud costs do rack up. It's not cents on the dollar anymore.

So it's more a future state of worry than today problem. And also I'm always concerned when so much of our COGS are dependent on such few companies who have inordinate pricing power because that's the only concern there. This might be a challenge as users start using more, right?

And as usage increases, we might see the costs rack up. So I don't necessarily think today is a problem, but I also don't know if this pricing model for the majors will persist. Do you think they'll turn around someday and say, look, between the three of us, we control 90% of the market and let's all get together and increase this 50% because people have nowhere to go.

**Richard Lichtenstein:** Yeah, that's an interesting question. I've heard other people express that concern that the low token rates today are a teaser to get people in, and then once they're in, they raise them. I haven't had any conversations that would suggest that's the actual strategy.

So I don't know if that paranoia is justified or not. I haven't heard anything that says it is, but I think it's not bad to plan for that, right? If you're building a product and you have a key input into that product and it's a monopoly situation. I don't think it's crazy to say, what if price went up? If that would bankrupt me or make my product unprofitable, that's probably not a good place to be. I think that's a reasonable thought although I I have no reason to think it's definitely gonna happen or anything.

**Vidur Gupta:** Quite a lot of our customers are probably users of Claude or ChatGPT and there's a watermark established on what you pay for using those tools.

I haven't seen that pervade into the agent world, but how do you think about that governing pricing models in the enterprise? Is that relevant or is that not relevant?

**Richard Lichtenstein:** I don't know. You're raising a good point which is we're going to get to this world with agents, right? And how agents are going to get priced is a real question. If I have my agent and the agent's running on a model who am I going to have to pay and how much do they have to pay them is an open question.

But then I've heard people starting to talk about this idea also of if I have an agent and the agent goes and connects to somebody's website or product, am I going to get charged a fee as part of that connection? They're trying to make money, right? So if my agent wants to use this, they have to pay some amount of money. Maybe it's less than a human would pay, but there's not zero cost there.

Then I think there's also a question with agents about how are you going to price the agent ultimately to the user? What are people's willingness to pay for agents going to be? How would they expect agents to be priced? These are all good questions. I don't have the answers. I don't think anybody really knows yet. But I agree for someone like you who's trying to build these agents and thinking ahead having a lot of flexibility is probably a good idea.

**Vidur Gupta:** I agree. And I think the people who have propensity to try and pay are enterprise users, right? Who have excess cash flow to invest in these things. But as you scale down to like mid-market companies, you got to have a sticker price and their propensity to pay is lower.

I always wonder when some of these are more pervasive across more than one category. What will that future look like? But that's a future problem and I'm sure there are other people way smarter than me who are thinking about this too.

**Richard Lichtenstein:** This is a question I see a lot of data companies grappling with, and I get that you're sort of a data company, but also sort of a workflow company, so you're in between.

But a lot of data companies really grapple with the question of the degree to which they should be willing to syndicate their data. And if I think about not the property manager user, but the investor user, right? So I'm an investor, I'm looking at buying some properties as investments.

I wanna use Beekin data as part of that because I want to figure out which apartments are going to have the best rent profiles or what have you. But I probably also might want to use a ton of other different data sources. I guess I won't name them here. I don't want to get in trouble or whatever.

But there's lots and lots of data sources that have characterized different aspects of the real estate market, right? And so I might want to have a model that has 10 sources of which Beekin is one of them. How do you think about that? Is that something you allow your users to do and make it easy for them? Do you make it hard for them? How do you think about that?

**Vidur Gupta:** We believe that the investment food chain starts from evaluation, underwriting, purchase, and then asset management, right? We have a pretty powerful tool for asset management because it increases their asset value.

We like to believe we should syndicate this far and wide because if they have uniform intelligence across the food chain, it'll make them powerful, make them stronger, right? They'll buy right, and then they'll manage right. So the way we do it now is we actually give it away for a fraction of the cost of what they would pay if they were using our asset management use case.

And the way we justify this is it makes our models more pervasive. There's some brand value uplift. And lastly, if they truly end up purchasing these properties, we have a shot at helping them manage these properties better. So as a data company, I think the most important thing I've learned is you've got to be pervasive.

People have to believe your data is right. And for that, they should be using that in 50 facets of their business or more. And when they do that, then there's no turning back.

**Richard Lichtenstein:** If anyone is listening to this who works at one of those many data companies that we work with that refuses to license their data to us to put into our models or use for AI, I hope you heard that.

I totally agree with it, that the more we can incorporate the data all over the org, the better. So again, I won't name names. You know who you are, if you're listening to this please cut us a deal and let us use your data in our models and other things because it'll make us use it more. I think that's the right attitude for data companies. I agree.

**Vidur Gupta:** The only caveat there is that as data governance becomes a thing, data attribution becomes a thing. There is this, headwind where people might build models trained on data, which they may not pay for, or might access or steal or scrape.

And then what happens to the data owner or the data provider? Long term, they are empowering an entire ecosystem without any of the value accreting to them. So that's the only thing people like us have to be careful of is we need to know where the data is landed.

**Richard Lichtenstein:** That's fair. That kind of thing is less of a concern for your type of business where there's a real time aspect to this data that's very important, right? It's not like I could say, I'm going to take the Beekin data, put it in my model, and then now I've got the model and I can cancel my subscription to Beekin, right?

Because you know what is happening in the market is going to shift and change and there's lots of things that happen in real estate and affect real estate. And so that model won't last for that long before it's out of date. So they need to keep paying you money to get your data, to keep their model fresh and accurate.

You can obviously decide how you want to price that, and if you think they're using that model in a lot of ways, you can always decide to charge more for it. But you are in the driver's seat. I suppose you're right that if you have a data company where your data asset is less about the real time nature of it and more about a historical backlog of hundreds and hundreds of reports that have a lot of value.

I get your point that once I've ingested those reports and put them into my model, then then you've lost a lot of the leverage in that relationship. Then maybe there is some sort of risk to you of being cut out. I think most data companies are more of the former type where the value of the data is not just historical data, but it's the ongoing feed.

But you're right, that's not every data company, right? But again, I think if you're a data company, you want people using their data as much as possible, and if they want to use it these days in AI stuff, just figure out a way to do it where you know what they're doing with it.

It's transparent, you understand what's happening to your data and where it's going. And you have some rights on that, but, but ultimately, your data's going where the customer's going. And that's probably what you want.

**Vidur Gupta:** Exactly.

**Richard Lichtenstein:** Let's wrap up there because I think we had a good discussion. Anything else that you feel we didn't touch on that you think is important for people to understand about Beekin or AI or anything?

**Vidur Gupta:** If there are real estate investors, private market investors here, I would just like them to believe that data is an opportunity. But I also want them to be realistic about what AI and AI cannot do. Just because to, to your point, Richard, there is a real time aspect of real estate, which is valid to trade off, but there's also the illiquidity of real estate, which makes it very hard to transact even if you have valuable signal or insights.

I think the market is in many cases getting ahead of itself. There is a lot of, utopian views about what AI can possibly do today. But I think it all starts with the hard work, the plumbing and that understanding that there are limitations to this. While we are very proud, we are pushing the envelope, I think it's also counterparties on the other side who need to be pragmatic about some of these pitfalls.

**Richard Lichtenstein:** It's a good point. Many of the people who are listening to this are investors in illiquid assets and so are probably hearing that, and it's resonating and they're saying “Yes, I own this company and it's great the data is saying X, Y, or Z. But, I'm not gonna sell this company for several years.” But I think the nice thing is a lot of the people who are listening to this are PE investors. They do own the company. They can do something. So I think having access to more data is helpful.

Because just like what you're saying is you get this data, you can adjust rents, you can make maintenance decisions, other decisions that will improve the value of the asset. I think if you're a PE owner and you own a company you can use the data to make better decisions about how to run the company and where to focus the management team's efforts.

If you're an LP and you own invest in a bunch of illiquid stuff, you're just sitting there, and you hope for the best. But if you're a GP and you have control over things, the data is always your friend because there's always something you can do with it.

Anyway, thank you so much for coming on. I thought this was really interesting. I learned a lot. So thank you for your time. Appreciate it. And if anyone is interested in learning more about Beekin send me a note. I'll connect you to Vidur. Thank you again.

**Vidur Gupta:** Thanks again, Richard. Enjoyed this.
