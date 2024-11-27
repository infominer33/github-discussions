---
title: "identus/issue/76: Improve Infrastructure provisioning"
date: 2024-10-21 14:31:35 +0000
author: elribonazo
categories: ["DIF"]
tags: ["identus"]
permalink: /identus/issue/76/
comments_file: DIF-identus-issue-76_comments
excerpt: >
  Working as expected
---
### Short Description

Improve the infrastructure provisioning by reducing the amount of services that are bundled by default + making those easier to configure and not require any specific SH configuration script. On top of that we also aim to make everything deployable from a single docker image and not require too many images.

### Value statement

Main goal behind this EPIC is to make our services easier to configure and maintain over time. For existing users, this will improve code maintenance and reduce the time spent on configuring the services and for our new users this will make it extremely easier to kick-off your project in Identus ecosystem. We mainly aim to reduce friction when it comes to configuring the services and get everything configured to start developing code.

### Components

[Cloud Agent](https://github.com/hyperledger/identus-cloud-agent)

### Team members

@hyperledger/identus

### Architect

@hyperledger/identus-maintainers 

### QA Member

@hyperledger/identus-maintainers 

### Owner

@hyperledger/identus-maintainers 