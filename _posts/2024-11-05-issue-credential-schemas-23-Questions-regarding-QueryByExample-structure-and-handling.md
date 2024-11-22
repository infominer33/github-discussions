---
title: "credential-schemas/issue/23: Questions regarding `QueryByExample` structure and handling"
date: 2024-11-05 17:54:02 +0000
author: geel9
categories: ["DIF"]
tags: ["credential-schemas"]
permalink: /credential-schemas/issue/23/
comments_file: DIF-credential-schemas-issue-23_comments
---

[_https://github.com/decentralized-identity/credential-schemas/issues/23_](https://github.com/decentralized-identity/credential-schemas/issues/23)

Hello,

I have some questions regarding the proper handling of `QueryByExample` objects.

I understand that many of these questions may not yet have answers, but I'd appreciate any insight that can be provided.

1. Are the `@context` and `type` fields required or optional?
2. What is the datatype of these fields? 
    - I am operating under the assumption that they are both `string | string[]` -- is this fair?
3. How are the `@context` and `type` fields to be handled?
	- I am operating under the assumption that every value in the example `@context` array (whether it be expressed as an array of strings or a string itself) must be present in the credential's `@context` array, but additional values may be present in the credential's `@context` array. Is this fair?
	- I am operating under an equal assumption for the `type` field.
4. Is `credentialSubject` limited to only `id` and `name` fields, or is it intended for arbitrary key/values to query against the credential's `credentialSubject`?
    - My intuition tells me that any key/value pairs are valid, but the comment above it in Example 2 states `You can request a specific subject id`, which implies that that is the _only_ intended usage.
5. Assuming `credentialSubject` is not limited to `id` and `name`, how is comparison meant to be handled?
	- Comparisons of primitives is intuitive, but stringy equality (does `5` match `"5"`?) should be clarified.
	- Comparisons of objects is also intuitive -- just recurse.
		- I am assuming, however, that all object comparisons (including the top-level `example.credentialSubject` to `credential.credentialSubject` comparison itself) are loose in the sense that the object on the credential may have additional fields not specified by the example object.
	- How should one perform a comparison of arrays?
		- See below


### Array Comparison in `credentialSubject`
_(This is all assuming that the `credentialSubject` field in the example query is not restricted to `id` and `name` fields)_

Given the following query:

```json
{
  "type": "QueryByExample",
  "credentialQuery": {
    "example": {
      "credentialSubject": {
        "primitive_array_one": [0, 1, 2],
        "primitive_array_two": [10, 11, 12],
        "complex_array": [
          {
            "a": 1
          },
          {
            "b": 2
          }
        ]
      }
    }
  }
}
```

And the following `credentialSubject` from a VerifiableCredential:

```json
{
  "credentialSubject": {
    "id": "whatever",
    "primitive_array_one": [0, 1, 2, 3],
    "primitive_array_two": [12, 11, 10],
    "complex_array": [
      {
        "a": 1,
        "b": 2,
      },
      {
        "b": 3
      }
    ]
  }
}
```


It's not entirely clear how to handle this query by example.

- `primitive_array_one`
	- The credential's `primitive_array_one` contains all values of the example's `primitive_array_one`, in the same order and position, but it has additional entries.
- `primitive_array_two`
	- The credential's `primitive_array_two` contains all values of the example's `primitive_array_two`, and has no additional values, but they are not in the same order. 
- `complex_array`
	- The example is looking for an object with an `a` value equal to `1`, and an object with a `b` value equal to `2`.
		- The credential does, in fact, have an object with an `a` value equal to `1`, _and_ an object with a `b` value equal to `2`. 
		- However, they're the _same object_, which likely isn't what the person who wrote the query was intending.