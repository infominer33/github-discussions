---
title: "ecdsa-rdfc-2019 Transformation passes wrong type to \"Deserialize JSON-LD\""
date: 2024-06-24 18:34:05 +0000
author: jyasskin
excerpt: >
  The error “Unexpected identifier ‘assert’” is occurring because:
  	1.	Node.js v22 removed support for “import assertions” in favor of “import attributes”.
  	2.	The `@veramo/credential-ld` package or its dependencies likely uses the older “import assertions” syntax.
  
  Here is a workaround
  Add the below lines to your package.json
    },
      \"engines\": {
      \"node\": \"20.0\"
    },
categories: decentralized-identity
tags: spec-up
comments_file: spec-up-issue-66_comments
permalink: /spec-up/66/
url: https://github.com/decentralized-identity/spec-up/issues/66
last_modified_at: 2024-12-27 00:00:25 +0000
---


**URL:** https://github.com/decentralized-identity/spec-up/issues/66

https://www.w3.org/TR/vc-di-ecdsa/#transformation-ecdsa-rdfc-2019 takes a [map](https://infra.spec.whatwg.org/#ordered-map) that is not the result of the [Node Map Generation algorithm](https://www.w3.org/TR/json-ld11-api/#node-map-generation) and passes it to https://www.w3.org/TR/json-ld11-api/#deserialize-json-ld-to-rdf-algorithm, which expects "a [map](https://infra.spec.whatwg.org/#ordered-map) node map, which is the result of the [Node Map Generation algorithm](https://www.w3.org/TR/json-ld11-api/#node-map-generation)".

https://github.com/w3c/json-ld-api/issues/579 reports that this type requirement is unclear, but the discussion there indicates that you're expected to do the extra step in callers.