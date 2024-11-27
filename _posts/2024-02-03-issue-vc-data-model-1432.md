---
title: "DIDComm Message Decryption + Disruption by `eth_getLogs`/`eth_getChainId` calls"
date: 2024-02-03 18:43:05 +0000
author: radleylewis
excerpt: >
  I can venture some guesses as to what's happening but without a sample to reproduce the issue it'll be harder to provide a clear solution.
  
  #### The calls to the network:
    * `eth_getLogs` is needed by the ethr-did-resolver to resolve a `did:ethr`.
      **The more history a `did:ethr` has, the more calls to getLogs it will require to resolve**.
    * `eth_chainId` is used by `ethers` to confirm that the call is going to the right chain. This can be reduced by creating the `provider` outside of Veramo and supplying it in the configuration for `ethr-did-resolver` instead of the `rpcUrl`. the provider should use the `staticNetwork` option like so:
   ```ts
  import { getResolver } from 'ethr-did-resolver'
  
  // see https://chainlist.org/ for more RPC options
  const SEPOLIA_RPC_URL =  `https://ethereum-sepolia-rpc.publicnode.com`;
  const SEPOLIA_CHAIN_ID = 11155111;
  const network = Network.from(SEPOLIA_CHAIN_ID);
  const provider = new JsonRpcProvider(SEPOLIA_RPC_URL, network, { staticNetwork: network });
  const ethrResolver = getResolver({
    networks: [{
        chainId: SEPOLIA_CHAIN_ID,
        name: 'sepolia',
        registry: '0x03d5003bf0e79C5F5223588F347ebA39AfbC3818',
        legacyNonce: false,
        provider: provider
      }]
  });
  ```
  
  #### The long decrypting time.
  This is very hard to pinpoint without a sample JWE+privateKey to try it locally, BUT there may be some things you can do to speed things up.
  I suspect that a major slowdown is the DID resolution. For a JWE that's encrypted using `authcrypt`, at least 2 DID resolutions take place: one for the sender and one for the receiver DID. For `anoncrypt` only the receiver DID is resolved.
  This is compounded by the fact that `@veramo/did-comm` doesn't use any sort of caching for the DID resolution, as it relies on the functionality from `@veramo/did-resolver`. Our examples don't show how to use caching for DID resolution as we don't have a smart caching layer (yet) and it may lead to DIDs resolving to older versions even after calls to `didManagerAddKey` and other methods that should update them.
  
  ```ts
  import { Resolver } from 'did-resolver'
  
  const resolver = new Resolver({ 
    ...ethrResolver,  // use the ethr resolver configured earlier
    // ... other resolvers here
  }, { cache: true }); // <<< ENABLE CACHING FOR DID RESOLUTION
  
  const agent = createAgent({
    plugins: [
       new DIDResolverPlugin({ resolver: resolver })
       // ... other plugins
    ],
  })
  ```
  
  You can implement your own caching mechanism. See how the inMemoryCache is implemented [here](https://github.com/decentralized-identity/did-resolver/blob/cc1326de0223d3bcefeef1e5d99449fda4d25c14/src/resolver.ts#L236). Then, instead of supplying `{ cache: true }` to the `Resolver` options, you use `{ cache: YourOwnCachingLayer }`
  
  #### Notes
  Configuring an agent like above will result in DID documents that are cached for the lifetime of the `Resolver` instance, which might not be desirable, but you have some options:
  * Veramo agents are free to create, so you can create a new agent with DID caching just for JWE decryption (and all other configs can remain the same)
  * Implement your own caching mechanism and clear the cache after calling `agent.didManager...()` methods.
  
  
  Long term, the did:ethr resolver should have its own caching layer for the results of `evm_getLogs` as the logs it uses to build up DID documents can be safely cached. Since it's an append-only list of events, there should be no need to invalidate the cache to purge older events.
  
  ---
  I hope this helps. Please provide updates if you implement these suggestions as you're surely not the only ones encountering this
categories: w3c
tags: vc-data-model
comments_file: vc-data-model-issue-1432_comments
permalink: /vc-data-model/1432/
url: https://github.com/w3c/vc-data-model/issues/1432
last_modified_at: 2024-11-18 12:03:13 +0000
---


**URL:** https://github.com/w3c/vc-data-model/issues/1432

**Problem**

In our use case we are decrypting didcomm messages within the context of our custom MetaMask Snap. This process is quite time consuming (up to approx. 100 seconds). Our specific use case does not invoke calls to the network, however, Veramo (via the provider) does invoke the `eth_getLogs` and `eth_getChainId` calls using `ethers`. In the case of their failure (i.e. in the case the RPC provider comes back with an error, for example, a rate limit), the long running decryption process (i.e. the decryption) is interrupted. Therefore, there are two components to this issue we are facing:

1. _Decryption Time:_ Why would the decryption take so long? In our case decrypting the DIDComm message (`jwe` encoded) takes around or over 100 seconds;
2. _Error Handling/Unnecessary Calls:_ Where calls to the network are not required, such as the case described above, what is the case for these calls?

**Solution**

As it relates to the _decryption time_ any feedback or insight you can provide on the matter is greatly appreciated. As it pertains to the provider calls on `eth_getChainId` and `eth_getLogs` errors bubbling up and cancelling the other processes - even when the aforementioned calls do not appear to be required - it would appear that these could be deactivated. 

**Other Questions**

Any information you can provide on this is greatly appreciated. If we can align on the solution, we would be happy to present a PR, but wanted to sync up here first. 

**Screenshot**
Example of offending calls within the background.html in the MetaMask Snap. 
![image](https://github.com/user-attachments/assets/eec20ac7-2bf1-4f7b-907b-aeda3b4a447d)
