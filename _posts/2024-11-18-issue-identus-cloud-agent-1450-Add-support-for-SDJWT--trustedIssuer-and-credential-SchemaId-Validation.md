---
title: "identus-cloud-agent/issue/1450: Add support for SDJWT  trustedIssuer and credential SchemaId Validation "
date: 2024-11-18 13:13:03 +0000
author: mineme0110
categories: ["Hyperledger"]
tags: ["identus-cloud-agent"]
permalink: /identus-cloud-agent/issue/1450/
comments_file: Hyperledger-identus-cloud-agent-issue-1450_comments
excerpt: >
  Related with https://github.com/hyperledger/identus-cloud-agent/issues/1438
---
### Is this a regression?

No

### Description

SDJWT is similar flow as JWT so need to support  similar to JWT 
{
 "connectionId": "{{VERIFIER_CONNECTION_ID}}",
 "proofs": [
            {
                "schemaId": "{{baseUrl}}/schema-registry/schemas/{{SCHEMA_ID}}",
                "trustIssuers": [
                    "did:prism:invalidddddđ"
                ]
            }
],
 "options": {
    "challenge": "11c91493-01b3-4c4d-ac36-b336bab5bddf",
    "domain": "https://prism-verifier.com"
  },
  "credentialFormat": "SDJWT",
  "claims": {
        "emailAddress": {},
        "givenName": {},
        "country" :{} 
    }
} 

### Please provide the exception or error you saw

_No response_

### Please provide the environment you discovered this bug in

_No response_

### Anything else?

_No response_