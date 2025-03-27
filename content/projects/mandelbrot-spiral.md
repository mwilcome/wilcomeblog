---
title: "Mandelbrot Spiral Project"
date: 2025-03-06
author: "Mike Wilcome"
---
# Mandelbrot Spiral

I built a project called `mandelbrot-spiral`. This was a "lunch break" project today. It’s a visualization of the Mandelbrot set that zooms in fast with a spiral twist. Wrote it quickly with Grok (xAI) helping in JavaScript using p5.js. The idea came from messing around with the Mandelbrot set—wanted to see it move, not just sit there. Took some trial and error to get the zoom right, but it’s out on GitHub now: [mwilcome/mandelbrot-spiral](https://github.com/mwilcome/mandelbrot-spiral). Here’s what it’s about.

The code runs a loop that calculates the Mandelbrot set for an 800x800 canvas. Each pixel maps to a complex number, and I iterate it to see if it stays bounded or shoots off. Then it zooms in toward a spot at (-0.75, 0.1)—picked that because it’s got cool spiral patterns. The zoom’s exponential, tied to a time parameter, and the center spirals in with some trig functions. Took a bit to tweak the speed; started slow, but now it dives in fast, like 400x in 10 seconds.

Here’s the first GIF showing how it starts and kicks into the zoom:

![Mandelbrot Spiral Start](/images/mandelbrot-1.gif)

### Mandelbrot Set Details

The Mandelbrot set is a set of complex numbers defined by a simple rule. For a number \( c \), you start with \( z_0 = 0 \) and iterate \( z_{n+1} = z_n^2 + c \). If \( |z_n| \) stays under 2 after a bunch of iterations (100 here), \( c \)’s in the set. If it blows up, it’s not. The magic’s in the boundary—crazy fractal shapes pop out, self-similar and full of spirals.

In this project, each pixel’s a \( c \) value. I map the canvas to a chunk of the complex plane, say -1.5 to 1.5 at first. For each pixel, I run the iteration and count how many steps before \( |z| > 2 \). That count sets the color—black if it’s in the set, a gradient if it escapes. The zoom shrinks the view with \( \text{scale} = 1.5 \cdot e^{-0.2t} \), and the center moves like \( c_0 + 0.75 \cdot e^{-0.2t} (\cos(0.15t) + i \sin(0.15t)) \). The exponential drop makes it zoom fast, and the trig gives the spiral. It works because the set’s fractal nature means there’s always more detail to see, no matter how deep you go.

### Why p5.js?

Used p5.js for this because it’s good for quick canvas stuff. It’s a JavaScript library that handles drawing and animation without a lot of setup. Just load it from a CDN, and you’re off. The pixel manipulation’s straightforward—set colors directly with `set()` and push them out with `updatePixels()`. Made tweaking the zoom and spiral easy, though it’s not the fastest for heavy math. Still, for an 800x800 grid, it holds up fine on decent hardware.

Here’s the second GIF, showing it deep into the zoom where the spirals really show up:

![Mandelbrot Spiral Deep](/images/mandelbrot-2.gif)

### Wrap-Up

It’s a small project, but I like how it turned out. Shows off some math, some coding, and a bit of visual tinkering. The repo’s got the full code and a static shot, but these GIFs give the real feel. Might mess with it more later—maybe add controls or push the iterations higher for detail. For now, it’s done and out there.
