---
title: Admission Details Bundle
keywords:  bundles
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_admission_details.html
summary: "The FHIR profiles used for the Admission Details Bundle"
---

## Heading Description ##
The details of the woman’s admission.

## Mapping for Bundle ##

|>|Level 1|[Bundle Resource](http://hl7.org/fhir/stu3/bundle.html)|>|Level 2| None|>|Level 3|[NHSD-Bundle-1 Profile](http://xxx)|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_admission_details_all.html#mapping-for-bundle)**|


|  **Name** | **​Card.** | **Conformance** | **Type** | **Constraints and mapping for XXX Implementation** |
| :--- | :--- | --- | :--- | :--- |
|  **Bundle** | **** |  |  | **Contains a collection of resources<br/>Constraint (bdl-7): FullUrl must be unique in a bundle, or else entries with the same fullUrl must have different meta.versionId<br/>Constraint (bdl-9): A document must have an identifier with a system and a value<br/>Constraint (bdl-3): Entry.Request Only For Some Types Of Bundles<br/>Constraint (bdl-4): Entry.Response Only For Some Types Of Bundles<br/>Constraint (bdl-1): Total Only When A Search Or History<br/>Constraint (bdl-2): Entry.Search Only When A Search** |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource <font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/ITK-Rest-Bundle-1'</font> |
|  - identifier | 0..1 | Mandatory | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Persistent identifier for the bundle |
|  - system | 0..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value |
|  - value | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - type | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | document : message : transaction : transaction-response : batch : batch-response : history : searchset : collection<br/>Binding (required): Indicates the purpose of a bundle - how it was intended to be used. [See FHIR STU3 for further information](http://hl7.org/fhir/stu3/valueset-bundle-type.html) |
|  - - modifierExtension | 0..* | Mandatory | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - request | 0..1 | Mandatory | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Transaction Related Information |
|  - - - method | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | GET : POST : PUT : DELETE<br/>Binding (required): HTTP verbs (in the HTTP command line). [See FHIR STU3 for further information](http://hl7.org/fhir/stu3/valueset-http-verb.html) |
|  - - - url | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | URL for HTTP equivalent of this entry |