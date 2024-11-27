---
title: "Backchannels Moved to Framework Repos"
date: 2024-10-22 21:49:59 +0000
author: nodlesh
excerpt: >
  In the VCX repo, the CI builds and publishes an image containing the VCX backchannel.  The Dockerfile in this OATH repo (for this backchannel) just references the name of the publishes image.
  
  For Aca-Py, we'll need to update the Aca-Py repo to contain all backchannel code, and to publish an image each time the `main` branch is updated in the repo.
  
  (For local testing, one can build a local backchannel image and then update the Dockerfile in the OATH repo to point to the locally generated image).
  
categories: openwallet-foundation
tags: owl-agent-test-harness
comments_file: owl-agent-test-harness-issue-881_comments
permalink: /owl-agent-test-harness/881/
url: https://github.com/openwallet-foundation/owl-agent-test-harness/issues/881
last_modified_at: 2024-11-26 19:19:10 +0000
---


**URL:** https://github.com/openwallet-foundation/owl-agent-test-harness/issues/881

Backchannels are moved out of AATH repo.

Follow the pattern of the Aries-VCX backchannel