# Inside Notion

> 原链: https://colossus.com/article/inside-notion/  
> 来源: colossus.com · 归档自 EP.53 · 抓取于 2026-08-05  

---

**Today’s discourse is littered with obituaries:** Software is dying, legacy giants are dead, swaths of startups are going extinct. Stuck at the center of this wave of AI creation is a debate about which companies are “over.” And the consensus is that one type of company is deader than the rest: the pre-IPO, pre-AI startup that everyone used to love. If you’re not AI-native, the internet tells us, chances are you’re not going to make it.

Thinking it might make for an interesting follow-up to [*Inside Cursor*](https://colossus.com/article/inside-cursor/) (the ultimate AI-native company) in our Company Dispatch series, we started asking around about which companies might be proving the internet thesis wrong. One name came up more than any other: Notion.

We were intrigued. Each of us had our own prior relationship with the company and assumptions about what we’d find. Camille joined Notion at the start of 2019 to lead marketing when it was just 10 people in a room. Brie drafted an early version of its values as an off-and-on editorial consigliere. If we’re being honest, it seemed like a non-obvious contender for AI evolution.

Notion always felt like a company built more on ideology, brand, and community than technical edge. For those new to it, Notion is software that gives users blank pages they can customize with modular drag-and-drop “blocks”—paragraphs, headings, checklists, databases, images, etc.—into whatever they want. After five years of obscure toil, Notion first took off in 2018 as a beloved heir apparent to Evernote, and became the canonical product-led growth company, propelled by brand ambassadors, influencers, and fandoms across Facebook and Reddit. People from Buenos Aires to Hanoi to Dallas used it to plan weddings, do schoolwork, and track movies. Then, buoyed by the remote revolution of the pandemic, it gained steam as an enterprise knowledge and project management tool. Toyota, Pixar, and Nvidia became customers. By the end of 2021, it was a decacorn.

But during all this time, it didn’t necessarily seem like *serious* software to many. How high can the ceiling of “a note-taking app” really be? To some, it was just a prettier version of Google Docs and Sheets. So how, five years later, could Notion be the breakout of the pre-GPT companies to get to AI-first, first?

To investigate, we started hanging out at its San Francisco HQ, doing some (paid) [storytelling work](https://x.com/ivanhzhao/status/2038670159259619644) together, and talking to the cast of characters core to the AI transition. We wanted to see firsthand how this was all working. But then, all at once, it felt like the internet also caught onto something happening at this non-model, non-lab company. There’s been a velocity of [tweets](https://x.com/kelanoo/status/2034868212790177849?s=20) highlighting a perceived Notion [renaissance](https://x.com/DarlingtonDev/status/2032189733451767813?s=20). Ramp [spotlighted](https://x.com/Johnsjawn/status/2033248325185765410?ref_src=twsrc%5Etfw%7Ctwcamp%5Etweetembed%7Ctwterm%5E2033248325185765410%7Ctwgr%5E5fd74d11abc27af655be7392c46ff0060cd7d682%7Ctwcon%5Es1_&ref_url=https%3A%2F%2Fwww.notion.so%2FInside-Notion-v-next-327b3d04abd780a38645c28022159120) the company as the only top-10 vendor on its platform that wasn’t the typical “AI-native.” Notion made [a16z’s](https://a16z.com/100-gen-ai-apps-6/) [list](https://a16z.com/100-gen-ai-apps-6/) of the 10 most-used AI products in the world.

The tipping point seems to have been its recent Custom Agents launch. Notion’s early runs at AI let users prompt writing inside of pages and search across workspaces—nothing groundbreaking. This newest iteration lets teams command agents (in co-founder and CEO Ivan Zhao’s words, “infinite minds”) to do real work—turning the hoards of context that Notion has spent over a decade capturing for companies into plans, executing them, and Slacking updates once they’re done. The impact has been transformative for users and revenue, and changing minds in the peanut gallery. We’ve seen the metrics with our own eyes, and even the most jaded and revered developers are sitting up to take notice. But product and business growth weren’t what interested us most.

We wanted to understand the culture that turned the key on all this. For most companies, any history before 2022 feels like a liability. Notion’s pre-GenAI past, instead, feels like deep roots—a shared worldview that ensures a certain standard, even as the team sheds old rules, features, people, and ways of working.

Of course, the company hasn’t actually won yet. The threat of competitors, big and small, looms large. The audience for AI tooling is more fickle than ever. Internally, no chickens are being counted. And yet, by all accounts, this is the most alive and most true to itself the company has ever felt.

Here’s what we saw inside a decade-old company reborn to meet the AI revolution.

![](https://colossus.com/wp-content/uploads/2026/04/Smaller-Size-Larger-Type-800x320-1.jpg) 

## 

Ask any Notino<sup>[\[1\]](#ref-1)</sup> where it all started and they’ll say the same thing: Mexico. They’re referring to the October 2022 company retreat where co-founders Ivan Zhao and Simon Last locked themselves in a room for three days, and upon emerging, declared Notion an AI company. Before ChatGPT happened to the rest of us, they saw the writing on the wall and moved.

After hearing the Mexico story for the third time, we casually chided the engineer across from us that they all spoke about it like it was Moses descending from Mount Sinai to deliver the Ten Commandments. We expected a knowing eyeroll but instead were met with a, “Yeah, it was exactly like that!” Anyone who speaks about those days in Puerto Vallarta—those who were there and those who only heard about it second-hand—does so with a particular reverence. Like they’re reciting some ancient legend that their grandchildren’s grandchildren might hear one day.

When we reflect this observation back to Ivan and Simon, they confirm that the experience was akin to a spiritual awakening (and yes, they know how that sounds). “You can’t lie to yourself about whether it’s happened to you,” Ivan explains. No matter how much we pry, it’s impossible to suss out what actually went down in that room in Mexico.

As they tell it, Simon got early access to GPT-4 through a twist of fate: his neighbor worked at OpenAI and one day said, “Hey look at this.” He ran home to play with what it made possible inside Notion, and called Ivan. That’s the moment they decided to share their intention to go all-in on AI with the company; not once the vision was more fully baked, but immediately.

There’s a running joke at the company that Simon never wanted to be a manager but now manages the largest team of all: his own fleet of agents.


Returning to San Francisco from Mexico, they started building with AI in earnest—a full month before the launch of ChatGPT—and haven’t stopped. Since then, Simon’s been more prolific than ever.

There’s a running joke at the company that Simon never wanted to be a manager but now manages the largest team of all: his own fleet of agents. Ivan’s also coding more than he has in the last four years. (“I’m back!” he exclaimed to us, showing off his codebase.)

Despite running the company together all day, Ivan and Simon get a lot of their big ideas out over the phone, talking sometimes three hours on nights and weekends about the possibilities of AI (many, but not all related to Notion). Neither ever wants to hang up, and when they recount what these calls sound like, it’s reminiscent of teens with a crush. It’s all “can you believe we get to” and “we’re so lucky to be alive at this time” and “what if we” and “yes, and” into the wee hours.

“We’re totally AI-pilled and have been for years,” says Ivan, who’s really not one to talk in Gen Z memes. Longtime Notion investor Mike Vernal recalls: “They were talking about AI and taking it very seriously well before most companies.” It’s clear this energy came from the founders, not a board mandate or keeping up with the Joneses charade.

![](https://colossus.com/wp-content/uploads/2026/04/260324_colossus_notion_0562.png) 

You expect this kind of “feel the AGI” talk from the big labs or young people caught up in the moment, not necessarily from executives who’ve spent the last decade building enterprise software and hired an illustrator before a first salesperson.

To speculate a bit, Ivan and Simon were probably well-primed to be “AI-pilled.” Notion’s [mission](https://dev.notion.so/notion/Pictures-of-the-greatest-thinking-together-324b35e6e67f801f9bbad7ac9ae65f90?source=copy_link&utm_content=324b35e6-e67f-801f-9bba-d7ac9ae65f90&utm_campaign=T024JLF7A&pvs=6) has always been about giving ordinary people power over their computing environments, directly inspired by Alan Kay and Douglas Engelbart’s writings on how computers can augment human intellect and collaboration (not just automation). If this is your dream, you can see how Notion was meant to be an AI company the whole time. You no longer have to wrestle with the conventions of docs. So perhaps AI saved them (in both the practical and spiritual sense) by bringing Notion into closer alignment with their true ambitions.

Through the same lens, it became clear to us why these particular founders were ready to lead a company that needed to change.

## 

Ivan is an inveterate micromanager. “Hands in the mud,” is how he describes it. He edits tweets, polishes pixels on the website, sketches designs, pushes code, and still reviews 100% of offers going out for every role. (His big litmus test question: “Have you done something remarkable with no resources and no one asking you to?”) He’s persnickety about the details but never condescending. In his words, after we complimented him on a project:

![](https://colossus.com/wp-content/uploads/2026/04/Screenshot-2026-04-14-at-3.54.57-PM.png) 

Ivan’s often seen walking the halls, stopping to look over people’s shoulders and offer them thoughts on whatever’s on their screen. He only wants to work with the person making the thing, not their manager or their manager’s manager. Over the years, many Notion managers have objected to this way of working; they are, respectfully, no longer with the company. Everyone we spoke to had their own story of working with Ivan directly…that week.

While there is no prescribed “process” for how Ivan reviews work—no formalized product reviews or PRDs to have stamped—there is a shared understanding of how to build well in Ivan’s world.

The first step is to prototype. Whether it’s a product or a user event, a doc won’t cut it; Ivan demands something he can interact with and get a feel for.

There also better be lots and lots of revs to look at. Every Notino knows to create as many permutations as their brain can muster. (The new sidebar they just launched had 22 tester versions you could toggle on or off in Notion’s internal workspace.) This explicitly includes wrong, unreasonable versions in case there’s a glimmer of something usable—which according to every Notino we asked, there usually is.

The feedback you’ll get when working with Ivan doesn’t feel like a wrist slap from someone who makes you feel like you suck at your job like so many exec reviews do. What you will get, instead, is what the team calls “Ivanisms.” There’s even an entire session for new hires dedicated to these.

“Make it dumb” is a team favorite. As Ivan himself puts it, “The best interface is the one where people know how to use it before they know how to use it.” The others read like snippets of poetry: features should be “light like a piece of paper,” simply delightful “like Japanese wooden toys,” have obvious UX “like a Chinese buffet,” stay “on the Golden Path” and “keep the main thing the main thing.” Walk the halls at the office and you’ll see scattered Easter eggs enshrining these principles.

![](https://colossus.com/wp-content/uploads/2026/04/260324_colossus_notion_1239.png) 

Product marketer David Tibbitts, one of the original 10 Notinos and still at the company, remembers drafting hundreds of versions of a single tweet, and going back and forth until it felt “dashed off, like we didn’t try too hard.” Like a film director known for needing dozens of takes to get the human truth of a scene (stop acting, just be natural!), Ivan pushes for as many tries as it takes to get something right. When they finally get there, Ivan was all smiles: “Great process!” he said.

Ivan is not the only instigator of exacting feedback. Notinos do this with each other all the time about what they ship. Debates coming out of Studio (known elsewhere on design teams as Crit) or a new prototype in Dev overflow to Slack and then lunch, and they can get spicy. Threads in Slack can top out in the hundreds of messages.

Adopted Ivanisms abound. Lego have always been his analogy for how Notion should feel. You should be able to stack software blocks to make anything you want. Features that don’t hit this bar of malleability are “horsey pieces.” (Any kid who’s built a Western Lego set knows horses come as single-purpose solid pieces. They can only be horses.) “It’s actually become one of the most devastating things you can say,” an engineer tells us. “Sometimes you’ll see someone respond to a new feature with a 🐴 in Slack, and you’ll think…ooh, ouch.”

When we inquired about how you know when something’s ready to ship, a designer told us, “You know it when you see it,” before adding: “Well, that and Ivan’s blessing.”

![](https://colossus.com/wp-content/uploads/2026/04/260324_colossus_notion_1272.png) 

Over time, Notinos learn about all of Ivan’s not-so-subtle preferences. Everyone knows he hates the color green (“It’s okay for trees to be green, just not software,” Ivan assures us) because of that one time he asked that all house emojis in Slack get swapped from 🏡 to 🏠. It’s also why there are no plants in the office. Notinos tell us about how he used to surreptitiously replace people’s white charging cords with black ones; he only got busted when someone thought theirs had been stolen. It had just been “improved,” he said.

Sometimes you’ll see someone respond to a new feature with a 🐴 in Slack, and you’ll think…ooh, ouch.


To better understand Ivan, it helps to know where he comes from. Raised by his mom in Ürümqi in China’s Xinjiang region, he discovered coding through the International Olympiad in Informatics, which earned him entry to high school in Canada. At 16, he moved to Vancouver alone, learned English by watching SpongeBob SquarePants, and promptly fell in with a crowd of artist, filmmaker, and fashion designer friends he credits with sharpening his eye for craft. He took up photography and Chinese watercolor, majored in cognitive science, and only started coding to help friends build apps and websites. All of this gave him conviction that good taste comes from being a voracious student of many domains at once, and that core belief is contagious.

![](https://colossus.com/wp-content/uploads/2026/04/image-5.png) 

Young Ivan learning to code.

We’re not surprised when Notinos tell us they’ve gotten more stylish since working here. Or how many say they meticulously planned their interview outfits. One bought new glasses to “look like an architect.” Another panicked over wearing pink given Ivan’s monochrome. The thing is, he does notice. Especially shoes and materials. It’ll never determine a hiring decision of course, but he notices. In one of Brie’s earliest encounters with him, she removed her shoes at the door. “Wrong feet,” he immediately pointed out, noticing that the left and right sock were swapped.

You can see how he’s attracted tech’s true craftspeople, and why Notion has been able to recruit otherwise ungettable talent. Many people decide to work at Notion, in large part, to get exposure to Ivan and his ability to see things most people can’t about software, the world, and other humans. To work at Notion is the chance to see it, too.

## 

Walk into an All Hands and you’ll hear, “We’re not safe.” Anthropic and OpenAI could be working on something that eats their lunch and dinner any day now. There’s no letting up. Even as Notion’s revenue charts soar upward and dozens of new things ship, there’s an air of desperation that the company must not miss this shot right now.

You see it in the pace of everything. In March alone, there were 15 new releases—any one of them would have been a headliner a year ago. Now it’s just another Thursday, says a product marketer, who just wrote the longest update email in company history. Everyone is “ON” to make this happen—we clocked most Slack response times under five minutes. New iterations come through within the hour. The most technically ambitious projects get swarmed with takers.

While most companies finding themselves at “war” cling to pre-war plans, this team is all too ready to throw things away and start again if it gets them closer to AI-native. In the New York office right now, there’s a tiger team on what everyone calls “Project Applecart”—because it might just upset everything. New codebase, full rewrite of the product from scratch for the agent era, no attachment to what came before, no hemming and hawing or preciousness about how it used to be or tiptoeing around feelings. Notion needs to be evolving its codebase at agentic scale, not human scale.

This is just one teardown of many we hear about. The biggest, and most meaningful, is related to the team. When AI became the core focus, there was an exodus, including tenured and senior folks previously thought to be mission critical. But there was no campaign mounted to save them. As Ivan told us, the people who stayed were the right people. “It was actually so much better after that,” one young engineer told us, only half joking.

![](https://colossus.com/wp-content/uploads/2026/04/260324_colossus_notion_0810.png) 

In another example, one of the first AI products they built, smart Q&A with your Notion workspace, was on the brink of ship. After six weeks of work, 10 days from launch, Simon called a do-over. He’d gotten an emergency ping from OpenAI—the planned product would exceed their entire serving capacity. They needed to rebuild with totally different API infrastructure to save it.

“So yeah, we privately panicked,” says engineer Abhishek Modi. “But like, we never considered the alternative or even delaying it.” It was a dead sprint. Prompts at the time were fragile, needed a ton of examples to calibrate, and often got it wrong (sometimes wrong in a completely different language). Still, they pulled it off. And since then, Modi says, every rewrite has become a little less painful. The muscle memory of starting over so many times has made everyone faster, not more cautious.

“Get it just about perfect, then throw it in the trash,” says Modi, with a wide grin and no hint of nihilism. “Simon has thrown away everything he’s ever built.” They say it with so much respect, it’s like there’s some kind of prize for discards. It’s not uncommon for teams to find a 30,000-line PR on Monday morning when Simon turns his attention to something not working quite right.

“Simon got the entire eng team to rebuild our agent harness twice,” a Notino told us. “Soon to be three times,” she added, after a beat.

“You just have to hang onto the ideals of how things should work and feel, and let the rest go,” says another engineer core to Notion’s early AI work. A big chunk of 2024 was spent building something called Notion Assistant that flopped, he tells us. But it ended up supplying the load-bearing infrastructure for agents. “Looking back, it was actually quite critical we did that one poorly,” Modi says.

Get it just about perfect, then throw it in the trash.

—Abhishek Modi

Something about it all reminds Camille of the 2022 GTM kickoff where Ivan showed a video he’d stumbled across on YouTube—one of those animated School of Life shorts that looks like it’s from 1970s PBS. The topic was eudaimonia: the Greek word for the sense of fulfillment that comes from suffering toward a worthy goal. Between the word PAIN raining down in blood onto contorted, striving figures and the [strange claymation](https://www.youtube.com/watch?v=GocIobQ9MLs) of it all, it wasn’t the rallying cry you’d see at any sales kickoff. Zoom comments flooded in. There was debate over whether the coffee crew should sign an NDA. But the real ones couldn’t stop smiling because there was something so true about it at Notion. The folks who are still here today remember it fondly.

![](https://colossus.com/wp-content/uploads/2026/04/DigitalMagazine_NotionDispatch_Colossus_x2.1-scaled.jpg) 

Wartime at most companies is scarring. People stop saying hard things and start saying mean things. Everyone starts to white-knuckle their fiefdoms. The more tired everyone gets, the more politics there are. This is not what we observed at Notion. People say things directly. Harsh comments are for expedience, not personal indictments. No one felt their access to executives was being gatekept, or that their boss was patrolling the way they talked to colleagues.

There’s no better example of this org-wide “live and let live” trust than the private ICs (individual contributors)-only Slack channel. No managers allowed. HR is present only as ICs themselves, not spies. Topics can be playful—team photos, planning one of the many parties people host—but they can also get spicy: teardowns of new policies, how an exec handled an All Hands question. We shared this with some other leader friends, who just said “nightmare,” and “never.”

In another example of radical openness, when co-founder Akshay Kothari took the CPO mantle, one of the new grad whippersnappers sent him a letter listing all the things the team was doing wrong. It wasn’t a private Slack but a full public letter. We were prepared for a “kids today” sigh, but instead Akshay says, “It was one of the most useful things anyone’s ever sent me. He saw so many things I couldn’t.”

With a heavy dose of self-awareness, people make fun of “wartime,” too—which in turn makes the seriousness of the matter more sustainable for many. “Sometimes I’ll just tell Ivan, ‘I’m so tired, I don’t want to celebrate wartime with you today,’” says people chief of staff Ayomi.

This tipped us off to the other big dynamic keeping Notion sharp and speedy. It’s hard to explain unless you’ve been in the room, but even “at war,” everyone seems to be…playing.

No one embodies this more than Simon, who, while responsible for the largest paradigm shifts in the product, is mostly just having a great time. “Simon is constantly solving problems for everyone else, but it’ll always be in these terms of, ‘I was just trying this thing and this happened,’ or ‘this thing failed and it was awesome,'” says a member of the engineering team. “He would never say this, but we’re all looking at him as a way to be obsessed and having fun.”

Sometimes I’ll just tell Ivan, ‘I’m so tired, I don’t want to celebrate wartime with you today.’

—Ayomi Samaraweera

Once we spotted him loitering around the engineering desks, which stood out because it’s odd not to see him with his fingers attached to his keyboard. When we asked what he was doing he said, “making sure no one’s coding.” It took us a beat, but we realized he meant coding manually—as in, not with an agent.

Multiple people tell us he’s living six months in the future, constantly bantering with his 10+ simultaneous agents, hooked on surprising himself with what’s possible on the edge. He brings discoveries back to the team with the “oh my god look at this!” energy of a time traveler who’s found gold. He’s the ultimate role model for hard technical work and play being the same thing.

Ivan’s playing a lot more, too. To welcome the team back from holiday “break” this year, he took the mic at All Hands, and shared photos from his vacation. There he was in Mexico, with his wife Yasmin, on the beach, ocean waves, Corona in hand—laptop open. They’d built a historical venture game together (graphics reminiscent of Carmen San Diego and all), speaking prompts into their respective microphones, giggling as it all worked so well.

![](https://colossus.com/wp-content/uploads/2026/04/Ivan-game-scaled.png) 

The crowd cheered as if at a concert, and the message landed exactly as he intended: imagine what you can do when building feels like this.

## 

As one tenured Notino remarked, “Early on, Ivan used to talk about how working at Notion is like playing jazz. Well, now it’s *really* jazz.”

It’s the kind of axiom you’d expect to see in an X article, but which surely couldn’t survive contact with reality. It’s hard to imagine how an over 1,000-person company operating across six global offices could run a cohesive product or organization with everyone improvising all day long. But as one recent [tweeter](https://x.com/martini_bn/status/2034018151566807238) remarked, “I never had a subscription which increases in value like…day by day.”

We got to experience the Notion jazz for ourselves working on Notion’s [Think Together video](https://x.com/ivanhzhao/status/2038670159259619644). The whole thing came together in under two weeks. A small handful of us were jamming on the things that make Notion special and someone, in passing, said the line: “think together.” The phrase sparked something for Ivan, undoubtedly related to the fact that he has been reading and talking a lot about Steve Job’s comeback with Apple in the ’90s, which included Apple’s iconic “Think Different” campaign. He suggested we keep playing with the idea. “We can find examples of the greatest teams/collectives in history and feature them. Like an homage to humanity.” No destination, just exploring something that resonated with him. Everyone joined in without asking why.

We started sharing names of teams we admire in the thread. Many  reactions piled on. Someone replied that they were getting emotional just seeing them all listed in one place. We knew we were onto something. Ivan said we should make a video and get it out by next week. A team snapped into action. This did not have the feeling of a “fire drill” but instead the good jitters of something new brewing.


AI isn’t a must do. It’s simply the cool new fun way to work around Notion.


There was no project brief, no meetings added to calendars, no declarations of DRIs, no stated goals for launch, no trackers. We felt like we were in that classic scene from *Stand By Me* in which the kids are walking along the train tracks, balancing on the rails, tossing a baseball back and forth, and every few minutes another friend jogs up from somewhere to join the growing pack, not a single word exchanged.

A group of us got together on Saturday morning on Zoom to keep things moving. People were in their living rooms, offices, or dialing in from roadtrips. Kids were walking across the screen and partners were delivering coffee and snacks to desks, waving to the camera.

As we got close to a final version, Ivan looped in another Notino to usher the video through launch who used a Custom Agent to build a run of show to take us through the day. The video posted, and just as soon as it hit the timeline, dozens of Notinos reshared with what the message meant to them. Ivan thanked the team warmly, everyone exchanged some high-fives on Slack, then got back to the thing they were working on before this project dropped out of the sky. It now has millions of views.

![](https://colossus.com/wp-content/uploads/2026/04/260324_colossus_notion_1037.png) 

This isn’t a thing that happened one wild time at Notion. It’s how most things happen most of the time, especially on EPD.

When asked about a centralized plan for what to build, Simon asks, “What’s the point? Everything’s changing all the time anyway.” Instead, Notinos tell us an idea could come from leadership, emerge from a whiteboard session, a customer email, a tweet, etc. It could start with widespread enthusiasm, a few flickers of excitement, or deep-seated dissatisfaction. A dozen people might wrap their arms around something for months or a skeleton crew of two or three might take on a new feature over the course of a few days.

We did eventually find our way to a document titled “2026 Roadmap,” but it did not contain the list of things to ship we expected. Instead, it simply said: *The thing to do is to be undeterred by trivial things, have conviction in our world view, and simultaneously be nimble enough to react to important changes around us.*

When we ask head of product Max Schoening about it, he genuinely seems unconcerned with the typical benefits of planning, roles, or org charts. After an extended conversation with him on the topic, we feel like total squares for thinking teams as talent-dense and trusting as Notion’s might need more than a few bullet-pointed goals to get to great work. Still, we had some questions, including several crowdsourced from jazz-curious friends:

**Duplicated efforts?** No problem. “We learn different things from different approaches.”

**Resolving dependencies?** No need. A team isn’t a team in Notion’s current definition unless it can own its work end-to-end. Identify a gap and someone’s always in the wings ready to fill it, even if that means things are happening late in the evening or over a weekend.

**Lack of ownership?** No sweat, everyone is supremely high-agency by default. If they’re not, they don’t usually make it in the door. And if for any reason they do, their tenure is likely to be short-lived.

**Wasting time on bad ideas?** No such thing when AI makes experimentation so efficient. Someone suggested in Slack, “What if we build a SKU that only agents can buy?” Max replied on the thread “Let’s try it! 🌱” and later tells us he thought it sounded like a terrible idea (and he’s a guy who loves terrible ideas). Despite the verboten color, Max is a big fan of the 🌱 emoji. He doesn’t want to squash ideas too early.

**Not taking on the most important or sufficiently ambitious or long-term ideas?** “If an idea is actually good, it’ll get worked on,” Max says assuredly. There are Notinos known for their taste in what to build next, and when they suggest an idea many people will naturally glom on. (Ivan and Simon are among them, but are by no means the only ones.) This was the case for features like meeting notes.

Some things are a slower burn. It took a while for Custom Agents to catch on. But as the prototypes started getting better, more and more people wanted to work on it. The mobile AI app was another such example. “It was totally organ-rejected for years,” a longtime Notino told us. But then, a new designer/engineer picked the project back up and, according to one initially skeptical Notino, “wrote the perfect one-pager.” Here’s a comment in the doc from another tenured engineer:

![](https://colossus.com/wp-content/uploads/2026/04/engineer-message.png) 

**People slipping through the cracks or not performing up to expectations?** This is the area where managers, geared less towards performance management than to helping people do their best work, can be quite useful. The best managers at Notion seem to have a really nuanced pulse on their people, asking things like, “I didn’t see as much progress as I expected last week. Anything in your way?” or “I saw murmurs of new integrations, which seems right up your alley in case you want to talk with the team about getting involved.” All welcome input from folks who are generally self-motivated to build.

The thing to do is to be undeterred by trivial things, have conviction in our world view, and simultaneously be nimble enough to react to important changes around us.


We got the sense that no one is expecting or waiting for anyone to stumble, a typical hallmark of high-performance cultures. As one engineer put it, “We’re always trying to say yes to each other.” “Even legal!” the Notino sitting next to her chimed in.

As you might imagine, the go-to-market team runs a bit differently. If the product and engineering side of the house wants to play jazz, sales and marketing want to be an F1 pit crew. They need to be a well-oiled machine to absorb the unpredictability of new features, while maintaining polished consistency with customers (and all the collateral and timelines that come with that). Head of global sales Pravesh Mistry describes the journey as “going from winning ugly to winning pretty.” Sales used to be a bit of a free-for-all. Now there’s a clear way to win.

It sounds a bit bro-y relative to the rest of Notion’s culture, but when they’re facing a major opportunity, salespeople will turn to each other and say “F1 ready?” “F1 ready.”

![](https://colossus.com/wp-content/uploads/2026/02/Cognition-ad-v2-scaled.png) 

Everything we observe reminds us that Notinos are capital-N Nice in a way that makes it easy to underestimate them. But watching them work up close gives a different impression.

As we were writing this, we kept referring to Notinos as the happy pointy people—whistling while they work, but piercingly intense. People join for this exact combo. You may have to work late nights and weekends, but you don’t have to worry about sharp elbows or hints of sociopathy.

It also helps that most people around you seem lit from within about the potential for AI at Notion, even if they’re on the fence about how it should show up.

## **ring people along with carrots, not sticks**

When we asked other companies how they’ve AI-pilled their teams, we heard: add AI use to OKRs, ding people on performance reviews for under-use, make leaderboards to expose low adopters, fire anyone who can’t keep up. We heard tales of one company’s surprise “AI-cation,” a day “off” to build something with AI. “My company spends $300 a day on tokens so I can game perf,” someone at a top startup told us—then “tokenmaxxing” started trending on X.

Notion doesn’t do any of this. That’s because the goal isn’t to get people to use AI for its own sake, but to help them find an authentic enthusiasm for it by creating the environment to help the unconverted see the light for themselves. *AI isn’t a must do. It’s simply the cool new fun way to work around Notion.*

As part of this, Simon’s work has become a lot more visible over the last couple years. Historically, he did his tinkering alone in a corner, most of it never to be seen. Now his work is center stage at the company—at All Hands, on Slack, the subject of lunch debates and discussions. Beyond helping define strategy and what’s next, he writes a ton of software himself—and he loves to share it around.

![](https://colossus.com/wp-content/uploads/2026/04/260324_colossus_notion_0630.png) 

Simon’s work is genuinely revered at the company, especially on the engineering team. “He had a single agent thread working for 15 days!” one Notino exclaimed as if he had just watched a skateboarder land a hardflip. “He’s the kind of engineer you want to be some day, but know you probably won’t be,” another remarks. It’s not uncommon for Notinos to go into full inspection mode on Simon’s work, thirsty for insight into how it all happened under the hood so that they can learn and try their own version of it. Simon warmly invites the inquiry. He’s been seen at the whiteboard coaching Notion’s team of “model whisperers” (described as “closer to philosophers than engineers”).

And for those who may not be as motivated by what’s on the cutting edge of AI where Simon lives, Notion’s culture of prototyping, dogfooding, and feedback often does the trick for the rest of the team. The company lives and works in Notion Dev—the employee-only test environment— all day long where variously baked AI features abound for real-time testing, especially since Custom Agents debuted. It’s become almost impossible not to get hooked.

Notion has over 1,000 employees and over 700 agents, all doing different tasks. During onboarding, for example, it’s suggested that you refer questions to Nosey, the company Q&A bot instead of your manager. “People doubt they’ll get useful answers, especially for things they assume require tacit knowledge, but Nosey is surprisingly good,” a new Notino tells us. “Smiler” agents rush to help with facility requests, from charging cords to blankets if it’s chilly. Task collector agents consolidate to-dos across pages, meetings, Slacks, so nothing gets forgotten. The more people experience AI doing the unexpected (even if it’s simple), the more they want to use it, the more curious they get about what else it can do, and the cycle continues.

![](https://colossus.com/wp-content/uploads/2026/04/Browse-Agents-scaled.png) 

People are constantly posting AI humble brags in #AI-wins on Slack. Everyone is there, and it’s a steady river of unfettered enthusiasm. Cool customer use cases, new fun agents, how they sped up a project 10x, or planned a family vacation. Ivan and Simon are quick to chime in with follow-up questions and new ideas. Quirky shares get just as much love as “real work.”

Some recent examples include “Calendar x Custom Agent helping me play calendar Tetris,” “Created a daily kanji quiz in Notion using Workers, Claude Code & Custom Agent,” “A Custom Agent that can order groceries on Instacart.”

Much of this comes out of the “Prototype Playground,” a code repository with all the product’s primitives, accessible to every team, and the launchpad for many user-facing features. There’s an ongoing friendly competition across all teams as to who can build the most helpful agents. The user research team decided to take this quite seriously once, stunning everyone with a second-place “win,” clad in custom team sweatshirts, game faces on. That’s the energy.

Even with all the carrots in place, “everyone’s on their own timeline with AI,” Ivan reminds us. He’s generally in a hurry with everything, but in this respect has been more patient.

Senior product leader Marina Camim is the prime example. She was out on Notion AI at first—it felt like a distraction. “Skeptic? No! I was a vocal dissenter,” she says, describing early efforts as “obvious bolt-ons” that “objectively didn’t drive much value.” She dogfooded what landed on Dev but couldn’t get excited. Then she got her hands on an early prototype of Custom Agents. “I was obsessed,” she says with a twinkle of mania. It was something about making programming agents easy for everyone, the dopamine of it working. Around the office, she’s now called the “bot queen” and became [one of the faces](https://www.linkedin.com/posts/notionhq_welcome-to-notion-on-notion-before-we-shipped-activity-7432155050501898240-kUjd?utm_source=share&utm_medium=member_desktop&rcm=ACoAAArg2XoBH8A4tyhUHKAOLAlYi-kpxg9zjBQ) of the product’s launch.

![](https://colossus.com/wp-content/uploads/2026/04/260324_colossus_notion_0814.png) 

The team is clear that product skeptics and non-users are still welcome, something that candidates would get dinged for in the interview process at most companies. “We don’t punish skepticism,” an engineer explains. “We punish pessimism.”

One product designer tells us she’d never used Notion before joining. She sat in one meeting about a potential product, went home that night and built it. Nobody asked her to and nobody stopped her. The day it went live, she was dogpiled with love.

AI tech lead Sarah Sachs made failure part of her job. She told Ivan in her interview that no one appreciated the role of failure in experiments. The only way to make something great is to max it out, not avoid it, she said. “Isn’t that just what it is to build AI?” he replied, and she knew he got it. Others warned her Notion “wasn’t a real AI company.” She knew differently.

Now she’s known (half jokingly) as the Anna Wintour of AI models—ruthlessly deciding which one should handle which task, the way a fashion editor influences the runway. Curious how Notion launches new models in-product so fast? They make sure Sarah has early access.

She sat in one meeting about a potential product, went home that night and built it. Nobody asked her to and nobody stopped her.


Perhaps most telling is Max Schoening, whose product leadership was nearly impossible to find given the required Ivan mind-meld. “Before I got here, my general theory was you could run anything with just iMessage and Apple Notes.” Now he’s all in on Custom Agents.

As warm and fuzzy as this all seems, you can still tell—from the speed at which everyone is moving to the animated Slack debates and the hyper-vigilance to customer feedback—that everyone is also under tremendous pressure.

We suspect it comes from the question hanging in the air across offices—how is all this transformation meeting the market?

![](https://colossus.com/wp-content/uploads/2026/03/Vanta_Calm-pliance_Newsletter_Ads_Beach_800x320.png) 

## 

The first couple years of AI implementation was no big whoop for revenue. A ton of work with no promise of changing the company’s trajectory. “It was kind of a swamp of despair,” says Akshay, who’d always played a role keeping go-to-market energized. Even Ivan, the true believer, was getting worried.

No one at Notion ever says it like this, but it’s clear they aspire to be in the big leagues—not in the standard <$20bn kiddie pool of the pre-AI set. They want their shot at the >$100bn seas. All of this depends squarely on Notion becoming mainstream for enterprises, and nailing AI implementation feels like their only ticket.

Last summer they saw their first little uptick, traceable to two things: Pravesh getting fully spun up as head of sales, and enough AI features finally starting to feel valuable for teams (Meeting Notes’ launch on May 13 tipped it over the edge). Since then, that slope has only gotten steeper, but not without some uncomfortable changes.

I don’t want anyone to ever say wiki or note-taking to me again. That’s not what we do. I don’t want to hear it.

–Akshay Kothari

They’ve needed to rethink not just how they sell but who they’re selling to. Last year, the executive team took a retreat to sharpen their ideal customer profile more than ever. In one session, Pravesh drew a big circle representing a new customer definition. The top of the class: companies already relatively savvy, or at least ready for AI. Enterprise was the bullseye of this target, then mid-market, then SMB. But he knew this wasn’t narrow enough to give his sales corps the solid direction they needed to storm the market. “I walked up and drew this triangle from the middle out containing only the engineers, product, and design people—we called it the wedge,” he says.

The wedge, he argued, had to get Notion’s full focus. EPD has always been the early adopting tastemaker with the biggest budgets. It would open up faster, more natural expansion. But after years of pushing ubiquity—that Notion should be a tool for all teams—it felt small. Like it’d leave a lot on the table. They decided to make a run at it anyway. “EPD is aspirational for every other function inside companies now,” one of the top salespeople told us, relaying Pravesh’s messaging. “No EPD leader picks a product because it worked for HR—only the reverse is true.”

The team has been ruthless about disqualifying customers outside of the wedge. And it’s working. Close rates jumped. Deal sizes have increased across all segments. Time-to-close is down. Revenue is accelerating faster than it ever has. And sales is driving a whole lot more of Notion’s revenue pie—once unthinkable at the world’s poster child for product-led growth.

![](https://colossus.com/wp-content/uploads/2026/03/800x320-1.png) 

Two other bets poured fuel on the fire. First came the then-controversial idea to sell AI with unlimited subscription pricing—$10 a month, no credits, no metering. The belief was that users needed freedom to test without a scarcity mindset holding them back. It was expensive for the company, but it threw growth into a new gear.

Then there was the full re-architect of the Notion pitch. “We were still talking about AI as knowledge management!” Akshay exclaims to us, in disbelief it went on so long. “I don’t want anyone to ever say wiki or note-taking to me again. That’s not what we do. I don’t want to hear it.” They needed a way to get the new Notion and the value of its fleets of agents to click with people, immediately.

“It all had to be re-centered on the ‘aha moment’ for people,” says one rising star on sales. “Customers don’t want a box of Lego to build themselves. They want you to build them the damn castle.” Spend no time on the ethereal benefits of collaboration. Get prospects who already know they need AI to see what Notion agents can do for their actual workflows.

We came across this doc about the new Notion pitch: “When you show agents, automations, integrations, the executives you’re talking to just hear elevator music in their heads. What they want is to see a solution to accelerate their AI team (our IT Helpdesk agent), their sales team (Sales Buddy agent), and their product managers (the Scrum Master 2000).” Each bot was built by someone on the sales team, likely on the fly during a live demo. Just like the EPD side of Notion needs to be able to build without a plan, its sales team also needs to be able, at a moment’s notice, to build all the castles needed for customers to see the light.

As we wrote this, sales just had its first kickoff since all these changes took shape, and everyone was hyped to have so much direction. The energy in the Miami convention hall, we heard, reached Tony Robbins’ heights of hysteria. “Everyone is so ready to explode this year!” Pravesh tells us, already hoarse after day one.

The data shows the strategy working. But across all the conversations we had for this dispatch, we detected a ribbon of something else: dissonance regarding what all this winning could mean for the entire Notion audience.

Everyone knows enterprise is the way to unlock the next level, but hundreds of employees and millions of users still see and love Notion as a tool for individuals who shouldn’t be left behind: the productivity wonks, students, recipe trackers, book listers, bullet journalers, and small business owners who liked it the way it was, and don’t want to hear about agents at all.

“Most of the world isn’t ready to adopt AI,” says one Notino committed to serving this audience and, as they put it, “defending Notion’s soul.” It should still feel like a place for them. If there’s a third rail at Notion, this is it.

![](https://colossus.com/wp-content/uploads/2026/04/260324_colossus_notion_1140.png) 

AI has only turned up the voltage. Now leadership is talking about an even newer distinction: the top of the class—customers already AI savvy enough to adopt right away—and the “rising class” of everyone else who will hopefully catch up in time. Continued speed demands going only after customers ready to move now, hardliners say.

We don’t envy the folks navigating this. Dropbox famously alienated its community long-tail with an abrupt shift to Dropbox for Business, eventually signing its death warrant. But then you look at Slack that failed to win enterprise fast enough, got trounced by Microsoft Teams, and had to seek safe harbor.

The conditions that made Notion’s shift possible weren’t easily repeatable tactics. They were qualities, most cultivated over years, that happened to become load-bearing when AI arrived.


You can feel the founders, and the rest of the company too, trying to thread the needle. In one presentation, you’ll see reference to “top of the class,” but in another “the Fortune 5 million” (one of Ivan’s favorite phrases for the masses that stand to benefit from Notion), and “no business left behind.” Missionary vs. mercenary is too tidy a framework to capture it. There’s a real sense of mission across both camps, but many Notinos feel deeply connected to serving the broader world outside the AI bubble and worry it’s going to get scrapped.

The tension was perfectly captured at an All Hands the other day. New sales messaging was met with a flurry of s and 👏s. But the most upvoted audience question at the end was: “How do you think this will land with our broader community who may be more skeptical of AI?” Also receiving its own snaps of support.


It’s the one question at Notion that doesn’t have an Ivanism for it yet. The bet is that a product built for the bleeding edge will eventually become simple enough for everyone—that the Fortune 5 Million will arrive at AI on their own timeline, and Notion will be ready. Whether that’s vision or rationalization depends on who you ask.

## 

For now, Notion is heads-down on what it can control. Not a plan or destination, or even its own product—only the way of working that’s allowed them to emerge from the chaos still ahead of the pack. They know everything stems from that, and that it must be continually refined, protected, and—much like the new codebase rewriting the product from scratch (nicknamed Notion Next)—reinvented when needed.

Initially, we hoped this piece might be a framework for other companies to use in their own AI transitions. But we realized that would be the horsey-piece version of an ending. The conditions that made Notion’s shift possible weren’t easily repeatable tactics. They were qualities, most cultivated over years, that happened to become load-bearing when AI arrived.

Founders who felt religious conviction in their bones and had the credibility to inspire it in others. An identity so strong and specific that it could absorb enormous change without losing coherence. A product capable of turning a decade of data and context into a competitive strength. A default to throw away finished work, not as a painful exception, but as a practice to get better. A culture of trust deep enough that a vocal dissenter could become the face of the launch. Organization-wide respect for people’s personal approach to AI, even inside 24-7 “wartime” urgency.

None of these are things you implement on a Monday. And maybe that’s the uncomfortable truth for many companies trying to make the same leap. The pre-AI player best positioned to survive this shift is the one with a mission much bigger than what they could build before, and a constant readiness to sprint toward it once it’s possible.

Whether the models shift in a direction that undermines what they’ve built, whether the Fortune 5 Million ever arrives, whether jazz can really scale to the next thousand people—in other words, whether Notion wins from here—is unknowable. But as we watch people argue passionately about a sidebar, program joke-telling agents, and build automation “castles” for customers, it feels less like a company pivoting, and more like a group of people relieved to finally have the right tools to build the thing they already believed in.

[Presented by](https://rogo.ai/)

![Rogo](https://colossus.com/wp-content/uploads/2025/09/rogo.png)
