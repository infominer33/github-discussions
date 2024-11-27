---
title: "Make `AuthenticatorAttestationResponseJSON.publicKeyAlgorithm` optional"
date: 2024-07-27 01:46:22 +0000
author: zacknewman
excerpt: >
  As noted in https://github.com/w3c/webauthn/pull/2107#issuecomment-2254153595 we can't make `AuthenticatorAttestationResponse.publicKeyAlgorithm` optional because that would be a backwards incompatibility pitfall. Since `AuthenticatorAttestationResponseJSON.publicKeyAlgorithm` is meant to reflect the non-JSON field, and `AuthenticatorAttestationResponseJSON` is constructed by the client which clearly already knows the `publicKeyAlgorithm` value since it's required in the non-JSON, there's not much reason for it not to be required in the JSON dictionary too. Keeping it required in both dictionaries is more consistent. Therefore we decided on the 2024-10-30 WG call to close this (it just took me a few weeks to get around to doing it...).
categories: w3c
tags: webauthn
comments_file: webauthn-issue-2106_comments
permalink: /webauthn/2106/
url: https://github.com/w3c/webauthn/issues/2106
last_modified_at: 2024-11-27 10:36:05 +0000
---


**URL:** https://github.com/w3c/webauthn/issues/2106

The motivation behind both [`AuthenticatorAttestationResponseJSON.publicKey`](https://w3c.github.io/webauthn/#dom-authenticatorattestationresponsejson-publickey) and [`AuthenticatorAttestationResponseJSON.publicKeyAlgorithm`](https://w3c.github.io/webauthn/#dom-authenticatorattestationresponsejson-publickeyalgorithm) is the same: [easy access to credential data](https://w3c.github.io/webauthn/#sctn-public-key-easy). For good reason though,  `AuthenticatorAttestationResponseJSON.publicKey` is not required since technically such data exists in the required [`AuthenticatorAttestationResponseJSON.attestationObject`](https://w3c.github.io/webauthn/#dom-authenticatorattestationresponsejson-attestationobject). I believe the same should be true for `AuthenticatorAttestationResponseJSON.publicKeyAlgorithm` since it doesn't really serve purpose without `AuthenticatorAttestationResponseJSON.publicKey` also existing.