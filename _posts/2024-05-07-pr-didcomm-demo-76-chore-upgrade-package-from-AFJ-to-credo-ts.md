---
title: "didcomm-demo/pr/76: chore: upgrade package from AFJ to credo-ts"
date: 2024-05-07 13:43:52 +0000
author: AmarjeetAkv
categories: ["DIF"]
tags: ["didcomm-demo"]
permalink: /didcomm-demo/pr/76/
comments_file: DIF-didcomm-demo-pr-76_comments
excerpt: >
  We fixed the changes requested by you.  I have moved genesis configuration from sample.env, from now ledger came from config.js  ```  indyVdr: new IndyVdrModule({      indyVdr,      networks: [config.ledger]   }),  ```  i have also updated config.js code from the PR #81
---
- Replaced AFJ package with credo-ts across the codebase
- Updated relevant imports and dependencies to ensure compatibility with credo-ts
- Refactored code to align with any breaking changes or differences between AFJ and credo-ts Tested the changes to confirm that the upgrade works as expected without any issues.