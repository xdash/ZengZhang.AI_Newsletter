# Apple Retreats

> 原链: https://stratechery.com/2025/apple-retreats/  
> 来源: stratechery.com · 归档自 EP.11 · 抓取于 2026-08-06  

---

If WWDC’s opening video — which cast Apple executives as characters in the upcoming F1 movie, with Senior Vice President of Software Engineering Craig Federighi in the starring role — was a bit of a fever dream, then the opening of Federighi’s presentation of Apple’s annual software updates had the air of a regretful admission the morning after that mistakes had been made.

To Federighi and Apple’s credit, there was no attempt to dance around the fact that last year’s WWDC ended up being a fever dream in its own right: Apple promised a litany of AI-enabled features, particularly for Siri, that have not shipped and may never ship. Federighi, after listing the basic and hardly ground-breaking Apple Intelligence features that did ship, admitted right up front:

As we’ve shared, we’re continuing our work to deliver the features that make Siri even more personal. This work needed more time to reach our high quality bar, and we look forward to sharing more about it in the coming year.

That’s only two sentences, of course, but the admission was notable and necessary; last year’s WWDC — which garnered high praise, including from yours truly — revealed that Something Is Rotten in the State of Cupertino. That was the title of John Gruber’s Daring Fireball article excoriating Apple for promising something it could not deliver:

Even with everything Apple overpromised (if not outright lied about) at the WWDC keynote, the initial takeaway from WWDC from the news media was wrongly focused on their partnership with OpenAI. The conventional wisdom coming out of the keynote was that Apple had just announced something called “Apple Intelligence” but it was powered by ChatGPT, when in fact, the story Apple told was that they — Apple — had built an entire system called Apple Intelligence, entirely powered by Apple’s own AI technology, and that it spanned from on-device execution all the way to a new Private Cloud Compute infrastructure they not only owned but are powering with their own custom-designed server hardware based on Apple Silicon chips. And that on top of all that, as a proverbial cherry on top, Apple also was adding an optional integration layer with ChatGPT.

So, yes, given that the news media gave credit for Apple’s own actual announced achievements to OpenAI, Apple surely would have been given even less credit had they not announced the “more personalized Siri” features. It’s easy to imagine someone in the executive ranks arguing “We need to show something that only Apple can do.” But it turns out they announced something Apple couldn’t do. And now they look so out of their depth, so in over their heads, that not only are they years behind the state-of-the-art in AI, but they don’t even know what they can ship or when. Their headline features from nine months ago not only haven’t shipped but still haven’t even been demonstrated, which I, for one, now presume means they can’t be demonstrated because they don’t work.

Gruber — my co-host on Dithering — has been writing and podcasting about Apple for over two decades; his podcast is called The Talk Show, and for the last ten years Apple executives have appeared for a live version of his show the week of WWDC. However, this year will be different; Gruber announced on Daring Fireball:1

Ever since I started doing these live shows from WWDC, I’ve kept the guest(s) secret, until showtime. I’m still doing that this year. But in recent years the guests have seemed a bit predictable: senior executives from Apple. This year I again extended my usual invitation to Apple, but, for the first time since 2015, they declined.

I think this will make for a fascinating show, but I want to set everyone’s expectations accordingly. I’m invigorated by this. See you at the show, I hope.

Neither Gruber nor (obviously) Apple said why the invitation was declined, but it was hard to not draw a line to Gruber’s viral article; Marco Arment said Apple was Retreating to Safety:

Maybe Apple has good reasons. Maybe not. We’ll see what their WWDC PR strategy looks like in a couple of weeks.

In the absence of any other information, it’s easy to assume that Apple no longer wants its executives to be interviewed in a human, unscripted, unedited context that may contain hard questions, and that Apple no longer feels it necessary to show their appreciation to our community and developers in this way.

I hope that’s either not the case, or it doesn’t stay the case for long.

This will be the first WWDC I’m not attending since 2009 (excluding the remote 2020 one, of course). Given my realizations about my relationship with Apple and how they view developers, I’ve decided that it’s best for me to take a break this year, gain some perspective, and decide what my future relationship should look like.

Maybe Apple’s leaders are doing that, too.

My biggest takeaway from WWDC is that Arment got it right: Apple is indeed “Retreating to Safety”. Retreating might, however, be exactly the right thing to do.

Apple’s Retreat to Its Core Competency

