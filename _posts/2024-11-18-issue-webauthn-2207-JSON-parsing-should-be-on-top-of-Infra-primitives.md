---
title: "webauthn/issue/2207: JSON parsing should be on top of Infra primitives"
date: 2024-11-18 13:58:14 +0000
author: annevk
categories: ["W3C"]
tags: ["webauthn"]
permalink: /webauthn/issue/2207/
comments_file: W3C-webauthn-issue-2207_comments
---

[_https://github.com/w3c/webauthn/issues/2207_](https://github.com/w3c/webauthn/issues/2207)

I suspect that most can be replaced by https://infra.spec.whatwg.org/#parse-json-bytes-to-an-infra-value. This will also require some changes to the following steps as they now have an Infra value. This should also allow for the removal of the notes as now this is all well-defined instead of somewhat hand-wavy.