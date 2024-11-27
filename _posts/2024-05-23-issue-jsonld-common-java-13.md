---
title: "A few errors in the Example 11"
date: 2024-05-23 20:15:47 +0000
author: timothee-haudebourg
excerpt: >
  Related to the above, the subject scope/subject domains are given to us in the DID-CORE specification:  
  Decentralized Identifiers (DIDs) v1.0 Specification
  Reference: https://www.w3.org/TR/did-core/  
  > Decentralized identifiers (DIDs) are a new type of identifier that enables verifiable, decentralized digital identity. A DID refers to any subject (e.g., a person, organization, thing, data model, abstract entity, etc.) as determined by the controller of the DID. In contrast to typical, federated identifiers, DIDs have been designed so that they may be decoupled from centralized registries, identity providers, and certificate authorities.  
  > DID subject
  > The entity identified by a DID and described by a DID document. Anything can be a DID subject: person, group, organization, physical thing, digital thing, logical thing, etc.  
categories: decentralized-identity
tags: jsonld-common-java
comments_file: jsonld-common-java-issue-13_comments
permalink: /jsonld-common-java/13/
url: https://github.com/decentralized-identity/jsonld-common-java/issues/13
last_modified_at: 2024-11-27 09:38:36 +0000
---


**URL:** https://github.com/decentralized-identity/jsonld-common-java/issues/13

I've spotted what I believe to be a few errors in the PDF-417 payload showed in [Example 11](https://w3c-ccg.github.io/vc-barcodes/#example-bytes-from-a-pdf417-including-an-encoded-utopia-driver-s-license-vcb).

1. There is a missing trailing space in the file type (should be `ANSI `), as mentioned in #12 
2. The `DL` subfile length seems wrong: it is set to `0267` where I find a value of `0234`.
3. The `ZZ` offset is wrong (probably because of 2.): it is set to `0308` (41 + 267) where I find a value of `0275` (41 + 275)
4. The `ZZ` subfile lenght seems wrong: `0162` instead of `0202`. This one can be easily decomposed as 202 = 2 (`ZZ`) + 3 + (`ZZA`) + 196 (base64-encoded CBOR-LD VC) + 1 (segment terminator)

Here is what I think is the correct payload:
```
@\n\x1e\rANSI 000000090002DL00410234ZZ02750202DLDAQF987654321\nDCSSMITH\nDDEN\nDACJOHN\nDDFN\nDADNONE\nDDGN\nDCAC\nDCBNONE\nDCDNONE\nDBD01012024\nDBB04191988\nDBA04192030\nDBC1\nDAU069 IN\nDAYBRO\nDAG123 MAIN ST\nDAIANYVILLE\nDAJUTO\nDAKF87P20000  \nDCFUTODOCDISCRIM\nDCGUTO\nDAW158\nDCK1234567890\nDDAN\rZZZZA2QZkpgGDGYAAGYABGYACGJ2CGHYYpBi4oxicGKYYzhiyGNAa5ZIggRi6ohicGKAYqER1ggAgGL4YqhjApRicGGwY1gQY4BjmGOJYQXq3wuVrSeLM5iGEziaBjhWosXMWRAG107uT_9bSteuPasCXFQKuPdSdF-xmUoFkA0yRJoW4ERvATNyewT263ZHMGOQYrA==\r
```

However it is possible I misunderstood something in AAMVA's PDF-417 data encoding.