The headline feature of WWDC this year was Liquid Glass, a new unified design language that stretches across its operating systems. I will reserve judgment on Liquid Glass’s aesthetics and usability — Gruber likes it, but I am not one to install developer betas on my devices — but will make three meta observations.

First, hand-crafted UI overhauls are the polar opposite of the probabilistic world of generative AI. One is about deep consideration and iteration resulting in a finished product; the other is about in-the-moment token prediction resulting in an output that is ephemeral and disposable. Both are important and creative, but the downsides of that creativity — unfamiliarity and edge cases versus hallucination and false confidence — are themselves diametrically opposed.

Apple’s historical strengths have always been rooted in designing for finality; in my first year of Stratechery I did a SWOT analysis of the big tech companies and said about Apple:

Apple’s product development process is wonderful for developing finished products, but that same process doesn’t work nearly as well when it comes to building cloud services. Cloud services are never “done”; they are best developed by starting with a minimum viable product and then iterating based on usage. This is precisely opposite of what it takes to design a piece of hardware, and it’s a big reason why Apple struggles so much with cloud services (and why other services companies struggle with products). The canonical example of this, of course, was the MobileMe launch, which was delivered fully-formed and which, when faced with real world usage, crashed-and-burned. Apple’s latest offerings are better, but still suffer from too much internal development time per release. This is a hard problem to fix, because it touches the core of what makes Apple Apple.

I think it matters whether or not Liquid Glass is good, because it will be a testament about the state of Apple’s strengths; the point for this Article, however, is that WWDC was a retreat to those strengths, away from a technology that is very much inline with Apple’s historical weaknesses.2

Second, the core premise of the Liquid Glass re-design is leveraging Apple’s integration of hardware and software. This is how Vice President of Human Interface Design Alan Dye introduced Apple’s new design language:

Now with the powerful advances in our hardware, silicon, and graphics technologies, we have the opportunity to lay the foundation for the next chapter of our software. Today, we’re excited to announce our broadest design update ever. Our goal is a beautiful new design that brings joy and delight to every user experience, one that’s more personal and puts greater focus on your content. All while still feeling instantly familiar. And for the first time, we’re introducing a universal design across our platforms. This unified design language creates a more harmonious experience as he move between products, while maintaining the qualities that make each unique. Inspired by the physicality and richness of visionOS, we challenged ourselves to make make something purely digital, feel natural and alive, from how it looks to how it feels as it dynamically responds to touch.

To achieve this, we began by rethinking the fundamental elements that make up our software, and it starts with an entirely new expressive material we call Liquid Glass. With the optical qualities of glass, and a fluidity that only Apple can achieve, it transforms depending on your content, or even your context, and brings more clarity to navigation and controls. It beautifully refracts light, and dynamically reacts to your movement with specular highlights. This material brings a new level of vitality to every aspect of your experience, from the smallest elements you interact with, to larger ones, it responds in real time to your content, and your input, creating a more lively experience that we think you’ll find truly delightful. Elements once considered for rectangular displays have been redesigned to fit perfectly concentric with the rounded corners of the hardware. This establishes greater harmony between our software and hardware, while thoughtfully considered groups of controls, free up valuable space for your content. Liquid Glass is translucent and behaves just like glass in the real world. Its color is informed by your content and intelligently adapts between light and dark environments, and as a distinct functional layer that sits above your app, the material dynamically morphs when you need more options, or as you move between views.

We’ve always cared deeply about every detail of our software design, and it’s these moments of beauty, craft, and joy that bring our products to life. Our new design blurs the lines between hardware and software to create an experience that’s more more delightful than ever, while still familiar and easy to use. Today marks an exciting and beautiful new chapter for our design, one that sets the stage for our next era of our products and how you interact with them every day.

Sebastiaan De With, in a remarkably prescient post predicting the nature of this new design, emphasized how only Apple could make Liquid Glass:

A logical next step could be extending physicality to the entirety of the interface. We do not have to go overboard in such treatments, but we can now have the interface inhabit a sense of tactile realism. Philosophically, if I was Apple, I’d describe this as finally having an interface that matches the beautiful material properties of its devices. All the surfaces of your devices have glass screens. This brings an interface of a matching material, giving the user a feeling of the glass itself coming alive…

