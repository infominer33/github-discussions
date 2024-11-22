---
title: "identus/issue/75: Some examples have the wrong / old context version"
date: 2024-10-21 14:18:04 +0000
author: dlongley
categories: ["DIF"]
tags: ["identus"]
permalink: /identus/issue/75/
comments_file: DIF-identus-issue-75_comments
---

[_https://github.com/hyperledger/identus/issues/75_](https://github.com/hyperledger/identus/issues/75)

Example 2:
https://w3c.github.io/vc-di-eddsa/#example-an-ed25519-public-key-encoded-as-a-multikey-in-a-controller-document

Needs the context updated from: "https://w3id.org/security/data-integrity/v1" to "https://w3id.org/security/multikey/v1".

Example 6:
https://w3c.github.io/vc-di-eddsa/#example-an-ed25519-digital-signature-expressed-as-a-ed25519signature2020

Needs the context updated from: "https://w3id.org/security/data-integrity/v1" to "https://w3id.org/security/suites/ed25519-2020/v1".