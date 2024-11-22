---
title: "identus/issue/22: Signing validation is not defined."
date: 2024-07-03 13:27:43 +0000
author: TomCJones
categories: ["DIF"]
tags: ["identus"]
permalink: /identus/issue/22/
comments_file: DIF-identus-issue-22_comments
---

[_https://github.com/hyperledger/identus/issues/22_](https://github.com/hyperledger/identus/issues/22)

As i understand signing, the only way to validate a signature is to resolve the did at the exact (with in a few seconds) time that the signature was made. The did resolution times are already at least 10% of a minute and that time will undoubtably climb as the methods become more popular. I would suggest that the only way for signature validation to be feasible is to create some sort of caching of the did (and/or did doc). Another way to put this is that did should have a validity period of (say) one week. Otherwise every signature validation will require another did resolution.