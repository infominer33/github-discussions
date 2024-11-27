---
title: "did-jwt/issue/194: Cleanup the GitHub workflows after moving to the GitHub pages"
date: 2021-08-25 04:51:03 +0000
author: yshyn-iohk
categories: ["DIF"]
tags: ["did-jwt"]
permalink: /did-jwt/issue/194/
comments_file: DIF-did-jwt-issue-194_comments
excerpt: >
  ok yeah if it isn't exposed at the signature scheme API level I think it's fine to leave it off then. Thank you @Wind4Greg 
---
The workflow files should be cleaned up: the docker image with the documentation portal and the corresponding helm chart are not needed anymore.