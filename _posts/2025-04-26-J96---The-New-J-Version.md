---
title: "Episode 104: J9.6 - The New J Version"
date: 2025-04-26 00:00:00 +0000
episode: 104
keywords:
- array-programming
- array-languages
- jlang
- jlanguage
- henry-rich
- j9.6
mp3-url: "/assets/audio/episode104.mp3"
episode-type: full
explicit: "no"
block: "no"
layout: podcast
excerpt_separator: <!--more-->
redirect_from: "/episodes/episode104-j96"
---
J9.6 - The New J Version of JFor the 7th time our guest is Henry Rich, the maintainer of the J language. Henry tells us all about the new J Version 9.6
<!--more-->

**Host:** Conor Hoekstra

**Guest:** Henry Rich

**Panel:** Marshall Lochbaum and Bob Therriault

---

[Original episode on ArrayCast](https://www.arraycast.com/episodes/episode104-j96)

## Show Notes

Array Cast -  April 25, 2025

Thanks to Bob Therriault for gathering these links:

**[01] 00:01:35**

- [code.golf](https://code.golf/about)
- [ngn/k programming language](https://k.miraheze.org/wiki/Ngn/k)
- [J programming language](https://www.jsoftware.com/#/)
- [APL programming language](https://aplwiki.com/)
- [BQN programming language](https://mlochbaum.github.io/BQN/)
- [Uiua programming language](https://www.uiua.org/)
- [APL thumbs up link](https://github.com/code-golf/code-golf/issues/135)
- [BQN thumbs up link](https://github.com/code-golf/code-golf/issues/474)
- [Uiua thumbs up link](https://github.com/code-golf/code-golf/issues/1115)
- [Henry Rich Episode #06 on the ArrayCast](https://www.arraycast.com/episodes/episode-06-henry-richs-deep-dive-into-j)
- [Henry Rich Episode #18 on the ArrayCast](https://www.arraycast.com/episodes/episode18-henry-rich-presents-j903)
- [Henry Rich Episode #48 on the ArrayCast](https://www.arraycast.com/episodes/episode48-henry-rich)
- [Henry Rich Episode #50 on the ArrayCast](https://www.arraycast.com/episodes/episode50-fold)
- [Henry Rich Episode # on the ArrayCast](https://www.arraycast.com/episodes/episode73-j95)
- [Henry Rich Episode #84 on the ArrayCast](https://www.arraycast.com/episodes/episode84-tacit6)
- [Release Notes for J9.6](https://code.jsoftware.com/wiki/System/ReleaseNotes/J9.6)
- [Singeli programming language](https://github.com/mlochbaum/Singeli/tree/master#readme)
- [C++ programming language](https://en.wikipedia.org/wiki/C%2B%2B)
- [Rust programming language](https://en.wikipedia.org/wiki/Rust_(programming_language))
- [Post Mortem Debugging](https://code.jsoftware.com/wiki/Vocabulary/Debug)

**[02] 00:14:45**

- [Visual Studio](https://en.wikipedia.org/wiki/Visual_Studio)
- [GDB GNU optimized debugger](https://en.wikipedia.org/wiki/GNU_Debugger)
- [Locales in J](https://code.jsoftware.com/wiki/Vocabulary/Locales)
- [CoLib Foreign conjunctions](https://code.jsoftware.com/wiki/Standard_Library/colib)
- [Threading in J](https://code.jsoftware.com/wiki/Vocabulary/tcapdot#dyadic)
- [Power Conjunction (^:)](https://code.jsoftware.com/wiki/Vocabulary/hatco)
- [Fold Conjunction (F. F: F.: F:: F.. F:.)](https://code.jsoftware.com/wiki/Vocabulary/fcap)

**[03] 00:23:55**

- [Catalan Numbers](https://en.wikipedia.org/wiki/Catalan_number)
- [Ruby programming language](https://en.wikipedia.org/wiki/Ruby_(programming_language))
- [q programming language](https://en.wikipedia.org/wiki/)
- [J pronouns x, y, m, n, u, v](https://code.jsoftware.com/wiki/Help/Release/J_6.01/:_Explicit_Names_Changed)
- [Fold Diagrams](https://code.jsoftware.com/wiki/Vocabulary/fcap)

**[04] 00:34:30**

- [J's Benchmarking page](https://code.jsoftware.com/wiki/Vocabulary/JCPUBenchmarks)
- [Adám's Reshape Contribution](https://code.jsoftware.com/wiki/Vocabulary/dollar#reshapeblank)
- [J forums](https://groups.google.com/a/jsoftware.com/g/forum)
- [ArrayPortal](https://www.arrayportal.com/)
- [Jsoftware.com](http://jsoftware.com/)
- [jsoftware.com/#](https://www.jsoftware.com/#/)
- [Dictionary Data Structure](https://en.wikipedia.org/wiki/Associative_array)

**[05] 00:44:19**

- [J9.7 Beta version](https://code.jsoftware.com/wiki/System/Installation/J9.7)
- [Line continuation discussion](https://code.jsoftware.com/wiki/Vocabulary/ReleaseNotes9.6RFC)
- [Dissect debugger](https://code.jsoftware.com/wiki/Vocabulary/Dissect)
- [Direct Definition in J](https://code.jsoftware.com/wiki/Vocabulary/DirectDefinition)
- [Kap programming language](https://kapdemo.dhsdevelopments.com/)
- [Index of (i.)](https://code.jsoftware.com/wiki/Vocabulary/idot#dyadic)

**[06] 00:51:52**

- [Java programming language](https://en.wikipedia.org/wiki/Java_(programming_language))
- [Stepinoff Series of Lectures](https://www.youtube.com/watch?v=1QvkTKNgHJk)
- [Tolerant Comparison](https://code.jsoftware.com/wiki/Essays/Tolerant_Comparison)
- [Phineas Porter Episode #98 of ArrayCast](https://www.arraycast.com/episodes/episode98-phineas-porter)
- [Aaron Hsu Tacit Talk #27](https://www.youtube.com/watch?v=BIc9iz-n7dM)

**[07] 01:01:31**

- [NARS2000 Implementation Episode #82 of ArrayCast](https://www.arraycast.com/episodes/episode82-nars2000-implementation)
- [Contact AT ArrayCast DOT ComIndexing Episode #99 of the ArrayCast](https://www.arraycast.com/episodes/episode99-selection)
- [Symbols in J (s:)](https://code.jsoftware.com/wiki/Vocabulary/sco)

<details markdown="1">
<summary><strong>Transcript</strong> (click to expand)</summary>

Transcript

Transcript prepared by

Adám Brudzewsky, Bob Therriault, and Sanjay Cherian

Show Notes

00:00:00 [Bob Therriault]

I am particularly interested to find out whether anybody selects my area that I would always like to find out more about, which is symbols in J, because I just don't see them used very much.

00:00:12 [Henry Rich]

They're not. It might be time to put them to the sword.

00:00:16 [BT]

Oh no, not before they have a chance.

00:00:19 [Marshall Lochbaum]

Shouldn't have brought it up, Bob.

00:00:21 [Music]

00:00:33 [Conor Hoekstra]

Welcome to episode 104 of Arraycast. I'm your host, Conor, and today with us we have a special guest, a multi-episode guest that we're going to introduce in a moment, and an exciting topic to talk about. But before we do that, we're going to do brief introductions. We'll start with Bob and then go to Marshall.

00:00:50 [BT]

I'm Bob Therriault. I am a J enthusiast, and today you will know why I'm especially enthusiastic.

00:00:57 [ML]

I'm Marshall Lochbaum. I was introduced to J by some nobody named Henry Rich a little over 15 years ago, and now I do BQN in Singeli.

00:01:07 [CH]

And as mentioned before, my name is Conor, massive Array Language fan of all the Array Languages, including J, even though I probably spend less time on J than I do some of the other Array Languages, but excited to hear about the news and the exciting announcements associated with the release that we're going to talk about today. But before we do that, there's one short announcement, and it's from me. [01]  And I actually need to pull the website up because seeing as we're going to be talking about J today, I might as well and go find out what version of J this website uses. And look at that, folks. J is on version 9.6 on Code.golf. We've mentioned this website before. It's a code golfing kind of competitive website. And for the Array Languages, it features ngn/k and J. So you can program in k and J officially on this site. However, I'm not sure if this is a new thing. Maybe Marshall knows. I'm not sure if you spend any time on this website. But there are a set of experimental languages. I only discovered this in the last month or a couple weeks or so. And on the experimental list are the following languages, folks. There's a ton. There's 60 official languages-ish. And then it looks like there's like 30 or 40 experimental languages. And of interest to our listeners will be three of them, folks, maybe more, but definitely three. And that is APL, Dyalog APL to be specific, BQN, and Uiua. So you can already go and solve these code golfing problems in the experimental language. However, because they're experimental, they don't count towards the points that you accrue on the site that affects your ranking. Luckily, though, I will put a link or Bob will put it. I'll just send it to Bob and Bob will put it there. A link in the show notes where each of these languages has a GitHub issue attached to the GitHub repo behind this website. And you can go and upvote your favorite languages that you want to get promoted from experimental to official. So I would recommend even if you've got a favorite, you go heart all three of those. And then maybe in the near future, we can have those as official languages. I'm not sure. Marshall, have you spent any time with this? Did you know of BQN's existence?

00:03:18 [ML]

Yeah, I saw BQN, I think, was added sometime last year. I didn't know what the procedure was to move up from experimental. But yeah, I knew it had support for fewer array languages.

00:03:33 [CH]

All right. So link will be in the show notes to the website and to all three of the GitHub issues. We've got several hundred listeners. Even if you don't interact with as much folks, you can go just click on the links, hit the heart. I actually I don't know from memory. I know from BQN because that's the one I would like most to see go to official. 12 thumbs up and two thumbs down. Actually, for fun, let's go. We'll go click on Uiua and we'll go click on APL. Except, of course, these ones are bringing us to the site. So actually what I have to do is go to a problem. Bear with me, folks. We're going to BQN. We go to APL and then we go to that GitHub issue. Then we scroll down to Uiua down at the very bottom due to alphabetical sorting or lexicographical, if you will. And APL has 40 upvotes and five downvotes plus five hearts. Not sure what that means. So that's got a better ratio. That's eight to one in favor versus a six to one for BQN. And overall, it's got absolutely more. And then Uiua, whoo, Uiua's got 19 thumbs up, one thumbs down. So that's a 19 to one ratio. So APL in the lead in terms of the arithmetic difference between the upvotes and downvotes. I'm not sure how they measure it, folks. But let's get those to 100 upvotes for all the array languages. That's a very long announcement. And with that, we will introduce our seven time appearing guest, the most frequent guest. I think that's now two behind our next most frequent guest, which is Nick Psaris. Henry Rich, the main developer of the J language. I will or we will link all six of his prior appearances. I think also you are our first guest, if memory serves correctly. Way back.

00:05:18 [HR]

Two years ago now, I guess.

00:05:18 [ML]

Yeah, yeah. Because I was right after.

00:05:20 [CH]

And so we're bringing you back as we usually do. Well, I think at this rate, we bring you back more than annually, but at minimum, we bring you back anually to talk about the latest and greatest J release, which this time is J 9.6. And so, yeah, we're here to talk all about that. I, to be honest, I looked a little bit at the changelog notes, but I haven't, you know, dived into it in detail. So I'm excited to hear what's new in J with J 9.6.

00:05:47 [HR]

Well, this release is more of a performance release than new features. But I will talk about the new features first. The really big one is support for two new data types. One, a double-sized floating point. So it's 104 bits of mantissa. And also support for short integers. So we have, in the past, we've only had native floating point and native integer, which for most people is 64 bits. We've had the long floating point for people who need that precision. We have some users who can't do without it. And then the shorter data types, if you need to save space.

00:06:27 [CH]

So that, the double float, the double float is 128-bit floating point, basically?

00:06:33 [ML]

It's constructed of two 64-bit floats. So...

00:06:39 [HR]

Yeah, there's an IEEE standard for 128-bit floating point. This is not that. Because it's not, that is not supported by any hardware that I know of. But you can take two double precision floats and make one of them the high half and the other the low half. So that the exponent on the low half will always be, you know, about 17 decimal places below the high half. And what you get then is 104 bits of mantissa and 13 bits of characteristic. Which if you add that up, shows that you've lost some bits. But still, it's so much better than trying to emulate. You can emulate, use that floating point at a performance cost of something like 10 to 1. It takes around 10 times as long to multiply two big numbers as it does one floating point number. That's not a bad trade-off.

00:07:38 [ML]

But the multiply is a lot slower than the addition, right? So if you're addition heavy, then you don't have that much cost.

00:07:46 [HR]

Yeah. If you have a long string of calculations internally, you can do them one after another. But for ordinary primitives, you have to have a canonical form. For the resulting value.

00:07:59 [ML]

Yeah, yeah, reduce it.

00:08:01 [HR]

Yeah. So you have to do something. There has to be a canonical form so you can compare for exact equality easily between two values. That takes a little time. But you're not doing this because of the time. You're doing this because you need 30 decimal places of accuracy. Applications that do need that really can't substitute anything else.

00:08:21 [ML]

Yeah. So this is actually, in Singeli, this is the only type of number we use at compile time. And we do that because it's a superset of both 64-bit integers and 64-bit floats. But it also means you get just basic high precision in all your compile time computations. And then at run time, everything has a specified type.

00:08:42 [CH]

Yeah. So the naming of this, because I guess initially I started my career in C++ land where they call the 32-bit floating point float and the 64-bit floating point double. And I went to the changelog or release notes and it says that this is called floating 16 for double double. So this does kind of map to the 128-bit space, but it doesn't because you're using the two 64-bit floats.

00:09:11 [ML]

Yeah. So you lose some of the bits from the exponent of the smaller number.

00:09:15 [CH]

But so floating 16, and also because a lot of the more modern, like Rust I know, they don't do this confusing float double. And I think even depending on the compiler implementation, they used to call them like long longs and things like that or whatever. Or you would prefix, they have prefixes that you can put in front of types to extend the precision.

00:09:35 [ML]

Yeah. Well, and it was CPU dependent. Yeah.

00:09:38 [CH]

It was just very confusing. But so now they have like I32, I64. But so when I see floating 16, I actually think of like a half precision float, aka like an F16. But this is not that. This is closer to the, like I said, it's a representation for something that doesn't get all the way to 128 bits because of how it's implemented. But just very clear.

00:10:05 [HR]

We could call it float 128, but we didn't. If we have float 2 in the architecture, but not implemented, that would be a very short floating point. Yeah. You can't call it quad precision floating point because IEEE got there first. There is a standard for that. So you have to call it something else. Double double is good enough.

00:10:27 [CH]

Yeah. I mean, and double double does make more sense to my C++ brain because that immediately maps it to double of double in C++, which is the 64 bit float. Anyway, naming is very hard.

00:10:40 [HR]

And we had a question with the short integers. There's a question of what should happen with mixed mode computation. If you have an 8 byte integer and you add it to a 4 byte integer, what should the result be? We decided to leave it as 4 bytes, except if there's an overflow, catch the overflow, but figure that the user specified 4 bytes for a reason and we'll preserve that through computation. That's probably not what other languages do, because if you don't start from 8 byte integers, you would end up making a different decision.

00:11:17 [ML]

Yeah. So it's kind of tricky because if the user just writes like 2 plus x, then that 2 is going to be 64 bit, right?

00:11:23 [HR]

Right. Yeah. So that would lose the value of having x being 4 bytes. So we made that decision. The second big thing we put out in the release actually is a consequence of all the performance improvements that have been made over the years. In the original interpreter, as of maybe seven or eight years ago, when you started a sentence, the interpreter would take the sentence and make a copy of it and produce a debugged stack frame and go off and interpret the sentence and if there was an error, it would come back. And as time went on, the execution and the parsing became so fast that just preparing the debugged stack frame takes longer than executing the sentence. So I got rid of it. And if you're not debugging, there's almost no overhead related to all those things that make an interpreter great. If you want to get debugging, you have to turn on debug and then you'll get all that extra stuff. And that's something of a pity because sometimes you don't know when you're going to have a bug and then something you thought was going to run crashes and you wish you could look around. What we added in this release is called post-mortem debugging, which allows you to go back after the crash, the system goes back and retroactively figures out what the stack frames would have been for the failing programs, everything on the execution stack, and gives you a chance to poke around and look at data there. So it combines the high speed of execution with the interpretive facility to name debugging.

00:13:23 [ML]

So can it always do that?

00:13:25 [HR]

Well, it can't get everything, but it can...

00:13:28 [ML]

It can always get some information.

00:13:30 [HR]

Well, it gets all the local variables in all the executing stack frames.

00:13:35 [ML]

So as long as the information is still around, it knows what to do with it.

00:13:39 [HR]

Well, yeah, but the information is going to be around. When it crashes, it crashes at the... Well, not crash. When the program, when it detects an error, it's at the bottom of a long stack. And what it does is, as it returns through those stack frames, it remembers all the namespaces. When it comes back to the console prompt, it says, "You had an error. Would you like to press enter if you would like to debug it?" Which was pretty tricky, because there's no command. The only command that we could use to enter debug is the command that is nothing. Ah, yeah. That was a problem, but hitting enter is an inspired solution. So if you hit enter, it instantiates all those stack frames, and then you can go debug it. Otherwise, it discards them and executes whatever sentence you did enter.

00:14:29 [CH]

I'm trying to think if there's anything else similar to this, because I don't think so. I mean, in all the IDEs I've ever used, which admittedly is only like three or four, but the biggest one was Visual Studio, [02] you have to be in debug mode in order to do anything. And I know that there's tools called like Undo, where you can debug and reverse and stuff, but that has to be turned on. You can't just, like, especially for compiled language, you know, you need to collect that info.

00:14:57 [ML]

I mean, I think it's more or less like GDB works, not talking about the implementation, but the interface. Like, if you run GDB on an optimized program, a lot of the time, like if you stop somewhere, and this is the debugger for C, GNU debugger. If you stop there, and you ask what some variable is, it'll say, "Oh, it's optimized out. It's not around anymore." Basically, so it has somewhere statically the information to make sense of what's in the registers and on the stack. I mean, I guess to run GDB at all, you have to start the program in debug mode, but it's kind of...

00:15:33 [HR]

If you're in debug mode, the compiler will push everything out of the stack. That's where the debugger can see it. Otherwise, it's hidden in registers and unavailable.

00:15:42 [BT]

Yeah. And is this also what allowed you to do the, I think, their negative locatives, that allows you to look back at the calling programs in the stack?

00:15:51 [HR]

Yes. Since this is a new feature, that now you can look back into stack frames. This applies no matter whether you're in post-mortem debugging or regular debugging. There's a syntax. So, they show me variable Y in the top stack frame or the one after that or after that. There needed to be some syntax to allow access to those local variables, because normally you can't see a local variable if you're not executing in that local context.

00:16:23 [BT]

And so, in J, negative numbers are preceded by an underscore. Right. And the locatives are two underscores after the name of the locale, right?

00:16:27 [HR]

Right.

00:16:34 [BT]

So, is it the three?

00:16:36 [HR]

Three underscores in the number. That's another happy accident. It makes it easy to...

00:16:42 [BT]

To spot them.

00:16:42 [HR]

...see what you're doing. Yeah. That was an important feature. I guess really the last big change is not a feature, but a removal of a feature. But it's interesting as a matter of a program design. It's a striking example of what happens if you don't think far enough ahead. In J, the current namespace is called a locale. The locale can be changed if you call a name in another namespace and say, "I want to switch that namespace." The system does it automatically, and when you return, it restores the original namespace, the original locale. But you can also decide at any moment that you want to change the current locale and execute a command that does that. And there was a foreign conjunction that did that. But it was intended to be used under a cover name, that cover name being cocurrent, meaning all the locale verbs start with C-O. So this is just set the current locale to X. And that posed a problem because normally when you call a name, the locale is reset when the name returns. So if I call cocurrent, cocurrent then executes command to set the locale to X. When cocurrent returns, that locale change would have been lost. So there was a little quirk put into the system that says, "For this particular example, the locale name is not restored." This was not actually spec'd out anywhere. It was just defined by the implementation. The way it was implemented was that there was a stack that J used for execution contexts, and the special command to change the locale would reach up into the stack and store the new value in the caller so that it was just an exception to the rule. And then threading came along, and there's no stack anymore. There's no single stack in the system. And all the stuff that was done by reference to the stack has to be done by other means. And this was, we did threading a couple of releases ago, but it took a tremendous amount of work around to make this locale stuff work, just because it bypassed the normal mechanisms. And finally, we bit the bullet and said, "Enough. We're not going to support that command anymore. We're going to define the name cocurrent as a predefined system name. It has that function, and there's no exception anymore. cocurrent does what it does." And again, all locale changes go through the name system, and it makes the code beautiful. But it really is a lesson. Don't let a function be defined by however you chose to implement it. You need precise specs for everything. But anyway, it made me very happy to get rid of that. As for the rest, they're mostly performance improvements, but they're pretty significant. The power conjunction is an extremely general operation. You have a verb, and then you say how many times you want to execute it. But that description can be also a gerund, so you can say, "Do several other verbs." Up to three verbs to participate in the execution of the verb. And unfortunately, it was implemented very generally also, which means that the case that you almost always have, which is when you want to execute something either zero times or one time, had a great deal of overhead. So that has been recoded so that the fast cases are very fast, and the general cases are very general, which is the way it ought to be. Another improvement, this was instructed to me to show how long it takes to develop a language. Several releases ago, we implemented Fold, a family of looping primitives that gives more features than simple reduction. And we implemented it in J, just so we could play with it, make it modifiable. And it looks like now I'm finally seeing, after all these years, people are putting examples to the forum using Fold. So a lesson to language designers, it takes a long time to get the users to follow on your idea, no matter how good it might be. So we decided this release was finally time to bring Fold internal. It's now coded in C, and it doesn't have any of the J overhead, even if the operations are very short. It's still pretty efficient.

00:22:06 [BT]

And for Fold, do you think that's a result of it being so simple? I mean, it's just the forward or the backward slash for Fold, you know, for the scan or the reduce.

00:22:17 [HR]

Well, yeah, most of the cases where you might use Fold, you could also do a reduce, and it would be pretty much okay. The times you really need a Fold are when there's a lot of internal state that needs to be passed on. And it's not in the case of a reduction either. It's in the case of a scan where you've got one output per cell, and there's a lot of internal state that you don't want to have to make part of that output.

00:22:48 [BT]

And Fold allows you to decide what part of the state you want to carry forward to the next operation, so you don't have to carry the whole thing.

00:22:55 [HR]

Yes, more precisely, you decide what part of the state you want to make part of the result. You carry the whole big state through the computation and peel off a little bit of it to be your result so that you don't end up with having to replicate the entire state for every cell. It also gives you the ability to go forwards or backwards and provide initial values for the operation. It's got some features, none of which are totally essential, which is probably why it took so long for it to have the uptake that it's had.

00:23:27 [CH]

Here's a related question, which you were explaining, yeah, Fold and that you can use, you know, reduces and scans in certain situations to do the same thing, but there are differences, obviously. Fold covers a much larger superset of operations. I was doing--I think it was the first, like, Catalan numbers [03] the other day, and I think I solved it in k because I was doing the cold golf thing, and I solved it in BQN. I might have even solved it in Ruby or something. And then I went to J, and I think I was never able to solve it in J. And I think I actually at one point I was trying to use prefix, a.k.a. scan, but J has that difference that they don't bundle the reduction with what they call prefix, a.k.a. scan, so you have to do, like, the, you know, slashes back to back in order to get that behavior. But I couldn't get the right result. At one point I got something close and it was wrong. And one of the problems sometimes when you're skipping between array languages is you cannot keep track of, like, what belongs in what language. Like, BQN, I'm always able to keep stuff straight, but when it comes to Q and J, sometimes I get confused. So is there a rule of thumb when it comes to where you have double struck X and W in BQN, alpha and omega in APL, that you've got X and Y in J, and then you've got X, Y, and I believe Z in k and in Q, but J, like, I think BQN and APL follow the same mechanism in that double struck X and omega are what you start with in a monadic function, and then you add the extra one, which becomes the second parameter, which is on the left, which is double struck W and alpha. But in J, correct me if I'm wrong, you start with Y and then you add X. And that's, like, the reverse of what BQN and APL do. And so I never – and this is – it becomes tricky because whenever you're dealing with a commutative binary operation and doing reductions and scans is where it matters more a lot of the times. And that's the thing is all the scans work differently. APL does the broken thing, in my opinion. I know J has both, but, like, almost every single time I do a noncommutative binary operation with a scan in an array language, I have to do the equivalent of what in APL is, like, a alpha, catenate, omega, just in, like, a defun, and then do a scan to see what the order – like, what is the accumulator argument. Like, I can never keep that – and it's a confusing thing even in other languages. Like, a lot of the times, depending on the –

00:26:15 [ML]

Yeah, well, Dzaima keeps complaining about this in BQN, so – for fold mainly.

00:26:20 [CH]

Yeah. And so I guess, yeah, my ultimate question is, is there a way to keep this – I mean, we'll talk about J specifically here, like Y goes Y to XY. And, like, I couldn't figure out if my problem was that the scan in J was that of APLs, and so sometimes you run into odd behavior. So at one point I tried switching to one of the, like, scan folds, the one that outputs the list instead of a single value. So I think it was a multiple forward fold.

00:26:49 [HR]

Oh, multiple, yes.

00:26:50 [CH]

Yeah, and so I switched to that. That didn't help. Then I went to suffixes just because I was – I had tried, like, six other things, and I was like, "I'm pretty sure I don't need suffixes, but we'll give that a shot instead of prefixes." And then I was switching the X and Y around because I was like, "Well, I must have the X and Y." So there was, like, a bunch of binary things, right? You can choose prefix, you can choose suffix, you can choose one of the folds. You can swap the X and Y. Probably I should just go and learn, you know, how to actually use the language instead of just being like, "I don't know what's going on here," and then what they do is edit and pray.

00:27:20 [HR]

That occurred to me too. There are pictures in the wiki. Oh. If you look up the – go to NUVOC and look under Fold, we do our best to show what happens.

00:27:34 [CH]

I'm at the NUVOC Fold page, aka /FCAP, because I guess it's a F colon.

00:27:41 [BT]

And one of the things with Fold is I believe you've got sort of two levels of X and Y, right? You've got the original X and Y you bring into your Fold, but then when you get inside the Fold, there's another X and Y that you're looping through.

00:28:00 [HR]

Yes. The individual applications of U and V have their own X and Y parameters. We had it one way to begin with, and people complained about it. We changed it to what it is now. We're hoping that making everything as much as possible flow right to left would be the most mnemonic thing, but it's particularly on the Fold forwards. Fold reverse seems natural to me. Fold forward seems –

00:28:31 [ML]

Yeah, because it's still – it takes the accumulator as the right argument, right? So it's kind of – I mean, if you think about the movement through the array, it's like the function's flipped in that respect.

00:28:37 [HR]

So you're going to have to get a right model in your head before it's going to work. I think maybe what you need to do is drop all those other languages and concentrate on J.

00:28:59 [CH]

When you said you need the right mental model, I was thinking in my head, I have a really good mental model of how all this stuff works. Just sometimes you go from one language to another, and then it swaps. The problem is that I have a good mental model. It's just that two little components get swapped, but there's six swappable components. Then when something goes wrong. I'm like, "Huh, well, the first thing I'm going to do is I'm going to replace every Y with an X and every X with a Y." Fingers crossed, that's what I need here. When that doesn't work, I'm like, "Well, I don't know what I'm going to do."

00:29:25 [HR]

I would say the first thing ought to be to bring up – what I do, because I have the same trouble remembering it, is I bring up the Fold page and look at the pictures again.

00:29:33 [CH]

Are the pictures the ASCII diagrams, or have I landed on the wrong

00:29:37 [HR]

I don't know let me see.

00:29:39 [CH]

The Fold page, because there are some ASCII diagrams, but it's only for the – or actually, that's not true. There's Fold, Multiple Forward, and then there's Reverse Folds, and each of those has an ASCII.

00:29:48 [HR]

Well, what I'm thinking about is not ASCII.

00:29:51 [CH]

Okay, because I was thinking that you were hyping it up a little bit more than not. There's nothing wrong with ASCII art, folks. It's pretty nice ASCII art, I got to say. It doesn't look LLM-generated. It looks like it was hand-human-curated ASCII art.

00:30:05 [BT]

It's hand-crafted, yeah.

00:30:09 [CH]

I was thinking that maybe there was a different diagram. And while Henry's looking that up, do we know why is it Y first and then add? Why did J –

00:30:15 [ML]

I think they just wanted to use X and Y, and they didn't want them out of order.

00:30:18 [BT]

Yeah, and it shows up as well when you're looking at adverbs or conjunctions, because you also have m and n and u and v. u and v if you're referring to verbs, and m and n if you're referring to nouns in a conjunction or an adverb.

00:30:35 [HR]

Well, Fold's always going to be u and v. Somebody's changed this page last time I saw it.

00:30:42 [CH]

Okay. Let's go to the history. Let's figure it out. Let's do this another time. We're going to call someone over here.

00:30:46 [BT]

Let's hope it wasn't me.

00:30:49 [CH]

There's a lot of edits by the person with the name of Cameron. If you're listening, Cameron, and you got rid of those diagrams.

00:30:55 [BT]

Cameron has done a lot of edits.

00:30:57 [HR]

Yeah, and good work, too. I don't see anything wrong with these. That does describe what it does. I'm okay with it.

00:31:08 [CH]

Cameron, you're on thin ice. We're going to send Marshall after you. We're going to send our local bouncer, and he's going to get you.

00:31:14 [ML]

I don't care.

00:31:17 [CH]

Yeah, just don't modify the BQN diagram. Do whatever you want to the JWiki.

00:31:21 [HR]

Those are fine diagrams. Yeah, look at them. Look where X comes in. X is switched all the way over to the right. It comes in. It goes up the tree. That explains everything. And it's more compact than the old diagram, which is a virtual win.

00:31:37 [CH]

Yeah, to skip back, I actually never realized that J and APL are consistent. TUV, WX, and I guess BQN as well. I've got to say the alphabet out loud because I can't tell just off the top of my head of W and X, what order they come in. But I guess that is the pattern. I guess I don't know why I never noticed that omega and alpha. I guess because there's less attachment. Like, they're just Greek letters floating in space to me. Like, obviously, it's beginning and end of the alphabet. But when I see X and Y next to each other, you add Y, then, yeah, it seems odd. But I guess it's to be consistent. You want them to be sorted. Yes. And all of them are that way. So, they actually all are consistent. I just had, like, a mental snafu. Yeah, it's better that I have a mental snafu than the languages designed something into them.

00:32:32 [HR]

Well, another performance issue that we work quite a bit on is the speed of name lookups, which is particularly important in a multi-threaded environment. Because since all global names are -- all public names are shared among all threads, you have to do something to lock the values when you access them. And that can be slow. So, it's a real shame if you have to search through multiple locales to find a verb, locking each one as you go along. So, we put a lot of effort into reducing the number of times a name needs to be locked. And in particular, verb names -- most programs don't change the verbs and modifiers very much. So, we cache those lookups. The caches are invalidated if a non-noun is modified, but this is particularly useful when a named verb was used with rank, where previously it looked it up every time. Now, it only looks up once.

00:33:43 [ML]

So, you had to deal with cache invalidation and naming things. Cache invalidation while naming things.

00:33:50 [HR]

Explain that a little more.

00:33:52 [ML]

Those are the two hard problems in computer science.

00:33:55 [HR]

Oh, okay.

00:33:56 [CH]

Don't they say that there's two hard problems in science?

00:33:59 [ML]

Don't! This is not a good joke. I don't like it. [everyone else laughs] I know what you're going to say.

00:34:07 [HR]

Off by one?

00:34:07 [CH]

It's naming, caching, and off by one errors? [everyone agrees and laughs]

00:34:09 [HR]

Yeah, I mean, naming, that was when we did threads. The name system was completely rewritten but fortunately, that's over. The other thing to bring up is there's a facility for timing sentences. It's a foreign conjunction. You give it a sentence and it tells you how long it took. That was so unsophisticated as to be unuseful because the only sentences whose performance really matters to you are ones that are executed out of an explicit definition, the ones that are repeated. And we have already done some pre-processing for those sentences. Quite a bit of pre-processing. If they refer to local variables, the local variables will have had a name slot permanently assigned. Any parenthesized string that contains only primitives will have been pre-parsed and stored as a compound. There's some other assists to speed up name lookup. So the upshot of that is if you type a sentence in from the keyboard, it does a lot more work in execution than a sentence that comes from an explicit definition. Of course, it doesn't have to do all the pre-processing that the one in explicit definition did. So if you time it, you're getting a different answer from the one you really want. Anyway, the timing function now reproduces all the pre-processing that is done as part of an explicit definition and _then_ it times the sentence. And it's surprising how precise this timing is. I could rearrange a few instructions to make a load instruction happen earlier, and I can see the difference now in the timing. But this gives a good example of the difference between precision and accuracy. It's very precise. I can tell a difference from a small code change. But I have to average together millions of executions because each individual execution has got a lot of noise in it. Mostly coming from system interrupts from other threads, but also whatever the cache happens to have as the sentence is executed. So it's inaccurate, but very precise. And that has been quite useful. I found some places that surprised me where, with a better timing tool, I was better able to find opportunities for improvement. As part of doing that, I made up a set of benchmarks for the different components of the interpretive overhead and also primitive execution. So there's a page with CPU benchmarks on it that several users have contributed to now, [04] showing how long it takes to start a sentence, end a sentence, run a small sentence. On the Apple Mac, a simple "A equals A plus B" sentence takes 11 nanoseconds on one of the Macs. The value of this is you can look at that page, if you want to get an idea of what CPU you might want to buy. I was very impressed with what Apple's done, I've got to say, considering that all I have is an Intel machine and I coded it to be as fast as it can, for that. The Apple does a very good job. And Bill Lam is a big part of that too, because he is in charge of the code that converts the parallel Intel arithmetic instructions into ARM or whatever, arithmetic instructions. The performance there is comparable. So that's it! That's release 9.6.

00:38:27 [BT]

One of the things you've added, Henry (I think you've added it) is you've made named locales permanent, unless you decide that you don't want them to be permanent. That wasn't always the case, was it?

00:38:41 [HR]

No, it wasn't. That's a performance thing. If a locale can be deleted, then any thread can delete your locale and you have to lock it every time you want it. When you want to use it, you have to make sure it doesn't go away. So that was part of the improvement for name lookups. An ordinary named locale sticks around. If somebody wants to delete it, the locale itself will just be empty, but it will continue to exist. That avoids some read for ownership cycles that are quite expensive.

00:39:17 [BT]

So what I used to do is I'd put coerase when I was working through something; I'd put coerase up at the top and clear the locale. It's still going to clear the locale and then do my new definitions, is it?

00:39:28 [HR]

I think so. I think it clears all the names.

00:39:31 [BT]

The locale will stay.

00:39:33 [HR]

Yeah, if you did a coerase and then look to see where the locales were, you'd find it's still there [Bob agrees]. It's just empty. If you really need to delete it, you can make the locale impermanent when you create it, but then it's going to be slower to access.

00:39:48 [BT]

Well, in that case, it's doing what I want because I don't want to get rid of the locale. I want to get rid of everything I've defined, so I start from scratch. Yeah.

00:39:55 [HR]

One thing that CPU benchmark pages showed was that the Apple CPUs are really fast for locking instructions. Most of the time spent in looking up a public name is in locking the public table while you read the value. The Apple machines do a much better job of that. Well, I don't have the latest. Nobody's got the latest Intel machine yet, but I was very impressed with the Apple CPUs.

00:40:30 [BT]

And I guess we should give credit to Adám for suggesting that we add the infinite to the left side of the shape or reshape.

00:40:41 [HR]

That's right. He gave me the whole spec for that and I've used it. It's great. It's a very terse way of saying what you need to have done.

00:40:49 [CH]

One of the things that I'm curious (and I'm not sure to what extent you can actually answer this) but you mentioned that you've started to see usage of the fold primitive on the forums and stuff. I guess we've never asked you this in the past, but if you're able to, is there a state of the unions where they give, not just feature specific, but from a community point of view? Do you have your finger on the pulse of what most folks on the forums or in the J community are using J for? I know ArrayPortal is something that's come out of the J community, and I just had it up. It hasn't been working for the last couple days, but then I refreshed it, and it did. I think it's just got so much material that it's scraping behind the scenes that it has some latency issues. I clicked "all" and then tried to search for something, and then it's completely fallen over. If I switch it to "none" and then go "J", and I still search it, it doesn't show up. I'm pretty sure if I refresh the page, and then I search right now (I'm just searching "Catalan"), now it all shows up. And I have to say: this ArrayPortal thing, if we can get this working smoothly, is like a godsend. It is so good for finding stuff across the Jsoftware website, all the ArrayCast show notes, everything like code, etc. It's so awesome. Anyway, I know that's something that's come out, but anyways, I'll throw it over to you. From your perspective, what is the state of the union address for the J community? If you aren't really able to say (because, what is it Marshall always says: "I have no idea what people are using!" because if they're happy, they never tell you anything, right?) ...

00:42:28 [ML]

That's exactly what I was thinking right now [chuckles].

00:42:30 [HR]

Well, yes, he's right. Those of us at Jsoftware have day jobs, and we use J, mostly. So I would say that most of our guesses about what's useful is what's actually useful to us for the stuff we do. That's going to obviously give us a warped view of what's needed, but users have not been reticent about asking for things if they want them. So we take that into account. Other than that, as long as it works out! The big thing we don't have is good dictionary support.

00:43:13 [ML]

Dictionary as in the data structure?

00:43:15 [HR]

Yeah. Priority queues, hashtables, binary trees, all that stuff. It doesn't fit in well with J's concept of a noun as an immutable thing. So we have to come to grips with how we're going to pass around an object that's subject to change, and yet without requiring copying of the object.

00:43:19 [ML]

And you have to address the issue of the circular references somehow, if you modify a hashtable to include itself as an element.

00:43:52 [HR]

Right. Well, the dictionary will be in some way a specially tagged data type.

00:43:59 [ML]

Yeah, so you can close that off in some way.

00:44:02 [HR]

Yeah, like a box that tries to box itself. So yes, don't allow that.

00:44:08 [CH]

So dictionaries are on the roadmap.

00:44:11 [HR]

Yes, for sure. That's one of the big focuses for 9.7. [05] We've had discussions about it, and I think to the point that we might be ready to start moving on it soon. It's really hard to get a good spec for that, so a lot of thought is required.

00:44:26 [BT]

One of the other requests for proposals you had was for line continuation: the dot dot and the triple dot.

00:44:32 [HR]

Yes, we could never reach an agreement on whether that's a good idea. I personally like it, but on occasions it is a lot of work for other people, too. It breaks a lot of things. How valuable is it really? Well, I'd like to see it. Maybe someday.

00:44:52 [BT]

And that's why I think on the site where we're talking about the different changes to J9.6 (we'll put a link into it), it's one of the things right off the top. There's a discussion about what people liked and what people didn't like. And as soon as I saw that was up there at the top, I went into J9.6 and said: "well, maybe they ..." and of course it's not there [laughs].

00:45:19 [HR]

It's not there. It does break a lot of things. Although it makes commentary much more effective, in my view. That's why I would like to see it.

00:45:31 [BT]

But I suppose there's other people that have a different perspective on comments.

00:45:36 [HR]

Yeah. Yeah. [Bob laughs] Opinions vary. Well, yeah, I'm fanatical about comments, so I can't use myself as a model for what ordinary users do.

00:45:48 [BT]

No, I think if anybody wants to see really extensively well-commented J code, they should go into [... thinking]

00:45:57 [HR]

Dissect, maybe

00:45:59 [BT]

Dissect, yeah. Because it's amazing. And is it 15,000 lines?

00:46:04 [HR]

Yes. 15,000 [chuckles]. That includes tests, but yeah, probably 14,000 lines of real code.

00:46:10 [BT]

And right now, it's not working for the newest versions, right?

00:46:15 [HR]

I think it is, yeah.

00:46:16 [BT]

Is it? Okay.

00:46:17 [HR]

Yeah, Marcin Zolek.

00:46:19 [BT]

Oh, okay, so you got somebody to work on it. Because at one point, you were waiting for ... [sentence left incomplete]

00:46:21 [HR]

Yes, he's been magnificent. He took it and we fixed the bugs that it showed in the J release. We fixed the bugs that J release showed in Dissect.

00:46:33 [BT]

Oh that's fantastic.

00:46:45 [HR]

It passes most of the tests. The problem was that J has changed a lot and requires a little bit of maintenance now, but it mostly works.

00:46:45 [BT]

Because I think the initial crack sort of showed up with direct definitions. I don't remember whether you implemented that to come in or whether that was kind of where you stopped, and I guess as Marcin took on.

00:46:57 [HR]

Well, it's a sentence debugger. I guess if the sentence includes the direct definition, would it work? It might. Yeah, probably still work. I don't know; I don't remember that. I could not take control. I gave it to Marcin [Bob laughs] and he's gone and run with it.

00:47:15 [BT]

Well, that's certainly good news because I know a lot of people really found that tool invaluable to be able to look in and figure out, almost as a flow state [Henry agrees], to see what was happening and when it was happening. As well as you had tutorial information in there as well, so there'd be explanations at different levels of verbosity.

00:47:36 [HR]

Well, it should still be working. If not, mail the forum. [laughter]

00:47:43 [CH]

Are there other features that you can tease the listener about in J9.7? You mentioned dictionaries. Are there things that are on the roadmap or that's the big one?

00:47:56 [HR]

That's the big one. I mean, I'm always rewriting the parser and the name lookup code. I've probably rewritten the parser 15 times now.

00:48:06 [CH]

You sound like Aaron [laughs]. Is this an array language implementer's common trait: re-implementing N times? N different for each language?

00:48:17 [ML]

I haven't touched it in months and months.

00:48:20 [CH]

All right. Well, you've got Singeli though, so I mean, how many times?

00:48:24 [ML]

But I don't rewrite the code there either.

00:48:25 [CH]

All right

00:48:25 [HR]

Well, I finally got the parser to where it runs entirely in registers on the Intel machine. It doesn't have to store any temporary variables and it's really fast. I'm hoping I won't have to rewrite that again. Dictionaries will keep us busy, I think.

00:48:48 [CH]

I can't remember [Kai's take about Uiua]. Because they have an experimental hash-map, but I think Kai's take was almost all of the times he's reaching for something, there's a primitive in Uiua that he prefers to reach for instead of reaching for the hash-map. But it is interesting that J's thinking about adding a dictionary. BQN got at least this round in the last year, people started using it. I think you said two years ago you were trying to get it ready.

00:49:18 [ML]

Yeah, it was two years ago or something.

00:49:19 [CH]

And k has their tables, obviously. APL is the one holdout, but it's interesting that a lot of these array languages (I think also Kap) are getting some support for a kind of hashtable or something like that.

00:49:38 [HR]

"i." in J is a hashtable .

00:49:42 [CH]

"i."?

00:49:43 [HR]

It's just not a persistent hashtable.

00:49:45 [ML]

Yeah, the thing is you have to have all your data there at once, which almost always you do. And that's so much faster [Henry agrees] because the language can just look at all the data and see: "well, what do I have here?" And it can check properties like what's the range of the data and so on.

00:50:02 [HR]

Right.

00:50:03 [ML]

But sometimes you have something that needs to be persistent and updated over time. APL also sort of addresses this because they've got an I-beam that basically accelerates the lookups with "iota" and "epsilon" and stuff. So it will store a persistent hashtable, but it's supposed to act more like a regular array.

00:50:29 [HR]

In J, if you know what the hashtable is and it's not going to change, you write "array & i." and that calculates the hashtable for the array and saves it for later use. So between that and just plain old "i.", you can go a long way without dictionaries.

00:50:58 [ML]

So that's similar to what Dyalog has, but it also has some special ... [sentence left incomplete]. It doesn't really make sense to say: "well, I have this immutable array and I want to declare it hashable and even if you change it, it should still be hashable". Because changing an immutable array is not what you actually do: you create a new array. But it's got some special cases, like if you concatenate something to it, the array in that variable will maintain the hashtable and so on.

00:51:29 [HR]

Oh, that's interesting. Well, when that's what you need, you got to have some special support for it because when the array gets to be ... [sentence left incomplete].

00:51:40 [ML]

Yeah. Well, my take in BQN was that this is just not an array operation, which is why I did it [in] very traditional Java style (or whatever object-oriented languages there were before Java even). [06] So I said: "if you want this functionality, you're not doing array programming anymore, so use the objects that don't act like array programs".

00:52:05 [CH]

To interrupt you for a sec, I'm a bit confused. You guys said "i.". And my first thought was like: "well, I know they're not talking about iota".

00:52:14 [HR]

We are.

00:52:16 [CH]

We are?

00:52:17 [ML]

Well, it's the same as APL iota: the monad is an index generator and the dyad is a search.

00:52:22 [HR]

That search has a hash built into it. Well, it might.

00:52:26 [CH]

Oh, I see. I see.

00:52:27 [HR]

As Marshall says, it might have a range table built under it. It might have a binary tree built under it

00:52:37 [CH]

I was going to say this is completely unobvious because [for] dyadic iota, I was like for all in intents and purposes, that can just be like a quadratic lookup, right? We don't know. But you're saying under the hood, it has a hash-map that's making that not quadratic.

00:52:55 [HR]

Yeah, you would lose all your customers if it were actually quadratic.

00:52:58 [ML]

They kept doing that for a surprising amount of time in the early interpreters, as far as I can tell. Like, there are notes that are like: "oh, we changed this search to use a hashtable or a lookup table".

00:53:10 [HR]

This is on APL?

00:53:11 [ML]

Yeah. I mean, you can't really do that anymore. I guess partly because the data that people work with is so much bigger. So quadratic is a much bigger deal than it used to be.

00:53:21 [HR]

Yeah, that's a very good point. [When] you get hundreds of millions of values, quadratic is out of the question. So everything has to be with some sort of index.

00:53:34 [CH]

Yeah. I mean, it's interesting that this comes up [on] (not the last virtual meetup that I had, but two meetups ago) this A9 series that Stepanov taught at A9, a subsidiary of Amazon (there's these lectures online; I'll link them if folks are interested). It's C++ based but one of the problems that we had all chosen to do was count of the unique numbers, where unique means deduplication, not the weird bash or C++ semantics of adjacent duplicate removal. And one of the individuals in the meetup, Jonathan (who's a data science, R individual but likes array languages) solved it with a dyadic iota. And I actually commented, because we were sharing solutions that people had submitted. And I was like: "okay, this would probably be quadratic" because I don't know anything about the implementation of Dyalog APLs. And naively, that's what you would think, right? Like if you had to guess how dyadic iota in an array language implemented, would I guess that behind the scenes, they materialize a hash-map and are copying the stuff. It's unclear. Like I imagine they do some kind of heuristic, like if there's only one value or a couple values, they just do the two linear searches, right?

00:54:54 [ML]

Well, yeah. Dyalog even has a special check to say: "are the two arguments to dyadic iota the same?" And in that case, it does a single pass instead of two passes.

00:55:08 [HR]

Yeah. J does that also.

00:55:08 [CH]

Oh yeah, yeah.

00:55:09 [HR]

I mean, [in] J there are totally different hashes for tolerant comparison and intolerant comparison. Intolerant comparison is ... think that over a while.

00:55:22 [CH]

This is actually a request that I've had from Phineas (past guest now; friend of the pod but we also knew each other before he came on the podcast). He was saying that some of his favorite episodes are the ones where we accidentally end up deep diving on a single or a couple primitives. I wonder if going forward, we could bring Henry on for some of these. We can bring different language implementers for different primitives just to get a variety. Where we deep dive on implementation. Some of them are going to be boring, obviously, like iota. We're not going to deep dive on iota.

00:55:54 [HR]

Wait, what? What!!

00:55:56 [ML]

Now, the multidimensional form ... [laughter]

00:55:59 [CH]

All right. Perfect! My point is made. Even the one I thought that wouldn't be exciting.

00:56:03 [ML]

You're talking about the monadic one, right?

00:56:05 [CH]

Yeah, the monadic one.

00:56:05 [HR]

Oh, monadic "i." Okay.

00:56:09 [ML]

The multidimensional one has a bit of subtlety. And actually, k's version of the multidimensional one is pretty interesting where it returns the same data, but it presents it in a row-wise format. So, the number of rows is the number of dimensions of your indexing and each row has all the flattened data of that one particular direction, I guess. They call it odometer. But yeah, there's actually some pretty sophisticated stuff in implementing that. Probably not a whole episode's worth.

00:56:46 [CH]

Well, I mean, that's what I'm saying. In my head, I was thinking [of] the monadic iota that only takes an integer. But then I completely forget that not every iota works the same way, right? [In] J, you can pass it a rank one list that gives you different behaviors. So the point being, even [with] the simple primitives, I guarantee you we could talk for an hour, if not more, about just monadic iota. But I was thinking about dyadic iota in this case.

00:57:12 [ML]

The important thing is you're definitely not writing one value at a time for iota [Henry agrees]. So, it's not as simple as you think, even for a very basic "iota one million". But I'll stop the derailment [chuckles].

00:57:24 [CH]

All right, here we go. And that's the thing, we bring Elias on for these conversations, too. It's going to be completely different when he comes on because he has a lazy language, right? So, for him, iota does nothing.

00:57:36 [ML]

Yeah, totally different implementation considerations.

00:57:38 [CH]

So, announcing a new series, folks. We've passed the 100 episode mark. We're now on 104. I don't know what season this is, but in the triple-digit episodes, we're calling it tentatively "Primitive Talk". When you see in your podcast app "Primitive Talk:", we're going to choose ... I don't know. For certain primitives, maybe we'll do both monadic and dyadic at the same time. The real confusing part is that some of these languages call them different things. I guess it's the primitive attached to semantics, not so much the actual glyph itself. I mean, J doesn't even have glyphs. But, yes, coming to a theater near you soon is deep dives. We'll try to bring implementers on. We'll mix it up from time to time, and then we'll deep dive on these. Because, yeah, I've even talked when I've had Aaron on ADSP and Tacit Talk. He alluded to that [in] some of the Dyalog implementations, [for] one primitive, [there are] 16 algorithms under the hood because of the amount of dispatching they do based on: "oh, we'll check this; we'll check this; we'll check this." I'm sure in J, it's even more tricky because you've got a richer stack of types, right? You've got a ton of stuff that the other array languages [don't have]. When you're code golfing and you need to print out some 100 character digit, BQN, really falls over. It falls over, folks. You probably can do it in BQN, but it's much easier to go to J and you just put the little X.

00:59:05 [ML]

Oh, okay. Yeah, when you're working with big integers.

00:59:08 [CH]

Yeah, yeah, if you need factorial whatever [Henry laughs]. Whereas [in] J, you just go and change the type on your integer and poof! There's the answer.

00:59:16 [HR]

Look at the grade on floating point lists. That's an interesting algorithm.

00:59:22 [CH]

Yeah, we should find a way. I mean, people can just email us, but we should get a poll where (like a little, what do you call it? a Reddit forum, minus everything that's terrible about Reddit), where people can upvote the primitives they want us to talk about. [Henry enthusiastically agrees]. Maybe we should start a GitHub issue or something. Although, that doesn't work. I guess that's the way to code golf. They set up a separate issue for every language. We're not going to set up a separate issue for every glyph [laughs]. We'll find a way, folks. For now, just email us if there's a primitive you really want us to talk about. Anyways, end of that wild tangent. I don't even know how we ended up talking about that.

01:00:00 [BT]

Our next episode, by the way, will be the start of season four.

01:00:03 [CH]

Season 4! Are we actually keeping track of seasons?

01:00:06 [BT]

Yeah, on the year.

01:00:07 [CH]

Woo!

01:00:08 [BT]

This is 104, right? So, 26 episodes in a year. It all works out.

01:00:16 [ML]

Wait, so you are counting starting at zero, right? Starting with season zero?

01:00:20 [BT]

Yeah.

01:00:22 [CH]

Didn't we re-index it at some point?

01:00:25 [BT]

We re-indexed it at episode four, I think.

01:00:28 [ML]

See, this is why you should use zero indexing, because it still works when you divide. [Bob laughs]

01:00:36 [CH]

I regret zero-indexing ADSP. I think I one-indexed all the other podcasts after that, because I just hate saying it's the 200th episode, when really it's the 201st. Because you zero-indexed one. Language doesn't match up with the pointer nicety [chuckles] of having zero be the first index. Anyways, we're definitely past the hour mark. It sounds like we got to all the major features in 9.6.

01:01:07 [HR]

Oh yes.

01:01:14 [CH]

Are there other things that we want to ask Henry? Or Henry, that you want to tell the people while we have you on the mic?

01:01:15 [HR]

No, I think we can wait until 9.7 release.

01:01:18 [CH]

Oh, we won't wait. We'll probably have you back at this point. If we're starting Primitive Talk in season 4 ...

01:01:22 [HR]

Yeah, we're doing Primitive Talk, I want to be on that.

01:01:24 [CH]

... we're going to have you. Let us know which ones. You said was grade on floating point. There's lots of people we can bring back, too. Bob Smith. We got tons of folks that I'm sure they'll be listening if they are listeners. [07] I'm sure there'll be some point we'll be doing primitive talk, and Henry will be thinking: "no, no, you got to do it this way; that's not the right way to do it." It'll be good. It'll be good. Primitive Talk. I'm excited.

01:01:47 [BT]

Quaternions.

01:01:50 [CH]

Oh, yeah, yeah. [laughs]. That's right. Quaternions and octonions.

01:01:56 [ML]

Did he say he defined an ordering on those? Can't remember. Obviously, they're not an ordered field, but I think he said he allows you to sort them.

01:02:04 [HR]

You could define the ordering, surely.

01:02:07 [ML]

Yeah, they're not an ordered field in the sense that the ordering doesn't respect certain algebraic properties.

01:02:12 [BT]

My intuition is way off on those things.

01:02:15 [HR]

Right.

01:02:15 [CH]

I don't have an intuition at all for that kind of stuff [laughs].

01:02:18 [ML]

Well, the thing is if you're ordering them right, you can't order them in a way that mathematically makes sense, which means you get to ignore all the mathematics and just treat them as a bunch of components.

01:02:29 [CH]

All right. Well, we will say thank you so much to Henry for once again, seventh time appearing on the podcast, soon to be eighth, soon to be ninth by the time we get to J9.7. I guess that means we're going to have to bring back some of the folks because we don't want you to be like twice as many as the next most frequent. But it's always a pleasure having you on to hear about J. If the listener has any questions about J9.6, any comments on what is the first primitive that we do a deep dive, a whole episode dedicated to, you can reach us at ...

01:03:02 [BT]

contact@arraycast.com. You can reach us there and yeah, I'm particularly interested to see whether there's ... [sentence left incomplete]

01:03:07 [ML]

Didn't we already do an episode on indexing though?

01:03:10 [BT]

Yeah, we did do it. I think we started on doing something on indexing, but they are deep dives. They do tend to wander around a lot, but contact@arraycast.com. I am particularly interested to find out whether anybody selects my area that I would always like to find out more about, which is symbols in J, because I just don't see them used very much.

01:03:35 [HR]

They're not. It might be time to put them to the sword.

01:03:39 [BT]

Oh, no! No, not before they have a chance!

01:03:42 [ML]

Shouldn't have brought it up, Bob [Marshalls laughs while Bob groans]

01:03:46 [CH]

What do you mean? Do you mean symbols as in the glyphs? You guys added glyphs to J?

01:03:50 [HR]

No, no, no, no, no. A symbol is an alternative to a boxed character string. Basically, there's a single table of boxed character strings. Each one of them has a number. So you could present boxed character strings to the system and it will remember them. You can then look up and find out what the number is for subsequent strings. And I expect that function will be subsumed into dictionaries.

01:04:30 [BT]

I was going to say, that's sort of what I was kind of thinking. Is that when you were talking about dictionaries, I thought that's probably going to absorb symbols, because that's kind of ... [sentence left incomplete]

01:04:38 [HR]

Yeah, there's only one global symbol database. It's shared among everything. I think dictionaries are better. I believe that our consensus has been that we don't really care much about keeping symbols, and there's been no real need to delete them, so they're still there.

01:05:00 [BT]

You could do some very interesting things with them, because you can use Unicode with symbols, and have things appear the same way, but declare them as different versions of Unicode, whether it's UTF-16 or whatever. They think of themselves as different things, even though they look exactly the same.

01:05:19 [HR]

Is that a good thing or a bad thing?

01:05:20 [BT]

I don't think it's a good thing. I just thought it was really wild [laughs]. If you wanted to obfuscate things.

01:05:27 [HR]

Thanks for your input [chuckles].

01:05:26 [BT]

Okay [laughter]. And if you want your input, contact@arraycast.com. We really drifted out in that one.

01:05:38 [CH]

That's all right. That's what we're used to here, is keeping a topic stack, and putting them on, popping them off, and we land the plane at some point.

01:05:46 [ML]

Yeah, we got to get this plane out of the water [laughter]

01:05:49 [CH]

[laughing] In the water? Whoa, it's a little turbulence on the way down. There's a couple of passengers.

01:05:53 [ML]

Our plane did a deep dive, and we're really not sure how that happened.

01:05:56 [CH]

The passengers, a couple of them have their hands gripped tightly to the armchairs of their seats. But everybody! This plane is going to land, and it's not going to roll over and catch on fire or anything like that. We always land the plane. Sometimes it's a bumpy landing, but we always land the plane [laughs]. Anyways, thank you for coming on, Henry. We'll do this again. We'll have you back for Primitive Talk sometime this year. Like we said, reach out to us if you've got thoughts on the episode, and we look forward to hearing whether symbols make it or not. With that, we'll say, Happy Array Programming!

01:06:02 [everyone]

Happy Array Programming!

[music]

</details>
