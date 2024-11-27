---
title: "Identus Cloud Agent Scalability - Background Jobs"
date: 2023-08-21 17:44:33 +0000
author: essbante-io
excerpt: >
  > Has a PR been created for this?
  
  No not yet, this is currently assigned to @mccown, like issue https://github.com/w3c/did-resolution/issues/17
categories: decentralized-identity
tags: credential-trust-establishment
comments_file: credential-trust-establishment-issue-18_comments
permalink: /credential-trust-establishment/18/
url: https://github.com/decentralized-identity/credential-trust-establishment/issues/18
last_modified_at: 2024-11-14 16:39:25 +0000
---


**URL:** https://github.com/decentralized-identity/credential-trust-establishment/issues/18

This Epic aims to investigate [ZIO Stream](https://zio.dev/reference/stream/) and [ZIO Kafka](https://github.com/zio/zio-kafka) as a replacement for the mechanism behind the execution of background jobs.

Currently, each background job is a recurrent ZIO effect created using `ZIO#repeat` that processes a configurable number of records in parallel during each iteration. This will inevitably lead to conflicts and race conditions as soon as we run two instances of the cloud agent in parallel, as the same record will be processed by those two agents sharing the same DB. The related flows will be executed multiple times, and the same DIDComm message will be sent several times to the DIDComm peer.

This can be solved using a message queueing system like Kafka and leveraging Kafka's `consumer groups` capability to concurrently distribute the load among multiple agent instances.

At a later stage, using a queuing mechanism like Kafka would allow us to better control - and allocate resources to - the execution of the resource-intensive tasks that put pressure on the system (e.g., generation of AnonCreds credential definitions via the Rust library).