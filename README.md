What You Will Learn
I mentioned previously that I’ll be equipping you with some new tools and techniques. Let’s flesh these out.
InTroduCTIon  Tools
On the tool end of things, we’ll be using the following:
•	JavaScript and the SvJs library. I’ll elaborate on this further later.
•	A code editor. Here I’ll be giving you a choice between
•	Visual Studio Code (an excellent open source code editor)
•	CodePen (a popular online code editor)
•	If you opt to use Visual Studio Code (which I recommend), we’ll also be using Node.js and NPM to manage dependencies (a good habit to get into as a developer).

All code examples are available on both GitHub and CodePen, so feel free to follow along whichever way you prefer. You can of course do both, work locally with a code editor but check out CodePen examples online for quick inspiration. For convenience, I’ll organize and embed all CodePen examples at davidmatthew.ie/generative-art-javascript-svg.

## Techniques
In terms of the techniques we’ll tackle, by the end of this book, you should have a good overview of the following:

•	The main functionality of the SvJs library and how it relates to the SVG spec
•	Creating generative art sketches with JavaScript using ES6+ syntax
•	Generating primitive SVG shapes

## InTroduCTIon
•	Creating iterative variations of sketches by randomizing parameters
•	Using noise to create organic variance
•	Generating complex SVG paths
•	Making sketches interactive
•	Animating sketches
•	Using SVG filters generatively

We’ll be covering a lot of ground, so don’t put yourself under pressure to understand everything. I must have encountered certain programming concepts 
umpteen times before the proverbial penny finally dropped (JavaScript promises anyone?), and whenever understanding did finally dawn, it would usually be because I was experimenting with something I wanted to build, rather than repeating tutorial steps by rote. Tutorials and instructional books certainly have their place (I wouldn’t be writing this book otherwise), but it’s important that you take what you want from them, rather than seeing them as syllabi to be strictly followed.
A sense of play is important, particularly when it comes to art. And although I mentioned tools previously, I would prefer if you viewed this book as more of a toybox than a toolbox. When I think of tools, I think of problems that need fixing, like the loose hinges on that crooked cabinet you’re going to tighten any day now. Tools tend to be more functional than fun, and I’d like you to have some fun with this book.

# CHAPTER 1
## The Beginner’s Path
Before journeying along any path, the groundwork needs to be in place. In this opening chapter, that’s what we’ll do, lay the groundwork. We’ll introduce SVG, explain what makes it a uniquely powerful image format, and show how it can be used with JavaScript to create generative art. In the process, we’ll set up our tools and a template we can use for subsequent sketches.

 ## Why JavaScript and SvJs?
Most books about generative art use a Java-based language called Processing, or its JavaScript port p5.js. Processing was created specifically for artists and designers new to coding and has a large and active community. So why doesn’t this book use it?
My first forays into generative art were with Processing, so I certainly acknowledge its value. I quickly moved to p5.js when the library was first released in 2013, which allowed generative sketches to be written directly in JavaScript, the language of the Web. But when I wanted to integrate some of my own sketches into real-world web development projects, its limitations quickly showed. It’s a large library, clocking in at close to a megabyte at last check, and while that may not sound like much, it’s a lot by web development standards.
© David Matthew 2024 	1
D. Matthew, Generative Art with JavaScript and SVG, Design Thinking,  https://doi.org/10.1007/979-8-8688-0086-3_1
The p5.js library is built on top of the HTML Canvas API, which I soon discovered is actually quite straightforward to use. Using this API directly, I was able to achieve much the same results as with p5.js, so that became my go-to. However, the output of all my sketches – p5.js or Canvas – was still resolution-dependent bitmap graphics, devoid of any semantic content. What does that mean, and why does it matter (to me at least)? Let me explain.

## Introducing Scalable Vector Graphics



