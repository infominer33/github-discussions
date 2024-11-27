---
title: "chore: upgrade package from AFJ to credo-ts"
date: 2024-05-07 13:43:52 +0000
author: AmarjeetAkv
excerpt: >
  We fixed the changes requested by you.
  I have moved genesis configuration from sample.env, from now ledger came from config.js
  ```
  indyVdr: new IndyVdrModule({
      indyVdr,
      networks: [config.ledger]
   }),
  ```
  i have also updated config.js code from the PR #81
categories: decentralized-identity
tags: didcomm-demo
comments_file: didcomm-demo-pr-76_comments
permalink: /didcomm-demo/76/
url: https://github.com/decentralized-identity/didcomm-demo/pull/76
last_modified_at: 2024-11-19 08:55:57 +0000
---


**URL:** https://github.com/decentralized-identity/didcomm-demo/pull/76

- Replaced AFJ package with credo-ts across the codebase
- Updated relevant imports and dependencies to ensure compatibility with credo-ts
- Refactored code to align with any breaking changes or differences between AFJ and credo-ts Tested the changes to confirm that the upgrade works as expected without any issues.