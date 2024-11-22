---
title: "bbs-signature/issue/318: Remove lowercase must text"
date: 2024-03-19 09:13:15 +0000
author: PatStLouis
categories: ["DIF"]
tags: ["bbs-signature"]
permalink: /bbs-signature/issue/318/
comments_file: DIF-bbs-signature-issue-318_comments
---

[_https://github.com/decentralized-identity/bbs-signature/issues/318_](https://github.com/decentralized-identity/bbs-signature/issues/318)

The [unlinkability section](https://www.w3.org/TR/vc-data-integrity/#unlinkability) has a lowercase must keyword.


> [...] This characteristic is called unlinkability which ensures that no correlatable data are used in a digitally-signed payload while still providing some level of trust, the sufficiency of which _must_ be determined by each verifier. 

I would suggest to:
A) Make this a normative statement
B) Change the wording to abstract the word `must` to avoid confusion

Suggested change:
> [...] the sufficiency of which ~must~ **has to** be determined by each verifier.
