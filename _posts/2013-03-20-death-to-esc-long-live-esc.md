---
layout: post
title: "Death to ESC, long live ESC!"
description: ""
category: 
tags: []
---
{% include JB/setup %}

I’ve been battling some pretty bad RSI in my arms and wrists for the past few
months. So far I have switched to a standing desk (which was a great decision
for several reasons), ergonomic keyboard and seriously considered making the
switch to Dvorak again.

While I searched for solutions I started paying attention to my typing habits
to try and identify potential causes for my pain. I noticed something peculiar:
The keys that I used most frequently in vim and tmux (ESC and CTRL) were in
incredibly awkward locations. Given that vi is nearly 40 years old, I couldn’t
help but wonder how people had been using such uncomfortable control keys for
so long without making a change.

Turns out the ESC and CTRL keys used to be in much more convenient locations:

![ADM3A](http://upload.wikimedia.org/wikipedia/commons/a/a0/KB_Terminal_ADM3A.svg)

*The [ADM3A](http://en.wikipedia.org/wiki/ADM-3A) keyboard used to develop VI*

Because I can’t get my hands on one of these bad boys these days I decided to
start looking into remap options to make accessing ESC and CTRL easier. That’s
when I stumbled on A Modern Space Cadet by Steve Losh.

In the article, Steve details how to configure your keyboard to mimic most of
his favorite functionality from the Space Cadet board originally used on MIT
LISP machines back in the day:

![Space Cadet](http://world.std.com/~jdostale/kbd/SpaceCadet1.jpeg)

As you can see that’s a grip of keys. While I don’t need convenient methods for
typing Greek characters, I did lift Steve’s configuration for allowing the CAPS
LOCK key to function as both the ESC and CTRL keys based on whether or not it
is pressed in conjunction with another key.

Though it seems like a small change, it’s made a huge impact on typing
efficiency as my fingers rarely leave the home row for most tasks. I also find
that the RSI aches have somewhat subsided since making the switch. If you’re
not tied to caps (and [you shouldn’t be](http://capsoff.org/history)) then
make use of the real estate and remap it to something useful.

You won’t regret it.
