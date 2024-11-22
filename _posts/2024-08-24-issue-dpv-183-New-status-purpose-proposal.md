---
title: "dpv/issue/183: New status purpose proposal"
date: 2024-08-24 16:58:44 +0000
author: PatStLouis
categories: ["DIF"]
tags: ["dpv"]
permalink: /dpv/issue/183/
comments_file: DIF-dpv-issue-183_comments
---

[_https://github.com/w3c/dpv/issues/183_](https://github.com/w3c/dpv/issues/183)

Greetings, while implementing `BitstringStatusList` in our use case (supply-chain), we uncovered a situation where an issued credential might have a new version available for pickup which doesn't warrant a revocation of the previous version, but it would still be worthwhile to have a status to signal that an updated version is available.

Therefore I would like to suggest adding a status purpose ~`supersession`~ `refresh`, which can have a value of `0`(meaning this is the latest version of the credential available) or `1` (MAY be refreshed).

The process for a holder and/or verifier to get the latest version is out of scope, however I would intend this to be used in parallel with a ~`SupersessionRefresh`~ defined `refreshService` type, which contains an endpoint to query and get an updated version of the credential.

Once the software have retrieved the latest version of the credential, they would archive the current version and replace it with the latest version in their software, or create a [Symbolic link](https://en.wikipedia.org/wiki/Symbolic_link) towards it.

edit: renamed `supersession` to `refresh` as proposed.