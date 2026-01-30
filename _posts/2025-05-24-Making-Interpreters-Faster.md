---
title: "Episode 106: Making Interpreters Faster"
date: 2025-05-24 00:00:00 +0000
episode: 106
keywords:
- array-programming
- array-languages
- jlang
- interpreters
- apl
- bqn
- henry-rich
- geoff-streeter
- clang
- optimization
mp3-url: "/assets/audio/episode106.mp3"
episode-type: full
explicit: "no"
block: "no"
layout: podcast
excerpt_separator: <!--more-->
---
Making Interpreters FasterOur guests are Henry Rich and Geoff Streeter in this deep discussion of how interpreters for array languages are optimized.
<!--more-->

**Host:** Conor Hoekstra

**Guest:** Henry Rich and Geoff Streeter

**Panel:** Marshall Lochbaum, Adám Brudzewsky, Stephen Taylor and Bob Therriault

---

[Original episode on ArrayCast](https://www.arraycast.com/episodes/episode106-interpreters)

## Show Notes

Array Cast -  May 23, 2025

Thanks to Bob Therriault and Conor Hoekstra for gathering these links:

**[01] 00:01:35**

- [Subreddit for the Array Languages](https://www.reddit.com/r/apljk/)
- [Marshall's 5 year retrospective](https://mlochbaum.github.io/BQN/commentary/fiveyears.html)
- [APL Demo 1975](https://www.youtube.com/watch?v=_DTpQ4Kk2wA)
- [Marshall's First Appearance on ArrayCast #7](https://www.arraycast.com/episodes/episode-07-marshall-lochbaum-and-the-bqn-array-language)
- [Henry Rich Episode on ArrayCast #104](https://www.arraycast.com/episodes/episode104-j96)
- [Roger Hui Memorial Episode on ArrayCast #13](https://www.arraycast.com/episodes/episode13-roger-hui)
- [Ken Iverson](https://en.wikipedia.org/wiki/Kenneth_E._Iverson)
- [Geoff Streeter](https://aplwiki.com/wiki/Geoff_Streeter)
- [Geoff Streeter - 40 years with Dyalog](https://www.dyalog.com/news/113/420/Geoff-Streeter-40-Years-with-Dyalog.htm)
- [Dyadic](https://aplwiki.com/wiki/Dyalog_Ltd).#Dyadic_Systems_consulting)
- [Dyalog APL](https://aplwiki.com/wiki/Dyalog_Ltd)
- [.Atkins Engineering](https://en.wikipedia.org/wiki/Atkins_(company))
- [Zilog 8000 Processor](https://en.wikipedia.org/wiki/Zilog_Z8000)
- [Nested Array APL](https://aplwiki.com/wiki/Nested_array)
- [APL Programming Language](https://aplwiki.com/)
- [NARS](https://aplwiki.com/)
- [/wiki/NARSScientific Time Sharing Corporation](https://aplwiki.com/)
- [/wiki/STSCUnix](https://en.wikipedia.org/wiki/Unix)
- [Linux](https://en.wikipedia.org/wiki/Linux)

**[02] 00:11:08**

- [John Scholes](https://aplwiki.com/wiki/John_Scholes)
- [John Daintree](https://aplwiki.com/wiki/John_Daintree)
- [Quad WC](https://help.dyalog.com/latest/#Language/System%20Functions/wc.htm)
- [dfns](https://aplwiki.com/wiki/Dfn)
- [Geoff's Presentation at Dyalog 24](https://dyalog.tv/Dyalog24/?v=M5aY5ySFM_o)
- [Interpreter](https://en.wikipedia.org/wiki/Interpreter_(computing))
- [Compiled Computer Languages](https://en.wikipedia.org/wiki/Compiler)
- [Cache Memory](https://en.wikipedia.org/wiki/Cache_(computing))
- [Processor Registers](https://en.wikipedia.org/wiki/Processor_register)
- [J Programming Language](https://www.jsoftware.com/#/)
- [Weakly Typed Computer Languages](https://en.wikipedia.org/wiki/Strong_and_weak_typing)
- [J Parts of Speech](https://code.jsoftware.com/wiki/Vocabulary/PartsOfSpeech)
- [Parsing Part 1 J for C Programmers](https://code.jsoftware.com/wiki/Help/JforC/38_Parsing_and_Execution_I#_Toc191734584)
- [Parsing Part 2 J for C Programmers](https://code.jsoftware.com/wiki/Help/JforC/39_Parsing_and_Execution_II#_Toc191734586)
- [Trace application in J](https://code.jsoftware.com/wiki/Scripts/Tracer)

**[03] 00:20:50**

- [Adverbs in J](https://code.jsoftware.com/wiki/Vocabulary/PartsOfSpeech#Adverb)
- [Locales in J](https://code.jsoftware.com/wiki/Vocabulary/Locales)
- [J Dictionary](https://www.jsoftware.com/help/dictionary/contents.htm)
- [CPU](https://en.wikipedia.org/wiki/Central_processing_unit)
- [Instruction Cycles](https://en.wikipedia.org/wiki/Instruction_cycle)

**[04] 00:35:50**

- [Branch Prediction](https://en.wikipedia.org/wiki/Branch_predictor)
- [C Programming Language](https://en.wikipedia.org/wiki/C_(programming_language))
- [Python Programming Language](https://en.wikipedia.org/wiki/Python_(programming_language))
- [C++ Programming Language](https://en.wikipedia.org/wiki/C%2B%2B)

**[05] 00:46:42**

- [Marshall's Binary Search Presentation](https://dyalog.tv/Dyalog18/?v=paxIkKBzqBU)
- [Elvis Operators](https://en.wikipedia.org/wiki/Elvis_operator)

**[06] 00:55:12**

- [Clang Compiler](https://en.wikipedia.org/wiki/Clang)
- [Decimal Floating Point](https://en.wikipedia.org/wiki/Decimal_floating_point)
- [Debug in J](https://code.jsoftware.com/wiki/Debug)
- [BQN Programming Language](https://mlochbaum.github.io/BQN/)
- [Context Free Grammar](https://en.wikipedia.org/wiki/Context-free_grammar)

**[07] 01:03:46**

- [Bytecode](https://en.wikipedia.org/wiki/Bytecode)
- [Stack Based Processing](https://en.wikipedia.org/wiki/Stack_machine)
- [Dyadic Iota](https://aplwiki.com/wiki/Index_Of)
- [Key Primitive](https://code.jsoftware.com/wiki/Vocabulary/slashdot#dyadic)

**[08] 01:11:35**

- [QA for Software](https://en.wikipedia.org/wiki/Software_quality_assurance)
- [Contact AT ArrayCast DOT ComSpecial Combinations in J](https://code.jsoftware.com/wiki/Vocabulary/SpecialCombinations)

<details>
<summary><strong>Transcript</strong> (click to expand)</summary>

Transcript

Transcript prepared by

Adám Brudzewsky, Bob Therriault, and Sanjay Cherian

Show Notes

00:00:00 [Henry Rich]

So when you hit a jump, a conditional branch, you just sort of imagine that it's followed by 30 lines of no up because the half the time that that branch mispredicts, it wastes a page of code doing a mispredicted branch. It puts you in the right frame of mind to tell yourself that the main thing I need to do here at the low level is make sure I don't have any mispredicted branches.

00:00:15 [Music]

00:00:32 [Conor Hoekstra]

Welcome to episode 106 of ArrayCast. I'm your host, Conor, and today with us we have two special guests, one returning and one new. We will get to introducing them in a couple minutes, but first we're going to go around and do brief introductions. We'll start with Bob, then go to Stephen, then to Adám, and finish with Marshall.

00:00:48 [Bob Therriault]

I'm Bob Therriault. I'm a J enthusiast and I'm going to learn a lot more about J today.

00:00:55 [Stephen Taylor]

I'm Stephen Taylor. I was an APL and q enthusiast before I went on holiday and I'm back and I'm keen to find out what this meeting is all about.

00:01:04 [Adám Brudzewsky]

I'm Adám Brudzewsky. I mostly deal with APL, but I guess I'll be learning some more J today and maybe even some details of the APL that I'm not aware of.

00:01:16 [Marshall Lochbaum]

I'm Marshall Lachbaum. I'm a designer and developer of BQN and a Singeli enthusiast.

00:01:22 [CH]

And as mentioned before, my name's Conor, massive Array Language fan of all the Array Languages, excited to talk to our guests today. But before we do that, we are going to have, I believe, two announcements. I think we've got one from Bob where we'll start and then we'll go to Marshall for our last announcement.

00:01:36 [BT]

And I'd just like to announce that on Reddit, [01] everybody has certain opinions about Reddit, but in the subreddit of APLJK has been dormant, I would say it was dormant for about six months. You couldn't even get on to put any new announcements on. In the last three weeks, it's come back again. They have a new moderator. He's very interested in getting it up and going again. And so if you haven't been paying attention to it recently, I think he's looking at it or they are looking at it more as a notice board. Maybe not so much directed, but a way people can go in and find out about things, which honestly is how I was using it because I was posting to people that we would have a new podcast out and anything new coming up, I would put on there. That seems to be the way it's being used, but it's kind of a nice central place to go to check out. And it's a nice safe space right now. So I commend them for doing that work and bringing it back online because it was missing for a while and it was a shame.

00:02:37 [CH]

I would say link in the show notes, but I'm pretty sure everyone can find their way to it. I mean, actually, well, it's got the /apljk, so link in the show notes, link in the show notes. Over to you, Marshall.

00:02:47 [ML]

So May 10th, 2020, I don't really know everything that was going on, but the interesting thing about that date is that it's the first recorded date where I was developing BQN because it's the first commit on the prototype that I did. So I figured it was a good day five years later, which was now just over a week ago, to look back at the design of BQN and say, you know, how things have gone. So I wrote up a page that focuses especially on the new primitives I added and the things that I shuffled around relative to APL and says, you know, what's good about these? What's bad? You know, kind of have they stood up to usage in the language? What other things would I look into now to replace them? And so on. So that's a pretty long page, and we'll have a link to it in the show notes that you can check out. And especially, you know, if you're designing a new array language, see what's happened.

00:03:46 [BT]

And I just like to say it's excellent. I told Marshall he should come on and announce this because it's a really good write up, and it gives you really good insight about how designing a language has so many levels and the approach you take to it. And on top of it, he's got a great way of being clear and honest about the things that did and didn't work, which is really amazing. It's just so cool to see something, somebody write something this clear and honest about how things worked out. It's a great piece.

00:04:19 [AB]

And as well, it's interesting about anniversaries. Marshall speaks in this thing that he's written about APL's time-tested ideas, and not any particular date right now, but this year marks 50 years since the video that's available on YouTube, APL demonstration 1975, well, was recorded. So it's 1975. So it's interesting. Time-tested ideas. Here we are. Half a century later.

00:04:48 [CH]

Well, we will leave a link not just to the blog, but also to that video. And maybe, I mean, I didn't know about this blog. This is part of the reason I love ArrayCast is I get to find stuff out real time. So I will be reading this after the fact. But maybe if folks want, we can re-elevate Marshall from panelist to guest and we can bring him on and we can talk about BQN five years, because I'm sure the listeners would like to hear. I'm sure there's some anecdotal stuff that could be added on top of the blog. And some people prefer to listen than they do to read, including myself. Anyways, with that out of the way, all the links that we mentioned in the show notes, I'm excited to introduce, as I mentioned before, two guests today. Our first guest we'll briefly introduce because all of our listeners should be very familiar with him. Henry Rich, the main developer of the J language and maintainer of the code base, the interpreter. He was just on a couple episodes ago, I believe 104, talking about the latest release of J and has, I think is the runaway individual with the number of times on our podcast.

00:05:52 [HR]

Don't give me credit for designing the language. That was Ken Iverson and Roger Hui. I do the interpreter.

00:05:58 [CH]

Oh did I say designing? I thought I said maintaining. But yes, Roger Hui and Ken Iverson, original implementers and designers of the language. But you are putting the J interpreter on your back as of late for the past few years and have been doing all the heavy lifting. And yeah, welcome back two episodes later. And our second guest is first time guest on the episode, Geoff Streeter. He is one of the original co-founders of Dyadic, which is now more commonly known as Dyalog Limited, the company that Adám currently works for and many guests that we have had on in the past on this episode. And he is now a emeritus employee of Dyalog, recently retired two years ago. But I found a blog post, I think it was published in 2017, that said 40 years at Dyalog. So has a very storied career and probably many stories to tell. Welcome to the podcast, Geoff.

00:06:57 [Geoff Streeter]

Yep. Hi, I'm one of the founders of Dyadic back in 77. And 81 is when we started Dyalog APL. So that gives you some sort of timeframe. And Adám asked me to come on to this thing, because I know a bit about how the scanner works in Dyalog, along with quite a lot of the other stuff in Dyalog. So I was going to go from there and see how the questions go.

00:07:26 [CH]

Yeah, we are absolutely excited to have you on. And maybe because it's your first time, that is the topic of today. It's parsing, implementing interpreters. But maybe before we do that, we can take a couple minutes to just have you introduce yourself. I'm not sure how far you want to go back. You just mentioned you founded Dyadic in 1977.

00:07:45 [ML]

And that was almost nine BQNs ago.

00:07:49 [CH]

But if you want to tell us a little bit about your path to the array languages. I mean, obviously, you've been working at Dyadic/Dyalog APL for the majority of your career. But yeah, I'd love to know a little bit more about, you know, before that, and what it's been like, you know, working for so many decades at Dyalog.

00:08:11 [GS]

I first came across APL when Ken Iverson spoke at the university I was at. And I completely missed the point, I will say. I came across APL again, when I was working for Atkins, which is a big engineering consultancy in the UK. And it was running its own time sharing service. And John Scholes [02] was working for Atkins Planning, I was working for Atkins Computing. John Scholes put the APL up onto the time sharing service. That was Sigma APL, which is Xerox machines. So I first came across that. And then we formed Dyadic from five people who worked for Atkins to do APL consultancy. And then in '81, we sort of got hijacked really by Xilog, who were introducing their Z8000 chip at the time. And they wanted an APL on it. So we opted, we actually organized enough to write a new interpreter. There was a half day's discussion going on about that time that sort of said, are we going to make this a version one APL, traditional, or are we going to go for a nested array APL? In that half day, we sort of came to the conclusion we were going to go for a nested array APL. And we did that, we took the NARS blue book, which came out from STSC, and implemented just about all of it. In fact, we implemented more than STSC did. So that's back sort of '81 to '83 or so. Took us 15 months to write the first one. And we went on from that to do lots of things. I mean, we did, we were a Unix company at that point, because the Z8000 was a Unix machine as far as Zilog was concerned. And you can forget Windows, it hadn't even, didn't even exist. DOS didn't really exist either at that point. So we were a Unix company. And I have stayed all my life through the Dyalog period as a Unix guy. Essentially the Windows and DOS, I got pushed into every now and then, but on the whole, I'm a Unix guy. So that has paid off, because essentially Linux is now the world's major operating system. So that's been an interesting, interesting path. In the process I did, I first started when, you know, you have to bootstrap an APL. And John Scholes was doing the parser and the memory management. I started with the scanner. And the first primitive I did was quad FMT. So basically because it was a big, biggish chunk that I could get on with whilst the rest of it was coming there. And then I did, at one stage I was writing two primitives a day. So that's the background at that point. And then we did a few things that stand out as advances. One of them was the one John Daintree did, which was the quad WC stuff, which I didn't really watch and I probably should have done, but didn't. The next one that came up is John Scholes did his skunk projects of the Dfns. In the meantime, I did 64 bit, convert the interpreter to 64 bit, which promptly paid things because then I could do the quad map stuff, which mapped the files because I now got some address space to map them into. And we went on from there and I learned a lot there about how to page systems. And we've got things that will enable fast startups and such like turned up later. So that's sort of part of the path. If you want some more of that path, there's stuff on the Dyalog site, which the paper I did at the last conference that covered some of that.

00:12:42 [CH]

No, that is super interesting. And I'll make sure to link the blog that I mentioned and some of those papers. And I'm sure, yeah, some of this will come up when we get into, which I guess is now, into talking about parsing and scanning. So I'm actually not sure where we should start. Maybe I should just throw it to Henry, because I think it was Henry actually that emailed us after recording episode 104 and said, "I think this would be a super interesting conversation and listeners would really enjoy it." And you mentioned a list of stuff that you had worked on specifically to get performance improvements and other things. So maybe I'll just throw it to you, Henry, and then you can guide where you want this discussion of interpreter work and parsing to start.

00:13:28 [HR]

Okay. Yeah, you had suggested in that podcast a couple weeks ago that internals would be of some interest. And I particularly think about performance, because, well, nobody ever asked if their LEARNING would run a little slower. And interpreted languages have a reputation for being slow. Not so much the array languages, because if you use them correctly, you're dealing with large data aggregates and the primitives run pretty fast. But array languages can be used in a way that makes them slow. And we'll talk about that in a minute. But I think if you come to array languages with the idea, or interpreted languages with the idea that, well, they have to be slower than compiled code. I think after you see what we actually do on your behalf to execute your sentences, you might rethink that glib judgment. In fact, you might even pick up some tricks to use in your day job when you're writing with a scalar language. So what does an interpreter writer have to worry about as far as performance goes? Well, the short answer for that is everything, because you never know what the use case is going to be. It depends on the individual user. If the user is dealing with large data blocks, then you have to worry about managing caches efficiently and making sure the computational units stay busy. For medium-sized computations, you have to balance the cache versus the internal register usage. And then for tiny computations, parsing becomes a bottleneck. Maybe it's only material for sentences that have small values, where the cost of parsing a sentence that adds one to a counter becomes larger than the actual time required to add one to the counter. Unfortunately, many users, especially beginning users, who are especially the ones that we want to not put off, are used to simpler languages. And they are used to writing small, short sentences. You might call that J-thon. They write J as if it were a simpler language. So for these beginners who are going to try J out and write some loop from one to a million, we don't want the parser to slow them down. And in fact, even on some well-written array programs, some algorithms just require short sentences and you need to parse them quickly. Now I should stop. Parsing in this sense, I'm using it in the J sense. I believe Adám, you said it's called execution in APL. But in a compiled language, parsing means examining the text of the program, breaking it into words, finding executable statements, finding control structures, finding declarations, all that stuff. None of that applies to J because J is weakly typed. And the unit that we're interested in is the sentence, which is basically like a statement in a compiled language. And unlike with a compiler, you can't pre-process the sentence because J being weakly typed, the parts of speech in the sentence may change from one execution to the next. A name may be a noun one time, a verb the next time. A value might be an array one time, a scalar the next time. Also, we have a long history of supporting multiple assignment statements per line so that as you execute the line right to left, we encounter a name and assign it a value and continue using that value in the sentence so that the parts of speech of words might even change in the middle of the sentence. So parsing in J is defined as scanning the words of a sentence from the right and looking for sequences of words that are executable. An example of an executable group would be one plus two. I can add one plus two and make three. But I can't just look at one plus two because there might be something to the left of the one. The one might be captured by a conjunction on the left. So it turns out that by very clever design of this important plumbing of the language, four words in a row is all you need to look at to decide whether a fragment of a sentence is executable. And that's what parsing is in J. Repeatedly, starting on the right of a sentence, take four tokens, four words. We call them words in J, tokens in most languages. Take four words, look at them, and see if they are executable. And there are nine different combinations that are executable. One of them is execute a dyad, one of them is execute an adverb, one of them is strip out parentheses that surround an expression. You've got to find these nine combinations. That's the job. How fast can you make it? And over the approximately 10 years I've been working on it, it has sped up by a factor of 10. That's not including the computers have gotten a lot faster too. So parsing is really pretty fast now. And that's what I want to talk about, the details of how that happened from the beginning implementation to the current implementation.

00:18:54 [BT]

And Henry, when you're talking about the rules, there's a hierarchy of the rules, right? Because as it steps down, I mean, you can actually look at this. I think there's a program called Trace or application called Trace where you can actually, it'll break it down and do it for you. But it's always going to take the top rule and then work its way down. If the top rule doesn't apply, it's the next one and it works this way down. And then if it gets to the bottom and there's no rules that apply, I think it advances and it goes to another token and basically works its way along the line.

00:19:27 [HR]

That's exactly right.

00:19:28 [BT]

When I did that in my head, when I was trying to figure out how parsing was working and I was working my way through my head, it's just mind boggling to watch this thing. That's just a series of rules go through something that you're in your head as a programmer, you're trying to make into a program that will work a certain way. This is doing it just by a hierarchy of rules, which is really impressive. It's quite a...

00:19:53 [HR]

It's a brilliant piece of design by Ken. The subtleties are very impressive. It's one of those things, hardly anybody pays much attention to it, but it is beautiful, a great piece of work. Maybe I should stop and let other people jump in. I have an outline of what I want to talk about. That's section one.

00:20:13 [ML]

Maybe just to clarify, you're talking about scanning from right to left. That's not just a choice to take it that way, because you have to encounter the tokens and execute things in the right ordering. If you have some function that executes at the right and some variable that's at the left of it, that can change the type of the value of the variable.

00:20:39 [HR]

We don't have any functions. You're saying a function, you mean an adverb? [03]

00:20:42 [ML]

No, if you have a sentence like x, y, 1, f, 2, when you execute f, it can change what x is, right?

00:20:52 [HR]

Oh, well, actually, no.

00:20:54 [ML]

Everything gets looked up before the...

00:20:56 [HR]

No, no, it's looked up just in time. That's another thing that... Apparently, there are some idioms that APLers use that J wanted to preserve. What you're saying is f can create x, but x has to be at least one more token to the left.

00:21:12 [ML]

Okay, yeah. I didn't say that. I should have said x, y, z, 1, f, 2.

00:21:16 [HR]

All right. Yeah, well, maybe x, z, 1, f, 2 would be enough. But yes, the meanings of the words can change owing to side effects of executions in the parse. That's not a real language feature.

00:21:31 [ML]

The point is here, if you had a fixed sentence there, if you had just ones and pluses and timeses and numbers, you could... There are various ways to parse that sentence in different orders. But because we have variables, it all has to go in a particular order. Right?

00:21:48 [HR]

And there's also that Ken's idea that you want to execute right to left just because you don't... If you have a language with 50 verbs, you don't want to have an operator precedence table. That would be just totally unworkable.

00:22:04 [ML]

Yeah. Well, I mean, you always do have to execute right to left, but you could conceivably parse it in any order. You could do something like look up, find the locations of all the adverbs and conjunctions, sort out what those do, and then all the verbs and so, but except that you can't.

00:22:23 [HR]

It's trickier than you think, because when you do an execution, it might change the current locale.

00:22:30 [ML]

Oh, yeah.

00:22:30 [HR]

And then everything changes. All your lookups go away or the names may be defined. The execution path may change. So it's important to do things at the time specified by the language in the parsing. Anyway, so when we started, when I started working on this project, the J interpreter originally followed the direct dictionary description pretty religiously. And given a sentence, it allocated a queue in which the sentence words would be put. It copied the sentence into the queue with markers at the front and the end to delimit the executable part of the sentence. It allocated a frame for debugging. It copied the sentence for error purposes into the debug frame. And then it executed this loop, which I've described as parsing, which is look at a sequence of four tokens, go through the nine parsing lines to find which to find the first line, as Bob mentioned, they are in a priority order to find the first line that matches and then execute that. Do that over and over again until you've executed everything down to a single word, then free up all the buffers. And that's just a lot of work. Here there's a lesson to beware of low expectations. When you look at something like that, you might feel up your hands and say, well, gee, what more can we do? Well, it turns out you can start by doing a great deal. Try to reduce the amount of work and share the work with other functions. So first thing was get rid of all that debug stuff unless debugging is turned on. Then allocate a big enough stack queue area to accommodate many calls to the parser so that we don't have to basically create a stack of J parsing stacks so that allocation and free are not required for them. And avoid copying the sentence. Sentences all the important sentences are coming from explicit definitions anyway. So there there's a copy of them stored so we can avoid the data movement of the sentence. We avoid the allocation overhead. And that's a good start, but you're still left with that parsing loop, which for every four words, you've got to go through nine searches. That's just going to be slow. But I had a good idea. I converted the parsing table into a set of bit masks. The parsing table itself, the first row of the parsing table says this row matches if the first word is a left parenthesis or the start of the sentence. The second word is a verb. The third word is a noun. And the fourth word can be anything. So I basically transposed that. So now each word in the sentence has four bit masks. One for each of the four possible stack positions it can be. For example, a noun in stack position two might be part of like, it is legal for line zero, six, and seven. Zero is executing a monad, six and seven are related to conjunctions and hooks and forks. So the mask for that word in position two would have bit zero turned on, bit six turned on, and bit seven turned on. So if you've done that for all the words of the sentence, consult that parse table. You can do it in nine instructions, not nine, nine machine instructions. Fetch the four masks and them together and see if the result's zero. If it's not, you have an executable sentence. This is a huge improvement compared to searching the table. And importantly, it's so fast that it allows us to think about further improvements that we could make to, now that the consulting the table is not the bottleneck, there's going to be some other bottleneck and we can go and try to work on that bottleneck. We keep doing this until we finally hit one that we can't break. And then that's when we're done. With these four masks are easy to generate. You look at the part of speech of the word, do one read from a table, which gives you all four masks because there are only eight bits each and save that at the stack. And that's the end of section two.

00:26:51 [BT]

So at that point, Henry, we've determined whether there's a rule that can be applied or not. It's sort of binary. It's on or it's off.

00:26:58 [HR]

Well, it's actually a number. It's zero through eight or zero through nine. Nine means there wasn't one. Zero through eight tells you which line matched.

00:27:09 [BT]

I was going to say, but in addition to that, you can tell which line is going to apply.

00:27:13 [HR]

Yeah. The location of the set bit, the lowest set bit tells you which line to execute.

00:27:19 [ML]

Yeah. And then you use that to jump into a function that does that or a computed go-to or whatever you use.

00:27:26 [HR]

Yeah. Well, they're just plain old go-tos, but yes, you get to the function to do that work. Okay. So now that the parse table is not an insuperable obstacle, what other, are there any other ways that we can duck work? There is one important, and that is what I call predicted unexecutability. The first example is when I shift in the first word of the sentence, well, there's no way that can be executable, right? It takes at least four, well, actually at least three. So I can shift in the first three words without bothering to check for executability. And there are a lot of times when you can avoid that check. If you shift in a right parenthesis, you know that that's not going to be executable for a while. So you can shift in a couple more words. If you shift in a conjunction, you can always shift in a word. And usually when you finish executing a monadic or dyadic verb, you can decide how many words to shift down and whether or not you need to rescan the sentence for executability. So we can reduce the number of times we have to check for executability. And as we do that, we are continually making the branch predictions better, those lines, because if we don't ask for executability for very many times when there isn't any, we're going to get a quicker answer in the cases where there is. It turns out about half of the scans for executability can be avoided by not very complex analysis in that section three.

00:29:03 [GS]

When you say you can't just execute one token, surely just a name is a token?

00:29:09 [HR]

You're absolutely right. I forgot that because I treat that as a special case. Because it happens so often and you can bypass so much work that the one word case is treated special and the two word case, well, even two words, well, they're only executable if one's an adverb. Adverbs make things a little bit different. As long as there are no adverbs, you can always start with at least three words. Okay, so we've reduced the job to the bare minimum. We're going to be stacking words. We're going to be deciding whether they're executable very quickly. And the question is, how can we finish it off as quickly as possible? This brings us face to face with the hardware. We have to make best use of the CPU. And there are a couple of features that you have to keep in mind because we're now dealing with a few dozen machine cycles to stack a word, a couple of dozen, a couple of dozen machine cycles to execute the word, to factor out to the routine that does it. So let's talk about stacking. Well, let's talk about generally load latency. What does that mean? Why do we care? Well, to put a word onto the stack, you have to load the word from the sentence. You have to look at it and decide what its type is. The type has been traditionally contained inside a field in the header of the block for the word. You have to convert that type to a part of speech. Now there are many different kinds of nouns, but they all look like the noun type for this purpose. Then you have to load the masks for that part of speech. These four things are dependent on each other, which is very important. A load has a latency of a minimum of five clock cycles. So when I say, if I say load, it's five clock cycles before I can use the answer. If I use that answer to make another load, I'm at cycle 10 by the time I get the second result and so on. Well, it turns out if you look at the accumulated latency of that set of processing that I described, the latency is much more than the amount of work that needs to be done for stacking. Stacking is just take the word, calculate the mask, store those into the stack, and then go look at the next word. I'm ignoring here the name resolution, which is a different problem, but I don't think we have time to talk about that. What can we do to reduce the number of loads? Now here's where I had a second good idea. Every word in J, every value in the J interpreter is described by a block that contains stuff like what is it? What's the rank? What's the shape? How many times, what's its use count? How many times is it used? It turns out there's about 64 bytes of information needed per value. It makes sense to align those values on cache line boundaries that will save the number. You won't have multiple half cache lines that are in use for values. So I made that system wide restriction that all values are aligned on 64 byte boundaries. And look at that. It leaves us with six low order zero bits in every address. Nature abhors a vacuum, you know. You can take those address bits and in those address bits, store the part of speech of the value. So that now when I'm going to create the mask for a value, I don't have to do three fetches and an analysis of the type. I do one fetch. That gets me a pointer to the value and also the part of speech. So I have just that one fetch and then I can fetch the mask. And there are only, the total number of dependent operations is just the one. You load the word and then you're ready to load the next word. So that brings stacking down to approximately the same amount of time as it takes to read the two words, but in the range of five to eight clock cycles.

00:33:32 [BT]

And that's because in the 64 bytes, you already have that word identifier in those lower four bits.

00:33:38 [HR]

Six bits, yes.

00:33:40 [BT]

Six bits, okay.

00:33:41 [HR]

Yeah. I need five of the six bits. There are, turns out there, I have to distinguish between names and assignments. There are a lot of different, there are parts of speech that are not associated with any value. They're associated with the word and the sentence, but five bits is enough to distinguish all the different possible things that a value can be used for in parsing.

00:34:06 [BT]

And you get that with just one fetch.

00:34:08 [HR]

Right. That's the end of section four.

00:34:11 [GS]

Yes. I'm slightly confused. There's a reference to 64 bytes and there's 64 bits for the address of which you pinch the bottom five.

00:34:20 [HR]

Bottom six, yeah.

00:34:25 [GS]

Okay. What's the difference for this reference to 64 bytes?

00:34:42 [HR]

The 64 bytes is the length of a cache line. It's the length of the smallest value we can store. And furthermore, the memory allocator allocates in power of two multiples. So it makes sense to put every data block on a 64 byte boundary. Right. It's the block header plus value that's on a 64 byte boundary. And that means that the lower six bits of its address are always zero.

00:34:47 [GS]

Are all machines cache lines on 64 byte boundaries? Is that true?

00:34:59 [ML]

Well, pretty much.

00:35:06 [HR]

I think the dominant ones are, and it doesn't matter whether they are or not. The system would work. It's just if you have 64 byte cache lines, it maps exactly to cache line boundaries. Okay. Minimizing the number of dependent loads is very important for making stacking efficient. For execution, there's another factor of modern CPU architecture that you have to come to grips with. And that is the concept of the CPU pipeline and the disastrous effect of a mispredicted branch. [04] The modern CPU executes from decode through final execution in a pipeline that for Intel architectures, X64 architectures is somewhere around 14 clocks. I think it's a little bit shorter for ARM, but I'm not completely sure. This is unavoidable because we've learned that if you say, well, how long does it take to execute instruction? The question is, gee, I don't know. How long does it take to fetch from memory? It might be five cycles. It might be 10 cycles. If you go to level three cache, it might be 30 cycles. And if it's in DRAM, it might be 60 cycles. So you can't have an idea that you're going to schedule instructions one by one. What the CPUs do is they throw all the executable instructions into a big buffer. And then as their operands become available, the instructions get executed. Something similar to a data flow architecture. This means that instructions are going to be released for execution long before it's known whether they will actually be executed. If I have, if I'm executing a branch instruction, that branch instruction was first encountered many cycles ago, let's say a dozen cycles before. Much has happened between the time that instruction was encountered and the time it's actually executed. So this is, you've got the front end of the pipeline, which is trying to guess what's going to be executed and the back end that's actually executing it. What happens if the front end guesses wrong? Well, then you have what's called a pipeline break. We did a test and we thought it was going to come out true, but it turned out to be false. When I say we, I mean the front end. The front end says, well, I'm going to predict that this branch is taken. And then it'll go execute instructions from the place where the branch would go. But if it turns out that branch wasn't taken, all those instructions that were released after the prediction are there, well, they're just mistakes. They have to be expunged from the pipeline. They represent wasted time that could have, you know, their execution slots are not doing useful work for you. The CPUs do a very good job of branch prediction. They'll look at your loops and figure out how many times you seem to go through this loop and expect you to go through that many times. They'll look at the branch history. They'll sometimes look at the history of one branch and use that to predict the next branch. And it's great, except when you have data dependent branches where the value comes in and you have to make a decision based on that value. And you really might not have any history if it's just data. And here's where the interpreters have a penalty because the text of the program is data as far as the interpreter is concerned. And when we're trying to decide what routine is going to be executed next, that depends on the user's program, which is to a large extent, unpredictable. So if you're reading the generated code from your compiler, and if you're going to be doing this sort of thing, you're reading the generated code a lot, you have to mentally, you go through it and say, okay, the add or exclusive or this, this. And when you hit a jump, a conditional branch, you just sort of imagine that it's followed by 30 lines of no up because the half the time that that branch mispredicts, it's going to waste 30 instructions. It's going to, it wastes a page of code doing a mispredicted branch. It puts you in the right frame of mind to tell yourself that the main thing I need to do here at the low level is make sure I don't have any mispredicted branches. And I think the listeners might enjoy this and you guys might too. Here's some coding example, coding quiz for you. So here's a program you're going to write in some scattered language. I'll give you a list of N integers. And the result of the function is the number of those integers that is in the range 1000 to 1999. So the program is going to look something like count equals zero for I equals one to N. And then you're going to have a statement that modifies the count. What should that statement be? And if you're listening to the podcast, you know, stop, stop until you've come up with your answer.

00:40:04 [CH]

Wait, so we're not supposed to solve this with our Array brains. We're supposed to solve this in like a C or C language or Python or something.

00:40:11 [HR]

Yeah. Yeah. C or Python. Cause, cause we remember you asked about how the, the interpreters implemented and we don't get to use the interpreter.

00:40:19 [CH]

So wait, can you, can you restate the question again? Cause I had an Array brain and was like building up masks in a fork.

00:40:25 [HR]

Yeah, you, yeah, you, you want to be able to write plus slash some, something on the list, but what is it? What do we have to do to make that actually fast? Given a list of numbers, you list a list of integers and it's like, of course, produce the count of the number of those integers that is in the range of 1000 to 1999.

00:40:49 [ML]

So that's inclusive, I'm assuming.

00:40:52 [HR]

Yes. And obviously there are trivial ways to do it, but I, let's say that you really care about how fast this runs.

00:40:58 [CH]

I mean, I feel like there's a trick and I just, I don't, I don't know the trick, but it's like, there are some tricks if you want to offer.

00:41:04 [HR]

I mean, if, if you want to offer something, I can swat it down or you can just let me off, talk about it.

00:41:11 [BT]

Well, you, you, you, you're going to put in a test, right? Just to see if it's in that range and then you're going to increment something based on that test.

00:41:18 [HR]

That's the, that's the idea.

00:41:19 [CH]

I mean, this is a classic map reduce, right? So like in C++, this is just a transform, reduce or an inner product where you've got a unit, a unary.

00:41:27 [HR]

You're way above me. I'm thinking of the level of subtract and jump greater than or equal.

00:41:31 [CH]

well, you can do it in a for loop as well, right?

00:41:36 [ST]

Is your trick to sort the list.

00:41:38 [ML]

That's really slow.

00:41:39 [HR]

No, no, no, no, no, no, nothing like that.

00:41:41 [GS]

I was going to say, is it already sorted? That's useful.

00:41:46 [HR]

Yeah. Now that's, that's the thing that, that's the first question that should have been asked. What do I know about these numbers? And if the answer, well, they're sorted, then you'd say, oh gee, well, bind a couple of binary searches and I'm done. So I'll tell you, they're uniformly distributed in the range zero to 2,999. So you want the middle third of that range. And I don't want to put you on the spot too much.

00:42:10 [ML]

Well, I can say what I'm thinking here. Okay. So I possibly the trick you have in mind, you want to use an unsigned type and first subtract a thousand. So that brings your 1000 to 1099 range to zero to 99 and everything else is above that. So then you test whether it's less than a hundred. And you've got the instructions for this really weird on x86, but you can do that test and add it to a counter.

00:42:39 [HR]

So yeah, in fact, give that man 10 marks. In fact, you don't, if you add it, the compiler will generate an added carry instruction for you. But what you must not do is if value is less than, I'm sorry, if value is greater than or equal to a thousand ampersand ampersand value is less than or equal to 1,999 count equals count plus one, which is, I would guess is what most listeners would write if they weren't given us as a test. And it's instructed, why must you not write that? Because the double ampersand instructs the compiler to do the first test and then do the second test. The first test, well, every branch is predicted. This is going to turn into a branch, right? If how is that branch going to be predicted? It'll be a test against a thousand. The machine will predict that that branch will succeed and it will succeed two thirds of the time, but it will fail. It'll mispredict one third of the time, one third of the time, the value will actually be less than a thousand, but the machine will have predicted that the value is greater than a thousand because two thirds of the values are greater than a thousand. The second branch will be predicted evenly because half the values are higher than 1,999 and half are lower, but that means half will mispredict. So you're going to mispredict two thirds of the time. You're going to have two thirds mispredicted branches per execution of that loop. One third on the first test, one third on the second test. That's nine clock cycles you're never going to get back for every word. So suppose you just got rid of that double ampersand and just wrote ampersand. Now you're instructing the compiler to do a test producing a zero or one, do another test and then add them together. That will mispredict only one third of the time and best is to not do, not do any branches at all, but instead count equals count plus the condition that produces a zero or one. So you can do this with nine wasted cycles, four wasted cycles or no wasted cycles. And let me go back and say, if you just change that double ampersand to an ampersand, clang will decide that you made a mistake and it will generate the worst possible code anyway. So you always have to check the generated code to make sure you get what you want. But here's another one. I've got, I have an, what in C, we call an enum. I've got a field that's got maybe 20 different possible values, which are given the integers zero to 19. And I want to see if the value is one of one, five, seven, 10, 13, or 17, six different values for this enum. How would, how should I do that test? Well, I've seen a lot of code that would just say, if value is equal to one or value is equal to five or value is equal to seven, et cetera. Well how's that going to perform? Usually all the branches will be predicted to fail. And whenever one of them succeeds, you have a pipeline break. But what you should do is take, take your, your value and take one shifted left by that many positions, producing a mask, and then just add that with a mask that has bits one, five, seven, 10, 13, and 17 set. And you can do, you do the whole test with fewer instructions, but crucially only one branch. Whenever possible, avoid, avoid unpredictable branches.

00:46:36 [ML]

I will say that if you are doing this in a loop, then what you really want to do with all this stuff is vectorize it. And I have a nice talk [05] on sub-nanosecond searching where I introduce the vector binary search that will, that will also, you can compare to six values with, it'll be three comparisons I think. And so you can get pretty good results that way. But I mean, I'm assuming that what you really want is you're in some context where you don't actually have all the values at a time.

00:47:04 [HR]

That's right. I'm saying it really isn't predictable and I'm I'm not going to be doing it. One last thing. I got 2 in it, 4 integers ABC&D and I want to ask the question is a equal to B&C is equal to D you know are these are these two pairs of equal entries? How do you do that? Well, I mean, you're if you're sloppy, you're right.

00:47:24 [HR]

That's right. I'm saying it really isn't predictable and I'm not going to be doing it. One last thing. I got two, four integers, A, B, C, and D. And I want to ask the question, is A equal to B and C is equal to D? You know, are these, are these two pairs of equal integers? How do you do that? Well, I mean, if you're sloppy, you write A equal equal B, ampersand, ampersand C equal equal D. But better would be exclusive OR A and B, exclusive OR C and D, or those two results together. And the result's zero if you have the desired equality. The point is you're saving, instead of two unpredictable branches, you have only one.

00:47:45 [BT]

And what you're saying is you're going to have an unpredictable branch at some point with these things. You're just trying to minimize the number of times it happens because otherwise…

00:47:54 [HR]

Well, okay, there's that. Now there are two factors involved. I can increase the predictability. I mean, you're right. I save a branch. But I also make the thing more unpredictable. Suppose in this case that I just described, suppose A is equal to B half the time, but C is equal to D almost never. Well, now I've converted two branches, one of which mispredicts half the time into one branch that almost never mispredicts. It's a big advantage.

00:48:27 [ML]

Well, although if almost never is rare enough, maybe you want to just put the C to D comparison first. So it's all data dependent.

00:48:36 [HR]

If you knew it in advance, that's right. It's all data dependent to the extent that you know you should lead with the conditions that you expect to fail that have the dependent ones and then end with the ones that you expect to succeed. Anyway, the point is there are a lot of things you can do to minimize branch misprediction. You can use bit arithmetic. Very importantly, you can use Elvis operators, [06] conditional expressions. It's called the Elvis operator because of question mark colon and some emoticon. Those execute after in the pipeline. They don't have predicted branches. They're like branches, but they don't require prediction. They give you tremendous scope for conditional operations without the risk of a branch misprediction. My rule is I try to avoid ampersand, ampersand and or, or as much as possible unless I know the values are predictable. If the branches are predictable, then they're the fastest way to do it. Oh yes. If any listener can answer this question, I've searched and haven't found an answer. There are actually two pipelines in the x64 architecture. There's a pipeline that starts decoding back at the instruction stream. And then in the middle, there's a, what they call the micro op cache, which has got decoded instructions ready to be executed. It would stand to reason to me that if you have a pipeline break, it's going to be satisfied out of them that that where the new location for execution is going to be the micro op cache that should have less penalty than one that goes all the way back to the beginning of the pipeline. And to the extent that I can measure it, it seems to be a little faster, but I sure would appreciate it if anybody has actual data on that. That's the end of that section.

00:50:33 [CH]

Well I guess, I mean, at some point I want to ask to get, yeah, input from Geoff and Marshall on to what extent the BQN and DyalogAPL interpreters do this stuff. But I'm not sure how many sections are left and should we just wait till the end of the sections?

00:50:48 [HR]

I got 20 minutes probably.

00:50:50 [CH]

20 minutes? What do you think?

00:50:52 [ML]

Well, the BQN answer's pretty short.

00:50:54 [CH]

All right, well, yeah. I don't know, this is section five or six that we finished?. We'll get a very short update from Marshall on the BQN answer, and then maybe we can hear from Geoff.

00:51:05 [HR]

Okay, so after that lengthy discussion of how bad pipeline breaks are, how do you actually use that to make your parser run faster? Well, execution in J means we have found an executable fragment. We found a sequence of three words that can be executed, and now we want to go and execute them. So what that involves then [is] you have to load the arguments into registers; there'll be arguments in the routine. You have to load the address of the routine that you're going to execute. Then you have to vector off to the routine. [There's] a feature that I added because the original J interpreter did not free arguments until the end of a sentence, and that led to excessive cache footprint. So there's a phase right after the execution of the routine where the interpreter decides whether it can free up arguments and whether it needs to account for arguments that were locked because of multi-threading. So that's an extra thing. Then you have to close up the stack. So how can we do this with a minimum amount of overhead? We have to face is that indirect branches are a terrible thing, unless it's in a loop (if you have a Duff loop or something like that, it's not so bad). The branch prediction for indirect branches cannot really be much more sophisticated than hoping it did the same thing it did last time. And if you're executing user functions, unless [say] the user does two adds in a row, that's great; it'll be right. But if the function is not repeated, there's going to be a pipeline break at the time of the vector off to the execution routine. And also, there's a load latency. Remember, we said we had to load the arguments; we have to load the address of the routine, and then we branch to it. But it's not going to know that the branch was mispredicted until that load has finished. So the cost to us is the latency of the load, plus the latency of a pipeline break. But this gives an opportunity. All that extra stuff that I talked about (where we're figuring out whether you need to free up a block that was not used by the function, or whether you have one that was protected by threading), that could be jammed into about 30 instructions that don't have any conditional branches. So we load the routine address; we load the arguments, and then we fill the execution pipe with a bunch of instructions that take some time to execute because they include loads. But we're able to fill the pipe before we execute the vectoring to the routine that we know is going to cause a pipeline break. After the pipeline break, all those instructions that have not been executed yet continue to execute, and so they don't represent dead time. As the pipeline fills again, those instructions are still being executed, and in effect, we get that 30 or so instructions for free during time that would have been otherwise a branch. So that's the limit on what I can do with a computer. The next question is, you've got your other opponent, which is the compiler. Actually modern compilers are fantastic at code generation. They generate just the right code. They're good at managing the pipeline, which is knowing where the CPU is going to be busy as instruction scheduling. They're pretty clever at moving data around between memory and registers so that registers are holding useful variables. But they don't always make the best judgment about what's useful. In particular, anything that's in a loop, they assume is very important and will strain (I'm talking about clang here, which is the one that we use; the one I know best), but anything in a loop will be preferentially put into registers. So you have to be prepared to guide the compiler. The first way is to use likely, unlikely, or set probability to tell the compiler the likelihood of the different branches. Use atomic load operations. The compiler will defer loads as late as it thinks it can get away with it. A lot of times that's good. A lot of times it's not. You can override it by using atomics. Also the compiler will inline subroutines, which is often a good thing. Well, inlining reduces the overhead of a call, but has its tendency to use more registers. So if you know that a subroutine is not going to be called very often, you might be best off to prevent it from being inlined to get better register usage. And then sometimes you can just go in and take over from the compiler. First you want to reduce the number of variables you have; combine flags into a portmanteau register with flags and variables; use lower address bits. And sometimes the compiler just cannot be put off; it insists on assigning a variable to a register. In that case, make up a dummy subroutine and call the subroutine with the address of that variable. That'll shut the compiler up. It can't do anything with it once you've done that. Well, it can do a little bit, and what it does is good, but it won't waste one of your precious registers. The place where you run out of registers most are after subroutine calls so you can reload variables right after a subroutine call so the compiler won't be tempted to carry it in a register. Rather than having a void function, have the function return something so you can pass something into the function and get it back. That way, in effect, you've saved another register. If you do all this and you get to the point where the compiler is not tempted to spill things to memory, it does a very good job. And that's where the J parser is now. It's entirely out of memory with none of the latency involved in register spills and restores. Anyway, that's what's going on under the hood when you say "count = count + 1".

00:57:35 [BT]

And the cost of the registers, it's because you don't want it to spill over and then have to store things in memory. You want to keep it in registers, and that's why registers become a thing that you really want to conserve, right?

00:57:48 [HR]

Well, it's a matter of latency. If the compiler spills something to memory, the loads and stores are very fast. It's just that when it comes back from the subroutine, it has to load something from memory and then it's five cycles before you can use that value. And we're talking about situations where five cycles is all it takes to finish up execution. It would greatly increase that if it had to restore registers.

00:58:13 [BT]

Yeah, and if you got it in a register already, you don't need to do that load. That whole sequence is already there for you.

00:58:18 [HR]

Right.

00:58:19 [GS]

You use the clang compiler?

00:58:22 [HR]

Yes.

00:58:23 [GS]

Does that mean you're not doing decimal floating point for any of your modules? No decimal floating point?

00:58:29 [HR]

That's right. J doesn't do decimal floating point. You needed a certain compiler?

00:58:34 [GS]

The IBM compilers (the old one, which wasn't clang based) had type declarations for decimal floating point and generated all the instructions and they were hardware instructions on B-series or Z-series. But Intel never implemented hardware instructions for it. And not only that, they changed the internal format, which was a pain [Rich agrees]. But the thing we found is the clang compiler has never been updated to support decimal floating point.

00:59:11 [HR]

Right, it's not part of the J language.

00:59:14 [GS]

It's really useful. In fact, if you're in commercial applications that are doing currency conversion, [you] actually need 18 digits and you can't quite get that on 64-bit floating point.

00:59:29 [HR]

Ah, that's true. We do have 128-bit floating point now.

00:59:34 [GS]

Oh, okay, so you're doing it on 128-bit binary floating point.

00:59:39 [HR]

I don't think we have any customers that are in that business [chuckles], actually.

00:59:44 [GS]

Oh, okay.

00:59:45 [AB]

But Dyalog definitely has customers that have to have more precision.

00:59:50 [HR]

Yeah, we talked about that at Cambridge. Well, anyway, I don't know if you thought that's what you were asking for, but that's what the interpreter deals with, at that level.

01:00:00 [BT]

So at one point, Henry, you were talking about taking debug out of the equation. After you've made all those improvements, do you put it back in because you need debug?

01:00:09 [HR]

Yeah, yes, the debugger still runs. It's just that the debug path is separate from the high-performance path. When debugging is engaged, it allocates a debug frame. Also I just don't want to corrupt the main line with anything that's not related. I don't want to put error paths in the main line. So the interpreter used to store a fair amount of information for use in case there's an error. What I have instead is an error analysis routine that goes through a fairly lengthy postmortem to try to figure out what happened to be able to reduce the error. It's a bit more code, but it's code that's not executed unless there's an error.

01:00:55 [BT]

And you implemented that in J9.5, didn't you?

01:01:00 [HR]

Postmortem debugging in that sense you're talking about was 9.6. But I just mean after any error, it goes back and reconstructs what the operands to the error were and where the error was, rather than every time you execute a fragment. What it used to do before it executed a fragment [was] it would store error information in case that fragment failed.

01:01:24 [BT]

This reminds me of when I was like 12 years old and I was trying to get out of work. I'd always figure out ways to get out of work before I even needed to start it, right?

01:01:29 [HR]

Very useful skill you've developed at a young age [Bob laughs].

01:01:38 [BT]

My mom didn't think so [laughs].

01:01:42 [GS]

We had a headmaster that always used to say he could tell the mathematicians because they were the lazy ones.

01:01:48 [CH]

All right. So Marshall, do you want to weigh in on how much of this machinery that J has, BQN does something similar? And then maybe we could get the same thoughts from Geoff: You said, Marshall, your answer was short.

01:02:01 [ML]

Yeah, I'm not sure you really realized how short this answer is. Are you ready for it?

01:02:08 [CH]

I'm ready. Hit me.

01:02:09 [ML]

Nil.

01:02:12 [CH]

[Laughs] Say some more though, because BQN is also immensely fast.

01:02:15 [ML]

I do have to explain the answer. And BQN is eventually interpreted. But we have a context-free grammar, which means you don't have every expression in the source code. You can look at that expression, and not the stuff outside the expression, and determine what role in the syntax the expression has. And I mean, the way we do this is by just having these spelling rules for names so a capital name is a function. I've described this in my five-year review that I talked about as just way too complicated, but blocks are the types determined by headers, and what variables are inside. So what that means is instead of interpreting the code and figuring out what role everything has while you're stepping through execution, you just do it all ahead of time. And also, you can do it all at once in an array style because if there's a modifier over here that's got its two operands, that doesn't interact with the modifier in some different expression. So we have this nice array compiler that sorts out all the syntax using array programming. And it spits out bytecode, [07] which is just a sequence of operations that work on a stack machine, actually. So implicitly, there are a bunch of values on the stack, and this operation will say, take the top three values off the stack, and apply the middle one as a function to the other two and things of that sort. So at that point, we have an interpreter for the stack-based byte code. But this interpreter doesn't have to know anything about the syntax at all. It just needs to know how the stack ... [sentence left incomplete]. Well, I guess it's the byte code syntax, which is much simpler. So it doesn't have all these questions that it has to resolve. I mean, I said some things about how really the best way to do things is to get all your values in an array and use vector instructions on them. The compiler's able to do that. The really nice thing about it is that I really haven't optimized the compiler. I mean, I followed certain rules when I was writing so I didn't _not_ optimize it. But I've never gone back to the compiler and said: "well, I really need to rewrite big sections of this to make it faster". Instead, the array operations are pretty within some fraction of as well-written as they could be. And the way to speed up the compiler is really to speed up the array operations in the interpreter. So that's really nice because at the same time that we're speeding up all the array programming that you want to do, we're speeding up how fast our code compiles as well [Rich agrees].

01:05:17 [CH]

So completely different model, therefore [Marshall agrees], not necessary, basically. And Geoff, how about all the work that you've done in the past? Does any of this ring bells of similar techniques you've used?

01:05:29 [GS]

On occasions, but not for the parsing. The places where we've tended to concentrate hardest on the code are things like dyadic iota and stuff, which is what penalizes most applications. So we've done loads of work on that. Roger Hui did an enormous amount of work on that. I did some earlier. Marshall's done some on that. So we've tended to concentrate on primitives. One of the things that changed me a lot is in the very early days, I went across to a photocopier company in Holland who were modeling the code for their photocopiers. And I realized at that point that they were throwing bool arrays around and our bool array code wasn't very efficient. So I did a load of work so I could do parallel operations on bool arrays and coping with the sort of alignment in the middle as it goes from row to row and all that stuff. So I did a load of that stuff and it has paid enormous dividends to have done that. If you're using Dyalog APL, those one bit bools really pay dividends. I don't know whether J's got one bit bools or not.

01:07:01 [HR]

No

01:07:02 [ML]

I can say they're used a lot in the BQN compiler as well. The types are going to be small integers, but you'll do lots of comparison on the types and say: "is this an operator? is it a one modifier? is it a two modifier?" and so on.

01:07:22 [CH]

Maybe as a preview of our future ... [sentence left incomplete]. I guess this isn't really primitive talk; this is more like parsing talk [Henry agrees] in the same flavor, but we haven't talked too much about primitives. But if you had to choose a top three, Geoff, of primitives that you've worked on (and maybe Henry and Marshall you can answer as well) what would they be? What would you be curious to hear a discussion on (like you mentioned, dyadic iota) of the interesting techniques? And it can be ones you personally worked on or ones that you just know are interesting.

01:07:57 [GS]

I don't know. I'd have to think about that [chuckles]. The sort of inner products are quite interesting.

01:08:02 [ML]

Yeah, that's why I left those out.

01:08:05 [CH]

[Laughs] Feel free to think about it and you can email us and we'll take that into account of which ones we cover first on our primitive talk series.

01:08:14 [ML]

Well, the dyadic iota search functions are definitely one that's up there [Henry agrees].

01:08:20 [CH]

All right. Maybe that'll have to be the first primitive that we cover then.

01:08:25 [HR]

Well, there's a whole family of them. All the search primitives are of critical importance. They're behind all the partitioning modifiers too.

01:08:37 [GS]

Modifiers? Can you clarify?

01:08:40 [ML]

Like key, right?

01:08:41 [HR]

Key.

01:08:42 [GS]

Key. All right. Yeah.

01:08:44 [ML]

And one thing that I don't think any array language is really that good at is search functions on strings. So in particular, taking advantage of the fact that if you have a list of lists, possibly every list in that is actually the same type and rank. So there's just so many different cases that search functions could deal with.

01:09:14 [GS]

One of the historical aspects of Dyalog APL in particular is we started off with an interpreter on the Zilog 8000. We had 64K of address space for the code and 64K of address space for the data. So we tended to write code that didn't use very many instructions. And as we've gone on, we have gone back and rewritten code so that it can use a lot more instructions. But it's still quite a tight interpreter.

01:09:50 [BT]

Would it be safe to say that there's always a balance between the amount of space you're using and the speed? As you give yourself more space, you should be able to move faster through some of it using some of these techniques?

01:10:02 [ML]

Well, the big advantage is that you get to use different algorithms. So like the string thing I'm talking about, you would just rewrite it. You wouldn't try to share code with the rest of the search function. So as you start supporting a lot of different cases, you might also have things like if one side of the search function is really small, you might do a completely different thing; like you might compare to every value even. That's just a completely different method, so you rewrite it. And that space allows you to kind of take advantage of more different situations. Henry was talking about inlining. Another thing that clang is really aggressive about is unrolling loops. That can have some advantages. But it's kind of just, there's no real advantage to having a small binary anymore outside of like really extreme scenarios. Especially if these are all like different loops, and you're only going to use one, because then all that's happening with that memory is that it's sitting on the disk. Well, your disk can fit a whole lot of code so that's not really a concern.

01:11:20 [GS]

Yeah, where it is a concern is when it comes to QA'ing your code. [08] Because the poor guy who's writing the QA has to know about all these algorithms switches that are happening in order to be able to QA.

01:11:34 [ML]

Yeah, because I if you have this special code for strings, and you don't test searching strings, I mean, you might think: "well, I tested the search function; I tested with all sorts of different values and stuff; I even tested with a mix of strings and numbers; I tested with arrays of different ranks". But you didn't test specifically a list of rank one character arrays. Well, hopefully you wouldn't specialize on just characters. But yeah, you pretty much have to know the internals of the interpreter to be able to test everything that's handled, because there's no way to know from the outside what the implementer one cares about.

01:12:09 [GS]

Not only that, it blows up the size of your QAs quite a lot. So they might not run overnight [laughs] on the various pieces of kit you're trying to run them on.

01:12:22 [ML]

Yeah, there are ways to reuse code, to not use too much code for all the tests, but all the time spent running them is going to be pretty large.

01:12:33 [BT]

And I guess the speed thing is, you're always trying to increase the number of registers; increase the number of the quicker caches over the expense of the lower caches, and then finally to the actual disk. The more you can increase those faster things, the faster your machine gets. So it's not overall space, it's the where that space is allocated.

01:12:54 [ML]

Well, I mean, that's kind of the micro-optimization level. You've also got stuff, like we mentioned: if you if you want to compare every value and see which ones are between 1000 and 1099, and you know, the array is sorted, well, then you can use a completely different algorithm. So with with the micro-optimization, you can get, in good cases, a factor of two or three, if it's the same code, and you're just going from not very carefully written to, very specially optimized. If you're choosing a better algorithm, there's really no limit to how much better you can do [Henry agrees]. I mean, there's no limit to the amount of improvement. There's usually a limit if you do an operation on the whole array: you are going to be limited by the amount of time that it takes to read the array and write the array. So there is a hard upper bound on that.

01:13:53 [HR]

Well, no, no, like, if you know the array is sorted, you might do a binary search and search just a tiny little bit.

01:14:00 [ML]

Yeah. In that case, you don't actually have to look at the whole array. And those are fairly rare.

01:14:06 [CH]

All right. Well, we have, as always (but in this time in particular) blown by [chuckles] the one hour mark. And we have covered quite a bit of content. So we will implore our listeners, if you have feedback or specifically an answer to Henry's question from earlier, you can reach us at:

01:14:27 [BT]

contact@arraycast.com. And we look forward to your answers to things like Henry's question, but also your input on this, because we've sort of diverged and gone a slightly different direction from what we normally talk about the higher level array languages. And instead of talking more about the lower level implementation, which I think if you're really into doing array languages, it's useful to know because if you know the things that are involved with putting this together, you're more likely to put your code into an area that optimizes those things. And I'm thinking particularly (this has given me insight into how Henry's done some of his special code within J) there are certain combinations of primitives that are much quicker. And I now understand why they're much quicker [chuckles] if he's taken those and actually optimized in those areas that he wouldn't make me do generally. But if you put that combination together, it's going to be quick for you.

01:15:24 [HR]

Well, that's more what Marshall was saying, that the special combinations allow you to use a different algorithm for those combinations.

01:15:33 [BT]

Yeah. But in that case, what you're doing is you're saying: "if you know you're going to be using this this way, use this part, and I'll interpret this part differently because I know that's what you're saying".

01:15:46 [HR]

Oh, yes. Yeah.

01:15:52 [BT]

So, I think there's real use even at a higher level, but I think at a low level, it's fascinating to hear the different things that you need to go through to make things quick.

01:15:59 [ML]

Yeah, but [with] the sudden turn in direction, I fear some of our readers are going to be stuck for 14 clock cycles or so. No one could have predicted this. [everyone laughs]

01:16:11 [BT]

An unpredicted branch has happened in the ArrayCast.

01:16:15 [CH]

[Laughs] I have nothing to say. Thank you so much, Geoff and Henry. I mean, we're definitely gonna have Henry back, as we've already got you like slotted for two episodes in the future. And Geoff, maybe we'll have you back if you're willing to talk about some of the primitive implementations that you said you've maybe spent more time on. Yeah, we can chat about that, because I know that is a direction we are taking this podcast in, to spend time deep diving on individual primitives and the work that goes on behind them.

01:16:46 [GS]

I'll have a think about that. [Bob laughs]

01:16:50 [CH]

All right. With that, we will say, Happy Array Programming!

01:16:53 [everyone]

Happy Array Programming!

</details>
