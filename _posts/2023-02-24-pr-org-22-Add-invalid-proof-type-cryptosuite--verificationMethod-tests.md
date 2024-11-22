---
title: "org/pr/22: Add invalid proof type, cryptosuite, & verificationMethod tests"
date: 2023-02-24 11:09:43 +0000
author: aljones15
categories: ["DIF"]
tags: ["org"]
permalink: /org/pr/22/
comments_file: DIF-org-pr-22_comments
---

[_https://github.com/decentralized-identity/org/pull/22_](https://github.com/decentralized-identity/org/pull/22)

1. Adds a new option `reason` to `verificationFail` so test report can see why verification should have failed
2. Adds a new test that simulates what happens when transformation options are invalid.

Statement tested: "The transformation options MUST contain a type identifier for the cryptographic suite (type), a cryptosuite identifier (cryptosuite), and a verification method (verificationMethod). "