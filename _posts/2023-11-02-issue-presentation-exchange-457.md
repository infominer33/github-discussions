---
title: "Unclear use of `tag` in key derivation and wrapping algorithm"
date: 2023-11-02 18:00:26 +0000
author: jakubkoci
excerpt: >
  Thanks @carez 
  
  I found that DIDComm spec mentions [2.3 Key Derivation for ECDH-1PU Key Agreement](https://datatracker.ietf.org/doc/html/draft-madden-jose-ecdh-1pu-04#section-2.3) for ECDH-1PU and that actually mentions `tag` exactly as your diagram depicts.
  
  But, there is no mention of `tag` in the spec for ECDH-ES I found [4.6  Key Agreement with Elliptic Curve Diffie-Hellman Ephemeral Static (ECDH-ES)](https://datatracker.ietf.org/doc/html/rfc7518?ref=blog.identity.foundation#section-4.6)
  
  So, maybe it's just an incorrect copy-paste of the sentence from ECDH-1PU to ECDH-ES.
  
  I also found a mention of the `tag` in Authenticated encryption part of [Understanding JSON Web Encryption (JWE)](https://www.scottbrady91.com/jose/json-web-encryption).
categories: decentralized-identity
tags: presentation-exchange
comments_file: presentation-exchange-issue-457_comments
permalink: /presentation-exchange/457/
url: https://github.com/decentralized-identity/presentation-exchange/issues/457
last_modified_at: 2024-11-19 20:55:58 +0000
---


**URL:** https://github.com/decentralized-identity/presentation-exchange/issues/457

I don't understand how to use a `tag` in key derivation/wrapping algorithm as described in sections:

- [5.1.9 ECDH-1PU key wrapping and common protected headers](https://identity.foundation/didcomm-messaging/spec/v2.1/#ecdh-1pu-key-wrapping-and-common-protected-headers)
- [5.1.10 ECDH-ES key wrapping and common protected headers](https://identity.foundation/didcomm-messaging/spec/v2.1/#ecdh-es-key-wrapping-and-common-protected-headers)

There is a mention

"As per this requirement, the JWE building must first encrypt the payload, then use the resulting `tag` as part of the key derivation process when wrapping the `cek`."

But I don't see any information on how that tag should be used in derivation of `kek`  or wrapping of `cek` with `kek`. Am I missing something? 