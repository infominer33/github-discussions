---
title: "webauthn/issue/2187: Remove authenticatorDisplayName from L3"
date: 2024-10-23 19:06:50 +0000
author: timcappalli
categories: ["W3C"]
tags: ["webauthn"]
permalink: /webauthn/issue/2187/
comments_file: W3C-webauthn-issue-2187_comments
excerpt: >
  I think that was more of an oversight as [the registration ceremony](https://w3c.github.io/webauthn/#reg-ceremony-store-credential-record) only mentions `credProps` as a possible _additional_ mechanism to set `authenticatorDisplayName`. The authentication section should have been written similarly. Regardless, I don't care enough about this; so if people want it removed, then so be it.
---
Discussed at TPAC as well as the 2024-10-23 call.

- Remove authenticatorDisplayName from credProps for Level 3
- Address the use case in Level 4 via https://github.com/w3c/webauthn/issues/2157


Relevant Issues and PRs:

- https://github.com/w3c/webauthn/pull/2163
- https://github.com/w3c/webauthn/pull/1880
- https://github.com/w3c/webauthn/issues/2156
- https://github.com/w3c/webauthn/pull/2005
