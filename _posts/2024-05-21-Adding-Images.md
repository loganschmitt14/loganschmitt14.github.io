---
layout: post
title: Blog Creation Process
description: A meta post about creating this blog
date: 2024-04-05T07:00:00-07:00
tags: Meta
---

# Adding Images to a GitHub Pages Blog

I was a little bit lazy about learning to add images to this blog when I first created it. I'm using a template instead of writing the whole site from scratch, so I knew I couldn't just embed images with HTML. Turns out, it's still pretty simple. The main caveat is that Jekyll expects embedded assets to live in a `/docs/assets` directory. I put my pictures into subfolders within an `images` folder in that directory for organization purposes. We'll see if I ever need any other type of asset.

From there, I just use `![Alternate text](path_to_image)` to embed the image in Markdown. In my case, I have to make sure I don't use `../docs/` or the image won't load in the browser, even if it renders just fine in VSCode. It doesn't work once translated to HTML.

I'm going through the process of resizing my images to have a maximum dimension of 1200px. It feels like a good task for automation at some point. 