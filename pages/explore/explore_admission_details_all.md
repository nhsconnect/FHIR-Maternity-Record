---
title: Admission Details Bundle
keywords:  bundles
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_admission_details_all.html
summary: "The FHIR profiles used for the Admission Details Bundle"
---

## Heading Description ##
The details of the woman’s admission.

## Mapping for Bundle ##

|>|Level 1|[Bundle Resource](http://hl7.org/fhir/stu3/bundle.html)|>|Level 2| None|>|Level 3|[NHSD-Bundle-1 Profile](http://xxx)|

|**View All FHIR Elements**|    |**[View Used Elements Only](explore_admission_details.html#mapping-for-bundle)**| 

|  **Name** | **​Card.** | **Conformance** | **Type** | **Constraints and mapping for XXX Implementation** |
| :--- | :--- | --- | :--- | :--- |
|  **Bundle** | **** |  |  | **Contains a collection of resources<br/>Constraint (bdl-7): FullUrl must be unique in a bundle, or else entries with the same fullUrl must have different meta.versionId<br/>Constraint (bdl-9): A document must have an identifier with a system and a value<br/>Constraint (bdl-3): Entry.Request Only For Some Types Of Bundles<br/>Constraint (bdl-4): Entry.Response Only For Some Types Of Bundles<br/>Constraint (bdl-1): Total Only When A Search Or History<br/>Constraint (bdl-2): Entry.Search Only When A Search** |
|  - id | 0..1 | Select | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Select | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource <font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/ITK-Rest-Bundle-1'</font> |
|  - implicitRules | 0..1 | Select | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | A set of rules under which this content was created |
|  - language | 0..1 | Select | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Language of the resource content<br/>Binding (extensible): A human language.[See FHIR STU3 for further information](http://hl7.org/fhir/stu3/valueset-languages.html) |
|  - identifier | 0..1 | Select | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Persistent identifier for the bundle |
|  - - use | 0..1 | Select | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known .[See FHIR STU3 for further information](http://hl7.org/fhir/stu3/valueset-identifier-use.html) |
|  - - type | 0..1 | Select | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [See FHIR STU3 for further information](http://hl7.org/fhir/stu3/valueset-identifier-type.html) |
|  - - - coding | 0..* | Select | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - system | 0..1 | Select | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - version | 0..1 | Select | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - code | 0..1 | Select | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Select | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - userSelected | 0..1 | Select | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - text | 0..1 | Select | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - system | 0..1 | Select | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value |
|  - value | 0..1 | Select | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - - period | 0..1 | Select | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Select | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - end | 0..1 | Select | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - - assigner | 0..1 | Select | [Reference ](http://hl7.org/fhir/stu3/references.html "Reference ") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   | 0..1 | Select | [(CareConnect-Organization-1)](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "(CareConnect-Organization-1)") | [see CareConnect-Organization-1 mapping for further information](xxx#careconnect-organization-mapping) |
|  - - - reference | 0..1 | Select | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Select | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Select | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - type | 1..1 | Select | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | document : message : transaction : transaction-response : batch : batch-response : history : searchset : collection<br/>Binding (required): Indicates the purpose of a bundle - how it was intended to be used. [See FHIR STU3 for further information](http://hl7.org/fhir/stu3/valueset-bundle-type.html) |
|  - total | 0..1 | Select | [unsignedInt](http://hl7.org/fhir/stu3/datatypes.html#unsignedint "unsignedInt") | If search, the total number of matches |
|  - link | 0..* | Select | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Links related to this Bundle |
|  - - modifierExtension | 0..* | Select | Extension | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - relation | 1..1 | Select | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | [See](http://www.iana.org/assignments/link-relations/link-relations.xhtml#link-relations-1) |
|  - - url | 1..1 | Select | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Reference details for the link |
|  - entry | 0..* | Select | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Entry in the bundle - will have a resource, or information<br/>Constraint (bdl-8): fullUrl cannot be a version specific reference<br/>Constraint (bdl-5): Must Be A Resource Unless There'S A Request Or Response |
|  - - modifierExtension | 0..* | Select | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - link | 0..* | Select | [see Bundle.link](https://fhir-test.nhs.uk/STU3/StructureDefinition/details.html#Bundle.link "see Bundle.link") | Links related to this entry |
|  - - fullUrl | 0..1 | Select | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Absolute URL for resource (server address, or UUID/OID) |
|  - - resource | 0..1 | Select | [Resource](http://hl7.org/fhir/stu3/resource.html "Resource") | A resource in the bundle |
|  - - search | 0..1 | Select | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Search related information |
|  - - - modifierExtension | 0..* | Select | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - - mode | 0..1 | Select | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | match : include : outcome - why this is in the result set<br/>Binding (required): Why an entry is in the result set - whether it's included as a match or because of an _include requirement. [See FHIR STU3 for further information](http://hl7.org/fhir/stu3/valueset-search-entry-mode.html) |
|  - - - score | 0..1 | Select | [Decimal](http://hl7.org/fhir/stu3/datatypes.html#decimal "Decimal") | Search ranking (between 0 and 1) |
|  - - request | 0..1 | Select | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Transaction Related Information |
|  - - - modifierExtension | 0..* | Select | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - - method | 1..1 | Select | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | GET : POST : PUT : DELETE<br/>Binding (required): HTTP verbs (in the HTTP command line). [See FHIR STU3 for further information](http://hl7.org/fhir/stu3/valueset-http-verb.html) |
|  - - - url | 1..1 | Select | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | URL for HTTP equivalent of this entry |
|  - - - ifNoneMatch | 0..1 | Select | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | For managing cache currency |
|  - - - ifModifiedSince | 0..1 | Select | [Instant](http://hl7.org/fhir/stu3/datatypes.html#instant "Instant") | For managing update contention |
|  - - - ifMatch | 0..1 | Select | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | For managing update contention |
|  - - - ifNoneExist | 0..1 | Select | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | For conditional creates |
|  - - response | 0..1 | Select | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Transaction Related Information |
|  - - - modifierExtension | 0..* | Select | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - - status | 1..1 | Select | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Status response code (text optional) |
|  - - - location | 0..1 | Select | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The location, if the operation returns a location |
|  - - - etag | 0..1 | Select | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The etag for the resource (if relevant) |
|  - - - lastModified | 0..1 | Select | [Instant](http://hl7.org/fhir/stu3/datatypes.html#instant "Instant") | Server's date time modified |