---
title: "credential-schemas/issue/21: Fix mac-os build"
date: 2024-11-04 13:41:24 +0000
author: WadeBarnes
categories: ["DIF"]
tags: ["credential-schemas"]
permalink: /credential-schemas/issue/21/
comments_file: DIF-credential-schemas-issue-21_comments
excerpt: >
  Hi @ianhamilton87 Thanks for the question.    Yes. We marked very few names as mandatory, the reasons for these ones in particular are:    - In certain cases people don't have middle names  - In certain cultures people don't use last names    We have corrected `title` and `salutation` to be optional now, thanks for the input!    The `nameFromDate` and `nameToDate` are also optional in the updated version.
---
See https://github.com/hyperledger/indy-cli-rs/pull/20