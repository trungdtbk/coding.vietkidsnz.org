---
title: "Ping Pong"
date: 2020-07-28T09:13:59+12:00
draft: false
tags: []
level: 
hidetitle: false
hidedate: false
hidesidenav: false
coverimg: /images/projects/ping-pong.gif
---

One more game for you this week: Creat a PING-PONG game.

<!--more-->

There is a ping-pong ball that's flying between the left and right edge.
There are two players who control the pad so that the ball is hit back and does not touch the edge on his side.

If the ball does touch the component's side, he gets 1 point. You got the idea?

So how would you do it?

First, think about the ball. It's boucing back and forth from left to right, right to left and so on.
I think you figure out how to do it. You've learned the technique already. 

Now, think about the first player. How do you control it? Conditions like `<key (a v) pressed?>` can be helpful
For example:
```
if <key (a v) pressed?> then
    change y by (10)
end
if <key (s v) pressed?> then
    change y by (-1)
end
```

So, what letter in the keyboard needs to be pressed to make the play go up?

{{< collapse text="See how it's done" >}}


### 1. Create a player

A player can be a simple as a rectangle that looks like a pad.
The pad can only go up and down in his side (can be either left or right)

Let say **left** means the `(x position)` is -224. Then the code for a player can look like the below:

```
when green flag clicked
    go to x: (-224) y: (0)
    forever
        if <key (a v) pressed?> then
            change y by (10)
        end
        if <key (s v) pressed?> then
            change y by (-10)
        end
```

Ok, we're done the first player. The second player is not much different. Can you figure it out yourself.

### 2. Code the ball

First, make it appear in the center of the screen.
Then pick a direction and move the ball towards to edge.

```
when green flag clicked
    go to x: (0) y: (0)
    forever
        if on edge, bounce
        move (15) steps
        wait (0) seconds
```

It's up to you to deicde how many steps the ball moves and how it should wait before each move.
This controls how fast the ball goes. Try with different values until you're happy with.

Now, make the ball bounce back if it hit the player's pad

```
if <<touching (player 1)?> or <touching (player 2)>> then
    point in direction ((direction) * (-1))
```

Ok, if don't understand `((direction) * (-1))` no worries. It is used to tell the ball reflect in the opposite direction.
If you put the above code within the `forever` you had for the ball, you can see how it work.

### 3. Score the player

I let you figure it yourself. I'll help you if needed.

{{< /collapse >}}