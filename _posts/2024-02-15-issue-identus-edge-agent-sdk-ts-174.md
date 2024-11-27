---
title: "TTL is mandatory 5 minute period if not specified"
date: 2024-02-15 15:55:21 +0000
author: msporny
excerpt: >
  PR #186 has been raised to address this issue. This issue will be closed once PR #186 has been merged.
categories: hyperledger
tags: identus-edge-agent-sdk-ts
comments_file: identus-edge-agent-sdk-ts-issue-174_comments
permalink: /identus-edge-agent-sdk-ts/174/
url: https://github.com/hyperledger/identus-edge-agent-sdk-ts/issues/174
last_modified_at: 2024-11-24 23:21:45 +0000
---


**URL:** https://github.com/hyperledger/identus-edge-agent-sdk-ts/issues/174

The specification currently states that if a TTL isn't specified, it's 5 minutes. This is a problem for offline use cases where organizations might not want to use the TTL and do not want to presume it is 5 minutes.

The specification needs to make TTL completely optional with no minimum timeout assumed unless stated.
