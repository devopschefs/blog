---
title: "OpenSSL on Windows"
excerpt: "How to find and use OpenSSL on Windows"
toc: false
last_modified_at: 2020-12-09
author: Alex Giannotti
header:
  overlay_image: "/assets/images/posts_header/opensslonwindows.jpg"
  overlay_filter: 0.5
  teaser: "/assets/images/posts_header/opensslonwindows.jpg"
show_overlay_excerpt: true
categories:
  - more
tags:
  - windows
  - openssl
---

Today I came across a project that I needed to do somethings using [OpenSSL](https://www.openssl.org/) and as a Windows 10 user I wondered how I would install it on my computer or even how to use it.

Turns out that if you installed [Git for Windows](https://git-scm.com/downloads) you already have openssl installed too. To confirm you really have that installed, you can navigate to the `usr/bin` folder inside Git and look for the `openssl.exe` file.

[![opensslonwindows_folder]({{ site.url }}/assets/images/posts_images/opensslonwindows_folder.png)]({{ site.url }}/assets/images/posts_images/opensslonwindows_folder.png)

Now that we know where it is, how do we use it?

You need to open your Git bash and run openssl commands there. Like this:

[![opensslonwindows_gitbash]({{ site.url }}/assets/images/posts_images/opensslonwindows_gitbash.png)]({{ site.url }}/assets/images/posts_images/opensslonwindows_gitbash.png)

Hope you liked this post and that we helped you. Thanks for visiting us!

See you on our next post!