The interfaces of computers of the future are often surprisingly easy to imagine. We often think of them and feature them in fiction ahead of their existence: our iPhone resembles a modern Star Trek tricorder; many modern AI applications resemble the devices in sci-fi movies like ‘Her’ and (depressingly) Blade Runner 2049. It’s not surprising, then, that concept interfaces from the likes of Microsoft often feature ‘glass fiction’:

The actual interface is unfortunately not nearly as inspired with such life and behavioral qualities. The reason is simple: not only is the cool living glass of the video way over the top in some places, but few companies can actually dedicate significant effort towards creating a hardware-to-software integrated rendering pipeline to enable such UI innovations…Only Apple could integrate sub pixel antialiasing and never-interrupted animations on a hardware level to enable the Dynamic Island and gestural multi-tasking; only Apple can integrate two operating systems on two chips on Vision Pro so they can composite the dynamic materials of the VisionOS UI. And, perhaps only Apple can push the state of the art to a new interface that brings the glass of your screen to life.

De With’s prescience actually gives me great hope for Liquid Glass: the best innovations are obvious to those who understand what is just becoming possible, and Apple’s integration has been and continues to be a meaningful advantage for things like user interfaces.

Third, Apple CEO Tim Cook has for a long time extended his framing of Apple’s differentiation to be the integration of hardware, software, and services, but while that is certainly true from a financial perspective, I’ve long had a hard time buying that the services component made for better products; as I noted above, Apple’s services have typically been something to be endured, as opposed to a reason to buy their devices, and the Siri debacle has only emphasized that point.

What is much more compelling — and the fact that Liquid Glass is a design language meant to unify Apple’s devices speaks to this — is the integration of Apple’s devices with each other. Every Apple product you buy is enhanced by the purchase of additional Apple products; to that end, one of the coolest parts of the WWDC presentation was about Continuity, Apple’s brand for features that connect various Apple products:

Let’s talk about the power of continuity. Continuity helps you work seamlessly across Apple devices, and we’re excited to introduce two new Continuity features. First, we’re bringing Live Activities to Mac. So if you’ve ordered Uber Eats on your iPhone, the Live Activity also appears in the menu bar, and when you click, the app opens in iPhone-mirroring, so you can take action directly on your Mac. We’re also enhancing the calling experience by bringing the Phone app to Mac. You can conveniently access your familiar content, like recents, contacts, and voicemail, synced from iPhone, and easily make a call with just a click. Incoming calls look beautiful on the bigger screen, featuring stunning contact posters of your friends and family, and the Phone app on Mac includes all the great updates we talked about earlier, like hold assist, call screening, and live translation. So that’s what’s new in Continuity.

These sorts of features aren’t going to change the world; they are, though, features that I can absolutely see making my life better and more convenient on an ongoing basis. And, to the broader point, they are features that only Apple can do.

More generally, yes, a focus on UI design is a retreat from The Gen AI Bridge to the Future; that future, however, will start from the devices we still use all day every day, and Apple focusing on making those devices better is a retreat that I expect will have a far more positive impact on my life than the company struggling to catch up in AI.

Apple’s Retreat to Empowering Developers and Partners

That’s not to say there weren’t some notable AI announcements in Apple’s keynote.

First, Apple announced the Foundation Models framework:

This year we’re doing something new, and we think it’s going to be pretty big. We’re opening up access for any app to tap directly into the on-device, large language model at the core of Apple Intelligence, with a new Foundation Models Framework. This gives developers direct access to intelligence that’s powerful, fast, built with privacy, and available even when you’re offline. We think this will ignite a whole new wave of intelligent experiences in the apps you use every day.

For example, if you’re getting ready for an exam, an app like Kahoot can create a personalized quiz from your notes to make studying more engaging, and because it uses on-device models, this happens without Cloud API costs. Or perhaps you’re camping off-grid, poring over the hikes you downloaded to AllTrails. Just describe what you’re in the mood for, and AllTrails can use our on-device models to suggest the best option. We couldn’t be more excited about how developers can build on Apple Intelligence to bring you new experiences that are smart, available when you’re offline, and that protect your privacy.

It’s important not to oversell the capabilities of Apple’s on-device AI models: of course developers who want to create something that is competitive with the output of something like ChatGPT will need to use cloud-based AI APIs. That reality, however, applies to Apple as well! Part of the folly of the initial Apple Intelligence approach is that Apple was promising to deliver beyond state-of-the-art capabilities on the cheap, using its users’ processors and power.

