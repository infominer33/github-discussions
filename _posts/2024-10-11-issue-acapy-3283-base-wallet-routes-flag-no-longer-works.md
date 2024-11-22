---
title: "acapy/issue/3283: `--base-wallet-routes` flag no longer works"
date: 2024-10-11 17:16:41 +0000
author: dbluhm
categories: ["OWF"]
tags: ["acapy"]
permalink: /acapy/issue/3283/
comments_file: OWF-acapy-issue-3283_comments
---

[_https://github.com/openwallet-foundation/acapy/issues/3283_](https://github.com/openwallet-foundation/acapy/issues/3283)

After the swap to using decorators to delineate routes accessible by tenants and routes accessible by admins, the ability to grant access to the base wallet to additional routes was lost.

This option made it possible for a base wallet to form a didcomm connection with a mediator and then use that as a base mediator for all tenants, among other things.

cc @esune @jamshale 