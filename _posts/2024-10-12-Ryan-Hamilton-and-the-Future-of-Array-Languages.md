---
title: "Episode 90: Ryan Hamilton and the Future of Array Languages"
date: 2024-10-12 00:00:00 +0000
episode: 90
keywords:
- array-programming
- array-languages
- q
- k
- kdb+
- open-source
- time-series
mp3-url: "/assets/audio/episode90.mp3"
episode-type: full
explicit: "no"
block: "no"
layout: podcast
excerpt_separator: <!--more-->
redirect_from: "/episodes/episode90-ryanhamilton"
---
May you live in interesting times and the possibilities they represent. Ryan Hamilton of TimeStored discusses the adaptations that may be required.
<!--more-->

**Host:** Conor Hoekstra

**Guest:** Ryan Hamilton of TimeStored

**Panel:** Stephen Taylor, Bob Therriault, Adám Brudzewsky, and Marshall Lochbaum

---

[Original episode on ArrayCast](https://www.arraycast.com/episodes/episode90-ryanhamilton)

## Show Notes

Array Cast -  October 11, 2024

Thanks to Bob Therriault for gathering these links:

**[01] 00:01:20**

- [APL/J/K Tokyo Meetup October 21](https://www.meetup.com/apl-j-k-meetup/)
- [Ryan hamilton](https://www.timestored.com/about)
- [Morgan Stanley](https://en.wikipedia.org/wiki/Morgan_Stanley)
- [First Derivatives](https://firstderivative.com/)
- [TimeStored](https://www.timestored.com/)
- [Ryan's Blog Future of Kdb+](https://www.timestored.com/)
- [/b/the-future-of-kdb/q Programming Language](https://en.wikipedia.org/wiki/Q_(programming_language_from_Kx_Systems))
- [KX.com](http://kx.com/)
- [kx.com](https://kx.com/)
- [ZX Spectrum computer](https://en.wikipedia.org/wiki/ZX_Spectrum)
- [Basic Programming Language](https://en.wikipedia.org/wiki/BASIC)
- [IBM PC](https://en.wikipedia.org/wiki/IBM_Personal_Computer)
- [Jonny Press Episode 85 on the ArrayCast](https://www.arraycast.com/episodes/episode85-jonnypress)
- [C++ Programming Language](https://en.wikipedia.org/wiki/C%2B%2B)
- [Java Programming Language](https://en.wikipedia.org/wiki/Java_(programming_language))
- [RoboCode](https://robocode.sourceforge.io/)

**[02] 00:09:45**

- [Lib Gibson Episode 35 on the ArrayCast](https://www.arraycast.com/episodes/episode35-lib-gibson)
- [Kdb](https://kx.com/products/kdb/)
- [Kdb+ tutorials](https://www.timestored.com/kdb-guides/)
- [Q Studio](https://www.timestored.com/qstudio/)
- [DuckDB](https://en.wikipedia.org/wiki/DuckDB)
- [Arthur Whitney](https://en.wikipedia.org/wiki/Arthur_Whitney_(computer_scientist))
- [Clickhouse](https://en.wikipedia.org/wiki/ClickHouse)
- [Leslie Lamporte](https://en.wikipedia.org/wiki/Leslie_Lamport)
- [Leslie Lamporte's State the Problem](https://lamport.azurewebsites.net/pubs/state-the-problem.pdf)

**[03] 00:19:50**

- [Inverted Tables](https://code.jsoftware.com/wiki/Essays/Inverted_Table)
- [QuestDB](https://questdb.io/)
- [JavaScript Programming Language](https://en.wikipedia.org/wiki/JavaScript)
- [Python Programming Language](https://en.wikipedia.org/wiki/Python_(programming_language))
- [PHP Programming Language](https://en.wikipedia.org/wiki/PHP)
- [C Programming Language](https://en.wikipedia.org/wiki/C_(programming_language))
- [Unix Operating System](https://en.wikipedia.org/wiki/Unix)
- [Richard Feldman Why isn't Functional Programming the Norm](https://www.youtube.com/watch?v=QyJZzq0v7Z4)
- [Roc Programming Language](https://www.roc-lang.org/)
- [Elm Programming Language](https://en.wikipedia.org/wiki/Elm_(programming_language))
- [Rust Programming Language](https://en.wikipedia.org/wiki/Rust_(programming_language))
- [Swift Programming Language](https://en.wikipedia.org/wiki/Swift_(programming_language))
- [Kotlin Programming Language](https://en.wikipedia.org/wiki/Kotlin_(programming_language))

**[04] 00:31:30**

- [SQL](https://en.wikipedia.org/wiki/SQL)
- [NumPy](https://en.wikipedia.org/wiki/NumPy)
- [Polars](https://pola.rs/)
- [APL Programming Language](https://aplwiki.com/)

**[05] 00:45:08**

- [Nick Psaris Episode 42 on the ArrayCast](https://www.arraycast.com/episodes/episode42-nick-psaris-q)
- [Fun Q](https://www.amazon.com/dp/1734467509)
- [Q Tips](https://www.goodreads.com/book/show/25221469-q-tips)
- [Ryan's Blog Kdb+ 5.0](https://www.timestored.com/b/kdb-5-0-the-roadmap-ahead/)
- [Stephen's talk in Madrid](https://www.meetup.com/everything-everywhere-all-with-kdb-q/)
- [Postgres](https://en.wikipedia.org/wiki/PostgreSQL)
- [parquet](https://pypi.org/project/parquet/)
- [MATLAB](https://en.wikipedia.org/wiki/MATLAB)
- [MATLAB Episode of ArrayCast](https://www.arraycast.com/episodes/episode79-matlab)
- [k Programming Language](https://aplwiki.com/wiki/K)
- [Dyalog APL](ttps://www.dyalog.com)
- [TypeScript Programming Language](https://en.wikipedia.org/wiki/TypeScript)
- [Klong Programming Language](https://aplwiki.com/wiki/K)
- long

**[06] 00:58:11**

- [John Earnest Episode 43 on the ArrayCast](https://www.arraycast.com/episodes/episode43-john-earnest-decker)
- [John Earnest Episode 41 on the ArrayCast](https://www.arraycast.com/episodes/episode41-john-earnest)
- [Lil Programming Language](https://beyondloom.com/decker/lil.html)
- [Decker](https://beyondloom.com/decker/index.html)
- [HyperCard](https://en.wikipedia.org/wiki/HyperCard)
- [Pulse](https://www.timestored.com/pulse/)

**[07] 01:02:20**

- [HTML](https://en.wikipedia.org/wiki/HTML)
- [CSS](https://en.wikipedia.org/wiki/CSS)

**[08] 01:08:14**

- Contact AT ArrayCast DOT Com

<details markdown="1">
<summary><strong>Transcript</strong> (click to expand)</summary>

Transcript

Transcript prepared by

Bob Therriault

Show Notes

00:00:00[Ryan Hamilton]

I was going on a wonderful ski holiday in Innsbruck. I was looking forward to skiing over a few days. COVID happened, everything locked down. You can't go anywhere. What do you do? You write a free version of q in Java.

00:00:19[Music]

00:00:28[Conor Hoekstra]

Welcome to episode 90 of ArrayCast. I'm your host, Conor. And today with us, we have our four panelists and a special guest who we will get to introducing in a couple of minutes. But first we're gonna go around and do brief introductions. We'll start with Bob, then go to Stephen, then go to Adám and finish with Marshall.

00:00:41[Bob Therriault]

I'm Bob Theriault and I am a J enthusiast.

00:00:44[Stephen Taylor]

I'm Stephen Taylor, APL and q developer. And I'm recording here from the Dyalog 24 conference in Glasgow.

00:00:54[Adám Brudzewsky]

I'm Adám Brudzewsky and I'm there with Stephen in Glasgow too. So you're gonna be enthusiastic about APL this week.

00:01:00[Marshall Lochbaum]

I'm Marshall Lochbaum. I am best known for BQN, I suppose, but I've worked with I and J and occasionally dabbled with k.

00:01:09[CH]

And as mentioned before, my name's Conor, the host of the podcast, array language enthusiast at large, big fan of all the array languages and very excited to talk to our guest today, who, as I mentioned, we will introduce after a couple of short announcements. So first we'll go to Adám and then we will go to Bob.

00:01:23[AB]

So the APL/J/K group out of Tokyo [01] is having an online event and it's the 21st of October, so coming up soon. And we'll leave a link to that. It looks like they're having an interesting agenda.

00:01:41[BT]

And my announcement is when you hear this episode, the next two episodes of the Arrayast will be special episodes. There'll be a slight change in format and you will hear Ken Iverson's voice on these episodes. So stay tuned for that. And then we'll be back with a regular format after that. But there are upcoming two episodes that I think you'll wanna hear.

00:02:07[CH]

Awesome, so I guess links not for the upcoming episodes, but links for the meetup. Be sure to check the show notes. And with those announcements out of the way, I am excited to introduce our guest for today, Ryan Hamilton. He has been in the industry for a decade or two now and has worked at a plethora of companies, including some you've heard of, Morgan Stanley, Citi, as well as First Derivatives, a company that has obviously come up on this podcast before. And he popped onto our radar after he posted a blog and the title of it was The Future of Kdb+. And I should mention that he is the co-founder of TimeStored, which I'm sure we're gonna get into. I got lost in the website of TimeStored because I had not heard of it before, but they have something called q Studio, which I'm sure is gonna come up. But the reason he popped onto our radar was because of this blog. It was talking about kind of his experience with Kdb+ and sort of where it stands next to some of the competing technologies. Very provocative. I think it was posted on Hacker News and it got a lot of discussion. I could be wrong about that. Maybe it was another orange website, but at this point, I will throw it over to Ryan. Maybe you can walk us through how you ended up in Kdb+ land and the Array Language land. So go back as far as you want to your schooling or your first programming language. We'll get your history and then we'll hop into this blog and everything about TimeStored and q and your opinions on the technologies.

00:03:35[RH]

Hey, Conor, thanks. Yeah, well, I guess the first thing I'd say about that article, ironically, it was to stop people asking me about Kdb. So it's kind of had the reverse effect. But maybe if I answer a few questions here, then people will stop asking me, right?

00:03:51[CH]

I'm sure that's the result of this episode.

00:03:55[RH]

As long as you promise me that. Go back to when, how far back should I go?

00:03:57[CH]

As far as you want. We've had people that have gone back to like age six when they got their first Commodore 64. Take us back to whenever you feel like is a good starting point.

00:04:11[RH]

Okay, my family couldn't afford a Commodore 64. That was too advanced. We got a Spectrum, ZX Spectrum. I think I was probably seven or eight. My mom got it for Christmas. Yeah, I think so. I have no idea how she knew that we would benefit from this at all 'cause we'd never had computers in the house. I initially played the games, but on the keyboard were like programming language words. And I kind of wondered what the heck those words were. And then when you looked in the manual, it turns out they were a programming language BASIC that came on the machine. And after a lot of trial and error, which you know, it's like an eight year old has a lot of free time, I eventually managed to get something kind of running. And I think that was pretty much me hooked. Again, my mom probably when I was about 10 or 11, then got us a PC, which was a massive upgrade, lot better games. And I moved from BASIC to QBasic, which seemed amazingly fast and had good visualization. And then that kept me pretty happy for a while, especially the games. And I think I thought I should get serious about programming. So, you know, it's funny, I listened to your podcast with Jonny and he hated programming languages. I thought I should get very serious and I went to C++. And I had this big, massive, thick book that I'd walked to get at the library. And it was terrible. It was so painful. And then I got something like C++ for dummies. And that kind of gave me a little hope. But no, after like a year, I gave up. And that was me for a few years 'cause it was just, it'd been so painful. Plus I think I was like 15, 16 and I just had better things to do. Like, you know, go outside and have fun. (laughing)

00:05:47[CH]

Yeah, that makes sense.

00:05:48[RH]

Yeah, I don't think I touched programming again until, I knew I still wanted to do computers. So university, typical kind of computer geek, chose to do computer science. I think it was even more typical, similar to Jonny's experience. Like there was 95 guys in the class and most of them were using Linux terminals. And then I got introduced to Java and that was my first in C++. Like I'd done some internet stuff, some HTML. And again, it was okay, but I didn't really get the point. And I think what changed it for me was this thing called Robocode. It's kind of cool. You can build little robot tanks that go off and battle other people's little robot tanks. So you have to program the movement and the scanning to find the enemy and the attacking. And it's kind of like when I find something to do with language, that's when I find it useful. So yeah, I pretty much stuck with Java during uni.

00:06:37[CH]

Was Robocode, was this a thing that was in Java as well?

00:06:40[RH]

Yeah, oh, it has a user interface that shows your little tank moving around and scanning and you can throw the speed up really high and watch your tank run and shoot the other tanks. And you can do tournaments and stuff. That's the part that appealed to me rather than the intricacies of Java, which is a bit of a speed bump getting started, setting up an IDE and running and stuff. And yeah, like it's always been about solving problems for me. And at university, I was at university around the time when Poker got popular. So I really enjoyed Poker. I managed to convince our kind of group project should be a Poker server. And then for my master's, I was neural networks were a thing. So I used neural networks to model opponents and it was all in Java. And then uni ended and my friends and I who had worked heavily in Poker decided to make Poker bots to play online. That's a much longer story. I won't go into that one. But suffice to say, eventually that didn't kind of work out and I then joined First Derivatives. The short version of that is that my friend recommended me and he got a pool table and I got a job. So we were both happy, I guess. He only told me after that he was getting the referral, but he did let me play on the pool table. So I can't really complain. So that then is how I got into Kdb. Basically, First Derivatives, I think I was one out of 40 that started at the time. If I remember right, the only person that was computer science. So they had me doing Kdb and I hated it. I mean, I was like, this thing is useless. Where's the debugger, the profiler, the ability to pause it, the library. But after a year of being forced and I used to begin to use it for some of the problems in jobs, I began to see how it was actually very useful for the problems we were solving. And that kind of kicked off, as you say, and I would like to say one decade of work, maybe slightly over, definitely not two decades. Building data platforms and working with quants to build Kdb-based applications for the last 10 years has been a lot of the work I've been doing.

00:08:39[CH]

And so your experience coming into First Derivatives and learning Kdb+ on the job was coming from being a Java developer.

00:08:46[RH]

Yeah, and then I kind of hated it. So I found my own job doing Java and kind of said, guys, can you send me to do Java? But then I kind of missed Kdb right after that 'cause I was writing Java and I was like, this is very verbose. Why can I do it not just shov in a lambda? And they didn't have the RL notation, like it took another 10 years for that. So I was like, this is really hideous. So I then went back to Kdb. And in fact, I was due to receive training to refresh it 'cause I'd been working in Java for a year. But Nathan, who is an absolutely excellent Kdb trainer, had a slight accident. And then they said, well, you won't be receiving the training. We need you to give the training in about two weeks' time 'cause Nathan can't give it. So I then had two weeks to learn Kdb enough to give training in Kdb. I'm sorry to the people that received that first lesson. I'm sure I delivered the material, but if you had questions, they probably were not answered very well.

00:09:44[BT]

Actually, there was a story that we'd done with Lib Gibson [02] where she was in the same situation with IP Sharp and she was new to IP Sharp. And Ian Sharp came by one day and said to her, well, she was talking to him and she said, are there any courses being given in APL? And he said, yeah, there's one in Ottawa. And she was in Ottawa. He said, there's one in Ottawa next week. And she said, oh, can I take that one? And he said, well, you're giving it. (both laughing) And so she was in the same situation.

00:10:14[RH]

It's a good motivator.

00:10:15[BT]

She said it was one of the best courses she ever gave because she wasn't trying to over-explain everything. She was just giving them answers to what she knew. And if she didn't know, they would try things. And she said she thought it was probably her best course.

00:10:27[ML]

Well, and she said she had no APL experience. So maybe your problem was that you were actually too experienced to give the course.

00:10:39[RH]

That definitely was not the case. (both laughing) But the material was fresh in my mind. So yeah.

00:10:43[CH]

So I guess maybe tell us about TimeStored and how that came to be. So you were at First Derivatives for a while. I think you worked a couple other places and then you decided to co-found this, I think it's a consulting company or I'll let you explain what TimeStored is.

00:10:59[RH]

Yeah, so I had really enjoyed my time at First Derivatives. They gave me a great opportunity to travel. According to my Amazon history, I was at 13 different addresses in two years. I wanted to stop living from suitcase and I wanted to own stuff, especially a bike. 'Cause I bought like two bikes and I had to give them away every time. I was like, I quite like those bikes. So yeah, I decided to leave and get more permanent jobs. I also knew that I didn't want to rewrite the same code always. And there were some problems that I wanted to solve that if I went straight in the bank, I couldn't do. They wouldn't necessarily let me write QStudio. They wouldn't let me put a lot of training articles up. 'Cause yeah, like 12, 13 years ago, there was no, well, there was very few training materials. And yeah, I wanted to try a few different things. Definitely not consulting 'cause you won't believe the human resources of having to manage people, especially in that way. But for the first few years, probably most of what I did was deliver training. So I delivered training at various banks, I had TimeStored. I got a bit bored of delivering training. I did get better at it. It's handy when you know the questions they're gonna ask and the parts they're gonna stumble on. So I converted it to a fully online course. And it was probably the only online Kdb course for like five years, which attracted quite interesting people, the ones that are willing to do online. So that was interesting. I had wanted, I was coming from Java. So I wanted more of an IDE. So I built QStudio mostly for myself. And then I gave it to a few others. Charlie was kind enough to provide some initial feedback and bug reports, especially on the Mac since I didn't have one. But I still get some from Mac users today. So yeah, I mostly build it for myself, but I find it almost everywhere now. It's quite satisfying when you're randomly walking around the trading floor or somewhere and you notice it over someone's shoulder and you're like, "Oh, that's me." That's very fulfilling. Definitely, it let me do some of those projects. But then in between, I was largely working and building big data platforms in banks, Kdb, pretty much always Kdb, whether that's market data. So like you said, I was quite privileged to work at Morgan Stanley for a period where they probably have the largest system. So it's quite a good opportunity to learn from it and see after five or 10 years where the platform goes and spreads to and the good parts and the bad parts. And then I basically got to write a new one at a different place and a new one again at another place to try and fix what I hadn't done quite right before. That's been good.

00:13:28[CH]

And so QStudio, you said you were kind of working on in the background. And so is that, 'cause when I was poking around on the website, that seems like that's, you just give that away for free. Is that accurate?

00:13:43[RH]

It's now free for everything but Kdb and it's free for all personal use. The people paying for it, the banks and stuff is what allows me to continue developing it. Otherwise I just couldn't really justify the time to do it all or to fix some of the more annoying parts. It's funny, I thought QStudio was done, after like two years, I was like, oh, okay, well, that's pretty much everything you need. And then four years ago, I had a revelation that it wasn't done and I should make it work for all databases. That was really good. It was good to interact with the different ones, get feedback from them. And then I thought it was done again. And I was like, and then like last year or two years ago, I was like, well, if it's for data analysis, I should probably help people perform that analysis, like perform pivots and stuff. So I did a lot of reworking, building DuckDB 'cause you can do your analysis within that and see if stuff look like, and now I think it's done again. But I'm not saying why Arthur, waits X years and then rewrites from scratch cause you think you're done, but there's really, there's a whole set of other problems.

00:14:49[CH]

See, and so maybe this is me, predicting and I could be wrong about this, but you having to add support for all these different databases, you mentioned DuckDB. And I remember reading the article, you'd mentioned a couple others, ClickHouse, et cetera. Was that what started to fill in the information? And this is hopefully how we'll kind of transition to the future of Kdb+ 'cause in that blog, I'll let you explain it, but you compare with a bunch of other technologies that didn't exist 15 years ago when you were initially first starting with Kdb+.

00:15:23[RH]

To touch on the blog, and then I could come back with you too, but so I've kind of not read, like certainly Kdb hasn't been my main thing for like at least two years. One of the reasons QStudio is mostly free is I've been working on a new product called Pulse. It generates a lot more and QStudio is kind of like the free sampler of the individual version of what you can then get in a hosted HTML5 version. So yeah, I do interact with a lot more people, but I haven't written Kdb as my main job in like two years. But I always like to start with, like what's the problem you're solving? There's a great article by like Leslie Lamport that goes into this that I'm obsessed with quite a bit, but people at KXCon and stuff, it's great to catch up with them, but they always ask me, "Well, Ryan, what do you think of Kdb? Where's it going? What's it doing? What do you think of where the kind of ecosystem is going?" So I guess it's probably worth recapping some of the article where there's probably four, three or four main problems I've used Kdb to solve in like a period of 10 years. The number one is historical market data, where you're storing level two tick data, you know, multiple petabytes, quite often spread geographically, collecting from various exchanges and bringing it back to allow quants, traders or other applications in the firm to get detailed pricing data and perhaps to help them go levels above that to build trade analytics and stuff. So that's use case one, huge database for time series data. Use case two is local quant analysis or probably what you guys do, you know, on your own desktop when you're munging data, converting it, extracting it, and then spitting out some kind of report or something like that. And then use case three, which is probably where something like Kdb actually is the best solution by far, but it's a hard sell is real time streaming analysis combined with historical. 'Cause everything's the same table and you've got the IPC format, it's extremely powerful to do something like TCA, transaction cost analysis, where you're taking in the latest market prices and spitting out a more advanced analysis based on that in real time. Like Kdb is absolutely beautiful for that and extremely fast. And then I would tack on, 'cause I'd heard some of your previous podcasts, one that I do and it sounds like you guys do is shell scripts, you know, kind of like a bash replacement. It's very useful for mildly cross-platform, but also just nicer than bash. And that's the kind of four use cases I was spelling out and then saying where I think each one's going to go to. Did that cover the article or did I?

00:18:07[CH]

Yeah, I think it did a great job. And do we wanna, where do you wanna go next? Do you wanna talk about kind of some of the technologies that are out there that are competing now with Kdb+ or do you wanna talk about more just Kdb+ specifically and how you think they're faring today? I'll throw it over to you on where you wanna go next with it.

00:18:26[RH]

Well, the article had been to stop people asking me, but yes, ironically, it got a lot more interest and caused more people to ask me. I think it's probably a little unfair, the title was unfair, to pick on Kdb. I guess the reason I did slightly want to nudge KX because I think what's changed, and this is for all array programming languages and languages in general, the environment we are in today is very different than 10, 20 years ago. Like the internet, Google, AI, how developers operate, how developers find language. Like, you know, remember I said, I went to the library to get a large book. No one is doing that. That book is out of date. Anytime you write a large book. And if I'm being harsh, which, you know, if it's something you love and you've operated with for 10 years, you can be, I don't think they've done enough to keep up. And I would like to see them do a little more. I guess that would be my angle. But on the flip side, like we are engineers, right? And we can use various tools. So actually for us, the changes that are coming, I think we should be excited about and we should actually embrace them. 'Cause okay, currently no one is coming forth with a wonderful new array language, but they have caught on to column-oriented storage, which is basically the underlying of most of the languages that we use. [03] And like if DuckDB or Clickhouse or whoever comes out with better tools, that's tools I can use to do stuff. It's also an opportunity. And like, I talk to them a lot because of the work with Pulse and QStudio to try and influence them to give us some of those array benefits. We may not get the most beautiful form that we would like. Like Conor, I think you talked about NumPy and not being the nicest with the np. We may not get the most beautiful one, but I do think the landscape is changing in such a way that smaller languages may not survive in a viable commercial form. I'd be interested to hear what you think about that, but 'cause you probably give it a lot more thought than me.

00:20:26[CH]

Well, I mean, before you flip the interview script on me, (laughs) maybe I wanna dig a little bit deeper when you're talking about not keeping up. Like, so I'm not sure if you wanna drill down on a concrete example or just talk at a high level, but like when you mentioned, you know, DuckDB or ClickhouseDB or QuestDB, are the things that you're mentioning like tooling things that ship with those kinds of databases or are they more like, you know, they in this one area, they are kind of have the same functionality, but it's just that on top of that, they've added something else that Kdb+ doesn't have. Is it more like a language feature level or is it more at a tooling level when you're talking that like they're not keeping up? Like, are there things specifically that, you know, you really miss when you go back to Kdb+ after having worked with some of these other databases and technologies?

00:21:19[RH]

Let's try to begin at a lower level and I can see if I can bring you on the journey and if you'll either agree with me on the journey or disagree, okay?

00:20:26[CH]

Sounds fantastic.

00:21:27[RH]

I'm going to put you in a very painful position. We're going to talk about non-array languages.

00:21:32[CH]

Uh-oh.

00:21:33[RH]

They do exist and I don't think we look at them enough.

00:21:36[CH]

But does it start with "huh" and end with "askle"? 'Cause if that's the case, it's okay.

00:21:40[RH]

No. So I said what I love about program languages is solving problems and not everyone's gonna let you use niche to solve problems and they may not be good to solve problems. So I've been writing TypeScript largely for the last two years. I thought JavaScript was horrendous language. In many ways it still is. But since the 10 years I looked at it last, they have thrown a million monkeys at it and it has got hundreds of times better just because they had so many people making crazy things that they discovered how to make it better due to the amount of resources they have. Now imagine if you could store that amount of resources at a better language to begin with. Okay, I guess to step back, right? I would say commercially, and there's a poetic beauty to languages, but commercially and popularity-wise, Java, Python, PHP, JavaScript has been successful. Would you agree?

00:22:37[CH]

Yeah, I think you mentioned all top 10 popularity programming languages there. So I don't think anyone would disagree with those regardless of their feelings towards the language. And for the listener, all the heads that I could see were I think nodding in agreement.

00:22:52[AB]

Well, did you say they were successful commercially?

00:22:54[RH]

Commercial and popularity.

00:22:56[AB]

Popularity, yes, but commercially, surely not really any money is being made from the people who implement, design, develop these languages.

00:23:05[RH]

There's a lot more being paid to them than probably the developers of APL and J, and there's a larger number being paid to develop the languages.

00:23:15[ML]

Yeah, I mean, they don't license their implementations in the same way, but the money is flowing.

00:23:19[CH]

Yeah, if you're probably gonna measure on a different, like 'cause most of the language popularity sites are just about like, you know, GitHub metrics and Stack Overflow metrics and Google Trends. But if you were also to measure, you know, annual salaries being paid for writing in language X, it would probably look something very similar to those rankings, even though we don't have that data, obviously.

00:23:44[RH]

Okay, so assuming you agree on the languages, what do you think caused them to be successful?

00:23:50[CH]

Well, that is a rabbit hole question for sure. (both laughing)

00:23:55[AB]

A lot of people have been thinking about and blogging about this, on what makes programming languages successful. Nobody has figured out what it is yet. There's nothing in particular these have in common.

00:24:08[ML]

But there is a very good answer for JavaScript. The others are more difficult.

00:24:12[AB]

In JavaScript, but it's not that particular language. It was the language that was put in that position. Any language could have been put in that position, good or bad, and it would have had that same kind of success. Likely, we can't test this, but it's likely.

00:24:17[ML]

Yeah, well, I mean, I think there's some quality threshold, but it's below even what JavaScript hit.

00:24:32[AB]

Right, it could have, I mean, what JavaScript's position could have been occupied by a language that would be radically different, and it would have still taken the same, it would still have seen the same kind of uptake because of that unique position it was put into, and there's unique circumstances of the time. And so I don't think there's anything particular about JavaScript that puts it in that position. Could kind of say the same thing about C. C took a path together with Unix, the same way as JavaScript took its path to go with development of web browsers. And the language that was in conjunction with Unix could have been very different.

00:25:17[RH]

So can I suggest the feature you're describing over all those languages would be a killer use case where you have no other choice but to use that language?

00:25:28[AB]

Yeah, it's piggybacking on the particular no choice scenario, I would say.

00:25:35[RH]

Yeah, Python for web development for reasonable people, not Python, PHP, Python for kind of data analysis, Java for cross-platform, you had no choices really. JavaScript for internet stuff.

00:25:48[AB]

I don't know, I think a lot of those, there are plenty of choices, and there were plenty of choices, it wasn't clear which one would win, and then one gets a bit bigger, and then people tend to use the one that's bigger 'cause they've got more options, more libraries, so on, and then that goes even bigger.

00:26:02[BT]

I think actually that's the key point, Adám, is when you, there's a critical mass. So there's the point at which the languages are introduced so there's an open field and there's an opportunity, and you wanna hit the right spot at the right time, and that's somewhat chance, but maybe somebody's thought about that, I don't know.

00:26:19[CH]

I don't think there's anything particular about Python that makes it more suited as a language for data analysis, or particularly about Java that makes it more suitable for cross-platform development.

00:26:31[ML]

I mean, I think you're stating this very strongly. I would disagree mostly about C, and definitely Python and Java somewhat. I mean, I think these are all, these do have some serious design consideration, and they fit into the areas where they're applied very well. I mean, so Python, the point is that you're able to, even as somebody who's not interested in programming specifically, you're able to pick it up very quickly and get stuff done with it, and I think most, the vast majority of other languages are not as good as Python at that.

00:27:04[CH]

I will say, to echo what you're saying, Ryan, there was a talk that immediately popped into my head when you asked this question that, of course, has caused this chaotic discussion, that is by Richard Feldman, who's the creator of the Roc language, and worked with the Elm language before, and it's called "Why Isn't Functional Programming the Norm?" But a better title for it would have been "What Makes a Programming Language Popular?" And he kinda has a couple different reasons, but the main thing he comes up with is what you said, these languages have a killer app. And yes, you can find counterexamples, like what is Rust's killer app? You know, it's just a better C++ with memory safety, I guess memory safety is the killer app, but not every language is gonna have this perfect answer to this question, but a lot of languages do. And even if there was a better language for it, sometimes timing is important, and I would agree with your answer that a lot of these languages, especially if you look at the ones that are tied to Swift for Apple and iOS, and Kotlin for Android development, these languages, sure, you can comment on whether they're good or bad, but they were tied to a mobile device, like app writing language, and now they're like top 20 languages, wouldn't be surprised if they become top 10 languages. Anyways, we'll let you fill in, because I feel like you had more to say after the killer app answer.

00:28:25[RH]

No, it's great, you just actually hit a few other points. Marshall's point about symbol to start.

00:28:33[ML]

Well, and that's for Python specifically. I don't claim this of C, of course.

00:28:37[RH]

Yeah, but well, here's the thing. I'm not trying to define what is the actual answer to what makes a programming language popular, 'cause we don't actually need that. We just need to find what is likely to. We're not trying to find the exact formula of the combo. So if I started listing out some, it would be killer use case, simple to start, open source, large libraries, strong modules, instant feedback, strongly typed. These would be the attributes that are kind of common. And we're not trying to find the exact combo. I'm just trying to say, if your thing has these attributes, you're more likely to succeed. So you should probably do some of them. It may not make the difference for yours, but you should be experimenting with these areas to try and get it to make a difference to your language. I'm not sure where I was going after that. Okay, so we had killer use case, symbol to start, free/open source, and large libraries. Would you roughly agree with those attributes? Not as the definitive answer to how to make it popular, but as attributes very likely to make it?

00:29:40[CH]

Yeah, I would agree, yeah.

00:29:42[BT]

Yeah, I mean, the other thing you mentioned previously was typing, which is something that most of the array languages aren't strongly typed. So is that something that would hold them back?

00:29:51[RH]

It's something I would like to see. I think what array languages don't, or even most programmers don't do a good job of, including myself, is looking for ideas from elsewhere and using them in their world. There's probably more people look at q and J and BQN than go look at old-school JavaScript or something like that. And there's more value in seeing something diverse and totally different. I mean, that's what we try to tell people, array languages, right? So we should go do the same. Yeah, that basic, oh, that's terrible, I'm not gonna look at it. Okay, I'll look at it. Oh my God, this is why they like it. You may learn more from that kind of diverseness. We could certainly learn more by making the language popular, I think. And unfortunately, I think the reality is, as I think about it, some of these trends are kind of against array languages. Like, let me give you two trends I kind of thought of. One attribute of successful languages, to put the theory out there, is how Google-able it is. Like, that's been a huge change since the year 2000. People Google to get the answer to a problem. Like, if you say, what is the first in a list? And let's say in SQL, it's list first brackets, that's gonna turn up fairly easy, but an array language will not turn up very easily. And you've probably seen this.

00:31:11[BT]

Well, certainly with the one letter name of a language, J is at a disadvantage, and we've known that.

00:31:17[AB]

So is C.

00:31:18[RH]

And like, I'm seeing that trend get worse, 'cause I'm using AI to generate SQL [04], and attempting to use it previously to generate Kdb, but it can't, 'cause it kind of needs a verboseness to find it. And like, I guess what languages are trying to do, if they're being really good, is slightly recreate how people think. Like, that's why you'll find some people naturally convert to array languages, whereas other people may think procedurally. And if AI is recreating slightly human thinking, it may show us that it needs fuller words. For most people, they kind of understand it. That's what I mean, that could be one trend working against this, that we may need to try and compensate for.

00:31:52[AB]

Mm, that one is actually testable. If you ask the so-called AI, or should we call them large language models instead, to generate a wordy language that's much less popular, and therefore much less code to have ingested, then I'm not sure it goes very well either.

00:32:09[RH]

I would love to see real human tests of taking five people. Like, I've given Kdb training, and I can see. So actually, to Marshall's point about easy to learn, that's a massive trend you've seen in languages. The ones with a learning slope that are gradual and gentle at the start have really taken off in popularity. And they throw all the complexity at the end. Or they throw an entire new language, like NumPy or Polars at you on top, that is totally different if you want speed. But the initial slope of learning is massively gradual. And I think array languages would benefit for thinking, how do we make that slope more gradual?

00:32:48[BT]

And I guess the question is, how do we make it more gradual for who? Because, or whom, I suppose. Because there's always anecdotal, I guess, stories about how easy it is to teach people who haven't had experience with computers an array language. Because you have some of the things that you mentioned before. You've got the immediate response, the REPL happens. A lot of the terms that they might be using with numbers, the addition, the multiplication, become really obvious. And they're not already programmed to think in their heads about loops. So they don't have to unlearn that process. But that's just a case of what I think you're talking about is finding a way to train people who already know a little bit about computers and already are thinking in loops, trying to get them away from thinking that way. Because that seems to me the big divide, the big paradigm shift, between thinking about procedural languages and thinking about array languages.

00:33:45[AB]

Yeah, I think it depends on how the person is. I'm in the middle of revising a bit my theory about people having studied computer science and what traditional programming languages have something been broken in them that it makes it harder for them to adopt an array language way of thinking. We recently hired somebody new to be an APLer at Dyalog. And I believe she has had most experience before with C++, but she has also had some MATLAB. And she's picking up APL better than anybody has ever taught APL before. But maybe we should also add here for full disclosure that she just got her PhD in computational physics. So the fact that she had learned other languages before didn't seem to be an impediment, but somebody who chooses that kind of education and field of study maybe has the mindset that is the right one for picking up one of these languages. And maybe our target audience shouldn't or couldn't be the broad one to gain much popularity. Maybe in the very nature of these languages, they cannot be wildly popular because then there wouldn't be these languages.

00:35:14[RH]

I worry you need to be widely popular to survive now. Keep in mind what I said about learning JavaScript and that 10 years later it was TypeScript with MPM and modules and a whole ecosystem around it. 20, 30 years ago, APL systems did not plug in to many other things. Nowadays, when you're in a bank or any large firm, there are 20 different systems. There are 10 business intelligence tools. There are multiple formats, and you have to work with all of them and in those scenarios. So you need somebody to care to those parts.

00:35:47[AB]

Yeah, we're working on these kind of bridges and foreign function interfaces and so on. But I don't think that really changes much. If it requires a certain type of person who is in the minority, that doesn't mean it can't survive. We could take it from any field and we can't all do the same kind of job. I think it takes a very special type of person, for example, to work as ATC, to be controller for airspace. Special type of nerves, special type of attention. I would not want to try my hands on that kind of thing at all. So we say, well, I mean, it's such a small part of the population that has that mindset. That kind of job is not gonna survive. But we need the people at the ATC, right? Maybe it's the right thing for those people to pursue that kind of profession. And the same thing goes for teachers in school. It requires a very special mindset to be a teacher in school, and that everybody can handle that. Not everybody has that kind of nature.

00:36:49[RH]

You're starting with the person. I think you need to start with the problem. We don't need computer programmers. And we don't need APL programmers. We don't need Java programmers. We don't need JavaScript programmers. But that's why the killer use case was one. What's the use case you're gonna continue solving better than everything else?

00:37:05[AB]

No, we can certainly turn it on its head. We don't need ATC people either. We don't need teachers either. We need airplanes to be guided, and we need children to be taught. But naturally, we have to take certain actions for those things to happen. In the case of children being taught, somebody has to teach them. In case of airplanes being guided, somebody has to guide them. And there comes the need.

00:37:28[RH]

That's not true. There are countless people being taught by YouTube. Our online courses.

00:37:37[AB]

Yeah, I think if we took classes of 25 children, sat them down in a room and played YouTube videos for them, and they might not have the same success rate and education. Or maybe some--

00:37:50[RH]

I'm scared that's what they're doing nowadays. (laughing)

00:37:53[AB]

Some of the children might have a mindset that would allow them to pick up something, but I don't think it would work in general. And certainly, you can't just show videos to the airplanes and how they should fly nicely between each other. That's not gonna work. You might be able to write some kind of computer program to guide the airplanes automatically, but then that guidance is not gonna be much better than the programmer that wrote the program for it, unless you throw magical AI and hope for the best. Your black box function telling the airplanes where to go, and nobody quite understands what's going on. And writing the algorithms for it doesn't seem to be a simple job, or it would have probably been done. Or it could even been done, and then people overseeing it somehow, like driverless cars, people overseeing what they're doing, and it's not going very well.

00:38:42[ML]

So I think with discussing programming languages, there is an extra step. So in air traffic control, you need to connect the planes that need guidance to somebody that can guide them. So there's one connection there. If you have a problem, say, analyzing financial data, you have the problem of financial data, and you need to connect that to a person who understands how to work with the data. And then the programming language is an intermediary that the person uses as a tool to solve the problem. So you have two connections that you have to make. First, you have to, well, one of them is that you have to connect the person to the programming language, and the other is that you connect the programming language to the problem. And so this killer app thing is more of a suggestion that what really works is to force, if you have a problem, then say, well, the only way to solve this problem is this programming language. And I mean, it's kind of hard to, you know, most problems these days do have some solution out there. So it's hard to break into that now. And you can look at the other end of connecting people to programming languages. But I think the fact that you have to make both connections makes this a very different sort of thing to solve.

00:39:55[AB]

Makes it harder to

00:39:56[ML]

Yeah, well, there's no natural place for a programming language. Like it's-

00:40:00[AB]

I don't know, I mean, people that need to communicate with the computer, some way of doing certain tasks, analyzing certain data, and the language may be a better or worse fit for them. I mean, we can easily find extreme examples of programming languages that are ill-suited for any particular task. And maybe a lot of the pie that's, or could belong to the array languages is or was being eaten by bespoke solutions to that particular problem. I certainly think that's the case. That doesn't mean that there aren't domains left and with their corresponding domain experts where these languages are, if not an optimal, that's probably impossible, but a very good fit. And they could easily be that such people in working with these domains are currently using suboptimal tools for instructing the computer what to do. And it's simply a lack of information about these languages that prevents them from being more effective at what they need to do.

00:41:06[BT]

I think it's really useful to talk like what Marshall's saying about the two-stage process. One is matching the language to the problem and the other is matching the person that's gonna solve the problem to the language. I think, and I might be wrong about this, Ryan, but I think what you're edging towards is make it easier for the people to choose the language you want them to choose. Because there's already languages that match up to problems, but if a person is choosing something different because they've got a different way around it, that's what you're up against? Is that kind of the thing that you're thinking with the array languages?

00:41:39[RH]

Well, I'm not sure if you've changed or refined my thinking from listening to you, but I guess if I was trying to say it as clear as possible, I believe there's a minimum viable popularity of a language else it won't survive. And what I am beginning to believe, and you guys can tell me if I'm wrong 'cause it's not a strongly held belief, is that that bar is getting higher as the other languages that are popular have plugins and modules and due to the complexity of the world increasing and they optimize their compilers and have pilot execution automated and have debuggers and tools and huge investment, huge. Even though they are not a good fit commercially, and I'm talking purely commercially, they maybe are more likely to be chosen. So that would be the trend I think is happening.

00:42:27[ML]

Yeah, well, and to that point, what I was gonna say about Adám saying, it's just a problem in information. If people knew that APL was better suited to their problem, then they could choose APL and benefit from that.

00:42:39[AB]

I didn't say it was just that problem. I said that would be one problem.

00:42:43[ML]

Well, all right.

00:42:44[AB]

There are other problems as well.

00:42:45[ML]

I'm gonna say it hardly matters. So the suitability for a language to a problem is not just in how the language is defined, but it's in all the tools and connections and even the culture of knowing which parts of the language you should use to solve this problem. So like, I mean, and this is kind of packaged in Kdb, but if somebody asks you, how do you apply an array language to financial problems? One of the key tools and the thing that Arthur Whitney really, if not discovered, popularized is using this inverted database system where each column in your database is a different vector. If you don't have that, then like an array language is just not any better than any other language. So figuring out that particular representation is a huge deal in knowing that k is applicable to financial situations. I mean, this is what allows people to be, you know, trapped in languages that are just not as good as they could be, is that you have to have people that are working with the language on the problem for a long time in order to build up these solutions. So I think it's not just a question of, you know, if people knew everything about programming languages, then they would be able to pick the perfect one. It's that they have to also, you know, they have to spend enough time with the language to figure out how it connects to the problem and make that connection strong. And if there's another language that, you know, just due to historical precedence works better for people right now, that's just not gonna happen. They won't switch over. And they won't be able to develop the usage of that language for that problem.

00:44:26[CH]

I think Ryan is, he's really onto something, or, you know, his article, at least in my head, has kind of made a different point than he has articulated. You know, at the end of his post, he kind of mentions a few different things that he'd like to see, or thinks that Kdb needs to change. And I think another way of like stating his article is that we don't live in a world where like any array language, whether it's q and Kdb+ or APL dominates some industry. But if we look at, you know, Kdb+ and q, like it was 15 years ago, like the number one best thing. And like, now we're in a world because we have other technologies, other DBs that are open source, have great documentation. They're easier to get started with. Like there's an alternative world where like KX and Kdb+ like went a different path. And like maybe at some point they open sourced it and the documentation, like I remember when we interviewed Nick at one point, Nick Psaris, [05] who I'm not gonna remember, does anybody remember the name of his book?

00:45:28[ML]

FunQ is one.

00:45:28[BT]

FunQ is definitely one, yeah.

00:45:29[CH]

FunQ.

00:45:30[RH]

Q-Tips.

00:45:31[CH]

Yeah, Q-Tips. And I recall him when we interviewed him, he said one of the reasons, the motivations for writing the book was because he got tired of having to rewrite the same recipes at all these different companies because they weren't allowed to like put them in a library where they could be shared. And like imagine a world where that wasn't the case and there was some kind of PyPI equivalent where you could share these libraries. Probably the finance world today would look a lot different than like all these different competing technologies that kind of have replicated each other's, what you can do with them. Potentially we could live in a world where just like, KX and Kdb+ was the Python for hedge funds and the four different verticals that Ryan mentioned. I'm not sure, Ryan, if you agree with that statement or like that's something I've been thinking in the back of my head while this conversation has been going on. I'm not sure if you agree or disagree or want to add anything to that or say something different.

00:46:30[RH]

Yeah, most of the things in the article were not my original ideas. I listened to that ArrayCast actually, that's like your second or third episode with Nick. And he mentions he wanted to get the modules out 'cause he was between jobs and that's the one way he could get code reusable. I'm sure that's why he said with TimeStored. I want to do q studio between jobs so that I can have it. And similar with something I wrote q unit, the unit testing framework, and it was the same reason. And yes, I would love to see actual, so I have a follow-up article about why we consider it for Kdb5 just to put my wishlist out there. And modules are one because every bank has the same modules. If I read another log.q, I may just cry. Like I think I've read 15 log.qs and none of them were innovating amazingly. I mean, you don't want innovation in your logger. And it would allow people to, together with free, a free version, it would allow people to experiment and build stuff in their areas where they can build something they're expert at. Like Bob in recording, he gave an example of a J plugin he wrote. I would have no hope of writing that. And if I could reuse that logic sometime I need it without having to fully understand it, I'd love to. So modules are one thing I'd like to see. Marshall brought up vectors and SQL, pure genius, on Arthur's part, absolutely genius, that it's based on this. I mean, when I write standard SQL and it's based on sets, it's painful. Just seeing that clarity that the order mattered. But to flip that around to what I mean of look at the other languages, look at the new environment, would it harness that much being slightly more compatible with standard SQL? Allow someone to write and instead of a comma, allow them to put the date somewhere else, allow them to do select star, maybe limit 100. I don't think it would harness. And if we can, maybe trick isn't the word, but if we could encourage beginners to write that and then later write the three hash, three sub list, ascending to get that nice little vector out, that's a win for everybody, I think.

00:48:36[CH]

The blog you mentioned too, I found that, that's the Kdb 5.0, the roadmap ahead. I think that's your most recent blog, if I'm not mistaken, that was just published. I guess this episode's coming out in October, so it'll be roughly a month ago. That's the one that you referred to where you mentioned modules as one of the things you wanted to see. Are there other things worth noting that, while we've got you on air in case someone, KX didn't read the blog, but they are a listener of the podcast, that's worth mentioning of things you'd like to see?

00:49:08[RH]

Well, I think I may have stolen Stephen's title, or maybe he got it from someone. Kdb for everyone on everything, everywhere. Did I steal that from you?

00:49:18[ST]

No, I think you're referring to a recent talk in Madrid, the title of that.

00:49:26[RH]

So it's at the back of my mind and formed the basis of my thoughts, yeah. So yeah, for everyone means make it easier, be more standard with SQL, change the wire protocol to also support Postgres. So anything that works with Postgres can just work. And they have some of these pieces. Parquet, so that works with everyone, everywhere. Make it, give it a free version out. Like you guys quite often mentioned getting stuff in the academia and stuff. I think nowadays no one is going to encourage students to use a non-free tool. I mean, if it didn't work for MATLAB and Wolfram, it's not going to work. It needs to, there needs to be a free version that you can rely on always being there. Even if it's somehow limited, they keep the golden goose laying in the other area.

00:50:11[AB]

Okay, but that now is the case, right? Now there are a few versions of whatever you might want.

00:50:16[RH]

Limited, it needs to also be clearly usable with a clear license.

00:50:21[ML]

Yeah, I mean, there are free versions of whichever language you might want, but they're not free versions of whatever functionality you might want in that language.

00:50:29[AB]

Wait, in what way are they limited?

00:50:32[ML]

Well, they're missing all sorts of stuff. I don't know which free version you would want specifically, but I mean, most of the free Ks don't have any database functionality at all.

00:50:43[AB]

No, but KX is k, q, whatever, and you can try out free, right? And that looks commercial product that has a free version that has absolutely no restrictions on it, functionality-wise.

00:50:57[ML]

Yeah, but there are strong restrictions on usage.

00:51:00[CH]

Q limits the number of cores to, I think, two. That's the one restriction I know off the top of my head. I don't know if there's other stuff.

00:51:08[AB]

That's a performance limitation rather than the functionality limitation. And I mean, once that makes a difference to you, then you're probably making enough money that you can afford to pay for it. I don't know, I mean, I don't know Q's prices.

00:51:21[RH]

So I make two pieces of software that I partly sell. The very awkward, what I think is reality that I've discovered is, whatever your competitors are giving away for free, you also need to give away for free. You have no choice. So right now I can use DuckDB for extremely fast column-oriented, date partition, querying. So it needs to be as good to give away, else you will use the other one. That's what I find to be the reality of the two products I make.

00:51:52[ST]

Ryan, did you not produce a free q interpreter? (Ryan laughs)

00:51:59[RH]

In COVID time, I was going on a wonderful ski holiday in Innsbruck. I was looking forward to skiing over a few days. COVID happened, everything locked down. You can't go anywhere. What do you do? Yes, you write a free version of q in Java. (Ryan laughs) So if I'd been able to ski, I wouldn't have written it. But yeah, and it was great. It was brilliant fun. I got to see, I think, some of the choices that Arthur made. I don't think he gets enough credit for not inventing stuff. Like I find it coming from Java, it's so hard not to invent something new and force someone to learn something stupidly new. Like when Arthur used lists for SQL, or when he reuses the same ability that you could do one thing here everywhere, I don't know if it takes some effort, 'cause it would take me effort to work it out. So it's pretty amazing if he doesn't. Like to give you an example from SQL, something that's really quite horrible, if you're doing a select, say you want the max, you say max, if you want it in a different area, you have to say greatest. And if you want it within a window, you may need to use a function called list max. And there's three different things. And when you're developing, I've done it, it's so easy just to bang out a new function, but to somehow find the underlying unifying concept and not invent something. As I wrote q, that was the one thing I was really amazed by. And it made it more powerful, not inventing stuff. But yeah, it was a great four days not skiing.

00:53:30[ST]

We have no sympathy, I got fond memories of skiing in Austria. I was wondering, given your views on what it would take for the language to flourish, if you see a role for a free, possibly even an open source version of Kdb, which would not, of course, be as performant as the expensive paid for version, but would run. I would allow developers to use Kdb for this, that, and the other, and just generally widen the use base and the experience and the pool of experience.

00:54:07[RH]

I think, given what I said before, that I think there's a minimum viable popularity, and I think it's going up, if they want to capture more markets, which it seems like they do. For a few years, I think they weren't as eager on it, they were more wary. If they want to capture more markets, I think it's essential they have a free version. For all the reasons we discussed before. I won't be writing another one, I don't have the right skillset. I'm very busy with Pulse, mostly writing TypeScript. Forgive me. If I had to say one area that I'm kind of holding out hope, the Python guys, similar to JavaScript, they've thrown thousands of people at this. They're now rediscovering a lot of the things that made array languages good. I mean, Polars and Parquet are very good. Whoever has done those, an RO, has seen Kdb, APL, or something like that. Maybe one of you guys can confirm, maybe you've talked to them. So they have the right basis there. If I had to guess what may appear, if you look at Klong today, it's a language that reuses the full Python infrastructure, and then provides a language on top of that. You should definitely talk to him. But someone could come out with a q interpreter that is a thin veneer over the Polars and the DataFrame, and they would get all the performance and the full Python modules for free. And then we would get the array-based language and the syntactic beauty and brevity. So Conor, you would get your NumPy. Basically, you could write an array language, and it would translate into efficient, even more efficient than NumPy.

00:55:45[ML]

Whoa, so KlongPy is worth mentioning along those lines. That is a, Klong is a k derivative that tries to reduce the amount of overloading in the language. And that's an implementation that seems to be fairly solid, that's based on running that as NumPy code. So what you're suggesting is pretty similar to use Polars, I guess, and possibly q being the language there.

00:56:11[BT]

Yeah, one of the things you mentioned is what I also often refer to as critical mass. You get to a certain size, and you can survive because you're a certain size. And hopefully, as you say, if that critical mass threshold is increasing, you're keeping up with it. In the case of the array languages, I think in a lot of cases, they're chasing critical mass. What I find really interesting is when you talk about almost using an array language like a wrapper around something like NumPy that's got big libraries and all this, people are sort of aware of it. You're building back into one of the killer at parts of the array languages that I've seen is they're very quick for prototyping. You can change things much quicker and make changes quicker. And that's something that languages that are more verbose don't allow you to do, one, because you've got actually more stuff to put in, although that might get easier with chat GPT and things like that, but also because you can keep more of it in your head if it's more terse and you understand what's going on. And I think that starts to build back into what one of the strengths of the array languages is prototyping and that maybe what they'd be really good for is allowing people that understand almost on a mathematical level what the constructs are doing because that allows them to think more quickly about how to change things. And then that can be reflected at a lower level in a language that might be more popular. But I guess you're still playing to a niche because you're talking about people who are actually looking at changing things as opposed to people who are just trying to keep things running. But what are your thoughts about that?

00:57:42[RH]

If that's for me, I haven't given it a lot of thought. So like I said, I posted the article and I thought like, you could now ask me about TypeScript or user interfaces for traders or web sockets. I could probably answer a lot better.

00:57:58[BT]

But does that sound sort of the area that you think there might be an opportunity in or do you think, no, that's just not gonna work?

00:58:04[ML]

Well, I do wanna kind of jump in and point out something that I feel is a little related that I should bring up. We've had John Ernest on the ArrayCast a few times [06] and he's been working on this language, LIL, which is very strongly influenced by k but it's going in a complete opposite direction because it's designed as the scripting language for this fun tool HyperCard, which is, or not HyperCard, Decker, which is like a new version of HyperCard, which allows, the idea is to allow, you know, just anybody to create nice presentations and almost webpage-like things. So LIL is intended to be a really not serious at all programming language. Of course, that doesn't mean it's designed in a non-serious way, but the goal is to bring these k ideas into a language that looks a little more traditional, that's much easier to get started with and that doesn't kind of throw you into the deep end right away. So that's why I find that interesting is because it is, rather than being driven by the idea of, well, how can we push array programming, it's driven by this application already. So, you know, I couldn't say where it goes in the future, of course, but that's one of the things that I think is a really interesting development in the space of array languages.

00:59:29[BT]

I'd agree. I think that's one of the things that John has done with Decker and LIL, but I think I agree with you as well. It's maybe not in an area that might be as, like it doesn't have the killer app. It's got the accessibility, but how many people want to write hypercards to it?

00:59:29[ML]

I mean, I think Decker has a good chance to be successful in the pretty small niche of, you know, making simple interactive things. I mean, that's not like a real killer app that kills everything, but it kills some things, right? So in that way, LIL has a very good chance of surviving as a language, which is not, of course, the same as, you know, becoming a mainstream programming language.

01:00:13[CH]

So I know we're past the hour mark, but I wanted to circle back to something you've mentioned a couple times, which is this new product that you're building, Pulse. And I think maybe that's a good note to end the podcast on is maybe you could tell us a little bit, 'cause so q Studio, it's out there. It's free for everything other than the Kdb backend, but you mentioned a couple times that you're working on this tool, Pulse, and you do have a link to it on the front of your timestore.com. So maybe you can tell us about it, or I'm not sure if it's available for use yet, or you can tell people what they can expect in the future from this kind of re-imagined tool. You did mention, you know, you were envious of Arthur being able to, you know, restart a couple times. So maybe this is, Pulse is the 2.0 of something for you. (laughs)

01:01:03[RH]

I think I'll take another five years before I reach the next one. Yeah, so like you said at the start, for 10 years, I built data systems in banks. What I most enjoyed doing was working with quants, because typically I'm knowledgeable in technology in one area, they're knowledgeable in the business, and together we can create something extremely useful. And I get to learn a bit about theirs, and they get to learn a bit about mine, but we also can excel in our own areas. While I was doing that, the need for a fast user interface and the ability for quants to reasonably make interactive data applications kept coming up, and they would try to shove various stuff together. And I thought, well, by the time I learned another language, you know, TypeScript appeals to me slightly, certainly compared to what JavaScript was. So it's like, I will go try to solve that problem. I did also have a belief that there are more databases appearing, and that we're going to see a more heterogeneous environment of multiple types of database running. So I wanted it to work with everything. And it has been great fun working with the other databases and seeing what each of them had to make. But yeah, it's basically to let quants or data people like us, if you don't know HTML, JavaScript, CSS, [07] to build little interactive data applications by just writing Kdb, or just writing Clickhouse, or whatever your database is. I should say that Kdb is certainly still the quickest one that I interact with. Some of the rest could be very slow.

01:02:34[CH]

Well, I'm sure the KX folks will be happy to hear that. All right, I'm not sure if I should ask if there's any final questions from any of the guests.

01:02:45[BT]

Or any of the panel, for that matter.

01:02:47[CH]

Or yes, any of the panelists.

01:02:50[BT]

We think of ourselves as guests.

01:02:52[RH]

Can I say, I was probably overly obsessed with the commercially successful ones. When Stephen brought up me writing Q, I think there's a huge value for programmers to try writing a language or look at how they're writing. I mean, I got a lot of fulfillment and learning from it, but I wish someone would also pay me for it. (laughs)

01:03:15[BT]

I just have the observation that talking about the critical mass and then the amount of awareness people have of a language, especially for array language, is gonna get more difficult because of the LLM issue, not recognizing them. So that may be a real significant barrier to success is that if they miss that boat, that's a big freighter that's heading out fast. And if you don't hook onto that, you may be struggling, well, you may be looking in a very different area.

01:03:44[CH]

Yeah, the rich are gonna continue to get richer as they say. Although a small, I guess, tip that I have had very little success trying to get LLMs and the GPTs of the world to generate array language code. However, with the token sizes, whatever, that you can feed these things, now if I need questions answered from BQN, I will just go and find the relevant documentation pages. I think one time I even used a grep command and I downloaded the Marshalls BQN Git repo and then downloaded every single MD or HTML file, copy and pasted basically the whole documentation, asked my question and said, these are the docs, here's my question. And it did actually answer it for me. So sometimes you just need to feed a corpus of documentation that someone's written pending it exists and then you can get your answer.

01:04:36[AB]

Considering that there exists a lot of text on the APL, the APL should be in a strong position if we can manage to feed like that. Still, I mean, these models are not writing precise anything really, even if they happen to get certain programming languages right some of the time, I would say at best. But if I'm asking more soft questions or- But you're saying that for--

01:04:59[CH]

Yeah, for specific, I just needed a single thing. It wasn't like write a whole program. It was like, I need to know, I don't understand the choose modifier yet and I wanna do this thing. Like, how do I do it? It's like, oh, well.

01:05:13[AB]

Squeezing things out of human text as a super powered search mechanism, I can see the value of that. And we have and are also making experiments. We're using things like that on APL texts. I still wouldn't trust actual programming. These things are intentionally made to kind of emulate human fuzzy thinking about things. And then we abuse them by asking them to do things that need to be precise, to be not human. And I don't believe it's a good measure of whether they're going to be successful.

01:05:57[CH]

This is the difference between Adám and I. Adám probably, if he's got full self-driving mode and a Tesla, watching everything it does. I don't even have full self-driving. I don't own a Tesla, but I rent one every once in a while. I'll just have like auto steering and I'm like, let's see how close to FSD this is. And I'm, you know, I am very trusting of the robots. I like to think they're already better drivers. And so I'm ready to hand over everything to the AI overlords that are lurking around the corner. And when you listen to this, remember I was your number one biggest fan. And if you need help, if you need someone to sit in that C level office, I'm your guy.

01:06:37[BT]

The limitation that they may face will be environmental because it's becoming apparent that they're having a significant effect on the environment and there may be some regulation introduced, hopefully not too late, that puts their use towards maybe more profitable or more efficient uses than they might be currently being used for. And maybe that might be something that will slow them down a bit, but I can see there being a real problem environmentally in the real world planet that I live in if they are used indiscriminately. And that might be something that slows them down.

01:07:12[AB]

I mean, you said environmental, I was thinking of this little road going between and outskirt of Basingstoke and Bramley where the Dyalog's main office is. And for all those talk about self-driving cars, I want to see two of these cars being let loose at the two ends of this road and see how long time it takes for them to negotiate their way to the other end, crossing each other in the middle. Kew Fort Lane, if you're in the area and wanna try it, but be careful, even human drivers are known to have issues with this road.

01:07:46[CH]

He's made my point for me, folks. He's made my point for me. Anyways, with that, we should land this plane. So we'll be sure to link all of the things we mentioned, your timestore.com website, which has the Pulse, the Q Studio, and both of the blog articles that I mentioned, as well as the blog in general. There's other blogs, if you enjoyed the two that we discussed, I'm sure that you might enjoy some of the other ones. So we'll make sure to link all that stuff. Bob will let us know where you can reach us at.

01:08:14[BT]

Contact@ArrayCast.com. [08] And if you wanna get in touch with us, that's a good way to do it. As I mentioned off the top of the show, the next couple of segments are going to be slightly different, they're gonna be special, and you will hear Ken Iverson in them. So look forward to that. And thank you as well to our transcribers for always providing an alternate way to interact with our podcast.

01:08:36[CH]

And also thank you to you, Ryan. It's been a blast chatting about everything. We chatted about the stuff that I was expecting to chat about, the stuff I wasn't expecting to chat about, and I'll be interested to see, will people follow up, ask you more questions, or will this be the end of the Kdb+ questions? Only time will tell. Thanks for taking the time to chat with us today, though. It's been absolutely great.

01:08:59[RH]

No, thanks, it's been great fun. Don't ask me back on the talk about Kdb again. (laughing)

01:09:06[CH]

Next time it'll be Pulse, Pulse only. And with that, we'll say happy array programming.

01:09:10[All]

Happy array programming.

</details>
