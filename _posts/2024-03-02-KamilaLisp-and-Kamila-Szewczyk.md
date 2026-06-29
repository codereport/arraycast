---
title: "Episode 74: KamilaLisp and Kamila Szewczyk"
date: 2024-03-02 00:00:00 +0000
episode: 74
buzzsprout-id: 18617053
keywords:
- array-programming
- array-languages
- conor-hoekstra
- kamila-szewczyk
- kamilalisp
- lisp
- apl
- compression
mp3-url: "/assets/audio/episode74.mp3"
episode-type: full
explicit: "no"
block: "no"
layout: podcast
excerpt_separator: <!--more-->
redirect_from:
  - "/episodes/episode74-kamilalisp"
  - "/episode74-show-notes"
  - "/episode-74-transcript"
---
For this episode, we spoke with wunderkind Kamila Szewczyk, creator of the KamilaLisp experimental language.
<!--more-->

**Host:** Conor Hoekstra

**Guest:** Kamila Szewczyk

**Panel:** Marshall Lochbaum, Adám Brudzewsky, Stephen Taylor and Bob Therriault

---


## Show Notes

Array Cast -  March 1st, 2024

Thanks to Bob Therriault, Adám Brudzewsky, Stephen Taylor and Conor Hoekstra for gathering these links:

**[01] 00:01:24**

