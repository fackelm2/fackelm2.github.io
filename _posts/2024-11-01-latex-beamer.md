---
layout: post
title: Presentation with Latex (beamer)
date: 2024-11-01 07:00:10
last_updated: 2024-11-01 07:00:10
description: How to present with beamer (Latex)?
tags: linux latex
categories: linux
featured: false
---

## LaTex beamer

"Beamer is a LaTeX document class for creating presentation slides, with a wide range of templates and a set of features for making slideshow effects." (wikipedia)

supports 
* pdfLaTeX
* LaTeX
* dvips
* LuaLaTeX
* XeLaTeX 

process
* install linux LaTex
* use documentclass beamer (in x.tex file)
* translate tex file into pdf file: pdflatex beamer.tex

#### good starting points 
* [LaTex beamer examples (Uni Freiburg)]
* [LaTex beamer tex file tutorial on Youtube]
* [LaTex beamer on wikipedia]

[LaTEx beamer examples (Uni Freiburg)]:http://www2.informatik.uni-freiburg.de/~frank/ENG/latex-course/latex-course-3/latex-course-3_en.html "Beamer Examples"
[LaTex beamer tex file tutorial on Youtube]:https://www.youtube.com/watch?v=0fsWGg81RwU "Tutorial Latex beamer"
[LaTex beamer on wikipedia]:https://de.wikipedia.org/wiki/Beamer_(LaTeX) "Wikipedia beamer"

#### themes
* [Ritsumeikan theme] 
* Warsaw
* Hanover
* CambridgeUS

[Ritsumeikan theme]:https://github.com/ming-hao-xu/Ritsumeikan-beamer "Ritsumeikan theme"

## LaTex foiltex
solid and small solution for minimalistic presentations 

````text
latex x.tex
dvi2ps x.dvi > x.ps
ps2pdf x.ps 
qpdfview x.pdf

````


