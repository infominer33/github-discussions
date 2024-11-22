---
title: "bbs-signature/pr/320: chore(deps-dev): bump @babel/runtime from 7.22.10 to 7.25.4 in /wrappers/javascript"
date: 2024-06-25 15:38:48 +0000
author: dependabot
categories: ["DIF"]
tags: ["bbs-signature"]
permalink: /bbs-signature/pr/320/
comments_file: DIF-bbs-signature-pr-320_comments
---

[_https://github.com/decentralized-identity/bbs-signature/pull/320_](https://github.com/decentralized-identity/bbs-signature/pull/320)

Bumps [@babel/runtime](https://github.com/babel/babel/tree/HEAD/packages/babel-runtime) from 7.22.10 to 7.25.4.
<details>
<summary>Release notes</summary>
<p><em>Sourced from <a href="https://github.com/babel/babel/releases"><code>@​babel/runtime</code>'s releases</a>.</em></p>
<blockquote>
<h2>v7.25.4 (2024-08-22)</h2>
<h4>:bug: Bug Fix</h4>
<ul>
<li><code>babel-traverse</code>
<ul>
<li><a href="https://redirect.github.com/babel/babel/pull/16756">#16756</a> fix: Skip computed key when renaming (<a href="https://github.com/liuxingbaoyu"><code>@​liuxingbaoyu</code></a>)</li>
</ul>
</li>
<li><code>babel-helper-create-class-features-plugin</code>, <code>babel-plugin-proposal-decorators</code>
<ul>
<li><a href="https://redirect.github.com/babel/babel/pull/16755">#16755</a> fix: Decorator 2018-09 may throw an exception (<a href="https://github.com/liuxingbaoyu"><code>@​liuxingbaoyu</code></a>)</li>
</ul>
</li>
<li><code>babel-types</code>
<ul>
<li><a href="https://redirect.github.com/babel/babel/pull/16710">#16710</a> Visit AST fields nodes according to their syntactical order (<a href="https://github.com/nicolo-ribaudo"><code>@​nicolo-ribaudo</code></a>)</li>
</ul>
</li>
<li><code>babel-generator</code>
<ul>
<li><a href="https://redirect.github.com/babel/babel/pull/16709">#16709</a> Print semicolon after TS <code>export namespace as A</code> (<a href="https://github.com/nicolo-ribaudo"><code>@​nicolo-ribaudo</code></a>)</li>
</ul>
</li>
</ul>
<h4>:nail_care: Polish</h4>
<ul>
<li><code>babel-generator</code>, <code>babel-plugin-proposal-decorators</code>, <code>babel-plugin-proposal-destructuring-private</code>, <code>babel-plugin-proposal-pipeline-operator</code>, <code>babel-plugin-transform-class-properties</code>, <code>babel-plugin-transform-destructuring</code>, <code>babel-plugin-transform-optional-chaining</code>, <code>babel-plugin-transform-private-methods</code>, <code>babel-plugin-transform-private-property-in-object</code>, <code>babel-plugin-transform-typescript</code>, <code>babel-runtime-corejs2</code>, <code>babel-runtime</code>, <code>babel-traverse</code>
<ul>
<li><a href="https://redirect.github.com/babel/babel/pull/16722">#16722</a> Avoid unnecessary parens around sequence expressions (<a href="https://github.com/nicolo-ribaudo"><code>@​nicolo-ribaudo</code></a>)</li>
</ul>
</li>
<li><code>babel-generator</code>, <code>babel-plugin-transform-class-properties</code>
<ul>
<li><a href="https://redirect.github.com/babel/babel/pull/16714">#16714</a> Avoid unnecessary parens around exported arrow functions (<a href="https://github.com/nicolo-ribaudo"><code>@​nicolo-ribaudo</code></a>)</li>
</ul>
</li>
<li><code>babel-generator</code>, <code>babel-plugin-proposal-decorators</code>, <code>babel-plugin-proposal-destructuring-private</code>, <code>babel-plugin-transform-object-rest-spread</code>
<ul>
<li><a href="https://redirect.github.com/babel/babel/pull/16712">#16712</a> Avoid printing unnecessary parens around object destructuring (<a href="https://github.com/nicolo-ribaudo"><code>@​nicolo-ribaudo</code></a>)</li>
</ul>
</li>
</ul>
<h4>:microscope: Output optimization</h4>
<ul>
<li><code>babel-generator</code>
<ul>
<li><a href="https://redirect.github.com/babel/babel/pull/16740">#16740</a> Avoid extra spaces between comments/regexps in compact mode (<a href="https://github.com/nicolo-ribaudo"><code>@​nicolo-ribaudo</code></a>)</li>
</ul>
</li>
</ul>
<h4>Committers: 4</h4>
<ul>
<li>Babel Bot (<a href="https://github.com/babel-bot"><code>@​babel-bot</code></a>)</li>
<li>Huáng Jùnliàng (<a href="https://github.com/JLHwung"><code>@​JLHwung</code></a>)</li>
<li>Nicolò Ribaudo (<a href="https://github.com/nicolo-ribaudo"><code>@​nicolo-ribaudo</code></a>)</li>
<li><a href="https://github.com/liuxingbaoyu"><code>@​liuxingbaoyu</code></a></li>
</ul>
<h2>v7.25.3 (2024-07-31)</h2>
<h4>:bug: Bug Fix</h4>
<ul>
<li><code>babel-plugin-bugfix-firefox-class-in-computed-class-key</code>, <code>babel-traverse</code>
<ul>
<li><a href="https://redirect.github.com/babel/babel/pull/16699">#16699</a> Avoid validating visitors produced by <code>traverse.visitors.merge</code> (<a href="https://github.com/nicolo-ribaudo"><code>@​nicolo-ribaudo</code></a>)</li>
</ul>
</li>
</ul>
<h4>:house: Internal</h4>
<ul>
<li><code>babel-parser</code>
<ul>
<li><a href="https://redirect.github.com/babel/babel/pull/16688">#16688</a> Add <code>@babel/types</code> as a dependency of <code>@babel/parser</code> (<a href="https://github.com/nicolo-ribaudo"><code>@​nicolo-ribaudo</code></a>)</li>
</ul>
</li>
</ul>
<h4>Committers: 2</h4>
<ul>
<li>Huáng Jùnliàng (<a href="https://github.com/JLHwung"><code>@​JLHwung</code></a>)</li>
<li>Nicolò Ribaudo (<a href="https://github.com/nicolo-ribaudo"><code>@​nicolo-ribaudo</code></a>)</li>
</ul>
<h2>v7.25.2 (2024-07-30)</h2>
<h4>:bug: Bug Fix</h4>
<ul>
<li><code>babel-core</code>, <code>babel-traverse</code>
<ul>
<li><a href="https://redirect.github.com/babel/babel/pull/16695">#16695</a> Ensure that <code>requeueComputedKeyAndDecorators</code> is available (<a href="https://github.com/nicolo-ribaudo"><code>@​nicolo-ribaudo</code></a>)</li>
</ul>
</li>
</ul>
<!-- raw HTML omitted -->
</blockquote>
<p>... (truncated)</p>
</details>
<details>
<summary>Changelog</summary>
<p><em>Sourced from <a href="https://github.com/babel/babel/blob/main/CHANGELOG.md"><code>@​babel/runtime</code>'s changelog</a>.</em></p>
<blockquote>
<h2>v7.25.4 (2024-08-22)</h2>
<h4>:bug: Bug Fix</h4>
<ul>
<li><code>babel-traverse</code>
<ul>
<li><a href="https://redirect.github.com/babel/babel/pull/16756">#16756</a> fix: Skip computed key when renaming (<a href="https://github.com/liuxingbaoyu"><code>@​liuxingbaoyu</code></a>)</li>
</ul>
</li>
<li><code>babel-helper-create-class-features-plugin</code>, <code>babel-plugin-proposal-decorators</code>
<ul>
<li><a href="https://redirect.github.com/babel/babel/pull/16755">#16755</a> fix: Decorator 2018-09 may throw an exception (<a href="https://github.com/liuxingbaoyu"><code>@​liuxingbaoyu</code></a>)</li>
</ul>
</li>
<li><code>babel-types</code>
<ul>
<li><a href="https://redirect.github.com/babel/babel/pull/16710">#16710</a> Visit AST fields nodes according to their syntactical order (<a href="https://github.com/nicolo-ribaudo"><code>@​nicolo-ribaudo</code></a>)</li>
</ul>
</li>
<li><code>babel-generator</code>
<ul>
<li><a href="https://redirect.github.com/babel/babel/pull/16709">#16709</a> Print semicolon after TS <code>export namespace as A</code> (<a href="https://github.com/nicolo-ribaudo"><code>@​nicolo-ribaudo</code></a>)</li>
</ul>
</li>
</ul>
<h4>:nail_care: Polish</h4>
<ul>
<li><code>babel-generator</code>, <code>babel-plugin-proposal-decorators</code>, <code>babel-plugin-proposal-destructuring-private</code>, <code>babel-plugin-proposal-pipeline-operator</code>, <code>babel-plugin-transform-class-properties</code>, <code>babel-plugin-transform-destructuring</code>, <code>babel-plugin-transform-optional-chaining</code>, <code>babel-plugin-transform-private-methods</code>, <code>babel-plugin-transform-private-property-in-object</code>, <code>babel-plugin-transform-typescript</code>, <code>babel-runtime-corejs2</code>, <code>babel-runtime</code>, <code>babel-traverse</code>
<ul>
<li><a href="https://redirect.github.com/babel/babel/pull/16722">#16722</a> Avoid unnecessary parens around sequence expressions (<a href="https://github.com/nicolo-ribaudo"><code>@​nicolo-ribaudo</code></a>)</li>
</ul>
</li>
<li><code>babel-generator</code>, <code>babel-plugin-transform-class-properties</code>
<ul>
<li><a href="https://redirect.github.com/babel/babel/pull/16714">#16714</a> Avoid unnecessary parens around exported arrow functions (<a href="https://github.com/nicolo-ribaudo"><code>@​nicolo-ribaudo</code></a>)</li>
</ul>
</li>
<li><code>babel-generator</code>, <code>babel-plugin-proposal-decorators</code>, <code>babel-plugin-proposal-destructuring-private</code>, <code>babel-plugin-transform-object-rest-spread</code>
<ul>
<li><a href="https://redirect.github.com/babel/babel/pull/16712">#16712</a> Avoid printing unnecessary parens around object destructuring (<a href="https://github.com/nicolo-ribaudo"><code>@​nicolo-ribaudo</code></a>)</li>
</ul>
</li>
</ul>
<h4>:microscope: Output optimization</h4>
<ul>
<li><code>babel-generator</code>
<ul>
<li><a href="https://redirect.github.com/babel/babel/pull/16740">#16740</a> Avoid extra spaces between comments/regexps in compact mode (<a href="https://github.com/nicolo-ribaudo"><code>@​nicolo-ribaudo</code></a>)</li>
</ul>
</li>
</ul>
<h2>v7.25.3 (2024-07-31)</h2>
<h4>:bug: Bug Fix</h4>
<ul>
<li><code>babel-plugin-bugfix-firefox-class-in-computed-class-key</code>, <code>babel-traverse</code>
<ul>
<li><a href="https://redirect.github.com/babel/babel/pull/16699">#16699</a> Avoid validating visitors produced by <code>traverse.visitors.merge</code> (<a href="https://github.com/nicolo-ribaudo"><code>@​nicolo-ribaudo</code></a>)</li>
</ul>
</li>
</ul>
<h4>:house: Internal</h4>
<ul>
<li><code>babel-parser</code>
<ul>
<li><a href="https://redirect.github.com/babel/babel/pull/16688">#16688</a> Add <code>@babel/types</code> as a dependency of <code>@babel/parser</code> (<a href="https://github.com/nicolo-ribaudo"><code>@​nicolo-ribaudo</code></a>)</li>
</ul>
</li>
</ul>
<h2>v7.25.2 (2024-07-30)</h2>
<h4>:bug: Bug Fix</h4>
<ul>
<li><code>babel-core</code>, <code>babel-traverse</code>
<ul>
<li><a href="https://redirect.github.com/babel/babel/pull/16695">#16695</a> Ensure that <code>requeueComputedKeyAndDecorators</code> is available (<a href="https://github.com/nicolo-ribaudo"><code>@​nicolo-ribaudo</code></a>)</li>
</ul>
</li>
</ul>
<h2>v7.25.1 (2024-07-28)</h2>
<h4>:bug: Bug Fix</h4>
<ul>
<li><code>babel-plugin-transform-function-name</code>
<ul>
<li><a href="https://redirect.github.com/babel/babel/pull/16683">#16683</a> fix: <code>ensureFunctionName</code> may be undefined (<a href="https://github.com/liuxingbaoyu"><code>@​liuxingbaoyu</code></a>)</li>
</ul>
</li>
<li><code>babel-plugin-transform-react-constant-elements</code>
<ul>
<li><a href="https://redirect.github.com/babel/babel/pull/16582">#16582</a> fix plugin-transform-react-constant-elements transform JSXFrament but not add JSXExpressionContainer (<a href="https://github.com/keiseiTi"><code>@​keiseiTi</code></a>)</li>
</ul>
</li>
<li><code>babel-traverse</code>
<ul>
<li><a href="https://redirect.github.com/babel/babel/pull/16587">#16587</a> fix: fixed issue16583 + test (<a href="https://github.com/nerodesu017"><code>@​nerodesu017</code></a>)</li>
</ul>
</li>
</ul>
<h4>:house: Internal</h4>
<ul>
<li><a href="https://redirect.github.com/babel/babel/pull/16663">#16663</a> Test eslint plugin against eslint 9 (<a href="https://github.com/JLHwung"><code>@​JLHwung</code></a>)</li>
</ul>
<h2>v7.25.0 (2024-07-26)</h2>
<!-- raw HTML omitted -->
</blockquote>
<p>... (truncated)</p>
</details>
<details>
<summary>Commits</summary>
<ul>
<li><a href="https://github.com/babel/babel/commit/cbf124ca42a4c34630040bf556e6a8507f961dfe"><code>cbf124c</code></a> v7.25.4</li>
<li><a href="https://github.com/babel/babel/commit/575863cf05c66810b9886a25b43c2dfa71de2e07"><code>575863c</code></a> Avoid unnecessary parens around sequence expressions (<a href="https://github.com/babel/babel/tree/HEAD/packages/babel-runtime/issues/16722">#16722</a>)</li>
<li><a href="https://github.com/babel/babel/commit/d2e3ee2c922daee20119c2233ace16999a666cbc"><code>d2e3ee2</code></a> v7.25.0</li>
<li><a href="https://github.com/babel/babel/commit/e774270843a520feffb0643fba236adbed6b0fb6"><code>e774270</code></a> Improve <code>super.x</code> output (<a href="https://github.com/babel/babel/tree/HEAD/packages/babel-runtime/issues/16374">#16374</a>)</li>
<li><a href="https://github.com/babel/babel/commit/1f5af441178256f5e846b4f6c678e2bd375e5d9d"><code>1f5af44</code></a> v7.24.8</li>
<li><a href="https://github.com/babel/babel/commit/bf1e9a34e4d66d8231dad2f12b9df46d4b730ead"><code>bf1e9a3</code></a> v7.24.7</li>
<li><a href="https://github.com/babel/babel/commit/14a0b08c42e3e99672ccc4b2fb7da6d32c9d8158"><code>14a0b08</code></a> [helpers TS conversion] async functions/generators (<a href="https://github.com/babel/babel/tree/HEAD/packages/babel-runtime/issues/16510">#16510</a>)</li>
<li><a href="https://github.com/babel/babel/commit/793496394e30fe37b56e54d76cabb417e1652dc2"><code>7934963</code></a> Use <code>type: module</code> in all <code>package.json</code>s (<a href="https://github.com/babel/babel/tree/HEAD/packages/babel-runtime/issues/16535">#16535</a>)</li>
<li><a href="https://github.com/babel/babel/commit/ab465cc0ab11196bcc8ef48068984e16193d8198"><code>ab465cc</code></a> Delete unused array helpers (<a href="https://github.com/babel/babel/tree/HEAD/packages/babel-runtime/issues/16525">#16525</a>)</li>
<li><a href="https://github.com/babel/babel/commit/9630250ca06f64a62d20caef62fcfa3b8d9165c8"><code>9630250</code></a> v7.24.6</li>
<li>Additional commits viewable in <a href="https://github.com/babel/babel/commits/v7.25.4/packages/babel-runtime">compare view</a></li>
</ul>
</details>
<br />


[![Dependabot compatibility score](https://dependabot-badges.githubapp.com/badges/compatibility_score?dependency-name=@babel/runtime&package-manager=npm_and_yarn&previous-version=7.22.10&new-version=7.25.4)](https://docs.github.com/en/github/managing-security-vulnerabilities/about-dependabot-security-updates#about-compatibility-scores)

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