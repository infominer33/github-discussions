---
title: "dwn-user-guide/issue/3: Move it2 helper to test reporter"
date: 2024-07-10 17:51:17 +0000
author: aljones15
categories: ["DIF"]
tags: ["dwn-user-guide"]
permalink: /dwn-user-guide/issue/3/
comments_file: DIF-dwn-user-guide-issue-3_comments
---

[_https://github.com/decentralized-identity/dwn-user-guide/issues/3_](https://github.com/decentralized-identity/dwn-user-guide/issues/3)

This is great code:

https://github.com/digitalbazaar/vc-data-model-2-test-suite/blob/6884551bb388784032d40a222340995c55adc75e/tests/10-vcdm2.js#L57-L65

But it should be here: https://github.com/digitalbazaar/mocha-w3c-interop-reporter

It also needs a better name, such as `reportRow({title: '', test: async function() {}})`
