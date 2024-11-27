---
title: "Support for subdirectory in SERVICE_ENDPOINTS"
date: 2024-11-24 00:04:25 +0000
author: robertocarvajal
excerpt: >
  Yes, forgot to mention, the service seems to still work but the webpage doesn't render.
categories: hyperledger
tags: identus-mediator
comments_file: identus-mediator-issue-382_comments
permalink: /identus-mediator/382/
url: https://github.com/hyperledger/identus-mediator/issues/382
last_modified_at: 2024-11-25 08:27:06 +0000
---


**URL:** https://github.com/hyperledger/identus-mediator/issues/382

Sometimes is desirable to run the mediator endpoint in a subdirectory of a webapp to avoid CORS issues, for example, defining `SERVICE_ENDPOINTS='https://www.myapp.com/mediator'`. If you setup the `ProxyPass` on webserver correctly, when you try to load the endpoint it fails trying to load `https://www.myapp.com/public/webapp-fastopt-bundle.js` because the mediator server endpoint is assuming the SERVICE_ENDPOINT is not on a subdirectory and on a web root.