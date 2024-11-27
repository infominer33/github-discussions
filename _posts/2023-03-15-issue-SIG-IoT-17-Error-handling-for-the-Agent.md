---
title: "SIG-IoT/issue/17: Error handling for the Agent"
date: 2023-03-15 17:24:28 +0000
author: essbante-io
categories: ["DIF"]
tags: ["SIG-IoT"]
permalink: /SIG-IoT/issue/17/
comments_file: DIF-SIG-IoT-issue-17_comments
excerpt: >
  This was discussed during the [did meeting on 14 November 2024](https://www.w3.org/2024/11/14-did-minutes.html#78c8).    <details><summary><i>View the transcript</i></summary>    <h4><a href=\"https://github.com/w3c/did-resolution/issues/17\" rel=\"noopener noreferrer\">w3c/<wbr>did-resolution#17</a></h4>  <p><cite>markus_sabadello:</cite> How DID resolution relates to DID Core.<br>  <span>… how a DID gets to the related DID Doc.</span></p>  <p><cite>Wip:</cite> currently assigned to Steve McCown -- issue 17 and 18.  Plans to look at those before the next meeting.</p>    <hr /></details>
---
Although PRISM already has some errors defined and returned by our Cloud Agent RestAPI calls, we do not have any mechanism to handle and report errors when they are happening during record processing or sending/receiving DIDComm messages. It is required to implement a mechanism of error handling for Cloud Agent to log, update records in the database, and report errors in the right way.

- [x] hyperledger/identus-edge-agent-sdk-ts/issues/308

