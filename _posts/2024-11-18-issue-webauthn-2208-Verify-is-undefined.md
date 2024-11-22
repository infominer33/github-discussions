---
title: "webauthn/issue/2208: \"Verify\" is undefined"
date: 2024-11-18 15:50:14 +0000
author: annevk
categories: ["W3C"]
tags: ["webauthn"]
permalink: /webauthn/issue/2208/
comments_file: W3C-webauthn-issue-2208_comments
---

[_https://github.com/w3c/webauthn/issues/2208_](https://github.com/w3c/webauthn/issues/2208)

For example, https://w3c.github.io/webauthn/#sctn-registering-a-new-credential has a step that reads

> Verify that the value of C.[type](https://w3c.github.io/webauthn/#dom-collectedclientdata-type) is webauthn.create.

but it's not at all clear what this means or what should happen when it cannot be true. If it's always meant to be true unless something outside of the scope of the specification has happened, it would be more appropriate to use Infra's [Assert](https://infra.spec.whatwg.org/#assert) primitive.

If it can actually have other values, you'll need to define how to handle those.