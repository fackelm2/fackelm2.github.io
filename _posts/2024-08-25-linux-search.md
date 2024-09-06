---
layout: post
title: Searching in Linux
date: 2024-08-27 18:00:10
last_updated: 2024-08-27 18:00:10
description: how to search in linux
tags: linux search
categories: linux
featured: false
---

draft
Linux 

find file(s) from 15.05.2024
````
find /path/to/directory -type f -newermt 2024-05-15 ! -newermt 2024-05-16

````

find string in file(s)
````

egrep -r -e "text"

````
d