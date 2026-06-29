---
title: "Episode 5: Responding to a Listener's Email"
date: 2021-07-10 00:00:00 +0000
episode: 5
buzzsprout-id: 18621527
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
  - "/episodes/episode-04-responding-to-listeners-email"
  - "/episode5-show-notes"
  - "/episode-4-transcript"
---
<!--more-->

**Host:** Conor Hoekstra

**Panel:** Nick Psaris, Richard Park, and Bob Therriault

---



<details markdown="1">
<summary><strong>Transcript</strong> (click to expand)</summary>

Transcript

Transcript prepared by Rodrigo Girão Serrão

Show Notes

00:00:00 [CH]

I'll probably read some version of it like plus slash divides tally iota ten. That's easy enough, and then I'm not going to go average paren paren zero dot ten paren dot collect colon colon angle vec angle underbar angle angle paren paren paren.

00:00:13 [RP]

Yeah, APL is definitely more pleasant to read aloud.

00:00:17 [music theme]

00:00:28 [CH]

Welcome to another episode of ArrayCast. I'm your host Conor, and we're going to quickly go around and do brief introductions. We'll start with Bob, then go to Nick and then go to Rich.

00:00:36 [BT]

I'm Bob Theriault. I am a J enthusiast and I've been programming in J, coding in J for coming up on 20 years and I am not a professional, just enthusiast so take what I say with a grain of salt.

00:00:54 [RP]

I'm Richard Park. Uh, I work for APL vendor Dyalog. I actually didn't know what APL was before I joined Dyalog, but now I love it so much. I teach it to other people. That's my gig.

00:01:06 [Nick Psaris]

Yeah, I'm Nick Psaris. I'm a quantitative developer in finance industry. My weapon of choice is q and kdb. I've been using it since 2006 and I also also teach a course with using q as the main main tool at Carnegie Mellon University.

00:01:26 [CH]

And, as briefly mentioned, my name is Conor Hoekstra. I'm your host and by now you probably know I'm, I'm not an APLer or a J-er or a q-er. I'm a C++ professional developer, but I have a huge passion and enthusiasm for the array languages, so doing these podcasts it's absolutely awesome. I get to ask the questions and get all the answers before all the listeners do, so I think we have two announcements off the top of the episode. I'll kick that over to Bob and then. We're going to hop into reading some feedback that we actually got from a listener, and we're going to read that sort of a couple paragraphs at a time and respond to that, which hopefully should be a great conversation. But first, Bob, we'll start with the announcements.

00:02:03 [BT]

Yeah, starting off kind of well, definitely sad news. Jean Iverson passed away and Eric wrote this message out to the J forums. It was, I thought really well put so I'm just going to read it out. I think it. It covers things quite well. "[Jean Iverson](http://www.jsoftware.com/pipermail/programming/2021-June/058312.html), 1925 to 2021. Jean Iverson passed away peacefully on Friday afternoon, June 25th, 2021, in a Toronto hospital. Her children were all able to have good in person visits with her during her last days. She had a full and wonderful life and will be missed. If Ken was the father of APL and J, then Jean was as important as a mother. She worked tirelessly alongside Ken proofreading 'A Programming Language' drafts and galley proofs, every APL character that appears in the book was meticulously drawn by her with a K+E Leroy set with a custom APL template and then, in parentheses, 'First tech stab at the APL character challenge.''. Then in the late 80s, with Ken and Roger joyously working on defining and developing J in Ken's Home Office, it was Jean who kept them fed and forced them to take breaks and even occasionally go for a walk. Those were some of her hobbies. Her true calling was helping people, especially young people, find their way and a path to a good life.". Again, she will be missed and our thoughts go out to the Iverson family and friends of Jean. It certainly sounds like a very well lived life and I'm sure a lot of people will miss Jean.

And on a certainly happier note the other day, there was the British APL Association AGM and during that they are going to strongly investigate digitizing all the old editions of vector and making them searchable on the Internet. And so if you have a hard copy, good for you. But in the future, we will be able to do searches and actually pull back some of the the very early articles out of a vector, which will be I'm. I'm really looking forward to that.

00:04:23 [CH]

Yeah, so I think they're announcing the digitization, but we'll we'll keep listeners updated when that actually starts to come online and people can check that content out. All right, so let's let's hop into this discussion. So we got a really thoughtful and long email from an individual named [Daniel Sockwell](https://www.arraycast.com/episode-4-daniels-email) and we're just going to read through it. It's in response to the episode we did earlier on the challenges that face array languages, and so we're just going to start off. I'm going to read the first couple of paragraphs, and we've inserted a couple breaks. And then we're just going to chat about. Sort of, you know, just respond live to this to this feedback that we got. So here we go.

"Hi and thanks for the ArrayCast. I greatly enjoyed your recent 'what challenges face the array languages' episode, but I have a fairly different take on why APL family languages aren't more popular, at least from my perspective. As someone who got very excited about APL but eventually decided not to pursue learning the language further, here's my APL story. I'd always heard about APL. I think the first I first encountered it in the novel "The wizardry consulted" where it was used as a language that puzzled dragons, but I didn't look into the language closely until I encountered some of Aaron Hsu’s writing/talks about how APL enabled concise expressive code, what Aaron and others wrote about keeping the cost of rewriting code as low as possible resonated deeply with me and I decided to investigate APL. Seriously, during my initial deep dive, I realized that Aaron and I actually lived in the same small town and that coincidence inspired me to send him an email, we ended up having coffee, which I thought would be a short chat, but turned into a multi hour talk with Aaron where Aaron thoroughly convinced me of the virtues of APL. My biggest takeaway from that talk was that the fundamental task in programming is to attempt to solve the impossible problem of leaky abstractions. Most languages take the strategy of trying to make abstractions as non-leaky as possible, and as a then-Rust programmer, I recognize that goal in many of the language design choices in Rust, but there's another way to solve the problem. Recognize that all abstractions leak and write code that minimizes their number. Compare the two following expressions, the first from APL –which I will attempt to read out, which is –plus slash divides tally, which is a fork, next to iota 10; to the equivalent Rust expression, which roughly is average of zero to 10, collect into vec. The advantage of the APL code isn’t just that it’s shorter, it’s that the APL expression removes a level of abstraction. The APL code is all right there so you can check for any edge cases or bugs. No abstraction, no leaks. And because APL is so concise, defining average is literally shorter than calling it in any other language. It facilitates this abstraction removal over and over again."

