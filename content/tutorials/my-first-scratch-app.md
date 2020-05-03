---
title: "My First Scratch App"
date: 2020-03-01T20:20:31+12:00
draft: true
tags: []
level: 
hidetitle: false
hidedate: false
hidesidenav: true
coverimg: /images/tutorials/my-first-project.png
---

This tutorial will show you how to create your first ever app in Scratch. It's gonna be a simple one but no worries, we all need to learn how to walk before we can run. Let's get started.

<!-- more -->

Our first Scratch app will have a cat that says hello and walks around from the right to the left and so on forever.

## Create a new project in Scratch

To create a Scratch project, open [**Scratch**](https://scratch.mit.edu) (we already learned how to create a Scratch account), then select [**Create**](https://scratch.mit.edu/projects/editor/). See the image below.


Want to know more about Scratch projects? Read [here](https://en.scratch-wiki.info/wiki/Project).

![](/images/tutorials/1.png)

When a project is created, Scratch already gives us a **Sprite** with a cat. But it doesn't do anything when you click on the **Green flag**. Oh wait, what is a Sprite? Find out at the end of the tutorial.

### Get to know Scratch interface
The Scratch interface will look like the image below. The main areas of the interface are **Code blocks**, **coding window**, **sprite window**, **backdrops** and **preview window**.

![](/images/tutorials/2.png)

## Let's add a backdrop

Each Scratch app has a stage which can have one or many more backdrops. You can program the stage almost the same way as 
you do with the Sprites. 
For instance, you can put codes to the stage to switch from the sunny backdrop to rainy one. We'll learn that later.
Click on the backdrop button and choose a backdrop that you like.

![](/images/tutorials/3.png)


## Let's make the cat say hello

Grab `say [hello] for [2] seconds` block from the Code blocks and place them into the coding window like the image below. Select the **Looks** tab to find the block.

See the `when green flag clicked`? It's important to have it before any other blocks. It's the first to be executed when you click the green flag.

![](/images/tutorials/4.png)

## Let's make the cat go around

We'll make the cat goes from the left to the right. When it hits the wall, it turns back and goes to the other direction.
Make your codes look like the image below.

![](/images/tutorials/5.png)

The block `forever` ensures that all the instructions within it will run forever. That's it. The `move [10]` makes the cat move 10 steps (i.e. pixels) at a time. What about the `if on edge, bounce`?

It works for now. But it looks like the cat is up side down when it turns. Can you fix that?

Add the `set rotation style [left-right v]` to your code to change how Scratch rotate the cat. You only need to set it once.

## Let's learn a bit about Scratch

### What is a Sprite?

In each project, you can many Sprites. A Sprite is kind of a character (or player) in your app. You will need to give each Sprite a sequence of **instructions** so that the Sprite will do thing you want it to do. Grab instructions from the **Code blocks** on the left and place them in the Coding window. Instructions are sticked together in a top-down manner. When the app starts, it will run instruction by instruction from the top to the bottom and causes the Sprite to do things.

A Sprite can have many different **costumes**. For instance, one Sprite can have a Cat costume while the other has a Dog one. Or the same Sprite can a standing cat and a sitting cat costumes. Click on the Costumes tab to see what you have and to add, delete or modify costumes.

### What are instructions?

Blocks in the Code block are instructions, for instance `say [hello]` and `move (10) steps` blocks. You see them visually as blocks but they will be translated into the computer code so that the computer can execute them.

For most blocks, to khow what it does you just need to click on it and see the effect on the Sprite in the preview window.