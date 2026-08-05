# Key Tech and Business Insights from Podscan's Success Journey

> 原链: https://thebootstrappedfounder.com/one-year-of-podscan-reflecting-on-tech-business-decisions/  
> 来源: thebootstrappedfounder.com · 归档自 EP.04 · 抓取于 2026-08-06  

---

So Podscan itself is doing pretty well. It has grown from an experiment into something substantial. It’s profitable now and has customers of all sorts that I didn’t even expect to serve in the beginning. With every week, I shift closer to the perfect messaging, reaching the right people at the right time.

What I want to share with you today is me walking through the tech stack and the business stack of the Podscan business and product. I’ll talk about what expectations I had at the beginning and if they’ve been fulfilled, if they’ve been exceeded, or if I had too big or too small expectations. Essentially: what worked out, and what’s still lacking?

I’ll start with the tech side of things, then go into the more business side—the services that I use to make Podscan run.

## The Tech Stack: Boring Technologies Win

There are a couple of major choices you always have to make in a software business: What’s the general infrastructure you build your product on? What is the development pipeline? And what are the components that you integrate your system with?

For me, the general architecture was to build one single, central application server that pretty much does everything. If I need any external servers, they’re going to be their own deployment somewhere else—any external services or background processes happen on another server.

### Laravel: A Spectacular Ecosystem

The biggest choice I made at the beginning of Podscan was to build this product with PHP, and more precisely, the Laravel framework. At the time I started, Laravel was at version 10 (it’s now at 12). I haven’t upgraded yet because it’s working more than well enough in terms of performance.

When I started using Laravel and looking into the Laravel space, I was quickly very pleasantly surprised and inspired by the ecosystem around the product. Nowhere else had I found such a plug-and-play ecosystem that seemed so well integrated—not just different libraries, but actual products that seamlessly fit with each other.

This isn’t surprising looking at all the work that the Laravel team and Taylor Otwell have been doing to create things like Laravel Forge for hosting, Envoyer for deployment, Spark for payments, Jetstream for users and team logic, and so many other components. Initially, it was almost overwhelming to see all these services, but I ended up massively benefiting from them.

The initial prototype was very quickly spun up with all these components, and none of them has been problematic over the long term. They’re all still well-supported, working extremely well, reliable, and I haven’t needed any extensions I couldn’t build or find someone who already built it.

### The AI Advantage of PHP

One benefit I found that I didn’t expect in the beginning (because I wasn’t working with AI back then—I was still coding everything by hand) is that once AI hit the scene and I could have AI tooling check my logic and build features for me, the fact that PHP is such a popular language with decades of people solving problems with it became a massive benefit.

AI systems, particularly the new versions trained on more material and with better reasoning capabilities, are extremely good at building PHP software. So choosing PHP—one of the oldest programming languages on the web—and using it to build on top of a well-distributed and popular framework was a spectacular choice.

I highly recommend if you build a new product to take this into account. There’s something called the Lindy effect—that a thing that has existed for a while is very likely to keep existing for just as long. Things that have been around for 20 years will probably be around for 20 more years, but something that’s only been around for two months might not be here anymore in two months.

Hypes are quick, but long-term things stay long-term. This effect is particularly true about programming language choices. Most technical choices benefit from things that have been around for a while because there’s this long rat tail of addendums and additional stuff that you might not think about.

If you choose a language that’s popular and has been around for a while, you’ll find:

- Potential experts to help you with problems (because they’ve had the opportunity to learn and become experts)
- Documentation and examples that AIs can draw from
- Well-maintained libraries with features you actually need in real-world projects

This is something that comes with a technology choice that might be boring or not as modern but is still incredibly impactful for how easy it is to build a business on top of it.

### The Database Dilemma: MySQL vs PostgreSQL

There are several cascading choices from the framework selection. Laravel, with its internal system Eloquent, supports several databases including MySQL, PostgreSQL, and SQLite.

I chose MySQL, and that’s a choice I don’t necessarily regret, but I think I could have made a different one and probably had a more positive outcome. As I created massive numbers of transcripts every day and fed them into the database, I had to deal with the fact that MySQL isn’t that good for full-text search or vector embeddings. Those things don’t really exist in MySQL.

MySQL has been around forever for web programming, but these capabilities aren’t part of the basic toolkit. That’s different for PostgreSQL, and it turns out to be much easier in SQLite as well.

SQLite doesn’t make sense for me because I have so much data to store—Podscan at this point is probably somewhere north of five to six terabytes in raw storage. I had to build a system to move some of this onto object storage and only reference and pull it in when needed.

One consequence of having massive amounts of data in a database table is that changing the structure or schema at that scale is almost impossible without workarounds. If you try to add an index to a database that’s constantly being read from and written to, that index is going to lock up your application—and you can’t afford this, particularly if you offer an API like I do.

What I can do is run what AWS calls a blue-green deployment, where I create a copy of the database, add my index to the synchronized copy, and then switch over. That’s additional cost—for every index I want to add, I effectively pay twice the daily hosting rate, which is easily hundreds of dollars. Not fun, and I rarely do this now unless it’s really needed.

### Search Engine: Meilisearch

The fact that I can’t do full-text search in MySQL meant I needed to externalize search to a different system. I chose Meilisearch out of several options (including Typesense and Algolia).

Back then, I think we were on version 1.7. I quickly learned that having every single item from my main database in my search engine would be impossible for the search engine to keep up with. It’s just too much stuff to ingest, because Meilisearch needs to build an index on massive transcripts of hour-long podcasts.

