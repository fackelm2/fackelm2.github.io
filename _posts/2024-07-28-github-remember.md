---
layout: post
title: Github notice (draft)
date: 2024-07-27 13:55:10
description: Github notice
tags: github notice
categories: github
featured: false
---

draft 

GitHub - Display Language of Code 

[GitHub Linguist]: https://github.com/github/linguist "https://github.com/github/linguist"
[GitHub Linguist]

Install the gem: (debian package: ruby-github-linguist)
```
gem install github-linguist
```
[ruby environment]: https://rvm.io/rvm/install "https://rvm.io/rvm/install"
You need a working [ruby environment]!

Install on Debian https://github.com/github-linguist/linguist/tree/master?tab=readme-ov-file
```
sudo apt-get install build-essential cmake pkg-config libicu-dev zlib1g-dev libcurl4-openssl-dev libssl-dev ruby-dev
sudo apt-get install ruby-github-linguist

/Projects/RepositoryDirectory$ github-linguist

/Projects/RepositoryDirectory$ github-linguist 
67.73%  5490455    HTML
15.45%  1252144    SCSS
12.40%  1005102    JavaScript
2.13%   172684     CSS
1.93%   156500     Liquid
0.25%   20185      Ruby
0.06%   4525       TeX
0.04%   3327       Shell
0.01%   865        Jupyter Notebook
0.01%   847        Dockerfile

```


[Display false Language in Github]: https://stackoverflow.com/questions/42544813/paths-not-excluded-from-github-language-statistics "https://stackoverflow.com/questions/42544813/paths-not-excluded-from-github-language-statistics"
[Display false Language in Github]

### Example pictures 

The screenshot on the right shows the used language used in this repository. The main language is Python, but it shows rich-text

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/github-language-01.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>


