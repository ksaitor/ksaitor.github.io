---
layout: post
title: How I in-validated a business idea in 3 months with little code, while traveling the world ✈️
date: 2017-09-28
tags: ['startups', 'podcasts', 'failure', 'sf', 'singapore', 'bali']
og-image: 'https://ksaitor.com/images/readbyhumans-postmortem/IMG_8422.JPG'
---

In this article I’ll share with you how I validated a fresh idea, by focusing on metrics instead of lines of code; did
that in 3 months, instead of 2.5+ years in my previous startup; got accepted in Y Combinator’s Startup School. All while
traveling across San Francisco, Singapore and Bali. Buckle up!

---

It was mid-April this year, I was in SF, recovering from my previous startup failure, trying to meditate and staying
away from jumping on new ideas, when all of a sudden… well I again got hit by a _new idea_! “Danger Danger!“ — my mind
told me — “avoid past mistakes you should. Give it time and space, you should, before pouring efforts in it”. Shuuuure…

### Idea 💡

I was going through a large list of newsletters that linked to an even larger list of articles. I was reading some,
[Pocket](https://getpocket.com){:target="\_blank"}ing others… and you know, never getting back to Pocket to actually
read them. 😅 Same time I started listening to podcasts again, and on one of the monday mornings it struck me — what if
I could save an **article**, the same way I could with Pocket’s browser extension, but it gets **converted into an
engaging audiobook**. Not a robotic-sounding text-to-speech, but something that’s actually **read by a human**. That was
it!

### Research 📚 

Again, I wanted to avoid mistakes I’ve done in the past and do hell-lot of research on this one, before sinking in too
much energy and being attached an idea that won’t work.

#### Is there demand?

After asking around what they thought about the idea, I quickly saw **two groups** emerge — those who were ecstatic
about podcasts and spoken content and those who did not care at all. Surprisingly I found **zero** people in between.
That was actually pretty good, I thought! That’s the reaction any good idea or product should get. Hate it or love it!
Great ideas are polarising. I was still surprised that audio content was like that. I felt I was onto something.

Next I took a look at some macros and comps. What’s happening to podcasting consumption and whether anyone has build
anything like that:

![fancy demand growth chart](https://cdn-images-1.medium.com/max/1600/1*MR2ifsngONIx-Y17SBGwyQ.png) Market is growing
and got ton of potential… _In the USA, that is…_

YC had a podcasting app in their W17 batch called
[Breaker](https://www.producthunt.com/posts/breaker-4){:target="\_blank"} — another good sign!

#### Can this be done?

So I learned that there might be more than 1 person (me) who wants this and likely to use it. Next on, I wanted to
figure out how to deliver the service. I saw 3 routes:

- Speech synthesis (TTS)
- Crowdsource narration from students
- Hire professional voice actors

I started by evaluating the state of speech synthesis tech. I tried out all available TTS solutions for the start. The
one from AWS, that’s powering Alexa, the one from Google and a few others. As I expected all of them sounded too robotic
and far away from producing engaging long-form spoken content. Like audiobooks or podcasts, for example… Price: **cheap
🤑**. Quality: **not engaging 😒**

Next, I tried narrating articles myself. Ableton Live + standard Apple earphones and mic. Okay. So I’ve been uploading
my audios to [SoundCloud here](https://soundcloud.com/readbyhumans){:target="\_blank"} and sending samples to friends.

<iframe width="100%" height="166" scrolling="no" frameborder="no" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/316663147&amp;color=%23ff5500&amp;auto_play=false&amp;hide_related=false&amp;show_comments=true&amp;show_user=true&amp;show_reposts=false"></iframe>

Quality was variable. Bearable, I’d say. Far away from sounding like a pro. I did this for a week, every day. One
**surprising side-effect** that I found, is that for someone like me, with english being second language, it’s an
amazing way to practice pronunciation and boost confidence with practice. Price: **cheap to mid-range 🤷‍**. Quality:
**may vary** **🤷‍**

Okay. Next, I decided to find out how much could a semi-professional and professional voice actors would cost. Long
story short, it was anywhere between $10/hour (if you are lucky to find a good voice for that), up to $100/hour.
Averaging 40–50 bucks for a quality North American accent. _Source_: personal network, Fiverr, Upwork. Price:
**expensive 💰😱**. Quality: **high quality engaging content 😎**

But the voice quality is clear. Compare my voice, you’ve heard above , with a professional. Here is an example, narrated
by [Darren Marlar](https://darrenmarlar.com){:target="\_blank"}. Darren rocks! 🤘

<iframe width="100%" height="166" scrolling="no" frameborder="no" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/344228341&amp;color=%23ff5500&amp;auto_play=false&amp;hide_related=false&amp;show_comments=true&amp;show_user=true&amp;show_reposts=false"></iframe>

Considering such high costs for content production, we better start off with a category or a submarket with a high
**content reuse**.

**Research** 📚 **Conclusion**: I decided to rely on professional voice actors. First version of service should
“**wow**” early adopters. **Current progress**: nothing built, no name, no domain name, no landing page, some research,
2 weeks of casual research. Excitement builds up 😁 but my mood is mostly chill so far.

---

So far all this research might sound boring. Loads of talk and little action — right? Especially for someone with an
engineering background like myself, who jumps on coding a full-fledged backend and native mobile app right on… “_because
only after the product is built you can validate its market potential_” — no no no! Bullsh\*t! In most situation you
don’t have to build anything, to validate demand. This is planning! Remember what Winston Churchill said?

> “If you **fail to plan**, you are **planning to fail**.”

---

#### Some tangible progress. Finally!

Finally i decided to come up with a name, domain and a landing page.
[**ReadByHumans.com**](https://readbyhumans.com){:target="\_blank"} —  boom 💥 ! Thank god domain was available.

![readbyhumans logo](https://cdn-images-1.medium.com/max/1600/1*gr26dl9OLpsD2onK7qB4fg.jpeg)

Simple landing page built on [Sails.js](https://sailsjs.com){:target="\_blank"}, Mongo to store email sign ups, deployed
on [dokku](https://github.com/dokku/dokku/){:target="\_blank"} on
[AWS Lightsail](https://amazonlightsail.com/){:target="\_blank"}. Nothing fancy. Spent a day. Just used the tech that I
use on daily basis. It’s tempting to try out newest shiny tech for your new business idea, but you are just adding risk,
instead of mitigating it. It was tempting to go [Serverless](https://serverless.com/){:target="\_blank"} +
react-navite-web + redux + GraphQL+ god-knows-what.js. But **no**! Resist the temptation. `rm -rf` your engineering
pride. **Validate** your **business,** not your tech!

---

![YC Startup School Logo](https://cdn-images-1.medium.com/max/1600/1*rJPfqmnodBBB8vblTLKQOA.png){: .center-image}

#### YC Startup School

I got accepted into [YC’s Startup School](https://www.startupschool.org/){:target="\_blank"}! OMG! Funny enough I
applied with my previous company, that I just “closed” after 2 years of hustle (follow me, I’ll blog about it some time
this year).

Second week of Startup School I told my mentor, [Brad Flora](https://twitter.com/bradflora){:target="_blank"}, that I’m
changing the direction. His feedback was: “yes! it’s a great idea and a growing market! In fact, just last week I
invested in _[company in a similar space]_…” I was like: \_WOW_! The reaction was 10x compared to all reactions that I
ever got to my other projects. Everyone in the batch loved the idea too. I was ecstatic! 😃

Next day, my emotions were 180 degrees. Learning from mistakes of my previous project I wanted to monetize this ASAP.
Current idea was consumer focused, and it would take years to make a dime. I put on my smartass hat and decided I should
do a B2B detour to break even first and then at scale go back to consumer idea. **Holly f\*ck** this was a **bad idea**.
It was driven by fear and previous negative experience. So I went on for 3–4 weeks to research potential B2B avenues for
“article to human read audio” service. That journey was not bad — it was a **roller coaster** 🎢.

First I thought about narrating content for teams. Soon, it turned out that reading white papers is a thing, and teams
got to do ton of that. I shared this idea on one of the group calls and then this happened:

![YC Startup School Chat screenshot](https://cdn-images-1.medium.com/max/1600/1*p3S_OJrAjK3Stf1_WD2iDQ.png)

I felt ecstatic again! 😁

Someone from YC batch introduced me to an HR/culture manager from Cisco HQ. **YC people rock🤘!** Had a brief call. They
could use our service to let their engineers listen to lengthy whitepapers on the way to work. Sounded great! Quickly I
realized that technical whitepapers are also hard to narrate, due to figures, formulas graphs, and charts. You just have
to _see_ them to understand. How much they were willing to pay also did not sound exciting and barely covered production
costs. But I was still quite high and excited about the progress!

#### 🇸🇬 Singapore. Roller coaster is going down🎢 😧

End of April. Had to go back to Singapore (That’s where I live). Startup School is still on. I went out and shared
ReadByHumans with friends, fellow entrepreneurs and VCs. I was surprised how different the feedback and environment was
compared to the Valley! Suddenly majority is skeptical and no one really listens to podcasts in Asia. In the USA,
meanwhile, podcast consumption has been growing something around 20% year on year. South East Asia — flat. Ouch!

![sad times](https://cdn-images-1.medium.com/max/1600/1*PDRAUb9XeJ_3D7utTlWuvQ.gif){: .center-image}

> Why podcasting is a big thing in USA? My hypothesis, is it’s because of the high car _🚙_ ownership in the USA,
> compared to SE Asia. In the USA everyone is listening to radio / Spotify / audiobooks while commuting to work.

While in Singapore, I tried out another spin on B2B. Targeted companies that rely on _content marketing_. Pitch sounded
like “convert your written content & case studies into audio, so that leads could consume it faster and be sold,
faster.” After talking to a few SaaS businesses, I quickly learned that they lukewarm.

![tradegecko embed demo](https://cdn-images-1.medium.com/max/1200/1*4anx-T34kdZ1sjOIkjPFLQ.png)

Product would also require additional operational and feature overhead — analytics, conversion tracking, consistency of
voice actor’s voice, ensuring voice actors are not reused by competitors, and so forth… Alrighty. Moving on… 😒

---

I was frustrated with myself more than with challenges of selling B2B. Suddenly I felt that these 3 weeks I was not
solving my own pain. I was trying to please some companies, teams… I almost forgot how and why I started this project.
If you are to pour your sweat and soul into something, you better be solving your own pain and find other people who
share this exact pain with you. It was time for yet another change.

#### 🌴 Bali. Getting real sh\*t done

After spending two weeks in Singapore, I went to Bali for a month. I wanted to focus on ReadByHumans and ship something
by the end of Startup School. There, I caught up with my friend
[Andrey Azimov](https://twitter.com/AndreyAzimov){:target="\_blank"}, who recently exploded with his
[When To Surf](https://medium.com/@AndreyAzimov/i-learned-to-code-and-build-a-web-app-in-2-months-da8f2932c139){:target="\_blank"}.
We thought it’d be cool to work side by side and keep each other in check. He also suggested to get my sh\*t together
and to ship, measure, rinse, repeat. 👊

![Raman and Andrey](https://cdn-images-1.medium.com/max/1600/1*xrXKcmUCzy1PymGkg_TZ8g.png)

Whole of June was dedicated to make and test an UVP (unique value proposition). I decided to build a simple landing page
with an email sign up, measure what conversion rates I was getting on all steps of my funnel. But first — UVP.

![Raman drafting a landing page on a whiteboard](https://cdn-images-1.medium.com/max/2000/1*RnBoHZBwYOV4QRos9LmixQ.jpeg)

Clear title, call to action are critical. And basic imagery to convey what ReadByHumans was all about. For this launch,
I had to go for a compromise. I wish I could offer “We narrate any article on demand for free”. But that would just
bankrupt me. Hence, I decided to narrate top 3 articles from Hacker News. Top 3 articles for free upon sign up + 1 more
article weekly. That value prop was concise, it was a no-brainer, and I could afford to pay my voice actors for 1–3
articles per week. For a few weeks at least.

A little bit of magic and the final result is:

![ReadByHumans landing page](https://cdn-images-1.medium.com/max/2000/1*5Jg8d2q4rwt0SLYbZ46PyA.png)

The landing page is done. Email capture is ready. Autoresponder with top 3 articles is set up.

### Time to Ship! ⛵

I had an external deadline, which was YC Startup School Demo Presentation. June 16\. I aligned my Product Hunt and
Hacker News submissions to be around the same dates.

#### Product Hunt 

I followed best practices of Product Hunt launch. Tons been written about that, so just Google “Product Hunt launch
checklist”. Tuesday midnight, SFO time. Which is 3 PM in Bali and Singapore — no need to stay up all night! One way or
another, you still should be ready for a 24+ hour sprint with minimum sleep. Handling server load, replying to comments,
calls, etc. Take time to prepare. Following up on all the comments is something special! It’s a race!

Chris Messina and Ryan Hoover jumped into the conversation. My heart was beating fast!

![Product Hunt comments screenshot](https://cdn-images-1.medium.com/max/1600/1*XUnR4ujNg3AIuLJBusIDsw.png)

You can read the nitty gritty of the convo in the
[Product Hunt post here](https://www.producthunt.com/posts/readbyhumans){:target="\_blank"}.

#### Startup School

YC Startup School Demo Day was on June 16th. We got some traffic from there. Also got good feedback. Notably, YC Partner
Adora Cheung (Co-founder & CEO of [Homejoy](https://en.wikipedia.org/wiki/Homejoy){:target="\_blank"}) tweeted about
ReadByHumans all of a sudden:

<center>
<blockquote class="twitter-tweet" data-conversation="none" data-lang="en"><p lang="en" dir="ltr">Readbyhumans - articles to human read audio. I&#39;ve heard so many people who&#39;ve wanted this to exist, it&#39;s nuts. <a href="https://t.co/q96xtCaEqJ">https://t.co/q96xtCaEqJ</a></p>&mdash; Adora Cheung (@nolimits) <a href="https://twitter.com/nolimits/status/875873488434716672?ref_src=twsrc%5Etfw">June 17, 2017</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>
</center>

And here is the application video itself:

<iframe width="100%" height="500" src="https://www.youtube.com/embed/B450Hk-8q54?rel=0" frameborder="0" allowfullscreen></iframe>

Startup School launch felt like a complete success!

#### Hacker News

I had no idea how to launch on HN. Andrey had no idea as well, so he ran this by Pieter Levels. Pieter said “it’s a
mystery, but it’s key to balance upvotes with genuine comments”. Oh well, let’s give it a try. As you will see below,
most of the traffic came from HN, but not the sign ups.

![HN Screenshot](https://cdn-images-1.medium.com/max/1200/1*t0mP_CEAAANHBIESAxWyRQ.png)

On HN, my [“Show HN” post](https://news.ycombinator.com/item?id=14543968){:target="\_blank"} quickly became a
controversial topic. I did not anticipate that, to be frank.

I think the very first comment was raising copyright implications.

It’s a long and complicated topic and I’m also not a lawyer. You can read the
[debate](https://news.ycombinator.com/item?id=14543968){:target="\_blank"} youself, if you’ve got time.

One thing I learned here, is that it’s illegal (in most cases) to make a derivative work sell it via _distribution_.
Distribution, basically, means re-packaging and reselling someone’s content. I found two ways of solving it:

- Strike deals with publications and authors. I could not do that in an individual capacity, since it’s just way too
  much work, takes forever, costs are insane and… tl;dr not feasible for a bootstrapping project.
- However, when someone finds your article and requests a narration in individual capacity — that is not considered
  distribution (correct me if I’m wrong). It’s like hiring a personal voice over actor, whom you pay to narrate your
  texts for you.

You can read all the drama and conflicting views
[here](https://news.ycombinator.com/item?id=14543968){:target="\_blank"}.

In the end of the day, I did not see this legal issue as signal to stop. You can find a gazillion legal issues in merely
any business idea, granted you throw several lawyers, big money and angry competition into the mix. So I continued
ReadByHumans validation.

Key lesson learned to HN growth — have a meaningful conversation, not just dummy upvotes. I think I did that, more or
less, and we were on the first page within a few hours. Got us more traffic than PH.

### Results. Let’s measure!

After about a day, it was clear that I was getting about 22% conversion rate. From landing page views to email opt-ins.

![google analytics screenshot](https://cdn-images-1.medium.com/max/2000/1*f4jC7CupO5m8hze6e1hZog.png)

You can’t really read it on the screenshot above, the way I derived with 22%, is by dividing roughly 1270 visitors by
276 signups.

Most traffic and sign ups, as you can see above, came from Hacker News. Most Signups from Product Hunt.

![second google analyrics screenshot](https://cdn-images-1.medium.com/max/2000/1*kCWjE91k25QTrh5YsQED0g.png)

#### Funnels

I’ve never really thought about funnels before this project. I drafted a list of steps that users would have to take to
start paying us money, if we were to sell a Premium tier. Those steps would be:

- Land on page (Traffic)
- Sign up with email (Subscribed)
- Add private podcast feed url to their favorite podcast app and start getting FREE value from us. (Active Free)
- Eventually start paying for more value (Paying)

![modeling funnel in excel](https://cdn-images-1.medium.com/max/1600/1*P2vmWBRHyJKxm2I300kj_Q.png)

In the right column, titled **Facts**, you can see the real numbers that i’ve got so far. In **Conversion %** I’ve
divided these numbers by each other. Except for th 2% conversion rate. There, I just used a very optimistic conversion
rate of 2 percent. Typically it’s closer to 0.5–1%.

This modeling using current facts allowed me to project amount of traffic I had to drive to get to desired number of
paying customers. E.g. I wanted **20** and and then, **Desired Qty** column would derive Active Free, Subscribed and
Traffic numbers:

> **20** / 2% = 1000 Active Free (target) 1000 / 29% = 3450 Subscribed (target) 3450 / 22% = **15875** Traffic (target)—
> unique hits on the landing page.

This was a new and very powerful thinking technique. I was blown away! I was not planning to do anything right away with
these numbers, but they were setting clear expectations and **goals**, if I chose to grow this project.

Knowing industry averages is critical to judging a health of any business. When I was starting out I did not know which
numbers are healthy or not. But even today, some averages is a mystery. For example. **25% conversion rate** (qty of
people who open your site _divided_ by qty of people who enter their email) on the landing page is quite good. **0.5–2%
conversion rate** from freemium to paid is okay for _consumer products_ and _games_. **20% open rates** of your email
campaigns is also healthy.  Again, why is this important to know? — Because if you are new to the Internet game, you get
50% conversion rate but you _expect_ 100 visits and 90 signups — you’ll decide that you are a loser and stop your
business, while in fact you are killing it.

Seems like ReadByHumans had good, healthy numbers. However getting those 15k hits (ideally for free) was not immediately
obvious. Ideas are welcomed in comments on Twitter [@ksaitor](https://twitter.com/ksaitor){:target="\_blank"} please 🙏

#### Customer Development

For the upcoming several weeks, I did not want to invest more time in growing sign-ups. Instead, I wanted to focus on
making my service loved by existing users. I wanted to email each of them personally, understand why did they sign up,
their expectations, their needs, and what would they pay for. Yes! It’s a good idea to ask about money ASAP. This was
not meant to be a Silicon Valley type project, where I’d raise 1.5 Gazillion of dollars and subsidize growth forever
without thinking of making a profit. I wanted to validate that people would pay for something here and do that fast.

I learned a few lessons on how to get genuine feedback from users and previously covered them in my other post
“[You dont have to reply…](/2017-09-17/you-dont-have-to-reply-if-you-dont-want-to/){:target="\_blank"}”

### So why did we shut down?

Well, this all was not too bad. But there were few major issues.

#### Copyright 👮

Article copyright was a serious issue and I’m not a subject expert. Fear of things you don’t know you don’t know is
real. Hacker News reaction reminded me that no one gives a f\*ck about your positive intentions. I’ll say no more.

#### Economics 📈

I was spending about $300 a month on voice actors. I did not have an infinite budget and wanted to monetize ASAP or shut
this thing down. Sooner or later I had to send out a sales email offering to pay for Premium service. The offer was
“_TOP 3 articles narrated on weekly basis + 1 free weekly article_”. Only 1 person gave me his/her credit card
information . 1 is better than 0\. I smiled 🙂 Time was running, I could no longer sustain spending $ on voice actors
and do all the weekly newsletters, article selection, audio editing and uploads. I gave myself time till the end of
July, to find a way to break even or shut down. And well, I had to shut down.

Here is some calculations that i did to estimate what it takes to break even. All numbers in bold are variables, that I
played with to see what happens to the **Profit** cell.

![excel love](https://cdn-images-1.medium.com/max/2000/1*PIB2aaZosYvB5Z5thlWu-Q.png)

### Lessons learned 🤓

- Stay true to yourself and build what you yourself want. Don’t waste time for indirect routes and stop looking for
  shortcuts.
- There are a ton of ways to validate an idea without writing a single line of code. Even when you think you should, try
  your best to find an off the shelf solution. Case in point: did not build a backend — just a landing page. Did not
  build mobile app — relied on existing podcast apps to deliver content.
- Know your funnel! Think in terms of funnels and apply them everywhere. I never really thought in terms of funnels
  before Andrey forced me into it. When you know your conversion rates, you can suddenly start planning actionable
  targets all the way to break even. Example: you calculated that you need 100 paying customers at 9.99 a month to break
  even. You learned your conversion rate is ~0.5% into a paying customer per month. Therefore you need to drive 20,000
  quality leads to your landing page to eventually hit monthly break even.
- Talk to your customers. Again and again. Talk to them all the time. Get their feedback and quantify it on as many
  decisions as you can.
- A popular idea and a business idea that makes economic sense are not the same.
- Markets worldwide differ. What might work in the USA, might not work in Europe or Asia.
- On the state of Text-To-Speech. When we sent some lower quality narrations, our users thought it was synthesized. I
  average human would be able to distinguish between robotic and human voice. The line gets more and more blurry. People
  also seem to have very high hopes and expectations from AI, since they confuse humans voice (non-North American
  accent) with a TTS output.

### Thank you ❤️

Special thanks to all who helped me with ReadByHumans along the way! Close friends, Startup School batch members, people
who reached out and offered feedback. Thanks [Andrey](https://twitter.com/AndreyAzimov){:target="\_blank"} for kicking
my ass. Thanks, [Adelina](https://medium.com/@adelinapeltea) and
[Ritesh](https://medium.com/@ringular){:target="\_blank"} for reviewing my writing. I omitted too many worth names here,
as the article was already too long. Thank you if you one of the subscribers of ReadByHumans and chatted with me over
email and skype!

### Stay in Touch! 

Hope this was useful! If you enjoyed this read, please clap below and share with friends. You can also reach me on
twitter [@ksaitor](https://twitter.com/ksaitor){:target="\_blank"}. If you’d like to save this article, I’ve prepared a
downloadable
[PDF for free here](/images/readbyhumans-postmortem/How%2520I%2520in-validated%2520a%2520business%2520idea%2520in%25203%2520months%2520with%2520little%2520code%2C%2520while%2520traveling%2520the%2520world%2520-%2520by%2520Raman%2520Shalupau%2520%40ksaitor.pdf){:target="\_blank"}.
You can engage me on freelance basis, if you need some js, react, node, ui/ux or growth help. Ready to help! 👋
