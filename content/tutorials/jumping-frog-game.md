---
title: "Game: Jumping Frog"
date: 2021-04-13T06:12:25+12:00
draft: false
tags: []
level: 
hidetitle: false
hidedate: false
hidesidenav: true
coverimg: /images/tutorials/JumpingFrog/jumping-frog.gif
---

This tutorial walks you through the steps to design and implement a game called Jumping Frog. This is a copycat version of a game called Tag the Frog on mobile phones.

<!--more-->

# Let describe the game in plain English

It's important to describe the game in words before designing it.

A frog standing on a leaf floating on a pond. It jumps from one leaf to another. There are endless number of leaves on the pond. Sometimes, the leaves stick together, sometimes they are far way with one leave missing in between. The frog can jump to the next leave or as far as over one leave. The challenge of the game is to jump as many leaves as possible.

This is what we want to see when it's completed.

![jump-frog](/images/tutorials/JumpingFrog/jumping-frog.gif)

# Let design the game

Let break it down into pieces. We see a Frog and Leaves. 

The Frog looks like jumping from one leave to the next but it's actually jumping up and down.

The Leaves are moving from the Right to the Left as the Frog jumps. Leaves seem to be missing randomly.
As the leaves move out of sight, another leave appears on the Right. This circle continues forever.

## Let design algorithm for the leaves

Let say the Frog can see 5 leaves at a time. Start by drawing them to a paper or on Scratch

![](/images/tutorials/JumpingFrog/1.png)

The leaves can move one step or two steps at most as the Frog jumps. For one-step jump, Leaf1 will go out of sight to the left, Leaf2 moves to Leaf1 position and so on.
If Leaf1 takes the place of Leaf5, it's going forever.
For two-step jump, Leaf1 takes Leaf4's place, Leaf2 takes Leaf5's.

Let make a variable `(Leaf_1_Position)` to say where Leaf1 currently is. For one-step, its new position would be `change(Leaf_1_Position) by (-1)` and for two-step `change(Leaf_1_Position) by (-2)`. So, if its current position is 1, the next would be 0 for one-step and -1 for two-step jump. This is not what we want. We want Leaf-1 to take Position 5 and 4 for one-step and two-step jump.

We need a bit of math to do that: `set [Leaf_1_Position] to ((5)+(Leaf_1_Position))`. Is it correct? 5-0 = 0?; 5-1=4?

The same algorithm applies for Leaf2,3,4 and 5.

## Let implement the first Leaf

Create a variable `(X_Posisition_5)` to keep the value of the X axis. It is where the Leaf at Position 5 should stay on the screen. I would set its value to 190.

Add the code to set the initial position of the Leaf-1

```
when green flag clicked
set (Leaf_1_Position) to (1)
```

Add the codes that change Leaf1 position.
```
when [leaf arrow] key pressed
change (Leaf_1_Position) by -1

when [leaf arrow] key pressed
change (Leaf_1_Position) by -2
```

Add the codes to make sure Leaf1 come back to the screen when it goes out of sight
```
when green flag clicked
forever
if < <(Leaf_1_Position) < (0) > or <(Leaf_1_Position) = (0) > >
set [Leaf_1_Position] to ((5)+(Leaf_1_Position))
```
Now test it to see if we get it correct. Yeah, it  is. Now the display Leaf1 in the correct place, we just need to use the `go to` block.
We need a bit more math over here as well. Let make a variable `(Jump_Distance)` to tell how the jump is in pixels. Set its value to 100.
Add `go to ( (X_Position_5)-( (Leaf_1_Position) * (Jump_Distance) ) )` to inside `forever` block, but outside the `if` block

```
when green flag clicked
forever
if < <(Leaf_1_Position) < (0) > or <(Leaf_1_Position) = (0) > >
    set [Leaf_1_Position] to ((5)+(Leaf_1_Position))
end
go to ( (X_Position_5)-( (Leaf_1_Position) * (Jump_Distance) ) )
```
Now test if it works. Now do the same for other Leaves.

## Let make the Leaves disappear

Now we have the Leaves go over again in a loop forever. But this doesn't make a game because all of the leaves are displayed, nothing interesting here.
We need to make one or more leaves disappear randomly to make it interesting and hard to play.

Let make the Leaf1 randomly disappear. To make a Sprite disappear we can use the `set [ghost] effect to (255)` block. We can use the `pick random (1) to (10)` block to determine if the Leaf1 should be shown or hidden.
```
when green flag clicked
forever
if < <(Leaf_1_Position) < (0) > or <(Leaf_1_Position) = (0) > >
    set [Leaf_1_Position] to ((5)+(Leaf_1_Position))
end
if < (pick random (1) to (10)) < (5) >
set [ghost] effect to (255)
else
set [ghost] effect to (0)
end
go to ( (X_Position_5)-( (Leaf_1_Position) * (Jump_Distance) ) )
```

The same logic is applied to other Leaves to make the game even harder and more interesting.

## Let design the Frog

This is simple. The Frog is jumping up and down at the same location. Create a Sprite for the Frog.
Use the block `change y by ()` along with `repeat` block to make the Frog go up and down.

# Let make the game look good

This is for you to figure out what to do and how to do.