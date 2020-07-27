---
title: "Get to Know Conditionals"
date: 2020-07-25T16:33:00+12:00
draft: false
tags: []
level:
hidetitle: false
hidedate: false
hidesidenav: false
---

What the heck are conditionals? Bruh. Be patient. I'll introduce them to you. For now, think about something like `IF <I am tired> THEN I go to bed :: control`.

<!--more-->
# What are conditonals?
In coding, conditionals are the way we use to tell our program what to do when something (i.e. condition) is TRUE. Lets take a look at an example below:
```
if <it is going to rain> then
    switch costume to (raincoat)
else
    switch costume to (t-shirt)
```

So what would happen? Or what costume our Cat (or Sprite) would wear eventually? We don't know. But at least we know that the Cat wears a raincoat when it's raining.

In Scratch, there are two types of conditionals: 
```
if <something is true> then 
    do something
```

and

```
if <something is true> then 
    do something 
else 
    do something else
```

# Boolean conditions

When I say `something is true`, it is called a boolean condition in coding. This is because it can either be **TRUE** or **FALSE** and nothing else.
Let have some fun exercises.

Is `<(10) > (9)>` true or false? Too easy hah?
How about `<<(10) > (11)> or <(12) < (13)>>`? Still too easy? Lets do something harder. Take a look the below code:

```
if <(score) < (4)> then
    say (Too bad!)
end
if <<<(score) > (4)> or <(score) = (4)>> and <(score) < (6)>> then
    say (Well done!)
end
if <<<(score) > (6)> or <(score) = (6)>> and <(score) < (8)>> then
    say (Very good!)
else
    say (Excellent!)
end
```

What would being said if `set [score] to (3)`? **Too bad** or else? how about `set [score] to (4)`? what if `set [score] to (9)`?

# Boolean conditions in Scratch

Look into the Sensing blocks, you will find various types of boolean conditions. For instance: `touching (edge v)?` or `touching (mouse-pointer v)?` can be used when you want your Sprite to do something when it touches the edge of the screen or the mouse pointer.

Another one that I find very useful is `key (space) pressed?`. It can be used to interact or control our Sprite using the keyboard. For example:

```
forever
    if <key (up arrow)> then
        change y by (10)
    end
    if <key (down arrow)> then
        change y by (-10)
    end
    if <key (right arrow)> then
        change x by (10)
    end
    if <key (left arrow)> then
        change x by (-10)
    end
    if <touching color (#d61128)> then
        say (too hot)
    end
end
```

Can anyone tell what does the code do? 

# Conditional Operators

Conditional Operators are blocks we use to create a condition - TRUE or FALSE thing. You can find them in the Operator blocks. Some of them are:
`<<> and <>>`, `<<> or <>>` and `<not <>>`.
The others are `<() > (10)>` or `<()=(10)>`.

# Truth Table

There is something called Truth Table. You may not need to care about it now but just in case you want to know. The table looks like this:

| Condition A | Condition B | `A AND B` | `A OR B` | `NOT A` |
|---|---|-----|----|-----|
| True | True | True   |  True |     |
| True | False | False   | True  |     |
| False | True | False   | True  |     |
| True |   |     |    |  False  |
| False |   |     |    |  True  |

No worries if you don't get it. 
