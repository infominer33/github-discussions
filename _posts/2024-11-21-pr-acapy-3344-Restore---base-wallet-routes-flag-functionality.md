---
title: "acapy/pr/3344: Restore `--base-wallet-routes` flag functionality"
date: 2024-11-21 18:21:14 +0000
author: esune
categories: ["OWF"]
tags: ["acapy"]
permalink: /acapy/pr/3344/
comments_file: OWF-acapy-pr-3344_comments
excerpt: >
  Actually just noticed a tiny spelling error here. Might as well fix it.
---
Resolves #3283

The `tenant_authentication` has been updated to also allow access to the base wallet when the route matches a path defined using `--base-wallet-routes`.

Please note that, when compared to the previous implementation, the matcher has been made more greedy to tighten security: if an extra route of `/test` is specified, the matcher will only match that and not `/testA` or `/test-something-else` as it appears it would have done before.

One drawback of having to use this matcher inside the decorator is that I could not think of an elegant way of caching the compiled pattern for reuse - suggestions on how to achieve that, if desirable/required, will be welcome.