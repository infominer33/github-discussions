---
title: "identus-apollo/pr/179: Remove proof options from base proof serialization again."
date: 2024-07-09 09:58:01 +0000
author: aljones15
categories: ["Hyperledger"]
tags: ["identus-apollo"]
permalink: /identus-apollo/pr/179/
comments_file: Hyperledger-identus-apollo-pr-179_comments
---

[_https://github.com/hyperledger/identus-apollo/pull/179_](https://github.com/hyperledger/identus-apollo/pull/179)

Corrects a potential regress of https://github.com/w3c/vc-di-bbs/pull/173/files

Removes the proofOptions section from base proof serialization again.
Interestingly the proofOptions did not need to be removed from the Algorithms section again.


<!--
    This comment and the below content is programmatically generated.
    You may add a comma-separated list of anchors you'd like a
    direct link to below (e.g. #idl-serializers, #idl-sequence):

    Don't remove this comment or modify anything below this line.
    If you don't want a preview generated for this pull request,
    just replace the whole of this comment's content by "no preview"
    and remove what's below.
-->
***
<a href="https://pr-preview.s3.amazonaws.com/aljones15/vc-di-bbs/pull/179.html" title="Last updated on Jul 2, 2024, 2:17 PM UTC (8699f90)">Preview</a> | <a href="https://pr-preview.s3.amazonaws.com/w3c/vc-di-bbs/179/3f3585f...aljones15:8699f90.html" title="Last updated on Jul 2, 2024, 2:17 PM UTC (8699f90)">Diff</a>