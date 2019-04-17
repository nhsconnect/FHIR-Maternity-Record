---
title: Attendance Details List
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_attendance_details_all.html
summary: "The FHIR profiles used for the Attendance details List"
---

## Heading Description ##
The details of the woman’s contact with services.

The following FHIR profiles are used to form the Attendance details list structure:

- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)
- [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)
- [CareConnect-Communication-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Commmunication-1)
- [CareConnect-EpisodeOfCare-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-EpisodeOfCare-1)
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)

The following profiles are referenced from the Attendance details list structure:

- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)

## Attendance Details Structure ##

{% include custom/attendance_details.svg %}

## Maternity Data Standard Mapping to FHIR profiles ##

## Mapping Overview ##


|**Data Standard Element**|**FHIR Profile Mapping**|**FHIR Element**|
|Date/Time|[List](explore_attendance_details.html#mapping-for-attendance_details-list)|period|
|ODS/ORD Site Code|[Location](explore_attendance_details.html#mapping-for-attendance_details-location)|identifier|
|Location Type|[Encounter](explore_attendance_details.html#mapping-for-attendance_details-location)|class|
|Professional Name|[Practitioner](explore_attendance_details.html#mapping-for-attendance_details-practitioner)|name|
|SDS Job Role Name|[PractitionerRole](explore_attendance_details.html#mapping-for-attendance_details-practitionerrole)|identifier|
|Contact type|[Encounter](explore_attendance_details.html#mapping-for-attendance_details-encounter)|type|
|Consultation method|[Communication](explore_attendance_details.html#mapping-for-attendance_details-communication)|medium|
|Care setting|[Location](explore_attendance_details.html#mapping-for-attendance_details-location)|type|
|Service|[EpisodeOfCare](explore_attendance_details.html#mapping-for-attendance_details-episodeofcare)|type|
|Care professional present (name)|[Practitioner](explore_attendance_details.html#mapping-for-attendance_details-practitioner)|name|
|Care professional present (role)|[PractitionerRole](explore_attendance_details.html#mapping-for-attendance_details-practitionerrole)|role|
|Care professionals present type|[Encounter](explore_attendance_details.html#mapping-for-attendance_details-encounter)|participant.type|
|First Given Name|[RelatedPerson](explore_attendance_details.html#mapping-for-attendance_details-relatedperson)|name|
|Family Name|[RelatedPerson](explore_attendance_details.html#mapping-for-attendance_details-relatedperson)|name|
|Relationship of person accompanying patient|[Encounter](explore_attendance_details.html#mapping-for-attendance_details-encounter)|participant.type|
|Outcome of contact|OutcomeOfAttendance extension |Currently not mapped due to "required" valueSet issues|


## Mapping for Attendance Details List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3|None|

|**[View Used FHIR Elements](explore_attendance_details.html#mapping-for-attendance-details-list)**|**[View All FHIR Elements]**|


|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  List | ​ |  |  | Information summarized from a list of other resources<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (lst-2): The deleted flag can only be used if the mode of the list is "changes"<br/>Constraint (lst-1): A list can only have an emptyReason if it is empty |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-List-1'</font> |
|  - implicitRules | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | A set of rules under which this content was created |
|  - language | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Language of the resource content<br/>Binding (extensible): A human language. [Common Languages](http://hl7.org/fhir/stu3/valueset-languages.html) |
|  - text | 0..1 | Not Used | [Narrative](http://hl7.org/fhir/stu3/narrative.html#Narrative "Narrative") | Text summary of the resource, for human interpretation |
|  - contained | 0..* | Not Used | [Resource](http://hl7.org/fhir/stu3/resource.html "Resource") | Contained, inline Resources |
|  - extension (clinicalSetting) | 0..1 | Not Used | [Extension-CareConnect-ClinicalSetting-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-ClinicalSetting-1 "Extension-CareConnect-ClinicalSetting-1") | **To record the clinical setting of a problem list<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>** |
|  - extension (warningCode) | 0..1 | Not Used | [Extension-CareConnect-ListWarningCode-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-ListWarningCode-1 "Extension-CareConnect-ListWarningCode-1") | **To capture warnings that the list may be incomplete<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>** |
|  - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>Slicing: Description: Extensions are always sliced by (at least) url, Discriminator: url, Ordering: false, Rules: Open |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business identifier<br/><font color='red'>An identifier for this Attendance details list</font><br/> |
|  - - use | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known. [IdentifierUse](http://hl7.org/fhir/stu3/valueset-identifier-use.html) |
|  - - type | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [Identifier Type Codes](http://hl7.org/fhir/stu3/valueset-identifier-type.html) |
|  - - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique<br/>Business identifier<br/><font color='red'>An identifier for this Attendance details list</font> |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | <font color='red'>An identifier'</font> |
|  - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - - assigner | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource<br/><font color='red'>The organization that allocated the identifier</font> |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | current : retired : entered-in-error<br/>Binding (required): The current state of the list [ListStatus](http://hl7.org/fhir/stu3/valueset-list-status.html)<br/><font color='red'>The status of the list MUST contain the value 'current'</font> |
|  - mode | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | working : snapshot : changes<br/>Binding (required): The processing mode that applies to this list [ListMode](http://hl7.org/fhir/stu3/valueset-list-mode.html)<br/><font color='red'>The mode of the list MUST contain the value 'snapshot'</font> |
|  - title | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Descriptive name for the list<br/><font color='red'>This MUST contain the value 'Attendance details'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading Attendance details'</b></font>  |
|  - code | 0..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | What the purpose of this list is<br/>Binding (preferred): What the purpose of a list is [CareConnect-ListCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListCode-1)<br/><font color='red'>The PRSB heading for this list. Note: for Maternity the value stated below is used which is not from the preferred value set </font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/><font color='red'>The SNOMED CT concept for the PRSB heading type</font> |
|  - - - system | 0..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant<br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font>  |
|  - - - code | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value '1077881000000105'</font> |
|  - - - display | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>This MUST contain the value 'Attendance details'</font><br/><font color='red'>Mapping to Maternity data item = 'PSRB Heading Attendance details'</font>  |
|  - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Not Used | [Group](http://hl7.org/fhir/STU3/group.html "Group") |  |
|   |  | Not Used | [Device](http://hl7.org/fhir/stu3/StructureDefinition/Device "Device") |  |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color='red'>This is the subject of the Attendance details List.<br/>This MUST use the CareConnect patient profile. </font>See[patient resource reference](explore_attendance_details.html#patient-reference) for information on how to populate the resource. |
|   |  | Not Used | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") |  |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - encounter | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Context in which list created<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>A reference to the encounter resource within the Attendance details list. </font/> <br/> |
|   |  | Not Used | [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1 "CareConnect-Encounter-1") | This is the context of the Attendance details List.<br/>This MUST use the CareConnect encounter profile. See [encounter resource](explore_attendance_details.html#mapping-for-attendance-details-encounter) for information on how to populate the resource. |
|  - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - date | 0..1 | Mandatory | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the list was prepared<br/><font color='red'> This MUST contain a system date to indicate when the list created or updated</font> |
|  - source | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who and/or what defined the list contents (aka Author)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [Device](http://hl7.org/fhir/stu3/StructureDefinition/Device "Device") |  |
|   |  | Not Used | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|   |  | Not Used | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") |  |
|  - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - orderedBy | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | What order the list has<br/>Binding (preferred): What order applies to the items in a list [List Order Codes](http://hl7.org/fhir/stu3/valueset-list-order.html) |
|  - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - note | 0..* | Optional | [Annotation](http://hl7.org/fhir/stu3/datatypes.html#annotation "Annotation") | Comments about the list |
|  - - author[x] | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Individual responsible for the annotation<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [RelatedPerson](http://hl7.org/fhir/stu3/StructureDefinition/RelatedPerson "RelatedPerson") |  |
|   |  | Not Used | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|   |  | Not Used | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") |  |
|   |  | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | <font color='red'>Who authored the comment on the list.</font>  |
|  - - time | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the annotation was made |
|  - - text | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The annotation - text content |
|  - entry | 0..* | Mandatory | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Entries in the list<br/><font color='red'>The entries MUST be as per the diagram for this PRSB headings list with the encounter resource being the focal resource. Multiple Encounters with associated resources MAY be present</font> |
|  - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - flag | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Status/Workflow information about this item<br/>Binding (example): Codes that provide further information about the reason and meaning of the item in the list [Patient Medicine Change Types](http://hl7.org/fhir/stu3/valueset-list-item-flag.html) |
|  - - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - deleted | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this item is actually marked as deleted<br/>Default Value: false |
|  - - date | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When item added to list<br/><font color='red'>The SHOULD contain a system time of when the item was added to the list.</font> |
|  - - item | 1..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>A reference to an Encounter resource included in the list<br/>This MUST use the CareConnect Encounter profile. </font>See [Encounter resource](explore_attendance_details.html#mapping-for-attendance-details-encounter) for information on how to populate the resource. |
|   |  | Not Used | [Resource](http://hl7.org/fhir/stu3/StructureDefinition/Resource "Resource") |  |
|  - - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>The reference to the included Encounter resource.</font> |
|  - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - emptyReason | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Why list is empty<br/>Binding (preferred): If a list is empty, why it is empty [CareConnect-ListEmptyReasonCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListEmptyReasonCode-1) |
|  - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |

## Mapping for Attendance Details Encounter ##

|>|Level 1|[Encounter Resource](http://hl7.org/fhir/stu3/encounter.html)|>|Level 2|[CareConnect-Encounter-1(https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)|>|Level 3|None|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  Encounter | ​ |  |  | An interaction during which services are provided to the patient<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Encounter-1'</font> |
|  - implicitRules | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | A set of rules under which this content was created |
|  - language | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Language of the resource content<br/>Binding (extensible): A human language. [Common Languages](http://hl7.org/fhir/stu3/valueset-languages.html) |
|  - text | 0..1 | Not Used | [Narrative](http://hl7.org/fhir/stu3/narrative.html#Narrative "Narrative") | Text summary of the resource, for human interpretation |
|  - contained | 0..* | Not Used | [Resource](http://hl7.org/fhir/stu3/resource.html "Resource") | Contained, inline Resources |
|  - extension (encounterTransport) | 0..1 | Not Used | [Extension-CareConnect-EncounterTransport-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-EncounterTransport-1 "Extension-CareConnect-EncounterTransport-1") | Encounter transport<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - extension (outcomeOfAttendance) | 0..1 | Required | [Extension-CareConnect-OutcomeOfAttendance-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-OutcomeOfAttendance-1 "Extension-CareConnect-OutcomeOfAttendance-1") | An extension to the Encounter resource to record the outcome of an Out-Patient attendance.<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/><font color='red'>This item is currently not mapped due to issues with the required valueSet</font><br/> |
|  - extension (emergencyCareDischargeStatus) | 0..1 | Not Used | [Extension-CareConnect-EmergencyCareDischargeStatus-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-EmergencyCareDischargeStatus-1 "Extension-CareConnect-EmergencyCareDischargeStatus-1") | An extension to the Encounter resource which is used indicate the status of the Patient on discharge from an Emergency Care Department.<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>Slicing: Description: Extensions are always sliced by (at least) url, Discriminator: url, Ordering: false, Rules: Open |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Identifier(s) by which this encounter is known<br/><font color='red'>An identifier for this Encounter</font> |
|  - - use | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known. [IdentifierUse](http://hl7.org/fhir/stu3/valueset-identifier-use.html) |
|  - - type | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [Identifier Type Codes](http://hl7.org/fhir/stu3/valueset-identifier-type.html) |
|  - - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique<br/><font color='red'>An identifier for this Attendance details encounter</font> |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - - assigner | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | planned : arrived : triaged : in-progress : onleave : finished : cancelled +<br/>Binding (required): Current state of the encounter [EncounterStatus](http://hl7.org/fhir/stu3/valueset-encounter-status.html)<br/><font color='red'>The status of the Encounter MUST contain the value 'finished'</font> |
|  - statusHistory | 0..* | Not Used | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | List of past encounter statuses |
|  - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - status | 1..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | planned : arrived : triaged : in-progress : onleave : finished : cancelled +<br/>Binding (required): Current state of the encounter [EncounterStatus](http://hl7.org/fhir/stu3/valueset-encounter-status.html) |
|  - - period | 1..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | The time that the episode was in the specified status<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - class | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Classification of the encounter<br/>Binding (extensible): Classification of the encounter [ActEncounterCode](http://hl7.org/fhir/stu3/v3/ActEncounterCode/vs.html) |
|  - - system | 0..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - code | 0..1 | Required | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - classHistory | 0..* | Not Used | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | List of past encounter classes |
|  - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - class | 1..1 | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Classification of the encounter<br/>Binding (extensible): Classification of the encounter [ActEncounterCode](http://hl7.org/fhir/stu3/v3/ActEncounterCode/vs.html) |
|  - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | The time that the episode was in the specified class<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - type | 0..1 | Required | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Specific type of encounter<br/>Binding (example): The type of encounter [EncounterType](http://hl7.org/fhir/stu3/valueset-encounter-type.html)<br/> |
|  - - coding | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | <font color='red'>The example MUST not be used the following valeSet MUST be used instead</font> [Care Contact Type](https://www.datadictionary.nhs.uk/data_dictionary/attributes/c/card/care_contact_type_de.asp?shownav=1) |
|  - - coding (snomedCT) | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system that describes an encounter between a care professional and the patient (or patient's record). [CareConnect-EncounterType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-EncounterType-1) |
|  - - - extension (snomedCTDescriptionID) | 0..1 | Not Used | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | The SNOMED CT Description ID for the display<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/> |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - code | 1..1 | Required | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - priority | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Indicates the urgency of the encounter<br/>Binding (example): Indicates the urgency of the encounter. [v3 Code System ActPriority](http://hl7.org/fhir/stu3/v3/ActPriority/vs.html) |
|  - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - subject | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | The patient or group present at the encounter<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [Group](http://hl7.org/fhir/STU3/group.html "Group") |  |
|   |  | Not Used | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|  - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - episodeOfCare | 0..* | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Episode(s) of care that this encounter should be recorded against<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [EpisodeOfCare](http://hl7.org/fhir/stu3/StructureDefinition/EpisodeOfCare "EpisodeOfCare") |  |
|  - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - incomingReferral | 0..* | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | The ReferralRequest that initiated this encounter<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [ReferralRequest](http://hl7.org/fhir/stu3/StructureDefinition/ReferralRequest "ReferralRequest") |  |
|  - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - participant | 0..* | Required | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | List of participants involved in the encounter<br/><font color='red'><b>Mapping to Maternity data item = 'Care professionals present' and 'Person accompanying patient'</b></font> |
|  - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - type | 0..* | Required | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Role of participant in encounter<br/>Binding (extensible): Role of participant in encounter [ParticipantType](http://hl7.org/fhir/stu3/valueset-encounter-participant-type.html)<br/><font color='red'>There will be serveral instances of this element. The first use case is for Care professionals present and this will use a reference to  the Practitioner resource and the second use case is for Person accompanying patient and this will use a reference to  the relatedPerson resource</font><br/><font color='red'><b>Mapping to Maternity data item ='Care professionals present type' and 'Relationship of Person accompanying patient'</b></font> |
|  - - - coding | 1..1 | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/><font color='red'>There will be one instance of the coding for each instance of type</font> |
|  - - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://hl7.org/fhir/ValueSet/encounter-participant-type'</font> |
|  - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>The Care professionals present will use the most appropriate code.</font><br/><font color='red'>The Person accompanying patient will use a code of 'ESC'</font>  |
|  - - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | <font color='red'>The Care professional will use the display associated with the code</font><br/><font color='red'>The Person accompanying patient will use a display of 'escort'</font>  |
|  - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Period of time during the encounter that the participant participated<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - - individual | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Persons involved in the encounter other than the patient<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This MUST be a reference to either the Practitioner or RelatedPerson resource</font> |
|   |  | Required | [RelatedPerson](http://hl7.org/fhir/stu3/StructureDefinition/RelatedPerson "RelatedPerson") | <font color='red'>The person accompanying the patient.<br/>This MUST use the RelatedPerson resource. </font>See [RelatedPerson resource](explore_attendance_details.html#mapping-for-attendance-details-relatedperson) for information on how to populate the resource. |
|   |  | Required | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") | <font color='red'>Care Professionals present during the encounter.<br/>This MUST use the CareConnect Practitioner profile. </font>See [Practitioner resource](explore_attendance_details.html#mapping-for-attendance-details-practitioner) for information on how to populate the resource. |
|  - - - reference | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the RelatedPerson resource or the Practitioner resource included in the Attendance details list</font>  |
|  - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - appointment | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | The appointment that scheduled this encounter<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [Appointment](http://hl7.org/fhir/stu3/StructureDefinition/Appointment "Appointment") |  |
|  - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | The start and end time of the encounter<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary<br/> |
|  - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - length | 0..1 | Not Used | [Duration](http://hl7.org/fhir/stu3/datatypes.html#duration "Duration") | Quantity of time the encounter lasted (less time absent)<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/>Constraint (drt-1): There SHALL be a code if there is a value and it SHALL be an expression of time. If system is present, it SHALL be UCUM. |
|  - - value | 0..1 | Not Used | [Decimal](http://hl7.org/fhir/stu3/datatypes.html#decimal "Decimal") | Numerical value (with implicit precision) |
|  - - comparator | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | < : <= : >= : > - how to understand the value<br/>Binding (required): How the Quantity should be understood and represented. [QuantityComparator](http://hl7.org/fhir/stu3/valueset-quantity-comparator.html) |
|  - - unit | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Unit representation |
|  - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | System that defines coded unit form |
|  - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Coded form of the unit |
|  - reason | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Reason the encounter takes place (code)<br/>Binding (preferred): Reason why the encounter takes place. [Encounter Reason Codes](http://hl7.org/fhir/stu3/valueset-encounter-reason.html)<br/> |
|  - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/><font color='red'>A concept from the Care planning health issues simple reference set</font><br/> |
|  - - - extension (snomedCTDescriptionID) | 0..1 | Not Used | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | The SNOMED CT Description ID for the display<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - system | 1..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - code | 1..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>A SNOMED CT from the Care planning health issues simple reference set as defined above</font>  |
|  - - - display | 1..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>The display associated with the SNOMED CT concept. This SHOULD be the preferred term</font> |
|  - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept<br/><font color='red'>This MAY be used where a suitable coded concept is not available to the sending system</font> |
|  - diagnosis | 0..* | Not Used | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | The list of diagnosis relevant to this encounter |
|  - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - condition | 1..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Reason the encounter takes place (resource)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Procedure-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Procedure-1 "CareConnect-Procedure-1") |  |
|   |  | Not Used | [CareConnect-Condition-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Condition-1 "CareConnect-Condition-1") |  |
|  - - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - - role | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Role that this diagnosis has within the encounter (e.g. Attendance, billing, discharge …)<br/>Binding (preferred): The type of diagnosis this condition represents [DiagnosisRole](http://hl7.org/fhir/stu3/valueset-diagnosis-role.html) |
|  - - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - rank | 0..1 | Not Used | [positiveInt](http://hl7.org/fhir/stu3/datatypes.html#positiveint "positiveInt") | Ranking of the diagnosis (for each role type) |
|  - account | 0..* | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | The set of accounts that may be used for billing for this Encounter<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [Account](http://hl7.org/fhir/stu3/StructureDefinition/Account "Account") |  |
|  - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - hospitalization | 0..1 | Not Used | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Details about the Attendance to a healthcare service |
|  - - extension (AttendanceMethod) | 0..1 | Not Used | [Extension-CareConnect-AdmissionMethod-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-AdmissionMethod-1 "Extension-CareConnect-AdmissionMethod-1") | An extension to the Encounter resource to record how a Patient was admitted to hospital.<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - extension (dischargeMethod) | 0..1 | Not Used | [Extension-CareConnect-DischargeMethod-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-DischargeMethod-1 "Extension-CareConnect-DischargeMethod-1") | An extension to the Encounter resource to record the method of discharge from hospital.<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - preAttendanceIdentifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Pre-Attendance identifier |
|  - - - use | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known . [IdentifierUse](http://hl7.org/fhir/stu3/valueset-identifier-use.html) |
|  - - - type | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [Identifier Type Codes](http://hl7.org/fhir/stu3/valueset-identifier-type.html) |
|  - - - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - - system | 1..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value |
|  - - - value | 1..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - - - assigner | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - - origin | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | The location from which the patient came before Attendance<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") |  |
|  - - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - - admitSource | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | From where patient was admitted (physician referral, transfer)<br/>Binding (preferred): The source of Addmision to a Hospital Provider Spell or a Nursing Episode when the Patient is in a Hospital Site or a Care Home. [CareConnect-SourceOfAddmission-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-SourceOfAddmission-1)<br/> |
|  - - - coding | 0..1 | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - system | 1..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - code | 1..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value 'https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-SourceOfAddmission-1'</font> |
|  - - - - display | 1..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>This MUST contain a code from the stated ValueSet</font>  |
|  - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept<br/> |
|  - - reAttendance | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | The type of hospital re-Attendance that has occurred (if any). If the value is absent, then this is not identified as a reAttendance<br/>Binding (example): The reason for re-admission of this hospitalization encounter. [v2 Re-admission Indicator](http://hl7.org/fhir/ValueSet/v2-0092) |
|  - - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open |
|  - - - coding (snomedCT) | 0..1 | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - extension (snomedCTDescriptionID) | 0..1 | Not Used | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | The SNOMED CT Description ID for the display<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - - system | 1..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - code | 1..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - display | 1..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - dietPreference | 0..* | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Diet preferences reported by the patient<br/>Binding (extensible): Medical, cultural or ethical food preferences to help with catering requirements. [Diet](http://hl7.org/fhir/stu3/valueset-encounter-diet.html) |
|  - - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - specialCourtesy | 0..* | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Special courtesies (VIP, board member)<br/>Binding (preferred): Special courtesies [SpecialCourtesy](http://hl7.org/fhir/stu3/valueset-encounter-special-courtesy.html) |
|  - - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - specialArrangement | 0..* | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Wheelchair, translator, stretcher, etc.<br/>Binding (preferred): Special arrangements [SpecialArrangements](http://hl7.org/fhir/stu3/valueset-encounter-special-arrangements.html) |
|  - - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - destination | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Location to which the patient is discharged<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") |  |
|  - - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - - dischargeDisposition | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Category or kind of location after discharge<br/>Binding (example): The destination of a Patient on completion of a Hospital Provider Spell, or a note that the Patient died or was a still birth. [CareConnect-DischargeDestination-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-DischargeDestination-1) |
|  - - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - location | 0..1 | Required | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | List of locations where the patient has been |
|  - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - location | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Location the encounter takes place<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>The site code of the unit to which the person was admitted</font> |
|   |  | Mandatory | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") | "<font color='red'>The location<br/>This MUST use the CareConnect Location profile. </font>See [Location resource](explore_attendance_details.html#mapping-for-attendance-details-location) for information on how to populate the resource." |
|  - - - reference | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the Location resource included in the Attendance details list</font>  |
|  - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - - status | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | planned : active : reserved : completed<br/>Binding (required): The status of the location. [EncounterLocationStatus](http://hl7.org/fhir/stu3/valueset-encounter-location-status.html) |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Time period during which the patient was present at the location<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - serviceProvider | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | The custodian organization of this Encounter record<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - partOf | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Another Encounter this encounter is part of<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1 "CareConnect-Encounter-1") |  |
|  - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |


## Patient Reference ##

The Admission details list has a mandated subject reference to the Patient resource. This means that any exchange of the Admission details heading data must also include the [Patient demographics List.](explore_patient_demographics.html)


## Mapping for Attendance Details Communication ##

|>|Level 1|[Communication Resource](http://hl7.org/fhir/stu3/communication.html)|>|Level 2|[CareConnect-Communication-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Communication -1)|>|Level 3|None|

|**[View Used FHIR Elements](explore_attendance_details.html#mapping-for-attendance-details-communication)**|**View All FHIR Elements**|  


## Mapping for Attendance Details EpisodeOfCare ##

|>|Level 1|[EpisodeOfCare Resource](http://hl7.org/fhir/stu3/episodeofcare.html)|>|Level 2|[CareConnect-EpisodeOfCare-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-EpisodeOfCare-1)|>|Level 3|None|

|**[View Used FHIR Elements](explore_attendance_details.html#mapping-for-attendance-details-episodeofcare)**|**View All FHIR Elements**|  


## Mapping for Attendance Details Practitioner ##

|>|Level 1|[Practitioner Resource](http://hl7.org/fhir/stu3/practitioner.html)|>|Level 2|[CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)|>|Level 3|None|

|**[View Used FHIR Elements](explore_attendance_details.html#mapping-for-attendance-details-practitioner)**|**View All FHIR Elements**|  


## Mapping for Attendance Details PractitionerRole ##

|>|Level 1|[PractitionerRole Resource](http://hl7.org/fhir/stu3/practitionerrole.html)|>|Level 2|[CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)|>|Level 3|None|

|**[View Used FHIR Elements](explore_attendance_details.html#mapping-for-attendance-details-practitionerrole)**|**View All FHIR Elements**|  


## Mapping for Attendance Details RelatedPerson ##

|>|Level 1|[RelatedPerson Resource](http://hl7.org/fhir/stu3/relatedperson.html)|>|Level 2|[CareConnect-RelatedPerson-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-RelatedPerson-1)|>|Level 3|None|

|**[View Used FHIR Elements](explore_attendance_details_all.html#mapping-for-attendance-details-relatedperson)**|**View All FHIR Elements**|  



## Mapping for Attendance Details Location ##

|>|Level 1|[Location Resource](http://hl7.org/fhir/stu3/location.html)|>|Level 2|[CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)|>|Level 3|None|

|**[View Used FHIR Elements](explore_attendance_details_all.html#mapping-for-attendance-details-location)**|**View All FHIR Elements**|  

## Attendance Details Heading Example ##

<script src="https://gist.github.com/IOPS-DEV/9216149861f148520680e97336625a36.js"></script>