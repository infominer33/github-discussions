---
title: "webauthn/issue/2207: JSON parsing should be on top of Infra primitives"
date: 2024-11-18 13:58:14 +0000
author: annevk
categories: ["W3C"]
tags: ["webauthn"]
permalink: /webauthn/issue/2207/
comments_file: W3C-webauthn-issue-2207_comments
excerpt: >
  For instance in https://w3c.github.io/webauthn/#sctn-registering-a-new-credential steps 5/6 would be combined by instead calling into Infra. Then step 7 and such can no longer use the `C.type` syntax to refer to members. Instead you'll have to use    > _C_[\"type\"]    which will make it more consistent with other specifications.
---
I suspect that most can be replaced by https://infra.spec.whatwg.org/#parse-json-bytes-to-an-infra-value. This will also require some changes to the following steps as they now have an Infra value. This should also allow for the removal of the notes as now this is all well-defined instead of somewhat hand-wavy.