---
title: "Escape the Maze"
date: 2020-07-27T05:40:52+12:00
draft: false
tags: []
level: 
hidetitle: false
hidedate: false
hidesidenav: false
coverimg: /images/projects/escape-the-maze.gif
---

This is a very simple and boring game for you to practice using conditonals block.

<!--more-->

The game is simple: you have a cat or whatever being trapped in the middle of a maze. The cat's home is located somewhere outside the maze (see the image). The player uses the mouse pointer to move the cat out of the maze and to its home without touching the maze. If the maze is touched the cat glides back to its original location.

Let break it down to many small tasks:

1. Draw a maze. You can draw it in a new Sprite or as a backdrop
2. Make the cat appear in the center of the maze?
3. Make the cat moves as the mouse pointer moves?
4. Make the cat glide to the center of the maze if it touches the maze
5. Stop the game when the cat touches its home.

Complete the task one by one.

{{< collapse text="See how it's done" >}}

1. Make the cat appear in the center of the maze.

Let say the center is `(x position)` = 0 and `(y position)` = 0.
Then the block `go to x: (0) y: (0) :: motion` would do it:

```
when green flag clicked
    go to x: (0) y: (0)
```

2. Make the cat moves as the mouse pointer moves

Look in the **Sensing** blocks you wil find something like `(mouse x)` and `(mouse y)`. These tells the position of the mounse pointer. 
So the block `go to x: (mouse x) y: (mouse y)` will make the cat move to the mouse pointer.

You won't see it works until you put the block into a loop, like this:

```
forever
    goto x: (mouse x) y: (mouse y):: motion
```

3. Make the cat glide to its original place if it touches the maze

Sensing blocks can be used to tell if something is touching something else.
So you can code it like this:

```
if <touching (maze) ?> then
    glide (1) secs to x: (0) y: (0)
```

Where should we you put the above block?

4. Stop the game when the cat gets home

The condition `touching (home) ?> :: sensing` can be used to tell if the cat is home.
So instead of using the `forever` loop, you may want to replace it with `repeat until`


Now if you play it it seems like there is a flaw in the game. A clever play can just move the mouse pointer to cat's home and it's done.

Can you fix it?

Instead of simply `go to x: (mouse x) y: (mouse y)` you can use a conditional like this:
```
if <touching (mouse-pointer) ?> then
    go to x: (mouse x) y: (mouse y)
```

This makes the cat move only when the mouse pointer touches the cat.

Ok, we're all done. Can you think of 1 or 2 things that the game can be improved?

{{< /collapse >}}