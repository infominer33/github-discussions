---
title: "dwn-user-guide/issue/3: Adding labels and triage process"
date: 2024-07-10 17:51:17 +0000
author: mkbreuningIOHK
categories: ["DIF"]
tags: ["dwn-user-guide"]
permalink: /dwn-user-guide/issue/3/
comments_file: DIF-dwn-user-guide-issue-3_comments
excerpt: >
  Potential additional attributes:
---
**Is your feature request related to a problem? Please describe.**
As the number of contributors is growing, the number of issues is growing. We need a triage process with a labelling system in place.

**Describe the solution you'd like**
Labels to be added in contributing.md (or another file that will be referred in contributing triage part) in Identus repo.
Each label should have a prefix: for example:
- Type: bug, docs, enhancement, support, research, maintenance, chore, ci, refactor, perf, test 
- Priority: critical, major, normal, minor
- Component: cloud-agent, infrastructure, mediator, edge-agent-SDK-swift, edge-agent-SDK-KMP, edge-agent-SDK-TS, node, VDR, ... 
- Team: marketing, product, engineering, management, dev-ops, security
- Triage: needs-repro, needs-fix, stale, good-first-issue/up-for-graps, help-wanted, question/query, tech-debt
- Closed: out-of-scope, can’t-repro, duplicate, won’t-fix, design-limitation
- Status: new, ready, in-review, in-progress, fixed, qa-ready, qa-progress, qa-support (to indicate QA team needs support), stale, done/closed/terminated

Colors for labels should follow a rule to be described.
Each label should have a description associated to it.

All Identus repos will use the same labels.
Triage process needs to be written down: Have a look at [Identus Technical Charter](https://docs.google.com/document/d/1FmuBuSz79Yvnv87HZLhhMEMp-VrztuIHyiaMgoIKZE8/edit) as reference first.

**Describe alternatives you've considered**
We need to check if the status are labels or customised fields.
Best practices to be looked at as well so the solution is practical.

**Additional context**
The triage should be efficient and regularly done (recommendation is every 2 days) and it should be linked closely to the release process and cadence.
Follow: https://docs.github.com/en/issues/using-labels-and-milestones-to-track-work/managing-labels
Use [Conventional commit](https://www.conventionalcommits.org/en/v1.0.0/) to match some labels 