And this is where we will do our first break. I think well kick it to Nick ‘cause I know Nick has prepared some notes and got, has some direct feedback to what we just heard.

00:07:08 [NP]

Yeah, sure, thanks. I I don’t doubt that the array languages reduce the number of abstractions, and that definitely makes the languages very appealing to everyone to use, because you’re not kind of wondering what’s happening under the hood. It’s all there in front of you. But I think, I don’t want to oversell the languages because there’s always some abstraction under the hood, that you end up needing to know once you dig a little bit deeper, and many of those are, you know... For performance, if everything was an array, hm, you know you’re hindered –and we’ll talk about that a bit later –so you need to understand the implementation in some sense in order to get them the maximum performance out of your code. The first one I want to mention is that you know, if you have a matrix, the reality is, it’s either row-based or column-based, and if you wanted to sum, for example, all the values in a matrix, you could either first sum all the columns and then sum the results of that, or you could sum all the rows and then sum the result of that; and the actual memory layout under the hood makes a difference on which one’s more performing. So in q, for example, every it it, it looks like every row is a vector and so if you were to want to sum the values in a matrix in q, the most efficient way to do it is to sum each of the rows and then sum the result of that, because if you were to sum the matrix, if you just say “sum M”, or if capital X was a matrix, you would actually be summing across the rows, which is not very memory efficient. And then you would sum the result. You could do it either way, but knowing the layout of the data structures inside the language really helps you know which is the most, uh, more efficient way of doing that. Hm, perhaps J and APL can respond to is there a more efficient method for summing values in a matrix?

00:09:14 [RP]

Well, we’ve got in APL, and J I think, these high dimensional arrays that are represented with the shape and then the ravel of all the data. So, I mean, what you’re saying? We would probably do plus slash comma in both J and APL, well, which is to ravel it first and then, I don’t know how far to go with this because it is this question of like, to what extent, so in Dyalog we have these idioms, but they’re like, a bit restrictive in that there are specific sets of tokens that are recognized by the interpreter and then some special code will run that. Like, is there some perfect language ideal where the person can just write whatever they thought of and then the interpreter or whatever will just do the most efficient way to get that answer, which obviously is what you’re saying is not the case, and that is true. It’s not the case in any of these languages, right? You do need to know something in terms of memory layout or the speed, yeah. Beyond the fact that because it’s all raveled, so the memory is all contiguous, then that’s a really fast access pattern for memory, so that’s going to be relatively fast, but I don’t have enough experience across the languages to know whether the semantics of like a vector of vectors or this contiguous matrix where it really is beneficial or not.

00:10:35 [NP]

Thank you. If you were to do what you’re suggesting, you know, with the comma, it would be called raise in q, you’re actually changing the memory layout. You would back, you know, you’d take a bunch of distinct vectors and just start appending them to the end of each other and that would actually just reallocate all the memory, it would be very painful. And that’s kind of why I suggested first sum over the rows and then sum over the resulting values. I do see what you’re saying, how in APL and J, if everything is already in a data structure that the data is all appended to each other, you just sum over everything. And that’s very efficient.

00:11:12 [RP]

I mean, that’s also very specific to this exact problem that you’re describing, right? Where actually actually when you have lots of these, I don’t know, it’s like... Creating your own abstractions, I guess. Or your own sort of representations or data type. They’re all based on arrays, because APL and J, these array oriented languages, you are generally trying to balance in some way the expressiveness of your particular representation for that particular domain. Like you know, the code just looks really beautiful, or it’s really easy to see how it’s working, so therefore you can modify it. But then sometimes, when you do that, you’re actually working with the not-so-efficient representation. The most obvious one that comes up in modern APLs with like either boxed, as in J, or whatever nested array system you have, is that you’ll have some really neat little idiom –you see this a lot in the code golf competitions –that’s a really neat way of getting some result, but you’re acting on nested arrays, which means that your actual under the hood implementation is having to chase a bunch of pointers around and then you go and you dig up, I don’t know, old Vector articles or APL quote quad or something, and you find from the 80s or whatever, someone has been doing this type of stuff, but back then they didn’t have nested arrays, so there is where you can find these, like, specific flat array techniques that end up improving your performance, but they are kind of esoteric to the world of programmers at large and domain experts and stuff like that, so it’s that kind of awkward balancing act a little bit.

00:12:53 [BT]

