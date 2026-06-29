---
title: "Episode 60: Rob Pike - Array Languages are Important"
date: 2023-08-19 00:00:00 +0000
episode: 60
buzzsprout-id: 18617067
keywords:
- array-programming
- array-languages
- conor-hoekstra
- numerical-accuracy
- numerical-analysis
- jlanguage
- apl
- bqn
- rob-pike
- go-language
mp3-url: "/assets/audio/episode60.mp3"
episode-type: full
explicit: "no"
block: "no"
layout: podcast
excerpt_separator: <!--more-->
redirect_from:
  - "/episodes/episode60-rob-pike"
  - "/episode60-show-notes"
---
Rob Pike, co-creator of the Go language and UTF-8, tells us why every programmer should know about the array languages.
<!--more-->

**Host:** Conor Hoekstra

**Panel:** Marshall Lochbaum, Adám Brudzewsky, Stephen Taylor and Bob Therriault

---


## Show Notes

Array Cast -  August 18, 2023

Thanks to Bob Therriault, Conor Hoekstra, Marshall Lochbaum and Adám Brudzewsky for gathering these links:

**[01] 00:01:15**

- [Adám's Leet code playlist](https://www.youtube.com/watch?v=MUNPk6_ro4o&list=PLYKQVqyrAEj_6ZSDwha9PeftgKKHeDJ7-)
- [Jot Dot Times - APL News Aggregator](https://apl.news/)

**[02] 00:03:08**

- [Rob Pike](https://en.wikipedia.org/wiki/Rob_Pike)
- [Talks 2007-20016](https://www.youtube.com/playlist?list=PL3NQHgGj2vtsJkK6ZyTzogNUTqe4nFSWd)
- [Go Time podcast #100 - Creating Go](https://changelog.com/gotime/100)
- [Ken Thompson](https://en.wikipedia.org/wiki/Ken_Thompson)
- [Robert Griesemer](https://en.wikipedia.org/wiki/Robert_Griesemer)
- [Go Programming Language](https://en.wikipedia.org/wiki/Go_(programming_language))
- [The Go Programming Language and environment](https://www.youtube.com/watch?v=YXV7sa4oM4I)
- [Ivy Programming Language](https://pkg.go.dev/robpike.io/ivy)
- [aplwiki.com/wiki](https://aplwiki.com/wiki/Ivy)

**[03] 00:05:50**

- [UTF-8](https://en.wikipedia.org/wiki/UTF-8)

**[04] 00:07:27**

- [2741 terminal](https://en.wikipedia.org/wiki/IBM_2741)
- [TryAPL](https://tryapl.org/)

**[05] 00:08:40**

- [Stephen Wolfram](https://en.wikipedia.org/wiki/Stephen_Wolfram)
- [Mathematica Programming Language](https://en.wikipedia.org/wiki/Wolfram_Mathematica)
- [Lisp Programming Language](https://en.wikipedia.org/wiki/Lisp_programming_language)

**[06] 00:11:09**

- [Plan 9](https://en.wikipedia.org/wiki/Plan_9_from_Bell_Labs)
- [Bell Labs](https://en.wikipedia.org/wiki/Bell_labs)

**[07] 00:12:10**

**[08] 00:17:20**

- [Russ Cox Advent of Code videos](https://www.youtube.com/playlist?list=PLrwpzH1_9ufMLOB6BAdzO08Qx-9jHGfGg)

**[09] 00:18:45**

- [J programming Language](https://www.jsoftware.com/#/)
- [Raul Miller episode on the ArrayCast](https://www.arraycast.com/episodes/episode59-raul-miller)
- [Transcendental functions](https://en.wikipedia.org/wiki/Transcendental_function)

**[10] 00:28:35**

- [q Programming Language](https://code.kx.com/q/learn/)
- [apl.wiki/q](https://apl.wiki/q)
- [Joel Kaplan episode on ArrayCast](https://www.arraycast.com/episodes/episode27-joel-kaplan)

**[11] 00:31:21**

- [Ken Iverson](https://en.wikipedia.org/wiki/Kenneth_E._Iverson)
- [Stop Writing Dead Programs Jack Rusher](https://www.youtube.com/watch?v=8Ab3ArE8W3s)

**[12] 00:35:00**

- [Leading axis agreement](https://aplwiki.com/wiki/)
- Leading_axis_theory)

**[13] 00:38:15**

- [Arthur Whitney](https://en.wikipedia.org/wiki/Arthur_Whitney_(computer_scientist))

**[14] 00:45:15**

- [Nested Array Theory](https://aplwiki.com/wiki/)
- Nested_array)

**[15] 00:50:00**

- [APL wiki](https://aplwiki.com/wiki/)
- [Dyalog documentation](https://www.dyalog.com/documentation_182.htm#CORE)
- [APLwiki documentation for Take](https://aplwiki.com/wiki/)
- [Take](https://mlochbaum.github.io/BQN/spec/index.html)

**[16] 00:52:09**

- BQN Programming Language specification
- [IBM specification APL2](https://www.ibm.com/downloads/cas/ZOKMYKOY)
- [Go Programming Language specification](https://go.dev/ref/spec)

**[17] 00:53:25**

- [Rank operator](https://aplwiki.com/wiki/)
- [Rank_(operator)](https://aplwiki.com/wiki/)

**[18] 00:58:23**

- Right tack function
- [IdentityCombinators](https://en.wikipedia.org/wiki/Combinatory_logic)

**[19] 01:02:25**

- [John Scholes Game of Life](https://www.youtube.com/watch?v=a9xAKttWgP4)
- [Simplicity is Complicated](https://www.youtube.com/watch?v=rFejpH_tAHM)
- [20] 01:10:40 Contact AT ArrayCast DOT Com


<details markdown="1">
<summary><strong>Transcript</strong> (click to expand)</summary>

Transcript

Transcript prepared by Bob Therriault, Igor Kim, and Sanjay Cherian

Show Notes

00:00:00 [Rob Pike]

Half the people look at that and think this is insane, how could you think like that? And the other half say, what's going on? This is pretty cool. But if you're open to more ideas or have programming in other languages, let's put that in there, then you might get attracted to the possibility that there's something really interesting going on behind those peculiar symbols. But I think some people are just not as curious as some others.

00:00:26 [MUSIC]

00:00:36 [Conor Hoekstra]

Welcome to another episode of Raycast.

00:00:38 [CH]

Welcome to another episode of ArrayCast. My name is Conor and today with us we have a very special guest. But before we get to introducing him, we're going to go around and do brief introductions. We'll start with Stephen, then go to Bob, then to Adám, and then to Marshall.

00:00:49 [Stephen Taylor]

I'm Stephen Taylor, APL and k programmer.

00:00:53 [Bob Therriault]

I'm Bob Therriault. I'm a J enthusiast.

00:00:56 [Adám Brudzewsky]

I'm Adám Brudzewsky. I'm a professional APLer.

00:00:59 [Marshall Lochbaum]

I'm Marshall Lochbaum. I'm a former J programmer and Dyalog developer, and now I work on BQN, which is my programming language.

00:01:05 [CH]

And as mentioned before, my name is Conor. I'm a polyglot programmer, but a huge array language enthusiast and your host today. So I believe we have two announcements. We're going to throw that to Adám, and then we'll get to introducing our our special guest today.

00:01:18 [AB]

Okay, so one is just briefly that I started recording some videos where I present APL solutions to lead code problems. [01] The subset known as Neat Code 150, apparently it's like a subset of all the lead code problems that are uniquely geared to prepare you for coding interviews at big companies. The other thing is that I've taken over running the jot.times. So jot.times is a revival of a very old name for an APL newsletter. And while that used to have actual content in it, this is just a news aggregator. So whenever I'm aware of somebody publishing a blog post, article, something about APL array programming, then I'll put it in there. And you can find it on apl.news. And we're really excited to hear from anyone. Anything that's been published, it's hard for me to keep track of everything that's published on the internet. So if you know something that's not there, please do let us know.

00:02:29 [ML]

Well, how should they get in touch?

00:02:32 [AB]

Well, any way you can get in touch with me, or there's a contact email address at the bottom of the site for those suggestions at apl.news. Or look, GitHub issue. It's just a GitHub pages site.

00:02:46 [BT]

Or an early plug for contact@arraycast.com, because we'll certainly pass it along if anybody gets in touch with us.

00:02:51 [AB]

Us. Yeah, that works too.

00:02:54 [CH]

Awesome. So links to all of those emails, apl.news, and links will be in the description-- or not the description, in the show notes. And with that out of the way, we will get to introducing our special guest for today, the one and only Rob Pike. So many of our listeners are probably already familiar with Rob, [02] but I will do an introduction. Uh, anyways, so Rob Pike is probably most famous for being one of the co-creators of the Go programming language, which according to several different websites, if you average them is the number 10 ranked programming language in the world, which is pretty outstanding considering that it was only created or work started. occurring on that, I believe, sort of right before 2010, the 2007, 2008 range, from the stories, at least, that I've heard. He co-created the language with, I believe, Robert Griesemer and Ken Thompson, who's probably, you've heard of at least one of those two individuals as well. So we might talk a little bit about Go. The reason that we're having Rob on today is because he tweeted or tooted-- I don't actually know what the right term is for Mastodon-- about one of his other projects, which is an array language that is written in Go called Ivy, which he actually notes in the sort of thread that is actually his second attempt or work on an array language-like thing. On top of all this, he also, well, he worked on Go while he was a distinguished engineer at Google for just under 20 years, and before that worked at Bell Labs alongside some very other famous people like Bjarne Stroustrup, who worked on the C++ language. While he was there, I think he spent most of his time working on Plan 9, but also worked on a ton of other things. He's also a co-author of two books with Brian Kernighan. So his resume is very, very long, a veteran of the industry. And we're super excited to have him on the podcast today to talk not just about programming languages in general, but his sort of experience with and thoughts on array languages. I'll read the quote that sort of got him here, which is in the midst of the thread. I'm not gonna read the whole thread 'cause that doesn't make for exciting podcast content. But at one point, Rob tweets or toots, the thing is if Lisp is about lists and recursion, APL is about matrices and loops, but the loops are completely hidden, which is magical and profound. So with that, I'll throw it over to Rob. If you wanna do, I don't know, maybe a brief introduction

and say anything that I've missed that you think is worth mentioning, and then we'll get into a discussion about sort of Ivy, Array Languages, Go and everything related.

00:05:22 [RP]

Sure, thanks so much for inviting me. That's a pretty good introduction. I'd like to make two minor corrections. One is I don't think of Ivy as a language. I think of it as a calculator. We'll come back to that. It's not at the level of programmability that the other array languages you speak of are, but it has unique properties of its own, which I'm sure we'll get into. The other thing is I probably am best known for Go now, but the thing that I think is of the biggest effect on the world is with Ken Thompson, one night in a diner in 1992, we designed UTF-8. [03] And I think it's really interesting that the biggest effect that my work has had in the world was basically done on a placemat in the diner in 20 minutes one evening. It's funny how the world works. So every time you send an emoji or for that matter, type an APL character in a modern terminal, you can thank Ken and me for that. We made that as easy as it is nowadays.

00:06:17 [ML]

You had nothing to do with UTF 16, right?

00:06:20 [RP]

No, UTF-16 is not a good idea. That's another story. I can talk for an hour about this problem, but let's not. I'm actually a little bit sort of out of my depth here because I am not an array language expert at all. I'm fascinated by them. I think the biggest APL program I've ever written might be 20 lines long. So I'm really not experienced or skilled APL programmer. But unlike, I think given the ages of most people here, I'm actually one of the people here who has used the original IBM APL on the 360 because I first saw APL in my first year physics classes back at the University of Toronto in the 1970s when they used APL with a 2741 terminal speed ball, you know, thing, [04] golf ball typewriter 2741 to do some of the physics labs work. And so I actually learned about APL because I had to use it for these assignments. And we weren't actually programming much APL in those assignments. We were just using it as an interactive learning aid. But it exposed me to it. And the University of Toronto had a very open attitude towards people using their computing resources. And so I could go in after hours, sit down in one of those terminals, log in and actually play around. And it got me interested in them back in the day. For those of you who weren't around then, it was a very different time. It was 134.5 baud, which is as slow as it sounds. And the thing that I think people forget is it was also half duplex, which meant that when the terminal was printing, the keyboard was not only not responsive, it was locked, and you could hurt yourself if you tried to type while it was talking back at you. So it was an angry time. But back then, that was the only interactive computer that most people would see because everything else was batch. I had done a little bit of interactive stuff on a controlled data thing as a high school student, but APL was way more interesting at the time. And I actually studied physics, then went and did graduate work in physics and ended up at Bell Labs. But while I was an undergraduate I was in the same, sorry, a graduate, well, I was a graduate, I was in the same graduate class as Stephen Wolfram, [05] who later went on to do Mathematica. And we actually worked together with a few other people there to build a system, sort of that became in fact, the precursor of what mathematical was. And it was based on a reaction, it's a very long story, and I can't tell all of it, because you know, physics, it's annoying. But they were using the KL 10 at MIT, to run maxima in order to do quantum electrodynamic and quantum chromodynamic calculations. And the KL 10 was I think, a 256 kilowatt, 60 bit machine, It was a 36-bit machine, pardon me. And it just wasn't up to the problem. And so a couple of us there who knew a little bit about Lisp suggested we write a list for the VAX11780 that had just come out. And Don Mishel actually wrote a Lisp for that machine. It had a life of its own in the end. It was pretty interesting. Lisp 1.5, like really simple Lisp, but still Lisp. And we built some interesting stuff with it. And one evening I was kind of bored. And so I said, I wonder if I could to write an APL in Lisp. And in the space of just a few, like two or three days, I had something that reacted semantically very much like the APL that I knew. It was, it's spelled differently. It was obviously, you know, ASCII only. It was not grammatically anything other than Lisp. It was, you know, open parenthesis, you know, three, four, row, iota, this, and you type all that stuff out. But the words like row and iota were, that's where I started using them myself in something approaching a programming language. I don't know if you know this, but Ken Thompson also implemented an APL when he was in University of Berkeley on sabbatical in '76. And Robert Griesemer, the third creator of Go, also did an APL when he was a student. So all three of us have in common that we've designed a programming language and we've implemented APL. So there you go.

00:10:35 [CH]

That's kind of weird. That is somewhere on the internet, because I recall I put it in a slide in a talk once that, uh, I had read somewhere, I think probably it was, it was on hacker news or something that all three creators, co-creators of go individually sort of on their own had done the same exercise independently, which I thought was, there's something there clearly.

00:10:55 [RP]

I'm the only one who's done it twice though. After grad school, I went to Bell Labs research, [06] worked in the Unix group there, did a lot of computer graphics, early computer graphics work, ended up doing plan 9 down the road. UTF-8 came out of that work, which was I think a really big deal. I sort of put my toe in the water when I was working in Greece one summer and the editor I'd written a year before called Sam turned out to be able to handle the Greek character set better than anything they could get from Microsoft. And so apparently Sam sort of caught on in Greece, which is kind of fun. But that got me thinking in the back of my mind about supporting languages from other places. And it was a very long road from there. But five or six years later, UTF-8 happened, and now it pretty much runs the internet. So that's pretty cool. And then many years at Bell Labs, lots of interesting things went on there, of course. Then lots of bad things happened, and I went to Google [07] around 2002, where I worked on a lot of infrastructure. And Go came out of that as a response to the difficulty of building network server programs in languages like C++ and Java. I'm quite proud of the way we brought concurrency into the systems programming mindset in a way that it really hadn't been before. And that's enabled some stuff to happen. Pretty much any new language now has to have some concurrency support in it. And I think we get at least a little bit of the credit for that. But I ended up being pretty senior at Google doing a lot of things that were less interesting but still very important. And one afternoon, Robert Griesemer, who had written a high precision number package with integers and then rationals designed to do cryptographic calculations, had this sort of dropped this thing on my desk. I said, what do you think of this? And I thought, hey, this should be a calculator. Let's have an exact rational arithmetic calculator. And so I sat down to write a calculator 'cause I liked writing little languages and it didn't take me very long to end up just doing an APL like one instead. And so I'm sure it's not the only one, but it's certainly one that I built. It was originally, Ivy was created as a simple toy for me to amuse myself in the form of an interactive calculator with exact rational arithmetic to arbitrary precision, which it still does. It still got all that in. And then later, like a year or two later, there's a property of Go that constants at compile time are high precision. So you can have floating point numbers  that are quite large as constants and combine them in expressions that will preserve higher precision until they're stored somewhere, like a floating point variable. So you can write things like pi over two or pi over 38 and not have it get incorrect low bits in the math. And the code to do that in the compiler was quite messy and to purpose, but Robert at some point decided that he should probably, I think I might've prodded him. I don't know if he did it first or I did it first, but the thing is I couldn't compute square root of two in Ivy and he did the floating point stuff, high precision floating point package to support the compiler. And I could use that inside Ivy. And there's some really interesting problems in Ivy doing high precision math, which we can come back to if you're interested. But anyway, nowadays it's got character data, integers of arbitrary precision, rationales of arbitrary precision, floating point numbers of very high precision, but you can control the precision. And so when you type something like,

you know, the factorial 100, it prints out a very large integer because that's exactly what it is. It's not floating point number the way the APLs of my youth were. I don't know what they are now in detail, but we can do some pretty interesting stuff with them. And I've seen some interesting number theory done with Ivy because it's good at that stuff. It's good at exact arithmetic with very large numbers and interesting stuff like that. And then I had a bad accident about a month ago, fell down, hurt myself. I'm okay, but it was pretty ugly. It was in the hospital for a while. And when I came home, I wasn't very mobile and I had nothing much to do. So I just decided to sort of dust off Ivy and get back into it again. So in the last month or so,it's become at least somewhat a nested APL, which it wasn't before. It's boosted in some of its capabilities. The famous Dyalog video with the game of life in it can be pretty directly translated now into an Ivy little program that works. Somebody did that for us. And so it's sort of my hobby play thing now. I left Google a few years ago, I'm retired now. And when I need to code, there's always something in Ivy that could be boosted. And I've got a long list of things I still like to do to it. But it's a lot of fun. And it is available on Android. It used to be available on iOS, but for political reasons, it's not, although it will reappear there. Although the version in mobile is very, very old. But the GitHub version, robpike.io/ivy, I kept up to date. The last commit was yesterday, I think. And it's a lot of fun. But I still tell you, the biggest APL programs I've written are tests for Ivy. I haven't actually used it to any real work in the life. It's just a hobby and it's really fun. But I would like to say one thing which was hinted at in that quote you read, 'cause I think it's really important to understand. A few, two, three years ago, Russ Cox, who is now the tech lead of the Go Project, did the advent of code. [08] And for about 80 or 90% of the problems, he decided to do them in Ivy. He actually tweaked Ivy a little bit to make it a little easier, but he showed how to do those problems using an array language. And he had never used a written array language before. He didn't know anything about them. But he was fascinated by the different way it made you think than the ways that he was used to with traditional sort of procedural languages for what we do for systems work. And that got me thinking about the narrowness of thought in most languages you see today, including Go. They're all kind of the same, and they're all kind of becoming more and more the same. And some people know about Lisp, especially Emacs users. Everyone knows about Java, JavaScript, C++, C, maybe Go, but hardly anybody in my circle knows about APL. When I gave a talk about Ivy soon after I started it, which is maybe years ago now, No one in the audience had ever seen an APL program or knew even what it was. And I think that's a shame because every different language you learn teaches you a different way to think. And APL's way of thinking is really fascinating to me. I'm fascinated by it, even though I'm not adept at it. And so maybe that's a good place to pause and see if you've got anything you wanna ask me about.

00:18:04 [CH]

I mean, there's a hundred things I could ask you about. I mean, maybe I'll pause myself and let some of the other panelists, if you've got questions to follow up and then I can ask them of mine later. Bob, I think I saw you potentially had something, maybe not.

00:18:18 [BT]

Well, the only thing I was gonna mention was actually Rob's talking about calculators. People who use J [09] often talk about being a calculator on steroids because it's a very programmable. And it actually, when I was looking at Ivy, there's a lot of similarities, which isn't surprising because of course it's an array language. But there are a lot of things that are very J-like, including the extended integers and the precision, which we actually had Raul Miller on last week or two weeks ago. And he was talking about implementing that in J, well, upgrading it, I guess, re-implementing it in J.

00:18:51 [RP]

Does it do high precision floats?

00:18:53 [ML]

It has rationals.

00:18:54 [RP]

High precision floats are an interesting problem because all the algorithms you look up work on 64-bit floating point numbers and have little coefficients and so on. And they're worthless when you've got a thousand bit number. And so the most technically interesting part other than the original design of it, which I actually would like to talk about, come back to that, is once I had floats in there and you could do simple things like addition, subtraction, division that Robert's library gave me. Square root was pretty easy, you use Newton's method, but the transcendentals are really tough because there's basically no guidance on how you do that stuff in any obvious thing that I could find. I'm sure there are people that know way more about it than I do. But there are a few real challenges. Arc tangent was a really interesting problem to get a high precision arc tangent implemented in a stable way that would convert quickly. Sine and cosine are pretty simple 'cause the Taylor series works, exponential is dead easy, but logarithm and exponential like X to the Y are really a challenge. And to do X to the Y, I needed a high precision value of log two. And I couldn't find one big enough. And so I sat there for a few minutes and I realized that I had all the tools in Ivy, even though it didn't have log2, to compute log2. And so I couldn't write it in the language itself, but I could write it with the code that I had inside Ivy. So I wrote a little sort of mini version of main that did something different. And I computed log2 to whatever it was, 10,000 digits or something. And then later stumbled on a copy of it on the internet and sure enough, it got it right. But I really had great satisfaction using it to do something as mundane as calculating a logarithm. But it's an interesting challenge when all the stuff you know about how to do sine and cosine with simple instructions or evaluating the coefficients of a simple expansion are simply not of any value. They're really fun to do. So if he decides he wants to do high precision floats, he's going to have some work cut out for him. And I'm not saying my algorithms are good. I know that the trigonometric ones have a very difficult time getting back to zero when you have pi. Like sine of pi is like 10 to the minus something huge, but I can never get it to zero. And there's convergence issues there in very low bits that I just can't lick. But I'm not a numerical programmer by nature, so someone who really knew what they were doing could probably do a better job. But those were really fun problems for me. I really enjoyed working on that. That was way more interesting than any management meeting I ever attended.

00:21:28 [CH]

It's a problem with seniority.

00:21:30 [BT]

Just to be clear,  J just uses 64-bit floats, so all the stuff you were talking about is fascinating and probably unexplored at this point. It sounds like it's terra incognito and there be dragons out there, but they're fun dragons to play with.

00:21:44 [RP]

They're fun dragons to play with, and I do not claim that my code is good, but as far as I can tell, it's mostly accurate. If you or your  J friends end up doing high-precision floats, I'd really be curious to know how you go about the transcendentals. And then when I put complex in, which I did last year, it was really fun putting in the transcendental functions for complex numbers too, but I had all the tools at my disposal. So it was pretty straightforward at that point.

00:22:11 [CH]

Adam, I think you were gonna say something earlier.

00:22:12 [AB]

Yeah, I noticed, well, obviously you say the main designers of Go have all done APL in the past. And then it says on Wikipedia, we'll take that with a grain of salt, that Go was influenced by APL I'm along with a lot of other programming languages. But are there actually any influences that you can identify?

00:22:33 [RP]

Yes, there's one. There's exactly one, which is the constant generator is called IOTA in honor of APL. The equivalent of an enum, not equivalent, but the parallel to a standard C enum in Go is a constant, and you can write a block of constants and expressions on the right-hand side that contain the word IOTA, count down. So if you just want a numerator constant, you can say, you know, x1 equals iota, x2 equals iota, and so on, and it counts. But you can also do more interesting things like, you know, two times iota, or one shifted up iota, or iota squared, or whatever. And that all works. That is the APL influence in its entirety, I believe. But it's there. And that spelling out of iota, I don't know that it happened before I did my stupid list back in grad school. But it probably did. But for me, I think I just typed IOTA because I couldn't type actual IOTA on my 24 by 80 glass terminal at the time. So that's how that came about. But you know, we were all APL aware. I think none of us was an expert. Ken did one for the PDP-11. I did one for the VAX in LISP. And Robert did one when he was a grad student, but I don't remember what he did it in. It was probably in Oberon.

00:23:50 [CH]

Stephen?

00:23:50 [ST]

Rob, a few minutes ago, you said that you found APL's approach fascinating. I wonder if I could press you to say a bit more about what you value about that approach.

00:24:01 [RP]

It's concision. It's an interesting, to people who first see it, you know, we used to talk about as a write-only language and I think that's unfair, but there's some validity to the complaint. It can be, you know, arcana to the uninitiated. But the concision of expression, and I don't just mean the funny characters. I saw a talk some time ago, I wish I could remember where it was, where somebody said, this is why programming languages are so difficult for people. Let's say that I have a list of numbers and I want to add seven to every number on that list. And he went through about a dozen languages showing how you create a list of numbers and then add seven to it. Right? And it went on and on and on. And he said, "Wouldn't it be nice if you could just type 7+ and then write the list of numbers?" And he said, "Well, you know what? There's one language that actually does that, and that's APL." And I think there's something really profound in that, that there's no ceremony in APL. If you want to add two numbers together in any language, you can add two numbers together. But if you want to add a matrix and a matrix, or a matrix and a vector, or a vector and a scaler or whatever, there's no extra ceremony involved. You just write it down. And we can get into the operators and the combinations of operations and functions and so on. But it's analogous in my mind, as I said in that-- I think the word is toot, but anyway that the Lisp guys are so comfortable working in Lisp and thinking about Lisp. And they know what it does. And they don't understand why the rest of the world doesn't think like them. And I think for certain problems, APL's thinking about, you call it an array language, I think that's a little unfair, because it's good at things that aren't arrays. It's good at vectors, it's good at matrices, it's good at tensors, it's good at complex arithmetic. But what it does is it abstracts away a lot of the ceremonial boilerplate that most languages we work in require you to use to be able to do something. For instance, in Go, multidimensional arrays are just awful. I mean, you know, they're not, we've actually tried very hard to figure out how to do them well and we couldn't. It's not that it's impossible, but doing it so that it fits in with the rest of the language is really, really difficult. And it doesn't matter that much because Go isn't the language that people tend to do large numerical calculations with. But having the ability to just pick up a matrix, multiply it by a vector or multiply it by another matrix or invert it or all these sort of linear, solve the least squares problems, all those sort of algebraic operations that we do in numerical calculations, you don't have to write down anything other than what the answer, what the problem you're trying to solve is. And I don't think there's another language on the planet where I can say that's true. I believe the fancy character set hurt APL because it made it look harder than it really is. And I think the more modern ones that use ASCII or have words in places, I think are a lot more approachable because the power is still there, but they don't look like, you know, sacred writing from an ancient time. I hope I'm not offending you.

00:27:23 [ST]

No, not at all, no. And I am personally very deeply grateful for UTF-8 and the ability to put this stuff into text files, simplified my world. You're pointing, I think, at something really quite profound and in a way, shocking. Because if you ask a non-programmer to add seven to every item in a list, and then you write out that solution, seven plus blah, blah, blah, blah, blah, it will seem, as you say, completely natural and normal. It's like, what is the problem here? But you ask someone who's been trained at computer programming to do it, and they'll be shocked that 7+ blah, blah, blah actually is a solution.

00:28:09 [RP]

Because where are the variables? Where are the declarations? Where's the scoping? Where's the module that does the blah, blah, blah? There's so much other stuff going on.

00:28:15 [ST]

I'm particularly interested in this because as you probably know, q [10] is a wrapper around a very APL-like language, k, which k4 is not publicly documented. It's not officially exposed. All the public see is q, which is wrapped up around it to make it easier for people whose brains have been trained by computer programming to write queries and get some stuff done. Of course, the wrapper doesn't teach them anything about the APL approach. It merely defers the need to learn it. In some cases, in many cases, forever. You never need to learn the vector approach. But I've seen many people struggling to get over that hump, to stop thinking in what an earlier guest on our program called the one potato, two potato approach, and to think in vectors is a real shift. I'm wondering if there's any insight you can share about that problem because I'm working on a book on how to get over that divide.

00:29:22 [RP]

Well, I don't know if I can help anyone get over that thing, but I faced that problem when I was trying to introduce Ivy to my team because they knew I was working on it, even though I wasn't supposed to be. I put into Ivy a demo mode. You set right parent demo and you get into a scripted demo where you can interact with it and it shows you a bunch of examples and talks you through how they work. And I have sat at a terminal or a desk countless times with a laptop and just gone through that demo with somebody to show them what it is. And seeing their eyes light up is always an amazing reward because most programmers today have never seen anything like it, right? Like, you know, shuffling a deck of cards, it's this easy, right? or all these are searching for prime numbers, although the APL prime number kata is not particularly efficient, but just seeing that they can see this, there's other ways to compute is really, really great. I don't know how to teach it as a thinking, 'cause I personally don't think I'm good at it myself. A lot of the stuff in the demo is stuff I found online looking for good examples, but I really love the way it warps my brain to free me from the way I tended to think. I don't like when everything feels the same. I don't like orthodoxy. I like to break out of orthodoxies. And APL is its own kind of orthodoxy, which is fine. But from the world I come from, it's as alien as the atmosphere of Jupiter.

00:30:55 [BT]

Do you think some of that lack of ceremony you were saying is because originally it was a blackboard language? You mean you're not gonna write down a whole procedure on a blackboard if you're trying to explain the ways you're manipulating matrices.

00:31:09 [RP]

Yeah, I agree with you. I think it was meant as mathematical notation. And even though it became a programming language, I don't know, I never knew Ken Iverson, [11] but I don't think he conceived as a programming language so much as a way of thinking about linear algebra. I may be wrong, I don't know.

00:31:29 [ML]

Well, he did name it after A Programming Language.So I think his idea of programming was not necessarily our idea of programming. Yeah. And I mean, the term has also changed its meaning somewhat.

00:31:41 [RP]

Right. But if he, you know, he's a mathematician, and so he used mathematical notation and, you know, power to him. And once you sort of see how those symbols work, it's really wonderful. But it is a fairly big wall to climb over when a beginner is just starting out with it. And I mean, honestly, I spent when I was working on Ivy, I spent a lot of time on Dyalog or the APL wiki trying to figure out what the symbols are supposed to do, because they're useful tools. But you know, a horizontal, you know, tack pointing right is not intrinsically anything that I can obviously see unless I've memorized it. It's more of a language than any other programming language I know, because it has its own symbology and semiotics and rituals. But having its own unique symbol space makes it a little bit harder. The beauty of it is that once you learn those symbols, the power that you get as a reward is worth it. But getting people to climb the wall to see what's on the other side is definitely a challenge sometimes.

00:32:46 [CH]

What is super interesting about what you just said. Also too, I'm going to pause and say there's a bunch of things that we will have links in the show notes for. So that talk that you were referring to, I'm almost positive was Stop Writing Dead Programs by Jack Rusher who gave it at Strange Loop 2022. It quickly became like the third most watched Strange Loop talk ever with close to 400,000 views and it's an awesome talk.

00:33:08 [RP]

That sounds right.

00:33:08 [CH]

If you want to watch that, link in the show notes. And also to the Advent of Code that Russ Cox did, I think there's a whole playlist where he shows them on YouTube, which I don't, I can't remember if you mentioned, but if folks are interested in, on seeing someone program with Ivy and solve problems, you can go watch the YouTube videos for those too.

00:33:25 [RP]

And those are models of explanation too. He's very good at explaining things.

00:33:29 [CH]

Yeah.

00:33:30 [RP]

Yeah, they're very well I mean he'd solve the problem and then he wrote a script and then he recorded the script so you get to see his thought process, but you also see a really clean explanation without any fumbling around. They're very well explained I think they're they're really good. They're actually a pretty good introduction to the whole idea of an array language.

00:33:48 [CH]

Yeah, it's amazing how sometimes I'll be working on a problem This is more when I was learning the language a couple years ago, but you're working on trying to solve something and you're kind of stuck in your C brain or your C++ brain or whatever you have and you're like, "Oh, this isn't probably possible in APL." And then you go watch some video of an expert doing it and they solve it in four and you're like, "What?" And you discover outer product or something like that and a rank-wise operation and you're like, "Hold, I didn't even, I thought this was a nested thing." If you don't know the different ways of solving or using array languages, sometimes it can seem incredibly difficult. But then the solution is extremely elegant. Marshall?

00:34:29 [ML]

So yeah, this is maybe a good place to jump in with something I noticed before. You said, well, in Ivy, it's just natural to add one of the things you said was a vector and a matrix. And at that point, I went, what? Because it's not necessarily natural. And actually, Dialog doesn't do it. So I checked. And what Ivy does is add the vector to each row of the matrix. And so I thought, oh, well, what j and some other languages do is to add it's called leading axis agreement. [12] And there's a different justification for it, but it turns out that it works the other way around. So I thought, oh, Ivy has trailing axis agreement. (Sometimes). And yeah, then I tried a rank 2 matrix and a rank 3 matrix, and I couldn't get them to add together. So I was wondering, what's the rule there?

00:35:20 [RP]

I fully believe that there's lots of stuff like that in Ivy, because I'm not an expert, and I do what seemed right, or I could figure out from trying some simple test. But sometimes I just went with my gut. I remember when I was doing the Lisp version back in grad school, when I had a book, which I fortunately lost for APL for the 360, and that was my only guide. But when I wrote the Lisp stuff, because the clarity and the dynamic programming and the recursion are so natural in Lisp, I found things like that. I'm not saying that particular one, but things like that, where it just seemed like there was more generality available than the actual APL provided. And I noticed in researching some stuff in the last few weeks, that there's actually a fair bit of discussion about just what some of those missing features should look like as in these other languages. And some of them disagree. And I'm not saying Ivy gets any of them right. I've tried to follow the lead because I'm fascinated by this question. If you have a good idea about a sort of kernel of a, of something like a programming language, development is something that's complete, requires filling in a lot of gaps that are not obvious from the beginning. and you can make mistakes, but also you have to be able to predict the right way to do something to solve a problem where you're not gonna face yet 'cause you don't even know it exists. One of the things that Ken Thompson is very good at, one of the things I love to work with him for, was he was better than almost anybody at that, at getting the solution to the problem you haven't thought of yet, to fall out naturally from the solution to the problem you're doing today. And I am fascinated by the step from the original idea of Ken Iverson writing some notation on a blackboard to something like a modern Dyalog or j, which is so much richer. And I think it's easy to forget the incredible amount of development in there about all the ideas of generality and expansion of things building on the framework, but also that you can make decisions in different ways along the way. They may be right or wrong for different problems, but what should they be? And if somebody points out that Ivy is inconsistent in some way, I might well think, you know what? You're right. I should probably change it because nobody it's not a big user base who's going to be offended by it. But yeah, I just said that vector plus matrix came out. It wasn't I wasn't thinking of anything in particular. And when you started talking about it, oh, God, does it not work? It kind of works.

00:37:58 [ML]

No, in this case, I do think it's perfectly fine and consistent. The reason j and BQN and Dialog, if it ever supports it, use leading axis is there's this whole framework that Arthur Whitney [13] developed that we call the leading axis framework, where basically you model an array with n dimensions as sort of a list of arrays within minus first dimension. And the list goes along the first dimension.

00:38:27 [RP]

When first, you mean like if you're writing out a shape expression. It's the first integer you write down as the first axis.

00:38:33 [ML]

Yeah. That's the leading axis.

00:38:35 [RP]

That's what you mean. Okay.

00:38:36 [ML]

In this model, if you add a list to a matrix, you're saying, "All right, I want to add a list to a list of lists," sort of. Then it comes out naturally that you should add each number in the list to each row of the matrix. Okay. But nothing else in Ivy that I've seen really has this leading axis framework. A thing that APL bring up a lot is that the leading access framework is really complicated and it's hard to get your head around when you're getting into it. So I'm not sure Ivy necessarily should take it up. If it did, it would make sense to use leading access agreement, but if it doesn't, you know, this vector plus matrix thing is what most people would expect, I think. So, nope, doesn't seem, seems like a fine decision to be.

00:39:20 [BT]

I'm not sure.

00:39:23 [RP]

I mean, as I said, it's really not obvious a priori. I had never heard of the leading axis framework, Although I think from its phrasing, I understand what you're referring to. And had I known about it, I might have done it that way. I probably would have, 'cause I was just trying. The thing that I understand about Ivy is it is a toy, but it is inspired by something that I loved when I was younger, right? And modern computing to my mind has gotten very different from what I grew up with, put it that way. And for me, going back to work in this array language model is a bit of a relaxation for me because it goes back to stuff that I worked with when I was younger and remember really well and have fun with it. And it also guarantees that I don't have to deal with users deploying on massive clusters and things like that, which I spent far too many years dealing with at other places. So to me, it's just a hobby and I'm ignorant of most of the things that have been gone on it since whenever, 1969 or whatever it was, when APL 360 came out. And so I'm just sort of learning, but I play with Dyalog to see what I could do in Ivy. I open up Dyalog, try some things. Oh, that looks cool. I should make Ivy do that. And that's pretty much my fun time in the evenings these days, when I have some time to kill and a desire to make something fun happen. Because for me, the joy of Ivy is the implementing of Ivy more than the use of it. The use of it is cool and I love it. and there's no reason to build it if you're not gonna use it. And there are people who've done interesting things with it. But for me, the real joy I get is wrapping my head around the technical problems of building an interpreter for a language with such a unified framework for thinking. But in the case of Ivy, a very complicated model of what a number is, right? There's five kinds of numbers in Ivy internally, right? APL probably has two or three because I think Booleans are special internally. But when you have to add a floating point number and a rational or an integer and a complex number, how to do that turned out to be, for me, the reason for working on Ivy in the first place. I was trying to, we hadn't done much language development work inside Go itself. The original Go compiler was written in C. It's now written in Go, but it's based on the original C one. And I wanted to write a language 'cause that's what I like to do. I wanted to play with these big numbers. But I rapidly found that the standard way to do that that I had been trained to think was terrible. And that was the idea of an object-oriented model for the numbers. So in the object-oriented model, a number, you might have an abstract class in Java terms or an interface in Go terms called value or number or something. And if you want to add two numbers, you implement every number type can do sum or multiply or exponent or whatever it is. But the problem is if you want to add a float and an integer, or a float and a complex, a float and a big integer, all those need their own interface methods. Or each of them has to do a type switch or something. And it becomes n squared. Every operation is n squared in the number of number types. And I got five number types. So every operation in these 25 methods just to do add, it's crazy. So I had a long talk with Robert about this problem. I didn't get very far into it before I realized it wasn't going to work. But I came up with a different model, which I think works out really, really well, although it does have put some limits on what's feasible inside Ivy. But that model is whenever you're going to do a calculation, you take the binary operator. What's word in APL it's not binary. (dyadic). Dyadic operator. You look at the two types of those values, and there's a hierarchy, you know, integer, big integer, rational, float, complex, that's the hierarchy, and char is over on the side. What you do is you promote the lower of the two to the same level because you can always turn one that's up on top of the hierarchy down into a deeper one. You can always turn integer into a float, you can always turn a rational into a float, you can always turn a float into a complex. So you always promote, you take the value, convert it to that, and then you only have to do an add once for each type. And that meant that with a little bit of thinking I can make the whole thing be this table-driven rather pretty structure. I don't know if it's easy to see the structure of the code, but adding a new operator consists of writing basically a declaration with a closure in it, and it all just happens automatically. The structure of it, I'm very happy with. But it makes some issues come up because, for instance, it's very hard to think about what to do when you're boxing a scaler. You can't box a scalar without making it turn into a vector, right? The idea of a vector as a scalar element of a larger object is quite tricky because there's nothing in that hierarchy that lets you wrap it up in the right way. There's no data structure associated with the value. There's only the behavior implemented by the interface. I'm getting very technical here. It's kind of weird. Anyway, the challenge of that, solving that problem was, other than the difficult transcendentals for large floats, for me the most interesting engineering problem in Ivy. Trying to find a way to have an extremely complex definition of number but not have the code become unwieldy. That was really interesting. Now it's just an interpreter. It doesn't compile, doesn't do anything fancy. It's certainly not efficient. But I like the fact that somebody files a bug and says, "I really want, oh, I don't know, split," which happened last week. I can go in, write five lines of code, and Split is now implemented. It's, it's, I love that. I love how easy that is. Some of them take a lot more work, of course, but the ease of developing it has been really, really rewarding to me. And I think all those years I spent writing in C++, if I tried to do it in C++, there would have been more declaration than code before I was done. And I don't like declarations. I like code. Sorry, that was a very long answer to a question I've long forgotten.

00:46:04 [ML]

Well, I'm actually glad you brought this scalar containing an array issue up, because this is something that I noticed in Ivy. Somebody added to the APL wiki that Ivy is now nested, [14] and so I went to investigate what's its behavior with nested arrays, And I found this, that you can't create a scalar array that contains an array, which was surprising to me.

00:46:31 [RP]

But I don't know what a scalar array is. And I think, as I said, I think I know what you're getting at. And I think it's exactly what I'm saying. There is no data structure associated with a number. There is only a protocol for a number. Or for a matrix or for a vector. There's a type called a value, and there's no place to put a box. I would have to invent a new value implementation, call it box or something like that. I have to figure out where it goes in the hierarchy, and I could do it, and maybe I should, I don't know. But it's a problem I never thought about until I decided. What happened with nested Ivy was somebody pointed out that there was an inconsistency because the documentation said, although not in those words, it wasn't nested. It said that every element of every vector or matrix has to be a scalar. But he showed that if you did plus expand 1, 2, 3, you actually got a nested array, a nested vector. And I said, oh, I don't deal with that. That's not going to work. So I went to try to make it so you couldn't do that. And it ended up being so complicated to stop it from happening with all the operators and all the ways things mix. And so after a couple of hours of trying to stamp it out, I said, well, maybe if I don't step up, maybe just let it happen. What do I need to do? And then I took about an hour to get basics of it up and running. The hardest part was figuring out how to print them. Um, and I, I guarantee that it is not a true nested APL. I didn't write that. Um, it has elements of nesting, but it's far from being a complete nested APL implementation. But you can enclose and disclose, or whatever the words are, I forget. You can build vectors of vectors and things like that. It was just easier to go with the flow than to try to prevent it happening. But I'm sure there's lots of things that are just not the way you experts would think of it.

00:48:34 [ML]

So the the way that APL would do this and, I guess one reason why I'm confused is that a scalar would just be a matrix with rank zero, with empty shape. So I guess maybe the hierarchy answers why that doesn't quite work out, because it would sort of be both above and below a vector or something like that?

00:48:54 [RP]

Yeah. If I was starting over, that's probably what I would have done, knowing what I know now, which is a lot more. But when I started, I didn't think it was going to be going on for 10 years of hacking around inside there. And some of these early decisions are clearly wrong; some of them are clearly right. But I think the fact that the shape and the number type are sort of handled differently is probably wrong. But it would be a very big deal to change it at this point. And I don't think anybody expects to be able to get this stuff to work at the level that I would. I mean, you're used to APL. You've got this thing that's a toy that some kid did one evening when he was bored with a management meeting. You're not going to get all the answers you want. But I hope you appreciate the effort. Put it that way.

00:49:47 [ML]

I mean, the thing that I would suggest looking at is just cutting out the vector type entirely. Make that a rank one matrix, and see if with that you can get scalar, vector, matrix as just matrices of different ranks, or arrays as we'd call them, of course.

00:50:05 [RP]

It's interesting. The "vector" word comes up a lot in the APL documentation. So you're supposed to think ... [sentence left incomplete]

00:50:11 [ML]

Yeah, it's just synonymous with the rank one array.

00:50:13 [RP]

Yeah, I know. But you take some of the algorithms work very differently when it's rank one versus rank two too, which is also interesting, but that's worth thinking about. By the way, I'd like to point out to the APL community that if you're an outsider like me and you want to understand it, it's very hard to find accurate specifications of what the operators do. [15] You get an example and a paragraph on a good day. The Dyalog book is very long, but honestly, getting questions answered by reading that is not easy and often impossible. The APL wiki does not tell you enough. For every operator I've implemented beyond the early first set that were very simple (all the sort of matrix manipulators like take and drop and so on), finding out what to do in unusual cases, I can only do by trying APLs and seeing what they do because it's not explained. You know, the words in the documentation that I can find are far from sufficient. And I think if I can make a request to the community, lift your documentation game and make it easier for amateurs like me to come in. It might help. I spent a long time trying to figure out "take", a very long time figuring out "take". It's really not clear what happens in take.

00:51:32 [ML]

Oh, but I spent a very long time writing the APL wiki! [everyone laughs]

00:51:39 [RP]

I appreciate all the work. I know how hard it is to write good documentation. I'm just observing that if you know nothing, it's very hard to know how to get a complete implementation that people will recognize as a correct implementation of what they expect [Marshall agrees]. So it's tricky. I spent a lot of time puzzling around in Dyalog trying to see what was going on.

00:51:58 [ML]

Yeah, I've spent much more time on the BQN specification, which is a full specification. [16]

00:52:03 [RP]

Oh, that's interesting.

00:52:04 [ML]

It's got that.

00:52:06 [RP]

Yeah, I've never seen an APL specification.

00:52:09 [ML]

There are some old standards. They're not free.

00:52:11 [AB]

The IBM documentation for APL2 tends to be really good at specifying exactly what's going on.

00:52:18

Oh, that's good.

00:52:19 [AB]

And I believe the ISO standard for APL is based off IBM's documentation, or at least IBM's behavior. And I'd like to thank you for UTF-8. It's awesome.

00:52:35 [RP]

You're welcome.

00:52:38 [AB]

At Dyalog, we actually have to build two versions of every interpreter: one that uses Unicode and handles UTF-8, of course; and one that uses our own character set. And everybody at the company hates that version. Unicode is good and UTF-8 is a good way to store things. That's how we store our source code in modern stuff.

00:52:59 [AB]

But going back to what you were saying about the enjoyment of implementing and understanding these patterns in order to be able to implement them, and then connecting that with adding a vector to a matrix and the lack of leading axis things, I think you would actually enjoy going into that leading axis theory, because the thing Marshall left out was this crucial "rank" operator. [17] And if you have the system [where] a vector added up to a matrix would pair one element from the vector with one row from the matrix (or even if you don't have it, say ... Dyalog APL doesn't do that), but in general things behave in a leading-axis fashion, then you can restrict the view of the functions to make them do trailing-axis things. So the rank operator allows you to say: "I want the left argument to never have any higher rank than this and the right argument to never have any higher rank than that". And then it will make sure that the function never sees higher rank arguments. And so if I have this behavior, like in J, where every element of a vector gets added to a row of a matrix, then I can say: "but I want this operation done rank one". So the rank one subarrays of the matrix are the rows. And now I get that other behavior. But if you have a language that distributes a vector to every row of a matrix, there's simply nothing you can do to coerce it to apply to a larger picture.

00:54:38 [RP]

The single biggest thing I wanted to do in Ivy and have bounced off a couple of times, although I think I finally have the wherewithal to do it, is to implement (I don't know what the word is in APL), but I call them closures, little nonce functions. And to do that, I have to make an operator (I'm using words that mean different things in APL, I'm sorry) ... function or operator be a value in this model I have. And I think I know how to do that now. Once I've got that, then I can start to do things like putting the index annotations and decorators on them, which are part of what you're getting at. I think the ability to say: "this is the axis, I want you to do it along; do it this way instead of that way". The only thing I've done recently is put in as a hack (which I will get rid of when I can get this other stuff working), the ability in scan and reduce, to take the other axis by putting a percent sign after it (which is gross) but it worked. But that's just a placeholder until I have a general way to write that annotation down, which I would love to have. I would love to be able to do that. But it's just, I bounced off it a couple of times, probably because I was trying to do it in hotel rooms instead of at my desk where I had a sensible amount of computing and thinking available. But that's the biggest lack I feel in Ivy now today is the inability to treat operators, functions (whatever you want to call them) as first class citizens.

00:56:19 [AB]

Well, APL doesn't have first class functions (or most APLs at least don't) but it's still able to do this.

00:56:26 [RP]

Well, those crazy bracket things in APL ... [sentence left incomplete]

00:56:28 [AB]

Yeah, you don't even need those.  With a rank operator, that's a completely uniform operator in the APL sense, a higher order function. It takes a function, and it takes some parameters, and it does something in a uniform way. It doesn't care about what the actual function is. And you can write that in terms of encloses and mixes. But it requires that the functions are amenable to this kind of usage. So you have slash for 'last axis reduce' and slash percent for 'first axis reduce', clearly showing that the first axis is the secondary thing. You want the first axis one to be the primary thing. Then you can restrict its view, because the first axis reduction over the row of a matrix is just the last axis reduction on that matrix. So I definitely recommend you look into that.

00:57:26 [RP]

Sounds interesting. You do have to remember that my APL world view was formed in the late '60s and early '70s. So I'm way behind the curve here.

00:57:39 [CH]

All right, I know it's getting super late for you, But hopefully I can make one comment/ask a final question. And the first comment goes back to [when] you were remarking on the character sets and the symbols being like a huge cliff that people have to climb in order to surmount at least (maybe not Q, because that comes with Q words and some of the certain array languages), but a lot of them, like APL and BQN. And you were describing this right-tack. [18] And at one point, right after that (I was gonna mention this), but I'm coming all the way back to it because it's maybe not a huge coincidence, because I spend a lot of my free time thinking about this stuff. Recently I've been trying to implement something where I need the semantics of the left and right tack, which inside a function that takes two arguments, (what APL calls a defun), it will (it's a binary function), and the tack that points to the left will give you the argument on the left and the tack that points to the right will give you the argument [on the right]. So technically, they're two binary functions that you give two arguments, and they just basically choose one of the two. These correspond to things in Haskell and functional programming languages and combinatory logic called K and KI. And I didn't want to use the tacks, because I'm not making a Unicode thing; I'm using words. And so at first, I just used K and KI, because those are the names of the combinators from combinatory logic. But then I thought to myself: "that's actually pretty bad". People are going to mix those up and forget which is which all the time. And  J uses the brackets because those kind of look like tacks pointing in a certain direction. And then I'm trying to think to myself, what is actually the best name for functions that discard their arguments that isn't spelling out left or right? It's just like a single character. And I could go on and on about this. But my ultimate thought was that actually, even though it does take a little bit to learn what the tacks mean, is that like, of all the options that I was thinking of, the tacks were actually (the ones in APL) were actually the most semantically meaningful, even though it's completely different to what you see in Python and Go and C. But from a meaningfulness point of view, when I'm trying to think, should I call them L and R for left and right, or K and KI for the names from combinatory logic, it's like APL actually nailed it. It just looks super different.

01:00:09 [CH]

Which is what brings me to my question, is that you used it when you were in school, and have said that you're coming back to your love for computer science and programming by returning to your Ivy project and APL. And I'm curious, what is it that separates the folks that see APL for the first time and get interested and folks that see it and they just kind of bounce off of it. Because you know, I think a lot of us have [seen] YouTube channels where they put content online that has APL and stuff and there's two different camps. There's people like: "Wow, this is so cool; I want to go check it out". And a lot of folks that say: "Thank goodness I saw this now so that I know never to look at anything like this again". What is it that you think separates those folks and do you have advice because you clearly think it's of value for people to go and explore these different paradigms?

01:01:02 [RP]

No, this is a really good question. I don't know that I have a good answer. You need to understand that at the time I first used APL, it was the coolest thing we could use because there was nothing else like it. You couldn't sit at a terminal and program the way everyone does today. It was all punch cards or worse. So APL was seductive because if you spent the time to learn it, you got to sit at a terminal and talk directly to the computer, which was an amazing thing in, let's say early '70s. It wasn't the way you typically spent your day's programming. So my own experience says that I was drawn in not because of APL or its model, but because of the interactivity it gave me. And the other stuff was like gravy that came later that when I used other languages, I realized what I'd left behind when I moved away from APL and its equivalents. For someone today coming up to them, I think it's very simple. I don't know that it's a particularly nice thing to say, but I think some people are just not as curious as some others. Some people look at those peculiar symbols and say: "Wow, that's really weird; what's going on? how is that possible?". The famous Dyalog person showing off how to do Game of Life ... [19] half the people look at that and think: "this is insane; how could you think like that?". And the other half say: "what's going on? this is pretty cool". And it goes back to my thing about orthodoxy. If you think things need to be done a certain way because it's the only way you've ever done it, seeing something like that can just make you think: "that guy's out of his mind; that's not how we do work". But if you're open to more ideas or have programmed in other languages (let's put that in there), then you might get attracted to the possibility that there's something really interesting going on behind those peculiar symbols. And I'm not criticizing those symbols. My point was that I think it makes it harder for you to get someone to come there. Because if they're one of the people who's not so curious about it, they're going to just stop when they see that. There's a psychological thing. You probably know this because I presume you have a job somewhere where you go to meetings and you have to go and talk to some organization in your company, who's doing something beause your manager has told you to go there and he's saying: "can you go find out what they're doing and should we be working with them?" But the real subtext is: "go there and find out what where we don't have to work with them; find something wrong with what they're doing that we can say, 'I am sorry, we can't work with you' and we get back to doing what we want to do anyway." There's a psychological thing about not wanting to be bothered by something new. And I think that really the APL character set really blocks people who think like that. That you're looking for a reason not to care about it. And they can say: "oh, I don't want to learn those stupid symbols; that's dumb".

01:04:06 [RP]

And then there's people who have a different mindset for whom it's a curiosity: "There must be something going on. This guy has managed to achieve something by putting some really funny scribbles down. What on earth could be going on there. Maybe that's interesting". I think it's just the kind of person you are going in. My own experience, I said, is very different from that.

01:04:25 [ML]

I do want to say, though, I mean, surely your personality plays into it. But, you know, some days I'm curious and some days I just don't have the time for it so ... [Rob laughs and says "That's fair"]. There's another factor (and I don't think this explains the people who clearly have enough time to post comments on YouTube dismissing APL [everyone laughs]). But for the people that just move on, nobody can investigate everything. So there is a factor of people are thinking: "how much time would I have to spend on this to learn it?". And maybe it's honestly not worth it. Maybe they've overestimated the time, and it would be worth it. But there are a lot of different possibilities there.

01:05:08 [RP]

Absolutely. And I think Ivy, for all of its weak APL-ness, has shown at least some people I know that there's really something worth going on there, you know, something interesting happening. And the more visibility that we can get for these array languages, the more people are going to see it and more people will get caught. But what happens? I don't know if you read Hacker News [https://news.ycombinator.com], but whenever something APL related comes up on Hacker News, it's always in the form of arcana you'll laugh at rather than fascinating work being being done by very smart people. I find that offensive, but I'm not going to push back on that. I don't talk on Hacker News. But I've seen a lot of interesting things being posted about it, and the comments are always almost universally, like: "what the hell is that for?". And not understanding that that language was once the best interactive language out there, and in many ways still is. And there's some phenomenal stuff being done with it. But it's hived off somehow from most of the rest of the computing world in a way that, for instance, Lisp (which is, I think, an almost contemporaneous language; Lisp was a little earlier, but similar) ... Lisp is sort of part of the universe of programming that people understand. They'll laugh at it, but they understand it, and they know what to do with it. And APL is something altogether different. I think that's a shame. Maybe we can change that somehow. I'm not saying the symbols are the reason that's not catching on; don't misinterpret me. I'm just saying it makes it a little harder to get people to come with you to the well.

01:06:43 [AB]

Clearly K and Q and J exist and haven't seen enormous uptake from using ASCII.

01:06:51 [RP]

No, but they also focus on concision. Well, K and (I don't know if I know it well enough. I probably should stop talking about it) ... [sentence left incomplete]. I just feel there's this resistance to arcana sometimes.

01:07:05 [ST]

Just on that thing you said earlier about showing people what Ivy would do and the demo command (I noted that your command began with a right paren like the system commands in APL). You mentioned many times showing people that command. Did you then walk away or did you sit with them?

01:07:30 [RP]

Sat with them. I sat with them. Sometimes I drove it; sometimes I had them drive it. Both worked in the sense of getting the wonder. I think what makes the difference is going through it, right? With me there, they're not going to walk away after the first line. They're going to play it through. And I tried to construct it so it was easy to follow, but builds up to a few really lovely examples along the way. And I think keeping them involved until you get to the real payoff, which comes fairly far down, actually helps a lot. Whereas if you see when you look at the Game of Life video (which is amazing; I love it), I can't really take anything away from that, except maybe this is a fascinating thing I should learn about, right? Whereas [as] something that was more interactive and exploratory, the demo allows you to try things out. And sometimes in a few places it encourages you. It says: "type this out and see what happens when you type this thing", because I want you to try it yourself and see it. But I think the presence of a longer narrative that is covering 1% of what can be done is nonetheless sufficient in my experience to at least get people curious about it. And in one case, I know (the Russ Cox thing), he went and he did Advent of Code with it afterwards. So that was cool. And those are really good explanations of how these things can be used. I don't know if you've watched them, but they're pretty good.

01:09:06 [CH]

Yeah, I didn't watch all 25 of them. I saw that a few of them were ... [sentence left incomplete]. I think one of them was an awk. Like you said, I think it's 80% to 90% of them are in Ivy. But yeah, they're nice [and] digestible, like you're not watching an hour video solving these problems. So if you just want to taste, I would go to the top of the list. We'll throw it in the show notes. And it's definitely a good way to dip your toe into the world of ... [sentence left incomplete]. I know you don't like calling Ivy an array language, but we'll call it ... [sentence left incomplete]

01:09:33 [RP]

I call it a big num calculator.

01:09:36 [CH]

A big num calculator. OK, well, we'll find a way to get the word "array" in there somewhere [laughs].

01:09:42 [RP]

I mean, it truly is. There's only one control structure. There isn't even a go-to or a loop. It's not really a programming language in any meaningful sense. But you can do stuff with it because the primitives are so powerful.

01:09:56 [CH]

All right. With that, unless there's any last questions or comments from the panelists (I'm not seeing any hands go up), Bob?

01:10:05 [BT]

Well, I'll do my usual spiel, but before I do that, this has been one of those episodes where normally I have to figure out how we're going to do the cold open and figure out what little thing I'm going to lift and put at the head of this. But in this case [chuckles] I have so many choices.

01:10:20 [ST]

You're gonna have a challenge [everyone laughs].

01:10:24 [ML]

Just do three in a row.

01:10:31 [BT]

It's just amazing. And thank you so much, Rob, for coming on. And I'll just give my quick spiel. If you do want we have show notes for this. If you go to our web page at https://arraycast.com. And if you need to get in touch with us: contact@arraycast.com.[20] You can get in touch with us, leave a message. And that's about all I've got to say for my little ... [to] get my business done.

01:10:51 [RP]

Well, thanks very much for inviting me. It was really fun to talk about this stuff. In the circles where I talk about, I'm the expert. And I know I'm nowhere near the expert that I should be when I'm talking about this. But it's really great to hear the ideas from you guys. And thanks so much for inviting me. It was a real honor.

01:11:07 [CH]

No, thank you so much for taking the time. This has been absolutely awesome. And also, I'm not sure if it's been mentioned, but you're in Australia and the rest of us are all over the globe. So it is past midnight for you at this point. And I think we're all so pleased that you're able to spend this much time answering our questions. We've talked about doing a virtual, maybe in-person array language thing in the future. But if it is virtual and you're willing, and we do make it happen, maybe you could come and give a talk on Ivy at some point, if it's hosted on YouTube at some point.

01:11:40 [RP]

Yeah, I'd love to do that.

01:11:48 [CH]

And yeah, if you are continuing to work on this, hopefully we can get you back at some point in the future to talk about what's new with Ivy. And we didn't even talk too much about Go today, other than the fact that it is one of the few languages with iota. C++ also has iota. We got to keep the torch going. Some people on the internet hate it.

01:11:58 [RP]

C++ has iota now?

01:11:59 [CH]

It had iota in C++ 11. It is not a constant generator, but it's an algorithm that basically generates a sequence starting from an integer N. And there was, at one point, a war on the Twitter-sphere, because someone said, people just use these names to feel smart. And then a very senior person said: "No, there's actually history in this word. And it has meaning. And we are professionals and should know the history of our profession, et cetera, et cetera" [laughs].

01:12:29 [ML]

Which, of course, made him look very smart [everyone laughs].

01:12:31 [CH]

But yeah, this was absolutely awesome. And I can't agree more with what Bob said, that we should just create a four-minute video of all the highlights from this and say: "you heard it here first, folks".  The co-creator of Go says: "go learn Array Languages" [laughs]. And maybe this is the turning point for our paradigm. This podcast is going to ... [sentence left incomplete] we're going to be soon [a] top 20 language, just like Go. One can hope.

01:12:56 [RP]

That'd be cool. I would definitely be thrilled to see that happen.

01:13:01 [CH]

All right. I think with that, we will say: "Happy Array Programming!"

[everyone]

Happy Array Programming!

[MUSIC PLAYING]

</details>
