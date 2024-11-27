---
title: "Incorrect hashing used in tests for `ecdsa-rdfc-2019` `P-384`"
date: 2024-11-14 16:12:54 +0000
author: sbihel
excerpt: >
  The edge agent does not require to be in a chrome extension. BUT, our SDK must talk cip-30 if that makes sense and be able to communicate with other cardano wallets to create and submit cardano transactions, starting by the prism did operations + their corresponding metadata
categories: hyperledger
tags: identus
comments_file: identus-issue-86_comments
permalink: /identus/86/
url: https://github.com/hyperledger/identus/issues/86
last_modified_at: 2024-11-26 11:18:46 +0000
---


**URL:** https://github.com/hyperledger/identus/issues/86

Hiya, the following tests are failing for `P-384` with our implementation:
- `ecdsa-rdfc-2019 (issuers) VC 1.1` `The "proof" MUST verify with a conformant verifier.`
- `ecdsa-rdfc-2019 (issuers) VC 2.0` `The "proof" MUST verify with a conformant verifier.`
- `ecdsa-rdfc-2019 (verifiers 1.1)` `MUST verify a valid VC with an ecdsa-rdfc-2019 proof.`
- `ecdsa-rdfc-2019 (verifiers 2.0)` `MUST verify a valid VC with an ecdsa-rdfc-2019 proof.`

After trying some random things, I noticed that if we used SHA-256 for [the hash data](https://w3c.github.io/vc-di-ecdsa/#hashing-ecdsa-rdfc-2019) instead of SHA-384 for P-384 keys, then all the tests would pass. So I'm assuming that the implementation used by the tests is incorrect, but maybe our interpretation of the specs is wrong?