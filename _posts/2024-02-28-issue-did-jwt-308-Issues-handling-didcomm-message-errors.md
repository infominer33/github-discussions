---
title: "did-jwt/issue/308: Issues handling didcomm message errors"
date: 2024-02-28 12:47:17 +0000
author: amagyar-iohk
categories: ["DIF"]
tags: ["did-jwt"]
permalink: /did-jwt/issue/308/
comments_file: DIF-did-jwt-issue-308_comments
excerpt: >
  Outline of template:
---
### Is this a regression?

Yes

### Description

## Brief

When didcomm message returns a `http status code` other than `ok` the message becomes undefined due a try-catch block. This issue's goal is to enable an error management for didcomm errors.
Spec: https://identity.foundation/didcomm-messaging/spec/#problem-reports

FetchApi.ts
```typescript
  async request<T>(
    method: HttpMethod,
    urlStr: string,
    urlParameters: Map<string, string> = new Map(),
    httpHeaders: Map<string, string> = new Map(),
    body?: string | Record<string, any>
  ): Promise<ApiResponse<T>> {
    // ...
    if (response.ok) {
      return new ApiResponse(
        data,
        response.status,
        response.statusText,
        response.headers
      );
    }
    throw new ApiError(response.status, response.statusText, data);
}
```

Mercury.ts
```typescript
  async sendMessageParseMessage(
    message: Domain.Message
  ): Promise<Domain.Message | undefined> {
    const responseBody = await this.sendMessage<any>(message);
    try {
      const responseJSON = JSON.stringify(responseBody);
      return await this.unpackMessage(responseJSON);
    } catch (err) {
      return undefined
    }
  }
```

Any `ApiError` thrown will cause message to return `undefined` as per described in the `Mercury.ts#sendMessageParseMessage` method

### Please provide the exception or error you saw

_No response_

### Please provide the environment you discovered this bug in

_No response_

### Anything else?

_No response_