---
title: "webauthn/issue/2203: Replace `USVString` with `DOMString`"
date: 2024-11-14 15:08:41 +0000
author: zacknewman
categories: ["W3C"]
tags: ["webauthn"]
permalink: /webauthn/issue/2203/
comments_file: W3C-webauthn-issue-2203_comments
---

[_https://github.com/w3c/webauthn/issues/2203_](https://github.com/w3c/webauthn/issues/2203)

It would appear that the same justification that was used for #2115 applies to the remaining areas where `USVString` is used:

> As recommended by the [Web IDL spec](https://webidl.spec.whatwg.org/#idl-USVString):
>
>> Specifications should only use `USVString` for APIs that perform text processing and need a string of scalar values to operate on. Most APIs that use strings should instead be using `DOMString`, which does not make any interpretations of the code units in the string. When in doubt, use `DOMString`.

Currently the only places where `USVString` is used are the following extensions:
* [`appid`](https://w3c.github.io/webauthn/#dom-authenticationextensionsclientinputs-appid)
* [`appidExclude`](https://w3c.github.io/webauthn/#dom-authenticationextensionsclientinputs-appidexclude)
* [`prf`](https://w3c.github.io/webauthn/#dictdef-authenticationextensionsprfinputs)

Should these all be changed to `DOMString`?