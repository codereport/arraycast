---
title: "Episode 68: Brian Ellingsgaard and the Rayed-BQN Games Framework"
date: 2023-12-09 00:00:00 +0000
episode: 68
buzzsprout-id: 18617059
keywords:
- array-programming
- array-languages
- conor-hoekstra
- brian-ellingsgaard
- games
- bqn
- rayed-bqn
- advent-of-code
- aoc
mp3-url: "/assets/audio/episode68.mp3"
episode-type: full
explicit: "no"
block: "no"
layout: podcast
excerpt_separator: <!--more-->
redirect_from:
  - "/episodes/episode68-brian-ellingsgaard"
  - "/episode68-show-notes"
---
Brian Ellingsgaard tells us about developing a games framework on BQN and we all discuss the challenges of Advent of Code.
<!--more-->

**Host:** Conor Hoekstra

**Panel:** Marshall Lochbaum, Adám Brudzewsky and Bob Therriault

---


## Show Notes

Array Cast -  December 8, 2023

Thanks to Bob Therriault, Adám Brudzewsky, Marshall Lochbaum and Brian Ellingsgaard for gathering these links:

**[01] 00:01:26**

- [J Viewer wiki](https://code.jsoftware.com/wiki/J_Viewer)
- [J Viewer video](https://youtu.be/SLJS84u4eVc)
- [APL Seeds](https://aplwiki.com/wiki/APL_Seeds)
- [March 27, 2024](https://www.dyalog.com/apl-seeds-user-meetings/aplseeds24.htm)
- [Dyalog User Meeting feedback](https://dyalog.fillout.com/umf-general)
- [Conor's Jelly streams](https://www.youtube.com/watch?v=XkLsy_I_H6w)
- [youtube.com/watch?v=zOB5D_NgVJU](https://www.youtube.com/watch?v=zOB5D_NgVJU)
- [Jelly vs. BQN](https://www.youtube.com/watch?v=k9BNn39gWiM)

**[02] 00:07:22**

- [Brian Ellingsgård's GitHub](https://github.com/Brian-ED)
- [Rayed-BQN](https://github.com/Brian-ED)
- [/rayed-bqnraylib](https://www.raylib.com/)
- [Faroe Islands](https://en.wikipedia.org/wiki/Faroe_Islands)
- [Python programming language](https://en.wikipedia.org/wiki/Python_programming)
- [Dyalog Competition](https://www.dyalog.com/student-competition.htm)
- [Jelly programming language](https://github.com/DennisMitchell/jellylanguage)

**[03] 00:13:36**

- [Advent of Code](https://adventofcode.com/)
- [Jeremy Howard episode on the ArrayCast](https://www.arraycast.com/episodes/episode31-jeremy-howard)
- [Brian's Advent of Code](https://github.com/Brian-ED)
- [/BQN-Advent-Of-CodeDyalog APL Ltd.](https://www.dyalog.com/about-dyalog-ltd.htm)

**[04] 00:17:36**

- [Trains as combinators](https://aplwiki.com/wiki/Train)
- [Brian's Discord bot](https://github.com/Brian-ED)
- [/Fire-Owl-botAPL Farm Discord](https://aplwiki.com/wiki/APL_Farm)
- [APL Orchard](https://aplwiki.com/wiki/APL_Orchard)

**[05] 00:22:54**

- [Advent of Code Day 5](https://adventofcode.com/)
- [2023/day/5Rust programming language](https://en.wikipedia.org/wiki/Rust_(programming_language))
- [ToNats](https://github.com/mlochbaum/bqn-libs/blob/205691d/strings.bqn#L149-L150)
- [Singeli programming language](https://github.com/mlochbaum/Singeli/)
- [Brian's Advent of Code](https://github.com/Brian-ED)
- [/BQN-Advent-Of-CodeAdám's video on parsing](https://www.youtube.com/watch?v=AHoiROI15BA)
- [Optima Plug-in](https://marketplace.visualstudio.com/items?itemName=OptimaSystems.vscode-apl-language-client)

- [Raghu's VSCode Plugin](https://github.com/razetime/bqn-vscode/)
- [Zig comptime](https://ziglang.org/documentation/0.11.0/#comptime)

- [nulldatamap](https://gist.github.com/nulldatamap)

**[06] 00:37:39**

- [Functional programming](https://en.wikipedia.org/wiki/Functional_programming)
- [Haskell programming language](https://en.wikipedia.org/wiki/Haskell)
- [Object Oriented programming](https://en.wikipedia.org/wiki/Object_oriented)

**[07] 00:40:14**

- [Kap programming language](https://kapdemo.dhsdevelopments.com/)
- [Kotlin programming language](https://en.wikipedia.org/wiki/Kotlin_(programming_language))
- [ngn/apl](https://aplwiki.com/wiki/Ngn/apl)
- [dzaima/apl](https://aplwiki.com/wiki/Dzaima/APL)
- [Java programming language](https://en.wikipedia.org/wiki/Java_programming)

**[08] 00:43:44**

- [J programming language](https://www.jsoftware.com/#/README)
- [Leading Axis Theory](https://aplwiki.com/wiki/Leading_axis_theory)
- [Modifiers and Functions in BQN](https://mlochbaum.github.io/BQN/doc/ops.html)
- [Uiua programming language](https://www.uiua.org/)

**[09] 00:48:55**

- [Scrabble](https://en.wikipedia.org/wiki/Scrabble)
- [Trie](https://en.wikipedia.org/wiki/Trie)

**[10] 01:01:50**

- [BQN raymath](https://github.com/Brian-ED/rayed-bqn/blob/master/src/raymath.bqn)
- [C raymath](https://github.com/raysan5/raylib/blob/master/src/raymath.h)

**[11] 01:05:16**

- [Intra](https://fo.linkedin.com/company/intra-fo?trk=public_profile_topcard-current-company)
- [Klaksvig Technical School](https://www.tsk.fo/)
- [Stormwind simulator](https://stormwind.fi/en/)
- [Video of Stormwind](https://www.youtube.com/watch?v=LKbnjVbed9Y)
- [youtube.com/watch?v=9IC78J55F-M](https://www.youtube.com/watch?v=9IC78J55F-M)
- [12] 01:13:16  Contact AT ArrayCast DOT Com


<details markdown="1">
<summary><strong>Transcript</strong> (click to expand)</summary>

Transcript

Transcript prepared by Bob Therriault, Igor Kim and Sanjay Cherian

Show Notes

00:00:00 [Brian Ellingsgård]

About two years ago, I was working with Python and I just stumbled in YouTube and found one of your videos Conor and I found out like you can express like a sum with a plus Slash and the slash just puts the plus between each and like that's so simple. That's amazing.

00:00:20 {Music]

00:00:29 [Conor Hoekstra]

Welcome to episode 68 of ArrayCast I'm your host Conor and today with us we have a special guest who we will get to introducing in a few minutes But first we're gonna go around and do brief introductions. We'll start with Bob then go to Adám then go to Marshall.

00:00:41 [Bob Therriault]

I'm Bob Therriault and I'm a J enthusiast and working crazily on the wiki right now so that I'm actually not doing advent of code.

00:00:49 [Adám Brudzewsky]

I'm Adám Brudzewsky doing language stuff at Dyalog and APL that is and I'm working crazily on getting our Upcoming release done.

00:01:02 [Marshal Lochbaum]

I'm Marshall Lochbaum. I've been through a lot of array languages I'm the creator BQN and the creator of Singeli.

00:01:08 [CH]

And as mentioned before my name is Conor polyglot programmer massive fan of all of the array languages and with that we're going to hop into a couple of announcements and we will start with I think Bob and then we'll go to Adám I think there's like a number of announcements in there. We'll go from there Take it away Bob.

00:01:26 [BT]

Okay, so I have teased this for a while probably about six weeks I think but we have released the J Viewer [01] which gives you the option to look through code and forum posts and the wiki and Rosetta code and GitHub and all sorts of things for J so It's done by Ed Gottsman. He deserves a ton of credit for this he's been working on a long time but it's finally at the point that if you would like you can go to the wiki page and we'll include a link in the show notes and you need to run JQt and you need to be running J 9.4 but once you've got those requirements Then it's fairly easy to open up the the the J viewer and the only other thing I should mention is I think it takes about a gigabyte of space on your computer because what it does is it downloads that and Then from that you do all your searches and stuff and it's lightning fast And as I said, it goes through all the forum posts You can do searches on code look at all the places that certain combinations show up. It's really quite amazing So that's my announcement

00:02:32 [CH]

And I think to add to your announcement you actually posted More than two weeks ago a short video previewing that on your YouTube channel, which we didn't announce Last episode because you wanted to wait till now So if people don't want to download it or just want to check it out before downloading it, there will be a link in the show notes to that video I think it's only a couple minutes long and sort of gives you a really nice preview.

00:02:54 [BT]

So it's about five minutes long and there's actually a link to it on the wiki page, too. So the link we will put both links in but yeah, it's what all the links.

00:02:58 [CH]

All the links will be there Yeah, all right. Awesome. We'll move over to Adám then for his announcements, right?

00:03:03 [AB]

So two things kind of related one is the APL seeds event, which is this a online meeting for people who are interested in APL or just getting started with APL and that's going to be March 27 so you have some advance notice now and we don't have everything settled yet as to what's going to be in it, but and it might be a little bit different than the previous years I'm sure it's going to be interesting though as soon as we have something we'll make sure to announce further on that. And then there's an another half of the year in the the fall of the autumn depending you where you are might even be the spring Dyalog arranges its traditional user meeting and there's been going on for many years now and we are in the process of shaking up in a few things in a Dyalog, and we really want to know What is it that make people come or not come to the user meeting? And what is it people would like to see and experience at such meetings? What works what doesn't work? Even for those people who have never been why didn't they go even if they were interested in the subject?So we're going to leave a link to a survey that you can fill out We'd appreciate that so that we can try to maybe change some things and make it more attractive.

00:04:27 [CH]

Awesome, and wait were the dates mentioned for apple seeds that I space out for like 10 seconds, right when you mentioned them I think I did yeah.

00:04:34 [AB]

It's a Wednesday, March 27, 2024.

00:04:38 [CH]

2024 March 27th. I think I did I did temporarily start thinking about an advent of code problem and BQN trains and combinators versus Jelly so I did I started drifted off at the exact wrong time and I'm listening to these announcements I'm like wait. He didn't even mention the date and I was like wait a second I must have just not been listening being a terrible host. March 27th. Very exciting folks. I think this is gonna be what the third edition of APL seeds

00:05:04 [AB]

Might even be.

00:05:04 [CH]

Might even be the fourth. Fantastic, I think it's a if it is going to be the same as it was in the past it's an online free conference half a day as far as Virtual, I'm just like plugging this even though. I don't work for Dyalog, but you know it's a great conference because it's short It's sweet. It's online. It's completely free and I think you know there's a lot of virtual conferences that'll last for like a week or something and it's kind of hard to attend a Virtual conference when you still got work to do and stuff, but like an afternoon of four hours Whatever super easy to take that off watch some nice talks I think they have a zoom chat and whatnot and there's a little get-together afterwards where you can chat one-on-one with people Anyways links, that's that's how it has been until now.

00:05:42 [AB]

I think we might be changing things a bit on the format there as well And we might even go more than half day We might do it like a continuous stream of all day long depending on the time zone as you can join in. We'll see.

00:05:54 [CH]

All right well. I take back everything I just said that Okay It's gonna be a 24-hour live stream for all time zones, and

00:06:03 [AB]

No I didn't. I'm not promising that but we'll see. We'll figure something out.

00:06:07 [CH]

I do know there are conferences. There's a Java conference. That's famous for that It's like a virtual 24-hour, and they just continuously talk and some people try and stand for the whole thing, but anyways links to all the things we just mentioned I think I was gonna mention too that I did a couple more Jelly streams I also made a Jelly versus BQN YouTube video. We'll throw links for that in the show notes, but we'll talk about Jelly another day. Let's get to introducing our guest today I'm going to attempt. I think we actually did announce his name on a previous podcast I will do my best attempt and then either Adám or Brian himself can correct me because I think they both know how to say correctly. It's Brian Ellingsguard is that is that pretty close?.

00:06:44 [BE]

No. Adám pronounced it differently actually Briann Ellings court is how I pronounce it in Faroese.

00:06:54 [CH]

Wow. That was very far off.

00:06:56 [BE]

But if you're gonna English eyes it then it's Brian Ellings guard, okay? Although Adám pronounces in Danish which is a Rian Ellings court a lot Ellings call

00:07:06 [CH]

All right, so we've got three different pronunciations. Sounds like I'm gonna fail at the the and how do you how do you pronounce the language?

00:07:14 [BE]

It's Faroese.

00:07:15 [CH]

So let's hear that one more time from you and then I'll do my best to to say it that way, but it's not going to happen.

00:07:20 [BE]

Bryan Ellings court.

00:07:21 [CH]

Briann Ellings good.

00:07:22 [BE]

It's OK.

00:07:26 [CH]

All right. We're probably gonna stick with Brian for today. But we've mentioned Brian. [02] I think at least on one other episode potentially not by name in two of them because Brian is the individual behind the raid BQN library which David at least through his videos has made a couple different videos making little snake games and different types of games I myself have played around with it and downloaded it locally. I think I even opened an issue

00:07:54 [BE]

Thank you so much for that.

00:07:55 [CH]

No, you're the one doing the work I'm just pointing out things that aren't and then you're fixing it for me, which is fantastic, so we're here today I guess this is the episode the first of maybe one or two episodes that we mentioned back a couple months ago where we said we were gonna dive into the game programming in array languages and Brian is our first guest to talk about that. So I'm not sure if you want to give us a brief introduction and sort of how you stumbled into the array language world or we can also pivot and do the advent of code because we mentioned we might chat a bit about Advent of Code because it is December of a year depending on when you're listening to this 2023 which means all the programmers are trying to code golf, you know solutions It's been pretty bad this year if you ask me, but over to you Brian, maybe a brief introduction and then we can go from there.

00:08:36 [BE]

Okay, I'm Brian Ellingsgaard. I'm the creator of raid BQN, which is a BQN library I've made a few BQN libraries that I'm very happy of but raid BQN is definitely my favorite and my passion project It's throughout the last few months.

00:08:51 [CH]

How did you discover the array languages? And we should say I can't say this with full confidence But I'm guessing that you are probably our youngest guest is that is that of all the guests we have it looks like.. I don't know how old you are, but I would say that you're either You know high school or university or you know We might need to cut that if you're actually like 20 years older than what you are But you you look quite young compared to our other guests.

00:09:13 [BE]

I am 18 years old currently.

00:09:15 [CH]

Okay? Yeah, so I think definitely that makes you our youngest guest by far, which is very exciting that you've already got a bunch of these libraries out So yeah, how I mean and it's been not directly mentioned, but you live in the Faroe Islands Which for those of you that don't know is a is quite remote compared to you know Where most of us are based and either on you know, Europe mainland or you know, Canada or the USA? So yeah, like how is there a big thriving BQN community in the Faroe Islands? Or is it just you like how did how did you stumble into array languages in BQN?

00:09:46 [BE]

I have never seen anyone else interested in the array languages here, but I will say one coworker actually knew about APL, so that's cool.

00:09:55 [CH]

That's pretty good.

00:09:56 [BE]

I have tried introducing people to the languages, but no no, no one is like interested really But that's oh, that's too bad. They're missing out.

00:10:05 [CH]

Their time will come. Their time will come, you know.

00:10:07 [BE]

Yeah, their time will come how I got introduced to the language or the array paradigm itself about two years ago I I was with working with Python and I don't I just stumbled in YouTube and found one of your videos Conor and I found out like you can express like a sum With a plus slash and the slash just puts the plus between each and like that's so simple. That's amazing I was so amazed with this. I then just watched more of your videos and each symbol I learned what each symbol did and then I tried myself and try APL, of course, and I was just every line I wrote I was amazed and then I got into like puzzles and I did not know what to do because like you can't just Loop your way out of it. I was thinking like how do you loop? How do you repeat stuff and then I used the repeat modifier to mutate a variable and then more and more as I did more of these in the first Dyalog competition two years ago or no not the first but yeah at my first I I I did these loops and stuff and it didn't work So I just I tried using array thinking and with the help of your videos. I actually got somewhat great solutions I'm very happy with them. And in fact that competition I actually won 1,500 kroner because or $200 because I got one of the phase two prizes the Getting the randomized participants. I think it's called making money.

00:11:32 [CH]

Making money. Look, look at that, folks. Making money off of learning the array languages.

00:11:36 [BE]

I was so happy. I even I had to ask my head teacher for for a confirmation that I'm a student there and I bragged so hard

00:11:49 [CH]

That's awesome and when you say when you started doing puzzles Do you mean like the the Dyalog competition like kind of one line or leet code kind of questions like that?

00:11:57 [BE]

Yes yes, oh, I actually asked some of my friends to join in all my friends that is and We had lots of on me and some guy called Dan we did them together and honestly we are we thought it was golfing So we we golfed solutions and told each other character counts.

00:12:17 [CH]

I mean, that's a very common thing to do.

00:12:19 [BE]

Yeah, Oh one solution. I got one less character than them and I was bragging the entire day. I told them like a year ago actually like a year later after the competition and he was like, yeah, I wouldn't have seen that. I was very happy.

00:12:33 [CH]

I mean there is.

00:12:34 [CH]

I mean, we're all kindred spirits here, but there is something very gratifying like that's something with the Jelly language is they literally optimize like they will search for token sequences and then add primitives to replace that so, you know, it seems like random. Why would they have this very specific thing and then you stumble across and you're like, oh, that's that's a replacement for like a four token sequence and it shows up like four different places and you're like, I don't know most people are probably listening to this. I don't know We have probably have an array audience in general, but it does sound a little bit odd to be like wow Why why are you so thrilled with like shaving off two or three or even one character? But there is something very gratifying about it.

00:13:11 [ML]

Well, it's measurable, right? I mean if you if you write like some code, that's really beautiful. I mean you can say oh, yes, it's beautiful But you can't you don't know it's beautiful You just think it's beautiful if you if you know, it's ten characters long then it's ten characters long and that's that right? So you get it there and you say aha. Yeah, there's a one moment of I have it now

00:13:32 [CH]

Especially when you just got like it actually just happened Not to bring up Advent of Code, [03] but I think it was day two where it had like, you know some different colored balls in bags and You needed to do some operations and in Python you have a counter collection, which is like a dictionary and they have operations defined on counters so you can compare counters you basically like if you want to check if all of the values in one dictionary Are less than all the values for the corresponding keys in another you can just do a less than comparison between these two Collections and that was part a and then for part B. You can actually do Max reduction over counters that like take the maximum values For the corresponding keys and I had just written a lambda a comma B colon a pipe B and then Jeremy Howard Previous guests of array cast pointed out that in the operator module you can use the or underscore Which is basically just like a shorthand form of not having to explicitly write out that max reduction now on the array podcast We're all thinking that's very silly because that's built into the language like to do a max reduction It's just you know two characters, but in Python because lambdas are very verbose They've had it to add this module where you and then there's an or keyword So they have to put an underscore after the or so it doesn't clash But anyways when he pointed that out. I was like oh, that's very nice I can I can replace my lambda a comma B colon a you know pipe B with three characters And it does look like a lot better and also like that's exactly what it was designed for right like so that you don't need To handwrite these like very common. You know lambda expressions because they're not very nice in in Python anyways away from Python Back to back to you, so you're you're playing you're not playing you're golfing these things trying to get you know one character less having a blast with your friend Dan and At some point you just start to dive Deeper and deeper and then you end up writing all these different libraries like what what caused that or you were just enjoying the languages so much

00:15:24 [BE]

I love the language and then my Real passion of mine was writing games so I actually started writing this Game in Dyalog APL with the window system I even tried showing Adám this when I was visiting him in Denmark. Do you remember that Adám?

00:15:43 [AB]

Of course, yeah.

00:15:45 [BE]

I don't remember if I got the game to work because it had glitches. I didn't know GitHub at the time, you know.

00:15:49 [AB]

Right You had no way to post me the code. I said to show me so yeah Yes, but I think Brian is the only one while I've been a Dyalog Who is like an APL enthusiast to just show up at our office? He came not just he came like came with entourage of his father and his grandfather we all and they all tracked out to to Northern Zealand in Denmark and showed up at our tiny little office and it was cozy and Morton was there and we had a blast all day long

00:16:19 [CH]

Wait, this this is like the coolest story ever you just decided to do like a Some kind of mini trip to visit the the Dyalog headquarters and you showed up and got to meet.

00:16:27 [AB]

That wasn't our headquarters though. We have two offices one in Denmark one in in England and people in general are welcome to come visit the English office probably a bit more interesting than the Danish one but they Brian came to Denmark and he came visiting. It was very nice.

00:16:41 [CH]

Interesting. So the HQ is the one in England, I've always assumed because a lot of the past user meetings have been in Denmark, I think or at least I've seen videos But interesting.

00:16:53 [ML]

Yeah, I don't think there's a good venue that they have in England, I don't know why.

00:16:58 [CH]

It's also way way more expensive going to England than it is..

00:17:01 [ML]

Yeah, very much.

00:17:03 [CH]

Anyway, so you hop over to Denmark and You're showing Adám. You're you're attempted bit of a glitchy game, but it's it's you know.

00:17:12 [BE]

Yeah, I was in Denmark for family reasons but I thought why not visit Dyalog because I mean I had the idea and then I talked with Adám about it and he was like fine with it and I talked with my dad about it and it's fun and then we just went It's great And he was Adám had to help me with the train system because I did not know how to travel through Denmark trains

00:17:34 [CH]

It's funny when you first said that I was like What you would talked about combinators on your first visit, but no, you meant like actual trains. [04]

00:17:45 [ML]

Yeah, they're not they're not the easiest thing to figure out but they're not terrible.

00:17:49 [BE]

Yeah, no, but I've never been a train before there's no train system in Faroe Islands.

00:17:55 [CH]

Oh, oh, yeah that that checks out Yeah, so it would be a pretty Confusing thing for you know first time.

00:18:01 [AB]

So you were one of the few people who did APL trains before you did you know railways.

00:18:07 [BE]

Yeah after that awesome time with Adám showing off my game I realized that my the project for that game stopped since the window system Definitely wasn't made for 60 frames per second games because It starts flashing at 60 with you try to refresh it that often, right? Because I assume it was just made for windowed applications. Just normal just normal GUI applications, but okay, that's fine I think I'll do some other projects. My discord bot is my other project that I work very hard on and Then I talk in That I found out the APL discord existed. I didn't know that for a long time Oh, wait, no, I this was way before I met Adám, but that's fine

00:18:52 [ML]

I think you were. You were on there pretty early. It had been only it had only been around for like less than a year definitely a few months.

00:18:59 [AB]

I think I remember you exclaiming in the APL orchard something like oh, wow the discord.

00:19:05 [BE]

Yeah, because I was very active in discord and I was amazed that there was a community there. I then talked with Dzaima once about how I'll beat you in the school and then I decided to try it and It was a very very cool At first I just tried it. I put dip my toes in and then I kept working with APL and Python Oh and my discord bot is in Python just so yeah, that's cleared But as I did more and more bqn I had very I had tons of fun with it And then I found out Raylib was a C library Which is very functional in nature like you can just there's no state in it it's just great in that sense and I tried linking to it sometimes actually I saw an example in the discord on this and I then Twiddled with it a bit and I just made a standalone library and that's when I started with Rayed BQN.

00:20:03 [CH]

So you were in the Faroe Islands you end up visiting out of in Denmark You're playing around with the APL on the windowing system reaching the limits there You find the discord you see an example, and then that just inspired you to Try and build a library and then here we are today you are oh That's fantastic. I mean there's a bunch of things I could ask and we could and I know I think Marshall You have a couple directions, but you know I'm always curious especially because it sounds like I'm not sure when you visited Denmark But it sounds like you've been like how many years have you been playing around with APL and BQN.

00:20:36 [BE]

About two years and 1/2.

00:20:38 [CH]

Okay, and what is it that you know you said you've had you've tried to convince friends, and they're just not interested Are you just special and like you have a fondness for them like because there seems to be you know? I've heard on different podcasts from different folks. You know some people they immediately fall in love with the language other folks They kind of bounce off of it other folks. They think it looks weird. You know what is it? Do you think about the languages like I know you talked about how you saw the the plus reduce and that was it you know? You just you saw that it was is that it like just for some people There's a spark or something that happens and other folks just don't have that spark.

00:21:11 [BE]

So I hadn't learned Python very long I've only been using Python for like one month max, and I've been using JavaScript for maybe two months I think a huge part of it was I wasn't introduced to any other language That deeply I hadn't you know I hadn't locked my brain in with that right So I think when I saw the language and just how easier how much easier was with what I was doing Just playing around writing scripts. It seemed like a much better language for my for my use case and the beauty in in the expressions also caught my eye a lot and that motivated me to just yeah, I wanted to work with this and.

00:21:54 [CH]

So the key is we got to get we got to get folks before they've been corrupted by by big by big Python.

00:22:01 [AB]

Yeah, I think I think that is really true. I'm teaching a lot of people APL on all kinds of levels, and I can definitely feel the difference when people have a CS degree, then it becomes very difficult for them to grasp it here, even with the best of will. Right not talking about them. I don't think it's a it's not because oh, they've seen something else and they Can't relate to this thing. It's just these patterns and the way of thinking it's just been Settled in some odd way that makes it hard for them to grasp how APL works.

00:22:35 [CH]

Alright, Marshall, I know I'll throw it over you for a second. I know that you had a couple of couple things that you wanted to make.

00:22:40 [ML]

Yeah. well I was saying now that we've gotten introductions out of the way we could do a little segment on Advent of Code since most people here have at least interacted with it in some way. We're currently on day five, which is really just killing everyone as far as I can tell. [05]

00:22:57 [CH]

I literally have part B running in the background and I know that that's not the way you're supposed to do it But I'm like we got to record this for like an hour an hour and a half like my brute-force Solution on part B may or may not actually provide me an answer in 45 minutes so stay tuned folks..

00:23:14 [ML]

Which language is this?

00:23:19 [CH]

This is in Python I've done all of them in Python and a little bit of APL and BQM I will say to not to actually keep going I'll save my remark for a little a little bit.

00:23:26 [ML]

I didn't have anything else to say I was just introducing the topic.

00:23:30 [CH]

Okay, perfect, then I will insert my remark Well, so in general we will leave links I am assuming most folks have heard of Advent of Code, but in case we have a new listener that just entered the programming world. Every year in December from December 1st to I believe the 24th or 25th. There are problems every night at midnight EST so that's the New York time zone and Some of the very fast people will compete like because it's time based And if you get in the top 100 on any day you get like 1 to 99 points depending on you know How quickly you solved it most folks do it sort of just for fun at some point over the next couple days and In general, it's a super great way to learn new languages. That's what a lot of people use it for I know my buddy He's doing it in both Python and Haskell to learn Haskell So the Python is usually not too bad and then Haskell takes a bit longer in years past It usually starts out quite easy. I remember last year my goal was to do it in Rust But then the first problem was like you're given lines of integers Calculate the maximum of each line and then the sum of all the maximums and I was like, all right Well, I'm not doing it in Rust. I'm doing this in APL or BQN because it's like it's four characters I'm not gonna write like I can't even write a single Rust function in the amount of code It's gonna be for the whole BQN or APL solution this year though I would say I don't know what's going I don't know if like because LLMs and chatGBT came out They're trying to make it more difficult, but it's been like Way way it didn't it was not an easy on ramp. I thought day four was the easiest The one remark I was gonna make is though I found that BQN I I miss so much and I actually saw on Twitter someone posted an str dot NATs function So maybe there's a library out here that I can get the answer to is there like a parsing thing out there? Because I dearly miss in APL the partition functions because BQN sort of got rid of those and replaced them with group Which for doing things like space separating? I don't know the idioms for I'm sure there's a way that is only a couple characters more But like for APL you can just do the not equals partitioned identity fork with a whatever your delimiter is on the left and Also, it is very nice in APL that you can just go You can call the evaluate glyph if you have a string of numbers And then it'll just turn that into an America ray, but in BQN because it doesn't use spaces for Stranding it uses the underscores you actually have to do something where you split and then turn those in so like in APL It's literally a single glyph to take a string that is just integers and turn that into a ray And so at one point I solved it quote I quote-unquote solved it in BQN by pretending I had these two array functions and like Str dot you know ints functions, and then just wrote like the expression code, so anyways. I'll let Marshall respond if if there's any resources for folks that are trying to do an in BQN and are missing the partition function or the evaluate function What do people do and I know this is a pretty specific way to start our Appendix code discussion, but? Answering my questions first not caring about the listener here.

00:26:36 [ML]

Yeah [chuckles]. Well I can answer. I mean one reason to go to do this section is because I think a lot of the listeners will be wondering the same things, having the same difficulties. So there is in BQN now, we added (probably in the past year) a ParseFloat system function. If you have a single integer that'll work just fine. I mean, it's not long (like it's a reduction in BQN) to get the value of an integer from the digits. But also you can [now] just write ParseFloat. For strings with natural numbers, I don't run into this because I don't do things that require this sort of parsing really (well sometimes but not often). In the BQN libs (which is my kind of libraries that I wrote for BQN), there's a function called ToNats  so it'll take a string which is just digits and anything at all in between them and it'll pull all the natural numbers out of that. So if you've got "123#*45", and you call it on that, you'll get 123 and 45. So that's what I use; it's like a two line definition, and there are a lot of other ways you could write it. Basically yeah, it doesn't have this built in. I mean you could also just replace the spaces with the ligature character for stranding and evaluated as BQN, but there's nothing as nice as APL's evaluate, which I kind of view as a good thing because [chuckles] I don't want people writing eval everywhere in their code.

00:28:08 [CH]

It is a cute trick that is specifically helpful for this kind of [chuckles], you know, Advent of Coding. It doesn't come up, you know, in the real world [Marshall agrees] that commonly. Adám?

00:28:18 [AB]

I don't participate in Advent of Code but during December, I get a flood of questions as to how to do various stuff in APL [chuckles]. And this is one of them: you get these rigid data formats as part of the problem set and you need to parse in, not just numbers but in general to parse it because they are fixed width or because they're delimited somehow. And something that Dyalog APL has a lot of, are these fancy system functions that do huge jobs for you and in particular, a relatively new one is quad-CSV (which is the CSV parsing thing), which can do so much more than the classic CSV. You can pretty much use it to parse anything, including say space separated, literal numbers in a string. You can just throw that at it and I think we should include a link in the show notes as well to a video that I made that shows how to parse a lot of different formats using this and all the options that it has. So even if it's a bit too cute to just use execute in APL, there are actually good tools there [Conor agrees] that'll safely convert.

00:29:30 [CH]

For doing it the right way. Yeah, I will say that at least (I mean maybe Bob you can add for J), but the quad-NGET is the main thing I use in APL and BQN has a system file dot read lines (Here's the BQN code: •file.Lines) which is super nice. That's basically where you can get started for those two. And if you're using VSCode, (I don't know how you guys have done this) but the BQN plugins are fantastic, so much so that you basically get the same experience [as] if you're on BQNPAD or Marshall's version on his BQN site. Like the backslash will automatically convert. I did not need to install any kind of keyboard. Whatever their plugin is when I'm at a BQN file it just knows: "oh, we're in BQN land, and it can do the glyph creating". And it also has autocomplete; when you hit the system dot and you start typing it autocompletes, which is fantastic. Kudos to whoever did that. I'm not sure if it was you, Marshall or some person out in the wild.

00:30:32 [ML]

I think that was all Ragu.

00:30:34 [CH]

Yeah, fantastic work there. like I know I've used the Optima or Optiva (there's a APL plug-in)  and I think also 2you  (the BQN one) has like font recognition, and maybe I just have the right fonts or whatever. But anyways, I've used the Optiva (if I'm pronouncing that company's plug-in correctly), and it's pretty good, but it doesn't have the autocomplete and I don't think it, by default, has the conversion into APL glyphs. Anyway, so for folks that are trying both out, there are plugins. Check them out and BQN is particularly good. Bob, I don't know if you want to hop in with ... for folks that want to do this in J.

00:31:07 [ML]

What font should people use for J? [everyone laughs]

00:31:11 [BT]

I think you know any fixed width font is probably fine for J. I mean, ASCII.

00:31:17 [CH]

Wow! That can't be the case!

00:31:18 [BT]

That's all you need.

00:31:20 [AB]

How do I type J again? Do I need like a special keyboard?

00:31:24 [BT]

Well, let's see on the keyboard, it's right between the H and the K as I'm looking at it right now. So right in the center there. In fact they put a little bump on the keyboard for the J, so you know where your fingers are. It's really, really easy to find J, unless you're searching for it.

00:31:38 [AB]

Oh, the way I find J is I find A, P and L, which are obviously easy on my keyboard and then just find the midpoint between them. That's where J lives.

00:31:48 [BT]

Okay. That's a very spatial way to do it [Conor laughs]. It's a very special way to do it. Anyway, yeah in J generally what I do is I just load the file down and then, in the past all I've done is created a noun with that in there. In the process of creating the noun I can take out line feeds or do whatever else I want, to make it into a form that I can actually work with and quite honestly when I did Advent of Code in the past, that was usually a good quarter of the job, was to try and figure out the format they actually wanted it into so you could work with it. [Conor agrees]. Once you got that done there was other stuff to work out, but what we felt the stumbling block was often trying to figure out getting it into the form, which is just creating a noun.

00:32:38 [CH]

That's the counter (I think that was day 2, the one where I use the Python counters). Both of those are technically one liners (if you format it, two liners), but the majority of that problem is that it gives a card, some "word:" and then space delimited [strings], with commas and semicolons, representing two to three different bags . So you have to split like three times, first on the colon, then on the semicolon [and] then you have to remove the commas (because the commas only exist for the n-1 colors). Then you need to split on spaces, and that's why I've never done Advent of Code to completion because usually that kind of problem (like that day 2 problem) that shows up around day 9 or 10 because that's when I'll give up. But when I saw that that was day 2, I was like are: you kidding me? This is why people don't like [it] at least for me. I love the calculation part, using a counter, calling a sum, calling a product, a reduction or whatever. But this parsing garbage, no one's having trouble doing this mentally. It's just a pain to get it in the right format, and if they did like every other [site like] leet code [which just] gives you the function and the list of values ... [sentence left incomplete]. They don't say: we're gonna make you parse stuff for 20 minutes and you're gonna have 20 lines of code. Anyways, off my little soapbox here. I wanted to ask Brian because I know when I was checking out your github, I did see that you had an Advent of Code for, I think, 2023 so have you done any of the problems in BQN? I think Marshall even said you might have been trying out Singeli this year.

00:34:13 [BE]

I have done one problem in BQN this year. Last year I did I think six parts. The Singeli part is fun. Singeli is a fun language. It's like, you know, zig comptime. It's like that, but on steroids.

00:34:28 [CH]

Okay. [laughs]

00:34:29 [BE]

You can write C in-line, and it just sometimes works and I'm still getting the hang of it, but I would say it's a super cool language. I can imagine it being useful for well, optimizing code since it's made for optimizing BQN. But it would be really cool to like use it in game programming even for having really a performance sensitive parts of the codebase being in Singeli. That'd be super cool. I'm thinking about it. I'm not gonna do anything with that for at least a few months.

00:35:04 [CH]

Interesting. So you've said you did one in BQN and have you also done the same problem in Singeli or have you done a couple of them in Singeli this year?

00:35:12 [BE]

Oh, I haven't even done one. I've just been playing around and then in my free time I've been preparing for actually this podcast. I've just prepared some notes.

00:35:22 [CH]

Okay, well if you've got things on your notes that you want to dive into right now, it's a great segue. [laughs]

00:35:26 [BE]

I first want to give credits. My first example that got me into making Rayed BQN, was made by "no data ma"  which is their username. You can probably find them on discord. I like [give] so much credit to them. It's great.

00:35:41 [CH]

And so they were just the inspiration. That was the example that you saw that led to you creating the Rayed BQN library?

00:35:46 [BE]

Exactly. Yeah. It was also when I started playing around with it, that's when I started making games with it and I just got hooked. Then also credit to Dzaima for helping me so much with FFI and being patient with me because I've asked for help so often. I didn't even know C before I did troubleshooting with FFI.

00:36:08 [CH]

Wow!

00:36:09 [ML]

And of course, we're very glad to have [chuckles], you know, somebody test it out and say: "I need this, I need that", to figure out what parts work and also what sort of libraries we need to get it to connect to because the choices you make with that foreign function interface really depend on what sort of stuff you want to do in C. Like what you want to connect to.

00:36:27 [BE]

The FFI system is incredible. Like once you get the hang of it, it's very, very nice to use. Another thing I would like to talk about is my idea of why would you use Rayed BQN right? Because usually for games you want to use some typed language maybe. Some safe language. But I love BQN since it's a lot less complicated. A lot less variables floating around. A lot less mutation and honestly, I haven't actually used mutation in all of my examples thus far. Even my snake game and stuff. I always give the state back to the next loop. So I keep it very functional and I do that very intentionally because I don't like states and I really want to limit amounts of variables and if I have an array of positions, I want to keep it in one variable and mess around with that.

00:37:29 [CH]

You know I technically I studied a bit of computer science in university but I didn't really discover functional programming as a paradigm until 5 years after ... [06] [sentence left incomplete]. After graduating and taking a number of CS courses, I worked. I technically wasn't a software dev but I was still writing code and then I went to my second company and it was there that there was a Haskell study group and so it was because of that study group that I started learning about functional languages. But you've seemed to like speedrun all the paradigms and like [chuckles] find array languages and you're doing it in this functional way. I now code very functionally, you know, small functions, minimizing state change. So, how did you end up at what I consider the golden way to program, so quickly? Was it just watching stuff on YouTube and seeing the different styles? I didn't even have the awareness to like know what a paradigm was at the time.

00:38:22 [BE]

So it was when I did Python. I always wondered why the syntax was so weird when working with some libraries. I worked with a window library actually in Python and it had classes and you had to do stuff with them and you had to like define stuff in them and it was like it was unintuitive to me. And then in APL it was just it's like: why don't people just use this kind of system where you just have a function. It does one thing and it just does it. When I asked for help in other places with the system, when they talked about it, it just seemed to make sense to them. Not for me. No. It always seemed like magic. Especially since some classes do stuff behind the scenes and I never liked that and especially when I learned that Python does, what's it called, metaprogramming with the classes sometimes. You make a meta class, it's called, and stuff like that. It was a mess, I would say. And then just going back to the simple ages of just using functions [chuckles] I like a lot more.

00:39:31 [CH]

So it's literally just style and preference [Brian agrees], like you just didn't like the way it felt. You discovered very early that there was a different way to program. So yeah, like we mentioned before you hadn't been taken to the dark side.

00:39:44 [BE]

I did actually learn APL before I knew what functional programming was. So I would say I was already a functional programmer before I knew what it was [chuckles]. It was just how my head worked I think and I got used to it very quickly and then when other people do object-oriented stuff I puke [Conor laughs] because: just use functions. It's simpler. Look at this. And then I give an example. It's like lots of lines shorter. Isn't this way simpler? And they're like: "no, it's a lot more complicated" [chuckles]. And I don't understand.

00:40:11 [CH]

Yeah. I was looking at the Kap implementation, [07] several weeks ago in Kotlin and it's I think the only APL implementation that I've looked at that is done in a class-based, inheritance kind of way. And I was trying to make some small change and I gave myself five or ten minutes (time boxed it), and I was not successful in making that change [chuckles]. You can do some powerful stuff with inheritance systems but I agree that if you can just stick to the small functions, separate concerns, not inheriting from everything (a dog is an animal, a cat's an animal, blah blah blah). I'm like you. I prefer the functional ... [sentence left incomplete].

00:40:55 [ML]

Yeah, Dzaima's Java implementations are also, I think, done in a pretty similar style. They have lots of classes and stuff and utilities that are in this or that class. Yeah, I think I probably had a similar thing with the changes I needed to be making in Dzaima BQN. It felt like everything was kind of hidden. Like this thing is defined in this class and you use it over here. And it's not always obvious what's in between those, I guess.

00:41:28 [CH]

So wait, Dzaima has two different implementations BQN?

00:41:32 [ML]

Yeah, so Dzaima BQN was not around for the first year or so of BQN, and I've never done like a real implementation [chuckles]. But the way it worked was first I adapted Nikolov's ngn/apl to use with BQN and then I worked on the self-hosted aspects of BQN. In parallel with that Dzaima (who was on the BQN team from the very first announcement that BQN was going to exist) converted his Dzaima APL to be BQN and so I started using that instead of my old JavaScript thing as a way to run the self-hosted code. Then for a while, I was working with a hybrid with Dzaima BQN, but that didn't have all the functionality implemented in Java. So there was some BQN code on top of that and then later he made the CBQN that we're using now. It uses the BQN compiler, of course, but it also has some of the runtime stuff for things that aren't implemented in pure C, or Singeli.

00:42:40 [CH]

Interesting. So that means that Dzaima APL, which was the predecessor to Dzaima BQN, is also in Java. Assumably. [Marshall agrees]. Interesting. I did not know that. Wow. And so Dzaima is this polyglot, just knows all the languages? What does he prefer Java to C or ... [sentence left incomplete]?

00:42:58 [ML]

He knows a pretty good number [chuckles]. Yeah, he likes the look of Java he said and I guess he is, or at least was, pretty used to object-oriented programming.

00:43:09 [CH]

Interesting. An array programmer that likes the look of Java. I've never heard such a confusing statement [laughs].

00:43:18 [AB]

It does have the benefit though that Dzaima APL is as far as I know the only APL implementation that runs natively on Android. That's actually available. Dyalog can run on Android but nobody can get their hands on it.

00:43:31 [ML]

Yeah, I mean, so can BQN.

00:43:32 [AB]

Yeah I know J [08] can run on Android, but it's not APL in my opinion [chuckles].

00:43:40 [BT]

[laughs] We shots fired! To bring this back around to games because actually I think there'll be something mentioned in the title about games, Brian and I were talking, setting this up and Brian you actually mentioned that there was a number of areas that you thought array programming hadn't ... [sentence left incomplete]. Essentially the paradigm has some advantages when it comes to making games that you don't think have been exploited or investigated maybe as well as they should have. Do you want to tell me about that?

00:44:12 [BE]

Yeah I love array programming with making games since if you have a bitmap, then you just apply it. If you have a Coordinates you just input them; you map with the drawing function and stuff. One thing that I like a lot is using the last axis stuff with making code a lot more readable. I played with rank a lot and at one point it was very complicated. Like I had to do so many transposes and switcheroos and stuff and then I decided to switch some stuff around and I decided to make the coordinates array be layer by layer instead of column by column. The benefit of it being row by row is that if you add two numbers (two coordinates), to a list or to an array of coordinates it just maps right away. But what I found is that it's a lot more intuitive and a lot nicer if you bind the two numbers with an addition and then using cells modifier and bqn to map to each row and this removed so many transposes and stuff from my examples. It's amazing. It's because of how the layers are like nested arrays, so each row is like one nested box and using cells just maps the addition to the boxes and and this was a lot better since if you map, let's say [an] array of booleans on [an] array of coordinates you just filter with the slash in bqn and it works. That's the biggest breakthrough I had, I'd say. Some other stuff I've been experimenting with is using modifiers a lot. One version of the model was where I had for example a modifier that was called "apply" and then you give a function and then you use the "under" transformation stuff. Just nesting modifiers to make it so that for example an addition is relative to the camera and stuff like this. I just, you know what [said] screw that ... modifiers. I even talked, in discord, with Marshall and Dzaima and they both said: just use functions [chuckles] and I decided to just remove the modifiers and just use functions, and it's a lot easier. It became a lot simpler. Modifiers, use them sparingly. That was the one lesson I learned.

00:46:59 [CH]

When you say modifiers here, are you talking about user defined ones like you're writing your own modifiers to do fancy stuff and that just becomes a bit tricky?

00:47:07 [ML]

And these would be APL operators and J verbs and conjunctions for other language people.

00:47:11 [CH]

Or uiua modifiers. I think the array community ... [sentence left incomplete]..

00:47:15 [ML]

Oh, yeah I forgot to say I mean uiua is the language to do Advent of Code in this year. There's a ton of people doing it.

00:47:22 [CH]

Is it? Yeah, it makes sense. I really wanted to do it in Jelly, but I can't figure out how strings work [laughs]. Bob you were gonna ask a question as well.

00:47:33 [BT]

Well, I was gonna stay on the game topic. Does that change the types of games that you tend to write? Are there some games that fit better to into that paradigm than others or is that just sort of a very foundational basis for writing games in APL or BQN.

00:47:51 [BE]

Yeah, whenever I start making a game I always go with a grid based game because those are always fun to do with array languages like minesweeper. I recently made a new minesweeper example and also snake, stuff like that. I haven't actually done any big games that have a non blocky kind of look, you know what I mean? So I always pick an array-oriented thing since I think that will be the most beautiful Implementation. So I'm kind of biased but I would say that if you use this for another game that is non blocky, I think it would be super cool and maybe it wouldn't be as beautiful. But it surely would use array programming a lot with with the boolean maps and stuff to do conditional logic.

00:48:47 [CH]

Yeah, I mean, the game that I am going to, at some point in my lifetime [laughs], write (and probably we'll use a Ray BQN) is Scrabble [09] which unfortunately is a tile based game, but I think it's interesting because the data structures behind storing your words in a dictionary (they use something called like a trie) you basically need to do that. I think trying to represent that in an array language will be interesting because I always wonder the things that array languages are good, they're amazing at them. But then when it comes to things that, it's not their bread and butter, are they still pretty good; can you get pretty far or does the language fall over? I'm not enough of an expert to know. I'm sure Marshall would say you can definitely do anything [chuckles]. You've done tons of array programming in all the languages.

00:49:40 [ML]

Well, so a trie (and this is T, R, I, E)?

00:49:43 [CH]

Also known as a prefix or suffix tree.

00:49:46 [ML]

I mean, it's really just made of arrays, right? Very few languages would have it built in, so it's just like at each layer, there's an array of things. I think the problem that you'd get is that ... [sentence left incomplete]. I mean for a read-only trie array, APL is just perfect because you set up the arrays and the arrays contain arrays, so it's one big nested array. But if you want to add things to it, then you kind of want mutable arrays and I think it would be fairly hard to get it so that so that you can do all the updates properly. Like in BQN I might want to use objects for it. You can kind of make a wrapper object around an array and then the object is gonna be the only thing that knows about the array so it can mutate it whenever it wants. In that way you sort of get a mutable array. But then it's an object and it's not an array, so you can't just like select elements and stuff. So I'm thinking that wouldn't be as nice if you need to mutate it.

00:50:43 [BE]

I would say, why not make a zero padded array and mutate a point in the list?

00:50:52 [ML]

Well, it's got to be nested so like it is a tree structure where like generally the idea of a trie is that at each level like the levels correspond to two elements in the thing that you're trying to look up So the first level you use as like an index into the first the first element is used as an index in the first level of the tree and then the second into the next level and so on and so like if you need to start updating this then you've got to be updating a nested array and you have. Like that that update has to be has to come up come through the whole nested structure So...

00:51:26 [CH]

I mean the good part is is that for a game of Scrabble you definitely don't need a mutable trie because you have your 100. It's just a 178,000 yeah word list.

00:51:37 [ML]

Ohh, it's just the word list is you just make one on the whole word list. Yeah. So you're probably pretty good in any.

00:51:42 [CH]

Oh, it's just the word list is you just make one on the whole word list Yeah, so you're probably pretty good in any array language Yeah the confusing or the unclear part for tackling like this kind of game is that or this kind of aspect of this game is is That you need ways to like traverse like the way It's designed in Python is it's just like a class with a bunch of methods for you know going backwards forwards. Checking whether it's a valid word at this point or a suffix or whatever. Which is Very useful in terms of like you don't want to do a full search Every time you're trying to generate word possibilities You just want you want to search what's possible given your tile rack and what's on the board and if you try and do it Exhaustively your program is gonna screech to a halt. And so I I think I guess you would end up building this trie with nested arrays of nested arrays and Then you would just have some pre functions that like given some information is able to like Traverse the trie because like they kind of do it by like pointer chasing and stuff in Python.

00:52:39 [ML]

Yeah, well, I mean traversing a nested array It's just like all right pick the first element of the second element of the third element of this array So that's actually really nice in APL.

00:52:49 [CH]

Yeah, well time will tell I will Brian you're gonna say something.

00:52:54 [BE]

May I so I want to talk a bit more about what I do in rate BQN with with types since what I like to do is use integers and and Less floats because BQN does this where it optimizes the integer down to the lowest Type (hopefully) some well you have to cast it. Well, you have to make sure it does that with a System function but Usually BQN and figures it out and I do this with images Where I tried to and then I realized that beacon doesn't optimize for unsigned integers. So I have to wrap them to be assigned integers with like modding by Yeah doing some funky stuff to make it within that range but it's a fun thing since if I make all the stuff intuitive with like making images and using functions with integers really intuitive and. You can do some stuff with integers right since coordinates are also integers. You can eventually like optimize it pretty well, and I feel like it could be It could be very useful to have actually an Optimized game with BQN, but I'm not entirely sure since it's very hard if you want to compete with like C++.

00:54:16 [ML]

Yeah, well, you're stuck on the CPU is the big thing until. Until somebody comes along and does the GPU thing and you're not but so you don't have access to quite the same capabilities But CPUs are still very fast.

00:54:29 [CH]

So what are there other recommendations? It sounds like this optimization thing. You're kind of playing with right now What would you if there's you know folks that are listening to this? They've been wanting to get into game programming and you've now built this, you know rayed-BQN which sits on top of Raylib. What's like the you know, what would your recommendation be? Because I know you have I think a set of like 10 or so Example games that you've written and it's just in the examples like sub directory of the github repo. So obviously, you know the link will be in the show note for folks that want to go check it out, But what would your recommendation be for folks that are trying to build their you know. First game using rayed-BQN like is there a Golden path to you know, maximize odds of success on sort of folks first run at this.

00:55:13 [BE]

I would first of all, you have to follow the instructions on installing it, of course. Get one example to run and then what I would do is playing around and just modifying tiny bits of the code maybe make a snake in the snake game move faster and make Make the arena bigger or and then go to more complicated stuff. Like maybe Well, like draw extra stuff on the map like instead of berries draw Draw blueberries or add more types of berries that they give power-ups and stuff. That's that would be my recommendation first and then afterwards you can try starting up your own game by copying an example and just pasting it in and then removing all the codes that Is the logic of that game and then you have a bare-bones Nothing in it. And then you just you can look back in the examples and stuff and then you just give a tiny tiny adjustments and then you draw stuff to the screen and then you make your game and Hopefully there are no issues and you can always report an issue because I see them as a to-do list. I'm very happy to see an issue that I can solve.

00:56:24 [CH]

Awesome, and this might be a question for David who I think is gonna be a future guest if not future very soon to be Guest because in one of his videos it looked like he and I think I asked Marshall this and Marshall see I don't know You'll have to ask You know either David or potentially, you know the answer Brian. He looked like he was doing some kind of Like hot reloading like he had some screen open and was making live changes, but like he was switching Workspaces or whatever or monitors so like you couldn't actually tell was it just the way it was edited. So it looked like it was like a hot reload. Meaning that like I don't need to relaunch an executable while I make changes. Do you know if that is what he was doing or that if that's possible because that's such a cool way To program like a snake game if you see like a canvas that's empty you make a code change you hit save and then like it. Automatically refreshes without having to launch anything.

00:57:14 [BE]

So he didn't use my hot reloading though. I have designed or made hot reloading he used what was it no, he just used editing, but I when I did implement it, I realized it doesn't work when mutating variables because the the hot reload is very simple and it just imports functions from a main file and and reframe work Mutates the functions with the new functions from your work file I don't know if that makes sense. Hopefully it does.

00:57:47 [ML]

So like you might have leftover state that doesn't make sense anymore or something like that.

00:57:50 [BE]

Yes, exactly But if you have variables defined outside the main loop Then those would get like either redefined at the every hot reload which is a few every few seconds when it checks and then you edit the code and then it refreshes it which means that you can't use mutation at all with variables outside the loop function or the per frame function. Also something I should note is that I don't have any async capabilities just yet. So any games that requires that does have limitations.

00:58:28 [CH]

I'm not enough of a game programmer to know if that's like a very limiting thing.

00:58:34 [BE]

It's not you can make basically any game with just per frame a function activating per frame.

00:58:40 [CH]

Well good to know in case there is someone in the back of their head thinking Of a very specific type of game that requires it. Yeah, I mean I feel like we've skipped around from topic to topic to topic we've gone back and forth from Advent of Code to Rayed BQN to You know for some reason prefix trees. Are there any other kind of topics you know things on your you said you had some notes or things you wanted to make sure that you got to or questions from the other panelists of Yeah, we have we have a library implementer here. So you know.

00:59:13 [BE]

One nice thing about BQN I can talk about is how lovely it is eliminating abstractions. That's also part of the raylib Philosophy as well. Because abstractions get in the way a lot although of course Opening window that's a good abstraction, but when you have these. Just you want to move the position of the camera. Well, just add the camera position by one Let's just do a plus one and then it moves at one Bottom well one down at one right since you add both coordinates. It's simple and I love it it removes the abstraction of moving camera relative to what and stuff like that and turning is also just multiplying the the degrees of the Camera well the camera nested array since oh yeah also I turn the structs from C into just nested BQN arrays and. Well, sometimes it's pointers, but I'll see if I can turn those into normal BQN arrays later. You can just modify a variable in these structs and it just works. It if you give it to a C function since reloop doesn't hold state It will just accept it and then run it even the font stuff if you might if you get a font from reloop and Modify the images in the font it just works, and I love it.

01:00:38 [CH]

Huh, so it sounds like there's a whole category of like what would be methods and some other library for doing rotations or scaling. Which are basically like, yielded obsolete or unnecessary because it's just a scalar operation on on vectors at the end of the day or matrices.

01:00:54 [BE]

And also something I would like to add is in BQN you can Generalize so much so if you have a math library for example in raylib it has Ray math dot C [10], and I just copied it and translated the entire thing is like 2,000 lines to BQN and I then after doing that which took like a few days I Generalize some of the functions for example if there was function that did vector 2x and Then vector 3x I just made them both work on any vector of any size. Yeah, that was very I was very happy doing that because it's very satisfying just make generalizing all the functions. Also, raylib always uses 4x4 matrices But ray BQN can use any size matrices because the ray math library That I've made in ray math of BQN it supports any size matrices for any calculation with the math library. Which is awesome super cool.

01:02:00 [CH]

Out of curiosity how many lines of BQN did the translated 2,000 lines of the math dot C? Code end up being.

01:02:08 [BE]

I'll have to double check give me like if you'd like to give me a minute Maybe someone else can talk.

01:02:13 [CH]

Adám. What's up?

01:02:14 [AB]

Well to fill this time. I thought I'd mention something interesting and going back to this Advent of Code thing and. How do you win so to say at the record. How do you consistently get on the on the first spot every year. There's one person isn't it. No Is known under the name betaveros. I think I'm not sure how to pronounce that. Who consistently places first and The way this person has done it is by making a programming language specifically to speedrun Advent of Code. Kind of similar to how Jelly is made specifically to win code golf challenges on average and this person has written this blog post about the design of this language and if based on that I can say with confidence that this person is at least somewhat familiar with the APL language family, so maybe there's something to it.I just thought that was interesting.

01:03:15 [CH]

I did just check to and my my Python program still running. And It is updating the minimum location This is for day five for those that are you know if there's listeners that also struggled with this. So it's it's just I'm printing the minimums constantly and then every once in a while it changes because it finds a new one, but the the current minimum that it's at Is not the correct answer. I think I've checked like three or four of them So we'll just you know, maybe we'll just let it run forever and on day 12 of Advent of Code It'll come up you know. All right Brian still he's still, He's still searching.

01:03:50 [BE]

I found the raylib file, and I now found the BQN file so without removing any comments which there are a lot of The result turned into 550 lines.

01:04:03 [CH]

That's pretty good 75% saving.

01:04:06 [BE]

I saved 4x lines. Without removing any comments, so I think that's a win and the functions are generalized.

01:04:15 [CH]

There's many reasons why less code is better. Number of bugs per lines of code, but my favorite thing is you know the code the best code is the code that I don't Have to write. All right any last questions From our our panelists.

01:04:30 [AB]

I'd like to know where you see your future it goes to this whole array language Venture.

01:04:37 [ML]

Like a job interview.

01:04:40 [CH]

Yeah, Adám doesn't happen to be the the programming language lead at a company that may or may not have.

01:04:44 [AB]

We're not looking to hire anybody right now I'm generally curious because. I mean I had a hand in getting you started with with APL And I'd like to know is it even something that that people might consider continuing with even professionally Or is it just a toy?

01:05:03 [CH]

And to end to add on to Adáms question I don't actually think if explicitly it came up we we chatted about the fact that you're in the Faroe Islands in your 18. But what are you currently are you working? Are you going to school?

01:05:15 [BE]

One of them let's try First I'm from Yeah, Faroe Islands. I work at a company called Intra,  [11] but I haven't worked there for a while I've taken like a long break. But I'm technically still employed there. I am in school. I'm in Technician School of Klaksvik which is a technical school in the Klaksvik. I guess since class we get since Englishized I've I'm finishing my last year there, which is very exciting right and then the Adáms question was Interesting what was it?

01:05:52 [CH]

What is the future hold for the author of rayed BQN?

01:05:55 [BE]

I've talked with a few friends of mine of like do you want like my friends ask do you want to make a commercial like. Do you want to get money from it and like stuff like that and I don't know I haven't thought or I have thought about. It I just don't know how to get money from this type of stuff and I've always dreamed of like being able to program rayed BQN and Earning enough money to Buy What I need it's a it's a dream. I don't think I'll make it with rayed BQN since it's open source of course. I've dreamt about making a game engine with it. But that's like Probably not gonna happen But it's a dream right?

01:06:42 [AB]

Here's an interesting idea for you. Just it is definitely not why I asked you about this because I didn't have that in mind It's just something popped into my head now. At some Dyalog user meetings and even in one of the APL seeds that happened there's presentation by somebody named Thomas Gustafsson and and he has pretty much single-handedly made I think the only large if you call it game in APL or like commercial thing it is a ship and boat simulator made for training actual, you know captains to be to navigate through between small islands and waterways and open seas and then weather and so on and  it's used in really commercially like to train Coast Guard military Personnel zone. However, it's also clear that some of his technology stack. So he like you said Dyalog's windows GUI Capabilities are not made for this kind of thing. So he has some custom made 3D engine that he interfaces with from his APL code and then that renders to some through some Layers to actual something that looks like a modern-day video game quality But there might be an opportunity if this is the kind of thing you want to do. This is the actual commercial thing and he needs to replace some of those layers to be able to continue on what's in the future. Something more modern.

01:08:17 [BE]

That would be awesome. I wish I was that technical I have never messed with. Well, Raylib does have 3d capabilities, but it's a very low-level library, it doesn't have a well. Well, what doesn't it have? I guess it has quite a lot actually I could I could see that that thing could be implemented with my library, but it's a very It's a very huge Project in in my head. It's it's like you have to collect map data and you have to have ocean Graphics and stuff.

01:08:54 [AB]

Oh, no, I wasn't suggesting that you you clone his his product that would nope.

01:08:59 [BE]

Oh, no. No, that's not it either just talking about how like making something that complicated, you know and making it successful. Maybe I my if I made a product with my library It doesn't need to be that complicated or use that stuff. I mean it uses what it has.

01:09:15 [AB]

Of course I don't know what his requirements are how much he does in the APL side and how much is done But this library thing that but it I mean, you know APL fairly well I don't think he would want to interface with a bqn thing then to learn a new language for that but it might be something to look into and something at least in your Kind of area and and and this needed thing and something you might actually be able to make a living of.

01:09:42 [BE]

I Really. I'm looking forward to my future and see if I can get something to work. It'll be very cool.

01:09:48 [AB]

I can definitely put definitely put you in touch with him if you want me to.

01:09:52 [BE]

I would love to talk about it Like talk to him about it. It would be interesting.

01:09:55 [AB]

Maybe she'd get him as a guest here as well.

01:09:57 [CH]

I think he's on our he's on our I was gonna say short list our very long list of.

01:10:03 [BT]

Our increasingly long list.

01:10:04 [CH]

Yes, which I have we we are in a good position where our list grows longer. Or at a faster rate than the the rate that we interview folks But yeah, I mean, it's funny hearing you say that like oh, that's a seems like a daunting complicated endeavor coming from Someone your age that has speedrun through like most of the paradigms that I hadn't even heard of Like I was barely even a programmer at your age and you've already you know You're building libraries doing FFI stuff, you know, you're basically trailblazing. So to hear you say like oh that sounds a bit tricky There's a bit of irony in that because I don't I don't think you realize You know the the complexity of what you're already doing is is up there. So Yeah, I guess I'll say, you know, thanks for your work. I know Marshall is definitely appreciated of what you're doing and oh, yeah I hope that you know, I don't I don't actually know what the age distribution of folks are that listen to our podcast But I hope that if there's some younger folks that they're inspired to you know, maybe take a stab at building something like this whether it's in the FFI space with BQN or J or APL or uiua you know Any of the languages these days. Because and that was maybe that's a sort of a good anecdote to end on is that I think people underestimate how willing You know folks would be whether that's you know, Marshall and friends for BQN or other folks. I know in the C++ community some of the experts in certain libraries ended up becoming experts because they started building something and then they reached out to the current expert and then. They were helping out with what they were working on and because they are basically doing something to help out with their initiative. They end up getting all this like free mentoring and like, you know, basically like edge like free education So yeah, don't be afraid to you know, if you want to start building something you'd be surprised how willing it's like Oh, you're gonna build something for my language that I've created or my project that I'm working on People get really really excited about that like whenever anyone opens up PRs on my stuff and they've done work I'm like, well, you've done free work for me. Why would I not want to merge this? So, yeah, thanks for you know, all the work that you've done it's gonna be very exciting to see what you do over the next couple of years and. You know If you do have some big updates or new libraries that you work on. Hopefully we'll be able to keep in touch and maybe bring you on and a couple years or so. You know to get to get more updates from from the Faroe Islands Maybe you maybe you'll you'll have moved so but you know, we will we will discover in due time. Yeah, thanks for coming on. This has been a blast and I guess we have to throw it to Bob first and He will tell us or tell us tell the listeners.

01:12:41 [BT]

Well, we now have a correspondent on the Faroe Islands.

01:12:48 [CH]

So that's pretty impressive We need to start ask we don't do that I know other podcasts they ask their guests where they're at. Maybe we should start doing that and we should build a little map of all the different places Probably the Faroe Islands has got to be the uniquest place that we've although we've had a few people in Australia as well.

01:13:01 [BT]

I was gonna say Australia, you know, the time zones are kind of crazy with those things. But yeah

01:13:06 [CH]

But Australia has trains so, you know.

01:13:11 [BT]

And with that and with that we'll mention that if you want to get in touch with us, you can get in touch with us at contact@arraycast.com  [12] and we will have show notes on on this show as we always do and so if you want to get deeper into these things. You the show notes may help you out If you have questions, you can use contact@arraycast.com and we can of course. Forward any questions to Brian and thanks so much for being on Brian and I'd look forward to seeing what you do I think a lot of times when People are breaking new ground. The next step always looks kind of wild and confusing as Conor says what you don't realize is where you're living right now It's kind of wild and confusing to a lot of other people and the next step will always look that way so don't worry about that just keep on marching through and and see what you find out because. There's so much so many different languages. There's so many different things to discover right now it's quite impressive to if you've got the energy and the focus to be able to do these things. There's a lot of things you can do these days. So congratulations for for the library and thanks for helping out and all this kind of stuff for other people that are going to use your library to explore other areas.

01:14:23 [BE]

Thank you so much.

01:14:24 [CH]

And with that we will say Happy Array Programming

01:14:27 [All]

Happy Array Programming!

</details>
