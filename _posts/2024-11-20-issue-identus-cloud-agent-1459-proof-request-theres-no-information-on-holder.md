---
title: "identus-cloud-agent/issue/1459:  proof request there's no information on holder "
date: 2024-11-20 10:34:25 +0000
author: mineme0110
categories: ["Hyperledger"]
tags: ["identus-cloud-agent"]
permalink: /identus-cloud-agent/issue/1459/
comments_file: Hyperledger-identus-cloud-agent-issue-1459_comments
excerpt: >
  Is this a priority
---
### Is this a regression?

NO

### Description

Right know when we have a proof request there's no information on holder side of what's being requested. 

Holder webhook data:

PresentationStatusAdapter(presentationId=94acbe0f-ed87-4477-9757-4b4ba8c3461d, thid=d080d2b5-0498-42aa-a829-22cf021ff3cf, role=PROVER, status=REQUEST_RECEIVED, metaRetries=5, proofs=[], data=[], connectionId=null)
GET /present-proof/presentations/$presentationId

{
    "presentationId": "94acbe0f-ed87-4477-9757-4b4ba8c3461d",
    "thid": "d080d2b5-0498-42aa-a829-22cf021ff3cf",
    "role": "Prover",
    "status": "RequestReceived",
    "proofs": [
        
    ],
    "data": [
        
    ],
    "requestData": [
        "{\n  \"options\" : {\n    \"domain\" : \"https://example-verifier.com\",\n    \"challenge\" : \"11c91493-01b3-4c4d-ac36-b336bab5bddf\"\n  },\n  \"presentation_definition\" : {\n    \"format\" : null,\n    \"name\" : null,\n    \"purpose\" : null,\n    \"id\" : \"345b056f-2889-458a-9f59-25d1ab249557\",\n    \"input_descriptors\" : [\n    ]\n  }\n}"
    ],
    "metaRetries": 5
}

The data is available in the RequestPresentation Attachment but we don't expose it on the endpoint 
This will be helpful fro cloud agnet  while testing test 


### Please provide the exception or error you saw

_No response_

### Please provide the environment you discovered this bug in

_No response_

### Anything else?

_No response_