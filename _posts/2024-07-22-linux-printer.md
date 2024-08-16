---
layout: post
title: Linux Printer (draft)
date: 2024-07-22 17:37:00
description: Linux Printer
tags: linux printer personalnote
categories: linux
featured: false
---

draft

LÖSUNG
Samsung M2525W

a) Drucker eingerichtet mit CUPS unter http://localhost:631/admin
b) Fehler bei Drucken -> error log -> /var/log/cups/error_log
D [05/May/2024:13:12:40 +0200] [Job 21] Samsung_ML-2525W_Series_on_192.168.178.91: error while loading shared libraries: libcupsimage.so.2: cannot open shared object file: No such file or directory
c) install libcupsimage
d) restart
e) first print with samsung printer M2525W over Network

TIPPS GUT : https://www.javatpoint.com/linux-print
DRUCKER STATUS

fackelm2@mutterschiff:~/PDF$ lpstat -p -d
Drucker PDF ist im Leerlauf.  Aktiviert seit So 05 Mai 2024 12:20:32 CEST
Drucker Samsung_ML-2525W_Series ist im Leerlauf.  Aktiviert seit So 05 Mai 2024 12:26:48 CEST
        Rendering completed
systemvoreingestelltes Ziel: PDF

DRUCKEN EINER DATEI
fackelm2@mutterschiff:~/PDF$ lpr -P Samsung_ML-2525W_Series ../MERKE/merke-android.txt

SET DEFAULT PRINTER
lpoptions -d < printer name>

TIPPS
https://www.zdv.uni-mainz.de/zdv-drucker-unter-linux-einrichten/

Error Messages
var/log/cups/error.log

#Verwaltungsschnittstelle CUPS
http://localhost:631/admin

