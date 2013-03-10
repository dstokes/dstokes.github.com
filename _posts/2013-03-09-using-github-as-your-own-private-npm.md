---
layout: post
title: "Using Github as your own private NPM"
description: ""
category: 
tags: [npm, node, github, javascript]
---
{% include JB/setup %}

When working on a production node application you'll inevitably find the
need to require packages that you don't necessarily want to release into the
wild. While there's ways to handle this currently (via tarball urls) it's easy
to start running into version management issues when iterating quickly or
working with a complex dependency tree.

Knowing there had to be a more elegant solution to this problem that could
hold me over until my invite for [Iris npm](https://www.irisnpm.com/) came
through, I started chatting with [@8bitDesigner](https://twitter.com/8bitdesigner)
who had a novel idea: "Why not just use git version tags?"

## Github as a package manager
The concept is pretty simple. Just use repo tag tarball urls to load packages
from Github right? There's a problem though. To ensure your app doesn't break when
it's dependencies change underneath it, you need to implement some tagging
workflow to lock down your module code. This can be really cumbersome for
several reasons (one of which involves me remembering to properly tag my
features).

But what if you could use the npm tools your already familiar with to keep
your package releasable in spite of changes.

## Versioning with NPM
Those of you who have packages on npm probably already know about The
`npm version [semver]` command. It basically affords you the convenience of
bumping your package json version number with SemVer terminology or a specific
version number with a single command. What you may not know is that the same
command will also create a commit and a tag for the new version if run within
a git repo. Wait.. what?!

Utilizing this feature means that releasing a new version of our private module
to github is as simple as:
{% highlight bash %}
  npm version patch && git push origin HEAD && git push --tags
{% endhighlight %}

**Now we're getting somewhere..**

## Taking it a setup further
We use Jenkins for continuous integration and interface aside, we love it. The
only logical next step for us was having Jenkins create our versions for us
once the builds passed. We accomplish this by creating descriptive branches
that contain the feature name and semver distinction. \*When we push a branch
like `minor/awesomesauce` Jenkins knows to run `npm version minor` followed by
a git push. Because we're pretty diligent about unit testing with Mocha this
means we get package versioning for free when code passes our tests. The only
thing left to do is update our apps package.json to use the new version.

\* It's a little more complicated than this. Jenkins runs against a detached
head state making it difficult to push to master, but thats easily solved.

## The Drawbacks
Of course this workflow does lack some of the luster of using npm directly.
When using Github tarball urls there's no way to specify version ranges and
each npm install will refetch the module when necessary because Github
doesn't support tarball 304's. In spite of this, it's working pretty well for
us so far.

## Conclusion
As your project grows dependency management will start to bite you at multiple
stages of your development process. This becomes exponentially more complex
when dealing with private modules if you're not running your own private npm
instance etc. However, if you need a simple solution for locking down your
private dependencies on Github, `npm version` might be the hero you've been
looking for.
