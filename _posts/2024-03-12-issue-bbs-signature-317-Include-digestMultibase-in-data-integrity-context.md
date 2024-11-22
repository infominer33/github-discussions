---
title: "bbs-signature/issue/317: Include `digestMultibase` in data integrity context"
date: 2024-03-12 15:56:31 +0000
author: PatStLouis
categories: ["DIF"]
tags: ["bbs-signature"]
permalink: /bbs-signature/issue/317/
comments_file: DIF-bbs-signature-issue-317_comments
---

[_https://github.com/decentralized-identity/bbs-signature/issues/317_](https://github.com/decentralized-identity/bbs-signature/issues/317)

The [resource integrity section](https://www.w3.org/TR/vc-data-integrity/#resource-integrity) refers to the `digestMultibase` property and its usage, however this property is not present in the data integrity context. It is, however, present in the vcdm 2.0 context, as described by the following text:
> JSON-LD context authors are expected to add digestMultibase to contexts that will be used in documents that refer to other resources and to include an associated cryptographic digest. For example, the [Verifiable Credentials Data Model v2.0](https://www.w3.org/TR/vc-data-model-2.0/) base context (https://www.w3.org/ns/credentials/v2) includes the digestMultibase property.

I want to suggest adding the `digestMultibase` to the data integrity context, keeping the same definition as is in the vcdm 2.0 context.
```
"digestMultibase": {
  "@id": "https://w3id.org/security#digestMultibase",
  "@type": "https://w3id.org/security#multibase"
}
```

Any particular reason it was not included?