What is compelling about the Foundation Models Framework is how it empowers small developers to experiment with on-device AI for free: an app that wouldn’t have AI at all for cost reasons now can, and if that output isn’t competitive with cloud AI then that’s the developer’s problem, not Apple’s; at the same time, by enabling developers to experiment Apple is the big beneficiary of those that discover how to do something that is only possible if you have an Apple device.

Second, Apple deepened its reliance on OpenAI, incorporating ChatGPT’s image generation capabilities into Image Playground and adding ChatGPT analysis to Visual Intelligence. There is still no sign of the long-rumored Gemini integration or the ability to switch out ChatGPT for the AI provider of your choice, but the general trend towards relying on partners who are actually good at building AI is a smart move.

Third, Apple is also incorporating ChatGPT much more deeply into Xcode, its Integrated Development Environment (IDE) for building apps for Apple platforms; developers can also plug in other models using API keys. Xcode still has a long ways to go to catch up to AI-first IDEs like Cursor, but again, partnering with foundational model makers is a far smarter strategy than Apple trying to do everything itself.

These are, to be sure, obviousmoves, but that doesn’t make them any less important, both in terms of Apple’s future, and also with regard to the theme of this Article: Apple’s initial success with the Apple II was because of 3rd-party developers, and developers were critical to making the iPhone a sustainable success. Trusting developers and relying on partners may be a retreat from Apple’s increasing insistence on doing everything itself, but it is very much a welcome one.

Apple’s [Forced] Retreat to App Store Sanity

Apple didn’t say much about the App Store in the keynote, but they did announce a new Games app; M.G. Siegler theorized late last month that this may be laying the groundwork for splitting up Games from the rest of the App Store:

What if this new gaming-focused app – let’s just call it ‘Game Store’ – is not only meant to unify Apple’s gaming-focused efforts, but also to separate them from the App Store itself? Why might Apple do this? Because this would allow them to more easily differentiate between the two and, importantly, give the two independent policies.

That means that Apple could, say, drop the rate developers have to pay when it comes to revenue share in the App Store, while keeping it the same as it is now in the ‘Game Store’. And that matters because actually, gaming makes up some two-thirds of Apple’s App Store revenue at the moment (between paid downloads and in-app purchases – but it’s predominantly the latter). It’s the actual key to Apple’s model for this segment of the Services business.

And guess what else is true? In gaming, a 70/30 split is a well-established norm. In fact, it’s where Apple’s own App Store split originates from (by way of iTunes, which also copied the model back in the day)! Yes, there are others who have tried to disrupt this split, notably Epic, but Apple has a much stronger case for a 70/30 split when it comes to gaming than it now does for the overall app ecosystem.

So hear me out: the ‘Game Store’ keeps the 70/30 model and the ‘App Store’ moves to something more like 85/15 as the standard (matching Apple’s currently convoluted system for small developers with various arbitrary thresholds). Perhaps for smaller developers, Apple even drops it to 90/10.

Apple did not announce such a shift yesterday, but the infrastructure is now in place to do exactly what I have advocated for years: treat games differently from other apps. Gaming revenue is almost entirely based on zero marginal cost content, and games are more susceptible to abuse and more likely to be used by kids; I don’t mind Apple’s more heavy-handed approach in that case and, as Siegler notes, this level of control is the industry standard for other gaming platforms like consoles. In other words, Apple should retreat from trying to take a cut of everything digital, and instead act like a console maker where appropriate, and a more neutral computer platform for everything else.

Unfortunately for Apple, keeping console-level control of games may no longer be possible, particularly after the Ninth Circuit Court of Appeals denied Apple’s request for a stay of Judge Yvonne Gonzalez Rogers’ order lifting anti-steering restrictions on all apps, including games. The functional outcome of Gonzalez Rogers’ order is a retreat by Apple from its overbearing control of app monetization, albeit not one Apple is engaged in willingly.

Once again, however, a retreat is exactly what Apple needs. The company has gone too far with the App Store, not only embittering developers and losing court cases, but also has put its fundamental differentiation at risk. I warned the company of exactly this in 2021’s Integrated Apple and App Store Risk:

This is where the nuance I discussed in App Store Arguments becomes much more black-and-white. Yes, Apple created the iPhone and the App Store and, under current U.S. antitrust doctrine, almost certainly has the right to impose whatever taxes it wishes on third parties, including 30% on purchases and the first year of subscriptions, and completely cutting off developers from their customers. Antitrust law, though, while governed by Supreme Court precedent, is not a matter of constitutionality: it stems from laws passed by Congress, and it can be changed by new laws passed by Congress.

