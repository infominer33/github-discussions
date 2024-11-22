---
title: "aries-endorser-service/issue/82: Unify Error Handling"
date: 2024-05-03 19:09:35 +0000
author: Wind4Greg
categories: ["DIF"]
tags: ["aries-endorser-service"]
permalink: /aries-endorser-service/issue/82/
comments_file: DIF-aries-endorser-service-issue-82_comments
---

[_https://github.com/hyperledger/aries-endorser-service/issues/82_](https://github.com/hyperledger/aries-endorser-service/issues/82)


Similar to issue https://github.com/w3c/vc-di-ecdsa/issues/63. To unify error handling language across this specification and other cryptosuite specifications I'd recommend:

1. Use appropriate error handling language as in DI specification, e.g.,  "an error MUST be raised and SHOULD convey an error type of ERROR_CODE_NAME." where ERROR_CODE_NAME is defined in the DI specification.
2. Use standardized error codes from DI Specification, and if needed add new codes to DI specification
3. Check for non-rigorous error handling language and if it needs to be updated (errors without codes that need codes)

Below I show codes used but not in the DI specification. I didn't find any error conditions without codes that should have them. Thoughts/Opinions?

## Error Codes Used but Not in DI Spec

Error codes: PROOF_TRANSFORMATION_ERROR, INVALID_PROOF_CONFIGURATION, INVALID_PROOF_DATETIME, MALFORMED_PROOF_ERROR,

* line 635: "If <var>options</var>.<var>type</var> is not set to the string `DataIntegrityProof` and <var>options</var>.<var>cryptosuite</var> is not set to the string `eddsa-rdfc-2022` then a `PROOF_TRANSFORMATION_ERROR` MUST be raised." In section *Transformation (eddsa-rdfc-2022)*.
* line 724: "If <var>options</var>.<var>type</var> is not set to `DataIntegrityProof` and <var>proofConfig</var>.<var>cryptosuite</var> is not set to `eddsa-rdfc-2022`, an `INVALID_PROOF_CONFIGURATION` error MUST be raised."
* line 730: "If the value is not a valid [[XMLSCHEMA11-2]] datetime, an `INVALID_PROOF_DATETIME` error MUST be raised."
* line 1005: "If <var>options</var>.<var>type</var> is not set to the string `DataIntegrityProof` and <var>options</var>.<var>cryptosuite</var> is not set to the string `eddsa-jcs-2022` then an error MUST be raised that SHOULD use the `MALFORMED_PROOF_ERROR` error code."
* line 1085: "If <var>options</var>.<var>type</var> is not set to `DataIntegrityProof` and <var>proofConfig</var>.<var>cryptosuite</var> is not set to `eddsa-jcs-2022`, an `INVALID_PROOF_CONFIGURATION` error MUST be raised."
* line 1090: "Set <var>proofConfig</var>.<var>created</var> to <var>options</var>.<var>created</var>. If the value is not a valid [[XMLSCHEMA11-2]] datetime, an `INVALID_PROOF_DATETIME` error MUST be raised."
* line 2017: "If <var>options</var>.<var>type</var> is not set to the string `Ed25519Signature2020`, then a `PROOF_TRANSFORMATION_ERROR` MUST be raised."
* line 2114: "If <var>options</var>.<var>type</var> is not set to `Ed25519Signature2020`, an `INVALID_PROOF_CONFIGURATION` error MUST be raised."
* line 2119: "If the value is not a valid [[XMLSCHEMA11-2]] datetime, an `INVALID_PROOF_DATETIME` error MUST be raised."
