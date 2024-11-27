---
title: "identus-edge-agent-sdk-ts/issue/174: MySQL Support"
date: 2024-02-15 15:55:21 +0000
author: niall-shaw
categories: ["Hyperledger"]
tags: ["identus-edge-agent-sdk-ts"]
permalink: /identus-edge-agent-sdk-ts/issue/174/
comments_file: Hyperledger-identus-edge-agent-sdk-ts-issue-174_comments
excerpt: >
  PR #186 has been raised to address this issue. This issue will be closed once PR #186 has been merged.
---
Our team currently uses [vdr-tools](https://gitlab.com/evernym/verity/vdr-tools) as the underlying framework to support AFJ on our mediator. The reasoning is better support for concurrency, as well as MySQL support.
We are now looking to upgrade AFJ to 0.4.x, and in by doing so upgrade to use Aries Askar etc.

Askar only supports SqlLite and Postgres - is there a workaround so that we can continue using MySQL?

