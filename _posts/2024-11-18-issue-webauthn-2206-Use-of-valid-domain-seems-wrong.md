---
title: "webauthn/issue/2206: Use of \"valid domain\" seems wrong"
date: 2024-11-18 13:55:36 +0000
author: annevk
categories: ["W3C"]
tags: ["webauthn"]
permalink: /webauthn/issue/2206/
comments_file: W3C-webauthn-issue-2206_comments
---

[_https://github.com/w3c/webauthn/issues/2206_](https://github.com/w3c/webauthn/issues/2206)

No user agent implements "valid domain". I suspect that instead you simply want to do a type check that the host of an origin is a domain.

Also, what kind of schemes can this origin have and do those need to be checked?