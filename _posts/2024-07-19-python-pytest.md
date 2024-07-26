---
layout: post
title: How to Unit-Tests with Pytest  
date: 2024-07-19 05:01:13
description: Writing unit tests with the Pytest framework for Python
tags: python
categories: python
featured: true
---

<hr><br>
Troubleshooting Pytest Error: 
````markdown
E   ModuleNotFoundError: No module named 
````

Solution: use the PYTHONPATH env. var (see on [stackoverflow pythonpath])

[stackoverflow pythonpath]: /https://stackoverflow.com/questions/54895002/modulenotfounderror-with-pytest  "https://stackoverflow.com/questions/54895002/modulenotfounderror-with-pytest"

````markdown
PYTHONPATH=. pytest

As mentioned by @J_H, you need to explicitly add the root directory of your project, 
since pytest only adds to sys.path directories where test files are (which is why @Mak2006's answer worked.)
Good practice: use a Makefile or some other automation tool

If you do not want to type that long command all the time, one option is to create a Makefile in your project's root dir with, e.g., the following:

.PHONY: test
test:
    PYTHONPATH=. pytest

Which allows you to simply run:
make test
````

<hr><br>
Pytest Links from antonywritescode

[Youtube: search pytest anthonywritescode]: https://www.youtube.com/@anthonywritescode/search?query=pytest
[Youtube: search pytest anthonywritescode]

[Youtube: getting started with pytest (beginner - intermediate) anthony explains #518]: https://www.youtube.com/watch?v=mzlH8lp4ISA&t=76s
[Youtube: getting started with pytest (beginner - intermediate) anthony explains #518]

[Test Driven Development]: https://www.youtube.com/watch?v=JmMxU8ljiOg
[Test Driven Development]

[python: raise SystemExit (beginner - intermediate) anthony explains #331]: https://www.youtube.com/watch?v=ZbeSPc5wL0g  
[python: raise SystemExit (beginner - intermediate) anthony explains #331]

[pytest: testing env variables (intermediate) anthony explains #317]: https://www.youtube.com/watch?v=N15X_pQHckQ
[pytest: testing env variables (intermediate) anthony explains #317]

[pytest: xfail vs xpass and all test statuses (beginner - intermediate) anthony explains #260]: https://www.youtube.com/watch?v=uzodcMcHbJU
[pytest: xfail vs xpass and all test statuses (beginner - intermediate) anthony explains #260]

[replay - pytest, github actions, and advent of code - replay 2020-05-23]: https://www.youtube.com/watch?v=dBekbQF-0Hk
[replay - pytest, github actions, and advent of code - replay 2020-05-23]

[replay - pytest-nunit + iptables - 2020-08-03]: https://www.youtube.com/watch?v=oBKtF_FWBj8
[replay - pytest-nunit + iptables - 2020-08-03]

[python cli tested with pytest - (beginner to intermediate) anthony explains #001]: https://www.youtube.com/watch?v=sv46294LoP8
[python cli tested with pytest - (beginner to intermediate) anthony explains #001]

[pytest: parametrize permutation (intermediate) anthony explains #174]: https://www.youtube.com/watch?v=QIUrd327tOQ
[pytest: parametrize permutation (intermediate) anthony explains #174]

[pytest's parametrize (beginner - intermediate) anthony explains #027]: https://www.youtube.com/watch?v=aQH7hyJn-No
[pytest's parametrize (beginner - intermediate) anthony explains #027]

[pytest: everything you need to know about fixtures (intermediate) anthony explains #487]: https://www.youtube.com/watch?v=ScEQRKwUePI
[pytest: everything you need to know about fixtures (intermediate) anthony explains #487]

[pytest: parametrize permutation (intermediate) anthony explains #174]: https://www.youtube.com/watch?v=QIUrd327tOQ
[pytest: parametrize permutation (intermediate) anthony explains #174]

[pytest: testing exceptions (beginner - intermediate) anthony explains #176]: https://www.youtube.com/watch?v=6nRxZyQwwlE
[pytest: testing exceptions (beginner - intermediate) anthony explains #176]

[are your python tests even running? (intermediate) anthony explains #438]: https://www.youtube.com/watch?v=0nPS_vVmhp0
[are your python tests even running? (intermediate) anthony explains #438]

[why pytest.mark.usefixtures? (intermediate) anthony explains #098]: https://www.youtube.com/watch?v=BE2v1VCmGwg 
[why pytest.mark.usefixtures? (intermediate) anthony explains #098]

[replay - pytest capfd fixing - 2021-04-26]: https://www.youtube.com/watch?v=a33dRrLO8ws 
[replay - pytest capfd fixing - 2021-04-26]

[pytest: everything you need to know about fixtures (intermediate) anthony explains #487]: https://www.youtube.com/watch?v=ScEQRKwUePI  
[pytest: everything you need to know about fixtures (intermediate) anthony explains #487]

[testing output with pytest (beginner - intermediate) anthony explains #246]: https://www.youtube.com/watch?v=dN-pVt7i4Us 
[testing output with pytest (beginner - intermediate) anthony explains #246]

[I don't use pytest-cov (intermediate) anthony explains #489]: https://www.youtube.com/watch?v=sPgvHGkmd0U 
[I don't use pytest-cov (intermediate) anthony explains #489]

<hr><br>
Pytest Links from Pycharm

[How to write unit tests in Python using pytest and PyCharm]: https://www.youtube.com/watch?v=Z0f00BdJ3yw
[How to write unit tests in Python using pytest and PyCharm]

<hr><br>
Pytest links from others

[pytest Basics: Introduction to Tests]: https://www.youtube.com/watch?v=3slDyeQYq8A&t=14s
[pytest Basics: Introduction to Tests]

[Pytest Tutorial – How to Test Python Code (freeCodeCamp.org)]: https://www.youtube.com/watch?v=cHYq1MRoyI0
[Pytest Tutorial – How to Test Python Code (freeCodeCamp.org)]

<hr><br>
TOX (anthonywritescode)

Command line driven CI frontend and development task automation tool 
(<a href="https://github.com/tox-dev/tox">https://github.com/tox-dev/tox</a>)

Tox aims to automate and standardize testing in Python. It is part of a larger vision of easing the packaging, 
testing and release process of Python software (alongside pytest and devpi).

Links:

[https://tox.wiki/en/latest/user_guide.html#basic-example]: https://tox.wiki/en/latest/user_guide.html#basic-example
[https://tox.wiki/en/latest/user_guide.html#basic-example]

[https://www.youtube.com/watch?v=SFqna5ilqig]: https://www.youtube.com/watch?v=SFqna5ilqig
[https://www.youtube.com/watch?v=SFqna5ilqig]
