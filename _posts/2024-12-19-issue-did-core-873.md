---
title: "Define fragment processing rules for `application/did`"
date: 2024-12-19 16:48:46 +0000
author: msporny
excerpt: >
  > should a resolver return the associated DIDDoc (and hence, the fragment) when the fragment is not in the current version of the DIDDoc but is in a prior version of the DIDDoc?
  
  As discussed, in my opinion this isn't possible, a fragment can't identify something that's not in the DID document
  
  > The DID Controller could choose to keep all #frag values in the current DIDDoc
  
  Yes this would work. Also note the \"revoked\" property in the CID specification: https://w3c.github.io/cid/#dfn-revoked
  
  > A DID URL of the form `<did>?versionId=<version>#frag` would work
  
  Yes this would also work.
categories: w3c
tags: did-core
comments_file: did-core-issue-873_comments
permalink: /did-core/873/
url: https://github.com/w3c/did-core/issues/873
last_modified_at: 2024-12-29 07:22:23 +0000
---


**URL:** https://github.com/w3c/did-core/issues/873

The specification currently doesn't define fragment processing rules. We have to define those rules by either reusing the one from `application/cid` or defining new ones.