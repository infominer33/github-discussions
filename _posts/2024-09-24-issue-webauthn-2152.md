---
title: "Add `challengeUrl`"
date: 2024-09-24 22:26:51 +0000
author: nsatragno
excerpt: >
  @zacknewman I've changed it to POST, along with a couple of other minor tweaks.
  
  The text now includes another motivation for implementing this, other than latency: RPs would have to generate and store far fewer challenges than they currently do when using conditional UI.
  
  It remains an open question of how feasible this is for RPs to implement given the proposed security-related restrictions on its implementation.
categories: w3c
tags: webauthn
comments_file: webauthn-issue-2152_comments
permalink: /webauthn/2152/
url: https://github.com/w3c/webauthn/issues/2152
last_modified_at: 2024-11-25 16:24:13 +0000
---


**URL:** https://github.com/w3c/webauthn/issues/2152

WebAuthn challenges usually need to be fetched from the server. This introduces extra latency, especially in cases where the page is loaded from offline storage and apps. This extra latency delays when WebAuthn credentials can be shown to the user in an empty allow-list request.

## Proposed Change

Add a `challengeUrl` parameter that lets authenticators (or user agents) asynchronously fetch the challenge. This would let browsers render the list of credentials before the challenge comes back, improving the user experience. Add feature detection for it.

This obsoletes issue #1856.