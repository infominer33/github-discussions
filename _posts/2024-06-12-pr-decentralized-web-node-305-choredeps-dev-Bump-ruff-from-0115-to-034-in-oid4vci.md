---
title: "decentralized-web-node/pr/305: chore(deps-dev): Bump ruff from 0.1.15 to 0.3.4 in /oid4vci"
date: 2024-06-12 15:21:27 +0000
author: dependabot
categories: ["DIF"]
tags: ["decentralized-web-node"]
permalink: /decentralized-web-node/pr/305/
comments_file: DIF-decentralized-web-node-pr-305_comments
excerpt: >
  Propose to replace it from  'https://didcomm.org/issue-credential/3.0/issue-credential'  to  SDK.ProtocolType.DidcommIssueCredential
---
Bumps [ruff](https://github.com/astral-sh/ruff) from 0.1.15 to 0.3.4.
<details>
<summary>Release notes</summary>
<p><em>Sourced from <a href="https://github.com/astral-sh/ruff/releases">ruff's releases</a>.</em></p>
<blockquote>
<h2>v0.3.3</h2>
<h2>Changes</h2>
<h3>Preview features</h3>
<ul>
<li>[<code>flake8-bandit</code>]: Implement <code>S610</code> rule (<a href="https://redirect.github.com/astral-sh/ruff/pull/10316">#10316</a>)</li>
<li>[<code>pycodestyle</code>] Implement <code>blank-line-at-end-of-file</code> (<code>W391</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10243">#10243</a>)</li>
<li>[<code>pycodestyle</code>] Implement <code>redundant-backslash</code> (<code>E502</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10292">#10292</a>)</li>
<li>[<code>pylint</code>] - implement <code>redeclared-assigned-name</code> (<code>W0128</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/9268">#9268</a>)</li>
</ul>
<h3>Rule changes</h3>
<ul>
<li>[<code>flake8_comprehensions</code>] Handled special case for <code>C400</code> which also matches <code>C416</code> (<a href="https://redirect.github.com/astral-sh/ruff/pull/10419">#10419</a>)</li>
<li>[<code>flake8-bandit</code>] Implement upstream updates for <code>S311</code>, <code>S324</code> and <code>S605</code> (<a href="https://redirect.github.com/astral-sh/ruff/pull/10313">#10313</a>)</li>
<li>[<code>pyflakes</code>] Remove <code>F401</code> fix for <code>__init__</code> imports by default and allow opt-in to unsafe fix (<a href="https://redirect.github.com/astral-sh/ruff/pull/10365">#10365</a>)</li>
<li>[<code>pylint</code>] Implement <code>invalid-bool-return-type</code> (<code>E304</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10377">#10377</a>)</li>
<li>[<code>pylint</code>] Include builtin warnings in useless-exception-statement (<code>PLW0133</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10394">#10394</a>)</li>
</ul>
<h3>CLI</h3>
<ul>
<li>Add message on success to <code>ruff check</code> (<a href="https://redirect.github.com/astral-sh/ruff/pull/8631">#8631</a>)</li>
</ul>
<h3>Bug fixes</h3>
<ul>
<li>[<code>PIE970</code>] Allow trailing ellipsis in <code>typing.TYPE_CHECKING</code> (<a href="https://redirect.github.com/astral-sh/ruff/pull/10413">#10413</a>)</li>
<li>Avoid <code>TRIO115</code> if the argument is a variable (<a href="https://redirect.github.com/astral-sh/ruff/pull/10376">#10376</a>)</li>
<li>[<code>F811</code>] Avoid removing shadowed imports that point to different symbols (<a href="https://redirect.github.com/astral-sh/ruff/pull/10387">#10387</a>)</li>
<li>Fix <code>F821</code> and <code>F822</code> false positives in <code>.pyi</code> files (<a href="https://redirect.github.com/astral-sh/ruff/pull/10341">#10341</a>)</li>
<li>Fix <code>F821</code> false negatives in <code>.py</code> files when <code>from __future__ import annotations</code> is active (<a href="https://redirect.github.com/astral-sh/ruff/pull/10362">#10362</a>)</li>
<li>Fix case where <code>Indexer</code> fails to identify continuation preceded by newline <a href="https://redirect.github.com/astral-sh/ruff/issues/10351">#10351</a> (<a href="https://redirect.github.com/astral-sh/ruff/pull/10354">#10354</a>)</li>
<li>Sort hash maps in <code>Settings</code> display (<a href="https://redirect.github.com/astral-sh/ruff/pull/10370">#10370</a>)</li>
<li>Track conditional deletions in the semantic model (<a href="https://redirect.github.com/astral-sh/ruff/pull/10415">#10415</a>)</li>
<li>[<code>C413</code>] Wrap expressions in parentheses when negating (<a href="https://redirect.github.com/astral-sh/ruff/pull/10346">#10346</a>)</li>
<li>[<code>pycodestyle</code>] Do not ignore lines before the first logical line in blank lines rules. (<a href="https://redirect.github.com/astral-sh/ruff/pull/10382">#10382</a>)</li>
<li>[<code>pycodestyle</code>] Do not trigger <code>E225</code> and <code>E275</code> when the next token is a ')' (<a href="https://redirect.github.com/astral-sh/ruff/pull/10315">#10315</a>)</li>
<li>[<code>pylint</code>] Avoid false-positive slot non-assignment for <code>__dict__</code> (<code>PLE0237</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10348">#10348</a>)</li>
<li>Gate f-string struct size test for Rustc &lt; 1.76 (<a href="https://redirect.github.com/astral-sh/ruff/pull/10371">#10371</a>)</li>
</ul>
<h3>Documentation</h3>
<ul>
<li>Use <code>ruff.toml</code> format in README (<a href="https://redirect.github.com/astral-sh/ruff/pull/10393">#10393</a>)</li>
<li>[<code>RUF008</code>] Make it clearer that a mutable default in a dataclass is only valid if it is typed as a ClassVar (<a href="https://redirect.github.com/astral-sh/ruff/pull/10395">#10395</a>)</li>
<li>[<code>pylint</code>] Extend docs and test in <code>invalid-str-return-type</code> (<code>E307</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10400">#10400</a>)</li>
<li>Remove <code>.</code> from <code>check</code> and <code>format</code> commands (<a href="https://redirect.github.com/astral-sh/ruff/pull/10217">#10217</a>)</li>
</ul>
<h2>Contributors</h2>
<ul>
<li><a href="https://github.com/AlexWaygood"><code>@​AlexWaygood</code></a></li>
<li><a href="https://github.com/Guilherme-Vasconcelos"><code>@​Guilherme-Vasconcelos</code></a></li>
<li><a href="https://github.com/KotlinIsland"><code>@​KotlinIsland</code></a></li>
<li><a href="https://github.com/anuraaga"><code>@​anuraaga</code></a></li>
</ul>
<!-- raw HTML omitted -->
</blockquote>
<p>... (truncated)</p>
</details>
<details>
<summary>Changelog</summary>
<p><em>Sourced from <a href="https://github.com/astral-sh/ruff/blob/main/CHANGELOG.md">ruff's changelog</a>.</em></p>
<blockquote>
<h2>0.3.4</h2>
<h3>Preview features</h3>
<ul>
<li>[<code>flake8-simplify</code>] Detect implicit <code>else</code> cases in <code>needless-bool</code> (<code>SIM103</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10414">#10414</a>)</li>
<li>[<code>pylint</code>] Implement <code>nan-comparison</code> (<code>PLW0117</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10401">#10401</a>)</li>
<li>[<code>pylint</code>] Implement <code>nonlocal-and-global</code> (<code>E115</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10407">#10407</a>)</li>
<li>[<code>pylint</code>] Implement <code>singledispatchmethod-function</code> (<code>PLE5120</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10428">#10428</a>)</li>
<li>[<code>refurb</code>] Implement <code>list-reverse-copy</code> (<code>FURB187</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10212">#10212</a>)</li>
</ul>
<h3>Rule changes</h3>
<ul>
<li>[<code>flake8-pytest-style</code>] Add automatic fix for <code>pytest-parametrize-values-wrong-type</code> (<code>PT007</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10461">#10461</a>)</li>
<li>[<code>pycodestyle</code>] Allow SPDX license headers to exceed the line length (<code>E501</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10481">#10481</a>)</li>
</ul>
<h3>Formatter</h3>
<ul>
<li>Fix unstable formatting for trailing subscript end-of-line comment (<a href="https://redirect.github.com/astral-sh/ruff/pull/10492">#10492</a>)</li>
</ul>
<h3>Bug fixes</h3>
<ul>
<li>Avoid code comment detection in PEP 723 script tags (<a href="https://redirect.github.com/astral-sh/ruff/pull/10464">#10464</a>)</li>
<li>Avoid incorrect tuple transformation in single-element case (<code>C409</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10491">#10491</a>)</li>
<li>Bug fix: Prevent fully defined links <a href="https://github.com/astral-sh/ruff/blob/main/link"><code>name</code></a> from being reformatted (<a href="https://redirect.github.com/astral-sh/ruff/pull/10442">#10442</a>)</li>
<li>Consider raw source code for <code>W605</code> (<a href="https://redirect.github.com/astral-sh/ruff/pull/10480">#10480</a>)</li>
<li>Docs: Link inline settings when not part of options section (<a href="https://redirect.github.com/astral-sh/ruff/pull/10499">#10499</a>)</li>
<li>Don't treat annotations as redefinitions in <code>.pyi</code> files (<a href="https://redirect.github.com/astral-sh/ruff/pull/10512">#10512</a>)</li>
<li>Fix <code>E231</code> bug: Inconsistent catch compared to pycodestyle, such as when dict nested in list (<a href="https://redirect.github.com/astral-sh/ruff/pull/10469">#10469</a>)</li>
<li>Fix pylint upstream categories not showing in docs (<a href="https://redirect.github.com/astral-sh/ruff/pull/10441">#10441</a>)</li>
<li>Add missing <code>Options</code> references to blank line docs (<a href="https://redirect.github.com/astral-sh/ruff/pull/10498">#10498</a>)</li>
<li>'Revert &quot;F821: Fix false negatives in .py files when <code>from __future__ import annotations</code> is active (<a href="https://redirect.github.com/astral-sh/ruff/issues/10362">#10362</a>)&quot;' (<a href="https://redirect.github.com/astral-sh/ruff/pull/10513">#10513</a>)</li>
<li>Apply NFKC normalization to unicode identifiers in the lexer (<a href="https://redirect.github.com/astral-sh/ruff/pull/10412">#10412</a>)</li>
<li>Avoid failures due to non-deterministic binding ordering (<a href="https://redirect.github.com/astral-sh/ruff/pull/10478">#10478</a>)</li>
<li>[<code>flake8-bugbear</code>] Allow tuples of exceptions (<code>B030</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10437">#10437</a>)</li>
<li>[<code>flake8-quotes</code>] Avoid syntax errors due to invalid quotes (<code>Q000, Q002</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10199">#10199</a>)</li>
</ul>
<h2>0.3.3</h2>
<h3>Preview features</h3>
<ul>
<li>[<code>flake8-bandit</code>]: Implement <code>S610</code> rule (<a href="https://redirect.github.com/astral-sh/ruff/pull/10316">#10316</a>)</li>
<li>[<code>pycodestyle</code>] Implement <code>blank-line-at-end-of-file</code> (<code>W391</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10243">#10243</a>)</li>
<li>[<code>pycodestyle</code>] Implement <code>redundant-backslash</code> (<code>E502</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10292">#10292</a>)</li>
<li>[<code>pylint</code>] - implement <code>redeclared-assigned-name</code> (<code>W0128</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/9268">#9268</a>)</li>
</ul>
<h3>Rule changes</h3>
<ul>
<li>[<code>flake8_comprehensions</code>] Handled special case for <code>C400</code> which also matches <code>C416</code> (<a href="https://redirect.github.com/astral-sh/ruff/pull/10419">#10419</a>)</li>
<li>[<code>flake8-bandit</code>] Implement upstream updates for <code>S311</code>, <code>S324</code> and <code>S605</code> (<a href="https://redirect.github.com/astral-sh/ruff/pull/10313">#10313</a>)</li>
<li>[<code>pyflakes</code>] Remove <code>F401</code> fix for <code>__init__</code> imports by default and allow opt-in to unsafe fix (<a href="https://redirect.github.com/astral-sh/ruff/pull/10365">#10365</a>)</li>
</ul>
<!-- raw HTML omitted -->
</blockquote>
<p>... (truncated)</p>
</details>
<details>
<summary>Commits</summary>
<ul>
<li><a href="https://github.com/astral-sh/ruff/commit/5062572aca9413670aafd018cb65037bcb4d6acb"><code>5062572</code></a> Bump version to v0.3.4 (<a href="https://redirect.github.com/astral-sh/ruff/issues/10515">#10515</a>)</li>
<li><a href="https://github.com/astral-sh/ruff/commit/dc6f6398e737f4496dfaa870b1dc07ee1ec85617"><code>dc6f639</code></a> Rename <code>list-reassign-reversed</code> to <code>list-reverse-copy</code> (<a href="https://redirect.github.com/astral-sh/ruff/issues/10514">#10514</a>)</li>
<li><a href="https://github.com/astral-sh/ruff/commit/01fe2686124fb4b0a94184e17e7b246fa7e5b689"><code>01fe268</code></a> [<code>refurb</code>] Implement <code>list_assign_reversed</code> lint (FURB187) (<a href="https://redirect.github.com/astral-sh/ruff/issues/10212">#10212</a>)</li>
<li><a href="https://github.com/astral-sh/ruff/commit/c62184d05781327ddde1c0b142790d351cf666e6"><code>c62184d</code></a> 'Revert &quot;F821: Fix false negatives in .py files when `from <strong>future</strong> import ...</li>
<li><a href="https://github.com/astral-sh/ruff/commit/9b3c73253809f10f6f6522a487eb393fc6477d9c"><code>9b3c732</code></a> Docs: Link inline settings when not part of options section (<a href="https://redirect.github.com/astral-sh/ruff/issues/10499">#10499</a>)</li>
<li><a href="https://github.com/astral-sh/ruff/commit/caa14508959781b9220f5c9f83c4e0a4c586ce0c"><code>caa1450</code></a> Don't treat annotations as redefinitions in <code>.pyi</code> files (<a href="https://redirect.github.com/astral-sh/ruff/issues/10512">#10512</a>)</li>
<li><a href="https://github.com/astral-sh/ruff/commit/60fd98eb2fe425eca4b89268dd608f4e1cc21b74"><code>60fd98e</code></a> Update Rust to v1.77 (<a href="https://redirect.github.com/astral-sh/ruff/issues/10510">#10510</a>)</li>
<li><a href="https://github.com/astral-sh/ruff/commit/ac150b9314c0359c499aff103a99007807f9f854"><code>ac150b9</code></a> Spruce up docs for flake8-pyi rules (part 2) (<a href="https://redirect.github.com/astral-sh/ruff/issues/10494">#10494</a>)</li>
<li><a href="https://github.com/astral-sh/ruff/commit/d9ac170eb45660b8ac3e61a81b168202b76f1582"><code>d9ac170</code></a> Fix <code>E231</code> bug: Inconsistent catch compared to pycodestyle, such as when dict...</li>
<li><a href="https://github.com/astral-sh/ruff/commit/c5ea4209bba318001e6c22ca84c75097977de305"><code>c5ea420</code></a> chore: remove repetitive words (<a href="https://redirect.github.com/astral-sh/ruff/issues/10502">#10502</a>)</li>
<li>Additional commits viewable in <a href="https://github.com/astral-sh/ruff/compare/v0.1.15...v0.3.4">compare view</a></li>
</ul>
</details>
<br />


[![Dependabot compatibility score](https://dependabot-badges.githubapp.com/badges/compatibility_score?dependency-name=ruff&package-manager=pip&previous-version=0.1.15&new-version=0.3.4)](https://docs.github.com/en/github/managing-security-vulnerabilities/about-dependabot-security-updates#about-compatibility-scores)

Dependabot will resolve any conflicts with this PR as long as you don't alter it yourself. You can also trigger a rebase manually by commenting `@dependabot rebase`.

[//]: # (dependabot-automerge-start)
[//]: # (dependabot-automerge-end)

---

<details>
<summary>Dependabot commands and options</summary>
<br />

You can trigger Dependabot actions by commenting on this PR:
- `@dependabot rebase` will rebase this PR
- `@dependabot recreate` will recreate this PR, overwriting any edits that have been made to it
- `@dependabot merge` will merge this PR after your CI passes on it
- `@dependabot squash and merge` will squash and merge this PR after your CI passes on it
- `@dependabot cancel merge` will cancel a previously requested merge and block automerging
- `@dependabot reopen` will reopen this PR if it is closed
- `@dependabot close` will close this PR and stop Dependabot recreating it. You can achieve the same result by closing it manually
- `@dependabot show <dependency name> ignore conditions` will show all of the ignore conditions of the specified dependency
- `@dependabot ignore this major version` will close this PR and stop Dependabot creating any more for this major version (unless you reopen the PR or upgrade to it yourself)
- `@dependabot ignore this minor version` will close this PR and stop Dependabot creating any more for this minor version (unless you reopen the PR or upgrade to it yourself)
- `@dependabot ignore this dependency` will close this PR and stop Dependabot creating any more for this dependency (unless you reopen the PR or upgrade to it yourself)


</details>