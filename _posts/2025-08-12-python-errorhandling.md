---
layout: post
title: Python Error Handling
date: 2025-06-12 05:00:10
last_updated: 2025-06-12 05:00:10
description: Python Error Handling the right way
tags: python programming
categories: python
featured: false
---
[Python Error Handling Guide]: https://blog.miguelgrinberg.com/post/the-ultimate-guide-to-error-handling-in-python "https://blog.miguelgrinberg.com/post/the-ultimate-guide-to-error-handling-in-python"


## Python Error Handling (HowTo)
Ever asked how to do Python Error Handling the right way? 
If found this very good guide: [Python Error Handling Guide]


a) Recoverable vs. Non-Recoverable Errors

- Type 1: Handling New Recoverable Errors
  - recover from the error and continue, without bothering anyone else!

``` 
def add_apkid_to_database(apkid):
    # ...
    if apkid.year is None:
        apkid.year = 'Unknown'
    # ...```
```

- Type 2: Handling Bubbled-Up Recoverable Errors
  - We use EAFP to catch the error, and then we do whatever needs to be done to recover from it and continue.
 

```
def add_apkid_to_database(apkid):
    # ...
    try:
        category = get_category_from_database(apkid.category)
    except NotFound:
        category = add_categroy_to_database(apkid.category)
    # ...
```

here the code that needs to handle the error knows how to adjust the state of the application to continue running, 
so it can consume the error and continue

- Type 3: Handling New Non-Recoverable Errors
 
the code does not know what to do and cannot continue
stop the current function and alert one level up the call stack of the error, 
with the hope that the caller knows what to do
in Python the preferred mechanism to notify the caller of an error is 
to raise an exception

```
def add_apkid_to_database(apkid):
    # ...
    if apkid.name is None:
        raise ValueError('The Android App must have a name')
    # ...
```

For many errors the exceptions that come with Python can be used, 
but you can always create your own exception subclasses. 

Example implemented with a custom exception:

```
class ValidationError(Exception):
    pass

# ...

def add_apkid_to_database(apkid):
    # ...
    if apkid.name is None:
        raise ValidationError('The Android App must have a name')
    # ...
```

- Type 4: Handling Bubbled-Up Non-Recoverable Errors

in this case we do  nothing
Not handling errors can be a great error handling strategy
Eventually the exceptions will reach a level at which the code knows 
how to do recovery (at that point they will be considered type 2 errors)

Moving error handling code to higher-level functions is a very good strategy 
that helps you have clean and maintainable code.


Catching All Exceptions

You should design your applications so that it is impossible for an exception 
to ever reach the Python layer. And you do this by adding a try/except block 
at the highest level that catches the runaway exceptions.
