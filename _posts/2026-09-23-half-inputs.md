---
layout: post
title: Half Inputs
subtitle: Using conditionals with simulated button and switch inputs
author: Gianluca Bocanegra
---

For this assignment, I wrote an Arduino program that simulates a button and a switch using two boolean variables. Depending on the combination of those two values (true or false), a different colored LED turns on, four possible combinations, four different colors.

I chose to use logical operators instead of nested conditionals. I combined both variables into a single condition for each case, in a flat if/else-if chain. I think this was the right choice here because there are only two variables with two possible values each, so just four combinations total. Writing it this way let me check both conditions in one line per case, which was easier to read than nesting one if-statement inside another.

That said, if I had more variables or more possible values, this approach could get messy. Combining a lot of conditions with `&&` and `||` in one line gets harder to read fast, and nested conditionals might make more sense at that point, since they break the logic into smaller, clearer steps.

**Tip for past me:** In each case, explicitly turn every LED either HIGH or LOW, don't just turn the correct one on and assume the rest are already off. I set all four LEDs in every branch to make sure only one is ever lit at a time, which avoided any leftover LEDs staying on from a previous state.
