---
title: "dpv/issue/180: Update Procedures for  Optional Features"
date: 2024-08-08 14:38:47 +0000
author: Wind4Greg
categories: ["Hyperledger"]
tags: ["dpv"]
permalink: /dpv/issue/180/
comments_file: Hyperledger-dpv-issue-180_comments
---

[_https://github.com/w3c/dpv/issues/180_](https://github.com/w3c/dpv/issues/180)

The *optional features* (anonymous holder binding, pseudonyms with known PID, and pseudonyms with hidden PID) are dependent on two IETF drafts which have recently been updated:

1. [BBS Blind Signatures](https://datatracker.ietf.org/doc/html/draft-kalos-bbs-blind-signatures)
2. [BBS per Verifier Lin](https://datatracker.ietf.org/doc/html/draft-vasilis-bbs-per-verifier-linkability)

The procedures, in particular, sections [3.4.5 Base Proof Serialization (bbs-2023)](https://w3c.github.io/vc-di-bbs/#base-proof-serialization-bbs-2023), [3.4.6 Add Derived Proof (bbs-2023)](https://w3c.github.io/vc-di-bbs/#add-derived-proof-bbs-2023), [3.4.7 Verify Derived Proof (bbs-2023)](https://w3c.github.io/vc-di-bbs/#verify-derived-proof-bbs-2023) and some of their sub-procedures need to be updated to use the updated APIs from these drafts.