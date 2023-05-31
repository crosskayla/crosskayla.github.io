---
layout: post
title:      Hardest thing(s) about the CLI project
date:       2018-05-16 18:40:44 +0000
permalink:  hardest_thing_s_about_the_cli_project
categories: assignments, projects
---


For my CLI project, I drew inspiration from my DC surroundings to make [CongressCLI](https://github.com/crosskayla/congress-rep-CLI), a simple command line program that scrapes senators' names from senate.gov and displays them by state. It also gives users the option to display contact information for their senators. Below are the hardest four things about the project.

**Nokogiri**

I thought I understood Nokogiri during the lesson, but I didn't fully wrap my head around the level of variation in the way different sites use Javascript. It took some serious trial and error to be able to isolate the elements I wanted from the Senate site.

My recommendation: do it the way the Learn curriculum teaches, in pry:

1. load your webpage with open-url
2. make a new nokogiri object
3. place a binding.pry after to play around with .css
4. use `.size`, `.text`, and `.first` or `[0]` liberally to avoid dealing with loooong strings of XML

**Learning Git/Github**

Git seemed abstract and hard to grasp to me at first.

I started thinking in analogy, comparing it to something I'm very familiar with - editing a Google Doc with multiple users.

* The master repository with committed changes is the original text of the Google Doc.
* You initialize this capability with `git init`. To "turn on" tracked changes for all your doc(s), use `git add .`.
* The changes you're committing are the colorful font of your edits. (`Git commit -am “string”` commits all changes with message - kind of like a Google Doc edit with a comment.)
* The underlying document has not changed when you track your changes - you have to accept the edits to make them permanent. Pushing is the equivalent of accepting those changes ( `git push -u origin master`).

Having a cheat sheet of helpful commands while using Git was very helpful. Some of the commands I saved from the lessons for quick reference are below:

* `git clone your-copied-github-url `- creates local copy of forked GitHub repo
* `mkdir` - new directory
* `touch` - new file
* `echo “string” > file` - adds string to file (useful for readme/logs)
* `ls` - lists all files
* `git init `- initializes new git repository in current directory
* `git status` – shows status of commits (if everything is committed & pushed to master repo, it will be 'clean')
* `git add` - tells git to track file
* `git add .` - tells git to track entire current directory
* `git commit -m “string”` - commits one change with a message
* `git commit -am “string” `- commits all changes with a message
* `git rm -r filename `- delete file
* `git push -u origin master` - push code to repository

**Listening to my own voice on the recording**

If you're using a Mac, it turns out recording a voiceover + walkthrough of your gem is incredibly easy! But listening to your own voice can be harder...

Simple screen recording with voice:
1. Open QuickTime Player
2. Click File > New Screen Recording
3. Click the mini arrow in the menu that pops up to select your microphone input and mouse settings

So in addition to working on my coding, after watching my walkthrough, I'm going to work on removing "um" from my vocabulary.

**Dork/life balance**

Finding long blocks of time for in-depth projects like this was another hard part of the project. Although those blocks are scarce, using them is so effective – I did the bulk of my CLI in one focused day. I love [this](https://www.amazon.com/Deep-Work-Focused-Success-Distracted/dp/1455586692) Cal Newport book on the importance of focused, deep work, and I've found it to apply to my programming process.

The biggest delay of the project was this blog post itself - there are no specs or suggestions, so it's harder to get started! Test based development gives me a framework so that I rarely have long stalls during which I run out of ideas.
