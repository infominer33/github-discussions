---
title: "Update maintainers `w3cid` value in documents"
date: 2023-08-23 13:13:40 +0000
author: msporny
excerpt: >
  I just added my w3cid. Sorry for the delay! Thanks!
categories: w3c-ccg
tags: traceability-interop
comments_file: traceability-interop-issue-589_comments
permalink: /traceability-interop/589/
url: https://github.com/w3c-ccg/traceability-interop/issues/589
last_modified_at: 2024-11-25 10:52:34 +0000
---


**URL:** https://github.com/w3c-ccg/traceability-interop/issues/589

Hi @apuchitnis @stenreijers @gatemezing @adam-burns @Steffytan @MizukiSonoko @rajivrajani @genaris @ajile-in and @KDean-Dolphin, 

Publication of did-extensions is currently failing because some of you don't have `w3cid` values listed in your Editor's entry in each specification. I need each of you to update your `w3cid` value in the "Editors" section of each document listed below:

* https://github.com/w3c/did-extensions/blob/main/index.html#L54-L95
* https://github.com/w3c/did-extensions/blob/main/methods/index.html#L95-L136
* https://github.com/w3c/did-extensions/blob/main/properties/index.html#L54-L96
* https://github.com/w3c/did-extensions/blob/main/resolution/index.html#L54-L96

If you don't have a free w3.org account, you can get one here:

https://www.w3.org/account/request/

You can then see your `w3cid` value by logging into w3.org and going to this link:

https://www.w3.org/users/myprofile/

The value will be in the URL in your web browser address bar. For example, when I go to the URL above, I get redirected to this URL (and my `w3cid` value is `41758`):

https://www.w3.org/users/41758/

Just raise a PR on all four documents above and I'll merge them as they come in.