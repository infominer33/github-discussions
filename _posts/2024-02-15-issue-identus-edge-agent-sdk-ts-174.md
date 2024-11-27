---
title: "MySQL Support"
date: 2024-02-15 15:55:21 +0000
author: niall-shaw
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

Our team currently uses [vdr-tools](https://gitlab.com/evernym/verity/vdr-tools) as the underlying framework to support AFJ on our mediator. The reasoning is better support for concurrency, as well as MySQL support.
We are now looking to upgrade AFJ to 0.4.x, and in by doing so upgrade to use Aries Askar etc.

Askar only supports SqlLite and Postgres - is there a workaround so that we can continue using MySQL?

