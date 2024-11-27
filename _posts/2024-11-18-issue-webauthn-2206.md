---
title: "Use of \"valid domain\" seems wrong"
date: 2024-11-18 13:55:36 +0000
author: annevk
excerpt: >
  @agl I think that's probably what you want to do here. You just need to check that it's of type domain (domain referencing the URL standard).
  
  @zacknewman the field in question here is well-defined and canonicalized as it's derived from an origin. (Modulo the usage of effective domain which is wrong, but I filed a separate issue for that.)
categories: w3c
tags: webauthn
comments_file: webauthn-issue-2206_comments
permalink: /webauthn/2206/
url: https://github.com/w3c/webauthn/issues/2206
last_modified_at: 2024-11-21 07:28:00 +0000
---


**URL:** https://github.com/w3c/webauthn/issues/2206

No user agent implements "valid domain". I suspect that instead you simply want to do a type check that the host of an origin is a domain.

Also, what kind of schemes can this origin have and do those need to be checked?