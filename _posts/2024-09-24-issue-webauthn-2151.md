---
title: "authenticatorDisplayName should use a localizable language map"
date: 2024-09-24 21:39:54 +0000
author: timcappalli
excerpt: >
  Ironically, this issue is now obsolete with PR #2194 merged.
categories: w3c
tags: webauthn
comments_file: webauthn-issue-2151_comments
permalink: /webauthn/2151/
url: https://github.com/w3c/webauthn/issues/2151
last_modified_at: 2024-11-13 20:57:26 +0000
---


**URL:** https://github.com/w3c/webauthn/issues/2151

Related to #1644

## Proposed Change

authenticatorDisplayName is currently a DOMString and does not support localization, specifically language codes and direction.

Change to a map following the String Meta spec: https://www.w3.org/TR/string-meta/#language-maps

```json
"authenticatorDisplayName": {
    "en":    {"value": "This is English"},
    "en-GB": {"value": "This is UK English", "dir": "ltr"},
    "fr":    {"value": "C'est français", "lang": "fr-CA", "dir": "ltr"},
    "ar":    {"value": "هذه عربية", "dir": "rtl"}
}
```

