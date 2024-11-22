---
title: "data-integrity-test-suite-assertion/issue/83: `selectPaths` of partial object in array"
date: 2024-07-21 21:17:46 +0000
author: brianorwhatever
categories: ["DIF"]
tags: ["data-integrity-test-suite-assertion"]
permalink: /data-integrity-test-suite-assertion/issue/83/
comments_file: DIF-data-integrity-test-suite-assertion-issue-83_comments
---

[_https://github.com/w3c-ccg/data-integrity-test-suite-assertion/issues/83_](https://github.com/w3c-ccg/data-integrity-test-suite-assertion/issues/83)

I believe I have implemented `selectPaths` and `selectJsonLD` correctly however I have a test failing that is supposed to select some of the elements of an object and drop the others. Here is the test:

```
const document = {
        '@context': {
          '@version': 1.1,
          'ex': 'https://example.org/vocab#',
          'credentials': 'ex:credentials'
        },
        'credentials': [
          { 'id': '1', 'type': 'A' },
          { 'id': '2', 'type': 'B' },
          { 'id': '3', 'type': 'C' }
        ]
      };

      const pointers = [
        '/credentials/0/id',
        '/credentials/0/type',
        '/credentials/2/id'
      ];
      const result = selectJsonLd(pointers, document);
  ```

and the resultant document is

```
{
    "@context": {
      "@version": 1.1,
      credentials: "ex:credentials",
      ex: "https://example.org/vocab#",
    },
    credentials: [
      {
        id: "1",
        type: "A",
      },
      {
        id: "3",
       type: "C",
      }
    ],
  }
  ```

so the array selection is working and making it dense.. however we are seeing the `type: "C"` property on the second element where I would expect to only see the `id`. I've traced it down pretty deep and in step 7 I am setting `selectedValue` properly but the selected Property already is:

```
{
  id: "3",
  type: "C",
}
```

Am I missing something?