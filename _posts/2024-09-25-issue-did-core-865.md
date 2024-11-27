---
title: "Question about query parameter ordering"
date: 2024-09-25 12:50:27 +0000
author: SaulMoonves
excerpt: >
  > your application/specification will have to contain some query parameter canonicalization rules to ensure equivalence holds in your application area
  
  If I'm reading this correctly, then you're saying that something like:
  
  ```json
  {
    \"@id\": \"did:example:abc123?service=foo&relativeRef=/\"
  }
  ```
  
  is going to require some additional equivalence-checking? Which I guess means that it's no longer opaque. So basically this should be part of the protocol considerations of whatever protocol is producing and consuming such identifiers. So basically this should be an ActivityPub concern (for example).
  
  Although I think that at least for the purposes of DID specs, a quick note about query parameter ordering wouldn't be amiss. For example in https://w3c.github.io/did-core/#did-parameters or something.
categories: w3c
tags: did-core
comments_file: did-core-issue-865_comments
permalink: /did-core/865/
url: https://github.com/w3c/did-core/issues/865
last_modified_at: 2024-11-18 03:47:08 +0000
---


**URL:** https://github.com/w3c/did-core/issues/865

I am looking for guidance on query parameter ordering, specifically where a DID URL with a query parameter might be used as an ID

In many systems such as ActivityPub, an ID is basically an opaque string but in practice it is a URL whose structure gives a hint on how to resolve it, like using an HTTPS URL that resolves to the object.

I am in the process of trying to implement `did:web` for activitystreams object IDs inside of an ActivityPub project, but this would I think equally apply to service IDs in the DID document: How do I deal with query parameters being seemingly unordered if some things rely on IDs equally matching? Is anyone dealing with this in their projects?