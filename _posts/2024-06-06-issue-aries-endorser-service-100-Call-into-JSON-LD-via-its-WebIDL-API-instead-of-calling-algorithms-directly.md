---
title: "aries-endorser-service/issue/100: Call into JSON-LD via its WebIDL API instead of calling algorithms directly"
date: 2024-06-06 00:08:20 +0000
author: jyasskin
categories: ["DIF"]
tags: ["aries-endorser-service"]
permalink: /aries-endorser-service/issue/100/
comments_file: DIF-aries-endorser-service-issue-100_comments
---

[_https://github.com/hyperledger/aries-endorser-service/issues/100_](https://github.com/hyperledger/aries-endorser-service/issues/100)

In the discussion at https://github.com/w3c/json-ld-api/issues/580#issuecomment-2463356600, @gkellogg says that specs should always use the JSON-LD API instead of calling directly into JSON-LD algorithms. `data-cite="JSON-LD11-API` seems to be a good search term in this spec to find places that need fixing.