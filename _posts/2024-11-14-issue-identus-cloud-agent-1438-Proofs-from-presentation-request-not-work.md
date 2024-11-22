---
title: "identus-cloud-agent/issue/1438: Proofs from presentation request not work"
date: 2024-11-14 02:19:10 +0000
author: kieutuan218
categories: ["Hyperledger"]
tags: ["identus-cloud-agent"]
permalink: /identus-cloud-agent/issue/1438/
comments_file: Hyperledger-identus-cloud-agent-issue-1438_comments
---

[_https://github.com/hyperledger/identus-cloud-agent/issues/1438_](https://github.com/hyperledger/identus-cloud-agent/issues/1438)

### Is this a regression?

Yes

### Description

Hello, regarding the request body for the presentation request:

I don't understand the fields proofs.schemaId and proofs.trustIssuers. Although I sent a credential that does not match the schemaId and issuerDid, the status in the cloud agent still returns "PresentationVerified."
Is that a bug?

```
{
    "connectionId": "bee34719-def5-4420-8d4f-35318e72e916",
    "proofs": [
        {
            "schemaId": "ddec9bf9-b187-3862-897d-dd11d1c1eb53",
            "trustIssuers": [
                "did:prism:invalidddddđ"
            ]
        }
    ],
    "options": {
        "challenge": "{{$randomUUID}}",
        "domain": "https://prism-verifier.com"
    },
    "credentialFormat": "JWT"
}
```

### Please provide the exception or error you saw

_No response_

### Please provide the environment you discovered this bug in

```Markdown
1.39.1-104-1c7c38e
```


### Anything else?

_No response_