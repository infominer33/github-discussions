---
title: "bbs-signature/issue/327: test vectors: inconsistency in random scalars"
date: 2024-10-08 00:55:53 +0000
author: NikZak
categories: ["DIF"]
tags: ["bbs-signature"]
permalink: /bbs-signature/issue/327/
comments_file: DIF-bbs-signature-issue-327_comments
---

[_https://github.com/decentralized-identity/bbs-signature/issues/327_](https://github.com/decentralized-identity/bbs-signature/issues/327)

Hi. When I look at [section 8.4.5.2](https://identity.foundation/bbs-signature/draft-irtf-cfrg-bbs-signatures.html#section-8.4.5.2)
or [section 8.4.5.1](https://identity.foundation/bbs-signature/draft-irtf-cfrg-bbs-signatures.html#section-8.4.5.1)
random scalars go as 
```
random scalars:
    r1 = "60ca409f6b0563f687fc471c63d2819f446f39c23bb540925d9d4254ac58f3
          37"
    r2 = "2ceff4982de0c913090f75f081df5ec594c310bb48c17cfdaab5332a682ef8
          11"
    e_tilde = "6101c4404895f3dff87ab39c34cb995af07e7139e6b3847180ffdd1bc
               8c313cd"
    r1_tilde = "0dfcffd97a6ecdebef3c9c114b99d7a030c998d938905f357df62822
                dee072e8"
    r3_tilde = "639e3417007d38e5d34ba8c511e836768ddc2669fdd3faff5c14ad27
                ac2b2da1"
```

When I look at [section 8.4.5.3](https://identity.foundation/bbs-signature/draft-irtf-cfrg-bbs-signatures.html#section-8.4.5.3) random scalars are:
```
random scalars:
    r1 = "44679831fe60eca50938ef0e812e2a9284ad7971b6932a38c7303538b712e4
          57"
    r2 = "6481692f89086cce11779e847ff884db8eebb85a13e81b2d0c79d6c1062069
          d8"
    e_tilde = "721ce4c4c148a1d5826f326af6fd6ac2844f29533ba4127c3a43d222d
               51b7081"
    r1_tilde = "1ecfaf5a079b0504b00a1f0d6fe8857291dd798291d7ad7454b39811
                4393f37f"
    r3_tilde = "0a4b3d59b34707bb9999bc6e2a6d382a2d2e214bff36ecd88639a141
                24b1622e"
    m_tilde_scalars:
        m~_1 = "7217411a9e329c7a5705e8db552274646e2949d62c288d7537dd62bc
                284715e4"
        m~_3 = "67d4d43660746759f598caac106a2b5f58ccd1c3eefaec31841a4f77
                d2548870"
        m~_5 = "715d965b1c3912d20505b381470ff1a528700b673e50ba89fd287e13
                171cc137"
        m~_7 = "4d3281a149674e58c9040fc7a10dd92cb9c7f76f6f0815a1afc3b09d
                74b92fe4"
        m~_8 = "438feebaa5894ca0da49992df2c97d872bf153eab07e08ff73b28131
                c46ff415"
        m~_9 = "602b723c8bbaec1b057d70f18269ae5e6de6197a5884967b03b933fa
                80006121"
```

There are few issues with it. 
First:
How were the first random scalars derived? This is not defined in the standard. I've figured that you can get them by using seeded_random_scalars(SEED, DST, count) where SEED = "332e313431353932363533353839373933323338343632363433333833323739" and DST =
"BBS_BLS12381G1_XMD:SHA-256_SSWU_RO_H2G_HM2S_MOCK_RANDOM_SCALARS_DST_" but I had to make a few guesses to find that. I think this better be defined in the standard.

Second:
How second random scalars are derived, I don't know

I mean you may argue that how the random scalars are derived is not necessary to run the tests. But then why defining `seeded_random_scalars` function and saying that it is used to get random scalars. This function can not be used so the whole section about `seeded_random_scalars` is redundant