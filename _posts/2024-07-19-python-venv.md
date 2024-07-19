---
layout: post
title: Using Virtual Environment in Python
date: 2024-07-19 05:10:00
description: cheatsheat for using venv in python
tags: python
categories: python
featured: true
---

https://python.land/virtual-environments/virtualenv#Python_venv_activation

````markdown
```c++
https://python.land/virtual-environments/virtualenv#Python_venv_activation
```
````

```c++
https://python.land/virtual-environments/virtualenv#Python_venv_activation
```

For displaying code in a list item, you have to be aware of the indentation, as stated in this [Stackoverflow answer](https://stackoverflow.com/questions/34987908/embed-a-code-block-in-a-list-item-with-proper-indentation-in-kramdown/38090598#38090598). You must indent your code by **(3 \* bullet_indent_level)** spaces. This is because kramdown (the markdown engine used by Jekyll) indentation for the code block in lists is determined by the column number of the first non-space character after the list item marker. For example:

````markdown
1. We can put fenced code blocks inside nested bullets, too.

   1. Like this:

      ```c
      https://python.land/virtual-environments/virtualenv#Python_venv_activation
      ```

   2. The key is to indent your fenced block in the same line as the first character of the line.
````

Which displays:

1. We can put fenced code blocks inside nested bullets, too.

   1. Like this:

      ```c
      https://python.land/virtual-environments/virtualenv#Python_venv_activation
      ```

   2. The key is to indent your fenced block in the same line as the first character of the line.

By default, it does not display line numbers. If you want to display line numbers for every code block, you can set `kramdown.syntax_highlighter_opts.block.line_numbers` to true in your `_config.yml` file.

tag
{% raw %}
{% highlight c++ linenos %} <br/> https://python.land/virtual-environments/virtualenv#Python_venv_activation <br/> {% endhighlight %}
{% endraw %}

The keyword `linenos` triggers display of line numbers.
Produces something like this:

{% highlight c++ linenos %}

int main(int argc, char const \*argv[])
{
string myString;

    https://python.land/virtual-environments/virtualenv#Python_venv_activation

}

{% endhighlight %}

Markdown style:
```python
import pandas as pd

numbers = []
for i in numbers:
    echo i
```