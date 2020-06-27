---
title: "Using Loops"
date: 2020-06-27T19:53:19+12:00
draft: false
tags: []
level:
hidetitle: false
hidedate: false
hidesidenav: false
---

Loops are very common in coding. Whenever you see something happens again and again, think about loops.
In this post, you will be learning about loops in Scratch and do a simple project using loops.

<!--more-->

# What are loops?

There are 3 types of loops in Scratch. They are `repeat [10]`, `repeat until <>` and `forever`.

You use `repeat [10]` when you want something to be done 10 times. Change **10** to something else if you want it to be more or less. For example:
```
repeat [5]
    next costum
    wait [1]
```

Do you get what do the above codes do? It means, if your Cat has two costumes and it's wearing one, then change to the other one, wait for 1 second and change back to the first and so on. Keep doing that 3 times.

So, what will be the costume that the cat is wearing after all?

The second loop `repeat until <>` seems to be tricky but it is very useful. A lot of times you don't know how many times something needs to be done but you know when to stop. Like, you may eat one cake, two cakes or 3 cakes until you're full.
See example below:

```
repeat until <touching (edge v)>
move (10) steps
```

The last loop `forever`, you get it, means repeat doing something forever, non-stop. It only stops when you stop your Scratch project (when you click the Stop button).

Can you get what the following code does?

```
when gf clicked
forever
if <touching [mouse-pointer]>
switch costume to (glowing-costume)
else
switch costume to (normal-costume)
end
```

See this example project to learn more about loops: [https://scratch.mit.edu/projects/393616083/]()