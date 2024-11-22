---
title: "aries-vcx/issue/1163: Edge-client initiated connections"
date: 2024-03-22 11:12:01 +0000
author: mixmix
categories: ["Hyperledger"]
tags: ["aries-vcx"]
permalink: /aries-vcx/issue/1163/
comments_file: Hyperledger-aries-vcx-issue-1163_comments
---

[_https://github.com/hyperledger/aries-vcx/issues/1163_](https://github.com/hyperledger/aries-vcx/issues/1163)

### Proposed feature

We have a Catalyst grant around reducing the overhead for edge-clients initiating connections with cloud-agents.

We've looked into how the SDK handles OOB invites, and discovered that the OOB is just converted into a `Message` which is then sent to the Agent. We would like the Agent to accept messages made by the SDK purely from the `peerDID`.

### Feature description

Either:
- A) help us craft the right sort of `https://atalaprism.io/mercury/connections/1.0/request` message
- B) change the cloud agent to to accept SDK initiated connections
- C) change the cloud agent to be configurable to optionally accept SDK initiated connections

