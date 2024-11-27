---
title: "Pollux as a plugin interface and new credentials type plugins can be inserted into the Agent"
date: 2024-05-21 14:59:32 +0000
author: goncalo-frade-iohk
excerpt: >
  PR #179 has been merged to address this issue, closing.
categories: trustoverip
tags: tswg-keri-specification
comments_file: tswg-keri-specification-issue-178_comments
permalink: /tswg-keri-specification/178/
url: https://github.com/trustoverip/tswg-keri-specification/issues/178
last_modified_at: 2024-11-18 02:02:08 +0000
---


**URL:** https://github.com/trustoverip/tswg-keri-specification/issues/178

### Proposed feature

Pollux will become a plugin interface, this will enable more control over the available credentials type that can be used by the agent. It will as well enable developers to provide their own Plugins for credential types that are not by default supported by the Agent.

### Feature description

Pollux will become more inline with a plugin interface. 
It will be adapted so each plugin as versioning and version support.
Each plugin can identify itself and identify the application/types it supports.

The agent will receive an array of Pollux plugins and pick the plugin that supports a type of credential to run the flow.

### Anything else?

_No response_