I had to figure out how to set up my server to handle the inflow. Over time, Meilisearch became much better—1.9 was the version that really started working for me, and I just upgraded to 1.14 a few days ago. Throughout this time, Meilisearch had a few hiccups, but I always run two servers so I can quickly switch if one needs maintenance.

It requires some monitoring, but once running, it’s extremely fast, very reliable, and produces very good results that I use both in my API and UI. With 1.14, ingestion has sped up so much—I can hammer it with transcripts, and it just keeps ingesting them.

The big benefit of building Podscan in public was being able to reach the people behind Meilisearch, do bug fixing with them, and give them data exports to play with. This led to features being prioritized that I can really use now.

I’m really happy with this choice, especially seeing where Meilisearch is going with AI-assisted vector embedding search. One day I’ll turn that on and have semantic search over the full corpus of all podcast episodes anywhere. That’s still something for the future since it requires resources I can’t spare yet—Podscan has only recently turned profitable.

### Hosting & Deployment

I host my server on AWS, which has been super reliable. There was only one time in the last year where my server died because of a physical rack malfunction, but I could quickly restore the virtual machine on another server.

I deploy through Laravel Forge and Envoyer, which has been an amazing choice from the start. It made it super easy to have a highly performant PHP FPM setup and easy git-based deployment. These tools have been reliable in helping me set up my main server and API servers for transcribing and data abstraction.

The whole Laravel ecosystem has been extremely useful and good to me.

## Business Services & Tools

Now let’s look at the business side—the services that help Podscan operate.

### Scraping: ScrapingBee

For all my scraping needs, I use ScrapingBee. They’ve been great from the start—a wonderful SaaS that delivers exactly what you want for scraping data. More recently, they added AI features where you don’t need to tell them exactly what to extract—just tell them what it is, and they extract it in your chosen format. This has been massively helpful to offload some AI complexity to another company.

### Error Tracking: Sentry & Flare

For error tracking in both PHP and frontend, I’ve been using Sentry and Flare (a PHP-centric error tracking tool). Both have been really helpful, and their alerting is spectacular.

### Email: From Postmark to Resend

For email, I initially used Postmark. That worked well at first, but it became super expensive over time, and their deliverability didn’t work for me. Switching to Resend has been a much better choice for transactional emails.

For marketing emails, I use Kit (formerly ConvertKit)—probably one of the best choices I made. It keeps everything useful and allows me to greet the team, help with emails, and have well-designed templates.

### Payments: Paddle

For payments, I chose Paddle. They’ve been the most reliable and least complicated payment provider I’ve ever worked with. I have almost $10,000 in MRR at this point because Paddle makes it happen.

I could probably have about $500 more per month if I didn’t use Paddle, but the headaches I would have and the things I would have to build that Paddle just provides for their fee is substantial. They handle renewals, failed payments, refunds, local currencies—all things I would have to manually build. It’s extremely useful and has been a really good choice.

This also means I don’t have to make field invoices to my customers—the people buying Podscan products are Paddle’s customers. I just have to reverse invoice with Paddle 12 times per year.

### Employment: [Remote.com](http://Remote.com)

I’ve been experimenting with [Remote.com](http://Remote.com) for employment for a couple of months. If you want to employ yourself or somebody somewhere but can’t do it because you don’t have a company registered in that location, [Remote.com](http://Remote.com) has been really good. They’ve been very easy to use and do exactly what they need to.

### Business Setup: Alt Space & Mercury

For banking and making the business happen—filing taxes and reports—I used Alt Space, a company that sets up US-based companies in Delaware or Wyoming. I set up Podscan as a Delaware C-Corp so I could take bootstrap-compatible investment from the Calm Company Fund. They also set me up with bookkeepers and tax professionals.

They set me up with a bank account at Mercury, which has been really good. Banking with Mercury is a breeze because it’s all app-based and professionally handled. They understand the business needs of a modern software business owner, and their UI and APIs are built with that in mind.

If you start a company or want to move banks because yours is getting weird and old-school, look into Mercury. It’s not a bank itself—it’s a financial service provider working with Evolve Bank and Trust, which is a pretty reliable and reputable bank.

## Reflecting on a Year of Choices

Obviously, Podscan is now a profitable business that’s doing well and growing. I made the right choices along the way so that it could do this. Looking at it after the fact makes it seem easy, but I do want to do this kind of reflection on a more regular basis.

I tend to do a yearly recap in my mind—looking at where things are, how I want them to go, how I wanted things to go a year ago, and how they are now. Maybe next year I’ll have different answers. Maybe I’ll find certain technologies don’t work anymore. Maybe my transcription system will be completely replaced by a service invented two months from now that’s 20 times more efficient, and I’ll have to rebuild everything.

But looking at it now, from April 2025 back to April 2024 when Podscan really got going as a fully-fledged product, I think the technical and business choices have been good.

I still try to ensure that any choice I make has a migration path to something else. It’s harder with fundamental choices like language, framework, and database, but easier with external services like email providers, scraping tools, or error tracking. I always think: if that service exploded tomorrow, would I still be able to run my product? How long would it take to get back to normal? And for all these services, I believe I have an answer.

Could I have chosen something wildly better? I don’t think so. I’ve met many new technologies along the way and experimented with them, but nothing really beat what I had going on—mostly because I’d already built a project with this stack. Part of the magic is just knowing what you’re doing and repeatedly doing it.

Let’s see how many good choices I make for the next year!
