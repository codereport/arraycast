---
title: "Episode 89: The Iverson College Experience"
date: 2024-09-28 00:00:00 +0000
episode: 89
keywords:
- array-programming
- array-languages
- apl
- uiua
- bqn
- q
- k
- j
- kap
- co-dfns
mp3-url: "/assets/audio/episode89.mp3"
episode-type: full
explicit: "no"
block: "no"
layout: podcast
excerpt_separator: <!--more-->
redirect_from: "/episodes/episode89-iversonreflect"
---
Participants of the 2024 Iverson College reflect.https://www.arraycast.com/episodes/episode89-iversonreflect 01:16:14
<!--more-->

**Host:** Conor Hoekstra

---


## Show Notes

Array Cast -  September 27, 2024

Thanks to Bob Therriault for gathering these links:

**[01] 00:01:55**

- [Iverson College](https://iversoncollege.com/)
- [APL Programming Language](https://aplwiki.com/)
- [Aldus Manutius](https://en.wikipedia.org/wiki/Aldus_Manutius)
- [Arthur Whitney](https://en.wikipedia.org/wiki/Arthur_Whitney_(computer_scientist))
- [Trinity Hall Cambridge](https://en.wikipedia.org/wiki/Trinity_Hall,_Cambridge)
- [St. Edmund Hall Oxford](https://en.wikipedia.org/wiki/St_Edmund_Hall,_Oxford)
- [Suffolk Farm](https://iversoncollege.com/)

**[02] 00:09:50**

- [The ArrayCast podcast](https://www.arraycast.com/)
- [Kai Schmidt Episode 77 on ArrayCast](https://www.arraycast.com/)
- [/episodes/episode77-uiuaKai Schmidt Episode 63 on ArrayCast](https://www.arraycast.com/)
- [/episodes/episode63-uiuaBrian Ellingsgaard Episode 68 on ArrayCast](https://www.arraycast.com/)
- [/episodes/episode68-brian-ellingsgaardRayLib APL](https://www.dyalog.com/user-meetings/dyalog24/presentations.htm)
- [Kamila  Episode 74 on ArrayCast](https://www.arraycast.com/)
- [/episodes/episode74-kamilalispKamila's presentation at LambdaWorld](https://lambda.world/speakers/?speaker=Kamila%20Szewczyk)

**[03] 00:21:50**

- [Alex Unterrainer's blog](https://www.defconq.tech/)
- [Iverson College Episode 87 on ArrayCast](https://www.arraycast.com/episodes/episode87-iversonsession)
- [q Programming Language](https://en.wikipedia.org/)
- [/wiki/Q_(programming_language_from_Kx_Systems)k Programming Language](https://en.wikipedia.org/)
- [/wiki/K_(programming_language)J Programming Language](https://en.wikipedia.org/)
- [/wiki/J_(programming_language)BQN Programming Language](https://mlochbaum.github.io/BQN/)
- [Uiua Programming Language](https://aplwiki.com/wiki/Uiua)
- [Data Intellect](https://dataintellect.com/)
- [Data Intellect BootCamp](https://dataintellect.com/)
- [/solutions/our-services/kdb-training/classroom-training/](http://q201.org/)
- [q201.org/](http://q201.org/)
- [KX.com](http://kx.com/)
- [kx.com](https://kx.com/)
- [New York City J User's Group NYCJUG](https://code.jsoftware.com/wiki/NYCJUG)
- [Hope Conference 2024](https://hope.net/)
- [Past NYCJUG Meetings](https://code.jsoftware.com/wiki/NYCJUG)
- #Notes_on_Past_Meetings

**[04] 00:34:00**

- [Dyalog APL](https://www.dyalog.com/)
- [Aaron Hsu Episode 19 on ArrayCast](https://www.arraycast.com/episodes/episode19-aaron-hsu)

**[05] 00:42:08**

- [Brandon Wilson Yaml Presentation](https://www.youtube.com/watch?v=bb6sIAJjMeM)
- [Co-dfns Compiler](https://scholarworks.iu.edu/dspace/items/3ab772c9-92c9-4f59-bd95-40aff99e8c7a)
- [Morten Kromberg Episode 21 on ArrayCast](https://www.arraycast.com/episodes/episode21-morten-kromberg)
- [Christ's College Cambridge](https://en.wikipedia.org/wiki/Christ%27s_College,_Cambridge)

**[06] 00:49:20**

- [Combinators](https://combinatorylogic.com/)
- [APEX Compiler](https://www.academia.edu/81780487/An_Overview_of_the_APEX_Compiler)

**[07] 00:58:11**

- [APL Orchard](https://aplwiki.com/wiki/APL_Orchard)

**[08] 01:01:10**

- [ADSP # 196 Aaron Hsu](https://adspthepodcast.com/2024/08/23/Episode-196.html)
- [ADSP # 197 Aaron Hsu](https://adspthepodcast.com/2024/08/30/Episode-197.html)

**[09] 01:10:54**

- [Westwood Lake](https://www.nanaimo.ca/parks-search/Parks/32-Westwood-Lake-Park)
- Contact AT ArrayCast DOT Com

<details markdown="1">
<summary><strong>Transcript</strong> (click to expand)</summary>

Transcript

Transcript prepared by

Bob Therriault and Adám Brudzewsky

Show Notes

00:00:00 [Aaron Hsu]

I want the equivalent of lots and lots of opinionated discussions covering lots of topics with somebody giving some crazy talk and letting everybody explore the range of possibilities in the most high bandwidth way possible. That's what I like.

00:00:16 [Music]

00:00:25 [CH]

All right, we are here at Iverson College 2024 on location and we are starting off this special episode of Raycast by interviewing our usually regular panelist. But today you are not a panelist, you are a guest, but more importantly, the warden of Iverson College. And this is not the first time. This is, I think, the nth time. Hopefully you'll fill in n if you can remember n. So maybe tell us a little bit about the history of Iverson College, when it started, what the motivation for it was, and then maybe a little bit about this edition because this is, I think, a slightly different edition and the first one in several years. It's definitely the first one I've been to and I think the last one was before the pandemic. So it's been a while.

00:01:09 [Stephen Taylor]

It has indeed been a while. And no account of the history should omit the central role of Ray Cannon in its genesis. [01] This goes back sometime to when Paul, Ray's son, was I think still in school and he was a video game enthusiast. And Ray was telling me how Paul and his friends would hire a church hall for the weekend and they'd bring along a network and all their PCs, they set up a fast internal network and they'd stay up all night eating pizza and playing video games.

00:01:56 [CH]

I had no idea that this is where the history is going to start.

00:01:58 [ST]

Yeah, so he was telling me all that and then we just stared at each other, we want to  do this, but not with video games, we want to do it playing with APL. And Ray christened these events a moot. I think we held the first one outside Stansted, somewhere near Stansted Airport. And to our astonishment, we had people flying in from all over. We didn't arrange any accommodation. The idea was you brought a sleeping bag and your laptop. Some people stayed bed and breakfast. Ray put on a big barbecue, it was mad. We had this crazy weekend and we did a few of those. So that was one of the roots of Iverson College. Another was Miki taking me to Venice. I think it was her third trip, my first visit. So we spent a day lollygagging around looking at all the buildings and thinking, wow, this is like Disneyland. No, this is the original. But I'm a terrible tourist, so after a day of wandering around, I said, I can't do this anymore, just staring at stuff. So I marched us into the tourist office and said, Aldus Manutius used to live here. He made books, did you keep any of them? Aldus Manutius was a famous printer and typographer at the end of the 16th century, 15th century. Completely revolutionized type design. They proposed to send me to his house, but I said, no, I don't want to see where he ate breakfast. What about the books? Well, those, it turned out, would be in the Biblioteca Nazionale Marciano, the National Library, which was just around the corner off the Piazza San Marco. So I go around there, and there's a big sign in the entrance saying, not open to visitors. And one of my greatest achievements, I managed to blag myself a reader's ticket in Italian, in a language I don't speak. Which really means I pretended to speak Italian until they got annoyed enough to give me a reader's ticket. And I sat in the library all day looking at ancient books while Miki went around and took photographs. And I realized, this is the way I like to travel. I have some work to do, and I see the city in peripheral vision. Came out to lunch, to meet Miki for lunch, and we went out for dinner. And I must have been, I think, maybe around 2007. Anyway, the next time I saw Arthur Whitney, I said, this is what we're going to do. I'm going to rent a huge apartment in Venice. And you'll come over, and you'll bring your work, and we'll get a few others of the guys. And we'll just work that, and go out for lunch and dinner. Because I really miss when we all used to work in offices together, and we're looking over each other's shoulder and getting inspiration and seeing what you're doing. I learned so much from other people that way. The idea just stayed dormant until I went to a summer school at a college in Oxford. And I realized, this is really easy. I thought it was logistically difficult. So when I got home, I booked 20 rooms for the next summer, for a week in the vacation at a Cambridge college. And invited people to come and live with me like a student for a week, just bring their work. No program, just meals, and our work would be interesting enough. That was the origins of Iverson College.

00:05:32 [CH]

Wow. And so you had a previous edition of this in Venice.

00:05:37 [ST]

We never did it in Venice. That's still the dream of the big palazzo.

00:05:42 [CH]

Oh my goodness.

00:05:43 [ST]

I don't know if we'll ever do that. But that would have been just half a dozen. This way we can get 25 people, which is effectively the limit. That's about as many as we can get around a big table and still hold a single conversation.

00:05:58 [CH]

That would be-- I mean, Venice is now this is on my bucket list that I do not have. Please, if there's a limited number of folks, make sure I'm on the invite list, especially if Arthur's there. I'm not sure if Arthur's listening to this, but that would be amazing. So I know that you've had, I think, two different installations that were at Trinity Hall, which is where we are. I'm not sure if they were at Trinity Hall.

00:06:19 [ST]

We held it previously twice at Trinity Hall. We held it once or twice at St. Edmund Hall in Oxford, Teddy Hall, as they call it there. One or two other places, and then twice at a converted Tudor barn in the middle of Suffolk.

00:06:39 [CH]

I have heard about the barn additions of this from Adam because he-- I'm not sure if he had an affinity for those ones, but he's definitely told me about them.

00:06:47 [ST]

Yeah. Well, the barn is just the loveliest place, a big converted Tudor barn, which with big tables inside, sofas, it makes a great workplace. There's a kitchen at the end. We had our own chefs.

00:06:59 [CH]

Wait, this doesn't sound like a barn.

00:07:02 [ST]

Well, it was a barn in Tudor times, but these days it's used for like wedding parties and so forth.

00:07:08 [CH]

Okay. So maybe closer to like a mini banquet hall or something like that. Yeah, that's pretty good. I was picturing haystacks in the corner and like--

00:07:11 [ST]

The haystacks aren't too far away because we're on a farm in the countryside. The accommodation there is a bit tight, but having our own cooks and just being our own party, we're kind of half conference, half house party, as you've experienced this week.

00:07:34 [CH]

Yeah, yeah. I mean, I've heard also-- two, did you have one in Italy at some point? Not in Venice, but I did hear, I think-- I'm not sure if it was the most recent addition, but there was one where-- I heard that one referred to as like half work, half party in some-- I don't know if it was Tuscany or something like that.

00:07:51 [ST]

It was in Tuscany. Yeah, we were in a villa just outside Lucca in Tuscany. In many ways, it was both the best and the worst that we've had. The best-- I think people just had the most terrific time there. We were next to a vineyard. We were drinking their wine. We had organic food suppliers doing deliveries to the house. We had our own chefs. It was amazing. But from the point of view of running it, it was a nightmare. It reinforced all my worst stereotypes about doing business in Italy. I think the venue double booked us at both ends.

00:08:32 [CH]

Perfect. That's always what you're looking for when trying to book something out for a double digit number of people. That's the history of Iverson College. How does this addition in 2024 compare to years past? Because I've heard from speaking to folks that have been to prior additions to this, that this one has a little bit of a different feel due to a different makeup of the participants this year.

00:08:56 [ST]

That's definitely true. It has been a while, and that is in large measure due to the pandemic, which changed so much. I really doubted that we'd do it again. I thought people have concerns about going and living with strangers for a week, epidemiological concerns. Everybody got used to working on Zoom calls. We massively normalized. And I got no enthusiasm for encouraging people to take plane flights. I really didn't think we'd do it again. But when I mentioned it to people, you included, their enthusiasm for it really took me by surprise. But the biggest difference has been that since we last did it, the ArrayCast started. [02] So we've always made a point of including younger people to kind of transmit the APL, the Iversonian vibe, and the knowledge and the culture. But this time, the ArrayCast has widened the network so much. We've got all kinds of really interesting young people who've got their own ideas, like Kai with his Uiua language, Kamila from Sear Brooklyn with her KamilaLisp. And that, yeah, it's way livelier, way more interesting. And that's almost entirely because of the ArrayCast.

00:10:18 [CH]

It's hard to.

00:10:20 [CH]

It's hard to live in a parallel universe, but potentially the ArrayCast led to this having, I don't want to say life breathed back into it. But you were saying at one point that you didn't think it would happen again. If the ArrayCast had any small part in bringing this back to life, I'm very, very thankful because this has been an awesome week. I'm not sure if you have any high-- because I think we're going to transition the rest of this podcast. We're going to try and bring folks in and just ask them about their experience, what their favorite moments are. So maybe that's a good way to end with you. What were your highlights? Technically, we have a day left, so we do apologize to Aaron. And I think actually it's Bob and friends that have a talk after dinner, or maybe it'll be at dinner. So those might end up being the highlights, but the listener will never know until maybe we mention it a couple episodes from when the listeners are listening to this. But up until now, what have been your favorite moments of this edition of Iverson College?

00:11:15 [ST]

My context for this is a YouTube video given by a guy down in Sydney in Australia. I think it's definitely Australia, in which he was giving-- it might have been a TEDx talk. But he was talking about the array paradigm and saying there's a danger that this amazing paradigm in computing may actually get lost because it was strong in a previous generation. And the highlights for me have been seeing the younger people here connecting and binding together. And it's like, they're going to carry this stuff on. And if we're doing nothing else but generating and fostering that, job done. Yeah, no, that is super, super important.

00:11:56 [CH]

I think actually I know the talk you are referring to. It was a talk by Dave Thomas at YAL, potentially. Maybe it was a-- I'm thinking of a different talk. OK. But in a similar talk. It's no longer on YouTube. I had a link to it in a previous podcast episode. And it's all been taken down because they shuffled some stuff around. But he made a similar comment saying there's this risk of this generation of shape thinkers and array thinkers that could get lost if we let languages like J and APL wither away. But clearly, that is not-- it's not what's happening.

00:12:36 [ST]

Not what's happening. We're glad at Iverson College. And hopefully, if this continues in future years, we'll just be able to see more of this. That's so exciting.

00:12:43 [CH]

Yeah. Any final things you want to say to potential listeners or potential participants? Will there be a future Iverson College, if not 2025, 2020x in the future?

00:12:54 [ST]

From the buzz here, it seems clear that we've got to do this again. And the big challenge for me is always to keep it surprising.

00:13:04 [CH]

Oh, so surprising meaning a different location. Will it be Venice, folks? We don't know. I can see from the look on Stephen's face the pain, the memories of dealing with the Italians. I don't want to put them all in one bucket. But I'm not sure if that's what the look on your face was. But potentially a different location, maybe new, maybe no one that will be revisited. But I definitely look forward to hopefully going to a future one of these. And thank you so much for all of your work putting this conference together. It's been amazing.

00:13:33 [ST]

It's such a pleasure. It's been so rewarding.

00:13:42 [CH]

All right, we're here with our first attendee of Iverson College 2024. Previous guest on Arraycast, I looked it up. It was episode 68. Link will be in the show notes if you haven't seen or heard that episode, I should say. It's Brian Ellingsgard. Did I get that pronunciation? No.

00:13:57 [Brian Ellingsgaard]

Brian Ellingsgaard.

00:14:00 [CH]

Brian Ellingsgard. Better. All right. We'll go with Brian. If you have listened to episode 68, he is the individual behind the Raid BQN library. And I think now Raid BQN APL library. I'm not sure if it's out yet. But we're here to talk about Iverson College. You've been here for the past four days. We've got one day left. Tell us about your experience, what you've gotten out of this conference, and maybe some of the highlights over the last couple days.

00:14:25 [BE]

Yes. So, first of all, Raylib APL is out, but unstable. Quick note. But my experience with the college has been very fun. Meeting all of these fantastic, amazing, smart people is very educational and so many perspectives on not even only programming, programming philosophy and lots of opinions to ping off of. And, yeah.

00:14:54 [CH]

What? What would you say you're and you also presented. I should mention. Probably we're gonna interview some of the folks that have presented What would you say your -- and you also presented, I should mention. Probably we're going to interview some of the folks that have presented, some that haven't. You are one of the few that did present. How did your presentation go?

00:15:04 [BE]

I loved it. So, I was very worried that I was going to, like, forget a lot of stuff. And I guess I forgot some stuff. But it went really smoothly, way smoother than I expected. And I felt like there were plenty of questions, which I loved. And I was actually able to answer most of them, I think. And I was -- when it was done, I was really proud of myself with how it went. Yeah.

00:15:28 [CH]

Yeah, I thought it was a very interactive presentation. You showed a lot of demos. The Dyalog Duck was probably my favorite. Maybe not the coolest because you showed some pretty cool examples. There were some games. I think we had both Aaron and Kamila try to solve that one game. Yeah. Maybe we'll link it if folks want to go check it out. What was it? Was it called ARK?

00:15:47 [BE]

It was called ARK. It was made by Rampoina, which is a guy's username, in the APL farm.

00:15:54 [CH]

And it was level 4. So, anyways, we'll link some stuff if you want to go check it out. But it was very interactive. Definitely loved the Dyalog Duck. If you had to choose maybe one highlight or one interesting thing that happened that you want to share with folks, what do you think it would be?

00:16:06 [BE]

What highlight? I mean, so me and Rory have been talking till 5 a.m. for a few days. Honestly, that's probably the highlight because it was such a lovely conversation. Although, if we talk about outside of that, I think the presentation itself that I did, I mean, I'm so proud of it. And it was really fun. I think that was the highlight. And I like being the center of attention sometimes.

00:16:37 [CH]

That is fantastic. I mean, people say all the time at conferences, the hallway track is the best part. It's getting to talk to folks. I feel like this conference almost is entirely the hallway track, and it's sprinkled a couple of presentations. And if you have forgotten from Episode 68 when we had Brian on, Brian is quite a bit younger than the rest of us, which is why he manages to still stay lucid and wake up in the morning after staying up till 5. I have not been up till 5, folks. I've been going to bed at a reasonable hour. Hopefully, we'll get to see you at one of these in the future. I think Stephen said that he's hoping to schedule one of these, if not next year, in a future year. So we hope to see you there.

00:17:15 [BE]

Perfect. Thanks so much.

00:17:23 [CH]

All right, we're here with our second attendee of Iverson College 2024. From episode 74, a returning guest to a raycast. Camilla Shevchuk, All right, we're here with our second attendee of Iverson College 2024. From Episode 74, a returning guest to Arraycast, Kamil Szewczyk. Welcome back to the podcast. Tell us, how has your Iverson College experience been? What are the highlights? What have you gotten from it? You also presented, just like our last interviewee, Brian. Yeah, tell us about your experience.

00:17:47 [Kamila Szewczyk]

I really liked it. It was a great meeting. What I really wanted to get out of it is just build some motivation to learn more about basics of other array programming languages. The only array programming language they know is actually APL. But I learned a lot about the fundamental tenets of other array programming languages that I was not really aware of. I didn't have the motivation to research them before. But now I had the chance to get a closer encounter with all of those. It was really nice seeing other people's ideas about developing array languages. It's nice to see the direction that people are trying to steer array languages to. That was actually my first time hosting a workshop.

00:18:38 [CH]

Oh, really? Yes. I just did mention that some of the folks here presented, not everyone, but a handful of them. You were one of them. How did that go?

00:18:45 [KS]

Well, in retrospect, there's a lot of things that could be improved. But I think my first workshop went really well. I'm really glad with how it turned out. I tackled all the interesting problems they had on my bullet list. I started preparing for it only, I think, one or two days before Iverson College.

00:19:06 [CH]

I did hear that you were deleting slides, adding slides, deleting slides all the 24 hours leading up to it.I could hear that you were deleting slides, adding slides, deleting slides, all the 24 hours leading up to it.

00:19:12 [KS]

Yes. At first, I didn't want to present anything. I was planning to just come here and hang out to see what other people are up to. But actually, I read a very interesting paper just before I came to Iverson College. It really inspired me to host a small workshop. It was very important for me in that I have only ever given actual presentations before. And I have never had this sort of connection with my recipients. I could actually talk in a free-form way with them and answer concrete questions and have them follow me. It was very nice.

00:19:54 [CH]

Did you prefer that to the regular, you know, sort of just up there talking presentation format?

**00:20:00**

Yes, very strongly.

00:20:06 [CH]

Awesome. And just before we go, I know that you are going to be, hopefully, this episode will go out before October. My guess is that it will. And if it does, you're going to be at a conference in October. Do you want to tell people the conference and the talk that you'll be giving in case they are interested in attending?

00:20:25 [KS]

Yes. So my talk is very cryptically titled "Concrete Functional Programming". And what I really want to get out of this talk is appeal to programmers who want to apply functional programming to their jobs. So I will not be discussing array languages that much. I will not be writing Haskell or OCaml. I just really want to demonstrate some applications of functional concepts in day-to-day use in traditional programming languages. So, for instance, one of the concepts that I really want to touch on are persistent data structures and efficient mutability control in programming languages. So my plan for a demo, which is not finished yet, I want to work on it, will be a text prediction engine, more like Google Search or T9, but a bit more advanced, using all those functional principles.

00:21:19 [CH]

Awesome. And that's going to be at Lambda World, right? Yes. October, I think, 2nd to 4th. And it'll be in Cadiz, Spain. So if you are in the EU area or if you want to hop on a flight and you're anywhere in the world, you can check that conference out. We'll have links in the show notes. Awesome. Thank you so much.

00:21:37 [KS]

Thank you.

00:21:42 [CH]

All right. We're here with our third attendee of Iverson College, Alex Unterrainer. Hopefully, I've gotten the pronunciation not too far off. And this is our first Iverson College attendee that hasn't previously been a guest on ArrayCast. So maybe introduce yourself briefly, tell us where you're based out of, and what array languages and technologies you're working with.

00:22:02 [Alex Unterrainer]

Yeah, sure. Thank you very much for having me. I'm Alex. I'm a Kdb/q developer. I'm based in London. I'm currently a consultant for Data Intellect, and I run my own blog, devconq.tech. [03] I write everything about KDBQ, trying to teach people who are not coming from a KDB background how to get into KDB and how to pick it up.

00:22:24 [CH]

Awesome. And actually, now that I think about it, technically, we heard your voice and you introduced yourself, I believe it was the ArrayCast episode 87. I could be wrong about that, plus or minus one. So technically, you are a returning guest now that I think about it. It was recorded and hasn't been released as of this recording. But by the time a listener is listening to it, this will be your second appearance on the podcast.

00:22:46 [AU]

Yes, and hopefully not the last one.

00:22:48 [CH]

Hopefully. Well, yes, we'll have to have you as a standalone. We definitely don't have enough q and Kdb+ representation in the form of guests on our podcast. A lot of these folks that work in the finance, hedge fund industry, they don't want to talk to-- it's not just us. It's-- Shy. They're just-- well, I'm not sure if they're shy. They're busy making money. So tell us about your Iverson College experience over the last four days. Highlights, what you've gotten out of it, and just overall how it's been.

00:23:12 [AU]

Yeah. It has been a very great experience. I think I've never been in a room with so many smart people at the same time. And what I found was-- or is great is you can see the complete history. It feels like the circle is closing. Kdb is based on k, which then was based on A+. And A+ was heavily influenced by APLs. And we have pretty much representatives from APL, Kdb, and k, obviously. And we also have J representatives and BQN. So it's very interesting to see the concepts that all those array languages have in common, but also the differences between them and when you would use one over the other.

00:24:01 [CH]

And you also gave, as well as our last two individuals we interviewed, a presentation. Tell us how it went and any highlights from it.

00:24:09 [AU]

Yeah, I gave a small, short presentation about Kdb architecture, how you would use Kdb in the real world. I think it went pretty good. A lot of people were interested in actually how you would build a system in Kdb. So I gave a brief overview of the plain, thick, vanilla setup. So I think it went pretty well, and a lot of people could take something away from it. And maybe they are inspired to build something similar in another array programming language. Maybe not, but I think it was a good experience for me to speak in front of these kind of people.

00:24:42 [CH]

If there's folks out there that are interested in this, because it is a topic that's come up several times, not just with respect to q, but array languages in general, this kind of building applications, architecting in these languages. Do they have to just come to Data Intellect and hire the consultants? Or are there resources, either in the form of your blog out there, that we can point people at?

00:25:02 [AU]

You can definitely point people in the direction of my blog. That's why I started it. KX also have a good documentation, and they recently rebranded their KX Academy. Data Intellect, they run boot camps and training as well. It's not free, though, so people would have to invest, but it's definitely worth it, because I think the Data Intellect boot camp is pretty much the best one out there. In the past, it was a little bit harder to find documentation or tutorials, but I see it's definitely picking up and people try to promote the language more and getting people to use it.

00:25:34 [CH]

Awesome. We will make sure that we link all of those resources you just mentioned in the show notes. Thank you so much, and hopefully we'll see you at a future one of these.

00:25:39 [AU]

Absolutely. Thank you very much.

00:25:48 [CH]

All right. We are here with our fourth attendee of Iverson College 2024, Devon McCormick, who I believe out of all of the four folks we've interviewed, or three that we've interviewed so far, you're the first one, excluding our warden, Stephen, that is a returning attendee to Iverson College. I believe you are the organizer of the New York J User Group. Maybe briefly introduce yourself and tell us about your experience at Iverson College and how it's compared to ones in the past that you've attended.

00:26:16 [Devon McCormick]

I'm Devon McCormick. I started programming in APL when I was 13 years old. I did it for about 20 years, and then I switched over to J. I'm hoping maybe one day to do q. I think this is the fourth one I've been to. They're terrific events. It sort of parallels, I think, the reason I formed NYC JUG is because we're such tiny communities that I formed NYC, the New York City J User Group, because it's such a dense urban area. I figured I could actually get a few people together. And, of course, Zoom sort of obviated my reasons for forming it, but nonetheless, it was a good experience. I think this is much the same thing. Each array language itself is such a tiny community, and we have so much in common that it makes a lot of sense to bring us all together. So it's a terrific experience. You get a lot of intellectual stimulation, get to visit these wonderful places, and I can't say enough good things about it.

00:27:21 [CH]

You were, I think we're four for four now on interviewees having been presenters as well. Probably that's not a coincidence. The folks that have presented are also comfortable being behind a mic. Tell us how your presentation, I believe it was last night, if I recall correctly. How did that go?

00:27:37 [DM]

It went great. I mean, even, initially, I was down by one vote, and I wasn't going to be presenting, but because of a change in the schedule, I got to present. But even if I hadn't presented, doing the work on my presentation to revise it and hone it and slim it down from when I originally gave it was worth the effort in its own. But it's always good to have an audience as well.

00:28:00 [CH]

And that was given at the HOPE Conference. Was that recorded? Are people able to watch it or no?

00:28:06 [DM]

It was recorded, but I haven't seen any indication of the videos being available anywhere.

00:28:12 [CH]

OK.

00:28:13 [CH]

Okay. Usually there's some lag time. It can be anywhere from a month to half a year in my experience.

00:28:17 [DM]

Yeah. As discombobulated as I was at that conference, I'd be just as happy if it never saw the light of day. Because I was experimenting with a new presentation method. I was using Google Docs because I saw other people using it, and then someone pointed me to Google Slides, which is more the appropriate tool.

00:28:36 [CH]

Okay. And I know that I attended, I think for several weeks, if not months in a row, during the pandemic, you were holding the user group, even though it was based in New York, it was online. And I'm in Toronto, so that was same time zone. Have they gone back to in person? So to wrap this up, I'm thinking, is it online and folks anywhere can attend? Or is it just if you're in New York, which I mean, as you mentioned, there are millions of folks in New York. I'm not sure how many listeners we have there, but who can attend these J-user group meetings if they're interested?

00:29:04 [DM]

Well, it's the second Tuesday of the month at 630 Eastern Time. And we generally get attendees from the Eastern Seaboard, but we get also people from the West Coast of North America and Australians, because it happens to work out for them time zone wise. I tried to move it to an earlier time period for a while there to get more Europeans, but no one showed up. So I moved it back to 6:30 because that was convenient for me.

00:29:32 [CH]

Awesome. Well, we will make sure to link to not just the user group, but I think there's also in the J-software website, there's a lot of links to past meetings. And there's pretty meticulous, not necessarily meeting minutes, but things that are talked about or linked to and you can see past presentations and slide decks. So we'll make sure we link all that stuff if people are interested. And hopefully we'll get to see you at one of these in the future if we end up having one of these again.

00:29:58 [DM]

Well, I sure hope so. The users group, we're ending our 20th year this year.

00:30:03 [CH]

Ohh wow.

00:30:03 [DM]

nd the work that Bob has been doing on the Wiki has inspired me to go back and post up some of the meetings I didn't post in the first place. So right now it looks like some years we only had three or four meetings. We actually probably had about 10. Eventually I'll get around to putting the material up for all of those.

00:30:20 [CH]

Awesome. So there's a ton of content and more to come. Thanks so much. And we will see you for the last day of the conference later today, I guess.

00:30:28 [DM]

Terrific. Thank you.

00:30:29 [CH]

Thanks, Devon.

00:30:35 [CH]

All right, we're back once again with our fifth, I believe if I'm counting correctly, interviewee and attendee at Iverson College 2024. You may or may not be familiar with him, folks. His name is Adám Brudzewsky, typically a panelist, but not today. He's an interviewee. I mean, I'd ask you to introduce yourself, but everybody already knows who you are on this podcast. So maybe let's hop straight into it. How has Iverson College been? And you have, similar to Devon, been to several of these before. So you can contrast and compare if you want. What are the highlights of this one? How does it compare to years past? Over to you.

00:31:10 [Adám Brudzewsky]

Years past over to you, I have been only to 1, I think.

I have been only to one, I think, before. Really? And it was quite different, I would say. I think actually I like the old one better, to be completely honest.

00:31:21 [CH]

Okay. This was the one in the barn, correct?

00:31:23 [AB]

That's the one in the barn. It was a different type of crowd and a different type of setting. I felt that the one in the barn, maybe that's just a romantic memory of things in the past, but it's been a few years, but I found it much more intimate. It was far away from everything, basically in the middle of nowhere. And there was nothing to go out and see, really, the way that it is in Cambridge. If I remember right, even like internet and phone connections were not very good. So we were basically there on a...

00:31:58 [CH]

Well, that sounds terrible, no?

00:32:00 [AB]

That sounds terrible. No, that changes everything, because that forced us to... Either we were working on something that we have with us like that, or people would just be together. And there weren't as many distractions like that. It wasn't that everybody is doing something else. We had just had this one big barn. And one end of the barn, there were couches and cushions, and people were hanging out and discussing things, taking their time. There was much less of a schedule. During that week, there was a q masterclass going on. So there were some extra students came in and left. But that was really the only thing. There weren't really presentations. People talked about things in smaller groups around. And this time, it was much more of a conference setting, but it more felt like a top meeting type setting. We came in the room, I was a bit surprised, at this U-shaped table, all set up with little pads and upside down glasses.

00:33:01 [CH]

Adám now has the floor. Please yield your time after two minutes now.

00:33:05 [AB]

And at the front, there was the projector screen. And we had a lot of talks, presentations, even some workshops arranged this time. The setting was less conducive to small groups gathering around. There wasn't space for that. It doesn't mean it didn't happen. I'm not going to say everything was bad this time. Not at all. It was good. It was just very different. And the people that participated in the previous one were mostly implementers. Some users, but mostly implementers. And they were discussing those kind of things. High level design of things. This time, it was a very mixed crowd. There were veteran implementers, though not from Dyalog. [04] So not for APL. Only APL users, but inside Dyalog, users creating special tools and so on. With some knowledge of the interpreter. And there were some young people. Not that that's a bad thing, but it makes a very different dynamic. And they're excited about upcoming projects. Not decades long running projects that people are running.

00:34:25 [CH]

Greenfield stuff.

00:34:26 [AB]

Yeah. And that's not necessarily a bad thing. It's just very different. It was very information packed this time. So I learned a lot of things about a lot of things in these various languages. In k, q, Uiua, J. And in that sense, I guess I got more information out. If I think back to the previous Iverson College I was at, then I can't really say anything that I learned from that. But it was more like a serum injection of excitement about bringing this whole thing forward. Here, it was more conference type things. I'm learning things. And a lot of nice hanging out and talking about all kinds of things. And comparing languages. So it was more because there were all these things presented, then it sparked all kinds of discussions about things. That's a great thing. So maybe I would have wanted both. And both the time for this more intimate setting that's just quiet, that's just away from everything. But also some information being served and some discussions. I think many of the presentations became more interactive. People were discussing, asking questions in the middle. And I think that's good. I'd rather, me personally at least, I'd rather that things that could just be a YouTube video, should just be a YouTube video. The things that you can't do on a YouTube video, and the chat next to a YouTube video is not good enough. People discussing things, people walking up, pointing at things. And immediately making changes to things or experimenting with things based on what the audience says. That I think is valuable, definitely.

00:36:20 [CH]

So you mentioned that the previous edition or installation that was at the Barn was more intimate. Do you think it was the location or the setting, the location, or the mix of participants that led to the-- it sounds like there was different types of conversations and more sort of break-off groups. What is it that you think that contributed? If you're saying both have their value and in a future edition, Stephen's looking to replicate that conference. What is it that is going to lead to that kind of thing? In your opinion, what enables that?

00:36:53 [AB]

TI think it's both. I think it's the choice of participants. Not that I would send people away from here, but I think it makes a difference. And who the participants are, what their roles are in the respective groups and companies that they come from. I think the setting makes a big difference, how it is. Even the food makes a difference. So here, we had the college, we're being served breakfast in the big hall with other people that have nothing to do with what we do. We have meals and it's kind of restaurant setting type thing. Again, it's not very personal. In the barn, we had deliveries from the supermarket and Miki and the friends were cooking for us specifically. Being there, part of it. Everything was bespoke for what we were doing. Everything just changes the feeling of it. This was much more conference type, standard conference type thing.

00:37:54 [CH]

Well, it's glad to hear that you liked both and it's a little exciting that potentially there's different styles of these that can happen. I mean, Stephen, our warden, mentioned that at one point, the goal was to get a flat in Venice and do an Iverson College there. Will that happen? I don't know, but if it doesn't, I imagine that's going to have also quite a different vibe than being at University of Cambridge, Trinity Hall. Any final things, parting words? Highlights that happened this week? Things you want to mention?

00:38:24 [AB]

I would say the message to take home from this is that these array languages, these Iversonian languages are very much alive. They're not going away. We're coming for you. And we need more of this. There were things brought up that came as a surprise to veteran implementers that didn't need to be a surprise at this point. Had there been more such cross communication and pollination, we can do more. We're not competitors. We're in this together. And I think we need much more. It's been a long time since the last Iverson College and it's been too long. I think we need this going forward. We should do this definitely more often than half a decade in between.

00:39:13 [CH]

Well, I mean, admittedly, it's not like there wasn't something preventing a few of those years from it happening. But hopefully, 2025, 2026, it'll be sooner than it was from the last one. And we hope to maybe see each other there again. Yeah, it's been awesome. Thanks so much, Adám.

00:39:30 [AB]

Thank you.

00:39:32 [CH]

We'll see you back on Zoom. [Laughter]

00:39:41 [CH]

All right. We are back with another attendee of Iverson College. I believe a first time attendee and like I said before with Alex, a first time guest, but not really because you were also on We Heard Your Voice on episode, I believe it was '87 of Arraycast when we recorded a couple days ago. We're here with Brandon Wilson. Maybe introduce yourself. Tell us where you're based out of, what Array languages you're working with, and then we can hop into your thoughts about Iverson College and your experience this week.

00:40:09 [Brandon Wilson]

Excellent. Thank you for having me here, Connor. My name is Brandon Wilson [05] and I'm a newly minted APL consultant. I started Array programming, dabbling in J about 2020-ish and just kind of did hobby, you know, advent of code kind of things for several years. Decided to get more serious about the language. And at that point I moved over from J over into APL and ended up getting convincing Aaron to mentor me and get me past the beginner level into writing like actually real production APL code. And I'm on that journey in that interim from beginner to intermediate.

00:40:53 [CH]

And so I guess before we get to your thoughts on Iverson College, and I think we're just going to have to bring you on for a full episode, but give us a taste of what it's like to be mentored by the infamous Aaron Hsu.

00:41:05 [BW]

I mean, you're talking to someone who has quite a bit of overlap personality wise. I'm not as boisterous as Aaron by a long shot, but our philosophies overlap quite a bit. And that's what drew me in to initially contacting Aaron. And a lot of the things he's saying seem ideally what I think we want to be doing with Array Languages. It's having these sort of Iversonian ideals of programming languages. And he's saying, "Hey, it's possible. Here's this thing." And it's, it's, there's a properties that I had been trying to instill in the products that I was producing for my clients at the time and the people that I was mentoring, you know, my junior engineers. But then Aaron comes along and say, "Hey, look, you can do this directly." And so I just, I wanted to see what, you know, look in the dragon's mouth and see what it is about. And it was great. I mean, like, so we, when I first contacted him, he was on board to do a mentorship and was like, "Hey, what, how do you want to do this?" He just let me sort of pick the format. And I said, I wanted to write in a YAML parser, which is like, I didn't know it at the time, but that's like right down his alley. So he was super excited about it. And the whole process was basically me writing some code, and then we would meet like once a week. And he would do his Aaron thing about talking about, you know, abstract kind of high level principle ideals. And it was my job to digest that and try and make that into something concrete. And it was, it was excruciating for at the beginning, absolutely excruciating. I would like not know, I would try to get what he was saying, and then I'd write some code and he'd look at it and be like, "Eh, let me try again." And then we just did that iteration for like a year, year and a half. And at the end, it came to something that looks like Code D funds. So he brainwashed me successfully.

00:42:55 [CH]

A disciple, you know, training at the feet of, that's awesome. So, I mean, tell us about your Iverson College experience. This is your first time attending an Iverson College, correct?

00:43:03 [BW]

Yes, it's my first time. I am honored to be here. And, you know, from the outside, Iverson College looks like this like insular thing of elites that come together. But I understand that this year has a lot more sort of new newcomers. And so it's been great to be part of that sort of new wave and coming in and also bumping up against non-APLers, right? You know, seeing that k is a real language that gets used and not this, you know, esoteric mystique thing that happens in finance and no one sees. Yeah, and then seeing all the kinds of characters. We have people, you know, like Ray Cannon, who's been there from the beginning of the beginning since the Big Bang, essentially. And then we have, you know, Brian here, who's, he's still in high school, I believe. I think he's in university now.

00:43:51 [CH]

He's in university. I should have interviewed him when he was either transitioning. So, yes, I was shocked when we didn't actually know how old Brian was when we had him on the podcast. And then I think I awkwardly asked, I was like, we can cut this question out if you want. But do you mind me asking how old you are? Because I'm guessing that like you're a full decade younger than I thought you would be. And it was the case. His age, I believe, starts with a one. And I don't even want to know what that works out to the year that he was born in, because it's just going to make us feel old.

00:44:19 [BW]

Yeah, exactly. It's sort of a pleasure to see that, you know, interact with people with a wide birth of experience and different perspectives on array programming. And to see how that affects how their ideas on what array programming is. Like Morten has his own particular, very austere kind of, or practical, austere practicality that he has, how he thinks about things. Aaron is often abstract, bland. And then you have like Rory here, who's very interested in interacting through like, from an academic perspective of helping him in his studies. And that's as using it basically as a tool of thought, right, for his, in his particular way. And he's absolutely mind-blowingly fast at it. And it's great to see all these different textures of using APL that break me out of my little bubble, Aaron bubble, right, that I've been in for a while. And like thinking about parsing and writing APL in this particular way. And then I've, you know, in my work now I see, apart from Co-dfns, like that kind of style of things, I also see just this old bag of trad funds style in APL. So it's really interesting to see, like the K-talks that we had were also fascinating. And since, especially since Adám interacts and is talking about the future of the language and everything. So yeah, it's been, it's been great. Iverson College is, I mean, meeting you, Conor, right.

00:45:44 [CH]

And seeing, watching me go toe to toe with Aaron and failing. Yeah, yeah.

00:45:46 [BW]

You hold your own, you hold your own pretty, pretty well.

00:45:52 [CH]

I might not have lost, but there's definitely no winning. So if there's, you know, if there's someone listening, you know, as a first time attendee, you know, what would you tell people they can expect to get out of this if they're thinking about attending one of these in the future?

00:46:04 [BW]

Yeah, that's a great question. More than anything, the networking and the connections with people. I mean, honestly, out of this particular conference, it would be hard for me to say what technical things that I learned. I mean, I can point to a few things, few interesting discussions we've had. But more than that, it's the, it's broadened my, the feeling, broadened my world about of array programming. I feel like, you know, next time if I meet any of these people around, since it's a week long thing, we've had the chance to sort of bond. Right. And so I feel like there's a, there's potentiality for future, you know, the relationships continuing on in the future. And I look forward to that. And for me, that's the most valuable and interesting part of Iverson College.

00:46:47 [CH]

PYeah, I couldn't agree more. And hopefully, you know, we'll bump into each other at a future. I think there's going to be future additions. We've talked to the warden, Stephen, and he said he would love to do these again. So hopefully we'll see you there in the future.

00:46:59 [BW]

I hope to be back.

00:46:59 [CH]

Awesome. Thanks so much, Brandon.

00:47:01 [BW]

Thank you, Conor.

00:47:05 [CH]

All right. I think this is our seventh interview with another attendee from Iverson College, Sasha Lopoukhine. Hopefully my pronunciation isn't too far off of that. A local, a PhD student at the University of Cambridge was kind enough to give me and a few others the other day a tour of, I believe it was Christ's College, correct? That's where you're staying. And it was absolutely gorgeous. You pointed out where Darwin used to live. That's not something you see every day. I think you said it was now the chair of computer science or their dorm where they stay. But yes, introduce yourself. I believe this is your first attending of an Iverson College. Tell us a little bit more about yourself and then we'll hop into your experience so far this week.

00:47:49 [Sasha Lopoukhine]

Yeah. So I'm a PhD student here. I'm researching mostly compilers for linear algebra, machine learning for special accelerators. And I think I'm probably the least experienced in array language programming here. I'm just really curious. I'm especially interested in the semantics of array languages and how they can be exploited for optimizing compilers.

00:48:21 [CH]

So what was, were there things that discussions that you had this week that, you know, changed how you might be going about your research or the kinds of things you're going to be looking into?

00:48:29 [SL]

Definitely. So Aaron is here and he's done some really interesting work using parallel computation for parsing itself. And that's very interesting. There's a lot of really interesting ways that array languages manipulate the structure of computation at the syntactic level. And when I think about how to actually compile it, it's a very interesting approach. And so I'm really I'm still playing with it, but it's really interesting to see how when you go from a sort of interpreted approach to a compiled approach, how these array languages behave. I think they're kind of unique with the combinators at the language level. [06] You get some really funky things happening. And so I'm looking forward to exploring that.

00:49:21 [CH]

It must have been pretty exciting to see Aaron's name on the attendee list, because to be honest, there isn't a ton of compiler research in the interpreted array language space. I know that there's a couple like Bob Bernecky has an Apex APL compiler, but in general, compilers are far and few between when it comes to these interpreted languages. So awesome that Aaron was here. I'm sure you talked to him a bunch. So what were the other highlights that you experienced while here?

00:49:48 [SL]

Well, it's really great that so many of the language implementers are here. I had some really interesting discussions with lots of the implementers of the different array languages. I've mostly been playing with Uiua and it's really great that Kai could come. And I've been asking him lots of questions about how it's actually implemented, the semantics and his plans for the language. It's really special to have all these people here to actually ask questions.

00:50:13 [CH]

Can we expect to see you potentially at a future one of these? I think we've talked to Stephen and he's hoping to do one of these. And if you're talking to a potential listener that's thinking about coming to one of these, what would you say they can expect to get out of this?

00:50:27 [SL]

Yeah, I'd definitely like to come again, especially if I do more research. It'd be nice to kind of present a bit more my take on the things because I'm just sort of starting out. I'd say even as someone without that much experience, it's been really useful. I've been getting most of my information through your podcasts. So that's kind of the way that I've been preparing for it.

00:50:51 [CH]

Are you prepared to hear your own voice or you're going to skip this episode?

00:50:56 [SL]

I'm curious. Yeah, it's definitely a very welcoming sort of group. And well, one of the things that I like about all the people I've met today is that there's a bit of a bias towards people who are willing to try weird things. It's not the most popular way to program. And so it's nice to have people who are very open to these ideas. It takes a little bit of a special mindset. And that's just like a really refreshing thing to see people who are really interested and open to different ideas. So it's been both like a lot of learning for me and really interesting discussions with everyone here.

00:51:39 [CH]

That's awesome to hear. And yeah, definitely I don't think there's a single person here that wouldn't identify as extremely curious. And, you know, they see something, they don't understand it, they want to go understand it versus you don't always get that vibe at different conferences. You know, people have their kind of bubble and they want to if it looks different, they're not going to go try it. So I completely agree with that statement. So, yeah, hopefully we'll see you at a future edition and good luck with your PhD research. I'll be looking for a dissertation. And I think you said you're about halfway through, so it's still a couple of years away. But I'll be looking for it when it comes out. And yeah, good luck with your studies. And we hope to see you at a future one of these.

00:52:13 [SL]

Thank you. Yeah. Hopefully I'll make it back.

00:52:22 [CH]

All right, we're back. Honestly, I'm losing track. I think you are interviewee number eight and attendee of Iverson College 2024. We're here with maybe the star of the week, Kai Schmidt, previous guest. I believe the numbers were episode 63 and 77. Links will be in the show notes. Also, I didn't guess. I looked at the show notes of my other podcasts because we linked to those when I was talking with Aaron. We're here. Kai Schmidt, creator of the Uiua language. Tell us about your experience at Iverson College and highlights, you know, things you got out of it. And also you gave, I think it was not, was it the first presentation of the week? It might have been.

00:52:59 [Kai Schmidt]

I think the second.

00:52:59 [CH]

The second. It was definitely on Monday, the first day of the week. So how did it all go?

00:53:04 [KS]

It's been really amazing being here. I've learned a ton about the other array languages, which is just directly from the people who are directly involved with them, which is awesome. I've talked to Adám a lot. I've spoken to the k guys and all the presentations that we've been people have been giving are have just been super awesome. And then, of course, after I gave the talk about Uiua, it's been really encouraging getting feedback directly from the array community. So that's been that's been awesome as well.

00:53:38 [CH]

I've got very excited about Uiua, you know, right before or was it right after we had you on the podcast? And yeah, there's a ton of different ideas that we was exploring that haven't been explored in the other languages. Not that, you know, k, APLJ are all the same, but I think Uiua sets itself apart. And that's been awesome to see people interacting like I'm sure you've had great conversations with folks about this, these kinds of, you know, language design decisions.

00:54:04 [KS]

Yeah, for sure. I mean, especially Adám, since he's also a language designer, because he has so many good ideas about what the way of say primitive should be and what is what is correct and what's useful for stuff.

00:54:16 [CH]

So are there going to be, you know, ideas or things that are implemented in Uiua in the next couple of months directly inspired?

00:54:22 [KS]

Likely, yeah.

00:54:32 [CH]

Awesome. Well, we will look out for those. If someone's listening and thinking about attending in the future, as you know, this was a kind of first time thing. What would you tell people they can expect to get out of this? Maybe not necessarily. I'm sure not everyone has their own language, but, you know, things in general that you're going to take away from attending an Iverson College.

00:54:42 [KS]

I mean, other than, of course, like people that are really smart, giving one on one conversations, but also like great talks and stuff. There's a I think there's a general sense of like camaraderie that we share as like members of the array community. And I haven't felt that as much as I have felt it here. So that's the best part for me.

00:55:06 [CH]

Awesome. Well, hopefully if there is an Iverson College 2025 or 2026 in a different location, we'll see you there.

00:55:12 [KS]

I'd be delighted.

00:55:13 [CH]

Awesome. Thanks, Kai.

00:55:18 [CH]

All right. We are back with I'm losing track. I think it's interview number nine with another Iverson College 2024 attendee, Rory Kemp, math's aficionado. And I from what I hear from Aaron, Advent of Code, you know, wizard constantly beating Aaron and upsetting him at the same time. How has first of all, introduce yourself a little bit. And then after that, we'll hop into how Iverson College has been.

00:55:46 [Rory Kemp]

All right. Well, so my name is Rory. I'm currently I've just finished my second year doing maths and computer science for university. And for the last four or so years, I discovered the array languages and APL. And, well, my two main array languages of choice at the moment are APL and k. Although actually, after some of the things I've learned in Iverson College, that may change in the future. But who knows? So I've been interested in these languages and the paradigm for a couple of years now. And I don't have much professional experience with them at the moment, but hopefully we'll do some of that in the future and just see where it goes.

00:56:34 [CH]

So the first question I have to ask is being a student at Oxford is how hard has it been for you having to be here at the University of Cambridge, your arch nemesis university?

00:56:45 [RK]

You know, I was slightly worried that the moment I crossed the boundary into Cambridge, I might spontaneously combustors something along those lines. But I mean, I seem relatively unscathed at the moment. So that's a good thing. You never know. Maybe the moment I go back into Oxford, everyone will have realized that I'm now a traitor and I'll be chased out of the streets and forced to leave and never come back.

00:57:13 [CH]

So how was this was your first Iverson College? How was the week? What were the highlights? What did you take away from this conference?

00:57:19 [RK]

It's been an incredible couple of days. I mean, it's still not finished, but it's been more than I could have ever hoped for in terms of number of people from all different backgrounds and who is really interesting and have so much to talk about and the variety of subjects and things like that. Even things that I thought, OK, I might not necessarily be interested in that have sometimes turned out to be the most interesting things of the week. I've talked to so many people. I've met a lot of people I've talked to or know about through online messages and forums and things like that. And to actually meet them in the flesh and talk to these people, I mean, I discovered APL and like a lot of people do when they discover APL, they go into the APL Orchard [07] and then I talked to Adám. So, you know, I've known him online for four years now and it's my first time meeting him in person. So with some of these people, it feels like I've kind of known them all my life almost. But I mean, it's so good to have this in this shared interest because it means that you can meet someone and talk to them and there's this instant connection.

00:58:32 [CH]

If there's someone that's listening, that's thinking, you know, I might want to attend one of these in the future. What would you say, you know, they can expect to get out, even if they maybe haven't been diving into array languages for four years like yourself? And, you know, what would you say to someone that might be thinking about attending in the future?

00:58:49 [RK]

I mean, I would say if anyone's ever asked to attend or thinks about attending in the future, then they should absolutely do it because it will be an incredible experience. No matter your background or professional experience or, you know, level or anything, anything like that. I mean, it's so welcoming. I don't think I would like to hope that everyone here has felt like they're an equal part and everyone has something to add. And, you know, I really feel like everyone here has had something to add and something that, you know, a couple of conversations I've had in particular, like, have really probably changed the course of my future life. You know, so it's been a big, big deal. I mean, when I was actually first got a message from Stephen saying we're organizing this thing and we'd like you to come. My instinct was because I've read about it before and, you know, the big names that have been here before, you know, the titans of the array world. And you think, hang on a minute, I'm going to sit there and not know anything that's going on. And, you know, I've never really worked professionally. And, you know, will these people even want this like relatively young guy that's not been doing APL since he was two. But I mean, I'm really glad I went because I mean, it would have been a terrible decision to say, no, I'm not going to do it. And then, you know, I'd have missed that one so much.

01:00:25 [CH]

That's awesome to hear. Yeah. And hopefully we've been talking with Stephen, the warden of Iverson College, and he said that he's hoping to do one of these in the future. So hopefully we'll be able to see you and some of the same folks and maybe some different folks at a future edition. Awesome. Thanks so much, Rory.

01:00:37 [RK]

No problem. Thanks.

01:00:48 [CH]

All right. I think we are here with Iverson College attendee number 10. I could be wrong at this point. I kind of have lost track. We're here with Aaron Shue. We've gone from the pub on Wednesday to now. I believe it's the Chatwood room. I could have that wrong. And we're back. We're back recording on another podcast. Technically, you were on episode 87 of Arraycast and then you were on episode 196 that just got dropped today of ADSP. You'll be on 197 of ADSP as well. [08] And now I don't know what number this is going to be, but we just can't get enough of you, Aaron.

01:01:23 [AH]

I've not done this many podcasts ever.

01:01:27 [CH]

But Aaron, and I actually messed up on ADSP. I said you were on episode 18 of Arraycast. It was actually 19. 19.

01:01:34 [AH]

Okay.

01:01:37 [CH]

So I hope the listeners will forgive me. I'm sure there was a couple of them fact checking me.

01:01:38 [AH]

Aren't you a C++ programmer? Don't you, you know? It's an indexing. It's off by one. You're supposed to be good on these things.

01:01:44 [CH]

Ever since coding in array languages, I don't have to worry about that stuff anymore. Right?

01:01:49 [AH]

Right, right, right. Quad I-O.

01:01:52 [CH]

Anyways, I think you might be our last person that we are interviewing about Iverson College 2024. Tell us how it's been, the highlights, you know, how this is compared. Because I think you're on the short list of three or four people that we've talked to that have been to previous installations of Iverson College. So how is this one compared to the ones in the past?

01:02:11 [AH]

Very different. The audience in terms of the attendees, the breadth of experience and the ranges of different experiences has been much larger compared to previous years. So that has altered the way conversations have gone. There's a lot more exploration of possibilities and things like that, rather than deep diving into, you know, very specific issues that, you know, the whole group is very well familiar with. There's a lot more breadth of topics and discussions. Now, one Iverson College I was with, there were a couple of key high-energy party animals, and that changes the nightlife a little bit.

01:02:50 [CH]

Oh, I thought when you said animal, I actually thought you meant like dogs and cats. And I was like, people brought their pets.

01:02:52 [AH]

No, no, no. I mean your standard, you know. So we don't have any crazy party people here, so, you know, we haven't been doing, you know, a lot of, say, bar games and drinking games or, you know, college games or anything like that. So, you know, maybe we're missing a little bit of that crazy, but, you know, other than that, I think it's been pretty good. Lots of good energy.

01:03:19 [CH]

You have not actually given your presentation yet. It is going to be in T-minus, I think actually less than an hour.

01:03:26 [AH]

Yeah, T-minus 45.

01:03:27 [CH]

So, I mean, we've been asking folks how their presentations have gone. We can't do that for you. So maybe tell us what you expect. Are people going to be shocked? Will their jaws be on the ground, or will this just be, you know, routine, nothing exciting? You know, what can we expect?

01:03:44 [AH]

So I'm expecting all the k people to sit down and immediately know the answers to pretty much every one of the solutions and have coded them up in k while I was explaining the problem. Okay. I'm expecting for some of the other people to be shaking their heads and just saying, "I'm not even going to try this because why bother?" And then I'm expecting Rory Kemp to challenge me on why on earth it's even worth it to do it this way because clearly this is just way too much work. And, you know, there's clearly a better, more typical way that we should be doing all this stuff. So I'm sort of expecting a little bit of a trident.

01:04:18 [CH]

This is perfect. And now I have, like, an expectation of what I can expect, and we'll see how close reality is to--

01:04:23 [AH]

We'll see how it goes. The wild cards are the J people. You never know what they're going to bring to the table.

01:04:31 [CH]

That's true. You know, Bob, he's a firecracker. You know, we we don't know.

01:04:33 [AH]

I don't know what to expect.

01:04:36 [CH]

Monday, Tuesday, completely different answers, you know? So for the folks listening that are thinking about attending, you know, what would you tell them in terms of, you know, what you've gotten out of it and what they can expect in the future to get out of these kinds of conferences, even if there are slight differences between the editions?

01:04:51 [AH]

That's hard, actually, because each Iverson College is so unique, and it's driven entirely by the people. So when Stephen says the conference is what you make it, he really means the conference is what you make it. Every Iverson College that I've been to has been distinctly different than the one following it in terms of what people focus on, what the energy is, all of that. So in general, I would say you should expect a conference that you have a lot of influence on in terms of what you guys want to do, what you want to explore, a lot of impact, a lot of room to dive into just about anything you want, and a lot of accessibility to ideas and people that, you know, maybe you want to get in the room for a lot of higher bandwidth conversation. So, you know, but other than that, it really -- who knows what you'll get from year to year.

01:05:38 [CH]

Adám mentioned that in the previous one he went to when it was hosted at the Barn. Were you at that edition?

01:05:43 [AH]

At the Bar?

01:05:45 [CH]

The Barn.

01:05:43 [AH]

Oh, the Barn, yes. I was at one of the Barn parties.

01:05:53 [CH]

It's worrying that Aaron actually had to do a mental check of which one was at the Barn, like --

01:06:02 [AH]

You know, the Europeans.

01:06:03 [CH]

So you were at that one, and he said it had a totally different vibe. Do you have a preference? Because I think you've been to a couple, not just one. Yeah, yeah, yeah. Because he said it completely changes the types of conversations, the, you know, ability for people to break off and kind of have a couple different conversations going on. Right, right. What's your preference in -- or do you just like the variety in that it changes, you know, year to year?

01:06:26 [AH]

Yeah, I like there to be a combination of a lively nightlife and the equivalent of programmers on old-school stock markets. Like, I want the equivalent of lots and lots of opinionated discussions covering lots of topics with somebody giving some crazy talk and letting everybody explore the range of possibilities in the most high-bandwidth way possible. That's what I like.

01:06:54 [CH]

OK. Well you heard it.

Okay, well, you heard it here first, Stephen. That's the Iverson College that Aaron wants. Let's see what we can do for him. Supposedly, I heard from Stephen, the warden, that back in the day they wanted to do an Iverson College in Venice. And he says he doesn't know if that's going to happen. But, you know, if I mention it enough times over the next, you know, several episodes and in this episode, maybe it will come to fruition.

01:07:17 [AH]

I could go for it, yeah. As long as we have that high-energy talk, then when we're done, we go and chill with some nice food at the end.

01:07:25 [CH]

And we can replace punting. I actually don't know. What are they called? What do they call? Gondolonians?

01:07:28 [AH]

I don't know. I'm not sure that's what they're called. Gondolians? We replace –

01:07:30 [CH]

Did you go punting this week?

01:07:38 [AH]

This week, no, no.

01:07:39 [CH]

No, no. And I think it's – I don't actually know for the listener. I heard punting the first several times via email, via Slack. I thought it meant going for a walk, but it actually has a specific meaning in Cambridge. You hop on a little gondola-like thing and you punt around with a stick.

01:07:54 [AH]

Yeah, I thought it was going to involve rugby football, but –

01:07:56 [CH]

Yeah, I mean, well, it is a thing in sports. Yeah, so I was totally wrong. I imagine that Stephen didn't want to go play rugby.

01:07:58 [AH]

Yeah. Now, see, I would be up for that maybe. I could have fun with that.

01:07:58 [CH]

Hopefully, we'll get to see you at one of these in the future if we do have a future Iverson College.

01:08:13 [AH]

Yeah, hopefully all right. Thanks.

01:08:14 [CH]

Awesome.

01:08:20 [CH]

All right, thanks a bunch. All right, we took a short break, folks, and we are back. It was about 30 minutes for us. I think it was zero seconds for you. And we are now here with our 11th attendee of Iverson College 2024, the producer of Arraycast, Bob Therriault. And we're here again to talk about what we've been talking about for the past hour. This was your first Iverson College, if I'm not mistaken. How has the experience been for you?

01:08:49 [Bob Therriault]

Well, it's been phenomenal. The only thing I can equate it to was I did a J conference in 2014. And that's really been my first – that was the first time I interacted with a lot of people in the Array programming community, even though it was "only J." There was actually – Stephen was there. Stephen Taylor was there. It's funny. He came and had to give a talk about – well, he wasn't a J programmer, so he gave a talk about poetry, which shouldn't seem surprising to people who listen to the podcast. It was really good, but it was basically what it was. You go to a place, and if you're – I don't know. I've been to a lot of broadcasting conferences and that sort of stuff. I never really felt with those like I was being put back on my heels because people are so frighteningly intelligent. You'd be somewhat intimidated by things people had done or their knowledge in an area, but this is more like you talk to some people about anything, and you're going to have your worldview shift because they've probably thought about it, and if they haven't, they're going to think about it deeper than you probably have. And there's been so many personalities I've met that – well, I've never met before. You and I have met before. You were subjected to a walk around the lake, I think.

01:10:07 [CH]

Oh, "subjected" is not the word that I would use. I think a walk was an amazing way to first meet each other. I think it was partially because of COVID, but also, you know, whatever. We could sit down in a cafe, or we could go for a walk, and Nanaimo is a very beautiful place. We did a loop around a lake. I do not recall the name of it, but Westwood Lake. [09] Well, maybe we'll put a link in the description, or we'll just let you go and search it up yourself. Yeah, it was very coincidental that we happened – well, I happened to be in your neighborhood. And that's the thing is I don't actually keep track necessarily of where all of the panelists on the Arraycast live. In general, I know that you're on the west coast of Canada, on Vancouver Island, but it's not something you're actively thinking about when you're traveling.

01:10:50 [BT]

It's not something you're actively thinking about, but when I'm putting together the show, I have to think about time zones.

01:10:57 [CH]

That's true.

01:11:02 [BT]

So it is definitely something that I'm aware of where a person is. Sometimes I'm negotiating how late at night they're going to stay up, or how early in the morning I'm willing to get up, because that really comes down to what it is. But yeah, this experience has been – well, it's not unexpected because, as I said, I've been through this experience before, but this is with a wider group of people and a wider group of ages. And honestly, I think that makes a difference.

01:11:24 [CH]

Yeah, having talked with both Aaron and Adám and Devon, you definitely get a sense that – I think it was Aaron specifically that said every installation of Iverson College is completely different. And if both of us or either of us are to attend these in the future, I think it'll be interesting. I'm jealous that they have this experience, the juxtaposition of the different conferences, because I would love to be at a converted barn with chefs at the back cooking meals and getting deliveries and stuff. I'm sure the vibe was completely different, but it sounds like you still get amazing conversations at all the different unique styles. And I'm interested to see what Stephen does next time, if he does, in fact. It sounds like he's working towards organizing another one.

01:12:10 [BT]

One other thing I found really gratifying is there's been a number of people who come up to me and mention the podcast. And not that I don't expect it – I know there's lots of people who do listen to this – but whenever anybody comes up to you and actually mentions it, that's a different level. It's nice. And they say nice things, which is – if they come up to you and tell you how awful it is, that wouldn't be fun at all. But the number of people who have actually said – whether or not they said it, and they've all been nice – that it's influenced what they've done, or it's changed how they've looked at things. I can think of – I've been sitting through these interviews with you, listening while you're doing all the work. But Sasha talking about how his interaction with the array languages began with listening to the podcast and hearing different voices. And since then, he's obviously taken it much further and probably did more research. But it's a starting point, and that's kind of neat. Kai's the same way. He would listen to the Arraycast as he was developing Uiua. And now, it's the coolest thing to see all these guys that have been implementers of different languages look at what Uiua's doing and changing the way they think about their language. They're not saying they're going to do it, but they see what he's able to do with that language, and they go, huh?

01:13:35 [CH]

Any final thoughts or things you want to tell – we've been asking, if people are sitting on the fence, "Should I go? Should I not go?" or what people can expect to take away. What's your final word on Iverson College 2024 and potentially future Iverson Colleges?

01:13:49 [BT]

That's a really good question, because I think most people would go into something like this with a bit of apprehension, because you're dealing with really, really smart people. And not being a really, really smart person, I think that always feels a bit intimidating. You don't know whether – well, honestly, you don't know whether you're going to present anything that would be interesting to them. But you know what else is really cool? Not every community has this, but the Array Programming community, I think, is actually very welcoming. And so people I talk to – I don't think I'm the most interesting person to talk to, but they're interested, and they'll challenge me at my level, and I get to challenge – and I'll have a perspective they don't have. That's one of the things I think if you get into a conference like this where you're dealing with people who really know their stuff, just remember you have a background and a perspective they don't have. So it's not like you have to show that off to them, but they'll find things that you know that are interesting. And so you can go to these conferences, be a bit apprehensive, because I think most normal people would feel that way, but also don't be afraid, because if they're really smart, they will take what you have to offer, and you'll be part of that. And you'll be included, and I certainly feel that at this conference.

01:15:17 [CH]

I think that is the perfect way to end this episode of Arraycast. We hope to see you and potentially listeners of this podcast at a future one, and I think that leaves us with just one last thing, maybe two last things. There's an email. You can reach us at this email if you've got questions, thoughts.

01:15:37 [BT]

Contact@arraycast.com, and I know what you're doing.

01:15:39 [CH]

The problem is, folks, they want me to be on the camera and answer some questions, but I've got very little to add, and it's already 2.06, which means we're missing the first six minutes. Of Aaron's talk and that's like missing half of someone else's talk.

01:15:58 [BT]

Happy array programming.

01:15:59 [CH]

Happy array programming.

01:16:00 [Music]

</details>
