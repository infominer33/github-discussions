---
title: "(chore) rust 1.83 update, dependency updates and workspace deps usage"
date: 2024-09-04 17:03:40 +0000
author: gmulhearn
excerpt: >
  disabled this flakey test. \"local/batch revocation\" needs to be re-assessed 
categories: hyperledger
tags: identus-cloud-agent
comments_file: identus-cloud-agent-pr-1320_comments
permalink: /identus-cloud-agent/1320/
url: https://github.com/hyperledger/identus-cloud-agent/pull/1320
last_modified_at: 2025-01-01 04:21:21 +0000
---


**URL:** https://github.com/hyperledger/identus-cloud-agent/pull/1320

Updates some major dep versions (notably askar), updates minor versions in the lockfile with `cargo update`, and convert alot of common dependencies to workspace deps