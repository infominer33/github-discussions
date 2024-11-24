---
title: "json-ld-syntax/issue/443: `@protected` creates unresolvable conflicts when the same term is defined in two contexts top-level"
date: 2024-10-19 09:53:21 +0000
author: trwnh
categories: ["DIF"]
tags: ["json-ld-syntax"]
permalink: /json-ld-syntax/issue/443/
comments_file: DIF-json-ld-syntax-issue-443_comments
---

[_https://github.com/w3c/json-ld-syntax/issues/443_](https://github.com/w3c/json-ld-syntax/issues/443)

I've just encountered issue #424 (and the related #361 as well) and in a similar situation with `https://www.w3.org/ns/controller/v1` defining `alsoKnownAs` top-level alongside `@protected: true`, while `https://www.w3.org/ns/activitystreams` defines `alsoKnownAs` in a different namespace (as: vs sec:, loosely)

From controller/v1:

```json
{
  "@context": {
    "@protected": true,
    "id": "@id",
    "type": "@type",

    "alsoKnownAs": {
      "@id": "https://w3id.org/security#alsoKnownAs",
      "@type": "@id",
      "@container": "@set"
    },
//...
```

From activitystreams:

```json
{
  "@context": {
    "@vocab": "_:",
    "xsd": "http://www.w3.org/2001/XMLSchema#",
    "as": "https://www.w3.org/ns/activitystreams#",
// ...
"alsoKnownAs": {
      "@id": "as:alsoKnownAs",
      "@type": "@id"
    }
// ...
```

Putting activitystreams before controller/v1 causes the later definition to override the older one, as expected (but not as desired):

```json
{
  "@context": ["https://www.w3.org/ns/activitystreams", "https://www.w3.org/ns/controller/v1"],
  "type": "Person",
  "id": "http://person.example",
  "alsoKnownAs": "https://person.example"  // sec:alsoKnownAs
}
```
```json
[
  {
    "https://w3id.org/security#alsoKnownAs": [  // should be https://www.w3.org/ns/activitystreams#alsoKnownAs
      {
        "@id": "https://person.example"
      }
    ],
    "@id": "http://person.example",
    "@type": [
      "https://www.w3.org/ns/activitystreams#Person"
    ]
  }
]
```

But putting activitystreams *after* controller/v1 triggers the error due to `@protected: true`:

```json
{
  "@context": [
"https://www.w3.org/ns/controller/v1",  // uses @protected
"https://www.w3.org/ns/activitystreams"  // will trigger the redefinition error
],
  "type": "Person",
  "id": "http://person.example",
  "alsoKnownAs": "https://person.example"
}
```
```
jsonld.SyntaxError: Invalid JSON-LD syntax; tried to redefine a protected term.
```

JSON-LD 1.1 4.1.11 Protected term definitions https://www.w3.org/TR/json-ld11/#protected-term-definitions describes two exceptions. The first exception is when the definition is the same, which is not applicable here. The second exception is for *property-scoped* context definitions, which is unworkable because in this case the singular top-level object is intended to be both an Actor as well as a Controller Document.

To veryify, here's a *type-scoped* context definition that errors out:

```json
{
  "@context": [
    "https://www.w3.org/ns/controller/v1",
     {
       "Person": {
         "@id": "https://www.w3.org/ns/activitystreams#Person",
         "@context": {
           "alsoKnownAs": {  // triggers the redefinition error
             "@id": "https://www.w3.org/ns/activitystreams#alsoKnownAs"
           }
         }
       }
     }],
  "type": "Person",
  "id": "http://person.example",
  "alsoKnownAs": "https://person.example"
}
```

And to reiterate, a *property-scoped* context definition can't be used because the `alsoKnownAs` property is top-level. So the way I see it, there's nothing that can be done to resolve this in a "plain JSON" compatible way except:

- a) convince whoever is responsible for controller/v1 to remove `@protected: true`
- b) convince whoever is responsible for controller/v1 to redefine `alsoKnownAs` with the activitystreams-namespaced `@id` instead of the security-namespaced one
- c) write my own context document

This leads me to think that `@protected` is a generally poorly-thought-out mechanism that highly increases the likelihood of such conflicts. Without it, as a producer I could just redefine the term later, for example by putting the activitystreams context last, or by using a local context object that comes after both remote contexts:


```json
{
  "@context": [
  "https://www.w3.org/ns/controller/v1",  // needs to remove @protected
  "https://www.w3.org/ns/activitystreams"  // as:alsoKnownAs will override controller/v1's sec:alsoKnownAs
],
  "type": "Person",
  "id": "http://person.example",
  "alsoKnownAs": "https://person.example"  // as:alsoKnownAs
}
```

or


```json
{
  "@context": [
"https://www.w3.org/ns/activitystreams",  // defines as:alsoKnownAs
"https://www.w3.org/ns/controller/v1",  // redefines sec:alsoKnownAs as @protected 
{
"alsoKnownAs": {
  "@id": "https://www.w3.org/ns/activitystreams#alsoKnownAs",  // won't work unless controller/v1 removes @protected
  "@type": "@id"
}
}],
  "type": "Person",
  "id": "http://person.example",
  "alsoKnownAs": "https://person.example"  // as:alsoKnownAs
}
```

I'm not sure the existence of `@protected` accomplishes its stated goal of "prevent[ing] this divergence of interpretation", nor that the rationale "that "plain JSON" implementations, relying on a given specification, will only traverse properties defined by that specification" is sufficiently addressing the issue of conflicts (or that it is a valid assumption in the first place). The issue arises when two specifications define the same term, and **both specifications apply to the current object or document**. It effectively leads to a hard incompatibility where it is impossible to implement both specs fully; you have to pick between them.

If there's an option I'm not aware of I'd like to hear it.