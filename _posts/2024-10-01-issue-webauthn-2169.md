---
title: "[[Get]] method doesn't exist in CredMan"
date: 2024-10-01 14:40:46 +0000
author: emlun
excerpt: >
  Fixed in PR #2180.
categories: w3c
tags: webauthn
comments_file: webauthn-issue-2169_comments
permalink: /webauthn/2169/
url: https://github.com/w3c/webauthn/issues/2169
last_modified_at: 2024-11-13 20:59:15 +0000
---


**URL:** https://github.com/w3c/webauthn/issues/2169

[§5.1.4. Use an Existing Credential to Make an Assertion - PublicKeyCredential’s \[\[Get\]\](options) Method](https://w3c.github.io/webauthn/#sctn-getAssertion) appears to reference a `[[Get]]` internal method on the [`Credential` interface](https://w3c.github.io/webappsec-credential-management/#the-credential-interface) from CredMan, but no such internal method exists (unlike [`[[Create]]`, which does exist](https://w3c.github.io/webappsec-credential-management/#algorithm-create-cred)). Rather, [`[[DiscoverFromExternalSource]]`](https://w3c.github.io/webappsec-credential-management/#algorithm-discover-creds) is the actual internal method we override.


## Proposed Change

- Delete the heading [§5.1.4.1. PublicKeyCredential’s [[DiscoverFromExternalSource]](origin, options, sameOriginWithAncestors) Method](https://w3c.github.io/webauthn/#sctn-discover-from-external-source) (without changing any of the text around it).
- Rename the heading [§5.1.4. Use an Existing Credential to Make an Assertion - PublicKeyCredential’s \[\[Get\]\](options) Method](https://w3c.github.io/webauthn/#sctn-getAssertion) to **5.1.4. Use an Existing Credential to Make an Assertion - PublicKeyCredential’s [[DiscoverFromExternalSource]](origin, options, sameOriginWithAncestors) Internal Method**.
- For consistency, change "Method" to "Internal Method" in the heading [§5.1.3. Create a New Credential - PublicKeyCredential’s [[Create]](origin, options, sameOriginWithAncestors) Method](https://w3c.github.io/webauthn/#sctn-createCredential).
- Similarly, change "Method" to "Internal Method" in the heading [§5.1.5. Store an Existing Credential - PublicKeyCredential’s [[Store]](credential, sameOriginWithAncestors) Method](https://w3c.github.io/webauthn/#sctn-storeCredential).