---
title: "Exchange of Electronic Certificate of Origin to facilitate Cross Border Trade"
date: 2024-09-23 22:29:56 +0000
author: cxcheng
excerpt: >
  Thanks Kevin for putting this up. We will get back to you in 2-3 weeks as some of our key members are on leave.
categories: openwallet-foundation
tags: acapy-endorser-service
comments_file: acapy-endorser-service-issue-157_comments
permalink: /acapy-endorser-service/157/
url: https://github.com/openwallet-foundation/acapy-endorser-service/issues/157
last_modified_at: 2024-11-24 06:44:54 +0000
---


**URL:** https://github.com/openwallet-foundation/acapy-endorser-service/issues/157

# Background

Today, cross-border trade and transport of goods take place on the basis of many documents and processes that are paper-based (hence manual), time-consuming, and resource-intensive process for all stakeholders. Another downside of such paper-based processes is that there is no easy way to verify the accuracy and authenticity of the trade documents. This results in inefficiencies and delays as the time required to process such paper documents far exceeds the actual time taken for the physical movement of goods. [According to a study by McKinsey in 2022](https://www.mckinsey.com/industries/travel-logistics-and-infrastructure/our-insights/the-multi-billion-dollar-paper-jam-unlocking-trade-by-digitalizing-documentation), documentation for a single shipment can require up to 50 sheets of paper that are exchanged with up to 30 different stakeholders.

To address these inefficiencies, we have developed TradeTrust. TradeTrust, which is built upon OpenAttestation framework, comprises globally accepted standards and frameworks that allow governments and businesses to issue, verify and effect title transfer of electronic documents across different digital platforms seamlessly. TradeTrust uses cryptography and decentralised identifier (DID) technical methods to assure the authenticity and provenance of these electronic documents.

As a framework, TradeTrust is designed and developed to support the digitalization of documents used in Cross-Border Trade processes. Such documents could include those that are used to convey information such as Packing Lists and Certificates of Origin (CO) thus making them verifiable with respect to their authenticity and provenance. A CO is a document commonly used in Trade to attest that a product originates from a particular country. For more information, please see https://iccwbo.org/business-solutions/certificates-of-origin/.

<diagram on workflow>

# Distinction

Existing trade documents are typically printed hardcopies secured with wet ink stamps. These documents are susceptible to forgery and manipulation. A digital verifiable document would allow for 
* Assurance that the document has not been tampered with 
* Assurance that the document was issued by a particular Issuer 
* As these trade documents are shared across different parties in a long chain that may cross many borders, the holders of these documents may want control over what information is shared downstream. A shipper may choose to selectively redact commercially sensitive information (such as suppliers' names or products' pricing) before sharing it onto the next receiving party. This is based on a lossy selective redaction, removing the need to re-issue ‘a version sans the commercially sensitive information’.

# Actors

Using an electronic Certificate of Origin (eCO) as an example of a digital document that is issued via the TradeTrust framework, below are the typical actors involved in its processing.

## Customs Administration or duly licensed parties like Chambers of Commerce
Customs Administration and/or Chamber of Commerce are the typical authorities responsible for producing an eCO. It is typically needed by importers/buyers to claim tariff exemptions from the importing customs authority or to provide assurance that the goods are indeed from a particular country. It is provided to importers/buyers by the exporters/sellers whom they buy from and often used in financing arrangements with banks.

## Banks
In cross-border trade, sometimes buyers and sellers may arrange for trade financing services to mitigate the risks of non-payment or non-delivery. Banks and other Financial Institutions are often engaged as intermediaries to mitigate these risks using financing instruments such as a Letter of Credit (L/C). A L/C is applied for by the Buyer and will specify a list of trade documents that the Banks will need to sight and verify on behalf of their clients. One of the often-required documents can be an eCO.

## Importer
An Importer/Buyer is the party who purchases and receives products from the seller. If there is a Free Trade Agreement between the importing country and the goods’ origin country, the Importer can provide the eCO during importation clearance procedures to obtain tariff exemptions for the goods.

## Exporter
An Exporter/Seller is the party who sells and transports products to his buyer. The Exporter is the party who applies for the eCO from the Customs Administration or duly licensed parties like Chambers of Commerce within the exporting country, upon the request of the Importer.

## Issuer

A Customs Administration and/or Chamber of Commerce are the typical authorities responsible for producing an eCO.

## Subject

The eCO attests that the origin of the goods is a particular country. It is used to claim tariff exemptions from the importing customs authority or to provide assurance that the goods are indeed from a particular country.

## Holder

The eCO can be held by the Importer (and/or their appointed customs broker) and presented to the importing country’s customs administration for import tariff exemption if there is an in-force Free Trade Agreement between the goods’ origin country and the importing country. The eCO can also be held by the Exporter and Banks for trade financing purposes.

## Verifier

The eCO is verified by the importing country’s Custom Authority during the importation of goods. It is also verified by Banks if the Exporter and/or Importer has financing arrangements that call for it. It is also verified by the importer to assure that the goods originated from the expected country.

# Validation Requirements

Document verification can be initiated by invoking the open-sourced verification library, or via the trusted verification portals which run the open-sourced verification library.

<sequence diagram available>

There are no other relationship or dependencies on other Verifiable Credentials.

# Example Artefacts

## Verifiable Credential

Electronic Certificate of Origin

Based on older OpenAttestation v2. Latest OpenAttestation v4 Alpha is now W3C VC Data Model 2.0 compliant.

```json
{
    "version": "https://schema.openattestation.com/2.0/schema.json",
    "data": {
        "firstSignatoryAuthentication": {},
        "supplyChainConsignment": {
            "exportCountry": {},
            "exporter": {
                "postalAddress": {}
            },
            "importCountry": {},
            "importer": {
                "postalAddress": {}
            },
            "loadingBaseportLocation": {},
            "mainCarriageTransportMovement": {
                "usedTransportMeans": {},
                "departureEvent": {}
            },
            "unloadingBaseportLocation": {}
        },
        "$template": {
            "type": "7a29f8c9-47a0-429d-a043-0eceee351090:string:EMBEDDED_RENDERER",
            "name": "907e4a2d-0d16-491d-99a6-531eb4a5d06f:string:CHAFTA_COO",
            "url": "7a149cd6-33d9-4813-9a6c-f7ea00b2683c:string:https://generic-templates.tradetrust.io"
        },
        "issuers": [
            {
                "name": "eef12038-1f5f-40de-9491-fea8a3c3771e:string:Demo Issuer",
                "documentStore": "b75454f5-79c8-4f8c-9e92-77626b6871d2:string:0x70f83193bE363348Ec769c8752690eB915E640A4",
                "identityProof": {
                    "type": "b4aee06a-d226-4f0e-8bf4-b0f125735a14:string:DNS-TXT",
                    "location": "4d830cea-5332-4cd7-91dd-0187c096e3af:string:sandbox.tradetrust.io"
                },
                "revocation": {
                    "type": "59cf4245-6d93-4b63-91b1-f9b100e8f304:string:NONE"
                }
            }
        ],
        "network": {
            "chain": "2d9f5493-416e-448c-8404-e308a6093bd7:string:FREE",
            "chainId": "bf39e664-b37c-4e0c-bf9b-e74c257da7bd:string:101010"
        }
    },
    "signature": {
        "type": "SHA3MerkleProof",
        "targetHash": "cff3db9808786f9ad214f3ae79cb83fccc74103a9db78f786335f85871b517cd",
        "proof": [],
        "merkleRoot": "cff3db9808786f9ad214f3ae79cb83fccc74103a9db78f786335f85871b517cd"
    }
}
```

# Trust Hierarchy

The trust can be separated into 2 parts.

1. The issuer’s identity is based on the ownership of the DNS 
   1. This is where we intend to have an alternative identity provided by the Trust Anchors
2.	Data integrity is based on the hash that is written on blockchain OR signed by the issuer.


# Threat Model

To be added.

## Risk - Put simple description here

Put detailed description here, including and especially the response(s) to the risk.
