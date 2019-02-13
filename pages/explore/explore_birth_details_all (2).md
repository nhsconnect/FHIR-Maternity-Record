---
title: Birth Details Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_birth_details_all.html
summary: "The FHIR profiles used for the Birth Details Event Message Bundle"
---

The following FHIR profiles are used to form the Birth Details Event Message Bundle:

- [NHSD-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-Bundle-1)
- [NHSD-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH005 - Birth Details' XXXXXXXXXXXXXXX
- [CareConnect-NHSD-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [NHSD-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-HealthcareService-1)
- [CareConnect-NHSD-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Patient-1)
- [CareConnect-NSHD-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Encounter-1) - where the type element is represented using Child Health Encounter type '003 - Birth' XXXXXXXXXXXXXXXX
- [CareConnect-NHSD-Condition-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-PhysicalProblemAtBirth-Condition-1)
- [CareConnect-NHSD-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-APGARScore-Observation-1)
- [CareConnect-NHSD-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-NeonatalResuscitationMethod-Procedure-1)
- [CareConnect-NHSD-Location-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Delivery-Location-1)

## Birth Details Event data item mapping to FHIR profiles ##

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:


## Mapping for Bundle ##

|>|Level 1|[Bundle Resource](http://hl7.org/fhir/stu3/bundle.html)|>|Level 2| None|>|Level 3|[NHSD-Bundle-1 Profile](http://xxx)|

|**View All FHIR Elements**|    |**[View Used Elements Only](explore_birth_details.html#mapping-for-bundle)**|   

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Maternity-Record Implementation** |
|  :------ | :------ | ------ | :------ | :------ |
|  Bundle | ​ |  |  | Contains a collection of resources<br/>Constraint (bdl-7): FullUrl must be unique in a bundle, or else entries with the same fullUrl must have different meta.versionId<br/>Constraint (bdl-9): A document must have an identifier with a system and a value<br/>Constraint (bdl-3): Entry.Request Only For Some Types Of Bundles<br/>Constraint (bdl-4): Entry.Response Only For Some Types Of Bundles<br/>Constraint (bdl-1): Total Only When A Search Or History<br/>Constraint (bdl-2): Entry.Search Only When A Search |
|  - id | 0..1 | Mandatory | [Id](http://hl7.org/fhir/stu3/datatypes.html#id) | Must contain a UUID to identify the instance of a bundle |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta) | The profile element MUST contain the value https://fhir.nhs.uk/STU3/StructureDefinition/NHSD-Bundle-1 |
|  - implicitRules | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | A set of rules under which this content was created |
|  - language | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | [Language of the resource content . Binding (extensible): A human language. ( http://hl7.org/fhir/stu3/valueset-languages.html )](http://hl7.org/fhir/stu3/valueset-languages.html) |
|  - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier) | Persistent identifier for the bundle |
|  - - use | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | [usual : official : temp : secondary (If known) Binding (required): Identifies the purpose for this identifier, if known . ( http://hl7.org/fhir/stu3/valueset-identifier-use.html )](http://hl7.org/fhir/stu3/valueset-identifier-use.html) |
|  - - type | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept) | Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. ( http://hl7.org/fhir/stu3/valueset-identifier-type.html ) |
|  - - system | 1..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | The namespace for the identifier value |
|  - - value | 1..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | The value that is unique |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period) | Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - assigner | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html) | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | CareConnect-NHSD-Organization-1 |  |
|  - type | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | document : message : transaction : transaction-response : batch : batch-response : history : searchset : collection<br/>Binding (required): Indicates the purpose of a bundle - how it was intended to be used. (http://hl7.org/fhir/stu3/valueset-bundle-type.html )<br/>Fixed Value: "message" |
|  - entry | 1..* | Mandatory | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html) | Entry in the bundle - will have a resource, or information<br/>Constraint (bdl-8): fullUrl cannot be a version specific reference<br/>Constraint (bdl-5): Must Be A Resource Unless There'S A Request Or Response |
|  - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension) | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - fullUrl | 0..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | Absolute URL for resource (server address, or UUID/OID). This MUST be a UUID prefixed by urn:uuid: |
|  - - resource | 1..1 | Mandatory | [Resource](http://hl7.org/fhir/stu3/resource.html) | [A resource in the bundle. This MUST be to the message Header resource profiled as NHSD-MessageHeader-1](explore_birth_details_used.html#mapping-for-messageheader) |

## Mapping for MessageHeader ##

|>|Level 1|[MessageHeader Resource](http://hl7.org/fhir/stu3/messageHeader.html)|>|Level 2| None|>|Level 3|[NHSD-MessageHeader-1 Profile](http://xxx)|

|**View All FHIR Elements**|    |**[View Used Elements Only](explore_birth_details.html#mapping-for-messageheader)**|   


|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Maternity-Record Implementation** |
|  ------ | :------ | ------ | :------ | :------ |
|  MessageHeader | ​ |  |  | A resource that describes a message that is exchanged between systems<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - id | 1..1 | Mandatory | [Id](http://hl7.org/fhir/stu3/datatypes.html#id) | Logical id of this artifact. This MUST be a UUID. |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta) | Metadata about the resource. The profile element MUST contain the value https://fhir.nhs.uk/STU3/StructureDefinition/NHSD-MessageHeader-1 |
|  - implicitRules | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | A set of rules under which this content was created |
|  - language | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | [Language of the resource content Binding (extensible): A human language. ( http://hl7.org/fhir/stu3/valueset-languages.html )](http://hl7.org/fhir/stu3/valueset-languages.html) |
|  - text | 0..1 | Not Used | [Narrative](http://hl7.org/fhir/stu3/narrative.html#Narrative) | Text summary of the resource, for human interpretation |
|  - contained | 0..* | Not Used | [Resource](http://hl7.org/fhir/stu3/resource.html) | Contained, inline Resources |
|  - extension (messageEventType) | 1..1 | Mandatory | [Extension-Maternity-Record-MessageEventType-1](https://fhir.nhs.uk/STU3/StructureDefinition/Extension-Maternity-Record-MessageEventType-1) | [The url attribute of the extension element MUST contain the value https://fhir.nhs.uk/STU3/StructureDefinition/Extension-Maternity-Record-MessageEventType-1 and populated as per specified here.](http://birth_details_used.html#extension-MessageUpdateType-1) |
|  - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension) | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>Slicing: Description: Extensions are always sliced by (at least) url, Discriminator: url, Ordering: false, Rules: Open |
|  - event | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding) | [Code for the event this message represents - Binding (required): The type of Child Health Event.](https://fhir.nhs.uk/STU3/ValueSet/Maternity-Record-ChildHealthEventType-1) |
|  - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | Identity of the terminology system. MUST contain the Fixed Value: "https://fhir.nhs.uk/STU3/CodeSystem/Maternity-Record-ChildHealthEventType-1" |
|  - - version | 1..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Version of the system - if relevant |
|  - - code | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | [Symbol in syntax defined by the system. MUST contain a value from the ValueSet ( https://fhir.nhs.uk/STU3/ValueSet/Maternity-Record-ChildHealthEventType-1](https://fhir.nhs.uk/STU3/ValueSet/Maternity-Record-ChildHealthEventType-1 ) |
|  - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Representation defined by the system. MUST contain the display text assoicated  with the code carried in the code element |
|  - timestamp | 1..1 | Mandatory | [Instant](http://hl7.org/fhir/stu3/datatypes.html#instant) | Time that the message was sent |
|  - source | 1..1 | Mandatory | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html) | Message source application |
|  - - modifierExtension | 1..1 | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension) | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - name | 0..* | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Name of system |
|  - - software | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Name of software running the system |
|  - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Version of software running |
|  - - contact | 0..1 | Not Used | [ContactPoint](http://hl7.org/fhir/stu3/datatypes.html#contactpoint) | Human contact for problems<br/>Constraint (cpt-2): A system is required if a value is provided. |
|  - - - system | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | [phone : fax : email : pager : url : sms : other. Binding (required): Telecommunications form for contact point ( http://hl7.org/fhir/stu3/valueset-contact-point-system.html )](http://hl7.org/fhir/stu3/valueset-contact-point-system.html) |
|  - - - value | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | The actual contact point details |
|  - - - use | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | [home : work : temp : old : mobile - purpose of this contact point. Binding (required): Use of contact point ( http://hl7.org/fhir/stu3/valueset-contact-point-use.html )](http://hl7.org/fhir/stu3/valueset-contact-point-use.html) |
|  - - - rank | 0..1 | Not Used | [positiveInt](http://hl7.org/fhir/stu3/datatypes.html#positiveint) | Specify preferred order of use (1 = highest) |
|  - - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period) | Time period when the contact point was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime) | Starting time with inclusive boundary |
|  - - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime) | End time with inclusive boundary, if not ongoing |
|  - - endpoint | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | Actual message source address or id |
|  - responsible | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html) | Final responsibility for event<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | CareConnect-NHSD-Organization-1 | [The responsible organization carried in the Organizaion resource in the bundle. This MUST be to the Organization resource profiled as CareConnect-NHSD-Organization-1](birth_details_used.html#mapping-for-organization) |
|  - - reference | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier) | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Text alternative for the resource |
|  - focus | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html) | The actual content of the message<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | CareConnect-NHSD-Encounter-1 | [The focus resource in the bundle. This MUST be to the encounter resource profiled as CareConnect-NHSD-Encounter-1](explore_birth_details_used.html#mapping-for-encounter) |
|  - - reference | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier) | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Text alternative for the resource |


## Mapping for Encounter ##

|>|Level 1|[Encounter Resource](http://hl7.org/fhir/stu3/encounter.html)|>|Level 2| [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)|>|Level 3|[CareConnect-NHSD-Encounter-1 Profile](http://xxx)|

|**View All FHIR Elements**|    |**[View Used Elements Only](explore_birth_details.html#mapping-for-encounter)**|   

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for XXX Implementation** |
|  ------ | ------ | ------ | ------ | ------ |
|  Encounter | ​ |  |  | **An interaction during which services are provided to the patient<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource** |
|  - id | 0..1 | **Not Used** | [Id](http://hl7.org/fhir/stu3/datatypes.html#id) | **Logical id of this artifact** |
|  - meta | 0..1 | **Mandatory** | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta) | The profile element MUST contain the value https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-NHSD-Encounter-1 |
|  - implicitRules | 0..1 | **Not Used** | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | **A set of rules under which this content was created** |
|  - language | 0..1 | **Not Used** | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | [**Language of the resource content. Binding (extensible): A human language. ( http://hl7.org/fhir/stu3/valueset-languages.html )**](http://hl7.org/fhir/stu3/valueset-languages.html) |
|  - text | 0..1 | **Not Used** | [Narrative](http://hl7.org/fhir/stu3/narrative.html#Narrative) | **Text summary of the resource, for human interpretation** |
|  - contained | 0..* | **Not Used** | [Resource](http://hl7.org/fhir/stu3/resource.html) | **Contained, inline Resources** |
|  - modifierExtension | 0..* | **Not Used** | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension) | **Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>Slicing: Description: Extensions are always sliced by (at least) url, Discriminator: url, Ordering: false, Rules: Open** |
|  - identifier | 0..1 | **Mandatory** | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier) | **Identifier(s) by which this encounter is known.** |
|  - - system | 1..1 | **Mandatory** | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | **The namespace for the identifier value** |
|  - - value | 1..1 | **Mandatory** | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | **The value that is unique. This MUST be a UUID** |
|  - status | 1..1 | **Mandatory** | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | [**planned : arrived : triaged : in-progress : onleave : finished : cancelled. Binding (required): Current state of the encounter ( http://hl7.org/fhir/stu3/valueset-encounter-status.html)**](http://hl7.org/fhir/stu3/valueset-encounter-status.html)) |
|  - type | 0..* | **Mandatory** | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept) | **Code defined by a terminology system<br/>Binding (required): The type of Child Health encounter ( https://fhir.nhs.uk/STU3/ValueSet/Maternity-Record-ChildHealthEncounterType-1 )** |
|  - - coding | 0..* | **Mandatory** | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding) | **Code defined by a terminology system<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open** |
|  - - coding (snomedCT) | 0..1 | **Mandatory** | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding) | [**Code defined by a terminology system. Binding (required): The type of Child Health encounter ( https://fhir.nhs.uk/STU3/ValueSet/Maternity-Record-ChildHealthEncounterType-1 )**]( https://fhir.nhs.uk/STU3/ValueSet/Maternity-Record-ChildHealthEncounterType-1) |
|  - - - extension (snomedCTDescriptionID) | 0..* | **Not Used** | [Extension-coding-sctdesid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid) | **Additional Content defined by implementations. Constraint (ext-1): Must have either extensions or value[x], not both.** |
|  - - - url | 1..1 | **Not Used** | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | **Identifies The Meaning Of The Extension<br/>Fixed Value: https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid** |
|  - - - value[x] | 0..1 | **Not Used** | [*](http://hl7.org/fhir/stu3/datatypes.html#open) | **Value of extension** |
|  - - system | 1..1 | **Mandatory** | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | **Identity of the terminology system<br/>Fixed Value: http://snomed.info/sct** |
|  - - code | 1..1 | **Mandatory** | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | **Symbol in syntax defined by the system. MUST contain a code from the stated ValueSet** |
|  - - display | 1..1 | **Mandatory** | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | **Representation defined by the system. MUST contain the preferred term for the concept** |
|  - - userSelected | 0..1 | **Not Used** | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean) | **If this coding was chosen directly by the user** |
|  - subject | 1..1 | **Mandatory** | [Reference](http://hl7.org/fhir/stu3/references.html) | **The patient present at the encounter<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided** |
|   |  | **Mandatory** | [CareConnect-NHSD-Patient-1](http://xxx) |  |
|  - - reference | 1..1 | **Mandatory** | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | **Literal reference, Relative, internal or absolute URL** |
|  - - identifier | 0..1 | **Not Used** | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier) | **Logical reference, when literal reference is not known** |
|  - - display | 0..1 | **Not Used** | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | **Text alternative for the resource** |
|  - participant | 0..* | **Not Used** | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html) | **List of participants involved in the encounter** |
|  - - modifierExtension | 0..* | **Not Used** | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension) | **Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both** |
|  - - type | 0..* | **Not Used** | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept) | [**Role of participant in encounter. Binding (extensible): Role of participant in encounter ( http://hl7.org/fhir/stu3/valueset-encounter-participant-type.html )**](http://hl7.org/fhir/stu3/valueset-encounter-participant-type.html) |
|  - - - coding | 0..* | **Not Used** | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding) | **Code defined by a terminology system** |
|  - - - - system | 0..1 | **Not Used** | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | **Identity of the terminology system** |
|  - - - - version | 0..1 | **Not Used** | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | **Version of the system - if relevant** |
|  - - - - code | 0..1 | **Not Used** | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | **Symbol in syntax defined by the system** |
|  - - - - display | 0..1 | **Not Used** | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | **Representation defined by the system** |
|  - - - - userSelected | 0..1 | **Not Used** | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean) | **If this coding was chosen directly by the user** |
|  - - - text | 0..1 | **Not Used** | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | **Plain text representation of the concept** |
|  - - period | 0..1 | **Not Used** | [Period](http://hl7.org/fhir/stu3/datatypes.html#period) | **Period of time during the encounter that the participant participated<br/>Constraint (per-1): If present, start SHALL have a lower value than end** |
|  - - - start | 0..1 | **Not Used** | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime) | **Starting time with inclusive boundary** |
|  - - - end | 0..1 | **Not Used** | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime) | **End time with inclusive boundary, if not ongoing** |
|  - individual | 0..1 | **Not Used** | [Reference](http://hl7.org/fhir/stu3/references.html) | **Persons involved in the encounter other than the patient<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided** |
|   |  | **Not Used** | [CareConnect-NHSD-Practitioner-1](http://xx) |  |
|   |  | **Not Used** | [NHSD-RelatedPerson-1](http://xxx) |  |
|  - - reference | 0..1 | **Not Used** | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | **Literal reference, Relative, internal or absolute URL** |
|  - - identifier | 0..1 | **Not Used** | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier) | **Logical reference, when literal reference is not known** |
|  - - display | 0..1 | **Not Used** | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | **Text alternative for the resource** |
|  - period | 1..1 | **Not Used** | [Period](http://hl7.org/fhir/stu3/datatypes.html#period) | **The start and end time of the encounter<br/>Constraint (per-1): If present, start SHALL have a lower value than end** |
|  - - start | 1..1 | **Not Used** | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime) | **Starting time with inclusive boundary** |
|  - - end | 0..1 | **Not Used** | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime) | **End time with inclusive boundary, if not ongoing** |
|  - reason | 0..1 | **Not Used** | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept) | [**Reason the encounter takes place (code). Binding (preferred): Reason why the encounter takes place. ( http://hl7.org/fhir/stu3/valueset-encounter-reason.html )**](http://hl7.org/fhir/stu3/valueset-encounter-reason.html) |
|  - - coding (snomedCT) | 0..* | **Not Used** | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding) | **Code defined by a terminology system** |
|  - - - extension (snomedCTDescriptionID) | 0..* | **Not Used** | [Extension-coding-sctdesid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid) | **Additional Content defined by implementations. Constraint (ext-1): Must have either extensions or value[x], not both.** |
|  - - - - url | 1..1 | **Not Used** | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | **Identifies The Meaning Of The Extension. Fixed Value: https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid** |
|  - - - - value[x] | 0..1 | **Not Used** | [*](http://hl7.org/fhir/stu3/datatypes.html#open) | **Value of extension** |
|  - - - system | 1..1 | **Not Used** | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | **Identity of the terminology system<br/>Fixed Value: http://snomed.info/sct** |
|  - - - code | 1..1 | **Not Used** | Code | **Symbol in syntax defined by the system** |
|  - - - display | 1..1 | **Not Used** | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | **Representation defined by the system** |
|  - - - userSelected | 0..1 | **Not Used** | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean) | **If this coding was chosen directly by the user** |
|  - - text | 0..1 | **Not Used** | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | **Plain text representation of the concept** |
|  - hospitalization | 0..1 | **Not Used** | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html) | **Details about the admission to a healthcare service** |
|  - - extension (admissionMethod) | 0..* | **Not Used** | [Extension-CareConnect-AdmissionMethod-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-AdmissionMethod-1) | **Additional Content defined by implementations<br/>Constraint (ext-1): Must have either extensions or value[x], not both** |
|  - - -  url | 1..1 | **Not Used** | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | **Identifies The Meaning Of The Extension<br/>Fixed Value: https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-AdmissionMethod-1** |
|  - - - value[x] | 0..1 | **Not Used** | [*](http://hl7.org/fhir/stu3/datatypes.html#open) | **Value of extension** |
|  - - extension (dischargeMethod) | 0..* | **Not Used** | [Extension-CareConnect-DischargeMethod-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-DischargeMethod-1) | **Additional Content defined by implementations<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>URL: https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-DischargeMethod-1** |
|  - - - url | 1..1 | **Not Used** | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | **Identifies The Meaning Of The Extension<br/>Fixed Value: https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-DischargeMethod-1** |
|  - - - value[x] | 0..1 | **Not Used** | [*](http://hl7.org/fhir/stu3/datatypes.html#open) | **Value of extension** |
|  - - modifierExtension | 0..* | **Not Used** | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension) | **Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both** |
|  - - admitSource | 0..1 | **Not Used** | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept) | [**From where patient was admitted (physician referral, transfer). Binding (required): The source of admission to a Hospital Provider Spell or a Nursing Episode when the Patient is in a Hospital Site or a Care Home. (https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-SourceOfAdmission-1 )**](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-SourceOfAdmission-1) |
|  - - - coding | 0..* | **Not Used** | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding) | **Code defined by a terminology system** |
|  - - - system | 0..1 | **Not Used** | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | **Identity of the terminology system<br/>Fixed Value: https://fhir.hl7.org.uk/STU3/CodeSystem/CareConnect-SourceOfAdmission-1** |
|  - - - version | 0..1 | **Not Used** | String | **Version of the system - if relevant** |
|  - - - code | 0..1 | **Not Used** | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | **Symbol in syntax defined by the system** |
|  - - - display | 0..1 | **Not Used** | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | **Representation defined by the system** |
|  - - - userSelected | 0..1 | **Not Used** | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean) | **If this coding was chosen directly by the user** |
|  - - text | 0..1 | **Not Used** | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | **Plain text representation of the concept** |
|  - - destination | 0..1 | **Not Used** | [Reference](http://hl7.org/fhir/stu3/references.html) | **Location to which the patient is discharged<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided** |
|   | 0.1 | **Not Used** | CareConnect-NHSD-Location |  |
|  - - - reference | 0..1 | **Not Used** | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | **Literal reference, Relative, internal or absolute URL** |
|  - - - identifier | 0..1 | **Not Used** | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier) | **Logical reference, when literal reference is not known** |
|  - - - display | 0..1 | **Not Used** | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | **Text alternative for the resource** |
|  - - dischargeDisposition | 0..1 | **Not Used** | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept) | [**Category or kind of location after discharge. Binding (required): The destination of a Patient on completion of a Hospital Provider Spell, or a note that the Patient died or was a still birth. ( https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-DischargeDestination-1 )**](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-DischargeDestination-1) |
|  - - - coding | 0..* | **Not Used** | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding) | **Code defined by a terminology system** |
|  - - - system | 0..1 | **Not Used** | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | **Identity of the terminology system<br/>Fixed Value: https://fhir.hl7.org.uk/STU3/CodeSystem/CareConnect-DischargeDestination-1** |
|  - - - version | 0..1 | **Not Used** | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | **Version of the system - if relevant** |
|  - - - code | 0..1 | **Not Used** | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | **Symbol in syntax defined by the system** |
|  - - - display | 0..1 | **Not Used** | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | **Representation defined by the system** |
|  - - - userSelected | 0..1 | **Not Used** | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean) | **If this coding was chosen directly by the user** |
|  - - text | 0..1 | **Not Used** | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | **Plain text representation of the concept** |
|  - location | 1..1 | **Not Used** | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html) | **List of locations where the patient has been** |
|  - - modifierExtension | 0..* | **Not Used** | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension) | **Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both** |
|  - - location | 1..1 | **Not Used** | [Reference](http://hl7.org/fhir/stu3/references.html) | **Location the encounter takes place<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided** |
|   |  | **Not Used** | CareConnect-NHSD-Location-1 |  |
|  - - - reference | 1..1 | **Not Used** | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | **Literal reference, Relative, internal or absolute URL** |
|  - - - identifier | 0..1 | **Not Used** | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier) | **Logical reference, when literal reference is not known** |
|  - - status | 0..1 | **Not Used** | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | **Text alternative for the resource** |
|   | 0..1 | **Not Used** | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | [**planned : active : reserved : completed. Binding (required): The status of the location. ( http://hl7.org/fhir/stu3/valueset-encounter-location-status.html )**](http://hl7.org/fhir/stu3/valueset-encounter-location-status.html) |
|  - - - period | 0..1 | **Not Used** | [Period](http://hl7.org/fhir/stu3/datatypes.html#period) | **Time period during which the patient was present at the location<br/>Constraint (per-1): If present, start SHALL have a lower value than end** |
|  - - - - start | 0..1 | **Not Used** | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime) | **Starting time with inclusive boundary** |
|  - - - - end | 0..1 | **Not Used** | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime) | **End time with inclusive boundary, if not ongoing** |
|  - - serviceProvider | 1..1 | **Not Used** | [Reference](http://hl7.org/fhir/stu3/references.html) | **The custodian organization of this Encounter record<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided** |
|   |  | **Not Used** | CareConnect-NHSD-Organization-1 |  |
|  - - - reference | 1..1 | **Not Used** | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | **Literal reference, Relative, internal or absolute URL** |
|  - - - identifier | 0..1 | **Not Used** | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier) | **Logical reference, when literal reference is not known** |
|  - - - display | 0..1 | **Not Used** | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | **Text alternative for the resource** |

## Mapping for Patient ## 

|   |  |  |  |  |
|  ------ | ------ | ------ | ------ | ------ |
|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for XXX Implementation** |
|  Patient | ​ |  |  | Information about an individual receiving health care services<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - id | 0..1 | Not Used | [Id](http://hl7.org/fhir/stu3/datatypes.html#id) | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta) | Metadata about the resource. <font color="red">The profile element MUST contain the value https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-NHSD-Patient-1</font> |
|  - implicitRules | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | A set of rules under which this content was created |
|  - language | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | [Language of the resource content. Binding (extensible): A human language. ( http://hl7.org/fhir/stu3/valueset-languages.html )](http://hl7.org/fhir/stu3/valueset-languages.html) |
|  - text | 0..1 | Not Used | [Narrative](http://hl7.org/fhir/stu3/narrative.html#Narrative) | Text summary of the resource, for human interpretation |
|  - contained | 0..* | Not Used | [Resource](http://hl7.org/fhir/stu3/resource.html) | Contained, inline Resources |
|  - extension (ethnicCategory) | 0..1 | Not Used | [Extension-CareConnect-EthnicCategory-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-EthnicCategory-1) | Ethnic category<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>Must be populated as specified [here](explore_birth_details.html#mapping-for-patient) |
|  - extension (religiousAffiliation) | 0..1 | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension) | Religious affiliation<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>URL: https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-ReligiousAffiliation-1 |
|  - extension (patient-cadavericDonor) | 0..1 | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension) | Flag indicating whether the patient authorized the donation of body parts after death<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>URL: http://hl7.org/fhir/StructureDefinition/patient-cadavericDonor |
|  - extension (residentialStatus) | 0..1 | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension) | The residential status of the patient<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>URL: https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-ResidentialStatus-1 |
|  - extension (treatmentCategory) | 0..1 | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension) | The treatment category for this patient<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>URL: https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-TreatmentCategory-1 |
|  - extension (nhsCommunication) | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension) | NHS communication preferences for a resource<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>URL: https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-NHSCommunication-1 |
|  - extension (birthPlace) | 0..1 | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension) | Birth Place: The registered place of birth of the patient.<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>URL: http://hl7.org/fhir/StructureDefinition/birthPlace |
|  - extension (nominatedPharmacy) | 0..1 | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension) | A patient's nominated pharmacy<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>URL: https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-NominatedPharmacy-1 |
|  - extension (deathNotificationStatus) | 0..1 | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension) | Representation of a patient’s death notification status (as held on Personal Demographics Service (PDS))<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>URL: https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-DeathNotificationStatus-1 |
|  - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension) | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>Slicing: Description: Extensions are always sliced by (at least) url, Discriminator: url, Ordering: false, Rules: Open |
|  - identifier | 0..* | Mandatory | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier) | An identifier for this patient<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open at End |
|  - - identifier (nhsNumber) | 0..1 | Mandatory | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier) | The patient's NHS number |
|  - - extension (nhsNumberVerificationStatus) | 1..1 | Mandatory | [Extension-CareConnect-NHSNumberVerificationStatus-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-NHSNumberVerificationStatus-1) | NHS number verification status<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - use | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | usual <code>&amp;#124;</code> official <code>&amp;#124;</code> temp <code>&amp;#124;</code> secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known . ( http://hl7.org/fhir/stu3/valueset-identifier-use.html ) |
|  - - type | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept) | Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. ( http://hl7.org/fhir/stu3/valueset-identifier-type.html ) |
|  - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | The namespace for the identifier value<br/>Fixed Value: https://fhir.nhs.uk/Id/nhs-number |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | The value that is unique |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period) | Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - assigner | 0..1 | Not Used | Reference ( CareConnect-Organization-1 ) | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - active | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean) | Whether this patient's record is in active use<br/>Default Value: true |
|  - name | 1..* | Mandatory | [HumanName](http://hl7.org/fhir/stu3/datatypes.html#humanname) | A name associated with the patient<br/>Slicing: Discriminator: use, Ordering: false, Rules: Open at End |
|  - name (official) | 1..1 | Mandatory | [HumanName](http://hl7.org/fhir/stu3/datatypes.html#humanname) | A name associated with the patient |
|  - - use | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | usual <code>&amp;#124;</code> official <code>&amp;#124;</code> temp <code>&amp;#124;</code> nickname <code>&amp;#124;</code> anonymous <code>&amp;#124;</code> old <code>&amp;#124;</code> maiden<br/>Fixed Value: official<br/>Binding (required): The use of a human name ( https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-NameUse-1 ) |
|  - - text | 0..1 | Select | String | Text representation of the full name |
|  - - family | 1..1 | Select | String | Family name (often called 'Surname') |
|  - - given | 0..* | Select | String | Given names (not always 'first'). Includes middle names |
|  - - prefix | 0..* | Select | String | Parts that come before the name |
|  - - suffix | 0..* | Select | String | Parts that come after the name |
|  - - period | 0..1 | Select | [Period](http://hl7.org/fhir/stu3/datatypes.html#period) | Time period when name was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Select | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime) | Starting time with inclusive boundary |
|  - - - end | 0..1 | Select | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime) | End time with inclusive boundary, if not ongoing |
|  - name (other) | 0..* | Select | [HumanName](http://hl7.org/fhir/stu3/datatypes.html#humanname) | A name associated with the patient |
|  - - use | 1..1 | Select | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | usual <code>&amp;#124;</code> official <code>&amp;#124;</code> temp <code>&amp;#124;</code> nickname <code>&amp;#124;</code> anonymous <code>&amp;#124;</code> old <code>&amp;#124;</code> maiden<br/>Binding (required): The use of a human name ( https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-NameUse-1 ) |
|  - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Text representation of the full name |
|  - - family | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Family name (often called 'Surname') |
|  - - given | 0..* | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Given names (not always 'first'). Includes middle names |
|  - - prefix | 0..* | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Parts that come before the name |
|  - - suffix | 0..* | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Parts that come after the name |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period) | Time period when name was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime) | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime) | End time with inclusive boundary, if not ongoing |
|  - telecom | 0..* | Not Used | [ContactPoint](http://hl7.org/fhir/stu3/datatypes.html#contactpoint) | A contact detail for the individual<br/>Constraint (cpt-2): A system is required if a value is provided. |
|  - - system | 1..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | phone <code>&amp;#124;</code> fax <code>&amp;#124;</code> email <code>&amp;#124;</code> pager <code>&amp;#124;</code> url <code>&amp;#124;</code> sms <code>&amp;#124;</code> other<br/>Binding (required): Telecommunications form for contact point ( http://hl7.org/fhir/stu3/valueset-contact-point-system.html ) |
|  - - value | 1..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | The actual contact point details |
|  - - use | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | home <code>&amp;#124;</code> work <code>&amp;#124;</code> temp <code>&amp;#124;</code> old <code>&amp;#124;</code> mobile - purpose of this contact point<br/>Binding (required): Use of contact point ( http://hl7.org/fhir/stu3/valueset-contact-point-use.html ) |
|  - - rank | 0..1 | Not Used | [positiveInt](http://hl7.org/fhir/stu3/datatypes.html#positiveint) | Specify preferred order of use (1 = highest) |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period) | Time period when the contact point was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime) | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime) | End time with inclusive boundary, if not ongoing |
|  - gender | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | male <code>&amp;#124;</code> female <code>&amp;#124;</code> other <code>&amp;#124;</code> unknown<br/>Binding (required): The gender of a person used for administrative purposes. (https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-AdministrativeGender-1 ) |
|  - birthDate | 0..1 | Mandatory | [Date](http://hl7.org/fhir/stu3/datatypes.html#date) | The date of birth for the individual |
|  - - extension (patient-birthTime) | 0..1 | Mandatory | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension) | The time of day that the Patient was born. This includes the date to ensure that the timezone information can be communicated effectively.<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>URL: http://hl7.org/fhir/StructureDefinition/patient-birthTime |
|  - deceased[x] | 0..1 | Not Used | Boolean <code>&amp;#124;</code> dateTime | Indicates if the individual is deceased or not |
|  - address | 0..* | Mandatory | [Address](http://hl7.org/fhir/stu3/datatypes.html#address) | Addresses for the individual |
|  - - use | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | home <code>&amp;#124;</code> work <code>&amp;#124;</code> temp <code>&amp;#124;</code> old - purpose of this address<br/>Binding (required): The use of an address ( http://hl7.org/fhir/stu3/valueset-address-use.html ) |
|  - - type | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | postal <code>&amp;#124;</code> physical <code>&amp;#124;</code> both<br/>Binding (required): The type of an address (physical / postal) ( http://hl7.org/fhir/stu3/valueset-address-type.html ) |
|  - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Text representation of the address |
|  - - line | 0..* | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Street name, number, direction & P.O. Box etc. |
|  - - city | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Name of city, town etc. |
|  - - district | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | District name (aka county) |
|  - - state | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Sub-unit of country (abbreviations ok) |
|  - - postalCode | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Postal code for area |
|  - - country | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Country (e.g. can be ISO 3166 2 or 3 letter code) |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period) | Time period when address was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime) | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime) | End time with inclusive boundary, if not ongoing |
|  - maritalStatus | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept) | Marital (civil) status of a patient<br/>Binding (required): The domestic partnership status of a person. (https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-MaritalStatus-1 ) |
|  - - coding | 1..1 | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding) | Code defined by a terminology system |
|  - - - system | 1..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | Identity of the terminology system |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Version of the system - if relevant |
|  - - - code | 1..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | Symbol in syntax defined by the system |
|  - - - display | 1..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Representation defined by the system |
|  - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean) | If this coding was chosen directly by the user |
|  - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Plain text representation of the concept |
|  - multipleBirth[x] | 0..1 | Mandatory | Boolean <code>&amp;#124;</code> Integer | Whether patient is part of a multiple birth |
|  - photo | 0..* | Not Used | [Attachment](http://hl7.org/fhir/stu3/datatypes.html#attachment) | Image of the patient<br/>Constraint (att-1): It the Attachment has data, it SHALL have a contentType |
|  - - contentType | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | Mime type of the content, with charset etc.<br/>Binding (required): The mime type of an attachment. Any valid mime type is allowed. ( http://www.rfc-editor.org/bcp/bcp13.txt ) |
|  - - language | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | Human language of the content (BCP-47)<br/>Binding (extensible): A human language. ( http://hl7.org/fhir/stu3/valueset-languages.html ) |
|  - - data | 0..1 | Not Used | [base64Binary](http://hl7.org/fhir/stu3/datatypes.html#base64binary) | Data inline, base64ed |
|  - - url | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | Uri where the data can be found |
|  - - size | 0..1 | Not Used | [unsignedInt](http://hl7.org/fhir/stu3/datatypes.html#unsignedint) | Number of bytes of content (if url provided) |
|  - - hash | 0..1 | Not Used | [base64Binary](http://hl7.org/fhir/stu3/datatypes.html#base64binary) | Hash of the data (sha-1, base64ed) |
|  - - title | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Label to display in place of the data |
|  - - creation | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime) | Date attachment was first created |
|  - contact | 0..* | Not Used | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html) | A contact party (e.g. guardian, partner, friend) for the patient<br/>Constraint (pat-1): SHALL at least contain a contact's details or a reference to an organization |
|  - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension) | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - relationship | 0..* | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept) | The kind of relationship<br/>Binding (extensible): The nature of the relationship between a patient and a contact person for that patient. (http://hl7.org/fhir/ValueSet/v2-0131 ) |
|  - - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding) | Code defined by a terminology system |
|  - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | Identity of the terminology system |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Version of the system - if relevant |
|  - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Representation defined by the system |
|  - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean) | If this coding was chosen directly by the user |
|  - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Plain text representation of the concept |
|  - - name | 1..1 | Not Used | [HumanName](http://hl7.org/fhir/stu3/datatypes.html#humanname) | A name associated with the contact person |
|  - - - use | 1..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | usual <code>&amp;#124;</code> official <code>&amp;#124;</code> temp <code>&amp;#124;</code> nickname <code>&amp;#124;</code> anonymous <code>&amp;#124;</code> old <code>&amp;#124;</code> maiden<br/>Binding (required): The use of a human name ( http://hl7.org/fhir/stu3/valueset-name-use.html ) |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Text representation of the full name |
|  - - - family | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Family name (often called 'Surname') |
|  - - - given | 0..* | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Given names (not always 'first'). Includes middle names |
|  - - - prefix | 0..* | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Parts that come before the name |
|  - - - suffix | 0..* | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Parts that come after the name |
|  - - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period) | Time period when name was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime) | Starting time with inclusive boundary |
|  - - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime) | End time with inclusive boundary, if not ongoing |
|  - - telecom | 0..* | Not Used | [ContactPoint](http://hl7.org/fhir/stu3/datatypes.html#contactpoint) | A contact detail for the person<br/>Constraint (cpt-2): A system is required if a value is provided. |
|  - - - system | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | phone <code>&amp;#124;</code> fax <code>&amp;#124;</code> email <code>&amp;#124;</code> pager <code>&amp;#124;</code> url <code>&amp;#124;</code> sms <code>&amp;#124;</code> other<br/>Binding (required): Telecommunications form for contact point ( http://hl7.org/fhir/stu3/valueset-contact-point-system.html ) |
|  - - - value | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | The actual contact point details |
|  - - - use | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | home <code>&amp;#124;</code> work <code>&amp;#124;</code> temp <code>&amp;#124;</code> old <code>&amp;#124;</code> mobile - purpose of this contact point<br/>Binding (required): Use of contact point ( http://hl7.org/fhir/stu3/valueset-contact-point-use.html ) |
|  - - - rank | 0..1 | Not Used | [positiveInt](http://hl7.org/fhir/stu3/datatypes.html#positiveint) | Specify preferred order of use (1 = highest) |
|  - - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period) | Time period when the contact point was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime) | Starting time with inclusive boundary |
|  - - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime) | End time with inclusive boundary, if not ongoing |
|  - - address | 0..1 | Not Used | [Address](http://hl7.org/fhir/stu3/datatypes.html#address) | Address for the contact person |
|  - - - use | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | home <code>&amp;#124;</code> work <code>&amp;#124;</code> temp <code>&amp;#124;</code> old - purpose of this address<br/>Binding (required): The use of an address ( http://hl7.org/fhir/stu3/valueset-address-use.html ) |
|  - - - type | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | postal <code>&amp;#124;</code> physical <code>&amp;#124;</code> both<br/>Binding (required): The type of an address (physical / postal) ( http://hl7.org/fhir/stu3/valueset-address-type.html ) |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Text representation of the address |
|  - - - line | 0..* | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Street name, number, direction & P.O. Box etc. |
|  - - - city | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Name of city, town etc. |
|  - - - district | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | District name (aka county) |
|  - - - state | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Sub-unit of country (abbreviations ok) |
|  - - - postalCode | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Postal code for area |
|  - - - country | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Country (e.g. can be ISO 3166 2 or 3 letter code) |
|  - - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period) | Time period when address was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime) | Starting time with inclusive boundary |
|  - - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime) | End time with inclusive boundary, if not ongoing |
|  - - gender | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | male <code>&amp;#124;</code> female <code>&amp;#124;</code> other <code>&amp;#124;</code> unknown<br/>Binding (required): The gender of a person used for administrative purposes. (https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-AdministrativeGender-1 ) |
|  - - organization | 0..1 | Not Used | Reference ( CareConnect-Organization-1 ) | Organization that is associated with the contact<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier) | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Text alternative for the resource |
|  - - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period) | The period during which this contact person or organization is valid to be contacted relating to this patient<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime) | Starting time with inclusive boundary |
|  - - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime) | End time with inclusive boundary, if not ongoing |
|  - generalPractitioner | 0..* | Not Used | Reference ( CareConnect-Organization-1 <code>&amp;#124;</code> CareConnect-Practitioner-1 ) | Patient's nominated primary care provider<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier) | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Text alternative for the resource |
|  - managingOrganization | 0..1 | Not Used | Reference ( CareConnect-Organization-1 ) | Organization that is the custodian of the patient record<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier) | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Text alternative for the resource |
|  - link | 0..* | Not Used | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html) | Link to another patient resource that concerns the same actual person |
|  - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension) | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - other | 1..1 | Not Used | Reference ( RelatedPerson <code>&amp;#124;</code>CareConnect-Patient-1 ) | The other patient or related person resource that the link refers to<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier) | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Text alternative for the resource |

| Maternity-Record Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| Location of Birth                   | CareConnect-Maternity-Record-Delivery-Location-1.identifier (ODS Site Code)           | Required                   |
| Delivery Place Type Code            | CareConnect-Maternity-Record-Delivery-Location-1.physicalType                        | Mandatory                   |
| Birth Order                         | CareConnect-Maternity-Record-Patient-1.multipleBirthInteger                     | Mandatory                   |
| Length of Gestation at Birth        | CareConnect-Maternity-Record-LengthOfGestation-Observation-1.valueQuantity           | Mandatory                   |
| Number of Births in confinement     | CareConnect-Maternity-Record-NumberOfBirths-Observation-1.valueQuantity                  | Mandatory                    |
| Problems during Delivery            | CareConnect-Maternity-Record-ProblemDuringDelivery-Condition-1.code                          | Required                    |
| Physical Problems detected at Birth | CareConnect-Maternity-Record-PhysicalProblemAtBirth-Condition-1.code            | Required                    |
| Neonatal Resuscitation Method       | CareConnect-Maternity-Record-NeonatalResuscitationMethod-Procedure-1.code                           | Required                 |
| Date and Time of Birth              | CareConnect-Maternity-Record-Patient-1.birthDate (with patient-BirthTime extension)                           | Mandatory                 |
| Type of Delivery                    | CareConnect-Maternity-Record-FinalDeliveryType-Procedure-1.code   | Mandatory                    |
| Attempted Type of Delivery          | CareConnect-Maternity-Record-AttemptedDeliveryType-Condition-1.code   | Required                    |
| Onset of Spontaneous Respiration    | CareConnect-Maternity-Record-SpontaneousRespirationOnset-Observation-1.component  | Optional                    |
| APGAR Score (1 Minute)              | CareConnect-Maternity-Record-APGARScore-Observation-1.valueQuantity                 | Mandatory                   |
| APGAR Score (5 Minute)              | CareConnect-Maternity-Record-APGARScore-Observation-1.valueQuantity                  | Mandatory                   |
| APGAR Score (10 Minute)             | CareConnect-Maternity-Record-APGARScore-Observation-1.valueQuantity                | Optional                    |
| Put To Breast                       | CareConnect-Maternity-Record-PutToBreastIndicator-Observation-1.code                  | Required                    |
| Identical Twin Indicator	      | CareConnect-Maternity-Record-IdenticalTwinIndicator-Observation-1.code               | Optional                    |

