---
title: "aries-endorser-service/pr/96: Add algorithm suites (2 -> 1)"
date: 2024-05-22 21:22:39 +0000
author: aljones15
categories: ["Hyperledger"]
tags: ["aries-endorser-service"]
permalink: /aries-endorser-service/pr/96/
comments_file: Hyperledger-aries-endorser-service-pr-96_comments
---

[_https://github.com/hyperledger/aries-endorser-service/pull/96_](https://github.com/hyperledger/aries-endorser-service/pull/96)

Algorithms is the largest section in the ecdsa spec.
This PR collects each individual algorithm suite for each cryptosuite after review
Add Tests for

- [x] ecdsa-rdfc-2019 (@aljones15 )
- [x] ecdsa-jcs-2019 (@PatStLouis 
- [ ] ecdsa-sd-2023 (@aljones15)


This PR is intended to be the major stop for all of the Algorithm related PRs and tests. It should be merged into `add-conformance-suite` or `main` on approval.