---
layout: post
title: Debian Suspend Mode Configuration (draft)
date: 2024-07-26 10:26:13
last_updated: 2024-08-16 08:14:10
description: Debian suspend mode  
tags: linux todo personalnote
categories: linux
featured: false
---

draft

````markup 
nts to blank the screen out of the box. To prevent, try putting:
$ xset dpms 0 0 0 && xset s noblank && xset s off
in .bashrc

to send to suspend:
$systemctl suspend

for systems which should never attempt anay type of suspension, the targets scan be disabled at the systemd level:
$sudo systemctl mask sleep.target suspend.target hibernate.target hybrid-sleep.target 

to re-enable hibernate and supend use the following command:
$sudo systemctl unmaks sleep.target suspend.target hibernate.target hybrid-sleep.target 

Also you can create /etc/systemd/sleep.conf.d/nosuspend.conf :
[Sleep]
AllowSuspend=no
AllowHibernation=no
AllowSuspendThenHibernate=no
AllowHybridSleep=no

The log for suspend and resume processes are in file 
$cat /var/log/pm-suspend.log

Kernel Suspend testing facility
freezer
devices
platform
processors
core

$systemctl mask sleep.target suspend.target hibernate.target hybrid-sleep.target
Created symlink /etc/systemd/system/sleep.target → /dev/null.
Created symlink /etc/systemd/system/suspend.target → /dev/null.
Created symlink /etc/systemd/system/hibernate.target → /dev/null.
Created symlink /etc/systemd/system/hybrid-sleep.target → /dev/null.
````
