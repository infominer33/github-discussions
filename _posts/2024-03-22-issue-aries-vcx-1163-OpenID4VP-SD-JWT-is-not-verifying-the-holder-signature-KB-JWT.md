---
title: "aries-vcx/issue/1163: OpenID4VP SD-JWT is not verifying the holder signature (KB-JWT)"
date: 2024-03-22 11:12:01 +0000
author: gmulhearn
categories: ["Hyperledger"]
tags: ["aries-vcx"]
permalink: /aries-vcx/issue/1163/
comments_file: Hyperledger-aries-vcx-issue-1163_comments
excerpt: >
  This lead to the development of the \"connectionless\" features for issuance and verification. I'm closing this issue :heart: 
---
I believe the SD-JWT cred processor `verify_presentation` is not actually checking the holder's signature (KB-JWT) on the presented SD-JWT. Meaning the SD-JWT holder does not have to prove they are bound to the SD-JWT. 

I tested this locally by using a malicious client that intentionally malforms the signature bytes of the KB-JWT it produces. The acapy plugin still reported verified=true (credo reported verified=false with logs that indicate the signature was invalid).

I believe this happens because:
* verify_presentation calls sd_jwt_verify with only 2 params; `profile, presentation`: https://github.com/openwallet-foundation/acapy-plugins/blob/main/oid4vc/sd_jwt_vc/cred_processor.py#L205
* `sd_jwt_verify` has 2 additional optional params, expected_aud & expected_nonce. so verify_presentation sets those as `None`
* sd_jwt_verify initializes SDJWTVerifierACAPy with those null values for self.expected_aud & self.expected_nonce
* sd_jwt_verify then calls SDJWTVerifierACAPy.verify(), which checks the SD-JWT VC signature, and then only IF `if self.expected_aud or self.expected_nonce:` does it check the KB JWT:
```
 if self.expected_aud or self.expected_nonce:
            if not (self.expected_aud and self.expected_nonce):
                raise ValueError(
                    "Either both expected_aud and expected_nonce must be provided "
                    "or both must be None"
                )
            await self._verify_key_binding_jwt(
                self.expected_aud,
                self.expected_nonce,
            )
```
* meaning the KB-JWT signature (holder binding/proof) is not checked
