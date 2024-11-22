---
title: "credential-schemas/issue/4: Use Chai assertions over node assert"
date: 2024-07-03 23:27:23 +0000
author: aljones15
categories: ["DIF"]
tags: ["credential-schemas"]
permalink: /credential-schemas/issue/4/
comments_file: DIF-credential-schemas-issue-4_comments
---

[_https://github.com/decentralized-identity/credential-schemas/issues/4_](https://github.com/decentralized-identity/credential-schemas/issues/4)

Currently tests here use node's assertion library.

Tests usually use Chai's should and expect interface.
Please do try to use should:

https://www.chaijs.com/guide/styles/#should

the use of `assert` is clever, but if a chai assertion doesn't throw the mocha reporter might not see it.

So use chai to assert on the error from the server.