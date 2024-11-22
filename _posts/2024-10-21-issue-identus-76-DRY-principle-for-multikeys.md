---
title: "identus/issue/76: DRY principle for multikeys?"
date: 2024-10-21 14:31:35 +0000
author: iherman
categories: ["DIF"]
tags: ["identus"]
permalink: /identus/issue/76/
comments_file: DIF-identus-issue-76_comments
---

[_https://github.com/hyperledger/identus/issues/76_](https://github.com/hyperledger/identus/issues/76)

This issue is also valid for the EdDSA and BBS specifications.

The [§2.1.1 Multikey](https://www.w3.org/TR/vc-di-ecdsa/#multikey) section gives a (normative!) definition for Multikeys for the various versions of ECDSA. However, _section [§2.2.2 Mulltikey](https://www.w3.org/TR/controller-document/#multikey) of the controller document_ also defines (normatively!) not only the concept of Multikeys, but also its specific definitions for ECDSA/EdDSA/BBS.

I think this is wrong, it violates the DRY principles and, worse, it may lead to discrepancies. (To be clear, I did not see any discrepancies today.) In the current setting of the various specifications, I believe the right place is the CD specification. 

(Note that the DID spec possibly adopting Multikeys as one of the standard key representation. The Multikey definition is relevant for DID, the cryptosuites are not...) 

In my view, the definition should be removed from the ECDSA (and EdDSA and BBS) specification. 