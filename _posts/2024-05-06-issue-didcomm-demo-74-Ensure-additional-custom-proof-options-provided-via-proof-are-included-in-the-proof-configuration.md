---
title: "didcomm-demo/issue/74: Ensure additional custom proof options provided via `proof` are included in the proof configuration"
date: 2024-05-06 11:09:29 +0000
author: dlongley
categories: ["DIF"]
tags: ["didcomm-demo"]
permalink: /didcomm-demo/issue/74/
comments_file: DIF-didcomm-demo-issue-74_comments
---

[_https://github.com/decentralized-identity/didcomm-demo/issues/74_](https://github.com/decentralized-identity/didcomm-demo/issues/74)

When creating a proof, other custom proof fields might be given, but it looks like the proof configuration algorithm will not include these -- and it should.