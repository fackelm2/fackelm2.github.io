---
layout: post
title: How to update Linux Debian (Entwurf)
date: 2024-07-19 18:35:13
description: update mechanism for linux debian
tags: linux todo
categories: linux
featured: false
---

Entwurf

## Update debian
Debian update 

````markup
# sudo apt-get update
````

or with aptitude (F10)
1. Paketliste aktualisieren (u)
2. aktualisierbare markieren (U)
3. Installieren/Entfernen von Paketen (g)

````markup
# sudo aptitude update
````


update are relevant for example also after changes in source.list like adding "contrib non-free"

