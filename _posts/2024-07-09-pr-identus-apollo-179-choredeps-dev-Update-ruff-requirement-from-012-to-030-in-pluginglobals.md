---
title: "identus-apollo/pr/179: chore(deps-dev): Update ruff requirement from ^0.1.2 to ^0.3.0 in /plugin_globals"
date: 2024-07-09 09:58:01 +0000
author: dependabot
categories: ["Hyperledger"]
tags: ["identus-apollo"]
permalink: /identus-apollo/pr/179/
comments_file: Hyperledger-identus-apollo-pr-179_comments
excerpt: >
  ```suggestion  <a data-cite=\"?CONTROLLER-DOCUMENT#multibase-0\">Multibase-decode</a> algorithm on the  ```
---
Updates the requirements on [ruff](https://github.com/astral-sh/ruff) to permit the latest version.
<details>
<summary>Release notes</summary>
<p><em>Sourced from <a href="https://github.com/astral-sh/ruff/releases">ruff's releases</a>.</em></p>
<blockquote>
<h2>v0.3.0</h2>
<p>This release introduces the new Ruff formatter 2024.2 style and adds a new lint rule to
detect invalid formatter suppression comments.</p>
<h2>Changes</h2>
<h3>Preview features</h3>
<ul>
<li>[<code>flake8-bandit</code>] Remove suspicious-lxml-import (<code>S410</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10154">#10154</a>)</li>
<li>[<code>pycodestyle</code>] Allow <code>os.environ</code> modifications between imports (<code>E402</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10066">#10066</a>)</li>
<li>[<code>pycodestyle</code>] Don't warn about a single whitespace character before a comma in a tuple (<code>E203</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10094">#10094</a>)</li>
</ul>
<h3>Rule changes</h3>
<ul>
<li>[<code>eradicate</code>] Detect commented out <code>case</code> statements (<code>ERA001</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10055">#10055</a>)</li>
<li>[<code>eradicate</code>] Detect single-line code for <code>try:</code>, <code>except:</code>, etc. (<code>ERA001</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10057">#10057</a>)</li>
<li>[<code>flake8-boolean-trap</code>] Allow boolean positionals in <code>__post_init__</code> (<a href="https://redirect.github.com/astral-sh/ruff/pull/10027">#10027</a>)</li>
<li>[<code>flake8-copyright</code>] Allow © in copyright notices (<a href="https://redirect.github.com/astral-sh/ruff/pull/10065">#10065</a>)</li>
<li>[<code>isort</code>]: Use one blank line after imports in typing stub files (<a href="https://redirect.github.com/astral-sh/ruff/pull/9971">#9971</a>)</li>
<li>[<code>pylint</code>] New Rule <code>dict-iter-missing-items</code> (<code>PLE1141</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/9845">#9845</a>)</li>
<li>[<code>pylint</code>] Ignore <code>sys.version</code> and <code>sys.platform</code> (<code>PLR1714</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10054">#10054</a>)</li>
<li>[<code>pyupgrade</code>] Detect literals with unary operators (<code>UP018</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10060">#10060</a>)</li>
<li>[<code>ruff</code>] Expand rule for <code>list(iterable).pop(0)</code> idiom (<code>RUF015</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10148">#10148</a>)</li>
</ul>
<h3>Formatter</h3>
<p>This release introduces the Ruff 2024.2 style, stabilizing the following changes:</p>
<ul>
<li>Prefer splitting the assignment's value over the target or type annotation (<a href="https://redirect.github.com/astral-sh/ruff/pull/8943">#8943</a>)</li>
<li>Remove blank lines before class docstrings (<a href="https://redirect.github.com/astral-sh/ruff/pull/9154">#9154</a>)</li>
<li>Wrap multiple context managers in <code>with</code> parentheses when targeting Python 3.9 or newer (<a href="https://redirect.github.com/astral-sh/ruff/pull/9222">#9222</a>)</li>
<li>Add a blank line after nested classes with a dummy body (<code>...</code>) in typing stub files (<a href="https://redirect.github.com/astral-sh/ruff/pull/9155">#9155</a>)</li>
<li>Reduce vertical spacing for classes and functions with a dummy (<code>...</code>) body (<a href="https://redirect.github.com/astral-sh/ruff/issues/7440">#7440</a>, <a href="https://redirect.github.com/astral-sh/ruff/pull/9240">#9240</a>)</li>
<li>Add a blank line after the module docstring (<a href="https://redirect.github.com/astral-sh/ruff/pull/8283">#8283</a>)</li>
<li>Parenthesize long type hints in assignments (<a href="https://redirect.github.com/astral-sh/ruff/pull/9210">#9210</a>)</li>
<li>Preserve indent for single multiline-string call-expressions (<a href="https://redirect.github.com/astral-sh/ruff/pull/9637">#9673</a>)</li>
<li>Normalize hex escape and unicode escape sequences (<a href="https://redirect.github.com/astral-sh/ruff/pull/9280">#9280</a>)</li>
<li>Format module docstrings (<a href="https://redirect.github.com/astral-sh/ruff/pull/9725">#9725</a>)</li>
</ul>
<h3>CLI</h3>
<ul>
<li>Explicitly disallow <code>extend</code> as part of a <code>--config</code> flag (<a href="https://redirect.github.com/astral-sh/ruff/pull/10135">#10135</a>)</li>
<li>Remove <code>build</code> from the default exclusion list (<a href="https://redirect.github.com/astral-sh/ruff/pull/10093">#10093</a>)</li>
<li>Deprecate <code>ruff &lt;path&gt;</code>, <code>ruff --explain</code>, <code>ruff --clean</code>, and <code>ruff --generate-shell-completion</code> in favor of <code>ruff check &lt;path&gt;</code>, <code>ruff rule</code>, <code>ruff clean</code>, and <code>ruff generate-shell-completion</code> (<a href="https://redirect.github.com/astral-sh/ruff/pull/10169">#10169</a>)</li>
<li>Remove the deprecated CLI option <code>--format</code> from <code>ruff rule</code> and <code>ruff linter</code> (<a href="https://redirect.github.com/astral-sh/ruff/pull/10170">#10170</a>)</li>
</ul>
<h3>Bug fixes</h3>
<ul>
<li>[<code>flake8-bugbear</code>] Avoid adding default initializers to stubs (<code>B006</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10152">#10152</a>)</li>
<li>[<code>flake8-type-checking</code>] Respect runtime-required decorators for function signatures (<a href="https://redirect.github.com/astral-sh/ruff/pull/10091">#10091</a>)</li>
</ul>
<!-- raw HTML omitted -->
</blockquote>
<p>... (truncated)</p>
</details>
<details>
<summary>Changelog</summary>
<p><em>Sourced from <a href="https://github.com/astral-sh/ruff/blob/main/CHANGELOG.md">ruff's changelog</a>.</em></p>
<blockquote>
<h2>0.3.0</h2>
<p>This release introduces the new Ruff formatter 2024.2 style and adds a new lint rule to
detect invalid formatter suppression comments.</p>
<h3>Preview features</h3>
<ul>
<li>[<code>flake8-bandit</code>] Remove suspicious-lxml-import (<code>S410</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10154">#10154</a>)</li>
<li>[<code>pycodestyle</code>] Allow <code>os.environ</code> modifications between imports (<code>E402</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10066">#10066</a>)</li>
<li>[<code>pycodestyle</code>] Don't warn about a single whitespace character before a comma in a tuple (<code>E203</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10094">#10094</a>)</li>
</ul>
<h3>Rule changes</h3>
<ul>
<li>[<code>eradicate</code>] Detect commented out <code>case</code> statements (<code>ERA001</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10055">#10055</a>)</li>
<li>[<code>eradicate</code>] Detect single-line code for <code>try:</code>, <code>except:</code>, etc. (<code>ERA001</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10057">#10057</a>)</li>
<li>[<code>flake8-boolean-trap</code>] Allow boolean positionals in <code>__post_init__</code> (<a href="https://redirect.github.com/astral-sh/ruff/pull/10027">#10027</a>)</li>
<li>[<code>flake8-copyright</code>] Allow © in copyright notices (<a href="https://redirect.github.com/astral-sh/ruff/pull/10065">#10065</a>)</li>
<li>[<code>isort</code>]: Use one blank line after imports in typing stub files (<a href="https://redirect.github.com/astral-sh/ruff/pull/9971">#9971</a>)</li>
<li>[<code>pylint</code>] New Rule <code>dict-iter-missing-items</code> (<code>PLE1141</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/9845">#9845</a>)</li>
<li>[<code>pylint</code>] Ignore <code>sys.version</code> and <code>sys.platform</code> (<code>PLR1714</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10054">#10054</a>)</li>
<li>[<code>pyupgrade</code>] Detect literals with unary operators (<code>UP018</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10060">#10060</a>)</li>
<li>[<code>ruff</code>] Expand rule for <code>list(iterable).pop(0)</code> idiom (<code>RUF015</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10148">#10148</a>)</li>
</ul>
<h3>Formatter</h3>
<p>This release introduces the Ruff 2024.2 style, stabilizing the following changes:</p>
<ul>
<li>Prefer splitting the assignment's value over the target or type annotation (<a href="https://redirect.github.com/astral-sh/ruff/pull/8943">#8943</a>)</li>
<li>Remove blank lines before class docstrings (<a href="https://redirect.github.com/astral-sh/ruff/pull/9154">#9154</a>)</li>
<li>Wrap multiple context managers in <code>with</code> parentheses when targeting Python 3.9 or newer (<a href="https://redirect.github.com/astral-sh/ruff/pull/9222">#9222</a>)</li>
<li>Add a blank line after nested classes with a dummy body (<code>...</code>) in typing stub files (<a href="https://redirect.github.com/astral-sh/ruff/pull/9155">#9155</a>)</li>
<li>Reduce vertical spacing for classes and functions with a dummy (<code>...</code>) body (<a href="https://redirect.github.com/astral-sh/ruff/issues/7440">#7440</a>, <a href="https://redirect.github.com/astral-sh/ruff/pull/9240">#9240</a>)</li>
<li>Add a blank line after the module docstring (<a href="https://redirect.github.com/astral-sh/ruff/pull/8283">#8283</a>)</li>
<li>Parenthesize long type hints in assignments (<a href="https://redirect.github.com/astral-sh/ruff/pull/9210">#9210</a>)</li>
<li>Preserve indent for single multiline-string call-expressions (<a href="https://redirect.github.com/astral-sh/ruff/pull/9637">#9673</a>)</li>
<li>Normalize hex escape and unicode escape sequences (<a href="https://redirect.github.com/astral-sh/ruff/pull/9280">#9280</a>)</li>
<li>Format module docstrings (<a href="https://redirect.github.com/astral-sh/ruff/pull/9725">#9725</a>)</li>
</ul>
<h3>CLI</h3>
<ul>
<li>Explicitly disallow <code>extend</code> as part of a <code>--config</code> flag (<a href="https://redirect.github.com/astral-sh/ruff/pull/10135">#10135</a>)</li>
<li>Remove <code>build</code> from the default exclusion list (<a href="https://redirect.github.com/astral-sh/ruff/pull/10093">#10093</a>)</li>
<li>Deprecate <code>ruff &lt;path&gt;</code>, <code>ruff --explain</code>, <code>ruff --clean</code>, and <code>ruff --generate-shell-completion</code> in favor of <code>ruff check &lt;path&gt;</code>, <code>ruff rule</code>, <code>ruff clean</code>, and <code>ruff generate-shell-completion</code> (<a href="https://redirect.github.com/astral-sh/ruff/pull/10169">#10169</a>)</li>
<li>Remove the deprecated CLI option <code>--format</code> from <code>ruff rule</code> and <code>ruff linter</code> (<a href="https://redirect.github.com/astral-sh/ruff/pull/10170">#10170</a>)</li>
</ul>
<h3>Bug fixes</h3>
<ul>
<li>[<code>flake8-bugbear</code>] Avoid adding default initializers to stubs (<code>B006</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10152">#10152</a>)</li>
<li>[<code>flake8-type-checking</code>] Respect runtime-required decorators for function signatures (<a href="https://redirect.github.com/astral-sh/ruff/pull/10091">#10091</a>)</li>
<li>[<code>pycodestyle</code>] Mark fixes overlapping with a multiline string as unsafe (<code>W293</code>) (<a href="https://redirect.github.com/astral-sh/ruff/pull/10049">#10049</a>)</li>
</ul>
<!-- raw HTML omitted -->
</blockquote>
<p>... (truncated)</p>
</details>
<details>
<summary>Commits</summary>
<ul>
<li><a href="https://github.com/astral-sh/ruff/commit/b53118ed0016ac37233d3dadbcea9ed3ac1f538e"><code>b53118e</code></a> Bump version to v0.3.0 (<a href="https://redirect.github.com/astral-sh/ruff/issues/10151">#10151</a>)</li>
<li><a href="https://github.com/astral-sh/ruff/commit/52f4c1e41be0ce09181c220b1e4918d5bb5ee596"><code>52f4c1e</code></a> Remove deprecated CLI option <code>--format</code> (<a href="https://redirect.github.com/astral-sh/ruff/issues/10170">#10170</a>)</li>
<li><a href="https://github.com/astral-sh/ruff/commit/eceffe74a06f0b1163491624c6c696ebdf3648e9"><code>eceffe7</code></a> Deprecate <code>ruff \&lt;path&gt;</code> <code>ruff --explain</code>, <code>ruff --clean</code> and `ruff --generate...</li>
<li><a href="https://github.com/astral-sh/ruff/commit/c73c497477f5abd0d4133c0508d233ebcd78aeba"><code>c73c497</code></a> [<code>pydocstyle</code>] Trim whitespace when removing blank lines after section (`D413...</li>
<li><a href="https://github.com/astral-sh/ruff/commit/c9c98c4fe350fc66d442737ac3b978387fb436e7"><code>c9c98c4</code></a> Fix mkdocs local link (<a href="https://redirect.github.com/astral-sh/ruff/issues/10167">#10167</a>)</li>
<li><a href="https://github.com/astral-sh/ruff/commit/72ccb34ba69969a15da3328248cdaebeccb82b38"><code>72ccb34</code></a> Fix ecosystem check for indico (<a href="https://redirect.github.com/astral-sh/ruff/issues/10164">#10164</a>)</li>
<li><a href="https://github.com/astral-sh/ruff/commit/dcc92f50cf3786fd3cc5a90d9c465fc80209aad6"><code>dcc92f5</code></a> Update black tests (<a href="https://redirect.github.com/astral-sh/ruff/issues/10166">#10166</a>)</li>
<li><a href="https://github.com/astral-sh/ruff/commit/a6f32ddc5e9582112e76ad25039e9b080e281dce"><code>a6f32dd</code></a> Ruff 2024.2 style (<a href="https://redirect.github.com/astral-sh/ruff/issues/9639">#9639</a>)</li>
<li><a href="https://github.com/astral-sh/ruff/commit/0293908b71eeaf610d8ce77d2950f0602fd88dc5"><code>0293908</code></a> Implement RUF028 to detect useless formatter suppression comments (<a href="https://redirect.github.com/astral-sh/ruff/issues/9899">#9899</a>)</li>
<li><a href="https://github.com/astral-sh/ruff/commit/36bc725eaa8d0decb4ad880ddb42094a967feb20"><code>36bc725</code></a> [<code>flake8-bugbear</code>] Avoid adding default initializers to stubs (<code>B006</code>) (<a href="https://redirect.github.com/astral-sh/ruff/issues/10152">#10152</a>)</li>
<li>Additional commits viewable in <a href="https://github.com/astral-sh/ruff/compare/v0.1.2...v0.3.0">compare view</a></li>
</ul>
</details>
<br />


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