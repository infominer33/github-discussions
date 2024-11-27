---
title: "vc-api/issue/383: Timeout on OPTIONS (cors preflight)"
date: 2024-05-14 16:12:53 +0000
author: robertocarvajal
categories: ["DIF"]
tags: ["vc-api"]
permalink: /vc-api/issue/383/
comments_file: DIF-vc-api-issue-383_comments
excerpt: >
  Thanks for catching that! As @panva noticed, the `[[usages]]` internal slot should be set as well :)
---
Seems like the mediator is responding like this:

```
atala-prism-mediator-identus-mediator-1  | 2024-11-24_00:56:53.696 WARN  f.d.f.TransportDispatcher@L167:[ZScheduler-Worker-1] {version=1.0.0, msg_sha256=c4946137e7ddb36a3261fd6dfb6b0b4265280b0a3dfc91c3e449513dd2c7ed10} - zio-fiber-1940542155 No url to send message
o.h.i.m.DIDCommRoutes@L167:[ZScheduler-Worker-2] {version=1.0.0} - zio-fiber-1688384339 Request Timeout
```

For a CORS check from the browser, this is causing Safari 18 to stop polling the endpoint since it triggers a CORS failure

Other browsers seems to just ignore this timeout and work fine.

In order for this bug to reproduce you need to run Safari 18 (Sequoia) on mediator v1.0.0.