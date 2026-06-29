---
title: "Episode 25: Vanessa McHale"
date: 2022-04-16 00:00:00 +0000
episode: 25
buzzsprout-id: 18617102
keywords:
- array-programming
- array-languages
- conor-hoekstra
- apl
- vanessa-mchale
- futhark
- jlang
- haskell
mp3-url: "/assets/audio/episode25.mp3"
episode-type: full
explicit: "no"
block: "no"
layout: podcast
excerpt_separator: <!--more-->
redirect_from:
  - "/episodes/episode25-vanessa-mchale"
  - "/episode25-show-notes"
  - "/episode-25-transcript"
---
In our twenty-fifth episode, we talk to Vanessa McHale, a polyglot programmer with experience in Haskell, Futhark, J and many other programming languages.
<!--more-->

**Host:** Conor Hoekstra

**Guest:** Vanessa McHale

**Panel:** Adám Brudzewsky and Bob Therriault

---


## Show Notes

- [https://code.jsoftware.com/wiki/System/Installation#J904_BETA](https://code.jsoftware.com/wiki/System/Installation#J904_BETA)
- [https://www.acm.org/articles/bulletins/2022/april/50-years-backfile](https://www.acm.org/articles/bulletins/2022/april/50-years-backfile)
- [https://bqnpad.mechanize.systems/](https://bqnpad.mechanize.systems/)
- [https://www.tryapl.org/](https://www.tryapl.org/)
- [https://jsoftware.github.io/j-playground/bin/html/emj.html](https://jsoftware.github.io/j-playground/bin/html/emj.html)
- [https://www.futhark-lang.org/](https://www.futhark-lang.org/)
- [https://www.jsoftware.com/#/](https://www.jsoftware.com/#/)
- [https://en.wikipedia.org/wiki/ATS_(programming_language)](https://en.wikipedia.org/wiki/ATS_(programming_language))
- [https://en.wikipedia.org/wiki/Idris_(programming_language)](https://en.wikipedia.org/wiki/Idris_(programming_language))
- [https://www.egison.org/](https://www.egison.org/)
- [https://www.acceleratehs.org/](https://www.acceleratehs.org/)
- [https://www.aplwiki.com/wiki/Aplette](https://www.aplwiki.com/wiki/Aplette)
- [http://vmchale.com](http://vmchale.com/)
- [https://www.apl.wiki/Jelly](https://www.apl.wiki/Jelly)
- [https://code.jsoftware.com/wiki/Essays/Incunabulum](https://code.jsoftware.com/wiki/Essays/Incunabulum)
- [https://www.youtube.com/watch?v=z8MVKianh54](https://www.youtube.com/watch?v=z8MVKianh54)

<details markdown="1">
<summary><strong>Transcript</strong> (click to expand)</summary>

Transcript

Transcript prepared by Rodrigo Girão Serrão

Show Notes

00:00:00 [Vanessa McHale]

You want something terse.

00:00:01 [VM]

You don't want something verbose because it's just one line, right? So the REPL is good. You could just throw away your code. It's not about like maintenance or anything, it's just about the result, and that's part of exploratory programming.

00:00:25 [Conor Hoekstra]

Welcome to another episode of Array Cast.

00:00:28 [CH]

I'm your host Conor and today we have a super exciting guest to interview. But before we do that, we're going to go around and do brief introductions. I'll throw it to Bob, then we'll go to Adám and then come back to me.

00:00:38 [Bob Therriault]

I'm Bob Therriault.

00:00:39 [BT]

I am a J enthusiast and I'm working on the J wiki. And I'm enjoying my time with J.

00:00:46 [Adám Brudzewsky]

Adám Brudzewsky, full-time APL programmer.

00:00:48 [AB]

Though I don't get around to doing so much programming busy with yeah, wikis and educational materials and so on.

00:00:56 [CH]

And I'm your host Conor nonprofessional array language and combinator enthusiast at large. I program in C++ day to day and yeah, super excited about our guest today because she is a fellow polyglot, probably even more so than I am. So before we get to introducing her, I think we're going to have one announcement from Bob, one announcement from Adám, and then a short announcement for myself. And then we will hop into introducing our guest.

00:01:19 [BT]

[1] Just this past weekend, the new J beta dropped J 904. So I think it may be in beta for a while. These often end up maturing around December and then the new version comes out. That's what happened with 903. The neat thing about 904 is it introduces concurrency and so there are all sorts of things you can do now or are going to be attempted to do. It's right in the midst of development. If you are interested in concern, concern concurrency, this is a great time to get involved because they literally are building it and getting ideas from people. And trying to put things together so any expertise is welcome in the J environment.

00:02:00 [AB]

[2] And I have good news. So for years very valuable, interesting APL papers and and other array programming papers have been stuck behind the Association for Computing Machinery, ACM's paywall, and they've just decided to open up everything from the 1st 50 years of ACM history to be completely free. So that basically means all those interesting papers are now available. Many of them are linked from, say, the APL wiki.

00:02:31 [CH]

Yeah, that's super exciting because I most of the papers that I read they date all the way back into the 20s, 30s, 40s. Or actually that might even be before ACM then so well. Uh, who knows? 'cause that's definitely more than 50 years ago, but definitely a lot of the J and APL papers are going to be available now if they weren't already available on the J software. Right, so yeah, we'll link to that in the show notes and my short announcement is I think I announced this maybe two or three episodes ago. There's a new sort of online editor or interactive REPL for BQN [3], and there's been some huge enhancements to it, and it's just getting better and better and better. Previously, I think when you were defining functions and then calling that on arrays, it would say oh, it wouldn't display the result 'cause they said side effects were involved, but now it shows the results. It's like halfway in between an editor and a REPL, and they've got light and dark mode. They've got different fonts, they've got different VMs. It's it's like crazy awesome. So once again I think Andre Pop is the individual that's primarily working on that. So huge kudos to him and we'll have a link in the show notes. And also we'll probably link the tryAPL [4] for APL and the J playground [5], I think is what they're calling it as well. 'cause yeah, all really easy ways to sort of step into the array language world.

00:03:52 [BT]

And and not to jump in on your announcement, but the J playground actually now has plot and viewmat as well, so you can actually plot things on screen, so it's growing as well really quick. So all these things are kind of taking off, it's really neat.

00:04:05 [CH]

Yeah, in the future no one is even going to be developing on their desktop. If you look at what GitHub and Microsoft are doing, you just hit what does it shift dot and then you're in like VS code online mode. So yeah, pretty exciting stuff. But with all those announcements and introductions out of the way, let's get to the most important of them all. Today we have a special guest of Vanessa McHale hoping pronouncing correctly and she is a polyglot programmer and also a former math major she has developed and has a ton of different projects on her website. I think primarily you develop in Haskell and you can correct me if I'm wrong, but also Futhark[6], J[7], ATS[8], Idris[9], a language I've never even heard of called Egison or Egison[10], i'm sure we've upset, you know, maybe one or two of our listeners that actually heard of it before and so I'll start with the introduction there, maybe throw it over to you and tell us a bit more about yourself and how you you know got to the point where you're developing and not just a plethora of languages, but also you know J and Idris. These are a lot less mainstream than you know, a lot of people have experience in Python and Java, so yeah. Super curious to hear your story and how you ended up in these different, you know, sort of i won't say esoteric languages, but just less mainstream languages for sure.

00:05:14 [Vanessa McHale]

I mean, I've been doing, I guess Haskell for five years professionally, so I was initially attracted to it because it was

00:05:22 [VM]

sort of interesting and obscure. The Haskell world is, i don't know if it's like, cooling off, but it's definitely gotten more mainstream recently, so I've been, you know, if Haskell is your job language, then you've got to do something else for your, I guess hobby language been doing some ATS and Futhark and J, i think those are the big ones, uhm. Futhark is also an array language. It's very much into like ML, Haskell side of things. ATS is like very hard to explain. It's very difficult. UM, sort of like C and ML crossover, academic language. Definitely a lot of fun. Got into J I guess there was like some Chris Double's presentation about APL. I did initially, I guess, brushed it off. Going back, just seeing, I guess how different it is from you used it for some data science stuff. I mean, I guess I'm excited about these sort of like exploratory programming they're I, i think a little bit better than Python and definitely cooler. And I mean there's a lot of good material on it, honestly, which is a big help.

00:06:46 [CH]

So do you mind telling us how like 'cause? I actually didn't really. I think maybe the first time I ever heard about Haskell was about was about two or three years into my career after graduating, and someone I think someone mentioned at work that I might like the arch Linux operating flavor because you need to know a little bit of Haskell to install it. That was the first time I'd ever heard it mentioned, and then it wasn't until like another three or four years later that I'd sort of going, I went outside the world of C++ and then someone said, oh, you should maybe pick up like a functional language like Haskell. And then I said, oh, I think I've heard of that before like so, but it sounds like you came across it pretty early. Did that come from studying or school or?

00:07:30 [VM]

I don't know. I think I've stumbled upon it online. Uhm, I guess this would have been like 2015 or so, so I was in the middle of school and part of it got me into it with the Accelerate Library [11], which is like, incidentally, an array library targeting the GPU, so there's a lot of just like cool functional and compilers stuff written in Haskell. And I didn't quite realize how big it would get, I think among the choices like Haskell versus OCaml [inaudible] at Haskell, and it's like I don't know if it's the default functional programming choice which is a little strange and shocking, but lots of good concurrency stuff. Lots of like good compiler stuff you can learn from there. So I've been, yeah, working at it for five years.

00:08:22 [CH]

And when you, when you when you first stumbled across it, did you have 'cause you? If you've listened to any functional programming podcasts or the rhetoric around a lot of people, they they discover Haskell and then they say, oh, this is not for me. It's way too difficult. What was your experience like first coming to Haskell and especially like accelerate is a uh, i'm not sure I actually haven't played around with it, but it was like a research library that I actually think some folks at NVIDIA worked at, so that's that's some advanced stuff that you were dabbling in. Like it's not like you were doing the hello world. You went straight straight for the the, you know, fun stuff.

00:08:57 [VM]

You know, I think the the Accelerate Library had, like all the hard stuff. I guess part of what is cool with haskell is like being able to do not the hard stuff but like, you can use Accelerate. You could write the sum of an array and you can write it on your GPU. And I mean I didn't know how to write CUDA or anything at the time. I still don't, but, uhm, you know you can encapsulate a whole bunch of that, I mean, in terms of the difficulty, I think. I don't know, I just stuck with it. I do like difficult, challenging things. I think over time I've appreciated that like the Haskell way is almost always the correct way. Uhm, I didn't have the perspective initially, but uhm. I don't know. I guess it just, partly good luck, it did work out so.

00:09:45 [CH]

And would you say the same thing about OCaml? It sounds like you have a little bit of experience with OCaml as well, or is it something specifically about Haskell and the laziness that you prefer?

00:09:55 [VM]

I don't know about OCaml. I mean, my impression is that OCaml is good. And then, like OCalm is strict and Haskell is lazy and Haskell is very different uhm, I think day-to-day people don't always use laziness that much, but it ends up being i mean, it's it's definitely very subtle.

00:10:12 [CH]

And so it sounds like, and up until that point when you had discovered Haskell, what programming languages had you had familiar with or familiarity with? Like is it just the standard stuff for was Haskell literally the first language you stumbled onto?

00:10:24 [VM]

Like from school there was like T-basic and then they learned learned like Scheme. Trying to think what else? I think yeah, yeah, Python, just like for scientific computing. Uhm, so Haskell was like, OK, well, I guess this is like better than Python, and you know, even initially it was quite irritating, but over time you know I appreciated it.

00:10:51 [CH]

And where did you go? So after you know that's been, I guess since 2015, since you first stumbled on it, at what point did you started? You know, is it once you got the taste for Haskell, then you started exploring what other kind of weird you know less mainstream languages are there and you know what was your journey from there to Futhark and J, and ATS and all these other languages.

00:11:10 [VM]

From Haskell to, I guess Idris was like sort of a natural step. It's like if you like obscure things. This is the even more obscure one, and cruise arc is written in Haskell. The compiler's written in Haskell. Idris, the compiler, was written in Haskell, so that was a pretty like natural branching off point, I guess Futhark, I think it has more capability than like, accelerate for instance, it just generates faster code, so that was sort of crazy to see, but a good thing for sure.

00:11:42 [CH]

So what can you tell us about 'cause I i know I've spoken with Troels Henriksen, the individual that created the language and is the main contributor if you look at the GitHub insights for sure, but I actually haven't programmed any Futhark. Is it very similar to Haskell or what's the difference is between the Futhark language and Haskell?

00:11:58 [VM]

Yeah, I guess from Haskell it's like Futhark is a proper OCaml so like the way you have abstraction is like modules and instantiating modules. It's like it's like it's very complementary to J, so like Futhark runs on the GPU and then J is like this very good exploratory language. I don't think, Futhark is just not as strong when it comes to like exploratory programming. There's various things that make it like, you know it has to be delicate. It has to be planned out. But other then on the other hand, J doesn't run on the GPU. It runs on the CPU so, it's very different. A lot of the time that you use like the same combinators or methods, right? Like there's basically one way to sum an array, right? If you have in J, it's like you have the dyad and the adverb right? And you can bind them. In Futhark there's like a reduce combinator of some sort and you reduce with the addition function. So you end up doing a lot of the same things, which I think is pretty interesting. Just in terms of like, the fold, the maps I guess in J that's like dyadic reductions using adverbs or the, what is it? It's the quote conjunction I think.

00:13:23 [CH]

Bob's our resident expert on J, so I'm well.

00:13:25 [VM]

Oh yeah.

00:13:26 [BT]

Yeah, so the quote conjunction you're talking about the ... I'm trying to think of evoke. Is that the one?

00:13:34 [VM]

I think so.

00:13:35 [BT]

Yeah, So what it does is it takes a series of gerunds and then you can use evoke to activate them and make them run like they're verbs, one of the things I think is kind of interesting though is is Futhark is compiled right yeah and and J is interpreted. What I mean? I'm guessing that J gets to call a compiled language that works, just that's not a big deal, but is is there are there are there issues between those two boundaries?

00:14:01 [VM]

I mean, I think the big thing, from what I understand with like J, and array implementations is like you could do reference counting, so there's like a different implementation if it's like an in place modification versus like copying. But you write the same function and then the interpreter does the work. I think with compiled languages, I don't think there's anything like that. At least not now, so i think that that's definitely one of the things that makes j and other things easier. It's nice to like, be able to run reasonably fast without, uh just putting in so much effort every time.

00:14:44 [BT]

Yeah, that's something that Henry's done a lot of work on is usually refer to it as special code so if you know those little idioms, those combinations things run very smooth and very quickly and use much less space because he's he's doing all that behind the scenes and that's what makes this whole concurrency thing kind of interesting, because suddenly he's delving into. I guess potentially using GPUs and actually in the last months J has brought in Arrayfire, so you can actually run Arrayfire from J, so that's sort of they're all nudging into the GPU, and it's interesting to see how it all works.

00:15:19 [VM]

Great right?

00:15:21 [CH]

I'm interested to hear more too, because I've I've really tried to find an articulation for why it is what what is it about J and other array languages that, like you said it, it leads to a more sort of exploratory feel slash, like the flexibility of it, is it I, you know, sometimes I think it's the dynamic typing and then I'm like, well, I don't even really use the dynamic typing and other times it's like, well, it's the REPL and I was like, well, you know, there's other languages like Schemes and Racket and Lisps, they have REPLs and it doesn't have the same and then some of them are statically typed. You know, most are a languages or or or that already said that yeah, dynamic typing and i just I'm not sure. Do you have thoughts on what is it that makes you know J versus Futhark or Haskell? You know what lends it to being more of an exploratory kind of playful experience.

00:16:13 [VM]

I mean, I think honestly, one of the things is like just it's shorter to type things like you can write a one liner and it does basically what you want. I think having a plotting library is good, Haskell doesn't. Uhm, Futhark like the way it does polymorphism in the OCaml way, a little heavier, so like you need to instantiate it for each type. If you're in Haskell or J, it's like just you can type in 1 + 2. You can type it 1.0 + 2.0. And it'll work either way. So I don't know if the dynamic types are all of it. I I do think like the, uh, I don't know if it's the rank conjunction like the double quotes. For the number, I think that's a pretty big one that like Haskell doesn't have Futhark doesn't have. I don't think anyone gotten around to adding that. I don't know what the like, technical PLT theory is but it does seem pretty different. Uhm, maybe rank has something to do with that.

00:17:21 [BT]

What does Futhark use instead of rank? If you're trying to or or because you're instantiating on the GPU, you're not worrying about the the shape of the matrix.

00:17:30 [VM]

So I mean like there's map in functional programming, so that's very familiar in Haskell, for instance, and that's the equivalent. Uhm, so you like you can also like map twice or map three times. But like saying map 3 times is a little like less fluent than just using the double quotes and the three, right? So I think that might be part of it.

00:17:53 [CH]

It's interesting because I never really think that rank polymorphism, which is the fancy term for the fact that you can just add scalars and vectors and matrix, is when you're dealing with scalar operations like I've never thought that that was really like a selling feature of the language. It's I could always get mentioned in the top five things of like oh what is it about array languages? They have rank polymorphism. And then i just remember one day I was switching from APL to Haskell and I had tried to do some sort of equality operation and which of course you just, you know whatever equals whatever in APL, and it'll work. And then I realized like why isn't this working and I had forgotten that I needed to explicitly map and it it becomes something that like you don't think is that nice. But like once you really get used to it, it's it's very irritating, especially if you have to, like you said, you have to map a map or map a map, a map like that's like it it is such a uh, not like a cognitive barrier, but just it's very simple. When you look at the, you know APL or J code that, like you know 1 equals 1 2 3 4 5 and it returns you a Boolean array like, oK, that makes sense. Why should I have to, you know, the implicit mapping via rank polymorphism is really really nice, and it's interesting too that you mentioned the first thing is that the tersity because I never want to say that, because i always the reaction you always get is like you know one of my co-hosts of one of my other podcasts he said what did parentheses ever do to you? I was or he said one time to like what do you have against like characters like it's 2 characters less like what's the big deal? But it it it like extremely impacts, you know, like being able to commute an operation with like reflex and J or commute in APL that goes from like one operation, a minus to, or one character which is a minus, to two characters. Whereas in in Haskell that the spelling of that is, you know flip flip space, parentheses around the minus, and then if you're going to pass that to a mapping operation, there's another set of parentheses that you have to add. And it sounds silly to say that like going from you know, one or two characters to 10, like, oh, that's that's too much it ruins the flexibility of the language, but I I do think like you know it has an impact that's like non trivial. And anyways, I just found it interesting that was like the first thing that you said and I always want to say that, but there's a part of me that says no, no, no like you shouldn't say that Conor because then people just it's easy for them to to make fun of you.

00:20:22 [AB]

But it's not once, Conor when you show show the example of like using one character to compute the arguments versus flip and parenthesis and so on. But it's the constant doing more and more and more the important part of your of your algorithm might be a few characters and it just drowns in in noise in map parenthesis and dots noise everywhere. I lose my I lose track of what I'm doing when I try to write JavaScript. I want to, i want to have two lists and I just want to add the the elements from one list to the elements with the corresponding element from the other list. I can't even use a map for that. I because it don't, it only maps over 1 array. So I have to have to do a map with an iterator and use that to index into the other array and nasty globals everywhere. I definitely think that has value. It's not, it's not the brevity as such, it's the lack of noise.

00:21:20 [BT]

Well, I'm a really undisciplined programmer, so for me it's that brevity means if something is not working the way I want, I go in and change one character and now it is. Or now it's working in a different way and I'm not having to change a whole list of things, I'm just changing one thing. OK, now I know what I got and it just speeds up the process that much more and from my style which is I said, very undisciplined. I'm just literally playing. It it it? If I had a a more verbose language, it would be really hard for me to have the same kind of feedback loop so quick.

00:21:55 [AB]

Then there's the fun of it, of course. Making lots of commits, each of which is a single character changed. And then with long comments as to what all the features just added, right?

00:22:07 [VM]

I mean, I think it's like a the whole like APL way works together and it's like I don't know if it's like a a cult thing or just like off in its own direction but like. You know you're in a REPL, you don't want to like type more than like 100 characters per line. If your function definition is like 200 characters, suddenly that's a problem. So, so I think that's part of it. Or like you know, depending on the tool, right? Like regular expressions are terse, but if you're searching for something in bash, you want something terse. You don't want something verbose because it's just one line, right? So I think it's like the REPL is good, you get to throw away your code. It's not about like maintenance or anything, it's just about like you get the result and that's part of exploratory programming and I think, and you know, there there are other styles, right? Like you wouldn't want your memory allocator to be like a throwaway sort of code. But that doesn't mean that like the way C programmers work is what you need to do for like scientific programming under now. I also think I guess like with numbers. It's easier to check yourself in like sophisticated ways, right? Like if you have like, OK, I'm going to compute the cumulative distributive function distribution function for like a normal distribution, for instance, right? And then you have your function. And you test your output and you know you know what it's supposed to be, right? Like you see oK, that's 0.84 that's basically exactly right, so if it gives me the exact right answer on several different numbers, it probably means I like wrote my procedure right because there's no way for this math to be. This correct like? So I don't know. I think working with numbers in general is probably easier in any language, but with J, you know it, just it works out.

00:24:09 [CH]

Yeah, it's interesting too that you you mentioned, like when you're when you're in a, you know bash terminal or your terminal of choice and you're building up some expression like how many times do people do the you know the cat of the dollar of a list of files and then pipe it to word count to get how many word counts or you? Like there's actually an interesting analogue there. Like everyone fine with LS and like TR for replace and cat for opening files like in all these short expressions so that you can build something up that's very terse but does a lot because like it is empowering empowering when you're in a terminal to be able to very quickly, you know, get some information. And I have actually thought that, like APL, would be like an amazing fit because so many times now, like I usually have a RIDE sort of editor open in the background, and I'll use it for like little calculus anything anytime I need to do like a calculator or a calculator plus plus sort of calculation, like literally the other day, i was I was I had a string of the characters that are possible to be used in a binary message in SmallTalk, which is very random, but like it had a bunch of unnecessary dollar signs and spaces. So I just took that as a string and did without, which I think that has an equivalent in j and then you can basically just you know, on the right put space and dollar sign and very quickly it removed everything and I was just like it's like it's basically like when you open up the calculator on whatever your operating system of choice, but it's like it's a calculator plus plus 'cause you can do things with lists and matrices. And it's I like never thought of that really, when you would just said oh like people are OK doing things on on a in a terminal is like no one has a problem with that. Well, I guess maybe there's some people that like to use a mouse, but...

00:25:56 [VM]

It must be like familiarity, I guess. I don't know, I think some of the J stuff like forks is like a little strange, stranger, but I think being terse in general it's definitely like a good thing. And you know there are a lot of builtins they've, you rely on, i guess. Like if you want to like, compute the seven day sliding average of. Some vector like you can do that super easy. In J, I think there's basically a built in for it. It's like dyadic infix or something.

00:26:29 [BT]

That's exactly what it is.

00:26:31 [VM]

Yeah?

00:26:32 [CH]

Yeah, there's definitely certain things, and maybe that's that's an interesting question to ask, like for your different projects. Or you know, when you're just playing around, is there times when you're reaching for seeing as you have such a toolbox of languages you know from from Haskell to Futhark to Idris, to J, to ATS, to the ones I haven't even heard of. Like how do you go about choosing which language you're reaching for when you're trying to solve a problem?

00:26:56 [VM]

I guess I use J or something like it for most like data processing, like if I have a CSV then i want I want to use a vector language often. Haskell's my default just because I know the most but. I actually was like working on like a speculative like text filtering program. And it's in many ways different from like J or in APL. But I really did like it has a little language you can type in expressions. And I did take inspiration from like terse symbols and characters right? So like there's a deduplication. There's like a length operator. So, i think that sort of style, uh, stayed with me. I don't know. Sometimes I end up thinking like I wish I could make another language which. A lot of work and might cause future problems, but you know that's where I'm at recently I think.

00:27:59 [AB]

So what's in your ideal language?

00:28:01 [VM]

I don't think I have like an ideal. I think Haskell's still pretty comfortable, I don't know. If I'd be capable of like making something else to move away from that, but like ATS has like linear types, it's good for manipulating memory. I think a big one like, would just be, whether it's a text filtering. Uhm, like APL on the command line where you like pipe in something and pipe out APL output. I don't know, that would be nice. I don't know if it would be APL or like J or some derivative. But I think that would be a nice thing. A lot of people would, well, people who are already enthusiastic but perhaps want it, I don't know.

00:28:47 [CH]

Yeah, the idea of an array language and we went for the one for the command line, with the idea that would be a little bit more like I don't want to say first class support for text processing, but some sort of yeah.

00:29:03 [AB]

I think somebody made such a thing, uhm, yeah Applette [12]. I think it was the other one. Uh, yeah. It's it describes itself as being like a specialized utility along the lines of awk and SED. But for array processing rather than text stream processing, and so it uses ASCII glyphs in order to have like super low overhead, then you could just type it on the command line to filter things when you aren't wrapping for text, but you want to extract some data from something on the command line.

00:29:40 [CH]

That would actually be yeah, like an interesting sort of toy project is basically like a dialect, but specifically for the command line where where every symbol is a single character, and although you can already get a lot done like I actually don't know, sed and awk very well, and I've heard awk is actually a really, really nice language. But yeah, that would be an interesting an interesting project.

00:30:04 [VM]

Not sure. I mean I think for the moment I still have things where I'm like, i wish this were better. Start working on it. There are times when I'm like working in Haskell and I'm like, you know, these dependent types are not as good as Idris, so not just, i don't know. Boring, frustrating, but, opportunities like to do more. I don't know. I think ATS is like, also, with big it's more academic research than like hobbyist. That's like, uh, definitely a big gap. There's like there's nothing to like manipulate pointers and arrays of bytes. Yeah, I don't know.

00:30:43 [CH]

It's interesting too that you seem to have you're both operating intellectually or like mentally at like the very high level of like J, but then also at the very low level of C languages. And you know, memory allocation and memory management. Where does that come from? 'cause usually like I think people like to choose like I accidentally ended up at the c level but I like, I think mentally I prefer being at the APL level where you know there's some sort of you know GC or or you know automatic reference counting, or you know there's all the different flavors. I don't really need to think about it and my my ideal is like if I can just get some GPU language that is blazingly fast and like a little bit of allocations. Not a big deal then? Who cares right? But like so yeah, you said you seem to think at both levels. Did that just come from your studies or or courses or?

00:31:38 [VM]

I'm trying to think I think I do, on some level prefer the higher level, but uhm, because I mean there's two things, right? There's like the K, K does something with memory mapping. Which I think is very impressive and they end up getting much better like performance than the R people with their data tables. And then I think there's like a trend in programming languages about thinking about like rather than thinking about languages, thinking about like what are the implementation algorithms that let you do XYZ and I think interestingly, there's a lot of stuff on like compiler backends which is not as well researched, right? Like people will talk about type systems and type systems and type systems, but there's not as much, or maybe this just is older, right? Not like explaining like how register allocation, you know changes the programmer experience, things like that, right? Or like I guess with K, how memory mapping makes the database so fast. It's like faster than any other CPU database. And yet for some reason you know people are not always imitating it.

00:32:53 [BT]

Have you have you have you got any feelings Vanessa about why these languages aren't quite as popular? I think I said I read something you'd written a number of years ago, something to the effect that language well constructed and effective languages are not necessarily the most popular ones, and quite often aren't. Why do you think that is?

00:33:15 [VM]

I don't know. I mean, I think with J, comparing it to Haskell, I think one of the big things is the CFFI. And I mean, that's, I think that's the same with like Lisp and smalltalk which get brought up as examples. It's like doesn't matter if you're a good language. The thing that C does, which it does better than any of the other language is, it, you know, shuffles around bytes and because it shuffles around bytes, you could call it from any language you can. You know, export your functions with the API. And I think that's like a very difficult thing. It's not just like exporting your functions in the C way, but it's like if you want to use. J inside Haskell. It's just difficult, or if you want to use like J within Python, how do you like bring to Python like forks and rank and like you have to be able to export your ideas in some useful way. And I think, you know, like K found its niche right? And now they're just like, you know, make a bunch of money. They have some happy customers. Uhm, but I think. Yeah, like when you compare it to C or like Haskell, Haskell has good fFI a lot of like weird sophisticated stuff they have to do but yeah, I think the like lack of communication between languages it's a big one. Just because people want to do that.

00:34:43 [CH]

Yeah, I think that's one of the huge reasons why Python is so popular, because its FFI stories so so good. Like I've always been curious, is that like Python is older than Java, like people think of Python as this sort of oh it's younger language, like Python python is not a young language and it had similar to Haskell, actually it has a similar story in that it had like created right around 1990. And had this kind of slow burn and got more and more popular as time went on. Sort of like Haskell did it, in spite of like they didn't their whole thing. Didn't Simon Peyton Jones say, like you know, we don't want to be successful? 'cause then we got to support people or something like that?

00:35:21 [VM]

Oh, it's like a this is like a famous one. It's not like avoid success at all costs. It's avoid success at all costs, right? So it's like less cute I think, but that's OK like the ideas. Do not like you know. I mean Java is like popular but it's they grew a lot. You know, Haskell grew more slowly, and they've like more principled decisions. You know it's better to get foundational decisions right than to like build your community by just like putting something out there, which I think did work out pretty well for Haskell.

00:35:58 [CH]

Yeah, it's definitely. It's definitely true. There's definitely in some languages that I can think of a couple off the top of my head that it's not clear that that decision destroyed the success of the language, but definitely it hindered companies ability like the language that I'm thinking that comes to mind is the D language, like early on on it couldn't make up its mind between coming like shipping with the GC or not shipping with the GC. So like I don't even know the full story, I just know at one point it it had one and then at one point it didn't have one and that led to like there being two different versions of the standard library. One that was sort of backed by a GC stuff and that wasn't it wasn't, and it was just like. Having toggling on that decision decision, there were definitely some companies that used it and we're super super, super happy, but others that are trying to upgrade from C++ if they hear like oh, they haven't made their mind up about GC or not GC that's going to be a big thing. But yeah, Python, Haskell, they both sort of slowly got popular, and I've always sort of been curious. I'm like, you know, I can see why Haskell got popular, because like you said, they were really making taking their time getting the important decisions right? But Python? I think Python has like a really great ecosystem, but like that ecosystem wasn't always there. Here, which is why I've sort of, you know, I've heard some people say, oh, it's just the FFI like that's it's one of the best languages uhm, for doing that, I'm not sure if you have thoughts on why Python is so much more successful than other languages out there.

00:37:28 [VM]

I think I've read something about like numpy. Numpy is like the API that scientists use, and I'm not sure like. One, I think they're just like going to be stuck in their ways for like at least. A few decades. Uhm, but I I think Numpy was inspired by J, right? So that makes sense. But then at a certain point. It's like J has like Numpy support. I think presumably K does to like every single bit of scientific code is in Numpy. Sometimes it will be like in pandas too, so. It's just, uh. I think partly momentum. I think Numpy is like not bad for the CPU. But, uh. Yeah, like at at that at this point, Numpy is like the API rather than like c almost, for scientific computing.

00:38:22 [CH]

Yeah, and it's I think momentum is a huge thing. Like you know, I work for NVIDIA and a part of our strategy right now. Like the team that I work for is on a team that basically builds a GPU accelerated version of pandas and there's another team at NVIDIA that is also working on basically a GPU accelerated version of Numpy or Numpy, i'm not sure how it's how it's pronounced, yeah, and and like I would love to like. Let's just start from scratch and and do something like shiny but there's it's a lot easier to convince. You know corporate management that, like hey, there's already X million people using this API or this library. If we go do this with it, you know we can get them. You know buying our hardware, that's a way easier sell than like let's start from scratch and convince people that like our way is better or like not even from scratch that like this language we have from the 90s or the 60s. Uh, you know whichever one you want that like this is the direction we should go in, because if people are already using something, it's it's way easier so. Which is just I guess. The way that corporate America works, or I shouldn't say, America, this is the way the world works, yeah?

00:39:29 [BT]

It's the way the world works really, because yeah, because I mean it's just any anybody doing any kind of performance if you do it to a small audience, it's going to take a while to catch on it. You can hit a mainstream audience. You're going to make a Big Bang and the money is with the mainstream audiences with the fat part of.

00:39:47 [CH]

So I wonder if we should, 'cause I mentioned at the top of the episode that you have sort of a plethora of projects, and I think you've alluded to a couple of them. I think one of them was this i'm not sure if it was one of the projects you have listed, but the speculative speculative was it string processing or string filtering? Do you maybe want to talk about whichever are your favorite projects 'cause it looks like you have a ton of really, really cool ones. That, like I would encourage, well, we'll definitely link this it's it's, i think your website is VM or vmchale.com [13] and then if you go to the portfolio, there's a huge section on programming that has a lot of it's open source 'cause you just have it listed on GitHub so you have stuff in J, Futhark... Do you maybe want to talk us through a couple of your favorite ones, and maybe some that our listeners might find interesting.

00:40:35 [VM]

Uh, so I guess I've got well. The two recent, I guess bigger ones one is Jacinda which is like this dumb text processing language partly inspired by APL and such which trying to be terse with syntax. Try to think. Futhark, I've got a nice little image processing library, so I think a bunch of that is working, and that's pretty fun. It's just like a showing that you can, just like literally just run your code on a GPU and it's faster than Scipy. I don't know. I guess speaks to Python and like where things could go. Uh, I have a like a stack based language. I don't know if that's a that's another weird one. I don't know if you've ever used like a Joy or Factor but this one is called Kempe and it's a well, it's a toy compiler. I don't think the language is great, but the whole world of what is it like stack based languages is pretty cool. Uh, it's some another area where, like, there's not necessarily like lexical scoping. I think J you sometimes want lexical scoping, but sometimes you can do with forks. So this is like a you don't think it's hmmm a smaller world. I think I guess stack based came a little bit after but also like APL or J has developed sort of in its own way so.

00:42:24 [CH]

Interesting, so I another term for the stack based is concatenated languages and I think I first heard of concatenated languages when listening to functional geekery back in 2018 and and yeah, so Forth was like the the OG stack based language and then yeah Factor, Joy. You've mentioned that Mirth was. So, first of all, I had no idea so we we have is, I guess, not necessarily, we, who else maybe was a program language creator that we've had on in the past, 'cause we. I mean, we've had implementers, but not necessarily creators, I think from our past this.

00:43:03 [AB]

Marshall Marshall

00:43:05 [CH]

oh yeah, what am I talking about? I I I don't have a full memorized list in my head, but that's super awesome that you've created a programming language. So yeah, tell us, and I've only I've watched maybe three or four sort of online talks, one about Forth one about Factor. Uhm, so I know a little bit and I've maybe typed a couple lines of code in in one or the other. But yeah, tell us a little bit more, maybe about concatenated languages in general, and also Kempe. This is super cool.

00:43:37 [VM]

So Kempe, I think it ends up being a very good exercise for like writing compilers. Uhm, I've actually, I don't know. Maybe you know, like teachers will want to use some such example I, i don't know if you're familiar with like some types, i guess that's like one of the things that are definitely good, not always easy to get right with array languages, but I think J people don't have that. There's a really like weird some way that like subtypes and pattern matching work in concatenated languages, which I think is pretty interesting, I don't think I'm the first to find that but it's pretty cool. Trying to think you know. Basically there's like no binding or names aside from like calling other functions, so everything is sort of the same, it's a it's sort of funny you're like pushing things onto the stack, popping them off. Which is definitely familiar to, I guess, like Forth programmers.

00:44:43 [AB]

Some people might have used reverse Polish notation on on HP calculators the same kind of thing.

00:44:50 [CH]

Yeah, I'm looking at the the manual right now, and it's yeah similar. I find it interesting that and I've actually I I have to we have to talk to Marshall about this, 'cause I'm curious 'cause I know he looked into concatenated languages at one point as well and his was. Actually the first array language that in the documentation did I ever find the word Combinator from combinatory logic like he actually refers to the a set of i guess he doesn't call them adverbs, he calls them modifiers, but what are adverbs in J and APL? Well, he actually referred to them as combinators and and yeah, yeah, it's it's interesting because in in your docs it mentions dup and swap, which they don't exactly map too, but they are functionally equivalent to sort of the reflex in J and passive, or I can't i can never remember 'cause they have such odd names reflexive, they're like reflexive.

00:45:47 [AB]

Reflexive, yeah.

00:45:50 [CH]

One of them does, yeah commute in self or whatever APL and BQN called them are are much understandable names from my from my point of view, but yeah, it's it's interesting that the overlap in that kind of like function application manipulation in both concatenated languages and array languages and also Haskell. Haskell has not very good uniform support. I actually have that in a in a paper that I'm trying to get published is that. They have all these combinators, but they're scattered across different libraries like control, dot, applicative, and control monad and and one of them is in one called data.composition.

00:46:30 [AB]

Have have you ever looked at Jelly? [14] Has anybody here ever looked at Jelly? I mean not not the food item, the programming language.

00:46:40 [CH]

I only know of this because Marshall mentioned it to me on that email that you were also on when when he when I I said oh Marshall's created the two most recent array languages and Marshall said oh that's not true. Jelly and Jelly is, if you think J and APL yeah, if you think J and APL are weird, well you haven't heard of Jelly yet.

00:47:05 [AB]

Also if you think APL and J are terse, you haven't seen Jelly. Uh, but but Jelly is interesting because it very I mean it is very much inspired by J and and in fact in in some things like a classic thing: plus slash is for summation, just like in any good APL with respect for itself. But it's it doesn't have the ambivalence of primitives. So every function is either monadic or dyadic or niladic. So then it makes like an array and that means and every and every function definition is tacit, so it's all using a type of trains, not the APL J triple trains, forks, but the interesting thing is it very much feels like it's concatenative, stack-based. Many people even get that wrong idea about it because it doesn't use any parenthesis, you can just string, it, think of it as like the K style the K style tacit functions, so it's just lots of atops just applying functional class function apply function. But because the functions are fixed valence, then it it can consume arguments if you have, uh, a dyadic function, it must consume one more argument. And and if there's a monadic function, it consumes one argument. In that sense, it's kind of like the stack based thing, but it really isn't, and it does use higher order functions to combine things. Uhm, it's really fascinating. We should we could get Dennis, the author of it to come visit but,

00:48:42 [CH]

we should, we should note though, for the listener that is not staring at the the GitHub necessarily a docs page. Is that although that all sounds very, very cool, the the character set that is used for this language is like capital A, capital A with a dot over it, capital A with a dot below it, capital A with a dot– i don't, I don't even know, but like the the deltas, the visual deltas between these characters are in many cases very subtle and like that I've seen the Hello world and it looks like you know you've tried to print something and like there was a printer error and it just ended up printing some noise.

00:49:20 [AB]

OK to be fair, that's the golf one. But meaning as short as possible, Jelly has built in string compression and decompression, so it doesn't, hello World doesn't spill out hello world, this just looks up word for which of a number is the word hello

00:49:37 [CH]

but why? Why would you what? isn't that at the top of the documentation like it's what it's what's shown as the..?

00:49:42 [AB]

Yeah, it's a golfing language. It's intended to be as short as possible, but but to be fair, the character set is all typeable on the US international layout, so it's actually easier to to get to typing it properly than, say, APL. They should. Or beginners, it doesn't require a specialized keyboard. Every computer has access to, and every operating system platform has access to the US international layout, so it does have some some merit in that it tries to use mnemonic names for things. It's not so bad. Sometimes I can see uh, I can see Jelly code and understand a little bit.

00:50:19 [BT]

And I think you have to be careful about saying that, uh, language looks like line noise because a lot of people claim that's what our languages look like.

00:50:30 [AB]

Who are we to speak? Oh especially J gives like you just.

00:50:36 [BT]

Yeah, but I love it.

00:50:37 [AB]

Hold down shift and is leaning on the number row in the keyboard.

00:50:43 [CH]

That's true, the Array Language podcast calling other language... Wow, I mean you know this is it's we should, that's true I should take that back. You know we should, we're all under the same umbrella. Let's let's if we're being honest with ourselves so.

00:50:56 [AB]

You can write readable anything and unreadable anything I think are within some limits. Just look at the Arthur Whitney C code. Is that readable?

00:51:05 [VM]

I think he just writes like that. I don't think it's like that. Intentionally obfuscated yeah.

00:51:12 [AB]

He don't he no, he doesn't try to obfuscate, he tries to not scroll.

00:51:16 [CH]

What conversation was I in the other day when the J Incunabulum [15] came up and I think it was the Denver C++ meet up. Uh, either one or two Thursdays ago and i showed the I shared my screen and showed it and I was like my I started off by being like you know I initially thought that this was absolute like line noise, but if you actually 'cause I think they they someone made a joke about using macros in C and then just like redefining everything to one letter. And I was like well hold my beer. This is actually a thing, and, uh, I went from like sort of joking about it to being like. Also though, if you like quickly, you know if you know that V1 and V2 or just monadic and dyadic verbs, and that do is a loop, you can actually Scroll down and see the definition of iota and like it's not immediately obvious what it's doing, but it's it's not like also, as impenetrable as as you'd think, like if you just take 2 seconds to to like familiarize yourself with like the four macros at the top, or you know four of the whatever 10 are at the top. And yeah, it's you know. It's it's very easy to say that something looks hard to read when you have 0 familiarity with it, and then as soon as you take a little bit of time, it's like actually this isn't as bad as as one might think. If you think of it, as maybe a different language then you know it's it's clearly not classical C. It's a kind of DSL that uses a bunch of macros, and once you know those macros, it still looks a bit odd. But I mean.

00:52:52 [AB]

But can you can't say that right? It's perfectly normal. See the fact that the world at large doesn't write C like that, it's not, nobody altered the language to be able to write it like that. Let's just say it's just valid C.

00:53:06 [CH]

I mean when I say classical yeah yeah, Vanessa just sort of went like this with her and it's a people don't you know it's like 90 plus percent of folks are writing sort of in a certain style and i don't think I don't think relying on macros to create a DSL, like I, i think that's I agree, totally valid way to write C. I think when my my quote unquote classical is just that that's not how most folks in fact like in C++ macros. They get used in cases where like there's no other option. But like a part of the evolution of C++ has been to try and add things that basically make the need for macros disappear, and so like the goal is is at some Point C++ 26 or 29 is hopefully going to get reflection and then that should, I mean, there's some people that theorize that it will never be possible to get rid of the macro system, uhm, 'cause it is just so powerful, I mean, to a fault.

00:54:07 [AB]

But you can say this in any language at least language that's under development for many, many years. It was perfectly normal in APL to create character vectors that were APL expressions and then, uh, compress them with the conditions or one or zero, and then execute them. So that's kind of if statement conditionally execute this code that you have built up or not. In today when, at least common popular APL's have control structures and some operators to choose what to do. Then that's looked down upon, but you can't come and say it's invalid APL.

00:54:51 [BT]

It's it's it's not normal APL.

00:54:53 [AB]

No, but it's not, it's it will it was normal APL, right? And who is to dictate what's what's the right way of doing things? It's not and some people might be uncomfortable with it, but then again, I can recognize this programming style in APL of of my colleagues. For somebody who doesn't know APL, they look at it and it's all garbled. Characters they don't know, that they don't know how to pronounce, but I can make sense of some of it because I do APL at the time and some of that that I see i don't like. It's perfectly valid APL, i just don't like it.

00:55:26 [CH]

Well, this is kind of a philosophical and I'm I'm interested maybe to to get Vanessa thoughts because you're primarily a Haskell programmer. It's this the question of, you know what makes a programming language a functional language? 'cause you know some some languages. You know Haskell OCaml, but then there's certain languages like you could mention Rust or Swift that you can code functionally in them, and there's a lot of people that do, and I think there's even like a functional Swift conference, but a lot of people if you call that language functional, they say Oh no, no it's not. Uh, like, you know, do you have thoughts on like what what is it that makes a a language fall into, like 1 paradigm or another or sort of by extension? Like what is? Classical or non classical.

00:56:12 [VM]

I don't. I think APL is like its own sort of like alt functional, like they're definitely functional languages. They have adverbs where you would say like higher order functions, and that was like independently invented, maybe it was invented first. I think the difference was like Haskell or APL. Is like at least in J, you can like use indexing, right? So like you can grade an array and you can use that result to index into the array and then you have like a sorted array. I don't think anyone who wasn't an array programmer would like think about it like that. It's a difficult thing to like, i mean, part of like what makes APL viable or makes J valuable is like the reference counting so that you can modify in place and all of these like efficiency things come so like if you write recursive code in certain cases with like standard ML then it gets compiled to a bunch of jumps the same way you know, like a for loop would in another language because of register targeting. So it ends up being like very difficult and i don't think anyone familiar with like compiler internals but like when you have Haskell, it's compiled with GHC and like a certain functional style becomes viable. If you do that in like Swift or Rust, i don't know if that happens, but I'm also like not familiar like you need to know compiler internals, so I think like. You know, immutable data structures and functional programming. It's just like it's a super hard to get it perfectly on the news.

00:57:54 [BT]

I'm going to jump in and ask the Stephen Taylor question and Stephen's under the weather today, he just let us know that he wasn't going to be part of the panel, but my question is how does the array programming languages change the way you think about the way you structure your programming?

00:58:10 [VM]

Yeah, that's well. I went into this with like Chris Double uhm, I guess like a slide presentation. I think I'd written off dynamic typed languages like OK. Well, that's like sort of wrong and outdated. And then I went to see it and I was like, OK, like this actually works approximately fine and like there are certain things that are missing, but like you can totally program in this. I think exploratory programming just doesn't get enough like uh, attention. I think programmers are all like in their world, and I think scientists and other people are in another one, uhm, trying to think I think there's just like a lot of like different wisdom and it ends up working together right like, other people like to like name their stuff over verbosely, and like you, split it out into 3 definitions. And in J, it's just like one line and it's all symbols, and all of those decisions like if you had decided to, just like write everything together in Haskell, that's a bad decision. Or if you, like decide to like split things out, I guess that's a good decision. And then in J you know, it works differently, right? Like everything together and you sort of have a sensible way to program. Even though, like all of your individual habits are basically totally opposed to the mainstream, right? So you're writing terse code like you don't bother to like factoring out, you just write it inline and throw it away I guess.

00:59:53 [CH]

That reminds me of the the Aaron Hsu talk [16]. I'm not sure if you've seen it where he has sort of like 8, 8, list of eight things that are sort of in in mainstream versus like an APL, and like one of them one of them is libraries versus idioms that in like in mainstream languages you have libraries for all these little string utilities, et cetera, et cetera. But he said it's more common in APL that like you just have some little 3 or 4 character expression that does that. And like do you do you need to name that split because split is more characters than like spelling out of the expression so it just becomes like a kind of better bread and butter thing that you start to learn these expressions that are spellable in fewer characters than it would actually take to name the thing. Uhm, which is like you said it's it's very antithetical to the you know what we learn in school or what we learn on the day job is that, oh, it's all about refactoring and a level of indirection and this whole thing is like no, no, no, no indirection, like you can just write it inline and it'll if you learn to read it.

01:00:54 [VM]

Yeah, no. I mean I think there's like opportunity like you have git for C programmers and then it's like in J world, it's like do you even need like version control? You can just like memorize it and then type it in every single time, which seems just like totally absurd and backwards, but it's actually not even that bad and I I think the way the J interpreter does like idioms is pretty cool. Like telling you this is fast explicitly right, so uhm, then you have like underlying implementation, which you know is probably going to be sensible, which I think is. Better than like, enter now in Haskell world they have their own stuff, but like being able to read the manual and say like if you write your code like this it will be efficient. I think that's something more languages should do because, you know, just not part of their system I guess.

01:01:49 [CH]

Yeah, it sounds, even when you just said like memorize it and rewrite it. Like my first thought, my gut reaction was like, well like, that's really like you have to rewrite your program from scratch each time, but then I just remembered that

01:02:01 [VM]

it's like 10 letters.

01:02:02 [CH]

It well, even when it's more Aaron, Aaron Hsu gave a talk at the most recent Functional Conf. where he it's called like 3 sort of DSL's or his coat, it's basically him showing the three different ways that he implemented his Co-Dfns compiler using sort of three different techniques, and he's actually rewritten each one of those techniques like you know a couple different times, so he's up there, basically saying you know, because my compiler, it's it's not a trivial amount of stuff, but it's also not like it's not an overwhelming, you know you know 100,000 or 200,000 line code base. I have the ability to play around and re implemented a couple different ways and that exactly lines up with what you just said. Like you don't need a version control system for for something that you can fit on, you know half a screen or or one line.

01:02:50 [VM]

I think it's like a better now like more respectful to the user in some ways like, other programming languages you're trying to be like really hard against errors, handle errors like explicitly and then I think in J it's more like about transparency, right like? If you write a mean function to like they say you have, like some verbs to say the seven day sliding mean and it has some implementation and like if your user calls it wrong, then like maybe that's on them and like you can just see the like four or five letters anyways, so. I don't know, it's it's a different approach, I think. Less like you know condescending maybe.

01:03:35 [CH]

Yeah, it's interesting 'cause I think both in J and APL and people can correct me if I'm wrong like the the code that's shipped in the different libraries at least I know this is the case for Dyalog aPL, the whatever dfns like you can, all that code you can look at like you can read which is similar to like the SmallTalk system where you can you know you can step in and look at sort of the code, where a lot of the times depending on which language you're debugging through, that's definitely not possible, so like...

01:04:01 [AB]

Wait, really?

01:04:01 [CH]

absolutely interesting point that like when you – Yeah.

01:04:04 [AB]

I didn't realize.

01:04:06 [CH]

It's just a lot of times when you're yeah, when you're dispatching to some you know binary, like you don't, you don't necessarily have the source with that, so uh, because of.

01:04:16 [AB]

That right, but that's that's that's more an artifact of being compiled, right? And then you can't just step into it like if you had something that's entirely interpreted. Any website you stop it in the middle and you inspect the JavaScript. You can trace through it unless it's been obfuscated, but.

01:04:34 [CH]

Yeah, sometimes the problem is is that with a lot of Python code it is interpreted, but then it's like the pandas in Python, it's basically it's exactly, so it is quote, unquote, interpreted, but the backend is some compiled C code or some compiled C++ code, so you can you can debug down to a certain point, but then

01:04:41 [AB]

it's calling to see eventually.

01:04:53 [CH]

Usually the point you actually want to get to it's like Oh no, now we

01:04:57 [AB]

oK, but then we always have that at some point, right?

01:04:57 [CH]

Don't have access to that.

01:05:00 [AB]

I work with. With a version of Dyalog APL, that's going to come out, and there are sometimes bugs and, and that has gone in into the into a pre release version and and at some point I get to like, this primitive doesn't seem to behave properly. I I give it some sample arguments, I can't step further into it. At this point it kind of calls into a C library, which is the interpreter itself, so you're always hitting that.

01:05:25 [VM]

What do you think like, i was looking at like Scipy code in Python and they tend to have like just i guess it's like a different attitude, right? It's like you i mean they commented heavily, they like check to make sure that like if you pass in a zero length factor, they won't compute the average of that. They'll tell you that like, it has zero length and the thing is like run Python's more verbose 'cause it has like for loops but then just like having the if check it makes the whole thing so much denser and harder to follow. I think you know if you have in J you, you don't even need an average function, but if you did and someone passed in zero length array, then it's like, OK, well that's on you, right? And it ends up, I think working better, right, because then you can actually like. See the code that you're using. Python not so much just because it's like, for both told tracks, it's full of extensive comments and I think, i don't know. Maybe that's alright too, but it's definitely different.

01:06:28 [AB]

I I can see the difference there, like when you're doing all this for fun APL, then yeah, you just or exploratory, you don't care about checking things, you know what it is you're getting, and then sometimes I write these utility functions that have to be like totally hardened. Whatever you throw at them, they must behave nicely and not leave the user in the middle of my code. And and and large amount of my code then ends up being just checks and error messages and things like that telling the user this isn't right. This isn't right, and the actual code that does something, there's just these tiny little short lines in between all the checks and all the error messages.

01:07:04 [CH]

So I will say we're getting, I think probably a little bit close to time, but I definitely want to ask a last question and maybe we'll we'll ask another if Bob and Adám have one, but I'm I'm wondering if you have any advice for maybe you know folks that are still in school or younger folks, because like I said, sort of at the beginning it's I don't think people have done enough what you have managed to very very successfully do, which is sort of explore different paradigms in different languages and not just you know the mainstream Java and what like you said Java, Python and Scheme. And I guess Scheme is kind of out there nowadays. It was less so, but you know back a couple decades ago when they were teaching SICP everywhere but do you have like advice for for sort of younger students on like how to I don't know, successfully explore the languages and like what is it, what is it that manage that you know, enabled you to sort of navigate all these different, sort of, you know less mainstream and build up, you know, get to the point where you're building a concatenated language in in Haskell and all that stuff.

01:08:08 [VM]

I mean, Haskell's in like a funny place now, sort of like calcifying, solidifying. But I think having like confidence and good ideas is like a big one, right? Uh, right, like Haskell, i mean, at the time I was doing it, there were just fewer jobs and now they're you know, a reasonable number of jobs people are using OCaml all over the place like Bloomberg uses OCaml, Facebook uses OCaml, so I think like having some confidence in good stuff and taste, and I mean it, it does take like a few years to pan out, but maybe looking you know, years ahead is a good idea.

01:08:48 [CH]

So then I guess the question is how do you develop that? I mean 'cause everyone here is going to agree that you've got great taste in programming languages, yeah, but yeah, how does one cultivate that? That sense of taste 'cause I definitely I did not have that early on I was just like I don't know, semicolons and braces seems good to me.

01:09:07 [VM]

I mean, I think. I don't know. I haven't done C++, I've used C uhm? I guess part of it was like exposure, just like doing Python, doing Haskell and deciding like you know, maybe Haskell's doing this like the sensible way. Not 100% sure. I guess like digging at foundations can work. I'm not sure like how I wasn't like super aware of what was good in Haskell at the beginning, but, uh. It was a weird one. It was like a little bit of hype, but you know, looking for like academic and difficult stuff can be fun, so that's good too.

01:09:46 [CH]

Yeah, so it sounds like it sounds like the advice is to just explore and you know when you think you see a good idea? Yeah, don't necessarily write it off just because it's in a language that you know, isn't a top 10 on whatever your TIOBE or or what? There's like 16 different, you know programming language rankings and depending on which one you look at, you know, it's it's, there's a, there's somewhat a bit of variety, but you know Python and javaScript are always always close to the top. So any last questions from Bob and Adám? Alright, well thank you so much Vanessa for taking your time to hang out with us today. This was a blast from, i mean, I'm like I can't speak for Bob and Adám, but I I always love nerding out on sort of different languages and I feel like we're definitely having you back at some point in the future, because at the rate that you are pumping out projects, I mean I won't be surprised if some new programming language in the future is normally like oh what's this? And then we're going to see your name attached to it, because it sounds like you're constantly exploring stuff and have already been thinking about a potentially, you know ideal language that may or may not come to fruition.

01:10:54 [VM]

Thanks for having me. It's a lot of fun. Nice to meet you.

01:10:58 [CH]

Alright, thanks so much for coming on, and with that we'll say happy array programming.

01:11:02 [Everyone]

Happy array programming.

</details>
