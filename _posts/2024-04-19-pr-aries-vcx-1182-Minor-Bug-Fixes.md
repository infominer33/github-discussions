---
title: "aries-vcx/pr/1182: Minor Bug Fixes"
date: 2024-04-19 05:37:21 +0000
author: mepeltier
categories: ["Hyperledger"]
tags: ["aries-vcx"]
permalink: /aries-vcx/pr/1182/
comments_file: Hyperledger-aries-vcx-pr-1182_comments
excerpt: >
  Indeed; subtle nuance is that `.get` will return a None if `sd_list` is present and null. We always want to treat it as a list, even if a null is given, so we have to do the `or` syntax here.
---
In our testing, we've come across a few minor bugs that this PR intends to sort out