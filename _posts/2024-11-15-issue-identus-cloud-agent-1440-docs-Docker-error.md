---
title: "identus-cloud-agent/issue/1440: docs/ Docker error"
date: 2024-11-15 01:27:38 +0000
author: mixmix
categories: ["Hyperledger"]
tags: ["identus-cloud-agent"]
permalink: /identus-cloud-agent/issue/1440/
comments_file: Hyperledger-identus-cloud-agent-issue-1440_comments
excerpt: >
  @bvoiturier The docs was no instructions how to build the docker image `atala-structurizr-lite`.  Can you have a look since you create the docker image
---
### Is this a regression?

Yes

### Description

Reading `docs/README.md` there are instructions for seeing swagger docs. They didn't work for me

### Please provide the exception or error you saw

```Markdown
docker compose -f docs/docker-compose.yml up

WARN[0000] /home/projects/IDENTUS/identus-cloud-agent/docs/docker-compose.yml: the attribute `version` is obsolete, it will be ignored, please remove it to avoid potential confusion
[+] Running 1/2
 ✘ atala-structurizr-lite Error pull access denied for atala-struc...                               4.0s
 ⠏ swagger-ui Pulling                                                                               4.0s
Error response from daemon: pull access denied for atala-structurizr-lite, repository does not exist or may require 'docker login': denied: requested access to the resource is denied
```


### Please provide the environment you discovered this bug in

```Markdown
Linux: Debian/Ubuntu 22.04
Docker: version 27.3.1, build ce12230
```


### Anything else?

Note I had to run `docker compose` not `docker-compose` ... i forget why docker split these out / when ... generally it's not a problem to swap those commands but it is a deviation from the documented command to run