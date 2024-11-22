---
title: "aries-endorser-service/issue/81: eddsa-jcs-2022 and nested documents"
date: 2024-04-30 18:23:13 +0000
author: silverpill
categories: ["DIF"]
tags: ["aries-endorser-service"]
permalink: /aries-endorser-service/issue/81/
comments_file: DIF-aries-endorser-service-issue-81_comments
---

[_https://github.com/hyperledger/aries-endorser-service/issues/81_](https://github.com/hyperledger/aries-endorser-service/issues/81)

Should any additional steps be performed when nested documents are being secured?

Example:

```json
{
  "@context": [
    "https://www.w3.org/ns/activitystreams",
    "https://w3id.org/security/data-integrity/v2"
  ],
  "type": "Create",
  "object": {
    "@context": [
      "https://www.w3.org/ns/activitystreams",
      "https://w3id.org/security/data-integrity/v2"
    ],
    "type": "Note",
    "content": "test",
    "proof": {
      "@context": [
        "https://www.w3.org/ns/activitystreams",
        "https://w3id.org/security/data-integrity/v2"
      ],
      "type": "DataIntegrityProof",
      "cryptosuite": "eddsa-jcs-2022"
    }
  },
  "proof": {
    "@context": [
      "https://www.w3.org/ns/activitystreams",
      "https://w3id.org/security/data-integrity/v2"
    ],
    "type": "DataIntegrityProof",
    "cryptosuite": "eddsa-jcs-2022"
  }
}
```

The document with type `Note` is secured first, then it is inserted into the document with type `Create` under the `object` property, then `Create` document is secured too. Here, I'm assuming that #79 will be merged. Some properties are omitted for brevity.

Is the resulting document valid?
 