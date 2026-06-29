---
title: "Episode 1: Why We Like Array Languages"
date: 2021-05-15 00:00:00 +0000
episode: 1
buzzsprout-id: 18621531
keywords:
- array-programming
- array-languages
mp3-url: "/assets/audio/episode0.mp3"
episode-type: full
explicit: "no"
block: "no"
layout: podcast
excerpt_separator: <!--more-->
redirect_from:
  - "/episodes/episode-00-why-i-like-array-languages"
  - "/episode1-show-notes"
---
There are lots of reasons to like the array languages APL, J and k/q! Listen and find out more.
<!--more-->

---


## Show Notes

- [Larry Breed (Wikipedia)](https://en.wikipedia.org/wiki/Lawrence_M._Breed)
- [No Stinking Loops - Stevan Apter](http://nsl.com/)
- [J for C Programmers - Henry Rich](https://www.jsoftware.com/help/jforc/contents.htm)
- [Consecutive 1’s Problem - ADSP Episode 25](https://adspthepodcast.com/2021/05/14/Episode-25.html)
- [Consecutive 1’s Problem - Bob Therriault YouTube video](https://youtu.be/lbi_PMVbeaQ)
- [LambdaCast](https://www.listennotes.com/podcasts/lambdacast-lambdacast-c8bseLqG1Eg/)
- [Arthur Whitney - by Bryan Cantrill ACMQueue](https://queue.acm.org/detail.cfm?id=1531242)
- [Shakti.com](https://Shakti.com)
- [I ❤️ APL and Haskell #2 - Conor Hoekstra](https://www.youtube.com/watch?v=a7CSK7HNEWQ)
- [APL](https://aplwiki.com/wiki/Learning_resources )
- [J](https://code.jsoftware.com/wiki/Studio)
- [k](https://estradajke.github.io/k9-simples/)
- [q](https://code.kx.com/q/learn/)
- [Stock Ups and Downs thread](http://www.jsoftware.com/pipermail/programming/2021-May/058201.html)
- [Aaron Hsu's tree algorithm thread](http://www.jsoftware.com/pipermail/programming/2021-May/058228.html)
- [Mastering Dyalog APL](https://mastering.dyalog.com/README.html)
- [APL Forum](http://apl.chat/ )
- [Course.dyalog.com](https://Course.dyalog.com)
- [TryAPL.org](https://TryAPL.org)
- [J](https://tio.run/#)
- [k](https://kparc.com/k/)
- [APL](https://aplwiki.com/wiki/Running_APL)
- [J](https://code.jsoftware.com/wiki/System/Installation  )
- [k](https://ngn.bitbucket.io/k.html )
- [Discord](https://discord.gg/yHna7nt7zx)
- [APL Campfire June 6th at 18:00 UTC](https://aplwiki.com/wiki/APL_Campfire)
- [Arraycast.com/resources](https://Arraycast.com/resources)

<details markdown="1">
<summary><strong>Transcript</strong> (click to expand)</summary>

Transcript

Transcript prepared by Rory Kemp

Show Notes

00:00:00 [Stephen Taylor]

I want to share with you a tiny origin story that literally no one else in the world knows. There’s an example there of a function being applied to a list of strings, cow, sheep, cat, dog. I’ve often used that list of words in demos and code examples, it comes from a school review in 1965. My friend was introduced, Michael Simpson will now say a few words. Michael walked up to the microphone and said “cow, sheep, cat, dog”.

00:00:34 [Music Theme]

00:00:45 [Conor Hoekstra]

Alright, welcome to the first episode of ArrayCast, a podcast about array programming languages and the array programming paradigm. My name is Conor Hoekstra, I’ll be your host for today and I think all of the following episodes, and we’re going to go around and do brief introductions with my three cohosts. We’ll go in the order of Stephen, Adám, and then Bob.

00:01:07 [ST]

Hello, I’m Stephen Taylor, I learned, I was shown APL a long time ago, hundreds of years ago I think, back in the days of timesharing services and teletypes, and I immediately liked it better than any other kind of programming I’d ever seen. I did my first email messages on an APL system, actually written by a guy I’m still working with. I became an APL developer, I moved on to other kind of work but spent 20 years ago considered I really hadn’t had anything like as much fun as I used to have coding in APL and came back to it. I’ve edited Vector, the journal of the British APL Association, and the last few years I’ve been the Kx librarian, working with the Q language, all part of the family.

00:02:01 [Adám Brudzewsky]

And I’m Adám Brudzewsky, I have been doing APL for pretty much all my life, and that means about a third of a century by now. For the last 6 or 7 years I’ve been doing it professionally, I work for Dyalog Ltd, mainly working on APL tools of various sorts and helping people, and I also do some teaching, create some teaching materials, take care of some social things.

00:02:31 [Bob Therriault]

And I’m Bob Therriault, and I’ve been playing with J, I’m not professional, I’m just sort of an enthusiast, and I’ve been playing with J for about 19 years, and I’m sort of active in the community, talked to lots of people, participate in conventions, those sorts of things. So um yeah I feel like I’m a little out of my league in terms of expertise but it’s a different language so that’s good.

00:02:51 [CH]

If you’re out of your league then I’m drowning. (laughs) So previously mentioned, I am Conor, I am completely different than your three cohosts, I’m a professional C++ developer, I work at Nvidia on a open source suite of libraries called rapids, which is basically focused on GPU accelerating data science. So I do no APL, or J, or K, or any array programming language professionally or you know, I jumped in to this a year and a half ago, so I’m definitely going to be the beginner on this podcast, asking the questions that hopefully the beginners have, and yeah so I guess the goal is that we try and get representation across three of the primary array programming languages, so Adám is representing APL, Bob is representing J, and Stephen is representing K, even though across the board everyone has experiences with these three different languages and other languages.

And I’m going to be asking all the questions, and learning just as much as the listeners, so I think the idea for today’s episode is we’re going to each spend three to four to five minutes explaining why we love array programming and/or one of the array programming languages and we’re going to go from there. So in the same order that we did introductions lets start with Stephen, and tell us why do you love the array programming paradigm?

00:04:12 [ST]

It’s a lovely question and I got asked some years ago to explain this one and I found it very confronting when I reflected on it, because I was forced to confront the fact that I don’t think of myself as a very serious programmer, although I’ve spent much of my life being paid to write code. I know guys who are like deeply into algorithms, and efficiency, and getting the most out of the iron, and none of that stuff touches me at all. When I reflected on it candidly, what I felt when I looked into it was I just love the way it looks, and that feels kinda dumb, but you see a really good program on the page, and I love it and I find that beauty more in the Iversonian languages in APL, in Q and K, a sort of conciseness, a correctness, and it’s the same kind of joy I get from a really good line in poetry or a really good piece of poetry that just effing nails it. And you look at it and you see that’s everything that needs to be said on that and it’s completely there. I get that experience in looking at a few lines of APL or K more often than I do in any other language. There’s that Leonard Cohen song isn’t it, “I came so far for beauty”, he’s musing on how his quest for beauty has left so much behind, his practice, his work, his family, his work, the people he loved, and I thought yeah it’s an aesthetic thing that’s pulled me this way, and while at first I thought that’s kind of strange, that’s kind of weird, I mean we program for money we need to get stuff done, it’s practical, over the years I’ve come to think the aesthetic impulse is, it drives us in our lives and in our work as developers. We have a sense of rightness, we have a sense of what’s fitting, and we rely on it in writing and developing code to guide us and to know what we’re doing, and I find that very intensely working with the array languages.

00:06:32 [CH]

Yeah, I can’t agree more. One of the most beautiful languages, if not the most beautiful language that I’ve ever seen is APL, and there’s something to be said about J and K as well. Let’s hop over to Adám, why do you love the array programming languages?

00:06:48 [AB]

For me it’s definitely the expressivity. I have these patterns in my mind of what I want to do, and how I want to do them, and I’m able to write them down. So for me, APL is very much a language like the human languages, like English is, and being fluent in this language and being able to express myself in this language, it just allows me to speak out to the computer, and write out to the computer what it is I want, and then I get exactly that. I just like, we don’t have to define every nitty bitty detail of the words we use when we speak in English, so too I don’t have to define every little pieces for the computer rather I can use these blocks, very much like playing with Lego, and put them together and it just works. It’s definitely what makes it for me.

00:07:46 [CH]

So we have beauty and poetry, expressivity, and just being able to put on the page what you’re thinking in your brain. How about you Bob, why do you love the array programming languages?

00:07:55 [BT]

Well I’ll bring math into it. Because one of the big things for me is that they’re executable mathematical notation. So you think well any programming language is, you’re going to be able to express mathematics, and that’s true, but the difference is with the array programming languages, the specific things that you’re doing with either numbers or characters is down to single or small groups of functions and modifiers. And what that means is if I want to add up a bunch of numbers, a string of numbers, I don’t need to start writing loops, I don’t need to start declaring variables, I don’t need to do anything else other than write a plus sign, a forward slash, and a backslash in J. And I’ve just, well, in that case I’ve actually scanned it, but if I just want to add the whole list together, it’s just a plus sign and a forward slash, and now I’ve got the total. And it’s, you know, it’s no harder than writing a sigma on a piece of paper and saying that’s what I want to sum up, except now I can put it in a computer and it gives the answer back to me. Not only that, if I want to change the plus to a multiplication sign, which in J is an asterisk, now I’ve got the product. So I don’t even have to learn a different way of expressing adding up a list, I can make multiplying a list, I can make it dividing a list, whatever that would mean. The thing it allows me to do is I will recognise patterns, and Adám brought up the point about patterns, you start to see patterns, it becomes like a telescope would be to a 16th century astronomer, you see quicker these things that are out there. And you think well no, if I multiplied stuff together I’m aware of how you know, I know how Gauss did it when he was in grade 6 or whatever, but the point is that you can actually go in and discover things like that because those patterns pop back at you. And if you want to change it, it’s interactive, so you just change it and get a different answer right away. And it’s amazing how fast that tunes your mind into looking for those kind of patterns so it becomes, you get the advantage of the unreasonable effectiveness of mathematics because essentially it’s a mathematical language that you get to interact with with a computer, and you don’t have to do the heavy lifting, the computer does it. Well I shouldn’t say you don’t have to do the heavy lifting, you do the really heavy lifting, you’re looking for the patterns, the computer does the calculations. And I find that’s what I love about array programming languages.

00:10:31 [CH]

It’s interesting that you say that too because I can a thousand percent appreciate what you just said, but I feel like until someone actually plays around with a J or a K or an APL repl, where they’re typing things in and getting instant feedback, it’s like trying to explain the Grand Canyon to someone, or even showing them a photo like, “oh it’s just sorta a hole in the ground, how amazing could it be”, but until you’re actually standing at the edge of it, actually looking at it, you can’t fully appreciate how powerful it feels to play with that, with that environment. So yeah, all three of those are awesome, I mean, I could spend an hour but I’m going to keep it to two minutes on why very quickly I’ve fallen in love with primarily APL, and I’m learning J at the same time, but you know, Ken Iverson, the creator of both APL and J, everyone that is familiar with those languages knows he won a Turing Award in 1979 and his famous paper ‘Notation As a Tool of Thought’ popularised the idea that the notation that he’s created, which initially wasn’t designed to be a programming language, it was designed to be a notation for explaining algorithms and teaching, it affects the way you think. But I think what’s not completely captured by that idea is the extent to which it changes the way that you think. As a primarily imperative C++ developer, I started learning functional languages like Haskell, and that definitely changed the way I thought, but then when I went from Haskell to APL, it was like a whole other order of magnitude, and it sort of speaks to everything that everyone’s said at this point, you know, Adám mentioned it’s the expressivity of it, but the primitives in the language, are what I think of as algorithms in C++, but when you’re programming in a language like C++ or Python or Java, you’re reaching for for loops, you’re reaching for if statements and while loops and these keywords, and building up something that eventually is expressive, whereas in APL, or in J, you’re reaching for algorithms, you’re reaching for a reduction, a plus operator, a partition, yes technically there are if keywords and for keywords, I basically never use them, and whenever you’re solving a problem you’re reaching for algorithms. There is no better in my opinion environment, or quote unquote playground to learn algorithms because that is what the primitives are, and as soon as you’re constrained to that, the way that you start solving problems is just, you know, massively different to what you might do, even in a language like Haskell, like Haskell’s my second favourite language after APL, but there’s just certain patterns that you’re only going to pick up from being forced to sort of think in this array thinking, this notation as a tool of thought, and on top of that yeah it’s just the most beautiful language I’ve ever seen, and it just makes, like when everything’s a single symbol, every primitive is just one tap of the key, a finger on the keyboard, it changes the way that you develop. Like, writing an algorithm in C++, it takes multiple lines of code, there’s a lot of noise, semicolons, colons for namespaces, parentheses, once you get something working, you’re not going to immediately go back and then try and do 6 other ways to solve the same problem, because there’s so much boilerplate on top of it, whereas in APL, you’ve solved your problem in like 6 keystrokes, ok maybe I’ll go try a couple of others because it’s only 4 or 5 more keystrokes, and it sounds like that’s silly, but it actually does change the way, you know, recently I gave a talk where I showed 8 ways to solve a problem, I’m not going to do that in a language like C++ because I got tired after solving it the first two, and I profiled it and I chose the fastest one, but who knows maybe the seventh solution that was not as intuitive based on my knowledge set was actually the best one but I never got there. And so at this point I’ll just let anyone jump in and comment on anyone else’s answers to the question and we can go from there.

00:14:27 [AB]

Stephen said that it’s kind of like poetry, and it reminded me there’s an old article from ’77 by Alan Perlis called ‘In Praise of APL: A Language for Lyrical Programming’, so I guess, you’re not the first to think of APL as poetry.

00:14:50 [CH]

That’s one of my favourite papers, and I forgot to mention, I actually meant to mention Alan Perlis. So for those of you that don’t know, Alan Perlis, I believe he’s the first, was he the first president of the ACM? I think that’s accurate, but he’s a very well respected individual in the community. He also has a quote that says “A language that doesn’t change the way you think, is not a language worth learning” which I think he was saying that with respect to APL, or at least I’d like to think that because APL changes so heavily the way I think about programs. Bob, you were going to hop in and say something.

00:15:21 [BT]

Well I was going to say actually the same sort of thing that Adám mentioned about the poetry, I think it is very much like poetry, other approaches to programming a computer feel to me more like prose, you’re sort of adding on things all the time, describing what you’re going to do and moving through the process, whereas I find with the array languages I’m pulling stuff away, I’m trying to get down to that core of what’s going to work, and that core feels to me an awful lot like poetry because you’re starting to become more and more precise with the words you’re using, and the order you’re putting them in, and all these things affect the way certain types of poetry, the way it lays out on the page is important, and honestly when I’m really in the moment and I’m programming, I get that kind of the same feeling as if I’m trying to be so precise with my language, it does the same thing and you were talking about how you would try something several different ways, well exactly, it gives me that exact feeling because when you’re in that flow, you are looking for other ways, could I change this, could I change that, and it really draws you in to the art I think of programming, which I find is so neat, so fun.

00:16:38 [ST]

There’s a New York poet I’d like to quote on this Bob, “It is a privilege”, “It is a privilege to learn a language, a journey into the immediate”. That’s Marilyn Hacker, the family name is a coincidence I’m sure.

00:17:03 [CH]

What year, maybe that’s where ‘hacker’ comes from. (jokingly)

00:17:07 [ST]

I’d like to pick up what you were saying Conor about the boilerplate and the noise, I get this feeling of quietness when working with APL, just like Bob was saying, I’m just working with the core of the problem, I don’t have to generate all this distracting stuff. I once heard a C programmer say “well I don’t really get this thing about getting rid of loops, I can write for loops in my sleep”. It’s sort of like, yeah, we’d like you to wake up.

00:17:44 [AB]

It’s funny you mention that actually, I have the responsibility for some code that part of it generates some APL code in a proposed extension of the language. And you talk about someone being able to write for loops in their sleep, and someone reported a couple of edge cases that were buggy in my code. And I looked at the code that I’d written, and it’s about 150 lines or so, and it was complicated, complicated stuff. I went to sleep, and I had a dream, and in the dream, it told me how to approach this in a whole different way that I had done before. So I woke up, I sat down at the computer at six o’clock in the morning, and by noon I’d rewritten the whole thing from scratch, pretty much. I kept 7 lines of code that were tangential to that, and it was all correct. It passed the QAs like that. So sure, you can write for loops in your sleep, but I can write entire correct programs in my sleep! Behold the power of expressivity in APL! I could remember enough details from a dream to just go and write it down.

00:19:06 [BT]

I’m always amazed how much programming I do in my sleep, and it literally is that sort of a thing, I’ll have worked through the day on something, and when I say worked through the day when I’m programming I literally play, I’ll go in and I’ll try something out and try something different, try a bunch of different ways, and it’s just like, the way I know it’s not working is if I keep adding things. Honestly if I keep adding things to fix this part of it, I know in the end it’ll work but it’s not actually, I haven’t got to the core of it. I had a math prof that said once that the solution to mathematical proofs or understanding a mathematical problem is to strip away everything else that’s not the problem, and then you have the solution, and I think that there’s so much of that’s true. When you play with it for a while, and I guess it gets back to this playing part, you play with it for a while, you seed in your mind with all the different things, if you don’t recognise them consciously, subconsciously you pick them up, you go to bed, often I wake up at about 5 in the morning and think, “Oh! I could do this!” and then it’s a struggle to get back to sleep because I want to jump upstairs and get hacking and find out, and what I found is more effective is actually thinking about it for a little bit, going back to sleep, getting up, and then I’ve got energy, I can go at it and sometimes it’s right and sometimes it’s wrong but that’s the nature of looking for patterns, you don’t always get them. The nice thing about the array languages, you can tell really quickly whether you’re on or off. And if you’re on, you can chase it down pretty fast.

00:20:41 [CH]

Yeah there’s Richard Park, who’s going to be a recurring cohost on this podcast, he has a Youtube channel, and he does this thing where he solves these Perl Weekly Challenges every once and a while and he just records it, and his goal is not at all to show the optimal solution, it’s just to show what it’s like to iterate and build up a solution really quickly. And so many of the times what I do afterwards, I follow along, I type along with him, and then I will start stripping away and trying to replace, and I’m going to make a Youtube video at some point, that shows that he has this really long expression, and you can remove like twelve characters with a single max scan, and it’s, the videos are still amazing because you’re seeing someone that knows the language and how they sort of navigate it, but that’s this topic, you’re trying to strip stuff away until – like, certain times you’ll look at a solution, and I’ll be, I’ll think in my head, this is not optimal, there’s too much APL here to be solving what is a very simple problem and I just need to go and think about it for an hour, a week, and just sort of in the back of my head, how could I do this separately, and that’s the thing like because I’m on my APL learning journey, I started off by just knowing just the basics, the reduces, the scans, the reverses, and every once in a while I’ll learn one of the new primitives that I just haven’t learned. Probably the most impactful one that I learned recently was key, that is an operator, so it’s a higher order function. It’s similar to like an SQL group by, or a group by from a functional language, and so previously if I needed to find the maximum occurring element in a list I’d do some sort, and then a grouping with you know, are the adjacent elements equal, and it was beautiful, I thought oh my God, in like six characters I can build up what you know, you spell out the algorithm in another language and it’s more characters to spell out that algorithm than just building it up with the primitives in APL! And then, fast forward six months, and I discover key, and I’m like oh my goodness there’s like a whole single character that I can use to reduce that seven or eight characters that I had, and so it’s, APL, J, I’m sure you can say the same thing about K, while you’re learning it, it’s like what you start of with is so powerful, and then you continue to add to that, J, I discovered under, which I’m sure we can talk about in a future episode, but it’s just, when you need that certain thing, and it’s there, it’s just so beautiful because it simplifies the solution that you have even further, and like Stephen said it ends up looking like poetry at the end of the day, and it’s hard to explain over a podcast, but believe me, it is beautiful.

00:23:32 [BT]

Under is one of my favourites too, as I always think of it as the tyre change algorithm, you jack up the car, you change the car, and then you let the car down. Well under, you do one operation, you do what you’re going to do to it in the middle, and then you reverse the first operation. And it’s so often used in so many things, like in your life, you do that all the time. You know, you open a drawer, you put a spoon away, and you close the drawer. It’s just over and over and over again, and then you can incorporate this idea into mathematics, and it’s incredible how powerful it is.

00:24:10 [AB]

I really like the case of surgery, ‘under anaesthesia’. We literally say that in English, and then you wake the patient up again. That’s the undoing of the action, but it’s all the steps. We don’t think about it, but this is our whole life is like this. Open the refrigerator, take out the food, close the refrigerator. You’re taking it out under opening the refrigerator, but even heart surgery under cutting up the chest, it needs to be sown back together afterwards. Under anaesthesia. You can use multiple of them. It’s these kind of, it’s again the Lego blocks, they’re made so perfectly, they just fit together snugly, and just you know that this is the right way of building it.

00:24:57 [CH]

And it becomes so irritating when you have that tool in an array programming language, and then I go back to my day to day, I get paid money to develop in C++, and I hit that pattern, and then what do I do? I just sort of sit there sadly, I code the transformation, then I do the operation and then I manually undo it, and so many times it’s just like, I love C++, very powerful language, there’s a reason it’s been as successful as it has been, but just, the joy of being able to reach for something that’s the exact thing you need when you go to certain other languages you sort of, you have, what’s the word, like jealousy, envy?

00:25:39 [AB]

Yeah, I definitely have that, sometimes I have to write some Javascript. Inevitably, I hit the same problem, I know exactly how I would do this in APL, and it’s just this long winded thing in Javascript. My Javascript surely looks very unusual, it has dot map all over the place, and dot foreach, and whatever, and one long line of code, and it just comes from frustration of not being able to express myself. I know what it is I want, but there are no words for it, it’s not that I can’t find the words for it, there are no words for it.

00:26:14 [BT]

It’s like translating poetry, you’re trying to fit your words into another language’s poetry and it’s, I guess the good thing is you know what you’re trying to do with it, right? The fact that the other language might not be able to do quite it as fluently, but you do know what you’re getting at, which is to me a lot of times the tool of thought is that it creates the thoughts that you need, and then from there you’ve got a language that can actually execute those thoughts.

00:26:44 [CH]

So, one thing that I’m sure that at this point, I’m not sure what percentage of our listeners are 30 minutes in to the first episode of a podcast on array programming languages and they’ve heard all of us gush about how beautiful the language is, and the first thing I heard about APL and friends was that it was the most unreadable programming language, it’s sometimes joked about as a write only language, and yet we’ve just talked for 30 minutes about how expressive, how beautiful, it’s like poetry, I’m pretty sure our listeners are just completely confused on either what we’re smoking or how this is possible, what has caused this dichotomy of people that are using the language just falling in love with it and then everyone else that’s looking in commenting that oh, it’s just line noise. How can we convince all of our listeners that what we’re saying is, there is really some beauty here and it’s not unreadable line noise.

00:27:52 [ST]

But when you can read it, you write fewer tests, and there’s a serious bottom line you get from it. So years ago I was talking to Kent Beck about ‘extreme programming’, a methodology which he codified which relies heavily on the use of tests, and I said ok so what do you write tests for? This is like one of those zen questions. And he said, “anything you think might break”. Anything you think might break, fair enough. So when I look at my code, what do I think might break? When I see 2+2, I know that’s going to evaluate to 4, I don’t need to write a test for that. I need to write a test potentially for anything that I cannot see is correct. And when you write at the higher level of abstraction that you get in the Iversonian languages, you can see certain things are correct. You use iterators to run through arrays and whatever, you don’t need to test that. The interpreter’s got it completely cold. So you write fewer tests.

00:29:02 [CH]

Adám, Bob, do you want to add what your take is on why if you’ve been learning J for 15 plus, close to 20 years Bob, why were you not running away when you just saw punctuation instead of words.

00:29:19 [BT]

I think the biggest thing initially was just to play around with the language and see what you could do with it. And certainly with J there’s sort of, because of digraphs often your beautiful single characters in APL become two characters and the second character is an inflection which is either a period or a colon in J and so you get a lot of periods and a lot of colons and it does start to look a bit like line noise. But, when I was a kid, we used to go down in Vancouver to Chinatown to have Sunday dinners, my dad had a lot of friends who were in the Chinese community so they’d tell you where the best chefs were. And when you go down to Chinatown in Vancouver then, now it’s a bit more widespread but then, when you walked in, everything that was written was in Chinese. The menus in the restaurants were written in Chinese. And if you don’t read Chinese, that is incomprehensible, it’s just like, I don’t get this. But obviously, people can understand it if they read the language, and they can read it as easily as any other language. And my sense of particularly array programming languages, they’re so short, that you can keep a lot of ideas together in a relatively short space of time which makes it actually easier to understand. So as much as somebody who doesn’t understand, doesn’t read the language would look at it and go “that’s – you can’t get that out of that!”, but if you get the chance to actually practice and learn the language, and there’s actually not that many characters that you have to learn what they do, there’s a lot of, one of the things I like about the language is there’s always a lot of little surprises how they’ll take a character and use it in a different way, and you go “I had no idea you could do that!”. We talked about under, under’s one of those things, you see under and then you see under happening all over the place, and then you see all the places you could use it. First time it’s explained to you, you go “oh that’s kinda neat” but by the time you get into it that pattern starts to build, and now when you see under in a piece of code, you know exactly what’s going on. And it becomes actually easy to read, but you have to learn the language before it becomes easy to read. And because it’s so different than what the more traditional programming languages are, it’s easy for someone to look at it and go “yeah well I already know how to do this” and you do in a different way, but as you said about Perlis’ quote, if it’s not changing the way you think, is it really worth learning a new one? You can pick up a lot of traditional languages, moving between Python and C, Basic, and any other of those type of languages, you start to get into Lisps and Object Oriented languages and it is changing the way you think a bit, but I find even more so with array languages, they really, as I said they have this connection to mathematics that I find really attractive and it tends to focus your mind.

00:32:29 [CH]

It seems like there’s an analogy in there too to when you start to learn the digraphs or the APL symbols you start to learn patterns the same way that when you learn a book we don’t spell out ‘h-e-l-l-o’ in our brain and then, ok, that’s hello, I know that word, our brain is capable of recognising those five letters juxtaposed next to each other and instantly knowing the meaning of it. We don’t have to work through character by character, parse that, put it together as a word, and then find the meaning of it. That’s actually how we learn to read as children, we take our finger and character by character we spell out the word, we sound it out, but that’s when you start. Once you can actually read the language you read very quickly and you’re even able to read and decipher the meaning of words you’ve never seen before, which there’s probably an analogy there. Adám do you want to hop in on what your take is on the unreadability versus poetry of these languages?

00:33:28 [AB]

Sure, I mean I’m a little bit not qualified to answer because I grew up with APL much like say, a child in China grows up with Chinese, and it’s not foreign. So –

00:33:40 [CH]

How is that possible? How come I, what? How could you grow up with APL?

00:33:46 [AB]

Yes I did, my father was a great APLer, and I was shown APL, I was taken along to conferences at an early age and I would sit on my fathers lap as a toddler and he would do APL and building it up, so there’s no real date when I started doing APL, it was just always there. And so the symbols were never foreign to me, and then much with the same thing as we were saying with Chinese, there’s a false sense of familiarity when somebody who knows English or other European languages see a text written in Latin letters. They recognise those symbols, and any other symbols would appear very foreign. So say, an Englishman looks at an Old English text written in runes, it looks very foreign, even though the language is actually pretty close to what he’s used to. And then you can take a language like Maltese, which is closely related to Arabic, but it’s written in English letters right, Latin letters, so you’d get a false sense of ‘oh this is immediately familiar’. But it’s false, because the language is entirely different, has nothing to do with it. Letters might more or less mean the same thing, or they might not. Even taking a letter in English like J and V, and then you go to German that have the same letters, but they have entirely different meanings in that language. So here too, it’s a matter of being more open minded, saying these symbols can mean something and I guess it’s a cultural thing, because we are very used to symbols. If you look around you, look at your smartphone, increasingly interfaces are replacing words with icons everywhere. They’re just little stylised symbols that often are not very good illustrations for what they stand for. The home icon might just be a triangle these days, or a circle, or three horizontal lines for a menu. But it’s taking the essence of an idea and boiling it down, and that’s originally what Chinese characters are too. And if you look at APL symbols especially, but also to quite a degree for J and also for K, the symbols are paired up with the functionalities maybe not in a way that somebody can just go and pick up, but if somebody points it out to you, you never forget what it means. They’re mnemonic in that sense, just like the symbol at the train station that tells you where to go for various things. As a little child you learn them, or you know what the stop sign means, right. There’s nothing in a horizontal sign with a bar that tells you that you can’t go. But once you know that, it just sticks with you, connects with something. So I think it’s very much that people are very much afraid of going outside of their comfort zone. But once they do, and they open their mind and they see the beauty, that’s when they’re sold on it.

00:36:54 [CH]

Yeah that’s one of the things that in my first couple of days of experimenting with APL that I just absolutely fell in love with the language because in mathematics, we, those that created the symbols for certain binary operations drew lines in the sand at where we stopped. So everybody knows that plus is a cross and minus is a flat hyphen, and then we have multiplication, which then it actually gets a bit confusing because in the textbooks as children it’s an X, but then when we get to programming we can’t use X because that’s also an alphabetical character so we actually use an asterisk instead, and then division well we have to come up with, well there’s the hyphen with the two dots in between but that also doesn’t exist on the keyboard so now we have to use slash but that’s not a character so we can use because it’s punctuation. The point is that there’s minus, subtraction, division, multiplication, we typically have a symbol for writing that on paper when we’re in elementary school and then also for typing it on a keyboard, but what about two other very common mathematical operations, minimum and maximum? We just arbitrarily decided that those don’t get symbols? Which like, you don’t really ever pause to think about that, it’s just what we’re taught and so we just take it, ok that’s fine, but like why? Why did we stop? Like we were you know, common binary operations, and min and max we said no, those ones you have to write out, ‘min’ and ‘max’. And then Ken Iverson in the fifties, he saw this and, I’m not sure if he was the first person in the history of the world to have this thought, and said like ok that’s nonsense, and so he created two symbols to represent min and max. And I was building up a slide deck once where I wanted to put all these binary operations, and I had the nice symbols, and then I got to min and max and I was like oh wait I’ve got to type out min and max, three characters, and it looks so asymmetric that these first four binary operations are just a single character, a single thing to represent it, and that is just one example but Ken Iverson I think has noticed that across different domains in math that we just drew the line at some point, oh you know summing a bunch of numbers gets capital sigma, multiplying a bunch of numbers gets capital pi, any other iteration with a binary operation, nah, those don’t get symbols we’re going to stop there, and he recognised this stuff and he fixed it in his notation which later became a language but yeah APL makes you, or array programming languages in general, it makes you sort of wonder, why did math make these decisions, and in my opinion fixed a lot of it. It’s unfortunate it didn’t get adopted by all education systems in my opinion because I find complex math or whatever domain you’re thinking about, linear algebra etc, it’s easier to think about in terms of APL notation than it is to actually think about it in the notation that that domain provides you with. That’s just my take.

00:40:04 [BT]

Even order of operations right? The fact that the order of operations are consistent in APL and if you want to change that order you just parenthesise. Otherwise they go exactly the way they always do, you don’t have to worry about PEDMAS or whatever kids learn in elementary schools, yeah.

00:40:23 [AB]

Some of it did get adopted though. Iverson was a mathematician, and he started off by just making suggestions as to how normal mathematical notation could be improved, and today it’s fairly common to see floor and ceiling written in notation that he used for it, and even conditionals, so predicates mapping to zero and one by putting them into square brackets on occasion, also something he came up with, and that became an integral part of APL and J and K, they all agree on this, that any kind of predicate returns a zero or a one. In a sense APL is evolution, it was never somebody sat down and said ‘hey lets make a new programming language’, it’s just an evolution of where math over centuries had added symbols for more and more things. It’s a natural conclusion

00:41:26 [BT]

What’s kind of interesting to me is that it sort of took a lot of the mathematical symbols that have grown over time and history, and it broke them apart. So that you could take plus and another modifier and you’d get sigma, but then you could do the same thing, you didn’t need two separate symbols for summation and multiplying out a list. You just change the one little, in the case of J we call them verbs, the one little verb that does the work and you modify that, change the verb and you change the way the whole thing works. By splitting it up you can use those combinations, Adám was saying before, it’s like Lego blocks, you literally put a different Lego block with something and you get a very different result.

00:42:12 [AB]

I think that’s a power of it as well, all of these languages take concepts and generalise them, and the power of generalisation is then there’s less to learn. If you learn in mathematics that a huge sigma means summation, and one day you see a huge pi, you have no clue what it means, right? There’s no indication. But if you learn that plus slash means summation, and then one day you see something new you’ve never seen that says multiply slash, you know immediately that then this is a product.

00:42:49 [CH]

Or maybe not immediately but you can at least make a good guess that that’s what it’s doing if you know that the slash in the plus slash is the reduction part of that operation.

00:42:58 [AB]

Ok so if you’ve seen plus slash, and you’ve seen times slash, then one day when you see and slash, you will know that it means all of them.

00:43:07 [CH]

Well I think this is something that potentially array programming language programmers or developers take for granted, of how explicit K, Q, J and APL they all make this, is that when you see a reduction, it’s right there, it’s explicit, maybe you could argue from the Q point of view that because they’ve wordified it that it’s not as explicitly clear but they make a beautiful pattern in Q that the scan always ends in an s of the reduction form, so if you have a reduction that’s a plus reduction, it’s sum, and the scan version of that is sums. Same thing for min and mins and max and maxs.

(Note: this is not a typo, ‘maxs’ is the Q word for a max scan)

When I – that was one of the other things when I fell in love with APL, coming from C++, there was a point in time where I had not made a connection between the different algorithms, accumulate, which is by default it does a sum reduction but you can pass it a custom binary operation to do a multiplies reduction etc, but we also have algorithms like min_element, max_element, we have another one called count_if which counts the number of elements that satisfy a unary predicate. There’s all these differently named algorithms, but there’s absolutely nothing explicit that they are reductions. It’s just an observation you have to make. And there was a point of time where the idea of a reduction was not something that I knew. I did not study computer science, I wasn’t a computer science major, and even if I was I’m not sure that’s something that’s covered in an algorithms course. Usually they’re doing divide and conquer and they’re not actually doing these sort of functional higher order algorithms. And so, at some point, I realised, ‘oh yeah’, because I watched a talk by one of my favourite speakers Ben Deane, who he has a talk called ‘std::accumulate: the algorithmic empire’, I apologise if I got the name slightly wrong, and it shows how of the 90 algorithms in an algorithm header, like 77 of them are implementable in terms of a reduction. And that was when I went oh wow the idea of a reduction, they’re everywhere. And it wasn’t until I went to APL, when you see a summation, or a product, there’s always a slash, it’s right there, you can’t have a reduction without that slash, which seems like a small thing, so Adám was saying, you’re obviously going to recognise that, but coming from a language where that’s not explicit, which is like almost every language, I mean you could argue some functional languages where you have generic folds and generic reduces it’s obvious from that point of view, but like Python for instance, it has a reduce, but primarily you’re using the custom sum and the custom prod for product functions, it’s not explicit and I basically made that observation from learning APL, which I think that there’s a whole category of things that APL and J developers just sort of take for granted and then I come in and I’m like ‘holy smokes this is amazing!’ and they’re like yeah ok that’s like basic 101 stuff, that’s not even why we love the language, that’s just like children’s play and I’m like ‘this is great’!

So that was a little bit of a ramble, we should start to wrap up, this episode we talked about why we love this paradigm and these languages, potentially in our second episode if you are intrigued and want to learn more we’ll dive in a little bit to what makes APL different than J different than K different than Q, and even other array programming languages. But are there any last comments and thoughts that folks want to say before we provide people with some resources and sign off for our first episode?

00:46:59 [BT]

So you’re saying we’re going to do this again? (laughs)

00:47:07 [CH]

We’ll see, we’ll take a look at the stats, honestly I personally even if we have zero listeners, I know I’m going to learn a ton from these meetings so I’m happy to do another one, but all of us are going to have different bars. My bar is at the ground level, you just have to step over it.

00:47:24 [BT]

It’s generally not a good idea for a podcast to have a goal of zero listeners, but –

00:47:31 [CH]

I like to set the bar low so I can over achieve very easily.

00:47:35 [ST]

I’m with Conor on this, not with zero listeners as a goal, but if we are finding this interesting enough to enjoy the conversation, it’s worth doing.

00:47:46 [CH]

And hopefully others will enjoy as well. My assertation is that there are a ton of folks that have heard of APL or heard of J or heard of K or Q or just this paradigm in general and that are – would love to passively listen while going for a walk or doing the dishes or while driving to and from work whenever we go back to driving to work if that ever happens again, this is being recorded in 2021 mid COVID, but they might not be curious enough to go and spend a weekend trying to figure out what do these symbols mean, but they’re curious enough for sure to just passively listen to some folks that are super excited about the technology, and hopefully we manage to attract some of that crowd.

00:48:28 [BT]

Well I would say the only thing with J to remember if you’re looking to find out more about it, don’t do a search of ‘J’, because you’re not going to find it. Start with ‘jsoftware’, all one word, and that will get you into the site for J, but J on its own, that’s kind of the curse of the one letter languages, you have to figure out a way to get into them and the first trick is not to search for the letter because it’s unlikely you’re going to find it. APL’s got a bit of a jump on us there.

00:48:57 [CH]

Even APL, when I – there’s a popular athletic clothing I think ‘Athletic Propulsion Lab’ or something and half the time I search for APL and I’m like, why am I looking at shoes right now. Maybe we’ll kick this over to Adám because you’ve got I think a list of resources or links that if folks want to, even before they get to the next episode go and check out these languages, where should they go to satisfy their curiosity.

00:49:22 [AB]

Yeah well, recently, I together with a bunch of friends overhauled an old site called APL wiki, and you can now find it at apl.wiki, and even though it’s obviously APL centric, it does have also articles about Q, K, and J, and it has links to everywhere. So I think it’s enough of a portal, just apl.wiki, and you can take it from there basically. There are links from the front page to all kinds of things, and a link to something called Introductions, and it has a list of various people presenting their thoughts. There’s an amazing article called Discovering APL written by someone called Stephen Taylor, highly recommend it, and there are also links to where you can try it out and lots of examples and things. It’s mainly on APL but there are links to K and J as well.

00:50:32 [CH]

Alright so APL wiki for a starting portal, google jsoftware for J, also code.kx.com/q for Q if you want to go straight to the Q source.

00:50:43 [BT]

I’d just like to jump in if I could and remind people that if you enjoyed this first episode with arraycast and you’d like to get in touch with us you can send us an email at contact@arraycast.com or tweet us at @arraycast and for more information on the array languages you can visit arraycast.com and there’s a resource page there for background on the array languages. And if you enjoyed this podcast as much as we did then head over to itunes and give us a rating, it really does make a difference in how many people will find out about the podcast, and helps to spread information about the array languages.

00:51:18 [CH]

We’ll sign off, thanks everybody for spending an hour of your day listening to us ramble about this esoteric paradigm that hopefully will catch a few listeners to get interested, because if you want to be a programmer poet, this is the way to do it.

Alright, thanks everyone, we’ll hopefully see you in the next episode.

00:51:39 [Music Theme]

</details>
