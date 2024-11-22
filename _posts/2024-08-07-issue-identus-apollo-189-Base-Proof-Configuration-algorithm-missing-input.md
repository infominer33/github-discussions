---
title: "identus-apollo/issue/189: Base Proof Configuration algorithm missing input"
date: 2024-08-07 09:41:58 +0000
author: brianorwhatever
categories: ["Hyperledger"]
tags: ["identus-apollo"]
permalink: /identus-apollo/issue/189/
comments_file: Hyperledger-identus-apollo-issue-189_comments
---

[_https://github.com/hyperledger/identus-apollo/issues/189_](https://github.com/hyperledger/identus-apollo/issues/189)

In the base proof config algorithm the inputs don't list the unsecured document however it is asked to set the proof `@context` to match it.

See https://www.w3.org/TR/vc-di-bbs/#base-proof-configuration-bbs-2023