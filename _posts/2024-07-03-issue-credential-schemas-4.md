---
title: "Add the identus release process"
date: 2024-07-03 23:27:23 +0000
author: mkbreuningIOHK
excerpt: >
  (Answering procedural questions as ED of DIF)
  This may introduce more complexity than needed, but it is possible to dedicate a small amount of time to proposing this at a future meeting for consideration by the WG and its chairs.
  
  My recommendation is that we hold off on this discussion until we are closer to determining which methods to focus on.
categories: decentralized-identity
tags: credential-schemas
comments_file: credential-schemas-issue-4_comments
permalink: /credential-schemas/4/
url: https://github.com/decentralized-identity/credential-schemas/issues/4
last_modified_at: 2024-11-25 22:43:50 +0000
---


**URL:** https://github.com/decentralized-identity/credential-schemas/issues/4

**Is your feature request related to a problem? Please describe.**
Identus is an eco-system and the release process should be described in this repository. Explaining who and what steps are being followed.
See ATL-7060 as well.

**Describe the solution you'd like**
Make a release vx.y:
- Go to Identus repo [hyperledger/identus](https://github.com/hyperledger/identus/) 
- Check the latest release version; it should be Identus va.b format. E.g Identus v2.12.
- Click on `Release` and `Draft a new release` button
   - In `Choose a tag` button, create the tag vx.y
   - Target = `main`
   - Previous tag `Auto`
- Click on `Generate change log`: this will generate the log for this repository only, which should be reviewed.
- Fill the release note in this change log, 
   - Copy the template (from the previous release if a template file is not existing yet)
   - For each component, add the change log according to each component (it should be already available from the component release).
   - Select `Set as a pre-release` and click on `Save Draft`
- Ask component owner to review: this is the critical step. The release owner should get an approval from each of the component: Cloud Agent, Edge Agent SDK Swift, KMP, TS, Mediator, Node, Docs.

*Note: This is not that convenient as having a PR where all can contribute: see alternatives considered*

- Ask QA team to validate the release by confirming there is no regression and critical bugs have been fixed.
- Once all component owners have accepted (with a check in the release note? TBC)), publish the release by editing it and unselect `Set as a pre-release` and click on `Publish release` button: the release `Identus vx.y` should be seen as the `latest`; if not, fix it.

**Describe alternatives you've considered**
- Previously, we have a file and a PR was submitted for review. See [atala-releases](https://github.com/input-output-hk/atala-releases/tree/master/Atala%20PRISM). 
- We should have a nice way to get the feedback from the component owners, maybe with a checkbox in the release.
Or a PR can be actually raise, with the checkbox that all the component owners have reviewed. Only then, the release is accepted. We shall have also the QA team to validate the eco-system.
- Using [automated release](https://docs.github.com/en/repositories/releasing-projects-on-github/automatically-generated-release-notes) would be a nice follow-up iteration. 

**Additional context**
Until Identus v2.12, the release was done as a PR in another repository: https://github.com/input-output-hk/atala-releases
