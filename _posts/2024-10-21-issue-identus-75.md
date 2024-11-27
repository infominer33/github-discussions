---
title: "DID management component discussion"
date: 2024-10-21 14:18:04 +0000
author: goncalo-frade-iohk
excerpt: >
  I cannot figure out how the rights are structured in the EU vocabs, or even if they are supposed to be complete (e.g. I couldn't find article 9 protection of personal data in there). Therefore, I suggest we add a note referring the reader to the resource, asking for contribution if they know how to interpret the structure/concepts.
categories: hyperledger
tags: identus
comments_file: identus-issue-75_comments
permalink: /identus/75/
url: https://github.com/hyperledger/identus/issues/75
last_modified_at: 2024-11-14 17:20:17 +0000
---


**URL:** https://github.com/hyperledger/identus/issues/75

The reason for this discussion is there is a need for a better did management component.
As part of this discussion the following is purposed:

- Separate Plutos DID Management side into a more flexible protocol.
- Make the DID management data more common, aka: instead of having a different storage for PrismDID and PeerDID have a storage for DIDs.
- Make a DID Management default component that is capable of manage (search, create, update, delete) DIDs and is components in the database.

Then make this component available within PrismAgent.