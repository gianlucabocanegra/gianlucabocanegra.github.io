---
layout: post
title: Responsive Buttons
subtitle: A different LED lights up every time I press a button
author: Gianluca Bocanegra
---

For this homework, I made an Arduino program where a different LED turns on every time I press a button. The LED stays on while I hold the button, and it turns off when I let go. The next time I press it, a new LED lights up. Only one LED is on at a time.

**Tips for past me:**

1. Save the button's last state in a variable. If you don't, the program thinks you're pressing the button again every single moment you hold it, and the lights change way too fast.

2. Set the random seed in setup(). I almost forgot, and the LEDs would have turned on in the same order every time I restarted the board.

3. Use a loop instead of copying the same lines for each LED, and use Auto Format before you submit. It makes your code shorter and a lot easier to read.
