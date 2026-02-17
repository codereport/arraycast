---
title: "Episode 110: Implementing Replicate"
date: 2025-07-19 00:00:00 +0000
episode: 110
buzzsprout-id: 18617017
keywords:
- array-programming
- array-languages
- apl
- k
- j
- bqn
- replicate
- copy
- primitives
- implementation
mp3-url: "/assets/audio/episode110.mp3"
episode-type: full
explicit: "no"
block: "no"
layout: podcast
excerpt_separator: <!--more-->
redirect_from:
  - "/episodes/episode110-replicate"
  - "/episode110-show-notes"
---
Implementing ReplicateWe do our first deep dive into implementing primitives by looking at Copy/Replicate
<!--more-->

**Host:** Conor Hoekstra

**Panel:** Henry Rich, Marshall Lochbaum, Bob Therriault and Adám Brudzewsky

---


## Show Notes

Array Cast -  July 18, 2025

Thanks to Bob Therriault, Marshall Lochbaum and Conor Hoekstra for gathering these links:

**[01] 00:00:40**

- [Henry Rich Episode #6 on The ArrayCast](https://www.arraycast.com/episodes/episode-06-henry-richs-deep-dive-into-j)
- [Henry Rich Episode #18 on The ArrayCast](https://www.arraycast.com/episodes/episode18-henry-rich-presents-j903)
- [Henry Rich Episode #48 on The ArrayCast](https://www.arraycast.com/episodes/episode48-henry-rich)
- [Henry Rich Episode #50 on The ArrayCast](https://www.arraycast.com/episodes/episode50-fold)
- [Henry Rich Episode #84 on The ArrayCast](https://www.arraycast.com/episodes/episode84-tacit6)
- [Henry Rich Episode #104 on The ArrayCast](https://www.arraycast.com/episodes/episode104-j96)
- [Henry Rich Episode #106 on The ArrayCast](https://www.arraycast.com/episodes/episode106-interpreters)
- [Dyalog APL](https://www.dyalog.com/)
- [BQN programming Language](https://mlochbaum.github.io/BQN/)
- [J programming Language](https://code.jsoftware.com/wiki/Category:Home)
- [APL programming Language](https://aplwiki.com/)
- [Replicate in APL](https://aplwiki.com/)
- [/wiki/ReplicateCopy in J](https://code.jsoftware.com/wiki/Vocabulary/number#dyadic)
- [APL\360](https://aplwiki.com/)
- [/wiki/APL%5C360Iverson Notation](https://aplwiki.com/)
- [/wiki/Iverson_notationBob Bernecky Episode #55 on The ArrayCast](https://www.arraycast.com/episodes/episode55-bob-bernecky)
- [I.P. Sharp Episode #91 on The ArrayCast](https://www.arraycast.com/episodes/episode91-ipsharpdoc)
- [Expand in APL](https://aplwiki.com/)
- [/wiki/ExpandNARS2000](https://aplwiki.com/)
- [/wiki/NARS2000Ken Iverson](https://en.wikipedia.org/wiki/Kenneth_E._Iverson)
- [Replicate in BQN](https://mlochbaum.github.io/BQN/)
- doc/replicate.html

**[02] 00:10:52**

- [Uiua Programming Language](https://www.uiua.org/)
- [Keep in Uiua](https://www.uiua.org/)
- [/docs/keepWhere in APL](https://aplwiki.com/wiki/Indices)
- [Omnibar Replicate table](https://omnibar.rubenverg.com/?s=replicate&ig=true&in=true&id=false&hid=true)
- [Hoogle Translate Page for Replicate](https://hoogletranslate.com/?q=25&type=by-algo-id)
- [APL2 Programming Language](https://aplwiki.com/wiki/APL2)
- [Indices in J](https://code.jsoftware.com/wiki/Vocabulary/icapdot)

**[03] 00:19:43**

- [Roger Hui](https://en.wikipedia.org/wiki/Roger_Hui)
- [Arthur Whitney](https://en.wikipedia.org/wiki/Arthur_Whitney_(computer_scientist))
- [Indices in Hoogle Translate](https://hoogletranslate.com/?q=18&type=by-algo-id)
- [Dzaima/APL](https://aplwiki.com/wiki/Dzaima/APL)
- [Replicate Operator or Function](https://aplwiki.com/wiki/Replicate#Operator_or_function)
- [?ngn/APL](https://aplwiki.com/wiki/Ngn/apl)

**[04] 00:27:55**

- [Multiple Personality Disorder](https://en.wikipedia.org/wiki/Dissociative_identity_disorder)
- [APL Plus Programming Language](https://aplwiki.com/wiki/APL*PLUS)
- [GNU APL Programming Language](https://aplwiki.com/wiki/GNU_APL)
- [Tacit Programming](https://en.wikipedia.org/wiki/Tacit_programming)
- [Trains in APL](https://aplwiki.com/wiki/Train)

**[05] 00:39:32**

- [Faster Population Counts Using AVX2 Instructions](https://arxiv.org/pdf/1611.07612)
- [Count Trailing Zeros Instruction](https://www.felixcloutier.com/x86/tzcnt)
- [AVX2](https://en.wikipedia.org/wiki/Advanced_Vector_Extensions#Advanced_Vector_Extensions_2)

**[06] 00:51:52**

- [X86 Parallel Bit Extract InstructionAVX512](https://en.wikipedia.org/wiki/AVX-512)
- [PDEP](https://www.felixcloutier.com/x86/pdep)
- [PEXT](https://www.felixcloutier.com/x86/pext)

**[07] 00:55:30**

- [Hacker's Delight](https://en.wikipedia.org/wiki/Hacker%27s_Delight)
- [Guy Steele](https://en.wikipedia.org/wiki/Guy_L._Steele_Jr)
- .

**[08] 01:00:34**

- [k Programming Language](https://en.wikipedia.org/wiki/K_(programming_language))
- [Kap Programming Language](https://kapdemo.dhsdevelopments.com/)
- [Kotlin Programming Language](https://en.wikipedia.org/wiki/Kotlin_(programming_language))
- [Elias martenson Episode #72 on the ArrayCast](https://www.arraycast.com/episodes/episode72-kap)

**[09] 01:12:34**

- [Contact AT ArrayCast DOT ComRust Programming Language](https://en.wikipedia.org/wiki/Rust_(programming_language))
- [Kai Schmidt Episode #77 on the ArrayCast](https://www.arraycast.com/episodes/episode77-uiua)

<details markdown="1">
<summary><strong>Transcript</strong> (click to expand)</summary>

Transcript

Transcript prepared by

Bob Therriault

Show Notes

Henry Rich

**00:00-00:24**

What I do is whenever I code an algorithm, I have an idea in mind of the speed I expect to get. And I always look at the generated instructions to make sure the compiler hasn't gone berserk. The compilers are fantastic now at code generation. They do occasionally, you can hit it with something they're not used to, and they go crazy.

Conor Hoekstra

**00:35-00:53**

Welcome to episode 110 of ArrayCast I'm your host Conor and today with us we have... actually we should have figured this out I think you might be a panelist this time not a guest but we'll get to introducing him in a second and we will do brief introductions from our regular recurring panelists we'll start with Bob then go to Adám and finish with Marshall. [01]

Bob Therriault

**00:53-00:58**

I'm Bob Therriault I'm a J enthusiast, and I'm very interested in what we find out about J today.

Adám Brudzewsky

**00:59-01:05**

I'm Adám Brudzewsky. I'm very excited for presenting APL here, but this is going to be awesome.

Marshall Lochbaum

**01:05-01:14**

I'm Marshall Lochbaum. I was introduced to J by our next panelist. Then I went on to work at Dyalog , and I have made BQN since then.

Conor Hoekstra

**01:14-01:21**

And I guess, yeah, we should let Henry, I think you're a panelist today, we didn't actually clear this up, but we'll let you introduce yourself today, seeing as I think that's the role you're playing today.

Henry Rich

**01:22-01:28**

I'm Henry Rich. I'm the current developer of the J Engine custodian and continuing developer.

Conor Hoekstra

**01:29-02:35**

And I believe this is the first edition of Primitive Talk. We talked about it over the last three or four episodes, and there had been some unofficial requests from listeners that reached out to me personally, and I think just via email, saying they enjoyed the deep dives, whether they were intentional or unintentional at the time, on just single primitives or single glyphs that might stand for two primitives. And today we are going to be talking about replicate slash copy modulo the name, because depending on the array language, it might have a different name. And, you know, even some of these, they kind of double as multiple algorithms in one, depending on the implementation behind the scenes. If you, you know, the dyadic version, your length of your shapes. Anyways, how do we want to start this? Do we want to throw it to our guest panelists? And then we'll go around and try and get coverage of all the different array languages. So I guess, Henry, we'll let you speak for J, and then we can get BQN comments, APL comments. I think we're going to try and cover k and q as well and figure out the name and implementation differences.

Adám Brudzewsky

**02:36-02:40**

Maybe we should give it like a historical perspective, where it started.

Marshall Lochbaum

**02:40-02:52**

Because, yeah, so you say multiple algorithms, but in APL 360, there was no replicate. There was a function called compress, and it was actually quite a while before replicate was introduced.

Adám Brudzewsky

**02:52-04:38**

Okay. So, I mean, should we start there then? Yeah. I think we should describe what it does, and then we can build on that. It doesn't matter really what the symbol or the name is, but we can see how they all kind of stem from there. And then I think we should take a slight detour to explain what q and k does, and then we can come back to actually discussing the primitives.

Conor Hoekstra

**03:06-03:21**

All right. Sounds like a plan. So who's – is it Marshall, Adám? Who's going to take the historical? Adám, maybe.

Adám Brudzewsky

**03:22-04:38**

Okay, I guess if I represent APL. So original, even Iverson notation had this notion of compress, which was applying a Boolean mask to some data. And so the ones and the zeros, the Booleans, they would then sort of squeeze out. Anything that corresponded to a zero would be squeezed out. Anything corresponding to a one would be kept. So in a way, it's also what we'd often call a filter, but it doesn't take a predicate. It takes the Boolean. And actually, original Iverson notation and carried over into APL has both a first and last axis. You can't really speak like that in the Iverson notation because there were only two axes, but like vertical, horizontal for matrices. And that was carried over in APL into a first and last axis and replicate. Well, it became replicate later, compress. Then, I don't know exactly who noticed that, But it was noticed that you could see the boolean also as a count. And so there was an extension made so that we look at the zero and one as counts. And that means you can have a larger than one value and you wouldn't get just one of the corresponding element or cell. You would get that many of them. So every count is that many and zero is just none of them.

Marshall Lochbaum

**04:38-04:53**

I can fill this in for you. It was  Bob Bernecky at IP Sharp. I don't know if it was like a flash of insight or kind of a slow process of, you know, figuring out what you want to do. But it was around 1980, I think, was the time of that.

Conor Hoekstra

**04:53-05:12**

Marshall beat me to it. But I was literally on the APL wiki because I recall going through the history. And I was like, this is actually explicitly mentioned in the history section. And right as you started talking, I had to pinpoint that it was, yeah, in 1980,  Bob Bernanky introduced the extension Replicate to Sharp APL.

Adám Brudzewsky

**05:12-05:19**

It doesn't mention. But you're right, it doesn't really say if that's something that people discussed and he presented it or what it is. We don't really, we could ask him.

Marshall Lochbaum

**05:19-05:25**

At some point, I was talking to Bob for some reason and Replicate came up and he said, well, this is my primitive.

Adám Brudzewsky

**05:25-06:39**

So everybody agreed that was an awesome idea. So that just went out to the various APLs and was adopted quickly. And then there was a further extension of it, which is sort of related to its companion function that we're not really going to cover here, I think, which is expand, which allows you to insert. It's the inverse of replicate. So a replicate takes out some elements. Of course, you can't really insert elements because they have been lost, but you could open up spaces in your array of prototypical values that would allow inserting the lost elements there. And that's what expand does. But somebody got the idea that you could use negative numbers and that I think it was in NARS as well. So it was shortly after the initial extension to replicate. And so negative numbers would be the number of prototypical elements or cells inserted at that position instead of an element. So Y2 would replicate something 2 times negative 2, which would spend that element, but put two prototypical slots in. I think that was also well-received and spread everywhere.

Henry Rich

**06:40-06:41**

Well, not into J.

Adám Brudzewsky

**06:41-06:43**

No, but not into J. No.

Marshall Lochbaum

**06:44-06:45**

Nor BQN.

Adám Brudzewsky

**06:45-06:47**

So we should say into all the APLs, I should say.

Henry Rich

**06:47-06:49**

I don't agree with that. J is an APL.

Adám Brudzewsky

**06:49-06:50**

Okay.

Henry Rich

**06:52-06:55**

The J developers probably can. Decided to use complex numbers.

Marshall Lochbaum

**06:56-06:57**

It's not in the standard, by the way.

Henry Rich

**06:57-06:59**

Which standard? APL standard, do you mean?

Marshall Lochbaum

**06:59-07:00**

The extended APL standard.

Henry Rich

**07:01-07:15**

Oh, okay. What you describe as a choice between copying and insertion. In J, you can do both because of the complex number. You can specify how many copies you want and then how many fills.

Adám Brudzewsky

**07:16-07:18**

Which order do they go in then? How do you know which one comes first?

Henry Rich

**07:19-07:44**

That is a very good question because you're fixed to the fills have to come second. And it means that you can almost do what you want, but you can't put fills at the very beginning of an array. And I've tried to figure out a good way to fix that. I haven't come up with it yet, but it isn't used very much at all. So I'm considering it not worth fixing.

Bob Therriault

**07:44-07:53**

So if you had a complex number that was 0J6, it's not going to put six fills and no initial?

Marshall Lochbaum

**07:53-08:04**

It will, but it'll use up an argument element. So you'd have to put some dummy value on the right argument, which is not that bad, but it's just like you don't really want to do it. It's inelegant.

Adám Brudzewsky

**08:05-08:14**

Does the J copy use negative numbers at all? Yeah. So why not just say that if the complex part is negative, it goes in front instead of after? You don't need zero.

Henry Rich

**08:15-08:27**

Yeah, you could, but suppose you want before and after. Yeah. You'd pretty much, you'd have to. Yeah, that fails in most general.

Adám Brudzewsky

**08:27-08:43**

Yeah, I mean, Ialso think that using complex numbers like that, it's just that it's a shortcut for giving a number pair, right? But it really has nothing to do with it. And I know J does this every once in a while using complex numbers like this. But I mean, it could have just been a tuple, right? It could have just been boxes.

Henry Rich

**08:44-08:45**

I really suppose.

Adám Brudzewsky

**08:45-08:57**

And if it had been a two element box, then it could have been the current real and complex part. And if it's a three element box, then it's how many before, how many of the element itself, how many after. I mean, it could have been. Anyway.

Henry Rich

**08:57-09:13**

But I would hold that if you have to change a number to a boxed thing, you're precluding it from use in large applications. And that's just poorly specified. It's too inefficient to use on a big job.

Adám Brudzewsky

**09:13-09:19**

Okay. Anyway, and then for BQN, Marshall, you want to fill us in on the situation? On the fills, I mean?

Marshall Lochbaum

**09:19-09:31**

I just threw that whole thing out. I said, you know, there's no really great way to wrap this into a primitive. Structural under does fills all right. So that kind of covers the space of expand, too.

Conor Hoekstra

**09:31-09:41**

I was going to, not to interrupt, but I was going to ask for clarification when you guys started talking about the negatives and complex numbers and fills. Are we talking about replicate here? Are we talking about expand that is sibling?

Adám Brudzewsky

**09:41-09:44**

No, no, only replicate. Expand will be a different episode.

Conor Hoekstra

**09:45-09:56**

Okay. Because I was saying, I don't recall this being like a feature of BQN's replicate. And so this fill extension doesn't exist on all replicates across the array languages.

Marshall Lochbaum

**09:56-10:31**

No, and not even all APLs. So there's also on that replicate page, there's a table in the extension support section that says, well, and you've got these competing NARS and APL2. So APLX is interesting in that it implements both the NARS version and the APL2 version. Because the left argument can't have the same length in those two extensions. So it checks the length and decides which one you must admit. But then a lot of other dialects, most of the mainstream dialects do one or the other.

Adám Brudzewsky

**10:31-10:33**

I haven't really explained what the difference is between those two.

Conor Hoekstra

**10:34-11:01**

I feel too, I put the cart in front of the horse. We will, this is our first primitive talk, folks, so I'll make sure not to do this next time. The first thing I'll do for next primitive talk is we will name them, because I realize probably our Uiua listeners, [02] if they're Uiua only, might be a bit confused. So in J, it's called Copy. In the APLs, you know, APL, tiny APL, it's called Replicate. Some people refer to it as Compress, or I guess that's the history behind it.

Adám Brudzewsky

**11:02-11:10**

You refer to it like that if you use it as a filter like that. Right, often we've given names of primitives by their usage to make it easier to understand. English is a terrible language. But

Conor Hoekstra

**11:10-11:20**

Uiua has a different name for this. They call it Keep. And I actually don't know if k and q, do they have an equivalent of this or is that a different story that we'll touch?

Adám Brudzewsky

**11:20-11:57**

No. So the way it works there is that when they designed the language implementation-wise, they rejected the idea of bit booleans. And therefore, there's no real reason to prefer working on bitmasks. So instead, they tend to work on indices. Therefore, the replicate function is completely gone, and they just use where with indexing. So if you take the Boolean mask, or not Boolean, one that has numbers higher than one, and you do a where on it, you get the indices corresponding to the ones. If you've got higher than one, you get that many of that index. If you use that to index into the array, then it's effectively the replicate.

Conor Hoekstra

**11:58-12:17**

Right. And that actually makes a lot of sense when you think getting back to BQN is that that is the overloads indices and replicate on the primitive there because they're very connected if you don't have replicate. Anyways, I did interrupt you, Marshall, when you were talking about BQN. So back to you.

Marshall Lochbaum

**12:19-13:14**

I was getting to it. Yeah, I think that that idea of saying that replicate and indices are connected and they should be on the same glyph, which I do use the slash for. that's what I consider at least an improvement BQN makes and that's the big change other than that as I said I throw out the whole idea of trying to add fills and stuff and there's one little minor thing which is that normally replicate you give it a list on the left and that just corresponds to the first axis of the right argument but you can actually also pass in a list of lists and then each of those corresponds to a different axis so if you wanted to if you had a table and you wanted to take you know every other column and every other row you could do that using replicate by with two lists that go one zero one zero so each of those acts on one of the axes

Conor Hoekstra

**13:14-13:15**

interesting

Adám Brudzewsky

**13:15-13:30**

Right I should I should mention this as well that that sort of requires BQN's array model because one thing we haven't mentioned is you don't have to have a list on the left of a replicate you can also have a scaler which will then...

Conor Hoekstra

**13:30-13:55**

I was gonna I was gonna bring this up and this is the confusing part is because if you go to google translate I have repeat for like Julia and c sharp but that only corresponds to like a subset of replicates functionality where it's only a scaler there so really replicate is both replicate and what many languages call repeat where you just have a number and then and that's actually a very common use of that.

Adám Brudzewsky

**13:55-15:04**

It's very common to conditionally append something, for example. So you might just have the thing you want to append, but then compress it away if the condition is false. So for example, let's say that I'm constructing a text that needs to go on some interface. So I write n items. So I format the number n, I concatenate that to the word item, but then I conditionally want an S. So then one way I could do that is I could do, in parentheses, N is greater than 1, end parentheses, slash, quote, S, quote. So I compress away, the S becomes an empty vector if we only have one. You might even want to just do that the N is different from one so that when it's zero items, you also get the S like that. Of course, when it's a scalar you're adding or a single character like S, then you could also use reshape or take. But that could be other phrases and things that you want to conditionally add. And this is a very common way to do it.

Marshall Lochbaum

**15:04-16:00**

Yeah. So you might actually use this. You have this thing where you can use just one number. And I mean, you can use it with like two or three. And so it'll copy every value two times or three times or whatever. So one thing you can do in BQN is actually you can use this multiple replicate thing together with that. So if you have a list of not a list, but of like enclose three and enclose three. So that's a list of two boxed or enclosed. Not really. I mean, BQN doesn't actually have boxes, but a list of two scalar arrays that contain numbers. Then it knows because the depth is two, it knows to use this nested mode. And so it applies each of those to an axis. And like if you've got an image and you want to scale up every pixel, scaling by three along both axes or both of the height and width, at least, that turns each pixel into three by three. So that's a good way to scale up. But if you tried this in APL.

Adám Brudzewsky

**16:00-16:08**

Yeah. Just a question, Marshall. Shouldn't you be able to like doubly enclose the scaler and that would automatically map it over to all the axes?

Marshall Lochbaum

**16:09-16:21**

Well, I mean, you could define it, but it's also pretty easy to do because you can just take the shape of the array and do the scaler, enclosed scaler each on the shape, and then you've got it automatically.

Adám Brudzewsky

**16:22-16:36**

Anyway, so let's go over to APL where there's a problem because we don't have enclosed simple scalers. So that array that you would need as left argument simply cannot exist. It can work if at least one of the accents.

Marshall Lochbaum

**16:36-16:41**

You do have enclosed simple scalars, and the way you write enclosed in three is just write three.

Adám Brudzewsky

**16:41-16:46**

Okay, but because there's no distinction, right? Let's say we have a two-by-two matrix.

Marshall Lochbaum

**16:46-16:46**

Yeah.

Adám Brudzewsky

**16:47-17:08**

Then one to replicate this matrix is indistinguishable, right? Wanting to replicate one of the first row and two of the second row is indistinguishable from wanting to replicate along the rows with one and along the columns with two. Because it doesn't matter how much you try to enclose a simple scalar in APL2 style APL, nothing happens. It just kind of floats up again. There is a way around this, which I believe I've modeled in things like extended Dyalog APL, which is there is often a leniency in APLs where they allow singletons or at least one element vectors to behave like they were scalars. And that is the case for replicate. So if you use a one element left argument to replicate, it will still work against all the cells on the right argument.

Marshall Lochbaum

**17:08-17:15**

Yeah, you could do a ravel each there.

Adám Brudzewsky

**17:15-18:08**

Yeah, exactly. You could do a ravel each instead of an enclosed each, and that would work. It's a little bit ugly, but it could be done, and I think it should be done because I think it's a really cool thing to be able to replicate along multiple axes together. We even have first and last axes replicate, so you could do all the leading axes and all the trailing axes. You didn't need the rank operator so much. Yeah, I think that covers just the description of the perimeter, right? There's maybe something to be said about...

Marshall Lochbaum

**18:08-18:10**

We didn't actually say what indices is, did we?

Adám Brudzewsky

**18:11-19:28**

Indices? Where? Yeah. So maybe, again, historically, very quickly it occurred in APL programs that the phrase slash, which is replicate, iota, which is the index generator, row, which is shape, became an idiom, or we call it, or it became a phrase that people just read as a whole thing, right? So what does that do? If you think about it, let's just do compress it first. So we have a Boolean on the left. Boolean compress the indices of an array, right? Iota row, or the indices of the shape of an array, that just enumerates all the cells or enumerates all the the element. And then if you use a compression that effectively selects certain indices, the indices corresponding to the ones in the Boolean. So this phrase actually is a translation from a mask format to indices format. Or in other words, it tells you where the ones were. And this is such a common thing. And of course, these have to conform. So you really don't need two arguments. You just need the Boolean mask. That it was a candidate for becoming a primitive, and it did become a primitive eventually in Dyalog APL, and it had been already a primitive in other...

Marshall Lochbaum

**19:28-19:44**

Yeah, well, I think the cause in Dyalog was probably... I'm not totally sure about this, but I think was because Roger came from J to work on Dyalog, and he'd added it in J, and I know actually he added it because Arthur Whitney told him to. [03]

Adám Brudzewsky

**19:45-19:53**

I mean, I don't know if that really fits chronologically because maybe. It's too late to ask him.

Marshall Lochbaum

**19:53-20:10**

I don't have positive proof, but there was a statement somewhere that I read that Roger said, well, like early on in J's development too. This was not long after the fact recollection. There's something where he says, oh, yeah, I added capital I dot because Arthur said this is a good idea.

Adám Brudzewsky

**20:10-20:18**

Oh, yeah. Oh, yeah. I believe you. But whether that's the reason why he added it to Dyalog APL, I'm not sure.

Adám Brudzewsky

**20:23-20:26**

Well, I mean, ultimately, he added it to Dyalog because he thought it was a good idea.

Marshall Lochbaum

**20:26-20:28**

Yeah, yeah. But, I mean, it was broad consensus. I mean, the reason for that is experience using it in J.

Adám Brudzewsky

**20:28-20:50**

Exactly. And everybody agreed. Everybody saw this idiom. And even a Dyalog sentence is an idiom. Slash a Iota row is a phrase that the interpreter will recognize and doesn't actually build all the indices first. It just directly translates the Boolean mask to indices. So it's definitely a top candidate to become a primitive, which it became version 16.

Conor Hoekstra

**20:51-22:13**

I didn't say, but I wanted to when... Was it Adám that you said we haven't described what indices are? One of us, it was either you or Marshall. And in my head, there's this Instagram guy that his response is he hears something he doesn't like and he goes, a la poubelle. And when you said, if we don't, we didn't describe indices, if you've made it 110 episodes and you don't know what indices is, a la poubelle. Anyways, it's, I might work that in for like the next 50 episodes. It makes my fiance laugh quite a bit. So I've been saying it quite often. Anyways, I'm screen sharing. This is one of the nicer Hoogle translates. Now we're not going to talk about indices anymore, but it has almost something different for like every single language. It's Iota underbar for the APLs. It's Slash for BQN, which we already mentioned. It's capital I dot for J, and it's ampersand for k, and it's just called Where. So one of the more, I mean, kind of sad that we don't have any unification, but it does bring me great joy when the diversification is at like 100% and not a single. I mean, I guess the APLs all share the Iota underbar. But yeah, as opposed to, I guess we didn't really talk about the symbols. It's the Octothorp or Hash and J. It's the slash in both APL and BQN. So there is a bit more agreement. And slash bar actually is more what it is because

Adám Brudzewsky

**22:13-22:21**

And slash bar actually is more what it is because slash bar, which was originally double slash in Iverson notation, is the leading access version.

Marshall Lochbaum

**22:21-22:38**

Okay, okay. Yeah, so maybe we should mention this whole issue with the slashes. What Dzaima APL does actually is to make the slash bar replicate only and the slash be reduced. Because, yeah, specifically the issue with the slashes is that replicate and reduce both use slash.

Conor Hoekstra

**22:38-22:38**

Oh, interesting.

Marshall Lochbaum

**22:39-22:47**

Replicate is a function and reduce is, well, replicate is usually implemented as a function. It's naturally a function.

Adám Brudzewsky

**22:47-22:52**

Oh, no. Hold on. Are you sure? Are you sure? It's usuallyimplemented as a function? I'm not so sure.

Marshall Lochbaum

**22:53-22:55**

Well, yeah, it does depend on your metrics.

Conor Hoekstra

**22:55-22:58**

A perfect transition into implementation details now.

Adám Brudzewsky

**22:58-23:30**

No, it's not an implementation detail, Conor. That's a syntactic detail. It's an actual syntactic role because it makes a difference. If you have a vector on the left, 1, 2, 3, and you do replicate each on, say, quote, ABC quote, right? If replicate is a function, then 1, 2, 3, replicate ABC is A, B, B, C, C, C. Are you with me? If replicate is a monadic operator, which is the alternative, then the entire array, 1, 2, 3, is bound as the left operand to replicate.

Conor Hoekstra

**23:30-23:37**

Wait, wait, wait, wait, what? A monadic operator. So we're talking about like a...

Marshall Lochbaum

**23:37-23:42**

Well, it's like reduce. It's just the version of reduce that instead of giving it a function, you give it an array.

Conor Hoekstra

**23:42-23:51**

Yeah, it's reduce, but with a... But what's the function that... Yeah, what's the function that this operator takes as an argument?

Adám Brudzewsky

**23:51-24:02**

No, it doesn't. It takes an array. There are operators that just takes arrays, like the constant operator and the at operator. And lots of other operators only take arrays as operands. Yeah, not many monadic operators do that. Or not only, but can take.

Conor Hoekstra

**24:03-24:13**

I was going to say, this is my mental model. I mean, I agree that what you're saying is true, but my brain is like, well, that's not the way I think about operators, though. They typically are like higher order functions. So you're saying it's...

Henry Rich

**24:13-24:15**

You can take anything anybody wants.

Adám Brudzewsky

**24:15-24:26**

Yeah. I think of them as function factories. You give them some raw materials and they spit out a new function. And the parameters you give them can either be functions or arrays, or a mixture.

Conor Hoekstra

**24:28-24:37**

Okay, but so you're saying if replicate is a monadic operator, its argument is the array on the right? It has only one argument.

Adám Brudzewsky

**24:37-25:23**

Its derived function is the right argument. And on the left, you have an operand instead. Okay, but bear with me. 1, 2, 3, replicate ABC is A, B, B, C, C, C. Doesn't matter whether the replicate is a function or an operator. So far, so good. Now let's do 1, 2, 3, replicate each ABC. Let's start off with replicate being a function. So clearly we pair up 1, replicate A, 2, replicate B, 3, replicate C. We're going to get a nested result. The first element of the result is going to be A, or a single vector of A. The second element is going to be the vector BB. And the third element is going to be the vector CCC.

Conor Hoekstra

**25:24-25:25**

I follow you.

Adám Brudzewsky

**25:25-26:15**

If replicate is an operator, then we have got 1, 2, 3 replicate as a derived function. Because 1, 2, 3 is the upper end. It gets bound strongly to the replicate. And we apply that function, 1, 2, 3 replicate, which is equivalent to 6 replicate, by the way, because we're going to apply it on scalars, on each of the letters A, B, and C. So we get 1, 2, 3 replicate A, 1, 2, 3 replicate B, and 1, 2, 3 replicate C. Now, 1, 2, 3, replicate A, because there's only a single scale on the right, is 1, replicate A, 2, replicate A, 3, replicate A, 2. You just sum up the 1, 2, and 3 to get 6. Exactly. So that's 6 As, and then we get 6 Bs, and then we get 6 Cs. So whether or not a replicate is a function or an operator makes a difference as soon as you go to nested arrays and each and so on.

Marshall Lochbaum

**26:15-26:22**

If the implementation allows you to do that, yeah. In ngn/APL, it just gives you an error because it doesn't like parsing that sort of stuff.

Conor Hoekstra

**26:23-26:42**

Bob's excellent editing skills are probably going to silence my sigh. So I would just like to vocally, you know, using words that can't be silenced, say that in the midst of Adám's description of a 1, 2, 3 replicate on a scalar, which is effectively the same thing as a 6 replicate on a scalar, I did have an audible sigh that you may or may not have picked up on.

Bob Therriault

**26:43-26:50**

I'm not sure I heard it. So if we didn't hear it, I can't put it in. But it's noted. It's noted.

Conor Hoekstra

**26:51-27:01**

Yeah, yeah. Well, I was going to say, I don't even know if it was picked up by my mic. So I just wanted to go on record that I was sighing.

Adám Brudzewsky

**27:01-27:09**

So the operator form of replicate is somewhat less useful. You generally do not want the 1, 2, 3, replicate on each.

Conor Hoekstra

**27:09-27:10**

Henry wants to say something.

Henry Rich

**27:11-27:20**

When you say operator form in J, it would either be an adverb or a verb. that would settle the banter.

Adám Brudzewsky

**27:20-27:22**

So too in APL. It's either a verb or an adverb.

Henry Rich

**27:23-27:24**

So which is it?

Adám Brudzewsky

**27:24-27:25**

Yes, exactly.

Henry Rich

**27:25-27:27**

Let me just answer the question. Which is it?

Adám Brudzewsky

**27:27-27:56**

Yes. Yes. It is something. So it is in a class of primitives that are nicely called hybrids, hybrid function operators. In the old days, when multiple personality disorder was considered a form of schizophrenia, it became the custom for APLers to call these replicate and related ones, call them schizophrenic primitives. [04]

Henry Rich

**27:56-28:03**

But we have to parse this, and it has some rule by which it decides what to do. What's the rule?

Adám Brudzewsky

**28:03-28:59**

Yeah, so that's very interesting, right? What exactly do we do? First, let's say the actual standard does not explain what to do in this case. It explains that replicate is as a function. It explains reduce, which uses the same symbol, as an operator, and it does not address what to do with this problem. APL2 went with a pure operator. So that means that one, two, three, replicate each is not very useful. You'd have to wrap it in a function, and without defense, it's sort of awkward, but you could do it. APLX, APL+, followed suit entirely for APL2. APL plus tried to find a way around this problem and originally introduced a syntax where if you parenthesize the primitive, it becomes a function. Otherwise, it behaves like an operator, which is a bit odd because normally when you parenthesize something, nothing happens.

Henry Rich

**29:00-29:01**

That's just a kludge, right?

Adám Brudzewsky

**29:02-31:51**

Yes, exactly. APL plus then gave up. They eventually removed that. So there's the setting of how compatible you want to be with APL2. If you want to be as much compatible as possible, well, then that's not available anymore. However, they just added a system function. They just added a named function, quad repl, which is replicate as a function and not as an operator, which is, again, sort of dirty to do that. But Dyalog APL and GNU APL managed somehow to implement this according to spec, where if you have an array on the left, then it is a function. And if you have a function on the left, then it is an operator. It's sort of a syntactic mess. It generally works the way you expect it to. Replicate each just does what you want. It does occasionally bite you. If you have a function on the left that represents an array, or if for whatever reason, you don't need the array on the left. So if you do like a self-replicate on something, for whatever reason, then there is no argument on the left. So you'd like replicate, selfie, or reflexive, or whatever you want to call it. and then an argument. And then you want to take the result of that and apply some other function to it, then things break down because the function could just be a minus, right? So in APL, we do minus slash selfie on another array. And then the slash will capture the minus as its operand. And well, things go really bad from there. That's bad. And also in tacit programming, things tend to go bad because you have a train and then you have many functions and the function on the left of the replicate is supposed to produce the left argument to replicate. but because they're adjacent to each other the replicate access and operator binds it so that's a bit of a mess and finally uh it is a useful thing if you have a two element vector of say a mask or some counts and some data you might want to insert replicate between those two elements and being that they are the same symbols and slash in APL's then you would write slash slash right so that's a that's a replicate reduction which is fine it sort of looks a bit odd but it's fine. The problem is in APL, that also implies an enclosure because reduce always encloses. So the next step, almost always after that, is you want to disclose. So you tend to write the phrase disclose, slash, slash, and it doesn't work because instead of getting the disclose of a replicate reduction, you now get a pick, which is the authentic form of disclose, a pick reduction reduction, which is absolutely not what you want. Or at least very, very rarely. I don't remember. I can probably construct some case where it will do something and not error, but I've never actually needed that. So it's a bit of a mess.

Bob Therriault

**31:51-31:59**

So when you've got that slash slash, the right slash is a function and the left slash is an operator?

Adám Brudzewsky

**32:00-32:43**

No. The right one is an operator because it has something on the left. And the left one is hybrid. We don't know until the last moment what it is. It's just a call time. And there are other weird effects of this because you can ask for the syntactic class of things and then the interpreter can't determine it until you actually use it. So it will claim it's a function, but then you can use it as an operator or you can take a slash as an operand. And we know operators can't take operators as operands, But you can give a slash as operand because it will then be a function temporarily until it's inside the operator. And inside the operator, you can then use it as an operator because it's just slashing. It does whatever you want of it.

Conor Hoekstra

**32:44-32:51**

You've got to be careful, Adám. This might be the last time Henry ever comes back for a primitive talk or ever attends because it looks like he's about to have an aneurysm.

Henry Rich

**32:51-33:13**

Well, no, I do want to be on record that all this nerdy laundry is part of APL. I guess Ken saw it all coming and he decided to make Sharp APL copy a verb and not try to overload it with the reduce function. If you do that, everything fits together pretty well.

Marshall Lochbaum

**33:13-33:15**

Well, I think he only fixed it in J.

Bob Therriault

**33:16-33:19**

While you were describing that, I was thinking, and you guys can actually make this work?

Marshall Lochbaum

**33:19-33:21**

Mostly. It always does something most of the time.

Adám Brudzewsky

**33:24-33:39**

Yeah, it might error, but yeah, it tends to work. In most cases, it's not actually a problem. It's already a problem. In most common cases are this slash slash thing, which occurs in like one single thing that you might do.

Marshall Lochbaum

**33:39-33:40**

And then the trains, the trains that occurfairly often.

Adám Brudzewsky

**33:41-34:59**

If you use trains much, it's really a hassle. And our CTO for a long time, he was like kind of dismissive about this problem. and then a couple of us pushed him to try out some trains more. And then he realized that, oh, when you do tacit programming, which he questions the value of, but if you do tacit programming, then yeah, you do hit this. So there are some mitigations for that. Often you can use that top operator and that sort of takes care of it because if you have the slash as the right operand, it will act as a function no matter what. Especially now with the behind operator, it takes care of a lot of the cases where you otherwise bump into this. Because very often you want a predicate providing the left argument to the replicate, and then you just want the original data as the right argument. So instead of writing as a three train predicate replicate and identity function, you can now write it as predicate behind or before if you want replicate, and then things just work fine. But there is the possibility, of course, of adding a new primitive or primitives to replace the function functionality of the slash and just sort of forget about slash ever being a function, just treat it as the operator, just treat it as reduce, and then use the new symbols for that. So there's a way out.

Henry Rich

**35:00-35:01**

Yeah, that would bring you up and would save. TODO

Adám Brudzewsky

**35:01-35:35**

Yeah, exactly. So a candidate symbol for that would be like the double slash going back to old Iverson days. That's what he actually used for first access replicate or it was compressed at the time. So there are some possibilities. But it's also expensive because then maybe you also want the last axis one. And if you're doing this, maybe you should do it for expand as well, which has the same sort of issue. So then we need four new primitives to get around the syntactic problem. Yeah, APL has some luggage. I'll be the first to admit that. Still the most beautiful though. Warts and everything.

Henry Rich

**35:35-35:37**

Some find warts attractive. TODO

Conor Hoekstra

**35:35-35:41**

I was going to say, should we follow up that? I don't know what the word is to use.

Marshall Lochbaum

**35:43-35:46**

This is one opportunity to leave it tacit

Conor Hoekstra

**35:49-35:59**

(Laughs) and yeah get a description of J's copy or or BQN's uh replicate I imagine does not have as much history or baggage maybe we'll choose that word as APL's replicate well.

Marshall Lochbaum

**35:59-36:02**

I mean we described him didn't he

Adám Brudzewsky

**36:02-36:05**

There's nothing to say really they just don't yeah they just don't have it

Marshall Lochbaum

**36:05-36:08**

Yeah I mean their functions they well...

Henry Rich

**36:08-36:14**

Yeah we don't have the problem of definition but the implementation is still interesting.

Adám Brudzewsky

**36:14-36:17**

Yeah, you want to segue to implementation now? Describe what they do.

Henry Rich

**36:18-39:15**

Yeah, it's almost trivial. You say X sharp Y. Each item of X tells how many copies we make of the corresponding item of Y. But the implementation is surprisingly large, really. In J, there are three separate cases. One is when X is Boolean, and that's a mask. as you've been talking about. The second is when X is an integer, and then you've got possibly more than one copy. So Boolean, you either keep the item or not. With integers, you have the option of keeping a certain number of copies of it. And the X can also be complex, which has this addition of fill. Well, I think the first thing to note is the only one of these that people use much at all is the Boolean version. So the integer and complex versions are implemented with the usual care, but without too much worrying about the individual machine cycles. So if you have Boolean X, well, what special cases are exactly as Adám said? Zero and one are both interesting. Zero returns an empty. One returns the wire argument unchanged. And so it's important to first cleave those off as special cases so that they take very little time. If X is an array, well, now there are a couple of questions that really you have to answer before you even start thinking about this primitive. How do you represent Booleans? Are they bit masks or are they individual bytes? And you can make an argument either way. The original implementation of J stored each Boolean in a single byte. And that's the way it still is. You might say, well, that's going to be wasteful of space. And that's true, it is. But in this case, where the X argument is so much shorter than the Yargument, the amount of space lost is not particularly important. And the first thing you have to do when you do this primitive is count the number of ones in X  So you have to count the number of bits, which is easy. With bitmasks, with individual bit booleans, it's easy if you have an instruction to do that. And if not, it takes a fair amount of time. I'm saying on the order of six or eight clocks per 64 bits. But nowadays, we have the advantage that you can process 64 bits per clock cycle, even with byte booleans. By using 256-bit loads, you can count the number of ones in a bit vector as fast or faster than if it were packed bits. So that greatly reduces one of the arguments that are advanced for having bit billions.

Marshall Lochbaum

**39:15-39:53**

Yeah, I don't think you can say faster. So you were talking about the pop count instruction for bits, but there is actually a method using vector instructions. There's a paper on this, something along the lines of counting bits faster with AVX2 than pop count or something. It's a very straightforward title. [05]  And it's a pretty tricky method. You have a pre-computed vector that tells you for each possible set of four bits what the count is there. And then you use shuffle instructions to select from that vector. And then you can add up those counts. And I'm pretty sure that's faster than just summing.

Henry Rich

**39:53-39:53**

Right.

Marshall Lochbaum

**39:53-40:00**

I mean, because the bandwidth you use is so much smaller. I don't think it could really be any slower than summing full bytes.

Henry Rich

**40:00-40:03**

Well, summing the full bytes. Again, you get 64 bits per clock cycle.

Marshall Lochbaum

**40:04-40:05**

Yeah, I mean, that's still very fast.

Henry Rich

**40:06-40:08**

Yeah, that's the thing.

Marshall Lochbaum

**40:08-40:38**

One of the things about bit booleans is that, like, yeah, the algorithms are eventually faster if you know how to do them. most of the time, but they're also a lot harder. And it only really matters if you're working mostly just with Booleans, because if you do all this super fast stuff on Booleans, and then at some point in the calculation, you switch over to eight byte floats, it's like that just blows everything else away. All that matters is how fast you worked with the...

Henry Rich

**40:38-43:03**

Yeah, exactly. Yeah, that greatly reduces the gain from going to bit booleans. So anyway, so in J, we stayed with byte booleans, and I'm okay with that. The second decision you have to make up front is, are you going to support modification in place? Are you going to allow X sharp Y to produce its result in place writing over Y? I would say it's really vital that you support in place modification for all arithmetic and this too, because adding an extra memory argument is very wasteful of cash bin. If the operands get big, it can take two or three times longer to take X plus Y producing Z rather than X sharp Y producing a modified Y.  So now we're down to X sharp Y possibly in place. And there are, in our implementation, three different paths that are taken. The first thing you do is find out how many ones there are in X. And then if it's mostly zeros, the important thing is to skip through the bits as fast as possible. Skip over the zeros. If the bits are mostly ones, it's almost all ones, then you want to shift away. You don't want to process each one bit independently. You want to find sequences of one bits so that you can, instead of copying each item, you can copy a burst of items at once. And in the middle, you've got the case where you've got a mixture of ones and zeros, and it's important to process those as quickly as possible. This is similar to what we talked about before, where minimizing mispredicted branches is very important in that middle case. I was surprised when I measured this that even when you have mostly ones, unless you get to more than 85% ones, there is not an advantage for finding long bursts of ones and converting them to a single memory copy. at least using the methods that I used. But still, that does happen.

Marshall Lochbaum

**43:03-43:21**

Yeah, I mean, in BQN, it looks like we switched over. I mean, it's over 95% is where we cross over. Although we recognize runs of ones, but we also try to recognize runs of zeros. So maybe if you were just dealing with the case with few zeros, you could be a little faster.

Henry Rich

**43:21-43:28**

Yeah, I handle both of those. Look for runs of zeros. When you hit a run of ones, when you hit a one...

Marshall Lochbaum

**43:28-43:31**

Yeah, so you just detect switches. That's probably about the same.

Henry Rich

**43:32-44:00**

Take the bits and take 64 bytes, convert them into 64 bits, and analyze that for runs of ones. But the important thing, well, in the middle case, where we've got a mixture of ones and zeros, it's very important that you use the count trailing zeros instruction. that you do not look at one bit and either copy it or not.

Marshall Lochbaum

**44:00-44:00**

Yeah.

Henry Rich

**44:01-45:05**

Because that would lead to a pipeline break every time you mispredict that branch. And these are data dependent. So there's a good chance that there's random data. And if you branch on each bit, the time will be totally dominated by the time of the mispredicted branches. So what you have to do instead is fill a 64-bit register with the mask, and then in the loop, you look for the lowest set bit, which you can do with a single instruction. All the machine architectures have an instruction that will do that. And once you find that bit number, then you can turn that bit off, use the number to copy an item, and repeat the loop without having any – The only conditional branch you'll have is when the register goes to zero, you're done. Well, that's going to be one misdirected branch for every 64 bits of input, rather than one misdirected branch for every, well, possibly for every bit in the mask.

Marshall Lochbaum

**45:06-45:18**

So now, because you're using byte Booleans, you can start that 64-bit region wherever you want. Do you take advantage of that? So that's an issue with bit Booleans. you can only start at a particular byte and you couldn't.

Henry Rich

**45:19-45:31**

Oh, yeah, that's right. Well, I think there's a problem with bit Booleans generally that a memory address is not enough. You have to have a memory address plus something else, which does complicate a lot of interfaces.

Marshall Lochbaum

**45:32-45:58**

Yeah, and so what we usually end up doing is working on algorithms that just work with aligned data and find ways to just deal with things directly where they are instead of shifting them over. And this is kind of also, that sort of strategy tends to work better with vector registers too, especially with AVX2 where you have the two lanes for each register and the instructions to cross between lanes are very expensive.

Henry Rich

**45:58-46:02**

Well, they're not all that expensive. When you say lanes, they're...

Marshall Lochbaum

**46:02-46:04**

Yeah, well, they have a much higher latency.

Henry Rich

**46:04-46:07**

Well, they have a three-cycle latency.

Marshall Lochbaum

**46:07-46:08**

Yeah, that's a lot of cycles.

Henry Rich

**46:11-46:13**

As long as it's not a carry dependency, it doesn't matter much.

Henry Rich

**46:14-48:12**

Yeah. If it's in a pipeline, it just means the final result is delayed two cycles. But I can still stack the requests in one per clock cycle. Like, for example, a thing that you would not want to do is if you had a six, the overall algorithm I described, I have a bit register, and I find the index of the lowest bit. Now, it would be tempting, and I know it's tempting because I made the mistake the first time I implemented it. It's tempting to say, okay, I found the lowest bit. Now I'll shift the register by that many bits and repeat. But that means that the loop, the carried dependency is you've got to find that lowest bit, which takes three cycles, and then shift. So that's four cycles before you can use that register again to find the next bit. If you do it the other way I described, you can find the lowest bit and then clear the lowest bit, but that doesn't require knowing where the lowest bit is. You do that by anding the register. You take the register and it with the register minus one, and that turns off the lowest bit without you ever knowing which it was. And in fact, under AVX2, under the modern Intel instructions, there's a one instruction variant that the compiler will find. And there, even though it takes three cycles to find the lowest bit, I can make a request every cycle. So the latency doesn't cost as long as I'm not looking at, I'm not using the resulting instruction that has latency. About the alignment, what I've found, and if there are any listeners out there who can amplify on this, I'd love to hear from it. It seems to me that unaligned stores of vector arguments are pretty expensive.

Marshall Lochbaum

**48:12-48:14**

Not like generally, not if they don't overlap.

Henry Rich

**48:14-48:18**

Well, I mean, they're going to overlap because you're doing them in series. Well, so I guess that's your problem. Well, yeah. Okay.

Marshall Lochbaum

**48:18-48:21**

Well, so I guess that's your problem.

Henry Rich

**48:21-48:23**

Well, yeah. Okay.

Marshall Lochbaum

**48:23-48:48**

It's not a problem with the alignment per se. It's a problem with not being able to do store forwarding, I think is more the issue. Because if you store something, if you have a single value, and you store it, and immediately something else reads it back again, there's a store forwarding path that it'll still go to memory, but the read won't touch memory. It'll kind of grab the value while it's in process.

Henry Rich

**48:49-49:03**

Right. The read can set itself to the write buffer. As far as I can tell, write buffers are not coalesced at any time. So if I store two consecutive values, I'll take two write buffers, even though they could be combined.

Marshall Lochbaum

**49:03-49:23**

Yeah, and if they overlap, I think it's actually dependency resolution is what the issue I'm talking about, or the issue you're running into is more. At some point, the hardware just can't keep up with a bunch of writes that all overlap because it needs to figure out what the final value is going to be. And it's really designed to work in this out-of-order paradigm.

Henry Rich

**49:24-50:05**

Right. anyway so so what I find when and all the arithmetic that the JE does you can't you have to decide what you want to have a line because you know the different arguments can have different alignments we make sure that the the argument we store to is aligned on a cache boundary and let the others fall where they may and that seems to work pretty well that the hardware handles unaligned loads just about as fast as aligned loads. And there's a penalty for unaligned stores, so we avoid having unaligned stores. But it means that we can handle these unaligned booleans without really, we don't have to worry about it.

Marshall Lochbaum

**50:05-50:12**

Yeah, because you're just reading from the booleans generally. And I guess you write bit booleans. That's the whole packing things into 64 bits deal.

Henry Rich

**50:13-50:15**

Well, no, I don't write them out. I use them internally.

Marshall Lochbaum

**50:15-50:17**

Okay, you just keep them in a register, yeah.

Henry Rich

**50:17-51:21**

Yeah, just keep them in a register. Of course, in the implementation, there are different loops at the bottom level for all different sizes of argument. It's one loop for bytes and a loop for fours and a loop for eights. In the case of copying, well, when there are a lot of ones and you're trying to turn the operation into a memory copy, Memory copy that's fairly short, an awful lot of time can be spent trying to get the last few bytes right. If you're copying something that's seven bytes long, or maybe it's 1,024 plus seven bytes long, the first 1,024 bytes go pretty fast, but then there has to be testing and branches involved in the last seven, which might end up taking more time than the bulk of the copy. so we carefully over copy when we know that that's okay and we only we copy in blocks of 32 bytes and over store whenever possible.

Marshall Lochbaum

**51:21-51:23**

Yeah we do something similar.

Henry Rich

**51:23-51:26**

That's how the JE does as you can talk about BQN if you know

Marshall Lochbaum

**51:26-51:51**

Yeah I mean so all the broad um cases are pretty similar one case we have that does have to be handled specially is the case where both arguments are boolean because with byte booleans it doesn't matter bytes are just another kind of data with bits I mean this is a whole specialized field really there is um on x86 there's an instruction for it uh the parallel bit extract instruction [06]

Henry Rich

**51:51-51:57**

x86 covers that's that's implemented really badly on a lot of amd machines

Marshall Lochbaum

**51:57-52:01**

Yeah on x86 since 2015 or something.

Henry Rich

**52:01-52:04**

Yeah but I mean it's in the it's supportive. Oh, yeah, yeah.

Marshall Lochbaum

**52:05-52:05**

There is the AMD problem.

Henry Rich

**52:06-52:06**

Yeah. Yeah,

Marshall Lochbaum

**52:06-52:13**

Yeah. On Xen 1 and 2, it's really a problem because the CPU tells you, oh, yeah, I've got these instructions. Great.

Henry Rich

**52:13-52:20**

And a major issue is that... Turns out it takes a micro-program check and emulates it.

Marshall Lochbaum

**52:20-53:10**

Yeah, so Intel really did something dirty on this because they took these two, these Pdep and Pext instructions, which are pretty difficult to implement, and they bundled them in into the BMI2 instruction set, which is mostly stuff. I think like it has that single instruction for a word and with the word minus one that clears the bottom bit. Like that sort of basic stuff hardly takes any space in the processor. It's all bundled together. So what AMD said was, well, we have to support all these basic operations. These are really important. What's PDF and Pext doing? No one's going to use these, right? And they wrote, I mean, They have this micro-coded implementation that's not even good by – there were very well-known algorithms at the time that are much better than what they did.

Henry Rich

**53:10-53:17**

We should probably – it's possible that some of the listeners might not know what PDEF and Pext do.

Marshall Lochbaum

**53:17-53:24**

Well, they – I mean, Pext does literally just a Boolean replicate a Boolean when they're both 64-bit words.

Henry Rich

**53:24-53:52**

Well, that's true. You have a mask of scattered ones and an argument that's got, say, there are eight scattered one bits. The low order eight bits of the argument are scattered so they match up with the ones. And like you said, what it's doing is exactly the Boolean replicate for you. So, yeah, that's a failure made for us.

Marshall Lochbaum

**53:52-56:09**

And probably while we're in instructions, we should also mention that in AVX 512, which unfortunately is still not really, you definitely can't depend on having it. There are even instructions called expand and compress. And they're even more like the APL instructions because they're named after our primitives. So if you happen to be on a machine that supports AVX 512, that's the way to go. But, well, and I guess the one thing you know about them is that they take the Boolean argument is in a mask register. So it's this dedicated kind of register for storing bit masks. Yeah, and it's pretty much designed to do what APL does. But yeah, so regarding the Boolean, the case with two Boolean arguments. So we don't currently try to detect Xen1 and Xen2 specifically. If you build BQN on those and you care about performance, you should actually pass in. We have a has equals slow Pdep argument when you're compiling is what it's called. So then we'll try to cancel. We use Pdep and Pext in various places and we'll avoid using those. I mean, if we've done our code properly. So yeah, and we do have a bunch of fallbacks. What I was saying about like the algorithms A and D should have used, there's a pretty good discussion of this in Hackers Delight, which talks about it goes into a pretty significant amount of detail about an algorithm that I think actually Guy Steele was... like the author of Hackers Delight asked Guy Steele about this. [07] And he just came back with his own original algorithm. So that's what it mostly discusses. And it also mentions there's another algorithm that's kind of like based on mask shifts, which is a little more like how you'd implement it in hardware, I think. But yeah, we have all sorts of like combinations of those two. Like which one you can use depends on which instruction or I mean, you can use either of them in any case, but like it's some are better with certain instruction sets. And so we have at least five different implementations of these methods that we use on different hardware, on different instruction set support levels.

Bob Therriault

**56:09-56:20**

What's the difference in performance? If you say you didn't specify for each, are we talking orders of magnitude? Are we talking two times?

Marshall Lochbaum

**56:22-57:01**

So the difference between, well, so BMI2, which has Pext and Pdep, came out at about the same time as AVX, well, Intel introduced it together with AVX2. And switching between those two algorithms on x86, it's a difference of about a factor of three, which I felt was pretty good getting our AVX2 version down to only three times slower than the dedicated instruction. So that's if you're on XIN 1 or 2, that's what you could expect would be three times slower for this particular operation, which usually, like I said, because it's using only Booleans, it very rarely would need to be as fast as it is. So that's usually acceptable.

Henry Rich

**57:01-57:14**

Yeah, and there's always a question of how much of the overall user's application is in this part of the loop. But if you use Pdep and make the mistake of using Pdep on XIN, it's like 10 or 20 times.

Marshall Lochbaum

**57:14-57:47**

Yeah, if you use that bad implementation, that's many, I think it's worse than that. That was slow enough that we found it because someone said, someone reported a timing for some program and we were like, me and Dzaima x86 were like, no, it's way faster than that. Did you compile with O3 and so on? Did you do an optimized build? And eventually we tracked down that it was this Boolean, replicate Boolean case that was so slow. So it was a pretty big factor in the overall program.

Bob Therriault

**57:47-57:52**

And is that how you would generally find these kind of pinch points? Is somebody reports them?

Marshall Lochbaum

**57:52-58:42**

No, we just, I mean, this was really a special case because it was on a type of processor that we don't have. And actually, this was the fact, we weren't aware that we knew the instruction was microcoded, but we didn't know how slow it is because the sites that report instruction timings, they had run it with mostly zeros and it uses like a looping implementation. So if you use it on mostly zeros, it's pretty decent. I was at some point scratching my head thinking, you know, I mean, I know they can implement whatever they want in hardware, but I mean, they must have some special operations to support this or something to make it that fast because my CPU versions are nowhere near that. But it turns out it was just a measurement problem. And it's actually, if you have a lot of ones, it's really, really slow. It's like hundreds of cycles.

Henry Rich

**58:42-59:41**

Well, I didn't know it was that bad. To answer your question about how you find this stuff, Bob, what I do is whenever I code an algorithm, I have an idea in mind of the speed I expect to get. And I always look at the generated instructions to make sure the compiler hasn't gone berserk, which the compilers are fantastic now at code generation. They do occasionally, you can hit them with something they're not used to, and they go crazy. But usually what you'll find is you didn't ask for exactly the right thing, and so the compiler generates more instructions than you actually need. You get all that fixed, and then you measure the performance and make sure it conforms to your expectation. And the problem is there's so many machines out there. I can do all this on Intel machines, but I really don't know what's happening on Apple M1.

Marshall Lochbaum

**59:41-59:49**

Yeah, I mean, and that's a totally different instruction set. So that only has 16 byte vectors instead of 32. You have completely different considerations.

Henry Rich

**59:50-59:58**

Yeah, although Bill Lamb has this emulation of AVX2 that runs on M1, and it's pretty fast. I'm amazed at how it happens.

Marshall Lochbaum

59:58-01:00:11

Yeah, I mean, it's very fast hardware. The shorter vectors don't, I'm not just saying it's worse, but actually you might consider going to scalar stuff where you wouldn't before, and it'll probably beat a lot of Intel processors.

Bob Therriault

01:00:12-01:00:20

So we mentioned at one point k and q, and that they use, [08] have we covered that enough, do you think, that they use a different process for their replicate?

Conor Hoekstra

01:00:20-01:01:10

I mean, I understood it. Okay. The thought in my head is that I've been trying to track down. I mean, it's a shame that Elias is not here to speak on behalf of KAP because Replicate is one of these operations that I would imagine can be implemented lazily. But I'm a noob when it comes to Kotlin. And I've gotten to the point where I figured out that Replicate, it corresponds to a function in the Kotlin code called select elements, first access function. And there's a couple of them. But then when I find the code, it says return zero in the body of the function. And I'm pretty sure that's not what... So, I mean, I could go test to see if this actually works. And I will say the docs say to do. So, I mean, I imagine it's only the documentation that is to do and not the actual implementation.

Marshall Lochbaum

01:01:10-01:01:10

Yeah, it's definitely implemented.

Conor Hoekstra

01:01:11-01:01:23

But I'd be curious. I mean, Elias, if you're listening, I'd be happy to hear if this is done lazily because, I mean, we've been talking about like an eager.

Marshall Lochbaum

01:01:23-01:01:57

Yeah, so I mean, that's a, it's an interesting case because, so first you can be lazy in the right argument. That's easy. The left argument, you pretty much can't because you have to, like, if you ask for element 100 of A replicate B, The only way you're going to know what that is, is calculate enough of A until you reach 100. I mean, assuming A is even Boolean, which is hard to know, you'd have to calculate enough of A to reach 100 or 99 ones. I think 100 depends on index origin.

Conor Hoekstra

01:01:57-01:02:37

I would imagine that a potential implementation of that, and this is just me hypothesizing on what KAP does, is that any kind of selection either then materializes the result. So it's like you have a lazy object that in certain situations you either have to materialize or you don't even technically need to materialize the whole thing. You just treat like index selection at 100 as like a take 100. And then you do just like the last of that operation. It's all implementation dependent, right? I have no idea what KAP actually does. But I'd just be curious to know like if he treats replicators in the class of things that are lazy if they can be, you know?

Marshall Lochbaum

01:02:38-01:02:42

I would expect so because, I mean, he's pretty serious about doing that right.

Conor Hoekstra

01:02:43-01:02:43

Yeah.

Marshall Lochbaum

01:02:43-01:02:53

And, I mean, yeah, usually, like, if the right argument is, I mean, it could be arbitrarily large elements. If you can skip even computing a lot of it.

Conor Hoekstra

01:02:53-01:02:54

Right.

Marshall Lochbaum

01:02:54-01:03:08

That's pretty great. And, I mean, the left argument, you know, the left argument can be, like, X is greater than 4 or whatever. Like, that's a fast computation. So if you have to materialize the whole left argument, that's not a really big problem.

Conor Hoekstra

01:03:08-01:03:08

Yeah.

Marshall Lochbaum

01:03:09-01:03:31

So maybe what it, I mean, kind of the obvious implementation to me would be if you're going to materialize the whole left argument, um, instead of trying to do it on a prefix, what you do is actually just call where on that left argument and then do a selection using however you implemented the selection primitive. It's definitely lazy. And then you, you're automatically lazy on the right argument.

Conor Hoekstra

01:03:31-01:04:02

Yeah. If you're listening, I know he's a listener or was a listener. I'm not sure if he stopped at any point. I don't know if we said something about KAP that would have caused that, but if you are listening. We've said a lot of things. If you are listening, I'd be curious to get a note and maybe we can organize one of these primitive talks in the future where he attends and then he can just recap every primitive that we've covered up until then and like a little rapid fire KAP differences because of all the APLs out there, I imagine his implementations are going to differ like the most widely from.

Marshall Lochbaum

01:04:03-01:04:06

Yeah. I mean, he can do it as rapid fire as he wants. We're still going to be sitting around for like days.

Conor Hoekstra

01:04:07-01:04:08

That's true.

Bob Therriault

01:04:09-01:04:13

Maybe we have to find out that he can do it lazily so that we don't have to, you know.

Marshall Lochbaum

01:04:13-01:04:22

Oh, yeah. So we ask him for this specific. Yeah. We say, all right, so consider replicate. Now consider this specific case and we'll ask you about that. And he'll lazily come up with it.

Conor Hoekstra

01:04:24-01:04:30

All right. I mean, well, is there, have we missed some corners of the replicate?

Marshall Lochbaum

01:04:30-01:04:40

Yeah, I think I didn't cover the BQN implementation quite well enough because, and I was actually originally thinking when you said, well, this is indices, but we won't talk about that anymore. I was like, you don't know how to implement replicate.

Conor Hoekstra

01:04:43-01:04:49

I was only saying that because when I brought up expand, Adám was like, no, no, no, no, that's another episode. So I was just as my moderator.

Marshall Lochbaum

01:04:50-01:06:08

Expand we won't, but indices. So indices is just so tied replicate. The main implementation that we use for compress when it's not one of these sparse cases, when we don't have mostly zeros or mostly ones or mostly runs of zeros and ones, the main method is to make a lookup table of indices. So you'll have a few different sizes, but maybe you'll have a table that takes one byte and produces the indices of those bytes into an AVX2 register. And then we'll use that together with the shuffle instruction, which is like the AVX or SSE form of selection. So we're basically just doing indices select. And then we also have to figure out how many ones were in the byte so we know how far. So we'll write that selection to the result. And then we'll also have to know how far to move along. And this is overlapping too because when you compress a register, when you do that selection, only the first some number of values are actually going to have anything in them the rest are just there because vector registers are fixed length so the basic idea is a lookup table of bytes to indices and then a selection and that's pretty fast because it just because it handles more stuff at once.

Conor Hoekstra

01:06:08-01:06:16

Adám you you had your hand up too when I was saying did we did we carve out all the corners of replicate

Adám Brudzewsky

01:06:16-01:06:32

Uh well I mean there's one thing that's that may be interesting. I've explored what happens in the other array languages and that is what happens when you replicate the scalar so does everybody agree that because really we say that...

Marshall Lochbaum

01:06:32-01:06:34

This is not about the implementation right because it's...

Adám Brudzewsky

01:06:34-01:06:37

No it's not about the implementation

Marshall Lochbaum

01:06:37-01:06:38

No but you did just add up the left argument.

Adám Brudzewsky

01:06:38-01:06:39

That's all you...

Marshall Lochbaum

01:06:39-01:06:45

Although I think Dyalog had some messy code if the left argument has a mix of positive and negative numbers.

Adám Brudzewsky

01:06:45-01:06:52

Yeah, so I mean, I assume, Conor, you're asking if there's any edges on Replicate that we want to address, not on the implementation of Replicate. Is that correct?

Marshall Lochbaum

01:06:52-01:06:56

Because we didn't even get to the implementation of Replicate, not Compress.

Adám Brudzewsky

01:06:56-01:07:03

So what was your question, Conor? Is it about the implementation or edge cases in general? I don't know if you're trying to wind down here or not.

Conor Hoekstra

01:07:04-01:07:24

Well, I mean, I was definitely trying to wind down because hard stop in T minus seven minutes. But if we need to, we can do replicate part two. It sounds like we didn't even touch on a whole corner of the... I mean, I'm not a language implementer here. It's your guys' job. I'm just trying to lift up the rock to see if there's any like caterpillars and beetles, you know, that were like, whoa.

Adám Brudzewsky

01:07:25-01:08:38

So, I mean, one thing I'd like to at least just mention is when the right argument to replicate is a scalar, right? Really, Replicate should be making duplicates along some axis first, last, given axis, whatever it might be. But there are no axes in the scalar. So what exactly happens? Do we treat a scalar as a one element vector in that case? And I know APL does that, which means that one replicate two is just a vector two. And the same thing for two replicate one and so on. Just one one as a vector. And this is used, actually, to make sure that an array has at least one axis. There are cases where you need it to have at least one axis. But you don't want to change anything otherwise about the array. So people will write an APL one slash on that array. So that's a one replicate. Presumably, it does nothing, right? Because whatever you have on the axis that it's working on, one replicate just means you take every cell or everything along that axis and do one of them. So everything stays as this. But if the right argument is a scalar, it gets transformed to a vector. And I don't know if the other languages do this. Do they error if the right argument is a scalar?

Marshall Lochbaum

01:08:39-01:08:51

I actually had to test this out in BQN and it does not allow it. As you can tell by the fact that I have no idea whether I allowed it or not. People don't run into issues with it very much, or at least they don't report them.

Conor Hoekstra

01:08:52-01:09:08

Yeah, this is one of these things where, I mean, it's important to figure out what to do. But this is where I'm just happy I'm not a language implementer. Because, you know, this is like not a thing I would ever type. And if I did, I'd just be like, oh, replicate doesn't do it. Let's see if reshape works. And then one of them will.

Marshall Lochbaum

01:09:08-01:09:25

Yeah, that is actually. So people do sometimes do like 5 slash A or something, trying to get a list of 5 As. Because that works in APL. Yeah, it works in J also. And then you have to say, well, use reshape instead. That's what the primitive we like for that. Yeah.

Adám Brudzewsky

01:09:25-01:09:42

Oh, so this wouldn't work for k either, k and q. because if you just have a scalar, you can't index into it with a where. So if you do a where on the five, that might give you 0, 0, 0, 0, 0. But those are not valid indices for a scalar.

Marshall Lochbaum

01:09:42-01:09:44

Well, we have the whole avdexing thing, right?

Adám Brudzewsky

01:09:45-01:09:49

I don't see how it could possibly work.

Marshall Lochbaum

01:09:49-01:09:54

So I'm not actually sure. Yeah, so ng in k does give you a type error.

Adám Brudzewsky

01:09:54-01:09:56

Yeah, so too in Shakti.

Marshall Lochbaum

01:09:57-01:10:07

I guess, I mean, yeah, the indexing primitive in k is the same as function application. So, of course, it really depends on the type and it does. It has to be a list for it to mean indexing at all.

Adám Brudzewsky

01:10:08-01:10:14

Yes. Otherwise, it doesn't mean something else. Yeah. It means execute or something. I think.

Marshall Lochbaum

01:10:14-01:10:15

It means lots of things.

Adám Brudzewsky

01:10:16-01:10:17

No, it's a scalar.

Marshall Lochbaum

01:10:17-01:10:19

It applies a function.

Adám Brudzewsky

01:10:19-01:10:26

I think if you apply to... Is that the one that with strings? Yeah, no, yes. Indexing is...

Marshall Lochbaum

01:10:26-01:10:34

Like the basic meaning in k is that it's the same as applying a function, which when you apply a list as a function, that's indexing.

Adám Brudzewsky

01:10:34-01:10:46

Yeah, but if you try to index or apply whatever on a character scalar, then it means execute in that language. So like if you apply to the letter, yeah, and if you apply...

Marshall Lochbaum

01:10:46-01:10:52

So yeah, that's a bit of a stretched interpretation in my opinion, but many k's do that.

Adám Brudzewsky

01:10:53-01:11:05

I mean, it makes sense. You apply a k on a string, that's executing k on it. Apply q on a string, run the q on it. Apply J on the string, then you run J on it. It makes sense.

Marshall Lochbaum

01:11:06-01:11:10

But it does have to be a single character, right? Because otherwise it is a list.

Adám Brudzewsky

01:11:10-01:11:25

Why would you ever name a programming language with more than one? Can you tell me one successful, well-established, recognized, respected programming language that has a language that has a name that's not a single character

Marshall Lochbaum

01:11:25-01:11:29

Good question. No exactly. Hard question.

Conor Hoekstra

01:11:29-01:12:18

All right all right let's let's calm down here I'm uh asserting myself as moderator and host of the podcast tune in next time and also uh you know i've thoroughly enjoyed this but we definitely this is our first time doing primitive talk like I said I did put the uh cart in front of the horse at that one point I'll fix that but if you've got feedback on the aspects of this conversation, whether it was the implementation deep dives, the design deep dives, the history deep dives, we definitely want to hear because, I mean, clearly you can tell that we get excited when we talk about this and it can turn into a little bit of ping pong back and forth of like super. Anyways, we want to make sure that we're giving you the content that you guys and folks want. So if you have feedback or even a next, should we do replicate part two next time? Or should we switch to a different primitive and then cycle back? If you have thoughts on that or questions or feedback, you can reach us at.

Bob Therriault

01:12:18-01:12:34

Contact at ArrayCast.com [09] and I won't do that lazily I will actually put it in there so contact at ArrayCast.com and uh certainly uh we may discuss KAP in the future episode because we always bring people back on again there's no reason we can't do that.

Conor Hoekstra

01:12:34-01:12:52

Yeah I was gonna say we should we should try and get a combination of I was also thinking you know we didn't really shout out Uiua much except for when I said it was called keep but um you know they do things in Rust. So potentially there's some different implementation or design details due to the fact that Rust is backing things. Maybe not. Maybe Kai's thinking, ah.

Marshall Lochbaum

01:12:52-01:12:59

It's not super optimized generally. So, I mean, there's probably some attention paid to it.

Conor Hoekstra

01:12:59-01:13:07

But it's not always about AVX and SIMD instruction optimizations. It is always about AVX.

Bob Therriault

01:13:07-01:13:15

Once again, the plane bounces down the runway, coming to a lovely rest, just short of the berm of the end.

Marshall Lochbaum

01:13:15-01:13:20

I just wonder, what is our home made of? At least we made it through the deep dive.

Conor Hoekstra

01:13:21-01:13:25

Ish, apparently we missed the whole floor, but...

Adám Brudzewsky

01:13:25-01:13:28

Conor, pull the brakes.

Conor Hoekstra

01:13:28-01:13:40

Anyways, thank you so much for joining us, Henry. We'll definitely have you back. and if you're Elias or Kai hopefully we'll get you on one of these primitive talks as well so we can get some different points of view and with that we shall say happy array programming

Everyone

01:13:41-01:13:42

Happy Array Programming.

</details>
