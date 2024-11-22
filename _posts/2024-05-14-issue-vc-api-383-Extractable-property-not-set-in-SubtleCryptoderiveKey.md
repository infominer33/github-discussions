---
title: "vc-api/issue/383: Extractable property not set in `SubtleCrypto.deriveKey`"
date: 2024-05-14 16:12:53 +0000
author: gmta
categories: ["DIF"]
tags: ["vc-api"]
permalink: /vc-api/issue/383/
comments_file: DIF-vc-api-issue-383_comments
---

[_https://github.com/w3c-ccg/vc-api/issues/383_](https://github.com/w3c-ccg/vc-api/issues/383)

Similar to `SubtleCrypto.importKey`, `.deriveKey` should set the `[[extractable]]` internal slot of the resulting key. None of the algorithms actually set this property on the key.