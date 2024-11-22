---
title: "bbs-signature/issue/315: Value of a verification method property?"
date: 2024-02-16 23:54:22 +0000
author: iherman
categories: ["DIF"]
tags: ["bbs-signature"]
permalink: /bbs-signature/issue/315/
comments_file: DIF-bbs-signature-issue-315_comments
---

[_https://github.com/decentralized-identity/bbs-signature/issues/315_](https://github.com/decentralized-identity/bbs-signature/issues/315)

In https://www.w3.org/TR/vc-data-integrity/#proofs the definition of `verficationMethod` says:

> **verificationMethod**
> A verification method is the means and information needed to verify the proof. If included, the value MUST be a [string](https://infra.spec.whatwg.org/#string) that maps to a [[URL](https://www.w3.org/TR/vc-data-integrity/#bib-url)].

This means that the following is not acceptable:

```json

 "proof": {
    "type": "DataIntegrityProof",
    "cryptosuite": "eddsa-jcs-2022",
    "verificationMethod": {
        "id": "https://controller.example/123456789abcdefghi#keys-1",
       "type": "Multikey", 
       "controller": "https://controller.example/123456789abcdefghi",
       "publicKeyMultibase": "z6MkmM42vxfqZQsv4ehtTjFFxQ4sQKS2w6WR7emozFAn5cxu"
   }
}
```

This is in contradiction with the definition of the same property for controller documents in https://www.w3.org/TR/controller-document/#verification-methods:

> If present, the value MUST be a [set](https://infra.spec.whatwg.org/#ordered-set) of [verification methods](https://www.w3.org/TR/controller-document/#dfn-verification-method), where each [verification method](https://www.w3.org/TR/controller-document/#dfn-verification-method) is expressed using a [map](https://infra.spec.whatwg.org/#ordered-map).

Which, interestingly, though would make the example valid if used on a controller document, would make this version invalid:

```json
"verificationMethod": "https://controller.example/123456789abcdefghi#keys-1"
```

which is the _only_ acceptable usage of the property for a proof.

Is this difference intentional? If so, why? Or are these both specification bugs? 

Personally, I tend to believe these are both bugs.
