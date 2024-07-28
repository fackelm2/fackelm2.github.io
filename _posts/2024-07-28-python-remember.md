---
layout: post
title: Python notice informations (draft)
date: 2024-07-27 06:55:10
description: Python notice informations for using python
tags: python notice
categories: python
featured: false
---

draft 

Python programming notice
 
Show functions in module / program
````markdown
>>> dir(progname)
````


build main function (def main()) with no "side effects" while importing (if __name__ == '__main__') 
````markdown
def main():
        print('hello i am userA')

if __name__ == '__main__':
        main()  
````
