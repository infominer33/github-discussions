---
title: "Section 3.2 should refer to OID4"
date: 2024-07-03 13:27:43 +0000
author: Sakurann
excerpt: >
  > So the DID method should only describe the mechanism for the Create, Resolve, Update and Deactivate operations and nothing about the actual identity of the entity.  
  This statement is not completely true.  
  The entire purpose of a subject's service endpoints are to enable interaction with the underlying entity (addressable by its DID). In Web 7.0, DIDScript(tm) exploits this concept:
  - DIDScript(tm) Language 0.3 Interpreter for DIDs, DID Documents, DID Agent Clusters, and DID Objects (https://youtu.be/mf0aKLvJoCw)  
  In addition, DIDScript supports round-robin,  load-balanced DID Agent Clusters.
categories: hyperledger
tags: identus
comments_file: identus-issue-22_comments
permalink: /identus/22/
url: https://github.com/hyperledger/identus/issues/22
last_modified_at: 2024-12-29 09:39:24 +0000
---


**URL:** https://github.com/hyperledger/identus/issues/22

[Section 3.2](https://w3c-ccg.github.io/vp-request-spec/#oidc-credential-provider) should probably be updated to[ OpenID for Verifiable Credentials Issuance Draft](https://openid.net/specs/openid-4-verifiable-credential-issuance-1_0.html)