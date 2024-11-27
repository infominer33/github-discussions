---
title: "Bugfix: vc.credentialSubject.id, vc.issuer, iss, and sub should be DID itself"
date: 2024-03-22 14:55:16 +0000
author: t-kanuma
excerpt: >
  Should this be an a tag? Isn't there a ReSpec way to reference this specification so that it appears at the bottom of the document as a reference
categories: hyperledger
tags: aries-acapy-docs
comments_file: aries-acapy-docs-pr-99_comments
permalink: /aries-acapy-docs/99/
url: https://github.com/hyperledger/aries-acapy-docs/pull/99
last_modified_at: 2024-11-21 15:58:30 +0000
---


**URL:** https://github.com/hyperledger/aries-acapy-docs/pull/99

[OID4VCI]
credentialSubject.id, iss, and sub should be DID, not DID URLs pointing to verification methods.