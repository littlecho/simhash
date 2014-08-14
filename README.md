simhash
===========

This repository is a patched version of liangsun's implementation of [Simhash](https://github.com/liangsun/simhash)



## Getting Started
You can refer to the guide which written by liangsun:
<http://liangsun.org/posts/a-python-implementation-of-simhash-algorithm/>


## What part is patched in this version of Simhash implemetation in Python?

In order to be more happy to working with utf-8 encoding strings and remove the punctuation within the input string during fingerprint generation, the following changes are made in __init__.py.


1. reg is assigned with re.compile(r'\w', re.UNICODE) instead of ur'[\w\u4e00-\u9fff]+', which will not limit the matching in Chinese and ASCII only mode.
2. The slide function in the class of Simhash is modified by setting the width to 1, which split the string into 'words' and each word is a token.


