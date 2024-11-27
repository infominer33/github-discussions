---
title: "org/issue/33: Cloud Agent to publish PrismDID on behalf of external wallet into VDR"
date: 2024-03-23 19:27:01 +0000
author: robertocarvajal
categories: ["DIF"]
tags: ["org"]
permalink: /org/issue/33/
comments_file: DIF-org-issue-33_comments
excerpt: >
  yeah, I feel we can close this issue and keep the discussion over the other one because it has a broader scope and was discussed recently over the weekly meetings.
---
**Is your feature request related to a problem? Please describe.**
Currently, Cloud Agent can only publish PrismDIDs that are created by the same Cloud Agent into the VDR. Most Edge Clients will never be connected to a full node in order to publish their PrismDIDs to the VDR and it could be useful for certain use cases.

**Describe the solution you'd like**
It would be great to ask the Cloud Agent to publish a PrismDID created from my Edge Client Wallet through the REST API.

**Describe alternatives you've considered**
Allowing the Edge SDK to connect directly to icarus (like the cloud agent does) and prepare the right payload which I would need to reverse engineer anyways from the cloud agent code :)
