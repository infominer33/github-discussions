---
title: "vc-data-model/issue/1432: DIDComm Message Decryption + Disruption by `eth_getLogs`/`eth_getChainId` calls"
date: 2024-02-03 18:43:05 +0000
author: radleylewis
categories: ["Hyperledger"]
tags: ["vc-data-model"]
permalink: /vc-data-model/issue/1432/
comments_file: Hyperledger-vc-data-model-issue-1432_comments
---

[_https://github.com/w3c/vc-data-model/issues/1432_](https://github.com/w3c/vc-data-model/issues/1432)

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
