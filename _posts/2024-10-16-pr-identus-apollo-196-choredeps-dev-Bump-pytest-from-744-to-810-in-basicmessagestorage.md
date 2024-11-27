---
title: "identus-apollo/pr/196: chore(deps-dev): Bump pytest from 7.4.4 to 8.1.0 in /basicmessage_storage"
date: 2024-10-16 12:48:45 +0000
author: dependabot
categories: ["Hyperledger"]
tags: ["identus-apollo"]
permalink: /identus-apollo/pr/196/
comments_file: Hyperledger-identus-apollo-pr-196_comments
excerpt: >
  Proposing to change 'https://didcomm.org/issue-credential/3.0/offer-credential' to SDK.ProtocolType.DidcommOfferCredential
---
Bumps [pytest](https://github.com/pytest-dev/pytest) from 7.4.4 to 8.1.0.
<details>
<summary>Release notes</summary>
<p><em>Sourced from <a href="https://github.com/pytest-dev/pytest/releases">pytest's releases</a>.</em></p>
<blockquote>
<h2>8.1.0</h2>
<h1>pytest 8.1.0 (2024-03-03)</h1>
<h2>Features</h2>
<ul>
<li>
<p><a href="https://redirect.github.com/pytest-dev/pytest/issues/11475">#11475</a>: Added the new <code>consider_namespace_packages</code>{.interpreted-text role=&quot;confval&quot;} configuration option, defaulting to <code>False</code>.</p>
<p>If set to <code>True</code>, pytest will attempt to identify modules that are part of <a href="https://packaging.python.org/en/latest/guides/packaging-namespace-packages">namespace packages</a> when importing modules.</p>
</li>
<li>
<p><a href="https://redirect.github.com/pytest-dev/pytest/issues/11653">#11653</a>: Added the new <code>verbosity_test_cases</code>{.interpreted-text role=&quot;confval&quot;} configuration option for fine-grained control of test execution verbosity.
See <code>Fine-grained verbosity &lt;pytest.fine_grained_verbosity&gt;</code>{.interpreted-text role=&quot;ref&quot;} for more details.</p>
</li>
</ul>
<h2>Improvements</h2>
<ul>
<li>
<p><a href="https://redirect.github.com/pytest-dev/pytest/issues/10865">#10865</a>: <code>pytest.warns</code>{.interpreted-text role=&quot;func&quot;} now validates that <code>warnings.warn</code>{.interpreted-text role=&quot;func&quot;} was called with a [str]{.title-ref} or a [Warning]{.title-ref}.
Currently in Python it is possible to use other types, however this causes an exception when <code>warnings.filterwarnings</code>{.interpreted-text role=&quot;func&quot;} is used to filter those warnings (see [CPython <a href="https://redirect.github.com/pytest-dev/pytest/issues/103577">#103577</a>](<a href="https://redirect.github.com/python/cpython/issues/103577">python/cpython#103577</a>) for a discussion).
While this can be considered a bug in CPython, we decided to put guards in pytest as the error message produced without this check in place is confusing.</p>
</li>
<li>
<p><a href="https://redirect.github.com/pytest-dev/pytest/issues/11311">#11311</a>: When using <code>--override-ini</code> for paths in invocations without a configuration file defined, the current working directory is used
as the relative directory.</p>
<p>Previoulsy this would raise an <code>AssertionError</code>{.interpreted-text role=&quot;class&quot;}.</p>
</li>
<li>
<p><a href="https://redirect.github.com/pytest-dev/pytest/issues/11475">#11475</a>: <code>--import-mode=importlib &lt;import-mode-importlib&gt;</code>{.interpreted-text role=&quot;ref&quot;} now tries to import modules using the standard import mechanism (but still without changing :py<code>sys.path</code>{.interpreted-text role=&quot;data&quot;}), falling back to importing modules directly only if that fails.</p>
<p>This means that installed packages will be imported under their canonical name if possible first, for example <code>app.core.models</code>, instead of having the module name always be derived from their path (for example <code>.env310.lib.site_packages.app.core.models</code>).</p>
</li>
<li>
<p><a href="https://redirect.github.com/pytest-dev/pytest/issues/11801">#11801</a>: Added the <code>iter_parents() &lt;_pytest.nodes.Node.iter_parents&gt;</code>{.interpreted-text role=&quot;func&quot;} helper method on nodes.
It is similar to <code>listchain &lt;_pytest.nodes.Node.listchain&gt;</code>{.interpreted-text role=&quot;func&quot;}, but goes from bottom to top, and returns an iterator, not a list.</p>
</li>
<li>
<p><a href="https://redirect.github.com/pytest-dev/pytest/issues/11850">#11850</a>: Added support for <code>sys.last_exc</code>{.interpreted-text role=&quot;data&quot;} for post-mortem debugging on Python&gt;=3.12.</p>
</li>
<li>
<p><a href="https://redirect.github.com/pytest-dev/pytest/issues/11962">#11962</a>: In case no other suitable candidates for configuration file are found, a <code>pyproject.toml</code> (even without a <code>[tool.pytest.ini_options]</code> table) will be considered as the configuration file and define the <code>rootdir</code>.</p>
</li>
<li>
<p><a href="https://redirect.github.com/pytest-dev/pytest/issues/11978">#11978</a>: Add <code>--log-file-mode</code> option to the logging plugin, enabling appending to log-files. This option accepts either <code>&quot;w&quot;</code> or <code>&quot;a&quot;</code> and defaults to <code>&quot;w&quot;</code>.</p>
<p>Previously, the mode was hard-coded to be <code>&quot;w&quot;</code> which truncates the file before logging.</p>
</li>
<li>
<p><a href="https://redirect.github.com/pytest-dev/pytest/issues/12047">#12047</a>: When multiple finalizers of a fixture raise an exception, now all exceptions are reported as an exception group.
Previously, only the first exception was reported.</p>
</li>
</ul>
<h2>Bug Fixes</h2>
<ul>
<li>
<p><a href="https://redirect.github.com/pytest-dev/pytest/issues/11904">#11904</a>: Fixed a regression in pytest 8.0.0 that would cause test collection to fail due to permission errors when using <code>--pyargs</code>.</p>
<p>This change improves the collection tree for tests specified using <code>--pyargs</code>, see <code>12043</code>{.interpreted-text role=&quot;pull&quot;} for a comparison with pytest 8.0 and &lt;8.</p>
</li>
</ul>
<!-- raw HTML omitted -->
</blockquote>
<p>... (truncated)</p>
</details>
<details>
<summary>Commits</summary>
<ul>
<li><a href="https://github.com/pytest-dev/pytest/commit/b9a167f9bbbd6eda4f0360c5bf5b7f5af50f2bc4"><code>b9a167f</code></a> Prepare release version 8.1.0</li>
<li><a href="https://github.com/pytest-dev/pytest/commit/00043f7f1047b29fdaeb18e169fe9d6146988cb8"><code>00043f7</code></a> Merge pull request <a href="https://redirect.github.com/pytest-dev/pytest/issues/12038">#12038</a> from bluetech/fixtures-rm-arg2index</li>
<li><a href="https://github.com/pytest-dev/pytest/commit/f4e10251a4a003495b5228cea421d4de5fa0ce89"><code>f4e1025</code></a> Merge pull request <a href="https://redirect.github.com/pytest-dev/pytest/issues/12048">#12048</a> from bluetech/fixture-teardown-excgroup</li>
<li><a href="https://github.com/pytest-dev/pytest/commit/43492f5707b38dab9b62dfb829bb41a13579629f"><code>43492f5</code></a> Merge pull request <a href="https://redirect.github.com/pytest-dev/pytest/issues/12051">#12051</a> from jakkdl/test_debugging_pythonbreakpoint</li>
<li><a href="https://github.com/pytest-dev/pytest/commit/82fe28dae4eec900123175cee87245f37b964e5c"><code>82fe28d</code></a> [automated] Update plugin list (<a href="https://redirect.github.com/pytest-dev/pytest/issues/12049">#12049</a>)</li>
<li><a href="https://github.com/pytest-dev/pytest/commit/5e2ee7175c145f84ff9882be9496abb56e6e56f2"><code>5e2ee71</code></a> monkeypatch.delenv PYTHONBREAKPOINT in two tests that previously failed/skipped</li>
<li><a href="https://github.com/pytest-dev/pytest/commit/89ee4493ccbcd118349082cd78eb52a761683120"><code>89ee449</code></a> Merge pull request <a href="https://redirect.github.com/pytest-dev/pytest/issues/11997">#11997</a> from nicoddemus/11475-importlib</li>
<li><a href="https://github.com/pytest-dev/pytest/commit/8248946a552635f5751a58c7a6dfd24e98db7404"><code>8248946</code></a> Do not collect symlinked tests under Windows (<a href="https://redirect.github.com/pytest-dev/pytest/issues/12050">#12050</a>)</li>
<li><a href="https://github.com/pytest-dev/pytest/commit/434282e17f5f1f4fcc1464a0a0921cf19804bdd7"><code>434282e</code></a> fixtures: use exception group when multiple finalizers raise in fixture teardown</li>
<li><a href="https://github.com/pytest-dev/pytest/commit/d6134bc21e27efee7a2e264bd089e6c223515904"><code>d6134bc</code></a> doc: document consider_namespace_packages option</li>
<li>Additional commits viewable in <a href="https://github.com/pytest-dev/pytest/compare/7.4.4...8.1.0">compare view</a></li>
</ul>
</details>
<br />


[![Dependabot compatibility score](https://dependabot-badges.githubapp.com/badges/compatibility_score?dependency-name=pytest&package-manager=pip&previous-version=7.4.4&new-version=8.1.0)](https://docs.github.com/en/github/managing-security-vulnerabilities/about-dependabot-security-updates#about-compatibility-scores)

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