---
layout: post
title: Recursive search for a word in files under Linux 
date: 2024-08-04 20:14:10
last_updated: 2024-08-16 08:14:10
description: Search for a text in a file in all directories
tags: linux howto personalnote
categories: linux
featured: false
---

To recursively search for a word within files under Linux, you can use the grep command.

The following command searches all files in the current directory and all subdirectories for a specific word:

````
$ egrep -r -e "serch term"
````

<br>
<br>
<hr>
<br>

For example, if you want to enable or disable the "last_updated" tag in your al-folio tree, 
you can find the configuration file "_config.yml"


````commandline
mypc:~/Projects/mysite.github.io$ egrep -r -e "last_updated"
_posts/2024-07-22-linux-printer.md:last_updated: 2024-08-16 08:14:10
..
_config.yml:last_updated: true # set to true if you want to display last updated in the footer
..
````