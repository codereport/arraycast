---
title: "Episode 7: Marshall Lochbaum and the BQN array language."
date: 2021-08-07 00:00:00 +0000
episode: 7
buzzsprout-id: 18621525
keywords:
- array-programming
- array-languages
- bqn
- marshall-lochbaum
- apl
- jlang
mp3-url: "/assets/audio/episode0.mp3"
episode-type: full
explicit: "no"
block: "no"
layout: podcast
excerpt_separator: <!--more-->
redirect_from:
  - "/episodes/episode-07-marshall-lochbaum-and-the-bqn-array-language"
  - "/episode7-show-notes"
---
<!--more-->

**Host:** Conor Hoekstra

**Guest:** Marshall Lochbaum

**Panel:** Adám Brudzewsky, and Bob Therriault

---


## Show Notes

- [Stack Overflow Developer Survey:](https://stackoverflow.blog/2021/08/02/2021-stack-overflow-developer-survey-results/)
- [Most loved/dreaded programming languages:](https://insights.stackoverflow.com/survey/2021#section-most-loved-dreaded-and-wanted-programming-scripting-and-markup-languages)
- [Top-paying programming languages](https://insights.stackoverflow.com/survey/2021#section-top-paying-technologies-top-paying-technologies)
- [Array language companies:](https://github.com/interregna/arraylanguage-companies)
- [I programming language:](https://github.com/mlochbaum/ILanguage)
- [BQN programming language:](https://github.com/mlochbaum/BQN)
- [Henry Rich:](https://aplwiki.com/wiki/Henry_Rich)
- [TI-BASIC programming language:](https://en.wikipedia.org/wiki/TI-BASIC)
- [2012](https://code.jsoftware.com/wiki/Community/Conference2012/Talks/ImageProcessing)
- [2014](https://code.jsoftware.com/wiki/Community/Conference2014/Talks/UsingDataAsCode)
- [Roger Hui:](https://aplwiki.com/wiki/Roger_Hui)
- [Factor programming language:](https://en.wikipedia.org/wiki/Factor_(programming_language))
- [Tacit programming:](https://en.wikipedia.org/wiki/Tacit_programming)
- [Just-in-time compilation:](https://en.wikipedia.org/wiki/Just-in-time_compilation)
- [Over and Atop:](https://aplwiki.com/wiki/Function_composition)
- [Unique mask:](https://aplwiki.com/wiki/Nub_Sieve)
- [APL Wiki](https://apl.wiki)
- [APL Wiki's article on A+](https://aplwiki.com/wiki/A%2B)
- [APL Wiki's article on BQN](https://aplwiki.com/wiki/BQN)
- [BQN chat room](https://app.element.io#/room/#bqn:matrix.org)
- [Apple food puns](https://aplwiki.com/wiki/Humour#Apples)
- [Glee, a left-to-right APL derivative](https://withglee.com/Frames/GFMain.htm)
- [Explicit defintion operator](https://code.jsoftware.com/wiki/Vocabulary/com)
- [Dfns](https://aplwiki.com/wiki/Dfn)
- [Context-free](https://mlochbaum.github.io/BQN/doc/context.html)
- [Array models](https://aplwiki.com/wiki/Array_model)
- [Based array model](https://mlochbaum.github.io/BQN/doc/based.html)
- [J Gerunds](https://code.jsoftware.com/wiki/Vocabulary/GerundsAndAtomicRepresentation)
- [Boxes](https://aplwiki.com/wiki/Box)
- [Strands](https://aplwiki.com/wiki/Strand_notation)
- [Strings and lists in BQN](https://mlochbaum.github.io/BQN/doc/arrayrepr.html#list-literals)
- [APL's Power operator](https://help.dyalog.com/latest/#Language/Primitive%20Operators/Power%20Operator.htm)
- [Where:](https://aplwiki.com/wiki/Where)
- [Where inverse](https://aplwiki.com/wiki/Where#Inverse)
- [BQN's inverse modifier](https://mlochbaum.github.io/BQN/doc/undo.html)
- [Extensions to partitioned enclose](https://aplwiki.com/wiki/Partitioned_Enclose#Short_left_argument)
- [where](https://tryapl.org?clear&q=%E2%8D%B81%200%201%200%201%200%200%201&run)
- [inverse](https://tryapl.org?clear&q=%28%E2%8D%B8%E2%8D%A3%C2%AF1%291%203%205%208&run)
- [Partition representations](https://aplwiki.com/wiki/Partition_representations)
- [Where and Replicate](https://mlochbaum.github.io/BQN/doc/replicate.html)
- [Leading axis theory](https://aplwiki.com/wiki/Leading_axis_theory)
- [Before and after combinators](https://mlochbaum.github.io/BQN/tutorial/combinator.html#before-and-after)
- [Tacit Techniques with Dyalog version 18.0 Operators](https://www.youtube.com/watch?v=czWC4tjwzOQ)
- [BQN namespaces](https://mlochbaum.github.io/BQN/doc/namespace.html)
- [Singeli](https://github.com/dzaima/singeli)
- [CBQN](https://github.com/dzaima/CBQN)
- [BQN Community](https://mlochbaum.github.io/BQN/index.html#where-can-i-find-bqn-users)
- [Online BQN REPL](https://mlochbaum.github.io/BQN/try.html)
- [BQN Tutorials](https://mlochbaum.github.io/BQN/tutorial/index.html)

<details markdown="1">
<summary><strong>Transcript</strong> (click to expand)</summary>

Transcript

Transcript prepared by Rodrigo Girão Serrão

Show Notes

00:00:00 [Bob Therriault]

I think you're torturing the computer.

00:00:02 [Marshall Lochbaum]

Well, fortunately your computer can't think unless maybe it's using neural networks for branch prediction, which you know probably it is.

00:00:10 [Music Theme]

00:00:20 [Conor Hoekstra]

Welcome to another episode of Array Cast. My name is Conor. We're going to go around and do quick introductions and then we're going to hop into a couple announcements and then an interview with our second guest. So first, we'll go to Bob and then we'll go to Adám.

00:00:33 [BT]

My name is Bob Therriault. I am a J enthusiast. I am not a developer or anything special like that, so my questions may be fairly elementary, but I do what I can and take what I say with a grain of salt.

00:00:46 [Adám Brudzewsky]

I'm Adám Brudzewsky. I work professionally doing APL and I've been doing APL, just not professionally all my life. Also, take a great interest in other array languages and the design of array languages.

00:00:58 [CH]

And my name is Conor Hoekstra. I am a professional C++ developer and a huge J slash APL slash k slash q slash potentially a couple more languages after this episode enthusiast and. And yeah, I'm super excited to get to today's interview. But first we have a couple announcements. Umm, we'll kick it to Adam 1st and and then I've got one announcement after that.

00:01:19 [AB]

I just want to mention that while APL has had a quiet period for many decades now, and stack exchange just published their [Stack Overflow developers survey](https://stackoverflow.blog/2021/08/02/2021-stack-overflow-developer-survey-results/) and for the first time, APL is on there and there's some really interesting statistics, including that APL is fairly popular among the people who use it, and that [APLers are very well paid](https://insights.stackoverflow.com/survey/2021#section-top-paying-technologies-top-paying-technologies).

00:01:47 [CH]

Yeah it's super interesting. Yeah, just to give a couple more sort of data points. So I find most interesting on this survey, the sort of [most loved versus most dreaded programming languages](https://insights.stackoverflow.com/survey/2021#section-most-loved-dreaded-and-wanted-programming-scripting-and-markup-languages), the top five are Rust Closure, TypeScript, elixir, and Julia, and then APL is sort of a down around the halfway mark, but it's above some popular languages. My day-to-day C++ it's right above Java and then more interestingly, it ranks above other sort of array languages. Obviously Julia I guess sort of wins 'cause it's in the top five. But APL would arguably be the second array language, and then below that are both R and MATLAB, so we'll definitely leave a link to this survey in the show notes for folks that want to go check it out. I find it pretty interesting. And the last announcement I keep on forgetting to announce this, I've meant to do it for like the last three episodes, but we will have a link in the show notes to a [GitHub repo](https://github.com/interregna/arraylanguage-companies) that is a list of companies that are using array languages. So if you work for a company and it's public knowledge that they use APL/J/k/q or another array language and you want that listed on this GitHub repo, feel free to go create a PR. It's really, really simple. As long as you have a GitHub account you can do that and it's pretty cool to be able to see all the different places in the world. So one of the most common questions you know. Array language developers get is, you know, do actual companies use APL or J? And here you can go see and if you're potentially looking for work. You can go to these sites and look at the career offerings to see if they're hiring.

00:03:22 [CH]

But with that announcement out of the way we're going to hop into our interviews. So today our guest is Marshall Lochbaum, who I don't know super well. I know Adám knows him a lot better, but Marshall was mentioned on our previous episode with Henry when talking about J because Henry was, or Marshall was one of Henry students. And what I know about Marshall is that at one point he worked for Dyalog APL and he has created two array languages himself. ["I"](https://github.com/mlochbaum/ILanguage) and I believe it's pronounced [BQN](https://github.com/mlochbaum/BQN). I messed that up if you were listening to the last episode, but it's apparently if you're making a pun, you can say bacon. But with that, I'll kick it over to Marshall. And if you want, just maybe start with a brief history of your sort of array language journey till today.

00:04:07 [ML]

Hi Conor, thanks for having me on on. So yeah, my my array language journey does start with my teacher, [Henry Rich](https://aplwiki.com/wiki/Henry_Rich). I have I still have to fight the impulse not to call him Mr. Rich, but he's Henry. So, I first learned J was my first programming language. Before that I'd done some work on the on the programming calculator [TI basic](https://en.wikipedia.org/wiki/TI-BASIC), but other than that? I started with J. Henry, as he discussed in the in the last episode, you should check it out, was teaching programming at my high school Raleigh Charter and he offered... Actually I knew him from doing math competitions. So he offered to teach me in a self study course on J and the summer before I read his book and I learned J. And so that was it. And I could. I could program I was using. I was using trains and rank. I think I was using nested rank within a month or two of starting with Henry, so I got started with J pretty quick. Then my kind of next big thing with the J community was when I presented at their conferences in [2012](https://code.jsoftware.com/wiki/Community/Conference2012/Talks/ImageProcessing) and [2014](https://code.jsoftware.com/wiki/Community/Conference2014/Talks/UsingDataAsCode). So that's when I got to meet everybody involved in J and and sort of get to know about that community. I met [Roger Hui](https://aplwiki.com/wiki/Roger_Hui), which was pretty cool. And also at those conferences I found out about about Dyalog and Dyalog APL, so they it was only one year. Maybe it was 2012? I'm not sure, but Jay and Morten came and gave a presentation on that, so that's when I learned that at least Dyalog existed. And that was the first time I think that I heard about using our bit booleans to implement arrays. So after that I went to college. I was I was really interested in programming languages for a while, 'cause I because I started with J and I was thinking, well, J is so great and nobody knows about J. What other great languages don't anybody know about? So I started using a bunch of languages. [Factor](https://en.wikipedia.org/wiki/Factor_(programming_language)) is one kind of obscure one that I remember a lot. And I also started implementing my own languages. Around 2012, maybe even before, I began work on I which we have J and k so I won't say that I is a cross product between J and k but it's something like that and I made I. I was a really terrible name for a programming language, so I saved you from from the mistake of doing that. But fortunately it's also a terrible programming language. I was really an exploratory, thing where I was really getting deep into [tacit programming](https://en.wikipedia.org/wiki/Tacit_programming), and what I found out is that you really shouldn't get that deep into tacit programming. You should use variables and stuff so. But uhm. I learned a lot. I started working on [just-in-time compilation](https://en.wikipedia.org/wiki/Just-in-time_compilation) with I, which is in maybe 2015 or 2016, which was pretty cool.

00:07:21 [ML]

And then after that I graduated college and went looking for a job and eventually I remembered about Dyalog that I'd seen at the J Conference and I checked their website and just a few months earlier they'd posted this job listing for a programming language implementer, and I said that sounds like me. So I knew that Roger was working with them and I emailed him and he said, Oh yeah, you should apply. I would put in the good word and so I did, and I was pretty soon hired at Dyalog. And I started. So there I worked on all sorts of implementation stuff that was at least half the time that I spent there was just speeding things up, which was, I learned a whole lot that way, developed a bunch of techniques that I haven't seen anywhere else, so it's a lot of new stuff, and also another thing that I did is start to introduce new functionality, well I don't think I added anything that was really new but I I worked to introduce some some stuff that had been developed at IP sharp for SHARP APL and it later made it into J, so that's why. Over and under, [over and atop](https://aplwiki.com/wiki/Function_composition), not under, and the, it's called [unique mask](https://aplwiki.com/wiki/Nub_Sieve) in Dyalog made it in at least as of now, is 'cause I pushed for those to be included and implemented them. So I I did a little bit of work on design and, and eventually things were not really working out at Dyalog and eventually I decided to leave. Just before this kind of coincidentally, I'd been working, So we started at Dyalog The young APLers group, which was, which was all the young APLers at Dyalog. We had, we've done some meetings. The first thing we did was actually set up the [APL wiki](https://apl.wiki), so that's great. You can. Maybe you've already seen some articles there and, and I've contributed a lot to that. But the the second big thing we did was start to discuss, you know how would we take APL further? So APLer's are always thinking about, you know APL's got all these issues? What if what if we could start again? And with APL this is really pressing because APL was designed in, you know, five or ten years and then. then there was APL360 and nobody ever really felt bold enough to break compatibility or several people have felt bold enough to break compatibility with APL 360. And I'm one of them too. But yeah, so the major attempts there are APL PLUS is the only thing that I'd really say is an APL, but breaks compatibility. Then there's J and [A+](https://aplwiki.com/wiki/A%2B), I haven't been able to get it to run, it's it's maybe still used in Morgan Stanley. This is Arthur Whitney's APL before he did k. And and there's j. And I mean k is getting pretty far from the idea of APL, so so we were talking about how would we take it, fix up the mistakes and make something that is still APL. But that's new and that doesn't have all the issues that we've discovered over 50 years of APL practice. Yeah, we had we had a lot of discussions along those lines and I was, always been interested in language design, so I was designing a bunch of things. And when I left, I decided to take this into it and I called it [BQN](https://aplwiki.com/wiki/BQN) and and that is a, so I guess we'll we'll talk more about BQN in the question section, but that's what I'm working on now. It's been a little over a year now since I started and BQN is doing pretty well I think. So we have an implementation that pretty much works. I've written a lot of things in it. It's got a self hosted compiler. And we've got a [chat room](https://app.element.io#/room/#bqn:matrix.org) with, I think, about 50 members. If you remove duplicates. And some people that are fairly active so BQN is really moving along, which is really cool. That's where I am now.

00:11:49 [CH]

Alright, so once again I feel like this is going to be a pattern. I have 1000 questions, but like the most obvious one which you sort of just alluded to was was BQN, so I'll ask a short version before I ask, you know what are the major differences and sort of can you compare and give like a a summary of the language? But where does BQN? I you know, I've read the readme so I know what it stands for, but I won't steal your thunder. So what does BQN stand for and where does the name come from?

00:12:17 [ML]

Well, yeah, Better Questions Notation is its acronym, in fact. I I kind of want to leave this as like a a shadowy rumour that no one will talk about, but I I put it in too many places. So the way I came up with the name BQN was I thought, well, alright, this was while I was still at Dyalog, even I thought alright, I'm working on this next APL. What do I call and of course, you know the obvious answer is APL plus, plus or whatever or, but then I thought about, you know how C leads to D and, well, J doesn't actually lead to k, but and so on. And so I took took APL and I moved it forward and I got BQN. And I said, well, BQN, that sounds pretty good, it's. I came up, you know? Big queries and better questions notation. That's a big questions notation is what I ended up with. I like it 'cause it suggests that not only you're solving big questions, but you have big questions about the notation, so it's a little tongue in cheek. And I said also, you can pronounce it like bacon, so there's even a [food pun like Apple](https://aplwiki.com/wiki/Humour#Apples). And after some half hour or an hour of thinking about this, I realized that the letter that comes after L is M, not N. I think it would be much more logical for N to come first, because it's the letter with two humps. BQM is a horrible, horrible name, and so I stuck with BQN.

00:13:47 [CH]

I was I, that's that's really two sad things just happened there. One I was really disappointed in myself that I hadn't made the observation that it was just a one rotate on the characters and then two. I'm sad that I didn't realize that it's not a one rotate on all of the characters. I just took your word for it. But wow, I'm very I should have noticed I should have noticed partially that.

00:14:10 [BT]

I'm also impressed that you're thinking of reordering the alphabet because of the number of humps in the letters.

00:14:16 [ML]

Well that was my excuse afterwards. I mean I, I assumed that's why I thought that end came after L but who am I to say?

00:14:25 [AB]

Always good to look things up of course.

00:14:26 [ML]

Well I figured it out on my own, it just took me a while.

00:14:30 [AB]

I remember when we, when we're in that young APLers group, and it was really fitting name big questions notation because we were questioning everything. We we were. We even had this kind of gradual thing of just tweaking existing APL a little bit to questioning absolutely everything APL and and all APL derivatives. Almost all APL derivatives are famous for running from right to left as people call it, or long right scope or right associativity and and you even questioned that. Right? And so it really is big questions notation.

00:15:09 [ML]

Yeah, well, in fact the the [left to right thing](https://withglee.com/Frames/GFMain.htm). I didn't really feel bold enough to question, so when I did I it ran. It ran left to right. Which I like at least for I, but I don't know if it works in APL, so that's, the the idea of BQN was to keep the essence of APL intact. To make something that was, that kept the strengths, but was better. I still don't know 'cause I haven't tried it, whether it's whether you really want to change the order, but I decided that was just too much. But otherwise, pretty much I've just made a clean break with APL, and it's important if you're coming to BQN to know that. It's not APL, you can definitely, your APL knowledge will help you a lot, but it's a new language that you're going to have to learn. So, and I've thought a bit about making a version of BQN that's closer to APL, and the problem is, which I guess we'll get to. There are just too many differences, so I can make. I can make it line up in the in most of the characters. So that said, maybe it would look like APL, but it really wouldn't be the same. You'd just be running into all these gotchas all the time, so, uhm, I do. I keep thinking about this, but I keep thinking also that I don't actually want to do it so.

00:16:31 [AB]

Then I'm not the only one keeping thinking that yeah.

00:16:36 [CH]|So I guess yeah. What are the you know? And even for our listeners I think. Well maybe I'm not sure, Bob, how much time you've spent on the GitHub repo, but talk us through, you know, the similarities and differences even as far to mention you know you know J obviously uses the digraphs and APL uses the Unicode symbols you know start from there and then, and then go in terms of like wherever you want to go.

00:16:59 [ML]

Yeah, so BQN is more like APL than J. Even though I started with J, I've come to dislike a lot of things about J. One is that it's got this well, J didn't even initially have functions. It was designed to use all tacit programming. Kind of like I, I didn't even know that when I started I but so they've got a function syntax that is, it's not actually a syntax, [it's an operator](https://code.jsoftware.com/wiki/Vocabulary/com) that you call that, then reads a string from your source file. If you want to do a multiline function and then turns that into a function. So that's pretty messy, and I think that makes it a lot harder to organize your code. So in that way BQN is a lot more like [dfns](https://aplwiki.com/wiki/Dfn). It's really the functional style is based on dfns. As for differences from APL, well and also J. The really big ones are first BQN has a [context free grammar](https://mlochbaum.github.io/BQN/doc/context.html) and second it it changes the [array model](https://aplwiki.com/wiki/Array_model), so it uses neither the nested array model from APL nor the boxed boxed flat array model from sharp and J. It uses what's the [based array model](https://mlochbaum.github.io/BQN/doc/based.html). I didn't actually name this. It was named well before the modern idea of based, but I think it is kind of based, so that's cool. So to start with the context free grammar. The idea is well, first I'll say what it means that APL doesn't have a context free grammar. In APL, when you run an expression, it goes right to left, and it it reads each part of the expression, and then it says what's the value of this thing, and then it says based on that what do I do with it so it reads an array, then it reads a function, then it reads another function that says OK. Now I know I can call this right function on the array. And then maybe the function on the left is going to be called with one or two arguments. So that the value of the expression is definitely a form of context. That means that the grammar isn't context free, and so what that means is that you can't say you can't just look at an expression and say what operations you're going to do to find the value of that expression. You have to know also what like all the names in it stand for. And so this is. This makes it harder to read because you need to know this context to even figure out how to parse things. And it makes it harder to execute because, because every time that it's running the whatever is the implementation, which for APL is always an interpreter, is going to have to check this value and then figure out how it fits into the syntax. And and the having variables is even really a particularly bad form of context because these variable values, they're only get ever going to be known at runtime, so it's not just there's a grammar, but it happens to not be context free. It's there's completely, you can't do it without this context. You could be getting your variable from a file or whatever. And even in the same program, a variable can do one thing and then another. So the way expressions are parsed could change. So BQN fixes that which k also does this. I need to point out. But BQN has a context free grammar which tries to preserve the APL model of thinking. k isn't so strong about that preserving this APL model of syntax while allowing you to to just look in an expression and see what it does. The way it works is that, it says the what's called in BQN the role, in APL you'd use the type for both the actual value type and what role it serves in the expression, but BQN separates this into the type of the role. And so we say that the role of an expression is always completely static. So, for a primitive it is whatever the role is, for function it is a function and for a modifier its a modifier. The the more interesting and kind of distinctive thing is that for a name, it depends on how you spell it. So if you write ABC. You can write it with capital or lowercase letters. That's always the same variable, but if you write it with a lowercase initial letter, in that case, it's treated as a subject. What an APL would call an array. And if you write it with an uppercase letter, it's a function. And if you want to make it a modifier which is like an operator, you put an underscore on the left or the right. And you'll notice even the vocabulary I've reworked too, usually to make it more direct I guess I try to make it so that things are just described in English what they are, so a lot of the time instead of monadic and dyadic I allow these those two, but I also just call it a function with one argument and with two arguments. So I just say what it is. So but yeah, this. This syntactic role concept makes it a lot easier to read the code and then another thing that's probably the best thing about it is that it also allows you to switch the roles so you can, you can use functions as anything you want, you can use arrays as anything you want. So for example, you can call an array as a function, and what that does is just return the value of the array. But also you can use a function as an array, and so as a result you can pass functions as arguments and do kind of real functional programming where functions are really first class values and so that means you can put functions in arrays and all sorts of stuff. And there's even a modifier that basically requires you to put functions in arrays which is called choose. So maybe if you're familiar with J, there's this. There's this thing called Agenda where you string functions together into [gerunds](https://code.jsoftware.com/wiki/Vocabulary/GerundsAndAtomicRepresentation), which is an array that represents the function. BQN has choose where you directly put the functions into an array and then you have an index to select which function you want to call. So that's much simpler in BQN you don't have to add this gerund concept, you just have a list of functions.

00:23:33 [CH]

Well, so this is this is just backing up to the lower case upper case, so say say I've got a, I want to do some, run some statistics and I type in AVG in capital letters for my average function and then I type in median MED for median and then a couple other. You're saying that those as functions, whenever typed with a capital letter, act as functions, but I can throw those in a list and I can do that just as simply by lower casing the 1st letter of each of those.

00:24:04 [ML]

Yeah, to put them in a list you don't even have to do that because BQN has a list notation which Adám is working on for APL as well, but... So what that that's sort of like? Half experimental right now or something?

00:24:18 [AB]

Yeah, well it has a release candidate.

00:24:22 [ML]

There's there are utilities that work with it, but it's not. It's not in a released version of the language yet.

00:24:28 [CH]

That's it's super interesting 'cause I I don't have a full list of languages that have like a delineation between uppercase and lowercase, but I know that Go, you know uppercase functions are allowed to be exported, or vice versa. So like if you if you try and export like a lowercase one or the other like it gives you a compile error saying you know it has to be uppercase, but that's the only other language that I know that does something with like the casing of of your your functions, so that's that's really cool. Anyways, back to you.

00:25:00 [ML]

Yeah, these are, there are other, like some languages, you use uppercase letters for types and things, but then it's just that there are two completely different classes of names that can't interact. So if you use an uppercase letter, you're in the type world and if you use a lowercase one, you're in the value world. With BQN, it's all the same, it's just how you choose to spell it determines what it does in the expression. And I said in a list you don't even care about the spelling 'cause you can use any role for an element of a list. But the main thing that writing a function in lowercase does. So if you had, I don't know some, some function that does some crazy statistical thing and you might pass a parameter to it. That's either the mean or the standard deviation or something. Then you can actually just pass it as an argument instead of forcing this thing to be a modifier. And Adám is actually the one who who came up with this idea. So I should point this out. He's actually always been a fan of case insensitive identifiers in general, so BQN is case insensitive, except this one thing.

00:26:07 [AB]

Yeah, I think maybe we go the other way around. Let's say we have a variable which means it has an array value, say 5 and it's called lowercase a. Now if we put a lowercase a by itself then we get back that value 5. But if we spell it upper case a instead, it's still 5, but it's the function of five. What does that mean? It means it's a constant function no matter what argument you throw at it, it returns 5. And now we can understand it backwards as well. We can take a function that we have defined the upper case and we spell it in lower case and now it just returns that value. That function value it never applies it, it just represents itself like any other array.

00:26:57 [BT]

And to me that part sounds more like the gerunds in J, right? You've got an atomic version of that func.

00:27:02 [ML]

Yeah, except that as the language is actually running, so this is purely syntax. When the language is actually running, there's just a function and what it does is the syntax tells you alright do I pass this function as an argument? Do I put it in a list or do I call it as a function and so you can call anything as a function? If you try to call a modifier, you get an error, but you can call a function or a, or an array, or a number, which is the other numbers are not arrays in BQN. That's the next thing. But so yeah, you can. You can get these cross roles that allow you to do functional programming and it's still, it's not quite as easy as functional programming in Lisp because you still have to, in Lisp the parentheses, tell you what's the function, right? So the first thing in every parenthesis is the function or. I don't know Lisp very well, but maybe it's a macro or something. Whereas in BQN, if you have something in a variable, you can always change this rule really easily, but if it's an expression then maybe you have to do some more work.

00:28:06 [AB]

Uh, I I think another thing to point out is that the gerunds in J, yes, you can get something that acts like an array that consists of functions. But what if you want something that's like an array consisting of of adverbs or conjunctions, those that are called modifiers, operators? You can't because they're fundamentally incompatible with with each other, and there's a whole thing, been for years already, discussion in, in, in APL that functions take arrays and operators take functions and what takes operators. That's that problem, and by being allowed to switch roles of things then that whole problem just goes away.

00:28:49 [BT]

Yeah, the gerunds are really tied to the verbs. You don't, when you get a level above that, they're not not really applicable as much anymore.

00:28:55 [ML]

Yeah, and the other thing is a gerund like, despite the fact that you might never use it this way, it is still an array, so you can't actually tell the difference between if you're taking a value from the user. Is it a gerund or is it? Did they just write an array that happens to have some strings in it? So when you're using the actual values, I think it works out a lot simpler.

00:29:16 [CH]

So I think that was that was sort of of your explanation that started from the CFG. You also mentioned the based array model that is different from from J and APL, so.

00:29:31 [ML]

So quick overview. There's also an APL wiki page on array models that I wrote, so it tells you my side of the story. At least I wrote it though before I came up with the based array model, so it's not. Hopefully it's not, but so biased. So at the beginning, of course we had APL 360 which had the completely flat array model where everything is an array and done. And you have your array always contains either numbers or characters, and that's it. That's the whole story. I mean, you can imagine something where arrays can contain a mix of numbers or characters, but that's a pretty minor variation. In the early 1980s, people started getting pretty serious about, well, we want to store arrays in our arrays. And they said, how does this work? Now, if you're starting with a scalar language like you know Python, JavaScript, Java, any of these, what they all do? I mean they all have one dimensional arrays, but it's kind of the same what they all do is say, well, an array is a container and it contains other values. So in the language you've got your numbers and your strings in your arrays and so on. And that's it, they're done. That model works. But the the problem with, to, as far as I'm kind of reverse engineering this. I think the problem people ran into with APL 360, is that when you start out with the idea that everything is an array, you can't just take that away and maintain backwards compatibility, so they can't then add an individual number thing because, well, in APL 360, a number is a scalar array that contains a number. And those might behave differently. For example, in BQN, when you call range on a number, you get, you get what you did in APL calling Iota. If you call it on an enclosed number, then it treats that as a list, so. So it gives you actually a multidimensional with exactly one dimension, but a multidimensional range where each value is not a single number, but instead of list of numbers. So you can't actually adopt that model. And what people did instead was they went to either the nested array model with floating arrays where it says yes every value is an array, and to include numbers in the language we're going to say that a number is the same as it's itself enclosed. So they sort of add numbers to the language, but make them equal to an existing value already. I mean, this has its issues because, like if you enclose something and you get the same thing back, that's pretty weird because you you should be saying I'm adding an extra layer of structure around that, but then the language goes in and says no, you're not. This is a number. And so that that kind of causes some subtle issues. And then on the other side, what the people at IP Sharp did was they said all right, we're going to add a new type of element that you can have, which is a [box](https://aplwiki.com/wiki/Box) and still in the language you can describe this differently, but I'd say that in the language everything is an array. It's an array of numbers, characters or boxes. And a box is still this atomic value. You can't. Actually, you can't actually use a box. You can use an array of boxes, and maybe it's a scalar. And then if you want to, you can go inside the box. This is this is at least an inductive type, so it's kind of it has better mathematical properties. But the base case is an array, which is really complicated, so you have this base case which is all your data is either an array of characters or an array of numbers, or an array of boxes, and furthermore a box might contain anything. So BQN does the thing that that other languages that didn't start with arrays would have done anyway, which is to say all right? We've got our scalar types, we've got numbers, we got functions. We've got namespaces. And then an array is just a data structure that can contain any other value. So it's actually simpler than either of these two models. The problem is that it's not backwards compatible with APL 360, but as I've said, I'm breaking compatibility, so I can do that. And so that's kind of I can see why it didn't go that way because people are trying to. They're just trying to extend APL, but that's how I think it should have gone. And and another way I'd describe this is to say. Well, if you want to add layers of nesting above, if you want to be able to put arrays inside arrays, you have to be able to go down to the lowest level of nesting. You have to be able to reach something that's zero times nested that's not an array. And so all these kind of subtle problems and inconveniences that you get, not that, so BQN has still has the inconvenience that you have to keep track of, you know, how many levels of nesting you do have, so you have to distinguish between a number and the enclosed number, which in the nested array model you don't because you can't. But I think these are. These are more fundamental differences, so you're saying well, there's a difference, but I actually have to keep track of this because it matters as opposed to just places where the array models kind of, I mean, I don't really want to say kludge, but where there is an adjustment made to the array model that changes it relative to the simplest case to make it match something that really it shouldn't match.

00:35:22 [BT]

So so in J, one thing I've always noticed, and this might be solved by the way you're approaching arrays in BQN, for a character string, say I've got 3 characters ABC and I enclose them in quotes. Now I've got a 3, a list that is 3, you know it's it's. That's effectively a character array that's has a length of three.

00:35:44 [ML]

But you've got a list of boxes there.

00:35:46 [BT]

Like a list of boxes? Yeah exactly yeah, I reduced that to two. I've still got that. I reduced that to 1 and in J now I don't have a list of 1 anymore. I have a single character so.

00:35:57 [AB]

That's just the notation. That's just the input notation. It's not the fundamental thing in the array model. You certainly can have a one element character vector. That's not that.

00:36:08 [BT]

No, I can make one, but I'm just saying as I reduce them is that is that where the induction breaks down. When I go from 2 to 1.

00:36:15 [ML]

Uhm, no. I'd say that's an issue with the string notation. And also an issue with [strand notation](https://aplwiki.com/wiki/Strand_notation) specifically. So BQN also fixes that, which again is something else that can introduce other inconveniences, but. Uhm, so in BQN, you use double quotes for a string. And that's always always a list of characters. And then you use single quotes for a character. That's done and you don't have to worry about that inconsistency. You have to remember to keep double quotes and single quotes straight, but characters and strings are different. And similarly with the list notation, I actually and a lot of APLers come to this and say Oh no, this is this is wrong. I've taken out stranding so if you write 3 4 or 5 in BQN you get a you get a syntax error where it says double subjects and it asks if you possibly want to use the little smile character, that's like a parenthesis on its side, which I call ligature. And yes, you do. That's the [BQNs explicit stranding notation](https://mlochbaum.github.io/BQN/doc/arrayrepr.html#list-literals). Although I I said I fixed the problem and explicit stranding is the notation that doesn't fix the problem, it still has this one element versus two element problem where if you write one thing well, you didn't write any ligature characters at all, so of course it's not a strand, so it's just a thing. Right, if you write two things stranded together, then you get a list of two. But at least it's a little more obvious because as opposed to using just nothing for stranding, you have this character that indicates, OK, I'm forming a list. And then the other list notation with the angle brackets is it's more like a typical list notation and that always, you can form an empty list with it you can form a one element list, two element list and so on.

00:38:03 [CH]

Two questions. I've heard of stranding notation, but I'm inferring that that is creating a list of numbers by putting spaces between them and that you were doing, you were closing the spaces with the sideways parentheses or the horizontal, whatever you want to call it.

00:38:23 [ML]

Not necessarily just for numbers. in J and k, it is just numbers. So they have this particular stranding which is actually considered part of token formation which I think is pretty weird. But when when you put numbers next to each other, those automatically form a numbered list as part of the source code. And then in a nested APL like Dyalog, pretty much any APL you'd use today, the stranding can be between any two values. This was Jim Brown, Jim Brown's thing that he was really big about was that it it should be general, it should. It should be, you know, a fundamental part of the language which, I mean, I agree, I agree with that. I just don't agree with it that you should write it without using a character for it. So BQN, yeah, BQN stranding is more like a nested APL where you can strand any two values together. It's just the explicit.

00:39:23 [CH]

What is the? What is the downside of upgrading from only allowing literal numbers to allowing a variable name or something in in your list? Like why? Because I do. I have in the literature read that there was a big war between camps back in like the late 70s slash early 80s. And that I don't want to say that that's what led to Iverson's departure from IBM to IPSA, IP Sharp, but like I do know that there was two camps.

00:39:51 [ML]

Yeah, well he was clearly thinking differently in a lot of different ways, but that was one.

00:39:53 [CH]

So yeah, what? Is there a downside? Or is this just like a matter of opinion?

00:39:57 [AB]

I think I can answer that, it's it, and it's not just about numbers. It's about everything and and that is sometimes you have and firstly, we should point out it's not space that does this, it's adjacency that causes stranding. So if you have two things that won't merge together so it's not 2 names or variables or two numbers where the digits will run into each other, there's a, then you don't need a space, for example, in, in APL you can write 'a5', and that they immediately adjacent to each other, there's no space in between them. The problem is that this has priority in binding in at least some APLs, and and what happens then is if you have a an operator, and the operator takes an operand or we can call it a modifier or an adverb or conjunction, and if you have a language with lingo, we're talking and that operand, which is an array ends up being next to the argument to the array. Then, before the operator has a chance to sort of, say, grab it's operand array, the two arrays that are now next to each other join together due to stranding, so a classic example, if this sounds very dry, a classic example of this is if you if you use in APL the power operator, it's kind of common and so you would have a function and then power operator and a number because you want to, it's like function power in mathematics you apply this, this function this many times and then comes the array you actually want to apply this function. Now you end up having two arrays next to each other and they bind together to one giant array, which is meaningless in the context. And finally, you end up having function power operator and then some giant meaningless array which is not at all what you meant. Yeah, and this tends to be a common cause of confusion. And leading to ugly code, trying to work around this.

00:42:07 [CH]

And I think actually I ran into this exact problem. I won't describe it in detail, but I was solving a LeetCode problem that was basically given a list of numbers, uh, convert that list of numbers into digits, so if you've got like 1, 10 and 100 you want to end up with a list of 1 10 and 100 all in like single digit form and then sum that up and then it'll tell you N number of times to basically repeat that process. And in there I ended up with like exactly what you said. The power operator to the power of whatever N is, and then also an array. Because I think it actually starts as a string, so I needed to do like ⎕A or ⎕C or something like that anyways. But then when I when I hit enter it went. Bam bam like you've got a problem and then the fix 'cause I was just, you know, editing and praying and I'm a noob was to put like the the right tack in or something to separate the two and that seemed to work.

00:43:05 [AB]

So yeah, so in J and in in the APL's that don't allow this stranding or list notation other than for numbers, there's less of an issue, but it can still happen. So if you have something that has parenthesis and so on the right then it won't join together, but you could still have something that's a literal list of numbers or a single number as your starting array, and then you're applying something with and it can actually happen on the left as well. And if you have an operator that takes an array operand on the left, then yeah, then you. Then you can have a left argument that clashes with it. Another one in Dyalog APL is the @ operator. You can you can apply something at some indices and there often the indices will clash with what you're applying to and and so by by making stranding explicit, then you can have adjacent initial calling tokens, items, whatever you want to call them, and they don't join together and it just looks much nicer.

00:44:07 [ML]

Yeah, and so the, the thing about this is that actually you run into this problem a lot less than you use stranding. So in theory you could say stranding is more convenient. But the issue is it's less consistent. So what happens is that you have to think about stranding, even when you're not doing stranding, even when you're just calling the power operator. And that's something that I find with BQN, and I've made a lot of decisions to, you know, APL was pretty consistent, but I've improved the consistency as much as I can. And what that means is that there's just less different things that I have to worry about when writing my code so you could call that cognitive load what I found after a few months of working with BQN is that I'm just I'm focusing more on what I'm actually writing and not what I'm trying to avoid writing. So it's just so much less worrying and thinking about other potential edge cases goes on and that of course means that I can write ever more inscrutable tacit combinations of you know all sorts of nonsense that then does like a recursion and self modifying code and stuff, and so that's really beneficial.

00:45:18 [CH]

Yeah we should. We should point out too in case we have some like myself array beginners the [power operator](https://help.dyalog.com/latest/#Language/Primitive%20Operators/Power%20Operator.htm) that's been mentioned a couple of times, it is mind-blowing. It's one of the coolest things, like if I had to rank like the top 10 things that I discovered up to this point about learning languages. We're learning, like APL, it basically like enables you to put your function to the power of a number. So if you need to do some function five times, you just do power 5. But what's awesome about it is that you can also do to the power of negative one and invert a function, which is like it's mind-blowing in certain cases. Like the other day I was trying to figure out, oh like, so there's a, uh, or a function in APL called "[where](https://aplwiki.com/wiki/Where)" where if you give it a a Boolean mask of ones and zeros, it'll return you the indices that correspond to the ones in that mask, but I needed the opposite and I was like, oh like that's got to exist in APL, so I'm like I'm looking for, you know what's the function that does that, and then I realize, wait a second, will that work with like [power to the negative one](https://aplwiki.com/wiki/Where#Inverse)? And sure enough, I typed it in and it worked and I was like Oh my goodness, that's the most amazing thing in the world like why no other does any other language has something where you can take a function and like invert what it does like that's it's? Anyways that's my. My tangent is over.

00:46:31 [ML]

You're lucky 'cause I was the one who implemented that. Not as much of a tangent as you thought.

00:46:34 [CH]

Oh, really. That's awesome, oh man.

00:46:38 [ML]

So yeah, I added that to Dyalog. I keep it keeps coming up on the J mailing list, and I've I've tried to push it as an idea for J, but I don't think it's in there yet.

00:46:49 [CH]

Uh oh, wait, so that didn't come. I assume that like 90% of the new things that get added to APL come from J, so that was something that like didn't come from J and that you implemented.

00:46:57 [ML]

Well, it it came from me writing reading the J mailing list years earlier I guess, but yes, I implemented that in version 17 or 18, probably 18. I guess it was at the same time as where was extended to handle non booleans. So probably version 18. And uhm. I've been, uh, I've thought you know that should be a standard programming tool for a long time. And so I got the chance to do it in Dyalog. Roger has actually been against it, and his reason for that is that it's not a unique inverse, the, because you can always add zeros to the end and it won't change the result of where, so you don't really know what length the inverse should give.

00:47:48 [CH]

I actually ran into that exact issue, but then I was like that's just a simple like take take in yeah?

00:47:53 [ML]

Yeah, so then you just use take. And I use this. I use where inverse in BQN all the time. You can now in BQN not only can you take and I call power 'repeat'. which I like a lot better. Again, it's more straightforward, it's less mathematical. But not only can you take repeat minus one times there's its own symbol for inverse, which is a superscript equals. There's no superscript minus one character unfortunately. But superscript equals is all right, so you write [slash superscript equals](https://mlochbaum.github.io/BQN/doc/undo.html) and that's your where inverse, and that's in the compiler all over the place. Or, well, you know probably just two or three times, but I use it a few times and yeah, you have to get the length right, but I think that's really powerful, especially as a tool of thought and and the way I think about it a lot is that it's actually infinite length. Then it just has as many trailing zeros as you want. So as a tool for studying, for studying certain kinds of lists of natural numbers, it's a it's really valuable to know that that's a concept.

00:49:03 [AB]

With regards to the infinite list, another thing Marshall implemented well at Dyalog was exactly this that at least one of the common use cases for the where inverse is to use this Boolean that comes out as a partitioning vector with the with the positioning closed primitive and so an [extension he implemented to partitioned enclose](https://aplwiki.com/wiki/Partitioned_Enclose#Short_left_argument) is that you can omit trailing zeros and it just assumes zero for the rest. So that problem actually goes away. You don't need to do the overtake to get extra 0 so you can just use it.

00:49:40 [CH]

Yeah, the thing I was going to say is, if we're if we've lost like the the array curious folks, I'll try and add some links that show examples in TryAPL  of you know how [where](https://tryapl.org?clear&q=%E2%8D%B81%200%201%200%201%200%200%201&run) works, which is actually it's [iota underbar](https://tryapl.org?clear&q=%28%E2%8D%B8%E2%8D%A3%C2%AF1%291%203%205%208&run). So for anyone who loves Iota, it's got like a, you know, visual relationship. A lot of C++ devs love Iota 'cause we have it as well. We stole it from APL, but yeah, we'll try and leave links because it's it's probably. If you haven't seen it before, it's very hard to follow what we're talking about in terms of where where inverse and ones and zeros going to numbers. But yeah, it's it's an extremely powerful concept. And yeah, I had no idea that you were the one that implemented that Marshall, but I've I've I've used it once now and I'm never going to forget 'cause it's. It is actually like of exactly what Adám was saying. Like many times, you can use that to create a mask and there's so many functions in APL or primitives in APL that require a mask to do something like partitioning or filtering etc. Yeah, yeah, it's it's a or I should say compressing. We don't really have filter.

00:50:45 [ML]

Even if you're even, if you're an experienced programmer, what you might want to check out is that I wrote while I was doing this partition extension, I wrote a page for the APL wiki called [Partition representations](https://aplwiki.com/wiki/Partition_representations), and we'll get a link to that, I'm sure. And that discusses this really powerful system where you think about these lists of natural numbers that I was talking about, as as ways to partition a list and there are four different ways, and they're related by plus scan and where so you can go one way with plus scan and, well, it's sort of a weird relationship, but. You can go around the whole 4 steps using plus scan and where and plus scan inverse and where inverse. So that's just a really powerful tool, and if you're ever partitioning something, knowing that system tells you pretty much immediately, like you'll be in one of these four cases, and you want to get to some other one at that point, you can just apply, you can just look up the diagram even and apply whatever the right transform.

00:51:48 [CH]

Wait, let's pause. Plus scan inverse. What does it mean? So let's say you have you have like you know or yeah, plus scans.

00:51:53 [ML]

Oh yeah, that's not too complicated.

00:51:58 [CH]

So actually it's not. I'm thinking of like max scan, which is you wouldn't be able. You can't think about plus scanning that my dream.

00:52:02 [ML]

That you can't invert, but yeah, plus scan. So each result is the previous result plus the corresponding number. So to invert it you just subtract that previous result from the current.

00:52:13 [CH]

Oh my God, inverse scans can ah.

00:52:16 [AB]

The way I think about inverses is is kind of like playing Jeopardy. When you tell the interpreter to do an inverse, it means I'm giving you the result and a function give me the argument for that I need to feed to this function so that I get this result. So the plus scan the cumulative sum is a transform. It's a transformation of some data and I'm basically just asking what is the list of numbers such that their cumulative sums are these numbers? And it will figure it out.

00:52:54 [CH]

That's so awesome. Oh man, I'm going to go back on my other podcast at ADSP 'cause we just the one that we have coming out on Friday is about inclusive scans and we've got a couple pre recorded. But I'm going to be like Bryce Bryce Bryce guess what guess what APL has inverse scans commute? Wow, man that is so cool that is so cool alright I gotta calm down.

00:53:15 [ML]

See, this is the same thing I think, except I say oh in this other programming language, I should put that idea in there.

00:53:24 [AB]

And kind of mentioned the iota underbar and the and the symbol in Iota, and I'm looking at the clock a bit here. Marshall, we got to talk about the symbols the glyphs in BQN.

00:53:36 [ML]

Oh yeah, they're different.

00:53:38 [CH]

OK, that’s all for today.

00:53:40 [AB]

That's all I would say.

00:53:45 [ML]

Yeah, one of the pretty interesting ones is actually where because I thought this for a while, uh. So for example, J has a, it has a grade function. It has a sort function. The grades monadic and the sorts dyadic. So it says I can't remember which way it goes, and it turns out that I didn't include this this function in BQN and that's part of the reason. But it takes one argument order and sorts the other argument according to that. And so those are together. And what I thought for a while was that actually at the indices are where and replicate have the same relationship, so. [Replicate](https://mlochbaum.github.io/BQN/doc/replicate.html), yeah, replicate tells you all right, the left argument is a number of times to repeat something and the right argument is the things to repeat. And then where there. just the right argument, and that's the number of times to repeat. And what you repeat is is sort of the universal value, which is the indices that would go into it, and so that means because you've repeated indices. Then you could take that and use select. So if you have where the left argument and use that to select from the right argument, that's the same as replicate. And of course, whereas just replicate with the indices. So they've got this very close relationship. And in BQN I wrote them both using slash and if you're wondering another thing I fixed is that reductions are not slashes. They're in BQN and all the modifiers are superscripts. All the 1-modifiers are superscripts, so it's sort of a superscript slash, which is an acute accent. But yeah, so where and replicate I put on the same key and uh, I think this just makes it, it makes it more obvious when you transform code and it's just it helps to form stronger connections. When you're thinking about stuff.

00:55:48 [CH]

Can you tell us more about because I've seen the character set, and yeah, there's definitely a lot of I don't want to say more like geometric, but just definitely like a whole new set of symbols that are completely a departure from the APL Unicode. Where do those come from and uhm, yeah.

00:56:06 [ML]

Yeah, regarding the overall feel it's... I did I think the initial strategy I was taking, probably it was Adám said something about the, you know, the Greek letters are really not good. In addition to just confusing Greek people, they they confuse other people who don't know Greek letters, and eventually I kind of came onto the idea that you know, really using any sort of letters at all as mathematical operators doesn't make sense, because the way we write mathematical operators and the way we write letters is usually completely different letters. Written with these kind of variable with pen strokes and mathematics is always, you know, straight lines and geometric figures. So I chose much more geometric symbols for BQN and that means that kind of. That BQN gets this this much more technical feel to it, and one way to even describe the differences to, say APL, is kind of a fantasy feel. It looks like Tolkien would write APL, where BQN is very sci-fi and I call it an APL for your flying saucer. For that reason, and also because I'm hoping to port it so that it's got a runtime in every language, and then I could say, oh, it runs on anything, even a flying saucer could could run BQN. But yeah, so you get this very geometrical feel that's a, that doesn't... Like that's not what I started with, but I've kind of leaned into that and made it so that you know BQN is this sci-fi language,

00:57:41 [AB]

But we also talk about the roles and the symbols.

00:57:50 [ML]

Yeah, so this was also Adám's idea. BQN has this nice system where you can see the role of a primitive just by looking at it. So I said 1-modifiers are all superscripts. That's a really easy rule and actually usually in English. A lot of the times, the superscripts end up modifying the thing they come after, so if you've got, you know a superscript one. That's a footnote for the preceding stuff. If you've got a superscript TM that says whatever comes in front of it's trademarked. And so on. So that's an easy visual association to make to say that a one modifier binds pretty tightly with the thing that's right to its left. And then two modifiers all use unbroken circles, so that's the I kept the APL symbols for. I kept one of the APL symbols for reverse and rotate. Which is this Phi symbol with the circle with the vertical line? I dropped the horizontal line 'cause I don't just don't think it looks good and also 'cause I only needed one because I'm using the [leading axis theory](https://aplwiki.com/wiki/Leading_axis_theory) like J, and transpose. So those are the broken circles 'cause they've got a line through them. Everything with a circle that doesn't have that line through it is a two modifier, so it's the composition, and that's so you've got the top is the composition for mathematics. That's just the small circle over is a large circle. There's these other really cool characters that are the. I call them [before and after](https://mlochbaum.github.io/BQN/tutorial/combinator.html#before-and-after). I guess that are circles with little lines coming out. So those are asymmetric and they tell you there's one side that's going to be applied first, then the line points towards that.

00:59:28 [CH]

I think I've seen those yeah, and they looked really nice.

00:59:30 [ML]

They are. They make tacit programming, and you know, confusing people incredibly easier because. You can, I mean, well, OK, it's harder to confuse people, but you can get more confusing accomplishments because you don't have to work through your own confusion. Because it's so so much visually telling you what happens, whereas when you do tacit programming in Dyalog, I mean it's great that this was also something that I really pushed for. I think I said that uh, atop and over and Dyalog was, and constant. Those have been around a while. Constant was, I think, Adám’s suggestion and the other two have been around since sharp, but I pushed for those being Dyalog, but they're written with these circles with dots over them, and it's it's just hard to read. And like the the simple, the jot actually does something fairly complicated. With BQN it's, I think tacit programming is still a bit harder, especially if you're using a lot of trains. It's a bit harder to wrap your mind around than simple variable one variable, two variable, whatever explicit programming. But BQN makes it so much easier to approach because it has these visual connections that you can go to instantly.

01:00:51 [CH]

So yeah, there's two questions that I've sort of had in the back of my head, and this leads in perfectly to one of them speaking of tacit programming. Before I ask that, though, I'll, I'll note that there's a[ great talk. I believe you gave on the Dyalog 18 features](https://www.youtube.com/watch?v=czWC4tjwzOQ), Marshall, that's on like Dyalog YouTube channel and it’s got some at some point in that talk it introduces those those new operators and it’s a fantastic talk and has these, I wouldn’t actually say that they’re easy to understand diagrams because I didn’t confuse, I didn’t understand sort of them at first and then, but like once yeah, like once, once you understand it, they’re great. Like, oh yeah, that’s exactly what it does. So you have to get past a little hump. But yeah, it’s a great talk and we’ll link that in the show notes. But speaking of tacit programming, you mentioned really early on at the beginning of the podcast that at some point you had sort of discovered that you know partially through your writing I yeah, that it’s that you know, and I think Henry in the last episode made the same remark is that it’s very easy to go too far with tacit programming and that variables that sort you know, do the, or, name the intermediate like variables and state are helpful. Can you talk a little bit more about, you know, of your thoughts on tacit programming, and BQN obviously supports it to some extent, but like what, what’s formed your opinion that that you know, maybe J went too far that way?

01:02:14 [ML]

I think BQN might be the best tacit language ever. I can't think of anything else that would really compete you could there are some stack based languages that are OK, but. The those there's composition with the line operators would be couldn't really nail it. So as far as the tacit versus explicit question, I'm a little more in favour of tacit than Henry, just based on having seen some of his J code. But yeah, generally tacit is good for the very small things. The way I described it in that talk is that tacit programming takes all your context and pulls it sort of outside the function, so. For example, everything in a train. Every other function has the same either argument or two arguments, so there's this extra context that gets pulled away, and that allows you to write less code a lot of the time, because this context is implicit within the tacit function. But it also means that you don't have this context available to you immediately. So if you're really good at this, you can keep track of it in your head and work out what everything is doing but. But eventually that adds up. Especially if you're working with more than one or two values at a time. If you're working with three values, it's just really a pain to get them all shuffled through this tacit stuff. And that's what I more or less force you to do in I because I doesn't have any sort of scoping at all. It's got global variables that you can assign, but otherwise you're supposed to define your program as a bunch of tacit functions. And as I understand it, this is about how J was initially and they pretty quickly they, unlike I, had actual users, so the user says no, this doesn't work and so they were forced to add functions. And so then you get with those functions you get scoping. And yeah, BQN goes further. BQN has complete lexical scoping. Which Dyalog dfns also have lexical scoping. The thing that they do that BQN doesn't is they don't allow you to form closures, so the syntax mostly prevents you from doing this. But even if you somehow smuggle a function outside of the execution of a function, when when that function ends, its scope is just going to get yanked away from it. So so you can't. Form a closure in Dyalog. But yeah, so so BQN goes. And it doesn't do anything that JavaScript doesn't. It's a it's a normal. Normal lexical scoping idea. But it's just allowing you to use the normal style in addition to the tacit style, and so you can. You can pick your own personal mix, you can say. Like I usually do, I'm really into tacit programming. Or you can say I'm less into tacit programming. I've intentionally written some BQN code, like the markdown processor that builds my whole website. I've I've intentionally written that in a simpler style that splits lines more and that has a lot more comments than that. You know breaks things down just to to know what it was like and also have an example. But yeah, you can write BQN like this if for some horrible reason you happen to not be me. You can. You can choose this other style. It's a tradeoff, but I think having both available is is really important. 'cause in some places tacit programming is really great, and in some places tacit programming is really horrible. So if you put them both together, you can do a lot better than just purely explicit programming, and definitely a lot better than the purely tacit stuff.

01:05:48 [CH]

Yeah, when I when I was first started learning J and I usually do that by just solving a little like I mentioned before. A little mini LeetCode problems I I was sort of a shocked at the way you had to write functions in J, which you mentioned before. Like you, you'd have to put it in little single quotes and like the one effect that that had is, you had no syntax highlighting like GitHub, just treats it as a string. And I was like this has got to be the worst language decision ever. Like every function you write just shows up as like a comment y'know colour, and then I realized, though most of the time you want to try and write tacit functions, and then so basically now whenever I write something in J, I'm I try to write it tacit. But this leads into sort of maybe maybe what we can close on, unless if Adám and Bob have other questions, is that I I as this podcast. It goes on and as time goes on I'm trying to decide, you know, APL is currently my favourite array language, but I've I've am growing to love J more and more. You know, when I discovered under in J and when I discovered 13 colon, which takes an explicit function and converts it into a tacit function like APL doesn't have anything like that. So I'm and so slowly like I've got this graph in my head. You know APL up here and J’s you know got an incline you know at some point there's going to be. Is there going to be a crossover? You know, BQN I've got to add to the list and start learning that to figure out you know what is the ultimate array language not to throw shade on J, but you mentioned that you know there was a couple things over time, I'm you, you know, we've talked about some of the things that are different from APL. Can you talk about, you know? What are the, uh, couple things that you you know definitely thought J should have done differently or that you've done differently with respect to J? Like 'cause? I think you you started with J. That was what you learned in.

01:07:37 [ML]

Yeah, well and and yes I had my own graph and well, at the beginning it's hard to even say. Well of course J is better than TI basic and I didn't even know how to write loops in TI basic. I was using GO TOs all over the place. But so yeah, I have my own graph and and J has gone down on the graph and and yeah, the functions are a big part of it. Now J has fixed this in the in the latest version or the one before. Where now it's got this double bracket syntax. Which, you know, two brackets is a lot more than one. J as I've used it, and I've I've used. The only reason I use J now like since I started BQN is either to move my code over from J to BQN or to figure out what J does in a particular case. So basically not at all, but as I've used J. There's this this awful function syntax. The worst thing about it to me is that it really discourages nesting. But there's also the problem that even if it was alright for nesting, it wouldn't handle it very well, because if you're in an inner function and an outer function has a variable, then the inner function doesn't see it. Which Python also does this? And I also don't like it in Python, so Python allows you to declare a nonlocal variable to access one J doesn't. So this this just takes away a lot of the power of functions. And so. In this way, BQN is completely moving towards the mainstream, and I think a lot of the reason J was designed the way it was, wasn't. Like definitely it was a deliberate choice, but I think Ken and Roger, they've worked, Ken, pretty much entirely in J. As far as I know and Roger in J and C almost entirely. And other low level languages. But so they're they're really not familiar with. They haven't used things like JavaScript that have, that have lexical scoping, and it took me a while after I learned J to even learn that this was good, I think I slowly started to realize that. Oh hey, if you've got a function and you have a utility function that's only used there, you can put it inside that function and. And then it's sort of that tells you that that's where that function lives, is inside this one scope. So that's the only place it's used. Which you typically wouldn't do in J. And from there I kind of slowly realized that you know, having all this scoping stuff. That allows you to. To encapsulate things and say, well, here's this thing going on over here, here's this thing going on over there where you have this nested structure. Your program is really useful. And so in that respect, BQN just does what everyone else figured out 30/40 years ago. So other other problems with J. There are a lot of little technical things. One, one other thing that I don't like is the way it handles namespaces. So J has what it calls locales. Which are namespaces, but they're not first class objects. You can't. You can't touch them in the language at all. What you do instead is you have a number or a string that refers to this namespace. So you create a namespace and then you get a string and you pass this string around and you pretend it's the namespace, but it's not, and the issue with this. Is that well? First, it's really awkward, but. When all that you have, that's referring to the namespace, it's a number. Well, that's just the number you can't. You can't tell that number apart from any other number in the implementation. So the J implementation can't possibly tell when the last time you'll need the namespace is, it can't garbage collect them, and that means you have to do manual memory management in a high level array language on your namespaces, which is, that's not high level, that's very low level, that's. I think that's just not how it should be. So in namespaces are first class objects in there. There's a pretty nice syntax where you write the, the namespaces is pretty much just, it works like a function, so now we have lexical scopes. We can create closures, so namespace is like a closure. But you write this double left arrow with a double stroke instead of a single stroke for assignment to say this variable is exported and then you can, you can use the dot syntax to see the exported variables in a namespace and so on. So that I think like Dyalog also has namespaces, but they're done in a very C#-like syntax because they were influenced by C#. And so [BQN brings namespaces into APL](https://mlochbaum.github.io/BQN/doc/namespace.html) really. And I found that that works. Like of course you don't want to be using mutable data, and you can use immutable data. There's no reason to replace an array with the namespace, but namespaces do a lot of good stuff. Like it's nice to have a file that returns a namespace where the file defines a bunch of functions and so you get a namespace out and you can import it. And then use dot syntax to say. Well, I've got this file and I'm using these functions from this file and you see where everything comes from. So yeah, with regards to mostly variables and things like that, BQN is just a lot cleaner than J.

01:13:19 [CH]

Awesome Bob, Adám, do you have any final questions that we want to. I mean, I feel like we're going to end up having all our guests on multiple times at this point.

01:13:31 [ML]

Yeah, I hardly talked about the implementations, so there's that.

01:13:35 [AB]

You’ve not spoken about that other language?

01:13:38 [CH]

Well, there's a. There's a third language? Is this breaking news?

01:13:42 [ML]

There's also [singeli](https://github.com/dzaima/singeli), which which is more or less implemented, which we might use to, implement BQN probably will.

01:13:48 [CH]

So what was it called? It was called singeli?

01:13:50 [ML]

Yeah, it's it's named after this genre of Tanzanian dance music that's very, very fast. At like 300 beats a minute and so and so on. So, uh. So if you write your code in singeli, maybe it'll go that fast.

01:14:06 [AB]

There's also iridescence, iridescence?

01:14:09 [ML]

Yeah, that that's I thought that was that language.

01:14:12 [AB]

Oh, I didn't know that was it's changed name OK? Well no, no no. OK, it's just secret Oh no OK, it's just secret.

01:14:16 [ML]

But it hasn't changed name. I thought you were not naming. It's not secret.

01:14:22 [CH]

It's not secret anymore.

01:14:22 [ML]

I don't want to say like. The problem is I don't have time to to 'cause I'm spending so much on BQN and I don't have time to sit down and you know. Write out how your doesn't works and there's a. There's a lot of details to work out, so I don't want to make too much noise about it while it's still just a vague concept, but it it has a name, so.

01:14:45 [BT]

So one of the things I wonder about 'cause I was, I had a discussion over email with Dave Thomas in the last week about languages that are really good, well designed languages and why they're not popular and the big reason of you know, a lot of cases is because there's not a community to carry them forward, or there's not a use. So for example, you have swift and then you have Apple behind swift, so swift going to march on into the future because you've got this huge base that's going to carry it through. Where do you see BQN going from now? How do you get there? Because there's a lot of things as you described them, and I think are really amazing. I want to go play with it, find out how that part works, 'cause there's limitations I'm working around right now that I won't have with BQN and I can see, but the fact that it's a great language. How does it get to that next level?

01:15:36 [ML]

Well, so the absolutely crucial linchpin is going on podcast. Aside for that. So I think we we are in the process of slowly building a community so. By we I mean like partly the Community, but mostly also me and dzaima, who I unfortunately have not mentioned very much. But he's he's implemented all the C code in [CBQN](https://github.com/dzaima/CBQN), which is the C implementation, and he's done a lot of helped with a lot of the design. A lot of it was done by the time I left Dyalog, but he's offered, you know, a whole lot of advice and stuff. Uhm, so [in terms of the community](https://mlochbaum.github.io/BQN/index.html#where-can-i-find-bqn-users) we have this chat room you can join on either matrix or discord that's linked on the main page. We can link it as well and. And that's that's fairly active we have. You know, right now there's one person. Other than me, I'm there on all the time. There's one person who's working on a project now. He's been commenting for the last few days and there are a lot of other people who come in occasionally, so it's. It's it's nearly as busy as the APL Orchard, I would say, which is pretty cool. It's an I mean, you can only build so much of a community while the while the language is still under development, but the it's it's less and less under development. It's more and more complete and usable, and I've used it for all sorts of things so I know it's it's not vapourware. So I think we're working on that. And yeah, I do recognize that the community of a language is really important. One of the other things that I wanted to do in BQN was make it easy for anyone to to write libraries. And I think we have the basis for that. We don't have the actual architecture that you would. We haven't finalized the design of what you do for a library, but but it's clear that one of the things is that BQN uses relative file path, so you can just write your library and have files load one another really easily. You don't have to know where the library is loaded.

01:17:52 [BT]

It seems to me when you when you were talking about locales and and having them as you know, in the case of BQN they're an independent object that would make a lot of that a lot easier.

01:18:03 [ML]

Yeah, the namespaces are really important for that. So almost always, if you make a library, it's going to be a file that creates a namespace, like a file can return just one value, but. You might use that if you've got, you know one big function. You'd put it in a file, but mostly you'd be saying alright. This file is namespace, then I know because I export the things at the top and then that makes it easier to distribute and to see, you know. Here's this library. What actually is it? You can just read the top. Hopefully the writers put all their exports and comments about what to do. And things like that so. So BQN should be easier for distributing code, I mean, right now we're we're we're kind of gathering interested people, and they're they're joining the chat room and you know most people post once or twice, say they're interested, and maybe I'll hear from them again. Maybe they're using it, I wouldn't know. But we're kind of gathering interest for the community now. Oh yeah, I could mention one of the things that interested me when I first started BQN, I figured my users would be like you. These pretty established array programmers. And what I've found is that the established array programmers, now your response is pretty positive and I definitely get a lot of positive feedback, but often they'll try it and they'll see a few things that are that are just not like their language. And they'll say all right well, this is too much work for me or whatever or, or something like that and just stick with what they're doing. So we've got a few. You know, regular array programmers on the in the BQN chat room, and they're not the ones who post BQN code often. What's what I think is happening is that the people who have tried APL who had maybe even used it for a while or a few years but but really didn't stick with it, those are the people who are trying BQN and who are most interested, and who are, who are writing their little programs, testing things out and getting used to it so that some? I don't know what I do with that information, but it's it's an interesting thing to know that that's the group that I'm targeting, not not the complete new people, although also more interest from that area than I'd expect, not the, not the experienced array programmers who already know everything but the people who are. Who've got a little bit of experience, but not that much.

01:20:40 [CH]

So for folks that have a, you know an interest piqued and want to go type some BQN code in. Is there something similar to like TryAPL.org?

01:20:49 [ML]

Oh yeah, I mean right on the BQN front page, there's a. There's a little copy of the REPL with some sample code. And there's a. There's a, uh [REPL page](https://mlochbaum.github.io/BQN/try.html) as well, which which a few people have common is is pretty nice and easy to use. It's based on ngn/APL’s from earlier that's non, it's Nick Nikolov who worked with APL for a while. Used to work at Dyalog. It's now working on k. So yeah, you can definitely run it online. The JavaScript implementation is 100 or so times slower than the C implementation, but it's it's down to not really having noticeable lag. Now, if you write a really long program, it'll take a little while to compile it. 'cause this is running a self hosted compiler in JavaScript. But yeah, definitely you can use it online. Very usable and CBQN. If you're on Linux, at least, just clone and make, I think. Uhm, it's probably going to run on other operating systems. I think we've had Windows users use it, but if you have problems with it, just come into the chat room and ask, so it's definitely pretty easy to get started. And there's there's also I've written. I've almost finished the documentation. There's some there's like [3 1/2 big tutorial pages](https://mlochbaum.github.io/BQN/tutorial/index.html) to get you started. So there's a lot of material you can read about it to to get going.

01:22:13 [CH]

Well, some that sounds like we'll definitely put all of the links to those resources in the show notes which.

01:22:20 [ML]

It's going to be the one that should feed ever.

01:22:22 [CH]

Which I yeah. I think it's a perfect transition. Bob, you were going to say a couple things about the the site and one where to reach us, but also to you know what we have listed on on our website.

01:22:33 [BT]

Yeah, a lot of times you know I'm not sure people are aware if you go through the website it's it's a lot harder. For whatever reason. A number of podcast catchers it's a lot harder to get access to show notes, but each episode has an extensive list of show notes which Marshall pointed out earlier when we were before we started recording. Might not be the best name, although I think it's sort of the standard name of show notes. Really, what it is is a series of links that will take you exactly where you want to go for more information, so it's very useful to be able to go in. And and get information back out when you hear something you're not sure about. Quite often we're putting a link in that will actually explain things which for people who aren't as experienced. Or sometimes we're, I mean. A lot of times when we're talking, we're using our hands because we're trying to explain things that are more visual. Well, show notes is an easy way to get into that, and so if you go to arraycast.com each episode has its own page and there's a button that takes either to the show notes or to the transcript. So if you want to do a quick search on something I found that's the easiest thing to do. As you click on the transcript, you can do a search through the text and find out exactly where people were talking about things. Also, I imagine for web crawlers and stuff it makes it easier for people to spot things, so there's that and then also the final thing I'd like to mention about the arraycast.com if you want to send us an email, it's contact@arraycast.com and that will go straight to us. We're pretty good about answering our emails. We've had lots of good positive feedback which has been fun. We've had some feedback. I think it was two episodes ago. We were able to take some uh feedback from Melissa and actually incorporate that into an episode because we could address some of the issues that they raise, so doesn't always have to be positive. We can we'll use it anyway. We we aren't. We aren't proud we'll we'll take negative information and turn it around on ourselves. Not that I'm looking for spam, but I know what to do with spam too I. I think that's the the main things go to arraycast.com for the episodes you'll see show notes and you'll see transcripts and contact at arraycast dot com if you want to get in touch with us, I think that's all I've got for that part.

01:24:51 [CH]

Alright, awesome and yeah I'll I'll close out by saying. Thank you so much Marshall. It was another these episodes where we bring on guests and we just get to pepper them with questions or by far my favorite and I'll definitely be checking out BQN. It's been on my radar for a while now but, yeah, thanks so much for coming on. I feel like we're definitely gonna have you on again in the future to answer the remaining 990 questions that I have. And yeah, we'll get you to talk about the implementation and everything we didn't get to in this episode. So yeah, once again, thanks so much for spending your time with us.

01:25:20 [ML]

Yeah, thank you.

01:25:21 [CH]

All right, and I guess we'll finish by saying Happy array programming.

01:25:25 [Music Theme]

</details>
