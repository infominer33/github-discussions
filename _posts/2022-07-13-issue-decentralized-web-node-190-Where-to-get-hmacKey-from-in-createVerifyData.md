---
title: "decentralized-web-node/issue/190: Where to get `hmacKey` from in `createVerifyData`"
date: 2022-07-13 20:46:02 +0000
author: brianorwhatever
categories: ["DIF"]
tags: ["decentralized-web-node"]
permalink: /decentralized-web-node/issue/190/
comments_file: DIF-decentralized-web-node-issue-190_comments
---

[_https://github.com/decentralized-identity/decentralized-web-node/issues/190_](https://github.com/decentralized-identity/decentralized-web-node/issues/190)

I am unable to complete step 3 of [createVerifyData](https://www.w3.org/TR/vc-di-bbs/#createverifydata) as I need the `hmacKey` however the previous step is calling `parseDerivedProofValue` which doesn't return an `hmacKey`. Am I missing something?