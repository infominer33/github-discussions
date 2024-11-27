---
title: "indy-vdr/issue/324: [Expo SDK 52][Android] failing with CMake Error at CMakeLists.txt:30 (add_library):"
date: 2024-08-29 16:38:05 +0000
author: sairanjit
categories: ["DIF"]
tags: ["indy-vdr"]
permalink: /indy-vdr/issue/324/
comments_file: DIF-indy-vdr-issue-324_comments
excerpt: >
  [Expo 52](https://expo.dev/changelog/2024/11-12-sdk-52) comes with RN 0.76 where a whole new architecture is being enabled by default. So, I believe askar and/or the wrapper will need some tweak
---
After adding the `@hyperledger/aries-askar-react-native` facing issue in building the package in expo version 52 in android 

```
CMake Error at CMakeLists.txt:30 (add_library):
    Target "ariesaskarreactnative" links to target
    "ReactAndroid::reactnativejni" but the target was not found.  Perhaps a
    find_package() call is missing for an IMPORTED target, or an ALIAS target
    is missing?
```