---
title: "org/issue/33: Distinction between the definitions of Verification and Authentication"
date: 2024-03-23 19:27:01 +0000
author: verocri
categories: ["DIF"]
tags: ["org"]
permalink: /org/issue/33/
comments_file: DIF-org-issue-33_comments
---

[_https://github.com/decentralized-identity/org/issues/33_](https://github.com/decentralized-identity/org/issues/33)

While the concepts are later clarified using the passport example, the initial definitions of [verification](https://github.com/w3c/identity-web-impact/blob/49d81e5e99d9c300f4277e3815a0a0a5e0d90058/index.bs#L85) and [authentication ](https://github.com/w3c/identity-web-impact/blob/49d81e5e99d9c300f4277e3815a0a0a5e0d90058/index.bs#L86) remain somewhat ambiguous. 

The example provided under the definition of verification also aligns with the provided definition of authentication. It would be more effective to illustrate verification with an example that does not simultaneously constitute authentication. For example, verifying a digital signature exemplifies verification alone: using a public key, one can verify that the signature is valid (in cryptographic terms, ensuring the signature was produced by the private key related to the public key used for verification). However, this process does not reveal the identity of the signer if the link between the public key and the individual (which constitutes authentication) is absent.

I find the NIST's definition of authentication as *identity verification* (in SP 800-63-3) convincing.

Furthermore, what do you mean with "formal" in `Authentication is a specific, formal verification type`?