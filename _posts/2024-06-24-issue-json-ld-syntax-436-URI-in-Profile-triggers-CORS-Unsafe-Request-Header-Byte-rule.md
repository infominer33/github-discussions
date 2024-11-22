---
title: "json-ld-syntax/issue/436: URI in Profile triggers CORS Unsafe Request Header Byte rule"
date: 2024-06-24 21:08:08 +0000
author: azaroth42
categories: ["DIF"]
tags: ["json-ld-syntax"]
permalink: /json-ld-syntax/issue/436/
comments_file: DIF-json-ld-syntax-issue-436_comments
---

[_https://github.com/w3c/json-ld-syntax/issues/436_](https://github.com/w3c/json-ld-syntax/issues/436)


In the IANA registration [1], we define a media type parameter called 'profile'. Its value is a space separated list of URIs, for which we registered six initial values. These can be composed together, and new values can be added for other "constraints or conventions".

The IIIF specifications use this functionality, for example to define the specific structure of the response in an API [2] as part of the media type. Similarly in Linked Art, we do the same [3].

However, in the WHATWG specification for fetch [4], it says that the *value* for the Accept header is NOT CORS safe, if it has more than 128 bytes (which multiple URIs might easily cause) or (more importantly) if the value contains an unsafe header byte. The unsafe header bytes include the character ":" ... which prevents *any* URI or CURIE with a namespace prefix separate by : from being CORS safe. 

This means that we cannot use the JSON-LD media type as registered for content negotiation via the `accept` header according to the fetch specification, which was much of the rationale for the profile parameter.

To resolve this, either WHATWG would need to change fetch, or W3C/IANA would need to change the definition of the media type and give some registration function for possible `profile` values, then all downstream specifications would need to register a safe profile value to use.

I've added the tag-needs-resolution label, as I think that's the level this would need to run up to :(

[1] https://www.w3.org/TR/json-ld11/#iana-considerations
[2] https://iiif.io/api/presentation/3.0/#63-responses 
[3] https://linked.art/api/1.0/json-ld/#introduction
[4] https://fetch.spec.whatwg.org/#ref-for-cors-unsafe-request-header-byte
