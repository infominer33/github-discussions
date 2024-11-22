---
title: "webauthn/issue/2202: AttestationFormats may have duplicate entries"
date: 2024-11-14 02:19:50 +0000
author: Kieun
categories: ["W3C"]
tags: ["webauthn"]
permalink: /webauthn/issue/2202/
comments_file: W3C-webauthn-issue-2202_comments
---

[_https://github.com/w3c/webauthn/issues/2202_](https://github.com/w3c/webauthn/issues/2202)

## Proposed Change

In the spec, we introduce `attestationFormats` for RPs to indicate the attestation statement format preference for create options.
The definition in the spec is as follows.

> attestationFormats, of type sequence<[DOMString](https://webidl.spec.whatwg.org/#idl-DOMString)>, defaulting to []
The [Relying Party](https://w3c.github.io/webauthn/#relying-party) MAY use this OPTIONAL member to specify a preference regarding the [attestation](https://w3c.github.io/webauthn/#attestation) statement format used by the [authenticator](https://w3c.github.io/webauthn/#authenticator). Values SHOULD be taken from the IANA "WebAuthn Attestation Statement Format Identifiers" registry [[IANA-WebAuthn-Registries]](https://w3c.github.io/webauthn/#biblio-iana-webauthn-registries) established by [[RFC8809]](https://w3c.github.io/webauthn/#biblio-rfc8809). Values are ordered from most preferable to least preferable. This parameter is advisory and the [authenticator](https://w3c.github.io/webauthn/#authenticator) MAY use an attestation statement not enumerated in this parameter.

Since the value itself is the list of ordered preferences, it implies that the element of the fields would be `unique`.
The [sequence<'T'>](https://webidl.spec.whatwg.org/#idl-sequence) does not have any such constraints for uniqueness. 

Thus, duplicated entries in the `attestationFormats` may be valid input as per the current spec. We may add some constraints around the field itself or we could describe the way for authenticator and client to handle such duplicated entries without throwing errors.

This issue is related to the #2145 and maybe we could resolve this issue with similar manner.