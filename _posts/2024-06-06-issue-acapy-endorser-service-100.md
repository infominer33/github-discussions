---
title: "Call into JSON-LD via its WebIDL API instead of calling algorithms directly"
date: 2024-06-06 00:08:20 +0000
author: jyasskin
excerpt: >
  The reason for this recommendation is that the algorithms make use of options set the API (e.g., `compactArrays`, `documentLoader`, `processingMode`, ...). That's not to say that you can't use the algorithms directly, but where they call for using the value (explicit or default) of an API option, you'll need to take a separate provision for this.
  
  As long as dependent specs are cognizant of this (e.g., using xxx for `documentLoader`) it should be fine, but the algorithms to take advantage of the envelope the API method steps provide.
categories: openwallet-foundation
tags: acapy-endorser-service
comments_file: acapy-endorser-service-issue-100_comments
permalink: /acapy-endorser-service/100/
url: https://github.com/openwallet-foundation/acapy-endorser-service/issues/100
last_modified_at: 2024-11-17 20:40:46 +0000
---


**URL:** https://github.com/openwallet-foundation/acapy-endorser-service/issues/100

In the discussion at https://github.com/w3c/json-ld-api/issues/580#issuecomment-2463356600, @gkellogg says that specs should always use the JSON-LD API instead of calling directly into JSON-LD algorithms. `data-cite="JSON-LD11-API` seems to be a good search term in this spec to find places that need fixing.