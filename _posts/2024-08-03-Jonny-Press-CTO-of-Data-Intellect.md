---
title: "Episode 85: Jonny Press, CTO of Data Intellect"
date: 2024-08-03 00:00:00 +0000
episode: 85
keywords:
- array-programming
- array-languages
- data-intellect
- q
- q-programming-language
- aqua-q
- first-derivatives
mp3-url: "/assets/audio/episode85.mp3"
episode-type: full
explicit: "no"
block: "no"
layout: podcast
excerpt_separator: <!--more-->
---
Jonny Press has a long history of working with the q language from First Derivatives to KX Systems and now as CTO of Data Intellect. There are some stories to tell and Jonny is a story teller.
<!--more-->

**Host:** Conor Hoekstra

**Panel:** Stephen Taylor, Marshall Lochbaum, Bob Therriault, and Adám Brudzewsky

---

[Original episode on ArrayCast](https://www.arraycast.com/episodes/episode85-jonnypress)

## Show Notes

Array Cast -  August 2, 2024

Thanks to Bob Therriault, Stephen Taylor and Adám Brudzewsky for gathering these links:

**[01] 00:01:07**

- [Dyalog User Meeting](https://www.dyalog.com/user-meetings/dyalog24.htm)
- [APL Challenge](https://www.dyalog.com/apl-challenge.htm)
- [APL Forge](https://forge.dyalog.com/)
- [Tokyo APL/J/K Meetup](https://www.meetup.com/apl-j-k-meetup/)
- [Data Intellect](https://dataintellect.com/)
- [KXCon '23](https://kx.com/events/kx-con-2023/)
- [Nic Psaris' Matching Algorithms in q and kdb](https://www.youtube.com/watch?v=Cegm1cqbSs8)
- [York University (England)](https://www.york.ac.uk/)
- [Scheme programming language](https://en.wikipedia.org/wiki/Scheme_(programming_language))
- [Haskell programming language](https://en.wikipedia.org/wiki/Haskell)
- [Java programming language](https://en.wikipedia.org/wiki/Java_(programming_language))

**[02] 00:09:55**

- [First Derivative](https://firstderivative.com/)
- [Brian Conlon](https://firstderivative.com/)
- [/brian-conlon/Arthur Whitney](https://en.wikipedia.org/wiki/Arthur_Whitney_(computer_scientist))
- [q programming language](https://code.kx.com/q/ref/)
- [k programming language](https://aplwiki.com/wiki/K)
- [KX](https://kx.com/)

**[03] 00:14:34**

- [Data structures in q](https://code.kx.com/q/basics/datatypes/)
- [Nick Psaris Episode on the ArrayCast](https://www.arraycast.com/episodes/episode42-nick-psaris-q)

**[04] 00:19:40**

- [kdb+](https://kx.com/products/kdb/)
- [Moving Minimum in q](https://code.kx.com/q/ref/min/#mmin)
- [Over and Scan in q](https://code.kx.com/q/ref/over/)
- [Punched cards](https://en.wikipedia.org/wiki/Punched_card)
- [APL programming language](https://aplwiki.com/)
- [en.wikipedia.org/wiki/APL_(programming_language)](https://en.wikipedia.org/wiki/APL_(programming_language))

**[05] 00:26:18**

- [k4.topicbox](https://k4.topicbox.com/)
- [Code golfing](https://aplwiki.com/wiki/Code_golf)
- [Stack Overflow](https://en.wikipedia.org/wiki/Stack_Overflow)

**[06] 00:30:50**

- [q201](https://q201.org/)
- [Joel Kaplan episode on The ArrayCast](https://www.arraycast.com/episodes/episode27-joel-kaplan)
- [Dictionaries, Tables and Lists in q](https://code.kx.com/q/basics/dictsandtables/)
- [Select statements](https://code.kx.com/q/ref/select/)

**[07] 00:40:20**

- [High Frequency Trading](https://en.wikipedia.org/wiki/High-frequency_trading)
- [Rapid Development Cycle](https://en.wikipedia.org/wiki/Rapid_application_development)

**[08] 00:43:27**

- [PyKX](https://pypi.org/project/pykx/)
- [Python programming language](https://en.wikipedia.org/wiki/Python_(programming_language))

**[09] 00:45:54**

- [Shakti](https://shakti.com/)
- [Open source Jq](https://www.timestored.com/jq/)
- [k wiki](https://wiki.k-language.dev/wiki/Main_Page)
- Contact AT ArrayCast DOT Com (edited)

<details>
<summary><strong>Transcript</strong> (click to expand)</summary>

Transcript

Transcript prepared by

Sanjay Cherian, Igor Kim, and Bob Therriault

Show Notes

00:00:00 [Jonny Press]

You know, you solve the core of the problem first and then you kind of build the bits out around it, right? You don't spend days, you know, defining classes and inheritance structures and all this stuff. And then you're, you know, and then you get this problem solving bit and you go, well, I forgot what I was trying to do here in the first place.

00:00:26 [Conor Hoekstra]

Welcome to episode 85 of ArrayCast. I'm your host, Conor. And today with us, we have our four panelists plus a special guest who we will get to introducing in a couple of minutes. First, we're going to go around and do brief introductions. We'll start with Bob, go to Stephen, then to Adám and finish with Marshall.

00:00:42 [Bob Therriault]

I'm Bob Therriault and I am a J enthusiast.

00:00:44 [Stephen Taylor]

I'm Stephen Taylor. I am a APL and q enthusiast.

00:00:48 [Adám Brudzewsky]

I'm Adám Brudzewsky. I'm an APL enthusiast.

00:00:51 [Marshall Lochbaum]

I'm Marshall Lochbaum. I'm a Singeli enthusiast, but I like BQN because that's how I program Singeli.

00:00:57 [CH]

As mentioned before, my name is Conor and I am an Array language enthusiast across the board. With that out of the way, I think we've got a few announcements all from Adám, so I will throw it over to him.

00:01:08 [AB]

Okay. Every year Dyalog has its user meeting and the deadline for guaranteed accommodation to this year's user meeting is Monday, the 12th of August.[01] And then by the time this episode is out, there will be a new round of the APL challenge live. So yeah, third round of that. And this time it is geared, especially towards a very much younger audience. In fact, I had my 10 year old and my 12 year old proofread everything to make sure that the language is understandable and concepts are reasonable, not making weird assumptions about what words mean in English for a programmer. Then together with the APL challenge, there's also something that Dyalog has called the APL Forge, which is it's kind of like a starter incubator system where people can submit some project or module that they have created. And this panel of APL judges buys the one that they like the best and they win some money and some guidance and help to take that project further. And the winner has been announced for this very first time. We have the APL Forge running. So we'll have a link to that. I'll leave you in suspense until you go and find the link. And then there's the Tokyo APL/J/K group. They have a meetup on August as well.

00:02:31 [CH]

Awesome. So links to all of that will be in the show notes as always. And that brings us to our introduction of today's guest. His name is Jonny Press, CTO of Data Intellect formerly under the name of another company, but we'll let him get into that. And I believe before, and that's, I think for over a decade, you've been CTO at Data Intellect. You can correct me if I'm wrong. I believe you also worked at First Derivatives and KX before that. And before that you were a KDB plus engineer at a couple of different companies. The first time Jonny and I met was at KX Con 2023. If I've got the years, correct. It seems like a long time now. I think it's been over a year and we met at that conference. I think his name has come up a couple times, at least once, I think because when Nick Psaris was on, Nick gave a talk at KX Con 23 and he brought up 10 q gods and Jonny, I think infamously, at least for all the attendees of that conference became an almost, or so I said, k god, q god, he became an almost q god because he didn't actually make the list of 10 people that Nick enumerated, but he tried to get up on stage anyways. I can't remember if you ended up being on the other side of the 10 folks, but it was a very hilarious moment. And I think we actually caught it all on camera. We will link Nick's talk from KX Con 2023. But we'll throw it over to you, Jonny. Maybe you can, if you want to color that story a little bit more, and if you want, take us back to, you know, the very beginnings of your careers and tell us the story of how you ended up at Data Intellect and sort of your path to q and the Array Languages.

00:04:07 [JP]

I guess it was kind of a funny one for me. So I never really had much interest in computers, to be totally honest. So I did at school, I was kind of maths and science and physics, and that was kind of where I was at. And you would go to go to careers fair and you go to counsellor in school and just sort of the background and the subjects I was doing, you know, the answers were, oh, you should be a doctor or you should be a lawyer. And I was kind of like, I don't really think that suits me. And there were some people came in and gave some talks at one point, and one of them was an engineer. So basically, they sort of explained a bit and then I talked to them and said, OK, engineering sounds good. So I thought, OK, maybe it's an engineer I should go and try and be. I've never really had any particularly brilliantly mapped out career plan, to be totally honest. It's kind of just, you know, do things that you enjoy and see what happens, really. So I ended up kind of, you know, in the UK system, you've got to put six courses down and I basically put down maths, but mostly engineering courses. So sort of electronic, not even electronic engineering, so like mechanical engineering, aeronautical engineering, that kind of thing. And I put one computer science course at the end of the form, basically to fill up the form, fill up the last spot in the form. And then we went and had a look at some of the universities. I went over with my dad over to England and we went round three of them. And I went to the university I went to was York in England and went there, had a look at the computer science department and just really liked the place. I spoke to one of the people, really liked what they said, really liked the sound of the course, kind of, you know, the sort of the mathematical element to it and ended up kind of deciding to go and do that. So turned up first day in a computer science course and was, you know, kind of, I don't know, it was probably this was the end of the 90s, right? And, you know, the majority of the course were that, you know, if you think about somebody who sits in a room and does computer programming, that's all the people who were on the most of the people who are on the course looked a bit like that. So, you know, day one, you get access to the computer room. They're all piling in, you know, going straight on to Linux terminals and starting to do stuff. And I'm there going, I don't know, you know, I didn't do I didn't do any computing at a level. So I was kind of coming from a very basic level. But, you know, the course kind of suited, right? You know, it's, you know, computer science is a proper scientific engineering, mathematical discipline. So, you know, there's actually the course I did, there was relatively little actual programming in it. There were some we did in a 95, we did Scheme, we did a bit of Haskell. We did we did a bit of C. One of the courses we did was building a compiler for C, which I still wake up with nightmares over, because it was just like, I don't know why we're doing, you know, I don't understand any of this. And I don't understand why we're doing it. And, you know, the point I was coming from was like, I now understand why we were doing it. Right. But the point I was coming from at that point, I was like, if you go and do a course of how to be a mechanic, you know, you don't spend three months learning how to make a spanner. Right. But, you know, I now kind of under I now get why why we were why we were doing that. And then I did a placement year in university, and that involved quite a bit of Java. And then I spent a year trying to do stuff in Java and mostly failing and getting frustrated. You know, we were using it was like Borland, I think it was at the time. And it just felt to me every time you tried to do anything, you know, you basically had to set aside two days to set up a project correctly. Right. And, you know, put all the classes building to the right place. And, you know, and I just, you know, sort of wasn't really being taught either. And I was just kind of cobbling along and wasn't. And then, you know, I still find Java a little bit weird. You know, it's like you write a program and then you write a program to test your program. And then you're like, OK, well, what bits broken now? You know, it's like, have I is the program broken or is the tests for the program broken? You know, I know it's all come along a bit since then, but, you know, it was I felt like I was in this like endless death loop. So I'm thinking back now, I don't know why I ever persisted with software development. Should have given up at that point and gone and been a doctor or something like they said I should have been. I got a job in Belfast. So I'm originally from Northern Ireland. Went away to university, placement year also in England, then kind of came back, got a job at Belfast, which I left about three months in, realised that wasn't for me either. It was doing something with like workflow processes, which, again, I didn't really understand. Maybe the career history here is me walking away from things I don't understand. Then I joined, applied for a job in First Derivatives and I joined FD. So it was still a relatively small company. So First Derivatives [02] at the time, the rights to sell and and they did all the consulting work for KX. you know, basically that story is that Brian Conlon, who's the CEO of FD, went to a conference in California in the late 90s and met Arthur and they saw what he was doing with the language and they together a deal where KX could do or FD could help with the selling, do a lot of the consultancy. So, you know, Brian and FD started training a whole bunch of q developers, well, k developers originally and then q developers in Newry. So I joined FD in Newry and I was told on my first day, don't learn k, just learn q, use this new thing. So I was like, OK, right. If Brian told you to do something or not to do something, you did exactly that, whatever that thing was. So basically I started learning q. There wasn't really a set pattern at the time, but I sort of immediately kind of enjoyed it, you know, because it was kind of like it was the interactivity of the environment. You type something and you get a result immediately back. And I was like, oh, wow, this is a bit different. You know, this is actually this makes a bit more sense. I can kind of think things through and, you know, I can write something and I can test it and then I know whether I've got it right or wrong or not. And I don't have to write a whole other separate program to do that. I can just get on with solving problems. But, you know, it was kind of like I had no clue what I was doing. You know, there was a lot of us. But the lovely thing was there was a lot of us who didn't really have any clue what we were doing. And we were answering support tickets for fairly large clients. But, you know, because the technology at the time was so young, you know, it was literally it was like 2004. So I think in terms of the, you know, the generation, it was k language. KDB+ was released in 2003 or 2004, you know, which is basically k with the database element that the q language wrapper on top. So we were all still kind of getting the grip, getting the grips with it. And, you know, there was very few people who knew how to how to really do it. So, you know, from that point of view, we weren't particularly disadvantaged that we didn't really know because we had time to try and we had time to learn. And we were kind of learning off each other. And there were some people who were really, really good, like still, you know, really young guys still, but they knew lots. And we would, you know, our method of learning was trying and then getting stuck and eventually, you know, smashing the glass and, you know, calling one of these people and said, you really need to give me a hand here type thing. So and we were trying to get these support tickets turned around for large clients in quite short time frames. So it was an interesting learning environment. But I think, you know, what it kind of did do was go in terms of learning the language. It was, you know, there's obviously loads more resources available to help out with that with this kind of thing now. But there wasn't really much at the time. You know, there was a three page document that Arthur wrote that, you know, probably a huge effort for him to make it as long as three pages. So we were just kind of like, you know, using that and trying to learn off each other. The thing I find was that when you're learning, certainly whenever I was learning anyway, it's obviously not the most straightforward language in the world, right? It's a mindset shift as well from, you know, anything that I would have tried to learn from a Java point of view in terms of how you have to think about problems. You know, that vectorized way of thinking is substantially different. So you got to do the mind shift change, you know, the syntax with all the overloads is, you know, you think you learn what a question mark does and you go, OK, great, I know what a question mark does. And then you look at it in another context and you go, that's not doing what I thought it was doing. And then you sort of go, actually, there's like 15 different things that a question mark does. But if you're learning that as you go, it's tricky and you sort of you kind of reach these points. And for me, it kind of felt like I reached a point after like three months, I actually know what I'm doing now. And then after six months, I was like, oh, no, I now actually know what I'm doing. And then probably two years I was like, no, I definitely know what I'm doing now. And then five years, same feeling. I think, you know, maybe eight or 10 years into it, I was like, oh, no, I actually probably do know what I'm doing now. It's just this sort of stepping. But that's quite rewarding as well. Right. You know, because you sort of you feel the improvement. And for me, it was there's certain principles that I think if you learn at the start, then it helps you massively in the understanding. Right. You know, it's like if you understand the concept of a list. Right. And just, you know, everything's a list. Right. And all the operations in the q space are on lists and the columns of a table are a list and the table itself is a list. And then once you kind of get your head around that, you go, it kind of all fits together. You go, OK, now that makes a lot more sense. Right. And, you know, once you can do a list or know how to operate through a list, then you can do most of it, really. [03]

00:14:42 [CH]

So that brings you to your time at First Derivatives and KX. And at what point, because First Derivatives ended up acquiring KX at some point, right? Did that happen under your tenure there?

00:14:54 [JP]

That's quite funny. So I think FD always had a small shareholding in KX, like as a part of that, I think as a part of that original deal. But then over time, I think they kind of increased their shareholding. I think whenever I left, so I left First Derivatives in about 20, was that 2013? 2012 or 2013? I think they owned about 22%. So I left FD and I joined KX. So I was working directly for KX as a pre-sales engineer. So a lot of the stuff I'd done towards the end of my time with FD was kind of pre-sales engineering. So whenever I left FD, I joined KX and then I joined what was AquaQ at the time, now Data Intellect. And then sort of about two years after I left, you know, we were essentially, we were, AquaQ were predominantly KDB+ consulting. So at that stage, we were competing with First Derivatives. And then First Derivatives bought KX and we were like, "Hmm, okay, that's a shift." Yeah, so that was uncomfortable for a little bit. But yeah, so yeah, and then, you know, then they sort of ruled, they ruled everything together and, you know, sort of became sort of FD Technologies essentially.

00:16:08 [CH]

So wait, you were at First Derivatives and then you went to KX after First Derivatives while they were only partly owned. Yeah. And so when you were at KX, they weren't like the, because technically I think some people, it still says on LinkedIn that they work at KX, even though like KX is under the FD umbrella now. But when you were at KX, they were separate entities. Yes. And then you ended up going to a consulting firm.

00:16:17 [JP]

Yes, so a competing consulting company. Yeah, so that was fun times.

00:16:32 [CH]

And then shortly after, KDB+ and KX was bought by First Derivatives. So the technology that you were doing consulting work for was now owned by another consultant. So how did that iron itself out? Like they decided that other folks are more than like welcome to consult and they tried to be friends or?

00:16:55 [JP]

We just kind of continued along and then, you know, at the same time, it's kind of, you know, we are, we were consulting for the clients, right? So it was the clients who were employing us, the customers of it, uh, the customers of the product were employing us. It wasn't kind of KX or it wasn't FD. So it kind of, it was, it was mostly all fine, but so yeah, whenever I was at KX, they were still a very small company. So I think whenever I was there, I was very incredibly proud of my Jonny@kx.com email address, which, you know, makes it even more of a kick whenever Nick Saris says I'm

not a q god. But so I think there was maybe like seven or eight people. So I was doing like pre-sales in Europe, which, uh, was, was, you know, I think there was like two of us in Europe at the time and there was, you know, Arthur and Charlie and Fintan. Yeah, there was Jeanette and Pierre and Oleg were there as well. I can't remember getting, getting hazy here.

00:17:45 [CH]

OK. And so wait, so maybe you're saying Pierre and Oleg used to work at KX as well before they worked at First Derivatives potentially.

00:17:54 [JP]

I think we did. I can't remember. I think we did though.

00:17:56 [CH]

We'll have to have them on if they're listening. They're probably not. [laughs]

00:18:03 [ML]

Have Pierre and Oleg ever like acted as, as separate individuals? Like, have they ever been seen in different rooms?

00:18:09 [JP]

I don't think so. I don't think I've ever seen them in different ... [sentence left incomplete]. Yeah, that's a good point [chuckles].

00:18:13 [CH]

I do think at KXCon 2023, one of them left the conference before the other one beause I remember finding, I think it was Pierre and I was like: oh, where's Oleg? And he's like: oh, he's gone. So I do know that at least one of them has been seen solo. Not the other one, technically.

00:18:32 [BT]

But everybody seems to fall into array languages in a different way, but it's often not planned. They often start out in another area and then sort of drift into this, get interested in this and go on. If you were going to give advice to anybody who was thinking about programming in the array languages, what would you tell them to look out for? Where do you think the low hanging fruit is for somebody starting out?

00:18:53 [JP]

Uh, well, I guess I would say for me, so I love programming, right? I love programming because it's problem solving, right? One of the things that sort of annoys me (well, not annoys me, but you know, a slight frustration) that I have at the moment with my current role is I don't get to do enough actual programming, you know? And people keep telling me: "you're not supposed to be doing programming anymore". And I'm like: yeah, but I want to [chuckles]. But then having said that there's been other days where I've like ditched myself you know, head first into an actual like delivery for a client and done programming for a full day and being absolutely exhausted at the end of it. Because it's just like: "my brain's so tired now, I need to go and lie down in a dark room". But to be honest if I hadn't ended up doing KDB+ or q, I probably would have gone right below  "programs is not for me; I just don't get it, right? I don't understand what everybody's doing here that's so interesting or so rewarding". Because in other languages it just always felt that it took so long to get to the part of solving the problem, right? Whereas with certainly in my experience the way that it works in the q space is, you solve the problem first. You solve the core of the problem first, and then you kind of build the bits out around it, right? You don't spend days defining classes and inheritance structures and all this stuff. And then you get to this problem solving bit and you go: "wait, I forgot what I was trying to do here in the first place". So if I was giving advice to somebody, I would say: "yeah, absolutely give it a go". We do a lot of recruitment and training. We take in graduates and we train them pretty hard. It's kind of one of the things that I think we do quite well as a business. But the graduates we get tend to be from sort of physics and maths backgrounds. Computer science as well, but for this side of the business (we have this other side of the business that is more software engineering oriented) but for the time-series, KDD+ oriented side of the business, [04] we find that actually a lot of the time not knowing any other programming language is beneficial. Because we sort of teach from the bottom up and it's kind of more of the mathematical, logical problem solving mindset. [That] is kind of what we're looking for. And we go: "okay we'll take it from here". We'll day one, throw them at a Linux terminal and they all had the same experience I did in my first day at computer science [chuckles]: "how do I send email from here?". But I would say if there was advice, just kind of go for it. It's very rewarding. It's a different way of thinking. I think back to some of the stuff where I was just like blown away and it maybe comes from the fact I didn't kind of learn k. You know, I was just sort of living in q world and in KDB+ space some of the keywords have an underlying implementation in the binary and some are just bits of k. I can't remember which one ... it was moving minimum. I sort of started looking at the definition of a moving minimum and I kind of had this conceptual notion in my head of how it would work. You know, you'd construct a window and you'd kind of iterate through an array and then you look at the implementation, you go: what is that doing? There's a couple of adverbs strung together in there and basically it's taking the whole array and then it's shifting it and it's anding it with itself and moving through and it's doing that N times as to how big the window is. In an over  Or is it a scan? I can never remember which one's scan and over. Every single time I do them, I've got to do it out on the keyboard and go: "that one's scan; that one's over". That's why I'm not a q god. That's why I'm not a q god. [everyone laughs]. I remember looking at it for like two days, trying to work it out and then eventually worked it out and was like: "right, okay, I get that now". I think in q there's a lot you can learn. There's a whole load more documentation, but to learn it properly, there's still a lot of just staring at random characters and banging your head off against the wall for a little bit until you work out what's happening.

00:23:16 [BT]

But one of the things you mentioned that attracted you in the first place compared to other types of programming was the interactivity. And honestly, I found that was one of the attractions I had when I did my computing science degree. It was batch programming. It wasn't quite cards, although I did go to an institution that did have cards for a while [chuckles]. You ended up submitting a batch and then you'd stand around for three quarters of an hour watching your little thing crawl up the screen. And eventually you found out where you'd made a mistake and you have to go back and do it again. I found that incredibly frustrating. And as you say, there's a lot of ceremony that you go through before you're even into the problem. Whereas when I started, I had a chance to play around with some APL and it's like: bang! answer's back. Bang! answer's back. Now it can be confusing as you say. You spend a lot of time staring at the screen, but you can try things out. And I found that was my way of learning is that if I could get quick responses, that feedback loop is short. I can learn much quicker. If I have to sit back and (I don't say ponder, because there's a lot of pondering that happens in mathematics and I know that that's a different type of thinking), but if I had to sit and wait to find out how things worked out, to me, it's just so hard [laughs]. I guess I would say to somebody who was studying on computing science, if you find it really hard, maybe try a more interactive approach.

00:24:33 [JP]

And, you know, I think for a lot of the sort of the analytical tasks that people end up doing in the KDB space, they're investigative. You're trying to form an idea in your head as you're going through it. And if you did have a wait loop, even if the wait was 15 seconds, for me anyway, I would just lose the train of thought. You're just kind of like: why was that like that? Whereas instead of just being able to get that performance from the language. So it's the rapid development loop that's very appealing and very rewarding. It's a very expressive language. You can write complex things quickly and then they also execute quickly, from an implementation perspective. You can, in an afternoon have done something that in another language [takes] days or weeks. You'd have to go and get a BA to spec out for you and create a document and you're like: "well, I've already done it". I'm not saying that because I'm a super genius or anything. I think it's the nature of the language and it's the nature of the way you work with the language as well.

00:25:47 [ST]

If I was following you, you've done quite a bit of programming in a whole handful of languages before you came to q and it's only after that ... [sentence left incomplete].

00:25:59 [JP]

A lot of bad programming.

00:26:02 [ST]

Well, we've all done that [chuckles]. It's only after that, that I was hearing you speaking with joy and enthusiasm, about coding. Does that sound fair? Was it only with q that you discovered joy in coding?

00:26:14 [JP]

Yeah absolutely. I would have got there with other languages. The K4 list box [05], we used to live or die over. It was kind of funny; it's kind of weird whenever you think about it now because there was this distribution ... [sentence left incomplete]. Somebody occasionally still sends emails to it. I don't know how it works; who it is anymore or whatever. But it used to be very busy, in like the 2000s or whatever (whenever KDB+ was like kicking off). Somebody would ask a question and I'm sure (I was working in London at the time) I would drop everything, right? I'm sure I was not the only one in one of these banks who was doing the same thing. It was like a race. [laughs] Who can get the best answer to this question? And there was so much like one upmanship as well. It was like: "I've shaved four milliseconds off this or whatever". There was always an element of golfing to it as well. I'm sure there was production issues going on in banks which got completely ignored because people were trying to come up with a code golf solution to some question that some guy they don't even know has asked on the list box. Then Arthur or Charlie would chip in with answers sometimes and, especially if Arthur dropped one, I'll just sit there and go: "I'll need to sort of study that for the next two hours". And that would be your day. But it's kind of weird because it's probably also one of the issues with KDB and KDB systems. It's kind of this notion of terseness;if you could compress your answer. Nobody ever stated the rules but to me the rules were always: the fastest solution wins. Then if there's not a lot in the fastest, it's the shortest. So you know there's golfing and there's performance which is kind of weird. There's this idea that we should make everything as short as possible all the time, which you know definitely has advantages right? Definitely advantages to having succinct code but stringing multiple reassignments in the same statement with single character variable names creates its own support opportunities.

00:28:55 [ST]

And to give credit where it's due, the Data Intellect dudes if not q gods at least Demiurges are still regularly active on Stack Overflow, answering questions and providing guidance. I'm particularly interested in the experience of, I've called it joy. Because I'm recognizing a pattern here. I'd done some programming and thought it was kind of okay until hundreds of years ago I got shown APL and I just didn't want to code in anything else after that. I'll speak I think for Gil Athoraya, who these days hosts the Swedish APL conference. He too had done a fair bit of of coding as part of a training in electrical engineering. He didn't think much of it until he came across APL and just thought: "ah, there's there's joy and pleasure in this". So the question I'm working my way around to is now you're taking in all these people at Data Intellect and training them: are any of them showing the same signs? Do other people have this experience too?

00:30:02 [JP]

I think so. I think with a lot of people that have limited or no prior programming experience really enjoy using the language. There's others who sort of go: "I don't really I really don't get this" or "this just boggles my mind", which is you know fair enough as well. But absolutely, we would do things internally to try to keep things interesting and people post to internal channels or set up challenges. We setup challenges and things like that, just to kind of keep it going and a little bit different from the standard kind of problems that that everybody sees. But yeah, like you mentioned, we join in the stackoverflow pieces and k4.topicbox community site  as well. But yeah definitely for some people. Definitely for some people.

00:30:51 [ST]

As you know, Jonny, I've spent much of the last year working on a project called Q201, [06] attempting to introduce people to the array programming paradigm that you were talking about before. And I truly suspect that Data Intellect has way more in its archives and on its servers, of material of this of this kind. I'm struggling along in your wake. However Q201 is available publicly and Data Intellect is its own garden. Can you tell us anything about that transition, from what a previous guest on the podcast called "one potato, two potato programming" into the array paradigm? Is there anything you learned about how to help people through that?

00:31:40 [JP]

We would do training courses and things where there's people coming in who come from other other backgrounds. And it's just, we spend a lot of time on those training courses, on the data structures. The base data structures basically: atom, list, dictionary. And focusing in the understanding of, that's all you have really, right? So a table is a list, a key table is a dictionary, and the reasons for that, such that if those are the only data structure supported, then all the native operators operate on these three types of data. Put this in and this is what you get out, right? And I think that kind of: table is a list; the columns of a table are lists. Once you start thinking about lists, you start to understand how you can do some of the really complex select statement syntax. Because I think where we kind of struggle is that people go: "I just really want to be able to do really cool selects, right on the database; do these mad manipulations within a single statement". And you're like: "okay, fair enough, but here's some things that you have to understand first". And some people get it really, really quick. You know, I worked with a guy who was a quant, who had [a] programming experience background. And I sat with him for like a morning, then came back two days later and he was much better than I was. It was just like: "oh no; I've been at this seven years at this point or something". It's just that core understanding, you know, like a by statement in a select. What it's doing is it's breaking a big list into little lists. Then you got to know how to aggregate or operate over that little list. And then once you can do that, then that's the game, right?

00:33:32 [ST]

Right. I've got a ton more questions as Conor always says, but I think it's time I step back and let someone else have a nitchew.

00:33:39 [CH]

Well, I was going to ask at one point, and maybe Bob will make you rearrange this or maybe not. Maybe we'll let the listener wait. I think it was K4 list box is what you were saying. If I was hearing correctly. I imagine that was just some kind of email list that something showed up in your email box, but do you mind rewinding a bit and just talking us through what we all, you know, missed it? Or not all of us, some of us were able to participate. I myself was not able to participate in this K4 list box. Was it just an email list or what exactly was it?

00:34:10 [JP]

Yeah. So it was like an email list for customers of KDB+. Yeah, that's pretty much what it was. And you could ask questions and all the customers were on it. So it wasn't sort of like, you know, you sent KX a question, then they sent you back an answer. It was basically just, it was kind of like a, well, I guess it was ultimately like a group or whatever. And just everybody was answering everybody else's questions. So, you know, somebody could send in a question and somebody else will answer it. So, and it just dropped into, it just dropped into your mailbox. And yeah, it was just, that was, it was good. It was good. You know, it was just, it was a, how quickly, you know, and you know, you'd be like, look at the timestamps and, you know, then, you know, there's, Attili used to beat me a lot, but he didn't cause he sat beside me. So if I knew he was doing it, then I wouldn't bother. But, you know, other, you could see other people coming in and, you know, I held my own at times, which was enough for me.

00:35:08 [CH]

It is very cool to think that, you know, for a period of time, and I guess this is a great way to transition into, cause you know, one of the things I wanted to get to seeing as we have a, you know, CTO of a consulting company for, you know, not just q, but is one of the main technologies that you consult on and KDB plus is the kind of the state of the industry and, you know, who uses q and how it's being used. But it is, you know, before we transition to that, it is cool to think that, I think it's well known that KDB plus and q it's a huge sector that uses it is the finance industry. And that like back in the day, there was a bunch of, you know, quants or, you know, people using this technology that a little expression would show up. Is there a better way to do this? And then everyone would stop across all the banks, you know, regardless of what market was open. And then everybody started golfing or, you know, trying to speed things up. And then Arthur would weigh in that, that must've been a fun experience. Cause definitely, you know, I work at a tech company, but there's no like mailbox where, you know, other major tech companies like Google, Apple, like something, a problem shows up. And then, you know, a few key members at each company, you know, pauses there. There's nothing that exists like that, that I know of, or maybe I'm just not a part of it, but that sounds very cool.

00:36:22 [JP]

Yeah, no, it was cause you know, if, if, if people, you know, people who posted first sometimes didn't really know how to frame the problem correctly. If you know, they put in like a big wordy thing or whatever with some ambiguity. Right. But then, you know, other people were like, you know, here is my data. Here is what I want to get out of my data go. Right. And, you know, because, you know, it's because, you know, you could just, you could lift the data off the email, you know, and drop it into the interpreter. Or, you know, if you're all running off the same random seed, right. And the interpreter, then you, and you, it's a random generation, you all get the same random data. So, you know, then you were all working off the same base and, you know, then, you know, you could be like sneaky and stuff and go like, Oh, well, you know, is that data really rep, you know, what, what if it like, if your data looks a bit like this, this is a better, a better solution and stuff like that. So it was, it was, it was good fun while it lasted.

00:37:17 [CH]

And yeah, so speaking of the transition, do you mind telling us a bit about, because I mean, we get a mix of the folks that we end up interviewing on here, but very rarely do we have, or not very rarely, but it is an opportunity to ask someone, you know, with a C in front of their title about the, the industry and how folks are using these array languages. And I think q and KDB plus is really a special case because it is probably alongside Dyalog, APL, one of the main array languages that is actually used extensively in certain industries. But, you know, we don't hear about it as much as obviously languages like Java, et cetera, because it's, you know, I, I wouldn't say more niche necessarily, but it's, it's shows up more in certain industries than others for sure. Anyway, so any sort of, you know, color or, you know, background you can give us about where your clients mainly coming from, you don't need to name drop any, but like, you know, what are the kinds of things that, you know, clients are using to solve? Is it all finance? Is it, you know, 80, 20? I'll let you run with it from there.  Well, so the C, right?

00:38:17 [JP]

I only got the C because we had to make up job titles for ourselves about six or seven years ago. So I took that one and other people took all the other C ones. So that's how I ended up with that. But the history of KDB+Q is finance in the finance domain and it's used for capturing, analyzing huge volumes, large volumes of data, analyzing it both historically and in real time in the sense of it goes into a database and then you analyze it from there and like an in-memory database and also streaming. So processing it as it comes through. So in terms of the use cases, the thing I think that kind of puts KDB+ or why it has been successful historically in there is because the performance is good, very, very good. The single architecture kind of question or piece comes up as well. It's a single technology that you can use to solve the large range historic data analysis problem plus the in-memory and streaming problem, which for its history to date, it's kind of really been the only one that fits all those use cases in terms of what they do with it. So there's just the storage for font analytics modeling. Those are mostly the historical use cases and in the real time use cases, we've done a lot of projects around calculating live risk across large volumes of data. We operate in the trading domain as well a little bit. So there was a period where people were building kind of automated trading systems with KDB+ as the primary technology. And the reason that they did that was because it was very, very flexible. They could get something out and running very, very quickly and participating in the market. You can do that still in certain domains where the latency isn't so much of a problem. You couldn't do that in like a proper sort of HFT [07] low microsecond type latency domains, but you can if you're sort of millisecond domains. It depends how you structure the system. But what you can still do in those is where KDB+ fits in that sort of a realm, a trading realm is kind of off to the side. So you would have a trading system built in C++ or Java, sort of highly, highly tuned Java. So you don't get caught out by garbage collector or whatever. And all the data passes into KDB+ and that's where kind of the analytics, the monitoring for the system and sometimes signal generation also gets done. So some signal generations that might be the order routing system or something like that. So it still participates in that sort of real time analytics arena. And KX have moved a bit outside of finance as well. So they have, I don't quite know how much I'm allowed to say, but you know, well, I guess, you know, you can tell a lot of this from their LinkedIn feeds and all that stuff. So they do work in defense, health care. And again, you know, it depends on those. I don't know exactly what those the problems they're solving are in there, but I would suspect they're more in the large volume data processing type realm than the sort of the live interactive streaming domain that would come up a little bit more in finance. But, you know, I think where KDB shines is that the rapid development cycle, right, this is kind of where the language helps it. You know, there's a sort of a school of thought that, you know, because the language is kind of niche and, you know, it's not taught in school, for example, you know, there's a learning curve associated, but you get pay off when you're building the systems because of the expressiveness. So you can build a system quicker, you can deploy it quicker. That's essentially the system that you can build with KDB plus, you know, it can usually, unless you kind of do it badly, it'll usually by default, you know, handle large volumes of data quite well. So you can compute analytics over large universes of instruments, right, or large universes of data, as opposed to, you know, having to, you know, think loads and loads and loads about how you distribute. I think, you know, realistically, you can do a lot, you can do a lot in KDB plus before you start, you know, you have to think about scaling horizontally later in KDB plus, you know, you can do a lot more vertically, like either that be on a single core on a single machine before you start having to think about scaling horizontally, which then, you know, reduces the overall complexity and cost of the resulting system that you end up with. That was a big long rambled, that kind of cover any of it or?

00:43:20 [CH]

No, no, it did. Well, I guess I'll ask one final question before we throw it to Stephen, is that I know that in, I think it was at KXCon 2023, they launched, or maybe I'm not sure if they launched, but I think they open sourced it, or maybe they launched it and then they open sourced it a couple months later, PyKX. [08] Is it the most of the consulting that Data Intellect is doing, is it still directly in the q and KDB plus technologies? Or is, has you seen, have you seen a lot of uptake with the PyKX? Because I know that there's a ton of technologies that, you know, they exist, but then they end up getting sort of embedded or hooked up to Python because it's such a popular ecosystem.

00:43:53 [JP]

Yes, so the majority of what we do would still be, you know, around KDB+ and the q language directly, sorry, in that piece of the business. So we do do some with PyKX for certain clients. KX do seem to be getting uptick there and, you know, that's kind of their play really. It's sort of to make it more Pythonic and lower the barrier to entry and, you know, try to, you know, remove the question of, okay, this is a really, really difficult language to learn. You know, I actually don't think it's that difficult a language to learn. It's just different, you know, it's different. It's a different way to think about it. It's probably more the problem than the syntax. You just got to make an investment if you want to do it, if you want to do it fully. But we do, and we have done some with PyKX. I think it's a good move for KX. I think it will open up new things for them. Yeah, Stephen?

00:44:47 [ST]

KDB and q is proprietary technology, and it's not cheap to use. So there's kind of a high wall around the q KDB technology. And I often get people contacting me saying, how do I get into this? How do I get some experience? And generally, you can only get in on sort of fairly big projects that are worth the price ticket for that. You can't propose to your IT managers, oh, let's use q for this. Like you might say, oh, let's write that in Python. So here's a hypothetical question. Suppose an open source version of a language very like q were released, and it was basically free to use. I'm wondering what opportunities would you see that opening up for data intellect or for the industry generally?

00:45:45 [JP]

Is this something you're writing, Stephen?

00:45:49 [ST]

Did you ever learn k?

00:45:50 [JP]

K? Yeah. I know a bit of k now, by accident, mostly.

00:45:57 [ST]

Yeah, me too. Arthur's latest company, Shakti, [09]is working on a new version of k, and there's an open source version of that around. So it's not actually a hypothetical question, as I pretended.

00:46:11 [ML]

Well, and there are other open source versions of k. What I was going to comment on is that I don't know of any open source efforts to do anything like q, which is interesting, just because there are so many different k efforts. Now, I mean, most of them don't have the professionalism of Shakti. But it's just, I guess, the people working on open source languages who are interested in array programming, they want to go all the way. They want to go to k rather than having something more approachable like q, I suppose.

00:46:42 [ST]

Well, the latest version, I mean, Shakti's k has got some keywords in it, like SUM on AVG. So it's retaining quite a bit of what distinguishes q from earlier versions of k.

00:46:55 [AB]

Does it have the query language, q?

00:46:59 [JP]

Yeah. Yeah, it would certainly, yes. It would open opportunities for us. It depends, you know, I guess with any of these things, it depends how fully featured it is, because I think, you know, it's more and more, you know, we see it more and more. It used to be that if you were building a system in KDB+, it was much easier to get started and get it in. I think, but, you know, there's more and more security and InfoSec requirements that come in from the very outset from any system, you know, any system design that we're involved in. You know, so it's kind of essentially, you know, you got to start, well, OK, how are you managing users? You know, how are you doing the connectivity, etc., etc., etc. And, you know, there's a lot of stuff, I think, you know, a lot of systems you used to get away with, which we just don't. The policies and the clients that we deal with are different now. So and we got to adhere to those. So it depends how probably depends how fully featured it is that we, you know, as to how far far we could go with it. You know, you could certainly you could see certainly how you could embed it or wrap it inside, you know, as the as the processing core inside another application that actually, you know, takes away or handles all those concerns.

00:48:13 [CH]

This has been an absolute blast and hopefully there will be a KXCon, I'm not sure 2024 at this point, but maybe 2025 and we'll see each other again in the future. And if you have any questions about the topics that we've talked about or anything else you can reach us at.

00:48:30 [BT]

Contact@ArrayCast.com. That's where we take questions, comments, everything. I'm sure people who are interested in the array languages and maybe getting involved in the array languages in a commercial sense might have taken a lot from this episode. We certainly get requests that way. So contact@ArrayCast.com and a thank you out to Sanjay and Igor, who helped with the transcriptions on this, and to Adám as well, who starts the whole process off.

00:48:56 [CH]

And we will end by saying happy array programming.

00:49:01 [ALL]

Happy array programming.

</details>
