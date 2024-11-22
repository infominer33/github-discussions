---
title: "tswg-keri-specification/issue/178: dueling edits"
date: 2024-05-21 14:59:32 +0000
author: TallTed
categories: ["Hyperledger"]
tags: ["tswg-keri-specification"]
permalink: /tswg-keri-specification/issue/178/
comments_file: Hyperledger-tswg-keri-specification-issue-178_comments
---

[_https://github.com/trustoverip/tswg-keri-specification/issues/178_](https://github.com/trustoverip/tswg-keri-specification/issues/178)

https://github.com/w3c/vc-di-bbs/blob/3f3585f8ca3162e019890531b5d73058a3f8727e/index.html#L1475

The second `if` is unnecessary. Even better, replace the later `if the` with `its`.

To be explicit, change —
`If |proofConfig|.|created| is set and if the value is not a`
— to —
`If |proofConfig|.|created| is set and its value is not a`

There seem to be dueling PRs for this. It was [changed earlier today](https://github.com/w3c/vc-di-bbs/pull/175/files), but now it <strike>doesn't appear</strike> appears to have been <strike>(or was un-changed)</strike> un-changed.

If there are different opinions about this phrasing, I would like to get them hammered out, and a final PR made.