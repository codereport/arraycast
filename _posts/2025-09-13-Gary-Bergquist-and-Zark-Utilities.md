---
title: "Episode 114: Gary Bergquist and Zark Utilities"
date: 2025-09-13 00:00:00 +0000
episode: 114
keywords:
- array-programming
- array-languages
- apl
- utilities
- gary-bergquist
- dyalog-apl
- apl+win
- apl2000
- aplnow
- top-down-development
mp3-url: "/assets/audio/episode114.mp3"
episode-type: full
explicit: "no"
block: "no"
layout: podcast
excerpt_separator: <!--more-->
redirect_from: "/episodes/episode114-gary-bergquist"
---
Gary Bergquist and Zark UtilitiesTo Gary Bergquist APL is more than the primitives. It is the whole top down approach of developing utilities.
<!--more-->

**Host:** Conor Hoekstra

**Guest:** Gary Bergquist

**Panel:** Marshall Lochbaum, Bob Therriault, Stephen Taylor, Adám Brudzewsky and Richard Park

---

[Original episode on ArrayCast](https://www.arraycast.com/episodes/episode114-gary-bergquist)

## Show Notes

Array Cast -  September 12, 2025

Thanks to Bob Therriault, Adám Brudzewsky, and Conor Hoekstra for gathering these links:

**[01] 00:01:56**

- [Jon McGrew's obituary](https://www.dailyfreeman.com/obituaries/jon-mcgrew-kingston-ny/)
- [Jon McGrew's Service](https://www.eventbrite.com/e/jon-mcgrew-memorial-tickets-1666048639329)
- [Quote Squad on the APL Farm](https://aplwiki.com/wiki/APL_Farm#Quote_Squad)
- [Ken Iverson](https://en.wikipedia.org/wiki/Kenneth_E._Iverson)
- [Ken Iverson Episode #92 on the ArrayCast](https://www.arraycast.com/episodes/episode92-iverson)
- [Bob Smith Episode #80 on the ArrayCast](https://www.arraycast.com/episodes/episode80-nars2000)
- [Bob Smith Episode #82 on the ArrayCast](https://www.arraycast.com/episodes/episode82-nars2000-implementation)
- [Jim Brown](https://aplwiki.com/wiki/Jim_Brown)
- [Dyalog APL](https://www.dyalog.com/)
- [James Price Episode #70 on the ArrayCast](https://www.arraycast.com/episodes/episode70-james-price)
- [Adin Falkoff](https://aplwiki.com/wiki/Adin_Falkoff)
- [Strand Notation](https://aplwiki.com/wiki/Strand_notation)
- [APL Farm](https://aplwiki.com/wiki/APL_Farm)
- [Gary's publications](https://dl.acm.org/profile/81100521417)
- [Zark Inc.](https://zarkapl.com/)
- [APL Tutor](https://tutorial.dyalog.com/)
- [APL Programming Language](https://aplwiki.com/)
- [14 Misconceptions About APL](https://vector.johnbutlerassociates.co.uk/art10000280)

**[02] 00:15:40**

- [Scientific Time Sharing Company STSC](https://en.wikipedia.org/wiki/Scientific_Time_Sharing_Corporation)
- [I.P. Sharp Associates](https://en.wikipedia.org/wiki/I._P._Sharp_Associates)
- [I.P. Sharp Associates Episode #91 on the ArrayCast](https://www.arraycast.com/episodes/episode91-ipsharpdoc)
- [Quad FMT](https://help.dyalog.com/19.0/#Language/System%20Functions/Format%20Dyadic.htm)
- [Personal Computers](https://en.wikipedia.org/wiki/Personal_computer)

**[03] 00:21:46**

- [APL 2000 Programming Language](https://aplwiki.com/)
- [/wiki/APL2000GUI environemnt](https://en.wikipedia.org/wiki/Graphical_user_interface)

**[04] 00:29:51**

- [ACM 1998 Zark Library of Utility Functions](https://dl.acm.org/doi/10.1145/312627.312707)
- [Open Source](https://en.wikipedia.org/wiki/Open_source)
- [Tatin Package Manager](https://www.dyalog.com/)
- [/uploads/conference/dyalog24/materials/D11_NewTatinPackages.pdfScreen Shots of Zark Library](https://www.arraycast.com/zark)
- [Excel Programming Language](https://en.wikipedia.org/wiki/Microsoft_Excel)

**[05] 00:41:28**

- [Namespace](https://aplwiki.com/)
- [/wiki/NamespaceMOM objects](http://www.apl2000.com/productwin.php#info3)
- [Phineas Porter Episode #98 of the ArrayCast](https://www.arraycast.com/episodes/episode98-phineas-porter)
- [Nick Psaris Episode #42 of the ArrayCast](https://www.arraycast.com/episodes/episode42-nick-psaris-q)
- [q Programming Language](https://code.kx.com/q/learn/)
- [C Programming Language](https://en.wikipedia.org/wiki/C_(programming_language))
- [Functional Programming](https://en.wikipedia.org/wiki/Functional_programming)

**[06] 00:56:04**

- [Reverse Function](https://help.dyalog.com/19.0/#Language/Primitive%20Functions/Reverse.htm)
- [System Functions](https://help.dyalog.com/19.0/#Language/System%20Functions/Summary%20Tables/Introduction.htm)
- [Primitives](https://aplwiki.com/)
- [/wiki/PrimitiveReplicate Episode #110 on the ArrayCast](https://www.arraycast.com/episodes/episode110-replicate)
- [J Programming Language](https://code.jsoftware.com/wiki/Category:Home)

**[07] 00:59:30**

- [APL 2](https://aplwiki.com/)
- [/wiki/CDC_APL_2NARS Programming Language](https://aplwiki.com/)
- [/wiki/NARSJ Cycle Permutation Verb](https://code.jsoftware.com/wiki/Vocabulary/ccapdot)
- [Lisp Programmimg Language](https://en.wikipedia.org/wiki/Lisp_(programming_language))

**[08] 01:08:00**

- [APL Tutor](https://tutorial.dyalog.com/)
- [Instructional Design](https://en.wikipedia.org/wiki/Instructional_design)

**[09] 01:19:04**

- [Hacker News](https://news.ycombinator.com/)
- [APL Bingo](https://aplwiki.com/)
- [/wiki/APL_BingoContact AT ArrayCast DOT ComShow Notes for Episode #113](https://www.arraycast.com/episode113-show-notes)

<details markdown="1">
<summary><strong>Transcript</strong> (click to expand)</summary>

Transcript

Transcript prepared by

Bob Therriault

Show Notes

Gary Bergquist

**00:00-00:25**

What I really want to be able to do is I want to be able to translate a real-world problem into functioning code rapidly and be able to modify it and maintain it rapidly. Get a call at 10 o'clock at night, and the guy says it's not working, and the markets are waiting for it, and we're going to lose millions of dollars if you don't fix this in the next 10 minutes. I want to open up a small piece of code, be able to read it, modify it, and send them a fix quickly. I don't care about the symbols.

MUSIC

**00:25-00:38**

Conor Hoekstra

**00:38-00:59**

Welcome to Episode 114 of ArrayCast. I'm your host, Conor, and today with us we have a special guest who we will get to introducing in a couple minutes. But first, we're going to go around and do brief introductions from our, I believe, record-setting number of panelists. We'll start with Bob, then go to Stephen, then to Adám, then to Marshall, and finish with Rich.

Bob Therriault

**00:59-01:04**

I feel like I'm leading the whole troupe here, but I'm Bob Theriault, and I am a J-enthusiast.

Stephen Taylor

**01:04-01:14**

I'm Stephen Taylor. I'm a q enthusiast and an APL enthusiast and particularly relevant for today. I am enthusiastic about teaching APL.

Adám Brudzewsky

**01:14-01:19**

I'm Adám Brudzewsky. I am also an APL enthusiast. I'm also an enthusiast of today's cast.

Marshall Lochbaum

**01:19-01:24**

I'm Marshall Lockbaum, Cingelli enthusiast and designer at BQN.

Richard Park

**01:25-01:37**

I'm Richard Park. I'm also a big APL enthusiast. Since our last episode, I'm now also another moderator of the APL JK subreddit. Thanks to Alex. So that's a lot of fun.

Conor Hoekstra

**01:37-01:55**

Very nice. Very nice. And as mentioned before, my name's Conor, host of ArrayCast, enthusiast of all the array languages. And very excited for our conversation today. But before we get to introducing our guest, we have two announcements. So we'll start with our first one from Adám, and then we'll finish with our last one from Marshall.

Adám Brudzewsky

**01:56-02:38**

Right. So unfortunately, Jon McGrew passed away a couple of weeks ago. [01] There has now been a published an arbitrary, and we'll have a link to that. Also a link to the memorial service website. which is going to be on October 5th. I would say that Jon McGrew sort of pioneered that which we do here at ArrayCast. So I think that we have a little bit of a special connection to him. As far as I know, he was the first one that was creating APL social content outside of what the commercial corporate entities were creating. We should be proud to carry on this legacy, even if he's not with us anymore.

Conor Hoekstra

**02:39-02:47**

And yeah, be sure to check the link in the show notes because the details for the memorial service, if you're in the area, will be in that link. Over to Marshall.

Marshall Lochbaum

**02:47-05:58**

What I've got is less of an announcement and more of a kind of just ongoing notes from our Quote Squad sessions, which have been happening every Sunday on schedule. This last one I found very interesting because to give you the backstory, I was reading some old papers about APL and found cited in there some letters to the editor. Yeah. from Ken Iverson, Bob Smith, and Jim Brown. If you know about APL history, these are big names. And we also interviewed Bob Smith a while ago. I think he's been on multiple times. Talking about strand notation. So I looked in... these were published in Quote Quad, and I looked at the ACM's Quote Quad articles, and I did not find it in the relevant issue. And the reason for this is that they apparently don't publish all the front matter, including letters to the editor. Now, this is kind of unfortunate for that issue, because these are probably the most interesting things in the whole issue. So what I did was asked on the Dyalog forum, hey, does anybody have a copy of the of the quote quad in question that they can maybe scan and Silas who works at Dyalog said yeah I'll get them when I'm back in the office and he did so he shared some scans on the forum and this coincidentally worked into our regular uh voting schedule on the quote quads where we progress one issue per week so um I very strongly encouraged everyone to vote for these ones uh And they did win the vote. So we discussed them on Sunday, mostly me and James Price, who's a former guest here as well. And they're I mean, they're just a really interesting look into what was happening in 1981, this big split between the grounded and the floating party. array models. And Iverson was just really against this new concept of generalizing his vector notation where you write, you know, numbers one, two, three. Stephen talks about really liking this a lot to, you know, ABC, anything, including expressions in parentheses. And so Iverson details his complaints and Bob and Jim come back with their thoughts about it and really push the idea that it's a natural generalization. And there's also a later reply by Adin Falkoff, who is also, he's in Iverson's camp. He's also really concerned about this new notation and particularly the idea of strand assignment, what matters. What are the implications of being able to write ABC, gets, and then an array, which does actually show up now in APL with a fair number of syntax problems. So this is an interesting discussion to maybe go back and read. And also, if you'd like to start joining in with our... Join the Quote Squad. We will be discussing on Sunday. We have another interesting article, which is a based system for general arrays by Randall Mercer, which you may actually recognize if you're a BQN enthusiast as the origin of the name. for BQN's based array model, which is very impressive that Mercer in 1981 was calling things based. So I actually voted against this article. But if you want to discuss it, it'll be this Sunday. And next Sunday, we'll have some other article to discuss and So on from many weeks.

Bob Therriault

**05:59-06:03**

And it's on the APL farm, and that's where the discussion is, Marshall?

Marshall Lochbaum

**06:03-06:31**

Yeah. And so there's actually now a little section in the APL wiki that sort of describes what it is and says, there's a keyword, a key phrase that I start everyone with, so you can search it. It's, quote, squad, convene, which is chosen because it's unlikely that anybody would naturally say it. That's how you can find them. And so you should be able to find them all. Yeah, it's in APL Farm and the main channel, which is titled Array Languages, I think.

Bob Therriault

**06:31-06:38**

And so you were talking about these letters. Are they available anywhere or do you have to go back to the discussion to find them?

Marshall Lochbaum

**06:38-06:53**

So, yeah, you'll be able to find them on the forum through that. So Silas just sent them as a chat message and I replied to that so you can follow through the reply and get to it that way and then... downloaded them and save them to make sure that lots of people have copies.

Conor Hoekstra

**06:54-08:13**

Awesome. So links for all of that, if you want to go back to that discussion or take part in a future one, will be in the show notes. And with the announcements out of the way, I am extremely excited to introduce today's guest, Gary Bergquist. And he is a longtime APL-er, founder and president of Zark Incorporated, and I hope he's going to tell us a little bit about that. I imagine that company was involved in promoting or authoring the Zark libraries, which I came across in researching Gary in preparation for today's episode, which I don't know much about. I think they have been mentioned once or twice, but definitely not in detail in this podcast today. But on top of that, he is also the creator, I guess we can call, or maybe co-creator, he'll tell us, of the APL Tutor, which is an educational tool that you can use to get started and teach yourself APL. And I'm sure many other things that I was not able to uncover on the interwebs because Gary has a lower profile than some other folks have. And anyways, I will throw it over to you, Gary. Take us back to whenever you'd like to, your first computer, your first written line of code, and tell us your story of how you fell into APL, fell into programming, and fell into starting your own company and also getting into teaching APL because I know that is a topic that comes up again and again on this podcast.

Gary Bergquist

**08:13-22:43**

I guess everybody said what they were enthusiasts of, I should say what I'm an enthusiasts of, I'm an enthusiast I guess primarily of people who are enthusiasts of me. Secondarily though, I'm an enthusiast of APL. This is I guess Primarily an array podcast Where we talk about various array languages So from that I assume that you've neatly divided the world into array languages and non-array languages. I've divided the world into APL languages and non-APL languages. I guess when people listen to the things that I have to say at various talks that I've done or listen to or read the articles that I've written or whatever, they tend to view me as a...I don't know, a utility guy. But generally, when I start talking about anything, I'm talking about my religious fervor, I guess you might say, towards APL. To understand that, and I think it's important to understand anything that I've done, is to understand my views about APL. There was a talk that I did, I think it was for ACM, it was one of these annual APL conferences a number of years ago, probably two or three decades ago. And I was speaking to the audience and my topic was misconceptions about APL, like the 12 misconceptions about APL. And I was about to explain the first one. I looked out into the audience. In the middle of the audience was Ken Iverson. And for those who don't know who Ken Iverson is, he's the inventor of APL, if you will. He was a mathematics professor at Harvard, and he wrote the book A Programming Language. Then he went over to IBM, joined IBM, and with a team of assistants. Other excellent programmers, they developed the first version of APL. Anyhow, he was out there and I thought, uh-oh, because my first misconception was that people tend to think that Ken Iverson is the inventor of APL. And I was very careful not to look at him when I said that. And of course, what I was really getting at wasn't so much that he wasn't the guy who came up with APL, but it's not so much that Ken Iverson invented APL as that he discovered it. To say that he invented APL to me is like saying that Newton invented calculus, you know? And without Newton, you wouldn't have calculus, so that if there's intelligent life forms on other planets – They don't have calculus because they didn't have Newton. So to me, it's the same thing. It's that APL, like mathematics, like calculus, is part of the fabric of the universe. And yeah, Iverson discovered it, and he came up with a notation for APL. And now we've seen other languages that I would call also APL languages that have... slightly altered notations, but they're APL. And it's important to distinguish. It's especially important, if there's anything I've been preaching over the years, it's that you need to understand what APL is. So when I go to conferences and I talk, I almost always start, especially when it's a conference that deals with APL developers, people who build the language. I usually start by asking them to tell me what it is they think APL is. How would you define APL? What makes APL different from other languages? And it's usually interesting because people think a little bit. And of course, if you've used APL, you're thinking about, well, let's see, there's right to left and there's symbols and there's mathematics and there's arrays. Yes, it has arrays. But how would you concisely explain what it is that makes APL different from other languages? And in general, people will struggle a little bit. And then I come up with my, the Gary Bergquist definition of APL. 10 words. It's 10 words. And the first five are the implementation of a notation. So far, it's the same as any other language, right? So you only have five more words here to conclude what is APL. What makes APL different from other languages? It's the implementation of a notation definition... design from the top down. That's what makes APL. And often I'll go up to the board or whatever and I'll type plus slash V divided by rho V. I mean, that's it. To me, that's APL. That was the first time I saw that, you know, after coming out of college and seeing that after working with other languages And you look at that, you laugh. It's just so delightful. It's just so straightforward. And it's because it's designed from the top down. I mean, Iverson, he was a professor. He was a teacher. His interest was in teaching mathematics and secondarily, I think, in computers. and... He didn't really know, I think, a lot about computers. And he developed a notation for representing solutions to problems. So you look at other languages that try to do the same thing. And they've got do loops, and they've got dimensions statements, and they're declaring data types and And it's clear that these other languages, whatever they are, have been designed from the bottom up. They've said, wait a minute, wait, wait, wait, the computer. Let's think first and foremost about the computer. I mean, obviously, you've got to reserve some space for the numbers, and you have to determine whether it's floating points, could be 64 bits or how many bits, and you have to… iterate through and set aside some room, some storage space within a computer to it. Iverson, you know, APL, APL says, no, no, don't do that. Look at the problem. Look at the problem. Come up with a notation. Implement the notation. There's the hard part, right? Off to IBM with the other guys. Implement the notation where you develop the notation not caring at all, about how hard it was for the computer to do and then implement the notation. And then what you have is you have something that's at such a high level, you can do things very quickly, you know? And if I complain, and I do, I tend to complain a lot, I feel that the development companies have lost sight of that. I think a lot of people who use APL, they love it, they use it, it's nice, you know? But they view it as a bunch of symbols, right? And that's not what it is. It turns out that it was convenient to use mathematical symbols and it was convenient or necessary, if you will, to have arrays and define arrays, have nested arrays and multidimensional arrays and all that kind of stuff. But it worked from the top down to come up with that. You asked me, I'm preaching. All right. So let me get back to what you asked me. You said, tell me a little bit about yourself. All right. So I come out of college and I went to a decent school and I've got a degree in management of all strange things. But the only thing I really enjoyed doing at school was computer programming. And I worked with crude languages. And one afternoon, a guy came in and he said, I do APL. Nobody knew what that was. And he explained what APL was. And on the final exam, there were a couple of questions about APL to make sure you were paying attention and that you had attended that class. And the key was you had to know that it went right to left, if you will, and that I don't remember what the other strange things were about APL. But I got out of college. I looked around for a job and it was difficult as it usually is for anybody, especially these days. And it was just a chance that I happened to walk into a building and look at the directory in the lobby and find that there was a headhunter there. And the headhunter led me to some guy, and I interviewed with him. And I ended up having a job for a computer time-sharing company called Scientific Time-Sharing in Houston. [02] And I was from Connecticut and half of my family was on the East Coast and the other half was in California. So half was lobbying for me to stay on the East Coast. The other half was lobbying for me to go to California. So when he offered me a job in Houston, I thought, this is perfect. I don't know anything about Houston, but I don't want to be listening to my family arguing about which side I chose. So I went to Houston. And I learned APL. And I really didn't know much about it. But I started off working for a computer time-sharing company. The thing that was perfect about computer time-sharing organizations in APL was the organization. At the time, there were really two big computer time-sharing corporations. There was one in Canada, Toronto, called I.P. Sharp Associates, and I was a big company. And there was Scientific Timesharing Corporation headquartered in Bethesda or Rockville, Maryland. And for some reason, I never did understand. They shared a development department. So there was a common set, even though they were competitors. I.P.Sharp, I guess, mostly was looking for business in Canada. And Scientific Timesharing Corporation was doing business in the United States, right? But they shared a common development department. So these two firms had had taken the language that had been developed at IBM and they developed at IBM because they got a lot of money and whatever, you know, they could do it. So they did do it. You had all of these PhD people working on it and they came out with it, but they weren't ready at that time to commercially. present the language. So these two firms started up and their job was to see if they could sell time on mainframe computers using the language APL. It was the old days and we had these computer Yeah. terminals that we would tote around. And I was in Houston, so I'd have meetings going to petroleum companies, Exxon Mobil, things like that. And say, look, look at the things that we can do. Your IT department, you know, they're using cards and tapes and everything. It takes forever. We can do things for you very quickly. Well, relatively quickly. I mean, very quickly for those days. Very slow nowadays. We can do things for you. And you use this computer time-sharing service. And you're going to, we're going to receive money from you by solving your problems. So we had APL at our disposal, and we would talk with financial analysts, actuaries, whoever, you know, who might be able to use these tools. So anyhow, the way these organizations work, and our organization in particular, is you had... Applications consultants, we were called, which were programmers with a marketing hat on. So we would go out to clients. We'd say, what do you want? And we'd go back to the office and we would build it for them, deliver it to them. They would use it through these terminals and they would burn up CPU time, use storage, and they would be paying for the use of the computer automatically. They really weren't paying much for the development of it. They were paying for the use of the computer's resources. And that was how we made our money. Now, this is the important thing, okay? So if I went to a client and they wanted something that I could not deliver, Then I would come back to the office and I would speak to the officers in our company and say, I can't do this because they want reports. And I don't know how to be able to generate a report using APL. APL doesn't have any report formatting capabilities. So the developers would all sit down and they would say, all right, we need report formatting capabilities. Now, this is the important thing, OK? At the time, you didn't just have people sitting there saying, how can we extend APL? How can we give it new symbols and greater functionality? Maybe they were thinking that a little bit. Mostly, they were listening to people in the field. Now, remember, I say APL is top down. Top is the application. It's the problem. It's the program that you're trying to write. And as a programmer out in the field, if I couldn't do something, I went back to the company and said, I need this. It went down to the development department and they would give me something. Now, at the time, they gave something called Quad FMT. Now, what you have to appreciate about the system function Quad FMT is that it's... ugly. It's bizarre. It's ugly. It's not anything that ever would be developed today. It has a left argument of a character string that's comma delimited and a right argument. It's a nested array, even though they didn't have nested arrays, items that are separated by semicolons. It was disgusting. It was disgusting from a developer's point of view. But from the field's perspective, It was heaven. It was APL because it was designed from the top down. It was exactly what we needed. What ended up happening, though, is come 1983 or so, in the early 80s sometimes, PCs came about. And that changed the game. It changed the game because the mainframe users of APL, the mainframe developers of APL, could no longer make money by selling time on the machines, right? They now had to sell PC software. And how do you make money on PC software? Well, you sell a copy of it to one guy somewhere, you know? So you were no longer solving problems in the same fashion. I consider that moment, the early 80s, to be the divorce, the separation of, of how things worked in APL. To me, it was the beginning of the end in a way. Because if you define APL as a language design from the top down, suddenly the connection that existed between the guy in the field and the developer had been broken. At the time, STSC, Scientific Times, changed their name to SCSC, and they split. Their mainframe APL business went off in one direction, and they came up with the very odd name, Manugistics. And in the other direction, APL 2000, I think, was the name that was selling products. [03] The PC product. And the way it worked now was entirely different. And I give you a good example of why that became a problem. So here I am out in the field. I left the company and became a consultant, APL programmer. I was still doing the same thing, still dealing with people that had problems to be solved. But the way they were paying for it was now different. The whole setup, the motivation, everything was different. Right. So now I'm out in the field and Windows comes out. We go from the DOS world, character-based user interfaces, to Windows graphical user interfaces. All right. So now the end user says, can you build me an application now? Let's say that a form pops up on a screen and it's going to be a mortgage calculator. So it's going to be a little form and at the top it says mortgage calculator and it's going to be a line that says interest rate and principal amount and what else do you need?

Bob Therriault

**22:44-22:44**

Term.

Gary Bergquist

**22:44-26:14**

Term. Thank you. How many years or months or whatever? And then at the bottom, maybe there'll be two buttons, calculate and cancel or done. And then there'll be a little field that'll say your monthly mortgage payment is. So you type in the three numbers and you click calculate and it shows to you. That's what he wants. I just described that for you in under a minute. Now, if I said to you, I wanted to compute the average of set of numbers, here's how you do it. You take the numbers, you add them up, and you divide by the count. You divide by how many there are. Now. It takes me 10 seconds to say that. APL, it takes you 10 seconds to write it. Now, I just described a user interface in under a minute. Now, APL top-down, I should be able to implement it in a minute or two or three. So what happened instead is when Windows came out, APL 2000, APL + Win, said, here you go. Here's an interface. Here's a system function quad WI, I guess, Dyalog as quad WC or something. Here's a system program that you can use to build user interfaces. And they gave us all of the access, all of the little Windows functionality things for putting up title bars and scroll bars and edit fields and lists and list views and trees and all these other kind of things. Okay. And it would take me days to use those tools to put together something that I can describe in a minute. And this is a different philosophy. See, if it was in the old days where I had a direct connection, Okay. I'd say, no, that's not good enough. How about this? How about if it's called quad Form, and I take that system function and just give it what I said. Just give it the minimum. So a title bar, here's-- just like I said. Now, we need a notation, right? APL is the implementation of a notation. So you need some notation. Fine define it like quad FMT you define a notation it did what I want to do that's good I have to be able to implement this form in a minute or two not in hours or days okay that was gone all right so what I was forced to do what my firm was forced to do what every APL consultant out there was forced to do was to do it on their own all right so this is why I ended up becoming known as the the utility guy right well I had to build APL on my own because the developers were no longer doing it. They were saying, well, what can we do? We've got a lot of little symbols. How about a symbol with a couple of dots in it with a little squiggle over it that takes the arguments of a function and it commutes them so that we can leave out a set of parentheses? Well, fine, that's nice. But when you send me that, it doesn't help me because I'm trying to put up a form on a screen. That's what my client wants. You're causing me to... to spend too much time. So I end up spending three quarters of my time and three quarters of the time of the people working with me building utilities. So then in fact, we could say, all right, the guy wants a form and it's got these fields on it. He wants a little list over there. And when he clicks this button, it does this. And he describes it in five minutes and we implement an intent using our utilities. But it's not APL. I mean, it is APL, but it's user defined APL. So I'll pause there and see if you have any questions or comments you want to say to ask me about that. Have I given you some information on my background and my views?

Bob Therriault

**26:15-27:13**

Yeah, I've just got an observation, I guess. When you talk about that, it sounds to me like if I said, you know what, I need to get from here to five miles away, I'd like a motor scooter. but instead of a motor scooter, somebody hands me all the parts and says, well, there you go. There is a motor scooter. And it's like, yeah, no, I didn't want to carry it five miles. I wanted to ride it. And they go, oh yeah, no, no, but you can, you can do that with this. So it's like the, the, the interface to the people that were working with it, they were given quote, careful what you ask for. You were given all the tools you needed to, but they weren't put in a form that you could actually use. And as you say, being top-down designed, the other way to do it is to say, okay, well, this is a motor scooter. And if you want to make changes to it this way, we could add these things to it, but it will start out as what you need. And then you can work from there. Is that sort of a good analogy?

Gary Bergquist

**27:14-29:38**

Yeah, I was spoiled because I never really worked with other languages. I got out of college and, you know, I had used some other languages in college, but when I got out, it was APL. And certainly I loved what I was seeing, but I was spoiled because I thought this is it. This is the way things are supposed to be. So when people would offer me solutions in other languages, or in this case, Windows, utilities from within APL, It's like, no, I don't want that. I'm spoiled. I want to be able to implement things quickly, as quickly as possible. And when you're out in the field, and my company is an APL consulting firm. We build applications. We support them. The way we make money is by spending as little time as possible actually programming and actually supporting, you know. So you need to write things at such a high level that you can do them quickly. You can support them quickly. And, you know, like all computer applications, nine-tenths of your time is spent in supporting it. So you have to have a small amount of code. It's not enough to have these code writers that write thousands of lines of code for you in 10 minutes. You now have to support thousands of lines of code. So it's got to be APL. It's got to be small. It's got to be compact. It's got to be directly related to to the application, to the problem that you're solving. So you can jump in quickly. You know, when someone calls and says, can you shuffle these columns around? You know, you don't want to be working at such a low level that you're counting characters here and there and everywhere. You just want to say, move this column from here to here. Or you're generating a report and they want so many columns and they want totals here and there. If they can say it in five minutes, the aim is you've got to be able to implement it in five minutes. And if we would do something that would take an hour, then there was always the question, why? Why did it take an hour? If they explained it in five, why did it take an hour? What can we do by way of altering our utility programs so that you could do it quicker? So, yeah, that's one of the things when you hear about Zark is the Zark library of utility functions. We've got a whole bunch of them. And I see that the functionality in those utility functions are slowly making their way, have made their way into some of the... Yeah. uh system functions that the uh APL system developers have you know such as Dyalog APL and APL 2000.

Stephen Taylor

**29:38-30:09**

Gary in 1998 you published a paper in ACM SigAPL published your paper on proposing the ZARC library of utility functions [04] and you seem to have invented the open source paradigm at that time by proposing people contribute to it in return for a license to use it. That was 1998. Can you bring us up to date on that?

Gary Bergquist

**30:10-31:27**

Up to date? Well, I've always been a fan of what you call open source, because, as I said, we make our money by… Having an application that benefits a client and the client is paying us to build it and to maintain it, always building the utilities and the utility library was a, you know, it's APL, so it's fun to do, but it was an exercise I'd rather not have done. So my offer always was, here they are, here's our utilities. Take them. I put them in a format, the library of utility functions that's easy to use. So you just quickly click on things and get descriptions on how they work and what their syntax is and pull them into your workspace. Take them, use them. If you find problems with them, that's terrific. We can fix them. If you think of enhancements, extensions to them, that's terrific. You do it. We do it. I don't care. I guess that's the open source mentality. It benefited, always benefited us. The idea that I would put together a library of utility functions and then... Try to sell it to those other struggling APLers out in the field who could use it. You know, maybe I'll make a few bucks, but I'll probably also make a few enemies. Like, nah, take it. Take it. It's the case with all of our stuff.

Stephen Taylor

**31:27-31:28**

And now it's 2025.

Gary Bergquist

**31:29-31:53**

2025. So there's still a library of utility functions out there, and we've extended it every time we come up with something new. So now it's got the Windows interface we use, utilities we use for working with Excel, utilities we use for building reports, Anything that we need that's not readily accessible, we write it and we throw it in there. And it's anybody who wants it can have it.

Stephen Taylor

**31:53-32:41**

Last month, I spent a few days at Dyalog's Galactic headquarters in Bramley, working with them on the package manager, Tatin, that they've been shipping with Dyalog for a while. And we still have this issue of putting stuff in places where everybody can use it. You're very clear that having access to this is essential for productivity. The Tatin package repository is still kind of coming to life now. and attracting content, it's a quarter of a century later. Why have we not stopped with this very important problem for APL's key issue of productivity? What's in our way?

Gary Bergquist

**32:41-33:37**

Well, it's not a problem for me. If it was, I suppose I would do something about it. I have the library, which is accessible to us and to the people that work for us and to anybody who wants it. It's a single file library. So anybody who's using, and we're using mostly APL + WIN and not Dyalog APL, but anyone who's using it, it's just a user command file, one file. I can email it to you. You just install it, and then the library is there to use. You're right. In this day and age, you know, it would be nicer if it was all online somewhere. It was on some server or something, so you could type something, and it would bring down whatever you needed and that sort of thing. But I haven't felt the need for it. for our particular clients so I haven't gone anywhere in that direction so my library is not accessible to the universe like that except if you ask for it.

Adám Brudzewsky

**33:37-33:50**

So I'm wondering what your approach is to import these things you say you have it as user commands in APL plus which I don't remember exactly this how it is they work but Do you copy things in from there to what you're working on?

Gary Bergquist

**33:50-34:28**

No, actually the way it works is you just say right bracket. User commands are invoked with the right bracket instead of a right paren. When you say right bracket, zarklib, z-a-r-k-l-i-b. And it presents a user interface and you can look at the functions by alphabetical order, by workspace categorization or date that it was installed or something. or by outline type of stuff, input routines and report writing routines and actuarial functions or whatever. And you click on it and you go to a particular function, you press F1, and it explains what it does and what its syntax is. And if you want it, you say define it and poof.

Adám Brudzewsky

**34:29-34:32**

So then it basically defines it in your workspace where you're working right now.

Gary Bergquist

**34:33-34:43**

Right. If you happen to know the name of the function that you want, foo, And you want to bring it in, you can say right bracket Zloads, Zarklive, load, Zload, foo, and it'll bring it in.

Adám Brudzewsky

**34:43-34:58**

Ah, I see. So there's a shortcut there as well. I think it would be great if it's okay with you, if you could send us maybe a screenshot or two of seeing that in action so that we can include it in the show notes for this episode. I think that would be enlightening.

Gary Bergquist

**34:58-34:58**

Sure.

Adám Brudzewsky

**34:59-35:20**

But that also means, this answers also my question, as to you bring in the minimal amount that you need. You don't bring in a giant library of everything and then just use the pieces you want. You bring in just, you copy in basically, or define in just the pieces that you need right now. Does that also mean that all your utilities are standalone? They don't depend on each other?

Gary Bergquist

**35:21-36:56**

They are mostly standalone. Philosophy, our philosophy, we need to talk a little bit about APL, I guess, here. I remember when I was first learning APL, we would go to conferences and one of the topics that was being discussed, because this was in the early days, people were still trying to wrap their heads around the idea of APL. So the question that came up was, what's the ideal size of an APL function? And oddly enough, the consensus, and I don't know that I agreed with this, but the consensus was, well, an APL function should be square. I don't know what that meant, really, but the small ones shouldn't have a lot of lines, and the bigger ones, I don't know. My philosophy is a little different from that. I always felt that I shouldn't have to have built this utility function in the first place. So if I'm going to write a function that really should be quad FORM to present an interactive form, then I want to be able to just bring in one function, FORM. So I'll bring in the one function and that function will do everything I need to do. Well, you go, whoa, wait a minute. That's got to do a lot of stuff. Yeah, it might be 5,000 lines. That doesn't bother me. Okay, so you bring in one function. Now, there are instances where, yes, multiple functions are being used. But in general, it's not like, I want to do forms. All right, so copy in this workspace or package or whatever of 642 functions. Every function is seven lines long or two lines long. No. And then you're living in this whole world of functions, a big jungle, trying to figure out what's what. Just one function. You bring it in and you use that function.

Adám Brudzewsky

**36:57-36:57**

Interesting.

Gary Bergquist

**36:57-37:22**

It's a different philosophy. It's a different philosophy for most APLers. And I can understand if you take a moment to throw up, because different people view different APL in different ways, but it's been very useful for us. So we have one function for generating reports and one function for generating forms and so on. And some of these functions do have some large sub-functions, but a handful. not hundreds where you have to understand all this other stuff.

Adám Brudzewsky

**37:22-37:25**

So how do you deal with dependencies when there are some?

Gary Bergquist

**37:25-37:26**

Such as?

Adám Brudzewsky

**37:26-37:38**

Well, so if I bring in one of the utilities and it actually requires additional utilities to be brought in, does your system then know about the relationship between these functions so that it gets all the subfunctions that it needs?

Gary Bergquist

**37:38-38:58**

No, let's say that you're using a reporting utility, which is called ZW-rip-it. And it's probably, I don't know, 4,000, 5,000 lines long. Pretty much stands on its own. There are a couple other functions that you can use, though, if you're going to be working with Excel. If you're using the reporting utility to write Excel files or read from Excel files, then you also need another function, Excel. name of that function. So you need two functions instead of one. So there's a dependency there, and it's commented in the header comments of that function that this function will need these other three or four or two other functions under certain circumstances. So we've kept it so that it's big and small, Not big or small. So that the functions are big, but the requirements are small. Rather than, you know, I've written a new function. This one's six lines long and it's called, it's got some name. And you've got a library of 7,000 functions that you need to know. Like you say, the interdependencies of all these functions. That's too much effort for us. Again, what we're doing is we're doing what I always felt that the developers should have done. They should have just given us these functions. So I'm trying to emulate it. We're writing APL, necessarily, not because we want to, but because we have to.

Richard Park

**38:58-39:05**

And what do you supply to your form utility function? If it can do everything, what do you tell it? What do you, what are the arguments?

Gary Bergquist

**39:06-39:08**

Oh, how does it work? I mean,

Richard Park

**39:08-39:15**

I guess we don't need to get the, get the API documentation. Unless you can do it in five, five minutes or less.

Gary Bergquist

**39:16-40:24**

Oh no, no, I can do it in five minutes or less. I mean, cause I don't have to tell you the details of it, but yeah, All right. So, so, um, FORM's definition, for example, um, basically you're providing an argument of property value pairs, you know, like caption mortgage calculator, two character strings, you know, so you're providing, and there's documentation for all these functions that explain, you know, what, what the structure is that you're, you're putting together. So because something like a form is, is not, such a simple array. There's enough information in it that it's not just a trivial array. You'll actually write a function of 10 lines where you're building up the array, the property value pairs, and then you'd call this Quad FORM, if you will. You call this function and it presents the form. And the philosophy, of course, is So is it defaults? Everything should default to something that's reasonable. So if you don't provide a title caption, it says something that says form or something. If you don't provide things you don't provide, it does a reasonable thing. So that if somebody says, I like this, except, well, you just go in and add a little something, change a little something.

Adám Brudzewsky

**40:24-40:42**

So I'd like to ask you about your philosophy for when designing those utilities. Say the user gives a faulty argument. Do you make them rock solid checking everything so that the user will never end up suspended inside the utility? Or do you assume they're used correctly?

Gary Bergquist

**40:42-41:40**

That's an interesting question. You know, the FORM utility in particular, I think the first time we developed the form utility was DOS-based, okay? And we learned some things, and then we redesigned it, and then we had to rewrite it for Windows, and then we had to fix it. Yeah. So it probably went through, like any good engineering project, probably went through five, six iterations before we finally got done. to where we were satisfied with it. Earlier on, yes, if you didn't give it the right arguments, the thing would blow up 18 levels deep and you had to try to figure out what was wrong. The fact that you gave it a character string instead of a number. But no, now... It validates everything. It validates all of the arguments, just like APL would. If you're giving something wrong, it gives you an error message. It returns an error message that tells you exactly what you did wrong, just like APL would point at the thing and tell you that it's a value error. It's the same thing. It's validating everything because otherwise it would take too long to try to figure out what you did somewhere in there.

Adám Brudzewsky

**41:40-41:56**

So I'm curious what you think of... of Dyalog's namespaces [05] then because that allows you some encapsulation of utilities without having to do a monolithic function and even APL plus plus are these mom objects I think oh I've never used

Gary Bergquist

**41:56-42:06**

any of those mom objects I understand that may be what they're for um I don't I don't No Dyalog APL intimately enough. I certainly understand what the, what'd you call them again?

Adám Brudzewsky

**42:07-42:07**

Namespaces.

Gary Bergquist

**42:07-42:43**

Namespaces, thank you. Namespaces are where you can combine a whole bunch of things and you can copy it in as a single thing and it's sort of isolated from all the other things. I mean, I think it's essential to have namespaces if you live in a world where the ideal APL function is three lines long. You have to do it that way, you know? And if you don't have namespaces, then maybe you have to write functions that are 3000 lines long. I don't know. I think it's valuable. And if I had them, I might use them in certain contexts. And I can't say. But yeah, I've got no problem with namespaces.

Conor Hoekstra

**42:44-43:02**

All right. I have a question that I've been hanging on to. I've been listening and enjoying the conversation. And I think we will try to get back because you took a break at one point. You said, all right, a break for questions. And then we will come back to the rest of your story. And I mean, we've been talking about Zark a little bit, but then we have to get to APL Tutor at some point in education.

Gary Bergquist

**43:02-43:03**

Okay.

Conor Hoekstra

**43:03-47:11**

Because that was in the original kind of introduction. But the question that I've been sitting on is when you started off, you know, talking to us, you mentioned the words... religious fervor. And I love the fact that you used those two words because it immediately took me back to when I first started falling down the APL, you know, Alice in Wonderland rabbit hole. I distinctly remember it was December 2019. I, for like the next one month, two months, was like almost intoxicated. I was like sending emails to people at work that I, you know, had found that had some relationship to APL and was just like, oh my God, like, did you, is your mind blown as well? And I remember specifically like coming back from a a Christmas Eve party. And, you know, I'd had several drinks and it's like past midnight. So it's technically Christmas. And there was a chalkboard on my wall. And I'm, I was like, I was just, Oh my God, you can do like a, a two wise reduction to get the differences between adjacent. And I was just like, I'm, I'm just like, I was like a, almost like a mad person. Just like, writing APL and chalk on a wall being like, I can't believe like you got to you got to use STD colon colon adjacent difference. And that obfuscates the fact that, you know, you can do any kind of generic binary operation, but you usually only use it for minus. And it's so beautiful in APL. Anyway, so when you said religious fervor, it took me back to that time when I was first discovering APL and I was I was in love with the language. And I went and actually looked it up because Phineas, past guest on the pod, he works in finance and he uses q a little bit at work and a lot recreationally and has used it in the past. I remember specifically we were chatting just via messages and we were talking about the curve of this kind of love for array languages and that I was saying something to him and then he responded. And this is, you know, I hope I'm not betraying your trust, Phineas. Just know that anything you message, I might end up reading on a podcast at some point. He said, I could be wrong. But you are in the honeymoon phase of APL. I had this feeling in q. It lasted five years. I still prefer q to everything else, but I now occasionally write C code to link to q. And when I do, I'm sad, but we can't do that stuff as well. And then he said right after that that Nick Psaris told him something very similar three years ago, and I didn't believe him. So enjoy the bliss. And this was what was the timestamp on this? Right. It says it was in 2025, six months ago. Okay, it was 2025. I said it's already been five years for me, so how long will it last? So this story I'm setting up to ask you the question is that you both mentioned the religious fervor, but then also have spent a significant amount of time and a part of your career writing these utility functions, is one of the things, especially when it comes to forms or, you know, graphical user interface, that I think array languages, it's not their, you know, superpower. Their superpower is the which... core of calculations. You know, there's this quote or phrase from functional languages where they say functional core imperative shell, where you try and write the, you know, internals of your application in the functional language, but then you have to kind of do some messy stuff that doesn't fit into the functional paradigm. And I think... Like array languages are the exact same way. You've got this array core and kind of messy shell or imperative shell. And this brings me to my question. How has this affected your love for APL and the religious fervor that you talk about? Because I definitely feel like I'm out of the honeymoon phase now. And a lot of it is because whenever I've gone to write like a unit test framework or a code formatter in one of these array languages... it loses some of the appeal and the beauty because you end up doing these things that APL isn't like a perfect fit for. And I'm, I'm curious, like what your experience has been using APL to write these utility libraries and how it's affected your, you know, love or, you know, feelings about the paradigm and APL.

Gary Bergquist

**47:12-47:32**

Unless I misheard you. I mean, you said the same thing that I just said, basically, the only thing is, you know, you've come up against the brick wall after five years or whatever, right? I'm still in the honeymoon phase after 50 years.

Conor Hoekstra

**47:32-47:35**

So how did you stay there? How did you stay there?

Gary Bergquist

**47:35-50:15**

Well, you just, you finally say, okay, you know, you go into a Zen state and you say, I'm not going to get the continuation of APL. APL is the implementation from the top down. They're not doing it anymore. You say, finally, you get to interfaces or other things and it's hard to work with. And you're saying, well, that's because APL is not good at these things. That's not true. APL is any implementation of a notation from the top down. They stopped developing it from the top down. And so if you need to generate reports, if you need to generate an interface, now, oops, I need some interface over to some other place where somebody has written something for me. So you're back down working at the very lowest level. In my case, it's like, no, I refuse. I refuse to not do it from the top down. If the problem is like designing a form, if it's designing a form, what are the minimum arguments you can provide to a function to give you the form you want? What are the minimum? That's APL. What makes you fall in love with APL is you're standing there at your chalkboard and you're going, I can't believe I can do this with three symbols. I can't believe that I can think of the problem and then translate it into notation that solves it for me so quickly. So all you have to do is just change the way you're viewing it. Instead of thinking it as a mathematical notation or symbolic notation, you want to think of it as a problem solving. If somebody presents you with a problem, and the problem, like I said, with the mortgage calculator is they describe the problem in a minute. So the question is, what notation could describe that problem in one minute? Then you implement that. the code that would take that notation and present the form. So, I mean, it's been fun, A, because I continue to work with APL. It's just not standard APL. It's our APL. It's our implementation APL. And it's been fun because I've had the opportunity to work on developing these incredibly sophisticated, the people that work in my firm, that work with me, When they go to put together a report, it's almost like what you described there, the giddiness of APL, except they're putting together a report or a form, right, which is like the driest thing you can imagine. But for us, it's just the joy. Somebody wants a form. Ten lines later, they got a form. They want a report with all of this and all this kind of stuff in there. And 15 lines later, it's done. And they want to change it. They just change a few things here and there. Oh, send it to Excel. You know, you send it to a printer. You want a landscape, whatever. You know, boom, boom. With no effort at all. It's been, the honeymoon's not over, is the answer to your question. So I don't know how to live life after the honeymoon. I just haven't gotten there.

Conor Hoekstra

**50:15-50:18**

All right, we'll let Adám follow up.

Adám Brudzewsky

**50:18-50:23**

So Gary, does it bother you that you cannot define names that are symbols, glyphs?

Conor Hoekstra

**50:23-50:24**

No.

Conor Hoekstra

**50:24-50:38**

That was, I was kind of thinking is when you were responding, Gary, I was thinking you're almost advocating for being able to extend the language and the notation to be able to handle different domains. Almost.

Gary Bergquist

**50:39-51:38**

No, no, no, no, no. See, here's the problem. All right. When the divorce happened, okay. And now the programmers of APL weren't basically on their own for extending APL. We all did it through necessity and we all went in different directions, slightly different directions. OK, so I have one that does this and someone else has one that does this and someone else. And I don't think the solution is let's let each of us, you know, implement their particular thing in a symbol. I think the problem is that we never should have gone in several different directions. You know, there should have been there should have been discussions with us about how it should be done. And then maybe there should have been a symbol by the developers of APL that implemented these things. I live with the fact that I have to copy my primitive function, if you will, into my workspace. It would be nicer if I could say QUAD this and not have to copy it in, but I don't really care. It's not a big burden for me to copy a function or two into the workspace.

Adám Brudzewsky

**51:39-51:46**

Explain to me your view on... The dividing line between system functions and primitives.

Gary Bergquist

**51:46-51:58**

There is no divide. I'm in the field. There's no dividing line. I don't care. I don't care if it's Quad fi or if it's a little symbol. I don't care. They're the same to me. They're primitive.

Richard Park

**51:59-52:03**

You'd have been happy with Quad plus. Quad plus. Quad Iota.

Adám Brudzewsky

**52:03-52:11**

Yeah. Well, if your plus has some of those, it has Quad enlist and Quad first and Quad expand.

Conor Hoekstra

**52:12-52:27**

Interesting, actually. So from your perspective as a builder of... solutions for people it doesn't actually matter to you if something is a single symbol or it's a quad function with a three to five character name it doesn't affect your feelings towards

Gary Bergquist

**52:27-52:41**

you know early early on in my APL career you know when I was working for stsc they were they would have competitions you know who can do this in the fewest symbols you know that was interesting academically interesting you know you know, fun.

Adám Brudzewsky

**52:42-52:44**

Just a bit of curiosity, when was that? Do you know approximately?

Gary Bergquist

**52:46-54:01**

Early 70s, from the 70s, 80s, 90s, you know, and they'd have the broken key problems, right? Well, how would you do this if your IOTA key doesn't work? And that sort of thing. I mean, those are fun. But remember, I don't, I mean, I've long since given up on that. I mean, my job is to make money by building APL applications, right? You know, so if I have to say Quad F-I-R-S-T, Quad first, instead of an up arrow or something like that, I'd rather not type six or seven characters, but I don't care, you know, because I'm only going to type it once and it's going to be in there and, you know. So I don't get a lot of thrill out of somebody saying, look at these seven or eight symbols and watch what they can do. It's like, it gives me a headache to have to think about that. If they do something useful, okay, then I'll use them, but I don't really care. What I really want to be able to do is I want to be able to translate a real-world problem into functioning code rapidly. and be able to modify it and maintain it rapidly. Get a call at 10 o'clock at night and the guy says it's not working and the markets are waiting for it and we're going to lose millions of dollars if you don't fix this in the next 10 minutes. I want to open up a small piece of code, be able to read it, modify it, and send them a fix quickly. I don't care about the symbols.

Conor Hoekstra

**54:01-54:02**

Wow.

Adám Brudzewsky

**54:02-54:10**

But do you not find it There's a difference in reading things between the symbols and the words.

Gary Bergquist

**54:10-55:00**

Well, that's okay. Readability. So now we're talking about maybe the tutorial a little bit. My philosophy on readability in APL is that every other line is a comment. You have a line of APL, which you can't read. I mean, you know APL, so you can read it, but it's work. So when I write a program, there's a comment line that says what I'm about to do, and then there's the APL, then there's the English, the APL, the English, the APL, the whole program is like that. So if somebody tells me it's no longer calculating the standard deviation correctly, I just scan through the English lines until it gets down to the standard deviation. Oh, it says we're calculating standard. Then I look at the APL symbols and fix them. Yeah. So there's my programs, all of our programs are at least 50% comments explaining what's going on. And then we labor over the APL as we have to.

Conor Hoekstra

**55:00-55:15**

Which is number five on the 14 myths. And number five is APL is unreadable. And the quote underneath it, which is something I assume you said during the talk is, you know what? Russian is unreadable. I don't know Russian, so it's unreadable. If you don't know it, it's unreadable. which I love.

Marshall Lochbaum

**55:15-57:19**

Maybe I can defend myself from the developer's viewpoint. One thing that sticks out to me is you said, well, a bunch of different people have solved this problem of providing forms, and they're all a little different. To me, that's really the big difference between primitives and system functions. I mean, I can say like you invented your form function because if you hadn't made that particular form function, if somebody else makes the form function, as we can see, it's a little different. You have to learn a new way of working with it to use that function. To me, primitives... almost entirely don't work that way. So like, if one person invents a reverse function, and another person invents a reverse function, [06] well, at least on lists, they're going to do exactly the same thing. So the reason why as a developer focused on primitives is because they're what you can't get wrong. Because getting stuff wrong when it's built into the interpreter is a really big issue, because it's got to stay in the interpreter forever because people are going to use it. So... I mean, if you came to me and said, well, I need to make forms in BQN. I need to have you provide something for this. All I can say is, well, I'm not very familiar with this. I don't know how to design a function like that. If I try, it's not really going to be that good. Whereas with primitives... And primitives are kind of sitting at the bottom of every computation. So you say you start from the top down. But I mean, you can start from the top down in a lot of places and you'll always find primitives like addition and like catenation. Those will be there in every problem. So what I provide with BQN is the things that you, is those things that sit at the bottom that you can use to build other things. And I say the solution for these, for things like building a form that you need to know a particular domain is really that we need to be better at distributing libraries and stuff. And yeah, I mean, maybe you could make an extension of BQN that builds in a lot of stuff for working with some particular domain. But really, I mean, I'd like to have a good library system so people can say, oh, I work with BQN plus this library, and that's good for me.

Gary Bergquist

**57:19-57:34**

I agree with what you're saying as far as the distinction between primitives and system functions. When I say that I don't care... it's because I don't have your job. So I don't care. I mean, if I were in your shoes, I probably do it the same way you do it.

Bob Therriault

**57:35-59:25**

It's really interesting because we've had some episodes where we go deep into the technical detail of how the primitives work. And I'm thinking of the one that we did with, oh, what was it? It was Replicate, I think, with Henry. And we went into great detail about how Replicate is done and all the different things that have to be done To me, that's the area, like as a person who writes J as a programming language, I don't have to think about all that. It's helpful to know where the shortcuts are, things that might work faster if I phrase them a certain way. But I don't have to think about that. That's the top down for me. The same way as if a user wanted to do something and they requested something from me, they want the same top down as I'm getting for the primitives. So the primitives I'm not concerned about. It's helpful to know a few things. They also are not concerned about how I'm putting the language together to deliver what they want. They just want the thing that works. So there's kind of a number of levels of top-down that are happening here. Right. And I think if I take your point properly, at the point where we're developing interfaces, it would be great if people were working together almost on projects to unify those so that you're getting the best at that level too. it's unlikely to happen because by the time you're moving away from the core of the language, it's naturally going to diverse like a river system. There's going to be different creeks all over the place. But the more that you could focus on one area and say, this is how we should do forms and have people working in that area, the better your results will be. The same way people working on the primitives... working to get optimum algorithms as things are discovered, they'll do better if they're working together as well.

Gary Bergquist

59:25-01:00:11

Yeah, I think a lot of the problems in the history of APL have to do with the fact that, you know, there have been several different APL developers. IBM with its APL, VS APL and APL2 [07] and, you know, everybody going off in slightly different directions. And it... You understand why it happened, but it really didn't help the language. The fact that they were able to sit down in a room at IBM when they originally implemented APL and make one single core APL with a common meaning for rho and epsilon and iota and all those other things was very valuable. And just unfortunately, things have gone in different directions. So you have these issues.

Marshall Lochbaum

01:00:12-01:01:01

Well, on the other hand to me, so I started out with J. Yeah. And after some years of working at Dyalog, I kind of got the notion that, you know, everything about APL was just kind of better designed and more thought through in a way. And I think the origin of that is really that Iverson got the language taken away from him. So actually, the stranding discussion that I was talking about plays into this. But he quit IBM and moved to I.P.Sharp and worked on Sharp APL, and made this grounded APL. And really didn't have, he didn't have the same popular support that other developers had. He wasn't moving in the direction that the users wanted as much. And so I think in a lot of areas, he just kind of stuck with wrong designs that nobody could talk him out of and things like that, so...

Gary Bergquist

01:01:01-01:01:11

Why would you say that was though? I mean, what was it? What was his objective that he would go down that path that we look back now and we say, That wasn't so good.

Marshall Lochbaum

01:01:11-01:01:14

Well, I think he just wasn't happy with other people telling him how the language should work.

Gary Bergquist

01:01:14-01:01:33

Well, that would be Iverson. Yeah, I think that – I think the problem is that he wasn't solving problems. He was writing a dictionary. You know, I mean his – He wanted to create this language, and that's fine. And that's fine. I mean, that was his definition of APL. But my definition...

Marshall Lochbaum

01:01:33-01:01:53

Yeah, and I don't object to him working on J after that at all. However, I think APL is better. Yeah. And not just any APL, but specifically the APL that's descended from Bob Smith's NARS and IBM's APL2.

Gary Bergquist

01:01:53-01:02:33

I agree. I agree. But again, what's the basis for that? And for me... So it's a computer programming language, meaning you're going to use it to develop applications to solve real world problems. So to me, the acid test is how well does it do it? You know, and if J turns out, again, you've got to be thinking about it as building a language and then let's see if it solves real world problems is backwards. You have to be out there. facing the fires and say, I can't do this easily. What could I use by way of a notation that would let me do this easily? I think you end up with something that's just so much richer.

Adám Brudzewsky

01:02:33-01:03:18

I think that's touching a good point there. Originally, Iverson's notation was to solve a problem, but describing processes. There were programs that needed to be done, do this, do that, and there was no good notation for formal notation for describing those processes. And then the notation was used to design the IBM 360. Again, it was always led by the need to, first. And then it was linearized and made into an actual programming language and people started writing proper applications with it. I have a sort of a controversial question maybe. Did Iverson ever program in APL?

Gary Bergquist

01:03:18-01:03:51

I have no idea. I have no idea. But I mean, I will say What he came up with, what they came up with was ideal for the mathematical – any mathematical thing you're trying to do was all there because it was – he was solving those problems. that You know, you got your Quad divide for doing, you know, matrix inverses and stuff. And flipping things around and all that was just marvelous. But I think it kind of ended there. I mean, yes, good question. Was he ever out there, you know, trying to build an accounting application? I don't think so.

Marshall Lochbaum

01:03:51-01:04:15

Yeah, well, in J, you have stuff added even like taking a permutation and giving the cycle representation of it. I mean... Yeah. In some areas of mathematics, maybe you say, well, gosh, this is something that I really need to investigate permutations. But I mean, I'm fairly mathematically oriented and it's really just not something that comes up for me. So he was solving problems, but they were very far down a particular path.

Gary Bergquist

01:04:16-01:04:19

They weren't my problems, put it that way.

Adám Brudzewsky

01:04:19-01:04:32

We might have a very ironic situation on our hands where the person who taught the world's first computer science course was not a programmer and didn't program.

Marshall Lochbaum

01:04:32-01:04:33

Wrote the book, A Programming Language.

Adám Brudzewsky

01:04:34-01:04:42

Yeah, exactly. He wrote a book and is considered the father of something that just has the generic name, A Programming Language, and wasn't the programmer.

Conor Hoekstra

01:04:42-01:05:23

Well, I actually had that thought when, Gary, when you were describing your 10-word description, and I believe the first five words were an implementation of a notation, and... When you paused and said that, I was like, I mean, well, technically, the implementation didn't come to like 1966 or whatever. And it started out just as a notation. There was no implementation similar to Lisp. I mean, McCarthy invented Lisp. And I think a student wanted to implement it. And he said, oh, it's unimplementable. And then the student went and did it. And he's like, oh, I guess it is a programmable language. But anyways, I had that thought that the implementation aspect didn't happen until like eight years or 10 years later after...

Marshall Lochbaum

01:05:23-01:05:29

Well, but it wasn't actually APL until it was implemented either. I mean, there were a lot of changes that were made in implementing it.

Conor Hoekstra

01:05:30-01:05:36

Right. Yeah. The APL in the book is very, very different than the linear APL that ended up in APL 360.

Gary Bergquist

01:05:37-01:05:58

And as an aside, I think you're on the right path if you start by saying this is not implementable. I can't think of how many of the utilities we've built where that was my first thought is there's no way I can implement this. But then when you think about it a little more and you finally find a way to do it, it's wooo – You know, it's nice.

Adám Brudzewsky

01:05:59-01:06:13

You wouldn't have had that woo if STSC had added another thousand quad functions to do every conceivable thing you want to do. I think another value of APL and similar languages is you actually having fun programming.

Conor Hoekstra

01:06:13-01:06:48

All right. I don't want to hijack this conversation because this has been great, but we already are well past the hour mark and we still haven't actually gotten to the end of, well, not the end, but to the point in your APL journey where I assume you're still working at Zark Incorporated. But at some point you got involved with teaching or maybe that was a lot earlier. And APL Tutor, I think, was kind of the genesis because it got mentioned either in the last episode or two episodes ago. And then we thought, why haven't we had Gary on? And so tell us about APL Tutor and education of APL.

Gary Bergquist

01:06:48-01:10:16

All right. So working at SCSC for this computer time sharing company, you were making your money by having APL being used on mainframe computers. And you weren't making money necessarily by doing the programming, but by educating. So when I was in the Hartford office of this company, all of our clients were insurance actuaries. And so we would hold classes and the actuaries would come. We teach them how to use it. They'd go away and they sit down at their terminals and they were delighted. Actuaries or assimilate APL wonderfully. So they sit down and they would build all of these kinds of things and they would use the resources of the computer. We'd make money. I taught many classes. And after I left STSC, I continued teaching APL classes to mostly to actuaries because they were heavy users of it in the Hartford area. So I think I've taught probably close to a thousand classes. I decided finally that I was tired of teaching classes. You know how that is when you're teaching the same thing over and over again. You can't remember what you said before. And so I decided I would put it in the form of a computer program and had a friend who I went to college with who was not in the APL community, but he was an expert on computer-based training. So I got together with him and I said, how would we do this? And it went down a path that I never would have anticipated. I really didn't know anything about writing computer software that would do computer-based training. But he told me what it needed to do. It needed to be able to interact with the user frequently and had to have a certain amount of humor and stuff. So I then took my experience at teaching APL, and I taught enough classes that anytime I'm covering a particular thing, say the difference between scalars and one element vectors, I know for somebody who doesn't know APL, I know what they're thinking, and I know where they're confused, and I know the questions that they're going to have. So based upon that, I was able to write the tutorial and put in the various problems and so on, working with this guy to build this ZARC APL tutor. [08] And for a while, we were selling it. People wanted to use it. And when they used the ZARC APL tutor, they also got enrolled in a subscription to – they got a free copy of the ZARC Library of Utility Functions. And they also received the quarterly Zark Tutor Newsletter, which was a newsletter that described various APL problems. And it was a little crossword in the back that had APL symbols running up and down it instead of letters. And then from there, you know, I didn't have to teach any classes anymore. Sold a certain number of those things. And they just generally gave it off to both Dyalog APL and APL 2000. And the tutorial is available through either of them to use. And we haven't spent much time keeping it up to date for all of the new operators and stuff that exist now. But it certainly gives you enough that it's been an excellent training tool. Anytime we hire somebody new, we just plug them into the tutor. And depending on the user, the person within... Within a month, let's say, they're at the point where the information is falling out of their ears as quickly as it's going into their eyes, and they shouldn't keep going with the tutor. At that point, we've got to actually plug them into real-world problems, and then they can go back to the tutor and continue on. But there's no substitute for it, I think, for people who need to learn APL.

Bob Therriault

01:10:17-01:11:25

As part of my education, I had an opportunity to do some instructional design and to be graded on how well I was doing it. And the tutor is a really good example of good instructional design. Your friend is a really good instructional designer. I can see what he's doing and I can see how he's doing it. And it's well put together. I think that's probably a big part of the success of it. It seems to me there's a reflection of the same thing that you're talking about. If you can describe the problem, can you solve it in five minutes? I think the tutor kind of does the same thing. Rather than having to go out and give a course to 20 people, you've created an application that people can go into and pull out that same information and a number of things. You can go to different areas if you're specifically interested in one part of learning APL and not others. You can jump to those areas in this. It's very flexible that way. Again, to me, that's a lot like when you were talking about the forms. You want a form, but you want it to do this. Well, we'll give you the option to do this. To me, that's all over the tutor as well.

Gary Bergquist

01:11:25-01:11:45

Because it's self-paced. Some people do actually jump around in the various units. I mean, they're designed to go from one to the next, but they'll jump around. And you finish a unit, they've got the reading problems and the writing problems to make sure you actually understand the material. If you don't, it's going to become clear. You better go back and read through it again. It works.

Conor Hoekstra

01:11:46-01:11:55

And this is the APL, well, I think it's under a different domain, but it's the tutor that is available online for folks that want to go and take it for a spin, correct?

Gary Bergquist

01:11:55-01:11:59

Yeah, there's a few sites you can go to to be able to use it, yes.

Bob Therriault

01:12:00-01:12:29

I accessed it through Dyalog, so I can put a link into the show notes for that if somebody wants to go in and play around with it. It's not hard to find. I think it's under learning. But we'll have a link there that you can go in and take it for a spin. I guess you haven't really made changes to it, as you were saying, since it's been developed. But to me, the instructional design part of it is solid. So I think all you'd be changing might be a few different details depending on how the language might have evolved.

Gary Bergquist

01:12:29-01:13:05

Yeah, that's it. A few missing primitives and things like that. I mean, the latter chapters are into things like readability and efficiency. So they're no longer teaching you the primitives, but they're teaching you how to make sure that the code that you write is good and formatting, you know, the design requirements for formatting reports and working with files and how you design files and stuff like that. As I say, you know, after a while, as somebody actually using the tutorial, you finally say, I've had enough. I need the real world now. I need to see if I really know how to use this stuff.

Conor Hoekstra

01:13:05-01:13:21

Yeah, I was just clicking through a few of them in the scan section. And, yeah, it's got a very interesting way of there's like conversational aspects of you know, a back and forth of, oh, we've got the reduction primitive. Maybe we can add something else. And it's it's.

Gary Bergquist

01:13:21-01:13:56

That's right. You have you have the three implementers who are having these discussions. I remember when we first implemented that I needed little icons for these instructors. So I've got three sons. So I gave each of them the assignment of sitting down at the computer and designing little faces for each of these three. They're not actually intended one of them to be Adin Falkoff or Ken Iverson or something. Instead, my kids just came up with little funny faces that they liked. I don't know if they're still the same faces now on the most recent version of it, but that's where they came from. So yeah, they have their discussions what to do.

Adám Brudzewsky

01:13:56-01:14:41

Then we shouldn't discard them in the new version. Somebody redrew those faces, but we should just make new high definition versions of them if they have such a real backstory. I'd like to hear a little bit about something special in the tutor that's unique there. There are some times when it asks you to write a solution to something. And then you do something clever where it gives you feedback on your solution saying like, Oh, you can also write it like that, or have you considered this kind of thing? It also catches certain types of mistakes cleverly and corrects them. And I'm curious if you could speak a little bit to how you did that and what the thinking was there.

Gary Bergquist

01:14:41-01:16:06

Yeah, sure. So at the end of each unit chapter, if you will, there's what we call reading problems, and reading problems are it says, all right, here's an expression. What do you think you're going to get as a result? And then they press the enter, and they see what it is. Now, that's passive. If somebody could just keep pressing the enter key and say, yeah, yeah, it's what I thought. So the acid test is the writing problems, and the writing problems are word problems. They say, how would you do the following? Suppose you have three individuals, and they each give this and that, and so on. What APL expression will solve that if you're, if V is a vector of the amount sold or whatever. And what we did is we know what we want for a result. So we take whatever expression they give us and we execute it and see if we get the right result. If we don't get the right result, we say, well, no, that's the wrong number. Or we say, well, you got the right value, but it's not the right shape. Or we can check the shape and the rank and that kind of thing. So we can give those responses. And if it turns out, we write down every way we could think of doing it, every way we could think of computing the average of a set of numbers. And they give one and we say, oh, all the ways you could have done it were this. But if it's any one of the ones that we're expecting, then we say, you know, that's correct. Or we say it's the right answer and here's some other ones. So, I mean, that's all it is, just basically simple. We've got a list of acceptable answers and we know what the result is and just some simple checking on what they gave us as we execute it.

Adám Brudzewsky

01:16:06-01:16:08

So it's actually, it's less intelligent than I thought.

Gary Bergquist

01:16:08-01:16:13

Absolutely. Hard-coded problem. Not AI.

Adám Brudzewsky

01:16:14-01:16:19

I was trying to figure out how it worked and I couldn't find the code that did this kind of thinking. That's all it is.

Bob Therriault

01:16:20-01:17:25

It's just what they used to call shoe leather. You get out on the streets and you do it until you know what they will be and that's what you write down. I found the areas where the discussions were really, that was one of the more powerful things I thought, because you put the learner in the position of saying, so here's the problem and we'll talk, you know, let's let the designers of the language talk through how you would solve this. And we could do it this way, or we could do it this way, or they could do it this way. And so by the end of it, the learner has a context, a much deeper context for what the problem is and how it was solved. And to me, when I was reading those parts, I thought, I really get this. I know exactly what they were trying to do, and this is how they did it. So now when I look at the solution, it just gloms onto my brain much stronger because I feel like I was in that conversation. We came up with this and it works. And that's why we did it that way. Did you find the same thing when you were writing it? Were you thinking that way?

Gary Bergquist

01:17:25-01:18:08

Well, of course, I was not. in the room with these implementers or designers as they were trying to decide how to do these things. But what I was is I was in the classroom with students who would be constantly asking all kinds of questions. Why don't you do it this way? What about this? Or they would just go down the wrong path and they would do it incorrectly from a misunderstanding of how it works. And so with that in mind, I would concoct a little dialogue between these implementers. Well, that doesn't make any sense. Why don't you just do this? No, you can't do that because of this. So you present all of the different arguments that are probably floating around in the brain of the student who's trying to learn this thing. And you can... Give it a little bit of a tale in that fashion.

Bob Therriault

01:18:08-01:18:13

Well, and you talked a little bit about humor and there's sort of humor sprinkled through the whole thing. So it stays entertaining.

Gary Bergquist

01:18:14-01:18:36

Well, it's Gary humor. You know, I got to say it's some people are not fans of it. I've had people say, well, it's OK, except I didn't like your jokes. You know, it's like, well, OK. It entertained me and it entertains the people that I know. It reflects my upbringing. But yeah, some people are not crazy about the jokes, but I think it keeps them awake.

Bob Therriault

01:18:37-01:20:04

And actually, I think when we were doing the test for this, you came up with a really interesting insight. I'll talk about it now because I think it's really important for people who follow the array languages and wonder why there's so much blowback sometimes to... those are crazy. I don't get it. What's going on. And, and you were saying it's kind of, you feel the same way with people say you were responding with flame wars and hacker news or whatever. [09] You said, you know, they're probably the same way as a person who's sitting in a group of people and a joke is told and they're the one that don't get the joke. So immediately they're defensive and they're angry and they want to know why all these other people are laughing. But they don't get the joke. And I think that was an interesting psychological approach to seeing what sometimes the resistance to the array languages is. If you think about it as a person who just doesn't get the joke, and to have the joke explained doesn't always work, because by the time a joke is explained, you don't get it anymore. But maybe over time, if they develop the nuance to understand what the joke is, they'll come on board. But it's a much harder process for somebody who maybe feels like they should understand it. But for whatever reason, their background in other programming languages, maybe they just don't get this one. And everybody else is laughing. They're going to feel a little... A little angry about that.

Gary Bergquist

01:20:04-01:20:55

After decades of APL, you definitely come upon people who do not like APL. And I think that's part of the reason. APL is a very abstract language. And so if you're good at thinking in abstract ways, then you're fine with it. But I think it's like a learning calculus. Some people just can't. You know, that's fine. I mean, that's just the way they are, but they just can't learn it. And some people can't learn. I mean, probably all of us have tried to teach our spouses APL and learned, uh, no, you know, or our friends, you know, some people can get it. Some people can't. And if you can't get it and people are pushing you to say it's a wonderful thing. Well, that's like you say with the joke. It's like, don't explain the joke to me. It's just not funny. Don't tell me it's funny. It's not funny. And I resent that you keep implying that it's funny. And I resent that you imply that APL is a good language because it's not because I don't understand it. Leave me alone.

Bob Therriault

01:20:55-01:20:56

Yeah, that's pretty much it.

Conor Hoekstra

01:20:58-01:21:28

I don't think I've tried to teach my spouse yet, but we're not fully married. So you got to wait till it's harder for her to leave me just in case things don't go well.

Anyways, we're definitely past the hour mark now. I should maybe ask, are there any final questions? I feel like we should definitely have you back, Gary, because I feel like we, you know, I interjected a couple times and switched topics so that we could make sure that we didn't end up spending three hours here. But I bet we could have easily spent three hours if I was not interjecting.

Gary Bergquist

01:21:29-01:21:34

I'm an empty vessel right now. I've said everything I could possibly say. There's nothing left.

Conor Hoekstra

01:21:36-01:21:58

All right, well, if that's the case, if you, the listener, have questions either for us Yeah. or for Gary or thoughts or comments, or you also have the same religious fervor and have managed to stay in the honeymoon period, and you've got advice for myself or other people that are potentially listening that have not, you can send those thoughts, questions, or comments to...

Bob Therriault

01:21:58-01:22:53

Contact AT arraycast DOT com. And we, this last week, we had somebody actually... send me a note that I had, although I had a link, I think it was for understanding APL1 and APL2, I had a link that took you to the page for it. The download link didn't take you, it broke at that point. So I had sort of, I was one link short of getting what you needed. They not only found that problem and found the proper link to APL1 and APL2, but also found a link to APL 3 and 4. So I was able to update the show notes that way. So much thanks to, his first name was Mark. I won't use his second name. I gave him credit in the show notes. But it's just great when we get responses like that on top of all the other responses we get of people asking questions or suggesting guests, but Contact AT arraycast DOT com is how to get in touch with us.

Conor Hoekstra

01:22:53-01:23:03

And thank you so much, Gary, for taking all this time. This has been a blast. From the get-go, as soon as we were talking about your experience with APL, I was like, oh, yeah, I remember.

Conor Hoekstra

01:23:03-01:23:05

Thank you for inviting me.

Conor Hoekstra

01:23:05-01:23:12

No, this has been absolutely awesome. And like I said, we'll have to do this again in the future once your vessel is refilled and you're ready to go again.

Gary Bergquist

01:23:13-01:23:14

Okay, be happy to.

Conor Hoekstra

01:23:14-01:23:16

With that, we will say happy array programming.

Conor Hoekstra

01:23:16-01:23:18

Happy array programming.

MUSIC

01:23:19-01:23:32

</details>