And with J, a lot of it is, at least the way I’ve approached it, is that the [idioms](https://www.jsoftware.com/help/phrases/contents.htm) that you use are the common ones, you sort of rely on the fact that those have probably been optimised to a fair level. You know that’s the consistent people working on that, but when you get to the point where you’re trying to get performant, that’s when special combinations come in. And if you really want to get a higher level of performance, you go into NuVoc. You start reading about special combinations and certain ways of putting verbs and conjunctions together, that have had code written for things like in-place so you don’t have to worry about swapping your memory, backing out if you do certain combinations, everything will be done in-place and it’s done specifically so you wouldn’t have to go out of place. And the code has been written to be able to take advantage of that, but it doesn’t do it every time, you have to use a [special combination](https://code.jsoftware.com/wiki/Vocabulary/SpecialCombinations://). I want to go back to what Rich was saying about “wouldn't it be nice if you could write what you wanted to happen and have the the code figure that out and do it for you in some sense?”. SQL on databases attempts to do that for you, right? They have a query optimizer behind the hood and when you type your query you don't need to know in principle which of the columns have the most unique values, where the index is applied. But in practice the reality is that you, if you know the structures under the hood, then you could write more efficient SQL and the same thing applies with q. The important part about q is, it has an SQL layer on it and you can type your SQL thinking that I don't need to know about the data structures under the hood, but that that abstraction is leaky. You need to know the fact that dates are partitioned on disk. Maybe the SIM column has a uh, partition attribute on it and and. Things like that. So the order of your where clauses where if you came from a normal SQL, you could put your where clauses in any order you want and the query optimizer would take care of that for you and q/kdb you, yourself are the query optimizer and you need to know how the data is physically stored on disk, and so there's abstractions, right? To to write quality performant code, you need to know about what's under the hood.

00:15:16 [CH]

I guess it also might be worth just pausing to to. We've been using the words ravel and raise, and everyone that's, I think, an array programmer’s keeping up, but there was a point where I had no idea what either of those meant. So do we want to briefly just mention what raveling a matrix is or what raising a matrix is?

00:15:37 [NP]

Oh yeah, and and include the. The term raise is, uh, if if you had a uh, if you know let's say you had a tensor, an array of rank five it's and you call raise it just removes one level of nesting and so you would end up with something of a rank 4. We rarely use data structures that are that deep, and so the typical example would be you have a 2 dimensional matrix you call raise on it. You end up with a vector. Uhm, and that's pretty much the standard. I mean, when you do it with dictionaries. If you have a list of dictionaries and you raise it. It'll try to concatenate them all together. If you have a list of tables and you try to raise them, you'll end up with one table with all the tables joined to each other. So you can do it on things other than matrices or vectors. Another example of when you might want to use it, although I don't find it the right way to use it. If you have a function that wants to take an atom or a vector, it can apply equally to both of them, but you want to make sure that what the person pass into you is always a vector, you can call raise on an atom and it'll turn it into a one element vector or list one element list. Uh, personally, I I prefer to just append an empty list to that value and that will turn anything into a list, but I've seen a lot of code that raises whatever comes in just to make sure it's a list.

00:17:02 [RP]

Yeah, I think it's best not to get too deep on that particular caveat, 'cause it's different in all the array languages and like it gets weird in some of them like Dyalog, scalar extension. Oh sorry, Singleton extension, right? Whereas, not like a one element vector and a one element matrix are kind of treated the same in certain circumstances and it's kind of useful most of the time, but sometimes it bites you right in the rear end and it’s just, yeah...

00:17:29 [BT]

In J the ravel would be used on an unnested or unboxed matrix, and raise is actually a different, it'll take any box and basically flatten it so you can have any structure of boxes and when you raise it you open up all the boxes and put it in one flat line and it's pretty powerful, but that's how you do it, right.

00:17:53 [RP]

Is that true in in k and q that like depth is rank or they kind of become the same thing in that model rather than the separate that you have in J and APL?

00:18:03 [NP]

There's only lists. There's only a vector like there's, yeah, you you would nest they they are nested in order to get multiple length you need to nest the structures themselves. Then it's it's required.

00:18:07 [RP]

Right exactly.

00:18:14 [CH]

In general, we should just know that there's raise, ravel, enlist, all across the languages and they all have to do with like unraveling a certain amount of structure. Whether that's all of it or a single level, you know, reach for one of those three. And yeah, Nick we'll... Yeah, we'll kick it back to you.

00:18:29 [NP]

I did want to say one more thing before we continue with with the the letter and that's I guess in some sense about reference counting in in at least q and we can talk about J and APL. When you have a table so all all data structures are reference counted and things are passed by reference to all the functions , but if you get a vector passed to your function, you're not copying the actual massive vector into the function. You get a reference to it, but then you actually don't need to fear of modifying that vector. Let's say you add a row to add an element to that vector. What ends up happening is that vector gets copied. And the in the in the method it seems it called copy on write everything passed as a reference until you try to modify it, and as soon as you modify it you get a copy of it. And this is very different than in Python, where when you pass in a a list to Python, if you modify it well, the the vector itself that was passed in it gets modified it in the calling function. And that's very tricky when you're not expecting it. In q you can be unconcerned about passing a table into a function. If someone does anything to it, your table is still still the same, although you know there's obviously going to get a performance hit if it's copying the whole table within the function. But those those semantics about how memory is managed, the fact that it's copy on write, you know it's memories in abstraction and you need to know what's happening there in order to make again performant code and correct code.

00:19:59 [CH]

Is that the same in both? I think J I've definitely seen has the same model. I'm not sure if you can confirm or deny Bob.

00:20:06 [RP]

I know that Dyalog, I mean that that is a, uh, an abstraction, but it's also like this weird, I don't know what to call it, semantic difference or whatever...

00:20:15 [CH]

It's a pattern.

00:20:19 [RP]

More like the end. Like me. The user of APL. From my perspective, the arrays are passed by value like you said. Like you can assign one to another name and then it's only you know when I modify one of them that the actual copy happens underneath. So I don't. I don't think about that that much, but you are right that if I was concerned about performance, I would.

00:20:39 [BT]

And and in J that comes down to what I was talking about in special code in place. And things like that will be done in a slightly different way than maybe it would be done if you weren't using the special code so that you can make changes and it well. And then there's I guess there's this other thing to introduce. Even more, there's memory maps as well, so you don't even have to, and then there's I guess there's this other thing to introduce. Even more, there's memory maps as well, so you don't even have to, you can go straight to the disk and pull memory off that, and then you're actually changing the memory on the disk. If you change that, so that's real real reference. You're going right to the right to the disk to do that, and you change things there. You change them everywhere so you know. Yeah, it's an abstraction then. You definitely have to be aware of it before you start playing in those areas, because there be Dragons.

00:21:23 [CH]

So to pick up where we left off, the feedback goes on.

“To say, put simply, I was sold and greatly enjoyed solving Advent of Code puzzles in APL, frequently with a solution that would fit in a tweet or in my case, toot, since I use Mastodon rather than Twitter. So what pushed me away from APL? I still believe in the power of everything Aaron and I discussed, and I still think that reduced abstraction enabled by concise code is a programming superpower. But despite all that, three things caused me to give up on APL, none of which were squarely addressed on the podcast. Poor integration with Linux/free software. This is related to the point, Nick started with about sharing code, but I have something much broader in mind. After writing enough APL to get serious about it, I decided to set up my environment to support writing programs with a broader scope than solving Advent of Code puzzles. One of the first steps turned out to be surprisingly difficult. Writing a simple program that reads from standard input and prints to standard output. The Dyalog docs have far more info about connecting APL to Excel than about using it with a terminal, even though I think that the latter is as the bread and butter of programming in the Linux environment. With some help from Adám and other saintly members of APL Orchard, I was able to get that working. If you're reading this Adám, thanks. –I think he definitely did read it –, but it was clear that integrating with normal Linux server tools that are part of my standard workflow AKA Unix, TCP sockets, Emacs, nginx, and other servers, terminal emulators etc would be a recurring challenge. As someone deeply committed to the free software FOSS ecosystem, being siloed like that, it felt like a much bigger challenge than just not having a package manager”

So we'll pause there. And whoever wants to kick it off can kick it off.

00:23:03 [NP]

Yeah, I think that, integration with you know. Well personally I use Emacs for everything my whole life, uh, and that that lack of integration pushed me to building an Emacs mode for q. When I was looking into J and APL, it turns out there are Emacs modes for them as well, and I think they're all, they're all available from either ELPA or MELPA. So that integration, if it turns you off, it's definitely there. One step that I know that I've built in mind is you the the REPL is great and you can use the up arrow to kind of pull back a previous statement. But what I find actually even more powerful is the ability to write code in one buffer and then send it into another buffer to for evaluation, so you don't have to. Actually you can have all your code. You can highlight what you need and evaluate it. In addition, q has the ability to connect to a running server and inject code in that way as well, and so from within Emacs you can write code. You can evaluate it and it evaluates it on a remote server, and that iterative process of development, I think is just unmatched in any other experience that I've ever had. But going back to, you know, integration with Linux and free software. He also mentioned the fact that he was having trouble to pipe the data from one process in, uh, you know a J or APL process and then pipe the result of that into another process. Originally speaking, that was definitely a problem, at least with q. The subsequent versions of it added the ability to read from standard in. Now if it's going to read from standard in, that's also where the REPL comes into play. And so either you can send data through the REPL. Or you can pipe it in from from another process and the fact that you can't do this both at the same time makes, you know, writing the code a little bit more confusing I I would say, but you can read from standard in. One thing I'd say, however, is that because, uh, you know, q likes to read things all in one chunk, you know you want to read a whole file. It comes in as a CSV, but when it gets into q, it's now a table, right? That's like one operation. It's not a streaming language. If you were to write similar code in Python, you would open and read standard in and, uh, process every record one at a time and then send the result out to standard out one at a time and that kind of fits along with the model of piping one process into another process. This is not the fact that q doesn't stream in that sense, and you could write it that way, but it's a lot more confusing in some sense the code the fact that it reads in all in one chunk and then spits it out all in one chunk kind of ruins the the streaming aspect of what you are actually doing. For for very massive datasets I do understand how you might want to do that, but since q really efficiently does things all in in one chunk, it it never really, for me at least, has become a benefit to write piping code from one process into another. The other thing is, in order to treat q scripts as a process that run just like a Perl or a Python script, you would want to be able to put the [shebang](https://code.kx.com/q/develop/shebang/://) line at the top of the code. I rarely see it, but it actually is supported and if it finds the the q binary as the first item on the first line of the code, it will start the process with that so that that all works.

00:26:44 [CH]

Rich, Bob, do you want to comment? I feel like Bob, like we actually chatted about this briefly right before started recording, is that you know this in particular, issue that he's bringing up. I feel like J maybe has made a lot more progress in this area compared to. I know I think specifically. He's responding to APL. But yeah, I think J J’s done a lot of work there over the years in terms of that, it’s like, open source.

00:27:08 [BT]

And J actually has three interfaces that you can choose from once the [console](https://code.jsoftware.com/wiki/Guides/jconsole://) which is your console line, there's a number of people who only work from that. There's also a web based IDE called [JHS](https://code.jsoftware.com/wiki/Guides/JHS) and that's basically, it hooks up you your your J core to JavaScript and so JavaScript takes the interactions and your all the movements of the clicks. All that kind of stuff is handled. And then when that information comes in then it's handled by J. And that's the answer is replied back out to the web page. So essentially you're running J on a web page, but you're running your J right next to JavaScript, so it's actually very strongly ontegrated and in fact I wrote an application that can take a noun and it displays it and includes a lot more information you normally get from the text based feedback that you get from J. And the way I did that was I basically wrote an SVG file and then wrapped it in an HTML and pop that on and I'm doing the display that way, so there's a very strong attachment between the web and and J in that sense, and then the the third one just to be complete is [JQT](https://code.jsoftware.com/wiki/Guides/Qt_IDE) which also has ways to display display over the web, but it's not primarily web driven. It's on the QT environment.

00:28:34 [RP]

Feedback like this is not really news to Dyalog. I mean being so I think proper scripting support like you describe with the hashbang script is like under development and maybe see it around Dyalog version 19 or so with any luck. But people come into, the people who frequent the APL Orchard chatroom have requested this a lot, but Dyalog has historically had specific commercial interests that drive its development, so that's kind of your reasoning, I suppose. And yeah, historically it's been this thing right that APL is quite cool, but it's a bit of a, uh fortress or whatever so you you have to struggle a little bit. Once you've got the data in, it's really really fun, you're laughing and once you get the data out, you know well you don't have to care anymore. But those processes can be a little bit painful. Historically they are getting better. The tooling is getting better. Like say especially web stuff, scripting with Dyalog but historically, yeah, that’s been a point for sure.

00:29:43 [BT]

And I I should mention that J has, supports hashbang as well. In fact, there's a a really interesting fact from 2008,[Joey Tuttle](https://code.jsoftware.com/wiki/NYCJUG/2009-09-08/ArrayHabitsHarmful) talked about how he could put a, uh, a verb inline, but to do it effectively to do it efficiently, he had to change the structure of the verb so that rather than taking in all the information and putting out all the information, he had it so it would take in part of the information, whatever it was fed, and it would only feed out the part that had processed. So it really became able to be dropped into a pipe that way. And it was the only example I found of doing it, so I don't think it's done very often, but it was pretty neat to see how he had to adjust his function to accommodate streaming and it actually didn't seem to be that big a deal once he'd he'd made a few little adjustments to it.

00:30:34 [CH]

Yeah, well, and while we're on the topic of editors, it's worth mentioning that there's the Dyalog editor I think is just what it's called. But there's also the open source Dyalog RIDE editor which is super super awesome and and this is totally like random. But while we've been talking about Emacs versus the three different sort of J editors and and one of the things that just popped into my head is that if you have never played around with J or APL, I'm not sure I've seen this in k or q, but it's the visualization of nested arrays is absolute even on like the command line in in a terminal is absolutely like phenomenal, so it's hard to explain unless you see it. But basically like when you have a list of strings, you know “cat”, “dog” “mouse” and that gets put in a nested array you end up seeing basically like a 3 by 1 box and I don't know how they do it, but they manage to get like perfect little boxes even on even in a terminal and it's so nice. Like seeing that visualization instead of just three words next to each other, I don't know why it tickles my brain so much, but like the first time I saw it, I was just like wow, this is that's that's a beautiful like, why is you would think that sort of other languages would have this sort of option, and you can, you can turn it on and off and stuff. It's it's really cool.

00:31:52 [RP]

Yeah, I found it really amusing when I first learned of what we call the line drawing characters, because I guess most people would default to doing like a vertical bar or a minus dash or a hyphen or some other kind of you know things people are familiar with in ASCII traditionally, or writing word documents or whatever. But these line drawing characters are specific for probably old terminals, right where everything back in the day was was via terminals, so you had to have these, and there's like a –I can't find them, doesn't matter –if you do quad AV in Dyalog, I think you get the list of all the characters that used to be in a specific font file. Nowadays it's all Unicode, but yeah, they're they're quite fun.

00:32:33 [CH]

Yeah, don't don't visualize like the README you know, plus sign for the corners and you know pipes and hyphens. It's a very beautiful like polished connected like you're going to ask yourself. Oh wow, how did they? How did they get that to pop up in my terminal? Like things like that don't look that nice. Usually it's you know your H top and top are great to look at, but they don't look super polished, but these do.

00:32:54 [RP]

I think it's also in J and APL+ ‘cause clearly there, because the structure can be quite complex and it's also very important to what you're doing in those languages. Oftentimes, part of your solution is you're encoding some of the logic by modifying the structure of your array, and then you can do some kind of like also recent Rodrigo's, oh he did the run length encoding as one of his, Rodrigo Girão Serrão’s YouTube channel, one of his [LeetCode](https://youtu.be/7FygzvlOMcE) solutions in APL, and the thing with run length encoding is what is it? It's like a number indicating how many of the next element is going to be there, so he just reshapes that into an N by two so that the length is right next to the element and then he's doing and he does a reshape slash across that reshape reduce across the rows, and that's how he basically solved it. But there, like I said, the logic of the solution is encoded in the reshaping of the array and so not just you know the shapes of flat arrays, but also in modern APL's, the deeply nested structure. It's quite important to be able to tell the difference between. It's not always obvious in the basic, even basic boxing in Dyalog, whether you've got a scalar or a one element vector or a one element matrix, or something. So there are these display functions that do the boxing and possibly even extra glyphs around to really indicate or really tell you clearly what the structure is when that's important. It's not always important.

00:34:28 [BT]

And with J, one of the things that one of the two two cautions one is you actually can use the pluses pipes and dashes. You have an option with whether you want it to look pretty or not. The reason sometimes you use the pluses hyphens and dash or the pipes, hyphens and pluses is because sometimes, when you're dealing with text in, especially in emails, the special characters kind of get messed up, so it it's a way to clean that up. The other thing is if you want it to stay pretty stay away from Unicode 'cause that can really mess up how pretty those are and that's I spent an awful lot of time working with my visualizer drawing my boxes so they are pretty, and it's not an easy thing to do.

00:35:13 [CH]

Why did I the other day? I was showing my? I might have told this on the last episode. I apologize if I have, but I was showing my coworkers as one of my APL solutions that used quad C quad A for like lower casing some letters and a couple of them were like, oh like your Unicode not rendering correctly and I was like no, no, that that quad is intentional. That's a that's a box when supposed to be there and and the other thing I was going to say I watched that video by Rodrigo and I had the observation of that like oh, because I saw the reshape reduce and I was like is it possible to do a replicate reduce which also has the same symbol as the slash? And then I went and tried it and I was like Oh my goodness, you can definitely do a replicate reduce.

00:35:53 [RP]

Yeah, so that's also. That's also a curse in trains because we have those hybrid characters where a forward slash or a forward slash bar could be either a function or an operator, depending on the context, right? So then if you want to write a train that's all elegant, but it uses replicate, then you have to use right tack atop, because it is.

00:36:14 [CH]

We're giving we're giving Daniel more reasons to add to his feedback speech. Speaking of which, we should probably, we should probably hop back. I'll read the next couple or I guess one paragraph here, and then we'll take another break. So yeah, picking up where we left off, Daniel Daniel says to us

“Sometimes arrays aren't enough. On the podcast, Conor mentioned that APL can sometimes struggle with text munging required for Advent of Code input. I agree, as great as APL is, it doesn't shine in domains that are primarily text centric. To a data scientist, that might sound like a niche concern, but I'm primarily a web developer. My entire platform is built on text and I'm focusing on text here, but there are other times when a set, hash map or other non ordered data structure is a far better conceptual fit for a particular domain than an array. You can model these domains as arrays, just as you can model strings as arrays of characters, but doing so sacrifices considerable expressive power. Similarly, without wading into a whole other debate, sometimes types are helpful”

And we'll pause there. And once again, I'm not sure if Nick if you want to start us off again.

00:37:14 [NP]

Yeah, sure, no problem. The first you know, listen, he's he's. He's obviously 100% correct and I just wanted to given that this is a podcast about these languages, I just wanted to address what is possible in the languages. But first of all, in q it has rudimentary regular expression. It allows you to do stars at the beginning and at the end, but not multiple stars within the string in the middle. It definitely doesn't have the full power of Python or Perl regular expressions like you know, backtracking and things like that, or lookahead nothing, nothing of that sort. It's it's done me well enough as it is, uhm? I think there's a [quote](https://en.wikiquote.org/wiki/Jamie_Zawinski) that basically when you have a problem and you say to yourself, oh, I think there's a regular expression to solve that problem, you now have two problems, so it's not clear whether whether or not you know the full functionality of regular expressions you know will make you, you know, force the user to learn two different languages beyond just the language they're working in. Additionally, he mentions that you know how you know why don't you have a set? You know there's a set container in in q. At least you can, you can have a dictionary and if you put a unique attribute on the key, actually you don't even need the unique attribute, there's a plain old dictionary, and every time you add elements to it will enforce the uniqueness of the key and that you know you can treat that as a as a set. You can just ignore the value component of the dictionary and he also mentioned a hash map. Hash maps again, or dictionaries, where this is where the new attribute comes in. If you put a new attribute on the key, when you look values up, you actually get a hashing algorithm which will be used to find the value. So if you have, you know, a million elements in your dictionary? You're not going to be doing a linear search as you would with an array. Uh, you can do a quick hash map and it will be just as performant as any other languages’ hash map. Agreed, you know other binary tree type of data structures don't exist and you kind of have to roll your own, but I just wanted to mention that it's not all you know downhill just because the only data structure you have arrays. These languages have algorithms on top of arrays. You can do a binary search on an array and things like that, so it's not so bad.

00:39:38 [RP]

Yeah, I think it's similar to what we were talking about before where you're balancing your sort of intuitive expressiveness until you hit a problem with performance and then you're reaching for other things. Or in the case I guess, Dyalog does have quad R and quad C which are just regular plugins to PCR Regex engine underneath, so they're pretty handy. Actually, the way they work, where you can do multiple regexes with a single uhm, single call to the function is pretty slick. Sometimes I think there's some nice little ways of swapping parts of text that's quite difficult to do if you don't have that.

00:40:17 [BT]

Well, one of the things that struck me with this is often when I'm looking at a problem and you know it doesn't fall apart with an array, which is kind of the feeling you get with some problems, it just falls apart, you go, that's easy, done. But with the ones that don't fall apart that way, I have this nagging suspicion. And then I'm not quite seeing the whole problem, and sometimes it's accurate and sometimes it's not. I can't say that there aren't times when you you just never quite figure it out, but it's kind of like we talked about. And and Daniel talks about Aaron Hsu talking about his tree manipulations and stuff, and he's doing this amazing stuff at speed with trees, that most people don't think is possible to do with APL. Well, he cracked that code and it wasn't easy, but the point is at some level there may be a way to do it, but it may not be obvious, and that's the feeling I get when I'm working with arrays. The other thing with J is you actually do have the option of, well, in two areas. One is you can do object oriented. You know there are things called numbered locales. You can create classes and then create specific instances you can have them do behaviors. You can attach methods to them you know. Information is attached to them. You can make it unique by the way you put it in. And and so you can create this stuff. It's the the ability to create it is there? It's not often used because I think usually it's easier to go back to the to the arrays and the final thing I'll talk about is symbols which are very underused. But symbols actually are, or if you in J if you took a boxed character string so that the box itself is a single atom and the contents would be a character string. A symbol in J is the same thing, except it hash maps so that it's represented a different way. It's not in a box, but it's an atom that is actually hash mapped. So if what you're doing is involving character strings, that's a very quick way to do it, and that is actually built into the language as well, and you could have arrays of symbols. And all these kind of things, but it does build this hash mapping ability into what you're doing for searches and things like that.

00:42:32 [RP]

Yeah no, this is, this is kind of what I wanted to say, actually, is that all of these languages are, especially the applications that sort of run the language and do the interfacing and everything. I guess you call it the language interpreter or whatever. Often all of our respective institutions kind of undersell all these additional things that we have for the sake of of having to interact with the outside world largely, or do these other types of manipulations, because I think we've spent a lot of time trying to tell people about the benefits of the core language, which you know obviously does have these amazing properties and I guess mainly it's so different to what else is out there. But like you say, there are things like hash maps, even Dyalog. You can have hashed arrays, object oriented similar in J and Dyalog. You can create classes and do things like this, it's just not often said, you know, yelled about out loud because I guess it's so basic everywhere else and they were kind of put in just so that you have that option right? You have the option in these different systems, not only to do, sure, you can roll your own solution using just the core language arrays and primitives. Build up your entire framework. Obviously that's feels like reinventing the wheel in some cases, but you also have the option to change into different modes. I think in all of these systems, q, kdb, J and APL. I think you can do something that isn't just the core language in order to facilitate having some kind of bigger framework, or maybe do some interfacing. Think create parts of your application which are extensible in the classic object oriented sense and other things like this. So yeah, maybe it's another case like we've talked about before. It's like more of a documentation slash evangelization problem where it's just not obvious to people who aren't in these circles that that these things exist, so we need to be better at getting getting the word out.

00:44:40 [CH]

I think I think to at least from my like polyglot point of view or or. You know, I'm an aspiring polyglot, you know, I code in C++ day-to-day, but I'm you know, trying to learn all the languages, and I, you know, I love learning languages and one of the things I think to recognize is that, like in my opinion, there is no one like perfect language. You know, say what is the best language you know there's. If you go on YouTube and like what language should I learn in 2021 there's 1001 videos of people giving their recommendations of this is my top five list of what you need to learn this year. Because, you know, Elixir’s, the new big thing and it's functional programs taking over the world. Uhm, in my opinion like those videos are all really silly because you need to ask yourself first. Like what problem am I solving. There are just certain programming languages that are better at solving different types of problems, and I don't think that's a bad thing like I think when this was a couple years ago, when I was at Amazon but I was, I learned go in a couple days 'cause it's a very simple language but one of the things that I think even the docs say is like Go is not a good language for a GUI application design because we don't have library supporting it like it's, it's primarily... The space that it operates in is like running large systems across servers and they even like I used to market it as sort of a systems level language, but they sort of went away from that because they found that like the really really good use case for Go was, like, you know Kubernetes stuff. And and you know and and so this ties back to sort of Daniel feedback is that he says, you know, I'm primarily a web developer and I don't know like I don't want to say that don't go and build your your websites with, you know, don't go and build it with Dyalog APL. I don't know APL well enough to like how, how good do they have support for those kinds of libraries and things. But in my mind, if I'm going to build the website, probably APL isn't as like a non APL expert, it's not the first language I'm going to reach for. I'm going to reach for a language like JavaScript or you know some other. You know what's more known as like a web front end language, even though I don't know those languages at all. I know that just like those are the go-to for that sort of particular problem, the same way that...

00:46:45 [NP]

But it's also because they have frameworks built and community contribution going back to you know a lot of what we were talking about before. The languages itself might be able to do it, but there's no Django for for APL, you know Ruby on Rails, they don't. Where is that for? For APL. So that that's potentially maybe the part of the problem.

00:47:04 [RP]

We have Dyalog MiServer slash what’s it called, DUI. It's like a web service framework. We can also write web pages in your APL, but I remember a user meeting couple years back, some Italian high school students came and they did like a a problem solving contest with us, who had attended the user meeting and the thing was a web framework they set up for like doling out the problems and keeping track of schools and stuff, and I remember they had said I don't know how much time they've spent on it. But like they were aware of MiServer, but because of their familiarity with it, what they actually did was set up a Python Django server and then used the Python to Dyalog bridge to set that up so I guess, yeah. You reach for the tools that you're aware of, or the ones you think will be best for the job, and then you hope that you can plug the other pieces together. Like a lot of people use APLs, J and q and k as a kind of Swiss army knife of doing other miscellaneous specific things that they can think of how to do and then for a lot of the big picture stuff, they'll stick to the established kind of frameworks and languages that they're out there and have, like Nick said, lots of community contributions and lots of support and googleable answers things like this.

00:48:20 [BT]

And and with JHS the front end, for for J in the on the web. Eric actually run’s a, written a little small subset to run it so it's it's really easy to learn. It's quite not quite as powerful as a lot of the other frameworks, but you can get into things and do them very quickly, very cleanly, so it has, there's actually this sort of little framework that sits within JHS that you can use yourself to write your own web pages. They're limited, but if you want to go further with it you can always extend them.

00:48:51 [CH]

Yeah, so I guess I guess yeah. The overall thing is just there's there's times and places where languages will excel. Like if I'm going to write an iOS app, you know. Sure I can go. I can go try and use APL, but probably it's just easier to go use Swift because that's what that language is primarily designed for and trying to use Swift outside of iOS apps, or you know, that ecosystem is extremely challenging, like they're trying to work on that, you know, and and so if you just want to build a standalone sort of game, you know it's a lot easier to do that in a languagelike C++ or something, because there's more of an ecosystem there, so it's... It's always good to like look at what domains does it best for, but definitely that's something that I just thought about is depending on the language. If someone comes and says yeah, I tried to do this and it wasn't great like that's not necessarily always a bad thing.

00:49:36 [RP]

So further on the letter, depending on how far you manage to get today, or if this is going to come back another time, Daniel talks about the Raku programming language, so I decided to ask. In the APL Orchard 'cause I know there's a couple of people in there who do Raku and stuff to give me their thoughts and the kind of contrast, but it's kind of relevant to what you're talking about, so I thought I'd just slot it in here. Where, uhm, he said. “If I want most of my work done for me and I want nice errors and nice documentation, I would always go for Rakudo. If I want to do something interesting and improve my understanding of an algorithm, I'd use APL or an APL family language.”. So I don't think that's comprehensive in any sense, but that's one example of this. You know someone who's decided for themselves, you know? This is what I like to use APL for, and this is what I like to use some Raku for.

00:50:23 [CH]

So at this point, I think we'll hop back to the third and final point that Daniel made, and it's on the following metaprogramming, introspection and extensibility these days with dfns that's D-F-N-S user-defined operators and all the features of modern APL.

“It's no longer fair to describe APL as a diamond that's beautiful in its current form, but that can't be extended in any way without ruining the whole effect. Yet some of the spirit remains when writing APL. I didn't feel that I was on a par with the language designers building my own libraries with exactly the same power they have when adding new primitives. The power of metaprogramming isn't one I reach for often, but when it's the right tool, it's usually the right tool by a huge margin.”

And we'll kick it off for folks that want to respond.

00:51:07 [NP]

I think metaprogramming is is a very powerful concept and paradigm. In in the the one thing that q has that goes along those lines is the ability to do introspection on the function. So if you call `[get](https://code.kx.com/q/ref/value/)` on a function, what you get back is a, uh, a list of items. One of the items is the the, the arguments that are being passed to it. You know how many are they? What are their names? Another element of the list is what are the local variables that are defined in the function and what are the global variables that are they're accessed from within that function? Another element is the actual raw function text. If you wanted to redefine the function by manipulating it, you could actually grab that text, prepends some new text in front, and some other text in the back, and then eval it and store it back into the function that was previously defined. That's not as elegant as perhaps what Lisp would would allow you to do where you can, just everything is just a list, and even the code is a list and you can prepend, postpend or or even insert in the middle all you want, but the functionality happens to be there. I've actually used that functionality to write, you know, a function profiler. You grab the function, you prepend a timestamp, you postpend a timestamp, and you subtract the two and insert the result into a table and you can now run your code and analyze the results of of of the profiling, so that is pretty interesting and the same problem, but I would say other languages probably do it in a more elegant fashion than that.

00:52:45 [CH]

Rich and Bob anything you want to add to the extensibility, introspection or metaprogramming points.

00:53:00 [BT]

And right now it's written as a J add on, so it's written in J. It hasn't been put into the C primitives. It's a primitive that runs In J. So in essentially what what's happening? There is the language designers are using exactly the same tools that you would have to use to create their primitive, and they're testing it out that way. The other thing that's interesting is they've taken some of the calculus primitives and they've moved them from being in C back out to J, and the reason for doing that, now they're sitting in a library it's easier for people to extend them and adapt them to whatever their particular needs are. What they were finding is a lot of people were coming and saying, well, this doesn't really work in this edge case or whatever calculus does work and it was getting so hard to keep up with what people’s needs were they said well, why don't we just put it out into an area? You make the adaptations you want. You change the verbs to what you want to, it'll be performant and you'll have the chance to change it as you wish. So in that sense, it's sort of an indication that with J they really have tried as much as possible. You use the same tools that the designers of the language are using. They won't necessarily become primitives, I guess along the line they could, but that's the sort of thing that J has been doing. In addition, everything if you want to look at a verb in J, you just type the verb name. It comes back at you. If you want to make adjustments to that, you can. It is called an atomic format, which means it's a format. It's actually captured as a noun even though it's a verb, it's called a gerund. So if you think like “the art of cooking”, cooking is a gerund, it's not a verb at that point, it's it's something it's a noun. It's cooking. “To cook” is a verb, but you can capture that cooking and add that that verb and make it a gerund, and then you can do all sorts of manipulation with it. But then you're starting to get into rewriting programs within themselves, and that can get messy. I mean, again, it's kind of a dangerous area to get into.

00:55:04 [RP]

I was going to say a couple of things. One is, recent primitives in Dyalog, beforehand, I think have been modeled as APL models, and you know they might not have, like you say, a Unicode primitive symbol that you can use. Although I know remember it's not, so it's not developed anymore, but Nick Nick loves NGN APL. You actually could. Although I now remember it's not, so it's not developed anymore, but Nick Nickolov’s ngn/APL. You actually could redefine plus if you wanted to. I think it fell over when I wanted to turn the split train into a yeah, emoji knife. I was going to have that as a split function, but it wasn't able to handle that because of the double width Unicode character or however it handled it. So that was kind of funny, but I do know that you know, for example “Under” which J has, I can just write that as a user defined operator. I tend to put underscores on, “underscore U underscore” if I'm defining my own dyadic operator just from my own so I can see what type it is, and then on that note something that's a little bit awkward is the indexing function squad in Dyalog. But you know there is a construct which I think we've taken to calling select or the indexer which allows you to select in a slightly different way and I used, I just use that these days. I'll do “I ?” the definition of select and then because it's a single letter it doesn't look too ugly in the in the rest of the code. So yeah, there are things that allude to that. I don't have loads of experience like you know about other languages in the way, and I've heard that Lisps and Scheme and stuff have really nice metaprogramming. Or maybe it's been argued they make it too easy to do metaprogramming. I don't really can't really speak on that. But I know that extending the language is something that APLers are interested in. I know for example, Adám has both, Dyalog Extended is a GitHub repository of his where he's just taken some of the primitives and extended them, and there's also another one, called APL Prime, that I think he started on, which is trying to iron out some of the historical warts a little bit so they're not so. APL Prime is not backwards compatible of Dyalog, but I think extended is or whatever. You know there are efforts in in that in that world, but I don't know if that's metaprogramming in the same sense that Daniel meant.

00:57:24 [CH]

Speaking of a Lisp, the, one of the co-creators of Scheme, Guy Steele, who has worked on a number of languages across the years. He is a big APL fan, but in his fabulous "[Growing a language](https://youtu.be/_ahvzDzKdB0)” talk and paper, which we will definitely link in the show notes, he makes a remark and kind of criticism that he thinks one of the reasons that APL wasn't as successful as that, it's it's what was sort of remarked on a couple times. You can't add a Unicode, like, primitive when you are writing a library, it does not look like the language, and it's one of the few languages that exist that actually has that case. When you're writing Java code or C code or Swift code or Python, your library that you're writing the code that you're writing looks like the core language. But APL does not have that, and I'm not sure whether it's true or not, but it is, I think, an interesting remark that in APL, and I guess q doesn't have this problem, 'cause q is wordified, so you can write functions, and that looks like the you know the built-in functions, but definitely for APL you can't. You can't write, you know, you know exactly, like, uh, not that I'd be trying to add a knife emoji, but if I wanted to go find some unused weird looking Unicode character, I couldn't, I couldn't define that to be something, at least I don't think think you can. And yeah, it's an interesting remark. Not sure if anyone wants to respond.

00:58:46 [RP]

I think it's just something people haven't pushed for that hasn't hasn't, not enough people have found it so desperately in need that an implementer implements it. But I don't think it's like it's not in principle not doable or anything.

00:59:02 [CH]

We will, uh, we will close out with uhm, not the end of the feedback that we got but this last paragraph that just, it says, Daniel sort of wraps up his three criticisms by saying

“Due to these drawbacks, I reluctantly decided to shelve APL and go back to Rust, but I resolved to keep my eyes out for another language that could deliver the abstraction smashing power of APL without some of the tradeoffs.”

And I think we will find a way to link the full feedback. If folks want to read the [full feedback](https://www.arraycast.com/episode-4-daniels-email) later on in the feedback, he starts to go on to talk about a programming language,[Raku](https://raku.guide/), which was formerly known as Perl 6 and talks about how a lot of the same advantages and reasons he fell in love with APL originally can be found in Perl 6. And it's it's definitely an interesting read, so we'll link that for anyone that's interested. Any last comments folks want to make before we head out? I think actually we did have one announcement that I believe Rich wanted to make.

00:59:48 [RP]

Oh yeah, just a another sort of general heads up about those who are interested in the history of APL, APL related languages, Adám Brudzewsky, who's obviously a regular on this podcast, hosts every four weeks an event called [APL Campfire](https://aplwiki.com/wiki/APL_Campfire). It's free, open to attend for anyone who's interested and if you want details on when the next one is and how to attend, you can go to APL dot wiki forward Slash campfire (apl.wiki/campfire).

01:00:16 [CH]

And I think with that said, once again, thank you to Daniel for providing us with such a long, wonderful email, and which caused this whole podcast episode. And I think Nick this will be the last time you're on for a little bit. So once again, thanks for coming on and sharing your knowledge about q and yeah...

01:00:31 [NP]

No problem, thank you.

01:00:32 [CH]

Really appreciate you coming on, and I think we'll say happy array programming and have a great day.

</details>
