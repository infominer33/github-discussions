---
title: "credential-trust-establishment/issue/8: User can backup and restore Wallet (KMM)"
date: 2023-05-25 22:58:54 +0000
author: urosmrvic-iohk
categories: ["DIF"]
tags: ["credential-trust-establishment"]
permalink: /credential-trust-establishment/issue/8/
comments_file: DIF-credential-trust-establishment-issue-8_comments
excerpt: >
  Accidental close; re-opened in case any questions.
---

Context | Functionality for backup and restoring wallet data will be available in the KMM SDK
-- | --
Enable developers to create wallets that will allow the secure backup and restoration of wallets including all of the wallet data
S&T TBD
We believe that -for wallet users  we will provide functionality to allow them to easily and securely backup and restore their wallet (and its data)and we’ll know this is true when we see:Users can easily backup their wallet (and its data) as an encrypted backup file Users can install a wallet on another device and using the seed can restore their wallet (and its data) Wallet data is encrypted to backup and includes keys, credentials, messages, dids, did-pairsWallet data is decrypted and restored from backup and includes keys, credentials, messages, dids, did-pairs
BDD ExampleScenario: Backup wallet data as an encrypted file Given the user has a wallet with data (keys, credentials, messages, dids, did-pairs) When the user initiates a backup operation Then the wallet data is encrypted And saved as a backup file  Scenario: Restore wallet data from an encrypted backup file using a seed Given the user has an encrypted wallet backup file And the user has the seed for the wallet When the user initiates a restore operation on another device Then the wallet data is decrypted And the wallet (including keys, credentials, messages, dids, did-pairs) is restored accurately  Scenario: Validate encryption of wallet data during backup Given the user initiates a backup operation for their wallet When the backup file is created Then the backup file should not be readable without proper decryption And include all wallet data (keys, credentials, messages, dids, did-pairs)  Scenario: Validate decryption and integrity of wallet data during restoration Given the user has an encrypted backup file and the correct seed When the user restores the wallet on a new device Then all wallet data (keys, credentials, messages, dids, did-pairs) is decrypted and restored accurately And matches the original wallet's data before backup  Scenario: Security of the backup file Given the user has created a backup file of their wallet When an unauthorized person accesses the backup file Then they should not be able to decrypt the wallet data without the seed
N/A
Release notes -Prism documentation -
 


Context | Functionality for backup and restoring wallet data will be available in the KMM SDK
-- | --
Enable developers to create wallets that will allow the secure backup and restoration of wallets including all of the wallet data
S&T TBD
We believe that -for wallet users  we will provide functionality to allow them to easily and securely backup and restore their wallet (and its data)and we’ll know this is true when we see:Users can easily backup their wallet (and its data) as an encrypted backup file Users can install a wallet on another device and using the seed can restore their wallet (and its data) Wallet data is encrypted to backup and includes keys, credentials, messages, dids, did-pairsWallet data is decrypted and restored from backup and includes keys, credentials, messages, dids, did-pairs
BDD ExampleScenario: Backup wallet data as an encrypted file Given the user has a wallet with data (keys, credentials, messages, dids, did-pairs) When the user initiates a backup operation Then the wallet data is encrypted And saved as a backup file  Scenario: Restore wallet data from an encrypted backup file using a seed Given the user has an encrypted wallet backup file And the user has the seed for the wallet When the user initiates a restore operation on another device Then the wallet data is decrypted And the wallet (including keys, credentials, messages, dids, did-pairs) is restored accurately  Scenario: Validate encryption of wallet data during backup Given the user initiates a backup operation for their wallet When the backup file is created Then the backup file should not be readable without proper decryption And include all wallet data (keys, credentials, messages, dids, did-pairs)  Scenario: Validate decryption and integrity of wallet data during restoration Given the user has an encrypted backup file and the correct seed When the user restores the wallet on a new device Then all wallet data (keys, credentials, messages, dids, did-pairs) is decrypted and restored accurately And matches the original wallet's data before backup  Scenario: Security of the backup file Given the user has created a backup file of their wallet When an unauthorized person accesses the backup file Then they should not be able to decrypt the wallet data without the seed
N/A
Release notes -Prism documentation -
 


Context | Functionality for backup and restoring wallet data will be available in the KMM SDK
-- | --
Enable developers to create wallets that will allow the secure backup and restoration of wallets including all of the wallet data
S&T TBD
We believe that -for wallet users  we will provide functionality to allow them to easily and securely backup and restore their wallet (and its data)and we’ll know this is true when we see:Users can easily backup their wallet (and its data) as an encrypted backup file Users can install a wallet on another device and using the seed can restore their wallet (and its data) Wallet data is encrypted to backup and includes keys, credentials, messages, dids, did-pairsWallet data is decrypted and restored from backup and includes keys, credentials, messages, dids, did-pairs
BDD ExampleScenario: Backup wallet data as an encrypted file Given the user has a wallet with data (keys, credentials, messages, dids, did-pairs) When the user initiates a backup operation Then the wallet data is encrypted And saved as a backup file  Scenario: Restore wallet data from an encrypted backup file using a seed Given the user has an encrypted wallet backup file And the user has the seed for the wallet When the user initiates a restore operation on another device Then the wallet data is decrypted And the wallet (including keys, credentials, messages, dids, did-pairs) is restored accurately  Scenario: Validate encryption of wallet data during backup Given the user initiates a backup operation for their wallet When the backup file is created Then the backup file should not be readable without proper decryption And include all wallet data (keys, credentials, messages, dids, did-pairs)  Scenario: Validate decryption and integrity of wallet data during restoration Given the user has an encrypted backup file and the correct seed When the user restores the wallet on a new device Then all wallet data (keys, credentials, messages, dids, did-pairs) is decrypted and restored accurately And matches the original wallet's data before backup  Scenario: Security of the backup file Given the user has created a backup file of their wallet When an unauthorized person accesses the backup file Then they should not be able to decrypt the wallet data without the seed
N/A
 

