---
title: "Snowflakes"
date: 2020-07-27T04:27:07+12:00
draft: false
tags: []
level: 
hidetitle: false
hidedate: false
hidesidenav: false
coverimg: /images/projects/snowflakes.gif
---

We'll be creating a scene in which snowflakes are falling from the sky...

<!--more-->

It may sound pretty simple and boring. But it's good for our practice with using loops.
You should make a Scratch project with a dark background and a lot of snowflakes keep falling down from the top of the screen.

If you already have ideas how it can be done that's great. Otherwise, let break it down.

1. Let think about a single snowflake first. You will need a Sprite for it
2. The flake should appear at the top of the screen
3. The flake should be falling down to the bottom of the screen
4. The flake should stop somewhere at the bottom and stay there
4. Now think about 10 flakes, 100 flakes and maybe millions...

The last one can be hard. We'll do togher in our class. But here are some hints if you want to try to do.

If you just want 2 or 10 flakes, you can just duplicate the first flake Sprite then you're done. Huh?

If you want a lot more, you can use the `create clone of (myself)` block to make millions or more copies of the same flake:

```
repeat (1000000)
    create a clone of (myself)
end

when I start as a clone
repeat until [hit the bottom]
    move down
```

Or to make an endless winter:

```
forever
    create a clone of (myself)
```

**Be careful when making copies of a Sprite. Doing it wrong can make your computer out of resources and go really really slow.**

When the flakes hit the ground, you should delete it using `delete this clone` 
Ok, you got it. But then the flake disappears. So, how do you make the flake stay at the ground?

You can use the **Pen blocks** like `stamp::pen` to make a mark of the flake before deleting the Sprite.

{{< collapse text="See how it's done" >}}

1. First draw a snowflake of your own
2. Add the Pen blocks

Use the following code to make a lot copies of the snowflakes...

```
when flag clicked
    go to x (0) y (170)
    forever
        wait (0.000001) seconds
        create clone of (myself)
    end
```

Try to run it see what will happen. Remember to stop it before too late. The `go to x (0) y (170)` makes the flake appear at the top of the screen (we call it the sky :))

Now make it fall.

```
when I start as a clone
    set pen (color) to (255)
    point in direction (180)
    repeat until <(y positon::motion) < (-180)>
        move (10) steps
        wait (0.05) second
    end
    stamp::pen
    delete this clone
```

These above codes run everytime when a clone is created. The `point in direction::motion` block is used to make the flake go down.
What does `<(y position) < (-180)>` do? Here we define *-180* is the ground, the `y position::motion` is the position of the flake along the vertical axis.
We move it 10 steps down until it reaches the ground.
Then the `stamp::pen` is used to mark the flake in the ground before the `delete this clone` removes it from our program, so that it uses no resouces of our computer.

{{< /collapse >}}
