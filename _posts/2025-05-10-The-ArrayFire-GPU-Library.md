---
title: "Episode 105: The ArrayFire GPU Library"
date: 2025-05-10 00:00:00 +0000
episode: 105
keywords:
- array-programming
- array-languages
- jlang
- gpu
- arrayfire
- john-melonakos
- umar-arshad
- opengl
mp3-url: "/assets/audio/episode105.mp3"
episode-type: full
explicit: "no"
block: "no"
layout: podcast
excerpt_separator: <!--more-->
redirect_from:
  - "/episodes/episode105-arrayfire"
  - "/episode105-show-notes"
---
The ArrayFire GPU LibraryOur guests are John Melonakos and Umar Arshad of ArrayFire as we discuss the challenges of implementing GPU performance for higher level languages.
<!--more-->

**Host:** Conor Hoekstra

**Guest:** John Melonakos and Umar Arshad

**Panel:** Marshall Lochbaum, Adám Brudzewsky, and Bob Therriault

---


## Show Notes

Array Cast -  May 9, 2025

Thanks to Bob Therriault for gathering these links:

**[01] 00:01:40**

- [Juno J on the Web](https://jsoftware.github.io/juno/app/)
- [Dyalog APL Challenge](https://challenge.dyalog.com/)
- [FinnAPL Spring Meeting](https://www.finnapl.fi/tapahtumat/)
- [Aaron Hsu Episode #100 of the ArrayCast](https://www.arraycast.com/episodes/episode100-100hsu)
- [Co-dfns compiler](https://github.com/Co-dfns/?ref=sacrideo.us)
- [ArrayFire.com](http://arrayfire.com/)
- [arrayfire.com](https://arrayfire.com/)
- [ArrayFire.org](http://arrayfire.org/)
- [arrayfire.org/docs/index.htm#gsc.tab=0](https://arrayfire.org/docs/index.htm#gsc.tab=0)
- [OpenGL](https://www.khronos.org/opengl/wiki/)
- [MATLAB](https://www.mathworks.com/products/matlab.html)
- [NVIDIA](https://en.wikipedia.org/wiki/Nvidia)
- [CUDA](https://en.wikipedia.org/wiki/CUDA)
- [GPU](https://en.wikipedia.org/wiki/Graphics_processing_unit)
- [MathWorks](https://www.mathworks.com/)
- [Intel](https://en.wikipedia.org/wiki/Intel)
- [SYCL](https://www.khronos.org/api/index_2017/sycl)
- [OneAPI](https://www.intel.com/content/www/us/en/developer/tools/oneapi/base-toolkit.html#gs.m4jjb8)

**[02] 00:11:21**

- [C Programming Language](https://en.wikipedia.org/wiki/C_(programming_language))
- [C++ Programming Language](https://en.wikipedia.org/wiki/C%2B%2B)
- [Forth Programming Language](https://en.wikipedia.org/wiki/Forth_(programming_language))
- [APL  Programming Language](https://aplwiki.com/)
- [JavaScript Programming Language](https://en.wikipedia.org/wiki/JavaScript)
- [Python Programming Language](https://en.wikipedia.org/wiki/Python_(programming_language))
- [NumPy Library](https://en.wikipedia.org/wiki/NumPy)
- [J Programming Language](https://www.jsoftware.com/#/README)
- [J ArrayFire add-on](https://code.jsoftware.com/wiki/Addons/math/arrayfire)
- [Array Language Paradigm](https://en.wikipedia.org/wiki/Array_programming)
- [Eric Iverson Episode #10 of the ArrayCast](https://www.arraycast.com/episodes/episode10-eric-iverson)
- [BQN Programming Language](https://mlochbaum.github.io/BQN/)
- [Google Scholar](https://en.wikipedia.org/wiki/Google_Scholar)

**[03] 00:23:28**

- [Reduce](https://aplwiki.com/wiki/Reduce)
- [Scan](https://aplwiki.com/wiki/Scan)
- [q Programming Language](https://code.kx.com/q/)
- [Reductions in ArrayFire](https://arrayfire.org/docs/group__reduce__mat.htm#gsc.tab=0)

**[04] 00:30:06**

- [JIT compiling](https://en.wikipedia.org/wiki/Just-in-time_compilation)
- [JAX](https://en.wikipedia.org/wiki/JAX_(software))
- [Rust Programming Language](https://en.wikipedia.org/wiki/Rust_(programming_language))
- [Tensorflow Library](https://en.wikipedia.org/wiki/TensorFlow)
- [Julia  Programming Language](https://en.wikipedia.org/wiki/Julia_(programming_language))
- [Anaconda Installer](https://en.wikipedia.org/wiki/Anaconda_(installer))

**[05] 00:40:04**

- [NVIDIA GTC](https://en.wikipedia.org/wiki/Nvidia_GTC)
- [Open Source Code](https://en.wikipedia.org/wiki/Open_source)
- [GitHub](https://en.wikipedia.org/wiki/GitHub)
- [Mag 7](https://en.wikipedia.org/wiki/Big_Tech#Magnificent_Seven)
- [Go Programming Language](https://en.wikipedia.org/wiki/Go_(programming_language))
- [Kubernetes Package Manager](https://en.wikipedia.org/wiki/Kubernetes)
- [IBM](https://en.wikipedia.org/wiki/IBM)

**[06] 00:50:32**

- [Dyalog APL Ltd.](https://www.dyalog.com/)
- [Clojure Programming Language](https://en.wikipedia.org/wiki/Clojure)
- [Mathematica Programming Language](https://en.wikipedia.org/wiki/Wolfram_Mathematica)
- [k Programming Language](https://wiki.k-language.dev/wiki/Main_Page)
- [Octave Programming Language](https://en.wikipedia.org/wiki/GNU_Octave)
- [GNU APL Programming Language](https://aplwiki.com/wiki/GNU_APL)

**[07] 00:58:02**

- [ArrayFire CoLab access](https://arrayfire.com/blog/cuda-computing-on-google-colab-with-arrayfire/)
- [ArrayFire Binaries](https://arrayfire.org/docs/index.htm#gsc.tab=0)

**[08] 01:02:05**

- [Richard Branson](https://en.wikipedia.org/wiki/Richard_Branson)
- [Crypto Currency](https://en.wikipedia.org/wiki/Cryptocurrency)
- [Miguel Raz - Julia Episode #103 of the ArrayCast](https://www.arraycast.com/episodes/episode103-julia)
- Contact AT ArrayCast DOT Com

<details markdown="1">
<summary><strong>Transcript</strong> (click to expand)</summary>

Transcript

Transcript prepared by

Adám Brudzewsky, Bob Therriault, and Sanjay Cherian

Show Notes

00:00:00 [John Melonakos]

It is very helpful and gives us a competitive advantage to have an ecosystem that's built around an open product, to give our customers the reliance that this thing is open source, that the rug's not just going to get pulled out from under them. And in hindsight, there's just so many more benefits, I think, to being collaborative versus competitive with how you build software.

00:00:33 [Conor Hoekstra]

Welcome to episode 105 of ArrayCast. I'm your host, Conor. And today with us, we have two special guests who I'm extremely excited to chat with. But before we get to introducing them, we're going to go around and do brief introductions. We'll start with Bob, then go to Adám and finish with Marshall.

00:00:49 [Bob Therriault]

I'm Bob Therriault. I am a J-enthusiast, and this is going to be a very interesting episode.

00:00:54 [Adám Brudzewsky]

I'm Adám Brudzewsky. I am head of language design at Dyalog Ltd. doing APL.

00:01:01 [Marshall Lochbaum]

I'm Marshall Lochbaum. I work on BQN and Singeli. I haven't really thought to give myself a title before.

00:01:07 [CH]

And as mentioned before, my name's Conor, host of ArrayCast and massive fan of all of the array languages, as well as array libraries, which we're going to be talking about today. But hang on for a few more seconds, because we've got, I think, three announcements. So we'll go to Bob with the first announcement, and then we'll hop over to Adám, who's got two other announcements.

00:01:25 [BT]

Yes, I have an announcement. [01] On the last episode, Henry Rich mentioned that Marcin Zolek had taken over Dissect, which was really cool because Dissect is a really neat debugging tool. But Marcin has also picked up and created his own Juno, which is an interface, an IDE using J. He's upgraded it to J 9.7. So by running this, you can actually run the new beta and you can test the new beta for everybody, which is great because we're finding errors and things that need to get fixed, which is what you want to do with a beta. But also what this is, this IDE, it's essentially on your browser. So it's like the J Playground, which was the previous one, but he's taken it a further step. He's upgraded it so that you can actually take J code and send links. And when you click on the link, it'll open up the Juno system on your browser. So you can actually send information back and forth. And also for people who want to use it on a laptop, there are sidebars that have extra information, but you don't always want the extra information. Sometimes you just want to use the center part of the field where you're putting the programming in, and you can make those sidebars disappear. It's on a menu item. So he's evolving as it goes along. I think I mentioned it probably about a month or six weeks ago, but if you haven't checked it out, it's worth checking out and we'll have a link in the show notes.

00:02:45 [CH]

Over to you, Adám.

00:02:46 [AB]

I can announce, I think from the past, that the new round of the Dyalog APL challenge has just started. So this is intended for people who are very new to array programming or APL. And even if you don't know anything, or if you know somebody who doesn't know anything, you can let them lose at challenge.Dyalog.com and it teaches you everything you need to know in order to complete the challenge and potentially win prizes. And then there is on the 20th of May, the FinAPL spring meeting in Helsinki in Finland.

00:03:21 [CH]

Awesome. So we will have links as always to all three of those announcements in the show notes, if you're interested in checking them out. And finally, that brings us to introducing two new guests today to talk about the GPU accelerated library ArrayFire, which you may have heard before. So with us, we have John Melonakos and Umar Arshad, who both currently work for Intel. I think officially the titles are AI Libraries Architect and AI Algorithm Engineer for John and Umar, respectively. And they are the current maintainers and have been working on ArrayFire for, I think if I'm correct, a decade and a half plus. I can be corrected in a second because I think we're going to do a deep dive into the history of ArrayFire. And for those of you that are thinking ArrayFire, I feel like I've heard that mentioned on this podcast before. That's because you definitely have ArrayFire, probably less notably for John and Umar, but notably for us because we've had Aaron on a couple of times, Co-dfns the GPU accelerated parallel APL compiler, targets ArrayFire. So there's a strong tie between one of the APL compilers and projects and this library. So I think now we're going to throw it over to John and Umar. And maybe you want to briefly both introduce yourselves and then we'll dive back to a decade and a half plus ago and we can get the story of ArrayFire.

00:04:45 [JM]

Hello, I'm John Melonakos. I'm one of the co-founders of ArrayFire. And I'll give that background story in a minute. But I've been working on ArrayFire and array-based programming, specifically how do you take arrays and make them accelerated on GPUs, my whole career. And now, three years ago, we joined Intel. And the ArrayFire team is now at Intel. And I'm a maintainer of the ArrayFire open source project, which includes Intel people as well as non-Intel people.

00:05:19 [Umar Arshad]

My name is Umar Arshad. I've been at ArrayFire since 2012, 12 years now. I've been maintaining ArrayFire since then, mostly on the development side, making different kernels using CUDO and CL and a SYCL recently.

00:05:40 [CH]

Awesome. So maybe let's hop right into it then. So take us back to the beginning. When did both of you get involved? I remember seeing John, I think it says CEO and co-founder. So I'm guessing you were involved from the beginning. And yeah, what is the history of ArrayFire and bring us from the genesis to today?

00:05:58 [JM]

I was a PhD student at Georgia Tech, and I was working in our lab. We were doing some computer vision algorithms, working on partial differential equation, sort of minimizing cost functions to detect various things in brain MRI imagery. And at the time, you know, it is brain volumes, especially the kind of volumes we were working with were just massive data sets and was taking half a day to, you know, a long time to process on the hardware we had at the time on the CPUs. And one of my lab mates and my co-founder realized you could run this through OpenGL shaders. And he built it, and we were doing all our work in MATLAB, so he built a GPU engine for MATLAB that ran through OpenGL shaders and enabled us to offload our MATLAB code onto NVIDIA hardware. And then when NVIDIA heard of this, they flew us out to California. This was like 2006, 2007, and told us about this thing called CUDA that they were building. And that started a very close partnership with NVIDIA from the very beginning. We were the way that people programmed to MATLAB on NVIDIA GPUs for a long time until about 2012. So for five years, we sold an add-on product to MATLAB, and that's how we got our start. It was very, very popular. We were in 40 countries around the world, and just rapidly, just sort of people picked it up because a lot of people had slow MATLAB code and wanted to have their arrays naturally expressed in faster hardware. We did a deal with MathWorks in 2012 that sort of ended that first phase of the company, and we sold that product to the MathWorks, but we retained the rights to the source code for other languages besides MATLAB. And so we retooled our whole business model from selling a MATLAB product to running an open source project and just selling sort of services to help people along the way. So we gave now our source code away for free, and that's what ArrayFire is today, is this open source project. We supported more than just CUDA. We supported OpenCL, and then more recently, we now support SYCL as well, and we also have a CPU backend. So from 2012 to 2022, for about 10 years, we just ran as this small boutique consulting shop, but really passionate about open source array-based programming and getting high performance out of GPUs. And in 2022, as we were starting to work on the SYCL backend, Intel told us more about oneAPI and the vision they have for sort of bringing in many different hardware vendors into one standard so people can write their code once and run it everywhere. And we had already been this for the array languages. We'd already been the place where you can write your code once and run on CUDA or OpenCL or the CPU. And so it just aligned, the visions aligned, and our team joined Intel. And within Intel now, we also are continuing to work on ArrayFire. We work on other libraries as well within the oneAPI ecosystem. And Intel wasn't interested in our consulting business and in the open source project. So that still runs with, there's other people that are consultants and other maintainers of ArrayFire that continue to build ArrayFire and then help users through commercial services to get success. And that's how we fund the project. But yeah, that's the story. So we've been at Intel almost three years, and it's been a beautiful journey.

00:09:48 [CH]

Do you want to add anything to that, Umar? Were you there from the beginning as well, or did you join at a later point in time?

00:09:54 [UA]

I joined a little bit later. I joined around 2012. I was working at an insurance company working on C# code. And I had invited John to an ACM meeting as a guest speaker at our school. So I'd known about him and he had posted a job and I thought this is a great opportunity. I'd been working on GPU competing for a while. That seemed like a perfect opportunity. They were in the same city I was in, so I applied and I got hired. And I came in just as we were transitioning from the 2.0 version of the software to 3.0. So I gave him a hand on building ArrayFire from that point on.

00:10:35 [JM]

He started just sort of coming in as a really learning GPU computing on the side. It wasn't his job and just quickly picked it up. And ultimately now he's the chief maintainer and architect and knows more of the code base than anyone else. It's been beautiful to watch over the last decade and 12 years or so.

00:10:55 [CH]

That sounds awesome. So you mentioned that at a certain point in time you were primarily focused on accelerating MATLAB and in 2012 you kind of ended that chapter and started a new chapter and that you maintained the rights for other languages. I primarily know ArrayFire as the GPU C++ library, but are there other front-end languages that lower down onto the C++? What's the landscape of the ways that people are targeting ArrayFire?

00:11:25 [UA]

When we transitioned from 2.0 to 3.0, we wanted a way to support other languages, not only C [02] and C++. Primarily we were targeting C++ for general case, but then we were also targeting Fortran at the time. But the way the library was structured, it forced you to adopt the C++ runtime, which is not as flexible as the C runtime. So we redesigned the library to provide our API through the C API. And then now people are able to run ArrayFire on Python, in JavaScript, in APL, a whole bunch, sort of, a host of languages.

00:12:09 [JM]

Yeah, there's lots of third-party wrappers. We're about to release next month ArrayFire 3.10, which will have our first officially supported Python version. And we're excited about that one. And it will comply with the data API standard. So it'll be a drop and replace to any data API NumPy scenario.

00:12:32 [CH]

Interesting. So how does this work, then? Currently if you want to use ArrayFire from Python, are you pip installing some kind of PyPI package? Or are you hooking something up, you're pip installing NumPy and you set some local settings or something? What's the story around that? Because I know a lot of libraries, or at least where I work, there will be an open source version of some library, and then we'll go create -- and by we, I mean NVIDIA -- we'll go create a GPU version. But it's basically just we built it from scratch, and we're calling it something different. And then our story is, like, oh, if you use this library and you're hitting performance concerns, consider changing your import statement and pip installing something. Or maybe you need to go install Conda. But there's a couple different ways you can do this. For the Python listeners, there's probably four of them that we have. How do they go and do this when 3.10 drops?

00:13:28 [UA]

Yeah, so we'll be creating a wheel for Python. So you'll be able to pip install ArrayFire with a specific version of Python. And for your specific OS, it'll download a bunch of binaries, and then it'll be ready to go. All you have to do is install default drivers, and it'll pick up the hardware.

00:13:48 [CH]

And then you can just use that directly from libraries like NumPy.

00:13:52 [UA]

Yes, exactly. So import ArrayFire, and then you can define which API you want to use. If you want to use the data API, you can do, like, import AF.dataAPI, and you'll be able to run it.

00:14:05 [CH]

Interesting.

00:14:06 [JM]

And you get all the back ends with the download, too. So you can run it through OpenCL, through CUDA, through CPU, through SYCL. If you have an NVIDIA GPU, you can literally run all of those back ends on the same NVIDIA GPU.

00:14:20 [CH]

So I have a bunch of kind of deep-divy questions that are, like, CUDA and GPU-related. But that's my bias. So I'm going to pause here and maybe throw it to Bob or the other two panelists, and maybe take a break. And later on, we can get into my, you know, satisfying my curiosity about, you know, how the engine works internally. But I see Bob's got a question, so we'll go to Bob first.

00:14:43 [BT]

Well, you work with a number of different languages, and there's always talk in the array languages about how easy it should be to port array languages over to GPUs. But you guys are one of the few ones that have really done it in a way that we can access them. There's an add-on in J that runs with ArrayFire. What's your feeling about that perception that array languages are just built for GPUs?

00:15:07 [UA]

I think that's a fair assessment, because GPUs are designed to work on parallel hardware. Basically, if you think about it, any graphics game that you're running, you're working on a bunch of vertices and pixels, which can be mapped to an array-like structure. So I think that's -- they map really well. The tricky part comes in on the runtime side, which can get a little bit more tricky, and optimizing for different hardware, that's where the interesting parts come in.

00:15:44 [JM]

Yeah, one of the things we've done over the many years is we notice there's a huge gain just in vectorizing your code from the start, and just removing loops or finding inefficiencies. Just even the process of going from a serial code to more of an array-based code makes people remove inefficiencies that are hardware-independent inefficiencies, and then moving it, mapping it naturally to data parallel hardware. Both stages of that give great improvement.

00:16:17 [UA]

Yeah, exactly. So we have -- C programmers have a tougher time porting over to ArrayFire than array programmers like MATLAB and Python.

00:16:28 [BT]

Yeah, I was going to say, that's something that we've often talked about to people. If they -- trying different paradigms, you end up having different skills. One of the strengths of the array paradigm is that it does work really well with -- or should work really well with parallel processing. Often the challenge is trying to get it into something that a GPU can understand, because a GPU wants to do things very quickly with a very, very defined group of functions, basically. In the case of what you might be doing in your general computing, it's a step to try and figure out how to convey that, and ArrayFire is something the add-ons can do that.

00:17:08 [CH]

And I had no idea that J -- I was only aware of Aaron's Co-dfns work, and that's like a full-blown compiler. So J has an add-on? I assume that's not -- it doesn't swap out a compiler underneath. It's just accelerating, like, a few set? Or do you know more? I guess we have to bring the J add-on guy on, or girl on, whoever is responsible for this. I had no idea that this existed.

00:17:32 [BT]

I think it's Eric that actually put it together, Eric Iverson. And essentially it just gives you an interface into ArrayFire, so I think you have the choices of what you're running and how you run it. So it's just an interface, yeah.

00:17:45 [CH]

I mean, speaking of different projects that are using ArrayFire on the back end, are John and Umar -- do you guys know if there's popular projects out there? Because I didn't actually know that Co-dfns was targeting ArrayFire until I spoke with Aaron one time. I think he does mention it out there, if you've read his dissertation or any of his articles, you can stumble across it. But are there other projects that potentially are using ArrayFire that folks might not realize? And this is classically the problem. I ask Marshall, "Oh, you know, how many people are using BQM?" But a lot of folks that are using, you don't ever know that they're using it, because if they're happy customers, they don't tell you, right?

00:18:26 [JM]

Yeah, there's quite a few projects using ArrayFire. You know, we don't know all the projects, of course, that use it, but we monitor, for instance, Google Scholar, and every year there's many, many research papers that are using ArrayFire. And one of the ones that we like the most comes out of Meta, because they took ArrayFire and built a machine learning framework called Flashlight. What do I want to say about Flashlight?

00:18:52 [UA]

Yeah, it's just the AI framework designed to efficiently process, you know, machine learning workloads on C++ instead of Python. One of the interesting things that they point out is that the Python system adds a lot of overhead to some small processes. So they were trying to target C++, and they chose ArrayFire as a backend for that.

00:19:17 [JM]

Yeah, yeah, that's really cool, this C++ framework for building AI applications and to see ArrayFire being used for it. And the reason they picked up ArrayFire for it is because it was something where they, you know, they could have done all those kernels directly in CUDA themselves, but they wanted something where they could have that productivity and performance balance and iterate really quickly in a research space and get a lot of, you know, get a lot of software built in a lower amount of time while getting most of the performance out of the hardware.

00:19:48 [CH]

Yeah, that makes a lot of sense. I mean, in the Python space, there's a ton of different options that are basically moving the dial on that trade-off, like how much flexibility do I want versus how quickly do I want to get something up and running. And depending on where you are in the research stack, you know, that ultimate performance is more important, but other times it's just, I need this accelerated, I don't need to tune the kernel parameter for whatever the block size, etc. You just want it on the GPU. It doesn't need to be completely optimized.

00:20:20 [JM]

And a lot of people use ArrayFire in those sorts of use cases where they'll start out with it to get quick performance, and if it's not hitting whatever performance benefits they need later on, maybe they'll write their hand-tuned code, but in most cases it just works out of the box and gets you very, very close to something that a hand-tuned code would do.

00:20:42 [CH]

All right, so I'm waiting to see if Bob, Marshall, Adám, if you're going to stop me from asking. I see Adám's unmuted, so he does have a question.

00:20:52 [AB]

Well, I don't know much about these subjects, of course, and I'm definitely not a C or C++ programmer, not even Python, but I find it notable that the name of this thing is ArrayFire and not, say, GPUFire or something like that, and maybe I missed something completely here, but were you familiar with array programming in general or array programming languages before you started this project?

00:21:21 [JM]

Yeah, so again, the project had its genesis with MATLAB, so we started by not creating our own API in any sense. We just overloaded all of MATLAB's arrays and their functions, and as we did that, we sort of in that mapping really understood the array languages. That initial project we just called "Jacket" when we were in there, but once we ... and we understood sort of MATLAB's inheriting from APL, and its sort of background of some of the array languages, and we felt like this project at the time was the first one to go from CPUs to now GPUs, and we felt like we were taking one of the first array-based approaches to do massively parallel hardware with GPUs, so that's sort of where we got the name.

00:22:18 [AB]

Okay, so that's what I didn't pick up on originally, that it's kind of modeled after MATLAB's array model and the array language that's in MATLAB.

00:22:28 [JM]

Yeah, so the functions we have in C++ are very, very similar to the ones that you would find in MATLAB. There's a few different names here and there, but it's pretty much the same thing. You index into arrays in the same way, you can search arrays in the same way, you can manipulate arrays in the same way, and then ultimately you can call different math functions on them in the same way.

00:22:53 [CH]

So this is a ... I'm not a MATLAB expert, but I did spend, I don't know, a couple days at one point messing around, and I think at the time I was doing my master's, and so I had access to the actual paid product because, correct me if I'm wrong, MATLAB, you do need a license to use. Right? And I think I recall they have a bunch of built-in, basically hard-coded reductions. They have your sum, your max, your prod, your et cetera. But trying to program a generic reduction was possible, but it wasn't ergonomic, if you will. So the question is, does that extend to ArrayFire, or do you guys have a generic reduce or fold, [03] or is it very similar to MATLAB, where if you see it in MATLAB, it's there, but if it's not in MATLAB, don't expect to see it in the ArrayFire API?

00:23:47 [UA]

Yeah, I think it's very similar to the way Python or MATLAB does it. Can you be a little bit more specific which kind of reductions we're talking about? Because I think we can handle a lot of them.

00:23:58 [CH]

So this one, if we stay in ArrayLand, all of the array languages, or at least in my head, I don't know, maybe the other panelists can disagree, two of the bread and butter operations are reduce and scan, and there's no such thing as a -- well, it actually depends on -- there's some esoteric, if you don't consider APL and J esoteric. There's some even more esoteric array languages that actually do provide symbols or primitives for things like summation or taking the product of something.

00:24:34 [ML]

Well, q has names for them, right?

00:24:35 [CH]

Most.

00:24:36 [CH]

Yeah, q has names for them, but in APL and J and BQN, you only get the generic version, meaning that there's a symbol for reduce and scan, but you always have to provide the binary operation, like plus or times, in order to spell that reduction. And so, I mean, there's a couple different flavors of whether they take an initial value, et cetera, things like that. And Adám's maybe going to add something. So the question is, in ArrayFire, can you spell a reduc or fold where you're passing it a custom binary op? So I'm sure you guys have some, but are you able to spell that an alternative way with a reduc or fold where you're basically typing in the plus operation? And therefore, you could do something that isn't in that set of six or eight hard-coded reductions.

00:25:25 [ML]

Yeah, so like an exclusive or XOR scan is something that you might want to be able to do.

00:25:28 [UA]

Yeah, no, I think we have a set number of reduction operations that we can do, kind of like plus, multiplication, and so on, min, max, et cetera. We're not really a compiler library, which would allow you to do something like that, where we can do it at runtime. Although we are compiling kernels at runtime, but you can't really encode any special operations like that, no.

00:25:56 [CH]

Okay. And Adám, what were you going to ask or add?

00:25:58 [AB]

It was basically just give an example, a concrete example. So where the sum is, shall we say, X1 plus X2 plus X3 plus X1, and so on, until the end of X, then what if I don't want plus? What if I want plus two times? So X1 plus two times X2 plus two times X3, and you keep adding like this. How would you do that? But it sounds like that's not something you can do, right?

00:26:30 [ML]

Yeah, well, it sounds to me like it's kind of a downside of the GPU model, where, I mean, on the CPU, you can have a C function that takes a function pointer, even, and that's not going to be the fastest thing, but it won't be that slow. And on the GPU, that's like, that just basically doesn't work.

00:26:50 [UA]

Yeah, so that's the interesting idea, because you can do composite operations, right? Because you can do a multiplication ahead of time and then do the reduction afterwards. So you have to come--

00:27:00 [AB]

Oh, then I should explain a bit further. I didn't spell out the parentheses. Obviously, if you just need to multiply it by some factors, that's-- but here we're saying, if you think of it as X1 plus two times open paren, X2 plus two times open paren, and so on, and so on, and then a whole bunch of those parens at the end. Or you could turn it around and have the parens on the left instead, that kind of thing, where it's a custom function that does not immediately map to something you could compute in two steps.

00:27:32 [UA]

No, you're right. I think for that, you would need to perform your own approach to that. You can code it, but it's not going to be a composite operation. Even though we do combine operations together in a runtime JIT sort of way, we can't do something like that.

00:27:51 [CH]

Yeah, we'll throw this in the show notes, too. I found-- well, I found-- I googled my way to the reduction operations page of ArrayFire, and sure enough, they've got all true-- and this isn't all of them, because I'm not going to bore you with the list here-- but all true, any true, max, min, some prod or product, and then some by key versions of those. So yeah, it's definitely like Umar said. The curious thing is I wonder what Aaron does for this, because in APL, you can definitely program a kind of bespoke or custom reduction.

00:28:26 [ML]

You can use these custom reductions, but you don't get the full-- in a traditional array language implementation, that implementation is going to recognize in special case folds like sum and max and whatever. And so if you don't use those-- and we probably have a wider set that's recognized generally than ArrayFire, just because they're-- I mean, array programmers are liable to do all these weird reductions. But it's not like massively larger. And if you don't use these, I mean, you get more interpreted kind of Python-like performance, Python without NumPy. So in my mind, they don't really belong to array programming as much when you have a just arbitrary fold.

00:29:07 [CH]

And Bob, you were going to say something.

00:29:09 [BT]

As a way of thinking about it, is it more like in J there would be adverbs or conjunctions, and the adverb is actually that part which would be a reduction or a scan. And then the operator that goes with it is the verb that you're applying to it. It sounds to me like with ArrayFire, when you're thinking about these things, you have to sort of take adverbs and conjunctions out of the equation, because you're really working with the basic functions at the GPU level. Is that accurate, or am I starting to build the wrong construct there?

00:29:39 [UA]

If I understand you correctly, I think you're right. You have to think about ArrayFire as a library. So we're not really compiling operations together. So if you have a custom type, we're not going to be able to access that custom type. But if you numerically define your operation, you can do it that way.

00:29:55 [CH]

Yeah, this is really interesting. And I guess it's a good segue into my satisfying my curiosity, because you did mention JITing a second ago. [04] And I think in that context, you were mentioning that you do have some kind of ability to fuse operations. And that's one of my things that I miss when I go to a lot of Array libraries, and even Array languages, for that matter, that I know that I've talked to Pierre and Oleg, who are two -- I guess, do you call them compiler engineers? They work on the interpreter for a language called q, which is used a lot in finance. And they have always said that they wish that there was a type in q that enabled you to kind of fuse or stream operations together. Because one of the downsides of using a library like NumPy is when you're doing something very simple, like you've got a matrix or an array, and you do add a number to it, multiply a number, et cetera, and then do a reduction at the end of the day, each one of those is doing like a separate allocation. You're basically creating a whole new array for a very simple thing. And I know NumPy does have some decorators that you can add to functions for JITing. And every library basically in Python has something like this. Jax has a decorator for fusing. CuPy, which is a CUDA version of NumPy, has a fuse decorator. By default, you don't get any of this JITing and fusing. But in C++, it's a lot different, right? Because we don't classically have any JITing capabilities. So you've got to do something different if you want. Does ArrayFire -- it sounds like they do -- you guys have thought about this. What's the story about if you want to do some kind of multiple operations and that boils down to a single kernel? Is that something that's recent? Tell us a little bit about that.

00:31:47 [UA]

Yeah. So we've been doing JITing with ArrayFire since the beginning. We knew ahead of time that, you know, every time you launch anything on the GPU, there's going to be some overhead. The driver has to set the context. You have to allocate extra memory. You have to allocate data memory for intermediate operations. So we had designed ArrayFire with JIT in mind from the beginning.

00:32:14 [ML]

So you knew ahead of time that you needed to compile just in time.

00:32:19 [JM]

Yeah, I caught that too.

00:32:20 [UA]

So whenever you perform an operation in ArrayFire, so for example, an addition operation between two matrices, ArrayFire will record that operation and that array that is returned, it's going to be a symbol for that operation. And whenever we cannot go forward with that operation, so for example, if you're doing a special type of sorting or something where you need the values to be evaluated, we will then go through that operation tree and generate a new CUDA kernel, OpenCL kernel or SYCL kernel and compile it at runtime and then execute it. And then pass that data to the next operation. So everything that is handled transparently in the background.

00:33:13 [CH]

Interesting. Does that happen by default or do you have to opt into that behavior?

00:33:17 [UA]

No, that's done by default. You don't have to do that.

00:33:20 [CH]

Oh, wow. Across all the backends, you were saying, too.

00:33:22 [UA]

Not just across all the backends, except for the CPU backend, where it's a little bit more tricky. We can do it there. We have concepts of a plan there, but we haven't done the work.

00:33:34 [CH]

Interesting. Is this trade secrets or is this all part of the open source stuff that you're able to talk about how this happens? Because that's a really impressive property of being able to say that the user doesn't need to think about this. You just go ahead, write your code, and if it's possible, ArrayFire will do the right thing.

00:33:54 [UA]

Yeah, exactly. So we have to take into account the limitations of the hardware, of course. So, for example, some GPUs will have the ability of processing larger kernels than other GPU kernels, but for the most part, we'll handle that transparently. Of course, there are some downsides to the transparent approach, but we have the necessary functions to enable you to trigger that evaluation ahead of time.

00:34:28 [CH]

Interesting. John, I saw you were maybe going to add something there. Do you?

00:34:31 [JM]

Yeah, no, that's probably one of the things we're known for the most. We had this JIT compiler from the very beginning, so like 2007, we were already JIT compiling CUDA kernels from MATLAB code onto the GPU. And we had a lot of competitors at the time, because we were, especially in the MATLAB space, including Mathworks themselves, they tried to make an initial version that sort of competed with what we did, but nobody had JIT. And if you don't have JIT, then every single function call you're doing round trip memory transfers and kernel launches, and it's slower than just using the CPU. The overhead is so steep. And so, it's been, especially in a runtime language like MATLAB, that really matters quite a bit. And also Flashlight, C++ version of, they did comparisons of Flashlight versus PyTorch versus TensorFlow. And also the JIT of ArrayFire is outperforming the JIT in TensorFlow and PyTorch as well. It's one of the things we're most proud of, because we've been just optimizing that thing for all, it's been 18 years now.

00:35:43 [CH]

I'd be curious, have you guys compared it with JAX? Because I've also done some benchmarking and profiling of PyTorch, TensorFlow, and JAX. And this is my personal observance, this is not NVIDIA saying anything, but JAX is, in my experience, it's had the best kind of performance profile. Because I think JAX was designed after the fact, that there were some issues with the way that PyTorch and TensorFlow were designed from the beginning that puts limitations on the upper bound of how much performance can you get out of this model. So then that's kind of where JAX and XLA came in. Have you guys tried to compare ArrayFire?

00:36:23 [UA]

We've done some benchmarks. I think we're right there with JAX, we have similar performance profiles, that library, I think we do similar things. I've read their blog post, they ran into many of the same problems we ran into when we were building it. So we'd been doing JIT way before JAX came to market, though.

00:36:45 [JM]

Yeah, the specific benchmarks I was quoting came from a paper from Meta, and they only compared PyTorch and TensorFlow and had hard numbers on it. But everything else is sort of like you're saying, just not as well benchmarked experience.

00:37:03 [CH]

Yeah, I can't remember the paper. Someone, I think it was actually an ArrayCast listener, I might have been talking about Rust or something. And someone sent me something. And similarly, yeah, they benched this Rust project, benched PyTorch and TensorFlow. And I was like, well, what I really care about is JAX, because they're the best in class for this kind of fusion work, at least in my opinion.

00:37:24 [JM]

Yeah, at least in the most recent years.

00:37:27 [CH]

And I do have another question, but my curiosity is satisfied for the moment. So I'll once again, I'll take a pause to see if the other panelists, I see Bob is, what do you call that, stroking his beard?

00:37:42 [BT]

Well, I feel like I'm getting in the way of some really interesting stuff. So I don't want to, I mean, my stuff is sort of more general. I mean, I guess the question right now that I've jumped in, I guess I have to ask this question. What's the community like for ArrayFire? Like, is it active? Are there lots of people doing stuff with it? Do you have interactions with other communities like the JAX community? How do you guys see your place in sort of the computing world? Where do you fit in? And what's that community like?

00:38:18 [JM]

Right. It's been, you know, being in the space for so long, there are very few that maintain a presence with us for the whole ride, right? But there are a lot that come in every year and spin up because they're interested in a particular project and have a particular need, and they become active and prolific users for a period of time for the space of the project in which they're working. And similarly, partnerships with other languages or other libraries or other open source projects are ongoing. And one that comes to mind is Julia, who in the early days wanted to have GPU support and didn't want to build it themselves from scratch. So they came in and created Julia wrappers for ArrayFire and maintained those. And we didn't have to do any of that work. They just sort of picked it up and ran with it. Similarly, some from Anaconda came to us at the early stages of Anaconda and wanted a GPU support. And the initial versions of NumPy sort of came from ArrayFire and inspiration from ArrayFire. And I happen to be close personal friends with Travis Oliphant, who's the original author of NumPy. And he was with Anaconda at the time. But yeah, so it's been a really cool community. Honestly, NVIDIA GTC has been the place that we go the most to sort of interact with our community. I still go there. I've been to every single one of them.

00:39:47 [CH]

Oh, wow. And how's that been, like, changing over the last...

00:39:51 [JM]

Oh, my gosh. You know, the very first NVIDIA GTC was not called NVIDIA GTC. [05] It was called Nvision.

00:39:57 [CH]

Yes.

00:40:00 [JM]

And it had more video game... It was a video game conference with some science in, like, a little wing. And the video game guys and the science guys could not have been in, like, a different... I mean, there were a lot of similarities, but a lot of differences, too. So the video games guys were brought in couches and were trying to set a Guinness Book of World Record for the largest continuous LAN party or something. So they were just playing nonstop on these couches in one side of the room. And then we were showing off MATLAB simulations. And there were a couple other fluid dynamics simulations and stuff on the other side of the room. And our side of the room all went to bed. Their side of the room just stayed through the night playing video games the whole night. And if they slept, they slept in their cars just on the street. It was just a really interesting and fun show. But that sort of spirit of this excitement made GTC really special. It's matured over the years from video games to now more science-y. And now it's AI. So it's got business... It's a very business conference. Deloitte was one of the biggest sponsors. So it's really migrated.

00:41:13 [BT]

My guess is there's not a lot of sleeping in cars anymore.

00:41:18 [JM]

No, not a lot of sleeping in cars. I mentioned that to people as I walk around. I was like, I really miss the days when you'd walk by the McDonald's and there'd be 50 cars with all kids sleeping in them. Yeah, they just came in from everywhere. And really just the early enthusiasts for NVIDIA GPUs.

00:41:37 [BT]

And what about working with open source? I mean, the story I've heard is that the whole internet is based on some guy in North Dakota maintaining this little sliver of open source code. What do you guys think about that sort of thing? I know you've approached it, I think, probably in a more sustainable way. But talk to me about that.

00:41:55 [JM]

We had this really scary experience of going from a... All of our revenue was selling this MATLAB product. And then overnight, we had to flip and go open source. And when you push that button on this code that for five years you've kept proprietary and was your secret sauce, and you were out competing other people because you have this JIT compiler, and then suddenly you push this button and now it's open. It was a really interesting experience and going through all of that. But it was a beautiful thing to build this community. And just the vibes in the office changed and people just had a lot of fulfillment in the interactions on GitHub and just interacting with the community. And in hindsight, we should have gone... Honestly, I love open source so much. I feel like so much more software should be built in the open, especially science and engineering software. And you can get miles further ahead in your work by having more people, more eyeballs on your code, just makes it better.

00:43:05 [BT]

And I've heard people talk about the fact that when you're working open source, there's no restrictions on publishing because basically you're publishing as you produce it.

00:43:13 [JM]

Exactly.

00:43:14 [BT]

So there's a lot of things you can do and get information out there and get that feedback loop going. That if you're in a silo, you can't do it.

00:43:23 [JM]

YYeah. Just getting PRs from external people just randomly. And when you see the thought and effort that they put into it, there's someone you don't even know that's contributing to the thing that you've worked on for a long time. It's really touching.

00:43:35 [BT]

So you're using the service part of it to basically sustain that. I guess it's changed now that you're working with Intel, but up until that point, you'd been working with the service end of it.

00:43:46 [JM]

Yeah. It's still pretty much the same. It's just that Intel employs four of the maintainers. So at least we don't have to pull money from the open source project anymore. So there's more stability for the core maintainers. And then we have a set of consultants that are spread throughout mostly throughout the US and they work on the project when they don't have a consulting job so that they can maintain income. And when they do have a consulting job, then they go work on the consulting job and it's sort of back and forth and keeps the cash flow going for the other maintainers.

00:44:24 [CH]

Yeah. I was going to ask, maybe you could say more about, you mentioned there that you wish you actually had gone open source sooner. And I know of folks that have closed source projects and they're generating revenue from this product, but they've considered going open source, but there's this fear of, well, if I just put my code out in the open, what are people going to pay for anymore? But you said you've gone through that process, it was successful. And in hindsight, you actually wish you had done it earlier. So for the folks out there that might be considering it, say more about that, because I think that's a story that not a lot of people have actual lived experience that they can talk to.

00:45:07 [JM]

Yeah. I think in a lot of cases, keeping your code closed is not the thing that's giving you the competitive advantage. It's your execution speed, it's your attention to customer, attention to your customers. It's the kind of product that you're building. And it's really, really hard, especially as technical spaces we're in for anyone to go and copy and somehow replicate the thing that you're doing. But it is very helpful and gives us a competitive advantage to have an ecosystem that's built around an open product, to give our customers the reliance that this thing is open source, that the rug's not just going to get pulled out from under them. And so in hindsight, there's just so many more benefits, I think, to being collaborative versus competitive with how you build software.

00:46:01 [CH]

Yeah. When I joined NVIDIA, NVIDIA is not famous for being the most open source company, but that culture is changing. A lot of our libraries now and teams that are developed, when I started at NVIDIA, it was on a 100% open source team. So my workflow was through GitHub. Technically, we have an internal GitLab, but I never used that because my work and the PRs that I opened were on the open source library. And it's an awesome feeling to be doing that work. But then also, too, heaven forbid I ever leave NVIDIA, which no plans to do that anytime soon. It's a great company. But you can point at your actual work. You can be like, "What did you do?" And it's like, "Well, there's my history of my PRs." Yeah, it's fantastic for a number of reasons. Awesome that you guys had that experience.

00:46:49 [JM]

Yeah, it's great for employee satisfaction and just letting people showcase their life's work. Intel's the same way, and that's one of the reasons we... I never would have thought of joining Intel back in the days when it was entirely proprietary. But Intel's been humbled, and the OneAPI plan is sort of new. This new concept of releasing public code and doing everything in the open is something when I saw that they had a change of heart that way, I was like, "Well, I want to go support that." And like you're saying, I think it's something that more and more companies are catching on to, especially when it's not... These are hardware companies, and so it just makes sense to give customers the opportunity to collaborate on the software a little more.

00:47:41 [CH]

Yeah, I mean, when you look at the... What do you call them? The Mag 7 -- whatever the term on the street for the large companies. But I remember talking to someone at Google once that was talking to someone that was upset that they didn't do more open source work. But the person was like, "What are you talking about?" And they just list it off. They're like, "I don't think you're aware of all the work, like Meta and Google now." It's almost by default, even if they have some internal thing, their long-term plan is to release it to the wild. Go, for instance, it's not a Google project anymore, but because it started there, people think, "Oh, Go is the Google language." But a lot of these things, and to a fault, actually. I think was it Kubernetes or one of the technologies that they handed off to the CNCF or whatever it's called, that some business folks, they think that that was actually a mistake because they gave away so much value. They owned the thing that became the industry standard. But a lot of these companies, it's been such a good choice for them, historically speaking, that they don't think twice about it, even if maybe they actually shouldn't have done it for competitive advantage reasons.

00:48:51 [UA]

Right.

00:48:54 [JM]

Yeah. Some of the short-term gains versus long-term goodwill is a calculus that people don't see the long game as readily sometimes, but it's real and powerful.

00:49:06 [AB]

Completely agree. The hardware companies, they make the money on the hardware, then they are able to support the open source software. But if you have a company that doesn't have the hardware part, then that's not the case. Another, I guess, the early open source company was IBM. IBM completely controlled the hardware market, and the software was just something that was shipping along with that.

00:49:34 [JM]

Yeah. I spent a lot of time trying to figure out how to make money in open source as a software company, like you're saying, and we weren't a hardware company. You really have three options. You can do services like we did. You can sell some sort of support, which still boils down to services. You can try to make a premium product too, but then that's also more going closed. Or a lot of companies will just go after government grants and try to get funded by the government. But that's no way to run a long-term business. It's really you're subject to the broader macro government funding environment and grant success rates of 10%. We did some of those too. But at the end of the day, just providing services to the customers that need it the most seemed to be the most stable.

00:50:27 [AB]

We have this thing at Dyalog, [06] quite often get questions from people, "Why don't we open source the interpreter?" Almost all our APL code is open source. The things I work on is all open source stuff. We have very little that we sell. But none of the things you're mentioning would even work for us, or we would have massive restructuring. We do have a couple of people that do consulting. Basically, they're rented out more or less full-time to other companies. We do have support calls. We do have support subscriptions, you could say. But that is part of buying the product. You get the support with it. We do try to do exceptionally well in the support department. We might not be the best at speaking, but at least you can get to us easily. Like we don't call up our call center and get a message that a lot of people are calling right now. You get to the expert on the subject you're asking about right away. But by far, most of the man hours at Dyalog goes on actual development and documentation and dealing with actually developing the product. If we didn't charge money for it, then we wouldn't be able to all work full-time like this.

00:51:53 [JM]

Oh, for sure. Yeah. Yeah. Yeah. It's a tough balance. Especially when it's sometimes easier, I think, for people that run web services or something, where you can do a SaaS model and just have a subscription running. But if you're doing installed software, it's really difficult in this day and age to sell installed software.

00:52:15 [AB]

Programming language as a service doesn't sound very palatable.

00:52:21 [CH]

The problem is that 99% of programming languages are free these days. So it's a real uphill battle. It's one thing for libraries. You can think of examples. I mean, ArrayFire, I guess, is one of them. But yeah, when I try and think of programming languages, Clojure and Julia are the two that come to mind. And they basically both did the services thing. I think they call it the Julia Computing Company or something like that, or scientific company. And I don't know a ton about that, but I get the impression that it's the same kind of model where you can hire experts and pay them to help build a system or something like that.

00:53:02 [JM]

Yeah. And then the elephant in the room is MATLAB, that sells $1.2 billion a year in software licenses for array-based programming. And if you think about the total spend of the addressable market for array-based languages, they're 90 plus percent of the whole thing. And it's crazy that that happens.

00:53:24 [CH]

Do you think that would be possible starting out today? Because when I hear that, I'm like...

00:53:31 [JM]

No, no, I don't think so at all. I think they started in the 70s. And they're so entrenched in the schools. And then they move, especially in defense contractors. And a lot of these shops just rely heavily on MATLAB. And they do a really, really good job at just making life easy for the programmers that use their product. So it just is a cyclical...

00:54:02 [AB]

It's interesting how the mathematical array programming languages are the ones that people are willing to pay for them, but people are willing to sell them rather than making them free. So it's not just MATLAB, right? Mathematica, a Wolfram language is also very closed. And k, at least the commercial parts of that, and APL as well. I don't know if that just means that all the array programmers have equally bad ideas about business, or if those languages are so valuable, those are the ones you can sell and nothing else.

00:54:40 [JM]

Yeah. Yeah. Mathematica and MATLAB were definitely born in the boon of installed program, installed software. And so they still are running that. And they're having to adapt and go online and sell online subscriptions to the software too.

00:54:57 [AB]

And why is it that Octave doesn't eat MATLAB's lunch?

00:55:01 [JM]

It's just not as well... The customer experience is not very nice in Octave. It's just... And it's improved over the years, but it's more than just the language. It's the whole... The examples in the documentation and just everything that makes it... Even just the IDE and how nice the IDE is. There's a whole very long tail of engineers that really want the simplicity and that helps them quite a bit.

00:55:35 [AB]

I guess I should have known the answer to this question because GNU APL doesn't eat the lunch of other APLs either.

00:55:41 [BT]

Well, and I wonder some of it has to do with the fact that, and it's sort of true, I think of ArrayFire, when you were talking about your JIT compiling as well, you've had years and years of crafting this. Nobody's going to come in new and do a better job of it. You have that experience. So you're building on something that people can't take away from you. They can use the experience you've gained, which is the open source part, but you still have those skills. You still have that experience that gives you that edge in a competitive environment.

00:56:14 [JM]

Yeah, exactly. Exactly.

00:56:16 [CH]

So you commented on Octave. What has been the Julia versus MATLAB? Is it sort of the same thing? I mean, Julia, I think it's not a disagreeable statement to say that Julia has been more successful than Octave has been. But $1.2 billion is still a lot of money to be generated by that product.

00:56:42 [JM]

Yeah. I think Julia is great. I think Julia keeps growing and has had tremendous success. But like you said, I don't see Julia being... It's really, really difficult. I don't know that any new product is going to be able to come in and sell as much installed software. People just aren't buying that way anymore. And when you're doing services, like you mentioned, the services just are not... You can't scale services businesses like you can product businesses.

00:57:17 [CH]

So getting back to ArrayFire here, as much as I love the discussion about open source and also, too, I've spent time thinking about how do you build a business around a programming language and I've come to the conclusion that it's just very, very difficult in 2025 to do that. So if folks are interested in taking ArrayFire for a spin, what's your recommendation? Because you mentioned that with the release of ArrayFire 3.10, there's going to be the Python way to consume it. What is, from both of you, what would you recommend people do if they want to take ArrayFire for a spin? Is it via C++? Is it via Python?

00:57:39 [JM]

Yeah. So just directly from ArrayFire.com, you can click on right on the home screen, there's a... It'll launch a... What's the Google service? Colab? Colab. [07] Yes. Yes. If you go to ArrayFire.com, it'll launch a Google Colab, which will load an ArrayFire set of instructions that will do the pip install and download the ArrayFire binary and then give you some sample code and you can just literally play everything and it'll run on an NVIDIA GPU that's just right there in the cloud. That's the easiest way to get started in Python and we'll update that with the new Pythonic version that's data API compatible once we release ArrayFire 3.10. And then also just from that same website, you can get the ArrayFire binaries for free and those install on your computer and then we have... You can build with it and build the examples and run the examples and just sort of get started. If you want to be a more experienced user, you can go to GitHub and get the source code and build from source. But yeah, we have the prepackaged binaries on the website and then the Colab for the Python space.

00:59:15 [CH]

Awesome. And I'm not sure how much you can speak to this because my guess is that a lot of the future direction of what's happening is kind of community driven and issue driven. But are there plans for 3.11, 3.12? Is it mostly going to be focusing on... I imagine if Intel is employing maintainers, they have an interest in building up the SYCL backend and stuff like that. But is there a short-term, long-term roadmap for stuff that's happening in ArrayFire land?

00:59:45 [UA]

Yeah, we have a plan on continuing our release, updating our source code to support all the new hardware with all the new features. We have a strong relationship with NVIDIA. We have monthly talks with them and they're a strong partner. Even though we work at Intel, we have a strong relationship with them.

01:00:05 [CH]

I have another podcast with an Intel employee, so there's no hate between Intel and NVIDIA, when it comes to me at least.

01:00:06 [UA]

Yeah.

01:00:13 [JM]

Yeah, especially on the software side, it's always fun to collaborate and work across companies that way.

01:00:20 [CH]

Awesome. I mean, I'm exhausted. I've asked all of my questions and more. Any final questions from... It looks like, yeah, Bob's got one more.

01:00:30 [BT]

I do have a final question. This is going to sound a little bit weird, but when you mentioned starting out the fact that you were using MATLAB and ArrayFire to be able to process MRIs of brain scans and huge amounts of data, and I guess the obvious place now would be in AI, is that's where there's huge amounts of data. When we're talking about really, really large amounts of data, is there any thought given to essentially trying to economize, to make dealing with that much data as efficient as possible? I'm thinking in terms of environmental concerns and all the other things that people are so concerned about AI creating almost a whole new country of energy consumption. Are there thoughts or are there things that you can see on the horizon that might be able to make that more efficient?

01:01:18 [UA]

Wow, that's a tough question. I think people are working on making AI more efficient using quantized weights and so on. At Intel, we do a lot of work with reducing the memory overhead of different operations. I think there's a lot of work going on making it more efficient. I think we will get there eventually. It'll take some time. Right now, we're on the exploration side of AI, and hopefully, we'll refine that in the future.

01:01:53 [JM]

Yeah, you reminded me of a story. Last year, I had the opportunity to go to Richard Branson's island. [08] He's like a grandpa now. He's not heavily involved in business, but he goes on bike rides three times a week up this really steep mountain. I'm riding this bike with him, and I'm trying to keep up with him. He just keeps going. I'm the only one that ends up keeping up with him. I have a half an hour with him at the top of this mountain. He knew before we went up there that I'm building AI libraries and whatnot. I'm hoping that maybe he'll have some introductions, or there might be some interesting conversation around this. He looks me straight in the eyes and he says, "How do we reduce the carbon footprint of AI?" He was really concerned about the energy usage that we're throwing at this problem. I don't have a great answer for that. I don't think any of us are going to be able to curtail the appetite for people to throw data into large racks and crank through enormous power bills to produce these AI models. I think we can, by continuing to iterate on tools, make things more efficient. The more efficiency you have and the more performance benefits that you get, the less time you spend and waste in the data.

01:03:20 [BT]

I'm guessing that part of it is the fact that you're running on a GPU already. Can you imagine trying to do this stuff on a CPU? How much power that would consume? Not just the time, but the amount of power it would take would be immense. You made that first step. I guess the whole thing is, what are we using this for? If it's used for a useful purpose in AI or it's used for analyzing MRIs or stuff like that, that's probably not a bad effect of it. If it's being used to generate cryptocurrency, maybe that's the issue as well.

01:03:55 [JM]

Hopefully, some of the outcomes will be in material science and in other areas where we can learn how to reduce things, even in ways that are breakthroughs. It's really incumbent upon humanity to use these things in wise ways.

01:04:13 [CH]

It's a billion-dollar problem. The good news is that whoever solves it or whatever company solves it is going to make a lot of money. It's only a matter of time, I think, before it ends up happening.

01:04:26 [BT]

Yeah, it might not be about money. It might be more valuable than money to solve that problem.

01:04:33 [JM]

Yeah.

01:04:34 [CH]

We both live in Canada, Bob, so I think we are closer to caring about that kind of stuff. Not everybody does, but if it's going to make someone money, then for the wrong reasons, they're going to solve the problem that we care about. Anyways, thank you so much, John and Umar, for spending all this time with us. I've learned a ton more, and hopefully we've inspired some of our listeners. I'm sure a couple of them already indirectly have been using it through the J add-on and Aaron's CodeDefense compiler, but potentially there's some folks out there that have their own project now, and they're going to go and take ArrayFire for a spin and try hooking it up to their personal project. This has been a blast, and I've learned a ton. If listeners that are currently listening have questions, either for us or for John and Umar, you can send those questions, comments, thoughts to...

01:05:27 [BT]

Contact@ArrayCast.com is the way to get in touch with us. My guess is we'll be hearing things from Raz about what we've said about Julia, but I'm not sure... Well, no, I'm pretty much guaranteed he'll probably respond to this. He listens. It was a past podcast that we were talking extensively about Julia. A shout out to our transcribers. Adám does the initial pass to give us all the transcription speakers and everything, and then the last while it's been Sanjay and I have been working on it, and I think Igor is going to come back in again to do some more work with us. But certainly hats off to those guys that are creating that, because people consume the podcast through a number of different ways, and we appreciate all the input we get back. And yeah, thanks for listening, and that's about it.

01:06:21 [CH]

Yeah, thanks so much again, John and Umar. Hopefully we'll, or at least for me, we'll run into each other at a future GTC.

01:06:28 [JM]

Yeah, yeah. Thank you. It's been great.

01:06:29 [UA]

Thanks for having us.

01:06:31 [CH]

And with that, we'll say happy array programming.

01:06:33 [All]

Happy array programming.

</details>
