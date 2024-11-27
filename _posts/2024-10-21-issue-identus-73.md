---
title: "Bug 27755 - Using the Subtle Crypto Interface with Streams"
date: 2024-10-21 14:15:57 +0000
author: mwatson2
excerpt: >
  Oh, I missed that proposal. Very elegant. +1 from me. (I'm jpsugar-flow, but this is not work-related for me.)
categories: hyperledger
tags: identus
comments_file: identus-issue-73_comments
permalink: /identus/73/
url: https://github.com/hyperledger/identus/issues/73
last_modified_at: 2024-11-22 19:03:40 +0000
---


**URL:** https://github.com/hyperledger/identus/issues/73

[Bug 27755](https://www.w3.org/Bugs/Public/show_bug.cgi?id=27755):

Though the StreamsAPI is referenced in Informative Reference, the functions under window.crypto.subtle are specified with only one-shot data inputs.

Use-cases: Data may not be available at once. Data may be too huge to keep in memory.

For encrypt()/decrypt() it would make sense to have a streaming readable output if the input is a readable stream.
