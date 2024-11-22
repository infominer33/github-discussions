---
title: "didcomm-demo/pr/76: Fix B.3 Representation: Ed25519Signature2020 test vectors"
date: 2024-05-07 13:43:52 +0000
author: filip26
categories: ["DIF"]
tags: ["didcomm-demo"]
permalink: /didcomm-demo/pr/76/
comments_file: DIF-didcomm-demo-pr-76_comments
---

[_https://github.com/decentralized-identity/didcomm-demo/pull/76_](https://github.com/decentralized-identity/didcomm-demo/pull/76)

Adds missing `@context` `https://w3id.org/security/suites/ed25519-2020/v1`  to `Ed25519Signature2020` test vectors.  Proof canonical form, hash, and signature are re-computed.

It's related to, but does not close, issue #75


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
<a href="https://pr-preview.s3.amazonaws.com/filip26/vc-di-eddsa/pull/76.html" title="Last updated on Feb 27, 2024, 5:41 PM UTC (52110f6)">Preview</a> | <a href="https://pr-preview.s3.amazonaws.com/w3c/vc-di-eddsa/76/215cdba...filip26:52110f6.html" title="Last updated on Feb 27, 2024, 5:41 PM UTC (52110f6)">Diff</a>