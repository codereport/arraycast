---
title: "Episode 59: Raul Miller - Precision"
date: 2023-08-05 00:00:00 +0000
episode: 59
buzzsprout-id: 18617068
keywords:
- array-programming
- array-languages
- conor-hoekstra
- raul-miller
- floats
- numerical-accuracy
- extended-integers
- numerical-analysis
- precision
- jlanguage
mp3-url: "/assets/audio/episode59.mp3"
episode-type: full
explicit: "no"
block: "no"
layout: podcast
excerpt_separator: <!--more-->
redirect_from:
  - "/episodes/episode59-raul-miller"
  - "/episode59-show-notes"
---
Raul Miller joins the ArrayCast to discuss precision in the world of computing.
<!--more-->

**Host:** Conor Hoekstra

**Guest:** Raul Miller

**Panel:** Adám Brudzewsky, Marshall Lochbaum, Stephen Taylor and Bob Therriault

---


## Show Notes

Array Cast -  August 4, 2023

Thanks to Bob Therriault and Adám Brudzewsky for gathering these links:

**[01] 00:01:49**

- [Stephen's book contributions sjt AT 5jt DOT comDyalog User Meeting](https://www.dyalog.com/user-meetings/dyalog23.htm)

**[02] 00:04:19**

- [Henry ArrayCast episodesArrayCast Episode #6](https://www.arraycast.com/episodes/episode-06-henry-richs-deep-dive-into-j)
- [ArrayCast Episode #18](https://www.arraycast.com/episodes/episode18-henry-rich-presents-j903)
- [ArrayCast Episode #48](https://www.arraycast.com/episodes/episode48-henry-rich)
- [ArrayCast Episode #50](https://www.arraycast.com/episodes/episode50-fold)
- [APL Farm Discord](https://aplwiki.com/wiki/APL_Farm)

**[03] 00:10:40**

- [Todd Rundgren](https://en.wikipedia.org/wiki/Todd_Rundgren)

**[04] 00:13:00**

- [J's Extended Integer type](https://code.jsoftware.com/wiki/Vocabulary/Constants#Extended_Integers)
- [lib.gmp](https://gmplib.org/)
- [Infinity in J](https://code.jsoftware.com/wiki/Vocabulary/Constants#Infinity)
- [Endianness](https://en.wikipedia.org/wiki/Endianness)

**[05] 00:20:25**

- [NaN or Indeterminate in J](https://code.jsoftware.com/wiki/Essays/Indeterminate)
- [Null in K](https://k.miraheze.org/wiki/Null%3F)

**[06] 00:25:46**

- [Fixed point type](https://en.wikipedia.org/wiki/Fixed-point_arithmetic)

**[07] 00:29:30**

- [Floating Point Math](https://0.30000000000000004.com/)
- [NARS2000](https://aplwiki.com/wiki/NARS2000)
- [J constants](https://code.jsoftware.com/wiki/Guides/Constants)

**[08] 00:35:20**

- [Hilbert Matrix](https://en.wikipedia.org/wiki/Hilbert_matrix)

**[09] 00:37:00**

- [Kamila Lisp](https://aplwiki.com/wiki/KamilaLisp)
- [Euler's Formula](https://en.wikipedia.org/wiki/Euler%27s_formula)
- [Dyalog Idioms](https://help.dyalog.com/latest/#Language/Introduction/Idiom%20Recognition/Idiom%20List.htm)
- [Roger's Comments](https://www.dyalog.com/blog/2015/12/apl-puns/)

**[10] 00:39:00**

- [World Math Day](https://www.jsoftware.com/papers/APLQA.htm#worldmathsday)
- [Complex Floor](https://aplwiki.com/wiki/Complex_floor)

**[11] 00:44:50**

- [Dyalog Time Functions](https://help.dyalog.com/latest/#Language/System%20Functions/dt.htm)
- [French Republican Calendar](https://en.wikipedia.org/wiki/French_Republican_calendar)
- [Proleptic Gregorian calendar](https://en.wikipedia.org/wiki/Proleptic_Gregorian_calendar)
- [Leap year rules](https://en.wikipedia.org/wiki/Leap_year)
- [Microsoft Date Time Picker](https://learn.microsoft.com/en-us/dotnet/api/system.datetime.ticks?view=net-7.0)

**[12] 00:48:20**

- [Ben Deane Calendrical C++](https://www.youtube.com/watch?v=qD8HQl1fU5Y)

**[13] 00:53:24**

- [Rosetta Code](https://rosettacode.org/wiki/Rosetta_Code)
- [J Wiki](https://code.jsoftware.com/wiki/Main_Page)

**[14] 00:59:13**

- [Ktye](https://aplwiki.com/wiki/APL%5Civ)
- [April](https://aplwiki.com/wiki/April)
- [ArrayCast Episode #23](https://www.arraycast.com/episodes/episode23-andrew-sengul)

**[15] 01:00:47**

- [Scrabble word list Collins](https://en.wikipedia.org/wiki/Collins_Scrabble_Words)
- [NWL](https://en.wikipedia.org/wiki/NASPA_Word_List)
- [Official Scrabble Players Dictionary](https://en.wikipedia.org/wiki/Official_Scrabble_Players_Dictionary)
- [16] 01:03:50 Contact AT ArrayCast DOT com


<details markdown="1">
<summary><strong>Transcript</strong> (click to expand)</summary>

Transcript

Transcript prepared by Bob Therriault, Igor Kim, Raul Miller and Sanjay Cherian

Show Notes

00:00:00 [Raul Miller]

Yeah, there's lots of infinities in math, and for the identities to hold, those infinities have to exist, but infinities are really not numbers per se. They're more my data is bigger than your data, expressed to the point of boredom. That's where the mathematician's stop at: it's boring, so we'll just say that that's the rule.

00:00:32 [Conor Hoekstra]

Welcome to another episode of ArrayCast. My name is Conor. And today with us, I have four panelists, along with a special guest who we will get to introducing in a few moments. First, we're going to do brief introductions. We'll start with Bob, then go to Stephen, then go to Adám and Marshall.

00:00:46 [Bob Therriault]

Oh, boy, I'm right off the top. This is great. I'm Bob Therriault, and I am a J-enthusiast.

00:00:50 [Stephen Taylor]

I'm Stephen Taylor, an APL and Q-enthusiast.

00:00:54 [Adám Brudzewsky]

I'm Adám Budzewsky, just an APL enthusiast.

00:00:57 [Marshall Lochbaum]

And to finish this up, I'm Marshall Lochbaum. I've been a J-enthusiast, sort of a Dyalog  enthusiast. Now I'm the BQN guy, and I-- well, no, as I've stated before, I'm not enthusiastic about it. [LAUGHTER]

00:01:12 [CH]

And as mentioned before, my name's Conor. I'm a polyglot programmer, love all array languages, and other languages as well. And with that, I think we are going to do two and a half announcements. We'll go to Stephen first, and then to Adám, and then we have half an announcement from Marshall.

00:01:28 [ST]

Just wanted to say thank you to the people who've contacted me about my book on vector programming in q and working with me to improve their q and the content of my book. If you feel like getting in touch with me and would like to work on your q on sjt@5jt.com. [01]

00:01:54 [AB]

And if you're listening to this immediately after it gets published, then you still have a chance to catch the early bird discount for the Dyalog 23 user meeting. It runs out on Sunday the 6th.

00:02:09 [CH]

And where's that being held/when roughly for folks if they don't know?

00:02:15 [AB]

It is in Elsinore on October 15 to 19. Elsinore in Denmark.

00:02:22 [CH]

With that, we will go to Marshall for his half of an announcement.

00:02:26 [ML]

This announcement is not entirely related to BQN. I will present it without comment. It's just information. You may be aware that BQN uses the letter double struck x in both lower and uppercase forms, actually, to indicate the right argument of a block function, So something like an APL defen. When I chose this letter, it was essentially unheard of, unused by anything I'm aware of. It follows the same kind of rule as the set notation, like real numbers double struck R in mathematics. But nobody really uses x. Sometime between one and two weeks ago, I think Elon Musk has opted to rename the Twitter service and the company owning it with the letter X. And as part of this, he chose as his logo the double struck X. So this character has another use. That's all I have to say.

00:03:26 [BT]

By this character, you're referring to Elon Musk?

00:03:28 [ML]

It's unclear whether he has uses.

00:03:33 [CH]

Maybe we will-- I was venting about this before we started hitting the record button. But maybe we'll dedicate part of an episode in the future to venting about the website formerly known as twitter.com and the people involved with the wonderful decisions being made around this platform. But we'll leave it at that and get to introducing today's guest who is Roll Miller. Roll is a veteran of the J programming language and has a long background with the language. I was notified by Bob that he's probably, I'm not sure if he's most well known for, But one of the things on his pedigree and resume is that he taught Henry Rich J. And Henry I think is our most frequent guest so far. I think he's been on three or four times at this point, typically talking about the new features that come in the J releases. [02] And Raul's also been involved in sort of extending the features of J. I think he worked on extending the integer type for faster performance, which I think we're gonna talk a little bit about today. He's also a very frequent, I don't know what you call, member or individual on the APL Farm Discord, which we'll leave a link in the description. We've mentioned it multiple times on the podcast before. It's a Discord server that has different channels for, I think, J, APL, BQN, KQ, I think all of them essentially. So if you have questions, you can go and ask them. It's one of the many places you can go and ask them. And with that, I think I'll throw it to Raul. If you want to, you know, fill in all of the gaps, take us back as far as you want and tell us, you know, a brief or a non-brief history of yourself, and then we can get into chatting about sort of integer types and performance and floating point representation and things like that.

00:05:20 [RM]

All right. I guess in the format of your original introductions, I've had aspirations to be something of a polyglot programmer, but I definitely have fallen into kind of a J focus in recent years. If we want to go back in time, at one point in high school, PCs were a new thing, and they were kind of a fun hobby at the time that I couldn't really afford very much of. So, in the back of one of the math classrooms, there was an ASR-33 teletype, which, 110 baud paper tape type machine that connected to a county HP-2000 system. That was, that's about my era. Some people had already been working on APL at that point, but not me, it was, I don't know, a logging Town. After high school, I got into things like, I had a job working on test and repair for navigation equipment, so I have kind of an electronics focus. I also did some electronics in high school, and over time I've hit computers from a variety of different angles, maybe not quite the focus that other people have had, but at one point I was working for about 10 years on search engines in APL, legislative database, And after that, did spend a good 20 odd years in doing media and advertising, stuff like that. And presently, I guess I'm just kind of goofing off. That's my history.

00:06:37 [CH]

So what point did you end up stumbling across the array languages and specifically J? 'Cause I guess you're quite involved with that community.

00:06:44 [RM]

I think I stumbled across array languages in when I was in college. I was going, my beginning of my college experience was community colleges. And one of the teachers there, Vin Grinnell, taught APL a lot. He had every single department of the community college using APL in some form or another. English department, history department, music department, biology, everybody he had. He had some using APL some way or another. And he liked it a lot. And he invited Ken Iverson to talk at various points. So I got to meet Ken Iverson there. And this was actually pre-J. And then J came somewhere after that. was kind of towards the end about the same point in time a couple years after that that J started community existence. Also there was I had some interest in k back then but that was more of a Manhattan thing and I didn't really have a job that focused on it. So I've kind of been with J for pretty much its whole life or not my whole life, J's whole life.

00:07:44 [BT]

I was going to say you must have been involved right at the beginning with like when J was starting up that was Roger and Ken, and I think soon after that was Chris and Eric and other people got involved. Were you involved with that group as well?

00:07:58 [RM]

I had loose connections. I mean, I met Ken and Roger at an APL conference and talked some time there. And I think I might have talked with them a little bit about some ideas related to J. I remember pushing the idea that ASCII was a good thing for a programming language because it enabled a lot of communications that, especially at the time, you couldn't really do with a custom character set. I remember talking a little bit about some things that maybe had to do with the parsing and some of the other ideas, but I don't know how much of my memories of that time are my influence versus me being influenced. So it's not a very interesting topic to delve into.

00:08:41 [CH]

And so at this time, so you discovered the array languages in college and you've gotten the opportunity to meet Ken because I can't remember the name, it was Vin something.

00:08:51 [RM]

Vin Grinnell, yeah.

00:08:52 [CH]

Vin Grinnell has basically, you know, disseminated APL throughout all the systems and every single department. And at this point, like, when you graduate, do you go and use Array Languages, like, for the rest of your career? Or does it, you're using other languages in your career and you're just sort of aware of it and then you come back to it at some point?

00:09:11 [RM]

It's close to that. I actually, I spent a summer doing, when I was a college student, I was doing temp work in the summer, and one of the places I temped for was Morgan Stanley, and I almost fell into an APL job there, but didn't. I actually fell into APL before I got out of college. I dropped out, got married, dropped out, had budget problems, and started an APL job that was LegiSlate. That was 10 years of user interface, where the user interface design was mostly around 3270s, and work-a-likes. And then after that I started working for US Today which didn't use array languages at all. And so that point became more of a hobby. And I guess in college I had an engineering focus. I had a little bit of mechanical engineering, a little bit of electrical, a little bit of civil. A good amount of physics and chemistry. And then because of, towards the end of it I fell into computer programming as my focus rather than engineering. Probably enough about me.

00:10:07 [CH]

No, no, no, so it's all about you. So you basically did APL for a while and got the opportunity to meet Ken. And the conferences, were those during college or were those afterwards?

00:10:17 [RM]

No, yeah, that was that was my attendance at the APL conference was organized and funded by Vin.

00:10:24 [CH]

Okay. For now. That's a neat opportunity that probably not a lot of college students or university students ever had the, you know, opportunity to go to to attend a conference like that during school.

00:10:35 [RM]

Yeah, we didn't have many other students. I do remember Todd Rundgren [03] was at the APL conference. You have the names that are hard to remember. A lot of people that were doing quite a variety of different things.

00:10:46 [BT]

So that's Todd Rundgren, the musician, Todd Rundgren. For those that have been millennials or such and may not know the name, Todd Rundgren is quite influential in music in the 70s, 80s, 90s, and then after that, probably still influential, but maybe not in wider circles.

00:11:05 [ML]

I just thought it couldn't be the same one. (laughing)

00:11:08 [CH]

And then so you said you switched to a job that wasn't using APL. So what's the story of coming back to J and then you ended up obviously working on the J language itself and starting to add features. What's the pathway or the story to your work there?

00:11:25 [RM]

I don't think I've ever really stopped using J since I never really started using J. It was always kind of a hobby. It was a side thing. I never had a professional, I can't quite say never. I did actually do some consulting work in J at some point in there, but for the most part, my interest in J has been personal rather than professional. As far as getting into working on J itself, that was, Henry had said, "Hey, you wanna do this?" And I said, "Sure, why not?" And I did it.

00:11:57 [CH]

Oh yeah, and so, you know, I mentioned that in your intro because Bob had mentioned that, so how did you and Henry up initially meeting because it sounds like from what Bob had mentioned that you were the one that introduced Henry to J and then Henry ends up introducing you to working on J. So what's the circular relationship or story there?

00:12:16 [RM]

I've always kind of been active on forums, computer forums and with J in the J email forum and my acquaintance with J initially was just on the J email forum and it wasn't so much I introduced Henry to J, it's just that early on, Henry had some questions about things. And I remember, since I had had a parsing focus and kind of a mental model, I was able to answer some of those questions.

00:12:44 [CH]

Interesting. And then so later on, after Henry had gotten involved working on J, he just reached out to you and said, Hey, do you want to do this? And you said, Sure.

00:12:54 [RM]

Yeah, pretty much.

00:12:55 [CH]

Cool. So tell us about, you know, the work or like the highlights of the work that you've done on on J.

00:13:01 [RM]

I think in over the long term, I've kind of had a minor focus on documentation, maybe a minor influence there. But the thing the interesting thing that we're talking about with Henry was the extended integers support and the rational type support. Js has always had extended integers [04], I think, or almost always. And the original implementation was as a basically Internally, it's an integer vector representing a polynomial where the value is 10,000, and the values in the integer vector are the coefficients of the polynomial. With just a couple of minor variations on that. The reason for 10,000 is because that's the largest power of 10, which is more than the square root of 2 to the 31 or 2 to the 32. So it fits nicely on even 32-bit machines, and you can multiply without having to worry about losing accuracy. And then you can, you know, fudge around from there to do the carry bits. It's, that's, wasn't a particularly fast approach, but it was simple to implement. And when J went to 64 bits that, you know, carried that same, same representation. The, the funny bits on it are, you know, normally with, currently in J we're using lib.gmp and there the underlying arbitrary precision integer is is an unsigned integer and there's a separate flag bit. That's the representation. With J's implementation, it was just a bit different because every digit in the coefficient or in the polynomial, we'd carry the sign that matches the polynomial representation. Also, they had a special value that they would turn to the coefficients for infinity. We actually had an infinity extended integer that was buried in the representation you never really saw. With, when we switched to lib.gmp, which is, most of my work wasn't really supporting extended integers, I was just ripping out the old support and plugging in lib.gmp, which is a much less impressive feat than it might seem. The lib.gmp form doesn't have an infinity for integers, but we do have infinity for integers in J. We still have had, you know, that's part of semantics. So the way I wedged that in was it's possible to represent infinity using rationals by having zero as the denominator. And lib.gmp doesn't support that, but we just... So I check every time I pass a rational number up to lib.gmp, I first check that it's not an infinity. That's maybe a quick sketch of what the change was like. like was take that polynomial representation, rip it out, use lib.gmp, which is a highly optimized way of handling arbitrary precision integers and rational numbers and plug that in. The "hard" parts would have been stuff having to do with prime number support and random numbers and probably the hardest part was the foreigns 3!:1, 3!:2, and 3!:3 which

export to binary or hex and import from binary or hex. And the reason that was hard, not really hard, but minorly hard, is because we have backwards compatibility requirements and requirements for other architectures. So the export and import has to work regardless of whether it's a big endian machine, a little endian machine, a 32-bit machine, a 64-bit machine. And it has to also import the old polynomial form on the new machine because people write this stuff to file and expect the stuff, the forms to still import those old format extended integers.

00:16:40 [ML]

Is that changing its behavior with the endianness and the word size, or it has to not change its behavior and get the same thing from the disk to memory?

00:16:49 [RM]

In the past, it has changed its behavior. I forget whether I'm included, and there is a little bit of... I mean, there's a difference between 32-bit representation and 64-bit representation, so that's still there. I think I might still be endian sensitive. I'd have to go look at the code though. It's been a while since I've worked on it.

00:17:13 [ML]

Yeah, so if you save something with this and you move it between endian machines, that might not be trustworthy.

00:17:19 [RM]

Oh, it includes a header that says what the format is.

00:17:24 [ML]

Oh, okay. So the total behavior, the header plus the data, always behaves the same. Right.

00:17:30 [RM]

I think they does some similar things where it uses native format as much as possible with a little bit of of overhead to let other machines know if they need to do conversions.

00:17:41 [RM]

On its serialization stuff.

00:17:43 [BT]

So one of the reasons that I had, I thought Raul might work really well on this, is because hearing him talk about representations of integers and numbers and such, you begin to realize that maybe numbers represented on computers aren't quite as stable a thing as you think they might be unless somebody does a lot of work to make them stable. Well, I've always thought that there's a lot of assumptions, maybe not so much by computer scientists, but a lot of people assume that a computer has accurate representation of numbers all the time. And ideally it does. But as soon as you get into some types like floats, you start to realize there's areas that a computer really can't represent physically every real number. It's just not possible.

00:18:28 [RM]

Yeah, there's lots of infinities in math. And for the identities to hold, those infinities have to exist. But infinities are really not numbers per se. Yeah, there's lots of infinities in math, and for the identities to hold, those infinities have to exist, but infinities are really not numbers per se. They're more my data is bigger than your data, expressed to the point of boredom. That's where the mathematician's stop at: it's boring, so we'll just say that that's the rule. And then when you get computers which are not infinite, uses run into those sorts of issues because they had to actually make something that works somewhere, check corners, so that things would fit in the bits available. And so as a result, for example, floating-point numbers do not actually have the... You can add floating-point numbers, but they don't have all the mathematical properties of addition when you with floating point numbers or any of the mathematical properties of addition really. It's not associative, it's not commutative.

00:19:26 [ML]

It is commutative.

00:19:27 [RM]

Oh it is? Floating point?

00:19:31 [ML]

Yes. There could be some issues with NaN's. I think it's perfectly commutative. It is definitely on finite numbers.

00:19:38 [RM]

Yeah, you're probably right. You're probably right. I mean, if you're going to overflow, you're going to overflow either way. So yeah.

00:19:41 [ML]

Overflow it away so yeah, so the annoying thing is maximum and minimum.

00:19:46 [ML]

So the annoying thing is maximum and minimum. There are instructions with SSE extensions or AVX for those. And those are not implemented as commutative. They could be, but they just chose not to. So the way they handle NaN's [05] is like, if you have a NaN on the left, I think the result is NaN maybe. And if you have one on the right, it's the thing on the left. Something like that. That's frustrating. Although J avoids this by not exposing NaN's to the user, which saves a lot of trouble.

00:20:19 [AB]

But it has indeterminate, right?

00:20:20 [ML]

It doesn't do calculations on it. You can import it, but you get an error if you try to use it.

00:20:26 [BT]

Yeah, that's one of the things. Sometimes people try and use NaN's as a marker, and they're always warned off doing that, because as soon as you try and do anything with it, it's going to blow up on you.

00:20:36 [AB]

I was going to say, in k, q, they use nulls, right? NaNs are nulls, and every type has them, and they're used as markers.

00:20:47 [ML]

Yeah, well, for the integer nulls, it just uses the smallest integer. And I guess the floats are probably NaNs. I don't know that for sure. But yeah, I don't know what happens if you do 0 divided by 0 in k or something-- float zero divided by float zero.

00:21:07 [AB]

Everybody pull up a k interpreter. Let's try this.

00:21:09 [RM]

Which version of k?

00:21:10 [ML]

Which k? [LAUGHTER]

00:21:15 [RM]

I've spent a little bit of time learning some of the versions of k, but not all the versions of k, and not in enough depth.

00:21:23 [ML]

Well, many versions of k, I think, just have not been presented to the public. So it would be very impressive to know them all.

00:21:30 [AB]

So in the KX k, it gives me 0n for 0 divided by 0.

00:21:38 [ML]

I think that means null, but 0.0 divided by 0.0. That's different.

00:21:43 [AB]

So that also gives me 0 lowercase n. So I think division always returns a float, no? So it's not an integer. If I remember right, 0 uppercase N is an integer, and null and lowercase N is a float. But if I do 1 divided by 0, it gives me 0w. Who knows?

00:22:03 [ML]

That should be infinity.

00:22:05 [ST]

That's correct.

00:22:08 [ML]

Is the idea with that the w is the lower half of infinity symbol? Is that it, or is it something else?

00:22:11 [RM]

Probably Omega.

00:22:13 [ML]

Oh, that's good too.

00:22:14 [AB]

That stands for wide or something. Like you need a lot

00:22:17 [ML]

Doesn't stand for like keys to the wingdom. [LAUGHTER]

00:22:20 [AB]

Oh, it's a wide integer. You need a lot of bits to represent infinity.

00:22:26 [ML]

But it uses the same number of bits. It's just the smallest, so they close off the smallest integer. That's no longer a regular number.

00:22:36 [AB]

Right.

00:22:36 [AB]

So that's missing one number, right?

00:22:38 [ML]

And they use that for null.

00:22:40 [ST]

Yeah, there's nulls and infinities for all the numeric data types.

00:22:46 [BT]

So a general question I've got is, why doesn't everybody use some form of extended (or rational if it's a fraction), and then convert it back to float at the end of calculations, because at every point you do a calculation with these approximate numbers, you get a little bit wider error. I'm assuming it would be slower to use extended forms.

00:23:13 [ML]

I don't think that's the big issue. The big issue, I would say, is that rational numbers, sure, they represent fractions exactly. But at the moment you have to take a square root, they're no longer exact.

00:23:24 [AB]

Or trigonometrics

00:23:27 [ML]

Yeah, yeah trig would probably be actually a more important problem because that's gonna show up like everywhere in geometry and stuff.

00:23:34 [RM]

Although the big annoyance with trig is when you're trying to approximate zero after a few calculations.

00:23:41 [AB]

Yeah

00:23:42 [RM]

The little fuzz leftover.

00:23:46 [ML]

So I guess this is a different discussion. It depends on your use case whether that matters or not. I mean, if your computation is inherently doing cancellations and unstable, then you can mess yourself up no matter what you want to do. But as long as you avoid that, then you're good. Like, if you're computing with real-world input data, then your input data has an error margin. It's definitely going to be larger than the error margin on a double-precision float. So, I mean, yes, float computations are going to introduce error as you go along. But no, it's probably not worth worrying about.

00:24:23 [RM]

It's mostly in banking calculations where you wind up with long series of plus and minus that you might have somebody pushing to be right near zero or something.

00:24:34 [ML]

But I think you've got a requirement to be ... or I'm not sure how this works. I think it's it's required to be inexact specifically in the way that decimals are, like base 10.

00:24:46 [AB]

What if there's three for a dollar?

00:24:51 [ML]

I don't think you can do that. I think it's just... [sentence left incomplete]

00:24:54 [AB]

[laughs] I'm pretty sure I've seen... [sentence left incomplete]

00:24:57 [RM]

If you're actually working with money, you want integer values, so you work with pennies rather than dollars for US coinage?

00:25:05 [ML]

Yeah. If you round off to the nearest penny, that's requiring fractions with the denominator being 100.

00:25:11 [RM]

I think we had a stock exchange crash related to that issue.

00:25:14 [AB]

I asked some financial people that actually do like commercial financial software about this. They wanted more precision. And in Dyalog APL, we have the option of switching to 128-bit decimal floats, which should give plenty of precision for this kind of thing. And I asked the question: "Why don't you use integers? Why are you using floats for people's money? That doesn't seem right."

00:25:37 [CH]

Note that there's an actual type (that exists in, I don't want to say every language, but you can implement it in every language) called a fixed point type. [06] There's integer types; there's floating point types. And then in between is a fixed point type, which is a floating point type represented by an integer. I only know all about this because I had to implement it for an NVIDIA library. And part of that was doing like a month long research of all the existing implementations and rounding behavior and stuff. But basically you have a type that's backed by an int32 or 64 or even 128 and you do all the conversions. So like you store it as an integer but $1.23 is stored internally as the integer 123. So you never end up with the floating point addition, like those problems. That being said, you still do inherit some of the problems of floating point numbers because sometimes you're going from a floating point type to the fixed point type. There's some conversions at some point that happen. And there are some numbers that are just not representable as a floating point number.

00:26:56 [ML]

Well, like half a penny.

00:27:00 [CH]

Um, no, so what I mean is like there are specifically because like a floating point number it... [sentence left incomplete]

00:27:04 [ML]

I should clear this up. The difference between this and a rational type is that the denominator here is fixed for all the computations you're doing. Is that right?

00:27:13 [CH]

Correct. Yes, you can choose any base you want, but the base that we're talking about is a fixed point type with base 10.

00:27:19 [ML]

And so I mean, no matter what you choose, there's always going to be a higher resolution. So you better choose the right base.

00:27:26 [CH]

Right, exactly. But the problem I was mentioning isn't that one. So definitely choose the right base because that's the resolution you're going to be stuck with doing your computations. But within a floating point number itself, there are just certain numbers that a floating point cannot represent. It's impossible for it to ... [sentence left incomplete]

00:27:43 [ML]

Nearly all numbers [chuckles].

00:27:46 [BT]

[laughs] Infinitely many numbers!

00:27:47 [CH]

[laughs] Well, I guess if you want to do the whole infinite number of numbers.

00:27:52 [ML]

All of them but a finite number, which is a whole lot!

00:27:55 [CH]

The finite numbers over infinity technically means yes: most of them aren't representable. But for your everyday calculations, usually it works and then you'll run into writing some test where you convert, because you'll have a constructor for your fixed point type that takes a floating point type, but the floating point type that you type in actually isn't representable, so it'll convert it. So for instance, I remember, I think it's 0.003 is not representable as a float 32. So when you pass that into the fixed point type constructor in base 10, you expect to get like 3 cents, like 0.003, but you end up getting 0.002. And I was like: what's going on here? I'm staring at the 0.003 and then getting back a different number. And then sure enough, like the way I ended up talking to like a senior person that knows everything about everything and especially about floating point types. And he was like: oh, go to this website where it actually shows you like the, you know, decimal representation in binary or whatever of your mantissa and your etc. And then it shows you that actually 0.003 in floating point is actually 0.029999999 and you end up truncating that into fixed point. Anyways, the point being is that at a high level, fixed point exists, and that at a very detailed level, there's issues with this stuff everywhere, no matter how hard you try to avoid it.

00:29:16 [RM]

Limits. You run into them.

00:29:18 [AB]

There's also a website called... uh oh, wait, am I supposed to say what the website is called? 0.30000000000000004.com [07]

00:29:33 [ML]

We're not going to put this one in the show notes. You got to piece it together yourself. [everyone laughs]

00:29:40 [AB]

That explains it in very basic terms, why you get it. And then shows for many, many programming languages how you can see the same problem everywhere. There will always be numbers we can't represent. But about the trigonometric stuff, NARS 2000 (which is an APL with all kinds of fancy features) has pi-point notation (so it's A times pi to the power of B) as a native type.

00:30:11 [ML]

Doesn't J have this? J has base E.

00:30:14 [RM]

In its notation it (J) has it, but it converts it into floating point internally, so it doesn't have it as a type.

00:30:23 [AB]

Oh, maybe NARS does that as well.

00:30:25 [ML]

Yeah, it sounds like the same thing to me.

00:30:27 [AB]

Yeah, maybe it's not actually native. Maybe it does ... [sentence left incomplete].  Oh, okay, but it allows you to do rational numbers with it.

00:30:34 [ML]

Oh. Yep, no, that doesn't sound like the same thing anymore.

00:30:37 [AB]

You can write 1R3P1. That is one third pi.

00:30:44 [RM]

Yeah, J will let you do that, but it'll convert it to a floating point number.

00:30:48 [AB]

Yeah. But do we actually need these things? Yeah, so the bankers need to make sure that people's money is right. And the financial people I spoke with, said that even if you try to scale things to pennies, you still end up with things and prices that are off and there isn't enough precision for these things.

00:31:09 [RM]

Advertising is often per thousand. So they're working on thousands of them because advertising isn't worth very much. They have very small quantities [of money] that they're working with. [laughs]

00:31:18 [ML]

Well, maybe pi comes up like if you walk in a perfect circle around the New York Stock Exchange. Some currency related pi things should happen, right? And you need to be able to represent that!

00:31:33 [AB]

One thing where it comes up: I remember seeing this. I used to play Kerbal Space Program from fairly early days when it wasn't very well implemented yet (hadn't fixed bugs and so on). It's a spacecraft simulator and you have the spacecraft in orbit. It doesn't do like N-body physics, so things are just in elliptical orbits. And it computes the orbits, you have the time, and then you have the orbital parameters and computes where you are. And if you go far enough out from your origin point in orbit, fun stuff starts to happen because of floating point issues, right? When you multiply floating point errors with astronomical distances, then you start feeling your spacecraft jumping.

00:32:25 [RM]

Yeah, I'm sure NASA has a bunch of interesting limit problems that we don't even think about?

00:32:30 [AB]

No, I think NASA doesn't have this.

00:32:32 [RM]

Well, no, they do. They've just dealt with it in various ways.

00:32:35 [AB]

No, and I think I read about that. No, it only comes up in simulation. It doesn't come out in the real world because the real world isn't precise enough that you actually need to make this kind of computation. We always need to make course corrections because we cannot make things precise enough.

00:32:49 [RM]

Well, they aren't simulating, of course, at NASA, but they do have all these bodies that that they're tracking, and they have to have a variety of arcane techniques to make sure that they have reasonable accuracy.

00:33:00 [AB]

I don't think so. I think [with] our measurements, there's nothing we can do observing orbital parameters of things where our measurements are precise enough that the floating point numbers matter. I've seen the question asked.

00:33:15 [ML]

I don't think we even know the rotation speed of the earth bed.

00:33:17 [AB]

No, I mean, just look at leap seconds that need to be adjusted, like on short notice. [chuckles]

00:33:23 [ML]

Not only our knowledge of the speed, but the error bars on that speed and its actual value might be that large.

00:33:30 [AB]

Somebody asked the question: how many decimals of pi does NASA use? It must be like some very large number and they use some very simple approximation of pi because ... [sentence left incomplete]

00:33:38 [ML]

They just use 3! [everyone laughs]

00:33:40 [AB]

I don't think it's quite 3, but I don't remember. It was surprisingly few decimals. [chuckles]

00:33:43 [ML]

Yeah, like what? 6 digits or something.

00:33:47 [RM]

There was a state legislature that apparently legislated three as pi at one point.

00:33:52 [BT]

I thought it was Indiana, but I'm not sure about that.

00:33:55 [RM]

That didn't work. I think that's what I remember. But when I was talking about NASA, I meant the equations they use to represent where things are heading. They don't have a floating point accuracy problem. They have a problem in representing equations. They have the n-body problem in spades. They have a very high n for their n-body problem. That's what I was trying to say.

00:34:18 [AB]

But again, simulation is different from [the] real world.

00:34:21 [ML]

Yeah, if you're simulating anything that you've measured, then the measurement error is the dominating factor.

00:34:28 [RM]

They don't specifically simulate the way you might in like Kerbal Space Program.

00:34:31 [ML]

Yeah, if you're simulating theory, I can see how you definitely come up with this.

00:34:36 [RM]

You know, they do have to plan flights, which means they do have to know where things are going to be when they get there. So they do have, you know, a variety of issues that they work with in various ways.

00:34:45 [AB]

Uh-huh. So I just looked it up and the JPL (not the J programming language, but the Jet Propulsion Lab): they spell out the digits they use, but then looking at it, it's actually just the 64-bit float. Binary float precision. That's what they use. So, probably not because they actually need that many. It's just because that's the value they've got.

00:35:08 [BT]

One of the first places it was sort of brought home to me with J was actually in a lab that Roger Hui put together, which was an idiosyncratic introduction to J, and I'm looking at it right now [chuckles]. There's 10 lessons or steps in this lab. Oh no; there's 15 altogether, but at the 10th one, he talks about the Hilbert matrix, [08] which is actually pretty simple. It's just an addition table, and then you add one to the whole table, and if at that point you take the inverse of it, you get the Hilbert matrix. If you do it with "extended" is really actually quite neat and precise. And then if you look at the lab, there's an equation that [shows] he can actually take that and you can tabulate the number of primes less than N. So if you had an N by N matrix ... [sentence left incomplete]. If it's 15, you're gonna have all the primes less than 15 will pop up out of this process. Now if you do that with an extended integer, it comes out absolutely clean. If you do it with float, of course, it's just way off the mark because of all the calculations and what it's trying to do. There's a precision in mathematics and certain number theory areas where this becomes really important because you're not dealing with the real world; you're dealing with concepts of numbers. And I find that's where J kind of gives me some leverage that I don't have in other languages, or if I'm not working with an extended precision.

00:36:42 [RM]

Another thing is there's a whole field of numerical analysis, which deals with some of those, creating some of those issues.

00:36:47 [ML]

I do think there are a few newer languages that have pretty good access to big numbers too, though. So you don't necessarily have to go with J. Kamila Lisp [09] is a newer one that's got like all sorts of math functionality. So that's cool.

00:37:02 [AB]

We have a fun trick in Dyalog APL. We have this (I think we mentioned it on this podcast before), this implementation of what we call "idioms". These are just phrases of characters after each other. The interpreter doesn't take at face value, but knows what it means and does something else. And if you write asterisk-circle and followed by a number, so that's "e to the power of pi times some number", then it won't actually do the math. It will give you a precise result for Euler's expression, ([the] famous formula). So it looks like we have better precision than we actually have got. If you modify anything, then it doesn't work. [chuckles]

00:37:44 [ML]

Yeah, that's a little scary.

00:37:45 [BT]

Now, is that the Volkswagen engineer issue, [chuckles] where if you set certain inputs, you get certain outputs? Is that how that works?

00:37:51 [ML]

Well, having an exact way to calculate that is useful functionality. I mean, you could get it from sine and cosine, which I think is what it does underneath. Having access to the idiom is pretty nice. Having it be an idiom is ... [sentence left incomplete]. I'm not going to say it's bad, but it's more questionable. There are definitely situations where you could have a problem with that.

00:38:13 [RM]

There's something of a spectrum between numerical calculations on one end and symbolic calculations (maybe Mathematica or Wolfram style) at the other end, and compilers being maybe a third point of that triangle. We have different ways of manipulating the concepts that we've expressed in math and trying to put them in machine form. I think J tried to step a little bit, you know dipped its toe in the water in that water, but there's a lot of infinity. So it's a huge pool to explore.

00:38:52 [AB]

Well so Roger Hui calls this star-circle, "show off" and if you do it with a large number, he calls it "shameless show off". But he also has a paper about it (we can link to it) with APL quotations and anecdotes about World Math Day. [10] And then he writes in little square brackets: "guess who did the coding to make this happen?"

00:39:23 [RM]

Knowing where you wanna go is kind of important. That's our use cases to getting… connecting the dots and getting anywhere with all this stuff. [chuckles]

00:39:31 [AB]

Clearly Roger Hui's reason to do anything was that he should be able to show it to the Galactic Emperor and make the emperor impressed [chuckles].

00:39:43 [ML]

So the emperor won't just say: "You're just shameless, aren't you?" [laughs]

00:39:47 [BT]

Well and that's even before we get into complex numbers because they have an entirely different challenge. I think it is especially with ceilings and floors and stuff.

00:39:58 [AB]

Oh, that's complicated.

00:39:59 [ML]

Yeah, that's not precision related. Well, there are some precision related issues with ceiling and floor if you're going to do it tolerantly. That's a big topic. I remembered, (I think this is closer to our current discussion) [and] this maybe should have been an announcement. Just a few days ago, I made a change to the BQN compiler, so it actually parses the numbers you put in correctly. [chuckles]

00:40:27 [AB]

Wait, what did it do before? [everyone laughs]

00:40:30 [ML]

Harder than it sounds. I mean, I knew this was a problem. When I made the compiler at first, I didn't know how to fix it. The issue is that the compiler is all array code. So it wasn't really clear to me at first how to make something that parses ... [sentence left incomplete]. it parses all the numbers in your program at once. And I didn't know how to do this and maintain the accuracy. Like you might think to parse a number: all right, you'll just go in order of the digits. And for each digit, you'll multiply what you've got by 10, and then you'll add the next digit. That's inaccurate. So what we get is like we got a report for BQN: "well, I typed in 17 nines, and this number should be representable in floating point". Well, it's not exactly representable, but it should give you 10 to the 17th. It should round up 1. And instead, it actually gave you a number above 10 to the 17th. It would round up further. And this is because of this adding procedure. Once you go past the numbers that are exactly representable in floats, which are a little larger than 10 to the 15th, then you start rounding at every step, which I guess we can get into and talk about how floating point numbers round. But you'll round at every step, and so this can give you the wrong result. So then what I did to fix this is I figured out: well, numbers up to the 10 to the 15th are always exact. So this strategy is perfect for those. So I'm going to split off the last 15 digits and do it that way. And then [for] the digits above that, if I did 15 digits, then I could get a number for those. But then I can't add it, because if I multiply by 10 to the 15, then I'm introducing a rounding again. So I've got my top number, and I would multiply, and that rounds, and then I would add, and that rounds again. So that's also inaccurate. But what does work is to take the five digits above that, because actually any five-digit number times 10 to the 15th can be exactly rounded, because 10 to the 15th has all these powers of 2, which are exact in floating-point numbers. So I take the five digits above that, and I add them to the 15 below that. And that way, I can parse up to 20 digits accurately, which is, of course, not perfect. But no programming language is really going to let go ... [sentence left incomplete]. You have to read thousands of digits to get an exact result for floating point numbers. And no programming language is really going to go that far. They're just going to ... [sentence left incomplete]

00:42:53 [RM]

Actually, you're reminding me of a problem I ran into when I was working on J on this stuff.

00:42:58 [ML]

I'm not surprised.

00:42:59 [RM]

J comes with a huge test suite, a lot of which Roger Hui put together. And he was very careful at the extreme ends of floating point precision to make sure that they converted properly to rationals and integers. And there's little off by one bit errors that you can get with 1,000 digit integers that I had to handle correctly to pass this test.

00:43:22 [ML]

Yeah, it's hard to-- everything is so finicky that it's like you get it working and then you say, what did I just do? I was actually surprised the 5 plus 15 thing came out that clean. Like when I originally did it, I was thinking, I just don't know a way I can do this with arrays. It might not even be possible. But then I found that strategy.

00:43:47 [RM]

If you have an array of fixed-width integers, you get some interesting constraints, don't you? Especially floating-point.

00:43:54 [AB]

I have another example where the precision runs out. Things are interesting. A couple of years ago, we added something called quad DT, a date time to Dyalog API. [11] And it does conversion between all the date time formats known to not humankind, but Dyalog-kind, I guess. If you find one missing, let us know. And that's interesting, because some of these formats are just counting ticks of some size from some time. So an epoch, that's called. And if they're using small ticks, and it's a long time ago, or it will be in a long time, then you have precision issues. So then things get interesting. So for example, we have something called J nanosecond time, which we picked up from J, using the epoch of 2000, beginning of year 2000, but it's using ticks of one nanosecond. There are a lot of those in a year. And then we get all kinds of interesting problems with internal computation. So internally, we have to store it as two different floats and combine it to make sure to maintain the precision.

00:45:08 [RM]

Did you handle the French Republican calendar there?

00:45:11 [AB]

We're doing everything on the proleptic Gregorian calendar. So to simplify matters. We actually had an interesting question this week as to what do we do about year 4,000. Is year 4,000 a leap year or not?

00:45:27 [RM]

And we'll all change between now and then to make it a leap year or not leap year.

00:45:33 [AB]

Yeah.

00:45:35 [ML]

So if you just extend the current rules, It's not a leap year, right, because it's a multiple of 400. But nobody's claiming--

00:45:44 [AB]

Yeah, so the problem is that Calendar would be slightly better if we had a 4,000 year exception rule. Yeah. Just like, it fits nicely into the pattern.

00:45:55 [RM]

Let's extend the pattern and go with it. If you're wrong, it'll be a while before anybody notices.

00:45:58 [AB]

Yeah, it's true. But the problem is that we're trying to convert between all these different data and formats. And then there's a Microsoft GUI element called the DateTimePicker, which allows you to select any date up to year 9999. So now, how do we deal with those dates? It turns out that our calendar is interesting because of issues, right? Things are not precise. Like we're talking about these astronomical measurements and then nothing is precise and it's all one giant mess. And we're assuming our calendar is fixed, like trying to approximate so that equinoxes, solstices end up in the right locations, but that's not the case at all. The Gregorian calendar is made for best approximation so that Easter ends up in the right place. But because of Earth's elliptical orbit, and everything is oscillating around, It's a giant mess.

00:47:05 [RM]

Yeah, you get leap seconds when dealing with astronomy. You go back in time, you get geographical Julian/Gregorian issues.

00:47:12 [AB]

Oh, what was that I saw the other day? The global warming affects the spin of the Earth.

00:47:17 [ML]

Oh yeah, makes sense.

00:47:19 [AB]

If you ever sit on an office chair spinning and you pull your arms in, you speed up. If you stretch your arms out, you slow down. Okay, so if we increase the temperature of the atmosphere, then the atmosphere expands, which is equivalent to spreading your arms out and slowing down Earth's rotation. So the future time values will depend on if we manage to stop global warming or not. Enjoy.

00:47:45 [ST]

I can't get the image out of my head of you sitting in an office chair spinning around.

00:47:53 [RM]

And NASA has to deal with that for every planet. Because other planets probably aren't warming at the same rate as here.

00:47:58 [AB]

Oh, and things could completely go insane if you try to deal with time across different gravity wells.

00:48:04 [CH]

For those that are interested, even though this is kind of-- it's on topic, but off language. There was a talk given by Ben Dean, who's one of my favorite speakers and has been a guest multiple times on my other podcast, ADSP. He gave a talk called "Calendrical C++." I believe the C++ Now version, by the time this airs, should be out on YouTube. I know the notification for this premieres at is already up. [12] And it's a talk that focuses on C++, but he even, he starts at the top of the talk and says, "This talk is being given, you know, "versus a couple of other C++ talks. "If you are here for the C++, "please leave now and go see one of the other talks. "I won't be offended." Because although there is a substantial amount of C++ in this talk, it's primarily a talk about history of calendars and he goes all the way back to like, you know before BC times and you know talks about the first calendar all the way to the Julian and Gregorian calendars and how a lot of the motivation for different Calendar types came up because of how to calculate Easter because you know religion's a large part of our history and You know back when they didn't have SMS and emails and whatnot like knowing when to celebrate Easter was like a pretty big deal because if you celebrated it on the wrong day was considered like you were not You know worshiping the Lord and Savior enough. Anyways. It's very very interesting And it touches on all this stuff, and I think it even touches on the fact that we are we are now in the Gregorian Calendar days, but there is actually this other type of calendar that is technically a little bit truer when it comes time to you know the year 4000 etc and Anyways, very fascinating link will be in the show notes even if you don't like C++ or don't know it. It's a it's a fantastic talk and Yeah, it's it's amazing You know how much complexity there is and it's all you know in this Standardized library in C++ called chrono so at the end of the talk he's showing how you can calculate You know when is based on the moon cycles if we define these you know types you can do all these Calculations in terms of moons and can we calculate Easter based on that? I won't ruin it for you go check out the talk if you if you want to see if it's possible but yeah, a lot of a lot of complexity and Insert, you know leap prefix year second, etc  And thankfully, I don't have to be the one to write that code.

00:50:41 [AB]

Months leap months. Those are fun.

00:50:45 [ML]

I will say it's very fortunate, though, that the time standards we use, they don't take into account the leap seconds. So if people say, like, a standard time format, and the one I use for everything in BQN, is what you would generally describe as seconds since the Unix epoch, but you leave the leap seconds out, and so that way there's exactly 24 hours to the day every day. So this is one thing you actually can do computations on. And I mean, if your timestamp is during a leap second, I don't remember what happens exactly. You may need to consider this. And the distance between two timestamps, you might be off by a second if there's a leap second between them. But it's pretty nice being able to say, well, this number of seconds since the Unix epoch means it's on this day and this time during the day. So sometimes there's a little bit of sanity floating around in all the chaos.

00:51:44 [RM]

Well, the simplifications are very handy. It's just when you get into the details, you run into the cases where you have to be aware that there are simplifications.

00:51:51 [ML]

Yeah.

00:51:52 [RM]

You deal with that somehow.

00:51:54 [ML]

But fortunately, I think for practical use, this second sense, the Unix epoch, it covers a whole lot of use cases without really worrying about those details.

00:52:04 [AB]

So coming back a little bit to the topic here, Raul, you mentioned that you haven't used J really professionally, but for your own things. I would love to hear what have you used it for? There must be fun things then, since you weren't paid to do it.

00:52:18 [RM]

Yeah, I goof off a lot. And when I said I haven't used it professionally, that's a little bit of a lie, because I did do a consulting job where I was working for Skip Cave. He was analyzing a bunch of audio files, a few terabytes of them. And a lot of that happened in J. We're mostly just classifying it. So it was parsing XML and computing SHA sums and building a database of things for audio files. So that is one of the things I've used J for. I use J as a calculator. I use it to build little editors. I can't say that there's any single purpose there. At one point, I did some cryptography work with it. There's no real theme that I can really pin down here, because it depends on what my focus was at the time and my focus over time changes. I've built parsers with it. I've spent a fair amount of time populating Rosetta code with J examples. [13]

00:53:18 [BT]

One of the big things Raul's doing right now is he's involved with the whole J Wiki endeavor. Which is much appreciated because Raul brings a lot of expertise to it and history and background. But that takes up a fair chunk of time, although I think it's, there have been times when he's been very interested in certain aspects of it and things have moved ahead very quickly. It's quite apparent if he's not interested, then somebody else may want to go to that because it's not going to happen as quick. But I'm guilty of that as well. If I'm interested in an area, I'll develop it a bit more. And if I'm not, it's a wiki, somebody else can go in and change it. But that's just the nature of being involved in something that big. But I know Raul is spending a fair amount of time in different areas of that working. And I think he probably sells short maybe his influence on the community and his providing of information either in forums or in other ways through the wiki of documentation and explaining different concepts and stuff, because he does that really quite well.

00:54:32 [CH]

Maybe a good question to end on as I just realized this is you are, I don't know how many people out there have more than a decade plus experience in both APL and J, but it It sounds like you're definitely on that list because you started off doing APL and then later on switched to J. So I'm always curious with folks that have experience in multiple of these array languages, what are the biggest differences that you found and things that you liked about one that the other didn't have, vice versa, in terms of... One of the top questions we get from not necessarily folks that are super experienced that are listening to this podcast, but a lot of folks that listen to this and get interested, they always ask, you know, what's the one I should start on for doing X or Y. And so I think, you know, highlighting some of the differences, some of our listeners are definitely including myself would love to hear your personal thoughts on that.

00:55:32 [RM]

It's really I think, if I was going to advise somebody to pick one or the other. I'd say, you know, look at the community that they're interacting with, and see which community fits, you know, which way they can find that community in the APL side of things on the J side of things. And make your decisions based on that. That's where I think I would go if I was giving that kind of advice.

00:55:54 [CH]

Yeah, that's a great, great piece of advice. I can't remember where where I heard recently, I think it was on a podcast. I mean, even if I didn't think that it probably was in a podcast, where someone was talking about Zig versus Rust and they had implemented I think it was a shell or some kind of command line thing to replace Bash or Zush or all the different flavors that you have, New Shell now. And one of the questions was why did you choose Zig versus Rust? And their answer would basically boil down to I went to Rust, tried it, and I had also tried Zig a little bit and I just liked the Zig community better. I just liked the things that they were talking about and the problems they were solving. And he said because it was a personal project that he just, you know, it's up to him and he thought he would be happier interacting with that community, which so that's kind of sounds similar to your advice is just find the community that you feel like you click with best.

00:56:55 [RM]

And you're going to be spending a lot of time on persistent issues, digging through finding the little technical problems. Having a community can fall back on is where there's a nice bit of sanity, fresh air there.

00:57:08 [CH]

Yeah, yeah, especially to, you know, interacting with that community is gonna influence, you know, your experience of, you know, using that language as well. I mean, some people have the opinion that ecosystem and community is less important, but then like the language itself, but in my opinion, I think that, like, if you look at Rust, you know, regardless of that other person liking the Zig community better. Like I think Rust is part of the reason they've been so massively successful, even only having started like a decade ago, is they've put so much effort into building a community and like an onboarding experience that is just super nice, where you don't know what you're doing, you type something, and then the compiler tells you, Oh, did you mean this? And you're like, Well, I don't know, But maybe ...

00:57:56 [RM]

There also are, you know, strong domain differences between different languages, you know, different languages have areas of focus where they excel. And you might want to be picking a language off of that. It's just in the context of APL versus J that  those differences aren't the sort of thing a beginner usually has in mind. That's why we focus on the community there. There are there are reasons to pick a line.

00:58:20 [CH]

Right, right. Like, yeah, if it's between JavaScript and Rust or something like that. There's major differences between those, but when it's sort of in the same ballpark, that's a great point, is that it's less important in terms of what the language is capable of, because it's roughly the same thing. All right, before we throw it over to Bob, any final questions from any of the other panelists?

00:58:44 [ML]

Don't say complex numbers. We need another episode or five.

00:58:51 [RM]

Or Gaussian integers.

00:58:54 [CH]

And I guess actually one thing is to note, and implicitly maybe we've mentioned this, but is J the only language that has support for extended integer types? Is there any other array language that...

00:59:07 [ML]

It's the only one of the big implementations, but like I said, there's stuff like Kamila Lisp.

00:59:11 [CH]

I meant more in the Iversonian camp of like APL, K, Q.

00:59:17 [ML]

I think there are even some k implementations that give you access. Like there's the one in Go by KTYE. [14] I think that one has extended precision numbers. So they're not as hard to come by as they used to be because a lot of the implementation languages are now offering them too.

00:59:34 [CH]

Right.

00:59:34 [ML]

April should have them because it's based on Lisp.

00:59:37 [CH]

Well if you are looking for extended integer types, check out J. Adám, what were you going to say?

00:59:42 [AB]

Gonna say well, N 2000, it's a proper APL open Well, NARS 2000. It's a proper APL, open source, free thing. It has some problems running on the Linux, I'm sorry. And I'm not sure, somebody should try if it can be run on the wine or not.

00:59:54 [CH]

We should, we should. I'm not sure if it's worth a whole episode. But right when, because this already came up too, is like which K, which APL, and that was also one of the reasons that Raul pointed out was, there's one J, right? Like there's different versions which you grab, but like there's one main implementation. And I wonder if it's worth chatting about that in a future episode of like the proliferation of the APLs and Ks, does that hurt the success? Because the thought in my head was that part of the reason, and no one's, if anyone guesses what I'm about to say, let us know, email Bob. If you can predict what I'm about to say is this it makes me think of why? Chess is popular and Scrabble is much less popular and it's because Scrabble in the Scrabble community. [15] There's a bifurcation of communities because there's two Main word lists. There's the call-in Scrabble word list csw and then there's the north american word list nwl And they can't agree on like what is the official? Scrabble list so at every like tournament at the elite professional level they've got like two sub-tournaments going on, or they only have one tournament, and if you operate with a CSW, the Collins word list, you can't compete in that because NWL is smaller and you're not familiar with that word list. And like, in my opinion, if the Scrabble people could just get over themselves, choose one dictionary, and there's technically a third one that's the official players dictionary that you buy in stores, that one's even different than those two. They just just need to get on the same page because I think like it hurts the community like people that are just casual Scrabble players don't really want to you know oh is it Collins is it NWL is it OSPD?

01:01:37 [ML]

See I didn't even know about this and I've definitely played Scrabble games where we've looked up words I don't have any idea what list we used so I'm not convinced it's a problem.

01:01:46 [CH]

If you google it you'll end up at OSPD which is the official Scrabble player dictionary, but that is not used in tournaments. That's a subset of the NWL, which is different than what they use globally and mostly in the UK. You know, does it matter? Maybe. Stay tuned for episode 81, where we run out of topics and we talk about APL, K proliferation. Yeah, were you going to say something Raul?

01:02:12 [RM]

Linguistic drft is just one of those annoying things that people do. But there's even chess has variations variants that people do is just that.

01:02:23 [ML]

Yeah, but there's an official established.

01:02:27 [CH]

Yeah. I feel like are you talking about the different versions in terms of classical versus bullet or like the ones where they change the rules of the game?

01:02:33 [RM]

The ones where they change the rules of the game.

01:02:35 [CH]

Yeah, I feel like chess though it's like 95% is the main one and then the 5% they just are starting to try and make things interesting because people argue who's actually the best chess player and it's all about memorizing openings and things and when you slightly tweak the rules it adds more like less stored knowledge so it's like oh well we know they're gonna use the you know something opening and and so this person is gonna try and keep them from doing that whereas if you change the rules and it's like it's all just like based on mental power and yeah it's less like the community is split in half. Sorry Bob you were...

01:03:12 [BT]

Well I was gonna say if you predicted that the conversation was gonna take that turn, then I definitely want you to send a message to contact@arraycast.com because you have powers that I would, I think anybody would treasure.

01:03:27 [ML]

So don't just send a message, send us our next ArrayCast episode and then we don't have to record it.

01:03:36 [ST]

And whatever it is you're taking, let us know where you can get it.

01:03:40 [CH]

Yeah, yeah. Is it available on amazon.ca? Because I would like some too, please.

01:03:46 [BT]

In any case, the ArrayCast contact@ArrayCast.com is how you get in touch with us [16] if you want to drop us an email. Show notes will be on the show. I think that's it. One thing I would say is I think community always is important. That's one of the things that I think this podcast manages to do, is bring different communities together and different people with different points of view. I think that's one thing that a lot of people have replied that they do appreciate the different approaches people have to some of these ideas, because they're, if you think just trying to match a computer to the real world, which is kind of what we were talking about today, that can get way more interesting than you think it could possibly be.

01:04:27 [CH]

Absolutely. All right, with that we'll say thank you so much Raul for coming on. This was a blast of a conversation and hopefully our listeners will agree. And hopefully maybe sometime in the future we'll have you back again to talk about what you've been working on since the last time we've had you on, All Things J.

01:04:43 [RM]

Now I have to work on something.

01:04:46 [CH]

Yeah, you know, you come on a podcast and you end up with homework, you know, that's what happens. All right, with that we will say, happy Array programming.

01:04:56 [ALL]

Happy Array Programming!

</details>
