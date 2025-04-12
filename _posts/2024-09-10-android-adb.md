---
layout: post
title: Android Programming
date: 2024-09-10 19:00:10
last_updated: 2024-09-10 19:00:10
description: Android Programming
tags: android programming
categories: android
featured: false
---

draft

adb

[android developer adb]: https://developer.android.com/tools/adb?hl=de "https://developer.android.com/tools/adb?hl=de"

[android developer adb]

print all users on the system

```commandline
pm list users
pm list packages -f
pm list permissions -f

adb backup

```

pull /system, /sdcard, /data/app/<packagename>, /data/system/uiderrors.txt

```commandline
adb pull remote local
```

Get Path to pull ..

```commandline
pm list packages -f <packagename>
adb pull <path-to-apk>
```
