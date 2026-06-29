---
title: "Episode 41: John Earnest and Versions of k"
date: 2022-11-26 00:00:00 +0000
episode: 41
buzzsprout-id: 18617086
keywords:
- array-programming
- array-languages
- conor-hoekstra
- j
- k
- 1010data
- john-earnest
- forth
- kerf
- ok
mp3-url: "/assets/audio/episode41.mp3"
episode-type: full
explicit: "no"
block: "no"
layout: podcast
excerpt_separator: <!--more-->
redirect_from:
  - "/episodes/episode41-john-earnest"
  - "/episode41-show-notes"
---
In this episode, we talk to John Earnest, creator of the ok.js k6 interpreter and an expert on k programming, about many aspects of array programming, including the relationship between k and Forth.
<!--more-->

**Host:** Conor Hoekstra

**Guest:** John Earnest

**Panel:** Marshall Lochbaum, Adám Brudzewsky, Stephen Taylor and Bob Therriault

---


## Show Notes

- [https://cs.unc.edu/news-article/remembering-department-founder-dr-frederick-p-brooks-jr/](https://cs.unc.edu/news-article/remembering-department-founder-dr-frederick-p-brooks-jr/)
- [http://www.jsoftware.com/pipermail/chat/2022-November/009134.html](http://www.jsoftware.com/pipermail/chat/2022-November/009134.html)
- [http://archive.vector.org.uk/art10001240](http://archive.vector.org.uk/art10001240)
- [https://en.wikipedia.org/wiki/System/360](https://en.wikipedia.org/wiki/System/360)
- [https://www.youtube.com/watch?v=BXzvyRGGBoE](https://www.youtube.com/watch?v=BXzvyRGGBoE)
- [https://cs.unc.edu/brooks](https://cs.unc.edu/brooks)
- [https://dyalog.tv/Dyalog22/](https://dyalog.tv/Dyalog22/)
- [course.dyalog.com](http://course.dyalog.com/)
- [https://course.dyalog.com/](https://course.dyalog.com/)
- [https://www.youtube.com/watch?v=aEN1MBTzCjY](https://www.youtube.com/watch?v=aEN1MBTzCjY)
- [https://code2.jsoftware.com/wiki/Main_Page](https://code2.jsoftware.com/wiki/Main_Page)
- [https://github.com/dzaima/CBQN](https://github.com/dzaima/CBQN)
- [https://kx.com/kdb-personal-edition-download/](https://kx.com/kdb-personal-edition-download/)
- [https://vector.org.uk/a-graphical-sandbox-for-k-2/](https://vector.org.uk/a-graphical-sandbox-for-k-2/)
- [https://www.forth.com/forth/](https://www.forth.com/forth/)
- [https://vector.org.uk/impending-kos/](https://vector.org.uk/impending-kos/)
- [https://en.wikipedia.org/wiki/Arthur_Whitney_(computer_scientist)](https://en.wikipedia.org/wiki/Arthur_Whitney_(computer_scientist))
- [http://web.archive.org/web/20050504070651/http://www.kx.com/technical/documents/kreflite.pdf](http://web.archive.org/web/20050504070651/http:/www.kx.com/technical/documents/kreflite.pdf)
- [http://web.archive.org/web/20041022042401/http://www.kx.com/technical/documents/kusrlite.pdf](http://web.archive.org/web/20041022042401/http:/www.kx.com/technical/documents/kusrlite.pdf)
- [http://web.archive.org/web/20060214100753/http://www.kx.com/technical/documents/cki.pdf](http://web.archive.org/web/20060214100753/http:/www.kx.com/technical/documents/cki.pdf)
- [https://johnearnest.github.io/ok/index.html](https://johnearnest.github.io/ok/index.html)
- [https://github.com/kevinlawler/kona/wiki](https://github.com/kevinlawler/kona/wiki)
- [https://github.com/kevinlawler/kerf1/raw/master/manual/refmanual.pdf](https://github.com/kevinlawler/kerf1/raw/master/manual/refmanual.pdf)
- [1010data.com](http://1010data.com/)
- [https://www.1010data.com/](https://www.1010data.com/)
- [https://kx.com/](https://kx.com/)
- [https://code.kx.com/q4m3/6_Functions/#64-projection](https://code.kx.com/q4m3/6_Functions/#64-projection)
- [https://codeberg.org/ngn/k](https://codeberg.org/ngn/k)
- [https://shakti.com/](https://shakti.com/)
- [https://k.miraheze.org/wiki/](https://k.miraheze.org/wiki/)
- [https://www.jsoftware.com/indexno.html](https://www.jsoftware.com/indexno.html)
- [https://en.wikipedia.org/wiki/OpenGL_Shading_Language](https://en.wikipedia.org/wiki/OpenGL_Shading_Language)
- [https://beyondloom.com/](https://beyondloom.com/)
- [https://dyalog.tv/Dyalog18/?v=mK2WUDIY4hk](https://dyalog.tv/Dyalog18/?v=mK2WUDIY4hk)
- [https://soundcloud.com/lambda-cast](https://soundcloud.com/lambda-cast)
- [https://factorcode.org/](https://factorcode.org/)
- [https://en.wikipedia.org/wiki/Charles_H._Moore](https://en.wikipedia.org/wiki/Charles_H._Moore)
- [https://www.greenarraychips.com/home/documents/index.php](https://www.greenarraychips.com/home/documents/index.php)
- [https://en.wikipedia.org/wiki/Donald_Knuth](https://en.wikipedia.org/wiki/Donald_Knuth)
- [https://en.wikipedia.org/wiki/TeX](https://en.wikipedia.org/wiki/TeX)
- [https://en.wikipedia.org/wiki/METAFONT](https://en.wikipedia.org/wiki/METAFONT)
- [https://en.wikipedia.org/wiki/Literate_programming](https://en.wikipedia.org/wiki/Literate_programming)
- [https://scholarworks.iu.edu/dspace/handle/2022/24749](https://scholarworks.iu.edu/dspace/handle/2022/24749)
- [https://www.sacrideo.us/](https://www.sacrideo.us/)
- [https://aplwiki.com/wiki/Aaron_Hsu](https://aplwiki.com/wiki/Aaron_Hsu)

<details markdown="1">
<summary><strong>Transcript</strong> (click to expand)</summary>

Transcript

Transcript prepared by Bob Therriault, Adám Brudzewsky, Igor Kim and Sanjay Cherian

Show Notes

00:00:00 [John Earnest]

Like when I when I started with OK. The legends about k5 were that Arthur Whitney implemented this entire language in about 400 lines of C.

So I was like, alright well I, John, a normal programmer ought to be able to write an implementation of this in about 1000 lines of JavaScript. And I did.

00:00:15 [MUSIC]

00:00:26 [Conor Hoekstra]

Welcome to another episode of ArrayCast. I'm your host Conor, and today with me I have 4 panelists and a special guest that we will get to introducing in a few minutes. But first, we're going to go around and do brief introductions. Let's first go to Bob, then to Stephen, then to Adám and then to Marshall.

00:00:48 [Bob Therriault]

My name is Bob Therriault and I am a J enthusiast.

00:00:51 [Stephen Taylor]

I'm Stephen Taylor. a q and APL programmer.

00:00:55 [Adám Brudzewsky]

I'm Adám Brudzewsky. I teach and write APL code.

00:00:59 [Marshall Lochbaum]

I'm Marshall Lochbaum. I'm a former J programmer and a Dyalog developer and now BQN developer.

00:01:05 [CH]

And as mentioned before, I'm Conor. I'm a research scientist at NVIDIA, but a polyglot programmer and enthusiast of all array programming languages. So I think at the top of the episode I'm going to throw it to Stephen, who is going to sort of make an announcement or a mention of something that's happened in the past week.

00:01:24 [ST]

Well, we are sorry to note this week the passing of Fred Brooks,[01] who, with Ken Iverson, who designed APL, taught the world very first computer science course at Harvard in was it 1960 at late 1950s? They wrote for that course, what must have been the world's first textbook for computer science which turned into two books? Automatic Data Processing, as data processing was what we used to call it back in the day and a book about the notation used in the first course and the book was called A Programming Language. It described Iverson notation and eventually became the name of the computer implementation of Iverson notation. Fred preceded Ken to IBM. Fred managed the development of the system 360 operating system and later achieved widespread fame as the author of the Mythical Man Month and in 1999 was awarded the Turing Award, just as Ken Iverson had been, it is pretty much the equivalent of the Nobel Prize for software. A great life well lived, sorry to see him go, great to have known him.

00:02:53 [BT]

And in in some personal reflections, Ken Lettow had was part of a documentary that Catherine Lathwell have been putting together in 2012 and part of that was Ken and and Catherine had a chance to actually interview Doctor Brooks and Ken had sent this this e-mail out, which I'll read now.

00:03:16 [BT]

So I was lucky enough to have spent a few hours with Doctor Brooks while helping with an interview Catherine Lathwell did with him discussing Ken Iverson at APL in 2012. Doctor Brooks was incredibly engaging, had a great laugh and a sense of humor during a break in the interview, I asked Doctor Brooks about the famous Dijkstra APL coding bums comment and why it seemed that Dijkstra was so bitter towards APL. He quickly corrected me. He wasn't bitter, so I offered overly critical. Then, before the word critical left my lips, he proclaimed HYPUH-critical in his amazing Southern drawl. I was instantly laughing in his response. He went on to say that he wasn't really sure why Dijkstra had such a seemingly dim view of APL outside of maybe "It wasn't invented here" syndrome. It was a meeting I will never forget.

00:04:14 [BT]

And from reading I think it was also a Vector article on the passing of Ken Iverson, it was also mentioned that Doctor Brooks and and Ken were very, very close. In fact, Doctor Brooks named his eldest son after Ken, so there was a real real strong connection between these two individuals. And I agree with Stephen that it's very sad to see these pioneers passing away, but that's what happens when you have a language that's that's been around for a long time and it does show how brilliant these guys were that they came together and created these things that we still use today.

00:04:55 [AB]

I would say we should be happy that they were there and without them we wouldn't be here. As you mentioned the book APL, but pretty much all of modern computing depends on Fred Brooks. He said that the decision design that he was the most proud of was introducing the 8 bit byte. We take it so for granted, like we can't even imagine computing without an 8 bit byte, but he introduced that and the system 360 design that he oversaw became the precursor for all modern computing. All other types of architectures just disappeared after that and everything we have today is basically a descendant of this of the 360. And then we of course wouldn't be here, because without the 360 and the design document for 360 written in Iverson notation there would be no APL and the first  the first proper APL, was the APL 360 and I mean they studied together Iverson and Brooks studied together under professor Aiken and Brooks was excited to become the teaching assistant for Iverson and I'm sure, as they were so close, that was also why, I suppose it was Brooks, at least he must have been involved in, that chose Iverson to write up or provide tools for writing up the formal spec for the this new computing system, which, by the way was an all in that IBM did. IBM was betting everything on the 360 and it succeeded. And that's where we are today with computing. So in many ways we would not be here, just the technology we are using to record this wouldn't be here.

00:06:54 [ML]

As an implementer, it is really incredible too, so if you want some Maple today, you say, well, all right. The user sees 64 bit floats, but underlying that I have 64 bit floats and 32 bit ints and smaller ints and packed booleans and then looking at the APL 360 implementation I saw, well, in fact it's the same. They had 64 bit floats and 32 bit ints and packed Boolean. So they skipped the smaller integers, but what's really incredible is that that was the very first machine that did that, so Fred Brooks is their pioneering the system that still works today and it's still super fast back in the the 60s.

00:07:38 [CH]

Yeah, the quote from standing on the shoulders of Giants comes to mind and clearly Fred was one of those giants, so I think there is a service that's being held and recorded and played online that we will link in the show notes if it's available by the time this podcast comes out, and even if it's not available, we will retrospectively go back and add a link when it is available for those that want to go and watch that service, as he will clearly be greatly missed, and in the CS community at large, but also his family and friends will miss him dearly.

00:08:12 [AB]

It's being livestreamed on YouTube right now as we record this.

00:08:17 [CH]

OK, yeah, so it it the link should definitely be available by the time this podcast podcast comes out. [02] With that said, then we will transition into our announcements for today's episode. So I believe Adám has three. Bob has two, Marshall has one, and then Stadam or Stephen has has one, so 3-2-1-1. Let's start with Adám and then go around.

00:08:44 [AB]

OK, just quickly the Dyalog 22 user meeting - all the videos are now available online. [03] There is course DOT Dyalog DOT COM which has been around as a work in progress for a while, but it's now been updated to be a proper introduction in self study course, so check it out. And then Richard and I recorded the third episode of the APL Notation as a Tool of Thought podcast is now available.

00:09:14 [CH]

Is it? Is it a podcast podcast yet? It's still just the YouTube channel podcast.

00:09:16 [AB]

I I knew you're gonna ask that no, I still need to figure out how to do that somebody suggested on  Reddit that it has the wrong content type or something that's why it can't be published, but I'll look into it, eventually.

00:09:33 [CH]

It's alright. You keep poking the bear until until the bearer responds, and you know that's how that's how things get done. You know, I'm like a project manager here. You know, I, just are you blocked? and I'm trying to unblock you, that's all, thanks. Right over to Bob.

00:09:47 [BT]

You may remember that Rodrigo had been doing transcripts for us and he has moved on from dialogue and he's moved on from doing transcripts for us. And once again we thank Rodrigo for that. In his stead we have two new people that are helping out with transcripts. We have Sanjay Chandrian and we have Igor Kim and we thank both of them for stepping up from the community and helping out with the transcripts 'cause it's great to have other people to shoulder the burden and and and much thanks to them. And my second announcement is that my long-awaited prototype J Wiki [04] is up and it's there for people to look at and what we're doing is we realized that the J Wiki had just a tremendous amount of information and is loosely organized, I would say, which made it very hard to find things. So, our response has been to create navigation bars and essentially a navigation route through what I think of as a front end of the wiki, which should satisfy most people and we are not getting rid of all the old archive pages, so you'll still be able to do searches and get that stuff, but we're hoping to make it more accessible. And in the show notes, we'll put a link to the proto-type and in fact if you go to the existing wiki, there's on the sidebar, there's a link that will take you to the prototype and you can see what we're proposing and we are looking for feedback now. So if you have opinions on that or routes to go or things that should be added, this is a great time to get in and mention them and then I would say in the next month we will be looking to transition into this sort of front end to the wiki which makes it a little bit easier to get around, and most of the stuff that everybody is looking for will be sort of front and center and the stuff that may have aged out will still be in archives. And there's just so much information there it's amazing. That's my second announcement.

00:11:42 [CH]

Very exciting, I'm on the wiki now. Found it, it doesn't have good SEO right now 'cause there's already 2 wikis, I guess, but it looks very nice. Very colorful, I'll have to poke around this, yeah, in the next couple days anyways, over to Marshall or you're going to say something Bob?

00:11:58 [BT]

Yeah, it is that essentially we do have two wikis that we're running. We won't be changing the address of the original wiki, so we're just going to build this front end onto the original wiki. So this has been a prototype that we've been working through

00:12:10 [CH]

Alright Marshall.

00:12:14 [ML]

So my announcement I mentioned earlier that we were working on this RPLXX [05] integration for BQN and that's now done. That's merged to the main branch. So you can build it all you have to do is instead of doing make you add an option. REPLXX equals one that's listed in the README and that will build with an integrated REPL. So if you just then run the executable, you get a REPL that has syntax highlighting. It has BQN input, and it has some main completion, which will probably be improving in the future. So, that's really fancy. I've now been using this for a little while and I find it really easy to use. It's nicer than the the old solution of just using RL Rep. Yep, so that's the, that's the new thing in BQN.

00:13:05 [CH]

And last but not least, one announcement from Stephen.

00:13:07 [ST]

No, I want to be part of this new merged entity Stadam with the increased memory and processing power. I think that'll be much better. A while ago, some of you may remember at kx was having trouble with abuses of the license on the Community edition, and there were some restrictions placed on access that's now being sorted out, and if you go to kx.com you'll find you can download the personal edition very easily. [06]

00:13:38 [CH]

Yeah, I just did that the other day and it worked great. And back up and working on my my local workstation. All right so with all of those announcements out of the way, our guest has been patiently waiting in the wings, and I'm very excited to talk to him today he is, I guess the second individual we've referred to two individuals that were hired at some point, I believe by 1010data, but this individual is John Earnest, who I'm guessing by the title of this podcast episode you already know by now, and he is also known by the pseudonym IJ, which stands for Internet janitor. We'll have to ask about that and how how that came to be, but more importantly is the creator of the JavaScript k implementation. OK, I think there's a list on either the APL wiki or maybe it is actually the k wiki of a list of the open source k implementations, because obviously Arthur Whitney implements his own, you know k1 through all the way to Shakti, but along the way there have been implementations, I believe Stevan Apter had a k3 implementation that he called Slack that was built on top of combinators that was sort of a side project k thing or maybe not a side project to him, but like a hobby project. But OK I think it's one of the more of the well known open source implementations I think Kona is also one of them, so we're going to talk about that a ton. It also refers to Special k that is not linked to on the APL wiki, but we'll get to ask about that and into looking into John, he's done a ton of stuff in terms of game creation and some sort of GUI applications. [07] He, I think, worked on one thing called Ike, which was sort of a programming environment for k. So tons of stuff around the k ecosystem. And yeah, we're going to link a really cool article that has some visualizations of some of the k stuff that John is done, which is fantastic. It was posted on the vector website. So with that I will throw it over to you John. Take us back to whenever you want to. When you're born, when you started programming, you know whatever point in your timeline and tell us how you got to. You know, sort of falling into k land if you will, and implementing OK sort of implementation.

00:15:50 [JE]

Sure, well let's see. I was born in a very early age. For a long time in kind of my early history, I didn't really have very much access to computers or information about computers or adults who could teach me about computers, so I spent a meaningful portion of my childhood, like in in the Public Library reading a bunch of random assorted books about computer stuff that I kind of a little bit understood but, most of it didn't really make very much sense. The first computer that I had that was mine was a Macintosh SE that I literally rescued out of the dumpster, and so that that sort of colored a lot of my a lot of my early experiences with things were kind of getting second hand or semi busted computers that were already obsolete by the time I had them. But you know, it meant that I had unfettered ability to fiddle with them to the extent that I could figure stuff out. I ended up going to college eventually and I got a degree in computer science. I learned a bunch of things that I didn't know. But I think a lot of my formative programming experience was just kind of like long years of pounding my head against the wall with nothing to consult and slowly figuring things out. I did a couple of jobs after college. One job was this sort of small shop that was a consultancy doing a whole bunch of contract work for different companies and that was a very enlightening experience about how little I understood about programming and and technology. Basically getting sort of paradropped into these new environments to do some consulting project and having to speed up on a whole bunch of stuff. Get used to a new team culture from the relative convenient safety of, you know, not actually having to go work at all these different companies. And eventually I sort of took from those experiences I decided that I would go back to grad school and work on a Masters degree and sort of flush out these areas that I hadn't. I had discovered gaps in in my theoretical computer science and and practical programming sides and as sort of a side effect of having the kind of free time that the specific kind of free time that a grad student has I got really deep into Forth [08], which is an interesting sort of minimalist language. It's one of these like ur languages, that sort of arrived at one point and then influenced a huge number of of languages that came later and coming from a different taxonomic tree than a lot of mainstream things.

00:19:05 [CH]

Sorry, what was the the word, what kind of language an ur language?

00:19:08 [JE]

And yeah, like like a a primordial sort of thing. You know, like like U-R.

00:19:13 [CH]

Yeah, right.

00:19:18 [JE]

Yeah, so you know the Forth is all about building like the these tiny minimalist systems where you sort of collapse all of the layers of complexity together. You throw out everything that isn't absolutely necessary. You know you program in direct harmony with the machine. And it's as much a kind of a philosophy of a way of doing things as it is a specific language. If you, if there are n Forth programmers in the world, it's a common adage that there are at least 2n+1 implementations of Forth. And so I think the like I gained a lot of aesthetic appreciation for minimalism, from from getting deep into Forth, and I, I guess, another thing that I sort of took away from it, was it kind of opened my mind and removed a lot of biases about what constitutes reasonable syntax for a language because Forth is a very unusual looking language has sort of, you know you have tokens that are separated by whitespace and that's it. There can be anything one can be the definition of a word, and so I guess in retrospect that sort of planted the seeds for me to eventually be able to encounter something like k and accept it on its own terms, instead of having the kind of knee jerk reaction that a lot of people have to the first time, they look at one of these APL derived languages, because it's you know they certainly have beauty that you can learn to appreciate, but it's so alien that a lot of people just kind of shut down when they first encounter one of these languages.

00:21:07 [JE]

So I read this article called Impending kOS [09], which is a story about this sort of eccentric genius programmer named Arthur Whitney and it painted this this very to my mind, romantic view of, uh, you know this this guy with a unique style of programming that was very dense and very efficient and he was on the cusp of releasing this a new version of the language, and I thought it was very, very intriguing and appealing to try to learn something from Arthur's approach to programming. And I was completely dissatisfied with the fact that I could only play with the older versions of of the language that was sort of a concretion of Arthur style. So I resolved that I was going to use the little scraps of information that existed about k5 at the time. The unreleased nascent version of what Arthur was working on and try to sort of rebuild that from first principles and there there's good documentation, available online on k2 and so I started with getting most of most of the k2 implementation together over a a long snowed in winter break one year. And then I started kind of growing it in the direction of K5. I had example programs that Arthur had, you know, posted on his website or given an interview or something, and so I knew what had to work in order to make that program meaningful and to a moderate extent I was able to work backwards and sort of graph things onto to k2 and grow it in that direction and eventually a bunch of people sort of bullied me into trying to reach out to to Arthur with this thing. So, I sent him an e-mail. And he sent me back another e-mail that was like a couple of sort of penetrating questions about how I had done certain things in my intro. After I answered those as well as I could and then he emailed me back with just an FTP address and a username and password, and then I logged in and I downloaded a k5 binary and from that point forward it was then continuing to build up OK [10] as a black box, you know clean room reimplementation of the same thing. I could observe its behavior and then try to replicate that. So Kona [11] was the first open source k implementation and that was sort of targeting K3, which is also the dialect of the language that I ended up using professionally to get a little bit ahead of myself. So OK was targeting k5 which is a little bit different, but of a similar lineages.

00:24:20 [ML]

And just to help keep things straight, OK as your implementation, Kona is someone else named Kevin Lawler's, right?

00:24:27 [JE]

So yeah, Kona as a project by Kevin Lawler. What was actually kind of interesting is that not that long after I was working on OK and had that publicly released, I ended up having an opportunity to work together with Kevin Lawler on one of his own projects. He was working on a commercial, now open source language called Kona or sorry code called Kerf [12] and I wrote the Reference Manual for that language. Sort of, I was brought on as a as a technical writer actually and ended up being becoming sort of the defective QA guy because I had to test everything and exhaustively pry through the language as as Kevin was, you know, adding things to it and and making continuous improvements to it. That was a really fun collaboration and then ultimately, you know through a couple of of turns of circumstance I got an offer I couldn't refuse from 1010data. [13] And I worked at 1010 for about four years, doing mostly k3, and at the time that I left I was the head of the user interface development team, which is sort of doing what you'd call full stack web development, except it's a pretty unusual stack because 1010 uses their own custom version of k3 for almost all their back end infrastructure and then the front end of course is the web which is an unmovable object, so there's also a write a lot of JavaScript and HTML and CSS stuff to that, but you're communicating with backends that happen to be implemented in k3.

00:26:17 [CH]

Is the custom k3 the macro language that Michal mentioned on the last episode, or are those two different things?

00:26:24 [JE]

Well, macro languages is a a series of sort of layered query languages against 1010 the application. You know you could think of 1010 as a particularly smart data warehouse. That is, you know it handles your data persistence. It handles data importing and then it has a very rich ability to perform queries, generate reports you can do sort of RAD application development on top of the 1010 has a very long history with kx systems, [14] and so to my knowledge they're one of the only places that has a source license for k3. And since kx doesn't really maintain k3 anymore and and 1010 has unlimited access to it, basically they they ended up continuing to make their own minor bug fixes and feature enhancements, so it's just a, it's an outgrowth of k3. Most of the additions, or you know, there there's some little quality of life things. A few primitives that are sort of introduced from the k5 lineage back into k3. And you know some improved concurrency and you know, interprocess communication, forking memory mapping, kind of, you know, low level mechanic stuff.

00:27:47 [CH]

Very cool.

00:27:48 [JE]

It's definitely recognizable as k3. It's not a different language, it's just a little bit better, a little bit modernized.

00:27:57 [CH]

If there's ever an ArrayCon conference, we'll have to get either you or someone from 1010data to come and give a you know, the k3 beyond of you know what's been done to the language since you you know or I don't know, some some catchy clickbaity title that you know we could hire someone to come up with the title for.

00:28:16 [JE]

It like I think the E as it's called is is definitely the best flavor of k3 that there has ever been, but the the tragic part of that, of course, is that it's extremely proprietary software that's going to be, you know, trapped behind copyrights, basically indefinitely, I think. I think even if 1010 wanted to make it public, which I don't think they do.  I don't think that they would be allowed to given their their agreements with kx. So it's if you ever want to use a really great version of k3, I guess, work for 1010data.

00:28:53 [CH]

Link in the show notes for job applications.

00:28:57 [AB]

And I'd love to see a table of k's with some comparison between them, I'm always at loss, I guess for the k community you know you throw out like k3 to k6, so everybody knows what which primitives are different and what's different than the data types and so on.

00:29:16 [JE]

The way that I think I would summarize it and and Stephen is free to give his own opinions after this, as k1was an internal like non public version of k that I believe was a Morgan Stanley project.

00:29:36 [JE]

K2 was the version of that, that became its own commercial product as sort of the nucleus of what KX systems did, and k2 is notable for the fact that it came with what some people refer to as the electric GUI. It's very, very easy to make data-driven UIs for k applications in k2; and the k2 reference manual and the k2 user manual are available online so there's very detailed documentation on how those are supposed work. k3 is sort of an incremental refinement of k2. It's just, you know, a newer version of the product; fewer bugs, some nice enhanced features, but it's basically this continuing through-line, although I think by the time k3 shipped, the GUI stuff had all been sort of lopped off, because they were focusing more tightly on backend service implementation rather than this kind of interactive analyst workflow, where people were really fond of being able to make GUIs easily.

00:30:39 [JE]

K4 is the basis of the q programming language. q is implemented in k4, and if you download Kdb+, you can get to k4 (we have to kind of claw it open; it's hidden inside and it isn't really documented). The documentation is all [from] the q perspective. But you can see the k4 implementation of q. It's just a file that ships with the thing, so you can reverse out how k4 must work in order for q to do what it does.

00:31:14 [JE]

K5 was an experimental project by Arthur that was originally intended as being part of kOS, which would be like a freestanding operating system that's just k as the applications language.

00:31:29 [ML]

Spelling there is: a lowercase k, capital OS.

00:31:34 [ST]

I have to admit I made that up.

00:31:36 [JE]

Right and k6 was an incremental refinement of K5. Basically, whenever Arthur decides that he has, like a fantastically new and better idea of doing things, he'll just throw away a previous version and start over from scratch; and that's kind of the K5-K6 transition; it was just same basic language ideas, but recycled.

00:32:03 [JE]

I guess, I should note that the semantic differences between k5 and k3 are a significant overall improvement of the language; like k3 has a dictionary type, but it's very, very limited in what it can do because it was intended to be, kind of, a correspondence between parts of the k tree (which is, k is sort of simple module system) and a dictionary. So a k3 dictionary can only have symbols as keys, and in fact it can only have symbols that are a direct mapping to k3 identifiers.  They're useful, but it's not really like what you'd think of as a general purpose dictionary.

00:32:54 [JE]

In K5, you have: anything is valid as a dictionary key and dictionaries have an algebra (the primitives through out the language generalize to them in a useful way). Like, if you comma a dictionary with another dictionary, what you get is the union of those dictionaries, and there are a lot of, kind of, subtle details that are not fresh in my mind about how all of the primitives apply but the general thrust that Arthur was going for was making it so that all of the arithmetic operations will work in a natural way if dictionaries are used to represent sparse vectors. So that was, you know, the structure behind that.

00:33:45 [JE]

Another big generalization is: k3 has projections [15] where, it's like a more convenient way of currying a function. You have a series of parameter slots for a function, and you can supply any subset of those arguments, in any order, and get a curried function, that has those arguments fixed. In k3 this is a syntactic property where you have to use the syntax of square brackets in order to get that projection behavior. In K5, it's a semantic property; any application of a lambda with not enough arguments gives you back, a projection with some of those arguments fixed, and a few additional slots waiting. So it's just, things like that; the language in k5 is much more general. It doesn't have a lot of entirely new things, but the generalizations bring out all these wonderful symmetries that you don't get in the earlier drafts of the language; and it also, you know, as a consequence, means that the surface area of the language (the surface area to volume ratio of the language) is even more absurd than it was to begin with.

00:35:14 [JE]

And then k7 was another, you know, a big overhaul. It diverged from k6 in a lot of ways, syntactically and semantically, and that was never shipped. I think that there were like some hand-picked users that did some high frequency trading, kind of stuff with it. But it was, you know, never really finished.

00:35:33 [ML]

That was developed at Shakti, is that right?

00:35:36 [JE]

K7 was the first thing that would, you know, become called Shakti.  And then they skipped over K8 just because, K9 (you know, dogs). I think Stevan Apter had something to do with that. And so k7 and K9 are both radically different languages from k5 and K6. k4 is a meaningful diversion, and there's a clear through-line of just simpler and more general, from k2 to k3 to k5 to K6.  Some of us in the open source community feel like k6 is maybe not the perfect K, but pretty darn close. And k7 is a bunch of, you know, experiments in a different direction that, maybe it will pan out, but he hasn't finished any of them yet; so we'll find out.

00:36:32 [CH]

So K9 is a evolution of k7 (like similar to how k6 was an evolution of K5)?

00:36:44 [JE]

Yes

00:36:44 [CH]

Interesting, I'm extremely jealous because this is one of my qualms (I think is the right word). There's even an open issue on a GitHub repository where I am comparing array languages, sort of, in the Iversonian circle and outside, like Julia and R, and then even some array language libraries. There's an open issue being like: "you should add k". And I'm like I agree but which k? Because I don't really know.  Like everything that you have stored in your brain, is the same info I have stored about C++; like I can think about the different ways to write a different line of code in C++(98) versus C++(11) versus C++(14) verses C++(17) verses C++(20) even versus C++(23); and I have all the different features catalogued because it's what I do professionally. And, like, having that information is amazing because it's in your brain and it doesn't take that much effort once you've catalogued it, but it is a lot of effort cataloging it. So I'm interested to get your thoughts because I've asked this on the APL Farm Discord of: "what is the overall community's take?". And I think you maybe just said it; it is that a lot of the folks in the open source community feel like k6 is actually the language that, you know, the open source, or k folks ... [sentence left incomplete]

00:38:04 [JE]

It's the dialect that there's mostly agreement on. So in terms of open source implementations, there are three that I would say are ok and are in some degree of a usable state. Kona, as I said earlier, targets k3 and that hasn't been evolving very much lately (I think it still gets some maintenance from time to time); and OK (that's my implementation); and ngn/k [16] (which is Nick Nikolov's implementation), are both basically targeting K6. There are minor differences between them, but for the most part you write a program in one, it works on both of them, or it should [chuckles]. And OK is implemented in JavaScript; it's designed to be very convenient and easy to just try and it has a bunch of environments built around it that let you do things that are not: load a CSV file and sum a column and or you know, kind of the boring things versus, you know, draw shapes and colors and make sounds; you know the useless fun things.

00:39:28 [CH]

[chuckles] 2D graphics.

00:39:28 [JE]

So OK is kind of the slow one with lots of fun bells and whistles and then ngn/k is the fast one that I think is in the process of formalizing a C FFI. So maybe, eventually it will also have some pretty cool bells and whistles. But there's a lot of ground work that needs to be done between "I have a good language interpreter" and "I have an ecosystem that I can build neat things in".

00:39:55 [CH]

Interesting; so I think maybe I just got my answer. It's K6. If the open issue [sentence left incomplete]. I should respond, link to this episode when it's out, and say k6 will be the k used going forward and if Shakti  [17] and k7 and K9, you know, blow up at some point (and take over spreadsheets and excel and everything) then I can [sentence left incomplete]

00:40:15 [JE]

I mean, it's certainly possible, but I mean, no matter what happens with that, they're probably going to be proprietary and closed source forever. So if you want something that you can just download and play with, and maybe make modifications to; if you want something fun to tinker around with, and maybe draw some graphics or something, try OK. And if you want to do something a little bit more practical, use ngn/k.

00:40:39 [CH]

Awesome yeah.

00:40:40 [JE] And you can use either one to learn stuff that will be highly applicable to the other.

00:40:44 [CH]

Awesome. Stephen?

00:40:46 [ST]

Let me just try and recap what I think I learned from you, John, 'cause I'm a little slow. That was great to get the chronological history of the sequence of the different ks and dialect does seem like a good metaphor for them because Arthur's always been insistent that they're they're not different versions of the same language, and there's no pretense of backwards compatibility, so I'm thinking about which of the k dialects are actually, sort of, in existence and in use and if I'm following you, k3 is the earliest (is the oldest survivor); well embedded at 1010, but nowhere else. You've got to go work for 1010 to use it there.

00:41:30 [JE]

There might be one or two other places that have it, but it's very, very rare. You can't buy it, you know, as a company anymore so you either have it or that's it [hosts laugh].

00:41:43 [ST]

Then there's k4, which is perhaps the version most widely in use, underlying q; and you mentioned it's undocumented. I'll add to that, as the KX librarian, that it's also unsupported. KX doesn't promise that your k code will run from one version to another. However, the reality is it's actually very, very stable, of course, but we don't document it and we don't support it. We only document the q. And then there is K6, which again, if I'm following you, there's these two open source versions: the ngn/k and OK which are available but the Whitney k6 is not around, it unless it's lying around in someone laptop somewhere.

00:42:28 [JE]

Yeah, I mean I have a virtual machine that's sort of my k museum with a whole bunch of binaries and many dialects of this, including a number of K5s and K6s but I cannot share that with anyone because because it's all copyrighted material. You know, maybe I'll will a disk image of this thing to the Internet Archive with permission to release it 70 years after Arthur's death or whatever the terms are for these things at this point, but it's not something that's, unfortunately, ever going to be publicly available.

00:43:02 [ST]

And then there's the experimental k7 and the emerging K9, and who knows. But they're not here yet.

00:43:09 [JE]

Yeah

00:43:10 [AB]

I don't think k7 is available anymore; that was abandoned for K9.

00:43:15 [JE]

Yeah, just like k5 for K6.

00:43:16 [CH]

Yeah, this is awesome. We're getting like a encyclopedic history of the ks. I know Stevan Apter; he sort of gave us, when he was on, a little bit of the similar history, but it's awesome to get it chronologically like this all the way up to K9 'cause it's, yeah, it's like I said: probably it's the same way I said I have this knowledge about C++. It's probably frustrating for people that want to learn C++ and they start with the most recent one but there's this whole history of changes that is actually useful a lot of the times when you're going back through a, you know a Git history, and you know, at some point there was an upgrade from one to the other; And yeah, awesome to get this info, Stephen?

00:43:54 [ST]

I missed two, thanks. So Kona, an open source implementation of K3; and Kona is currently available?

00:44:02 [JE]

Yes it is.

00:44:04 [ST]

Yeah, and you also mentioned Kevin Lawler: Kerf. Is that an actual implementation of one of the ks or is it's quite closely related?

00:44:15 [JE]

So Kerf is a k-inspired language, or in some ways maybe more of a q-inspired language because it, you know, it has keywords and it has, you know, a very large collection of primitives compared to most of the k family languages. Maybe a little bit closer to how many primitives q has. It has an integrated query syntax. So aesthetically it's very much its own thing, but mechanically, you can see that there are a lot of features of the language where there's sort of a one to one translation of "here's the Kerf way of doing things" and "here would be the corresponding k way of doing things". And there are a few others; so Kerf was originally intended as a commercial product and that just didn't pan out. It is available with source code now, including the reference documentation is written by a fantastic technical writer and I think that he is actively tinkering with a Kerf-2. So I don't know very much about that, aside from the fact that it exists, but it's presumably in the same kind of lineage.

00:45:34 [ST]

Oh, by the way, when I when I got hired to work on the KX reference documentation, the Kerf documentation got shoved at me: said "look at this"

00:45:42 [JE[

Oh, wow. I mean I was really strongly influenced by the k2 reference documentation because that was how I learned k in the first place.

00:45:53 [AB]

OK, so that's the history, although I think it's a little bit different when you're comparing it to C++. Surely the C++ standards are mostly backwards compatible.

00:46:03 [CH]

Oh yeah, the two big differences are: 1) almost entirely backwards compatible and 2) the standards are completely [sentence left incomplete]. Well, I shouldn't say completely public 'cause the ISO documents technically you have to pay for, but there is a website that releases the drafts so you do have access to basically the ISO standards and there's websites that detail all of the evolution, so like it's all very, very public and it's all backwards compatible. The comparison, though, is that, like there are different (we call them versions, whereas in k they're dialects) ways to write things, potentially from version to version and keeping track of that, it's a task.

00:46:45 [JE]

Epochs of functionality in the language, mostly climbing uphill. Whereas in k it's a little bit bumpier.

00:46:55 [CH]

Yeah

00:46:56 [AB]

But see, there's a big difference: if you write something in C++(23) then it might not work in older versions. But if you write something, older version works in newer versions. Which means the basic functionality, core language, is much the same. I don't know very much about these programming languages, but I would imagine that (from just somebody getting started writing some basic things) it's probably more advanced stuff that's being added on top because the basic stuff is something that everybody needed from the beginning, so it was added right then, but that's not so for k. And we have the same thing for APL as well: the core language is the same across the board mostly, but in k, I would still like to have a table that says: these primitives, like the the most fundamental parts of the language, actually means something else from version to version, right?

00:47:48 [JE]

Well, there is actually a breakdown of how all the primitives do that on the k wiki. [18]

00:47:55 [ML]

Yeah, which is really nice.

00:47:56 [JE]

I think the user Razetime did a huge amount of the early work on sort of driving that forward, and I provided some clarifications. The open source k community, it kind of all emerged out of k5 and k6 culture stuff so we have kind of the advantage that at least the handful of dialects that sort of circle around this are quite similar to one another, for the most part and you know, the earlier versions of k are all commercial and extremely expensive (with the exception of of Kona) and a lot of the the newer implementations of open source ks have just referenced the documentation for OK as their reference guide. So it's less heterogeneous than it could have ended up being if the early versions of k were more accessible.

00:49:01 [CH]

And the bumpiness/difference (in that there are different ways to spell things); honestly I don't really view as like a huge cognitive barrier. For me it's the same thing as like translating in my head between BQN, J and APL. Like: there's three different ways to spell things. Sure, maybe because it's slightly more similar in the different k dialects, it might be more confusing, but I'm very used to cataloging different ways to write things programmatically (in whether it's Haskell, C++, whatever). It's more that it's less well documented just because k in general is a very niche language compared to languages like Python or Rust or C++, you know. When some new thing comes out in Python, there's a bajillion blogs you know, written about it, and like 17 different redundant stackoverflow questions. Whereas if I want to go find something in k there's way, way fewer blogs being written about the new thing in k6 or k7, right?

00:49:56 [JE]

Right. I mean, it also kind of helps that among all of the major array languages, if you pick any given dialect of k, it is by far the smallest and simplest. It has, you know the smallest number of basic primitives, although it has overloads on them; the syntax is the least daunting; it's just ASCII; there're few digraphs, you know, your curly braces and brackets and things always match ([chuckles] which is something that scares a lot of people about J). A lot of the mechanics of the language are very similar to LISPs or just garden-variety imperative programming languages.

00:50:45 [JE]

So like you can do things in a cutting-against-the-grain sort of way in k as if it were just a normal language, and then if you make better use of the language then it becomes more array-language-like but it's you know, it's syntactically regular; its feature set is small; it's the most, like, human scale in the sense that a person could just write an implementational language. Like when I started with OK, the legends about k5 were that Arthur Whitney implemented this entire language in about 400 lines of C. So I was like: "all right. well I, John, a normal programmer, ought to be able to write an implementation of this in about 1000 lines of JavaScript". And I did. I even limited myself to 100 columns which is not something that Arthur does [chuckles]. So you know, like within an order of magnitude of the amount of brilliance that was going into the original thing. It's human scale, like Forth is human scale; anybody can implement a Forth with a couple of weekends and a little bit of dedication. Anybody could implement a k if they have access to good documentation and test fixtures, which are something that's still, you know, a little bit lacking. Implementing something like J from scratch would be a much, much bigger project; possible, but very hard and you could make your own implementation of Python with a tremendous amount of difficulty and pain, 'cause it's a pretty hairy language. But then it's entire ecosystem? No way! So you know small things that one person could implement have a lot of intrinsic benefits.

00:52:36 [AB]

Maybe it's a good thing; it happens quite a lot that hobby APLers create hobby implementations of APL as well.

00:52:45 [JE]8

Yeah, and that speaks to the simplicity of the language.

00:52:47 [AB]

But maybe that's bad, because then you have a fractured community and ecosystem. J is so difficult to implement that there's only one J, as far as I know.

00:52:59 [JE]

Well, I mean some people could argue that the fractured ecosystem worked pretty well for Lisp, but maybe it didn't, because you know [incomplete]

00:53:08 [AB]

There's a reason for CommonLisp, right?

00:53:10 [ML]

I think it is possible that having you know one very strong open source implementation like J and possibly BQN as well (it hasn't been long enough to say), but I think that kind of suppresses people from making their own implementations, because I mean there's nothing you could really want more out of a J interpreter. [19] There are a few things, but there's nothing like life changing that you're going to add to the J interpreter that's worth, you know, building your own J for. Which, I mean, maybe if it was a very simple language, you could say, people would do that, but I think there's also the effect of having the implementation there already.

00:53:44 [JE]

Well and if you compare it to all of the other open source array languages, J has by far, the strongest and most mature ecosystem. Like you know, you could make a GUI application; you can load an image; you can do all of these things related to solving practical problems, in addition to having a nice language.

00:54:06 [ML]

Yeah, and to get any of that code running, yeah, it would be a huge amount of effort because J is very complicated.

00:54:11 [CH]

So is the OK implementation still 1000 lines of code?

00:54:14 [JE]

Yeah

00:54:15 [CH]

Wow!

00:54:16 [JE]

And it's actually written in a fairly older dialect of ECMA script so if I use some of the stuff like, you know, arrow functions and stuff, I could make it a lot smaller and neater.

00:54:31 [CH]

Maybe I should do a livestream of [incomplete but continued below]

00:54:34 [JE]

It's small, you can look it.

00:54:35 [JE]

[continuing from above] porting OK to TypeScript or something like that, yeah?

00:54:39 [ML]

Yeah, 'cause you tried the J thing, right?

00:54:41 [JE]

I guarantee that you could make it smaller and simpler with a fairly superficial amount of effort, because this is basically the program that I learned how to write JavaScript with!

00:54:54 [CH]

That inspiring!

00:54:56 [CH]

Yeah well, Marshall just mentioned, I had a, I don't know if it was like 15 or 20 livestreams totaling some ungodly number of hours, trying to port J from C to C++(20) and I think I got, I don't know, a handful of verbs done. Most of it was just like, plumbing of getting formatting and how to get the C code running with the C++ compiler. It sounds like doing something similar for OK and k6 would be like: I could do one stream. I mean actually saying that out loud, I realize I'd just be eating my words, but like: it probably wouldn't take, you know [sentence left incomplete]

00:55:36 [JE]

Well, the thing about TypeScript is, you start with JavaScript and then you just tighten the screws a little bit right?

00:55:42 [CH]

It's a very nice path.

00:55:44 [JE]

You know it's done when you decide it's done.

00:55:46 [CH]

That's that's very inspiring, though, that you you wrote this in 1000 lines of code while learning the language you were implementing it in.

00:55:53 [JE]

Yeah, and there's a lot of things about the implementation of OK that are like more complicated than they needed to be because they were based on fundamental like, you know, flawed assumptions about the way that the language worked. If I started over from scratch now, there are a lot of things about the semantics of k, like the fact that adverbs are syntactic entities, right? They have no meaning at runtime, really.

00:56:23 [ML]

They're just functions.

00:56:24 [JE]

Yeah, they're just functions, but you know when you first start you're thinking: "oh well, adverbs are one of the conceptual entities that I need to have floating around; I need to be thinking about applying over adverbs; and applying, you know? Monads and applying [incomplete]. You know, you start with assumptions like the fact that a nilad is a thing that exists when, very, very clearly it is not a thing that exists; it's just a convenient expression. There are lots of things that could be simplified about that code.

00:56:54 [CH]

Interesting, yeah, well, we'll definitely leave a link in the show notes to the GitHub repo and I will definitely be poking around in it and, stay tuned, maybe in the next five years whenever my cycles, free up, I will do some livestream of [sentence left incomplete]

00:57:08 [JE]

If you took a look at the implementation of Special-k, that's probably a little bit closer to, more like, the way that I would rewrite it from scratch today. So Special-k is a transpiler, and it's a significant subset of k but the idea is that you're converting k syntax and general semantics into GLSL, the OpenGL shader language. [20] You're writing a fragment shader, and the job of the fragment shader is just: you perform some calculations to figure out the color of 1 pixel on the screen, and then that program is applied in parallel as the final pass of doing 3D rendering. And I have some complications like the fact that I actually have to do type inference to make everything work. But if you compare the parsers, it has a similar kind of structure in Special-k to the OK one, but it's much simpler and cleaner.

00:58:10 [CH]

Wow. Is that open source as well?

00:58:11 [JE]

Yeah, I mean I just have it on on my website, but if you just go to https://beyondloom.com/tools/specialk.js or something like that. [21] It's just one source file and Michal Wallace bugged me a year ago to add an MIT license header to it, so that it's valid open source.

00:58:41 [CH]

Yes, yeah tips to all open source people, posting stuff on GitHub: always put a default license, even 'cause something without a license is very scary, especially to corporations, but even individuals. They'll see it and [sentence left incomplete]

00:58:56 [ML]

It's not open source.

00:58:57 [AB]

No, it's still open source, just not free. You can't use it, so you can look at it.

00:59:02 [JE]

Or it's free and it's not open source.

00:59:05 [CH]

Lawyers are, yeah, they view no license as the worst license. No, I shouldn't say the worst license, but yeah.

00:59:12 [ML]

Well, that's not just lawyers; that's the laws. He said if you don't license it, nobody is allowed to use it.

00:59:15 [CH]

Alright well, we're already at the hour mark, but I've already decided in my head, pending that my co-panelists agree, that you're going to have to come back maybe even if it works out time-wise for a part 2, like immediately after. We might have our first ever part-1/part-2 back to back. We're not going to end immediately 'cause I still have a ton of questions, and I'm not even sure if we got... 'cause we sidetracked you at some point when we started getting the history of all the k dialects ... I'm not actually sure you got to the end of your k journey. You were, I think, in the midst of telling us that you had just finished working with Kevin Lawler on Kerf and then you went to 1010data and then it was there I asked a question about the macro language and the k dialects, and then we veered hard left (which was amazing that we veered and I enjoyed the conversation). But so I'm not sure should we. Is there a remaining part of that story that we should come back to now? Or should we save that for Part 2? And maybe there is no? Part or should we go to? Q&A's that we might have about everything that we've covered up to that point. I don't even know as the moderator what to do here, so I'll just ask you, John, what should we do? And keep in mind, if you're free, we'll just have you back for Part 2. So we can answer whatever we don't cover there.

01:00:35 [JE]

Well, yeah, I. I guess I can, I can give you a little menu of things that. I could talk about so I haven't really talked about Ike. Which is a an interactive programming environment wrapped around OK. I haven't. I briefly talked about Special K. I haven't talked about Applejack, which is a fun little toy that I wrote and I haven't talked at all about Decker and Lil, which is my current array language adjacent big project.

01:01:04 [CH]

OK, I mean well, we'll ask. I'll ask the panelists, but my thoughts are. We should save. All of that for Part 2 'cause I still have a bunch of questions that pertain to things that were.. Like I've been trying to keep track in my head, but I've got so many that a couple of them have probably fallen off the stack of questions that I've wanted to ask about everything that's happened up till now so. I guess do the panelists or their nods of the head or shaking of the heads. I got a couple thumbs up, one nod. Alright, so we've decided live. Listeners stay tuned till either next episode if Johns available or sometime in the next couple episodes when we figure out scheduling. And I'll, I'll start with a question and the folks other folks have questions too.

01:01:44 [CH]

So one thing I wanted to hop back to. This is going be way back closer to the beginning of the interview, is when you started off talking about FORTH. It occurred to me that we've now had, I think, including you 4 guests. So I think the 1st guest maybe that mentioned it was Vanessa McHale [22] who had mentioned that she had done a sort of stack based language implementation. The name is going to escape me now, but she mentioned FORTH on that episode. Romilly Cocking [24] , when we had him on, FORTH also came up there and I guess Marshall when we interviewed you, before you were a regular recurring panelist. [25] And so actually, maybe that makes you first.

01:02:29 [ML]

I probably mentioned Factor.

01:02:31 [CH]

Yeah, yeah, I think you didn't mention FORTH, but you mentioned Factor and I've always wanted to ask Marshall.

01:02:36 [ML]

Because I haven't used FORTH.

01:02:36 [CH]

But yeah, we'll save that for another in my my third podcast that I'll launch. I'll bring Marshall on and we'll talk about that there, but so that's that's Marshall Vanessa  Romilly. Which is not a small number of the guests that we've had on that like FORTH has come up. So my first question is, after that long monologue that was probably unnecessary. How did you end up discovering FORTH? And do you think that there's something there that there's some connection or it just? It seems like an odd occurrence that on an array language podcast now out of however many guests we've had concatenative based stack languages like FORTH Factor Joy have come up on multiple guest episodes.

01:03:18 [JE] Well as for how I got into FORTH. Part of it is just a general interest in programming languages and to some extent, the esoteric programming language is sub community. Which is sort of a, you know an expansive hobbyist group of people who make little toy languages, often as a joke or sometimes to prove a point. And Firth is is one of these. You know, these Euclidean ideals of a language. That a lot of of random stabs in the design space end up sort of converging towards.

01:03:55 [ML]

Yeah, so actually I think I did mention that I made a lot of concatenative Array languages first. But I mean kind of before I wanted to care about the syntax because in a concatenated language there basically is no syntax. So that was what I would do for a while. I would write all these little languages that you know had FORTH or whatever like syntax and then array semantics.

01:04:17 [JE]

Yeah, a lot of people, think of "S-expressions" as being like the simplest syntax you can have. And in truth, concatenative languages have the simplest syntax because it's just a sequence of tokens that do something and you can create the illusion that you have nested structure if you want to, but you don't actually need it for those languages. As for whether or not there's some sort of deeper connection between array languages and FORTH. I think that philosophically very much so. If you look at k especially and FORTH, these are both languages that are made by eccentric creators with their own highly distinct style of problem solving that is centered on this idea of radical minimalism. In FORTH, you bend the problem in order to suit the language and the language to suit the problem. In order to try to find a balancing point where the entire system is as simple as possible. And in terms of languages, you know, FORTH is generally considered to be a pretty low level language. Although you can build it up to be suitable for a specific application. You know k is a comparatively, high level language, and frequently you're able to just solve problems directly in the language without introducing abstractions. But in both cases it's a system that has been like viciously attacked over its evolution. Constantly hacking things off and throwing away anything that doesn't carry its weight. So you end up with this thing that is uhm, you know. Instead of continuously growing and getting larger and more powerful, it is staying about the same size and becoming sharper and more effective.  And I guess what's a? Little bit tragic about k. Is because it's "closed source". For Arthur it is this unbelievable tool, where he can give himself more leverage by just tweaking a feature a little bit or adding a primitive or something. But for users of the language you don't actually have that ability.

01:06:31 [CH]

Wow, that is a. That is awesome. We got a clip. That we got to clip that, put it on YouTube, put it on Twitter's well. I mean, Twitter might not be around anymore.

I mean, I still think it'll be around, but the Internet seems to be disagreeing.

01:06:46 [AB]

By name.

01:06:48 [JE]

I mean, Myspace is still around for a really long time, right?

01:06:51 [ML]

That's about my analogy.

01:06:53 [JE]

Does Yahoo still exist? I think it does.

01:06:56 [CH]

That's true, yeah Yahoo Yahoo Finance is a it's it's. It's thriving.  It's doing great. That, yeah, paints like a picture in my head of a rainbow, where sort of FORTH is on one end of the rainbow and k and array languages on the other end.

01:07:11 [JE]

And another thing about it though is that FORTH and k are both heavily about mechanical sympathy in the language. [26] In k the the primitives generally map to simple, straightforward and predictable thing that the hardware is going to do. You know, modulo goofiness about modern architectures and automatic vectorization, and pipelining, and all this other junk. But like you know.... In general, it's a language about simple, predictable memory access patterns. Which modern CPU like very much and FORTH is a language about, you know. Don't throw up abstractions, don't add indirection, just you know. Treat the machine as it asks to be treated. Know about the intimate details of what's going on and and harness them. So it's, you know, it's mechanical sympathy in both cases. But it's it's attacking the problem from a different direction. Whereas, you know, there are other functional languages that sort of start from what would be the nicest way to express something. What would be the the clearest way that we could write our programs. And then as an afterthought I guess they have to run on a computer at some point. Maybe we can figure out a way to make that fast ... maybe. Maybe if we, you know, if we jab the the hardware designers with a stick, we can get them to do the thing that we want them to do.

01:08:43 [CH]

Yeah, what this really want? What I really want now after having heard you say that sort of wax rhapsodic on the philosophical connection between FORTH and k and array languages is there is Lambda cast [27] that exist, which is not really active but is a fantastic 21 episode podcast on functional languages. We've got array cast. We're thriving, slowly taking over the world. There's no OO cast. Which I've wanted, there was a a small talk podcast called Smalltalk something, but it's not active either.

01:09:17 [ML]

You should just get like Smalltalk.

01:09:19 [CH]

Uh, oh, yeah but I. Mean I like the the regularity of a, you know, insert thing cast. Uhm, which then brings me to now. Now I really want there to be like FORTH cast. Except I don't know what do you call it. 'cause like FORTH Factor Joy.  What do you call those like Concatenative Cast? That's a bad name, Statcast. That's too ambiguous.

01:09:37 [AB]

Casts FORTH.

01:09:39 [ML]

Well, but there is a big difference too, we've kind of glossed over it. But, uh. A lot of these stack based languages are very abstract and they they define you know what?

What these operations do without relation to the hardware. FORTH by its design is  supposed to really work based on the hardware so. You actually. I mean, you could build a different FORTH for every CPU architecture you work on. So there is a really different philosophy around those. And I would say FORTH is a lot more k like. And

some other stack based languages are more APL like where, where it puts more abstraction between you and the hardware.

01:10:18 [JE]

Certainly I mean Factor [28] is a very rich, powerful functional language that is pretty fast. And let's you know, dig down to a low level, but by nature it is pretty abstracted. The concatenative languages are sort of, you know, it's this theoretical design space. And FORTH is actually like the, you know the the. The grungyist most down in the muck of that whole family. Which also means that it's been, you know actually used to do those things.

01:10:49 [CH]

Yeah, I've heard that FORTH is a lot of the times it's used in like embedded places where you have a very very small, you know, constrained resources and you can get like something super small up and running.

01:11:01 [JE]

It is the only language where in like 8 KB you could have an editor and a debugger, and you know and the library and the language and everything just running on the little microcontroller that you're attached to with a TTY or something. And in almost anything that you could compare FORTH too, you're comparing for the live system on the little piece of hardware to the end result of this gigantic thing that gets distilled down and and baked. So really, you know, not all the same.

01:11:35 [ST]

If I remember correctly, the language was originally designed for running a telescope, and maybe even to run on a clockwork.

01:11:44 [JE]

So the version of the of the history that that I've read is that basically Chuck Moore, [29] the designer for started from the the point of he's working with with mainframes as a physics student. It's a big pain to have to like go and and punch a stack of cards and then bring them over to the computer and he came up with this with an interactive REPL system that would let him just compose, you know, a function on the fly. And this system evolved over the course of like lots of different jobs. He took this system with him from task to task, refining it, improving it, making the interpreter more efficient, and adapting it to this whole series of radically different weird domain frames. From you know the area that was in, so it was subjected to all of this buffeting and evolutionary pressure to stay small and to stay open minded about about computer hardware. And then the the version that ended up controlling radio telescopes was, you know? Chuck Moore finds his way to this job and like usually takes his system, customizes. It builds the solution to the problem and Elizabeth Rather was like a consultant who was brought on to I think, like document and formalize some aspects of the system that was running. And initially she was like horrified because you're telling me there's this gigantic codebase that's being used all the time and it's implemented in a language that this guy made by himself, and nobody else has ever heard of it? But you know, but she learned more about it and became kind of like the second or third FORTH programmer in the world, and eventually was one of the founding members of a FORTH incorporated. So what does that tell you about the impression that it ultimately made? He was kind of like discovered and then became this broader thing that there was more awareness of. And you know, books written about it, ports available for basically every 8 bit home computer any  tinkerer now had access to it. And there was this whole Cambrian explosion of FORTH stuff. And you know, unfortunately, a lot of. That stuff has died out just because. Uhm, the the languages that it's competing against. Could all get away with being a lot less efficient and a lot less interactive because computers were faster or more resources available. Portability became something that people cared about more and it's difficult to have the benefits of FORTH as it's intended and also have like a standardized FORTH that you can count on 'cause. It's it's supposed to be tailor made, you know, adjusted for it's environment. Every time a lot of people think that ANSI FORTH was sort of a bad idea, 'cause there is a standard and it's kind of complicated, and it's not as FORTHy as you might hope that it would be.

01:14:55 [ST]

It's interesting to hear the warmth of your enthusiasm for this language.

01:15:00 [JE]

Well, it's a. It's a nice language I like. It a lot, it's just not practical for solving most of the problems that I have today. But if I you know if I ever get an opportunity where it's a good fit, I'm absolutely going to use FORTH. If I ever have to write a a power controller firmware for an embedded device or something, that's being implemented in fourth, no question.

01:15:21 [CH]

Yeah, it's it's super cool. We'll leave links in the show notes as always. And I think one neat. Some fact about Chuck more and I don't think it has any relation to array languages, but he went later on in his career to found a company called GreenArrays or something like that.[30]

01:15:38 [JE]

So the GreenArrays hardware is it is a realization of... In FORTH you have a  particular virtual machine in mind that most FORTH's are built around, which you'd call a dual stack architecture. In a conventional, you know, PC hardware or whatever. You have a you have this model of having a single stack. In FORTH you peel apart activation records into return addresses on the return stack and parameters to the functions and the results into a second stack, the parameter stack. And these can grow independently of one another and shrink independently. And you can do a lot of really fun tricks by screwing around with them at at runtime. But so Moore did a lot of work on creating FORTH machines that were, you know, small, extremely energy efficient hardware that was designed to suit the the language and the language evolved to suit this hardware. The GreenArrays chips have the GA144 is kind of the famous one. It's 144 cores that are arranged in a in a literal grid. Every one of those cores is called an F18A and it has an 18 bit data word. A word can fit in a sense 3 1/2 instructions. With kind of an unusual and clever instruction encoding. Every one of those cores is extremely weak, and you need to gang them up and and network them together in order to solve and any kind of practical problem. But you end up with this kind of semi programmable systolic array. And it's completely radically wild way of performing concurrent programming on them. Like the the GA144 Dev kit is a pair of GA144's. One of which is running a complete GA144 development environment talking to the second one that's for your application. And you just you just plug the board in and connect to it with a serial terminal. And then you use one to program the other it's wild?

01:18:00 [CH]

How do you know so much about this? Did you end up getting one? Of those dev kits, or you just read about it online.

01:18:04 [JE]

I don't actually have one of the Dev-kits. But I read all of the the GreenArrays white papers, 'cause they're really interesting. And one of my computer architecture courses I wrote a little simulator for an F18A core and you know basic development toolchain for it. Because I just think it's it's really conceptually interesting. The challenge, of course, is finding problems that this is extremely well suited to is a challenge, because it's this boutique low volume hardware because it's waiting for a killer app. But you know in terms of just overall energy efficiency, the GA144 is insane. Compared like, if you're actually finding something that can dollars to donuts compare on. It's very, ... it uses sort of a clock less architecture. Because Chuck Moore discovered the clock synchronization was ending was dominating most of the energy consumption of his design, so he just got rid of it. And the whole thing was like, you know it was designed using circuit CAD and simulation tools that he wrote himself that was running on hardware. That he himself had designed. And as you know, this whole you know it, .... It's a fun, romantic image of the of the programmer, you know, actually levitating by yanking out his own bootstraps and and creating a guardian of pure ideology.

01:19:37 [CH]

Yeah, that's reminiscent of who was it that went in? Created the LaTeX language. Donald Knuth. [31]

01:19:47 [ML]

Can you create TeX.

01:19:49 [CH]

Oh TeX yeah TeX. Yeah he was working on The Art Of Computer Programming and then was realized that typesetting and, you know, wasn't good enough. So he had to go write a nice way to write his books and then a decade later he had TeX, you know, I just.

01:20:04 [JE]

And he ended. Up having to design two programming languages to do that right. 'cause there's TeX, and there's also TeX you know, sister Metafont, because he also needed a way to programmatically describe the typefaces to feed into TeX, so it could typeset nice things. That's where we get the computer modern typeface from. And you can actually use Metafont as a rather interesting interactive calculator if you're so inclined, because it's actually a constraint solving language. It's not like a general purpose programming language. I don't think it's turning complete, but it's very a very flexible calculator.

01:20:48 [BT]

From what I remember he did that also, sort of developed literate programming [32] that way too, because I think a lot of his documentation, the way he he could manage such an immense thing. He actually wrote novels about what was going on in the in the in the programming.

01:21:05 [JE]

Yeah, well, the whole concept of literate programming as as he originally defined it, was that it's not just that you have a nice concordance to go along with your source code, it's that you need to be able to freely peel apart the source code and rearrange it into a comprehensible form interspersed with explanations and diagrams and all that thing. So that's Tex and WEB is a is a system for writing a nice literate document in TeX and then having being able to process that and suck out all of the chunks of code and then glue them back together and it's a like a dialect of Pascal that he used.

01:21:45 [ML]

Now the crazy thing is, Co-dfns [33] was using this for like a few months and then he gave up on it I guess. But Co-dfns was almost Literate.

01:21:54 [JE]

Well, I mean it, a version of it was that there was also like a version of it that was written in scheme and ...

01:21:59 [ML]

Well, that was a long time ago.

01:22:01 [JE]

Well, yeah, but you know he went through, Aaron, went through a whole series of of iterations on making the thing, and then throwing it away to make make a new, better, clearer, simpler version. And I mean, when you're that aggressive about simplifying something. It's presumably possible to just get to the point where the linear order of the thing is clear. Enough and that. All you really need are comments, maybe as opposed to having, you know the the the WEB, reorganization.

01:22:34 [ML]

And Aaron never said like "you should be able to just look at the code and understand".He said read my thesis instead where it explains it.

01:22:41 [JE]

So it's true.

01:22:42 [ML]

But I think the literary attempt, which was which was sometime last year, was kind of an attempt to integrate that more closely. And he wrote, you know, 100 pages or so on it, and then throgh it out.

01:22:53 [CH]

Very Arthur Whitney-esk.

01:22:55 [JE]

You know, sometimes the the act of writing something and throwing it away and then starting over is just the process to get something that's clear and works well.

01:23:04 [ML]

Oh, definitely.

01:23:06 [JE]

One of the tragedies of the software industry is that. It's possible to subject our prototypes to real world conditions. Like if somebody designs a bridge and then make a nice little model of it, and they're explaining how you know "we've done the calculations and these are the stresses on and this is what we think it can stand up to". Nobody is ever going to like look at that scale model of the bridge saying well, "can we put this into production by start running cars over this?". How is, uh, I'll give you a week, how about you just spend, just take that bridge to span it across the the water will be fine. But with software like, that's always a real threat if you if you make a system that can be used as you know, as the real world thing then it will be. And we're not given the opportunity to make things that that we can then throw away unless you know an insane individualist carves out this space for themselves. Or if, unless we design toy environments that are specifically designed to make it so that you couldn't use them for anything practical, but they allow you to play with ideas and and tinker and and do that discovery process of what's a good way to do it, and that's what Decker is. As like a teaser when we do the Part 2. I suppose Decker  is a beautiful toy box that is not intended to have any economic value whatsoever, but it's fun and you can learn from it maybe.

01:24:41 [CH]

I was going to say that seems like a perfect place to end Part 1 of this two-part interview, unless if there's any folks that have a question right at the edge of their the tip of their tongue, not the edge of their tongue the tip.

01:24:56 [BT]

Of their tongue as an additional teaser. All my questions have to do with Part 2. Because as soon as you delineate it that way I thought "OK. I'm not gonna have very much to say in this part, but there's all sorts of stuff I want to talk about in the other one.".

01:25:08 [CH]

I mean I got halfway through well. We got halfway through this interview and I was like I don't know how this is going to work with like. I got a whole stack and even some of them I've saved, because I know I could ask them next time and I was like at some point I just decided as like it's fine. We'll just do part one, Part 2 there's. I mean we run this show we can do what we want, right? All right, well thank you so much John. This has been so fantastic. I know our listeners are going to absolutely love hearing all about this. Not just. I think k and the array language stuff, but I think the FORTH stuff is incredibly, at least for me, intellectually like makes me think you know of the differently about the landscape of these niche languages. And that they're more similar than than we might think. And like you said that there's a philosophical connection between them and, even comparing like when you were comparing Chuck Moore and and Arthur Whitney, I think is yeah. It's an incredibly interesting comparison, and yeah, thanks so much for coming on and sharing all your stories and thoughts, and hopefully we'll be able to get you back for Part 2. I mean we've been promising our listeners. You're kind of hoping hooked into it, so hopefully you're not disappearing up you know, Mount Everest for the next couple months or something. And we'll be able to get you on. I think I'll throw it to Bob who will plug our e-mail, which I always forget.

01:26:31 [BT]

contact@arraycast.com. And we do look forward to your responses and your questions and your observations, and I think there'll be a number that come out of this one, and I again I think it was fantastic. The amount of information I've got a much clearer sense of k now than I have ever had before. Really thank you for that.

01:26:52 [JE]

Well, thanks for having me, this has been fun.

01:26:54 [CH]

Yeah, thank you so much for for coming on John. This was awesome and with that we will say "Happy Array Programming!".

01:26:55 [ALL]

"Happy Array Programming!"

</details>
