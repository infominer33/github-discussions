---
title: "identus-apollo/pr/185: chore(deps-dev): Bump indy-vdr from 0.3.4 to 0.4.1 in /rpc"
date: 2024-07-18 17:25:42 +0000
author: dependabot
categories: ["Hyperledger"]
tags: ["identus-apollo"]
permalink: /identus-apollo/pr/185/
comments_file: Hyperledger-identus-apollo-pr-185_comments
excerpt: >
  lowercase?  ```suggestion  credential's <a data-cite=\"VC-DATA-MODEL-2.0#refreshing\">refresh service</a>  ```
---
Bumps [indy-vdr](https://github.com/hyperledger/indy-vdr) from 0.3.4 to 0.4.1.
<details>
<summary>Release notes</summary>
<p><em>Sourced from <a href="https://github.com/hyperledger/indy-vdr/releases">indy-vdr's releases</a>.</em></p>
<blockquote>
<h2>v0.4.1</h2>
<h2>What's Changed</h2>
<ul>
<li>fix(js): add missing parameters to rn wrapper by <a href="https://github.com/genaris"><code>@​genaris</code></a> in <a href="https://redirect.github.com/hyperledger/indy-vdr/pull/218">hyperledger/indy-vdr#218</a></li>
<li>Update to indy-data-types 0.7; remove indy-utils by <a href="https://github.com/andrewwhitehead"><code>@​andrewwhitehead</code></a> in <a href="https://redirect.github.com/hyperledger/indy-vdr/pull/224">hyperledger/indy-vdr#224</a></li>
<li>fix a typo in logs by <a href="https://github.com/xiaolou86"><code>@​xiaolou86</code></a> in <a href="https://redirect.github.com/hyperledger/indy-vdr/pull/231">hyperledger/indy-vdr#231</a></li>
<li>fix(js): use quotes instead of brackets for local dependencies by <a href="https://github.com/berendsliedrecht"><code>@​berendsliedrecht</code></a> in <a href="https://redirect.github.com/hyperledger/indy-vdr/pull/232">hyperledger/indy-vdr#232</a></li>
<li>fix(js): use universal architecture for darwin by <a href="https://github.com/berendsliedrecht"><code>@​berendsliedrecht</code></a> in <a href="https://redirect.github.com/hyperledger/indy-vdr/pull/233">hyperledger/indy-vdr#233</a></li>
<li>fix(rn): do not try to deserialize again if it is a stream by <a href="https://github.com/berendsliedrecht"><code>@​berendsliedrecht</code></a> in <a href="https://redirect.github.com/hyperledger/indy-vdr/pull/234">hyperledger/indy-vdr#234</a></li>
<li>Faster pool refresh by <a href="https://github.com/andrewwhitehead"><code>@​andrewwhitehead</code></a> in <a href="https://redirect.github.com/hyperledger/indy-vdr/pull/242">hyperledger/indy-vdr#242</a></li>
<li>Add genesis transactions caching by <a href="https://github.com/andrewwhitehead"><code>@​andrewwhitehead</code></a> in <a href="https://redirect.github.com/hyperledger/indy-vdr/pull/243">hyperledger/indy-vdr#243</a></li>
<li>genesis cache js by <a href="https://github.com/berendsliedrecht"><code>@​berendsliedrecht</code></a> in <a href="https://redirect.github.com/hyperledger/indy-vdr/pull/244">hyperledger/indy-vdr#244</a></li>
<li>Update setup.py by <a href="https://github.com/tnkhanh"><code>@​tnkhanh</code></a> in <a href="https://redirect.github.com/hyperledger/indy-vdr/pull/245">hyperledger/indy-vdr#245</a></li>
</ul>
<h2>New Contributors</h2>
<ul>
<li><a href="https://github.com/xiaolou86"><code>@​xiaolou86</code></a> made their first contribution in <a href="https://redirect.github.com/hyperledger/indy-vdr/pull/231">hyperledger/indy-vdr#231</a></li>
<li><a href="https://github.com/tnkhanh"><code>@​tnkhanh</code></a> made their first contribution in <a href="https://redirect.github.com/hyperledger/indy-vdr/pull/245">hyperledger/indy-vdr#245</a></li>
</ul>
<p><strong>Full Changelog</strong>: <a href="https://github.com/hyperledger/indy-vdr/compare/v0.4.0...v0.4.1">https://github.com/hyperledger/indy-vdr/compare/v0.4.0...v0.4.1</a></p>
<h2>v0.4.0</h2>
<ul>
<li>Added support for <code>did:indy</code> in <a href="https://redirect.github.com/hyperledger/indy-vdr/pull/166">hyperledger/indy-vdr#166</a>, thanks to <a href="https://github.com/domwoe"><code>@​domwoe</code></a>, <a href="https://github.com/c2bo"><code>@​c2bo</code></a></li>
<li>Added new nodejs and react-native wrappers, thanks to <a href="https://github.com/berendsliedrecht"><code>@​berendsliedrecht</code></a>, <a href="https://github.com/TimoGlastra"><code>@​TimoGlastra</code></a>, <a href="https://github.com/karimStekelenburg"><code>@​karimStekelenburg</code></a>, <a href="https://github.com/genaris"><code>@​genaris</code></a>, <a href="https://github.com/mrlunin"><code>@​mrlunin</code></a></li>
<li>Switched from Ursa (now archived) to <code>indy-blssignatures</code></li>
<li>Added builder for POOL_UPGRADE request into FFI and Python by <a href="https://github.com/Artemkaaas"><code>@​Artemkaaas</code></a> in <a href="https://redirect.github.com/hyperledger/indy-vdr/pull/148">hyperledger/indy-vdr#148</a></li>
<li>Proxy client by <a href="https://github.com/mirgee"><code>@​mirgee</code></a> in <a href="https://redirect.github.com/hyperledger/indy-vdr/pull/184">hyperledger/indy-vdr#184</a></li>
<li>Support HTTPS by <a href="https://github.com/mirgee"><code>@​mirgee</code></a> in <a href="https://redirect.github.com/hyperledger/indy-vdr/pull/187">hyperledger/indy-vdr#187</a></li>
<li>Issue <a href="https://redirect.github.com/hyperledger/indy-vdr/issues/210">#210</a> InvalidClientTaaAcceptanceError time too precise error if container timezone is not UTC by <a href="https://github.com/Ennovate-com"><code>@​Ennovate-com</code></a> in <a href="https://redirect.github.com/hyperledger/indy-vdr/pull/211">hyperledger/indy-vdr#211</a></li>
<li>Fix minor typos by <a href="https://github.com/omahs"><code>@​omahs</code></a> in <a href="https://redirect.github.com/hyperledger/indy-vdr/pull/213">hyperledger/indy-vdr#213</a></li>
<li>Now publishing arm64 packages</li>
</ul>
<p><strong>Full Changelog</strong>: <a href="https://github.com/hyperledger/indy-vdr/compare/v0.3.4...v0.4.0">https://github.com/hyperledger/indy-vdr/compare/v0.3.4...v0.4.0</a></p>
<h2>v0.4.0-dev.16</h2>
<h2>What's Changed</h2>
<ul>
<li>fix(rn): android works with JSC and Hermes by <a href="https://github.com/blu3beri"><code>@​blu3beri</code></a> in <a href="https://redirect.github.com/hyperledger/indy-vdr/pull/194">hyperledger/indy-vdr#194</a></li>
<li>chore: update version by <a href="https://github.com/blu3beri"><code>@​blu3beri</code></a> in <a href="https://redirect.github.com/hyperledger/indy-vdr/pull/195">hyperledger/indy-vdr#195</a></li>
</ul>
<p><strong>Full Changelog</strong>: <a href="https://github.com/hyperledger/indy-vdr/compare/v0.4.0-dev.15...v0.4.0-dev.16">https://github.com/hyperledger/indy-vdr/compare/v0.4.0-dev.15...v0.4.0-dev.16</a></p>
<h2>v0.4.0-dev.15</h2>
<h2>What's Changed</h2>
<ul>
<li>fix(nodejs): compatible with Windows builds by <a href="https://github.com/blu3beri"><code>@​blu3beri</code></a> in <a href="https://redirect.github.com/hyperledger/indy-vdr/pull/183">hyperledger/indy-vdr#183</a></li>
<li>feat: react native 0.71.x and Expo support by <a href="https://github.com/blu3beri"><code>@​blu3beri</code></a> in <a href="https://redirect.github.com/hyperledger/indy-vdr/pull/186">hyperledger/indy-vdr#186</a></li>
<li>build(android): use custom cross images by <a href="https://github.com/blu3beri"><code>@​blu3beri</code></a> in <a href="https://redirect.github.com/hyperledger/indy-vdr/pull/189">hyperledger/indy-vdr#189</a></li>
<li>chore: update version by <a href="https://github.com/blu3beri"><code>@​blu3beri</code></a> in <a href="https://redirect.github.com/hyperledger/indy-vdr/pull/190">hyperledger/indy-vdr#190</a></li>
<li>build(js): use local network by <a href="https://github.com/blu3beri"><code>@​blu3beri</code></a> in <a href="https://redirect.github.com/hyperledger/indy-vdr/pull/192">hyperledger/indy-vdr#192</a></li>
</ul>
<p><strong>Full Changelog</strong>: <a href="https://github.com/hyperledger/indy-vdr/compare/v0.4.0-dev.14...v0.4.0-dev.15">https://github.com/hyperledger/indy-vdr/compare/v0.4.0-dev.14...v0.4.0-dev.15</a></p>
<!-- raw HTML omitted -->
</blockquote>
<p>... (truncated)</p>
</details>
<details>
<summary>Commits</summary>
<ul>
<li><a href="https://github.com/hyperledger/indy-vdr/commit/c4b558c2e99a6e0751642056b66511046a5a35ef"><code>c4b558c</code></a> Merge pull request <a href="https://redirect.github.com/hyperledger/indy-vdr/issues/247">#247</a> from andrewwhitehead/upd/ver-041</li>
<li><a href="https://github.com/hyperledger/indy-vdr/commit/0d975070f1caf5274563b327718132dab85328bf"><code>0d97507</code></a> use lockfile when installing cross</li>
<li><a href="https://github.com/hyperledger/indy-vdr/commit/162a1f34f294f099cd925ec3a6ec02a7074c51c1"><code>162a1f3</code></a> update proxy version to 0.1.5</li>
<li><a href="https://github.com/hyperledger/indy-vdr/commit/a19834485f8c8bd72511d37f8969cf3278f6f164"><code>a198344</code></a> update python wrapper version to 0.4.1</li>
<li><a href="https://github.com/hyperledger/indy-vdr/commit/83f3507068b8dcbc78e9cef9681d3f414066da9e"><code>83f3507</code></a> Merge pull request <a href="https://redirect.github.com/hyperledger/indy-vdr/issues/245">#245</a> from tnkhanh/patch-1</li>
<li><a href="https://github.com/hyperledger/indy-vdr/commit/fb2bbbedb68f6a29cbe6dbe04e3cf861054ae35d"><code>fb2bbbe</code></a> Merge branch 'main' into patch-1</li>
<li><a href="https://github.com/hyperledger/indy-vdr/commit/f70a6d80ff1d2aa53e4cc3f29bfb0bd452dd3e09"><code>f70a6d8</code></a> Merge pull request <a href="https://redirect.github.com/hyperledger/indy-vdr/issues/244">#244</a> from berendsliedrecht/genesis-cache-js</li>
<li><a href="https://github.com/hyperledger/indy-vdr/commit/9695a179160be3178cc2cb6b39470faedd97f317"><code>9695a17</code></a> Merge branch 'main' into genesis-cache-js</li>
<li><a href="https://github.com/hyperledger/indy-vdr/commit/a914ef401ed7258c14a89365deb1c5a32dc5d1d5"><code>a914ef4</code></a> Merge pull request <a href="https://redirect.github.com/hyperledger/indy-vdr/issues/243">#243</a> from andrewwhitehead/feat/genesis-cache</li>
<li><a href="https://github.com/hyperledger/indy-vdr/commit/cc7e2bb4ddae1fe8f6a4bbcf17c4c20a8fedd362"><code>cc7e2bb</code></a> Update setup.py</li>
<li>Additional commits viewable in <a href="https://github.com/hyperledger/indy-vdr/compare/v0.3.4...v0.4.1">compare view</a></li>
</ul>
</details>
<br />


[![Dependabot compatibility score](https://dependabot-badges.githubapp.com/badges/compatibility_score?dependency-name=indy-vdr&package-manager=pip&previous-version=0.3.4&new-version=0.4.1)](https://docs.github.com/en/github/managing-security-vulnerabilities/about-dependabot-security-updates#about-compatibility-scores)

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