---
title: "Many errors in rocksdb/_rocksdb.pyx cause build failure"
date: 2024-02-07 07:19:56 +0000
author: swcurran
excerpt: >
  It's unreasonable to consider moving this thread or to re-duplicate it somewhere else.  
  I'll continue to reply and update it here.
categories: decentralized-identity
tags: uni-resolver-driver-did-key
comments_file: uni-resolver-driver-did-key-issue-9_comments
permalink: /uni-resolver-driver-did-key/9/
url: https://github.com/decentralized-identity/uni-resolver-driver-did-key/issues/9
last_modified_at: 2024-11-26 00:47:53 +0000
---


**URL:** https://github.com/decentralized-identity/uni-resolver-driver-did-key/issues/9

The first error is:

```
/tmp/pip-build-clvy4twe/python-rocksdb/.eggs/Cython-3.0.8-py3.5.egg/Cython/Compiler/Main.py:381: FutureWarning: Cython directive 'language_level' not set, using '3str' for now (Py3). This has changed from earlier releases! File: /tmp/pip-build-clvy4twe/python-rocksdb/rocksdb/_rocksdb.pyx
```

After that, there are hundreds of errors in the module — many referencing a missing “gil”.