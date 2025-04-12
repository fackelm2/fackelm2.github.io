---
layout: post
title: How to use Pycharm on Linux Debian (draft)
date: 2024-07-19 05:01:13
last_updated: 2024-08-16 08:14:10
description: Tipps for Pycharm on Linux Debian
tags: python pycharm personalnote
categories: python
featured: false
---

draft

Linux Debian Pycharm Install

```markdown
#debian install
apt-get install openjdk-XX-jdk

tar -xvfz professional-pycharm....gz
./bin/pycharm.sh
```

Set pycharm to PATH directory

```commandline
linux:~$ ls -al /usr/local/bin
insgesamt 200
drwxr-xr-x  2 root root   4096 13. Jul 12:49 .
drwxr-xr-x 10 root root   4096 25. Feb 2024  ..
lrwxrwxrwx  1 root root     52 13. Jul 12:49 pycharm -> /home/fackelm2/Tools/pycharm-2024.1.4/bin/pycharm.sh
-rwxr-xr-x  1 root root 196592 16. Mär 22:45 scrcpy

linux:~$ echo $PATH
/usr/local/bin:/usr/bin:/bin:/usr/local/games:/usr/games
```
