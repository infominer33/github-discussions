---
title: "Convert suites over to local issuers / vc-gen"
date: 2024-06-30 12:28:40 +0000
author: aljones15
excerpt: >
  @mixmix these are great points, I suggest we create a [Github discussion](https://github.com/hyperledger/identus/discussions) to discuss it further.
categories: decentralized-identity
tags: linked-vp
comments_file: linked-vp-issue-53_comments
permalink: /linked-vp/53/
url: https://github.com/decentralized-identity/linked-vp/issues/53
last_modified_at: 2024-11-25 14:27:19 +0000
---


**URL:** https://github.com/decentralized-identity/linked-vp/issues/53

Currently the JCS suite still creates test data by calling on a remote endpoint:

https://github.com/w3c/vc-di-eddsa-test-suite/blob/720e2b094cb87a165eb4e7de79fd2c597ec366b9/tests/50-jcs-verify.js#L10-L31

This suite needs to remove all test data creation using endpoints (even outside of the JCS verify suite). 

1. expand the vc-generator to cover all suites involved with the test
2. use that vc-gen to create both rdfc and jcs test fixtures