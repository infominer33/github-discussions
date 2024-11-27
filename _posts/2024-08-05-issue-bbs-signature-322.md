---
title: "Necessary update on the formal vocabulary?"
date: 2024-08-05 22:36:40 +0000
author: iherman
excerpt: >
  PR #320 has been merged, closing.
categories: decentralized-identity
tags: bbs-signature
comments_file: bbs-signature-issue-322_comments
permalink: /bbs-signature/322/
url: https://github.com/decentralized-identity/bbs-signature/issues/322
last_modified_at: 2024-11-23 18:35:07 +0000
---


**URL:** https://github.com/decentralized-identity/bbs-signature/issues/322

Reading through w3c/controller-document#116 it helped me to understand some things. My way of getting my thoughts in order was to try to map what I read to the [security vocabulary](https://w3c.github.io/vc-data-integrity/vocab/security/vocabulary.html) (which is, after all, simple ontology).

To check my understanding, I believe the following statements are true (some are trivial, some less):

1. _VerificationMethod_ and _ControllerDocument_ are two distinct concepts (i.e., they should be considered as distinct Classes, in RDFS parlance).
2. The _verifcationMethod_ property designates a _VerificationMethod_ instance (i.e., the _range_ of the property is a resource of type _VerificationMethod_)
3. The _VerificationMethod_ class has some subclasses defined in the controller specification, namely _Multikey_, _JsonWebKey_, and _Ed25519VerificationKey2020_.
4. The two classes in (1) have a common property, namely _controller_ (i.e., the property's _domain_ is the union of those two classes). 
5. The _ControllerDocument_ concept is ***not*** used by the Data Integrity specification, only the _VerificationMethod_ (by the way of the _verificationMethod_ property).
6. As consequence of the previous statement that it would be a mistake to define the _domain_ of the _verificationMethod_ as being a _ControllerDocument_ (i.e., ontologically one cannot restrain the classes on which it is used to be a controller document.) Actually, there should be no restraint on the domain whatsoever.

Looking at the [vocabulary](https://w3c.github.io/vc-data-integrity/vocab/security/vocabulary.html) (see also its [graphic representation](https://w3c.github.io/vc-data-integrity/vocab/security/vocabulary.svg)) we are _almost_ o.k. but not fully. The glaring (and significant) missing concept is the _ControllerDocument_. Per (1) above I believe it should be added as a separate class and, per (4) it should be an alternative domain for the _controller_ property.

(Note that the _alsoKnownAs_ and _service_ properties, though listed in the [specification](https://www.w3.org/TR/controller-document/#controller-documents) as properties on controller document, do not appear in the vocabulary or in its diagram. That is because these two properties are "borrowed" from other vocabularies.)

Long story short, I believe the following changes should be done on the vocabulary:

- Add the _ControllerDocument_ class to the vocabulary
- The _domain_ of the _controller_ property should be changed to include _ControllerDocument_ as an alternative.

I also believe that the statement (5) is not absolutely obvious from the current text, and it should be reinforced somehow...