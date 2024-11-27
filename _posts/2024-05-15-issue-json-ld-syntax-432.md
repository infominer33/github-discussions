---
title: "An asynchronous issuance"
date: 2024-05-15 10:12:27 +0000
author: filip26
excerpt: >
  I'm going to guess/assume that this issue is primarily about workflows/exchanges. The reason for this is that if they aren't being used for delivery of a credential, then whether an additional process is required can be handled by the coordinator in any way whatsoever prior to making calls to the issuer API. So, we should focus this consideration on workflows/exchanges.
  
  Now, for workflows/exchanges, the current design has some primitives in it already that are thought to cover this sort of situation and others like it. In particular, a VC API exchange does not require any VCs to be returned (issued) when it terminates *and* it can return a `redirectUrl` to continue the interaction. I can't link directly to this, but see these sections for `redirectUrl`:
  
  https://w3c-ccg.github.io/vc-api/#participate-in-an-exchange
  https://w3c-ccg.github.io/vc-api/#workflows-and-exchanges
  
   Therefore, the thought is that, for a process that requires additional interaction / approval prior to issuance the exchange would return a `redirectUrl` to send a user back to a coordinator website where it can tell the user that their request has been accepted and that they will be notified (by some coordinator+user-determined means) when they can return to be issued any VC(s). In theory, these primitives should enable a number of more complex / interesting flows to be built without having to specialize further.
categories: w3c
tags: json-ld-syntax
comments_file: json-ld-syntax-issue-432_comments
permalink: /json-ld-syntax/432/
url: https://github.com/w3c/json-ld-syntax/issues/432
last_modified_at: 2024-11-22 15:14:03 +0000
---


**URL:** https://github.com/w3c/json-ld-syntax/issues/432

Hi,
it might be out of the scope of this spec, it's not a microservice, but asynchronous issuing is crucial in order to enable:

* an approval process - a process that might involve collecting additional information, checks, and even human involvement
* optimal infrastructure utilization - e.g. a queue of requests scheduled to be processed on an issuer's terms 

To keep this spec simple, perhaps, simply allowing to return `202 Accepted` code without specifying any further details, leaving the further interaction details on an implementer for now, could be enough to keep the issuance interface being used for advanced use-cases without a need to introduce a proprietary endpoint on issuer's side.