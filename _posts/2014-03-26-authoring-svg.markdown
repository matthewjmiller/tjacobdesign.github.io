---
layout: post
title: "Authoring SVG"
date: 2014-03-27 10:25:00
---

SVG (aka Scaleable Vector Graphics) is a programming language for drawing images. It’s a pretty difficult language to learn, and it has a lot of quirks, so most people don’t bother even trying to write it. We use programs that make it easier, like [Adobe Fireworks](https://www.adobe.com/products/fireworks.html), or (my personal favorite) [Bohemian Coding’s Sketch](http://bohemiancoding.com/sketch/). And they do the job well, they give us images that scale to be as big or as small as we like. But they aren’t enough.

## Why Would You Ever Code Pictures?

There are a bunch of different ways to store and display images on the web. The big names are <abbr title="Joint Photographic Experts Group">.jpg</abbr>, <abbr title="Portable Network Graphics">.png</abbr>, and <abbr title="Graphics Interchange Format">.gif</abbr> (yes indeed, .gifs are well known for animations and cats). Those three formats all work very differently, but they share one thing: They’re just a storage medium for pixels. They store every pixel on the image (give or take) as a color, and the computer merely has to read through those colors and build the image.

SVG doesn’t do that. Instead of storing individual pixels, SVG stores shapes. For example, SVG has a `rect` element. Given the correct information, that bit of code draws a rectangle. There’s also a `circle` element, an `ellipse`, a `line`, and so on and so forth. SVG constructs an image through the use of these shapes, rather than dumbly rendering just one pixel at a time.

### Why is SVG Useful?

SVG has a few strengths over traditional image containers:

#### Infinitely Scaleable

It’s even in the name: it’s scaleable. We’re telling the computer to draw a shape, not a pixel, so it can keep the edges of that shape nice and sharp for us.

<p data-height="268" data-theme-id="5360" data-slug-hash="KBbpd" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/creativembers/pen/KBbpd/'>Blinking, flapping, pecking chickens</a> by Creativembers (<a href='http://codepen.io/creativembers'>@creativembers</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//codepen.io/assets/embed/ei.js"></script>

(click “Edit in CodePen” and try resizing the window)

#### Dynamic Data

SVG is great for graphs, because all you have to do to change the graph is give it new numbers. We can change the image based on any data we like, and change that data whenever we like. No photoshop required.

<p data-height="399" data-theme-id="0" data-slug-hash="EqKit" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/tjacobdesign/pen/EqKit/'>EqKit</a> by Timothy Miller (<a href='http://codepen.io/tjacobdesign'>@tjacobdesign</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//codepen.io/assets/embed/ei.js"></script>

(plus it makes hover effects really easy)

#### Easily Animateable

Animation with other image formats is really precise, but kind of a pain. I have a confession to make: I get the shivers when I think about drawing frames. Good news for me then, SVG handles that too. All you have to do is tell it where to start and where to end, and it draws all the frames for you.

<p data-height="350" data-theme-id="5360" data-slug-hash="EmCoa" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/agrimsrud/pen/EmCoa/'>SVG Pie Timer</a> by Anders Grimsrud (<a href='http://codepen.io/agrimsrud'>@agrimsrud</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//codepen.io/assets/embed/ei.js"></script>

(this one is a little more complex than that, but still no frames)

### And Another Thing

SVG works out-of-the-box for high definition screens. That may not be a big concern right now, but with [sub-$1000 4K displays coming](http://daverupert.com/2014/01/4K-RWD/) we’d better be ready to scale in a big way. SVG gives us a good way to do that.

## So Jump on the SVG Band Wagon

[Here’s a good way to get started](http://css-tricks.com/using-svg/). It doesn’t involved actually writing any SVG, but it’s a good way to start thinking about it. We’ll get into the nitty gritty in future posts.
