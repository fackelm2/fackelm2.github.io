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
<hr>
<br>

For example search for activate or deactivate the "last_updated" tag in al-folio you can find the configuration
file "_config.yml"
````commandline
mypc:~/Projects/mysite.github.io$ egrep -r -e "last_updated"
_posts/2024-07-22-linux-printer.md:last_updated: 2024-08-16 08:14:10
_layouts/post.liquid:      {% if page.last_updated %}, last updated in {{ page.last_updated | date: '%B %d, %Y' }}{% endif %}
..
_includes/footer.liquid:      {% if site.last_updated %}
_includes/footer.liquid:      {% if site.last_updated %}
..
_config.yml:last_updated: true # set to true if you want to display last updated in the footer
..
````