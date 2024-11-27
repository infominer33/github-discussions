---
title: "\"Verify\" is undefined"
date: 2024-11-18 15:50:14 +0000
author: annevk
excerpt: >
  If you want to record an error or return from the algorithm with some kind of error you need to actually state that.
categories: w3c
tags: webauthn
comments_file: webauthn-issue-2208_comments
permalink: /webauthn/2208/
url: https://github.com/w3c/webauthn/issues/2208
last_modified_at: 2024-11-21 07:28:47 +0000
---


**URL:** https://github.com/w3c/webauthn/issues/2208

For example, https://w3c.github.io/webauthn/#sctn-registering-a-new-credential has a step that reads

> Verify that the value of C.[type](https://w3c.github.io/webauthn/#dom-collectedclientdata-type) is webauthn.create.

but it's not at all clear what this means or what should happen when it cannot be true. If it's always meant to be true unless something outside of the scope of the specification has happened, it would be more appropriate to use Infra's [Assert](https://infra.spec.whatwg.org/#assert) primitive.

If it can actually have other values, you'll need to define how to handle those.