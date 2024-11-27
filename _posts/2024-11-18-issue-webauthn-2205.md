---
title: "Usage of \"effective domain\" seems wrong"
date: 2024-11-18 13:54:16 +0000
author: annevk
excerpt: >
  Because the domain field is only set when `document.domain` is used. Generally that's an internal field for the HTML Standard.
categories: w3c
tags: webauthn
comments_file: webauthn-issue-2205_comments
permalink: /webauthn/2205/
url: https://github.com/w3c/webauthn/issues/2205
last_modified_at: 2024-11-21 06:01:57 +0000
---


**URL:** https://github.com/w3c/webauthn/issues/2205

No other specification really ought to use "effective domain". That's only for `document.domain`-related business. I suspect you just want to grab an origin's host and ignore this operation.