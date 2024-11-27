---
title: "identus-mediator/issue/382: Support for subdirectory in SERVICE_ENDPOINTS"
date: 2024-11-24 00:04:25 +0000
author: robertocarvajal
categories: ["W3C"]
tags: ["identus-mediator"]
permalink: /identus-mediator/issue/382/
comments_file: W3C-identus-mediator-issue-382_comments
excerpt: >
  Yes, forgot to mention, the service seems to still work but the webpage doesn't render.
---
Sometimes is desirable to run the mediator endpoint in a subdirectory of a webapp to avoid CORS issues, for example, defining `SERVICE_ENDPOINTS='https://www.myapp.com/mediator'`. If you setup the `ProxyPass` on webserver correctly, when you try to load the endpoint it fails trying to load `https://www.myapp.com/public/webapp-fastopt-bundle.js` because the mediator server endpoint is assuming the SERVICE_ENDPOINT is not on a subdirectory and on a web root.