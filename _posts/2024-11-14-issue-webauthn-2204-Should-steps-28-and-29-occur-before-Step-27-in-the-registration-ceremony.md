---
title: "webauthn/issue/2204: Should steps 28 and 29 occur before Step 27 in the registration ceremony"
date: 2024-11-14 21:07:57 +0000
author: zacknewman
categories: ["W3C"]
tags: ["webauthn"]
permalink: /webauthn/issue/2204/
comments_file: W3C-webauthn-issue-2204_comments
---

[_https://github.com/w3c/webauthn/issues/2204_](https://github.com/w3c/webauthn/issues/2204)

Currently [step 27](https://w3c.github.io/webauthn/#reg-ceremony-store-credential-record) occurs before steps [28](https://w3c.github.io/webauthn/#reg-ceremony-verify-extension-outputs) and 29; however it seems weird to "create and store a new [credential record](https://w3c.github.io/webauthn/#credential-record) in the [user account](https://w3c.github.io/webauthn/#user-account)" _before_ successfully completing steps 28 and 29, right? This means one could save a credential even though the ceremony fails later.

A similar issue exists for the authentication ceremony where [step 23](https://w3c.github.io/webauthn/#authn-ceremony-update-credential-record) occurs before steps [24](https://w3c.github.io/webauthn/#authn-ceremony-verify-extension-outputs) and 25.

I think moving those steps last makes the most sense since this way any credential creation or update occurs iff the ceremony succeeds.