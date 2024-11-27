---
title: "Able to create an in-memory sqlite database?"
date: 2024-03-19 09:13:15 +0000
author: jamshale
excerpt: >
  PR #319 was raised to address this issue, closing.
categories: decentralized-identity
tags: bbs-signature
comments_file: bbs-signature-issue-318_comments
permalink: /bbs-signature/318/
url: https://github.com/decentralized-identity/bbs-signature/issues/318
last_modified_at: 2024-11-17 19:11:39 +0000
---


**URL:** https://github.com/decentralized-identity/bbs-signature/issues/318

From the python library is there a way to create an in-memory sqlite database?

I see this https://github.com/hyperledger/aries-askar/blob/main/askar-storage/src/backend/sqlite/provision.rs#L50 and will try and figure it out myself. Just posting this here is anyone knows off the to of their head.

***context:*** We're trying to rely on askar fully in aca-py and remove the existing in-memory wallet that was created for testing. Having the option to create an in-memory wallet that is askar based would really help speed up the tests and prevent file IO errors.
