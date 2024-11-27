---
title: "webauthn/issue/2211: CR: Need a way to detect \"cancel\""
date: 2024-11-21 17:31:50 +0000
author: hemanth
categories: ["W3C"]
tags: ["webauthn"]
permalink: /webauthn/issue/2211/
comments_file: W3C-webauthn-issue-2211_comments
excerpt: >
  `NotAllowedError` can also be returned synchronously without user interaction?
---
## Proposed Change

Need a way to programmatically detect when the user has cancelled the "Use passkey from another device" browser native prompt by clicking the "Cancel" button. This could be achieved by adding a new property or event to the prompt that indicates whether the user has cancelled the prompt.


<img width="468" alt="image" src="https://github.com/user-attachments/assets/748537c7-c9e7-4fb4-bd9c-715fc10d3f28">

^ the "cancel" button there.




