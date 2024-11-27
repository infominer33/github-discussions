---
title: "bbs-signature/issue/315: SDJWT SDK to SDK Verification"
date: 2024-02-16 23:54:22 +0000
author: elribonazo
categories: ["DIF"]
tags: ["bbs-signature"]
permalink: /bbs-signature/issue/315/
comments_file: DIF-bbs-signature-issue-315_comments
excerpt: >
  Ok. There is also https://github.com/w3c/vc-data-integrity/issues/315#issuecomment-2424992041, but I trust you will do this at some point in the near future.    I let you decide whether you want to close the issue now or when that overall editorial pass is done.
---
### Proposed feature

Our aim is to bring verification capabilities across the different SDK platforms. We will do so by allowing Edge Wallets to initiate a ProofRequest to a known Identifier (DID), also this same Edge wallet need to be capable of Generating the Proof and send it back. This would basically allow any Edge wallet to initiate and complete verification requests by itself with Credential Type SD JWT. As this is a Selective Disclosure JWT, during the verification process the Verifier will receive both the shared disclosures and the SD JWT Credential.

User Cases
High level description [SD-JWT-Based Verifiable Credentials: An Introduction (criipto.com)](https://www.criipto.com/blog/sd-jwt-based-verifiable-credentials)

Current Draft Spec https://datatracker.ietf.org/doc/draft-ietf-oauth-selective-disclosure-jwt/

EBSI Spec https://hub.ebsi.eu/vc-framework/did/selective-disclosure-sd-jwt

Age Verification: For services that require age verification, such as venues where entrants need to be over 18. Entrants can share their driving licence as verifiable presentation and security can receive on a mobile device and automatically confirm that they are over the age of 18 without actually disclosing their age.

Voting Systems: In digital voting systems, edge wallets can store digital identities, allowing citizens to vote securely and anonymously, ensuring the integrity of the electoral process.



### Feature description

Using Presentation exchange protocol we add the ability for any SDK Verifier to now request SDJWT Presentation with all the disclosure capabilities bundled in. 

The verification will only pass if the claims we asked have been provided by the user, and disclosed correctly

### Anything else?

_No response_