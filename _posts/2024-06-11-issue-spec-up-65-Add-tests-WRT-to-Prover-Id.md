---
title: "spec-up/issue/65: Add tests WRT to Prover Id"
date: 2024-06-11 16:45:29 +0000
author: aljones15
categories: ["DIF"]
tags: ["spec-up"]
permalink: /spec-up/issue/65/
comments_file: DIF-spec-up-issue-65_comments
---

[_https://github.com/decentralized-identity/spec-up/issues/65_](https://github.com/decentralized-identity/spec-up/issues/65)

# BBS
4 missing statements...
"If featureOption is set to 'anonymous_holder_binding' or 'pseudonym_hidden_pid', the commitment_with_proof input MUST be supplied."
"If featureOption is set to 'anonymous_holder_binding' or 'pseudonym_hidden_pid', the commitment_with_proof input MUST be supplied; if not supplied, an error MUST be raised and SHOULD convey an error type of PROOF_GENERATION_ERROR"
"If featureOption equals 'anonymous_holder_binding', the REQUIRED additional inputs are holderSecret and proverBlind"
"If featureOption equals 'pseudonym_issuer_pid', the REQUIRED additional input is the verifier_id which is communicated to the holder by the verifier"
"If featureOption equals 'pseudonym_hidden_pid', the REQUIRED additional inputs are the pid, proverBlind (both known to holder), and verifier_id which is communicated to the holder by the verifier"
 - make an issue
