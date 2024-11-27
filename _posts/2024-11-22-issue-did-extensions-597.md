---
title: "SUPER/META PROPOSAL: Authentication of unique DID Method names: allowing for multiple approaches"
date: 2024-11-22 15:09:36 +0000
author: mwherman2000
excerpt: >
  Please don't use pictures of text when the text itself could be used.
categories: w3c
tags: did-extensions
comments_file: did-extensions-issue-597_comments
permalink: /did-extensions/597/
url: https://github.com/w3c/did-extensions/issues/597
last_modified_at: 2024-11-26 15:01:00 +0000
---


**URL:** https://github.com/w3c/did-extensions/issues/597

@msporny proposed restricted approach here: https://github.com/w3c/did-extensions/issues/595

In this Super/Meta Proposal, I want to suggest that the DID method registration section in the spec be modified to support more than one _Authentication of unique DID Method names_ approach that covers the following objectives:
1. Removes the burden from the reviewers
2. Removes the W3C from having to arbitrate DID method uniqueness issues
3. Produces a tangible result in terms of authenticating the uniqueness of new DID Method registration applications

The idea is to support, in the specification, more than one _trivially easy-to-access_ _Authentication of unique DID Method names_  approach - with the goal of giving registrants/controllers at least a couple choices that they can choose from based on time, effort, and cost.  For example, tradmarking is costly especially for registrants who do not have _in-house legal council_ - more cost effective solution(s) are also needed.  The wording of the specification cannot be prejudiced for or against any registrant.  In addition, a DID Method name may not be trademarkable: https://github.com/w3c/did-extensions/issues/595#issuecomment-2494098759

So what's on the table in terms of approaches (in order of strength: _effectiveness, cost, time, and effort_):
1. DNS Registration: Leveraging what is already available using Internet Doman Name System (DNS) domain name registration. Examples of such an approach can be found in https://github.com/w3c/did-extensions/issues/590
2. Registered trademarks per the concepts outlined here: https://github.com/w3c/did-extensions/issues/595
3. Unregistered trademarks
4. No authentication of uniqueness supplied in the application

NOTE: The implication of point 4 is that we add a field to the DID Method Name registration file to specify the registrant's _Authentication of unique DID Method names_ approach/evidence.  This can be a simple text field with a link to the domain registration, a trademark statement, etc.  An empty or missing field would default to class 4: No authentication of uniqueness provided.  This field can also be used to ajudicate new applications that have or claim to have a stronger authentication.

Q: any additional _Authentication of unique DID Method names_ approaches that would be simple in terms of effort, time and cost for the registrant and as well the reviewers and the W3C?

Other thoughts?