- [kDB new features](https://www.youtube.com/watch?v=EUGJPO7ObNg)
- [KX webinar introducing version 4.1:](https://www.brighttalk.com/webcast/19020/607221?utm_campaign=communication_viewer_foll[%E2%80%A6]72VzwHTR3atQ2vad7lgsEcr31FZ6aOSWclNA%3D&utm_content=webcast)
- [DYNA April Meetup](https://dyna.dyalog.com/)
- [ProgLangCast Reaction to Adám's reaction](https://www.youtube.com/watch?v=I57buGfKm3w)
- [Adám's response video](https://www.youtube.com/watch?v=0k_lfwprF2M)
- [ProgLangCast Original APL video](https://www.youtube.com/watch?v=0Xdzez9L5iM&list=PLeC-4KM2-YJekeunVyJrE0iuXeCCJ8I5D&index=4)
- [Dyalog APL](https://www.dyalog.com/)
- [Kamila's GitHub](https://github.com/kspalaiologos)
- [Palaiologos](https://palaiologos.rocks/about/)
- [JavaScript Programming Language](https://en.wikipedia.org/wiki/JavaScript)
- [Java Programming Language](https://en.wikipedia.org/wiki/Java_(programming_language))
- [APL Programming Language](https://en.wikipedia.org/wiki/APL_(programming_language))
- [Assembly Programming](https://en.wikipedia.org/wiki/Assembly_language)

**[02] 00:10:07**

- [IRC Freenode](https://en.wikipedia.org/wiki/Freenode)
- [J programming language](https://en.wikipedia.org/wiki/J_(programming_language))
- [C Programming Language](https://en.wikipedia.org/wiki/C_(programming_language))
- [KamilaLisp Programming Language](https://github.com/kspalaiologos/kamilalisp)
- [Fork in APL](https://aplwiki.com/wiki/Train#3-trains)
- [Monadic, Dyadic and Variadic](https://en.wikipedia.org/wiki/Arity)

**[03] 00:16:41**

- [Based Array model](https://aplwiki.com/wiki/Array_model#Based_array_theory)
- [Depth operator in APL](https://aplwiki.com/wiki/Depth_(operator))
- [Introduction to Functional and Array Programming pdf](https://github.com/kspalaiologos/kamilalisp/blob/v0.3/doc/main.pdf)

**[04] 00:19:56**

- [Clojure Programming Language](https://en.wikipedia.org/wiki/Clojure)
- [Scheme Programming Language](https://en.wikipedia.org/wiki/Scheme_(programming_language))
- [Jacobian Matrix Determinant](https://en.wikipedia.org/wiki/Jacobian_matrix_and_determinant)

**[05] 00:27:28**

- [Garbage Collection](https://en.wikipedia.org/wiki/Garbage_collection_(computer_science))
- [Rust Programming Language](https://en.wikipedia.org/wiki/Rust_(programming_language))
- [bzip3 Data compressor](https://github.com/kspalaiologos/bzip3)
- [Burrows-Wheeler transform code](https://en.wikipedia.org/wiki/Burrows)
- [–Wheeler_transformInterpreted Computer Language](https://en.wikipedia.org/wiki/Interpreter_(computing))
- [ML Programming Language](https://en.wikipedia.org/wiki/ML_(programming_language))

**[06] 00:34:54**

- [Morten Kromberg Episode on ArrayCast](https://www.arraycast.com/episodes/episode21-morten-kromberg)
- [LZP Algorithm Charles Bloom](https://ieeexplore.ieee.org/document/488353)

**[07] 00:47:46**

- [Kamila's Talks, Lectures and Presentation](https://palaiologos.rocks/about/#talks-lectures-and-papers)

**[08] 00:51:42**

- [Dyalog APL Reverse Compose](https://aplwiki.com/wiki/Reverse_Compose)
- [PHP Programming Language](https://en.wikipedia.org/wiki/PHP)

**[09] 01:00:16**

- [Arthur Whitney](https://en.wikipedia.org/wiki/Arthur_Whitney_(computer_scientist))
- [ngn/k Programming Language](https://k.miraheze.org/wiki/Ngn/k)
- [Aaron Hsu Co-dfns](http://dl.acm.org/citation.cfm?id=2627384)
- [Aaron Hsu Episode on the ArrayCast](https://www.arraycast.com/episodes/episode19-aaron-hsu)

**[10] 01:06:17**

- [Dyalog 23 Talk by Kamila Szewczyk](https://www.youtube.com/watch?v=ToQoJ1Bbpus)
- [Henry Baker](https://en.wikipedia.org/wiki/Henry_Baker_(computer_scientist))
- [Contact AT ArrayCast DOT ComAmadeus - Mozart improvises on Salieri](https://www.youtube.com/watch?v=9jlQiHHMlkA)


<details markdown="1">
<summary><strong>Transcript</strong> (click to expand)</summary>

Transcript

Transcript prepared by Bob Therriault and Igor Kim

Show Notes

00:00:00 [Kamila Szewczyk]

My real motivation is just that I really want to learn how things work. I mean, I want to know how to solve this problem, right? And I feel like this is a good approach, the problem solving, because if you want to learn how to solve a problem, you don't necessarily just write the code and call it a day. You want to learn more about the problem. It's very educational and very fun at least for me.

00:00:25 [Music]

00:00:35 [Conor Hoekstra]

Welcome to ArrayCast episode 74. My name is Conor, and today with us, we've got our four panelists plus a special guest that we are going to get to introducing in a few minutes. First, we're going to go around though and do brief introductions. We'll start with Bob, then go to Stephen, then go to Marshall, and finish with Adám.

00:00:49 [Bob Therriault]

I'm Bob Therriault and I am a J-enthusiast.

00:00:53 [Stephen Taylor]

I'm Stephen Taylor. I know something about APL and q.

00:00:57 [Marshall Lochbaum]

I'm Marshall Lochbaum. I've worked with J and APL and BQN and Singeli and now k.

00:01:04 [Adám Brudzewsky]

I'm Adám Brudzewsky. I started with APL. I stick to APL.

00:01:07 [CH]

And as mentioned before, my name is Conor. I am a polyglot programmer, maybe not even compared to our guest today, but we'll cover that in a few minutes. A massive Array language fan and host of this podcast. Before we get to introducing our guest, I believe we've got three announcements. We've got one from Stephen who we'll start with, and then we'll go over to Adám for the last two.

00:01:29 [ST]

Yes, Conor, this month KX released kdb 4.1. [01] It's got some very interesting new features to make it more powerful, like multi-threaded data loading. But you know me, I'm only here for the poetry. I'm interested in the new language features, which include a dictionary literal syntax, pattern matching in assignments and Lambda signatures, and type checking and filter functions so you can write even more beautifully expressive code than you could before.

00:02:01 [CH]

We are, I mean, already on our list, we won't spoil the surprise because we don't have any of them confirmed, but we have some attendees of KXCon lined up. But now that you mentioned that, the pattern matching, that was from Oleg and Pierre's talk. They previewed this feature, I think, at KXCon 23. So we will have to get someone, whether it's Oleg or Pierre or someone else from the core KX team, if they would like to, we'll have to get them on because that pattern matching stuff was awesome. Link will be in the show notes. I'll go find the talk that talks about it. They gave a preview of that stuff. I think that one was recorded. I think they were all recorded. Anyways, and stay tuned. Hopefully we'll get someone from the KX core language team on to talk all about these new features. All right. I interrupted. Over to Adám.

00:02:50 [AB]

And yes, two more announcements. Right. So on April 11, there is something called DYNA. So that's like Dyalog North America, a meetup. And that's in New York. It's not so much for a reprogramming enthusiast, although they're welcome. It's really about big commercial systems, small commercial systems, and especially about moving from APL vendor to APL vendor, which is something that can be easy, can be hard. And what can be done about that? I think one thing that's really exciting about that meetup is the speakers. They're all APL experts and there's a chance also to sit down with them one on one. So if that's something, check our show notes for a link to that. And then in the previous episode, I mentioned a reaction video that I had made to the ProgLangCasts video about APL and related languages. And turns out that ProgLangCast just came out with a reaction video to my reaction video. So check that out. Link in the show notes.

00:04:06 [CH]

And I think it might be more than just a reaction to the reaction video, because I guess they did have BQN in episode four.

00:04:15 [AB]

But yeah, they continue with, they say they continue with BQN as well, because they didn't really have time in the last episode to get into that.

00:04:22 [CH]

We, we as members of the ArrayCast podcast panel and your host, we apologize. The video only came out like an hour ago, and YouTube only notified me of it like 20 minutes before we hit the record button on this. And I only was able to get through four minutes, which sounds bad, because it sounds like there was an extra 16 minutes in there. But then I had to switch over to a different lecture. Anyways, we will, we will, I don't, I don't know if we will all watch it, but I'm going to finish watching it afterwards. And we might have more to say in episode 75. But yes, links for all of that stuff. KX 4.1, the KXCon lecture about pattern matching and links to the meetup, links to the podcast from ProgLangCast, even though the YouTube channel is ProgLangBase, all in the show notes. And with that all out of the way, I am extremely excited to introduce our guest today. I believe her name is pronounced Kamila Szewczyk . She will maybe pronounce me in a couple minutes, or depending on how long my introduction is. And she is an extremely impressive programmer. At the age of 19, she's already an international conference speaker, apparently has been listed on Wikipedia for some crazy programming feats. She knows, according to her bio, C, C++, APL list, X86, 8051, 6502, Z80 assemblies, Perl, Java, LaTeX, the list goes on to mention others that she's comfortable with, Lua, TypeScript, ActionScript, Rust, Haskell, OCaml, and then is learning a bunch of other languages. And this is just the stuff she knows. We will link to her Dyalog23 talk on the APL array notation. I got partway through watching that talk. And while she was interning at Dyalog, she did a ton of stuff, primarily on the APL array notation, but also she implemented quad diff, she implemented reverse compose, which potentially means we might be doing, you know, Tacit 5.5 or whatever, you know, mini Tacit episode in the midst of this, and a bunch more stuff. On top of that, she's got like a bajillion projects. We will link to her About Sort of Me website. Also, I don't know how, I'm gonna attempt, and then once again, Kamila can correct me if I've said it incorrectly, your online alias you typically go by is Palaiologos. And I'll stop there. I'll let her correct the pronunciation of that. And there's so much stuff to talk about, but yeah, maybe I'll throw it over to you. You can correct my pronunciations and maybe give us a sort of brief background on how you have become so accomplished at your age at all of this different stuff, 'cause I am dying to know.

00:06:55 [KS]

Well, that was just mostly by curiosity, right? It's also what's driven me towards APL. It's like I was particularly interested in the right programming or, you know, all the features of right languages that you see. To me as a maybe 12 year old, 13 year old, it was just interesting that it was sprinkles and it was rather compact and cool challenges. So I thought that maybe I should learn it and see if it's comfortable to work with. I think it was a great decision overall.

00:07:23 [CH]

At 12 or 13. Wow.

00:07:25 [KS]

Yes, I really enjoyed the APL. I think that it's really changed me as a programmer because I really find myself very productive when I think in terms of very high level problems, right? And I no longer think of individual steps that I would write in an imperative language to accomplish a task. And instead I think in a high level view of what really needs to be done. For instance, I was working on a project, which is a neural network that can model Java code. And the point of that was to create the golfing language to be used in PPCG in order to beat, hopefully, all the existing golfing languages. So in order to train a neural network, you need to have a data set and a verification set, right? And you want to harvest the data set, for instance, using an SQL query to the CodeGolf database to get all the Java programs. And then you have to filter them, right? And to me, it seems kind of obvious how you would filter them. But then I realized that if I wanted to write the filter in Java or C, it would be extremely long because there are certain criteria, right? For instance, you want to extract the actual code snippets from the posts, which are a CSV file. You want to remove the ones that have too long strings that are generally not very representative of the actual Java program, right? And the APL program that cleans up the whole thing is nine lines. And I have really never felt as productive as I do with APL. I mean, even if you look at the history of my projects, you'll notice that all the things that I made have been made after my initial exposure to APL. And a lot of the projects that you see listed that don't have the source code attached have been in some ways modeled with APL.

00:09:16 [CH]

That is very interesting, especially given that you've done projects in assembly, because you've gone from the most, I mean, other than ones and zeros, basically the lowest level of you need to code in instructions all the way to the highest level. And you've come out of this experience saying that, "I like APL the best by far just because I don't need to think in these tiny steps. I can think at this extremely high level and understand what's going on under the hood, but be way more productive because I can avoid some of the detail and not spell that stuff out and just work in these high level operations."

00:09:54 [KS]

Yes. There's actually a lot of high level operations that you have to execute in your head if you want to write performance assembly code by hand. It's a good but technical example of dividing by constant in assembly. It's usually done through module arithmetic with a shift and multiplication. And how do you compute it is basically just a very complicated math formula, but you can write an APL program. And then you feed the divisor and the generator to the assembly program that divides by the given value very quickly.

00:10:25 [CH]

That's amazing. I mean, and so how, you said at 12 or 13, you started messing around with APL and falling in love. Were you programming already at that point for a number of years? Or were you going through some course that was at school that was teaching you a bunch of stuff? Or was this all sort of on your own? Or how did you get to this point?

00:10:43 [KS]

Well, I have never talked to a person who could actually program until I was maybe 18, like in person. I've talked to people who could program by the internet. But well, my first introduction, even before Adám, was on IRC, on the now unfortunately dead Freenode network. [02] It was an esoteric channel where people were discussing some sort of a weird combinatorics problem. And then I thought, "Oh, well, they're verifying their computations using that weird language." And they linked me the channel of J software on Freenode. And I was really keen on learning it, but I wasn't mature enough to appreciate array languages, I think.

00:11:27 [CH]

And what age was this?

00:11:27 [KS]

Oh, I don't even remember. That was maybe 2019.

00:11:30 [CH]

2019, Okay.

00:11:32 [KS]

Well, it was very difficult for me to appreciate because I was mostly a C programmer. I mean, I've got a very long ways since then, but I never really focused on algorithms or how you would write mathy code. I wasn't even that good at math before I learned APL. But APL really gave me the insight into how the theory of computing works. And you could really see this throughout the years, all the projects I've done. For instance, KamilaLisp is a somewhat controversial language, a research language, which I made. It is built entirely on the premise that I want APL to be a math language. I don't want it to be a computer language necessarily.

00:12:16 [CH]

Interesting. So tell us more about this KamilaLisp, because I think that was going to be one of the main topics. And I listed it under the number of projects. But yeah, tell us, KamilaLisp, is it a Lisp? Is it an APL? Is it both? What is KamilaLisp?

00:12:29 [ML]

Jumping straight into the controversy, I was going to say there wasn't any, but you found it.

00:12:35 [KS]

Yes. Well, initially I wanted to start with something that is a bit like APL, but then I realized that APL syntax is sort of beautiful, but difficult to modify. If you want to change APL syntax, you start adding a lot of stuff that's incompatible with APL. And then you end up with something that's not really an APL either. And I really wanted to avoid the whole syntactic part of APL, which is arguably very important for APL, but not very important for a research project like mine. So I decided to settle with a Lisp framework. Obviously, a lot of the scheme code that you write will be probably valid KamilaLisp code, but KamilaLisp doesn't actually provide you with lists, for instance. It provides you with arrays. That changes a few things, but it's possible to map scheme operations into array operations. And on the other hand, it has tail call optimization like most schemes, but it doesn't really encourage the Lisp programmer point of view, where you have small recursive functions that accomplish a simple goal. Instead of a recursive function, you would probably prefer a reduction or a filter or some sort of other operations like expand, compress. So it's really hard to throw it into any bucket really. I think that the easiest way to categorize it would be a Lisp-like array language.

00:14:09 [CH]

So can you talk to us a bit about what it looks like? Because I looked at the GitHub repo readme, and it has a couple examples. One of them is like a SKI calculus with some pattern matching for the SKI combinators. And it looks very, very Lispy. It's got like a parenthesis, defun, SKI, variable X, and then a bunch of parentheses everywhere. But then right underneath that, it has a example of quote unquote list operations and point-free programming. And this looks very, very different than Lisp. There's not a single parentheses. And you can see what looks kind of like an iota glyph, a row glyph for sort of iota and reshape. And then there's what kind of looks, because it has the APL and Haskell underneath, and it kind of looks like some kind of fork syntax and some composing. So I'm assuming both of these are valid KamilaLisp. Is that correct?

00:15:07 [KS]

Yes, that's true. What you're seeing is a shortened version of a KamilaLisp program, because it's something that certain Lisps implement, whereby if you don't want to type like 30 closing brackets at the end of your expression, you can use a backslash to say, "There we open a paren," and the paren closes at the next closing paren.

00:15:29 [CH]

Oh, really?

00:15:31 [KS]

Yes. And the forks in Kamila Lisp are forky trains in APL. But again, Kamila Lisp lifts the whole notion of having only two arguments. So you can have variadic forks, which is one of the recursive functions where you compose the functions in a way such that the middle operation of the standard APL fork gets the result pre-processed by each of the functions that follow it in the fork on each of the arguments.

00:16:08 [CH]

Right. And that covers both the monadic and dyadic fork, and then any number of arguments, as long as... Yes. That is very cool. So that's like a superset of the forks that you get in BQN, APL, and J.

00:16:19 [KS]

Yes. It also implements the proposals from Dyalog, and I say quote-unquote "implements." Well, actually, while implementing Kamila Lisp, I have noticed a lot of implementation problems that stem from my design choices that I made previously. I regret some of them.

00:16:38 [CH]

It happens.

00:16:52 [KS]

For instance, I've decided to settle on the based array model, [03] which some people might not necessarily agree with. At the time, I thought that the based array model makes a bit more sense for my research project than the floating array model. But then I noticed that I can't really model inner product without breaking a lot of stuff, following Roger's implementation that you can see on APL wiki. Another problem that I had is... Do you know the APL step operator that Adám proposed? The step operator?

00:17:08 [CH]

The step operator or depth operator, I think it's been brought up once or twice on this show, right?

00:17:15 [ML]

We should probably describe it.

00:17:18 [CH]

I was looking for confirmation from Adám.

00:17:19 [AB]

Trying to play playback or 70 something episodes my mind here quickly too.

00:17:23 [CH]

Whoa, we talked about this. Everyone has to know everything they've said up until now.

00:17:29 [AB]

The depth operator is just applying a function either at a certain number of steps into an array from the outermost level or at leaves of a certain minimum depth, and then keep going through the array, traversing the array.

00:17:45 [ML]

So it's a lot like the rank operator, where in the rank operator, you say what rank you want to operate on. But in the depth operator, you say what depth you want to operate on.

00:17:52 [AB]

And you can combine the two operators for various effects.

00:17:56 [KS]

Yes. It's very easy to notice how the depth operator works in the monadic case, right? It's a bit more difficult to notice how it works in the dyadic case, right? Because of all the mappings and different boxing. But the problem was that KamilaLisp has variadic functions. And implementing the variadic depth operator, in turn, turned out to be an extremely difficult task, at least for me. And so far, I haven't found a convincing model for that either, actually. So I've decided to settle on a depth operator that models the shape of the first argument, and then sort of coerces the rest of the arguments to play along. Which is, again, not how, for instance, map works, because the map will adapt to the shape of both arguments, right? It will not follow just the first argument shape. But on the other hand, implementing depth the same way as map is very complicated. I'm not even sure how you would do it now. But that includes a small discrepancy. And because it's just a research project where I try to combine various ideas, KamilaLisp might be a bit confusing to someone who is not familiar with programming. But I tried my best to convey some stuff about KamilaLisp in this small book that I wrote. It's present as documentation in the repo. It's, I think, around 90 pages. And it teaches functional programming and array programming using my language.

00:19:23 [CH]

This is under the doc-- oh, yeah, doc and then slash content. And there's a bunch of tech files. Is that accurate?

00:19:31 [KS]

Yes. There should be a PDF somewhere, I think.

00:19:34 [CH]

Oh, yeah, yeah. Just under doc slash, and then there's a main.pdf. Yes. Very cool. I will definitely be reading this. Well, I have two quick questions. Well, hopefully one that's quick, and then maybe the other one's not quick. The first one is, you mentioned that certain LISPs do this thing with the backslash that controls opening and ending parentheses. Are there common LISPs? Like, I know of Clojure, [04] and I'm pretty sure it doesn't have that. I don't know Scheme super well, but I never came across that. Like, what's the most popular LISP that does this kind of technique?

00:20:06 [KS]

I can't say what off the top of my head. But it's very common in cases where we have restricted input. For instance, if you've ever used a TI calculator, which runs TI Basic, then TI Basic will automatically put the closing parents at the end of the expression when you decide to evaluate it.

00:20:23 [CH]

Ohh interesting. I didn't know that.

00:20:25 [KS]

I've seen the same idea in some LISPs. I actually feel bad about not recording which LISP in order to credit them.

00:20:32 [CH]

It's OK. Actually, that makes me feel better, because I don't like to think I'm an expert in stuff, but I've touched enough LISPs that I was like, "Oh, wow, I've never..." If you were to say Scheme, and then I never came across that, I'd be like, "Wow, I clearly didn't learn Scheme well enough. I didn't go down the Scheme rabbit hole." So that's totally OK. The second question is, so you mentioned that the depth operator was a lot trickier. If not, you're still struggling with wrapping your head around how to implement that. Are there certain primitives or operators in Kamila LISP, or however you refer to them, that because of the variaticness of functions, you were able to unlock some cool functionality that isn't possible in an APL or BQN because we're limited to only dyadic functions? Do you have any examples of stuff? Because I imagine you must run across some stuff that like, "Oh, this is really cool." For instance, you can use forks with the two outer functions having any variaticness. I'm not sure if I've ever run across a case where I've needed that, but that's probably because I know that I don't have access to that, so I'm not looking for that case. But if I did have that tool, it probably would come up now and again. Do you have any examples of that or not really?

00:21:49 [KS]

Well, I don't really have that many examples of this on hand, but you have to also remember that the language that you use forces a thought model upon you, right?

00:21:58 [CH]

Yes. Exactly..

00:22:19 [KS]

So because you're forced to have only two variables, it's natural for you to not seek to use three variables. And I distinctly remember having quite a lot of examples like this back when I actually invented this syntax, but they're kind of difficult to come up with now. I think there was some code in the convolution code example that I gave in my book that used them.

00:22:25 [ML]

One thing I'm thinking of is that, I don't know if KamilaLisp does this or not, but reduction on multiple arrays at once is pretty neat. So you could define a reduction that takes any number of arrays, and when it's called, it reduces the function on the... It calls the function for the reduction on the current value and a new value from every one of these arrays. So you can take more inputs in. That's one thing that you could do.

00:22:58 [KS]

Yes, that was actually something I was thinking of, but I didn't implement this feature. Well, there's a lot of code in the repo, right? I've worked in this for a pretty long time, and the scope of the project is somewhat big. And given that it really focuses on math, I spent a lot of time working primarily on the math utilities. There's a few screenshots you can see in the releases tab, which show you how to integrate, how to perform indefinite integration of functions. They measure the numerical computation capabilities of KamilaLisp. There's something with Univate Tether Series that you can expand of a function. And there's also an example of deriving the Jacobian matrix and its determinant for the polar to Cartesian coordinate transformation. There's a KamilaLisp that can prove that the determinant is precisely equal to r.

00:23:53 [CH]

All right, so maybe one other question. I found that there is a chapter or section, 1.5 of the book, is a chapter called Function Composition. And so we have the fork. Do you implement all of the kind of.. because I know you worked on reverse compose in DyalogAPL. Do you have all of the kind of compose and.. I don't know what they're called.. the top and over composition functions? And even more? Or do you just stick to what's in APL?

00:24:27 [KS]

There is an over. There's definitely an over. There is not an atop, because there doesn't need to, because of the Lisp syntax. There is a compose, the regular compose. But I didn't really add that many composition operators, because I just didn't find a necessity. Because Tacit in KamilaLisp works slightly differently from APL. Where the compositions were explicit, right? Now that you no longer have two arguments, it's not as cumbersome to express using the variadic fork syntax or nested forks or- or you can really come up with.

00:25:03 [CH]

As you have variadic forks, that enables you to do more with them, is what you're saying? So there's no need for a richer set of different composition patterns defined by different symbols, is what you're saying? Yes. Interesting. Yeah, I'm definitely going to have to go and.. well, here's the next question. How do people go and play around with this? Do you have to go and locally just do a git clone and build locally? Or is there a?

00:25:28 [KS]

Well, if you go to releases tab, there is usually a jar file attached to the assets, together with a digital signature with a PGP key. You can run it with a --ide function, which will bring you up an IDE that I wrote with Swing across a week and a half or so. But uh. It's not very polished, but it still has some interesting features, such as project management, compressed project files, a Tiling Window Manager, and some other features. So you could also use that. And it was also a small experiment on my side, because I was used to using Write for managing my APL programs. But I never really felt comfortable with the idea that my code resides in the APL interpreter. In my opinion, it makes more sense if the code is attached to the project file that is loaded by the IDE. And then, for instance, the parsed data is being sent to the interpreter so it can execute it. This is the premise on which the remote IDE bundle of KamilaLisp works.

00:26:29 [CH]

And so when you mentioned Swing 2, it made me realize that this had to be implemented in Java, which I just went and checked and is the case. Was there any reason you chose Java as opposed to any of the other 100 languages that you know?

00:26:43 [KS]

Well, it mostly came to be because of the many different iterations of KamilaLisp. As you can see, it's version 0.3. There was a 0.2 and a 0.1 as well. So the 0.1 was also written in Java, and it featured lazy evaluation, among others. But at some point, I became kind of comfortable with the GC pressure of KamilaLisp. And then I decided that I might rewrite the whole thing in C++.

00:27:11 [CH]

Oh wow.

00:27:12 [KS]

And I got a chunk of work done, but I never really liked my runtime design. I felt like I can never be really satisfied with a runtime that I can put together in the free time I have from school and during vacation. For instance, one sore point of the language was garbage collection. [05] I mean, obviously, if you have persistent data structures, your language is going to generate a lot of garbage. But it's somewhat easy to alleviate, right? You just need a good garbage collector with generations. The first generation has to be copying in the nursery and then your space for old objects. But that's kind of difficult to implement efficiently, right? I mean, if you look at the source code of G1GC for Java, it's extremely long and somewhat complicated as well. And I never really felt good with my implementations of the C++ runtimes. So I decided to just go back to Java and experiment a bit more. And the other reason is that I feel really productive in Java. And that's probably not representative of most of the people who work with Java, I'm certain. But this feels very unobtrusive to me. And it's probably my second favorite language for actually writing prototyped in.

00:28:26 [CH]

Really? Java? And assuming the first is APL? Yes. Wow. And are you out of curiosity, because now these days, I think they're up to what, Java 21? It might even be more modern than that these days. Are you in 11, 17, 21?

00:28:40 [KS]

I turn on the newest.

00:28:42 [CH]

Wow. And is that is your feeling productive in Java because of some of the new features that they've added in 14, 17, 21? Or is it just because you're comfortable with the language and you like it for insert reasons?

00:28:57 [KS]

Most definitely it's because, well, half is because I feel so comfortable with the language, right? It doesn't really make you think that much about things that are not your ideas. I mean, I don't really like to, I really don't like to prototype when I don't know what I'm doing. I mean, it's normal to not know what you're doing, right? When you're starting out, you don't know what you're doing. And I don't know what I'm doing. So it's difficult for me to model a memory model for what I'm going to do. I don't know what object is going to own any other object, right? But I still have to model the whole object tree so that I don't have memory leaks, right? Or all the objects are alive when they need to be. Right. But then there is a requirements change. I think that I can implement in a better way. And then there's a problem of how do you rearrange this object tree to accommodate it for the change without having to rewrite three quarters of it into some other style frantically while trying to also do other things. Right. And JavaScript doesn't, sorry, Java doesn't make me think of all those things, right? Yeah. I mean...

00:30:03 [CH]

No, definitely true.

00:30:05 [KS]

I just think that my Java code is remarkably good. I think that it's actually pretty hacky. But given that I could research my ideas and verify them in such a short time, it's very remarkable.

00:30:19 [CH]

Yeah, definitely. I mean, GC language, they eliminate a whole set of challenges that you need to think about at some point, usually pretty soon. And in a sense, that's kind of similar to APL. You know, APL eliminates things like, you know, loops and indexes. And I don't have to think about that stuff. I just can work at this level. And it eliminates a certain set of problems that exist in other languages.

00:30:43 [AB]

And also type conversions as well for various numeric types, for example.

00:30:47 [CH]

Yeah, yeah, as well. Yeah. I'm interested, I think Rust was on the list of, not to take a complete left turn, but I guess it is a complete left turn. Because Rust is a language that does the opposite of what Java is doing. They introduced a whole new facility called the borrow checker, as you know. Yes. For this kind of like, you know, oh, it'll save you from all these problems, but you have to now think about lifetimes and whatnot. So I'm curious, like, what are your feelings about Rust as a language compared to C or C++ or even Java and APL?

00:31:22 [KS]

Well, if I were to put that to a high level, right? Suppose the Kamila list, right? I would probably choose something that's less obtrusive and generally ends up with like a minimum viable product as soon as possible so that I can see what works and what doesn't. But at the other end of the spectrum, there's the need to have C code, right? And well, the other field that I work with that I'm somewhat known for is data compression. And in data compression, there really isn't that much object wrangling as you'd think. I mean, there's a buffer, the input buffer, there's the output buffer, there's a bunch of auxiliary buffers or some simple data structures. But besides that, we don't really see that many complicated object graphs that would benefit a lot from Rust, right? I mean, Rust does, for instance, implicit bounce checking. And that would completely hamper the performance of my code. It would make it completely unusable. But it would make it safe. I mean, I wrote bzip3, which is the data compressor that sometimes outperforms mostly all the available general purpose data compressors. It's based on the Burrows-Fuller transfer and a very simple context model. So I wrote it when I had my high school finals during the exact month, and I finished it in a single month from the start of how I wanted to go to work into having a somewhat finished product. And I made a lot of bugs, but I ultimately managed to fix them. And my current feeling is that Rust wouldn't have prevented me from having made those bugs. So I'm somewhat interested in Rust, but I don't really see an application to use it myself. I'm sure that if I had a reason to use it, I would happily use it.

00:33:16 [ML]

Yeah, well, for an interpreter specifically, it's like, so if you implement a function in the interpreter, it's going to take some value in the language in and put some value in the language out. So all this memory management stuff, it's like, well, you don't know where your input came from. You don't know where your output is going. So you can't say anything at all about how this function interacts with object lifetimes or anything. So Rust's facilities for making sense of that and organizing that are just not powerful enough for an interpreter. I mean, yes, you can still write safe code with Rust, and Rust has a lot of other features coming from the ML family that are pretty nice for interpreters, but the memory model is just like, that's not helpful to write a programming language with.

00:34:04 [KS]

For instance, Dyalog could never be written in Rust, because if you have a compacting garbage collector, then the pointers start moving around your feet. And it's not like Rust has any facilities to stop you from making errors regarding those. And also the pointer provenance of Rust, if I remember correctly, will not guarantee that your local pointers are updated when the garbage collector decides to move some objects.

00:34:33 [ML]

Yeah, for Dyalog, I mean, I think it makes a lot of decisions just based on the fact that it's written in C. So it's hard for me to say that that's necessarily-- like, there are probably better approaches that you would use if you were working with a language that's not so tied into the idea of pointers.

00:34:49 [KS]

Yeah, I mean, when I first when I was going to intern at Dyalog, Morten [06] suggested me to make the array a notation evaluator. And at first I thought, I can't really commit to it, because I haven't seen the code, and I'm prepared to be a little scared. But after I joined Dyalog, and it's like after the first few days of interacting with Dyalog code, it's actually one of my favorite code bases. It's very pleasant to work with, and despite being somewhat old, it's actually very easy to hack on. I mean, on the second or third day of my work, I had actually something tangible that you could show to someone.

00:35:29 [AB]

Yeah, which you did show to me. But maybe it's more about your programming skills than about the Alex code base. I'm not sure.

00:35:40 [CH]

Yeah. I'm still shocked. Like, I'm looking at the bzip3 GitHub repository, and you've got a matrix of what looks like 60 different Linux installations, or I don't know if they're all Linux or some of them are other. And you've got benchmarks of the Calgary corpus, the Linux kernel sources, and the Cilicia corpus, and bzip3-- or sorry, is it Cilicia? Cilicia. Yes. And you've got benchmarks, and you've outperformed every single bzip2, gzip, lzma. I don't recognize half of these other than bzip2 and gzip. And you did this while you were in your final year of high school studying, or maybe not studying for your finals. I guess potentially you didn't need to study, and you were just working on-- like, this is phenomenal. I don't know. All I did was have my head in a book, trying to do well on my exams, and somehow you've found time to not only write a compression algorithm, but write a compression algorithm that was a successor to an already quite popular compression algorithm, and then outperform it and a bunch of others. Yeah. Mind blown.

00:36:56 [KS]

Compression is a little relative. I mean, for instance, my code, by virtue of being based on the BuVT and context-bundling, is somewhat symmetric, meaning that the compression types and decompression types are similar. And some people cross it out only for this reason. And, well, it's true if you consider an example of having a web server that compresses a payload and it says it's declined. Of course, the file is going to be decompressed many times and compressed once, so it makes sense for the compression to be long and the compression to be short. But there are many examples, many cases, in which compression is as frequent as decompression. I mean, arguably, if you have a dynamic payload on the website, it's going to be compressed on the server and decompressed on the client. It's not like you're going to send the payload multiple times if it's dynamic. And I'd really like taking a lot of credit for this, because all of the ideas were already there. They just needed someone to put them together. And it was really not that difficult. I mean, for instance, the LZP algorithm was already invented by Charles Bloom. I've learned about it from his paper. So what this whole codec does is eliminating the edge cases, or rather the edge cases, meaning files with weird distributions that other compressors would work better on, and trying to equalize it as a general-purpose codec. So for instance, you might notice that if you compress a text file with gzip, it doesn't really compress as well as with bz2. And the reason for that is-- well, there are many reasons, but Lempel-Ziv algorithms, gzip, or lzma, or whatever, generally model data that has some sort of a pattern. For instance, the last occurrence of a certain letter is a fixed distance at any record point. But if you have a sentence and you encounter the letter A at some point, you can't really model where the letter A was previously seen. But if you have, for instance, a binary file, which is like a, I don't know, 24-bit color image, that if the pixels repeat, they're going to always repeat on a certain boundary. This is also what Lempel-Ziv codecs exploit. So it's important to think of codecs as geared for a particular purpose. All the examples you see are mostly just corpuses or text, for instance, source code. That's what bzip3 will do. It doesn't really excel at binary data, unfortunately.

00:39:29 [CH]

I mean, it sounds like you're being incredibly modest. You know, Steve Jobs took a bunch of stuff that existed and then put together the iPhone. And I'm not saying this is like Steve Jobs, but he didn't--

00:39:37 [ML]

With just bare hands.

00:39:40 [CH]

Yeah, he didn't acknowledge any of that prior work and was just like, well, you know, it's a bicycle for the mind. And everyone was like, ah! And, you know, obviously there's pre-existing stuff, but it's still very impressive. I think these days there's very rarely anyone doing completely original work and not standing on the shoulders of giants of previous work, et cetera. So caveats made, it's still extremely impressive that you've done this work and not only did it, but just at a time, I think, when most of us were at other priorities of just trying to graduate high school and university applications and whatnot. I'm not sure-- we can pause if there's questions from other panelists, because I feel like there's so many different directions, because you have so many other projects. You've also got sort of the work at Dyalog that we haven't talked about a lot in terms of the array notation and quad diff and reverse composing and all that stuff. But I'll pause before we start a new topic if there's questions from the panelists that haven't been asked about the stuff we've been talking about so far before we move to a next chapter or if someone wants to suggest the next chapter and not just leave it up to the dictator that I am on ArrayCast.

00:41:03 [BT]

A benevolent dictator.

00:41:05 [CH]

I'd like to think so. I'd like to think so. But I don't think a lot of dictators are thinking to themselves, well, I'm definitely malevolent.

00:41:13 [ML]

I want to say with the iron fist more tacit.

00:41:18 [AB]

I don't know. It's not really a question. I just like to point out for the rest of you who haven't seen Kamila write C code in real time, because there might spur some interesting discussions here. I've both seen Kamila write C code at the office and on my couch at home and at the Dyalog user meeting while-- I don't remember if it was a break. I think it was a break between talks or something like that. Maybe it was in the middle of a talk or also in the middle of a talk. I mean, it's a whole different world. I don't know. I don't understand how you can program like that. Like the physical obstacles, she has this little laptop and she's got these really long nails. And it looks very awkward to me. I can barely push the buttons properly on the keyboard with the nails being in the way. And then I'm looking. Obviously, I don't understand this gobbledygook they call C. Just weird symbols and stuff. But then she's just selecting stuff in the editor and just pasting a whole bunch of it, the same thing, and then making some modifications to each one of these copies. And then, oh, and now it runs. And that was on the couch. At the user meeting, she was like-- she must have been bored by whatever was going on at the time. So she just added another primitive to Dyalog on the fly like that. I would like to know, how do you even go there? How-- like, I didn't even meet a person in real life that was doing programming for years. And so you're just busy with things and you get better at it? Or were there influences, even though if they were virtual, that helped you to get to that kind of level of programming? Or you're just very clever naturally?

00:43:15 [KS]

I think that I got so much good at programming by wrangling my head at it. And I think there's a particular reason. I mean, it gets with practice, right? The thing you mentioned about working with the Dyalog code. Well, a lot of the issues that you don't see in APL, probably in C code, right? When you deal with strings in APL, you don't really care whether they're Unicode or ASCII or whatever. They just come from somewhere and you deal with them. But in the C code, as you mentioned, I kept copy-pasting stuff all the time because I had a whole switch for the character type, whether it's 8-bit, 60-bit, 32-bit. And that took 400 lines of code. That's the same thing.

00:43:56 [CH]

So there's no secret. You just-- I mean, I heard a quote once that the difference between junior and senior programmers is that a senior programmer is just willing to sit for like 10 hours in a row and bang their head at a problem. And they just-- they know that they can solve it. It'll just take a certain amount of time. And a junior programmer, they get like 30 minutes into it and they're like, "I just-- I probably don't know how to do this." And they give up. And that's the only difference. It's not like a matter of skill. It's just a matter of like belief in one's ability. If I keep at this, I can solve it. And I don't know if that's like actually-- I think the person was joking. But it kind of resonated with me. It's like a lot of the times, I know I can solve this. And it's like six hours later and I'm still trying to diagnose some diagnostic. And then eventually it works. And then you get up and you run around the room. But like there's no real skill level difference other than like, I know within an amount of time I can get this. And it kind of-- what you were saying, Kamila, reminded me of that. It's just when Adám asked you, "How did you get so good?" And it's just, "Oh, I just banged my head at problems and got better as time went on."

00:45:00 [KS]

My real motivation is just that I really want to learn how things work. I mean, I really approach problems thinking I can solve it. This is simple. More, I keep thinking I want to know how to solve this problem. Right? And I feel like this is a good approach, the problem solving. Because if you want to learn how to solve a problem, you don't necessarily just write the code and call it a day. Right? You want to learn more about the problem, about the happy paths and the sad paths of the problem, and about the variance of the problem. It's very educational and very fun, at least for me.

00:45:38 [AB]

So you spend a lot of time researching the problem space before you even start coding? Or while you're coding?

00:45:46 [ML]

Yeah, I mean, this is kind of the-- you said there's no secret. And I mean, yeah, there's no-- it's not like there's one thing that'll make you a great programmer that's hidden. There are a thousand things that you should know if you want to program well. And none of them are secret. But you need to know at least a substantial portion of it. So it's-- committing a lot of time to it is one thing.

00:46:09 [ST]

When you finally did meet somebody who was a programmer in person, in real life, was there anything different that happened? I mean, you'd come a long way just over the internet connections before that. So once you met someone in real life, was there anything different there?

00:46:25 [KS]

Yes. I think that once I went to uni and I started interacting with other programmers and started learning the stuff I never really had an occasion to learn. I become more well-rounded, right? I mean, it's difficult to convey. But if you're an amateur programmer like me, you generally tend to research things that you find interesting, right? You don't really care about what you should learn. You care about what's fun. And if you go to university, it's the other way around. The things are not necessarily that fun, but you should learn them.

00:47:00 [AB]

Ah, yeah. And if you're having fun, then you have a better incentive to go and just do... It's almost like science for science's own sake, yeah. Research how the world works for its own sake. And then it turns out you're better equipped. - Yes. - So I guess all the universities, they should just kick out all those course requirements and just say, "Here's a computer. Go have fun. Learn stuff."

00:47:23 [ML]

Well, you need something that's fun overall, but that kind of embeds in all the non-fun bits that you need to learn in a way that you don't notice.

00:47:33 [KS]

Yes, most definitely. When I was working on my data compression book, [07] I was thinking, well, I was definitely that good at statistics, right? But I knew the very basics to get myself around, but I really discovered that I quite like them. And then I went to a university course that taught me statistics. And I thought to myself that if it wasn't for the fact that I had the resources before, I would have been completely lost. And yes, that just proves your point.

00:48:03 [ML]

Yeah, I think I've learned a lot of statistics through benchmarking and some adjacent stuff. With sorting, there's some statistics around sampling the input that you want to sort to figure out. You can sample it randomly and figure out if certain problems will occur with some algorithm. And so, yeah, I've gotten a much better understanding of statistics by saying, "Well, I want to know whether this property holds and I have this information. How do I figure it out?" And that can get pretty heavy on various statistical methods.

00:48:37 [KS]

Yeah, I also liked the randomized algorithms part of my algorithms course. - Oh, yeah. - So we were basically discussing how many comparisons does an insertion sort make in the expected case. If, for instance, the list is uniformly random or whatever. It was pretty fun. I quite like it.

00:48:55 [CH]

All right, so here's...my mind is still being blown. So you've got your first book, which we actually haven't even mentioned the title of. The title of the book is "An Introduction to Functional and Array Programming." And if I saw that, if I was walking through a bookstore and I saw that, I'd be like, "Holy smokes. The Lord has shone down the sun on me and placed a book here just for me." So that's the title of your first book. And also, this is none of this. On your already amazing resume of an "About Me" page that lists all your stuff, it doesn't mention this book. Just casually, it didn't make the short list of stuff that you've done, has written a book. And now you casually mentioned you have...I'm not sure if you finished, right? Do you have a second book on data compression?

00:49:38 [KS]

Yes, I work on a small book on data compression. It mostly explains the basic methods such as static minimum redundancy codes, context modeling, elapsive methods. And well, I don't consider myself an innovator in data compression, but the reason why I'm making this book is it was just so painful to research this all myself. And I feel like I would be doing a service, I think, to a lot of people just by giving them a book which explains the concepts, gives them exercises, code samples of all the stuff that you need to know to get started. I have approximately 100 pages now. And I plan to work a bit during my spring break, which is coming up very soon.

00:50:22 [CH]

And is this the...actually, there is a section that says talks, lectures, and papers. Is this the statistical data compression pending or is that a paper and not a book?

00:50:33 [KS]

That's a talk I'm going to give on April 22nd.

00:50:36 [CH]

So you've got one completed book and you're in the midst of finishing your second book.

00:50:40 [KS]

Yes, I also before wrote a small booklet, which is like approximately 60 pages on how I implemented the Lispy-Malbulge, but I wouldn't consider it a book. It's just more like a funny explanation.

00:50:52 [BT]

I guess that's what you do over spring break.

00:50:57 [CH]

This is like, you're giving me like, you're like increasing my imposter syndrome as this interview goes on, as I discover, "Oh yeah, the book section, I just thought would be too much. I left that off of my About Me page because, you know, it didn't make the cut." Wow. All right. Well, you know, the journey continues. We still have hopefully a little time left. If we're allowed to start kind of a new topic, it's been mentioned a couple of times. You interned at Dyalog previously and you worked on a ton of stuff. So maybe I'll leave it up to you. I'm super curious about Reverse Compose because I know Adám has referred to it in, I want to say at least a couple of the upcoming features when you do like a Dyalog 18.0 talk. There's always a section that says, "For future releases." And I think Reverse Compose [08] is one of those things. But yeah, maybe if you want to talk about like some of the work, whatever you found most exciting when you were at Dyalog and your time there.

00:51:58 [KS]

Well, I had a really good time. I really liked it at Dyalog. I think that was a very good experience for me. I've learned quite a lot. And I met some people to which in some ways I look up to. I'm sure that a lot of people at Dyalog will remember me as the most unlucky intern to have ever been at Dyalog.

00:52:20 [AB]

Why is that? No, the community just keeps having incidents and accidents from public transit delays to sleeping on steps and et cetera.

00:52:34 [CH]

So nothing to do with the code base, commuting and going between floors.

00:52:40 [AB]

Did not by mistake erase our entire code base or anything like that. Nothing of the sorts. Well, you only ended up in the hospital once, right? While you were interning.

00:52:51 [CH]

Yes. Hopefully it's not because you were programming in your head or something like that, which I probably assume you do from time to time. You don't have your computer, so you're just...

00:53:00 [ML]

She was programming in her head, but it's not because she was programming in her head.

00:53:03 [AB]

She's always programming in her head. That doesn't matter. Kamila, do you even program while you're programming?

00:53:11 [KS]

I think so, yes.

00:53:12 [AB]

I figured.

00:53:14 [CH]

I'll let my fingers type out the code that I have stored and I'll work on the next problem.

00:53:20 [KS]

Actually, it's something that I've experienced a few times where I'm faced with a problem and I intuitively know the solution, so I just type it out. Then I convince myself it is correct, because at first I don't understand it. I'm not sure it's just something weird about me or whether it's a universal experience. Have any of you experienced that ever?

00:53:39 [CH]

No, I think you're operating at a level, at least I'm speaking for myself personally, not the rest of the podcast panelists, but I think you're operating at a level, a couple of rungs, if not on a whole different ladder than where I code at.

00:53:54 [BT]

It's not an experience I'm familiar with, that's for sure.

00:53:58 [AB]

We're sitting here in ND space looking at a bleak projection of your N plus something space.

00:54:07 [CH]

Was Marshall, were you going to say that you've...

00:54:09 [ML]

Well, I do go sometimes from understanding how it works in a very roundabout way to understanding why it really works.

00:54:17 [CH]

Steven, you're the last one. Marshall's the closest to being on the same ladder or whatever this analogy. I was thinking of Interstellar where, what's that guy's name? Matthew McConaughey, he's in some other dimension that the people can't see. Maybe that's what Kamila is here. Marshall's up there, kinda. I'm definitely just in 2D land or 3D land or wherever the rest of us are.

00:54:39 [AB]

It happens to me with other people's code that I think I understand it somewhat, and then I get some better understanding of it, like really understand it so I can explain it right. But my own code...

00:54:50 [BT]

I think that I was going to say, I think the difference is that I'm not usually writing it before I understand it.

00:54:58 [KS]

That's how you should do it, yes.

00:55:00 [BT]

Yeah, I should, but obviously it's not working for me.

00:55:04 [AB]

My father spoke to me about, he called it Zen type programming. He would meditate on the problem for a long time, closed eyes, not doing anything else at the time, and then go and write, possibly punch the entire program and just run it, and it would be bug free.

00:55:22 [CH]

I actually have heard this as well. Sean Parent, who's a many-time guest on my other podcast, I've heard stories that he also will sometimes just sit there for hours and just think in his head and then types it out and then it just works. I don't know if that's a mythical exaggeration, but this is the second time I've heard that there is a person out there that just sits cross-legged. I'm sure he's not cross-legged, but that's what I picture. It's like meditation with clouds lowering from the heavens and then this moment of, "I have it," and then they go type and then the code works.

00:56:12 [AB]

I never asked my father about this, but I also had this internal image of definitely sitting on the floor. You can't sit on the chair and do this, I think. You have to sit on the floor. Yeah, I have no idea. And then you go and type or punch, depending on which year you're at.

00:56:16 [ST]

I think I find rewriting avoids a lot of debugging. So when I've got a draft of the code, I just keep rewriting to make it look better and remove redundancies and see if there's better ways I can put it. And in that process, I think I find and eliminate a lot of errors. I see connections I didn't before.

00:56:41 [KS]

Yeah, I quite like this process too, actually.

00:56:44 [ML]

So is this as in revising or as in just completely throwing out and writing it again from memory?

00:56:49 [ST]

Oh, that's a good one. No, I'm talking about the revising. The complete rewriting is a good idea and I like doing that too. If I think, "Oh no, this is the wrong approach. Maybe a third of it's wrong," start from scratch. But my focus is always on getting it to look as beautiful as possible. Well, I said beautiful. I guess I'm relying on an aesthetic sense, a minimum of redundancy, looking for the connections and logical patterns in it. And having written that way is much more likely to work. I did this once at Dyalog, actually. It wasn't in fact in APL. I think we were writing PHP for the web server and I was sitting with one of the Dyalog staff and I sketched out the PHP and he very patiently watched while I fiddled and fiddled and fiddled with it and rewrote lines and broke lines in different places and moved them around until I was satisfied and fiddled with the indentation. And then it just ran. He was like, "Holy cow, Batman." I didn't know that was possible.

00:58:14 [ML]

Yeah, I do that a lot with arithmetic in particular where there's so many different ways to write your index arithmetic. I'll try to arrange it so that it becomes clear that there's a concept coming out of it. One thing that I often find is that initially I write based on an index from the... Or based on the location of the beginning of the segment I'm working on. But then if I rewrite the algorithm to be focused on the end of the segment, it actually becomes a lot clearer. So I'll explicitly compute at the beginning, start plus length is end, and then do things relative to that. So that's sort of rewriting. I think, yeah, that gives you a much better comprehension of what exactly you're writing.

00:59:01 [CH]

All of this talk about enlightened programming, for lack of a better term, makes me want... I was searching it up in the last couple of minutes to see if I could see if you had done any live streams, Kamila, or something like where you've coded live or given a talk where you've done some demo. And I didn't find it. Maybe it exists online. But if you haven't, I think I would be definitely one person interested. And I think a few of our listeners, if not the panelists, would be interested to see you code because it sounds like, yeah, that you are operating at a certain level that would be inspiring, if not to aspire to, but at least to see. I'm not sure if you ever thought about that.

00:59:46 [KS]

Well, I actually like doing live demos because the golden rule of live demos is that they always fail.

00:59:51 [CH]

Yeah, this is true.

00:59:52 [KS]

And I've never thought about live streaming, but there is at least one person in the panelists group that has seen me program live.

01:00:01 [CH]

Bob, you were going to say something too.

01:00:03 [BT]

Well, I know you were talking about your abilities, C programming, and Adám was talking about that. Arthur Whitney [09] has a particular style of C programming. What's your perception of that? Is that something that you've looked at or is that... How do you feel that works with the way you program in C?

01:00:24 [KS]

Well, when I was going to go to Dyalog, I was actually scared the code would be written like that. And this is why I didn't want to commit to having done anything. But I think that it works if you're a lone developer working on a research project or something. I've actually tried it once for my Advent of Code solutions in 2023, but I see the merits, but I don't necessarily see why would you want to write a whole program like that. It's very pretty for algorithms, right? That's for sure. But I think that when you deal with the programming parts of interacting with systems, etc., it's no longer as pretty.

01:01:04 [ML]

So I can... I mean, and I think a lot of that is accurate. I can talk about now that I'm working with NGNK, how I feel about that, because Nick has modeled a lot of his style on Arthur's. And I don't think it's exactly the same. But what I notice about the NGNK interpreter is that there's... So, I mean, there's a fixed header of all these definitions that you have. You know, it defines A of whatever and B of whatever, and it uses up pretty much every letter and a lot of them twice because they're both a type and a function. So you have this fixed header, but then after that, there's just no abstraction. Everything is written out as exactly what operations you do. So even if there are things that are applied to multiple types, what it'll do is get the basic operation simple enough so that it fits on one line or a fraction of a line and just write it out for each type. And this is actually seems so far to be pretty nice to work with because, I mean, everything's right there. If you understand the basic model of how this code is written, you know exactly what it's doing. And I was actually even thinking as I was writing it, you know, in many ways, this is a lot simpler than Dyalog because Dyalog has this whole memory management structure under it. And there are a bunch of kind of hidden things you have to know about working with stuff. And I guess there are a few hidden things in NGNK. Like there are operations that are sort of utility-like, but they operate in chunks in order to vectorize. So you have to know that, you know, if you write all the integers up to some value, it's not going to stop at the end. It's going to go past it. But there's not like this whole underlying framework to learn about, you know, when things are going to move around under you and how you have to register things with the garbage collector and so on. So, and I don't know if the style of writing enables that, but it kind of seems connected that it lets you write things out in full more simply. And so then you don't rely on kind of higher level abstractions. And I think it would only work up to a point, but that's how I see the advantage.

01:03:23 [KS]

Yeah. I mean, I can fully agree actually, because if you look at the array style, the Arthur style C code, it's very ad hoc, right? And if you look at C code, J code, APL code, it's also very ad hoc. I mean, look at co-dfns source code and you can see a bunch of ad hoc implementations of trees based on, you know, arrays or whatever. But APL and the quote unquote Whitney C programming models kind of make it less painful to type everything out ad hoc. It's kind of fun. Yeah.

01:03:57 [CH]

All right. We've blown past the hour mark as per usual. I mean, I feel like our listeners would be upset at this point if we somehow landed the plane at, you know, the 55 minute mark, they'd be like, "Whoa, whoa, whoa, whoa. This is, it's the goal, but it's not what we expect."

01:04:14 [AB]

I don't know what hour mark you're even talking about. I don't get a particular mark at an hour. Well,

01:04:19 [CH]

I usually start recording like, you know, T minus 30 seconds before we start actually recording. So, you know, unless if you look at the clock when we say, "Welcome to ArrayCast," although this is like meta now.

01:04:33 [ML]

So you actually have like a mark for an hour that you're looking at?

01:04:35 [AB]

That's what I'm saying. There's nothing happening. So it says 0059 and then it says 100 and it doesn't feel any different.

01:04:43 [ML]

I mean, I assumed it was a conceptual mark.

01:04:45 [CH]

Oh, no. Like, I guess that's the thing is, you know, I danced it was a super meta and the listener is like, "What is happening here? This may not make it in at all."

01:04:53 [ML]

So I think they're aware that we usually go over an hour.

01:04:55 [CH]

But I actually have like a little, if I share my screen, like, you know, blue bars, blah, blah, blah. And like a little red line that's going. And so I can see all like a 30 second window of time. So I actually do at one point, I see if I'm paying attention, the hour mark, like slide by the screen. And now all I see is like 111 to, you know, one.

01:05:18 [AB]

That moves in front of you. Wow. Okay.

01:05:21 [CH]

Anyways, that's what I mean by the mark. There is actually a mark and it does go by. Whereas everyone else is just looking at a Zoom window. So I'm not just making something up for, you know, colloquial wisdoms on the podcast.

01:05:37 [BT]

And just to put all the cards on the table, when Conor does his intro, I look up at the corner of my screen and see what time it is. So there you go.

01:05:45 [CH]

But I guess maybe, yeah, before we totally wrap up, is there any last questions or comments from any of the panelists or maybe any last sort of things you want to say, Kamila? I feel like they were definitely having you back at some point in the future with the rate that you are producing content and books. And you said you've got, there's an upcoming talk section. We'll make sure to, like I said in the beginning, we'll link your Dyalog 23 talk that's currently out on the YouTubes. [10] But the future talks we'll try and keep an eye out for as well and announce them maybe in the announcement sections. But yeah, any closing thoughts from the panelists or anything? Last questions, quick questions?

01:06:22 [AB]

What's next? What are you going to be doing next, Kamila? I mean, you're 19.

01:06:26 [KS]

Well, that's a pretty broad question.

01:06:29 [AB]

I'm twice your age and I've done very little, tiny fraction of the amount that you've been doing. So I suppose you could just retire and be happy with a fulfilling life that you've had and so many accomplishments. And I hadn't just noticed on your website that you have had two mentions on Wikipedia, not one.

01:06:48 [KS]

Really? Maybe the other one.

01:06:53 [AB]

The other one was about cracking the messenger twister?

01:06:56 [KS]

Oh, yes. That was a really long time ago.

01:06:59 [AB]

At age 14?

01:07:01 [CH]

I just thought too that 19 means that you were born in like 2005?

01:07:12 [ST]

Four. Four. I feel so old. You'll get over it, Conor.

01:07:15 [AB]

Okay, okay. Kamila, can you implement negative number support for 4DL?

01:07:21 [KS]

I might fork on it.

01:07:24 [ST]

Kamila, who would you like to hear as a guest on the ArrayCast?

01:07:28 [KS]

I think that someone I would really like to hear, but it might be very difficult to actually reach out to is Henry Baker. Henry Baker was actually published in Code Quad. He's an APLer. He did a lot of work around symbolics. He's one of the pioneers of efficient garbage collector strategies. Also someone I kind of look up to.

01:07:51 [CH]

Yeah. He has a Wikipedia page. American computer scientist who has made contributions in garbage collection, functional programming languages, and linear logic. And one of the founders of Symbolics, a company that was designed, that designed and manufactured a line of Lisp machines.

01:08:07 [ML]

Yeah, I think Elijah Stone has mentioned him once or twice.

01:08:11 [KS]

Okay. Yes, because he's related to the whole CL garbage collection stuff, because he's a treadmill collector and the other stuff.

01:08:18 [CH]

Well, we will definitely reach out to Henry Baker. Henry, if you're listening, we'll be reaching out. Odds are you're not. But on like the 0.01% chance that you are, expect an email. And yeah, this has been wildly fun, Kamila, to hear about all your accomplishments that you list and all the ones that you don't list, because you have too many of them. I hope we'll be able to have you back on as a guest in the future and chat about what you've been working on. And you're still in university, that's correct? Yes. Okay, so yeah, we're expecting great things. No pressure. Yeah, no pressure. I can't wait to hear about what you're doing after that. And yeah, hopefully we'll get to see you at a conference in the future or something. I'm not sure about Dyalog 24 25, but yeah, fingers crossed that we'll get to see some more talks from you and maybe even a live stream at one point, because yeah, this has been super fun. But before we go, we will throw it over to Bob, who will tell you how you can reach us.

01:09:21 [BT]

You can reach us at contact@ArrayCast.com, although at this point, I feel fully unable to answer any questions that anybody has, because I'm just... One of my favorite movies when I was a young man was Amadeus, Milos Forman's Amadeus with the story of Mozart and Salieri. And I sit here thinking, I can see how Salieri would react to Mozart, but it's much nicer just to sit and just be amazed at abilities than it is...

01:10:02 [ML]

Which was probably what he actually did.

01:10:04 [BT]

Yeah, possibly, because it's not as good a movie. That's true. That's probably true. But I can also see why you'd be very... If you'd worked your whole life at something, you'd feel like, I've done nothing. But on the other hand, just to witness somebody who's so able, has such abilities. Honestly, thank you for being on. I just... I'm not sure enjoyed is the right term to use, because I don't know that I've understood everything that's gone on. But to be witnessed of it is... I'm grateful for that. Thank you.

01:10:36 [AB]

Think about how many programming languages the Kamila could have mastered instead of sitting with us for an hour.

01:10:42 [BT]

Yeah, I hope we've made good use of your time.

01:10:44 [KS]

Thank you for inviting me. It was great.

01:10:46 [CH]

No, thanks. Thank you for taking the time to be interviewed. And maybe we'll leave a couple links for those that haven't seen the Amadeus movie. There's a couple amazing scenes where Salieri comes out with this, I've been working on this for a week. And then Mozart says, oh, and starts tinkering around, or maybe this, this. And there's the one scene where he plays the piano upside down just for fun. And there's some great... I'm sure we can find them on YouTube, and we'll link them. And that'll be the metaphor for what has happened today.

01:11:15 [ML]

Yeah, those scenes were good, though. Those scenes were good, even if they weren't entirely historically accurate. But anyways, thank you again, Kamila, for coming on. And hopefully we'll get to chat in the future. With that, we will say, happy array programming!

01:11:24 [CH]

Things. Yeah. They made made. Those scenes were good, though those scenes were good, even if they weren't entirely historically accurate, though. But anyways, thank you again, Camilla, for coming on, and hopefully we'll get to chat. In the future. With that, we will say happy array programming.

01:11:36 [ALL]

Happy array programming!

[music]

</details>
