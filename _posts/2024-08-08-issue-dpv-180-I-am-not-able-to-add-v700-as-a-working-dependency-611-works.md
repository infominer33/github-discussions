---
title: "dpv/issue/180: I am not able to add v7.0.0 as a working dependency, 6.1.1 works"
date: 2024-08-08 14:38:47 +0000
author: coveloper
categories: ["Hyperledger"]
tags: ["dpv"]
permalink: /dpv/issue/180/
comments_file: Hyperledger-dpv-issue-180_comments
excerpt: >
  Note, that v6.1.1 does not actually compile, but the SPM appears to install correctly.
---
### Is this a regression?

Yes

### Description

If I add v7.0.0 as a Package Dependency, it never fully resolves, leaving me in a state where I can't link it to my target, or import it into Swift files.

This works fine with v6.1.1

### Please provide the exception or error you saw

```true
When adding the Swift SDK as a Package Dependency, it should resolve all the packages and it should show the display name of the package.  The package list should allow me to open each package and see its contents. This does not happen with v7.0.0 for me.

v6.1.1 works fine.
```


### Please provide the environment you discovered this bug in

```true
Using from the 7.0.0 Tag in Xcode Package Dependency screen
```


### Anything else?

Here is how my Package Dependency screen looks when I tag it to 7.0.0:
<img width="774" alt="IdentusSDK-7 0 0-DoesNotLoadCorrectly" src="https://github.com/user-attachments/assets/9931473c-80a3-4515-a2bc-2e78b3114633">

You can see that the packages aren't fully resolved:
<img width="340" alt="IdentusSDK-7 0 0-DoesNotLoadAllPackages" src="https://github.com/user-attachments/assets/ff9d57d2-0a3b-4363-a251-94a2b90373af">

v6.1.1 works fine, shows up as it's name "EdgeAgentSDK" (not the slug name) :
<img width="825" alt="EdgeAgent-6 1 1-LoadsCorrectly" src="https://github.com/user-attachments/assets/d929696a-7b98-42ea-9807-2a2f19f6e5e3">
And 6.1.1 can be found when I add it to my Target, 7.0.0 does not load fully so it's not available to this menu.
<img width="232" alt="EdgeAgent-6 1 1-availableToTarget" src="https://github.com/user-attachments/assets/d30cdb3b-5a4b-4c7a-8b55-8b0fd64a120c">


