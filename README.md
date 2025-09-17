# On the Importance of "Boring" Software

I stumbled on this gem of an article. It's a few years old but still feels incredibly relevant.

You can read it here: [Choose Boring Technology](http://boringtechnology.club/)

---

I found this post really interesting because in school and on social media, there's so much hype around using the newest, coolest, most cutting-edge technology. You see job postings asking for 5 years of experience in a framework that's only 3 years old, and it's easy to feel like you're constantly behind.

What I love about this article is that it makes a strong case for the opposite: choosing stable, well-understood, and "boring" technology to get the job done. The author's point is that the goal is to build something useful for people, not to build a resume or experiment with shiny new toys on the company's dime. Using boring tech means less time debugging weird, undocumented edge cases and more time actually building features.

It's a refreshing perspective that takes a lot of the pressure off. It reminds me that being a good engineer isn't about knowing every new library that comes out, but about making smart, practical decisions to solve problems effectively. A really great read!

### Additional insights from the full talk (by @apoorvib):
The author, Dan McKinley (formerly of Etsy and now at Mailchimp), introduces the concept of "innovation tokens" - a limited budget for doing something creative, weird, or hard. Early-stage companies get maybe three of these tokens, so if you're trying to "reshape the entire world economy" (like Etsy claimed), you're already spending at least one token on your core business innovation. It makes little sense to also be innovating on databases or programming paradigms simultaneously.

McKinley distinguishes between "known unknowns" (things we know we don't know) and "unknown unknowns" (things we don't know that we don't know). New technology has a much larger set of both categories, making it inherently riskier. "Boring" technology isn't boring like C-SPAN - it's boring in the sense that it's well-understood. "It's bad, but you know why it's bad. You can list all of the main ways it will let you down."

One of the most compelling examples is Etsy's activity feeds feature. Built using their existing stack (including Memcached instead of the "better" Redis), the feature scaled 20x over several years without the original team even knowing - because they used shared infrastructure that others were already maintaining and scaling. Had they used Redis just for this feature, it would have required dedicated attention as it scaled.

The talk emphasizes that adding technology is easy, but living with it professionally is hard. You need monitoring, backup strategies, security patches, scaling plans, and expertise - all perpetual costs. The author warns against "polyglot persistence," arguing that giving teams free reign to choose their own infrastructure is "handing developers a ball of chain and padlocks."

McKinley also shares the "law of software" - every piece of software is awful when you first start using it because you discover all its problems. The naive response is to switch to something new for the next feature, which is how you end up with "nine alerting systems in production." The better path is pushing through to mastery, where "there are still problems. Everything still sucks but it feels manageable."