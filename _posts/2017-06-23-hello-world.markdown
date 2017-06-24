---
layout: post
title:  "Hello World!"
date:   2017-06-23 23:49:00 +0100
excerpt: "A few words on redesigning my website with Jekyll and the blog posts to come."
---

(This post is more of a ramble than anything. The blog posts which follow will have much more interesting content!)

For the past year, I have felt the urge to revamp my [old website](https://old.iamkelv.in/). Not only using a theme removed quite a lot of control from me, but the amount of plugins made the website feel lacking in performance (and not to mention, the horrible jQuery scrolljacking!). Likewise, I've frequently had ideas of topics to blog about (usually related to my projects), but [Medium](https://medium.com/) simply felt like the wrong medium (pun not intended) for a technical blog.

In the past week, I finally found the motivation to go ahead and work on this project. The requirements for a new site were as follows:

- A simpler site design (with bigger fonts and more concise text)
- A focus on performance (avoiding jQuery wherever possible)
- Painless updating of site content (preferably using Markdown instead of editing HTML directly)
- Self-hosted blogging platform

I naturally chose [Jekyll](jekyllrb.com) to handle the last two points. Jekyll is a static-site generator, which takes all your content and generates a HTML version of a site. It contrasts heavily with traditional CMS/blogging platforms like WordPress and Drupal; static-site generators let you host the output HTML directly, removing the performance impact (and security risk) of requiring a huge PHP codebase to generate pages on each visit. Additionally, for my blog, I offload comments to [Disqus](https://disqus.com/), whose embed code is conveniently already included the base theme ([Minima](https://github.com/jekyll/minima)) which I worked from.

What I love about Jekyll is the simplicity when I need to update the site: all of my projects are stored as a Markdown file per project in a `_projects` folder; all of my posts are stored in the same format in a `_posts` folder. When I need to add a blog project or blog post, I simply log onto GitHub, create a Markdown file for the new content, and as soon as I commit the file to the repository, [Codeship](https://codeship.com/) automatically tests and rebuilds my site.

Overall I am very pleased with this setup and look forward to writing blog posts on this soon!

