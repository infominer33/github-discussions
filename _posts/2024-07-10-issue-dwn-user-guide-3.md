---
title: "Move it2 helper to test reporter"
date: 2024-07-10 17:51:17 +0000
author: aljones15
excerpt: >
  Potential additional attributes:
  - DID Verification Approach: VDR/blockchain-based, self-verifying, not applicable, ... etc.
  - Target SDO: for standardization.  Different clusters (or subclusters) may want to target different SDOs ...e.g. W3C, IETF, European, ...?
  - DID Resolution Approach: this however is covered to a large extent by the column labels/horizontal axis
  -  Others?
  
  Instead of adding more dimensions to the DID Method Clustering Model, we can allow a DID Method to have multiple additional attributes/properties.  These, in turn, can be used to create sub-clusters of methods within a cluster (with corresponding sub-circles and sub-circle membership).
categories: decentralized-identity
tags: dwn-user-guide
comments_file: dwn-user-guide-issue-3_comments
permalink: /dwn-user-guide/3/
url: https://github.com/decentralized-identity/dwn-user-guide/issues/3
last_modified_at: 2024-11-22 20:36:32 +0000
---


**URL:** https://github.com/decentralized-identity/dwn-user-guide/issues/3

This is great code:

https://github.com/digitalbazaar/vc-data-model-2-test-suite/blob/6884551bb388784032d40a222340995c55adc75e/tests/10-vcdm2.js#L57-L65

But it should be here: https://github.com/digitalbazaar/mocha-w3c-interop-reporter

It also needs a better name, such as `reportRow({title: '', test: async function() {}})`
