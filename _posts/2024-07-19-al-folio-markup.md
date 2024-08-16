---
layout: post
title: Markup for the Jekyll Al-Folio Theme
date: 2024-07-26 10:20:00
description: Using the Github Flavored markup in the Al-Folio Theme
tags: linux al-folio jekyll tool personalnote
categories: linux
featured: false
---
What is [markup]?

[markup]: /https://github.github.com/gfm/#introduction "markup"

"markup is a plain text format for writing structured documents, based on conventions for indicating formatting in 
email and usenet posts. It was developed by John Gruber (with help from Aaron Swartz) and released in 2004 in the 
form of a syntax description and a Perl script (markup.pl) for converting markup to HTML. In the next decade, 
dozens of implementations were developed in many languages. Some extended the original markup syntax with 
conventions for footnotes, tables, and other document elements. Some allowed markup documents to be rendered in 
formats other than HTML. Websites like Reddit, StackOverflow, and GitHub had millions of people using markup. 
And markup started to be used beyond the web, to author books, articles, slide shows, letters, and lecture notes."

Default Al-folio Markup is GitHub Flavored markup - GFM
(<a href="https://github.github.com/gfm/">https://github.github.com/gfm/</a>)


<hr>
Example 1 [ markup / markdown ]

\`\`\`\`
````
[example text]: /https://nmit.de "Network Management IT" 
[example text]
````

\`\`\`\`markup
````markup
[example text]: /https://nmit.de "Network Management IT" 
[example text]
````

\`\`\`\`markdown
````markdown
[example text]: /https://nmit.de "Network Management IT" 
[example text]
````



<hr>
Example 2 [ LINK ]

````markup
[Markup Instructions]: /https://github.github.com/gfm/ "Markup Instructions" 
[Markup Instructions]
````

become to:

[Markup Instructions]: /https://github.github.com/gfm/ "Markup Instructions" 
[Markup Instructions]

<hr>
Example 3 [ LINK in text]

First write the "palceholder" in text, than you can define the URL at any place ..

````
What is [markup]?

[markup]: /https://github.github.com/gfm/#introduction "markup"
````
become to:

What is [markup]?

[markup]: /https://github.github.com/gfm/#introduction "markup"
<hr>
Example 2 [ CODE FORMAT]

````markup
\````
def Code example
    just a test
\````
````

become to:

````
def Code example
    just a test
````
<hr>

Example 4 [ CODE FORMAT]

\`\`\`python
import pandas as pd ...
\`\`\`

becomes to:
```python
import pandas as pd

numbers = []
for i in numbers:
    echo i
```


