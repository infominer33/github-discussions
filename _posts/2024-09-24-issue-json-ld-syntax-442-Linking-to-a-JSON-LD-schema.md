---
title: "json-ld-syntax/issue/442: Linking to a JSON-LD schema?"
date: 2024-09-24 19:03:22 +0000
author: trwnh
categories: ["DIF"]
tags: ["json-ld-syntax"]
permalink: /json-ld-syntax/issue/442/
comments_file: DIF-json-ld-syntax-issue-442_comments
---

[_https://github.com/w3c/json-ld-syntax/issues/442_](https://github.com/w3c/json-ld-syntax/issues/442)

Based on my understanding, "context is not a schema" -- `@context` serves to map terms to IRIs via term definitions, not to describe the actual data.

To address this, I've considered the following:

- Serve a remote context document at one location, and serve a remote schema document at another location. Declare the remote context document as the `@context`. Manually import the schema document.
- Serve the two in the same document. My understanding is that `@context` processing will only work with the `@context` entry of the resolved document ( as described in step 5.2.4 of the algorithm https://www.w3.org/TR/json-ld11-api/#algorithm ), so it is okay to put additional entries into the document, but it is *not* okay to put additional entries if the context was locally embedded instead. (Which is to say: a term definition having `@id` is a completely separate mechanism from what that `@id` represents, right?)

In the latter case (assuming I am correct that it is valid), there is a need to express that the document resolved not only contains a `@context` key to be used in context processing, but that it also contains a graph of statements representing RDF Schema, OWL, and other such metadata. For this, I wonder if it makes sense to declare a new keyword `@schema`, to be similarly applied until overridden by a more recent definition.

It's also possible I'm confused about all this, and there's a more idiomatic way to accomplish this. In either case, I'd appreciate feedback about this idea.