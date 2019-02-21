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
|  - id | 0..1 | Select | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Select | Meta | Metadata about the resource <font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/ITK-Rest-Bundle-1'</font> |
|  - implicitRules | 0..1 | Select | Uri | A set of rules under which this content was created |
|  - language | 0..1 | Select | Code | Language of the resource content<br/>Binding (extensible): A human language.[See FHIR STU3 for further information](http://hl7.org/fhir/stu3/valueset-languages.html) |
|  - identifier | 0..1 | Select | Identifier | Persistent identifier for the bundle |
|  - - use | 0..1 | Select | Code | usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known .[See FHIR STU3 for further information](http://hl7.org/fhir/stu3/valueset-identifier-use.html) |
|  - - type | 0..1 | Select | CodeableConcept | Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [See FHIR STU3 for further information](http://hl7.org/fhir/stu3/valueset-identifier-type.html) |
|  - - - coding | 0..* | Select | Coding | Code defined by a terminology system |
|  - - - - system | 0..1 | Select | Uri | Identity of the terminology system |
|  - - - - version | 0..1 | Select | String | Version of the system - if relevant |
|  - - - - code | 0..1 | Select | Code | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Select | String | Representation defined by the system |
|  - - - - userSelected | 0..1 | Select | Boolean | If this coding was chosen directly by the user |
|  - - text | 0..1 | Select | String | Plain text representation of the concept |
|  - system | 0..1 | Select | Uri | The namespace for the identifier value |
|  - value | 0..1 | Select | String | The value that is unique |
|  - - period | 0..1 | Select | Period | Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Select | dateTime | Starting time with inclusive boundary |
|  - - - end | 0..1 | Select | dateTime | End time with inclusive boundary, if not ongoing |
|  - - assigner | 0..1 | Select | Reference  | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   | 0..1 | Select | (CareConnect-Organization-1) | [see CareConnect-Organization-1 mapping for further information](xxx#careconnect-organization-mapping) |
|  - - - reference | 0..1 | Select | String | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Select | Identifier | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Select | String | Text alternative for the resource |
|  - type | 1..1 | Select | Code | document : message : transaction : transaction-response : batch : batch-response : history : searchset : collection<br/>Binding (required): Indicates the purpose of a bundle - how it was intended to be used. [See FHIR STU3 for further information](http://hl7.org/fhir/stu3/valueset-bundle-type.html) |
|  - total | 0..1 | Select | unsignedInt | If search, the total number of matches |
|  - link | 0..* | Select | BackboneElement | Links related to this Bundle |
|  - - modifierExtension | 0..* | Select | Extension | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - relation | 1..1 | Select | String | [See](http://www.iana.org/assignments/link-relations/link-relations.xhtml#link-relations-1) |
|  - - url | 1..1 | Select | Uri | Reference details for the link |
|  - entry | 0..* | Select | BackboneElement | Entry in the bundle - will have a resource, or information<br/>Constraint (bdl-8): fullUrl cannot be a version specific reference<br/>Constraint (bdl-5): Must Be A Resource Unless There'S A Request Or Response |
|  - - modifierExtension | 0..* | Select | Extension | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - link | 0..* | Select | see Bundle.link | Links related to this entry |
|  - - fullUrl | 0..1 | Select | Uri | Absolute URL for resource (server address, or UUID/OID) |
|  - - resource | 0..1 | Select | Resource | A resource in the bundle |
|  - - search | 0..1 | Select | BackboneElement | Search related information |
|  - - - modifierExtension | 0..* | Select | Extension | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - - mode | 0..1 | Select | Code | match : include : outcome - why this is in the result set<br/>Binding (required): Why an entry is in the result set - whether it's included as a match or because of an _include requirement. [See FHIR STU3 for further information](http://hl7.org/fhir/stu3/valueset-search-entry-mode.html) |
|  - - - score | 0..1 | Select | Decimal | Search ranking (between 0 and 1) |
|  - - request | 0..1 | Select | BackboneElement | Transaction Related Information |
|  - - - modifierExtension | 0..* | Select | Extension | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - - method | 1..1 | Select | Code | GET : POST : PUT : DELETE<br/>Binding (required): HTTP verbs (in the HTTP command line). [See FHIR STU3 for further information](http://hl7.org/fhir/stu3/valueset-http-verb.html) |
|  - - - url | 1..1 | Select | Uri | URL for HTTP equivalent of this entry |
|  - - - ifNoneMatch | 0..1 | Select | String | For managing cache currency |
|  - - - ifModifiedSince | 0..1 | Select | Instant | For managing update contention |
|  - - - ifMatch | 0..1 | Select | String | For managing update contention |
|  - - - ifNoneExist | 0..1 | Select | String | For conditional creates |
|  - - response | 0..1 | Select | BackboneElement | Transaction Related Information |
|  - - - modifierExtension | 0..* | Select | Extension | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - - status | 1..1 | Select | String | Status response code (text optional) |
|  - - - location | 0..1 | Select | Uri | The location, if the operation returns a location |
|  - - - etag | 0..1 | Select | String | The etag for the resource (if relevant) |
|  - - - lastModified | 0..1 | Select | Instant | Server's date time modified |