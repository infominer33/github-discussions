---
title: "bbs-signature/issue/322: Wallet recovery with a password-protected backup file (from a single point of failure to 2FA) in addition to Seed Phrase Recovery"
date: 2024-08-05 22:36:40 +0000
author: seira-yun
categories: ["DIF"]
tags: ["bbs-signature"]
permalink: /bbs-signature/issue/322/
comments_file: DIF-bbs-signature-issue-322_comments
excerpt: >
  PR #320 has been merged, closing.
---
### Proposed feature

We propose to contribute to this repository to add a functionality to recover a wallet through a password-protected backup file.

We’ve already implemented this on the Socious Wallet. 

Demos:
Backup wallet flow:
https://drive.google.com/file/d/1ae7t0MfNhgFz4FKy3LfLVfibYimfUgR8/view?usp=drivesdk

Restore wallet with a password-protected backup file flow:
https://drive.google.com/file/d/1qXmEhtN3Z4IEPWdSzdVmRTUZgeOI-mwj/view?usp=drivesdk

## **Problem:** The reliance on seed phrase-based wallet recovery is hindering mass adoption.

The widespread adoption of blockchain wallets is significantly hindered by the use of seed phrases for wallet recovery. Seed phrases, also known as recovery or mnemonic phrases, are a list of words required to recover a blockchain wallet. This applies to both crypto wallets for token transactions and identity wallets for managing Decentralized Identifiers (DIDs) and Verifiable Credentials (VCs). For security reasons, this phrase must be kept confidential[^1^].

**Backgrounds on seed phrases**

Since a private key consists of random binaries, it's not human-readable, so it must be stored digitally. However, due to hacking risks, BIP39 was created to allow these keys to be written down on paper[^2^].

However, the seed phrase being a single point of failure poses several challenges. Firstly, users may forget their seed phrases or misplace the physical copy containing it[^3^]. Secondly, if another person acquires the seed phrase, they can access the wallet and its funds[^4^]. Lastly, non-technical users may find the concept of a seed phrase difficult to comprehend and manage[^5^].

