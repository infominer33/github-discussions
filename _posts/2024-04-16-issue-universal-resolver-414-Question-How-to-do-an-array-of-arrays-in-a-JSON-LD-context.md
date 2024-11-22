---
title: "universal-resolver/issue/414: [Question] How to do an array of arrays in a JSON-LD @context"
date: 2024-04-16 01:38:28 +0000
author: melvincarvalho
categories: ["DIF"]
tags: ["universal-resolver"]
permalink: /universal-resolver/issue/414/
comments_file: DIF-universal-resolver-issue-414_comments
---

[_https://github.com/decentralized-identity/universal-resolver/issues/414_](https://github.com/decentralized-identity/universal-resolver/issues/414)

Hi All

I need to create a context that models an array of arrays, and I was wondering how to do it.

Possibility 1: "tags": {"`@container`": "`@list`", "`@type`": "`@list`" }

```json
{
  "@context": {
    "@version": 1.1,
    "@vocab": "http://example.org/",
    "tags": {
      "@container": "@list",
      "@type": "@list"
    }
  },
  "tags": [
    ["A", "B", "C"],
    ["D", "E", "F"],
    ["G", "H", "I"]
  ]
}
```

Possibility 2: "tags": {"`@container`": "`@list`"}

```json
{
  "@context": {
    "@vocab": "http://example.org/",
    "tags": {"@container": "@list"}
  },
  "tags": [
    ["A", "B", "C"],
    ["D", "E", "F"],
    ["G", "H", "I"]
  ]
}
```

Possibility 3: Other (?)

Any help greatly appreciated