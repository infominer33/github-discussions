---
title: "webauthn/issue/2205: Usage of \"effective domain\" seems wrong"
date: 2024-11-18 13:54:16 +0000
author: annevk
categories: ["W3C"]
tags: ["webauthn"]
permalink: /webauthn/issue/2205/
comments_file: W3C-webauthn-issue-2205_comments
excerpt: >
  Because the domain field is only set when `document.domain` is used. Generally that's an internal field for the HTML Standard.
---
No other specification really ought to use "effective domain". That's only for `document.domain`-related business. I suspect you just want to grab an origin's host and ignore this operation.