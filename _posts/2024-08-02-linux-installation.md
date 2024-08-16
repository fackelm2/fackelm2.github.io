---
layout: post
title: Linux local deb paket installation
date: 2024-08-02 11:24:10
last_updated: 2024-08-16 08:14:10
description: Linux local deb paket installation
tags: linux personalnote
categories: linux 
featured: false
---

draft 

[Linux lokale Pakete installieren]: https://debianforum.de/forum/viewtopic.php?t=183470 "https://debianforum.de/forum/viewtopic.php?t=183470"
[Linux lokale Pakete installieren]

helpfull information: apt zur Installation lokaler deb-Pakete?

Die Option -f macht hier etwas anderes, als man es von anderen Programmen für diesen Fall tatsächlich gewohnt ist.
Du kannst mit apt aber problemlos lokale .deb-Dateien installieren. Du musst nur darauf achten, 
das der Pfad eindeutig als solcher zu erkennen ist, also mit einem / oder ./ anfängt:

Code: Alles auswählen
````
# apt install /home/user/foobar.deb
# apt install ./foobar.deb
````

