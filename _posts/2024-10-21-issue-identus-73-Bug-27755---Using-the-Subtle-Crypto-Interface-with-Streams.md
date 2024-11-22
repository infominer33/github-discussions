---
title: "identus/issue/73: Bug 27755 - Using the Subtle Crypto Interface with Streams"
date: 2024-10-21 14:15:57 +0000
author: mwatson2
categories: ["DIF"]
tags: ["identus"]
permalink: /identus/issue/73/
comments_file: DIF-identus-issue-73_comments
---

[_https://github.com/hyperledger/identus/issues/73_](https://github.com/hyperledger/identus/issues/73)

[Bug 27755](https://www.w3.org/Bugs/Public/show_bug.cgi?id=27755):

Though the StreamsAPI is referenced in Informative Reference, the functions under window.crypto.subtle are specified with only one-shot data inputs.

Use-cases: Data may not be available at once. Data may be too huge to keep in memory.

For encrypt()/decrypt() it would make sense to have a streaming readable output if the input is a readable stream.
