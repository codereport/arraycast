---
title: "Episode 43: John Earnest and Multimedia"
date: 2022-12-24 00:00:00 +0000
episode: 43
buzzsprout-id: 18617084
keywords:
- array-programming
- array-languages
- conor-hoekstra
- k
- ok
- john-earnest
- decker
- lil
- special-k
- beyondloom
mp3-url: "/assets/audio/episode43.mp3"
episode-type: full
explicit: "no"
block: "no"
layout: podcast
excerpt_separator: <!--more-->
redirect_from:
  - "/episodes/episode43-john-earnest-decker"
  - "/episode43-show-notes"
  - "/episode-43-transcript"
---
John Earnest returns to talk about his work extending the array languages into other domains and his new project, Decker.
<!--more-->

**Host:** Conor Hoekstra

**Guest:** John Earnest

**Panel:** Marshall Lochbaum, Adám Brudzewsky, Stephen Taylor and Bob Therriault

---


## Show Notes

- [https://twitter.com/a_brudz/status/1607653845445873664](https://twitter.com/a_brudz/status/1607653845445873664)
- [https://beyondloom.com/](https://beyondloom.com/)
- [https://github.com/JohnEarnest/ok/tree/gh-pages/ike](https://github.com/JohnEarnest/ok/tree/gh-pages/ike)
- [http://johnearnest.github.io/ok/index.html](http://johnearnest.github.io/ok/index.html)
- [https://vector.org.uk/a-graphical-sandbox-for-k-2/](https://vector.org.uk/a-graphical-sandbox-for-k-2/)
- [https://en.wikipedia.org/wiki/L-system](https://en.wikipedia.org/wiki/L-system)
- [https://aplwiki.com/wiki/K](https://aplwiki.com/wiki/K)
- [https://docs.python.org/3/library/turtle.html](https://docs.python.org/3/library/turtle.html)
- [https://en.wikipedia.org/wiki/Swift_Playgrounds](https://en.wikipedia.org/wiki/Swift_Playgrounds)
- [http://worrydream.com/](http://worrydream.com/)
- [https://processing.org/](https://processing.org/)
- [https://www.arduino.cc/](https://www.arduino.cc/)
- [https://github.com/dzaima/APL/blob/master/APLP5/docs](https://github.com/dzaima/APL/blob/master/APLP5/docs)
- [https://github.com/dzaima/BQN/blob/master/app/readme.md](https://github.com/dzaima/BQN/blob/master/app/readme.md)
- [https://en.wikipedia.org/wiki/Arthur_Whitney_(computer_scientist)](https://en.wikipedia.org/wiki/Arthur_Whitney_(computer_scientist))
- [https://aplwiki.com/wiki/The_name_APL](https://aplwiki.com/wiki/The_name_APL)
- [https://aplwiki.com/wiki/Adin_Falkoff](https://aplwiki.com/wiki/Adin_Falkoff)
- [https://aplwiki.com/wiki/Dyalog_APL](https://aplwiki.com/wiki/Dyalog_APL)
- [https://aplwiki.com/wiki/Dyalog_Ltd](https://aplwiki.com/wiki/Dyalog_Ltd)
- [https://en.wikipedia.org/wiki/Zilog](https://en.wikipedia.org/wiki/Zilog)
- [https://beyondloom.com/tools/specialk.html](https://beyondloom.com/tools/specialk.html)
- [https://www.khronos.org/opengl/wiki/Fragment_Shader](https://www.khronos.org/opengl/wiki/Fragment_Shader)
- [https://learnopengl.com/Getting-started/Shaders](https://learnopengl.com/Getting-started/Shaders)
- [https://learnopengl.com/Getting-started/Shaders](https://learnopengl.com/Getting-started/Shaders)
- [https://beyondloom.com/decker/index.html](https://beyondloom.com/decker/index.html)
- [https://beyondloom.com/decker/lil.html](https://beyondloom.com/decker/lil.html)
- [https://en.wikipedia.org/wiki/MacPaint](https://en.wikipedia.org/wiki/MacPaint)
- [https://en.wikipedia.org/wiki/Interface_Builder](https://en.wikipedia.org/wiki/Interface_Builder)
- [https://en.wikipedia.org/wiki/Visual_Basic](https://en.wikipedia.org/wiki/Visual_Basic)
- [https://www.lua.org/](https://www.lua.org/)
- [https://aplwiki.com/wiki/Q](https://aplwiki.com/wiki/Q)
- [https://aplwiki.com/wiki/APL-sharp](https://aplwiki.com/wiki/APL-sharp)
- [https://rescript-lang.org/](https://rescript-lang.org/)
- [https://aplwiki.com/wiki/Niladic_function](https://aplwiki.com/wiki/Niladic_function)
- [https://en.wikipedia.org/wiki/HyperCard](https://en.wikipedia.org/wiki/HyperCard)
- [https://en.wikipedia.org/wiki/HyperTalk](https://en.wikipedia.org/wiki/HyperTalk)
- [https://www.javascript.com/](https://www.javascript.com/)
- [https://en.wikipedia.org/wiki/System_6](https://en.wikipedia.org/wiki/System_6)
- [https://en.wikipedia.org/wiki/Microsoft_Excel](https://en.wikipedia.org/wiki/Microsoft_Excel)
- [https://code.jsoftware.com/wiki/Studio/Viewmat](https://code.jsoftware.com/wiki/Studio/Viewmat)
- [https://en.wikipedia.org/wiki/Regular_expression](https://en.wikipedia.org/wiki/Regular_expression)
- [https://www.python.org/](https://www.python.org/)
- [https://www.haskell.org/](https://www.haskell.org/)
- [https://en.wikipedia.org/wiki/Myst](https://en.wikipedia.org/wiki/Myst)
- [https://itch.io/jam/decktember](https://itch.io/jam/decktember)

<details markdown="1">
<summary><strong>Transcript</strong> (click to expand)</summary>

Transcript

Transcript prepared by Bob Therriault, Adám Brudzewsky, Igor Kim and Sanjay Cherian

Show Notes

00:00:00 [John Earnest]

Right. APL is a language and languages are user interfaces, and these concise expressive languages that you could use at a REPL are a a significant user interface and and a big part of the power of these things, but if it, you know, if the only thing you ever give the these array languages to play with is like Posix standard I/O and M mapping, their possibilities are sort of boxed in just by the nature of what you give people immediately at hand. If you broaden the range of of things that are are available to play with, then the the outcomes get much more interesting.

00:00:42 [Music]

00:00:57 [Conor Hoekstra]

Welcome to another episode of Array cast. I'm your host Conor and today with us we have a guest that we're bringing back from a couple episodes ago, but before we introduce him again, we're going to go around and do brief introductions from our panelists. So, we'll start with Bob, go to Stephen, then to Adám and then to Marshall.

00:01:16 [Bob Therriault]

I'm Bob Therriault. I am J enthusiast and I'm working away on my wiki.

00:01:20 [Stephen Taylor]

I'm Stephen Taylor APL and q enthusiast. Yes, and I'm waiting to see Bob's wiki.

00:01:27 [Adám Brudzewsky]

I'm Adám Brudzewsky. I do APL teaching and coding and more. (pause) I'm looking forward to the wiki too I guess.

00:01:37 [Marshall Lochbaum]

I'm Marshall Lochbaum. I did Ji did APL and now I do BQN.

00:01:41 [CH]

And as mentioned before, my name is Conor. I'm a polyglot programmer and array language enthusiasts at large, and the host of this podcast, so I believe we only have one announcement today, so I'll throw it to Adám for that quickly, and then we'll hop into introducing and interviewing our guest.

00:01:58 [AB]

Again, right so I'm sure everybody is waiting and suspends to figure out what are we going to rename, if anything, the currently called APL Notation as a Tool of Thought podcast [01], which a bit of a mouthful, and so we had this poll and there firstly, there weren't very many people that participated. And secondly, Conor suggested calling it something else and that got some some likes there on Twitter. Yeah, I, I think everybody agrees that we shouldn't keep the current name, but it's not very clear what the name should be, and we can't really make a decision since Conors' got a lot of likes, so I think we'll just redo that and we'll link to that from the show notes.

00:02:38 [CH]

So, a new Twitter poll will be in the show notes and available. I think you made it for like 6 days or seven days last time. So it'll probably be something similar, so if you're listening to this in the first few days that this is out go to the show notes or just go to Adáms Twitter, find the poll and vote and that'll be the official name. I'm guessing this is the last one. We're not gonna have .... Actually I take that back folks, we don't know what's going to happen! OK, stay tuned this is poll #2 potentially the final poll and yeah, looking forward to knowing what the next name will be. Will it be what I suggested or will it be the other options? Alright with that out of the way. Today, the guest, Part 2 of interviewing him is John Earnest. We interviewed John on episode 42 two episodes ago, I believe this is episode 44. [02] (Editor's Note: This is episode 43 and John was first interviewed in episode 41) We said at the end of that episode we were gonna bring him back because we had only gotten through a fraction of what we wanted to talk about with him. A brief introduction because we already introduced him and I would totally stopped listening to this episode if you haven't listened to episode 42 (Ed: episode 41) because we're gonna be talking sort of extending a lot of the things we talked about in the first episode, so it'll make a lot more sense, and episode 42 was fantastic. We covered all the different versions of ok and a ton of stuff. But yes, John Earnest, former employee of 1010 data, which Michal Wallace was also one of those employees, and we interviewed him as well. You can find that link in the show notes. I think his claim to fame is and that what he's known most for, at least I think in the array language community is for implementing OK, which is a JavaScript implementation of k6 initially was k5, which we learned in interviewing him but is now sort of formally k6, but has done a ton of other projects. That is what we're going to sort of focus on today because we never got to that in the first interview. So, I think I might get these wrong off the top of my head is Decker, Lil, iKe, and I don't know if there's other projects that you want to cover. I'll just pause there, throw it to John and we can also I'm not sure if we had follow up questions that we wanted to ask, so I'll throw it to John first. You list us the projects, sort of the menu list of things that we can talk about today and maybe the things you would love to talk about and then we'll go from there.

00:04:49 [JE]

Sure, well it's great to be back. [03] I guess the the main things that come to mind is we could talk a little bit about iKe, [04] which is sort of carrying on from some of the stuff that we talked about with OK. iKe is basically a a front end that builds on top of the ok interpreter and gives you the ability to make little graphical interactive programs with it. I also wrote a transpiler for a subset of k2 GLSL, which is a GPU shader language that's called special k, which is sort of an interesting experiment. And lately I've been working on a sort of holistic programming environment called Decker that has a scripting language named Lil which is probably not properly an array language, although I know that that you guys have gone in quite a few circles debating what what exactly qualifies a language for being an array language and rule has some of those properties, so you know we can dive into that at its own time, I suppose.

00:06:06 [CH]

So where do we want to start, folks? First, do we have questions that we need to ask right off the bat or should we hop straight into iKe? What do what do the people say? What do the panelists say?

00:06:14 [ML]

I like iKe.

00:06:19 [CH]

Alright, let's start with iKe give us a sort of a, I don't know 30 second to five minute, however, long summary you want to give of iKe and I should mention right off the bat for the folks listening, if you happen to be in front of your computer, which or not because you're listening to a podcast, you can go directly. We'll have links and you can play around this. Play around with this in your browser without having to install anything, and it's super neat because you have a bunch of visualizations built in, including like the game of life, I believe if I recall correctly, and a ton of other like really neat things and you you see the code. I'm like I'm giving away you're supposed to be describing it, I'm gonna stop, but you go ahead.

00:06:54 [JE]

It's OK. So so when I wrote ok, [05] one of the design choices that I made with it is that I removed all of the built in I/O capabilities. normally k sort of comes with, you know standard in and standard out, the ability to memory map files that that kind of functionality baked into the language. So I made my interpreter just kind of this this pure unit and then I built a number of different front ends that let you use it in different contexts. So like there's the browser based REPL, there's a NodeJS command line REPL for it, and there's even a version that's sort of adapted to use on cell phones, so like or a touch device, it gives you sort of like a calculator style interface for entering k symbols, but iKe's the most elaborate one and it it basically gives you a little sandbox where you can write a k program. And the the end result of the the program that you write is either a value or a function definition with the special name called draw that will return a a structure of drawing operations describing something that you want to have shown on the screen. And there's also sort of an event input system where just you write functions that have a conventional name, and if the function exists and say you you know you press a key on the keyboard, then a particular function will get called and there's also sort of magic variables that automatically get bound with mouse coordinates and things like. So you write a function that yields a set of things to do to draw an image on the screen, and that's really it. You can from this basis leverage the full k language to make all sorts of things. You can make graphs, you can do cellular automata, you can draw fractals, you can do all sorts of things like that and part of the the purpose behind like was it's sort of like a like an object lesson in the idea that k is not a language that is only suitable to the domain of working with databases, because that's sort of its conventional niche and and sort of the way that that a lot of people think about array languages in general is that, well, they're they're good for. Big piles of tabular data, but a lot of the same you know bulk operations that are useful in that domain are also applicable to computer graphics, and a lot of other things like that, so it was really you just give the language some new I/O capabilities and then that is what opens up all these new domains rather than needing new language features per se. There's also a paper that I wrote about it that is in Vector, I think, a few people found out about it through that. [06]

00:10:15 [BT]

So, so how do you draw a fractal? Do you like? Is it a seed and then it's it follows the mouse pointer as you as you move around the screen.

00:10:24 [JE]

The most straightforward approach would be drawing fractals that are based on Lindenmayer systems [07] where you have sort of a, you know production rule that you iterate a certain number of steps and then you can just iterate the production rule as a, you know, applying a function multiple times to the same value and then convert that into coordinates for drawing a sequence of line segments. Or you could compute that and then over time, you know splay it out and then you get an animation pretty simply and cheaply.

00:11:02 [ML]

So the output here this is you'd be outputting SVG or something like that?

00:11:07 [JE]

Well, that would probably be the like the the general all inclusive way to do it. In iKe you you basically have two kinds of drawing primitives. There's a shape of a tuple that describes drawing a bitmap, including a bitmap and a a palette for it, and there's an operation that is draw a closed outlined Polygon, and with those two things you know, you can you can achieve a a whole variety of other things from that basis like you can generate an appropriate Polygon. Now you can draw ovals and rectangles. If you generate a very skinny Polygon and you can use it as a simple line drawing operation. So the the idea in iKe was to sort of give you this arbitrary creative limitation, which I guess is sort of a recurring theme in a lot of my work. But you know, you, you distill graphics programming into these very simple primitives, and then you can build back up a richness of expression.

00:12:17 [ML]

Yeah, and is that in the actual browser.

00:12:21 [JE]

Well, in the actual browser implementation I'm using a canvas and browsers have canvas elements and those have their own drawing API in the Canvas API is actually very similar to the Postscript drawing API in a lot of ways where you sort of imperatively set up paths.

00:12:25 [ML]

OK, yeah.

00:12:43 [JE]

And and render modes and things whereas its model built on top of that is a totally functional approach. It's possible to.

00:12:52 [ML]

Yeah, and you could of course render it anywhere.

00:12:55 [JE]

Sure, I mean part of part of the design there is, you know, I wanted to at least somewhat abstract the way that that browsers do things, because if you if you just kind of blend k with with JavaScript and write a program that like emits one of these complicated web standards that's simple in the implementation, as long as you're in a browser, but then you're you're welded to a browser forever and browsers are pretty complicated. So there's sort of a, you know, a power slash, cleanliness straight off and and that kind of a decision.

00:13:33 [CH]

What would you say, cause I've gone through I don't know if all of them and if you've seen on the zoom call here, my head's been turned cause I've just been mesmerized looking at this  Lindenmayer graphic, which it's impossible to describe, and I assume for folks that have seen it, they know what it is.

00:13:52 [JE]

Well, I mean it is possible to describe. It takes about a paragraph of k and I don't think anybody wants to hear us dictate that in words.

00:14:00 [CH]

I mean, do you want to do you want to attempt to describe it in English, nothing. It's just basically drawing a bunch of what looks like Pascals or variant of Pascals triangles. I assume they're  Lindenmayer triangles.

00:14:13 [JE]

It's a Sierpinski triangle, described using a lindenmayer system.

00:14:18 [CH]

Yeah, and it draws it sort of sequentially, but it has this like it uses turtle graphics. It looks like from the comments in the code and it has a sort of line that's drawing it and then it flips the colors of certain triangles. Anyways, very mesmerizing.

00:14:34 [JE]

It it's pretty data-driven too. There's a section in there where you can see that the rules themselves are just defined as like a little a little list of symbol. So you can see how the symbolic substitution part happens, so you could change those rules and you can get a completely different shape.

00:14:51 [CH]

Yeah I would imagine that like this kind of doing this kind of thing with like Turtle Graphics in Python, I have no idea how long it would take, but I would be very surprised if it's as concise as the k code because it fits on literally half of half of my monitor. So my question was off the top of your head, do you have like favorites of the example programs that come with iKe.

00:15:18 [CH]

Yeah, that you would point people at to be the most mesmerized or the most impressed. Like I know there's the snake game, there's the game of life.

00:15:25 [JE]

The snake game is sort of a fun hack. It's an implementation of the classic, you know, Snake game where you have a a series of of segments that move around the screen and you have to direct them to eat apples or something like that, and if it crashes into itself, then it deresses. But that is a an implementation of snake in k [08] that doesn't have any conditional statements just to kinda demonstrate that you know we we have different tools to bring to bear in in these languages, it does use some global variables, but you know I could have done without that.

00:16:07 [CH]

So sneaky. My favorite that I think I've seen is this lindenmayer one just cause yeah, and and that one you.

00:16:13 [JE]

It's a good illustration of just it. It uses k as a nice functional language. There isn't a huge mass of data being manipulated there, but it's still, you know really expressive I think. And I make some gainful use of function projection in there to to implement the Turtle graphics system, because as I said it doesn't. It has a very primitive simplistic notion of of graphics drawing that is not stateful. And if you want to make something that behaves like turtle graphics, [09] you need to build a little abstraction on top of it, and that's just a few lines of code in k. I guess sort of intended as a as a live coding language. This is something that you can view building up and manipulating the program as something that you could do as a performance, and the conciseness of array languages make them extremely well suited to that that sort of works because you you don't have to have a bunch of boilerplate or use snippets or anything like that in order to have small changes have an impactful change in what you see.

00:17:27 [CH]

Yeah, there's tons of examples, like, uh, probably the most famous is this. Is it called the swift playground. [10] I actually don't know, but it's only it only works on Macs and you have to have X code or whatever, so it's kind of a bummer, but it was an amazing presentation when they first demoed it at WWDC, and there's been tons of these, like Bret Victor has a bunch of these sort of live coding things and that dates all the way back to small talk and they're super like engaging ways to show how you can iteratively build up some cool little you know thing.

00:17:57 [JE]

There's a tool called Processing which is sort of a programming environment that at least originally was kind of based around Java with some syntactic sugar laid on it to make it a little bit less verbose with a built in graphics API and ability to to interact with you know GPIO stuff and play sounds. It was kind of originally conceived as a a thing for making art installations. This is, but it's also excellent as just a teaching tool, and because you can just dive in and it's fast, especially compared to like doing graphics with π game and Python processing is just unbelievably faster, so you could do things in a very simplistic way and still get good results from it and Processing is available in a entirely web-based version, sort of like this. I guess. Another maybe notable thing about Processing is that the little IDE that it uses was the basis of the Arduino IDE, so you know that's a very popular hobbyist electronics platform.

00:19:16 [ML]

Another notable thing about it is that my BQN co-author Dzaima has actually. He's a big fan of Processing and has integrated it into both his Java based implementations, Dzaima APL and Dzaima BQN, [11] which is not the same as the sort of mainline implementation CBQN, but yyou can use Processing from both of those.

00:19:38 [JE]

Right and and you know when I was when I was making it, I was really thinking of it as it's Processing for k and you can just write a little program you can immediately start seeing visual results and you know and and and play with stuff and it. You know that they're they're interesting things that you can do with the normal key interpreter, but I feel like giving beginners some more interesting IO really opens up the the range of things that could you could do with the languages that catch people's interest. And you know, and again you make you you have. A visual program that's making an animation or something you can just reach in and change some numbers or or reorder some things and you immediately say see a change. You can explore the possibilities of of program space without really having to fully understand all the moving parts at least not at first.

00:20:30 [ML]

So I am wondering. You said like you could do the snake thing without global variables. How do you keep track of state when you're using pure functions? Do you like pass it from one call to the next?

00:20:43 [JE]

There's sort of a magic feature where there's a way that you can up front once, declare an initial state, and you define sort of a tick function that will take a previous state and yield the next state that also gets fed into your draw function. So like if you want to be all neat and tidy, there's kind of a a pipeline for for tracking state through your program. Or you can just, you know, be messy and make global variables it's just as good.

00:21:13 [ML]

Yeah, well, I mean, global variables are just sort of elements in this one big well, especially in k. They're in one big dictionary that you're modifying, so it's not all that different.

00:21:26 [JE]

Sure, I mean when you're programming in small global variables are are are not an evil thing. It's something you need to kind of like you need to kind of unlearn when you're doing k programming, in particular because you know k has a very limited concept of of closure. And so a lot of people really tie themselves in knots trying to to make the neat, tidy implementation of the thing that you know uses no global variables and everything is a pure function, whereas if you just let yourself use a few globals here and there, you can still be careful about it and and thoughtful about it. But if you are less dogmatic about it than your code gets simpler, much shorter, much easier to understand.

00:22:16 [ML]

Yeah, well, I mean even as a fan of closures and working with BQN that does closures, a lot of people try to write like stuff using scans and all sorts of things when really the just keeping, not necessarily a global but a local mutable variable can be a lot clearer.

00:22:34 [JE]

Right? I totally agree.

00:22:36 [CH]

This to skip back to this processing thing. I was confused at first because I was like what process what is process, what is this thing we're using a gerund like the noun version of a verb to name a product here. So at first I was confused and I was like, OK, I must I must be misunderstanding that this is the name of a product because there's no way, and especially if you're going to choose a gerund, don't choose process, one of the world's most generic vague verbs that also is like overloaded how many times in computer science, sure. Enough though, I Google. Processing Java and go to Processing.org and it's an IDE graphical library experience and anyways, this looks amazing, but also I just think we got to pause here for a second and like what are the folks what's going on? I know naming is hard, but Processing?

00:23:32 [BT]

From from the people who brought you J.

00:23:35 [AB]

And k and q and APL a programming language should need a name.

00:23:39 [CH]

That's a good point.

00:23:42 [JE]

At least in the case of in the case of q, you know q is a query, it's a question.

00:23:48 [CH]

Is that what q stands for?

00:23:49 [JE]

Or a quartermaster I guess.

00:23:51 [AB]

Well, yeah, that's what I thought.

00:23:52 [JE]

Depends on who you ask.

00:23:53 [AB]

It makes the same sound as k, but it's for querying.

00:23:56 [CH]

I said on one podcast I think the other one that I didn't know what k stands for, but I actually did. It was keys to the Kingdom.

00:24:02 [ML]

Well, he just made that up one day.

00:24:03 [CH]

He just made that up one day?

00:24:07 [ML]

Yeah, I mean somebody asked him and he was like I'm so tired of this question. I'll just of course he didn't tell anyone that, but that's what happened.

00:24:14 [JE]

There are a bunch of different stories that I've heard, and another one is that that the the symbol k resembles the 1st letter in the Phoenician alphabet and this is sort of this sort of fits, because apparently because E of course is the the 10:10 data successor to to k in a sense. And apparently E sort of resembles the 2nd letter in that alphabet, so.

00:24:38 [AB]

That's that's true... but a capital A certainly looks more like the first letter than the k does.

00:24:46 [ML]

Well, he'd already used A.

00:24:48 [AB]

Yeah, exactly so I would have thought that it would just got one over from J.

00:24:56 [JE]

There's the first available single letter file name in the directory that he happened to be in when he started.

00:25:02 [BT]

And at this point I should jump in and do the usual. We are talking about He is Arthur Whitney. [12]

00:25:07 [CH]

Oh yeah, Arthur Whitney.

00:25:10 [BT]

He's gone to the point we're not even saying Arthur, we're just saying he.

00:25:15 [AB]

Don't you dare mention his name explicitly like that.

00:25:18 [CH]

This has nothing to do with with John, but while we're on the topic, so we know APL. They had trouble in like 1966 and then I can't remember who was it that walked in the room and just said, let's just use the name of the book, you know, the acronym APL and they all said OK, I think it was Eugene McDonald. It's in the forward to a book.

00:25:39 [ML]

Yeah, maybe he just wrote about it, maybe it was Falkoff.

00:25:41 [CH]

Yeah, yeah might have been Aidan Falkoff. I think that's what I recall it being anyways.

00:25:44 [ML]

There's an APL wiki article about it. [13]

00:25:49 [JE]

I think it's too bad they didn't go with Iverson's Better Math. But the the executive that is, his employer were not too happy with that.

00:25:57 [AB]

No, they wouldn't have it.

00:25:58 [CH]

For those that don't know they were working at IBM at the time. So it wouldn't have worked out well.

00:26:02 [AB]

It would be weird to have IBM's product called IBM right.

00:26:06 [CH]

Probably probably some trademark issues there.

00:26:07 [JE]

For all these years you've been waiting. And finally, our flagship product arrives...

00:26:12 [AB]

But didn't Iverson protest and say that God's world is just the world. You shouldn't call it Iverson notation, it's just the annotation.

00:26:23 [CH]

Anyways, we got to cycle through and get back to talking about John.  BQN was supposed to be APL plus one, but now it's Fibonacci plus one. I think we talked about that in the past episode. You can go watch, listen to every single episode to find that conversation. J was because it was the key underneath the right finger on the keyboard is what I heard. Yep, when when you touch typing, yeah? So if you look at your, if you have once again if you happen to be in front of a computer and a keyboard. If you look you know there's two little dots usually on most keyboards, one's an F, one's a J.

00:26:54 [ML]

Qwerty layout of course.

00:26:55 [CH]

Qwerty, of course. And k reverse engineered or you know couple different stories is k after J. Is it keys to the Kingdom? q? I actually don't know q, but I guess is maybe query Stephen, do you have any?

00:27:10 [ST]

Query and before we can totally leave, k, consider the possibility it's named after Ken Iverson.

00:27:21 [AB]

It's actually nice.

00:27:23 [CH]

Why wouldn't Arthur just come out and say that, though?

00:27:25 [ML]

I think there are probably multiple reasons he chose k.

00:27:28 [CH]

Yeah, that's true. AmI missing any other array languages that we should cover the back story of the single letter or three.

00:27:38 [AB]

A - it was an abbreviated APL by shaving away stuff.

00:27:44 [ML]

Right and then they added a plus.

00:27:46 [AB]

Yeah, plus for the extensions. (laughs) Then on top of that, do you know why it's called Dyalog?

00:27:53 [CH]

It's a combination of the two companies that merge no?

00:27:56 [ML]

Not quite.

00:27:57 [AB]

They didn't merge, but yeah, a lot of people think it's because, like you speak with an interactive programming, you speak with the computer, not at all. For some reason, which I have no clue. Actually, I don't know if anybody knows the that old company that the people founded was called Dyadic systems. As in, like their dyadic functions, and then they decided to make an APL for the Zilog processor. So dyadic Zilog is Dyalog. [14]

00:28:23 [ML]

And the company wasn't called that the company stayed Dyadic for a long time and eventually renamed themselves the Dyalog because that was what everyone knew them for.

00:28:31 [AB]

Hmm yeah they took the name of the product.

00:28:35 [JE]

It's the rim BlackBerry situation.

00:28:37 [CH]

Ohh yeah yeah yeah Canadian company for the win woo! except they lost their... But there's a whole book about that called.

00:28:48 [AB]

I don't know. So the next language after that should be L.

00:28:51 [BT]

Lil.

00:28:55 [CH]

What a great transition to Lil, alright.

00:29:00 [AB]

Well, Marshall, why did you call I?

00:29:03 [ML]

Well, I wouldn't describe it as a cross between J and k, but it's certainly in that space.

00:29:09 [AB]

It's above them on the on the QWERTY keyboard. If you look where J and k are and then you go up.

00:29:14 [BT]

Because it was imaginary?

00:29:16 [ML]

No, I was thinking about the normal the unit vectors or quaternions, or there there's a trio with an IJK. And I thought, well, that one's missing. And I also thought this is not gonna be a very good language, so I'll take this terrible name so other people don't have to use it. But the other people still want to use that name for their own language, so I mean, there's already another I Lang, so that didn't work at all.

00:29:37 [AB]

Hey, do you know that on the QWERTY keyboard the average position of A, P and L is J?

00:29:45 [ML]

It doesn't look quite right. It looks closer to H to me, but maybe not.

00:29:51 [AB]

No, it is because think about it. If we do the math. Even if whether you round off to to integers first, or you do the actual quarter with position from typewriter terminals. It comes out to J either way.

00:30:08 [CH]

All right we'll it to our listeners to determine what the true average is, and with that we will conclude our our tangent on the history of the names of array language. Is is there anything else we want to talk about with iKe other than to tell folks definitely go check it out? It looks awesome. Before we move on to either special k or Decker. All right, I'll take all the vociferous nodding of head's. Let's move on to the next thing. John, what do you want to talk about next? Do you want to talk about special k [15] or do you wanna hop to Decker?

00:30:38 [JE]

Well, let's just talk about "special-k" very briefly,[15] because it's a pretty simple hack. So for for those who have never worked with GPU's before or written shader programs before. A fragment shader is the final stage in a  modern graphics rendering pipeline. The responsibility of a fragment shader is to come up with the color that a single pixel should be rendered on the display. And so you can write a program in this one of several closely related Shader languages to describe a function that gets applied to every pixel that that is asked to be rendered. So there's a whole zoo of interesting things that you can do by basically writing a program that draws one big triangle that fills the whole screen, and then you post process it with fragment shaders in order to make it look like absolutely anything. You can render fractals. You can even do 3D rendering. Using like sine distance functions and and ray marching techniques, it becomes this whole thing. You kind of just intentionally discard most of what the GPU is built to. Do and focus on the fun part and you get this again from a simple rendering primitive. You get this this flexible base. And part of my my beef with with GLSL is that it's C derived. Despite the fact that you're constantly working with vectors and  applying this in a collective, you know, context and so it's it's really unnecessarily bulky and ugly. So I just as an experiment, tried it writing in k notation. Basically the the semantics that you you want for writing shader programs and I made this thing called special-k. It's pretty concise. There are things that you can't really bring over from the k side to shader programs. Because like for example you you can't really write unbounded loops in a shader program. One of my old friends at one point was telling me about a revelation they'd had writing compute shaders for the compute pipelines and they were sort of a new thing and he said "NVIDIA [16] has solved the halting problem. If your shader runs too long it stops." That's kind of the the ethos that you're doing. You're... You don't have the full power of a general purpose programming language, but it turns out that you have enough power that you can write some very, very interesting things entirely in shaders. And it's not exactly true that shader programs are not Turning complete. Because in fact people have managed to use, you know, texture buffers is a way of storing arbitrary state. You can emulate a whole CPU in a shader if you want to. It's just not necessarily a good idea, but it is, you know, an effective idea when you're in an environment where the only mechanism that you have for injecting your own conde is supplying a shader. So, so anyway, Long story short. special-k is an Ike like programming playground where you can write in this restricted subset of k and it shows you the longer, uglier and nastier explicitly typed GLSL that it generates. And it comes with a couple of fun example programs. With that you can... A few of those demonstrate sine distance fields, for example, which is a very fun and flexible rendering technique.

00:34:46 [CH]

So is there a similar like Web preview thing that you can do that shows three different panes? The special-k code, the generated GLSL?

00:34:56 [JE]

Yeah, if if you. Go to beyondbloom.com and under the "The Things" section there's a link to to special-k. And if you if you go to the the same URL that it takes to you but replace the dot HTML with dot JS, you can see the complete compiler, which is pretty compact.

00:35:19 [CH]

And it's telling me that your website is unsafe.

00:35:21 [ML]

You thought so.

00:35:24 [JE]

Well, that goes without saying.

00:35:28 [CH]

I'm logged into my VPN right now. And it says that your domain is blocked. Man I'm going to get a message from NVIDIA HR saying why are you going to... I won't say.

00:35:42 [JE]

Yeah, you're in anybody who visits. My website should be should be aware that visiting it has significant potential to expose them to dangerous thoughts.

00:35:55 [CH]

It provides a reason that I'll tell you off-air. You'll be very confused. You'll be very confused or maybe not, I'm not sure.

00:36:04 [JE]

It's because of the spiders. Isn't it? Yeah, go ahead.

00:36:09 [CH]

We all burst out laughing. Alright, well when I'm logged off VPN I will take a look and we as always, will leave a link in the description. I haven't checked that one, but it definitely sounds cool and. Yeah, I mean there's a bunch of spaces where I've had that exact same thought where you're looking at a program that is its primitives are like arrays and array operations. But it's written in this like ALGOL or C derived language and you're just going like. What like you don't need to use APL, but like there's a language out there that is a much better fit for this problem. But you know, it's not always choose the best language because you sometimes you're stuck with whatever environment you're in. But yeah, super cool that you built that tool and I will definitely take a check. Take a look later. All right, let's move on to Decker.

00:36:59 [JE]

So Decker [17] is what I've been working on for quite a while now. I think at least a year in total. So Decker is kind of... It's the everything machine. It on a very superficial level Decker is this environment that looks sort of like a presentation tool like PowerPoint or something. You have cards that are,  comprise a deck and you can flip between the cards. You can draw on the cards using a bunch of tools that gives it kind of a Mac Paint or MS Paint style feeling and you can also put widgets on cards. Widgets are these interactive elements. There are five different flavors of them, but the most important one is the  button. You can put buttons on cards. When you click on the buttons things happen. In the simplest case, clicking on a button just brings you to another cart. So it's kind of this hypertext like system that's very free flowing and free form. You could you immediately start to to think about how like, well, you know I could organize my notes for things in sort of a nonlinear way. Or I could explain a topic, make something sort of like a website where I can navigate around in this. But beyond just having navigation as a result of interacting with these widgets. You have a full scripting language that can control, you know, you can make new widgets. You can change the properties of widgets. You can draw stuff on the screen. You can play sounds. You have a full flexibility to kind of manipulate this environment and and build things in it. So it becomes sort of, again on on like a superficial level, it kind of feels like interface builder [18] or like Visual Basic or something. You can just drag things out, make a little application. And the reason that this has some applicability to this podcast, as I mentioned earlier, is that the scripting language that you have for controlling this thing and building stuff which is called Lil. Is a very ... It's sort of designed to resemble Lua, which is a popular mainstream imperative programming language. Because that way it's sort of unassuming, and it's not too scary for people. You don't get this immediate knee-jerk revulsion from people. But it's actually much closer to q in terms of its semantics and the primitives that it gives you. It can, on a superficial level, seem like, oh it's just a very simple imperative language. But really, it's a functional programming language. Everything is an expression. All of the built in types are or value types. You do immutable operations on lists and dictionaries. It has tail call optimization or elimination I should say. It has lexical scope and closure, but then you know you dig a little bit deeper. It has a a query language built into its syntax that's in many ways similar to to qSQL a little bit more limited, a little bit more simple. And so you have this kind of database programming capability built into it, and that's also reflected in the environment. One of the widgets that you can create is called a grid widget that just represents a a reification of a table of data you can display on the screen. And low is also a vector oriented language in the sense that it has uniform operator precedence. It has automatic spreading of the the arithmetic primitives to  lists and dicts. It has a small set of operators that are generalized appropriately to a full set of data types and the sort of dynamic system it has many of the same primitives as q or k. So it's kind of, you know, it's like a wading pool into a lot of these ideas. You can ease yourself in to thinking about operating on data in a holistic way in this language that has very low barriers to entry. And as in iKe having these nice vector semantics and some of these primitives works really well for doing graphics programming there. It also works very well and the Decker environment. Sorry there's a question.

00:42:09 [ML]

Yeah, so one of the things I wanna pull out of this that's really important that I don't think we touched on enough when we were talking about like array languages. Is that the arrays are immutable, so that's something that you don't get in Python or JavaScript or even Julia or Numpy.. Is that when you have an array, it's just the data. So while I said that I think mutating variables can be good, I really don't like mutating arrays cuz in a lot of cases you wanna have copies of this array around and you want them to say the same. You wanna say I mean this array is [1 2 3] and that's what it is. You can't change the two to a four because that's a different array.

00:42:50 [JE]

Yeah, and and you have semantics that make it look like you can amend a thing in place. But really what you're doing is constructing a new thing and if anything, you know, new about the the old structure if that was stored in another variable, you still... It it's not chained.

00:43:05 [ML]

Yeah, which is also a feature of a of pretty much all. Yeah, I think every array language has something like that... J.

00:43:14 [JE]

Usually the term for this is "copy on write semantics".

00:43:17 [ML]

Well yeah, but the having a syntax that says: "Well, I want to change this, but the meaning is yeah." Is that you're not changing it. So I think J is probably the furthest from having a dedicated syntax for it or like a specific thing, but even it has an adverb called amend where you say you know what you want to put in and the places where you want to put it. So that's kind of a way to work around. Well to to have that ability to change part of an array even though you don't want that to be like changing the array, you just want a different array.

00:43:53 [AB]

So Dyalog had an experiment going many years ago when it looked like Microsoft Silverlight was going to be the future, and that Microsoft was running in the world and everything was going to be .Net. There's something called APL# [19] and there they. Don't blame me. I didn't wasn't there to make any decisions, but they made the decision that in best .Net language style values should or yeah, I guess should be mutable and you would have to clone arrays in order to not have subsequent changes affect each other, which I at least find very strange and foreign. Maybe this is another characteristic of these array languages or Iversonian languages that pass by value. Is Everything is just a value.

00:44:48 [JE]

I mean, it's also a characteristic of many functional programming languages. I mean, that's that's part of the the big reason that Lil has value types is that it's also trying to be a nice functional language. Where if you're going to have mutation, it's pretty explicit. That's the it's becomes.

00:45:09 [ML]

Maybe. I've seen some functional languages like. I know ReScript [20] goes the other way where you can't mutate variables, but you can have a mutable reference type. So if you want a mutable variable, what you do is assign an immutable variable to a reference to some value, and then you can change the reference.  So that's the direct opposite of array languages, where in an array language you can mutate variables, but you but all your data, I mean, you might have mutable objects, but the main data is just immutable stuff.

00:45:44 [AB]

But didn't k have or has k something called the view which is different type of assignment that is connected to where the data came from. Grammar completely out in the weeds here.

00:45:58 [ML]

You can't think of what you would mean.

00:46:00 [AB]

No, I think there was a... There was, at least for a while cause k changes over time where it has a special type of assignment, like with double colon or something where.

00:46:08 [JE]

Right, this is a construct, that's it sometimes it's referred to as like a spreadsheet like definition. Which is basically just it's syntactic sugar for a memoized Lambda that understands the globals that it depends on. And we'll recompute its value if and only if you know something that is referred to is changed when you when you fetch its own value. And "ok", actually has support for these. It's existed in a number of dialects. It's something that I was, I initially found very intriguing. And in practice, I found it was less useful than I hoped it was going to be.

00:46:50 [AB]

It's similar to how traditional APLs, as opposed to modern hobbyists. Whatever new APLs have these traditional functions. And they have a header that declares their syntax when you use them, and you can then declare a function that has no argument. So it's an niladic function. [21] If you can call that a function. Or program if you want. And you can then refer to variables or refer to various names. It can do everything a normal function can do, just doesn't take an argument, but so it behaves syntactically like an array. But it's whenever you call it, it recomputes. And based on this.

00:47:31 [JE]

It recomputes, if necessary, the whole point is that it's memoir.

00:47:35 [AB]

OK, so it's an it's a memoized. OK yeah, that's the difference between them.

00:47:39 [JE]

Yeah, so the degree to which it's helpful basically comes down to how often is this going to to hit cash and save computation versus, you know. Otherwise It's just kind of syntactic sugar.

00:47:57 [AB]

So I could implement this by memorizing manually in the APL.

00:48:01 [JE]

Right, it would just be, you know, a little bit clumsier and and more verbose.

00:48:06 [BT]

One of the things about lil is it strikes me and we haven't mentioned Hypercard, [22] but to me that there's just an obvious correspondence to look at everything as Hypercard.

00:48:19 [JE]

Absolutely. Decker is not Hypercard clone, it doesn't. You're not ever going to run Hypercard stacks in this. It does a lot of things very differently, but in in broad strokes it is very similar to Hypercard. Which was sort of it's the everything program for for early Macs. It's really important to understand that so many of the ideas in Hypercard significantly predate web browsers. And almost everything that early web browsers did was a clumsier or limited version of Hypercard, except it's delivered over a network. That's kind of the the one difference. But you were saying.

00:49:02 [BT]

Well, I was going to say HyperCard had HyperTalk, and one of the things about HyperTalk was it was sort of a method of, I guess using a human language. There were extended words. Similar to some of the things that q has done with the way they've introduced words to describe what you're doing. But lil has something else to me, it you've also made choices that seem to me to make it easier and more natural to use. Is that one of the motivations you have when you were creating it.

00:49:31 [JE]

Well sure it lil is more of a conventional programming language than HyperTalk in a lot of ways. So HyperTalk has a very verbose nature. Part of the the motivation behind the design of HyperTalk was, that was trying to make HyperCard as accessible to novices as possible, and so the a well written HyperTalk script reads like English prose, describing a sequence of things that need to happen. You know you literally write code that's like, put the value of card field 1 into a put a * b into c. So it has.

00:50:22 [BT]

And and you had variables that might be called this.

00:50:24 [JE]

Right this and it have sort of a a special meaning for carrying value between between expressions and and so it is certainly true that the nicely written hypertalk is extremely readable. But the downside to this design is that it has, it is a language with an enormously complex grammar. There are many ways to express any given idea. Everything is very verbose and it is not actually that easy to write hypertalk, let alone write hypertalk that looks really nice and is easy to comprehend. My experience is as like a 9 year old playing with this stuff was it was enormously frustrating. It might have. Been better if I'd had someone looking over my shoulder and pointing out no you you can do it this way, and here's the better way to approach that. But I think that HyperTalk was a success at making understandable programs to novices, but not really a success in in allowing novices to to compose complex and interesting programs. It also has other shortcomings, like the fact that it doesn't really have any notions of data structures beyond, like, manipulating comma separated lists of strings. I mean, really just manipulating strings. And there's some there's some deep intelligence to that, and there's a lot of primitives for flexibly manipulating text to kind of get around that, but... At the end of the day. I think that you know not having proper dictionaries, let alone table types and and lists, is enormously enormously limiting, and so lil is a totally different approach. There are a few things that are superficially similar, because I thought that they were the right decisions. But it is more like a normal programming language, but written from with with sympathy to beginners and from the perspective that it should be something that you can learn in layers. You you don't have to have a full understanding of a complicated language to do useful things in lil, and you can gradually learn about its features and primitives over time and expand, you know, the range of things that you can express with it. That you can, you could do things in a verbose imperative way. That's just, you know, using using while loops and and variables to do everything, and that's fine. Because the the idea of Decker is not really that it's supposed to be a like a classroom with a stern teacher who wraps your fingers if you do things wrong. It's an environment where you can just play. There are no wrong answers, as long as you're you're tinkering and and making something and expressing yourself creatively. And in fact, there's a lot of stuff you can do with Decker that doesn't involve writing any code at all. And I hope that some of the people that that play with it will be people who do not think of themselves as programmers. And maybe overtime we'll learn a little bit of programming, but they don't have to go off the deep end to to find use and and enjoyment in the tool.

00:53:44 [BT]

That's actually where Decker becomes almost a teaching environment. It encourages you at a very light level. You can as simple as you know, clicking on buttons to say whether you want an animation to happen or something like that, which it's just clicking on a button. You're just making a selection. But as you get deeper into that, as you say, it's layered as you get deeper into that, it encourages to start playing to create animations. And that's another level and you have to learn a little more to do that. But when you do learn a little more, as soon as you make those changes, you can see them happen on the screen. So there really is an interactive play environment to it.

00:54:20 [JE]

And and there are some people that you know will look at this and say well. Why didn't you go with a conventional existing programming languages. The scripting language for this thing, and you know I could have added Lua or JavaScript [23] or something else popular and I would have some advantages in terms of allowing people that are already steeped in these things to just jump in and start making. But the flip side to it is that by having a custom scripting language for this thing I can tailor every aspect of the language to suit the environment and and make it so that the the things that you can do in the environment, the things you want to do in the environment have a nice expression. In the language, so like, if you want to treat Decker as a personal database system. lil has first class tables as a type. Decker has a first class reification of those and the grid widget. It has a query language. It has primitives for reading and formatting columnar data. It understands text interchange formats like CSV and XML and JSON. And so you have all of the things that you need to solve this domain of problems immediately at hand. And sort of, I guess, philosophically, one of the main things that I hope that I've carried forward in the design of Lil from Vector languages. Is the idea of solving problems directly in the language. You don't need to build up a bunch of abstractions on top of lil in order to start to start doing things. You can. It's a functional language. You have all the normal facilities for making utility routines and things, but you know you have take and drop and the ability to filter data, built based and baked into the language, you've got parse and format baked into the language. You don't need to import those things or build them up. They're just immediately at hand.

00:56:27 [BT]

In in my days of, you know, playing around with cards, cards and things like that. And often cars were referred to as sleepers. Somebody would take an old VW bug and put a Porsche engine in it and I think Decker is a bit of a sleeper.

00:56:42 [JE]

As they're mechanically compatible, right.

00:56:46 [BT]

Well, yeah they were in the case of portion and VW could drop it right in, but the resulting performance is quite different. And that's one of the things with I see with Decker is. It's just I would love to see somebody show up at a conference with that interface. And then start showing things with it because it can do things that you don't expect. That kind of a a program which looks like it's right out of what the early 90s or late 80s.

00:57:14 [JE]

Yeah, I guess another facet of Decker that nobody's explicitly mentioned in this discussion so far is that Decker uses a custom UI toolkit that is designed (especially if you go into full screen with it), [to] look like Mac OS 6 [24]. And part of the reason for that is sort of pragmatic: I want this application and the things that you build in it to look absolutely consistent on every platform that they run on. Whether you're running it on a Mac or Windows based computer, or if you're using the web-based port of the thing. It's a desktop application that you can export a (single file) HTML version of your deck [from] that includes all of the editing tools and the whole runtime and environment. It doesn't lose anything in the translation And so, in all of these different contexts, I wanted things to look exactly the same. So I built my own windowing toolkit and it needed to be small, in order to make this something that I could do at human scale and port to the web easily. So I wanted something crisp and simple and clear. And the first thing that comes to mind for me is Classic Mac OS, which you know looks very different from computers today in a lot of ways, but I think that many of the things that were good about it then, are still good even if it looks kind of retro. So it's consistent and the other thing about it is that it's the simplicity of the appearance of the widgets and the overall user interface and its visual coherence goes along with the drawing tools. All of the built in widgets are something that a person could very easily draw by hand using the drawing tools that are available. So you get this this symmetry. You don't have, a beautiful, elegant, modern, subtly gradated button on top of an MS paint squiggle. It would look weird; it would look out of place. But the the UI toolkit and Decker and the facilities that the user have match, and things look like they fit together. I think that is really empowering and encouraging to users in kind of an important way. It makes the user's creations feel like they're first class in this environment.

00:59:45 [BT]

Well, and as you say, it's very encouraging to a user who might be new to the environment because what they're going to create looks like it fits the environment already, so you're not only working with something that looks simple, but as you create, it fits into it. And again, I think it beckons you to take it another step, which is what I really find impressive about it. There's so many places between Decker and Lil that it's taking a user and encouraging them to take that next step over and over again. That's really quite cool.

01:00:14 [JE]

It's encouraging them to play. You know, you can take any deck that anybody has made (and Decker's default mode is the interact tool where you can click on buttons and select text fields and and enter text and, you know, just operate an application). [And] at any time, you can switch to widget mode or drawing mode and just lift the hood and start changing things around. Everything is inherently plastic and user customizable. Hypercard was a revolutionary piece of software because it blurred or even erased the lines between programmers and users. And I think that kind of empowerment is something that's enormously valuable in computing and something that we should see more of in the software that people make. If you ask people: "what is the most popular programming language in the world?", you'll get the redditors or whatever go: "C++". [JE says] Wrong!

01:01:24 [JE]

You dig a little bit deeper and maybe you'll have people say: "well, JavaScript, because JavaScript runs absolutely everywhere". There's literally billions of phones that have a browser in it that can run JavaScript code. And of course it will be that people point out that Java Card runs on even more things, because every SIM card and every every credit card you own is capable of running Java Card. But the [with emphasis] real answer is Excel because the number of people that are composing software using Excel [25] just [with more emphasis] blows out of the water everything that we would think of as being like serious real programming. And Excel has a lot of strengths are also its weaknesses. You know it sort of gives and takes in equal quantities. And of course it's proprietary software that is not really customizable or understandable in a lot of ways. But what is unambiguously true is that it's user empowered. And also you know it lets you do things in a vector oriented way. Maybe that's no surprise.

01:02:33 [BT]

Well, and that actually brings it around to the real languages. Again, I think, because we've had a lot of people come on and talk about the fact that a person who wants to work with a language like APL or any of the array languages doesn't necessarily have to be an expert programmer but quite often it's a subject matter expert that brings their expertise to that. And that allows them to work with that language.

01:02:53 [JE]

Right, APL is a language, and languages are user interfaces. And these concise, expressive languages that you could use at a REPL are a significant user interface and a big part of the power of these things. But if the only thing you ever give these array languages to play with is, [the] POSIX standard I/O and and memory-mapping their possibilities are sort of boxed in just by the nature of what you give people immediately at hand. If you broaden the range of things that are available to play, then the outcomes get much more interesting. I mean of course, J ships with bindings for a bunch of great facilities. It comes with everything that you need to make graphical programs, manipulate windows, load media types. It's not necessarily all beginner friendly or immediately close at hand, but at least it has a pretty rich standard library.

01:04:02 [ML]

But one of the really great things it has is just a function ... (I think it's in a package) ... but it's a Viewmat function [26] [JE agrees] that all you do is pass an array and it shows the array on the screen as a bitmap looking thing. I mean, there's a default color selection and so that itself is just a big step towards being able ... [sentence left incomplete]. Like you can very easily make a picture and see: "what is the picture I just put together?"

01:04:29 [JE]

Exactly and like Dyalog, has you know a whole bunch of ... (unfortunately, a lot of them seem to be kind of windows oriented) but like you know, you have full access to all this .NET stuff, this big toy box you can play with, but part of the problem there is that you have these things, but they aren't necessarily all exposing APIs that are nicely designed with the array languages in mind. You can do things but not as cleanly or beautifully or conveniently as you would like to. And the process of, sort of, designing nice APIs for doing these things in a way that mates well with the vector oriented languages is a big design problem. It's something that should be, you know, respected as an important challenge to take on as opposed to saying like: "well, you know, we just don't do that kind of thing". [ML chuckles] There's, you know, kind of a popular perception (among the people who don't just immediately reject array languages on an aesthetic basis) that: "well, these are neat powerful languages that are domain specific languages and so just like a regular expression, [27] we just want to tuck it away in a little closet where nobody has to look at it. And maybe when I have to do something with an array, I'll reach for this language".

01:05:54 [ML]

This was the thing that I said we needed to ask you about when Michael was on: your opinions on embedding languages. [28] So just continue what you're talking about because you're answering it already.

01:06:07 [JE]

Sure, sure. Right, so there's always this temptation of: "well, we have these languages like Q, J and k that are very small and that don't have an established software ecosystem; so what if we could come up with a way to sort of, team up with an existing software ecosystem like Common Lisp or like Python?" Python [29] has tons and tons of packages, and you could argue that the success of Python is in many cases, in spite of the language itself. But because of its wonderful expansive ecosystem of nice things that are close at hand to solve problems, there's this temptation. It's like: "Well, what if we make it so that we could just interoperate with this big language that's popular? And then maybe people who are using that big language will see how wonderful we are and then they'll start using us more and more". But it doesn't really flow that way, because if you make it so that you can tuck Q code into a little nodule that gets sealed away in a Python package, anything that q is good at gets just sort of hidden and abstracted. Maybe somebody writes a pythonic interface on top of it, and then it's gone and out of sight and out of mind. And from the flip side, if you want to use these wonderful things that Python can do from the Q side, nothing is ergonomic. Everything is ugly and awkward and strange. You have to manipulate things in ways that aren't natural. So you end up deferring to Python and doing in Python, more and more of those imperative object oriented manipulations. And you just pare down and pare down and pare down the scope of the things that still feel like they're suitable for this language. So in a way what you're doing is you're trying to maximize the language, but you're really minimizing it and and buying into the idea that this is a little toy domain specific language (DSL) that's only suitable for very narrow range of applications and for everything else. It's better to just use a normal scripting language. And I don't buy that because I think that if vector languages are domain specific, it is an extraordinarily broad domain in ways that are generally unappreciated. So most of my projects are basically attempts to disprove this myth with varying degrees of success.

01:08:48 [ML]

Yeah, I mean I agree with some of that. I guess what gets me is that, if the boundary is tough, I don't see why that necessarily pushes you towards the Python side of the boundary; because I think, one particular thing is that if you have Q embedded in Python, the reason you embed it (I would think) is to use the syntax. Now, maybe for kDB specifically you would treat that the same as SQL, like an engine.

01:09:20 [JE]

Well, you wrap an ORM around it and then you're not writing q anymore.

01:09:23 [ML]

Yeah, exactly, but I wouldn't think you would do that for an array language itself (I think). You do have problems ... [like for instance] you don't want your source code to just be a string in the language. That's not really nice, but you can probably get it so that you can [sentence left incomplete]. I think that as more of a challenge to solve in terms of making the embedding nice as opposed to something that would cause a Python user to say: "well, I still want to use APL, but I want to just call Python functions". Because once they're calling the Python functions, they'll realize that you know it's ... [sentence left incomplete].

01:10:00 [JE]

Well, sure, but I guess part of my point is just that having the the Python way of doing things that is not ergonomic for the the Q or k or J way of doing things, it sort of takes away the motivation for coming up with good solutions in the array languages. There's less of a motivation to figure out a nice way to do it from the perspective of this esoteric language, when: "I could just well ... I'll just dip down into this other language and I'll solve it the way that it already exists; I'll use the library and interface that has already been designed instead of expanding the scope of what I do with q".

01:10:44 [ML]

Maybe I mean, I think so ... [sentence left incomplete]. Currently the situation is if you're programming in Python you have no reason to use q ever; you have no reason to know about it. So I kind of would think that ... I guess it does bother me that by saying that by giving people the option to work in q or Python, they're going to choose Python. Like if that's the case, then everybody should just use Python [chuckles]. And I get that you're saying that they would choose it for the wrong reasons, for this interoperability and stuff. But I feel like a better solution to that is to make the interoperability better; make it very nice to use q from Python. And so then it comes close to the level of the language and at that point if you're using [it] a lot, you probably realize that it's better for a whole lot of things, and then you can actually start increasing your usage of q.

01:11:45 [JE]

Well, I mean I am of the belief that nice interfaces to libraries from q is not a thing that can be generated automatically. I know, you're not explicitly implying that in any way. My point is that it is a hard human design problem to adapt domains into the array language way of thinking. And a big aspect of education of array languages is sort of getting people to reopen their minds to the way that they think about a problem, the way that they think about instructing a computer to do things. And it kind of depends on changing the way that people go about solving problems and from an API perspective, changing the way that you go about expressing an interaction.

01:12:45 [ML]

Yeah, so I can see there's this problem where if you have an interface that's not good, people think they've been exposed to array programming, but actually have not.

01:12:59 [JE]

Yeah, certainly that's an aspect to it that. You know, they try it and it's unpleasant and so they step back. Or they would be pushed to think about solving a problem in a new way, if they were just using q but they've got the bumper bowling experience of: "Python is always at hand". Python is always singing the siren song to them that: "it would be so much easier if you just did it the way that you're used to" [others chuckle] And so it's kind of, you know, I don't think that it's an environment that is perhaps conducive to solving problems right now. To, you know, getting through it, to making the thing work. But I don't think that it's an environment that's conducive to broadening one's personal understanding of vector languages or an environment that's conducive to encouraging people to improve the array programming ecosystem itself.

01:13:58 [ML]

Yeah, so metaphorically kind of we've got a big gap between the conventional languages and array languages, and we'll say array languages are higher up, so you got to jump up across this gap. And the question is: do we want to build a ramp or not? And I can see both sides of this, definitely. I can see, #1, if you build the ramp people will start walking up the ramp and see there's a slope and they'll say: "this is awful; this place is higher up; I don't like it; I'm coming back down". Whereas if they're forced to jump, they've gotta do it all at once. But I can also see, you know, people looking across at this ravine and saying, I'm not jumping that! [chuckles]

01:14:44 [JE]

Well, maybe look at this from a different perspective, sort of tying into something that I noted in iKe. And I said in iKe that it would be really powerful if you can just init JavaScript; you can just play directly with the existing canvas APIs. But the problem with that is that now you're forever trapped in this ecosystem. Whereas again, if you weld yourself to the Python ecosystem then that means that if people are using this [sentence left incomplete]. I mean, I guess in a way this is less of a problem in array programming because there's more of a willingness to just throw things out and rewrite them from scratch to begin with. But you know, to a degree you can end up just carrying this boat anchor around forever; this piece of technology that you used to solve this one problem, you don't really need this whole ecosystem that's attached to it, but now, you know, we decided on the standard and now we're stuck. As opposed to, if you design something from whole cloth, it's really really hard work and you have to solve a bunch of problems that, you know, maybe have already been solved before and in other ways and it's entirely possible that you're going to end up reinventing wheels with four flat sides, but it's also possible that you can make something that's better, or at least better in the context of the language that you're using. It's a challenge, not a burden, I think, to try to enrich the array ecosystem and tackle new domains that are traditionally not close at hand.

01:16:26 [BT]

And I think one of the things you've done with Decker and Lil [sentence left incomplete] And I think Marshall's analogy of the ramp is a really good one because I think as soon as you talk about walking up a ramp to get to something else, you've identified your issue. What you want is a ramp that goes down so it's easier and it invites you into doing something with it, and I think that's the change in view that Lil has with Decker. It continually invites you: you could do this; you could do this; you could do this. And look what the power you would get out of it? Whereas I think if you're used to working with Python and that ramp looks like it's going up to start with, there's already this: "Hmm, I'm going to have to learn. I don't know. Is the pay off enough?" And all those questions are going to come into your head. Whereas, is a ramp taking you down into something, I think is a better way of thinking about it and I switched the [sentence left incomplete].

01:17:26 [JE]

It could be simpler; it could be nicer; it could be easier.

01:17:30 [ML]

Swinging bridge so you can go down to the bottom, but then you're just gonna get nauseous hanging out up there so you gotta go one way or the other.

01:17:38 [BT]

But I think the thing is, John is saying it's very hard to design ramps that go down because you're taking somebody from one environment to another environment. Inherently it feels like it should go up, and if it goes down the person who's designing the environment is working much harder to make that more inviting.

01:17:58 [ML]

Well, so of course, if you know how to program one way you're always going to think of it as easier, regardless of whether it is. I mean, I've seen people say, you know: "here's this super complex thing with all these ... [sentence left incomplete]". Maybe it's Haskell, [30] maybe it's like there's all these types and crazy ideas that you have to spend years learning and they say: "oh, this is the easy way to do it" and for them, it is.

01:18:23 [JE]

We're familiar rather than rather than more natural.

01:18:26 [ML]

So yeah, it's not necessarily possible. But I agree that it's definitely cool to have these languages that #1: they let you let you program in either style; #2: they let you go smoothly from an imperative style to an array style. You can say, just use an array here or there. And are just, you know, fun to work with. So it makes it easier to approach array programming exactly like you said without starting with, well: "I have to learn; what are what are these arrays doing? All these difficult array concepts right away".

01:19:06 [BT]

So where do you see Decker and Lil going, John? Where you going to take it from here?

01:19:11 [JE]

Well, I'm gonna continue to improve its breadth and and depth. I'm spending you know, most of my time right now squashing bugs and improving usability; making it more accessible; making it run better on more computers. There's a lot of work to do going forward to make it work better on touch only devices because there are an enormous number of people that, you know, primarily interact with computers through phones or tablets. That's the thing that's most affordable to them and there are adaptations that I can make to the system that will make it it work better there. The big thing really is that there are a small number of people that have played with Decker and have had a lot of fun with it, and maybe learned something and I hope that over time I can I can broaden that audience and more people will play with it; more people will have ideas of things that they want to make with it. It's, you know, the purpose of the thing is that it's trying to be an empowering creative medium and if it's educational along the way, and if it opens peoples minds to trying other languages and other ways of thinking about solving problems, those are those are great bonuses.

01:20:35 [BT]

I've seen somebody is actually doing Advent of Code in Lil.

01:20:38 [ML]

Ah yes, Raghu.

01:20:41 [JE]

Yeah. Razetime has been working through this. Hopefully it's been a mostly positive experience. He's filed a few bugs and I've tried to take care of those as quickly as possible.

01:20:54 [CH]

Well, if the currently non-existent Array Con ever becomes existent, we will definitely ... [corrects himself] ... the people (maybe the listeners) that end up setting up this fictitious conference can invite you to give a talk called Decker and Lil. And this is my request (I've had this question for like 30 minutes now, but it's much less interesting than the discussion that's been going on). My first thought when you described Decker was that it would be a perfect tool for designing something that I've seen designed in PowerPoint, and it's two different game shows. The first one is "Family Feud" and the second one is Jeopardy. Because if you've got slides, you can do it in PowerPoint, but it's completely terrible because you got to figure out how to you know, change the colors. "I've already asked questions, blah blah blah" and [for] Family Feud, if you've got built-in matrixes and arrays, it sounds like it'd be perfect for it because it's literally just like a 5x2 ... [thought left incomplete], but you're smiling, so potentially you or ... this hasn't happened yet? But so the question is: is my intuition that a Family Feud like game that shows just a 5x2 grid of top answers on the board, would that be a perfect thing to try and implement in Decker?

01:22:14 [JE]

That's the thing that you could build in Decker. I mean, there's certainly a wide range of of games, and you know, manipulatives that you can put into a deck. I guess a point of history ... we've talked a little bit about how Hypercard is one of the big influences on Decker and Hypercard was used by a lot of people to make toys and personal applications, but it was also used to make Myst, [31] which is one of the best selling video games of all time.

01:22:45 [CH]

Really?

01:22:46 [JE]

And also one of the most accessible video games of all time. It was a video game that was very well responded to by people who did not think of themselves as people who played video games, and it was written using a piece of software that was intended to cater to people who did not think of themselves as programmers.

01:23:05 [CH]

Yeah, that is a great point to end it on and we look forward to your future talk at this non existing conference that doesn't exist yet. Or I'm not sure, do you have like a, YouTube Channel or anything like that?

01:23:16 [JE]

I don't have a YouTube channel, but from time to time I'll write things or release new games and toys on beyondthem.com. I guess as a little bit of an advertisement, I'd like to point out that this month (the month of December) I'm hosting a little kind of game jam, or really like a thing jam where people can make stuff (make a deck in Decker) and submit it and share it with other people. By the time this comes out there will still be some time to participate. You could definitely make something worth submitting; an afternoon of tinkering. And so I'll provide a link to that. The the event is called "Decktember"  [32]

01:23:59 [CH]

Decktember? Awesome. Well, we will definitely leave ... [sentence left incomplete]

01:24:02 [ML]

Yeah, I was gonna tell you: you're going with thing jam ... at least call it a Deck Jam.

01:24:08 [JE]

Deck the halls [everyone chuckles]

01:24:11 [CH]

All right, yeah? We've covered a lot and we will put links to everything, including Decktember for those that are listening in December and want to join that. Check the show notes out for all of that. Anything else we want to [say] before we plug our contact info? Questions or things, John?

01:24:30 [ML]

I had a very important question that I failed to ask about Special-K. You said it covers the screen with a triangle. Now a screen is a rectangle. What orientation is the triangle in? [others chuckle]

01:24:39 [JE]

I don't remember, but it doesn't actually matter because from the programming perspective you're just getting a top left coordinate space.

01:24:44 [ML]

I know it doesn't matter.

01:24:48 [JE]

It's just [with emphasis] BIG triangle.

01:24:50 [ML]

So is it likely to be, like, a right triangle aligned with the top left corner?

01:24:53 [JE]

It is a right triangle, I'll give you that.

01:24:56 [ML]

Then it's a right triangle. OK, we have some information.

01:24:57 [JE]

Right. I thought about making it scalene, but it just felt too post-modernist. Yes, so I decided to go with an old standby.

01:25:06 [ML]

All right, yeah sounds.

01:25:07 [CH]

Good, we had such a good outro Marshall and then you just come in and you just flip the Scrabble board upside down. The tiles are everywhere now [everyone laughs], you know? You're like the person that comes in the room with a deck of cards, and then squeezes it and watches all 52 just fly around the room [laughs].

01:25:23 [JE]

That's another excellent thing you could build: if you could do "52 card pickup" You just need to write 52 cards [lots of laughs]

01:25:30 [ML]

That's an outro.

01:25:32 [JE]

For that, you could use those scripts to do that automatically.

01:25:35 [CH]

Alright, well Decktember folks. You heard it. Great application. Go write that. Pick up a 52 deck of cards. We'll finish. I'll throw it to Bob. He's got our contact info.

01:25:45 [BT]

contact@arraycast.com. The usual and big shout out to our transcribers, Igor and Sanjay, and they do a great job and provide you the transcript of each episode as it comes out. That's the target and we've been able to hit it so. It's a great way ... [sentence left incomplete]. We're talking about accessibility: there's a lot of people who access the the podcast that way, and I think it's a very important thing that they do and they do it very well.

01:26:10 [CH]

Yeah huge thanks to both of them. It is a ton of work and yeah, a debt of gratitude from all, both myself and the rest of the panelists of Array Cast. And yeah, I guess with that we'll say once again, John, thank you for coming on. At one point I just kicked up my feet and was just like: "this is like just entertainment for me". Listening to you go back and forth with Bob and Marshall and everyone. And yeah, we'll probably at some point have you back in the future. I mean, you keep on pumping up creative projects, and you know, maybe when this this Family Feud talk comes out, you know, the conference that, you know ... [sentence left incomplete]. If I say it enough times, it'll happen [meaning, the conference]. It'll just materialize, you know!

01:26:48 [BT]

I thought you would do Family Feud with Decktember.

01:26:52 [CH]

Uh, maybe

01:26:52 [BT]

I thought that would be your project [everyone laughs]

01:26:58 [CH]

I also said on episode 42 that I was going to go and implement K and K6 in my language of choice and I have not gotten [to it]. You know, I think there's a lot of things I've committed to on this podcast.

01:27:10 [JE]

No pressure. And I'll probably be viewing it next year too if you want to just take a very slooow approach.

01:27:16 [JE]

This is true; this is true. I've got, I want to say several decades, but I'm not going to say that, you know. Just knock on wood ... whatever number, you know, because ... [sentence left incomplete]

01:27:26 [JE]

Well, you gave an open interval on it, so you know like as long as you do it at some point in the future before you die, you didn't technically lie.

01:27:33 [CH]

Oh, of course, of course, yes, I mean, as your veteran podcast guest you know [chuckles]

01:27:40 [JE]

And as we all know, following through on a throwaway comment in a podcast is one of the most important quests that you can give yourself in life.

01:27:49 [CH]

All right, John thanks so much for coming on and I guess at that we'll say: Happy Array Programming!

01:27:52 [everyone]

Happy Array Programming!

[theme music]

</details>
