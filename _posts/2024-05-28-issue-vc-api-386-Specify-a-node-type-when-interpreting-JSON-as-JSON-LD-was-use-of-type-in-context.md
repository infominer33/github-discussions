---
title: "vc-api/issue/386: Specify a node type when interpreting JSON as JSON-LD (was: use of \"@type\" in \"@context\")"
date: 2024-05-28 19:08:45 +0000
author: ioggstream
categories: ["W3C"]
tags: ["vc-api"]
permalink: /vc-api/issue/386/
comments_file: W3C-vc-api-issue-386_comments
---

[_https://github.com/w3c-ccg/vc-api/issues/386_](https://github.com/w3c-ccg/vc-api/issues/386)

## Question

It's not clear to me if it's legitimate to use `@type` in `@context` instead of in the JSON object, eg.

```
"@context":
  "@vocab": "https://schema.org/",
  birthplace:
    "@type": "City"
birthplace:
  name: Roma
```

since the jsonld playground renders this as

```
_:c14n0 <https://schema.org/birthplace> _:c14n1 .
_:c14n1 <https://schema.org/name> "Roma" .
```
while I expect

```
_:c14n0 <http://www.w3.org/1999/02/22-rdf-syntax-ns#type> <https://schema.org/City> .
_:c14n0 <https://schema.org/name> "Roma" .
_:c14n1 <https://schema.org/birthplace> _:c14n0 .
```

## Note

changing the payload to

```
"birthplace": "Roma"
```
results in

```
_:c14n0 <https://schema.org/birthplace> "Roma"^^<https://schema.org/City> .
```

meaning that in some way the "City" type is processed in some way.
