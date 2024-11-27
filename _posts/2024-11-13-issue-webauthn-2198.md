---
title: "WebAuthn Clients should NOT zero out AAGUIDs from security keys when attestation is none"
date: 2024-11-13 20:51:20 +0000
author: timcappalli
excerpt: >
  @zacknewman I think your conclusion is accurate - clients are expected to conform to the normative algorithm definitions.
categories: w3c
tags: webauthn
comments_file: webauthn-issue-2198_comments
permalink: /webauthn/2198/
url: https://github.com/w3c/webauthn/issues/2198
last_modified_at: 2024-11-14 13:04:56 +0000
---


**URL:** https://github.com/w3c/webauthn/issues/2198

There has been some confusion across multiple issues, so creating another one 🫠.

In #2058, spec text was added to only zero out AAGUIDs for none attestations when the authenticator was *not* a platform authenticator.

Proposal is to remove this change altogether, which would allow AAGUIDs from security keys to not be zeroed out.

Remove:
```
If authenticator is not a [platform authenticator](https://w3c.github.io/webauthn/#platform-authenticators) then replace the [aaguid](https://w3c.github.io/webauthn/#authdata-attestedcredentialdata-aaguid) in the [attested credential data](https://w3c.github.io/webauthn/#attested-credential-data) with 16 zero bytes.
```

This makes the behavior the same across all authenticator types from the client perspective.