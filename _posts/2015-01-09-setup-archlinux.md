---
title: "Setting it up, Arch Linux style"
description: "Going from a Ruby-less Linux distro to one that can generate your
static website in a couple of seconds, serve it locally and
regenerate it, while you write up new posts. Can it make tea as well? Let's find out."
layout: post
tags: Jekyll, GitHub
category: website
comments: no
---


As [I've mentioned](/2015/01/08/new-construction-options.html), I'm thrilled to
be using [Jekyll](http://jekyllrb.com) as my static site generator. The
simplicity of it made me finally build my own website, while letting me enjoy
the experience. 

Before you can fetch and edit the code I've written about in the previous post,
there's a little bit of setting up to do first. I'm using Arch Linux, which is
[awesome in it's own right](https://wiki.archlinux.org/index.php/The_Arch_Way), 
if you're in for a new Linux distro you most certainly should 
[check it out](http://www.archlinux.org).
This guide will be based on Arch to jump-start you ASAP, it should translate to 
most other distros seamlessly.

You can find more detailed guides, on the 
[archwiki page](https://wiki.archlinux.org/index.php/jekyll) and on the 
[Jekyll website](http://jekyllrb.com/docs/home/).


First of, you'll need something to run Jekyll, which is Ruby.

On Arch you can simply use pacman or yaourt to install it the usual way.

    pacman -S ruby

Which conveniently installs RubyGems as well, which you'll need.
On other distros, use your package manager or binary of choice.

Once up, be sure to update your gems.

    gem update

Next, you'll need the Jekyll gem with all its dependencies.
A simple

    gem install jekyll

should do the trick.

It's time to pick a markup language, which converts your
text based files to HTML pages. Jekyll supports both 
[Markdown](http://daringfireball.net/projects/markdown/) and 
[Textile](http://en.wikipedia.org/wiki/Textile_%28markup_language%29) as
defaults. There's no problem in installing both and just siding with one
depending on your project. I've decided Markdown does the job fine for me.
The gem which uses Markdown is called Rdiscount and more info is available on
the detailed guides above.
To get rdiscount use: 

    gem install rdiscount -s http://gemcutter.org

Be sure to specify you're using rdiscount in your Jekyll config
file \_config.yaml.

    markdown: rdiscount


This should be all the setup you need. Let's take it out for a spin.


Open a terminal and punch in 

    jekyll new my-new-awesome-site
    cd my-new-awesome-site


Your newly generated default Jekyll folder should look something like this:

    .
    |-- _config.yml
    |-- _layouts
    |   |-- default.html
    |   `-- post.html
    |-- _posts
    |   |-- YYYY-MM-DD-super-descriptive-long-ass-title.markdown
    |   `-- 2015-01-01-will-be-a-good-year.md
    |-- _site  (this won't be here until you run jekyll with build or serve)
    `-- index.html

There will be a couple of extra bits, an .xml file for RSS, a bit of styling in 
CSS and an all important about.md page plus the usual GitHub structure.
Notice you can use .markdown or .md for your markdown files.

You can now run jekyll with a flag to serve you the content for inspection with

    jekyll serve --watch

Jekyll will happily build you the content in the \_site folder and the _watch_
flag will trigger rebuilds if any files change while serving the content.

You can check your new website in your browser at <http://localhost:4000>.
Cool, no?


Sadly, it won't make tea for you automagically (yet!). It does however support 
[Sass](http://sass-lang.com/) and [CoffeeScript](http://coffeescript.org/) 
out of the box.


That's the basics and you're all set to build your website from foundations up 
or go look for ideas in 
[other people's lovely Jekyll code](http://jekyllrb.com/docs/sites/).
