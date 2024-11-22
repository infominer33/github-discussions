---
title: "credential-trust-establishment/issue/35: Migration to new AnonCreds object format"
date: 2024-02-12 18:05:40 +0000
author: dbluhm
categories: ["DIF"]
tags: ["credential-trust-establishment"]
permalink: /credential-trust-establishment/issue/35/
comments_file: DIF-credential-trust-establishment-issue-35_comments
---

[_https://github.com/decentralized-identity/credential-trust-establishment/issues/35_](https://github.com/decentralized-identity/credential-trust-establishment/issues/35)

ACA-Py will eventually move a feature that is currently experimental to ready-for-use status: AnonCreds RS support. With this change, the migration strategy used in the wallet upgrade tool will require tweaks to migrate an Indy wallet to the new AnonCreds format.

Is this something we should worry about? It should be technically possible to upgrade using this tool as is and then use the upgrade endpoint @jamshale is working on in https://github.com/hyperledger/aries-cloudagent-python/pull/2922.

cc: @swcurran 