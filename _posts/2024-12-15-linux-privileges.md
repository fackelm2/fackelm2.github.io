---
layout: post
title: Dropping Linux privileges
date: 2024-12-15 07:00:10
last_updated: 2024-12-15 07:00:10
description:  Dropping Linux privileges 
tags: linux
categories: linux
featured: false
---

draft

##  Dropping linux privileges

[https://blog.habets.se/2022/03/Dropping-privileges.html]: https://blog.habets.se/2022/03/Dropping-privileges.html "dropping privileges"
[https://blog.habets.se/2022/03/Dropping-privileges.html]

"If you’re writing a tool that takes untrusted input, and you should treat almost all input as untrusted, then it’s a good idea to add a layer of defense against bugs in your code.
What good is a buffer overflow, if the process is fully sandboxed?
This applies to both processes running as root, and as normal users. Though there are some differences."

