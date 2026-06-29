---
title: "Episode 23: Andrew Sengul - The April APL Compiler"
date: 2022-03-19 00:00:00 +0000
episode: 23
buzzsprout-id: 18617104
keywords:
- array-programming
- array-languages
- conor-hoekstra
- apl
- april
- andrew-sengul
- common-lisp
- dyalog
mp3-url: "/assets/audio/episode23.mp3"
episode-type: full
explicit: "no"
block: "no"
layout: podcast
excerpt_separator: <!--more-->
redirect_from:
  - "/episodes/episode23-andrew-sengul"
  - "/episode23-show-notes"
  - "/episode-23-transcript"
---
In our twenty-third episode, Andrew Sengul, creator of the April language tells us about the advantages of combining Lisp and APL.
<!--more-->

**Host:** Conor Hoekstra

**Guest:** Andrew Sengul

**Panel:** Adám Brudzewsky, Stephen Taylor and Bob Therriault

---


## Show Notes

- [https://jsoftware.github.io/j-playground/bin/html/emj.html](https://jsoftware.github.io/j-playground/bin/html/emj.html)
- [https://www.youtube.com/watch?v=vyILnD0e2IE](https://www.youtube.com/watch?v=vyILnD0e2IE)
- [https://adspthepodcast.com/](https://adspthepodcast.com/)
- [https://youtube.com/watch?v=AUEIgfj9koc](https://youtube.com/watch?v=AUEIgfj9koc)
- [https://github.com/phantomics/april](https://github.com/phantomics/april)
- [https://zenodo.org/record/6381963](https://zenodo.org/record/6381963)
- [http://jmc.stanford.edu/](http://jmc.stanford.edu/)
- [https://en.wikipedia.org/wiki/Steve_Russell_(computer_scientist)](https://en.wikipedia.org/wiki/Steve_Russell_(computer_scientist))
- [https://en.wikipedia.org/wiki/M-expression](https://en.wikipedia.org/wiki/M-expression)
- [https://en.wikipedia.org/wiki/Common_Lisp](https://en.wikipedia.org/wiki/Common_Lisp)
- [https://en.wikipedia.org/wiki/Lisp_machine](https://en.wikipedia.org/wiki/Lisp_machine)
- [https://devpost.com/software/scenario-engine](https://devpost.com/software/scenario-engine)
- [https://yaml.org/](https://yaml.org/)
- [https://vimeo.com/269495385](https://vimeo.com/269495385)
- [https://aplwiki.com/wiki/K](https://aplwiki.com/wiki/K)
- [Bloxl.co](http://bloxl.co/)
- [https://bloxl.co](https://bloxl.co/)
- [https://github.com/phantomics/april/blob/master/spec.lisp](https://github.com/phantomics/april/blob/master/spec.lisp)
- [https://github.com/phantomics/april/blob/master/vex/vex.lisp](https://github.com/phantomics/april/blob/master/vex/vex.lisp)
- [https://github.com/cbaggers/cepl](https://github.com/cbaggers/cepl)
- [https://www.youtube.com/playlist?list=PL2VAYZE_4wRKKr5pJzfYD1w4tKCXARs5y](https://www.youtube.com/playlist?list=PL2VAYZE_4wRKKr5pJzfYD1w4tKCXARs5y)
- [https://racket-lang.org/](https://racket-lang.org/)
- [https://en.wikipedia.org/wiki/Scheme_(programming_language)](https://en.wikipedia.org/wiki/Scheme_(programming_language))
- [https://groups.google.com/g/comp.lang.apl/c/vRjMvZZUIiw/m/CxGL-FR-AAAJ](https://groups.google.com/g/comp.lang.apl/c/vRjMvZZUIiw/m/CxGL-FR-AAAJ)
- [https://news.mit.edu/2021/professor-emeritus-paul-penfield-dies-0903](https://news.mit.edu/2021/professor-emeritus-paul-penfield-dies-0903)
- [https://kparc.com/lisp.txt](https://kparc.com/lisp.txt)
- [https://github.com/phantomics/april/blob/master/patterns.lisp](https://github.com/phantomics/april/blob/master/patterns.lisp)
- [https://www.dyalog.com/apl-seeds-user-meetings/aplseeds22.htm](https://www.dyalog.com/apl-seeds-user-meetings/aplseeds22.htm)

<details markdown="1">
<summary><strong>Transcript</strong> (click to expand)</summary>

Transcript

Transcript prepared by Rodrigo Girão Serrão

Show Notes

00:00:00 [Andrew Sengul]

Now recall I was originally a writer and I may approach programming in a way that's different than most people, because when I program, I think in terms of creating patterns of meaning, it's like a a prose that informs a a computer process. So what APL allows me to do is switch into a complete other mode where I'm suddenly operating on entire bodies of data at once and distilling algorithms down to their very bare elements.

00:00:40 [Conor Hoekstra]

Welcome to another episode of Array Cast.

00:00:43 [CH]

I'm your host Conor, and today we have another special guest. But before we get to introducing him, let's go around and do brief introductions. We'll start with bob, then go to Stephen and then go to Adám.

00:00:53 [Bob Therriault]

I'm Bob Therriault, I am a J programmer. I'm an enthusiast, I'm not actually a professional programmer. I just do this for fun and I do it in J.

00:01:02 [Stephen Taylor]

I'm Stephen Taylor. I'm an APL and q programmer, and I definitely do this for fun.

00:01:08 [Adám Brudzewsky]

I'm Adám Brudzewsky. I'm a professional APL programmer, but that doesn't mean it isn't fun most of the time, at least.

00:01:16 [CH]

And as mentioned before, I'm your host, Conor. I'm an unprofessional APL slash BQN slash J slash all the other array languages, programmer and combinator enthusiast at large, and I think we have two announcements so i'll throw those over to Bob and then we will introduce our guest for today.

00:01:32 [BT]

Well, speaking of fun, J has a playground now, so you are able to run J off your browser and in our show notes, which you should always pay attention to, our show notes and our show notes will have a link to that. [1] That and there are some really cool things you can do with this playground. It not only running J and it's in its development stages, so there are a few things that it doesn't do quite as well. It does run labs. You can drop labs down, run labs off the menu and it does some really other cool things. Like for instance you can set up a multi line definition, make a link out of it and send it to somebody else and they get the multi line and definition in the browser which is really cool and so I think it'll change the way some people are using J and sharing their information, and in addition to that, as we record this, yesterday, if you're is, the Julian calendar is original anyway, in our calendar march 14th is known as π day, and I did a video yesterday on the digits of π and how you can obtain those up to a fairly large number in J [2], and those were my two announcements.

00:02:36 [CH]

Awesome and I actually just remembered that I meant to announce something, although I can't actually remember if I stated this on this podcast or my other podcast [3], so maybe I'm making a correction for a mistake I didn't even make on this podcast. But for a while and this will actually not make sense to most people, so just feel free to tune this out, i've been saying that the psi combinator, which is known as over in both APL and q as a specialization of the S Prime Combinator, AKA the fork. That's actually not true at all, because the monadic fork takes only a single argument and the psi combinator, AKA over, takes 2 arguments. It is a specialization of the D2 combinator. I'm not going to explain that 'cause I've already confused everybody, but stay tuned either on this podcast or on my other podcast. We will get into that in more detail, but I apologize for having made that mistake for I don't know how many weeks or months at this point, but with those announcements out of the way, let's get to our guest for today so our guest is Andrew Sengul, who i'm sure a few of our listeners have heard of at this point, as he's given multiple talks he recently. I think it was at the British APL webinar gave a talk and that was in the last couple months at this point, so we're recording this in march of 2022, but I actually first saw this talk at the Lisp New York meetup back, i went and looked up the date it was September 8th of 2020 [4], so we're talking about what is that 2? Is that a year and a half a year and a half ago at this point and Andrew gave a talk basically of an implementation of APL, which also has some influences from k and other array languages in Common lisp and that's why he was giving the talk at the Lisp New York meetup and I actually reached out and we ended up having a conversation a couple weeks after that. So Andrew is a super fascinating person to talk to. He's currently, I believe, the principal at scenario technology, which I'm sure he'll tell us a little bit more about, and I think this is the first time that we have a non, sort of APL programmer first, i think, Andrew, or he can correct us is a Lisp, Common Lisp programmer first and APL programmer second. But with that introduction I'll throw it to Andrew. Feel free to tell us a little bit more about yourself and your journey through tech and how you ended up writing an APL compiler in Common Lisp.

00:04:49 [AS]

Thank you Conor and great to be here. I appreciate everyone hosting me today. OK, so let's start off talking a bit about April [5]. So April compiles the core APL language into Common Lisp. It includes almost all the core functions and operators that are in Dyalog APL, and they mostly work the same way. They're similar enough that I ported many of Dyalog's dfns over to April, and they're used as part of the test suite. So as you mentioned, April has some extras like the k style if statements. And like in k, you can use any number of named variables, so you have your own variable names as opposed to alpha and omega. If you use that format, you can use the syntax from k with a set of indices at the beginning of the function listing the variables. So right now April main use case is invoking APL within a Common Lisp program, so you write open parenthesis April and then a string containing APL code and then close parenthesis. There is a lot of other options for the input and configuration, but that's kind of the minimal use case. So I'm investigating some options to do things that would make April more independent of common lisps from the viewer, from the users point of view, like making April plugin for Emacs, that would allow you to use it like you would use any other APL interpreter with a REPL that you would type stuff into and get results without seeing any of the lisp code, but that's not ready yet, and my use cases for April so far have involved building kind of the semantic and logical structure of a program in Common Lisp and then doing the like the heavy algorithmic lifting inside of APL. So I recently wrote a paper for the 2022 European LISP Symposium where you can see examples of some of this and we'll put that out there for the viewers in the notes [6], and I have a one line example where you use a Lisp library to load the contents of a PNG image into an array of RGB integers and then you feed that to April to build a matrix of the color palette in the image. So each row in the matrix is 3 elements wide with one set of RGB values per row. So that kind of demonstrates what you can do combining common Lisp and APL. Well, so for for those of for those listeners who aren't familiar with APL, LISP and APL actually have a surprisingly similar history. Both of the languages were the work of mathematicians creating a new math notation. The creator of Lisp, John McCarthy [7], wanted a language to express the Lambda calc. So he built this parenthetical notation and neither McCarthy nor Ken Iverson initially thought that their languages could be input to a computer. McCarthy told his student, Steve Russell[8], that you can't make eval work on a computer. Eval is a theoretical thing, but Russell ended up, he went and made it work. He wrote the original Lisp interpreter on an IBM 704. So McCarthy's original writing on Lisp was in the late 1950s, about the same time as Iverson was creating the APL notation. But this was implemented on computers sooner than APL was, when Russell wrote the The Lisp interpreter, he simplified the expression syntax. Originally they had something called M expressions [9]. He changed to using S expressions which were everything in the expression inside a set of parentheses. So and this was kind of analogous to how Iverson colleagues simplified his notation to use with a teletype. They got rid of the kind of the superscripts and subscripts he was using and made it a more linear format, so both languages were simplified a bit to use with the computers of the day. And both Lisp and APL came to prominence in the mainframe world. Both of the languages served as operating systems for the mainframes that they ran on, like APL, had all the features like, you know, send a message to someone else's terminal and all that stuff built in and Lisp, no, APL has historically been an interpreted language. Lisp pretty quickly went to being a compiled language, but when a lot of people think about compilers, they think of something that produces a static executable. But Common Lisp [10]and other lisps they have, they're both compiled and they are also a real time interactive system, so you get a REPL. You can evaluate things in that REPL, and one of the interesting things about Lisp is that you can evaluate and re compile a single function out of your program, and this is something a lot of people don't expect or realize is present there, but in Lisp programs you can recompile function or even in any individual closure in your program, re evaluating it in real time. So when you're writing a program, you can actually create things in the source code that are like control panel elements that you can re-evaluate to change things in your program as you write. But anyway, something another interesting thing that happened with Lisp was that people created computer systems that were engineered to run Lisp on the bare metal called Lisp Machine [11]. The earliest of these were mainframes at universities, but there were a couple companies that built desktop Lisp machines. Those were Symbolics and LMI, and to this day they're some of the most unique computers ever made. Their architecture is like nothing else out there and they enable interactive development debugging down to the hardware level. So Lisp and APL both hit a kind of a slump when the micro computers took off. Having a computer that could fit on a desk and that a computer consumer could afford was, it was a revolutionary step in technology, but you needed to use low level languages to really practically program on those machines because a a higher level garbage collected language wouldn't run in an acceptable speed. And of course there were lisps and APLs for these computers, but you couldn't use them as much more than a toy. So they were locked out of the market segment that ended up defining computing, and that legacy has persisted today, even though our phones are thousands of times faster than mainframes from the 70s. So now it is notable that APL was powering one of the first PCs, the MCM 70, but it didn't, it didn't hang on in that market segment. So from this point, let's talk a bit about April history and my own. So I was fascinated by computers as a young age, but from a young age, but when I got to college, the main thing that I was interested in there was journalism and my initial plan was to be a writer at one of the big daily papers. So I got to have a lot of fun as a reporter. I would, you know, I would go to all these stories and I would i would write something interesting by the end of the day, and I picked up photography later and started, i became a combination writer, photographer for the school paper. This was at the University of Washington, but toward the end I started checking out the world of the daily papers in the professional journalism world, and I learned that if you're working at a big daily paper, it's actually a call center job. You're sitting at a phone, calling people and talking to them about your your stories, you don't go to you don't actually physically go to anything unless you're one of the most elite magazine journalists. And moreover the print, the whole print journalism world was spinning in the drain and most openings were in the online journalism world where you were expected to work for free forever and maybe get a a prayer of getting some kind of paying job. So I was increasingly put off by the world of journalism and I I tried my hand at different things and it turned out that people liked getting websites built. Lots of people wanted me to write websites for them, so I started off in the very shallow end of the programming world as a WordPress PHP developer. I always wanted to do something more and I had various ideas for really interesting things I could do on the web and I my first real big project was a web application called the Scenario Engine [12] and that's the Scenario, that's what Scenario, that's what I built: that scenario technology. So the Scenario Engine was a detailed system for building out interactive "choose your own adventure" games. You had a visual vector graphics based system for viewing this network of nodes that you created, and so a user would hop from node to node by making choices and the nodes could have custom JavaScript attached to them for program logic, and it had a YAML [13] based system where you would specify the media in these nodes and you could. Also you could also create custom code generating interface elements to allow non programmers to specify things in a node within set of boundaries like in a typical scenario you would have point values for things like say that each character has an affection score depending how much they like you and you could give the non programming developer the ability to increment or decrement that score with a little drop down menus say you know at this node if you say this, the character will like you five points more. Something like that. Or you could have a money system or some other kind of variable tracking. And then the this was a presentation agnostic system. It communicated with the front end via JSON, but the front end was designed so it could have any kind of media you wanted and the YAML system allowed the programmer to specify what kind of media interface the non programmer would get. So you could you could like for my scenario, 'cause the presentation layer I built was a pretty simple web application. You could have line of text and a picture and maybe a sound effect at a given node, but you could potentially set something up that would run in a 3D game engine and you could maybe choose meshes and backgrounds and more sophisticated media so it was all very programmable and very meta programmable, but in the course of this project I learned two things, for one, the learning, the corporate learning and development field wasn't interested in trying new, innovative things like the scenario engine. No one wanted to budget for ambitious projects, and that was the market that I had aimed at because this did things that in the L&D field were very unique and hadn't been seen before. But no one wanted to make the stretch to try this or to train people to use it, and the second was that there were the second thing I learned was there were limits before I could go with metaprogramming JavaScript. I thought that my system had accounted for nearly any eventuality, but I was wrong when somebody asked me if they could write a, they wanted to write a story node where a character you could ask a character, a series of questions, and as you ask questions, they would be removed from the list of things you could ask. It's pretty simple concept, but I realized that implementing this within my model would be very complicated. It would require essentially a basic extension to the model, and that more extensions to the model would start to really exponentially increase the complexity of the system. So I searched far and wide for a solution to this and my perspective then was limited to the world of mainstream languages and technologies. But for a long time, I'd heard whispers in these rumors that there were other ways of doing things in programming. In particular, I'd heard about the Lisp language. I'd heard it was a programmable programming language where data and code were the same. But Lisp and the languages like it were always framed as this weird fringe thing that nobody used anymore. Any use of them had happened in the distant past, and they were basically forgotten. But in the world of mainstream languages, I couldn't see a solution to these problems that were cropping up, so I went down this path to see what I could unearth of these forgotten technologies. My R&D into Lisp was long and difficult because Lisp requires you to think in a way that no other language does, and my initial project was Lisp, with Lisp was one of the most ambitious things I've ever done. It was a general framework for interactive multimedia program. And this framework can represent a program as multiple interfaces from a straightforward text editor to a spreadsheet to a vector based graph node editor like what I built for the Scenario Engine. So that project is called seed and to get into the details of it would take us far off track. But I presented that at a previous Lisp NYC so you can post that link for everyone listening [14]. So let's focus on my other major Lisp project. At the same time that I was learning about Lisp, I had friends who introduced me to the world of array languages, in particular to k&kdb [15]. I was amazed to learn about kdb because it seemed like some kind of super technology that had kept a secret within the financial world. So I wanted to try building a kdb application of my own, but I was having trouble understanding how the syntax of k&q worked. Some of it made sense, but some of it seemed totally alien and backwards, and while I was investigating the history of the language, the name APL came up and learned about Arthur Whitney and how he was a protege of Ken Iverson, and Iverson had written APL, and that was kind of the ancestor of all these languages, so it wasn't the first time I'd heard about APL, I remembered hearing about it once a long time before. I don't even remember exactly where this was, but it was on some old Internet programmers board. Someone posted a message about Iverson's original book, a programming language. And they explained that there was this computer language APL, that used special characters that were unique to it. I thought, wow, that's the weirdest thing I've ever heard of. Why would anybody do that? And I promptly forgot about it. So APL had come up again probably 10 years or more after I first heard about it, and this time I thought maybe I should try this APL. Maybe it'll help me understand k better. In the moment that I tried APL, it clicked. The power the the flexibility, the potential to perform dramatic data transformations with a handful of characters. There was nothing else like it and I immediately picked up on the allure of golfing, finding out how few characters I could use to produce an interesting effect. And then I understood k&q because they were a departure from APL. The APL paradigm was their starting point, with the right to left evaluation, and they had absorbed some concepts from other languages and kind of drifted from it. But the APL concept was at their core. And I was thinking it would be great if I could use APL Lisp together and it just it happened that one evening in 2017 I attended a presentation by some guys from Kx Systems who were out spreading the word about kdb and showing some of the recent features from Kx. And on my way home from that, I thought I should try making an APL compiler in Lisp. How hard could it really be? I'd heard that compiling APL into Lisp was that compiling APL was supposed to be impossible, but maybe the power of Lisp would make a difference. So April began its life as a file called APL test dot lisp. I wrote a very crude parser which could write it could build vectors of numbers. It would read numbers. If it was just one, it would make a scalar. If it was multiple, it would make a vector and it could recognize some of the APL characters and from that point it evolved. So writing an APL compiler turned out to be a much bigger job than I anticipated. Every part of April has been rebuilt at least three times. Early on I had a very elegant system for handling array transforming functions. So to implement any array function like take or partition, enclose or shape, you start with your input array. And then based on the input array and the parameters given, you figure out the shape of the output array and then you copy elements from the input to the output. So all the array transformations are basically following that pattern. So the system I had for doing this would take a vector of the coordinates of each element and it would do a transformation on that vector of coordinates. That's analogous to the transformation done on the array shape of the input. So let's say that you have a 2 by 3 by 4 array, and you enclose with axes one and three on the array. So to get the output shape, you take the two dimensions specified by those axes, these you make that the shape of each inner array and then the remaining dimensions you make the shape of the outer array. You do the same transformation on the coordinate set for each element, so you take the 1st and 3rd coordinate and those are the coordinates in the inner array and the 2nd coordinate is the coordinate in the outer array. So this was really elegant to program. I built it on a recursive function that was less than 25 lines going through the coordinates of each element. But this algorithm was impossible to parallelize. It was recursive and it it needed to reuse the vector for each set of elements. Otherwise you'd have huge memory usage, so now the way I do array transforms is to go over the output array in linear order, and I do arithmetic on each row major index to find out where to put the value. So the programming for that is a good deal more complicated, but it's parallelizable so that just reflects some of the work that's been done. And like I said, even since that original Lisp NYC presentation, I estimate that about 95% of the code is different between then and today. So April has April, what's really driven the development of April partially is that April is being used for a hardware startup called Bloxl [16], where I'm CTO. And there are other users working on projects with April, but Bloxl is the flagship application and you can see the Bloxl website at bloxl.co and that will go into notes. Bloxl is a giant LED matrix, which is the LEDs are inside of transparent block windows. Everyone seen those block those kind of old school block windows that are used in architecture blocks all uses those same windows. The blocks of ones are made out of acrylic and each block contains 4 LED which light it up and the block functions as a pixel. So the Bloxl is a very low resolution display because each pixel is 6 inches square and April is used to build the animations and process other types of data for the display. Like Bloxl can be interacted with through movement, it can respond to sound using fast Fourier transforms and it can also take in MIDI input and other forms of input to generate patterns. So Bloxl's IO and the creation of its animations is all done using April. So comparing April two other APLs, the most distinctive thing about April is its interoperability and extensibility. So in April you can add in new functions from the outside Lisp environment in a handful of lines and this means that every Lisp feature in all the libraries in its ecosystem are accessible for use within April, so April doesn't have any built-in tools for system interaction by default, but you can add them if you need to within within a few minutes. In my paper I have an example of adding a function to run shell commands and it's only 7 lines. And April is also a modifiable extensible language. My paper has an example where you add a new lexical function to April in just 12 lines, including two unit tests. So Common Lisp is one of the best languages to build an APL in, because it natively has all the array types you need. Common Lisp supports high rank arrays and the like. The current builds of most CL support up to 256 dimensions. Older, some of the older, like SL builds, supported arrays of up to 2 to the 16th power minus 7 dimensions. It's a really amazingly high number, but I think they removed that because it was, it was slowing something some things down. So now the ceiling is a bit lower 256, but still higher than most other APLs. And Common Lisp also supports 0 rank arrays, so the arrays that April outputs you can process using standard common Lisp code with no special libraries. Now, for example, in Python you couldn't do anything to a multidimensional array coming out of numpy with Python standard tools, because Python only supports vectors. And April also gives you multiple windows on the compilation process, and you can see this in the paper 2. You can pass an option to April to make it print it's compiled output instead of evaluating it, so you can see what a given expression compiles to. So I've done considerable work to make this compiled output human readable. There's a lot of macros I wrote, yes, for the compiled output so that it would be succinct and this has helped me to debug. So I pass that benefit on to the users who can check out their compilations and see what they produce. And you can also see the tokens that April lexer outputs by passing a different option to the April compiler you could say is a 2 1/2 pass compiler. It first has a lexer which transforms the tokens into code, and then it does a lexer post processing stage. So lexer post processing is used to pick up the function variable names, and this helps a lot for for knowing what the what's a function, what's a variable before things are passed into the main compiler, and it also does the like processing of guards has to be done at the post lexer state. Guards are kind of a tricky thing to compile, if you can imagine, because in for an interpreter guard is easy to handle because once you encounter that, that colon you figure out if the statement before it was true or false, and then you either skip the next line or skip the line after the next line, depending on whether it's true or false. But in a compiler you don't know if that first thing is true or false, so you have to find out if there's a guard and then you have to wrap the following lines in an if statement. And that's that's best done before you hit the actual compile stage, but that's just it's one of the hurdles that comes up compiling APL. But with the important part is it all works, and Lisp helps to make it possible. To talk a bit about my language philosophy and why I embedded Common Lisp in APL, different groups of APL implementers have grappled with the fact that APL core notation itself isn't enough for all programming needs, so Dyalog dealt with this by building up its system of control statements like the if the else, if the the case. And Morten Kromberg himself has said that these aren't really APL. These are kind of an add on to APL, so I'm not such a big fan of the Dyalog control statements and adding procedural things directly into the language. So my approach is to create a more distinct boundary between APL code and an external language that's used for the logic. And if I'm going to use an external language, I want to use the most powerful one available to me, which is Common Lisp, where I can design any semantic structure I want for my program. So this has really empowered the development of Bloxl, because for instance, the animations for Bloxl or the pixel animations use a spec format that I built in Common Lisp, and those animation specs often require custom functions for an individual animation. So if I'm writing these specs, I'm faced with it if I'm writing this in a more verbose language like Lisp, I'm faced with a choice. If I want to have a custom animation effect in a given animation, I can put that program in the individual animation spec and I can bloat it by dozens of lines like it might be 15 lines versus 50 lines for a spec if you have that behavior in there, or I can put the animation function, the dedicated function in a different place. In that case, I'm bulking out my codebase with many functions which are each only used for a single animation, so that's more technical overhead, more bookkeeping I have to do. On the other hand, if I build the custom animation function in APL, then it's only one or two lines that's being added to the spec. And it all the all the animation happens in that one line, so that's a way to fold away the complexity of that of that operation. So that's a that's a win that you can't get using any other programming paradigm. Speaking of April design, when it comes to April design, one of the most distinctive things about it is the fact that the language is based on a central specification, so you can see this in April source file spec.lisp. Which will link in the notes [17]. And in the vector language group some people have, you know, they said to me that this was a bad language. It's an ugly language. There's no reason to use it. It's needlessly verbose and complicated. They like to bring up that comparison where they say that APL is a jewel and Lisp is like a ball of mud that just becomes a muddier the more you add to it. And they ask me why I use Lisp and my reply to that is just read spec dot Lisp in APL. I don't know of any other language whose codebase is organized around a central specification, and that spec describes everything in the language in under 1000 lines, and there's more with all the unit tests, but the the spec has all the all the functions and operators in there. They have like listings like the inverse forms of every function, there's tags on every function that say whether they're scalar, whether they're commutative and some fun–, whether they can be used for things like the assignment by selection, some functions have alternative characters like the the and function can either be the the basic ASCII character or the specialized APL and character and all of these things are expressed to the spec. In other languages whose code I've looked at, the standard library functions are sprawled out over dozens of source files, and there's no central place that you can go to get a bird's eye view of the language, and that's the kind of development that Lisp enables where you can create semantic structures that are adapted for your specific application. And then a word about code size. I've heard reports that Dyalog core interpreter is about 100K lines of code, and the entire Dyalog APL system is about half a million, and GNU APL is also about 100,000 lines in total based on their webpage. So April, most current count made today is 11,557 lines and this brevity is another thing that is enabled by Common Lisp. So for a student who wants to understand vector languages, the April code base is reasonably approachable, especially when you have specced out Lisp as a starting point and the other the other languages. Even if Dyalog source were available, would be daunting to approach. April is based on a framework called VEX and you can see this in the repository. There's a folder called Vex and Vex is a general framework for building vector languages [18]. So later on, like I'm one of my, you know, one of those plans on the horizon is to making a variation of April with first class functions and some other changes of mind to the language. So this will be enabled by VEX, and that's going to be one of the first kind of tests of vex flexibility is, if I can create a variant on April with first class functions. But later vex, could even be used for a k in Lisp or a BQN in Lisp. So that, that's something on the horizon so thus far, does anybody have any burning questions? Any things you'd like to better understand?

00:34:45 [CH]

Yeah, I think we probably all have a bunch of questions. It's interesting that you just answered one of my questions, which was going to be, do you have a current line count? Because I think I recall back in September of 2020 it was roughly 7000, so it's grown, uh, by about 50% and and when you were saying that you've rewritten things, you know at least two or three times I went and took a look at the insights, and so I'm not actually sure this has been mentioned, but April is totally open source and or actually, I'm not. I haven't checked with the licenses.

00:35:17 [AS]

Yes, April is Apache 2.0 license, so it's very permissive.

00:35:24 [CH]

Yeah, and with the awesome part about that is that everything that Andrew's been talking about you can go and take a look at the source so the spec dot Lisp, uh, spec dot lisp, all of the implementations like you can if you're looking to get started. I know at this point there are quite a few open source there's J, there's BQN, there's April, but back in the day there wasn't a lot of open source implementations of vector languages that you could go and look at, but on the insights page just to wrap up what I was saying, there's been since August 2020. 87,000 additions and 74,000 deletions. So you can see that that's considering that the core of the language is only you know roughly 10,000 that there's definitely been, uhm, he's not making that up. He's definitely been doing a lot of rewriting, but yeah, I do have another comment or question, but I'll pause and let other folks, II think Bob you were you were rubbing your hands together.

00:36:14 [AS]

Like, I've I've done some simple estimates that show that April code base is 95% different than it was when I gave my Lisp NYC. presentation and I've had some great users who have been doing a lot of bugs. Justin Dowdy in particular has been has given over 100 bug reports. Many other people have made contributions as well, so thankfully there's an enthusiastic community forming around April who have been helping to drive its development and it would, it wouldn't be it wouldn't have come as far without their contributions.

00:36:53 [CH]

Is that Justin the same Justin that was the one who posted the Dyalog APL in Clojure repo just recently?

00:37:01 [AS]

Yes, the May project.

00:37:03 [CH]

Interesting, yeah yeah. So we have April, which is APL and Common Lisp. And now we have May which is APL and Clojure. So someone out there listening to this can go and create June which will be insert other Lisp or insert other language uh, with APL in it.

00:37:20 [AS]

Maybe J and Lisp.

00:37:21 [BT]

Yeah, I was going to say the obvious one is J in some form of Lisp and you've got June.

00:37:27 [CH]

That's true.

00:37:28 [AS]

Now, April was originally named as a, so it stands for array programming reimagined in Lisp.

00:37:36 [CH]

Ah, that's interesting. I don't think I knew that.

00:37:41 [ST]

Andrew in your NYC, in your Lisp for my C presentation you showed in Lisp the output from the parser. So nice expressions where parenthesized, which showed a a function and then the data following him. And they reminded me immediately of parse trees in k&q. So our q do have functions as first class entities and they make available the results of the parser in the language so that you can take the parse trees that come from passing expressions and then manipulate them as ordinary k or q data structure. And then evaluate the results of that. If I was following what you were explaining in New York, that's that's not something well, it's certainly not something that APL normally does. And if I was following you, it isn't something that April does, but it occurred to me: well, you, you can get the results of parsing your APL expressions, and they're available to you in Lisps, so I suppose your Lisp programs could manipulate APL expressions rather than composing them as text, to have them evaluated. I just wondered if that's anything which you've exploited.

00:39:07 [AS]

Yes, as a matter of fact something you can do in April, you can't do in other APLs is invert a dfn using the power with a negative. So there's a considerable amount of code manipulation that goes on inside of April with the taking the compiled code and putting it through multiple transformations. Then one avenue of development that I've considered for April has been using the compiled output and instead of evaluating it, passing it to a downstream compiler which may produce optimized output in different paradigms. So for example, if I want to do something if I want to do some kind of real time processing and code it in APL, vector languages have traditionally not been considered or options for real time because they can do operations that would not work in a real time language, but you could have a downstream compiler that will it will convert a subset of April output into real time languages like JLD. If you want to write a shader, say with APL, if you do a big array transformation like re enclose or something like that. It would say you can't do that and throw an error, but as long as you're doing simple arithmetic and other transforms that are doable on the GPU, then it would, it could produce a JLD. There's already a there's already Lisp systems that produce shaders. One of these systems is called CEPL and there is a YouTube Channel where you can watch a number of videos demonstrating it [19]. So this is how Lisp has been applied to the creation of shaders and at some point it would be great to tie APL in there via April using a downstream compiler. I'd really like to write a shader in APL, because it would give me the most expedient way of of expressing that logic. So that's and then there's also, I've been looking at real time audio processing. All things that you could do with using a downstream compiler and some glue connecting it to April.

00:41:11 [CH]

One of the questions that I had, uhm, 'cause you've mentioned you know, choosing Common Lisp is one of the most powerful languages to do this kind of thing in when you were entering the world of lisps. Did you look at other Lisps like Racket and Scheme and Clojure? And is there a reason that Common Lisp is a better fit than other languages or other Lisp languages?

00:41:32 [AS]

Yes, I started the first Lisp. I really did much with was Racket [20] and I've looked at the the Scheme world. So the thing about Scheme [21]is that it's it's fragmented and there's a risk of betting on the wrong horse when you pick a Scheme because everyone got their variation and maybe the one that you choose isn't going to be around for the long term, maybe people are going to gravitate to another. And Racket is that Racket actually seems to want to get away from being a Lisp altogether. So the thing with Common Lisp is now, its detractors will say it has an ultra conservative philosophy. It has a standard that hasn't changed since I think 1995. And there's not much change going on, but Common Lisp is one of the most future proof languages around. Libraries written in the 90s with Common Lisps can still be used today. Bit rot is much much slower in the Lisp in the Common Lisp world, and that's because it has this unifying specification. So for those who don't know, Common Lisp has a variety of of implementations. There's the one that I mostly uses SBCL, steel bank Common Lisp, which started out as Carnegie Mellon University common Lisp, and that that's that one emphasizes performance. Then there's Clojure Common lisp. There is armed bear common Lisp, which compiles to Java. There's embeddable common Lisp, ECL, which is more efficient, runs on small processors. There's the the new class compiler that compiles, that is, is implemented in C++ and C++ interop, and there is allegro com. There's allegro, common Lisp and Lisp works, which are both proprietary implementations, but they all have, they're all mostly compatible and April has been tested and made to work on all of them. So in the Common Lisp world we have multiple of these alternatives, but you are guaranteed a level of baseline functionality. So if I want to write something that's going to be usable in the long haul, Lisp is what, Common Lisp is one of the the best solutions for that reason, and while Scheme is aesthetically beautiful and very kind of conceptually pure, Common Lisp, in my experience is the the one that you go to to really build things that work out in the real world. And I I really like its macro system and it's a, for real world applications, Common Lisp has been a great solution.

00:44:15 [CH]

This is a totally random question, but so I I'm a day to day in C++ and C++ also has a a bunch of compilers, but our names are very boring. They're just GCC, clang or C Lang, which stands for C language, the Microsoft compiler is MSVC, which is just an acronym for, I think Microsoft Visual C or C++. Uh, is there a reason for the very colorful like steel bank, armored bear, allegro? Do those come from something, are those backronyms like they just want it to be ABC or?

00:44:50 [AS]

Well armed bear is just ABCL, so they're just saying ABC, so Steel bank is called that because it came from Carnegie Mellon University. Andrew Carnegie was a steel magnate, Andrew Mellon was a banker. So that was its its name source. Clojure Common Lisp is just that. They were thinking of, you know, closures in the language. Embeddable common lisp is it is obvious. Allegro, I don't i don't know why they called it that it started out from a company called Harlequin I think, making a Lisp of implementation now it's Franz that produces that and the Franz, so you know something funny about Allegro Common Lisp is that when I implement when I tried it with April, it turns out that Allegro Common Lisp thinks that the arrow and the star and the other unique APL characters are alphanumeric. They match its alphanumeric tests. So I emailed them about this and they were like oops, that's a mistake. So I guess that no one has ever tried so the only things that don't match alphanumeric in Allegro CL are the common keyboard out non alphanumerics. Like the minus the plus. But anything literally any other fancy character from the box drawing characters to you name it are considered alphanumeric, so I don't know what they were thinking when they wrote that, but I don't know if they have a those proprietaries have a ton of users. The main thing that people use Allegro common Lisp for is the allegrograph technology, so they have a very advanced graph database with a search engine. That's all in Lisp and bridges to other languages, but, uh that's the main thing that their implementation gets used for.

00:46:39 [CH]

And this will be this will be my last because I'm hogging all the questions here but you mentioned Racket was, in your opinion, trying not to be a Lisp. Uh, is there? Do you want to share like a couple words on because that's the first time i've heard something like that.

00:46:52 [AS]

What I what I just recall seeing something about them wanting to move to a non Lisp syntax because parentheses are are hard for people.

00:47:02 [CH]

Interesting, I'll have to look into them.

00:47:03 [AS]

So I would have to look into that more. Listeners can do that research, but that's just what I recalled from it was that Racket is kind of the biggest Scheme right now, but that people were thinking maybe we should move to a different syntax.

00:47:21 [CH]

All right, we'll throw it to Bob and then to Adám, 'cause I think they both have questions lined up in the queue?

00:47:25 [BT]

My question goes back a little bit more to the history of listening history history of APL. 'cause Lisp I believe is based on Church's lambda calculus.

00:47:35 [AS]

Yes

00:47:35 [BT]

and in APL at the same time, was actually sort of an outgrowth of combinators, which at that time before I can't remember who it was, put them together, but somebody realized that Lambda calculus was just a different way of describing what combinators can do. But combinators are actually a simplified form, because you're not using your pointfree, you're not using variables. In that case, you don't have to bind all your variables. By putting April with the Lambda calculus and the combinator form together, what sort of things have you found out about those two ways of describing procedures?

00:48:14 [AS]

People will say that Lisp and APL are very different, but I find there to be deep similarities within the language and parallels that you wouldn't have expected. And Lisp is actually, lisp has actually been influenced by APL. Well, there was a long standing bug in one of its trig functions because of a missed transcription from APL, and I suspect that the Common Lisp array model was influenced by APL, because it's got the zero rank, it's got all it's it's row major ordering, so I suspect that the there's been a long standing cross pollination between the languages, and I also did a Usenet post where I asked why Dyalog does it's, I think it's arctan in US, in a way, and I received an answer from one from the the programmer who did the who actually pioneered that method [22]. And I'm going to see if I can find his name here...

00:49:21 [CH]

Just while you're looking that up, I can confirm that Guy Steele wrote a book called "Common Lisp the Language" and APL is referenced, I think like 8 or 10 different times in there, and I've heard talks from him where he says that APL definitely inspired Common Lisps in many different ways.

00:49:38 [AS]

So Paul Penfield [23] was the name of this person and he unfortunately passed away last year. But I received one of his last communications, probably when he clarified why, uh, APL Dyalog and some APLs handle trig functions the way they do. He wrote a paper on how to do this before the branch cuts were really finalized in Common Lisp and as well as J and other languages do it a different way so that he helped, he helped to clarify that, but you know, comparing comparing APL and Common Lisp, they're quite similar in how they in in kind of the model where you have operations enclosing other operations, like what gets is almost perfectly analogous to like the print function in Common Lisp, you can print something and then it will return its output. It will return it's output and to and pass it on to the next thing, so you can do like 1 plus quad gets a vector and it will give you one plus that vector and print it before. So getting deep into Lisp and APL, you'll find a lot of a lot of similarity, and that's helped it that that's made implementing APL Lisp easy, because a lot of the structures you find are analogous to each other.

00:51:12 [AB]

So, uhm, I found this to be kind of an interesting and closing circle type thing. Uhm, you mentioned, uh, something I I I think I'll have to correct you on that term about the original Lisp using something called M expressions. It's actually the other way around, and there's the reason for the name Lisp 1.5 is because the original vision was to go to something called M expressions and the S expressions was is like a more primitive form. This impression is what people associate with Lisp today: lots of parenthesis everywhere, and M expressions are actually something that people don't use this name very much, but they see it everywhere in every common programming language. It's the thing where you have the function name and then some type parenthesis or brackets, something and then a list of arguments to that.

00:52:09 [AS]

Yes, the so John McCarthy originally his idea was that Lisp his language would primarily use M expressions and S expressions were seen as a more primitive precursor. So when the APL, when the Lisps were implemented, they went to S expressions and mcCarthy said something like we thought we would originally, we thought that we would one day implement M expressions, but the M expressions were basically were basically pushed off inevitably into the future and ended up never getting used.

00:52:42 [AB]

Right, but that doesn't mean that i mean he he wrote things using M expressions, even though there was no lisp that could handle them. And with apparently envisioning that his his writings would be future proof because one day M expressions would be the thing and the the intermediary step S expression in part of the parsing would be, yeah, an intermediary thing, an old an old thing, but what I found is interesting then is there you see the similarities between APL style languages and and Lisp there's this, I think fairly amazing page on this website called kparc.com [23] which is just lisp.text. And we'll put the link to that, obviously, and it compares there's the FP languages for APL type languages, and uhm, including a timeline, it's it's written in in Arthur Whitney English, meaning it's very terse. But and it, and it it basically. Yeah, I mean the conclusion I make from it at least is that k is basically Lisp 2.

00:53:52 [AS]

k, well k was heavily influenced by Lisp in in it's it's kind of Lisp structures that it uses. So it's, uh, it's another example of the the kind of longstanding relationship between these languages.

00:54:08 [AB]

Right and then, and so that that brings me to the question, really so OK April is an APL or it's very specifically Dyalog APL, more or less in in Lisp. Maybe k would have been a more natural fit, or maybe it could be would be impossible to melt them even closer if doing k.

00:54:29 [AS]

Perhaps now something now one of the most salient features of k is that it is strongly typed down to the scalar value. So for Lisp doing scalar types is more complicated. Doing array types is simple. Arrays in Lisps are typed and April uses a lot of kind of type changing under the hood, you don't, you don't get exposed directly to any of it unless you want to manually work with types in April, but there's a lot of you know things use minimal types under the hood and then they get upgraded as necessary. April actually includes functions that let you find the type of an array and assign a type to an array. So for example, if you're making a PNG image, the library I use for that assumes that you are having an array of all 8 bit integers, so you can do, you can do 3 quad DT your array in April, and what that does is it it coerces it to an 8 bit array if you're going to do PNG images, so the number 3 can correspond to 8 bit array because two to the third power is 8, and then, if you're going to do a – and that's unsigned. If you're going to do a signed array, it would be 13, so 10 + 3 means 2 to the third power signed. But that's just kind of an example of the format that that quad DT function uses. And then as an aside, April includes a minimal subset of the quad functions that you have in Dyalog. Basically, the really important ones, but you can always add others if it helps you, using that interface I described which is you can read about in the APL in my APL paper.

00:56:19 [AB]

Stephen, would you really call k slash q strongly typed?

00:56:23 [ST]

How strong do you need it to be?

00:56:25 [AB]

I don't know, Andrew was saying this.

00:56:27 [ST]

To oversimplify, which is, which is my special subject in APL, you you can pretend you just got two data types, text and numeric. And in q we have three types of integers, symbols, characters.

00:56:50 [AS]

And the and the symbol thing is also a definite influence from Lisp. There's not a lot of characters that have the symbol type, and Lisp is one of those, and Lisp uses them to an even greater extent than k. They're used in the in the macros. Where you meta program. Yeah, that's something that at some point I may look at introducing into April. But then you were talking about, you know you can pretend you only have a couple types in APL, and it's a little different in April. So here's one of the differences you know arising from the compiler design. So in April there is a more definite distinction between floating point numbers and integers. For instance, the complex numbers in Dyalog and other APLs i don't think that there's any other that has complex numbers with any other type of part than floating point in Dyalog. Your float parts, your complex parts are floats in April. Your complex parts can be either floating point or rational, and April supports rational numbers which are, it just inherits those from Common Lisp. I don't know if I could have implemented them otherwise, but the rational numbers in April, they're printed with an R as the separating the numerator, the denominator. So if you do something like division sign IOTA 5, you'll get one, one half, one third, one fourth, one fifth. So those numbers rationals are only really useful if you have bignum support in your language, which Common Lisp does, and they can be quite slow to process, so you have to be conscious about using them, but the important thing is that they're there and you can have complex numbers with rational parts. So in the way that April prints complex numbers is it will it will not print, you know .0 of anything if they're not floating point and April will only print a number that's actually internally afloat with decimals. So you need to be a bit more aware of that distinction when you're using April. This is in contrast Dyalog and other APLs, but this is is necessary because April April is more porous than the other APLs. You can easily process its output with outside code and the mentality that goes into most APL's is we don't want the developer to have to worry about whether something is a float or an integer under the hood and often things will be printed like floats or coerced to floats. For instance, if you if you have a an array made out of if you have of a row of a column of complex numbers, and actually complex numbers always have floating point parts, but in April you need to be a bit more aware of the type of numbers that you have, because when you can pass them out easily into Common Lisps and work with them, there's important distinctions between the floats and the integers in that outside code.

00:59:56 [AB]

Have you had a look at the NARS 2000 at all?

00:59:59 [AS]

I haven't. I know that it has I know that it has rationals, but I haven't looked at it.

01:00:06 [AB]

It has rational complex numbers as well.

01:00:10 [AS]

OK, yeah so.

01:00:10 [AB]

If you if you tell if you tell that so in APL and J as well, uses a J delimiter between the letter J delimiter between the real part and the imaginary part. So if you say it for example in in NARS 2000 using the R like like you've described as well. So if I say 2R4J3R4, so that's two quarters, real part and 3/4 imaginary part. It will respond back one or two J 3 or 4. So it simplifies the 2R4 to 11R2, so it's using rationals the complex numbers.

01:00:54 [AS]

Exactly and and April will do the same thing.

01:00:57 [AB]

Right, it is not.

01:00:58 [AS]

So I haven't gotten into NARS 2000 because it's Windows only.

01:01:03 [AB]

It's supposed to run on on wine I think, but yeah.

01:01:07 [BT]

So Andrew, did you ever look at J for for this? 'cause when you're describing the the rational numbers and extended numbers big numbers, J has all those and actually sounds like it implements in the same way and does distinguish between those different types.

01:01:21 [AS]

Yeah, I've, I've looked at J a bit, so I recall the Eric Iverson podcast. So I'm going to weigh in on the controversy myself, and I'm not a big fan of the J approach. And to me the the strong point of APL is it's it's a notation and going back to Iverson's paper notation as a tool of thought. The advantages of a custom notation are manifold, in my opinion, compared to ASCII, and that's another reason that I'm excited about what Marshall Lochbaum is doing with BQN because he's pushing forward the development of new notations for programming languages and dealing like for k, I think k is about at the limit of what you could reasonably do with ASCII, because k is just a vector language it doesn't use the higher ranks doesn't have those functions, and even even k has overloading to the point that it can be very daunting to understand. But when you get to J, you've got your period and your colon system, and I can't like, I  just can't process it as easily as I can APL looking at these combined symbols.

01:02:42 [BT]

So it's a notation as a notation that is the issue you have with it, not so much the ways it's structured in terms of what it's doing with the different functions.

01:02:52 [AS]

Now the well the other thing about J is that it follows an approach of using operator like using a lot more operators for things as opposed to axes. And I'm a big fan of axes and actually my axis paradigm is a bit different from how people consider axes in APL, like APL considers axes to be an operator. That's how they're described in the doc. I consider axes to be another type of argument or parameter to a function or operator. They're a way to step outside of the one dimensional APL paradigm where you have things on either side with with operators you can, with axes you can add another, as opposed to just the two.

01:03:39 [AB]

Yes, OK, so can you just with an operator, right? An operator can take an operand which can be an array.

01:03:45 [AS]

Yes, operator like their default is to just have things before and after. But operators also kind of let you step outside, I see what you're saying there, but in J like I was saying, the idea is have operators for everything like there's operators that that implement a comparison tolerance, and some of those things, that you might assign local variables and reading some snippets of J, it took me a long time to kind of wrap my head around, oK, so they're doing a comparison tolerance here and to me it balances the kind of the balancing decisions in the language we're taking in, we're taking in a different direction than I would have favored, so I'm more a fan of the APL model and the APL way of doing things. It it just it just clicks with my mentality better than the the J approach. So the APL approach is is what I favour and my evolutionary direction for APL is going to be going in the direction of first class functions and doing doing some some things on my own in terms of what I call lexical statements like, I've got the APL if statement in there, and it's more flexible than a guard because it allows you have multiple statements inside a clause. Guards you can only have multiple statements in the final clause so it's more like the if statement in Dyalog, but it's it's more APLish than the control statements.

01:05:17 [CH]

This conversation ties perfectly into a question that I was going to ask 'cause you mentioned I think in in the history part of the conversation earlier that you first found out about k and kdb, and then were a bit confused by the syntax and so you went up the lineages tree and found the sort of root language APL. And then you ended up eventually implementing April, AKA APL, in Common Lisp, and so you've been talking a bit about j versus APL, and you did a little bit about k versus APL. But is there anything more to say? I think you mentioned that you know the overloading was can get a bit confusing because they do it quite a bit, so it's not just once or twice. But you know, there's a bunch of different contexts. Was there other things about k that ultimately led you to choosing APL? Or is it just that you ended up liking that model better?

01:06:03 [AS]

I like being able to work with high rank arrays. The uh, you know my my, you know one of my friends says that k is k is more practical. APL gives you basically every option, but k gives you the most important things, but I prefer the the higher power of APL. The fact that you can work at any rank, and I've used it to do some remarkable things in modeling things like the Bloxl display. So for instance the Bloxl display is modeled as a four dimensional array, so you have the main display dimensions, so for our big blocks, well, that's 10 by 20 blocks, so that's a 10 by 20 array. And then you have a third dimension, which is 4 because each block has four subpixels inside it and then each of those subpixels has three elements to its color, red, green and blue. So it's a 10 by 20 by 4 by 3 array of of 8 bit integers. So doing that I can use, 'cause I can expediently address every you know, just using those axes and lighting axes, I can address every red element in one row and just gives you all that flexibility. So that kind of that kind of flexibility and the brevity, and the fact that when I see those rotation characters of those shapes or in alpha I know exactly what it means and I'm not, you know, going over in my mind wait, the the the exclamation point means this in Perl, and this in C and this in, oK, you know there's none of that. There's none of that overloading of ASCII characters. You see APL characters, you know what they mean, right?

01:07:54 [CH]

That's really, that's really interesting, I think to hear, because not often or maybe often, but maybe we just don't ask it or it doesn't come up. Do we have people that have looked at all of J, k, q, APL and a little bit of BQN as well that are able to offer that kind of what's their preference? Or you know what are the differences? So yeah, it's super interesting to hear that. Are there other questions from the other panelists before maybe I hop into the potentially what could be last question we still got 10 minutes or so? Or should I ask away? Stephen?

01:08:26 [ST]

Andrew, back to your New York presentation you during that you kind of commended the learning of APL on three different grounds that I picked up. One of them was efficiency. Where and when you were showing your blocks or display you you were saying I couldn't get this kind of performance in in in Brand X languages. That kind of surprised me. It reminded me of something that Arthur Whitney had said about k in the British APL Association's 40th anniversary celebration 2004 that was, he said k routinely performs, outperforms hand coded C, and of course that's theoretically impossible because every k program compiles into C, so there is a for every k program, there is a C program that's equally fast. The reason why it's so often true in practice is that it's a lot easier to see your errors in four lines of k than in 400 lines of C, so i, I guess in the context of that, would you still stand by your efficiency clamp?

01:09:53 [AS]

Now let's now a word about efficiency. I think I may have meant it was more efficient to write the, it was I could more efficiently write and create patterns in APL, so I can, I could do anything imaginable with pixel graphics in just a few lines compared to if I was writing dozens of nested loops to do that. So my my just my line about efficiency may have concerned that but, if you're going for absolute efficiency, then I mean really you should be writing in assembler or FORTRAN, but the question is, how long will it take for your brain to burn out trying to write large, sophisticated array transformations in those languages versus APL? And the thing is that C compilers will often produce faster code than people who are writing hand coded assembly. If you had a team of assembler wizards working on every function for a year, you could probably get them faster than anything in C, but C compilers can take the aggregate knowledge of developers and apply those to optimizing the structures they produce. And the same thing goes up the abstraction train to languages like APL. So obviously a lot of work has been put into special code for APL and April also has a special code system. You can see it in the file called patterns.Lisp [25] in April main repository. We can link that. And it has a pattern matching system where it recognizes things like let's say that you're doing disclose ravel or disclose rotate ravel of an array. So you're taking the last row major element in that array if you interpret that literally, it's incredibly wasteful. You're producing a raveled structure just so you can end reversing it just so you can take the first element, but if you if you just, if you recognize that pattern and you compile it to, you know, just take the last real major element, then it's very fast, so that's one of the things that I detect in my pattern matching. And it's also a hassle to write parallelized code. Does parallelization of just about everything that it's possible to, except operators at this point I need and I need to write an accounting system to check whether an operator produces side effects in the function given to it in order to properly parallelize those with no risk that there will be a side effect that's out of order. But, uh because you've got this inherent parallelization. And then there's also the possibility I mentioned of doing downstream compilers. Practically speaking, you will get, you can get higher performance out of an APL, now reminding everyone that Dyalog is still much faster than April Dyalog has had a 30 year head start. But April has a robust framework for doing multiple kinds of optimization, and that's what's going to make a difference in the long run. But in terms of efficiency, it you know what really counts is how fast you can get an efficient program written and by leveraging the you know the power of computers as a labor saving technology, we can make the, we can, we can get the, we can create more efficient output using the computer to recognize patterns than we could if we were writing a FORTRAN or assembler programs by hand.

01:13:40 [ST]

Thank you. You mentioned two other, uhm, reasons for paying attention to APL you spoke I, I think of what I call code management about the about APL permitting you to write what would otherwise be lengthy chunks of code, special customizations for blocks, or for example in just one or or a handful of lines, and as a result, these these special customizations didn't bloat out the main code base and and lastly, and I think you said least about this, but I really invite you to say some more, you were suggesting that a lot being learning APL, allowing to solve problems in APL would change your thinking, and I infer it in other programming languages, other places you you developed.

01:14:36 [AS]

The lesson of APL is that you can consider entire bodies of data at once and in like, obviously in most languages to do the things you do in APL, you need to write dozens of nested loops, and that takes you away from from the problem itself. It forces you into this lower level of thinking and also creates opportunities for error, so I'll take this chance now that we're nearing the end to expound on some of my programming philosophy, so talking about how it changes your perspective, I spoke to a C developer a while ago who told me the, you know, the really hard thing in programming, naming things, that's the main challenge is naming things. What I take is the true challenge in programming is creating balance. It's balancing the factors in your program. Now, C only allows you a few degrees of articulation and the reason that he thinks of naming as the challenge is that naming everything and creating a namespace for everything is one of the only points of articulation that you get in C, so you create these giant long names like table interface template, module specification and stuff like that. Now Lisp gives you more points of articulation. What Lisp allows you to do is change the behavior of the compiler so that when it encounters a certain form a certain symbol, it will expand the form to another form before evaluating and Lisp also gives you control over read time so that when the reader encounters certain characters, it'll carry out special behaviors so this will give you 2 points of flexibility that simply don't exist in other languages. And although I have heard of people working on macro systems for vector languages and again to understand what this means, just look at spec dot Lisp in the April repository where you can see all the APL functions laid out. So having that degree of flexibility opens up great possibilities for programming. And it also gives you thousands of new, exciting ways to fail. You need to you need to write Lisps. You have to conceptualize multiple points along the timeline. You have to understand what happens at compile time and then what happens at runtime. And if you're using reader macros, you also need to know what's going on at read time with those macros. So if you mix up any part of this you're going to have very mystifying bugs. So if, uh, that that balancing act is where APL comes into play, and adding April, the mix of Lisp gives me balancing possibilities that didn't exist before. I can go from the more verbose Lisp format into the ultra tourist APL format and suddenly do things that Lisp didn't enable me to do. So when Lisp I do, I think I think semantically, and I think logically now recall I was originally a writer and I may approach programming in a way that's different than most people, because when I program, I think in terms of creating patterns of meaning. It's a it's like a a prose that that that informs a a computer process. So what APL allows me to do is switch into a complete other mode where I'm suddenly operating on entire bodies of data at once and distilling distilling algorithms down to their very bare element. And that gives me a just another degree of flexibility, but it all requires balancing and and being aware of what's happening within the program.

01:18:23 [CH]

I think there's no better way to end it than than on that note, and as we wind down, I should mention because we should have announced this at the top of the episode, so hopefully our listeners stayed to the end 2 weeks from today where today is the recording date and it's actually more like 9 or 10 days from the actual release date or less than that depending on when you're listening to this, APL Seeds [26], which is the 2nd edition of that conference, will be taking place on March 29th and Andrew is going to be one of the speakers there. So on top of him having a presentation with you know visuals along with audio as you only get on this pod. First, I think he might be sticking around, you can confirm or deny Andrew to the live recording that we'll be having at the end of that conference. So if you have questions either for us or for Andrew, you'll be able to stick around to the end and ask them, and I will save my last question that I had for Andrew for that or a you know another recording in the future.

01:19:18 [AS]

Yes, I will be at 8:00 PM at APL Seeds and I will also be presenting at the European LISP Symposium on the 21st of this month and my paper there is an introduction to that presentation so that paper again is linked for all who would like to read it, and it's for an audience of Lisp developers, but it's got some fun bits of APL code in there, like there's a snippet that you can use to make a fun pattern that it takes multiple iterations of the game of Life adds them up and then builds a character matrix out of them so that and more will be featured at that presentation.

01:19:56 [CH]

Awesome, so if you're listening to this in the month of March in 2022, two different opportunities to tune into Andrew March 21st the Lisp Symposium and March 29th at APL Seeds. Thank you so much Andrew for taking your time to come and talk with us. This was a blast. We got to dive deep not just into APL, but a little bit into k&J and also into Lisp and the different dialects of Lisp, so yeah, looking forward to chatting with you again in T minus 2 weeks.

01:20:21 [AS]

Yeah, anytime Conor, Bob, Adám, and Stephen, thank you so much for stopping by today.

01:20:27 [CH]

Awesome, and with that we'll say happy array programming.

01:20:30 [All]

Happy array programming.

</details>
