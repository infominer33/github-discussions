---
title: "Improve capability delegation example and explanation"
date: 2024-08-05 11:27:24 +0000
author: wip-abramson
excerpt: >
  Hmm, this seems like it could be more clearly stated like this:
  
  ```suggestion
          In the example above, the DID document for <code>did:example:123456789abcdefghi</code> defines two verificationMethods, <code>#keys-1</code> and <code>#keys-2</code>, that can be used for the purpose of capability delegation. This means that these verification methods can be used to verify delegated capabilities issued by <code>did:example:123456789abcdefghi</code>.
  ```
  
  Notably, a root capability may not be \"issued\" at all -- except perhaps conceptually from the target / system of authority -- and yet if the controller (of that root capability) were `did:example:123456789abcdefghi`, then that entity could still delegate it by using this verification method. Further, the verification method isn't really used to \"produce\" a delegated capability (aka \"a delegation\"), but rather to verify one.
categories: openwallet-foundation
tags: acapy-plugins
comments_file: acapy-plugins-pr-875_comments
permalink: /acapy-plugins/875/
url: https://github.com/openwallet-foundation/acapy-plugins/pull/875
last_modified_at: 2025-01-04 19:48:49 +0000
---


**URL:** https://github.com/openwallet-foundation/acapy-plugins/pull/875

Hopefully this clarifies the confusion raised in #812


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
<a href="https://pr-preview.s3.amazonaws.com/wip-abramson/did-core/pull/875.html" title="Last updated on Jan 3, 2025, 10:47 AM UTC (9fd64e0)">Preview</a> | <a href="https://pr-preview.s3.amazonaws.com/w3c/did-core/875/3fa1d8d...wip-abramson:9fd64e0.html" title="Last updated on Jan 3, 2025, 10:47 AM UTC (9fd64e0)">Diff</a>