---
title: "Fix mac-os build"
date: 2024-11-04 13:41:24 +0000
author: WadeBarnes
excerpt: >
  Hi @ianhamilton87 Thanks for the question.
  
  Yes. We marked very few names as mandatory, the reasons for these ones in particular are:
  
  - In certain cases people don't have middle names
  - In certain cultures people don't use last names
  
  We have corrected `title` and `salutation` to be optional now, thanks for the input!
  
  The `nameFromDate` and `nameToDate` are also optional in the updated version.
categories: decentralized-identity
tags: credential-schemas
comments_file: credential-schemas-issue-21_comments
permalink: /credential-schemas/21/
url: https://github.com/decentralized-identity/credential-schemas/issues/21
last_modified_at: 2024-11-19 20:00:20 +0000
---


**URL:** https://github.com/decentralized-identity/credential-schemas/issues/21

See https://github.com/hyperledger/indy-cli-rs/pull/20