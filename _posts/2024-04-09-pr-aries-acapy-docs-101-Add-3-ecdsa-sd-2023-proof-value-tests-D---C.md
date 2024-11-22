---
title: "aries-acapy-docs/pr/101: Add 3 ecdsa-sd-2023 proof value tests (D -> C)"
date: 2024-04-09 20:10:16 +0000
author: aljones15
categories: ["Hyperledger"]
tags: ["aries-acapy-docs"]
permalink: /aries-acapy-docs/pr/101/
comments_file: Hyperledger-aries-acapy-docs-pr-101_comments
---

[_https://github.com/hyperledger/aries-acapy-docs/pull/101_](https://github.com/hyperledger/aries-acapy-docs/pull/101)

Adds 3 proofValue related tests:

1. "If the proofValue string does not start with u, indicating that it is a multibase-base64url-no-pad-encoded value, an error MUST be raised and SHOULD convey an error type of PROOF_VERIFICATION_ERROR"

```js
  "proof": {
    "type": "DataIntegrityProof",
    "created": "2024-11-17T15:51:32Z",
    "verificationMethod": "did:key:zDnaepBuvsQ8cpsWrVKw8fbpGpvPeNSjVPTWoq6cRqaYzBKVP#zDnaepBuvsQ8cpsWrVKw8fbpGpvPeNSjVPTWoq6cRqaYzBKVP",
    "cryptosuite": "ecdsa-sd-2023",
    "proofPurpose": "assertionMethod",
    "proofValue": "2V0BhVhANk3uoC2QPhe9knhEUtqpGS9cdbp1oRKf3SZ9v1iUO-UKS-hFqgacRYOrCSh8duVDK_zY5N5Hndkq8l7VRVAMNFgjgCQDR-DKGWfNv3Kq9TKO1wKXsgvmVlsjqhTWw4U8N-zL23yHWEAjupTpyzvis37wkzIwiXKuizfcF9VvpZfMx7uF2tVW3Al-BbTXQy_HO-EOM3WdH_sZO7K0CP_8fgGMk3UwsmrzWEDBizvJxii_nXROPhqvulJp1e27ZmixVmPUm9ZMT-zl-WAoocGzZnLfwdP_ujRfZVSs_CSJRnz87cqKtgRxG0HqWEBTp4qhxcXJbNVup9iCZAlHLt5oKEYNDEn2KWFMeUqBtwFAWjbVDOQQbPiiZ8XN6Ko8sD0MsSmQ28YkyQD9sir5WEA00uDbdz-gaeeQwPMm4gO-eLWSoIx9LRGLK8F5QEJGa4amwfn8eJ178DUCpr1BRZoGiJAkVR8AzE1Xk8vuXF-JWEAgknRMffrzujB2IW79_1O0SnQf9NyOzPpsws5dbhD8l5PsrzQI6HFaZrhSNayha0ppCw50UdtMo2zSRXWYoVMRWECaWckwEmY6BgddbWySxeYgUwHB3p72kxQ7Eg-9Idd5Z9fEcj8tFwCFDjZJJdXKhBSM71J8dAf9HVZo12Wm51_CWECmmVvtaKWgUlvRoPN6G6wfV25e4fPeo4d8l1ApSllxZ19Ls7-uCRl2jE28NbrCvzmPfg3mLbQBRhM3fabvdcbhoQBYIKzZT5KJrjiCO1Dhv0Ww6rqGS8K_yY56UpQc9j12-oHohAECBAU"
  }
```
2. The base proof assertion: "If the decodedProofValue does not start with the ECDSA-SD base proof header bytes 0xd9, 0x5d, and 0x00, an error MUST be raised and SHOULD convey an error type of PROOF_VERIFICATION_ERROR." Is tested by examing the base proof from the issuer. As base proofs are not designed to pass verification the statement from the spec might be incorrect.

3. "If the decodedProofValue does not start with the ECDSA-SD disclosure proof header bytes 0xd9, 0x5d, and 0x01, an error MUST be raised and SHOULD convey an error type of PROOF_VERIFICATION_ERROR." 

The invalid disclosure proof header bytes are `[0xA1, 0x44, 0x01]` and replace the original proof value header bytes. The actual proofValue is left as is and the invalid header bytes are encoded as a base64 url with the prefix `u`.

Additionally:

- DRYs up an assertion on base proof proofValues into a single assertion
- Changes several async function related to decoding bs58 and bs64 strings into non-async functions
- Changes relevant helpers and assertions into non-async functions if the function only depended on a bs decode function previously.