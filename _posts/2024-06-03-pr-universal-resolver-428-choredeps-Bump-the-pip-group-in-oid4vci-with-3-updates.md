---
title: "universal-resolver/pr/428: chore(deps): Bump the pip group in /oid4vci with 3 updates"
date: 2024-06-03 12:16:56 +0000
author: dependabot
categories: ["DIF"]
tags: ["universal-resolver"]
permalink: /universal-resolver/pr/428/
comments_file: DIF-universal-resolver-pr-428_comments
excerpt: >
  ```suggestion
---
Bumps the pip group in /oid4vci with 3 updates: [idna](https://github.com/kjd/idna), [jwcrypto](https://github.com/latchset/jwcrypto) and [pillow](https://github.com/python-pillow/Pillow).

Updates `idna` from 3.6 to 3.7
<details>
<summary>Release notes</summary>
<p><em>Sourced from <a href="https://github.com/kjd/idna/releases">idna's releases</a>.</em></p>
<blockquote>
<h2>v3.7</h2>
<h2>What's Changed</h2>
<ul>
<li>Fix issue where specially crafted inputs to encode() could take exceptionally long amount of time to process. [CVE-2024-3651]</li>
</ul>
<p>Thanks to Guido Vranken for reporting the issue.</p>
<p><strong>Full Changelog</strong>: <a href="https://github.com/kjd/idna/compare/v3.6...v3.7">https://github.com/kjd/idna/compare/v3.6...v3.7</a></p>
</blockquote>
</details>
<details>
<summary>Changelog</summary>
<p><em>Sourced from <a href="https://github.com/kjd/idna/blob/master/HISTORY.rst">idna's changelog</a>.</em></p>
<blockquote>
<p>3.7 (2024-04-11)
++++++++++++++++</p>
<ul>
<li>Fix issue where specially crafted inputs to encode() could
take exceptionally long amount of time to process. [CVE-2024-3651]</li>
</ul>
<p>Thanks to Guido Vranken for reporting the issue.</p>
</blockquote>
</details>
<details>
<summary>Commits</summary>
<ul>
<li><a href="https://github.com/kjd/idna/commit/1d365e17e10d72d0b7876316fc7b9ca0eebdd38d"><code>1d365e1</code></a> Release v3.7</li>
<li><a href="https://github.com/kjd/idna/commit/c1b3154939907fab67c5754346afaebe165ce8e6"><code>c1b3154</code></a> Merge pull request <a href="https://redirect.github.com/kjd/idna/issues/172">#172</a> from kjd/optimize-contextj</li>
<li><a href="https://github.com/kjd/idna/commit/0394ec76ff022813e770ba1fd89658790ea35623"><code>0394ec7</code></a> Merge branch 'master' into optimize-contextj</li>
<li><a href="https://github.com/kjd/idna/commit/cd58a23173d2b0a40b95ee680baf3e59e8d33966"><code>cd58a23</code></a> Merge pull request <a href="https://redirect.github.com/kjd/idna/issues/152">#152</a> from elliotwutingfeng/dev</li>
<li><a href="https://github.com/kjd/idna/commit/5beb28b9dd77912c0dd656d8b0fdba3eb80222e7"><code>5beb28b</code></a> More efficient resolution of joiner contexts</li>
<li><a href="https://github.com/kjd/idna/commit/1b121483ed04d9576a1291758f537e1318cddc8b"><code>1b12148</code></a> Update ossf/scorecard-action to v2.3.1</li>
<li><a href="https://github.com/kjd/idna/commit/d516b874c3388047934938a500c7488d52c4e067"><code>d516b87</code></a> Update Github actions/checkout to v4</li>
<li><a href="https://github.com/kjd/idna/commit/c095c75943413c75ebf8ac74179757031b7f80b7"><code>c095c75</code></a> Merge branch 'master' into dev</li>
<li><a href="https://github.com/kjd/idna/commit/60a0a4cb61ec6834d74306bd8a1fa46daac94c98"><code>60a0a4c</code></a> Fix typo in GitHub Actions workflow key</li>
<li><a href="https://github.com/kjd/idna/commit/5918a0ef8034379c2e409ae93ee11d24295bb201"><code>5918a0e</code></a> Merge branch 'master' into dev</li>
<li>Additional commits viewable in <a href="https://github.com/kjd/idna/compare/v3.6...v3.7">compare view</a></li>
</ul>
</details>
<br />

Updates `jwcrypto` from 1.5.1 to 1.5.6
<details>
<summary>Release notes</summary>
<p><em>Sourced from <a href="https://github.com/latchset/jwcrypto/releases">jwcrypto's releases</a>.</em></p>
<blockquote>
<h2>Version 1.5.6 - Moderate Security release</h2>
<h2>What's Changed</h2>
<ul>
<li>Address potential DoS with high compression ratio by <a href="https://github.com/simo5"><code>@​simo5</code></a> in <a href="https://redirect.github.com/latchset/jwcrypto/pull/349">latchset/jwcrypto#349</a></li>
</ul>
<p><strong>Full Changelog</strong>: <a href="https://github.com/latchset/jwcrypto/compare/v1.5.5...v1.5.6">https://github.com/latchset/jwcrypto/compare/v1.5.5...v1.5.6</a></p>
<h2>Version 1.5.5</h2>
<p>This version fixes a pypi distribution problem introduced in 1.0 when pushing was automated.
With 1.5.5 a binary wheel is now also made available on pypi.</p>
<h2>What's Changed</h2>
<ul>
<li>Fix doc generation by <a href="https://github.com/simo5"><code>@​simo5</code></a> in <a href="https://redirect.github.com/latchset/jwcrypto/pull/345">latchset/jwcrypto#345</a></li>
<li>Update publish action to upload also binary dist by <a href="https://github.com/simo5"><code>@​simo5</code></a> in <a href="https://redirect.github.com/latchset/jwcrypto/pull/347">latchset/jwcrypto#347</a></li>
<li>Fix pypi publishing by <a href="https://github.com/simo5"><code>@​simo5</code></a> in <a href="https://redirect.github.com/latchset/jwcrypto/pull/348">latchset/jwcrypto#348</a></li>
</ul>
<p><strong>Full Changelog</strong>: <a href="https://github.com/latchset/jwcrypto/compare/v1.5.4...v1.5.5">https://github.com/latchset/jwcrypto/compare/v1.5.4...v1.5.5</a></p>
<h2>v1.5.4</h2>
<p>One more release bump to address issues with typing_extensions minimum required version</p>
<p><strong>Full Changelog</strong>: <a href="https://github.com/latchset/jwcrypto/compare/v1.5.3...v1.5.4">https://github.com/latchset/jwcrypto/compare/v1.5.3...v1.5.4</a></p>
<h2>v1.5.3</h2>
<p>Bumping release due to inconsistency in python 3.6 support that affected pypi
<a href="https://github.com/latchset/jwcrypto/files/14201083/jwcrypto-1.5.3.tar.gz.sha512sum.txt">jwcrypto-1.5.3.tar.gz.sha512sum.txt</a>
<a href="https://github.com/latchset/jwcrypto/files/14201084/jwcrypto-1.5.3.tar.gz">jwcrypto-1.5.3.tar.gz</a></p>
<h2>What's Changed</h2>
<ul>
<li>Drop python 3.6 and 3.7 and add 3.11 support by <a href="https://github.com/simo5"><code>@​simo5</code></a> in <a href="https://redirect.github.com/latchset/jwcrypto/pull/340">latchset/jwcrypto#340</a></li>
</ul>
<p><strong>Full Changelog</strong>: <a href="https://github.com/latchset/jwcrypto/compare/v1.5.2...v1.5.3">https://github.com/latchset/jwcrypto/compare/v1.5.2...v1.5.3</a></p>
<h2>Version 1.5.2 -  maintenance release</h2>
<p>This is a minor maintenance release to improve interoperability with debuggers
<strong>Note: yanked from pypi due to 3.6 incompatibility, use 1.5.3</strong></p>
<h2>What's Changed</h2>
<ul>
<li>replace deprecated package with typing_extensions by <a href="https://github.com/david-homelend"><code>@​david-homelend</code></a> in <a href="https://redirect.github.com/latchset/jwcrypto/pull/337">latchset/jwcrypto#337</a></li>
</ul>
<h2>New Contributors</h2>
<ul>
<li><a href="https://github.com/david-homelend"><code>@​david-homelend</code></a> made their first contribution in <a href="https://redirect.github.com/latchset/jwcrypto/pull/337">latchset/jwcrypto#337</a></li>
</ul>
<p><strong>Full Changelog</strong>: <a href="https://github.com/latchset/jwcrypto/compare/v1.5.1...v1.5.2">https://github.com/latchset/jwcrypto/compare/v1.5.1...v1.5.2</a></p>
</blockquote>
</details>
<details>
<summary>Commits</summary>
<ul>
<li><a href="https://github.com/latchset/jwcrypto/commit/ecde4efdc7c9364b53bd1b4232e97557d821abdf"><code>ecde4ef</code></a> Version 1.5.6</li>
<li><a href="https://github.com/latchset/jwcrypto/commit/90477a3b6e73da69740e00b8161f53fea19b831f"><code>90477a3</code></a> Address potential DoS with high compression ratio</li>
<li><a href="https://github.com/latchset/jwcrypto/commit/240cc60fe4fe7458d3a7828c3e793795eb59a438"><code>240cc60</code></a> Modernize pypi action</li>
<li><a href="https://github.com/latchset/jwcrypto/commit/491f4485562e94473e57bb9164eb290dcd3be3c5"><code>491f448</code></a> Version 1.5.5</li>
<li><a href="https://github.com/latchset/jwcrypto/commit/7f51d28eea46f039ac363eaf348123394f17310c"><code>7f51d28</code></a> Update publish action to upload also binary dist</li>
<li><a href="https://github.com/latchset/jwcrypto/commit/5dc2ea2a87ea9fb3ed833f9f0f7864edc7b01e7b"><code>5dc2ea2</code></a> Fix doc generation</li>
<li><a href="https://github.com/latchset/jwcrypto/commit/b9432ef46fc8ee90c813469440ea86b049916e52"><code>b9432ef</code></a> Version 1.5.4</li>
<li><a href="https://github.com/latchset/jwcrypto/commit/e7ef80f286883f6710df54c2b7ef78f528d95ee8"><code>e7ef80f</code></a> Set a minimum version for typing_extensions</li>
<li><a href="https://github.com/latchset/jwcrypto/commit/a06b84a1281a2cd6a27eeed3b38ae38e74938d86"><code>a06b84a</code></a> Version 1.5.3</li>
<li><a href="https://github.com/latchset/jwcrypto/commit/c659e385883e3067acf1bf4503d244e95eba4a3d"><code>c659e38</code></a> Drop python 3.6 and 3.7 and add 3.11 support</li>
<li>Additional commits viewable in <a href="https://github.com/latchset/jwcrypto/compare/v1.5.1...v1.5.6">compare view</a></li>
</ul>
</details>
<br />

Updates `pillow` from 10.2.0 to 10.3.0
<details>
<summary>Release notes</summary>
<p><em>Sourced from <a href="https://github.com/python-pillow/Pillow/releases">pillow's releases</a>.</em></p>
<blockquote>
<h2>10.3.0</h2>
<p><a href="https://pillow.readthedocs.io/en/stable/releasenotes/10.3.0.html">https://pillow.readthedocs.io/en/stable/releasenotes/10.3.0.html</a></p>
<h2>Changes</h2>
<ul>
<li>CVE-2024-28219: Use strncpy to avoid buffer overflow <a href="https://redirect.github.com/python-pillow/Pillow/issues/7928">#7928</a> [<a href="https://github.com/hugovk"><code>@​hugovk</code></a>]</li>
<li>Use <code>functools.lru_cache</code> for <code>hopper()</code> <a href="https://redirect.github.com/python-pillow/Pillow/issues/7912">#7912</a> [<a href="https://github.com/hugovk"><code>@​hugovk</code></a>]</li>
<li>Raise ValueError if seeking to greater than offset-sized integer in TIFF <a href="https://redirect.github.com/python-pillow/Pillow/issues/7883">#7883</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Improve speed of loading QOI images <a href="https://redirect.github.com/python-pillow/Pillow/issues/7925">#7925</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Added RGB to I;16N conversion <a href="https://redirect.github.com/python-pillow/Pillow/issues/7920">#7920</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Add --report argument to <strong>main</strong>.py to omit supported formats <a href="https://redirect.github.com/python-pillow/Pillow/issues/7818">#7818</a> [<a href="https://github.com/nulano"><code>@​nulano</code></a>]</li>
<li>Added RGB to I;16, I;16L and I;16B conversion <a href="https://redirect.github.com/python-pillow/Pillow/issues/7918">#7918</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Fix editable installation with custom build backend and configuration options <a href="https://redirect.github.com/python-pillow/Pillow/issues/7658">#7658</a> [<a href="https://github.com/nulano"><code>@​nulano</code></a>]</li>
<li>Fix putdata() for I;16N on big-endian <a href="https://redirect.github.com/python-pillow/Pillow/issues/7209">#7209</a> [<a href="https://github.com/Yay295"><code>@​Yay295</code></a>]</li>
<li>Determine MPO size from markers, not EXIF data <a href="https://redirect.github.com/python-pillow/Pillow/issues/7884">#7884</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Improved conversion from RGB to RGBa, LA and La <a href="https://redirect.github.com/python-pillow/Pillow/issues/7888">#7888</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Support FITS images with GZIP_1 compression <a href="https://redirect.github.com/python-pillow/Pillow/issues/7894">#7894</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Use I;16 mode for 9-bit JPEG 2000 images <a href="https://redirect.github.com/python-pillow/Pillow/issues/7900">#7900</a> [<a href="https://github.com/scaramallion"><code>@​scaramallion</code></a>]</li>
<li>Raise ValueError if kmeans is negative <a href="https://redirect.github.com/python-pillow/Pillow/issues/7891">#7891</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Remove TIFF tag OSUBFILETYPE when saving using libtiff <a href="https://redirect.github.com/python-pillow/Pillow/issues/7893">#7893</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Raise ValueError for negative values when loading P1-P3 PPM images <a href="https://redirect.github.com/python-pillow/Pillow/issues/7882">#7882</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Added reading of JPEG2000 palettes <a href="https://redirect.github.com/python-pillow/Pillow/issues/7870">#7870</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Added alpha_quality argument when saving WebP images <a href="https://redirect.github.com/python-pillow/Pillow/issues/7872">#7872</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Fixed joined corners for ImageDraw rounded_rectangle() non-integer dimensions <a href="https://redirect.github.com/python-pillow/Pillow/issues/7881">#7881</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Removed Python and NumPy pinning on Cygwin <a href="https://redirect.github.com/python-pillow/Pillow/issues/7880">#7880</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Update UnidentifiedImageError and <strong>version</strong> imports <a href="https://redirect.github.com/python-pillow/Pillow/issues/7644">#7644</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Stop reading EPS image at EOF marker <a href="https://redirect.github.com/python-pillow/Pillow/issues/7753">#7753</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>PSD layer co-ordinates may be negative <a href="https://redirect.github.com/python-pillow/Pillow/issues/7706">#7706</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Use subprocess with CREATE_NO_WINDOW flag in ImageShow WindowsViewer <a href="https://redirect.github.com/python-pillow/Pillow/issues/7791">#7791</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>When saving GIF frame that restores to background color, do not fill identical pixels <a href="https://redirect.github.com/python-pillow/Pillow/issues/7788">#7788</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Fixed reading PNG iCCP compression method <a href="https://redirect.github.com/python-pillow/Pillow/issues/7823">#7823</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Allow writing IFDRational to UNDEFINED tag <a href="https://redirect.github.com/python-pillow/Pillow/issues/7840">#7840</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Fix logged tag name when loading Exif data <a href="https://redirect.github.com/python-pillow/Pillow/issues/7842">#7842</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Use maximum frame size in IHDR chunk when saving APNG images <a href="https://redirect.github.com/python-pillow/Pillow/issues/7821">#7821</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Prevent opening P TGA images without a palette <a href="https://redirect.github.com/python-pillow/Pillow/issues/7797">#7797</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Use palette when loading ICO images <a href="https://redirect.github.com/python-pillow/Pillow/issues/7798">#7798</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Use consistent arguments for load_read and load_seek <a href="https://redirect.github.com/python-pillow/Pillow/issues/7713">#7713</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Turn off nullability warnings for macOS SDK <a href="https://redirect.github.com/python-pillow/Pillow/issues/7827">#7827</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Fix shift-sign issue in Convert.c <a href="https://redirect.github.com/python-pillow/Pillow/issues/7838">#7838</a> [<a href="https://github.com/r-barnes"><code>@​r-barnes</code></a>]</li>
<li>winbuild: Refactor dependency versions into constants <a href="https://redirect.github.com/python-pillow/Pillow/issues/7843">#7843</a> [<a href="https://github.com/hugovk"><code>@​hugovk</code></a>]</li>
<li>Build macOS arm64 wheels natively <a href="https://redirect.github.com/python-pillow/Pillow/issues/7852">#7852</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Fixed typo <a href="https://redirect.github.com/python-pillow/Pillow/issues/7855">#7855</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Open 16-bit grayscale PNGs as I;16 <a href="https://redirect.github.com/python-pillow/Pillow/issues/7849">#7849</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Handle truncated chunks at the end of PNG images <a href="https://redirect.github.com/python-pillow/Pillow/issues/7709">#7709</a> [<a href="https://github.com/lajiyuan"><code>@​lajiyuan</code></a>]</li>
<li>Match mask size to pasted image size in GifImagePlugin <a href="https://redirect.github.com/python-pillow/Pillow/issues/7779">#7779</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Changed SupportsGetMesh protocol to be public <a href="https://redirect.github.com/python-pillow/Pillow/issues/7841">#7841</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Release GIL while calling <code>WebPAnimDecoderGetNext</code> <a href="https://redirect.github.com/python-pillow/Pillow/issues/7782">#7782</a> [<a href="https://github.com/evanmiller"><code>@​evanmiller</code></a>]</li>
<li>Fixed reading FLI/FLC images with a prefix chunk <a href="https://redirect.github.com/python-pillow/Pillow/issues/7804">#7804</a> [<a href="https://github.com/twolife"><code>@​twolife</code></a>]</li>
<li>Updated package name for Tidelift <a href="https://redirect.github.com/python-pillow/Pillow/issues/7810">#7810</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
<li>Removed unused code <a href="https://redirect.github.com/python-pillow/Pillow/issues/7744">#7744</a> [<a href="https://github.com/radarhere"><code>@​radarhere</code></a>]</li>
</ul>
<!-- raw HTML omitted -->
</blockquote>
<p>... (truncated)</p>
</details>
<details>
<summary>Changelog</summary>
<p><em>Sourced from <a href="https://github.com/python-pillow/Pillow/blob/main/CHANGES.rst">pillow's changelog</a>.</em></p>
<blockquote>
<h2>10.3.0 (2024-04-01)</h2>
<ul>
<li>
<p>CVE-2024-28219: Use <code>strncpy</code> to avoid buffer overflow <a href="https://redirect.github.com/python-pillow/Pillow/issues/7928">#7928</a>
[radarhere, hugovk]</p>
</li>
<li>
<p>Deprecate <code>eval()</code>, replacing it with <code>lambda_eval()</code> and <code>unsafe_eval()</code> <a href="https://redirect.github.com/python-pillow/Pillow/issues/7927">#7927</a>
[radarhere, hugovk]</p>
</li>
<li>
<p>Raise <code>ValueError</code> if seeking to greater than offset-sized integer in TIFF <a href="https://redirect.github.com/python-pillow/Pillow/issues/7883">#7883</a>
[radarhere]</p>
</li>
<li>
<p>Add <code>--report</code> argument to <code>__main__.py</code> to omit supported formats <a href="https://redirect.github.com/python-pillow/Pillow/issues/7818">#7818</a>
[nulano, radarhere, hugovk]</p>
</li>
<li>
<p>Added RGB to I;16, I;16L, I;16B and I;16N conversion <a href="https://redirect.github.com/python-pillow/Pillow/issues/7918">#7918</a>, <a href="https://redirect.github.com/python-pillow/Pillow/issues/7920">#7920</a>
[radarhere]</p>
</li>
<li>
<p>Fix editable installation with custom build backend and configuration options <a href="https://redirect.github.com/python-pillow/Pillow/issues/7658">#7658</a>
[nulano, radarhere]</p>
</li>
<li>
<p>Fix putdata() for I;16N on big-endian <a href="https://redirect.github.com/python-pillow/Pillow/issues/7209">#7209</a>
[Yay295, hugovk, radarhere]</p>
</li>
<li>
<p>Determine MPO size from markers, not EXIF data <a href="https://redirect.github.com/python-pillow/Pillow/issues/7884">#7884</a>
[radarhere]</p>
</li>
<li>
<p>Improved conversion from RGB to RGBa, LA and La <a href="https://redirect.github.com/python-pillow/Pillow/issues/7888">#7888</a>
[radarhere]</p>
</li>
<li>
<p>Support FITS images with GZIP_1 compression <a href="https://redirect.github.com/python-pillow/Pillow/issues/7894">#7894</a>
[radarhere]</p>
</li>
<li>
<p>Use I;16 mode for 9-bit JPEG 2000 images <a href="https://redirect.github.com/python-pillow/Pillow/issues/7900">#7900</a>
[scaramallion, radarhere]</p>
</li>
<li>
<p>Raise ValueError if kmeans is negative <a href="https://redirect.github.com/python-pillow/Pillow/issues/7891">#7891</a>
[radarhere]</p>
</li>
<li>
<p>Remove TIFF tag OSUBFILETYPE when saving using libtiff <a href="https://redirect.github.com/python-pillow/Pillow/issues/7893">#7893</a>
[radarhere]</p>
</li>
<li>
<p>Raise ValueError for negative values when loading P1-P3 PPM images <a href="https://redirect.github.com/python-pillow/Pillow/issues/7882">#7882</a>
[radarhere]</p>
</li>
<li>
<p>Added reading of JPEG2000 palettes <a href="https://redirect.github.com/python-pillow/Pillow/issues/7870">#7870</a>
[radarhere]</p>
</li>
<li>
<p>Added alpha_quality argument when saving WebP images <a href="https://redirect.github.com/python-pillow/Pillow/issues/7872">#7872</a>
[radarhere]</p>
</li>
</ul>
<!-- raw HTML omitted -->
</blockquote>
<p>... (truncated)</p>
</details>
<details>
<summary>Commits</summary>
<ul>
<li><a href="https://github.com/python-pillow/Pillow/commit/5c89d88eee199ba53f64581ea39b6a1bc52feb1a"><code>5c89d88</code></a> 10.3.0 version bump</li>
<li><a href="https://github.com/python-pillow/Pillow/commit/63cbfcfdea2d163ec93bae8d283fcfe4b73b5dc7"><code>63cbfcf</code></a> Update CHANGES.rst [ci skip]</li>
<li><a href="https://github.com/python-pillow/Pillow/commit/2776126aa9af322b416eaca247f4f8ebefd08128"><code>2776126</code></a> Merge pull request <a href="https://redirect.github.com/python-pillow/Pillow/issues/7928">#7928</a> from python-pillow/lcms</li>
<li><a href="https://github.com/python-pillow/Pillow/commit/aeb51cbb169eb3285818ba1390ddf2771d897e6e"><code>aeb51cb</code></a> Merge branch 'main' into lcms</li>
<li><a href="https://github.com/python-pillow/Pillow/commit/5beb0b66648db8b542bb5260eed79b25e33d643b"><code>5beb0b6</code></a> Update CHANGES.rst [ci skip]</li>
<li><a href="https://github.com/python-pillow/Pillow/commit/cac6ffa7b399ea79b6239984d1307056a0b19af2"><code>cac6ffa</code></a> Merge pull request <a href="https://redirect.github.com/python-pillow/Pillow/issues/7927">#7927</a> from python-pillow/imagemath</li>
<li><a href="https://github.com/python-pillow/Pillow/commit/f5eeeacf7539eaa0d93a677d7666bc7c142c8d1c"><code>f5eeeac</code></a> Name as 'options' in lambda_eval and unsafe_eval, but '_dict' in deprecated eval</li>
<li><a href="https://github.com/python-pillow/Pillow/commit/facf3af93dabcbdd8cdbda8c3b50eefafa3bb04c"><code>facf3af</code></a> Added release notes</li>
<li><a href="https://github.com/python-pillow/Pillow/commit/2a93aba5cfcf6e241ab4f9392c13e3b74032c061"><code>2a93aba</code></a> Use strncpy to avoid buffer overflow</li>
<li><a href="https://github.com/python-pillow/Pillow/commit/a670597bc30e9d489656fc9d807170b8f3d7ca57"><code>a670597</code></a> Update CHANGES.rst [ci skip]</li>
<li>Additional commits viewable in <a href="https://github.com/python-pillow/Pillow/compare/10.2.0...10.3.0">compare view</a></li>
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
- `@dependabot ignore <dependency name> major version` will close this group update PR and stop Dependabot creating any more for the specific dependency's major version (unless you unignore this specific dependency's major version or upgrade to it yourself)
- `@dependabot ignore <dependency name> minor version` will close this group update PR and stop Dependabot creating any more for the specific dependency's minor version (unless you unignore this specific dependency's minor version or upgrade to it yourself)
- `@dependabot ignore <dependency name>` will close this group update PR and stop Dependabot creating any more for the specific dependency (unless you unignore this specific dependency or upgrade to it yourself)
- `@dependabot unignore <dependency name>` will remove all of the ignore conditions of the specified dependency
- `@dependabot unignore <dependency name> <ignore condition>` will remove the ignore condition of the specified dependency and ignore conditions
You can disable automated security fix PRs for this repo from the [Security Alerts page](https://github.com/hyperledger/aries-acapy-plugins/network/alerts).

</details>