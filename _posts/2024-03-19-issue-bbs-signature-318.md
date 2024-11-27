---
title: "Remove lowercase must text"
date: 2024-03-19 09:13:15 +0000
author: PatStLouis
excerpt: >
  PR #319 was raised to address this issue, closing.
categories: decentralized-identity
tags: bbs-signature
comments_file: bbs-signature-issue-318_comments
permalink: /bbs-signature/318/
url: https://github.com/decentralized-identity/bbs-signature/issues/318
last_modified_at: 2024-11-17 19:11:39 +0000
---


**URL:** https://github.com/decentralized-identity/bbs-signature/issues/318

The [unlinkability section](https://www.w3.org/TR/vc-data-integrity/#unlinkability) has a lowercase must keyword.


> [...] This characteristic is called unlinkability which ensures that no correlatable data are used in a digitally-signed payload while still providing some level of trust, the sufficiency of which _must_ be determined by each verifier. 

I would suggest to:
A) Make this a normative statement
B) Change the wording to abstract the word `must` to avoid confusion

Suggested change:
> [...] the sufficiency of which ~must~ **has to** be determined by each verifier.
