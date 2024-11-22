---
title: "did-core/issue/865: Question about query parameter ordering"
date: 2024-09-25 12:50:27 +0000
author: SaulMoonves
categories: ["W3C"]
tags: ["did-core"]
permalink: /did-core/issue/865/
comments_file: W3C-did-core-issue-865_comments
---

[_https://github.com/w3c/did-core/issues/865_](https://github.com/w3c/did-core/issues/865)

I am looking for guidance on query parameter ordering, specifically where a DID URL with a query parameter might be used as an ID

In many systems such as ActivityPub, an ID is basically an opaque string but in practice it is a URL whose structure gives a hint on how to resolve it, like using an HTTPS URL that resolves to the object.

I am in the process of trying to implement `did:web` for activitystreams object IDs inside of an ActivityPub project, but this would I think equally apply to service IDs in the DID document: How do I deal with query parameters being seemingly unordered if some things rely on IDs equally matching? Is anyone dealing with this in their projects?