# Wikimedia wants to make it easier for you and AI developers to search through its data

> 原链: https://www.theverge.com/news/789288/wikidata-ai-friendly-database  
> 来源: www.theverge.com · 归档自 EP.26 · 抓取于 2026-08-06  

---

The late English writer Douglas Adams is best known as the author of the 1979 book *The Hitchhiker’s Guide to the Galaxy*. But there is much more to Adams than what is written in his [Wikipedia entry](https://en.wikipedia.org/wiki/Douglas_Adams). Whether or not you *need* to know that his [birth sign](https://www.famousbirthdays.com/people/douglas-adams.html) is Pisces or that libraries worldwide store his books under the same string of numbers — [13230702](https://viaf.org/en/viaf/113230702) — you *can* if you head to an [overlooked corner](https://www.wikidata.org/wiki/Q42) of the Wikimedia movement called Wikidata.

# Wikimedia wants to make it easier for you and AI developers to search through its data

Wikipedia’s sister project Wikidata just got a new database that is easier for AI models to ingest.

![acastro_STK013_02](https://platform.theverge.com/wp-content/uploads/sites/2/2025/04/acastro_STK013_02.jpg?quality=90&strip=all&crop=0%2C0%2C100%2C100&w=2400)

![acastro_STK013_02](https://platform.theverge.com/wp-content/uploads/sites/2/2025/04/acastro_STK013_02.jpg?quality=90&strip=all&crop=0%2C0%2C100%2C100&w=2400)

There, images, text, keywords, and other information related to Adams are stored both in a [webpage](https://www.wikidata.org/wiki/Q42) and, for the robots among us, in formats designed for machines like [JSON](https://www.wikidata.org/wiki/Special:EntityData/Q42.json).

Now, Wikidata is getting a new AI-friendly database that makes it easier for large language models to ingest the information. The database comes from the [Wikidata Embedding Project](https://www.wikidata.org/wiki/Wikidata:Embedding_Project) out of the German Wikimedia chapter, Wikimedia Deutschland, which oversees Wikidata. The Berlin-based team spent the past year using a large language model to turn 30 million entries within Wikidata from clunkily structured data into vectors that capture the context and meaning around the Wikidata entry.

In this vectorized format, information is best imagined like a graph with dots and interconnected lines — Adams would be connected to “human” as well as the titles of his books, Lydia Pintscher, Wikidata portfolio lead, told *The Verge*.

While the front-end user experience will remain the same — no, Wikipedia is *not* becoming a chatbot, the project leaders say — the back end will become easier for AI developers to access when building, for example, their own chatbots using the data.

The goal of the project is to level the playing field for AI developers outside the monied core of Big Tech, Pintscher said. Companies like OpenAI and Anthropic have the resources to vectorize Wikidata, just like Pintscher and her team did. It’s the smaller outfits that most benefit from the new access to curated data stored in the vaults of Wikidata. “Really, for me, it’s about giving them that edge up and to at least give them a chance, right?” Pintscher said.

She points to [Govdirectory](https://www.govdirectory.org/) as an example project that harnessed Wikidata’s vast data curated by volunteers for good. The platform allows users to find the social media handles and emails for public officials across the world.

Most AI chatbots prioritize popular words and topics across the internet. In addition to giving Little Tech a leg up, the team hopes that easier access to Wikidata will result in AI systems that better reflect niche topics not widely represented across the internet, Pintscher said. This could be a better way to get information into ChatGPT, for instance, than “generating a ton of content and then waiting for the next time for ChatGPT to retrain, and maybe, or maybe not, taking into account what you contributed,” Pintscher said.

In practice, the vectors will allow AI systems to better access the context around information in addition to the information itself, Philippe Saadé, Wikidata AI project manager, told *The Verge*.

The team used a model from AI company Jina AI to turn Wikidata’s structured data, captured through September 18th, 2024, into vectors. IBM company DataStax currently provides the infrastructure to store the vector database to the project for free.

The team is waiting for feedback from developers who use the database before updating it with information added over the last year. While the current database does not include entirely new information added in the last year, Saadé says small edits or tweaks to existing Wikidata will not diminish the database’s usefulness. “At the end of the day, the vector that we’re computing is like a general idea of an item, so if some small edit has been made on Wikidata, it’s not going to be super relevant,” he said.

*Correction, October 1:**An earlier version of this article misstated the number of entries included in the project. It is 30 million entries, not 19 million. *The name of the Wikidata Embedding Project has been corrected from Wikipedia Embedding Project.* A reference to the Wikimedia Foundation has been adjusted to the Wikimedia movement.*

**Follow topics and authors**from this story to see more like this in your personalized homepage feed and to receive email updates.
