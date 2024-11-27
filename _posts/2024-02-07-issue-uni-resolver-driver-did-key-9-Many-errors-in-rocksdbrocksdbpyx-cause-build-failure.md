---
title: "uni-resolver-driver-did-key/issue/9: Many errors in rocksdb/_rocksdb.pyx cause build failure"
date: 2024-02-07 07:19:56 +0000
author: swcurran
categories: ["DIF"]
tags: ["uni-resolver-driver-did-key"]
permalink: /uni-resolver-driver-did-key/issue/9/
comments_file: DIF-uni-resolver-driver-did-key-issue-9_comments
excerpt: >
  It's unreasonable to consider moving this thread or to re-duplicate it somewhere else.    I'll continue to reply and update it here.
---
The first error is:

```
/tmp/pip-build-clvy4twe/python-rocksdb/.eggs/Cython-3.0.8-py3.5.egg/Cython/Compiler/Main.py:381: FutureWarning: Cython directive 'language_level' not set, using '3str' for now (Py3). This has changed from earlier releases! File: /tmp/pip-build-clvy4twe/python-rocksdb/rocksdb/_rocksdb.pyx
```

After that, there are hundreds of errors in the module — many referencing a missing “gil”.