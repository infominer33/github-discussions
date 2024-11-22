---
title: "webauthn/pr/2209: Add test vectors"
date: 2024-11-20 18:38:52 +0000
author: emlun
categories: ["W3C"]
tags: ["webauthn"]
permalink: /webauthn/pr/2209/
comments_file: W3C-webauthn-pr-2209_comments
---

[_https://github.com/w3c/webauthn/pull/2209_](https://github.com/w3c/webauthn/pull/2209)

Closes #1633. Sorry it took so long!

The test vectors proposed in #1633 use RP IDs of real websites unaffiliated with W3C, which felt out of place to me, so I chose to generate new ones instead. Also in order to pre-empt any worry that there could be something nefarious hidden in these values, they are all generated deterministically from disclosed PRNG seeds. Consequently the attestation statements are synthetic values rather than real attestations from the corresponding trusted source, which unfortunately means there's more room for error, but I think it's worth it to have the examples self-contained and transparent. I invite library authors to try running their registration and authentication procedures on these examples so that we may work out any inconsistencies.

I plan to also share the code used to generate these, but I needed to patch some of the libraries I used, so I need to resolve that first.


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
<a href="https://pr-preview.s3.amazonaws.com/w3c/webauthn/pull/2209.html" title="Last updated on Nov 20, 2024, 6:43 PM UTC (643273b)">Preview</a> | <a href="https://pr-preview.s3.amazonaws.com/w3c/webauthn/2209/e2987a9...643273b.html" title="Last updated on Nov 20, 2024, 6:43 PM UTC (643273b)">Diff</a>