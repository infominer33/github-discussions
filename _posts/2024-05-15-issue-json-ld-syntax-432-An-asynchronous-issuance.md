---
title: "json-ld-syntax/issue/432: An asynchronous issuance"
date: 2024-05-15 10:12:27 +0000
author: filip26
categories: ["DIF"]
tags: ["json-ld-syntax"]
permalink: /json-ld-syntax/issue/432/
comments_file: DIF-json-ld-syntax-issue-432_comments
excerpt: >
  I'm going to guess/assume that this issue is primarily about workflows/exchanges. The reason for this is that if they aren't being used for delivery of a credential, then whether an additional process is required can be handled by the coordinator in any way whatsoever prior to making calls to the issuer API. So, we should focus this consideration on workflows/exchanges.
---
Hi,
it might be out of the scope of this spec, it's not a microservice, but asynchronous issuing is crucial in order to enable:

* an approval process - a process that might involve collecting additional information, checks, and even human involvement
* optimal infrastructure utilization - e.g. a queue of requests scheduled to be processed on an issuer's terms 

To keep this spec simple, perhaps, simply allowing to return `202 Accepted` code without specifying any further details, leaving the further interaction details on an implementer for now, could be enough to keep the issuance interface being used for advanced use-cases without a need to introduce a proprietary endpoint on issuer's side.