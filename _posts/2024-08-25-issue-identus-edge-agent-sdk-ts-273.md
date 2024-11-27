---
title: "npm install fails"
date: 2024-08-25 23:32:42 +0000
author: mixmix
excerpt: >
  As discussed for user stories, and in the new introduction to user stories, the functional is the \"Why\" (purpose/motivation) and the technical is the \"What\" (capability).  We can also add the SWEBOK reference for definitions to fully resolve this.
categories: hyperledger
tags: identus-edge-agent-sdk-ts
comments_file: identus-edge-agent-sdk-ts-issue-273_comments
permalink: /identus-edge-agent-sdk-ts/273/
url: https://github.com/hyperledger/identus-edge-agent-sdk-ts/issues/273
last_modified_at: 2024-11-13 12:59:18 +0000
---


**URL:** https://github.com/hyperledger/identus-edge-agent-sdk-ts/issues/273

### Is this a regression?

Yes

### Description

Doesn't install happily on a fresh install with npm. Seems to be some typedoc version problems in your repo

### Please provide the exception or error you saw

```true
➜  ATALA cd test
➜  test npm init -y
Wrote to /home/fakename/projects/ATALA/test/package.json:

{
  "name": "test",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC"
}


➜  test npm i @hyperledger/identus-edge-agent-sdk
npm WARN deprecated inflight@1.0.6: This module is not supported, and leaks memory. Do not use it. Check out lru-cache if you want a good and tested way to coalesce async requests by a key value, which is much more comprehensive and powerful.
npm WARN deprecated rimraf@2.7.1: Rimraf versions prior to v4 are no longer supported
npm WARN deprecated glob@7.2.3: Glob versions prior to v9 are no longer supported
npm WARN deprecated text-encoding@0.7.0: no longer maintained
npm ERR! code 1
npm ERR! path /home/fakename/projects/ATALA/test/node_modules/@hyperledger/identus-edge-agent-sdk
npm ERR! command failed
npm ERR! command sh -c sh preinstall.sh
npm ERR! running preinstall in /home/fakename/projects/ATALA/test/node_modules/@hyperledger/identus-edge-agent-sdk
npm ERR! npm ERR! code ERESOLVE
npm ERR! npm ERR! ERESOLVE unable to resolve dependency tree
npm ERR! npm ERR!
npm ERR! npm ERR! While resolving: @hyperledger/identus-edge-agent-sdk@6.0.0
npm ERR! npm ERR! Found: typedoc@0.25.13
npm ERR! npm ERR! node_modules/typedoc
npm ERR! npm ERR!   dev typedoc@"^0.25.6" from the root project
npm ERR! npm ERR!
npm ERR! npm ERR! Could not resolve dependency:
npm ERR! npm ERR! peer typedoc@">=0.26 <2.0" from typedoc-plugin-external-module-map@2.1.0
npm ERR! npm ERR! node_modules/typedoc-plugin-external-module-map
npm ERR! npm ERR!   dev typedoc-plugin-external-module-map@"^2.0.1" from the root project
npm ERR! npm ERR!
npm ERR! npm ERR! Fix the upstream dependency conflict, or retry
npm ERR! npm ERR! this command with --force or --legacy-peer-deps
npm ERR! npm ERR! to accept an incorrect (and potentially broken) dependency resolution.
```


### Please provide the environment you discovered this bug in

```true
➜  node -v
v20.10.0
➜  npm -v
10.2.3
```


### Anything else?

:cry: 