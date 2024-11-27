---
title: "bbs-signature/issue/318: Able to create an in-memory sqlite database?"
date: 2024-03-19 09:13:15 +0000
author: jamshale
categories: ["DIF"]
tags: ["bbs-signature"]
permalink: /bbs-signature/issue/318/
comments_file: DIF-bbs-signature-issue-318_comments
excerpt: >
  PR #319 was raised to address this issue, closing.
---
From the python library is there a way to create an in-memory sqlite database?

I see this https://github.com/hyperledger/aries-askar/blob/main/askar-storage/src/backend/sqlite/provision.rs#L50 and will try and figure it out myself. Just posting this here is anyone knows off the to of their head.

***context:*** We're trying to rely on askar fully in aca-py and remove the existing in-memory wallet that was created for testing. Having the option to create an in-memory wallet that is askar based would really help speed up the tests and prevent file IO errors.
