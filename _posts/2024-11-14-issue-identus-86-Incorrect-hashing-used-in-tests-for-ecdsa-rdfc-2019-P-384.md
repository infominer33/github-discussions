---
title: "identus/issue/86: Incorrect hashing used in tests for `ecdsa-rdfc-2019` `P-384`"
date: 2024-11-14 16:12:54 +0000
author: sbihel
categories: ["Hyperledger"]
tags: ["identus"]
permalink: /identus/issue/86/
comments_file: Hyperledger-identus-issue-86_comments
---

[_https://github.com/hyperledger/identus/issues/86_](https://github.com/hyperledger/identus/issues/86)

Hiya, the following tests are failing for `P-384` with our implementation:
- `ecdsa-rdfc-2019 (issuers) VC 1.1` `The "proof" MUST verify with a conformant verifier.`
- `ecdsa-rdfc-2019 (issuers) VC 2.0` `The "proof" MUST verify with a conformant verifier.`
- `ecdsa-rdfc-2019 (verifiers 1.1)` `MUST verify a valid VC with an ecdsa-rdfc-2019 proof.`
- `ecdsa-rdfc-2019 (verifiers 2.0)` `MUST verify a valid VC with an ecdsa-rdfc-2019 proof.`

After trying some random things, I noticed that if we used SHA-256 for [the hash data](https://w3c.github.io/vc-di-ecdsa/#hashing-ecdsa-rdfc-2019) instead of SHA-384 for P-384 keys, then all the tests would pass. So I'm assuming that the implementation used by the tests is incorrect, but maybe our interpretation of the specs is wrong?