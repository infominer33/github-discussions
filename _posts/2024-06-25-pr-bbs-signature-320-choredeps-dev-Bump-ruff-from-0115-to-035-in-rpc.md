---
title: "bbs-signature/pr/320: chore(deps-dev): Bump ruff from 0.1.15 to 0.3.5 in /rpc"
date: 2024-06-25 15:38:48 +0000
author: dependabot
categories: ["DIF"]
tags: ["bbs-signature"]
permalink: /bbs-signature/pr/320/
comments_file: DIF-bbs-signature-pr-320_comments
excerpt: >
  ```suggestion              both of these extra connecting lines are styled as \"Domain Of\".  ```
---
Bumps [ruff](https://github.com/astral-sh/ruff) from 0.1.15 to 0.3.5.
<details>
<summary>Release notes</summary>
<p><em>Sourced from <a href="https://github.com/astral-sh/ruff/releases">ruff's releases</a>.</em></p>
<blockquote>
<h2>v0.3.5</h2>
<h2>Changes</h2>
<h3>Preview features</h3>
<ul>
<li>[<code>pylint</code>] Implement <code>modified-iterating-set</code> (<code>E4703</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10473">#10473</a>)</li>
<li>[<code>refurb</code>] Implement <code>for-loop-set-mutations</code> (<code>FURB142</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10583">#10583</a>)</li>
<li>[<code>refurb</code>] Implement <code>unnecessary-from-float</code> (<code>FURB164</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10647">#10647</a>)</li>
<li>[<code>refurb</code>] Implement <code>verbose-decimal-constructor</code> (<code>FURB157</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10533">#10533</a>)</li>
</ul>
<h3>Rule changes</h3>
<ul>
<li>[<code>flake8-comprehensions</code>] Handled special case for <code>C401</code> which also matches <code>C416</code> (<a href="https://redirect.github.com/astral-sh/ruff/pull/10596">#10596</a>)</li>
<li>[<code>flake8-pyi</code>] Mark <code>unaliased-collections-abc-set-import</code> fix as &quot;safe&quot; for more cases in stub files (<code>PYI025</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10547">#10547</a>)</li>
<li>[<code>numpy</code>] Add <code>row_stack</code> to NumPy 2.0 migration rule (<a href="https://redirect.github.com/astral-sh/ruff/pull/10646">#10646</a>)</li>
<li>[<code>pycodestyle</code>] Allow cell magics before an import (<code>E402</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10545">#10545</a>)</li>
<li>[<code>pycodestyle</code>] Avoid blank line rules for the first logical line in cell (<a href="https://redirect.github.com/astral-sh/ruff/pull/10291">#10291</a>)</li>
</ul>
<h3>Configuration</h3>
<ul>
<li>Respected nested namespace packages (<a href="https://redirect.github.com/astral-sh/ruff/pull/10541">#10541</a>)</li>
<li>[<code>flake8-boolean-trap</code>] Add setting for user defined allowed boolean trap (<a href="https://redirect.github.com/astral-sh/ruff/pull/10531">#10531</a>)</li>
</ul>
<h3>Bug fixes</h3>
<ul>
<li>Correctly handle references in <code>__all__</code> definitions when renaming symbols in autofixes (<a href="https://redirect.github.com/astral-sh/ruff/pull/10527">#10527</a>)</li>
<li>Track ranges of names inside <code>__all__</code> definitions (<a href="https://redirect.github.com/astral-sh/ruff/pull/10525">#10525</a>)</li>
<li>[<code>flake8-bugbear</code>] Avoid false positive for usage after <code>continue</code> (<code>B031</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10539">#10539</a>)</li>
<li>[<code>flake8-copyright</code>] Accept commas in default copyright pattern (<a href="https://redirect.github.com/astral-sh/ruff/pull/9498">#9498</a>)</li>
<li>[<code>flake8-datetimez</code>] Allow f-strings with <code>%z</code> for <code>DTZ007</code> (<a href="https://redirect.github.com/astral-sh/ruff/pull/10651">#10651</a>)</li>
<li>[<code>flake8-pytest-style</code>] Fix <code>PT014</code> autofix for last item in list (<a href="https://redirect.github.com/astral-sh/ruff/pull/10532">#10532</a>)</li>
<li>[<code>flake8-quotes</code>] Ignore <code>Q000</code>, <code>Q001</code> when string is inside forward ref (<a href="https://redirect.github.com/astral-sh/ruff/pull/10585">#10585</a>)</li>
<li>[<code>isort</code>] Always place non-relative imports after relative imports (<a href="https://redirect.github.com/astral-sh/ruff/pull/10669">#10669</a>)</li>
<li>[<code>isort</code>] Respect Unicode characters in import sorting (<a href="https://redirect.github.com/astral-sh/ruff/pull/10529">#10529</a>)</li>
<li>[<code>pyflakes</code>] Fix F821 false negatives when <code>from __future__ import annotations</code> is active (attempt 2) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10524">#10524</a>)</li>
<li>[<code>pyflakes</code>] Make <code>unnecessary-lambda</code> an always-unsafe fix (<a href="https://redirect.github.com/astral-sh/ruff/pull/10668">#10668</a>)</li>
<li>[<code>pylint</code>] Fixed false-positive on the rule <code>PLW1641</code> (<code>eq-without-hash</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10566">#10566</a>)</li>
<li>[<code>ruff</code>] Fix panic in unused <code># noqa</code> removal with multi-byte space (<code>RUF100</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10682">#10682</a>)</li>
</ul>
<h3>Documentation</h3>
<ul>
<li>Add PR title format to <code>CONTRIBUTING.md</code> (<a href="https://redirect.github.com/astral-sh/ruff/pull/10665">#10665</a>)</li>
<li>Fix list markup to include blank lines required (<a href="https://redirect.github.com/astral-sh/ruff/pull/10591">#10591</a>)</li>
<li>Put <code>flake8-logging</code> next to the other flake8 plugins in registry (<a href="https://redirect.github.com/astral-sh/ruff/pull/10587">#10587</a>)</li>
<li>[<code>flake8-bandit</code>] Update warning message for rule <code>S305</code> to address insecure block cipher mode use (<a href="https://redirect.github.com/astral-sh/ruff/pull/10602">#10602</a>)</li>
<li>[<code>flake8-bugbear</code>] Document use of anonymous assignment in <code>useless-expression</code> (<a href="https://redirect.github.com/astral-sh/ruff/pull/10551">#10551</a>)</li>
<li>[<code>flake8-datetimez</code>] Clarify error messages and docs for <code>DTZ</code> rules (<a href="https://redirect.github.com/astral-sh/ruff/pull/10621">#10621</a>)</li>
<li>[<code>pycodestyle</code>] Use same before vs. after numbers for <code>space-around-operator</code> (<a href="https://redirect.github.com/astral-sh/ruff/pull/10640">#10640</a>)</li>
<li>[<code>ruff</code>] Change <code>quadratic-list-summation</code> docs to use <code>iadd</code> consistently (<a href="https://redirect.github.com/astral-sh/ruff/pull/10666">#10666</a>)</li>
</ul>
<!-- raw HTML omitted -->
</blockquote>
<p>... (truncated)</p>
</details>
<details>
<summary>Changelog</summary>
<p><em>Sourced from <a href="https://github.com/astral-sh/ruff/blob/main/CHANGELOG.md">ruff's changelog</a>.</em></p>
<blockquote>
<h2>0.3.5</h2>
<h3>Preview features</h3>
<ul>
<li>[<code>pylint</code>] Implement <code>modified-iterating-set</code> (<code>E4703</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10473">#10473</a>)</li>
<li>[<code>refurb</code>] Implement <code>for-loop-set-mutations</code> (<code>FURB142</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10583">#10583</a>)</li>
<li>[<code>refurb</code>] Implement <code>unnecessary-from-float</code> (<code>FURB164</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10647">#10647</a>)</li>
<li>[<code>refurb</code>] Implement <code>verbose-decimal-constructor</code> (<code>FURB157</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10533">#10533</a>)</li>
</ul>
<h3>Rule changes</h3>
<ul>
<li>[<code>flake8-comprehensions</code>] Handled special case for <code>C401</code> which also matches <code>C416</code> (<a href="https://redirect.github.com/astral-sh/ruff/pull/10596">#10596</a>)</li>
<li>[<code>flake8-pyi</code>] Mark <code>unaliased-collections-abc-set-import</code> fix as &quot;safe&quot; for more cases in stub files (<code>PYI025</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10547">#10547</a>)</li>
<li>[<code>numpy</code>] Add <code>row_stack</code> to NumPy 2.0 migration rule (<a href="https://redirect.github.com/astral-sh/ruff/pull/10646">#10646</a>)</li>
<li>[<code>pycodestyle</code>] Allow cell magics before an import (<code>E402</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10545">#10545</a>)</li>
<li>[<code>pycodestyle</code>] Avoid blank line rules for the first logical line in cell (<a href="https://redirect.github.com/astral-sh/ruff/pull/10291">#10291</a>)</li>
</ul>
<h3>Configuration</h3>
<ul>
<li>Respected nested namespace packages (<a href="https://redirect.github.com/astral-sh/ruff/pull/10541">#10541</a>)</li>
<li>[<code>flake8-boolean-trap</code>] Add setting for user defined allowed boolean trap (<a href="https://redirect.github.com/astral-sh/ruff/pull/10531">#10531</a>)</li>
</ul>
<h3>Bug fixes</h3>
<ul>
<li>Correctly handle references in <code>__all__</code> definitions when renaming symbols in autofixes (<a href="https://redirect.github.com/astral-sh/ruff/pull/10527">#10527</a>)</li>
<li>Track ranges of names inside <code>__all__</code> definitions (<a href="https://redirect.github.com/astral-sh/ruff/pull/10525">#10525</a>)</li>
<li>[<code>flake8-bugbear</code>] Avoid false positive for usage after <code>continue</code> (<code>B031</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10539">#10539</a>)</li>
<li>[<code>flake8-copyright</code>] Accept commas in default copyright pattern (<a href="https://redirect.github.com/astral-sh/ruff/pull/9498">#9498</a>)</li>
<li>[<code>flake8-datetimez</code>] Allow f-strings with <code>%z</code> for <code>DTZ007</code> (<a href="https://redirect.github.com/astral-sh/ruff/pull/10651">#10651</a>)</li>
<li>[<code>flake8-pytest-style</code>] Fix <code>PT014</code> autofix for last item in list (<a href="https://redirect.github.com/astral-sh/ruff/pull/10532">#10532</a>)</li>
<li>[<code>flake8-quotes</code>] Ignore <code>Q000</code>, <code>Q001</code> when string is inside forward ref (<a href="https://redirect.github.com/astral-sh/ruff/pull/10585">#10585</a>)</li>
<li>[<code>isort</code>] Always place non-relative imports after relative imports (<a href="https://redirect.github.com/astral-sh/ruff/pull/10669">#10669</a>)</li>
<li>[<code>isort</code>] Respect Unicode characters in import sorting (<a href="https://redirect.github.com/astral-sh/ruff/pull/10529">#10529</a>)</li>
<li>[<code>pyflakes</code>] Fix F821 false negatives when <code>from __future__ import annotations</code> is active (attempt 2) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10524">#10524</a>)</li>
<li>[<code>pyflakes</code>] Make <code>unnecessary-lambda</code> an always-unsafe fix (<a href="https://redirect.github.com/astral-sh/ruff/pull/10668">#10668</a>)</li>
<li>[<code>pylint</code>] Fixed false-positive on the rule <code>PLW1641</code> (<code>eq-without-hash</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10566">#10566</a>)</li>
<li>[<code>ruff</code>] Fix panic in unused <code># noqa</code> removal with multi-byte space (<code>RUF100</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10682">#10682</a>)</li>
</ul>
<h3>Documentation</h3>
<ul>
<li>Add PR title format to <code>CONTRIBUTING.md</code> (<a href="https://redirect.github.com/astral-sh/ruff/pull/10665">#10665</a>)</li>
<li>Fix list markup to include blank lines required (<a href="https://redirect.github.com/astral-sh/ruff/pull/10591">#10591</a>)</li>
<li>Put <code>flake8-logging</code> next to the other flake8 plugins in registry (<a href="https://redirect.github.com/astral-sh/ruff/pull/10587">#10587</a>)</li>
<li>[<code>flake8-bandit</code>] Update warning message for rule <code>S305</code> to address insecure block cipher mode use (<a href="https://redirect.github.com/astral-sh/ruff/pull/10602">#10602</a>)</li>
<li>[<code>flake8-bugbear</code>] Document use of anonymous assignment in <code>useless-expression</code> (<a href="https://redirect.github.com/astral-sh/ruff/pull/10551">#10551</a>)</li>
<li>[<code>flake8-datetimez</code>] Clarify error messages and docs for <code>DTZ</code> rules (<a href="https://redirect.github.com/astral-sh/ruff/pull/10621">#10621</a>)</li>
<li>[<code>pycodestyle</code>] Use same before vs. after numbers for <code>space-around-operator</code> (<a href="https://redirect.github.com/astral-sh/ruff/pull/10640">#10640</a>)</li>
<li>[<code>ruff</code>] Change <code>quadratic-list-summation</code> docs to use <code>iadd</code> consistently (<a href="https://redirect.github.com/astral-sh/ruff/pull/10666">#10666</a>)</li>
</ul>
<h2>0.3.4</h2>
<!-- raw HTML omitted -->
</blockquote>
<p>... (truncated)</p>
</details>
<details>
<summary>Commits</summary>
<ul>
<li><a href="https://github.com/astral-sh/ruff/commit/200ebeebdc8ab8ee14f56922e21b218f41a5a7e4"><code>200ebee</code></a> Bump version to v0.3.5 (<a href="https://redirect.github.com/astral-sh/ruff/issues/10717">#10717</a>)</li>
<li><a href="https://github.com/astral-sh/ruff/commit/23e8279093d8f891fc8bb59ebea2532649801ed3"><code>23e8279</code></a> chore(deps): update npm development dependencies (<a href="https://redirect.github.com/astral-sh/ruff/issues/10716">#10716</a>)</li>
<li><a href="https://github.com/astral-sh/ruff/commit/221b3236a8770e2f9a0c502290b78a5ec58698cc"><code>221b323</code></a> chore(deps): update strum to 0.26.0 (<a href="https://redirect.github.com/astral-sh/ruff/issues/10715">#10715</a>)</li>
<li><a href="https://github.com/astral-sh/ruff/commit/a0e15448488badd81b0924653c180cd18029b2c2"><code>a0e1544</code></a> chore(deps): update rust crate pep440_rs to 0.5.0 (<a href="https://redirect.github.com/astral-sh/ruff/issues/10703">#10703</a>)</li>
<li><a href="https://github.com/astral-sh/ruff/commit/2740fab7ad8963892d15581e624764c7a7894999"><code>2740fab</code></a> Renovate: group all <code>strum</code> dependencies together (<a href="https://redirect.github.com/astral-sh/ruff/issues/10714">#10714</a>)</li>
<li><a href="https://github.com/astral-sh/ruff/commit/7042b9b16dcb91ffa6a49bab6e8d43066131af2a"><code>7042b9b</code></a> fix(deps): update rust crate similar to v2.5.0 (<a href="https://redirect.github.com/astral-sh/ruff/issues/10711">#10711</a>)</li>
<li><a href="https://github.com/astral-sh/ruff/commit/4047d456b6e1b5bfd67cf81b921350e2f2989a6c"><code>4047d45</code></a> chore(deps): update rust crate insta to v1.38.0 (<a href="https://redirect.github.com/astral-sh/ruff/issues/10701">#10701</a>)</li>
<li><a href="https://github.com/astral-sh/ruff/commit/20d69ea504b95e4cd7751dbb5a17aa446721945d"><code>20d69ea</code></a> chore(deps): update npm development dependencies (<a href="https://redirect.github.com/astral-sh/ruff/issues/10697">#10697</a>)</li>
<li><a href="https://github.com/astral-sh/ruff/commit/d021cac0c9755e7f34ee3941c9a98aa7befa9750"><code>d021cac</code></a> chore(deps): update rust crate tracing-tree to 0.3.0 (<a href="https://redirect.github.com/astral-sh/ruff/issues/10709">#10709</a>)</li>
<li><a href="https://github.com/astral-sh/ruff/commit/46369d48fe1089d48e0590fcf6fb028218ab84b0"><code>46369d4</code></a> chore(deps): update rust crate uuid to v1.8.0 (<a href="https://redirect.github.com/astral-sh/ruff/issues/10710">#10710</a>)</li>
<li>Additional commits viewable in <a href="https://github.com/astral-sh/ruff/compare/v0.1.15...v0.3.5">compare view</a></li>
</ul>
</details>
<br />


[![Dependabot compatibility score](https://dependabot-badges.githubapp.com/badges/compatibility_score?dependency-name=ruff&package-manager=pip&previous-version=0.1.15&new-version=0.3.5)](https://docs.github.com/en/github/managing-security-vulnerabilities/about-dependabot-security-updates#about-compatibility-scores)

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