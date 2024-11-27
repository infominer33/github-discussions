---
title: "dpv/issue/182: Link in the CONTRIBUTING.md is broken"
date: 2024-08-15 08:22:02 +0000
author: mkbreuningIOHK
categories: ["Hyperledger"]
tags: ["dpv"]
permalink: /dpv/issue/182/
comments_file: Hyperledger-dpv-issue-182_comments
excerpt: >
  Thank you, this does answer my question. I'll keep an eye on this then.
---
### Is this a regression?

No

### Description

Steps:
- Got to https://github.com/input-output-hk/atala-prism-wallet-sdk-ts/blob/master/CONTRIBUTING.md 
- Click on the link on the line 53 "1. Follow all instructions in [the template](https://github.com/input-output-hk/atala-prism-wallet-sdk-ts/blob/main/.github/PULL_REQUEST_TEMPLATE.md)"
- It will open this browser window: https://github.com/input-output-hk/atala-prism-wallet-sdk-ts/blob/main/.github/PULL_REQUEST_TEMPLATE.md

![image](https://github.com/input-output-hk/atala-prism-wallet-sdk-ts/assets/97112931/9b3adaca-c2ec-4f15-be48-de6ba3977058)


### Please provide the exception or error you saw

```true
The error is that the file does not exist: 404 - page not found
The master branch of atala-prism-wallet-sdk-ts does not contain the path CONTRIBUTING.md.
```


### Please provide the environment you discovered this bug in

```true
On the GitHub remote site (corresponding to latest version v5.0.0), master branch.
```


### Anything else?

No