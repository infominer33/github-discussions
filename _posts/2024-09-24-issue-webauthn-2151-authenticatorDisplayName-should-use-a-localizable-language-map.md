---
title: "webauthn/issue/2151: authenticatorDisplayName should use a localizable language map"
date: 2024-09-24 21:39:54 +0000
author: timcappalli
categories: ["W3C"]
tags: ["webauthn"]
permalink: /webauthn/issue/2151/
comments_file: W3C-webauthn-issue-2151_comments
excerpt: >
  Ironically, this issue is now obsolete with PR #2194 merged.
---
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

