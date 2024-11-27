---
title: "CR: Need a way to detect \"cancel\""
date: 2024-11-21 17:31:50 +0000
author: hemanth
excerpt: >
  `NotAllowedError` can also be returned synchronously without user interaction?
categories: w3c
tags: webauthn
comments_file: webauthn-issue-2211_comments
permalink: /webauthn/2211/
url: https://github.com/w3c/webauthn/issues/2211
last_modified_at: 2024-11-21 17:38:36 +0000
---


**URL:** https://github.com/w3c/webauthn/issues/2211

## Proposed Change

Need a way to programmatically detect when the user has cancelled the "Use passkey from another device" browser native prompt by clicking the "Cancel" button. This could be achieved by adding a new property or event to the prompt that indicates whether the user has cancelled the prompt.


<img width="468" alt="image" src="https://github.com/user-attachments/assets/748537c7-c9e7-4fb4-bd9c-715fc10d3f28">

^ the "cancel" button there.




