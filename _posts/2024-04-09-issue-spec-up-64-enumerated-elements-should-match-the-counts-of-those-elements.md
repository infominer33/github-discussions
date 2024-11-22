---
title: "spec-up/issue/64: enumerated elements should match the counts of those elements"
date: 2024-04-09 05:47:46 +0000
author: TallTed
categories: ["DIF"]
tags: ["spec-up"]
permalink: /spec-up/issue/64/
comments_file: DIF-spec-up-issue-64_comments
---

[_https://github.com/decentralized-identity/spec-up/issues/64_](https://github.com/decentralized-identity/spec-up/issues/64)

_Originally posted by @TallTed in https://github.com/w3c/vc-di-bbs-test-suite/pull/63#discussion_r1809211211_

> The first paragraph of [3.3.7 parseDerivedProofValue](https://w3c.github.io/vc-di-bbs/#parsederivedproofvalue) —
>
>> A single derived proof value object is produced as output, which contains a set of six or seven elements, having the names "bbsProof", "labelMap", "mandatoryIndexes", "selectiveIndexes", "presentationHeader", "featureOption", and, depending on the value of the featureOption parameter, "pseudonym" and/or "lengthBBSMessages".
>
>— is internally inconsistent (the set may have six, seven, or eight elements) and it disagrees with the last paragraph of that algorithm (again, should say "six, seven, or eight elements" including "featureOption", "pseudonym" and/or "lengthBBSMessages") —
>
>> Return derived proof value as an object with properties set to the five, six, or seven elements, using the names "bbsProof", "labelMap", "mandatoryIndexes", "selectiveIndexes", "presentationHeader", and optional "pseudonym" and/or "lengthBBSMessages", respectively. In addition, add featureOption and its value to the object.
>
> These should be brought into agreement. Whatever the result is, it should then be applied to this part of the test suite.
