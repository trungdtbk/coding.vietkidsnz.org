---
title: "Animate Your Name"
date: 2020-06-07T08:00:00+12:00
tags: []
level: beginner/advance
hidetitle: false
hidedate: false
hidesidenav: false
coverimg: /images/projects/animate-your-name.gif
---

In this project, you gonna create an animation of your name in several ways, like spinning.

<!--more-->

## Description

Draw your name and animate it in many possible ways you can.
For instance, for beginner level, make your name gliding from the left to the center or make it spin or make it appear slowly while spining or whatever animation you can think of. 

### Beginner

1. Make you name fly in from the top/bottom/left or right and park in the center.
2. Make the name appear in the center, begin with a tiny size and slowly getting bigger.
3. Make the name glow when move the mouse over it.

### Advance

1. Make two or more animations (you can use the begineer ones) for your name at the same time.
2. Animate each letter of your name separately. For instance, make a wave of letters.
2. Create an app that asks for a word and then animate that word or each letter as in the above.

## Some Hints

Some techniques you may need to use to complete this challenge.

{{< collapse text="Try to do it first" >}}

1. You need blocks that change the look of the Sprite (see Tutorial - [Getting Started with Look blocks](/tutorials/getting-started-with-look-blocks))
2. Use **loop blocks** to change from a look to another to create an animation (see Tutorial - [Working with Loops](/tutorials/working-with-loops)).
3. To have multiple animations at the same time, use the **concurrency technique** (see [Getting Started with Concurrency](/tutorials/getting-started-with-concurrency))


Play with [this Scratch tutorial](https://scratch.mit.edu/projects/editor/?tutorial=name) to gain some experience.

### Make it spin
```
when green flag clicked
point in direction [90]
repeat [30]
    turn [12] degrees
```

### Make it pop up
```
when green flag clicked
set size to [0] %
repeat [30]
    change size by [30]
```
### Make it glow when hoverover
You should have created two costumes for your name already to make it work. Name them **normal** and **glow**.

```
when green flag clicked
forever
    if <touching [mouse-pointer]>
        switch costume to [glow]
    else
        switch costume to <normal>
```

{{< /collapse >}}