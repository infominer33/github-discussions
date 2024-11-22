---
title: "did-resolver/issue/97: Remove `checks` option in favor of loading from implementation configs."
date: 2021-08-30 09:14:56 +0000
author: BigBlueHat
categories: ["DIF"]
tags: ["did-resolver"]
permalink: /did-resolver/issue/97/
comments_file: DIF-did-resolver-issue-97_comments
---

[_https://github.com/decentralized-identity/did-resolver/issues/97_](https://github.com/decentralized-identity/did-resolver/issues/97)

> @PatStLouis @BigBlueHat so DB needs `checks: ['proof']` but other implementers might not need that option and further `options.checks` has not be in the VC API for awhile so the best way to handle this is to add `options.checks` to the DB implementation and do something like this:
>
> https://github.com/w3c-ccg/data-integrity-test-suite-assertion/blob/6d61d0f3940694edb12437bcb0f457a8b7cb56cb/assertions.js#L25-L46
>
> How to handle this situation in the bitstring status list suite is another issue as those tests will probably need us to expose a second verify with the correct checks for our verifier.

_Originally posted by @aljones15 in https://github.com/w3c/vc-data-model-2.0-test-suite/pull/92#discussion_r1693550614_
            