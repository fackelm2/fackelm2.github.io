---
layout: post
title: Markup for the Jekyll Al-Folio Theme
date: 2024-07-26 08:37:00
description: Using the Github Flavored Markdown in the Al-Folio Theme
tags: linux al-folio jekyll tool
categories: linux
featured: false
---

What is Jekyll? <a href="https://de.wikipedia.org/wiki/Jekyll_(Software)">https://de.wikipedia.org/wiki/Jekyll_(Software)</a>

Jekyll ist eine in der Programmiersprache Ruby geschriebene Software, 
die zur Erstellung statischer Webseiten dient. 
Dabei kombiniert sie vereinfachte Markup-Texte mit Designvorlagen und erzeugt für jede 
Teilseite ein statisches Abbild als HTML-Datei.

Der Jekyll-Quellcode wird unter der MIT-Lizenz als Open Source bereitgestellt.

Häufig eingesetzt wird Jekyll zur Erstellung von Blogs, aber auch Softwaresysteme wie GitHub 
oder andere Content-Management-Systeme nutzen Jekyll im Hintergrund zur Erstellung von Webseiten. 


to use the Al-Folio Theme you must follow the instructions on the Al-Folio github site:
- download /home/user/PycharmProjects/<name>.github.io
- change informations, text and images etc.
- start local <name>.github.io$

````markdown
sudo docker-compose up
````

Use a Browser to connect to your instance 
````markdown
localhost:8080
````

A god starting point is <a href="https://github.com/alshedivat/al-folio">https://github.com/alshedivat/al-folio</a>

also a good instruction site on medium.com:<br> 
<a href="https://medium.com/@carlbettosi/create-a-personal-academic-website-easily-with-github-pages-and-jekyll-minimal-coding-f1115eeb5ab7">
https://medium.com/@carlbettosi/create-a-personal-academic-website-easily-with-github-pages-and-jekyll-minimal-coding-f1115eeb5ab7</a>


Github Actions: Al Folio on Github (check links)

````angular2html
...
name: Link Checker 🔗
        uses: lycheeverse/lychee-action@v1.9.0
        with:
          fail: true
          # only check local links
          args: --offline --remap '_site(/?.*)/assets/(.*) _site/assets/$2' --verbose --no-progress '_site/**/*.html'

````

