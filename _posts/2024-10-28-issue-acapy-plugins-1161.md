---
title: "Multitenancy support for OID4VC plugin"
date: 2024-10-28 14:14:18 +0000
author: pradeepp88
excerpt: >
  Hi @dbluhm I was able to get the `wallet_id` into the oid4vc issuer url as a subpath and use that to extract the tenant profile. I have created a Draft PR #1214 of the work done so far. Please review and add your comments - I am updating the integration tests now, if the design is ok, I can finalize the changes and make the PR ready for review.
categories: openwallet-foundation
tags: acapy-plugins
comments_file: acapy-plugins-issue-1161_comments
permalink: /acapy-plugins/1161/
url: https://github.com/openwallet-foundation/acapy-plugins/issues/1161
last_modified_at: 2024-11-20 21:01:57 +0000
---


**URL:** https://github.com/openwallet-foundation/acapy-plugins/issues/1161

Currently, the OID4VC plugin doesn't support multitenancy, and all operations are saved in the base wallet. When we secure the admin API, the supported credentials data is not passed on to the `.well-known` endpoint for the OID4VCI server.

We have reviewed the initial design options and have started work on enabling multitenancy for the OID4VC plugin.

The following changes are proposed:

- Pass wallet information to the OID4VC server. This can be done by:
  - Creating a separate sub-path for each wallet and hosting all endpoints within that sub-path, e.g., `<OID4VCI-Endpoint>/<wallet-id>`, using it for identification; or
  - Passing the wallet ID as a request parameter, e.g., `<OID4VCI-Endpoint>/.well-known/openid-credential-issuer?<wallet-id>`.
- Use the sub-path or request parameter to pass wallet information when issuing the credential offer.

We’re opening this issue to gather feedback from maintainers and other OID4VC developers to finalize the design and continue the work. cc: @dbluhm, @jamshale