---
title: "Crazy Shark"
date: 2020-06-28T06:17:21+12:00
tags: []
level: beginner
hidetitle: false
hidedate: false
hidesidenav: false
coverimg: /images/projects/crazy-shark.png
---

Can you create a shark that looks for fish and eats any fish it can see?


<!--more-->

In this project, we continue practicing on how to use loops in Scratch.

You will be creating...

- A fish tank or ocean which has
- two or more fish that swim arround
- a shark that swims toward those fish and eats when they meet

It sounds hard, hah? Don't worry, we'll do it together in our next meetup.
For now, think youself how you would do it. And do it as much as you can.

## Some Hints

You can break down the project into many small tasks, like this:

1. Creat a fish and make it swim. Use the same technique you had for your name animation
1. Make the fish swim back and forth between two edges.
2. Create a shark and make it swim. Again, very similar way to the fish
3. Make the fish disappear when it got eaten by the shark.
4. Make it more fun by making the fish appears at random location when start
5. Make it interesting by adding more animations like: swirling reef...


{{< collapse text="See how it's done" >}}

How do you create more than one fish? You can just create a fish Sprite and then duplicate it.
Or a better way? Use the block `create clone of (myself v)`. For example:
```
repeat (3)
create clone of (myself)
```
will make 3 fish of the same kind

How do you make the shark swim towards the fish. Take a look at this block `point towards (FIsh v)`

How to make the fish keep swimming until it meets and gets eaten by the shark? The block `repeat until <touching (Shark v)>` will be very useful.


How do you make the fish disappear when it got eaten? Use the animation techniques you've learned: use `repeat [10]` and `change [ghost v] effect by (10)` for example.

{{< /collapse >}}