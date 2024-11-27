---
title: "Use Chai assertions over node assert"
date: 2024-07-03 23:27:23 +0000
author: aljones15
excerpt: >
  @kimdhamilton Apparently we need to start recording our conversations for authentication.   
  I expressed my disgust with your unilateral move on the call (unilateral with no prior consultation). Nothing from my perspective has changed.  
  You didn't change your post - so nothing appears to have changed from your side either.
categories: decentralized-identity
tags: credential-schemas
comments_file: credential-schemas-issue-4_comments
permalink: /credential-schemas/4/
url: https://github.com/decentralized-identity/credential-schemas/issues/4
last_modified_at: 2024-11-27 07:53:09 +0000
---


**URL:** https://github.com/decentralized-identity/credential-schemas/issues/4

Currently tests here use node's assertion library.

Tests usually use Chai's should and expect interface.
Please do try to use should:

https://www.chaijs.com/guide/styles/#should

the use of `assert` is clever, but if a chai assertion doesn't throw the mocha reporter might not see it.

So use chai to assert on the error from the server.