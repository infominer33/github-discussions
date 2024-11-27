---
title: "AttestationFormats may have duplicate entries"
date: 2024-11-14 02:19:50 +0000
author: Kieun
excerpt: >
  > One could make the argument that duplicates are most likely unintended, so it's better to reject them so the RP finds out about the issue. This would, however, not be backwards compatible with existing RP implementations that (intentionally or accidentally) rely on duplicates being silently ignored.
  
  I agree that throwing an error is a bad approach. But, adding some notes explicitly make the readers and developers to clearly understand how the underlying client and authenticator would work.
categories: w3c
tags: webauthn
comments_file: webauthn-issue-2202_comments
permalink: /webauthn/2202/
url: https://github.com/w3c/webauthn/issues/2202
last_modified_at: 2024-11-21 03:56:06 +0000
---


**URL:** https://github.com/w3c/webauthn/issues/2202

## Proposed Change

In the spec, we introduce `attestationFormats` for RPs to indicate the attestation statement format preference for create options.
The definition in the spec is as follows.

> attestationFormats, of type sequence<[DOMString](https://webidl.spec.whatwg.org/#idl-DOMString)>, defaulting to []
The [Relying Party](https://w3c.github.io/webauthn/#relying-party) MAY use this OPTIONAL member to specify a preference regarding the [attestation](https://w3c.github.io/webauthn/#attestation) statement format used by the [authenticator](https://w3c.github.io/webauthn/#authenticator). Values SHOULD be taken from the IANA "WebAuthn Attestation Statement Format Identifiers" registry [[IANA-WebAuthn-Registries]](https://w3c.github.io/webauthn/#biblio-iana-webauthn-registries) established by [[RFC8809]](https://w3c.github.io/webauthn/#biblio-rfc8809). Values are ordered from most preferable to least preferable. This parameter is advisory and the [authenticator](https://w3c.github.io/webauthn/#authenticator) MAY use an attestation statement not enumerated in this parameter.

Since the value itself is the list of ordered preferences, it implies that the element of the fields would be `unique`.
The [sequence<'T'>](https://webidl.spec.whatwg.org/#idl-sequence) does not have any such constraints for uniqueness. 

Thus, duplicated entries in the `attestationFormats` may be valid input as per the current spec. We may add some constraints around the field itself or we could describe the way for authenticator and client to handle such duplicated entries without throwing errors.

This issue is related to the #2145 and maybe we could resolve this issue with similar manner.