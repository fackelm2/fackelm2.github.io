---
layout: post
title: Connect to GitHub via ssh
date: 2024-07-19 18:32:13
description: using and configure ssh for GitHub
tags: operation linux github
categories: operation
featured: false
---

````markup
$ ssh-add .ssh/id_github_username
Enter passphrase for .ssh/id_github_username: 
Identity added: .ssh/id_github_userna<me (user@name.de)

$ ssh-add .ssh/id_github_username (user@name.de)

$ ssh -i id_github_username -T git@github.com
````

### Github Pages
<a href="https://docs.github.com/en/pages/quickstart">https://docs.github.com/en/pages/quickstart</a>

"You can use GitHub Pages to showcase some open source projects, host a blog, 
or even share your résumé. This guide will help get you started on creating your next website."