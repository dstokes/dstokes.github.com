---
layout: post
title: "Tools I Use"
description: ""
category:
tags: []
---
{% include JB/setup %}

I love reading about the tools other developers use to build awesome shit so
I figured sharing my toolset would be a good place to start a new blog.

Here's what my setup looks like:
![My Setup](http://f.cl.ly/items/090U0v2t1d0q431w3A0X/Image%202013.02.28%208:14:48%20PM.png)

tmux
----
Some of us use the command line sparingly, commiting files, running build
scripts and watching [ascii star wars](http://lifehacker.com/373571/watch-star-wars-in-text-via-telnet)
on lunch breaks for the lolz. The rest of us spend our waking hours navigating
through a sea of terminal panes with the grace and precision of a tiger shark.
This kind of efficiency is greatly aided by a terminal multiplexer like
[tmux](http://tmux.sourceforge.net/). I could write an entire post about the
benefits of a multiplexer, and [many people have](https://www.google.com/search?q=why%20tmux%20is%20awesome)
but the short version is tmux allows me to manage sessions, windows and panes
all from my keyboard and it is completely scriptable.

vim
---
For many years I used vim primarily as a tool to quickly update configuration
files and bash scripts. It wasn't until I started using SublimeText 2 with
vintage mode that vim full-time actually became palatable to me.

**Making the switch was the best decision I ever made**

There's a steep learning curve coming from an IDE or gui text editor, but the
efficiency gain and configuration possibilities are astronomical. I couldn't
imagine writing code or prose in any other editor.

zsh
---
I drank the zsh kool-aid after reading [The Text Triumvirate](http://www.drbunsen.org/text-triumvirate.html)
and I gotta say, it payed off. zsh is an awesome shell that provides most of
the functionality of bash with some really cool extras. Things like auto cd,
extended globbing and when used in concert with the awesome [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh),
loadable plugins for git, node, sane history-search etc.

others
------
The short version of some additional tools that make hacking awesome:
* [git](http://git-scm.com) - duh..
* [irssi](http://www.irssi.org/) - cli irc client
* [ack](http://betterthangrep.com/) - grep for code
* [tig](https://github.com/jonas/tig) - awesome repo browser

There's so much awesome you can accomplish with the right setup. To learn more
about mine, checkout my [dotfiles](https://github.com/dstokes/dotfiles) on github.
