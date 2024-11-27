---
title: "labs/issue/7: Running cargo test shows failure status for most of the test cases"
date: 2024-03-18 16:16:27 +0000
author: vivekjain007
categories: ["DIF"]
tags: ["labs"]
permalink: /labs/issue/7/
comments_file: DIF-labs-issue-7_comments
excerpt: >
  Most likely the Introduction needs to include a paragraph that also defines the Target SDO.    > Target SDO    > TBD
---
Fork repository using main branch and clone it on my system. Then execute following:-

cargo build => successful
cargo test => many test cases reported failed
 
![image](https://github.com/hyperledger/indy-cli-rs/assets/927903/ee77f6cb-b839-4837-bf78-df7adf4328dc)



Build system : Fedora 38
rustc version: rustc 1.72.0 (5680fa18f 2023-08-23)
cargo version: cargo 1.72.0 (103a7ff2e 2023-08-15)