These challenges are discussed in several sources. For instance, [[this Cointelegraph article](https://cointelegraph.com/learn/how-to-recover-a-crypto-wallet)](https://cointelegraph.com/learn/how-to-recover-a-crypto-wallet) states that seed phrase recovery is a hindrance to mass adoption: “As the Web3 space looks to onboard its first billion users, intuitive wallet experiences are critical. Seed phrases are a hindrance to that experience.” In addition, [[this Blockworks article](https://blockworks.co/news/what-are-seed-phrases)](https://blockworks.co/news/what-are-seed-phrases) states that seed phrases have become a “major pain point for users”. 

Currently, the [[Atala PRISM Identity Wallet SDK](https://github.com/input-output-hk/atala-prism-wallet-sdk-ts)](https://github.com/input-output-hk/atala-prism-wallet-sdk-ts) only supports wallet recovery based on seed phrases. This limitation hinders mass adoption.

[^1^]: Nakamoto, S. (2008). Bitcoin: A Peer-to-Peer Electronic Cash System.
[^2^]: Bitcoin Improvement Proposals. (2013). BIP39: Mnemonic code for generating deterministic keys.
[^3^]: Lee, T. B. (2018, August 4). I forgot my PIN: My epic tale of losing $30,000 in bitcoin. ARS Technica.
[^4^]: Hern, A. (2016, March 18). What happens to your bitcoin when you die? The Guardian.
[^5^]: Mearian, L. (2014, February 7). Bitcoin's software gets security fixes, new features. Computerworld.

## Alternatives to seed phrase-based recovery:

Two primary alternatives to seed phrase-based recovery exist: social recovery and multifactor recovery involving backup files. Social recovery, which has been endorsed by Ethereum co-founder Vitalik Buterin[^1^], utilizes trusted contacts to help users regain access to their accounts. A prominent example of a wallet employing this method is the Argent wallet[^2^].

On the other hand, multifactor recovery involves the use of backup files in addition to other authentication measures. Wallets using this method are rare, especially within the Cardano ecosystem. However, some examples do exist outside of it. For instance, the [[Dock.io](http://dock.io/)](http://dock.io/) identity wallet uses a recovery system involving a password-protected backup file[^3^]. Our plan includes implementing a similar solution to enhance the security and user experience of our wallet.

[^1^]: Buterin, V. (2018, January 11). [[A simple and secure wallet](https://vitalik.ca/general/2018/01/11/secure_wallets.html)](https://vitalik.ca/general/2018/01/11/secure_wallets.html).
[^2^]: Argent. (2019, May 13). [[Introducing Argent V1: A new type of Ethereum wallet](https://www.argent.xyz/blog/introducing-argent/)](https://www.argent.xyz/blog/introducing-argent/).
[^3^]: [[Dock.io](http://dock.io/)](http://dock.io/). (2021). [[Wallet Recovery](https://docs.dock.io/learn/wallet-recovery)](https://docs.dock.io/learn/wallet-recovery).

See also: 

https://wirexapp.com/

https://www.cypherock.com/features/no-backup

https://medium.com/@bitizenwallet/private-keys-single-point-of-failure-a20b5f00a67d

## **Solution: We improve the Atala identity wallet SDK to allow wallet recovery using a password-protected backup file instead of a seed phrase.**

The solution aims to address the vulnerability of seed phrases by enhancing the Atala identity wallet SDK to allow wallet recovery using a password-protected backup file instead of a seed phrase. Essentially, this wallet eliminates a single point of failure through the use of two-factor authentication, i.e., a password and a backup file. Consequently, even if someone acquires your backup file, they can't decrypt it without your password. Similarly, a password alone is useless without access to your backup file. Moreover, you can always change your password. Implementing two-factor authentication for recovery significantly improves both security and user experience. 

Wallets with multi-factor authentication are rare, but they do exist outside the Cardano ecosystem. For example, the [[Dock.io](http://dock.io/)](http://dock.io/) identity wallet uses a recovery system with a [[password-protected backup file](https://drive.google.com/file/d/1qatflQ6aDrQOqx8QlBtda5GlnILuckyV/view?usp=drive_link)](https://drive.google.com/file/d/1qatflQ6aDrQOqx8QlBtda5GlnILuckyV/view?usp=drive_link). We plan to implement a similar solution.

Specifically, we will contribute to the [[Atala PRISM Identity Wallet SDK](https://github.com/input-output-hk/atala-prism-wallet-sdk-ts)](https://github.com/input-output-hk/atala-prism-wallet-sdk-ts) repository. We aim to add new features without affecting the existing wallet recovery feature which uses seed phrases. The new features include the following:

- Users do not see seed phrases when creating a wallet.
- Users see an alert: "Please secure your wallet by backing up the wallet".
- Users select a secure password to encrypt the backup file.
- Users have the freedom to save the backup file wherever they prefer, including on an external hard drive or cloud.
- Users can restore a wallet by decrypting the backup file with the password.

This plan has been discussed with IOG's Atala PRISM team. They have confirmed that this improvement is not part of their roadmap and would welcome this additional feature to the SDK.

This solution allows projects in the Cardano ecosystem to create their own wallets using this SDK. They can use a password-protected backup file for wallet recovery. This method is not only user-friendly but also secure. It will contribute to the widespread adoption of identity wallets and Self-Sovereign Identity.

With this enhanced SDK, we'll boost Socious Wallet's security by shifting from seed phrase recovery to multifactor file backup recovery. This will let end-users enjoy the advantages of SSI, DID, and VC without the complexity of managing seed phrases or the risk of a single point of failure. Upon completion of this project, users will have a secure identity wallet on their iOS and Android mobile devices without the need to manage seed phrases.

### Feature description

We propose to contribute to this repository to add a functionality to recover a wallet through a password-protected backup file.

We’ve already implemented this on the Socious Wallet. 

Demos:
Backup wallet flow:
https://drive.google.com/file/d/1ae7t0MfNhgFz4FKy3LfLVfibYimfUgR8/view?usp=drivesdk

Restore wallet with a password-protected backup file flow:
https://drive.google.com/file/d/1qXmEhtN3Z4IEPWdSzdVmRTUZgeOI-mwj/view?usp=drivesdk

## **Problem:** The reliance on seed phrase-based wallet recovery is hindering mass adoption.

The widespread adoption of blockchain wallets is significantly hindered by the use of seed phrases for wallet recovery. Seed phrases, also known as recovery or mnemonic phrases, are a list of words required to recover a blockchain wallet. This applies to both crypto wallets for token transactions and identity wallets for managing Decentralized Identifiers (DIDs) and Verifiable Credentials (VCs). For security reasons, this phrase must be kept confidential[^1^].

**Backgrounds on seed phrases**

Since a private key consists of random binaries, it's not human-readable, so it must be stored digitally. However, due to hacking risks, BIP39 was created to allow these keys to be written down on paper[^2^].

However, the seed phrase being a single point of failure poses several challenges. Firstly, users may forget their seed phrases or misplace the physical copy containing it[^3^]. Secondly, if another person acquires the seed phrase, they can access the wallet and its funds[^4^]. Lastly, non-technical users may find the concept of a seed phrase difficult to comprehend and manage[^5^].

These challenges are discussed in several sources. For instance, [[this Cointelegraph article](https://cointelegraph.com/learn/how-to-recover-a-crypto-wallet)](https://cointelegraph.com/learn/how-to-recover-a-crypto-wallet) states that seed phrase recovery is a hindrance to mass adoption: “As the Web3 space looks to onboard its first billion users, intuitive wallet experiences are critical. Seed phrases are a hindrance to that experience.” In addition, [[this Blockworks article](https://blockworks.co/news/what-are-seed-phrases)](https://blockworks.co/news/what-are-seed-phrases) states that seed phrases have become a “major pain point for users”. 

Currently, the [[Atala PRISM Identity Wallet SDK](https://github.com/input-output-hk/atala-prism-wallet-sdk-ts)](https://github.com/input-output-hk/atala-prism-wallet-sdk-ts) only supports wallet recovery based on seed phrases. This limitation hinders mass adoption.

[^1^]: Nakamoto, S. (2008). Bitcoin: A Peer-to-Peer Electronic Cash System.
[^2^]: Bitcoin Improvement Proposals. (2013). BIP39: Mnemonic code for generating deterministic keys.
[^3^]: Lee, T. B. (2018, August 4). I forgot my PIN: My epic tale of losing $30,000 in bitcoin. ARS Technica.
[^4^]: Hern, A. (2016, March 18). What happens to your bitcoin when you die? The Guardian.
[^5^]: Mearian, L. (2014, February 7). Bitcoin's software gets security fixes, new features. Computerworld.

## Alternatives to seed phrase-based recovery:

Two primary alternatives to seed phrase-based recovery exist: social recovery and multifactor recovery involving backup files. Social recovery, which has been endorsed by Ethereum co-founder Vitalik Buterin[^1^], utilizes trusted contacts to help users regain access to their accounts. A prominent example of a wallet employing this method is the Argent wallet[^2^].

On the other hand, multifactor recovery involves the use of backup files in addition to other authentication measures. Wallets using this method are rare, especially within the Cardano ecosystem. However, some examples do exist outside of it. For instance, the [[Dock.io](http://dock.io/)](http://dock.io/) identity wallet uses a recovery system involving a password-protected backup file[^3^]. Our plan includes implementing a similar solution to enhance the security and user experience of our wallet.

[^1^]: Buterin, V. (2018, January 11). [[A simple and secure wallet](https://vitalik.ca/general/2018/01/11/secure_wallets.html)](https://vitalik.ca/general/2018/01/11/secure_wallets.html).
[^2^]: Argent. (2019, May 13). [[Introducing Argent V1: A new type of Ethereum wallet](https://www.argent.xyz/blog/introducing-argent/)](https://www.argent.xyz/blog/introducing-argent/).
[^3^]: [[Dock.io](http://dock.io/)](http://dock.io/). (2021). [[Wallet Recovery](https://docs.dock.io/learn/wallet-recovery)](https://docs.dock.io/learn/wallet-recovery).

See also: 

https://wirexapp.com/

https://www.cypherock.com/features/no-backup

https://medium.com/@bitizenwallet/private-keys-single-point-of-failure-a20b5f00a67d

## **Solution: We improve the Atala identity wallet SDK to allow wallet recovery using a password-protected backup file instead of a seed phrase.**

The solution aims to address the vulnerability of seed phrases by enhancing the Atala identity wallet SDK to allow wallet recovery using a password-protected backup file instead of a seed phrase. Essentially, this wallet eliminates a single point of failure through the use of two-factor authentication, i.e., a password and a backup file. Consequently, even if someone acquires your backup file, they can't decrypt it without your password. Similarly, a password alone is useless without access to your backup file. Moreover, you can always change your password. Implementing two-factor authentication for recovery significantly improves both security and user experience. 

Wallets with multi-factor authentication are rare, but they do exist outside the Cardano ecosystem. For example, the [[Dock.io](http://dock.io/)](http://dock.io/) identity wallet uses a recovery system with a [[password-protected backup file](https://drive.google.com/file/d/1qatflQ6aDrQOqx8QlBtda5GlnILuckyV/view?usp=drive_link)](https://drive.google.com/file/d/1qatflQ6aDrQOqx8QlBtda5GlnILuckyV/view?usp=drive_link). We plan to implement a similar solution.

Specifically, we will contribute to the [[Atala PRISM Identity Wallet SDK](https://github.com/input-output-hk/atala-prism-wallet-sdk-ts)](https://github.com/input-output-hk/atala-prism-wallet-sdk-ts) repository. We aim to add new features without affecting the existing wallet recovery feature which uses seed phrases. The new features include the following:

- Users do not see seed phrases when creating a wallet.
- Users see an alert: "Please secure your wallet by backing up the wallet".
- Users select a secure password to encrypt the backup file.
- Users have the freedom to save the backup file wherever they prefer, including on an external hard drive or cloud.
- Users can restore a wallet by decrypting the backup file with the password.

This plan has been discussed with IOG's Atala PRISM team. They have confirmed that this improvement is not part of their roadmap and would welcome this additional feature to the SDK.

This solution allows projects in the Cardano ecosystem to create their own wallets using this SDK. They can use a password-protected backup file for wallet recovery. This method is not only user-friendly but also secure. It will contribute to the widespread adoption of identity wallets and Self-Sovereign Identity.

With this enhanced SDK, we'll boost Socious Wallet's security by shifting from seed phrase recovery to multifactor file backup recovery. This will let end-users enjoy the advantages of SSI, DID, and VC without the complexity of managing seed phrases or the risk of a single point of failure. Upon completion of this project, users will have a secure identity wallet on their iOS and Android mobile devices without the need to manage seed phrases.

### Anything else?

_No response_