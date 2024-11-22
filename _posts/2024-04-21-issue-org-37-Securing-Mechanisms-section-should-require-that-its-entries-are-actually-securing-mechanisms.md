---
title: "org/issue/37: Securing Mechanisms section should require that its entries are actually securing mechanisms"
date: 2024-04-21 01:16:24 +0000
author: jyasskin
categories: ["DIF"]
tags: ["org"]
permalink: /org/issue/37/
comments_file: DIF-org-issue-37_comments
---

[_https://github.com/decentralized-identity/org/issues/37_](https://github.com/decentralized-identity/org/issues/37)

https://w3c.github.io/vc-data-model/#verification says to look up a media type in https://w3c.github.io/vc-specs-dir/#securing-mechanisms (or other mechanisms known to the implementation) and that the result "MUST implement the interface described in [[5.12 Securing Mechanism Specifications](https://w3c.github.io/vc-data-model/#securing-mechanism-specifications)]." But nothing in this registry constrains the editors to only accept specs that implement that interface. This puts an unnecessary burden on implementations to check every entry in the registry themselves and only use it if it implements the interface.

I don't think the editors should need to check the quality of the securing mechanisms, just that they provide the right interface.