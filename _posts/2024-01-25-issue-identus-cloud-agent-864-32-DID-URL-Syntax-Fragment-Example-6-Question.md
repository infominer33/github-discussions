---
title: "identus-cloud-agent/issue/864: 3.2 DID URL Syntax \"Fragment\" Example 6 Question"
date: 2024-01-25 09:23:55 +0000
author: SaulMoonves
categories: ["Hyperledger"]
tags: ["identus-cloud-agent"]
permalink: /identus-cloud-agent/issue/864/
comments_file: Hyperledger-identus-cloud-agent-issue-864_comments
---

[_https://github.com/hyperledger/identus-cloud-agent/issues/864_](https://github.com/hyperledger/identus-cloud-agent/issues/864)


[Example 6](https://www.w3.org/TR/did-core/#example-a-resource-external-to-a-did-document): A resource external to a DID Document
```
did:example:123?service=agent&relativeRef=/credentials#degree
```

So, this dereferences a service in the DID document with an ID fragment of `agent`. What then does `#degree` fragment refer to in this context?

Is it meant to be part of relativeRef? If so shouldn't it be percent-encoded?

And, just to be clear, I am reading the spec and `agent` is meant to be like a relative reference, if I had a service ID that wasn't relative to the DID, I could use the full URI in the parameter value (percent encoded I guess?)