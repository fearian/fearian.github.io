---
title: "How I Made This Website"
date: 2022-11-15T19:54:20Z
draft: true
toc: false
images:
tags:
  - meta
---

I am not a web developer. The last time I made a website for myself, I did it in notepad.exe, with a CSS textbook I took from the library. The mere glimpses of this world that I catch through [fireship.io YouTube videos](https://youtu.be/pEfrdAtAmqk) scare me.

But I do like markdown and YAML. I actually [love using markdown for all my note-taking](https://obsidian.md/). So when I started getting curious about creating a landing page for myself - with the discourse of impending twitter diaspora in mind - I was interested to hear about HuGo: A "Static Site Generator" that would turn markdown files into pages. It sounded like if I could just get over the setup hurdle, it would be exactly what I needed.

The first-page-result tutorial I found was ["Create a website with Hugo and GitHub Pages"](https://4bes.nl/2021/08/29/create-a-website-with-hugo-and-github-pages/), which got me up and running shockingly fast. If you want to set up a simple website yourself, I can recommend HUGO and GitHub for quick results! However, as a non-developer, I tripped on hurdle after hurdle, so I thought I'd cover some of my pain points here.

### Install Hugo... Using a terminal?
Assuming you follow the tutorial pre-requisites and have VS Code, Git, and GitHub setup, your first speedbump might be installing Hugo through a terminal on windows.

I advise downloading the pre-built binaries from [here](https://github.com/gohugoio/hugo/releases/latest), taking care to grab the *extended* build for your platform. Don't worry about "path variables" if this is a strange term to you. After creating my empty git project, I placed `hugo.exe` in the root of the project directory and in VS Code opened the terminal with `Ctrl + '`. Here you can follow along with tutorial commands by prefixing your inputs with `.\`, e.g. `.\hugo new site .\ --force`.

### Install a theme... But not that one!

Setting up a theme is pretty simple. Just place it in the themes folder, make some small changes to `config.toml` and boom! However making edits to a theme is where the struggle begins. Every theme is developed differently, and behind the scenes it's just full front-end development. You might run into some CSS... or Post CSS, or SASS, Tailwind, Bootstrap, Netlify? Forestry? And obviously, the whole thing is coded in a mix of HTML 5 and Go that my editor doesn't know what to do with.

My now obvious mistake was thinking that I could take elements from one theme, and add them to another. Just working out how one theme constructs it's site is reaching into the guts of the operation, and transplants are not a surgery for beginners.

The "hello-friend-ng" theme itself is a modification of two other existing themes. So I had to bounce between three GitHub pages to check the documentation for each. It might be "one of the most popular blog themes at the time of writing", according to our guide, but that means popular with people who know what they're doing.

I advise taking a few hours to try out different themes to find something that uses a minimal amount of external libraries and JavaScript, or at least is very close to the functionality you are looking for.

Submodules