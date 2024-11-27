---
title: "The did is not a url for the did, but for a resolution structure which as yet has no name"
date: 2024-11-05 17:54:02 +0000
author: TomCJones
excerpt: >
  > OIDC itself only uses a 'flat' structure with singular values for everything
  
  Yes, which is quite unfortunate, as our experience is that information in credentials often do not have a flat structure (especially when you start combining credential data about the same individual).
  
  > This could lead to a mismatch between 'name' in OIDC
  
  Yes, and to put a finer point on how different information models fail to capture properties like \"name\" properly, see \"Falsehoods Programmers Believe About Names\":
  
  https://www.kalzumeus.com/2010/06/17/falsehoods-programmers-believe-about-names/
  
  No one said data modelling was easy. :P 
categories: decentralized-identity
tags: credential-schemas
comments_file: credential-schemas-issue-23_comments
permalink: /credential-schemas/23/
url: https://github.com/decentralized-identity/credential-schemas/issues/23
last_modified_at: 2024-11-20 21:02:12 +0000
---


**URL:** https://github.com/decentralized-identity/credential-schemas/issues/23

This not only makes the definition of did incorrect, but it points to a need for a name for the structure returned by a did resolution. Would also like to understand how redirects fit into this structure.