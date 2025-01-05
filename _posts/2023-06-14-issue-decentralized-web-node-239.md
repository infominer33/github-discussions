---
title: "Problematic support of multiple schema versions when using JsonSchemaCredential"
date: 2023-06-14 16:47:37 +0000
author: antonio-ivanovski
excerpt: >
  @antonio-ivanovski I'm supportive of these changes (1 and 2), I'm not certain about 3--the version should be self evident if 1 and 2 are done. Are you able to make a PR? Unfortunately, my bandwidth is limited at the moment.
categories: decentralized-identity
tags: decentralized-web-node
comments_file: decentralized-web-node-issue-239_comments
permalink: /decentralized-web-node/239/
url: https://github.com/decentralized-identity/decentralized-web-node/issues/239
last_modified_at: 2025-01-03 19:32:25 +0000
---


**URL:** https://github.com/decentralized-identity/decentralized-web-node/issues/239

While implementing support for JsonSchemaCredential I have stumbled on implementation issue that I have not foreseen at the beginning. Namely it is the JSON Schema versions supports for the `jsonSchema` property.

Let me explain.
From the spec, the `JsonSchemaCredential` document requires the `credentialSchema` property to be exactly:
```
{
  "id": "https://www.w3.org/ns/credentials/json-schema/v2.json",
  "type": "JsonSchema",
  "digestSRI": "sha384-S57yQDg1MTzF56Oi9DbSQ14u7jBy0RDdx0YbeV7shwhCS88G8SCXeFq82PafhCrW"
}
```

Fetching "https://www.w3.org/ns/credentials/json-schema/v2.json" gives the following schema for `jsonSchema`:

```
"jsonSchema": {
  "anyOf": [
    {
      "$ref": "https://json-schema.org/draft/2020-12/schema"
    },
    {
      "$ref": "https://json-schema.org/draft/2019-09/schema"
    },
    {
      "$ref": "http://json-schema.org/draft-07/schema"
    }
  ]
}
```

As you can see, the schema itself is referencing all the recommended JSON Schema versions by spec (draft-7, 2019-09, 2020-12). 

I am using Ajv as the most standard JSON Schema library for JS, and for the support of 2020-12 version it has a note (https://ajv.js.org/json-schema.html#draft-2020-12) that it is not compatible with older schemas. When using this and when the schema is being compiled, it is failing to load the 2019-09 and draft-07 schemas over and over again entering into endless loop. This is because this schemas as not being expected and not considered meta schemas.

I am still not able to find workaround for this issue for using Ajv. I am considering switching to [hyperjump-io/json-schema](https://github.com/hyperjump-io/json-schema) as it seems to support this.

Before doing switch or another hacky workaround, it is very suspicious to me that the Ajv team that has focused so much on JSON Schema would make such limiting design decision when not being required. My concern is that such schemas may be considered invalid. 

Can you please clarify the support of all these schema versions? 
Maybe it makes sense to make the `jsonSchema` field be just an object schema and let the implementations try to compile the contents it.