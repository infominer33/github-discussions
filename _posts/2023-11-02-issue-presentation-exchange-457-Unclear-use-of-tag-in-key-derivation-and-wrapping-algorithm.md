---
title: "presentation-exchange/issue/457: Unclear use of `tag` in key derivation and wrapping algorithm"
date: 2023-11-02 18:00:26 +0000
author: jakubkoci
categories: ["DIF"]
tags: ["presentation-exchange"]
permalink: /presentation-exchange/issue/457/
comments_file: DIF-presentation-exchange-issue-457_comments
---

[_https://github.com/decentralized-identity/presentation-exchange/issues/457_](https://github.com/decentralized-identity/presentation-exchange/issues/457)

I don't understand how to use a `tag` in key derivation/wrapping algorithm as described in sections:

- [5.1.9 ECDH-1PU key wrapping and common protected headers](https://identity.foundation/didcomm-messaging/spec/v2.1/#ecdh-1pu-key-wrapping-and-common-protected-headers)
- [5.1.10 ECDH-ES key wrapping and common protected headers](https://identity.foundation/didcomm-messaging/spec/v2.1/#ecdh-es-key-wrapping-and-common-protected-headers)

There is a mention

"As per this requirement, the JWE building must first encrypt the payload, then use the resulting `tag` as part of the key derivation process when wrapping the `cek`."

But I don't see any information on how that tag should be used in derivation of `kek`  or wrapping of `cek` with `kek`. Am I missing something? 