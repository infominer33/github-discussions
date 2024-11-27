---
title: "Failed deployment is shown as successful"
date: 2024-07-29 16:04:08 +0000
author: mkbreuningIOHK
excerpt: >
  PR #81 was applied to address this issue. Closing.
categories: w3c
tags: did-resolution
comments_file: did-resolution-issue-80_comments
permalink: /did-resolution/80/
url: https://github.com/w3c/did-resolution/issues/80
last_modified_at: 2024-11-17 19:16:01 +0000
---


**URL:** https://github.com/w3c/did-resolution/issues/80

In order to deploy the docs corresponding to prism v2.9, https://github.com/input-output-hk/atala-releases/blob/master/Atala%20PRISM/2.9.md, I have chosen the wrong version (OEA version instead of the documentation version).

In https://github.com/input-output-hk/atala-prism-docs/actions, click on `Deployment` and then `Run workflow`
I chose: main branch, v1.25.0 and production and click `Run workflow`.
It gave a successful deployment when looking after but the docs.atalaprism.io was still not updated as it showed in API --> Agent API the same old version v1.22.0. See attached screenshot.

The expectation is that as the workflow failed, the status should show as failed. 
![image](https://github.com/input-output-hk/atala-prism-docs/assets/97112931/c6ca4531-464e-4b5b-b133-716b881da379)

 If you look at the workflow file, there is no information that would give any indication of what was run.
If you look at the https://github.com/input-output-hk/atala-prism-docs/actions/runs/7959863521/job/21727672596 , there is no information on the parsing of the version for example.