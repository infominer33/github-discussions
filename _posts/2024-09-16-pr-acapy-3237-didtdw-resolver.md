---
title: "acapy/pr/3237: did:tdw resolver"
date: 2024-09-16 22:01:14 +0000
author: jamshale
categories: ["OWF"]
tags: ["acapy"]
permalink: /acapy/pr/3237/
comments_file: OWF-acapy-pr-3237_comments
---

[_https://github.com/openwallet-foundation/acapy/pull/3237_](https://github.com/openwallet-foundation/acapy/pull/3237)

- Uses the trustdidweb-py library to implement the resolver. 
- Plugs the resolve endpoint and library into the base_resolver class for caching and future other resolution. 