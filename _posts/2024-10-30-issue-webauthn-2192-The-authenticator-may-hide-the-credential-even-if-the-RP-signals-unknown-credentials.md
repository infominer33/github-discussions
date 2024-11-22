---
title: "webauthn/issue/2192: The authenticator may hide the credential even if the RP signals unknown credentials"
date: 2024-10-30 09:03:05 +0000
author: Kieun
categories: ["W3C"]
tags: ["webauthn"]
permalink: /webauthn/issue/2192/
comments_file: W3C-webauthn-issue-2192_comments
---

[_https://github.com/w3c/webauthn/issues/2192_](https://github.com/w3c/webauthn/issues/2192)

## Proposed Change

In the spec, there are some description and recommendation how the authenticator handles signal APIs.
Currently, in many parts, there are description like this.

> [WebAuthn Relying Parties](https://w3c.github.io/webauthn/#webauthn-relying-party) may use these signal methods to inform [authenticators](https://w3c.github.io/webauthn/#authenticator) of the state of [public key credentials](https://w3c.github.io/webauthn/#public-key-credential), so that incorrect or revoked credentials may be `updated, removed, or hidden`.

The authenticator may decide not to remove the credential at the time of receiving the signal and it may remove it after certain amount of time passes. It implies that the credential would not delete the credential and for some reasons the hidden credential would be changed to active credential.

In the case of the user directly goes through the authenticator dedicated UI and then delete the credential, it would not be reported to the RP and which causes credential mismatch. So, for this case, the authenticator would hide the credential if the user deletes the credential through menu and it would be restored depending on some cases, and it would still work without any issue.
For this scenario, the hidden feature might be a good choice as an authenticator to prevent the credential is accidentally removed so that the user avoid user lock out case.

However, for the signal APIs, RP indicates that the acceptable credentials with an intention, so It would be better for authenticators to delete or update credentials if it is required to meet the original requirement (synchronization between authenticators and RP).

