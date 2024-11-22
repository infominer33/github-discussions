---
title: "acapy/issue/3343: DID Management Proposed Update"
date: 2024-11-19 16:58:08 +0000
author: dbluhm
categories: ["OWF"]
tags: ["acapy"]
permalink: /acapy/issue/3343/
comments_file: OWF-acapy-issue-3343_comments
---

[_https://github.com/openwallet-foundation/acapy/issues/3343_](https://github.com/openwallet-foundation/acapy/issues/3343)

In light of our current push to add support for more DID Methods to ACA-Py, some primitives within ACA-Py need some updates. This issue outlines the updates I propose. I plan to update this further as the topic is discussed or as implementations better inform decisions.

# Proposed Updates

## DID Storage (updating `DIDInfo`)

### Current State
At present, the DIDInfo object looks like this:

https://github.com/openwallet-foundation/acapy/blob/f5c49b0710dd180ea31c45f73bc82ef06f9523b4/acapy_agent/wallet/did_info.py#L20-L29

This is stored in the wallet with a category of `did`, the primary identifier being the DID value, and the following tags:
- `method`: the method name
- `verkey`: the `verkey` element of the tuple where it is the base58 encoding of the public key
- `verkey_type`: the key type of the verkey (e.g. `ed25519`)

As currently used, metadata will include:
- `posted`: a boolean value representing whether this did has been published to an indy network
- `endpoint`: a string value representing associated with the endpoint attrib of this did on an indy network.

### Evaluation

As is plain to see, the structure, tags, and metadata of the `DIDInfo` object are very Indy-oriented. This structure has been in use for years.

Currently, ACA-Py will retrieve a `DIDInfo` object in order to use the key associated with the "DID." It will do this by taking a "DID" as input (usually, actually more like a "nym" value, i.e. 16 base58 encoded bytes without a `did:` prefix), then using the `verkey` value to retrieve a `Key` object that it can then use to perform a signature or pack a DIDComm message.

### Solution

DIDs should have multiple keys associated with them rather than a single key. To achieve this while also having an efficient lookup mechanism, we should reorient our storage as outlined below.

#### Quick background on Askar

[Askar](https://github.com/openwallet-foundation/askar) is a secure storage solution used by ACA-Py. Askar encrypts all data and provides a tagging mechanism to enable lookup of encrypted records. An entry in Askar is composed of the following elements:

- **Category:** The major group or "bucket" that the entry belongs to.
- **Name:** The primary identifier for the record; this is roughly equivalent to primary keys on a traditional DB table. The most efficient lookup possible is by name.
- **Value:** The value stored in the entry. This is usually a serialized JSON object.
- **Tags:** A mapping of strings to strings or lists of strings. These values can be used with the ["Wallet Query Language (WQL)"](https://github.com/hyperledger-archives/indy-sdk/tree/main/docs/design/011-wallet-query-language) to look up encrypted Askar entries efficiently.

Askar has a dedicated API for storage and retrieval of keys. However, this API is conceptually just a shorthand for record storage and retrieval from a "private" `key` category with the key itself as the value of the entry. Key entries behave almost exactly the same as non-key entries, including names and tags.

#### Key Storage

Building off of Patrick's contributions of managing keys by multikey instead of "verkey," the multikey representation of a key should be the default identifier for keys in the wallet.

- **Name:** multikey representation of the key
- **Tags:**
    - Implicit tag for the `KeyAlg` (automatically included on every key)
    - `did`: the DID (or a list of DIDs) the key is associated with
    - `vm_id`: an absolute DID URL (or a list of DID URLs) representing the verification method ID(s) of the key
    - `rel`: A list of verification relationships as defined by the DID Core spec; e.g. `["authentication", "assertionMethod"]`. This represents the intended use of this key.
    - `alias`: A human-friendly alias (or list of aliases) that can help identify a key to a user

These sets of tags enable us to look up keys with a combination of `did` and `rel`; when these tags are lists, Askar will return all keys that contain the tag filter value in their respective list. This permits the controller to continue to specify just a DID as the issuer/signer/sender of a value without having to know exactly which key ACA-Py should use to perform the operation. This also permits the controller to continue to use the verification method ID directly to specify a key that might not normally be selected first. Additionally, when a specific proof type is desired, Askar can also filter by `KeyAlg` so a simple mapping from proof type to appropriate `KeyAlg`s can efficiently accomplish this filtering.


#### DID Storage

DIDs should be altered to be stored in a way that simply acknowledges that we own the DID and not as the primary key retrieval mechanism.

- **Category:** `did`
- **Name:** the DID itself
- **Value:**
    - ...
- **Tags:**
    - `method`: a string representing the DID Method
    - (Maybe?) `features`: the list of features the DID is capable of
    - Other things it would be valuable to use to look up the DID?

## Migration

Existing ACA-Py wallets should have the following migration performed to accommodate this reorientation:

- Migrate all existing records in the `did` category to the new structure and also duplicate the record to a legacy `nym` category
  - If the `did` value is unqualified, "move" to the new `did` category and map old values onto new, adding `did:sov:` to the front.
  - If the `did` value is unqualified, also create a record in the new `nym` category with a structure matching the original `DIDInfo` object, where a verkey is closely associated with the nym. This should enable us to continue using the builtin Indy support in a way that distinguishes the old from the new.
  - For `did` values that are qualified, move to the new did category and make sure the associated key entries are properly tagged. This will depend on the DID Method. Plugged in DID Methods may need to account for their own DID methods in a separate migration process.
