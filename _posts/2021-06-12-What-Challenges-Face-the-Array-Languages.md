---
title: "Episode 3: What Challenges Face the Array Languages?"
date: 2021-06-12 00:00:00 +0000
episode: 3
buzzsprout-id: 18621529
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
  - "/episodes/episode-02-challenges-facing-the-array-languages"
  - "/episode3-show-notes"
---
<!--more-->

**Host:** Conor Hoekstra

**Panel:** Nick Psaris, Adám Brudzewsky, and Bob Therriault

---


## Show Notes

- [Nested Array Theory - Scholes](https://aplwiki.com/wiki/Array_model#Nested_array_theory)
- [What is an Array - Hui](https://www.jsoftware.com/papers/array.htm)
- [Is a Scalar an Array - Hui and Rich](https://code.jsoftware.com/wiki/Essays/Scalars)
- [Nuvoc](https://code.jsoftware.com/wiki/NuVoc)
- [Inverted Table - Hui](https://code.jsoftware.com/wiki/Essays/Inverted_Table)
- [Rectangles All the Way Down - Thompson](https://dyalog.tv/Dyalog18/?v=mK2WUDIY4hk)
- [Chunking](https://en.wikipedia.org/wiki/Chunking_(psychology))
- [Shape Thinking - Thomas](https://www.youtube.com/watch?v=ng-QNLdgQeY)
- [Perlis Epigrams](https://www.cs.yale.edu/homes/perlis-alan/quotes.html)
- [J phrases](https://www.jsoftware.com/help/phrases/contents.htm)
- [APL phrases](https://aplcart.info)
- [q phrases](https://code.kx.com/phrases/intro/)
- [tryAPL.org](https://tryAPL.org)
- [APL Orchard](http://apl.chat)
- [Dyalog ‘21](https://www.dyalog.com/user-meetings/dyalog21.htm)
- [Campfire](https://aplwiki.com/wiki/APL_Campfire)
- [Dyalog Problem Competition](https://www.dyalogaplcompetition.com?goto=welcome)
- [Thinking in APL Part 1 - Dyalog webinar](https://dyalog.tv/Webinar/?v=myoK22rq1jk)
- [Thinking in APL Part 2 - Dyalog webinar](https://dyalog.tv/Webinar/?v=Qzwn6z3y0DA)

<details markdown="1">
<summary><strong>Transcript</strong> (click to expand)</summary>

Transcript

Transcript prepared by Rodrigo Girão Serrão

Show Notes

00:00:00 [Conor Hoekstra]

I already have q on both my computers. It makes me want to go like... There's too many, you know? I gotta learn APL. Now I want to learn J and now I'm just going to end up having to quit my job.

00:00:10 [Music theme]

00:00:20 [CH]

Welcome to the third episode of the Array Cast podcast. My name is Conor, I'm your host and we're going to go around and do brief introductions. We'll start with Bob. Then we'll go to Adám and then we'll go to Nick, our first time, recurring co-host.

00:00:32 [Bob Therriault]

Thank you Conor. I'm Bob Therriault. I'm a J enthusiast. I am not a professional developer or programmer, I'm just really interested in the language and I've been doing it for about 19 years.

00:00:43 [Adám Brudzewsky]

Adám here, I work as an APL tools developer full time at Dyalog Ltd. I've been doing APL for about 25 years or so and professionally for 7-8 years.

00:00:58 [Nick Psaris]

Hello, I'm Nick Psaris. I've been working in finance for 20 some odd years but picked up kdb/q in 2006, uh, when I went to to Hong Kong. And I had many years of solo learning of the language and kind of my perspective from that experience has given me, um, i think different insights into the language. I've coded in many different languages, but my my favorite is definitely q, um, and look forward to discussing it today.

00:01:27 [CH]

Awesome and my name is Conor Hoekstra. As recurring listeners will know I'm a professional C++ developer at NVIDIA so I don't do any array programming per say in APL or J, but I'm a huge APL and J enthusiast and love getting to interview people on this podcast 'cause I learn a ton and hopefully our listeners get to learn as well. So I think we've got a super interesting topic for today, and that topic is to discuss why we think the array languages, APL, J, k, q, have not been as popular as of late. I mean, anecdotally, we can include a link to this article that has been sent to me by many people at this point of like [the top ten dead programming languages](https://www.hillelwayne.com/post/influential-dead-languages/), and sure enough, APL is on that list, so I'm not sure. Maybe we'll start with Nick because right before we started recording, you said that you had written up a long list of the reasons that you thought that array languages may have fallen out of favor. 'cause at one point they were. They were quite popular back in the 70s in the 80s, so let's kick it to Nick and we'll go from there.

00:02:32 [NP]

Sure, like I said, I've got like 10 items. Maybe I can come with more, but I'll kick off one or two of them and we can start from there and then we can come back around and pick off a few more.

I think, the the first one is about the community, and if you want to share code with other people, how are you going to do that? Uhm, there's no native import statement in, for example, in kdb, everyone kind of has to define their own, and that that problem of bootstrapping the language, um, is an issue, because you can't all agree on how does a package get loaded locally and you you can't import a namespace from, you know, let's say you had a .com and your package, your project, and then the subpackage. You can't, like in Python, you can say `from package import function`. None of that's available natively within the language, and so there's no agreement on how you can incorporate other people's code and that stifles a little bit of the community, I think. And along those lines, um, there is no centralized package management system. Uh, Pearl had CPAN, And then there's latex CTAN and Anaconda has the `pip`... I'm sorry, Python has `pip` and the Anaconda package management system. There is no communal package management system for q and that lack of community forces everybody, when they get the language, they say to themselves “OK, and now what? Like, what do I do with this? All I've got is the language. I don't have all the tools and the the logging utilities and timers and things like that and that." And that just stops you right from the beginning when you're learning.

00:04:12 [CH]

Adám, Bob, do you want to respond to that? Maybe from the J or APL perspective? Does that ring true for those languages as well, or is it a different story there?

00:04:20 [BT]

Yeah, it doesn't sound so much as it does for J. We've got an add-ons package. You start up with the language, you get the same package as everybody else, and then you can you can choose which add-ons you have, but you have access to all of the ones that have been written, so I don't think that that actually applies so much to J.

I kind of wonder, Nick, whether that's because of the way that q is used in a lot of financial institutions, are they actually trying to silo things a bit?

00:04:48 [NP]

Well, I mean. Like I mentioned, the language itself doesn't have an import. I mean you can load up a physical path, but there's no silent way of setting up a load path and then having packages installed locally and then imported. You could probably write your own code and I think every company has set up something to that effect, but it's all kind of, you know, everybody does it differently, and so there's no standardization.

To your point, that because the language is used in a corporate environment, there's less of a permission to share that code outside. I mean, I know in Python, for example, AQR let their pandas, you know, package be open sourced and then it went on from there, but there's no examples of such a thing in kdb.

00:05:39 [CH]

Adám, how about APL? Is it more similar to J or more similar to q and k?

00:05:45 [AB]

Definitely more similar to what's being described about q. There are a couple of issues really on the APL side and one is “yes, there is no real import and command structure” or anything like that, and people have kind of rolled their own things much in the same way.

There's also the problem that APL code is traditionally stored in binary blobs, called workspaces and not as plain text files.

And it also ties into the fact that APL uses special symbols, and until the advent of Unicode, everybody had to deal with those in their own way. So everybody had to roll their own code page.

And various vendors of APL were not compatible with each other, and people did invent systems, various transfer forms and so on, but just that those are our technical obstacles to sharing code. And I think also, especially for APL, it dates back so far that there was no Internet where you could just go and find stuff and share it. It was much harder to send something to somebody else. And so a lot of the veteran and advanced APL programmers are from that era where it wasn't open source, free things, people writing code out of goodwill, it just wasn't a thing, and that has influenced also that it hasn't gone into the various implementations of APL, until recently, so there are modern versions of APL that are beginning to go in that direction.

Text files for APL code and ability to require certain things, but no package manager or searching facility has really taken over and become the go-to place to find things.

00:07:44 [CH]

I wonder if there's a space, you know, another language that was created in the late 70s, before the Internet and package managers and, you know, the proliferation of GitHub, was Smalltalk, and Smalltalk struggled with the same thing for decades. And now, in the most recent Smalltalk editor [Pharo](https://pharo-project.github.io/pharo-launcher/), they have very good integration with GitHub, where you can now, even though you've got this whole class system,it keeps track of the delta of the code that you've added, and it's got a couple different sort of formats where you can export and then everything ends up in .st, sort of Smalltalk files. I wonder if there's a space in the array languages to, going forward, try and get some of that like GitHub integration 'cause as soon as you have that it just decreases the barrier to entry.

Right now, whenever I post APL code on GitHub, I'm just copy and pasting, opening up a text file and then watching the lack of an APL font on github.com just skewer some of the Unicode symbols, like tally, is the worst, like the slash through the three lines shows up like a whole character next to it.

I'm not sure is there any work, I would assume probably not for for k&q, but you know is there any work that's headed in that direction, or is there a space for that.

00:09:02 [NP]

I think that, well, the issue would be that adding a new keyword such as `import`, you know, might break things for people who happen to use that as a variable name or function name. So any new functionality would have to be put into what they have is this `.Q` namespace. So namespaces start with a dot and the `.Q` namespace is typically off limits to most people. You are not allowed to put stuff in there. So they could create a `.Q.import`, in principle, and a new environment variable which had a search path, for example. I think they could retrofit such a thing into there, and then... But it wouldn't be as, you know, elegant as native syntax, 'from package' like Python would have it, it would be a little bit more, uh, terse of course, but I, I think it could be possible for them to provide such a thing.

00:09:53 [AB]

There's a different requirement. The community has to get together and actually populate some kind of central place with stuff that you can import. It's not enough that there is an import statement and it's not enough to have just a plain text file hosted somewhere. There has to be a decided-upon structure.

How do you deal with connections between my stuff and your stuff that I've imported and all of these things? It's a chicken and egg problem, and at Dyalog we're very much working on hashing out these kind of things. What does a collection of APL code look like? What does it look like if it's in an end-user application? What does it look like if it's a utility, what if you want to use an end-user thing as a utility? How exactly do we package things up? What does the directory structure look like and what do we do about name clashes as you say? The order of importing things or a lot of things, and then where do people go? So there's a very very new project, called [Tatin](https://tatin.dev), which is a type of apple tart, (hence the pun) and the idea is that it's a strictly regulated collection of packages that people can submit, and then they're then subject to peer review and then there are what we call user commands, commands you can use from inside the APL session to automatically fetch those things from that collection place and deal with version control and all that stuff. There's a lot of design work that needs to be done. It's not just straightforward.

00:11:35 [BT]

In J, that's what the [add-ons](https://code.jsoftware.com/wiki/Addons/Developers_Guide) are and Chris Burke is the one that basically, I guess, is the sheriff in town for the Wild West that that is, although it's actually really well regulated, I'm making sort of fun of the fact that it could be crazy. It's not, it's actually really well controlled, but yeah, it's definitely a big job. He does a great job of giving people access and then once you've got access, I think it's mostly the honor system, but at this point in the community, everybody wants to put in things that are useful and quite often the biggest challenge is finding out what's in there because there's code in there that goes back, like 20, 25 years is a stretch, but 20 years, there are add-ons in there that have been written in the early 2000s that are really valuable. The language hasn't changed that much. There's a few changes, but it's sitting there and often you don't even know it. In fact, often when you're trying to do something, the first thing you do is you run back into into that, library and say, “is there something already written or at the very least something that I can adapt?”. Because you can copy those files down, you edit them as Adám was saying, they're not blobs, they're text files. There's plain text you can go in and edit them to make it work for you and it's very collaborative, very open, but it's really, really useful. It's a nice way to work with things, and it does interact with git. You can work with git, do your pulls and everything and have it go straight up to the up to the add-ons.

00:13:03 [NP]

So I'm saying I think along the lines of, you know, sharing packages and collaborative coding, another thing that goes along with that is the coding style as well.

And I know everyone is going to argue about the style, but unless you can read someone else's code, and these languages are so terse, I think it's really important to put some structure around that and don't allow people to have code that's, you know 180 characters wide and, you know, pretending to put k code instead of q code in the language. Like, you can do things to purposely make it confusing. But just like you know, Python has a PEP 8, for example, which says, you know, these are the standards and capitalization goes this way, and I think if the community got together, they need to put some standards so that you could jump right into someone else's code and kind of understand what's happening up front.

00:13:53 [CH]

Is this a comment on why another reason that the array languages haven't?

So it's the fact that maybe due to the terseness and the fact that we've got digraphs or Unicode symbols, or very short, you know, names of our functions? It enables more, sort of than other languages, freedom to create your own style and that can lead to the opposite of what like Go, a language like Go has, where they've just got a single formatting standard, and even a language like Python. They've got, you know, PEP 8, or black ,like they've got a couple options, but basically all large projects adopt one of the two, whereas in APL or J, if you look at Aaron Hsu's code of his Co-Dfns compiler, it is extremely dense and all his variable names are either one character or two characters and then he's just got a legend somewhere and for him he says it's just the most readable thing he's ever seen.

But there is like, a learning curve, and it's very, very different if you compare that to some other code, just like the APL dfns library, because you can go and look at that like it's usually a lot more linear, nicer variable names, so yeah.

Bob, Adám, would you agree that that is an issue and is there like a space for something like PEP 8 in the array languages.

00:15:18 [BT]

Well, actually I'd push back a little bit. Just because one of the things I've found, going back 15 years, seeing the evolution of the way the code is written because at certain times people have written code in certain ways. That actually opened up a lot of opportunities for me that I didn't know existed. I can see the way people have written in different styles. If it's well enough commented and it being, meaning, it tells you what variables are going in what, the purpose of the code is. Not that every line is absolutely, you know, diagrammed or anything, but just you get a sense of it. From that you can read it and you start to pick up the style, and the variety of styles, I think, is actually a strength in programming because you can adapt your style to what you're trying to do. There are times when tacit just works beautifully and there are times when you really want to go to a more conventional style with `if`s and `select`s and `do-while`s and things like that. You can adapt it to what you're doing. The downside of that is that if a person first approaches a language, they are reading a number of different styles, and that's sort of the situation in J you see a lot of different styles. There's really no format as long as you give it enough comments. I think it's useful.

00:16:37 [AB]

Yeah I would say, especially probably in APL and the least important in in k&q are some style guides, because it's important that a human can read the code and the syntax is very powerful in J and APL, but it also means that any particular phrase, say you have three names next to each other with spaces in between `A B C`, you can't tell at all what the structure of this program is if you don't know what syntactic class `A`, `B`, and `C`, are of, whereas k is restrictive on user-defined names to the point where it's, it doesn't actually matter what syntactic class things are. It all parses in the same way.

But on the other hand, it means that in J and APL you can write things that at least I find way more elegant and way more natural to the human. And so I think that it's not just that there's space for it. I think it's extremely important to come up with some style guides. I've personally been frustrated by this thing and I wrote up [my own personal style guide for APL](https://abrudz.github.io/style/), which is very strict, dictates exactly how you have to name things, and with that it actually makes it possible to do a static parsing of the language and without running it.

So I think that's part of what's necessary to make it easier to cooperate. But I also want to go back a little bit on the terseness. I think there's some part of it that has to do with feelings as well, again and again, as we at Dyalog are moving towards putting things on GitHub in text files, it feels so clunky. I make a repository, I initialize it with a license and a README file, and then I put my code there, which is a single text file with five lines of code. It's like “and that's it, that's my repository”, yeah, I mean, it's done. It's all full featured, right? You can do all these various things and I make a wiki for it and so on, but it's still only a few lines of code, it just feels wrong, in a sense, to over complicate methods with packages and things when it's faster to just type it yourself.

And with that terseness, I think there's also traditionally been a pride, especially in the older generation of APL programmers, that you don't trust other people APL code. You'd rather write everything from scratch every time. So when you build it up, you know exactly what everything is doing.

00:19:24 [CH]

Well, so this is really interesting because this speaks to once again to bring up Aaron Hsu. He has a talk, I'll find the name of it afterwards and send it to Bob so you can add it [[Patterns and Anti-Patterns in APL: Escaping the Beginner's Plateau](https://www.youtube.com/watch?v=v7Mt0GYHU9A)]. I don't recall 'cause I've seen too many of Aaron's talks, but in it he makes this sort of list of 10 points of what is idiomatic in other languages, like depend on libraries et cetera, and then sort of the equivalent in APL, which a lot of the times is different, and one of them is to prefer idioms and patterns to libraries, which is exactly what Adám was saying there, and I think that's great. The point being that a lot of the times where you need to depend on some third party library in another language it's four or five characters in APL. So the overhead is, and I'm sure it's the same in J&k&q, the overhead is so small that it's like “why go import something, depend on it?”.

That being said, there have been cases where I have been trying to do something, the example that comes to mind is like generating every single possible permutation or combination or sub-sequences and if you go to Adám's `[APLcart.com](https://apl.wiki/APLcart)` where you can search for this pre-written code that does it, the pre-written code is like 20 or 30 characters, there's certain things in APL or array languages where it's not four or five lines, and in that case, if I have to copy and paste 20 or 30 lines, really, I would just prefer to be able to go, you know, some like one-letter library dot `prm` for permutation, or even `permutation` outright.

So like I would be curious to get people's thoughts on that scenario where, you know, in general we do want to prefer the four or five character you know patterns or idioms, but sometimes it does feel like it would just be easier to depend on some built-in function from some library.

00:21:14 [BT]

In terms of J there's sort of two areas you can look at there. One is phrases. There's actually, within the dictionary, there's a section that's just [phrases](https://www.jsoftware.com/help/phrases/contents.htm), and it's actually just short phrases split out to things that you might want to try and, and it's not every idiom, but there's an awful lot of them, and you usually find an idiom that will work. Often the question is, will it work best in the new versions of J 'cause there's been improvements in certain areas where doing something a different way would actually be quicker, but at least it gives you a start as to what a common idiom would be, and usually it's the common idioms that have been worked on and then I, I suppose the other thing is that you do have this add-ons library that's broken up into different sections, different descriptions. So if you're looking for a math add-on you can go to the math add-on and you can see the things that have already been written, so that's sort of how they've structured it within J.

00:22:12 [CH]

So J might actually have, probably does have, the permutation function then somewhere in some library.

00:22:16 [BT]

There's actually a [number of them](https://www.jsoftware.com/help/phrases/permutations.htm), and recently I think it was Rick Sherlock, I'm just trying to think of what the function he was improving, I think it was [histogram](https://code.jsoftware.com/wiki/Addons/stats/base)– and I'm just going by memory –but I think he rewrote his histogram from, I think it was about 10 years ago, because somebody pointed out something itdidn't do well in a special case, so he just rewrote another case and now, well, the histogram is back working the way that you would expect it to work and it's just, it evolves over time, but he was able to go back into his library, update it, and now when you download that library I think you get just that version. But you might even get the old version in case you needed it.

00:22:57 [CH]

So I guess it's the question is more than for the languages without the package manager, what is the recommended solution for those? Is it just the copy and pasting of the thirty line thing?

00:23:10 [NP]

That's typically what people do. Yeah, I mean, there's certain small algorithms, I guess what you're referring to as phrases, which yeah, you read it once, you learn it, and you can incorporate that yourself. But when the functionality gets beyond just an algorithm, you know, q has JSON parsing natively inside of it, but, if it didn't, you're not going to go out and copy and paste that, you would prefer to just have a JSON library to import.

You know that I referred before like a logging utility or like kdb has a form of "getopts" natively built-in, but it's not very easy to use so everyone ends up creating "opts" or a "getopts" library themselves. This is kind of the first things you do when you start up a new project. Like, I need command line argument parsing and so you kind of write that. But why wouldn't it be something that you just want to import? Because it's not just 20 characters, it's you know a couple of different functions and print statements and things like that.

00:24:10 [CH]

Yeah, Python Python devs don't, they've got `argparse` or I think there's a couple different ones, but I don't think Python devs are ever writing the command line, you know, they just go import that, and yeah, they're done with it. They don't have to think about it. So Adám, do you have a thoughts on the 30 character solution to something. What do APL's do?

00:24:34 [AB]

Yeah, I think they do have a tendency to go and copy things around and no APL I know of has a standard library, meaning a collection of things written in APL that's always available to you wherever you are. And with things we discussed before and the complications of trying to import things, people tend to copy things around, and it's not just 30 characters. They might copy even substantial amounts of code.

It's not necessarily hurting anything. But in general we say as programmers you shouldn't repeat yourself and it means that if you want to add a feature in one place and you want to have a matching feature addition to another place, you have to go and track down all those places where that or similar code that may have been tweaked a little bit for other purposes, instead of using a library and then doing something with the result, has been used.

And so, off the top of my head, something comes to to mind is: the default display of arrays and functions in APL is rather sparse, it doesn't really give a whole lot of information, and so for many, many years there has been a function called `display` that people have used to draw some lines around pieces of an array to show its structure better. And I don't even know where it originates from. It's probably something that people wrote in the very early days of adding arrays of arrays. And just in say, a default install of Dyalog APL, there are more copies of that code then I can immediately count, it's just all over the place. And is it bad? I mean it's working and the code might actually be identical or functionally identical here and there. But I do find that it's a bit sad. It makes it harder to maintain things. So I think at some point you reach a limit where things really should be packaged up.

00:26:49 [CH]

So that's why you mentioned standard library and I had never even really thought about that, so I guess, briefly,[dfns](https://apl.wiki/Dfn), the library that is the go-to for a lot of things, that's not considered a standard library in APL. That's just a library that comes with Dyalog APL.

00:27:01 [AB]

Yeah, it's definitely a library, and some people say about it. It's like the closest thing that Dyalog APL has to a standard library, but in reality, and if you look at its description of itself, it is originally intended as a demonstration suite for the new feature that was dfns there. The sleek notation for very functional functions and then evolved into basically being where John Scholes would put in, he was the inventor of dfns, would put in his solutions to whatever subject of interest he had today. So when he was very busy with trees and dealing with trees and traversing graphs and so on, then he added lots and lots of functions to deal with that into the workspace. And when was busy with compression algorithms then he added one compression algorithm after another, but it's in no way a standard library. For example, a common operation is splitting a text on some kind of delimiter, and while it is in fact only a handful of characters in APL, it's something so common that you might actually want a standard library function for it, and it's not there because nobody has ever sat down and thought, you know, what needs to go into a standard library.

00:28:33 [CH]

Right, and just so I want to get responses from Nick and Bob as to whether their languages have standard libraries, but very quickly. Just because I know we've got a bunch of folks that are not array language developers. Do you want to very briefly sort of spell out dfns? Just 'cause I know the first time I heard it, I didn't know how that was spelled and explain just what a dfn is compared to other languages, 'cause we were or APL's were very novel or maybe not novel. No, it was not novel 'cause Lambda calculus came out in the 30s so. But yeah, do you want to briefly just explain that just so that our listeners that are going “What's a dfn? What's a dfn?” are not confused anymore?

00:29:13 [AB]

It's actually on Wikipedia, its own article on dfns. It's the name we use today for what was originally called direct functions or even dynamic functions. When I speak about it, to those that speak other programming languages, I just tend to call them lambdas and they are just a clean way of expressing a relationship between some arguments and the results without a whole lot of syntactic noise.

00:29:47 [CH]

Yeah, so “dfns” spelled D F N S. Yes and yeah so, other languages also, like Go doesn't call them lambdas, they call them function literals, Smalltalk calls them blocks but if you're familiar with an anonymous function, a function literal, a block, a lambda, it's all basically the same thing, and APL calls theirs dfns.

00:30:07 [AB]

What it mostly reminds me off is, if you look at JavaScript, you originally had this clunky "function, something something declaration" with a block and then finally you return something at the end and then recently extended with the arrow notation where you can have an anonymous function. Just defines some input to some output. It's basically similar to that.

00:30:29 [CH]

Back to the standard library. So did do k... Does k have a standard library or q?

00:30:34 [NP]

So yeah, I mean the short answer is “no”. My attempt at that was when I wrote my first book I was in between jobs when I said to myself “listen, I built a whole bunch of code in my last job and I don't want to write it again at my next job” and have it be you know, held captive, so during the time between my jobs I wrote, rewrote them as my own code, put it on GitHub and I said this is going to be the foundation for the book and so in the first book “[q tips](https://www.goodreads.com/book/show/25221469-q-tips)” I take people from the, you know, each chapter builds on a complex event processor engine but each chapter introduces a new part of the language by showing you a library. So one chapter is on logging and then logging needs the print statements and it actually checks how much memory the machine has and what's the current user name, what's the host name. And so I integrate building these tools into into the chapters of the book, and my hope was that I could extend the user base by just going out there and providing these libraries so that people could, I know there's no package management system, but at least they could, if they read the book, say “Oh my God, I could totally use this” and just like slap it into their code. There's no standard library, but you know, I've tried, you know, to try to give people some code to get them up and running, because anytime you write it inside of a company, it can't be, you know, pulled out in some sense. And because you have to pay for the license to run q and kdb, it's rare that people are going to be, if you're building something cool and complex, it's typically part of a company. So that's the problem.

00:32:16 [BT]

And with J when you first start it up when you first install it, you're going to create a number of scripts and what J has is, I suppose, they're kind of like workspaces, it's [locales](https://code.jsoftware.com/wiki/Vocabulary/Locales), and so when you're working within a locale, you have all your variables in that locale. You have the verbs you've described on that locale, and they're local to that locale, so you can move back and forth between locales so essentially you can make your code modular so it sits off and you're not going to get name conflicts or anything because you can call it from a different locale and come back and forth. Well, the standard locale, when you first set up the language, is the Zee if you're in the States, and Zed if you're in Canada, locale; and that locale is sort of a very base locale, you don't have to do anything to create it. In fact, there's a number of verbs and names that are already located already in that locale, and if you can't find a name in the locale you're in, it will default to that locale, so you can set a path that it goes through that, so that's essentially how you get access to all the things that have already been declared. So something like the name `each` is in the [Z locale](https://code.jsoftware.com/wiki/Vocabulary/ZeeLocale) and it's declared as an under. You open up a box, you do your work, and then you close the box. That's what `each` does for you, and so that name is available. If you declare `each` as something else in the locale you're working in, you'll override that, which can be surprising, but it's also very powerful that as you get used to the names that you can use, you can actually rely on the fact that the Z locale is always available to you and it's there for sort of the standard things, and then, as I mentioned before, the add-ons are in addition to that you have to load those scripts separately, but the Z locale is already set up for you, and that's sort of your base level for the J language.

00:34:12 [CH]

Interesting. So we've sort of stumbled into, I guess a third thing. It does seem to be that J is leading the way on a couple of these things, so the first one was, you know, a lack of package management and also the ability to just simply include some library or something of the like.

A proliferation of styles across these languages? You know, maybe to a certain extent, that has some benefits, but also can create problems.

And then also I guess J has a standard locale, but it seems that most of the array languages don't have a standard library, which I guess isn't too surprising. When you think of how the array languages started back in the late 60s and 70s, but yeah, so that's the three things, and two of them came from Nick. And then one of them organically showed up, so maybe we'll kick it. I'm not sure Adám or Bob if you want to choose one of the things that you think have been contributing to the less "mainstream-iness" of the array languages as of today. Adám?

00:35:14 [AB]

I cannot say that I'm a first hand witness to this because I'm too young, but my father told me a lot being that I grew up with him as a main APLer in the world and and he said that a lot of it is what you guys called political. And it used to be that companies, and even those that where the core of what they were doing was in computation. They would still have an IT department and a computer department. And at the head of the computer department would be some kind of manager who probably didn't know a whole lot about computers, but he was in charge of running the thing as opposed to today where things have to be slim and agile and so on. And there was a big thing in having a lot of subordinates under you. And so it was well-known that using array languages –well, APL, there weren't really any alternatives at the time –was a huge plus in productivity and people used to use a factor of 10 that you only need a 10th as many programmers. And everything gets done 10 times as fast and the code obviously is very small compared to what you otherwise would have to write and that met with active resistance from the IT managers because they did not want to have to get rid of 90% of their workforce. It doesn't look good on their resume. And if you come and say “I've had three people work under me”, “I've had 30 people work under me”, “I've had 300 people work under me”, it sure makes a difference and so, actually, it's interesting [in 1977 my father filed a patent brief](https://codegolf.stackexchange.com/q/119361/43319) with the Patent Office in Denmark for using, a slogan you could call it, in promoting APL, and he was an APL consultant, and it is an infinite sentence.

So you can start anywhere you want. It goes like this. “Easier communication means faster coding means fewer coders means easier communication means faster coding means fewer coders means faster communication...” and so on, right? And this is very much what you have in the array languages, that we slim things down, we find out what is the essence, the core of the algorithm of the thing you're trying to do, and get rid of all that, all the noise or the syntactic noise of all the structure around the very core. And IT managers, they simply don't want to see that.

00:38:09 [NP]

I think that come along those lines, uhm, what what you're seeing at least on on the on the q side, is that when a technology department goes out to hire somebody. Uhm, you know what do you need to hire? Technology departments have a a price on what they're willing to hire a developer for, and you could hire you maybe two or three if you have three headcounts, you could hire two or three Python developers or Java developers. But then when you come to a, you know a single q/kdb developer, or perhaps an APL developer, they typically be, they're typically more expensive because there's fewer of them, and they just, they're priced out of it. Like the the manager can't hire the person because of the cost. And well, you don't need three people, you just need that one to get the job done. Yes, he's more efficient, but you run into this problem of of of what does it cost to hire a a resources.

00:39:11 [BT]

I think the other thing that becomes an issue when you've got very small departments is what I've heard referred to as the as the bus problem. What happens if somebody gets hit by a bus? You if you've got one or two or maybe even only one person who's doing the coding and something happens to them now,you might have a problem. And that's not something that I think a lot of companies are willing to, you know they like a little bit of redundancy. They don't want too much redundancy. Some people would say that becomes government, but like a company you want a little bit of redundancy, so that's your fall back in case something else happens. And I think that can be actually sort of a drawback to the languages. They're very powerful, but because they're very powerful, you also are concentrating that power in a few individuals and that can be risky.

00:40:01 [CH]

Yeah, the the bus factor is, I prefer the less morbid lottery factor, which is the same thing but doesn't involve anyone being hit by a bus. Interesting, so yeah, I had never really thought about that. The political side of things and and when you said that Adám, it made me think of another political thing and this is for of contrasted to the history of C++, which for those of you that are not familiar, C++ was developed by Bjarne in in the 80s and it ended up they started working towards standardizing the language so it has a ISO C++ standard. The first standard came out in 1998 and there is at least three primary, and then there's a couple others if you include Intel, but there's a GCC, clang and MSVC, three different basically, implementations of the standard library and the language all working off of the same standard, and I think that's been amazing for C++ - it leads to more bugs being caught. It leads to competitiveness in implementations, and it's just a great model. If you compare that to what I know about APL, right around 1980, there was like a fracturing of, I don't want to say the community, but you know, Kenneth Iverson ended up leaving IBM to go to IP Sharp. And that's where APL2 and then the start of like Sharp APL. And so then there was this like fork in the road where there were two different implementations, and if you look at [the diagram Adám was showing just I think last week at the British APL webinar](https://aplwiki.com/wiki/Family_tree_of_array_languages), there is a ridiculous proliferation of like implementations, and all of them sort of to a certain extent, competing with each other, helping each other in certain ways because one good idea is implemented and then adopted, but you end up with these sort of flavors or variants, which means that if you're going from APL2 to Sharp APL and back, whenever it is or from nowadays Dyalog APL to some other APL implementation, you don't know exactly what to expect. Obviously a certain percentage will be the same, but it's not like C++, where if I go from using the GCC compiler, I just copy and paste my code and go use the clang compiler. It should work identically, and if there's a if there's a problem that means that there's a bug somewhere in the compilers, so it has that. Is that a good thing? A bad thing? Like what how does the APL community view sort of the the variance if you will? That started popping up in the 80s and sort of exploded.

00:42:44 [AB]

Wasn't just the 80s, I mean yes there was the big split between the two different ways of having arrays of arrays. Between Jim Brown at IBM and Iverson over at IP Sharp, even before that, then again, time back to the fact that people didn't share code and nobody really shared code back in those days. No matter which language they were in, every hardware manufacturer, with respect for itself, had to have an APL implementation. And of course, and so they made one, and though there wasn't really any standards, the standards weren't really as common back in those days as they are today. And even if you took a reference implementation, so IBM's APL 360 was very much like the original APL, it wasn't the first implementation, but it very much was the standard by which everything else was was measured, so everybody cloned that basically. And then they had to add additional features because it was too bare bones and there wasn't any standard on all those additions. That's really where it is, because I think APLers very much are proud of the fact that you can take code that would run 50 years ago and you just stick it into a modern day interpreter and it will just run all the same. It all works, no need to set any compiler flags or anything like that. But it's all those all those additions that were there to the language. It's literally why it was called APL “plus”, because it's with additions. That's where things diverged, and then once they added arrays of arrays then there was a huge conflict, and that splintered the community. Eventually, the APL2 side won, probably due to the, if you say the economic heavyweight of IBM, right.

00:44:56 [CH]

I think they were making making money back then. They had profit margins.

00:44:58 [AB]

Exactly, so when Reuters brought up IP Sharp for their collection of raw data, but wasn't interested in continuing the APL language. And Iverson went on to create J, and at that point, and so that whole branch of the APL tree was abandoned. And Arthur Whitney left to create his A language and A+. And k. And nobody was left on what was Iverson's vision of what APL could and should be.

Today there is only that one type of APL, but every vendor has added their own utilities to it, and they're not compatible, and again, code in binary blobs. You can't transfer them. I think there is a, conversion, converging, going on and toward more uniformity, at least in the core language. Dyalog has been a very strong player, both in spreading the word of APL and making it available to people, and so various hobbyist implementations tend to follow what Dyalog APL has done, but not every implementation does. And yes, it does fracture things, but a lot of literature, even if the code cannot be ported, a lot of literature can be shared, and that at least is good for community building.

00:46:32 [CH]

Speaking of Arthur's k, Nick, is there an impact of, you know Arthur is, you know, famous. I think it's even been mentioned on the podcast before that he'd every couple of years he you know, delete hits, CTRL+ALT+DELETE on his computer or not CTRL+ALT+DELETE, CTRL+SHIFT+DELETE and wipes everything, starts from scratch and that's led to, you know K0 to K4 which became q and then k se– like has that impacted things or.

00:47:02 [NP]

I think that the the the the small community where everybody knew each other, I mean because when when Kx started it was, you know like there's like four or five, you know four people, five people, and it stayed that way for for years until you know it started to get bought out by first derivatives.

Uhm, that that small community where the the innovation was focused on the language, like what can we add to the language to make it better? That was, it was an amazing time. I'd send in requests and you know within like a couple of days, you know a new feature was added or a bug fix was fixed, you know, a bug was fixed. That, all you needed to do is convince Arthur, at the time, that A made the language faster or B it made the syntax shorter or something like like, as long as it was more elegant or faster like that was enough, right? And it got in there. That's not necessarily, I mean, there's definitely that vibe still in there, but it's not as as powerful anymore. The the new features on on q are more for big datasets, it's less on a language and more about integrating it with massive datasets and things like that.

Now admittedly, he's gone on, Arthur has going on to, you know, start a new a new K9. You know in his company [Shakti](https://shakti.com), and he's definitely also focused on really, really, really big datasets. But also the language itself. And he's he's made a lot of updates to the language, one of which you know, in some sense, there is competition there, one of which was all the primitives in the language are now natively parallelized. So if you start your process up with four threads you you run a a command. If the algorithm can be parallelized with 'each', it will use, you know a parallel 'each' instead under the hood, like you don't have to try to do it. That, word got out about that and that was backported into to q. So q now has that functionality under the hood and so you know Shakti needs to kind of push the the the the the the barrier, you know the the target further along, you can't just add a feature in, so they will, they will add things in in k so that competition in a little bit is is a good thing.

But the language in some sense in q is is, you know it's baked, it's done, it's it's pretty stable. It's not going to be enhanced. The core language and and what Arthur is doing now is, like you know, it's over and over, changing the syntax over and over just to make it as elegant as possible with with people contributions and say “well, what if it did this? And what if it did that?” It's pretty powerful, what what he's been what he's been doing with the language.

00:49:37 [BT]

Yeah, I follow the the Shakti mailing lists and stuff to just and it is just astounding to watch them shift and change something in process and, you know somebody will come on and say well this isn't working. Oh no, your version is like from 3 days ago come on like what are you thinking? This is amazing and I guess the the expectation there is that yes, you will update as soon as the new version comes out. You just keep you keep up with the with the herd and if you don't then you're not going to come on and be taken very seriously for very long if you're you're complaining about things that were three or four or five versions ago, which might have been last week. So, it's really amazing to watch it develop and and and it's there's a lot of power to it, but I would imagine if you were, and I don't think anybody ever is proposing this. If you were a company, there's no way you're going to be basing it on what Arthur is doing with Shakti right now. In the future, I think obviously there'll be some standardization. And then it'll he'll go off and and hit, you know, CTRL+SHIFT+DELETE again and start and start off, you know on his on his new adventure, but right now it's fascinating to watch this development go through and and it's one of the it's funny we're talking about what was holding the languages back.

It's like so many things they're the same thing that holds them back is the thing that is attractive to them and so a lot of what I find in the these languages is, there's such an exploration. There's such an opportunity to go in and explore different ideas. Do those kind of things. At the same time that sense of exploration is not for everybody. There's a lot of people who you know want to use a computer to get a job done and a specific job done in a set, you know a set length of time, and so it's kind of like. Well, I I can use this cart to get from A to B and why would I want to use a 10 speed bicycle if they don't carry as much? Yeah sure, they're faster, but I have to learn what the brakes do. I have to shift gears. Why would I do all that? I just want to get from A to B and I think that's it's really interesting 'cause there's also a culture,

I think, of people that have picked up array programming languages that they're actually easier to pick up for people who haven't already learned a more traditional language. So it's like you've got these levels at a low level of experience, not a low level of person but a low level experience. You've got people who haven't been exposed before, and an array language might actually be very easy for them to pick up. And then you get trained in the computing sciences and you learn what your structures are and your strings and your trees and all these things and you get to that point. And then it becomes harder to pick up an array language. But the people that haven't had the experience, it's easier to pick up an array language, but they're not as familiar with computers, so there's this, it's almost this step thing that gets the level of experience with computers gets in the way of making that step up to array languages, and people who don't have as much experience are less likely to use a computer.That way, they're less likely to explore with a computer. They're more likely to use a computer as a tool.

And one of the examples I can think of in that is is Excel, where you have people that are using a computer as a tool. And you look at what Excel did and people actually are, I think legitimate programmers with Excel, and I think Excel has added a [lambda function](https://www.microsoft.com/en-us/research/blog/lambda-the-ultimatae-excel-worksheet-function/) which actually allows you to write programs in Excel, which is a new thing. But it, but it's something you can see that language evolved into what it needed, which was a higher end and and APL, J, q, k, those languages were that high end and, and you could sort of see where that base level of user when they needed the high end, they didn't jump the computer, they just said, well, well, let's do it this way and then they came up with lambda.

00:53:45 [CH]

I feel like Microsoft just wanted to be able to say that Excel is now Turing complete, so they tapped Simon Peyton Jones, their Haskell guru and said hey make it happen and then fast-forward a year they're giving a talk saying Excel is now Turing complete. I haven't played around with the lambdas, but I saw the demo and it's it's scary. It's scary to see what's going to come out of that.

00:54:08 [BT]

Well, and that's a case where the freedom the freedom that's developed there, now they'll have a different challenge to work with, because that freedom is really going to create a lot of with people that weren't thinking or and have not thought traditionally the way computer scientists have thought about computers, now you're just giving the keys over to. You know, Tommy teen. Let's see where they go.

00:54:33 [AB]

I I think we know we know exactly what's going to come out of it. Somebody is going to implement Conway's Game of Life in Excel.

00:54:41 [CH]

I'm sure you could do Conway's Game of Life even before lambdas but using the lambdas would be a neat, now some listener that's a request. If you do it, tweet us. Tweet at us at @arraycast and and we'll mention it in a future episode, but we're getting close to the end of time, but I know that Nick, you said you had a list at 10, so maybe what we should do to wrap up is if you want to like rapid fire, just read through the rest of your list and then maybe we'll choose one or two to sort of quickly round off of, you know between the three of you, you know, which one of those do you think have led most or contributed most to the lack of popularity these days?

00:55:18 [NP]

So we've covered, I would say five of them already. I think you know, in essence. I think one of the other ones to start with, is like the the feeder system like where are people going to be picking up the language. And, you know, I know [academia is an important place for languages to be harnessed](https://kx.com/blog/kx-in-academia-carnegie-mellon-university-teaching-with-kdb/), and because they will produce graduates, PhD or masters students who are already experienced and versed with the language that they can just be hired and and plugged right in. And if we can't get the languages into academia there, there's a big hurdle there because then you have to train them on your own money, in some sense, you hire the person and you have to train them up.

So, where is that training going to happen? It would be great, you know, if if if people did research in these languages and they were forced to learn them, that now that goes on to the next bullet point here is is the price tag, at least for for q and kdb you know it's it's it's a private company who owns it, and there's a license for the 32 bit, oh, actually, you know these days you can use the 64 bit version of q, as long as you're constantly connected to the Internet and it sends a ping and you can run it on 4 different instances of it. But that price tag is, you know it's something to be to be considered when an academic institution is considering whether or not they're going to be, you know, doing some research with that language.

Another item is uhm, and this kind of shifts too beyond just the language, kdb is used in a corporation as a database, and I've seen the ground, it was a leader in that space for many years at least for massive massive time time databases. Ticks, quotes, and things like that. The the problem here is that it's great when you're running the process as yourself and you have a full control of it, but it doesn't scale well when you open it up to other individuals. And so the q process itself doesn't have some some some robust functionality and one example is you know if if a client connects to your server and allocates too much memory, the server will crash, the process will crash. Like for a corporation you cannot allow that to happen. And how do you? How do you prevent someone from connecting to your software and killing it? It needs to be a bit more robust than that.

And then the last one, as far as the database side of things, there are alternative databases that allow you to partition on things beyond just for example, a date symbol is one example, and when I'm talking about partitioning, when you get data from a vendor, you usually get it every day, for example, and so you can put it into a date partition and then yesterday's date doesn't get touched. It's a clean copy and then you just keep adding partitions and and the directories you you don't have to load the whole database, you can just load your little partition.

Other databases allow you to partition on things like a string or a symbol and you know you might take an example as an option tick database and there you have a bunch of different option exchanges in each exchange has a, you know, you know the exchange symbol and when you get the file from the vendor from the exchange, you want to just store that into a directory in addition to as a subdirectory, for example, of a date and so all the partitions are separate and then the database only needs to load one of those partitions at a time when your 'where' clause filters on that.

Now Shakti does, I believe, allow you to have nested partitions, and so that's a fantastic attribute that Shakti is incorporating and it's along the lines of other databases that allow that as well, but that's what I've seen is is a hindrance to the growth of kdb specifically.

Academia is something that maybe other languages can share, so I I can stop there.

00:59:13 [CH]

So yeah, I think the one thing we should mention, so q, I definitely know you can, yeah, download a version of it, but it is a limited version. They limit the number of cores and because it is a product that you have to purchase for, you know to use it in a corporation. But J is just completely open source and you can go and download that and then APL, I believe for a very long time you needed to sort of register to get a free copy, but these days, for non corporate purposes –Adám, you can correct me if I'm wrong –as a student or as someone that's not profiting off of it, you're able to go and download Dyalog APL. And it's a nonlimited, so it's completely what you're using at a corporation. That's correct? So it's J and APL you can get access to the full thing and it's just q. Yeah, correct me if I've misspoken there.

01:00:04 [AB]

Oh, it's it's even more than that, actually. I just checked this today and even if somebody decided to explore APL and they could develop their their whole system with Dyalog APL on the non-commercial license, meaning just download the thing and no questions asked. It's only once you start making money on it that we would ask for for royalty on that. But there are other APL implementations available as well, including some open source ones.

01:00:31 [CH]

So that's that's good to know, so I I think maybe the the point that one of the point that Nick made that's most relevant and probably could have the biggest impact is the feeder points. Like you know, how do we? Is it possible to get certain courses or certain universities and I'm sure there are definitely some, you know, a handful of universities that either teach a comparative languages course that one of the languages that they focus on is APL or J. And I definitely know in the past there used to be a ton more, you know, back in the 80s. What are what are folks thoughts on? Does that exist? Is there more we can be doing, Bob?

01:01:14 [BT]

Yeah, back in the 80s.

Yeah, that's actually when I was doing my computing science degree and and I was at Simon Fraser University and there was actually a guy there named Ted Edwards who was a real advocate of APL, and so, as a result, I didn't take courses from Ted, but I there was comparative languages that took a comparative language course, and APL was one of the languages that I could use, and there were people around that who were using APL, so that was actually the first experience I'd had with APL.

I think that's a big deal, but you know, to be honest, my sense and this is since I've got out of school and I've sort of bounced around the world, academia is actually one of the most conservative places to try and get changes done. It's almost, it's really difficult. People get really entrenched in what they believe in, and they and it's a difficult road to hoe in that.

I my background actually is in Community television and so my sense is you look for a population that would be more likely to take something viral, and so you're looking for a kind of population that's already exploring. And just as an example, if you look at the people that are doing maker kind of things and I know Dyalog is in the past, done things with [Raspberry Pi](https://www.dyalog.com/dyalog/raspberry-pi.htm) and things like that. It's a really powerful language to use in those areas, and although you're not going to get a corporate change at that point, the popularity of the language could grow astronomically if people if you're working next to somebody and suddenly their device is doing something you can't do. And they're changing things much faster than you can. I don't think it would take too long to have you know people uptake, take up those languages and say “oh, how are you doing that?”. And that's more of a viral approach, and you might actually be able to drive some changes in academia by grassroots, because at a certain point, if all your students are coming in and they're already using an array languages, why are we doing this like? Well, why do I need to use a loop? Right, why I can I can do this functionally? I could OK give me Haskell, I can work with Haskell, but I don't I I don't really want to go back to, you know, some of the more traditional procedural languages so I don't know I think, although academics is a really important, it might not be the easiest thing to breakthrough in a traditional sense.

01:03:44 [AB]

I've found that the [code golf](https://apl.wiki/Code_golf) community or communities, meaning those programmers that for recreational purposes, compete for the shortest code possible and have are much more receptive, even if they do have computer science degrees and and do program in normal programming languages or more common programming languages, and they're much more receptive to to the to say the message of the array languages because they already have the mindset of thinking out of the box in order to, you know, at all costs and make the code shorter. That doesn't mean and it's especially dangerous for these languages that you should be golfing your code, because that makes it, as Nick mentioned before, because it's almost impossible for people to read and and then, and it may impact performance as well. But I really think it's the open minded, people say the academia can be stuck in their ways. You need to find those, the impressionable crowd and really get it out there to them.

01:04:48 [CH]

I was going to say to speak to the conservativeness of academia. I took a online course, was it a year ago in the last year or so and it had it had like a prof component. And one of the exercises, it was a course that focused on advanced algorithms and it was to implement a pseudocode solution to the balanced parentheses problems. You're given a string with left and right parens and figure out if it's balanced or not, and this is very, this shows up in like APL papers from you know, 30-40 years ago, so it's a a very common paper or problem that is easily tackable solvable with scans, which you know makes it perfect for APL. So and I didn't want to, you know, I figured putting an APL solution in a single line wouldn't count as like pseudocode. So I wrote like a Haskell pseudocode that made uses of like fold scans, maps and zips, and the feedback that I got was like don't do this again. This is not this is functional pseudocode, I just want pseudocode pseudocode. When you write a paper, you know the academic community is expecting you to be using this sort of like Python-esque for loops and if statements and I was just made me so sad because like in my opinion, the pseudocode of like the sort of functional Haskell style, which is really, I'm just trying to like, you know, figure out a way to put the closest thing that'll be accepted to APL in my assignment. It was just yeah, completely rejected and in my opinion it looks way nicer than the the imperative sort of for loops things, but yeah it was You know, I sort of expected it. I wasn't like super disheartened, but it was, I was hoping there was a part of like a small voice in my brain being like maybe the Prof will go “This is amazing”, but that did not happen at all.

01:06:33 [AB]

Well, I can say it's not really academia so, but when I was in high school I wrote a paper in we had to write some final paper in the end of high school and I chose my subject to be mathematics and the subject in there was whether there is room for improving the mathematical notation that we use. I was already already very used to APL at the time, of course, and of course my answer is “yes, there's plenty of room for it, just do APL instead”, but they they took that. I mean, I got the highest grade on the paper. And if the even though the teacher was there, that at the high school, he was actually a university professor in the mathematics of education and he seemed to accept the fact that APL sure did seem superior to traditional mathematics.

01:07:36 [BT]

And actually building on the previous comment that Adám had about code golfing the other place, and I know Conor's big into this from a [recent interview](https://corecursive.com/065-competitive-coding-with-conor-hoekstra/) that I heard him talk about, is LeetCode and those code competitions. If a few of those competitions adopted an array language, that would actually make a huge difference, I think, in uptake because you've already got people that are looking to compete based on speed and ability to use algorithms and identify things, and in a lot of the array languages, it's almost an unfair advantage to approach a problem that way because you've already got your your symbols and everything built to go, you know that's a big step.

01:08:19 [NP]

There's an annual [Advent of Code](https://apl.wiki/Advent_of_Code) you know, come towards the end of the year and Christmas time, and you know, there's lots of competition who can write, you know, the fastest code to solve the problems. And you know, I honestly felt that with all of our you know, slap, patting ourselves on the back, that our languages are better, in fact, the the winners are not APL, Q, or J programmers. They are the people who are doing it in Python or Perl with regular expressions or something like that. You know code golf is cool and uhm, but like if you're looking for, you know, getting your idea implemented as fast as possible, sadly, uh, you know, these languages are not always the best solution. Although I think they're easier to map from the screen into your brain or or vice versa, those competitions are not often won by these languages.

01:09:13 [CH]

Yeah, it, I think it depends on the problem. Like one of the observations, 'cause I've competed in Advent of Code a couple times, is that all of their problems, especially after the first couple are very heavy on the parse side of things like they give you some like, oh, here's a paragraph or here's some comma delimited blah blah and like the worst ones are like you know, you have to pull the the first word before the 1st comma out and like the third to last word from the end and then also you know something else, and yeah, doing that in APL, you can do it, but it's not what APL was designed for, so a lot of the times, like you know Perl with Regex, it's going to be way more performing, but on on the flip side, things like on LeetCode, there's definitely like the first couple questions sometimes are super, super easy and like one of them the other day or not the other day, but in the past you know several months was like transpose a matrix. Well, show me an array language, a non-array language that can beat, like APL, single Unicode character or q's you know, flip, I think it's called or J, I think has also a single digraph for it. So yeah, I think it depends on the type of problem, but definitely for certain types of problems, because that's the thing, Advent of Code, you aren't given like a function signature or anything like that like you're just given the problem statement and you have to input the result, whereas in LeetCode they give you like a little function signature and you just implement it. So it's literally just implementing the algorithm. You don't have to deal with parsing if they're going to give you a, you know some text that's going to be in a string or a vector of strings, so. Yeah, it's interesting for a certain for a certain category of problems I think array languages are untouchable, but then for certain other category definitely you know Pearl is going to win.

We're definitely, I think, a little bit over time here though, so maybe I'll go around if there's you know any last comments from folks about, you know, why people, so we've been talking about why the languages aren't as popular. Maybe there's some flip side to that on, you know, if if you're, as Adám mentioned, the open minded, curious person you know don't don't worry about everything we've been saying, the lack of a package manager and the different code styles I'm not sure. Yeah, any final comments from folks. The return of the array languages, it's coming. I can feel it.

01:11:33 [BT]

Well, I guess one of the things that we've done is we've created a podcast, right? So I mean, that's one way to get the word out to people. I mean, I think quite right now we're probably preaching to the converted, but I think there's a long tail on these things, and this episode might be listened to three or four years from now from somebody who's taking coming at it from a completely different perspective. And that's how communities grow. So I think just by doing these kind of things, getting the word out there, I think it makes a big difference in addition to everything that you're working in building libraries and explaining things and doing teaching and online, you know, youtubes and all those things, they're all important, they all contribute and at some point I think there'll be a critical mass and you may find that in certain areas that these language really, really go viral, because I think that's got that kind of potential.

01:12:28 [AB]

I would say I don't think everybody listening to this podcast is already convinced about using the languages. They might just be curious and we're all this talk. Just try it at least for APL the barrier to entry is actually quite low.[tryAPL.org](https://tryapl.org) and just try it. Don't worry about learning the whole language, mastering the whole thing. Just try a couple of things. Look at the examples and it takes a certain mindset, but you might just get hooked.

01:13:00 [NP]

Just my my experience was, I loved Pearl when I first started, I've done Java and C++ and and I had a conversation with with with a fellow about you know he was telling how kdb was so awesome, and I was like, "well can't possibly better than Perl". And so I started. I started my job, and I was, you know, immediately sold on the language. And I would say the reason why, for me, and why you know I come to this language, is I am personally very efficient. It's just, it's a, I hate wasting my time. I hate writing lots of code looking at functional interfaces. The operators are so well overloaded that the vocabulary that you need to use is so small and it just handles it every single time that I can get my job done at work, and fun at home, just so efficiently. And my journey ended there because I just didn't want to give up my personal efficiency in coding.

01:13:57 [CH]

Yeah, that's awesome. Yeah, maybe that you sort of answered a question we didn't ask is “you know why do you love the array languages?” And maybe whenever we have either recurring co-hosts on for the first time, we should make sure to answer 'cause that, yeah, a lot of what you said really rings true to me. Why write anything more than plus slash? If you're going to sum some numbers like that's all you need 2 characters and you're done. And then when you do anything else in any other language, you're sort of sad about how much you're typing or why do I have to specify the you know initial element of this list.

But yeah, that's awesome and I think this was mentioned at the beginning, but Nick has a [couple](https://www.goodreads.com/book/show/25221469-q-tips)[books](https://www.amazon.com/dp/1734467509) on q which I think in within the q&k community are regarded as like the [gold standards](https://vector.org.uk/book-review-fun-q-a-functional-introduction-to-machine-learning-in-q/) of sort of where to get started. So we will for sure put show notes links to in the show notes to those books, and we'll probably have to have you back on as like a you know the interview guest where we just we just pepper you with questions about the q language and what it's like to write those books so, yeah, I think I think with that we will, we will sign off and wish everyone happy array programming.

01:15:00 [Music theme]

</details>