One of the central planks of many of those pushing for new laws in this area are significant limitations on the ability of platforms to offer apps and services, or integrate them in any way that advantages their offerings. In this potential world it’s not simply problematic that Apple charges Spotify 30%, or else forces the music streaming service to hope that users figure out how to subscribe on the web, even as Apple Music has a fully integrated sign-up flow and no 30% tax; it is also illegal to incorporate Apple Music into SharePlay or Shared-with-you or Photos, or in the most extreme versions of these proposed laws, even have Apple Music at all. This limitation would apply to basically every WWDC announcement: say good-bye to Quick Note or SharePlay-as-an-exclusive-service, or any number of Apple’s integrated offerings.

I think these sorts of limitations would be disappointing as a user — integration really does often lead to better outcomes sooner — and would be a disaster for Apple. The entire company’s differentiation is predicated on integration, including its ability to abuse its App Store position, and it would be a huge misstep if the inability to resist the latter imperiled the former.

This, more than anything, is why Apple should rethink its approach to the App Store. The deeper the company integrates, the more unfair its arbitrary limits on competing services will be. Isn’t it enough that Spotify will never be as integrated as Apple Music, or that 1Password will not be built-in like Keychain, or that SimpleNote will only ever be in its sandbox while Apple Notes is omnipresent? Apple, by virtue of building the underlying platform, has every advantage in the world when it comes to offering additional apps and services, and the company at its best leverages that advantage to create experiences that users love; in this view demanding 30% and total control of the users of its already diminished competition isn’t simply anticompetitive, it is risking what makes the company unique.

This is exactly what is happening in Europe: the DMA requires Apple to open up a whole host of capabilities that undergird its integration both on individual devices and especially between devices, and Apple is signalling that it will simply remove those features in the E.U.. That is one way to solve the company’s DMA issues, but the cost is severe: in one of Apple’s largest markets it can’t actually deliver on the differentiation that, earlier in this Article, I was celebrating its retreat to.

Retreat and Reset

The biggest part of WWDC — and the biggest part of this Article — was about Liquid Glass, which has drawn some unflattering comparisons to past Microsoft operating system releases:

The Windows Vista update with aero glass was a huge part of my childhood, so I'm getting serious flashbacks

Again, I’ll withhold judgment on Liquid Glass until it ships, but there is another Microsoft OS comparison I’ve been thinking about recently: to me last year’s Siri disaster is a lot like Windows 8.

Windows 8 was an attempt to leverage Microsoft’s large PC install base into a competitive position in touch-based devices, and it did not go well: consumers — particularly enterprises — hated the new UI, and developers weren’t interested in a platform without users. Microsoft was forced to retreat, and eventually came out with Windows 10, which was much more inline with traditional Windows releases.

Apple has clearly missed the boat on cutting edge AI; what I’m open to is the argument that this was a ship the company was never meant to board, at least when it comes to products like ChatGPT. Meanwhile, I’ve long been convinced that Apple has gone too far in its attempt to control everything even tangentially related to its devices; from 2017’s Apple and the Oak Tree:

Apple has had a special run, thanks to its special ability to start with the user experience and build from there. It is why the company is dominant and will continue to be so for many years. Apple as an entity, though, is not special when it comes to the burden of success: there will be no going back to “Rip. Mix. Burn.” or its modern equivalent.

In short, Apple is no longer the little reed they were when Jobs could completely change the company’s strategy in mere months; the push towards ever more lock-in, ever more centralization, ever more ongoing monetization of its users — even at the cost of the user experience, if need be — will be impossible to stop, for Tim Cook or anyone else. After all, such moves make Apple strong, until of course they don’t.

To that end, while I understand why many people were underwhelmed by this WWDC, particularly in comparison to the AI extravaganza that was Google I/O, I think it was one of the more encouraging Apple keynotes in a long time. Apple is a company that went too far in too many areas, and needed to retreat. Focusing on things only Apple can do is a good thing; empowering developers and depending on partners is a good thing; giving even the appearance of thoughtful thinking with regards to the App Store (it’s a low bar!) is a good thing. Of course we want and are excited by tech companies promising the future; what is a prerequisite is delivering in the present, and it’s a sign of progress that Apple retreated to nothing more than that.
