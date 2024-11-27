---
title: "webauthn/pr/2209: Add test vectors"
date: 2024-11-20 18:38:52 +0000
author: emlun
categories: ["W3C"]
tags: ["webauthn"]
permalink: /webauthn/pr/2209/
comments_file: W3C-webauthn-pr-2209_comments
excerpt: >
  For these next 3 sections, I'm assuming no attestation is used despite the existence of the variables `attestation_private_key` and `attestation_cert_serial_number`? If so, it would be nice to add that in the section names. If they do have attestation, then the actual attestation should be added. For example if no attestation is used, this section should be called 'ES256 Credential with No Attestation and \"crossOrigin\": true in clientDataJSON'. Additionally like my first comment, it's less confusing if `attestation_private_key` and `attestation_cert_serial_number` were removed.    I say this since it's not uncommon for RPs to not support attestation—at least non-self attestation—and it would be nice to immediately know which tests are inapplicable/need-to-be-amended without actually parsing `attestationObject` to see if and what attestation is used.
---
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