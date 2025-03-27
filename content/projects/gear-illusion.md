---
title: "Creating an Impossible Gear Illusion with p5.js"
date: 2025-03-04
author: "Mike Wilcome"
---

## A Wild Idea Comes to Life

I recently teamed up with **Grok**, an AI from xAI, to tackle a fun challenge: building an optical illusion that makes you question how gears work. The result is the **Impossible Gear Cascade**—a stack of gears where the bottom one spins the *same way* as the top, which shouldn’t happen in real life. We brought it to life using **p5.js**, a JavaScript tool that’s perfect for creative projects like this.

Want to see it for yourself? Check out the code on my GitHub: [github.com/mwilcome/gear-illusion](https://github.com/mwilcome/gear-illusion). Stick around, though—I’ll walk you through how we pulled this off.

---

### The Illusion: Gears That Break the Rules

Normally, when gears stack up, each one turns the opposite way of the gear above it. Top gear goes clockwise? The next one goes counterclockwise. That’s just how it works. But in our illusion, the bottom gear spins the *same direction* as the top one—like some kind of mechanical rebel. It looks impossible because, well, it is. And that’s what makes it so cool.

Here’s what it looks like in action:

![Impossible Gear Cascade](/images/myAnimation.gif)

See that? The gears seem to mesh perfectly, but that bottom one matches the top gear. It's not the perfect illusion but hey for a Grok project that's pretty neat. I wonder what else kind of things Grok can do with illusions...

---

### How We Made It Happen

This was a team effort. I had the idea, and Grok helped me learn and work on it. Here’s the rundown:

- **One Gear at a Time**: We started simple—drew a single gear with p5.js, using circles for the body and little rectangles for the teeth. Easy enough.
- **Stacking ‘Em Up**: Then we added more gears—eight total, lined up vertically. Each one had to spin the opposite way of the one above it, except for that bottom gear, which we set to match the top.
- **Making It Click**: Getting the teeth to line up was the hard part. We shifted every other gear, so they’d look like they were actually turning each other. Took some tweaking, but it worked.
- **A Little Extra Fun**: We threw in a feature where you can click the screen to flip the direction of all the gears. The illusion still holds up, which is honestly pretty neat.

---

### Why p5.js Rocked for This

If you haven’t messed with **p5.js** before, it’s a JavaScript library that makes drawing and animating stuff a breeze. Here’s why it was clutch for us:

- **Simple Shapes**: We used basic commands like `ellipse()` for circles and `rect()` for teeth. No fancy graphics knowledge needed.
- **Smooth Animation**: p5.js has this `draw()` function that loops constantly, so we just updated the gear angles each frame to keep them spinning.
- **Click and Play**: Adding that click-to-reverse feature was dead simple with p5.js’s built-in mouse controls.

Oh, and when it was done, we used `saveGif()` to snag that animation you see above. Just hit a key, and it records a few seconds—perfect for sharing.

---

### The Fun of Figuring It Out

Working with Grok was a blast. We’d toss ideas around, tweak the code, and watch the gears come to life. There were a few hiccups—like when the teeth wouldn’t line up right—but we kept at it until it looked smooth. Capturing that GIF was the cherry on top; it’s one thing to see it on your screen, another to share it with the world.

> **Quick Tip**: Want to grab your own GIF in p5.js? Add this to your code:
> ```javascript
> function keyPressed() {
>   if (key == 's') {
>     saveGif('myAnimation', 5); // Snags 5 seconds
>   }
> }
> ```

---

### Check It Out Yourself

If this sounds like your kind of thing, swing by the [GitHub repo](https://github.com/mwilcome/gear-illusion) and take a peek. You can run it, mess with it, or even build your own crazy illusion. p5.js is super approachable—check out their [get-started page](https://p5js.org/get-started/) if you’re new to it. It’s a great way to mix art and code.

---

### Wrapping It Up

The **Impossible Gear Cascade** was a fun ride—part puzzle, part playground. I love how it turned out, and teaming up with Grok made it even better. It’s the kind of project that makes you blink twice and wonder, “Wait, how’s that work?” (Spoiler: it doesn’t, and that’s the point.)

So go ahead—click around, flip the gears, and see if you can figure it out. I bet you’ll have as much fun as we did making it.

![Gear Illusion in Action](/images/gear-illusion.png)  
*[Source: [GitHub - Gear Illusion](https://github.com/mwilcome/gear-illusion)]*