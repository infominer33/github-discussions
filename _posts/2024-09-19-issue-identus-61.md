---
title: "Service Endpoint Construction inconsistency"
date: 2024-09-19 13:27:35 +0000
author: clehner
excerpt: >
  This was discussed during the [#did meeting on 21 November 2024](https://www.w3.org/2024/11/21-did-minutes.html#4c13).
categories: hyperledger
tags: identus
comments_file: identus-issue-61_comments
permalink: /identus/61/
url: https://github.com/hyperledger/identus/issues/61
last_modified_at: 2024-11-21 17:01:21 +0000
---


**URL:** https://github.com/hyperledger/identus/issues/61

The example (https://w3c-ccg.github.io/did-resolution/#example-11) is inconsistent with the algorithm (https://w3c-ccg.github.io/did-resolution/#algorithm).

The example says:

> Given the following input service endpoint URL:
>
> `https://example.com/messages/8377464`
>
> And given the following input DID URL:
>
> `did:example:123456789abcdefghi?service=messages&relative-ref=%2Fsome%2Fpath%3Fquery#frag`
>
> Then the output service endpoint URL is:
>
> `https://example.com/messages/8377464/some/path?query#frag`

But by following the algorithm, I get this as the output URL:
```
https://example.com/messages/8377464?service=messages&relative-ref=%2Fsome%2Fpath%3Fquery#frag
```
It looks like in the example the `relative-ref` DID parameter is used instead of (or in addition to) the input DID URL path and query.

There is also an example in `did-core` (https://w3c.github.io/did-core/#example-9) for "A resource external to a DID Document", using service and relativeRef:
```
did:example:123?service=agent&relativeRef=/credentials#degree
```

Is using `relativeRef`/`relative-ref` the way to go? If so, how should it interact with the path component and other query parameters in service endpoint construction?