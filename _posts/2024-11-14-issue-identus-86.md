---
title: "Cardano Connector for SDK"
date: 2024-11-14 16:12:54 +0000
author: FabioPinheiro
excerpt: >
  The edge agent does not require to be in a chrome extension. BUT, our SDK must talk cip-30 if that makes sense and be able to communicate with other cardano wallets to create and submit cardano transactions, starting by the prism did operations + their corresponding metadata
categories: hyperledger
tags: identus
comments_file: identus-issue-86_comments
permalink: /identus/86/
url: https://github.com/hyperledger/identus/issues/86
last_modified_at: 2024-11-26 11:18:46 +0000
---


**URL:** https://github.com/hyperledger/identus/issues/86

### Short Description

A connector for the SDKs to submit the PRISM Block to the Cardano Blockchain.



### Value statement

As a community we already agreed this is value coming from the discussion in https://github.com/hyperledger/identus/discussions/80

But just the summarize:

The PRISM Node can be view as a Cardano Connector. But is a component that is able to do much more that simple submit transaction with metadata.
But this is a very common use case in Cardano.

The value of this come from bypassing this dedicated component of the `did:prism` method. With a generic component that uses infrastructure that already exists and that is largely available. 


Again, the ONLY concern that we care about in here is the **Writing Path**.
We don't care about the status of DID in here. But to create valid PRISM Block you need to know the status of the DID. For that you have the **Reading Path**. Both PRISM Node or the universal resolver cover that.
For example when you create a new `did:prism` you already know the state of the DID, because it is no existed.


So let's split responsibility:
- The SDKs needs to produce the bytes that constitute a valid PRISM Block.
  Note the PRISM Block is already sign with the private keys if the DID, so the Keys is never shared with the connector.
- The Cardano Connector receive the bytes of the PRISM Block (which is a protobuf) and create a transactions with those bytes on the metadata and a metadata id `21325`.
  See Appendix A & B on the [PRISM DID method specs](https://github.com/input-output-hk/prism-did-method-spec/blob/main/w3c-spec/PRISM-method.md) for more for more information.
- Private keys. There are you two pairs of Private keys, one is the Master key on the DID and another is the key of the wallet.
  - The Master private key of the DID is never shared with the Connector. This key is used to sign the PRISM Object in order to make the PRISM Block.
  - The private key of the wallet its also never shared to other components. This key is used to sign the Cardano transactions.

I propose we do a proof of concept of a connector that will be a Chrome extension and use the TS SDK to call the Lace wallet and make a transaction via the Lace wallet.

The idea is to explore CIP30 API and try to build from there https://cips.cardano.org/cip/CIP-30

### Components

Proof of concept for a new company Component
Writing path of the `did:prism` method using the TS SDK