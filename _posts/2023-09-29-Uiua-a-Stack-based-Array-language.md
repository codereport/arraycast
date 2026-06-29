---
title: "Episode 63: Uiua, a Stack based Array language"
date: 2023-09-29 00:00:00 +0000
episode: 63
buzzsprout-id: 18617064
keywords:
- array-programming
- array-languages
- conor-hoekstra
- bqn
- marshall-lochbaum
- uiua
- concatenative-languages
- stack-based-languages
- kai-schmidt
mp3-url: "/assets/audio/episode63.mp3"
episode-type: full
explicit: "no"
block: "no"
layout: podcast
excerpt_separator: <!--more-->
redirect_from:
  - "/episodes/episode63-uiua"
  - "/episode63-show-notes"
---
Kai Schmidt tells us all about Uiua (wee-wah), a very new stack based tacit array language.
<!--more-->

**Host:** Conor Hoekstra

**Panel:** Marshall Lochbaum, Adám Brudzewsky, Stephen Taylor and Bob Therriault

---


## Show Notes

Array Cast -  September 29, 2023

Thanks to Bob Therriault, Marshall Lochbaum and Adám Brudzewsky for gathering these links:

**[01] 00:01:30**

- [Aaron Hsu talk promotions:Good for 30% off until Oct 1st:](http://www.eventbrite.com/e/540887036687/?discount=AaronHsu30)
- [Good for 15% off up to the conference:](http://www.eventbrite.com/e/540887036687/?discount=AaronHsu15)

**[02] 00:02:35**

- [APL Toronto Meetup](https://www.meetup.com/programming-languages-toronto-meetup/events/296185743/)

**[03] 00:04:01**

- [Uiua programming language](https://www.uiua.org/)

**[04] 00:05:52**

- [BQN programming language](https://github.com/mlochbaum/BQN/blob/master/README.md)
- [Combinators](https://en.wikipedia.org/wiki/Combinatory_logic)
- [ArrayCast tacit programming episodes](https://www.arraycast.com/episodes/episode-09-tacit-programming)
- [arraycast.com/episodes/episode11-why-tacit](https://www.arraycast.com/episodes/episode11-why-tacit)
- [arraycast.com/episodes/episode15-tacit-3-and-other-topics](https://www.arraycast.com/episodes/episode15-tacit-3-and-other-topics)
- [arraycast.com/episodes/episode17-tacit4-the-dyadic-hook](https://www.arraycast.com/episodes/episode17-tacit4-the-dyadic-hook)
- [CodeReport YouTube Channel](https://www.youtube.com/c/codereport/videos)

**[05] 00:10:52**

- [k programming language](https://k.miraheze.org/wiki/)
- [Array Models](https://aplwiki.com/wiki/Array_model)
- [Jagged arrays](https://en.wikipedia.org/wiki/Jagged_array)

**[06] 00:16:35**

- [Bob Smith: A Programming Technique for Non-rectangular Data](https://dl.acm.org/doi/10.1145/800136.804488)

**[07] 00:19:55**

- [Windows function BQN](https://mlochbaum.github.io/BQN/doc/windows.html)
- [Windows function Uiua](https://www.uiua.org/)
- [docs/windowsCombinator Birds](https://www.angelfire.com/tx4/cus/combinator/birds.html)
- [Uiua language tour](https://www.uiua.org/)
- [tourUiua tutorial](https://www.uiua.org/)
- [docs#tutorial](https://en.wikipedia.org/wiki/Stack-oriented_programming)

**[08] 00:24:33**

- Stack programming paradigm
- [Forth programming language](https://www.forth.com/forth/)
- [Factor programming language](https://en.wikipedia.org/wiki/Factor_(programming_language))
- [Arity](https://en.wikipedia.org/wiki/Arity)
- [Ambivalent functions](https://aplwiki.com/wiki/Ambivalent_function)

**[09] 00:34:04**

- [Vigil](https://github.com/munificent/vigil)
- [I programming language](https://aplwiki.com/wiki/I)
- [Hook](https://aplwiki.com/wiki/Hook)

**[10] 00:43:15**

- [Modifiers in Uiua](https://www.uiua.org/)
- [docs/functions](https://www.uiua.org/)

**[11] 00:47:25**

- Over combinator
- [docs/over](https://www.nial-array-language.org/)

**[12] 00:52:25**

- Nial programming language
- [Nial episode on ArrayCast](https://www.arraycast.com/episodes/episode61-lynn-sutherland-and-nial)
- [q programming language](https://code.kx.com/q/)

**[13] 00:55:23**

- [Scan](https://aplwiki.com/wiki/Scan)

**[14] 00:58:30**

- [Audio in Uiua](https://www.uiua.org/)
- [docs/audio](https://www.arraycast.com/episodes/episode43-john-earnest-decker)

**[15] 01:00:04**

- John Earnest Media episode on ArrayCast
- [Rust programming language](https://www.rust-lang.org/)

- [Rust binding to CBQN](https://crates.io/crates/cbqn/)

- [detegr.github.io/cbqn-rs/cbqn](https://detegr.github.io/cbqn-rs/cbqn/)
- [C++ programming language](https://en.wikipedia.org/wiki/C++)

**[16] 01:04:16**

- [Take function](https://www.uiua.org/)

**[17] 01:05:46**

- [April episode on Arraycast](https://www.arraycast.com/episodes/episode23-andrew-sengul)
- [April programming language](https://aplwiki.com/wiki/April)

**[18] 01:07:26**

- [Github](https://github.com/uiua-lang/uiua)
- [Uiua website](https://www.uiua.org/)

**[19] 01:10:05**

- [Contact AT ArrayCast DOT ComAPL Farm Discord/Matrix](https://aplwiki.com/wiki/APL_Farm)


<details markdown="1">
<summary><strong>Transcript</strong> (click to expand)</summary>

Transcript

Transcript prepared by Bob Therriault and Igor Kim

Show Notes

Transcript

00:00:00 [Marshall Lochbaum]

I've chosen a number of names for strange reasons. So what are your strange reasons?

00:00:04 [Kai Schmidt]

I think it's, I like the all vowels thing. I like that it's kind of fun to say, it kind of just like flows out of my mouth. Uiua. Right? There's something fun about that. That's about it.

00:00:15 [Conor Hoekstra]

Does it have a meaning?

00:00:16 [KS]

Not, not really.

00:00:18 [Adám Brudzewsky]

Oh, but you could say it does mean something. Because it's actually Latin.

00:00:22 [KS]

Is it?

00:00:23 [AB]

It's a, it's a nominative, accusative, vocative, plural of uīuum

00:00:28 [KS]

And uīuum being what?

00:00:30 [AB]

That, that, that which is alive.

00:00:33 [KS]

I didn't know that

00:00:34 [ML]

Oh well, that's pretty nice.

00:00:36 [Bob Therriault]

It lives.

00:00:39 [MUSIC]

00:00:48 [CH]

I'm your host, Conor. And today with us, we have a special guest who we will get to introducing in a couple minutes. But before we do that, we're going to go around and do brief introductions from our panelists. We'll start with Bob, then go to Stephen, then go to Adám and finish with Marshall.

00:01:04 [BT]

I'm Bob Therriault, and I am a J enthusiast.

00:01:07 [ST]

I'm Stephen Taylor, enthusiastic about APL and q.

00:01:12 [AB]

I'm Adám Brudzewsky. I do APL.

00:01:15 [ML]

I'm Marshall Lochbaum. I'm still a Singeli enthusiast, but maybe more relevant for this podcast, I'm the creator of BQN. And in the past, I've been a J programmer and worked at Dyalog.

00:01:23 [CH]

And as mentioned before, my name's Conor. I am a polyglot programmer, research scientist by day, and array enthusiast by night-- and by day, actually, I guess. And we have a couple announcements. We have two from Adám and then one from me. So we'll go to Adám first.

00:01:40 [AB]

OK. So if you hurry up just as this episode comes out, then you can get a 30% discount on entrance to LambdaConf, [01] where Aaron Su will be doing some APL. If you don't hurry up so much, then you'll only get 15%, but we will have in the show notes links to both of those reductions in the price. And then there are still a couple of weeks left to the Dyalog23 user meeting. That's the 15th to the 19th of October in Denmark. And what's special now is that all the program is up. So you can see titles and abstracts of everything that's going to be there. So interesting stuff. Have a look, you can still make it.

00:02:29 [CH]

Awesome, links in the show notes. And my announcement, if you recall back in 2022, I think it was late August, September, there was a Dyalog run meetup in both Toronto and New York where we had a couple of different speakers. There is going to be a 2023 edition of just the New York or just the Toronto version on October 2nd, which I believe is gonna be two or three days after this podcast gets released. [02] So if you are listening to this within 72 hours of its being released and you happen to be either in or near Toronto and you are free on Monday night, October 2nd, there will be a meetup that's taking place downtown Toronto, very easy to get to via transit. And there's gonna be, I think, four different speakers. This is off the top of my head, So if it's wrong, I apologize. I believe Richard Proctor, who is local, he is going to be speaking. And then both the CTO and CEO of Dyalog Limited, aka Warren Kronberg and Gita Christensen are going to be speaking as well as myself. And there's gonna be a social afterwards, I think around 8.30-ish. So even if you don't wanna come for the APL talks, I'm not sure why you wouldn't wanna come for that. But you just wanna show up to the social, you can also do that. So links will be in a meetup.com link in the show notes. With all of that out of the way, Today's guest I am very excited to talk to is Kai Schmidt, who is the creator of, if I'm pronouncing this correctly, the Uiua language, which is spelled U-I-U-A. (Pronounced wee-wah) [03] So I definitely would not have guessed that. And if I, I mean, Kai's gonna fill us in on his background, but this is a, I think, array and stack programming language that is implemented, I think, entirely in Rust, which makes it even more interesting because I don't think I'm aware of any array languages that are implemented at any level in Rust. I think most of them are just implemented in C that I know of. Anyways, I will stop there, throw it over to Kai. I'm not sure if you wanna start with sort of giving us a brief background or introduction to yourself and then we can hop into talking everything about this Uiua language, which looks very, very cool.

00:04:44 [KS]

Thanks, Conor. Yeah, so my name is Kai. I've spent most of my career in the construction industry, making automation tools and things like that. I don't actually use any array languages in my day-to-day, or I didn't use really any at all before I started listening to this podcast. I'm actually an avid listener. I've listened to most of the episodes, many more than once. A lot of what you guys have talked about here has really inspired a lot of the – Well, one, it's been a lot of the material I've used to learn about array languages. And it's also helped me make a lot of the decisions because I kind of fell in love with the paradigm. I first heard about APL, I think, in college, but it wasn't from someone who was into APL. It was just part of like, "Oh, here's a bunch of languages and here's what they're all like." But later, I think it was a few years ago, I saw a post on Hacker News about this language called BQN. [04] I was like, "Oh, what's this all about?" And when you go to it and I don't know, the editor and Marshall's writing and stuff, I was like, "Whoa, why have I never seen this before? This is so cool." And my first instinct was like, "This is such a cool idea, except I don't really like this and this and this. I'll just make my own." That didn't come to anything. That was a while ago. That was a few years ago. So I think once or twice I've tried to make my own. Well, I'm kind of a language enthusiast as well. I like writing interpreters and stuff. And so finally, when I started starting to write Uiua, I had that name that I'd come up with a few years before, but it wasn't even going to be an array language. What I started with was, it was definitely a combinator language though. The idea being that a bunch of combinators would be first class like operators that you could compose these combinator primitives into higher order combinators. You have these basic ones like your hooks and your forks and things, and there'd be ways of simply composing them to take more arguments than that so that you could could do full tacit programming. Your guys' episodes about tacit programming, I think-- those are some of my favorite ones. And those are the ones I wanted to-- or that's what I wanted to try to shoot for. I really like the idea and the beauty of just having your data just flow through a bunch of functions and not have to worry about variables or scope or any of that. And so that's kind of been the driving design principle behind Uiua. So that's kind of a background of how I got to this.

00:07:34 [CH]

All right, I've got, I mean, a thousand questions. I mean, but should we, should we let, I mean, I feel like we should let Marshall have the first question 'cause, you know, he has inspired this whole, you know, I don't want to call it journey, the language with BQN. And I guess, well, I'll steal the first question. When you saw the BQN post, was this pre-ArrayCast or was this while ArrayCast had already started?

00:07:57 [KS]

I don't remember. What I do remember is I listened to the, started listening to the ArrayCast. I think a few episodes in. And then as I listened to him, I was like, wait a minute, this Conor guy sounds a lot like that YouTube channel I'm subscribed to, Code Report. Like, wait a minute, it's got to be the same guy. There's no way.

00:08:15 [CH]

Yeah, I realized that sometimes I don't mention often enough that I have a YouTube channel, and I'll be giving a talk at a conference. And like at the 75% mark, I'll show a thumbnail from one of my videos and then a couple people after will be like, "Oh, I didn't realize that was your YouTube channel. You never mentioned it." And I was like, "Oh, I thought I did. Oops." Anyways, if there's people listening, I assume they know at some point I mentioned it in the podcast. But anyways, back to Marshall. What's your first question, Marshall?

00:08:46 [ML]

Well, I have to ask about the name, I guess. So you said you came up with the name before even coming into the array paradigm. I've chosen a number of names for strange reasons. So what are your strange reasons?

00:09:00 [KS]

I think it's, I like the all vowels thing. I like that it's kind of fun to say it kind of just like flows out of my mouth. Uiua. Right. There's something fun about that. That's about it.

00:09:12 [CH]

Does it have a meaning?

00:09:12 [KS]

Not, not really.

00:09:14 [AB]

Oh, but you could say it does mean something because it's actually Latin. It's a it's a nominative, accusative, vocative. Plural of uīuum.

00:09:18 [KS]

Is it? And uīuum being what?

00:09:26 [AB]

That that which is alive.

00:09:30 [KS]

Ah, so those that which are alive.

00:09:33 [AB]

Those which are alive.

00:09:34 [KS]

I like that.

00:09:34 [ML]

Ohh well, that's pretty nice.

00:09:36 [BT]

It lives

00:09:36 [AB]

It lives. Yeah, something that it could be like like make a a free translation to it lives.

00:09:46 [KS]

I could talk about actually the kind of the history of like the design iterations I went through and how I came to think about array programming and tacit programming and things.

00:09:59 [ML]

Well, so the thing that I'm curious about, which I think probably should wait until we've gotten over that stuff, is actually the the array model because I know you started with a flat array model and you went to.

00:10:09 [KS]

Oh, I started even earlier than that with other stuff. I'd love to talk about that.

00:10:14 [ML]

You're currently on a non-flat array model, which seems to be different from all the others. So that'll be very interesting to hear about.

00:10:21 [CH]

Yeah. Take us back in time to the beginning and tell us the history of how you got to.

00:10:26 [KS]

Yeah. So it wasn't originally, it wasn't originally an array language. Like I said, it was a combinator language. Then I, as I started like getting more into like the array paradigm, I was like, oh, I can, I can do this. So I started with the easiest thing to implement, which is of course, non-multidimensional arrays, kind of the, I believe the more of the K type model where things are still ranked polymorphic, [05] but a multi-dimensional arrays of vectors of vectors. And then I was like, I think I could do the whole shape-based flat array thing. And so then I started implementing after reading the thing on the BQN website about the based array model. I was like, oh, I'll try implementing this. And so I did. And it was very complicated, at least I found, because you had to do checks for, "Okay, is this an array? Is this a scalar?" You have to write different cases for different things. And I also found it hard to reason about. And so I simplified it to just a flat array model, like APL 360 style, no nesting, no nothing. What I did have in that model was this idea of fill values. So there are special values for each type, for floats. For regular numbers, it's like nan for characters, it's the null character, etc. And this value would be present in arrays to simulate having jagged arrays, arrays where the rows are of different lengths. So for functions like group or partition or just splitting things up, anytime you could have an matrix or anything that has different lengths, you'd fill in the ends with these fill values. And so while you still have a nice square, rectangular, however many dimensions are raised, you could still have this non-homogeneous length data. And of course, this creates-- you waste some memory here, but I kind of liked the simplicity of it. What was not simple was putting the checks everywhere in the interpreter to properly handle those fill values. And it also had the unfortunate side effect of for a byte array. I added byte arrays because I wanted to be able to efficiently read in files. For a byte array, it had the unfortunate effect of making the bytes two bytes long because there's no value between zero and 255 you can use to indicate this is a fill value. So it ended up being two bytes long because it was basically a union or an enum. There might have been a way to do it such that the fill status was stored separately, like a bit mask or something, but I decided I didn't really like how it was working. And so I moved to something, and you talked about how it's not really like, it's kind of different from all of them. And I guess it is kind of what I settled on is kind of different, but it's most closely related, I think, to J's model where everything's flat. They're not actually boxes that you can put the arrays in. They're actually, there are only three data types. There's numbers, characters, and functions. And so the equivalent of J's box is actually just a constant function, a function that return, that just pushes your value to the stack. And so there's a function called constant, which if you say constant one, it creates this function that returns one. And then of course, there's a call function, which is the equivalent of J's unbox or I think for APLs, disclose. And so you have this simplified model, it unifies boxes and functions and things. And I think it's fine. It works. I do want to explore further the idea of simplifying the model further. Being able to have nested arrays seems very necessary inherently in trying to solve problems. I would like to explore ways of making it so it's not actually necessary, just because I like the elegance of the flat arrays. But that's something I'll have to investigate more. Well, it clearly isn't necessary because, should we say, in APL's heyday, it wasn't possible in mainstream APLs, and that's when people were making money using APL. I'm curious then, I don't know, how did they… If you wanted to do something, Say I wanted to just split a string into the words in the string and they're all different length, and I want an array of that. How would you do that in...

00:15:00 [AB]

You'd be very clever. You start off by finding the separators, I suppose, and then you can compute how long the segments are, and that allows you then to expand with filaments at the end of each segment, and then you reshape into a fixed column width.

00:15:19 [KS]

I see. Before I actually had something like that, but that has the fill elements. Each row gets appended with fill elements. I currently, I do still have, I don't know if you guys have seen it, there's a modifier.

00:15:33 [ML]

Well, and to be clear, they would just use spaces. This is not always safe for if your data had spaces in it. You may not end up with the best code for working around that.

00:15:45 [AB]

There's also the issue of the separator. What if your data has the separate in it? But I should also say, why would you want to split it?

00:15:53 [KS]

That's what I'm trying to answer. I'm trying to think, is there a way to not split it? Is there a way I can solve problems I'm trying to solve without having to do things like split it? So, I don't know, say I wanted the counts of every word in some corpus of text, things like that.

00:16:08 [AB]

There are all kinds of clever algorithms.

00:16:10 [KS]

I'm sure.

00:16:11 [ML]

Yeah, well, for counts, you don't even need to be, have to be that good. what you do is just take all the indices of the separators and subtract the index of the previous separator from the current one. Or well, index of the next separator probably. And that gives you all the lengths. There's a very nice paper that

00:16:31 [KS]

You're saying you index your array separately and work on the indices?

00:16:35 [ML]

Well, you find the indices of every separator that's in your big string with everything together. So you say, where is this separator, and the next separator, and the next separator. And the length of the segment, well, I I think you have to subtract one, too. But it's just the number of characters in between the two separators. There's a really nice historic paper by Bob Smith that's-- I don't remember the title exactly. [06] It's about operations on partitioned arrays, which has, for a lot of more complicated stuff, like if you want to sum each segment of an array or something like that, it has a bunch of operations that you can do just purely using flat arrays, where you'll take in just a list of all the data and a Boolean list that has a one where each segment starts. And then you can do, there's reductions, there's scans, all sorts of things. And they all require slightly different techniques, but there's kind of a, once you get used to this style, you can kind of think of how you would do it for even something that's not covered in the paper.

00:17:40 [CH]

I think Kai's point though is, it's a good one. like there's a lot of small, you know, leak code-ish interview-esque problems, like, you know, given a sentence, you know, separated by spaces, return a sentence where every word in that sentence is reversed. And like in a language like Haskell, you can just go words, which splits it into your, you know, each word in the string, then you can map reverse, and then you can unwords, and like put everything back together. And like, you can clearly do something in APL, which is the equivalent of like a scatter or gather where you figure out, you know, each word and then create the indices that you would, you know, I don't actually, what's the operation with indexing called in APL? In like NVIDIA programming, that's called a...

00:18:30 [ML]

Selection?

00:18:34 [CH]

So like you could technically rebuild up a string with the right indices that are the basically reversed indices of each string, But implementing that to do that in an array language without actually just splitting, reversing, and then unsplitting is a lot more complicated. You can make it happen, but

00:18:54 [ML]

Well, it'll end up looking pretty short, because I think you find the word starts, and then you take the sum of those, and then you do the grade down. And that's it. Those are your indices.

00:19:03 [AB]

There are all kinds of these old techniques that were found for all kinds of flat things. And yes, maybe it is shorter, and maybe you can call it more elegant to do it the nested way.

00:19:15 [ML]

No, I don't think it's more elegant.

00:19:16 [CH]

In Haskell, it's more-- like, it's definitely more elegant.

00:19:22 [AB]

But the flat way is much more sympathetic to the hardware. Doing it the nested way is terrible from the computer's perspective. Nothing can really do to make it good or fast.

00:19:33 [CH]

But as Marshall always says, do we even-- I mean, I don't believe this, but do we even care in Perf? Like, that's the, I saw that Uiua has Windows [07] and I was like, you know, it's, I don't actually know the extent that you have support for the different combinators as in like, you know, SKI, Combinatorial Logic Combinators, but I was thinking, wow, if this is like a stack, you know, BQN with Windows, this is a contender now for like one of my top five favorite languages 'cause famously, BQN does not have a Windows function, which is very, very sad.

00:20:05 [KS]

Wait, Are you sure?

00:20:07 [CH]

Ohh no wait sorry.

00:20:09 [ML]

I think that's where Uiua got it's Windows function.

00:20:11 [CH]

Wait, wait, wait, I misspoke. It doesn't have the n-wise reduction.

00:20:16 [ML]

Yeah, that's true.

00:20:17 [CH]

You have to do a. You have. You have to do a reduce over each of the lists created by Windows.

00:20:25 [CH]

You have to do a reduce over each of the lists created by Windows. Is that the same with Uiua?

00:20:26 [KS]

Yeah, yeah.

00:20:27 [CH]

Nevermind, you're out of the running.

00:20:32 [KS]

And that's actually in my list of to-dos for optimizations 'cause currently if you do that, materializes all the windows.

00:20:38 [CH]

Yeah, exactly.

00:20:43 [KS]

I do want to put like a, an optimization in the interpreter that says, no, if you see this pattern, do it smarter. I would like to talk about the, the com doing combinators though, because in moving to, I forget why I even thought, oh, I could make this a stack oriented language, but it turns out that with just some very simple stack operations, they can be composed and generalized to most of the combinators you're familiar with. So something just something as simple as composition is implicit, right? Just putting one function after the other, it just, they're just composed immediately. And it's, and it's not just like the blue bird and black bird. It's every level of composition, right? So you're, I forget what the other names for those are, but you know what I'm talking about, Conor, all the birds.

00:21:26 [CH]

Yeah. So blue bird is just composing two unary functions. Blackbird is composing.

00:21:31 [KS]

Yeah. And doing both those compositions is ends up being the same in a stack language. And something like flip. So flip is one of the functions in Uiua, and it just flips the top two things in the stack. But just combining duplicate, which just duplicates the top item and makes a copy of it on top of the stack, combining duplicate and flip by themselves, these can make the self combinator, the flip combinator, I think both hooks, both left and right hook, you might need a little more to have dyadic hooks.

00:22:05 [ML]

Yeah, well at some point you gotta duplicate the top, but then flip below the first element.

00:22:11 [KS]

Yeah, so there's also the over function, which takes the second item on the stack, makes a copy of it to the top, and so with just those three, you can make most of them. I have a couple extra things to do more complicated stuff. There's also roll and unroll, which works with the third. It'll either move the top roll, moves the top item on the stack down to down two places. And unroll takes the third item on the stack moves to the top. I'm not copying just moving it.

00:22:41 [CH]

So that's similar to like the ROT rotate. Yes, yes, it would be in like languages like forth and joy. Also to we should I mean, I'm following around along perfectly, partly because I did the the language tour. And also partly because I spent all my free time thinking about combinators. But maybe we should rewind a second. Kai, you can explain to the listener how does -- or maybe even we can go back a little bit further. How did the stack part -- because you said you don't even really remember how you ended up first seeing BQN, thinking about combinators, but then you ended up with both a stack language and an array language. So maybe if you want to -- if there's a story there to tell, or maybe not, you can tell that. And then also explain to the listener, how does a function assignment in like applying functions work if folks aren't, 'cause like in order to understand how you get implicitly for free, like the B and the B1 combinator, I think you need to understand how functions work in a stack language like a Uiua.

00:23:45 [KS]

Yeah, so I think I was aware of stack languages much before I was aware of array languages. [08] So yeah, in a stack oriented language, every function manipulates a global stack of values. And in general, you pop your arguments off the stack, do some operation on them, and then push the results back onto the stack. And so this is why you get composition for free. So if you do something like, if I wanted to find the negative, take the square root of a number and negate it, I would just say, okay, square root function, negate function, that's it. And because each of those pops, its inputs and pushes its outputs back to the stack, they just compose this naturally. This is really nice for tacit programming, because a lot of the times you don't have to name your variables and things. It does get complicated when you need to refer to more than say two arguments. Notoriously, it can get very complicated with juggling lots of values on the stack. I've tried to come up with ways to mitigate how weird that gets. But this is kind of an old paradigm. It's very simple to write a compiler and interpreter for because the computer does have a stack in it, kind of. And so it's actually a very old paradigm as far as I understand, with the original languages being some things like Forth. There's more modern ones like Factor, which does have variable assignment and things like that. But that's the idea. And that's already, it's already a pretty terse paradigm. And so combining that with array, the array paradigm, which is also very terse, kind of comes together to make this very, very terse language.

00:25:30 [CH]

Yeah. And I actually didn't really think about this till now, but I think one of the differences with Uiua compared to array languages is that the arity of all your operations is fixed, correct? Which is- - Yes. - Which is an- - Yes. - Sounds like a small thing, but it actually leads to interesting things you can do with the language, there's no ambiguity of is this a unary or binary or monadic or dyadic function. The arity is fixed.

00:25:54 [KS]

Yeah, that was when I remember. So when I was first learning, reading the documentation for BQN, I did find – and I found this also reading APL and J code – is that I did find it kind of hard as a learner, as someone who's new to the array paradigm, saying like, "Okay, what is this greater than? Is this – or what is this less than? Is this dyadic or monadic? What does this do?

00:26:18 [ML]

That'll definitely slow you down, even as an experienced user. It's like you're looking at this sentence and it's like you haven't figured out what the parody of everything or the airity of everything is yet. And then it all snaps into place, but there doesn't have to be that step.

00:26:35 [KS]

Yeah, you end up having to bind in your mind each glyph two different meanings that your mind has to then parse through the expression to figure out which one to use in that case. So yes, in Uiua, and actually I don't think you could have, what do you call it, ambivalence? I don't think you could have ambivalence in a concatenative language. Concatenative being another word for the way that you write stack-oriented code, because there would be no way to tell what its valence should be if it should take one or two arguments, because everything is just the function. In most stack languages, you write the functions after their arguments. In Uiua, you write them before. So if you wanted to add one and two, you write plus one, two. So what ends up happening is that for every built-in function you need, for everything you want a glyph for, you need two different. Would be one symbol in APL or J or BQN ends up being two symbols. And so, I don't know, something like, I know in APL and BQN, you've got one glyph that represents both the concept of reversing an array and also rotating it by some amount. And so in Uiua, that's two different glyphs, reverse and rotate. The other thing that makes it different to write is there are no special keyboard bindings, basically, to write the glyphs. You don't do some escape code and then type a character on your keyboard and that makes the glyph. You type the name of it, or the prefix of the name of it, and then the formatter turns that word into the glyph. And so this makes it easier to write without any special support. And it also lets you, by just learning the name of something, you can write it.

00:28:18 [CH]

Yeah, it's a novel. Like I don't think there's any, I mean, there's very similar things in the ride EPL editor where you, with some kind of backtick, you get the, you know, the conversion, but there's always something extra. There's, I don't know of any of the languages that are an editor that you just type it. And then when you hit run, It unicodeifies your code.

00:28:42 [AB]

How does that work? How does it disambiguate between user-defined things and built-in names?

00:28:48 [KS]

There are compromises that come with this approach. So the parser is-- it is a context-free grammar. Well, I don't know about grammar. It's a context-free parser. There's no semantic analysis done.

00:28:58 [ML]

The grammar is just like sequence of terms, right?

00:29:00 [KS]

For the most part. We can get into how modifiers and stuff work, which is like the one precedence rule that exists. But yes, it is mostly just this term, then this term, then this term. But disambiguating that from user-defined things, the answer is that if your user-defined term has the same name as a built-in one, it gets parsed, it gets lexed as the built-in token. And so you must capitalize your username.

00:29:25 [AB]

You use capitalization as as the disambiguator, but names are not otherwise case sensitive or what?

00:29:32 [KS]

Names are not case sensitive.

00:29:33 [AB]

Okay, so the first letter, kind of like what BQN does, but using that for something entirely different.

00:29:38 [KS]

Any letter, actually. You can capitalize any letter.

00:29:41 [AB]

Any letter, then it's your name, and if it's all lowercase, it's built in.

00:29:46 [KS]

Yes. Although, you can, if you like, and maybe this is something that needs to get changed for the, once I care about, once I start caring about backwards compatibility, which I don't yet, eventually it might have to be the case, because currently, an all lowercase name, it doesn't get recognized as a glyph, or as the name of a built-in function, will be interpreted as just a regular identifier. That does create barriers then for backwards compatibility if I were to add more built-in functions, of course, because what was originally identifier might become a different kind of token.

00:30:21 [AB]

That's the same answer as, basically the same thing as the answer to people, why can't we just allow people to assign to glyphs in these languages? because then it becomes impossible to be backwards compatible and add things.

00:30:38 [KS]

Well, I didn't think about that because you don't just have to do names. Identifiers can also be single non-ASCII glyphs. So if you just want to make up your own glyphs and make them functions, you can. Maybe that's not a good idea.

00:30:52 [AB]

So accented characters are symbols.

00:30:54 [KS]

Currently, yes. Yes, they are. Actually, no, I take that back. It has anything that's non-alphabetic. That's different than ASCII.

00:31:05 [ML]

Yes. So it actually does like a Unicode lookup.

00:31:07 [KS]

Yes, yes. Now rust has built in. Yeah. So the. Yeah, the interpreter is implemented in rust, so rust has stuff for that.

00:31:14 [AB]

So you can store your source code using the ASCII names, is that correct?

00:31:23 [KS]

Oh, yeah. So binding, naming functions and constants and things?

00:31:28 [AB]

No, no, I mean, you're saying there would be a problem of compatibility if you were to introduce some new built-in and somebody had used a lowercase name. But that sounds like this translation from ASCII names to the symbols happens at runtime and not at some kind of definition time or earlier stage, -which means that.

00:31:53 [KS]

It it does.

00:31:54 [AB]

That means you can store Weaver code as just ASCII text without any Unicode glyphs at all, right? And then run that.

00:32:04 [KS]

It's stored in, it's expecting the input to be in UTF-8. So, no, turning the names, turning identifiers or strings of characters into tokens, turning the ones that look like names of glyphs into those tokens is done in the lexer.

00:32:27 [AB]

Sure, but that's after writing the code, right? So I could potentially write all my code using just English words and no symbols whatsoever.

00:32:37 [KS]

Yes, you could. And then when you run the formatter, it'll turn it into that. Yeah, this is not usually a problem as long as you format your code. I don't enforce that you you format the code, although it is recommended and the default, you could just write code that's all the names of all your functions are ascii and just pass the flag that says don't format.

00:32:57 [AB]

But don't format-- sounds like you're modifying my code. Surely, once I've developed my application, I can run it, and it doesn't change my source code when I run it.

00:33:05 [KS]

Oh, it changes your source code when you run it, unless you tell it not to.

00:33:10 [AB]

And what if my files are read only or on a CD?

00:33:15 [CH]

[LAUGHS] Yeah, details, details, that doesn't matter. Don't make your code files read-only, you know?

00:33:22 [KS]

I haven't-- no, that's a good concern, though. I actually haven't thought of that. I don't know, whenever I write code, I have control of it. But I haven't considered those cases, so that's good to know.

00:33:32 [AB]

It makes it very unique in having a programming language that changes your source code when it runs it the first time.

00:33:38 [KS]

Yeah, I guess I'm very used to using a formatter in whatever language I use, which formats on stage.

00:33:45 [CH]

It's becoming the default of all languages. Like it started with Go and now Rust. Even languages that don't have 'em built in, almost, like I refuse to work for a team that doesn't have a, 'cause you just end up in so many arguments over formatting. You can get rid of 90% of code review arguments by just choosing a formatter. It's like I don't even care what the, I might disagree with the style, but I just don't want to argue about it. I'd rather not argue and be unhappy with the way the code looks than have to argue and try to be happy. Sorry, what did you link there?

00:34:25 [ML]

I linked to Vigil, [09] which is a leader in this field, I believe. What it does is if your code has errors, it deletes them when it runs. the program finally runs successfully, there are no errors in the code.

00:34:42 [AB]

Well, it does this recursively, we should say, right? So if any source file has an error and it gets deleted, then it reruns. And then you do that recursively until no more errors present themselves.

00:34:53 [ML]

I don't know what it does if your source is read-only. Never considered that.

00:34:56 [CH]

Yeah, I wanted to go back to-- because we kind of went on a little mini history of how the stack part got added to the array part of your language. And so hopefully now the listener, if they rewind when we were talking about, you know, the B and the B1, which correspond to the blue bird and the black bird, I think those make, those are pretty easy to grok your head. And so also just for the listener, the way that at least that I understand that functions work is that if you can just assign a sequence of functions to a function, and because there's no data or arguments there, that's going to just basically be like a mini stack. So if you assign two unary functions to a function, that is implicitly the B1 combinator, because it'll

00:35:45 [KS]

I don't know, if I say F and then left arrow, and then a bunch of characters. It looks at those characters, and it does some analysis, that says, okay, how many in aggregate, how many values is this going to pop from the stack and how many is it going to push? If it pops any more than zero, it gets bound as a function. If it pops zero, then it gets bound as a constant and is immediately evaluated. If I say X arrow one, then X is one. If I say X arrow minus or negate plus, it's a function that adds two numbers together and then negates the result.

00:36:25 [CH]

Right, because the arity of plus is two and the arity of negate is one. And then that is an example of an implicit B1 combinator where you're composing the blackboard. You're composing a binary and then a unary after that. So what I can't, or that I'm not certain how I would do is you mentioned that you can do things like the left hook or back hook, or I guess they're in J it's called hook and then I introduced the back hook, which correspond to the S combinators.

00:36:57 [ML]

That's I, the programming language.

00:37:00 [CH]

Yes, Marshall's first language where he was exploring combinators. So that would involve, that involves a binary operation, a unary operation, and then my guess is you're gonna be duplicating, so you're gonna be using your.

00:37:17 [KS]

No, for the left, you're talking about the left hook?

00:37:19 [CH]

Left hook or what?

00:37:22 [KS]

Left hook's the simpler case, actually. So left hook in uiua looks exactly the same as composition. So for example, if I wanted to, I don't know, what's a good left hook example?

00:37:32 [CH]

Palindrome.

00:37:34 [KS]

Yeah, palindrome, perfect.

00:37:35 [ML]

Well, so it depends on how many arguments you're taking, right? So you're talking about the left hook that takes two arguments, right? So it doesn't duplicate one of them.

00:37:44 [CH]

No, so..

00:37:46 [KS]

Oh, no, sorry. No, you're right. The left hook would usually involve a duplicate.

00:37:48 [CH]

I'm talking about the S combinator where the composition returns you a unary function. So you're given a binary, a unary, and it applies the unary to your argument and then takes a copy of your argument as well and passes those to the binary function. So in the palindrome case, your binary function is match, or as they call it in APL, or like Haskell or something you'd have to you know you'd compose that but it's checking what the equality of two strings your unary function is Reverse and then you compose that somehow so you get that pattern so I guess can you walk us through? Yeah, both the hook which is the s-combinator and then the back hook which they both do the same thing But it's applying the unary operation to either the first or the second argument.

00:38:35 [KS]

Yeah, so the left hook is the simpler example so in the case of say palindrome. There's three three functions you usually use duplicate reverse and match And so you take your value and you use duplicate. So now you've got two of them. Then you do reverse, which reverses the top one. Then you do match, which checks if they match. That's it. So it would be spelled match, reverse, duplicate, since the code runs right to left.

00:39:00 [CH]

So interesting. So in this, I'm visualizing this as like, so how did you spell it?

00:39:05 [KS]

It's match, reverse, duplicate, and then code runs right to left.

00:39:09 [CH]

And then so say you pass the value, Or say you pass the value taco cat. Um, and then you duplicate that. So then you end up with

00:39:18 [KS]

taco cat, taco cat on the stack,

00:39:21 [CH]

taco cat, taco cat. And then the top one,

00:39:24 [ML]

Maybe you want to use an argument. That's not, it's not a palindrome.

00:39:26 [CH]

Yeah. Yeah. Yeah. So, okay. We'll just use cat. We'll just use cat. So you end up with cat cat. And so visually I'm, I'm in my head, I'm spelling this equal match cat cat. And then the top value, is that like the, the value on the left? Technically it's not.

00:39:40 [ML]

Well, you can think of it in whatever direction you want, right?

00:39:43 [KS]

Yeah. Left and right break down.

00:39:47 [CH]

Yeah, that's true. Really, you should just separate your stack of functions and your stack of arguments, or is that not a good way to think about it?

00:39:54 [KS]

No. The code runs just always right to left. If you see the duplicate first, it takes your cat and now you've got two strings on top, cat and cat. Then the next function reading right to left is reverse. And so one of those gets reversed. So on the top of the stack, you've got TAC. And then under that, you've got CAT. And then finally, reading right to left, you see the match function. And the match function popped both of those off. It says, are these the same? No, they're not. And so it pushes your zero or your false back onto the stack.

00:40:26 [CH]

Interesting. Yeah, I'm trying to visualize like when you have a sequence or a stack of, at the top of your stack is multiple arrays. and then you have a function of arity that is less than that number of arrays, which array is that applying to?

00:40:45 [KS]

It's always the top.

00:40:47 [CH]

It's always the top one. So technically you could be calling a function that is the fourth thing in your stack, but it's applying to the top array. So it's kind of skipping and ignoring.

00:40:58 [KS]

No, sorry, the functions in general, or in most cases, the functions themselves don't go on the stack. functions are in the code and they operate on the stack. You can put functions on the stack. Functions are after all just arrays, but they're also executed. But in general, unless you're doing a modifier or something, they don't actually go on the stack.

00:41:20 [CH]

Interesting. That makes sense. Then in the backhook example.

00:41:25 [KS]

Yeah. That came up actually when Marshall was looking at it. Somebody was asking about how to do the matrix multiplication. And in the matrix multiplication, basically, before you multiply, you have to transpose the second argument. And so this ends up being.. is that what you mean by a back hook, like a right hook?

00:41:42 [CH]

A back hook being so instead of

00:41:44 [ML]

It sounds like it to me. So your transpose is the monadic part of that backwards hook. Yes. And it's weird because I is left to right. So its hook and back hook are going to be swapped around.

00:41:56 [KS]

But yeah, for the right hook, basically, I think the easiest way is to just do two flips. So you do flip and then your monadic function, and then another flip to put it back down, and then your dyadic function.

00:42:11 [ML]

Although, so if it's a one argument hook, you start out with a duplicate, you don't need a flip after that. So it's flip, then transpose maybe, or duplicate, transpose, then flip, and then your two argument function.

00:42:25 [KS]

Yes. So it ends up being that the only difference between say your monadic and dyadic hooks is going to be whether you have a duplicate at the end or at the beginning.

00:42:34 [CH]

Okay. Hopefully the listener's following along. This makes sense. So the final question at the end of this combinator rabbit hole is, are you able to code an higher order function that saves this pattern? That so, you know, having to spell either a couple of flips or a duplicate is definitely going to be less ergonomic than, you know, the single glyph that BQN has for those things. So could you spell a function that, as arguments, takes functions?

00:43:07 [KS]

Yeah, the syntax for modifiers. [10] So in APL, these are operators. In J, they're adverbs or conjunctions. I think BQN also calls them modifiers. I think that's where I took the name from.

00:43:20 [ML]

Well, J actually calls them collectively modifiers, but that's pretty rarely used over adverbs and conjunctions.

00:43:26 [CH]

You missed the opportunity, Kai, a new language, new word for it.

00:43:30 [KS]

Because we New name. Yeah. Marshall, correct me if I'm wrong, but in BQN functions, one modifiers and two modifiers are all different types. Yes. Yeah. So, so uiua all just, they're all just functions. The only thing that's different between them is how they're parsed. And so glyphs glyphs that are modifiers will parse that because even though the language runs right to left, the parsing is left to right. And so if it sees a modifier, like say reduce, whatever the next glyph is will be interpreted not as something to be called immediately, but as something to be called within the modifier. So if you do slash plus, which is the same as say APLs plus slash, that plus rather than immediately operating on its arguments to the right as it normally would, will be part of the reduction. You cannot define your own, can't name things and then have them be parsed as modifiers, since the grammar is context-free. And so, what that means is that if you have your own thing that wants a higher-order function, something that's going to take a function as an argument, you have to wrap whatever your function is, whatever the code of your function is, in parentheses, so that it won't be called. So, parentheses, rather than being a grouping construct, as it is in most languages. Because you don't need to group anything ever, parentheses lets you define inline functions. And so if I do, say, plus 1, 2, that adds 1 and 2. But if I do surround the plus in parentheses, now I've just got a 2 on the stack, a 1 on the stack, and a plus on the stack.

00:45:13 [ML]

Yeah, so I think this answers something I was wondering about when you mentioned that when you do assignment, it'll turn it into a function only if it's taking arguments from the stack. Yes. I was wondering, how do I make a function that takes no arguments but still does some computation when it's called? And the sounds like parentheses are the answer there?

00:45:34 [CH]

Yes. Yes. Yeah, this is very cool. So it's-- we might have lost a couple of listeners. Don't worry. We'll skip.. I've got a new line of questions and topic conversation in a couple of minutes. But this is... it's very cool. It would be the equivalent of in one of J, APL or BQN, kind of having just like a reduced set of combinator glyphs, you know, whatever they call them. And so in this case, we kind of have not just B, so like in other than J, 'cause J uses S as the to train, but in APL, at least, you know, Dyalog APL and BQN, they use the B combinator as the to train. Because of the fact that this is a concatenative or stack language, you actually get B, B1, B2, B3, Basically, what is B underscore n because the juxtaposition of any two functions regardless of arity just means you're gonna call those in sequence, so if you pass you know a Function that takes three arguments, and that's gonna be the equivalent and then a unary after that That is I think they call that the Bacard or the bunting They they only go up to you know B is blue bird B. One is black bird.

00:46:49 [KS]

There's only so many birds.

00:46:50 [CH]

Yeah, and then they ran out of I think Birds that start with B, but yeah, but card and bunting I think are like B2 and B3 You get that all for free and then you have flip which is the C combinator You've got dupe which is the W combinator and then you've also got I think the other one you call duplicate Which is the one that duplicates?

00:47:12 [KS]

Well, well, there's dupe. There's there's flip and there's over

00:47:15 [CH]

Over was the one that uh.

00:47:17 [KS]

Over is a name taken from like stack languages. [11] Or copies the second value to the top. I don't know if there's a if there's a normal combinator name for that

00:47:23 [CH]

Yeah, I'd have to look that one is it's a little bit different But but with that sort of that small set you can then spell the other ones which is kind of similar I think in Dyalog APL. They don't have the equivalent of The back hook or what is called, you know left in BQN, but you can spell it with you know a combination of the W combinator and I can't remember if it's the D combinator. Anyways, it's just a very, it's very like, I don't know, at least for me, it's like a fun intellectual exercise like understanding what you've done in Uiua and yeah, I'm definitely gonna highlight it and at some point I'd like to give a talk that's like the different ways that you can spell combinators in different languages and like stack languages. I don't really think it mentioned that much. And now I have the perfect language. I don't actually have to leave Array Language land. I can just go to Uiua and then poof, I've got my stack language. And yeah, that's kind of it.

00:48:29 [KS]

It might seem weird to, I don't know, maybe the listener or whoever, like why do you need all this stuff? And the answer is because Uiua does not have named local variables. you cannot give names to things that are not global. Not even like alpha and omega or in BQM, like the script X, script W. And so at one point I did have like a defun style, but basically you could type special letters in and it would correspond to say the, if you typed A would be the first argument, B would be the second argument. And I just didn't like how that made the code look. I didn't like doing that. And so I took that out. And so now everything is just fully tacit. And what I'm trying to explore with the language, I think, is... Because you guys have talked about tacit code a lot and how when it gets too big, it just gets unwieldy and complicated. And so what I'm trying to explore with the language is how to make it not that way. I want these kind of like data flow type operations, or actually, and in fact, all code in my language to just to be that way, to be this like pure, beautiful construct. That's my goal. How much I reach that as the language currently is, I don't know, you can look at some of the expressions and be like, what's going on here? But I don't know, Some of the other modifiers I've added address some of the more complicated things you would have to make.

00:50:10 [CH]

Yeah, that's awesome. I mean, I for a long time have thought it's a kind of a shame that this space isn't explored. Like the different ways to implement or to call combinators, like the stack, stack languages provide one kind of avenue, array languages provide another avenue. you know, the fact that the fixed arity versus ambivalence, like that affects your design choices. But like in languages like Python, C++, Java, like having parentheses, I kind of just, you can't really do much in that space. And that is like 90% of the languages. And I've even looked for papers in like academia that, you know, explore the different ways to, you know, invoke functions and combine functions. It doesn't really exist that I can find. I mean, Haskell is another, you know, Functional language is another space. And they do odd things 'cause most of their combinators are implemented via operators where you define a precedence. That's a part of like defining an operator is like you choose the precedence between zero and nine. But function application..

00:51:15 [ML]

I did basically the same thing in Singeli. Although you can choose any number.

00:51:18 [CH]

Oh, really? Well, it's the thing in Haskell, that 10 is always function application. So there's no way that you can define a operator that has higher precedence than function application, which is also like a design choice. Like you don't necessarily need to have that. And I think in BQN, it's quite interesting that you have the ability with like the underscore, underscores of like defining your one and two modifiers and that like affects. Anyways, it's just a, it's a very interesting space and it's awesome that you are, you know, you've done, you've created this cool language and are exploring that. I hope the same way that ArrayCast inspired you, or at least partly inspired you to go and create Uiua, maybe someone's listening to this conversation now and thinking, "Wow, if Kai did it, I can do it too. " We're going to have all these cool languages competing in some arena in the future. I don't know, there's some Pokemon or Digimon show.

00:52:12 [ML]

There doesn't have to be only one winner, though. I must point that out. That's a big deal. to be able to go in all these different directions. And maybe you say, well, this feature is great. This feature is great. They don't go into the same language, but we have two different languages and you can choose one or the other.

00:52:29 [CH]

And I think it's awesome too that your language, like I don't know an array language, I guess maybe Nial counts, [12] but most array languages, including BQN that get created that are based on sort of APL and J inherit the ambivalence. Every operator has both a monadic and dyadic definition. And that, I think, is a huge choice that affects the language and potentially can make it a lot harder to learn, a lot harder to read. And yeah.

00:53:04 [AB]

Wait, what would Q? Doesn't Q not do that, or try to not do that, or encourage not doing that? I'm not really-- I'm never really sure.

00:53:12 [CH]

I mean, K, Q is just K, right?

00:53:14 [AB]

No, not in this respect, I think. No? Isn't it that Q replaces all the monadic forms of the symbols with words instead? And therefore, they are separate.

00:53:25 [CH]

I guess that's true. I mean, every word built-in function has fixed arity now that I'm jogging through all the different..

00:53:34 [ML]

So this is also true in, I think, most case, at least. But I mean, it's still trying to give you the ambivalent syntax over it all. So what happens is that you have the syntax that's resolved when it's parsed. And then after parsing, everything has only-- well, I mean, and there are some weird caveats to this. But as far as I understand, everything has only one valence after it's parsed. But I mean, it's still-- it's trying to fit into this model of you have your infix and your prefix functions. And so, I mean, basically the APL design. And I mean, Q might be kind of different from that.

00:54:19 [CH]

Yeah. I think it's just, yeah, it's interesting though to see a language that doesn't adopt that because, you know, who knows, maybe that makes it way easier to learn and they go.

00:54:29 [ML]

Yeah, well, so if I can comment on one thing that I was just thinking about this episode. One really interesting thing about the stack paradigm, which you've used for the combinators, is that every operation that you have can, of course, take multiple arguments, but also return multiple arguments. So that's what the flip does. It takes two, returns two. And I was thinking that even one thing that I brought up on the ArrayCast is that actually, instead of having scan and fold be separate, one really nice combination is that you can take the function and your list of things to scan. And what you return is both a scan, an exclusive scan, and a fold. [13] So you get the two things together. And I mean those together like if you want an inclusive scan, then you shift the exclusive scan over and you add the fold element to it. So that's a shift function. But for a lot of other things, like if you're using it for race rides or something, that's just kind of the natural form. You want both of those together. And then another common example that people probably know is the division and modulus. For a whole lot of algorithms, you want to calculate division and modulus at the same time. And in APL, you have to do two different functions. I mean, I guess there's a thing that you can use with encode and Dyalog, but it's not that nice. So yeah, just a comment is one interesting thing to explore would be array functions that return two things and see if there are other constructs that allow you to do more natural array programming that way.

00:56:09 [KS]

Yeah, I've only got-- so there's only one-- other than those flip and I guess over technically takes two arguments and returns three, right? And so do roll and unroll do three and three.

00:56:21 [ML]

Yeah, I mean, but those are just stack manipulation. They're all kind of the same.

00:56:23 [KS]

Yeah, but the only one that actually I think returns two is gen. And gen is not a-- it doesn't have a glyph. You type gen and that's it. and that generates a random number based on a seed. But that returns, it pushes the random number, but it also pushes the next seed that you can feed to the next call of gen. That's the only one I have that returns two things other than the stack functions, I think. There actually is a little bit of ambivalence in some of the functions. So in particular with, actually with the modifiers. So some of the modifiers, not very many, a couple of them do something slightly different depending on whether the function you give them takes one or two arguments. So the ones I'm mainly thinking of are group and partition, and so group was inspired by BQN's group. And then I looked at the APL BQN dictionary for, oh, how do I do the partition in BQN? And this is this long thing of how do you like group things by sequential keys. And so I just added a partition one too. But both of these, basically, they'll in one way or another split your array into segments based on something. So by grouping things by an index and partition it's by sequential sequences and another array. It doesn't really matter. But basically, if you pass part group or partition a dyadic function, it acts like a reduce. But if you pass it a monadic function, it acts like an each or like a rose or a cells, something that builds up a new array, basically. And that's what I've settled on for now. I don't know how much I like that, but it makes it more flexible and it makes it you not have to nest quite as often. Interesting. I was going to bring up, it's kind of funny we haven't talked about it. The one thing that I am proud of for the language is the audio and the images. [14] I could talk about that a little bit. Yeah, absolutely. So built into the online interpreter, and then you can also do it in the native interpreter. You can create image data if you make, say, an array of pixels. They can either just be grayscale or they can be RGB or RGBA. If you make an array of this data, you can, on the web interpreter, it'll just show you the image of what that data represents. And so you can do something similar with audio, where if you make an array of the audio samples, it'll just give you a little player that plays that audio for you. And it's cool because you can do these math operations to generate waves and things, and you can compose them in different ways to create cool images or audio or whatever you want.

00:59:18 [AB]

And how does it decide again whether or not my data represents sound or images?

00:59:24 [KS]

Yeah, so on the web interpreter, just because it's trying to present the language to you, it just does a check like, oh, does it make sense to convert this to audio data? And is it above a certain size? Oh, then it's audio. And otherwise, it's images. Well, if it doesn't look like image data, then do an image. If not, then it just does a normal array. On the native interpreter, if you're actually just trying to run it on your machine, you have explicitly call functions to do that. So there's like an audio play function, an image show, an image encode, so you can save it to a file, things like that.

00:59:56 [CH]

Yeah, it's very cool. I think it's similar to what, was it John Ernest did with? [15]

01:00:05 [KS]

I remember that one, yeah. He did it with K, right?

01:00:08 [CH]

Yeah, his implementation of K and had some similar kind of web ID built into his version. you could very quickly get some sort of graphic stuff, which makes it very, very fun to play with. And yeah, you are now the second language that does that. And yeah, it's definitely fun to play around with it on the Web IDE.

01:00:32 [KS]

Yeah, one cool thing I also added, and it doesn't work on web. I don't know how it would make it work on the web. But on native, I have another function called audio stream, which basically you give it a function, and this function takes in an array of times, and you return an array of samples. And it calls that function over and over again with progressing times, and it will just play audio forever. And what's also cool is that in further invocations of the interpreter, it keeps the time that you're on. And so you could almost-- what I'm going for is kind of almost like a digital audio workstation, is that you can modify these functions. And then as you save that, it picks up the music right where you were or picks up the sound right where you were and continues playing with your modifications.

01:01:25 [CH]

Yeah, that's super neat. One of the questions too, I know we're past the hour mark, so I'm not sure how much time we have to chat about this, is the fact that you've implemented this in Rust. And I'm curious, 'cause you said you've always been interested and implementing interpreters. So like if it was a number of years ago that you were doing that, have you always been doing this stuff in Rust or were you doing it in other languages and sort of what was the path to Rust and how have you found implementing a language in Rust and would you recommend it to other folks out there?

01:01:56 [KS]

Yeah, when I first started like working professionally, I was working with C++ and this was about a couple of years after I think Rust hit stable. And I started using that And the company I was at, I had a lot of freedom to kind of work with what I wanted to. So I started using Rust. And ever since then, I've used Rust whenever I could for projects. I just like the way, the fact that it's, one, it's fast. I can make an interpreter as fast as like a C interpreter could be, theoretically. But also the type system a lot helps me with a lot of stuff. And then the macros. So especially for something like array code, array code is, array interpreter code is like notoriously macro heavy from what I understand. Yeah. And so the Uiua interpreter uses a combination of macros and traits, which are like the type classes in Haskell. And it uses these together to make it so that your functions can be implemented on every type of array. But yeah, so I mean, professionally I program in Rust and also some C#, But it's kind of my go-to language for most things.

01:03:05 [CH]

Interesting, yeah. It's very cool that there's now a-- I think actually there is-- I have seen a Rust BQN VM, I think, implementation, or the start of some implementation.

01:03:19 [ML]

Yeah, that was never finished. We do have a binding from-- so if you want to run BQN in Rust, what you have is just a binding to CBQN that calls into the C interpreter. So that's kind of the preferred way now, which puts a damper on anybody wanting to do something for Rust embedding.

01:03:39 [KS]

Yeah, writing an array language interpreter is an interesting exercise, especially with a lot of the algorithms you have to write. I think some of the hardest ones for me were like windows, or multi-dimensional windows is complicated, and by extension, a multi-dimensional find. Yeah. I don't know if that's what it's called in BQN, the one where it puts ones wherever it finds instances of your array in another. Then things like take can be multidimensional.

01:04:12 [ML]

Take is astonishingly hard for what it does. [16]

01:04:16 [KS]

No, just taking one-dimensional take is simple, but as soon as you get multiple dimensions in there, it gets complicated.

01:04:21 [CH]

Gets it gets complicated. That's the thing for folks out there that want to implement a little array interpreter. Like honestly, it's very similar to a stack language as well. Like if you just.

01:04:32 [KS]

Stick to scalers.

01:04:34 [CH]

That's the thing. For folks out there that want to implement a little array interpreter, honestly, it's very similar to stack language as well. Like if you just stick to scalars and rank one, you know, vectors, it's really honestly pretty straightforward, especially if you're coming from a language with a decent either you know, library ecosystem or standard library, like a lot of the operations in APL just map to algorithms in C++. So if you're not worried about efficiency, you know, you can just naively call those, do a bunch of copies all over the place and you're good to go. But as soon as you skip up to those higher dimensions, it can be, you know, I don't know how many interpreters I've written where I just sort of stopped at, you know, rank one for most operations. I did a couple other products and stuff, but then never have I implemented like, you know, the higher ranks for, you know, glyph like take or something like that, 'cause it just hurts my brain.

01:05:19 [KS]

Yeah, what's weird about it is it's a very different way than you normally write code. 'Cause normally you know the dimensionality of the code you write. you just write a couple loops that go over this dimension or these items or whatever. But when you're writing the looping array code, looping over items in dimensions, and you have to also be looping over the dimensions and things, and it gets really complicated really quick.

01:05:40 [CH]

Yeah, it is. I remember looking at April, [17] which is implemented in Common Lisp, if I recall. And the implementations there are, it's very interesting, 'cause a lot of them are just super, super simple. And then you look at the most complicated functions. And yeah, I definitely, I think I recall a take, but there are some pretty elegant, you'd think, oh, this is pretty complicated, but then I'm not a scheme or lisp programmer, but that code is pretty nice and pretty easy to read. All right, I feel like we're past the hour mark. I do have one last question, but I feel like also I've been asking a lot of the questions. Are there questions from other folks about Uiua? No, no. All right. Well, I'll take the last one then, uh, which is, I mean, I will, we'll, you know, leave links for folks to check it out, but how, uh, you know, how much, um, buzz has this, have you posted this on the hacker news is or the Reddits?

01:06:38 [KS]

I have not. Um, I think Marshall actually pointed it out in the discord, but no, I have not posted this in a single place. Um, this is actually my first like public discussion. How did, how did you and Marshall end up crossing paths? Were you just, did you ask him a question? We didn't. I don't know. Marshall, how did you find it?

01:06:56 [ML]

I don't, I'm not entirely certain. Either you followed me on GitHub and then I checked your profile or I did some search for bqn and ran into it.

01:07:08 [KS]

That makes sense. Yeah, so it is public on GitHub. The best resource for information on the language is UIUA.org. [18] So it's got a full interpreter and it's got tutorials, language tour, and all the tutorials have the built-in interpreter embedded inside them, which I think is a cool way to present it. It's mostly inspired by BQN's website. So it's all public. It's mostly at a point where I'm happy with people seeing it and giving input because I would like feedback on actually using it for things. Because the most cut I've written, or the biggest program I've written is an HTTP server, like a very basic one. I specifically made it good enough to serve the website itself. But I would like feedback on whatever, honestly.

01:07:57 [CH]

I'm not sure, you know, Hacker News is a dangerous, I mean, so is Reddit. Is it dangerous? You know, they're kind of like the dumpster fire corners of the internet that you got it, you know, if you did not grow - if you were - I can't remember, born after certain - but like, you know, certain people I've talked to, they'll post something and then they're like on YouTube and they're like, "Oh my God, people are so mean. " I was like, "Don't you know what like YouTube comment sections are? Like you can't take that stuff seriously. "

01:08:25 [KS]

I think r/programming language would be pretty kind. That's probably where I'll start.

01:08:31 [CH]

There are nice places. But I would be interested to - I think something like this would, you know, I'm biased though, I obviously would click the upvote button, but yeah, I would be interested to see, you know, if BQN gets, you know, a certain amount of traction in APL, I'd be interested to see folks' thoughts and just like, you know, get more people aware. And also too, if you are listening and you are also like Kai, who has a programming language that you have spent an immense amount of work on that is, you know, totally usable, it's like way past the leet code stage, which I'm thinking already about making a YouTube video 'Cause you know, that's basically all I do on my channel is I just solve YouTube leet code problems. So if you've got a language that's, you can solve a couple leet code problems, it's good enough for me. But if you were listening thinking, oh yeah, maybe I should plug my language, we would love to hear about your array languages if you're working on them. Because yeah, like I, you know, clicked on your website this morning, I was like, holy smokes, like this is a full blown thing. Like I had no idea that it was out there, which is why I was kind of asking, like how did I miss this? And the answer is, is because you've never plugged it anywhere.

01:09:40 [KS]

Yeah. Well, this is, this is my, this is my official plug. Check it out.

01:09:43 [CH]

All right. Well, unfortunately, you know, I don't, I don't know. How many listeners do we have, Bob? Do we know, you know?

01:09:48 [BT]

I don't, um, any given episode usually gets around 800 to a thousand downloads.

01:09:55 [CH]

We're not at the a million listener.

01:09:57 [BT]

Listen, we're not at the million listener yet. All right.

01:10:00 [KS]

Well, it's all right. The, the, the listeners of this podcast are my target audience.

01:10:07 [BT]

Well, and if they want to get back in touch with us, of course, contact@ArrayCast.com, [19] and we can forward any questions or comments back on to Kai, although I think if you go to Uiua.org, there'll be ways to get in touch with him more directly. Super cool language, really interesting. One thing I noticed, you were talking about your pursuit of Tacit. run into the same issues as soon as you go left to right or right to left when you want to do modifiers suddenly you have to start using parentheses to group them you just really can't get away from that at least it seems because the same thing with j is it's right to left except for modifiers which are left to right because you've got a long left reach and and you have to do that just because that's the way you have to be able to separate them them from the standard functions. Anyway, that's my little bit. Contact@ArrayCast.com and this has been super cool. And you have done a lot of work and I was really impressed with how advanced the site is and how far you can take it. Just for a language starting out, it's quite remarkable. And it does remind me of BQN as well.

01:11:17 [KS]

Thanks a lot, Bob.

01:11:22 [CH]

Yeah, this conversation has been, I know, this is awesome. Like I've been so entertained getting to ask you questions and I'm excited for our listeners to hear And I'm sure they'll have, um, you know, some exciting thoughts to share and hopefully they'll go check it out. And, uh, you know, maybe in the future we can have you back and get some Uiua updates, uh, and it is, it is a very, yeah, that'd be great.

01:11:39 [KS]

I'm all, I'm also on the APL farm discord. If anyone wants to just,

01:11:43 [CH]

Oh, awesome. Is there a Uiua, is there a Uiua channel?

01:11:46 [KS]

No, I think the index there was her. I was talking about a little bit.

01:11:49 [ML]

I would just use the main one.

01:11:51 [KS]

OK.

01:11:52 [CH]

All right. Yeah. So if you want to reach Kai as well, APL farm, we'll have a link in the show notes for that discord. And yeah, like, we'd love to have you back in the future and chat again. I feel like we probably could, I mean, I definitely could have asked, you know, probably an hour more worth of questions, but we got to dice these up a little bit. Otherwise, you know, our listeners are going to be like, what is going on? A four hour podcast? Although there are other podcasts that have, you know, three to four hour conversations, but that's not us. So anyways, thank you Kai.

01:12:19 [BT]

I'm not editing those podcasts.

01:12:24 [CH]

Yeah, maybe at some point in the next few years we'll get some LLM editor, you know, that we can save Bob a lot of work and have that stuff automated, but we're not there yet. So we thank Bob for all his hard work and doing all the heavy lifting. And also, as well, Sanjay and Igor are hardworking transcribers.

01:12:44 [BT]

The transcription team, Sanjay and Igor, yes, they do a great job.

01:12:47 [AB]

They fix what the LLMs can't do. Exactly.

01:12:51 [CH]

Yeah. We still need, we still need, you know, humans are still important for the moment. Anyways, thanks so much for coming on, Kai. This has been awesome.

01:13:02 [KS]

That's been great.

01:13:03 [CH]

Looking forward to talking to you again in the future and seeing where we all go. So with that, we will say happy array programming.

01:13:11 [ALL]

Happy Array programming!

</details>
