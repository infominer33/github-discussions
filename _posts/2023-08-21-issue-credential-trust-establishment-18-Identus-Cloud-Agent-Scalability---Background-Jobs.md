---
title: "credential-trust-establishment/issue/18: Identus Cloud Agent Scalability - Background Jobs"
date: 2023-08-21 17:44:33 +0000
author: essbante-io
categories: ["DIF"]
tags: ["credential-trust-establishment"]
permalink: /credential-trust-establishment/issue/18/
comments_file: DIF-credential-trust-establishment-issue-18_comments
excerpt: >
  > Has a PR been created for this?    No not yet, this is currently assigned to @mccown, like issue https://github.com/w3c/did-resolution/issues/17
---
This Epic aims to investigate [ZIO Stream](https://zio.dev/reference/stream/) and [ZIO Kafka](https://github.com/zio/zio-kafka) as a replacement for the mechanism behind the execution of background jobs.

Currently, each background job is a recurrent ZIO effect created using `ZIO#repeat` that processes a configurable number of records in parallel during each iteration. This will inevitably lead to conflicts and race conditions as soon as we run two instances of the cloud agent in parallel, as the same record will be processed by those two agents sharing the same DB. The related flows will be executed multiple times, and the same DIDComm message will be sent several times to the DIDComm peer.

This can be solved using a message queueing system like Kafka and leveraging Kafka's `consumer groups` capability to concurrently distribute the load among multiple agent instances.

At a later stage, using a queuing mechanism like Kafka would allow us to better control - and allocate resources to - the execution of the resource-intensive tasks that put pressure on the system (e.g., generation of AnonCreds credential definitions via the Rust library).