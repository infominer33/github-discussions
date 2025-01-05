---
title: "New verification material property supporting JWK sets by reference"
date: 2021-12-18 01:31:10 +0000
author: codeglobally
excerpt: >
  The group discussed this on the 2024-08-29 telecon and came to the conclusion that the request is achievable through the standard extension mechanism and that there was no broad desire to implement the feature in the base specifications.
  
  This issue has been marked pending close and will be closed within seven days if there is no objection.
categories: w3c
tags: did-core
comments_file: did-core-issue-811_comments
permalink: /did-core/811/
url: https://github.com/w3c/did-core/issues/811
last_modified_at: 2025-01-04 18:11:33 +0000
---


**URL:** https://github.com/w3c/did-core/issues/811

Presently, *publicKeyJwk* and *publicKeyMultibase* are the only verification material types supported for verification methods in the specification. This is limiting for enterprise adoption where security best practice dictates frequent key rolling and hygiene, along with the broad adoption of external key management capabilities such as Azure Key Vault or the Amazon Key Management Service.

Proposal is to add a new verification material property **publicKeyJwks** of type URL, which is similar in behaviour to the **jwks_uri** property in OpenID Connect metadata.