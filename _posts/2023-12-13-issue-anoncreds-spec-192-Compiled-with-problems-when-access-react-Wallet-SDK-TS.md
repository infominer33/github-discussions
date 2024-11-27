---
title: "anoncreds-spec/issue/192: Compiled with problems when access react Wallet SDK TS"
date: 2023-12-13 19:16:33 +0000
author: c2vn
categories: ["Hyperledger"]
tags: ["anoncreds-spec"]
permalink: /anoncreds-spec/issue/192/
comments_file: Hyperledger-anoncreds-spec-issue-192_comments
excerpt: >
  Yep got it, thanks
---
### Is this a regression?

Yes

### Description

I follow "Running a demo project" guide at https://github.com/input-output-hk/atala-prism-wallet-sdk-ts
then got "Compiled with problems" when access react Wallet SDK TypeScript Demonstration

![image](https://github.com/input-output-hk/atala-prism-wallet-sdk-ts/assets/107251579/7924915a-e482-48b3-b42c-050f0ef2903b)


### Please provide the exception or error you saw

```true
``
`Compiled with problems:
×
ERROR in ../../build/browser/anoncreds-3aba21a7.js 3120:12-57
Module not found: Error: Can't resolve 'anoncreds_bg.wasm' in '/home/cardano/did/atala-prism-wallet-sdk-ts/build/browser'
ERROR in ../../build/browser/didcomm_js-c556b936.js 770:12-58
Module not found: Error: Can't resolve 'didcomm_js_bg.wasm' in '/home/cardano/did/atala-prism-wallet-sdk-ts/build/browser'`
/

from console I saw these log


Failed to compile.

Module not found: Error: Can't resolve 'anoncreds_bg.wasm' in '/home/cardano/did/atala-prism-wallet-sdk-ts/build/browser'
WARNING in ../../node_modules/@atala/apollo/Apollo.js 1766:11-24
Critical dependency: the request of a dependency is an expression

WARNING in ../../node_modules/@atala/apollo/Apollo.js
Module Warning (from ./node_modules/source-map-loader/dist/cjs.js):
Failed to parse source map from '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/common/src/generated/_Arrays.kt' file: Error: ENOENT: no such file or directory, open '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/common/src/generated/_Arrays.kt'

WARNING in ../../node_modules/@atala/apollo/Apollo.js
Module Warning (from ./node_modules/source-map-loader/dist/cjs.js):
Failed to parse source map from '/home/src/commonMain/kotlin/io/iohk/atala/prism/apollo/derivation/HDKeyOptions.kt' file: Error: ENOENT: no such file or directory, open '/home/src/commonMain/kotlin/io/iohk/atala/prism/apollo/derivation/HDKeyOptions.kt'
WARNING in ../../node_modules/@atala/apollo/kotlin-kotlin-stdlib.js
Module Warning (from ./node_modules/source-map-loader/dist/cjs.js):
Failed to parse source map from '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/src/kotlin/ranges/ProgressionIterators.kt' file: Error: ENOENT: no such file or directory, open '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/src/kotlin/ranges/ProgressionIterators.kt'

WARNING in ../../node_modules/@atala/apollo/kotlin-kotlin-stdlib.js
Module Warning (from ./node_modules/source-map-loader/dist/cjs.js):
Failed to parse source map from '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/src/kotlin/ranges/Progressions.kt' file: Error: ENOENT: no such file or directory, open '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/src/kotlin/ranges/Progressions.kt'

WARNING in ../../node_modules/@atala/apollo/kotlin-kotlin-stdlib.js
Module Warning (from ./node_modules/source-map-loader/dist/cjs.js):
Failed to parse source map from '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/src/kotlin/text/Appendable.kt' file: Error: ENOENT: no such file or directory, open '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/src/kotlin/text/Appendable.kt'

WARNING in ../../node_modules/@atala/apollo/kotlin-kotlin-stdlib.js
Module Warning (from ./node_modules/source-map-loader/dist/cjs.js):
Failed to parse source map from '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/src/kotlin/text/Char.kt' file: Error: ENOENT: no such file or directory, open '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/src/kotlin/text/Char.kt'

WARNING in ../../node_modules/@atala/apollo/kotlin-kotlin-stdlib.js
Module Warning (from ./node_modules/source-map-loader/dist/cjs.js):
Failed to parse source map from '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/src/kotlin/text/StringNumberConversions.kt' file: Error: ENOENT: no such file or directory, open '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/src/kotlin/text/StringNumberConversions.kt'

WARNING in ../../node_modules/@atala/apollo/kotlin-kotlin-stdlib.js
Module Warning (from ./node_modules/source-map-loader/dist/cjs.js):
Failed to parse source map from '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/src/kotlin/text/Strings.kt' file: Error: ENOENT: no such file or directory, open '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/src/kotlin/text/Strings.kt'

WARNING in ../../node_modules/@atala/apollo/kotlin-kotlin-stdlib.js
Module Warning (from ./node_modules/source-map-loader/dist/cjs.js):
Failed to parse source map from '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/src/kotlin/util/HashCode.kt' file: Error: ENOENT: no such file or directory, open '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/src/kotlin/util/HashCode.kt'

WARNING in ../../node_modules/@atala/apollo/kotlin-kotlin-stdlib.js
Module Warning (from ./node_modules/source-map-loader/dist/cjs.js):
Failed to parse source map from '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/src/kotlin/util/Lazy.kt' file: Error: ENOENT: no such file or directory, open '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/src/kotlin/util/Lazy.kt'

WARNING in ../../node_modules/@atala/apollo/kotlin-kotlin-stdlib.js
Module Warning (from ./node_modules/source-map-loader/dist/cjs.js):
Failed to parse source map from '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/src/kotlin/util/Preconditions.kt' file: Error: ENOENT: no such file or directory, open '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/src/kotlin/util/Preconditions.kt'

WARNING in ../../node_modules/@atala/apollo/kotlin-kotlin-stdlib.js
Module Warning (from ./node_modules/source-map-loader/dist/cjs.js):
Failed to parse source map from '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/src/kotlin/util/Result.kt' file: Error: ENOENT: no such file or directory, open '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/src/kotlin/util/Result.kt'

WARNING in ../../node_modules/@atala/apollo/kotlin-kotlin-stdlib.js
Module Warning (from ./node_modules/source-map-loader/dist/cjs.js):
Failed to parse source map from '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/src/kotlin/util/Standard.kt' file: Error: ENOENT: no such file or directory, open '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/src/kotlin/util/Standard.kt'

WARNING in ../../node_modules/@atala/apollo/kotlin-kotlin-stdlib.js
Module Warning (from ./node_modules/source-map-loader/dist/cjs.js):
Failed to parse source map from '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/src/kotlin/util/Tuples.kt' file: Error: ENOENT: no such file or directory, open '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/src/kotlin/util/Tuples.kt'

WARNING in ../../node_modules/@atala/apollo/kotlin-kotlin-stdlib.js
Module Warning (from ./node_modules/source-map-loader/dist/cjs.js):
Failed to parse source map from '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/unsigned/src/kotlin/UByte.kt' file: Error: ENOENT: no such file or directory, open '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/unsigned/src/kotlin/UByte.kt'

WARNING in ../../node_modules/@atala/apollo/kotlin-kotlin-stdlib.js
Module Warning (from ./node_modules/source-map-loader/dist/cjs.js):
Failed to parse source map from '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/unsigned/src/kotlin/UByteArray.kt' file: Error: ENOENT: no such file or directory, open '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/unsigned/src/kotlin/UByteArray.kt'

WARNING in ../../node_modules/@atala/apollo/kotlin-kotlin-stdlib.js
Module Warning (from ./node_modules/source-map-loader/dist/cjs.js):
Failed to parse source map from '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/unsigned/src/kotlin/UInt.kt' file: Error: ENOENT: no such file or directory, open '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/unsigned/src/kotlin/UInt.kt'

WARNING in ../../node_modules/@atala/apollo/kotlin-kotlin-stdlib.js
Module Warning (from ./node_modules/source-map-loader/dist/cjs.js):
Failed to parse source map from '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/unsigned/src/kotlin/UIntArray.kt' file: Error: ENOENT: no such file or directory, open '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/unsigned/src/kotlin/UIntArray.kt'

WARNING in ../../node_modules/@atala/apollo/kotlin-kotlin-stdlib.js
Module Warning (from ./node_modules/source-map-loader/dist/cjs.js):
Failed to parse source map from '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/unsigned/src/kotlin/ULong.kt' file: Error: ENOENT: no such file or directory, open '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/unsigned/src/kotlin/ULong.kt'

WARNING in ../../node_modules/@atala/apollo/kotlin-kotlin-stdlib.js
Module Warning (from ./node_modules/source-map-loader/dist/cjs.js):
Failed to parse source map from '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/unsigned/src/kotlin/ULongArray.kt' file: Error: ENOENT: no such file or directory, open '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/unsigned/src/kotlin/ULongArray.kt'

WARNING in ../../node_modules/@atala/apollo/kotlin-kotlin-stdlib.js
Module Warning (from ./node_modules/source-map-loader/dist/cjs.js):
Failed to parse source map from '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/unsigned/src/kotlin/UShort.kt' file: Error: ENOENT: no such file or directory, open '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/unsigned/src/kotlin/UShort.kt'

WARNING in ../../node_modules/@atala/apollo/kotlin-kotlin-stdlib.js
Module Warning (from ./node_modules/source-map-loader/dist/cjs.js):
Failed to parse source map from '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/unsigned/src/kotlin/UStrings.kt' file: Error: ENOENT: no such file or directory, open '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/unsigned/src/kotlin/UStrings.kt'

WARNING in ../../node_modules/@atala/apollo/kotlin-kotlin-stdlib.js
Module Warning (from ./node_modules/source-map-loader/dist/cjs.js):
Failed to parse source map from '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/unsigned/src/kotlin/UnsignedUtils.kt' file: Error: ENOENT: no such file or directory, open '/home/cardano/did/atala-prism-wallet-sdk-ts/node_modules/@atala/apollo/unsigned/src/kotlin/UnsignedUtils.kt'

ERROR in ../../build/browser/anoncreds-3aba21a7.js 3120:12-57
Module not found: Error: Can't resolve 'anoncreds_bg.wasm' in '/home/cardano/did/atala-prism-wallet-sdk-ts/build/browser'

ERROR in ../../build/browser/didcomm_js-c556b936.js 770:12-58
Module not found: Error: Can't resolve 'didcomm_js_bg.wasm' in '/home/cardano/did/atala-prism-wallet-sdk-ts/build/browser'

webpack compiled with 2 errors and 220 warnings
No issues found.
```


### Please provide the environment you discovered this bug in

```true
I am running in Ubuntu 20.4 and follow Running a demo project guide at https://github.com/input-output-hk/atala-prism-wallet-sdk-ts
```


### Anything else?

Please not that service is still running
![image](https://github.com/input-output-hk/atala-prism-wallet-sdk-ts/assets/107251579/f5e68d40-6aab-41cd-895f-ba30539a03a8)
