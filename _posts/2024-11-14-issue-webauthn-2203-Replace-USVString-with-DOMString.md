---
title: "webauthn/issue/2203: Replace `USVString` with `DOMString`"
date: 2024-11-14 15:08:41 +0000
author: zacknewman
categories: ["W3C"]
tags: ["webauthn"]
permalink: /webauthn/issue/2203/
comments_file: W3C-webauthn-issue-2203_comments
excerpt: >
  That argument applies to _many_ of the `DOMString`s in the spec (i.e., many areas where you see `DOMString` _have to be_ valid Unicode). Making these lone 3 `USVString`s into `DOMString`s is a much smaller change, makes the spec consistent, and does not make it more fragile since there are _more_ requirements than just valid Unicode. base64url decoding is defined on arbitrary bytes. If the input is not valid UTF-8, then the decoding will either fail or decode into something invalid which is possible even when the input is valid UTF-8.    The `prf` extension is also inconsistent with how the base64URL encoding of a Credential ID is typed elsewhere. For example, [`RegistrationResponseJSON.id`](https://w3c.github.io/webauthn/#dom-registrationresponsejson-id) is a `DOMString`.    It would be nice to pick one approach and stick with it:    * Pick the most strict type possible  * Define all strings as `DOMString` per the recommendation    The first approach will cause _a lot_ of `DOMString`s to be changed to `USVString`—including some of which _revert_ previous changes from `USVString` to `DOMString`—and I don't think it appreciably makes the spec that much more type safe since many things require additional properties anyway (i.e.,`USVString` won't make it infallible anyway).    The second approach is much easier, aligns with the recommendation, and aligns with previous PRs that changed `USVString`s to `DOMString`s.
---
It would appear that the same justification that was used for #2115 applies to the remaining areas where `USVString` is used:

> As recommended by the [Web IDL spec](https://webidl.spec.whatwg.org/#idl-USVString):
>
>> Specifications should only use `USVString` for APIs that perform text processing and need a string of scalar values to operate on. Most APIs that use strings should instead be using `DOMString`, which does not make any interpretations of the code units in the string. When in doubt, use `DOMString`.

Currently the only places where `USVString` is used are the following extensions:
* [`appid`](https://w3c.github.io/webauthn/#dom-authenticationextensionsclientinputs-appid)
* [`appidExclude`](https://w3c.github.io/webauthn/#dom-authenticationextensionsclientinputs-appidexclude)
* [`prf`](https://w3c.github.io/webauthn/#dictdef-authenticationextensionsprfinputs)

Should these all be changed to `DOMString`?