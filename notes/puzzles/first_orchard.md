---
layout: page
title: First orchard
date: 2023-11-07
tags: [puzzles]
share: false
---
[First
Orchard](https://www.habausa.com/products/my-very-first-games-first-orchard) is
a board game for toddlers. The orchard has four trees, with four fruit each. You
want to pick all the fruit before the raven reaches the orchard. The raven
starts five steps away.

The gameplay consists of rolling a six-sided die. Four of the sides correspond
to the trees: you get to pick a fruit. One of the sides has a raven on it: the
raven advances one step along its track. One side is a wildcard: when you roll
it, you get to choose any of the four trees, and pick the fruit from it.

The optimal strategy is of course to always pick the tree with the largest
remaining number of fruit, but in my experience three-year-olds don't reliably
figure that out.

The puzzle is this: if you play optimally, what's the probability that you win
the game? How does that change if the raven's path is shortened or lengthened?
Or if the number of fruit per tree is changed?

There's probably an analytic solution, but I just [did some
simulations](https://colab.research.google.com/drive/1fJjfaxLQZO8hYSjBxv32WNSTMI8ThDp7?usp=sharing).

*   Optimal players win with roughly 0.63 probability. Less than I expected!
*   Random players only win with 0.43 probability.
*   Optimal players facing a crow that starts one step closer to the orchard
    only win with probability 0.46.