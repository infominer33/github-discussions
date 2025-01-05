---
title: "eddsa-rdfc-2022 Transformation passes wrong type to \"Deserialize JSON-LD\""
date: 2024-04-04 15:14:36 +0000
author: jyasskin
excerpt: >
  @FabioPinheiro moving back to `Planned` because it's lacking the `cloud-agent` part  
  About the prism node: https://hub.docker.com/r/identus/prism-node  
  Let me know if you need any help on the semantic-release side
categories: trustoverip
tags: tswg-cesr-specification
comments_file: tswg-cesr-specification-issue-87_comments
permalink: /tswg-cesr-specification/87/
url: https://github.com/trustoverip/tswg-cesr-specification/issues/87
last_modified_at: 2025-01-03 13:16:06 +0000
---


**URL:** https://github.com/trustoverip/tswg-cesr-specification/issues/87

https://www.w3.org/TR/vc-di-eddsa/#transformation-eddsa-rdfc-2022 takes a [map](https://infra.spec.whatwg.org/#ordered-map) that is not the result of the [Node Map Generation algorithm](https://www.w3.org/TR/json-ld11-api/#node-map-generation) and passes it to https://www.w3.org/TR/json-ld11-api/#deserialize-json-ld-to-rdf-algorithm, which expects "a [map](https://infra.spec.whatwg.org/#ordered-map) node map, which is the result of the [Node Map Generation algorithm](https://www.w3.org/TR/json-ld11-api/#node-map-generation)".

https://github.com/w3c/json-ld-api/issues/579 reports that this type requirement is unclear, but the discussion there indicates that you're expected to do the extra step in callers.