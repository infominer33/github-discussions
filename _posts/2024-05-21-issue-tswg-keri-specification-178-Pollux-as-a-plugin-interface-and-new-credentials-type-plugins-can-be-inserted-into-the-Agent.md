---
title: "tswg-keri-specification/issue/178: Pollux as a plugin interface and new credentials type plugins can be inserted into the Agent"
date: 2024-05-21 14:59:32 +0000
author: goncalo-frade-iohk
categories: ["Hyperledger"]
tags: ["tswg-keri-specification"]
permalink: /tswg-keri-specification/issue/178/
comments_file: Hyperledger-tswg-keri-specification-issue-178_comments
excerpt: >
  PR #179 has been merged to address this issue, closing.
---
### Proposed feature

Pollux will become a plugin interface, this will enable more control over the available credentials type that can be used by the agent. It will as well enable developers to provide their own Plugins for credential types that are not by default supported by the Agent.

### Feature description

Pollux will become more inline with a plugin interface. 
It will be adapted so each plugin as versioning and version support.
Each plugin can identify itself and identify the application/types it supports.

The agent will receive an array of Pollux plugins and pick the plugin that supports a type of credential to run the flow.

### Anything else?

_No response_