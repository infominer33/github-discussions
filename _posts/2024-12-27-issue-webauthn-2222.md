---
title: "Add a method to get all the credentials for a rely party on the client device to support the rely party (website) to limit the number of accounts a user can register"
date: 2024-12-27 00:29:59 +0000
author: bigradish
excerpt: >
  Hi Shane,
  
  I think we should not emphasize the user privacy too much. Providing more info to the RP properly may make Webauthn be used more widely.
  Thank you very much anyway. :)
categories: w3c
tags: webauthn
comments_file: webauthn-issue-2222_comments
permalink: /webauthn/2222/
url: https://github.com/w3c/webauthn/issues/2222
last_modified_at: 2024-12-27 04:22:27 +0000
---


**URL:** https://github.com/w3c/webauthn/issues/2222

It is very easy for a user to register many accounts on a website which using webauthn, but it seems that there is no an easy way to limit this capability of the user, for it is not easy to identify the user or the authenticator (many platforms do not return its AAGUID even if the "enterprise" conveyance option is used.) using javascript in browsers when the user is registering.
If there is a method that can get all the credentials for a rely party on the client device, the rely party (website) can easily limit the number of accounts a user can register using the client device.
Thank you very much.