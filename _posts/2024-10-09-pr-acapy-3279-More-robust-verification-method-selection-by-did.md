---
title: "acapy/pr/3279: More robust verification method selection by did"
date: 2024-10-09 20:02:31 +0000
author: dbluhm
categories: ["OWF"]
tags: ["acapy"]
permalink: /acapy/pr/3279/
comments_file: OWF-acapy-pr-3279_comments
---

[_https://github.com/openwallet-foundation/acapy/pull/3279_](https://github.com/openwallet-foundation/acapy/pull/3279)

This PR is intended to supersede #3138 by adding a default verification method selection strategy for all DID methods.

This strategy relies on proof type and proof purpose to select the most appropriate verification method. For example, if proof type is `Ed25519Signature2020` and purpose is `assertionMethod`, the changes in this PR will select the first matching method in the `assertionMethod` relationship that can produce a `Ed25519Signature2020`.

This places more expectations on the DID -- specifically that it is well formatted (which many aren't). By well formatted I mean that verification methods used for issuance are properly referenced in `assertionMethod`, methods used to authenticate the DID owner are in `authentication`, etc. In practice, this may cause challenges but it is possible for users who depend on a DID method/document that isn't well formatted to create their own strategy and plug it in. So I'm comfortable making the assertion that we can expect the DIDs we're working with to be well formatted.

This PR does adjust the interface for the VerificationKeyStrategy to better account for this. This might be painful to some plugin users who've added DID Methods by plugin and added a strategy to match. However, my hope is that those same users won't need to plug in their own strategy anymore with these changes since they should be robust enough to cover most use cases.

Shout out to @aritroCoder for his original work on #3138!