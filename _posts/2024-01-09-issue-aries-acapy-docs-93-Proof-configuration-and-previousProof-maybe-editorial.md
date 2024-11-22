---
title: "aries-acapy-docs/issue/93: Proof configuration and previousProof (maybe editorial)"
date: 2024-01-09 18:41:08 +0000
author: iherman
categories: ["Hyperledger"]
tags: ["aries-acapy-docs"]
permalink: /aries-acapy-docs/issue/93/
comments_file: Hyperledger-aries-acapy-docs-issue-93_comments
---

[_https://github.com/hyperledger/aries-acapy-docs/issues/93_](https://github.com/hyperledger/aries-acapy-docs/issues/93)

Just checking.

[§3.2.5 Proof Configuration](https://www.w3.org/TR/vc-di-eddsa/#proof-configuration-eddsa-rdfc-2022) does not mention the `previousProof` property, if applicable. I.e., when calculating the value of _canonicalProofConfig_, that value is not taken into consideration.

I do not know whether this is intentional or an omission. 

If it is intentional, it might be worth emphasizing. The formulation in [§3.2.2 Verify Proof](https://www.w3.org/TR/vc-di-eddsa/#verify-proof-eddsa-rdfc-2022), point (2) only mentions `proofValue` as the property to be removed, which gives the false impression that `previousProof` is fine. (I know that in §3.2.5 the properties to be used are listed explicitly, but then why bother with point (2) in §3.2.2 in the first place?)

(The ecdsa case is identical.)

