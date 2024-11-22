---
title: "linked-vp/issue/50: Test VC doesn't include proper context"
date: 2024-02-29 08:53:59 +0000
author: brianorwhatever
categories: ["DIF"]
tags: ["linked-vp"]
permalink: /linked-vp/issue/50/
comments_file: DIF-linked-vp-issue-50_comments
---

[_https://github.com/decentralized-identity/linked-vp/issues/50_](https://github.com/decentralized-identity/linked-vp/issues/50)

The only context included in the [test vc](https://github.com/w3c/vc-di-ed25519signature2020-test-suite/blob/8a18d629d472bb35f4d0f9f5b9709f206f2cb8f5/tests/vc-generator/testVc.js#L2) is the credentials context. This context unfortunately doesn't have properties for this suite. I think the `'https://w3id.org/security/suites/ed25519-2020/v1'` context is required