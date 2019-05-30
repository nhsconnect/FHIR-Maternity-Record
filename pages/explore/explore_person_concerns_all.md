---
title: Person concerns List
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_person_concerns_all.html
summary: "The FHIR profiles used for the Person concerns List"
---

## Heading Description ##
Details of the woman’s concerns, expectations and wishes.

The following FHIR profiles are used to form the Person concerns List structure:  
- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)  
- [CareConnect-CarePlan-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-CarePlan-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-Contract-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Contract-1)  

The following profiles are referenced from the Patient demographics list structure:  
- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)

## Person concerns Structure ##

{% include custom/person_concerns.svg %}  

## Maternity data standard Mapping to FHIR profiles ##  

## Mapping Overview ##

|**Data Standard Element**|**FHIR Resource Mapping**|**FHIR Element**|
|Date/time|[CarePlan](explore_person_concerns.html#mapping-for-person-concerns-careplan)|period.start/note.time|
|Concern, wishes or goals details|[CarePlan](explore_person_concerns.html#mapping-for-person-concerns-careplan)|goal/note|
|Maternity Care Plan Type|[CarePlan](explore_person_concerns_all.html#mapping-for-person-concerns-careplan)|category|
|Planned delivery setting|[Location](explore_person_concerns_all.html#mapping-for-person-concerns-location)|type|
|Reason for change of planned delivery setting|[CarePlan](explore_person_concerns_all.html#mapping-for-person-concerns-careplan)|activity.detail.reasonCode|
|Advance Statement Date|[Contract](explore_person_concerns_all.html#mapping-for-person-concerns-contract)|meta.lastUpdated|
|Advance Statement Details|[Contract](explore_person_concerns.html#mapping-for-person-concerns-contract)|text|
|Location of Advance Statement Document||unmapped| 

## Mapping for Person concerns List ##  

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3|None|

|**[View Used FHIR Elements](explore_person_concerns.html#mapping-for-person-concerns-list)**|**View All FHIR Elements**| 


|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  List | ​ |  |  | Information summarized from a list of other resources<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (lst-2): The deleted flag can only be used if the mode of the list is "changes"<br/>Constraint (lst-1): A list can only have an emptyReason if it is empty |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1'</font> |
|  - implicitRules | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | A set of rules under which this content was created |
|  - language | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Language of the resource content<br/>Binding (extensible): A human language. [Common Languages](http://hl7.org/fhir/stu3/valueset-languages.html) |
|  - text | 0..1 | Not Used | [Narrative](http://hl7.org/fhir/stu3/narrative.html#Narrative "Narrative") | Text summary of the resource, for human interpretation |
|  - contained | 0..* | Not Used | [Resource](http://hl7.org/fhir/stu3/resource.html "Resource") | Contained, inline Resources |
|  - extension (clinicalSetting) | 0..1 | Not Used | [Extension-CareConnect-ClinicalSetting-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-ClinicalSetting-1 "Extension-CareConnect-ClinicalSetting-1") | To record the clinical setting of a problem list<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - extension (warningCode) | 0..1 | Not Used | [Extension-CareConnect-ListWarningCode-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-ListWarningCode-1 "Extension-CareConnect-ListWarningCode-1") | To capture warnings that the list may be incomplete<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>Slicing: Description: Extensions are always sliced by (at least) url, Discriminator: url, Ordering: false, Rules: Open |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business identifier<br><font color='red'>An identifier for this Person concerns List</font><br/><br/> |
|  - - use | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known. [IdentifierUse](http://hl7.org/fhir/stu3/valueset-identifier-use.html) |
|  - - type | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [Identifier Type Codes](http://hl7.org/fhir/stu3/valueset-identifier-type.html) |
|  - - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came</font> |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique<br/><font color='red'>A value for the identifier</font> |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Time period when id is/was valid for use |
|  - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - - assigner | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource<br/> |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | current : retired : entered-in-error<br/>Binding (required): The current state of the list [ListStatus](http://hl7.org/fhir/stu3/valueset-list-status.html) |
|  - mode | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | working : snapshot : changes<br/>Binding (required): The processing mode that applies to this list [ListMode](http://hl7.org/fhir/stu3/valueset-list-mode.html)<br/><font color='red'>The mode of the list MUST contain the value 'snapshot'</font> |
|  - title | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Descriptive name for the list<br/><font color='red'>This MUST contain the value 'Person concerns'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading Person concerns'</b></font>  |
|  - code | 0..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | What the purpose of this list is<br/>Binding (preferred): What the purpose of a list is [CareConnect-ListCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListCode-1)<br/><font color='red'>The PRSB heading for this list. Note: for Maternity the value stated below is used which is not from the preferred value set </font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/><font color='red'>The SNOMED CT concept for the PRSB heading type</font> |
|  - - - system | 0..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant<br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font>  |
|  - - - code | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value 'tbc'</font> |
|  - - - display | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>This MUST contain the value 'Person concerns'</font><br/><font color='red'>Mapping to Maternity data item = 'PSRB Heading Person concerns'</font>  |
|  - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Not Used | [Group](http://hl7.org/fhir/STU3/group.html "Group") |  |
|   |  | Not Used | [Device](http://hl7.org/fhir/stu3/StructureDefinition/Device "Device") |  |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color='red'>This is the subject of the Person concerns List.<br/>This MUST use the CareConnect patient profile. </font>See [patient resource reference](explore_person_concerns.html#patient-reference) for information on how to populate the resource. |
|   |  | Not Used | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") |  |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - encounter | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Context in which list created<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><br/> |
|   |  | Not Used | [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1 "CareConnect-Encounter-1") |  |
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
|  - - author[x] | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Individual responsible for the annotation<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [RelatedPerson](http://hl7.org/fhir/stu3/StructureDefinition/RelatedPerson "RelatedPerson") |  |
|   |  | Not Used | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|   |  | Optional | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") |  |
|   |  | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | <font color='red'>Who authored the comment on the list.</font>  |
|  - - time | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the annotation was made |
|  - - text | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The annotation - text content |
|  - entry | 0..* | Mandatory | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Entries in the list<br/><font color='red'>The entries MUST be as per the diagram for this PRSB headings list with the CarePlan resource being the focal resource. </font> |
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
|  - - item | 1..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>A reference to a CarePlan resource included in the list</font><br/> |
|   |  | Not Used | [Resource](http://hl7.org/fhir/stu3/StructureDefinition/Resource "Resource") |  |
|  - - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/> |
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


## Patient Reference ##
The Plan and requested actions List has a mandated subject reference to the Patient resource. This means that any exchange of the Plan and requested actions heading data must also include the [Patient demographics List.](explore_patient_demographics.html)  

## Mapping for Person concerns CarePlan ##  

|>|Level 1|[CarePlan Resource](http://hl7.org/fhir/stu3/careplan.html)|>|Level 2|[CareConnect-CarePlan-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-CarePlan-1)|>|Level 3|None|  

|**[View Used FHIR Elements](explore_person_concerns.html#mapping-for-person-concerns-careplan)**|**View All FHIR Elements**| 


|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| --- | --- | --- | --- | --- |
|  CarePlan | ​ |  |  | Healthcare plan for patient or group<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource  <br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-CarePlan-1'</font>  |
|  - implicitRules | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | A set of rules under which this content was created |
|  - language | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Language of the resource content<br/>Binding (extensible): A human language. [Common Languages](http://hl7.org/fhir/stu3/valueset-languages.html) |
|  - text | 0..1 | Not Used | [Narrative](http://hl7.org/fhir/stu3/narrative.html#Narrative "Narrative") | Text summary of the resource, for human interpretation |
|  - contained | 0..* | Not Used | [Resource](http://hl7.org/fhir/stu3/resource.html "Resource") | Contained, inline Resources |
|  - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>Slicing: Description: Extensions are always sliced by (at least) url, Discriminator: url, Ordering: false, Rules: Open |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | External Ids for this plan <br/><font color='red'>An identifier for this Plan and requested actions CarePlan</font><br/> |
|  - - use | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known. [IdentifierUse](http://hl7.org/fhir/stu3/valueset-identifier-use.html) |
|  - - type | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [Identifier Type Codes](http://hl7.org/fhir/stu3/valueset-identifier-type.html) |
|  - - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system <br/><font color='red'>The system from which the identifier came from</font> |
|  - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - system | 0..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value <br/><font color='red'>The system from which the identifier came</font> |
|  - - value | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique <br/><font color='red'>A value for the identifier for this Plan and requested actions CarePlan</font> |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - - assigner | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - definition | 0..* | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Protocol or definition<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [PlanDefinition](http://hl7.org/fhir/stu3/StructureDefinition/PlanDefinition "PlanDefinition") |  |
|   |  | Not Used | [Questionnaire](http://hl7.org/fhir/stu3/StructureDefinition/Questionnaire "Questionnaire") |  |
|  - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - basedOn | 0..* | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Fulfills care plan<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-CarePlan-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-CarePlan-1 "CareConnect-CarePlan-1") |  |
|  - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - replaces | 0..* | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | CarePlan replaced by this CarePlan<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-CarePlan-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-CarePlan-1 "CareConnect-CarePlan-1") |  |
|  - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - partOf | 0..* | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Part of referenced CarePlan<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-CarePlan-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-CarePlan-1 "CareConnect-CarePlan-1") |  |
|  - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | draft : active : suspended : completed : entered-in-error : cancelled : unknown<br/>Binding (required): Indicates whether the plan is currently being acted upon, represents future intentions or is now a historical record. [CarePlanStatus](http://hl7.org/fhir/stu3/valueset-care-plan-status.html) |
|  - intent | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | proposal : plan : order : option<br/>Binding (required): Codes indicating the degree of authority/intentionality associated with a care plan [CarePlanIntent](http://hl7.org/fhir/stu3/valueset-care-plan-intent.html) |
|  - category | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of plan<br/>Binding (example): Identifies what "kind" of plan this is to support differentiation between multiple co-existing plans; e.g. "Home health", "psychiatric", "asthma", "disease management", etc. [Care Plan Category](http://hl7.org/fhir/stu3/valueset-care-plan-category.html) <br/><font color='red'><b>Mapping to Digital Maternity data item 'Maternity care plan type'</b><br>Valueset Care Plan Type</font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - system | 0..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - code | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - userSelected | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - title | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Human-friendly name for the CarePlan |
|  - description | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Summary of nature of plan |
|  - subject | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who care plan is for<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [Group](http://hl7.org/fhir/stu3/StructureDefinition/Group "Group") |  |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  context | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Created in context of<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-EpisodeOfCare-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-EpisodeOfCare-1 "CareConnect-EpisodeOfCare-1") |  |
|   |  | Mandatory | [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1 "CareConnect-Encounter-1") |  |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - period | 1..1 | Mandatory | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Time period plan covers<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - start | 1..1 | Mandatory | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary<br><font color='red'><b>Mapping to Digital Maternity data item 'Date/time'</b></font>  |
|  - - end | 0..1 | Optional | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - author | 0..* | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who is responsible for contents of the plan<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|   |  | Not Used | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|   |  | Required | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") |  |
|   |  | Not Used | [CareConnect-CareTeam-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-CareTeam-1 "CareConnect-CareTeam-1") |  |
|   |  | Not Used | [CareConnect-RelatedPerson-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-RelatedPerson-1 "CareConnect-RelatedPerson-1") |  |
|  - - reference | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - careTeam | 0..* | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who's involved in plan?<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-CareTeam-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-CareTeam-1 "CareConnect-CareTeam-1") |  |
|  - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - addresses | 0..* | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Health issues this plan addresses<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Condition-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Condition-1 "CareConnect-Condition-1") |  |
|  - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - supportingInfo | 0..* | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Information considered as part of plan<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [Resource](http://hl7.org/fhir/stu3/StructureDefinition/Resource "Resource") |  |
|  - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - goal | 0..* | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Desired outcome of plan<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br><font color='red'><b>Mapping to Digital Maternity data item 'Concern, wishes or goal details'</b></font>  |
|   |  | Required | [Goal](http://hl7.org/fhir/stu3/StructureDefinition/Goal "Goal") |  |
|  - - reference | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - activity | 0..* | Required | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Action to occur as part of plan<br/>Constraint (cpl-3): Provide a reference or detail, not both |
|  - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - outcomeCodeableConcept | 0..* | Optional | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Results of the activity<br/>Binding (example): Identifies the results of the activity [Care Plan Activity Outcome](http://hl7.org/fhir/stu3/valueset-care-plan-activity-outcome.html) |
|  - - - coding | 0..* | Optional | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - system | 0..1 | Optional | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - code | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - userSelected | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - outcomeReference | 0..* | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Appointment, Encounter, Procedure, etc.<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [Resource](http://hl7.org/fhir/stu3/StructureDefinition/Resource "Resource") |  |
|  - - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - - progress | 0..* | Not Used | [Annotation](http://hl7.org/fhir/stu3/datatypes.html#annotation "Annotation") | Comments about the activity status/progress |
|  - - - author[x] | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Individual responsible for the annotation<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") |  |
|   |  | Not Used | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|   |  | Not Used | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") |  |
|   |  | Not Used | [CareConnect-RelatedPerson-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-RelatedPerson-1 "CareConnect-RelatedPerson-1") |  |
|  - - - time | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the annotation was made |
|  - - - text | 1..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The annotation - text content |
|  - - reference | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Activity details defined in specific resource<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [Appointment](http://hl7.org/fhir/stu3/StructureDefinition/Appointment "Appointment") |  |
|   |  | Not Used | [CommunicationRequest](http://hl7.org/fhir/stu3/StructureDefinition/CommunicationRequest "CommunicationRequest") |  |
|   |  | Not Used | [DeviceRequest](http://hl7.org/fhir/stu3/StructureDefinition/DeviceRequest "DeviceRequest") |  |
|   |  | Not Used | [NutritionOrder](http://hl7.org/fhir/stu3/StructureDefinition/NutritionOrder "NutritionOrder") |  |
|   |  | Not Used | [Task](http://hl7.org/fhir/stu3/StructureDefinition/Task "Task") |  |
|   |  | Not Used | [ReferralRequest](http://hl7.org/fhir/stu3/StructureDefinition/ReferralRequest "ReferralRequest") |  |
|   |  | Not Used | [VisionPrescription](http://hl7.org/fhir/stu3/StructureDefinition/VisionPrescription "VisionPrescription") |  |
|   |  | Not Used | [RequestGroup](http://hl7.org/fhir/stu3/StructureDefinition/RequestGroup "RequestGroup") |  |
|   |  | Not Used | [CareConnect-ProcedureRequest-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-ProcedureRequest-1 "CareConnect-ProcedureRequest-1") |  |
|   |  | Not Used | [CareConnect-MedicationRequest-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-MedicationRequest-1 "CareConnect-MedicationRequest-1") |  |
|  - - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - - detail | 0..1 | Not Used | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | In-line definition of activity |
|  - - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - - category | 0..1 | Optional | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | diet : drug : encounter : observation : procedure : supply : other<br/>Binding (example): High-level categorization of the type of activity in a care plan. [CarePlanActivityCategory](http://hl7.org/fhir/stu3/valueset-care-plan-activity-category.html) |
|  - - - - coding | 0..* | Optional | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - - system | 0..1 | Optional | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - - code | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - - userSelected | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - - definition | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Protocol or definition<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [PlanDefinition](http://hl7.org/fhir/stu3/StructureDefinition/PlanDefinition "PlanDefinition") |  |
|   |  | Not Used | [ActivityDefinition](http://hl7.org/fhir/stu3/StructureDefinition/ActivityDefinition "ActivityDefinition") |  |
|   |  | Not Used | [Questionnaire](http://hl7.org/fhir/stu3/StructureDefinition/Questionnaire "Questionnaire") |  |
|  - - - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - - - code | 0..1 | Optional | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Detail type of activity<br/>Binding (example): Detailed description of the type of activity; e.g. What lab test, what procedure, what kind of encounter. [Care Plan Activity](http://hl7.org/fhir/stu3/valueset-care-plan-activity.html) |
|  - - - - coding | 0..* | Optional | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - - system | 0..1 | Optional | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - - code | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - - userSelected | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - - reasonCode | 0..* | Required | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Why activity should be done or why activity was prohibited<br/>Binding (example): Identifies why a care plan activity is needed. Can include any health condition codes as well as such concepts as "general wellness", prophylaxis, surgical preparation, etc. [Activity Reason](http://hl7.org/fhir/stu3/valueset-activity-reason.html)<br/><font color='red'><b>Mapping to Digital Maternity data item 'Reason for change of planned delivery setting'</b></font> |
|  - - - - coding | 0..* | Optional | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - - system | 0..1 | Optional | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - - code | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - - userSelected | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - - reasonReference | 0..* | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Condition triggering need for activity<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-Condition-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Condition-1 "CareConnect-Condition-1") |  |
|  - - - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - - - goal | 0..* | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Goals this activity relates to<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [Goal](http://hl7.org/fhir/stu3/StructureDefinition/Goal "Goal") |  |
|  - - - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - - - status | 1..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | not-started : scheduled : in-progress : on-hold : completed : cancelled : unknown<br/>Binding (required): Indicates where the activity is at in its overall life cycle. [CarePlanActivityStatus](http://hl7.org/fhir/stu3/valueset-care-plan-activity-status.html) |
|  - - - statusReason | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Reason for current status |
|  - - - prohibited | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | Do NOT do<br/>Default Value: false |
|  - - - scheduled[x] | 1..1 | Not Used | [Timing](http://hl7.org/fhir/stu3/datatypes.html#timing "Timing") | When activity is to occur |
|   |  | Mandatory | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") |  |
|   |  | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") |  |
|  - - - location | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Where it should happen<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") |  |
|  - - - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - - - performer | 0..* | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who will be responsible?<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|   |  | Optional | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|   |  | Optional | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") |  |
|   |  | Optional | [CareConnect-CareTeam-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-CareTeam-1 "CareConnect-CareTeam-1") |  |
|   |  | Optional | [CareConnect-RelatedPerson-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-RelatedPerson-1 "CareConnect-RelatedPerson-1") |  |
|  - - - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - - - product[x] | 0..1 | Optional | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | What is to be administered/supplied<br/>Binding (example): A product supplied or administered as part of a care plan activity. [SNOMED CT Medication Codes](http://hl7.org/fhir/stu3/valueset-medication-codes.html) |
|   |  | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") |  |
|   |  | Optional | [Substance](http://hl7.org/fhir/stu3/StructureDefinition/Substance "Substance") |  |
|   |  | Optional | [CareConnect-Medication-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Medication-1 "CareConnect-Medication-1") |  |
|  - - - dailyAmount | 0..1 | Optional | [Quantity (SimpleQuantity)](http://hl7.org/fhir/stu3/StructureDefinition/SimpleQuantity "Quantity (SimpleQuantity)") | How to consume/day?<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/>Constraint (sqty-1): The comparator is not used on a SimpleQuantity |
|  - - - - value | 0..1 | Optional | [Decimal](http://hl7.org/fhir/stu3/datatypes.html#decimal "Decimal") | Numerical value (with implicit precision) |
|  - - - - unit | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Unit representation |
|  - - - - system | 0..1 | Optional | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | System that defines coded unit form |
|  - - - - code | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Coded form of the unit |
|  - - - quantity | 0..1 | Optional | [Quantity (SimpleQuantity)](http://hl7.org/fhir/stu3/StructureDefinition/SimpleQuantity "Quantity (SimpleQuantity)") | How much to administer/supply/consume<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/>Constraint (sqty-1): The comparator is not used on a SimpleQuantity |
|  - - - - value | 0..1 | Optional | [Decimal](http://hl7.org/fhir/stu3/datatypes.html#decimal "Decimal") | Numerical value (with implicit precision) |
|  - - - - unit | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Unit representation |
|  - - - - system | 0..1 | Optional | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | System that defines coded unit form |
|  - - - - code | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Coded form of the unit |
|  - - - description | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Extra info describing activity to perform |
|  - note | 0..* | Required | [Annotation](http://hl7.org/fhir/stu3/datatypes.html#annotation "Annotation") | Comments about the plan<br><font color='red'><b>Mapping to Digital Maternity data item 'Concern, wishes or goal details'</b></font>  |
|  - - author[x] | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Individual responsible for the annotation<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") |  |
|   |  | Optional | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|   |  | Optional | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") |  |
|   |  | Optional | [CareConnect-RelatedPerson-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-RelatedPerson-1 "CareConnect-RelatedPerson-1") |  |
|  - - time | 1..1 | Mandatory | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the annotation was made <br><font color='red'><b>Mapping to Digital Maternity data item 'Date/time'</b></font>  |
|  - - text | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The annotation - text content |  


## Mapping for Person concerns Contract ##  

|>|Level 1|[Contract Resource](http://hl7.org/fhir/stu3/contract.html)|>|Level 2|[CareConnect-Contract-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Contract-1)|>|Level 3|None|  

|**[View Used FHIR Elements](explore_person_concerns.html#mapping-for-person-concerns-contract)**|**View All FHIR Elements**| 


|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| --- | --- | --- | --- | --- |
|  Contract | ​ |  |  | Legal Agreement<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource <br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-CarePlan-1' <br><b>The lastUpdated element maps to Digital Maternity data item = 'Advance Statement date'</b></font>  |
|  - implicitRules | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | A set of rules under which this content was created |
|  - language | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Language of the resource content<br/>Binding (extensible): A human language. [Common Languages](http://hl7.org/fhir/stu3/valueset-languages.html) |
|  - text | 0..1 | Required | [Narrative](http://hl7.org/fhir/stu3/narrative.html#Narrative "Narrative") | Text summary of the resource, for human interpretation<br><font color='red'><b>Mapping to Digital Maternity data item = 'Advance statement details'</b></font>  |
|  - contained | 0..* | Not Used | [Resource](http://hl7.org/fhir/stu3/resource.html "Resource") | Contained, inline Resources |
|  - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>Slicing: Description: Extensions are always sliced by (at least) url, Discriminator: url, Ordering: false, Rules: Open |
|  - identifier | 0..1 | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Contract number<br/><font color='red'>An identifier for this Person concerns Contract</font> |
|  - - use | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known. [IdentifierUse](http://hl7.org/fhir/stu3/valueset-identifier-use.html) |
|  - - type | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [Identifier Type Codes](http://hl7.org/fhir/stu3/valueset-identifier-type.html) |
|  - - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value <br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique <br/><font color='red'>A value for the identifier for this Person concerns Contract</font> |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - - assigner | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - status | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | amended : appended : cancelled : disputed : entered-in-error : executable : executed : negotiable : offered : policy : rejected : renewed : revoked : resolved : terminated<br/>Binding (required): A code specifying the state of the resource instance. [Contract Resource Status Codes](http://hl7.org/fhir/stu3/valueset-contract-status.html) |
|  - issued | 0..1 | Optional | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When this Contract was issued |
|  - applies | 0..1 | Optional | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Effective time<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - start | 0..1 | Optional | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - end | 0..1 | Optional | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - subject | 0..* | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Contract Target Entity<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [Resource](http://hl7.org/fhir/stu3/StructureDefinition/Resource "Resource") |  |
|  - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - topic | 0..* | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Context of the Contract<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [Resource](http://hl7.org/fhir/stu3/StructureDefinition/Resource "Resource") |  |
|  - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - authority | 0..* | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Authority under which this Contract has standing<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - domain | 0..* | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Domain in which this Contract applies<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") |  |
|  - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - type | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type or form<br/>Binding (example): List of overall contract codes. [Contract Type Codes](http://hl7.org/fhir/stu3/valueset-contract-type.html) |
|  - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - subType | 0..* | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Subtype within the context of type<br/>Binding (example): Detailed codes within the above. [Contract Subtype Codes](http://hl7.org/fhir/stu3/valueset-contract-subtype.html) |
|  - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - action | 0..* | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Action stipulated by this Contract<br/>Binding (example): Detailed codes for the contract action. [Contract Action Codes](http://hl7.org/fhir/stu3/valueset-contract-action.html) |
|  - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - actionReason | 0..* | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Rationale for the stiplulated action<br/>Binding (example): Detailed codes for the contract action reason. [PurposeOfUse](http://hl7.org/fhir/stu3/v3/PurposeOfUse/vs.html) |
|  - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - decisionType | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Decision by Grantor<br/>Binding (extensible): The type of decision made by a grantor with respect to an offer made by a grantee. [ActConsentDirective](http://hl7.org/fhir/stu3/v3/ActConsentDirective/vs.html) |
|  - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - contentDerivative | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Content derived from the basal information<br/>Binding (example): This is an example set of Content Derivative type codes, which represent the minimal content derived from the basal information source. [Contract Content Derivation Codes](http://hl7.org/fhir/stu3/valueset-contract-content-derivative.html) |
|  - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - securityLabel | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Security Labels that define affected resources<br/>Binding (extensible): Security Labels from the Healthcare Privacy and Security Classification System. [All Security Labels](http://hl7.org/fhir/stu3/valueset-security-labels.html) |
|  - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - agent | 0..* | Not Used | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Entity being ascribed responsibility |
|  - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - actor | 1..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Contract Agent Type<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [Device](http://hl7.org/fhir/stu3/StructureDefinition/Device "Device") |  |
|   |  | Not Used | [Group](http://hl7.org/fhir/stu3/StructureDefinition/Group "Group") |  |
|   |  | Not Used | [Substance](http://hl7.org/fhir/stu3/StructureDefinition/Substance "Substance") |  |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|   |  | Not Used | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|   |  | Not Used | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") |  |
|   |  | Not Used | [CareConnect-RelatedPerson-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-RelatedPerson-1 "CareConnect-RelatedPerson-1") |  |
|   |  | Not Used | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") |  |
|   |  | Not Used | [CareConnect-Contract-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Contract-1 "CareConnect-Contract-1") |  |
|  - - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - - role | 0..* | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Role type of the agent<br/>Binding (example): Detailed codes for the contract actor role. [Contract Actor Role Codes](http://hl7.org/fhir/stu3/valueset-contract-actorrole.html) |
|  - - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - signer | 0..* | Not Used | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Contract Signatory |
|  - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - type | 1..1 | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Contract Signatory Role<br/>Binding (preferred): List of parties who may be signing. [Contract Signer Type Codes](http://hl7.org/fhir/stu3/valueset-contract-signer-type.html) |
|  - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - party | 1..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Contract Signatory Party<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|   |  | Not Used | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|   |  | Not Used | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") |  |
|   |  | Not Used | [CareConnect-RelatedPerson-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-RelatedPerson-1 "CareConnect-RelatedPerson-1") |  |
|  - - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - - signature | 1..* | Not Used | [Signature](http://hl7.org/fhir/stu3/datatypes.html#signature "Signature") | Contract Documentation Signature |
|  - - - type | 1..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Indication of the reason the entity signed the object(s)<br/>Binding (preferred): An indication of the reason that an entity signed the object [Signature Type Codes](http://hl7.org/fhir/stu3/valueset-signature-type.html) |
|  - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - when | 1..1 | Not Used | [Instant](http://hl7.org/fhir/stu3/datatypes.html#instant "Instant") | When the signature was created |
|  - - - who[x] | 1..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Who signed |
|   |  | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") |  |
|   |  | Not Used | [Device](http://hl7.org/fhir/stu3/StructureDefinition/Device "Device") |  |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|   |  | Not Used | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|   |  | Not Used | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") |  |
|   |  | Not Used | [CareConnect-RelatedPerson-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-RelatedPerson-1 "CareConnect-RelatedPerson-1") |  |
|  - - - onBehalfOf[x] | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The party represented |
|   |  | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") |  |
|   |  | Not Used | [Device](http://hl7.org/fhir/stu3/StructureDefinition/Device "Device") |  |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|   |  | Not Used | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|   |  | Not Used | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") |  |
|   |  | Not Used | [CareConnect-RelatedPerson-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-RelatedPerson-1 "CareConnect-RelatedPerson-1") |  |
|  - - - contentType | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | The technical format of the signature<br/>Binding (required): The mime type of an attachment. Any valid mime type is allowed. [Mime Type](http://www.rfc-editor.org/bcp/bcp13.txt) |
|  - - - blob | 0..1 | Not Used | [base64Binary](http://hl7.org/fhir/stu3/datatypes.html#base64binary "base64Binary") | The actual signature content (XML DigSig. JWT, picture, etc.) |
|  - valuedItem | 0..* | Not Used | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Contract Valued Item List |
|  - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - entity[x] | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Contract Valued Item Type |
|   |  | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") |  |
|   |  | Not Used | [Resource](http://hl7.org/fhir/stu3/StructureDefinition/Resource "Resource") |  |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Contract Valued Item Number |
|  - - - use | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known. [IdentifierUse](http://hl7.org/fhir/stu3/valueset-identifier-use.html) |
|  - - - type | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [Identifier Type Codes](http://hl7.org/fhir/stu3/valueset-identifier-type.html) |
|  - - - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value |
|  - - - value | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - - - assigner | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - - effectiveTime | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Contract Valued Item Effective Tiem |
|  - - quantity | 0..1 | Not Used | [Quantity (SimpleQuantity)](http://hl7.org/fhir/stu3/StructureDefinition/SimpleQuantity "Quantity (SimpleQuantity)") | Count of Contract Valued Items<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/>Constraint (sqty-1): The comparator is not used on a SimpleQuantity |
|  - - - value | 0..1 | Not Used | [Decimal](http://hl7.org/fhir/stu3/datatypes.html#decimal "Decimal") | Numerical value (with implicit precision) |
|  - - - unit | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Unit representation |
|  - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | System that defines coded unit form |
|  - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Coded form of the unit |
|  - - unitPrice | 0..1 | Not Used | [Money](http://hl7.org/fhir/stu3/datatypes.html#money "Money") | Contract Valued Item fee, charge, or cost<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/>Constraint (mny-1): There SHALL be a code if there is a value and it SHALL be an expression of currency. If system is present, it SHALL be ISO 4217 (system = "urn:iso:std:iso:4217" - currency). |
|  - - - value | 0..1 | Not Used | [Decimal](http://hl7.org/fhir/stu3/datatypes.html#decimal "Decimal") | Numerical value (with implicit precision) |
|  - - - comparator | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | < : <= : >= : > - how to understand the value<br/>Binding (required): How the Quantity should be understood and represented. [QuantityComparator](http://hl7.org/fhir/stu3/valueset-quantity-comparator.html) |
|  - - - unit | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Unit representation |
|  - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | System that defines coded unit form |
|  - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Coded form of the unit |
|  - - factor | 0..1 | Not Used | [Decimal](http://hl7.org/fhir/stu3/datatypes.html#decimal "Decimal") | Contract Valued Item Price Scaling Factor |
|  - - points | 0..1 | Not Used | [Decimal](http://hl7.org/fhir/stu3/datatypes.html#decimal "Decimal") | Contract Valued Item Difficulty Scaling Factor |
|  - - net | 0..1 | Not Used | [Money](http://hl7.org/fhir/stu3/datatypes.html#money "Money") | Total Contract Valued Item Value<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/>Constraint (mny-1): There SHALL be a code if there is a value and it SHALL be an expression of currency. If system is present, it SHALL be ISO 4217 (system = "urn:iso:std:iso:4217" - currency). |
|  - - - value | 0..1 | Not Used | [Decimal](http://hl7.org/fhir/stu3/datatypes.html#decimal "Decimal") | Numerical value (with implicit precision) |
|  - - - comparator | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | < : <= : >= : > - how to understand the value<br/>Binding (required): How the Quantity should be understood and represented. [QuantityComparator](http://hl7.org/fhir/stu3/valueset-quantity-comparator.html) |
|  - - - unit | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Unit representation |
|  - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | System that defines coded unit form |
|  - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Coded form of the unit |
|  - term | 0..* | Not Used | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Contract Term List |
|  - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Contract Term Number |
|  - - - use | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known. [IdentifierUse](http://hl7.org/fhir/stu3/valueset-identifier-use.html) |
|  - - - type | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [Identifier Type Codes](http://hl7.org/fhir/stu3/valueset-identifier-type.html) |
|  - - - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value |
|  - - - value | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - - - assigner | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - - issued | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Contract Term Issue Date Time |
|  - - applies | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Contract Term Effective Time<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - - type | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Contract Term Type or Form<br/>Binding (example): Detailed codes for the types of contract provisions. [Contract Term Type Codes](http://hl7.org/fhir/stu3/valueset-contract-term-type.html) |
|  - - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - subType | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Contract Term Type specific classification<br/>Binding (example): Detailed codes for the subtypes of contract provisions. [Contract Term Subtype Codes](http://hl7.org/fhir/stu3/valueset-contract-term-subtype.html) |
|  - - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - topic | 0..* | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Context of the Contract term<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [Resource](http://hl7.org/fhir/stu3/StructureDefinition/Resource "Resource") |  |
|  - - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - - action | 0..* | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Contract Term Activity<br/>Binding (example): Detailed codes for the contract action. [Contract Action Codes](http://hl7.org/fhir/stu3/valueset-contract-action.html) |
|  - - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - actionReason | 0..* | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Purpose for the Contract Term Action<br/>Binding (example): Detailed codes for the contract action reason. [PurposeOfUse](http://hl7.org/fhir/stu3/v3/PurposeOfUse/vs.html) |
|  - - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - securityLabel | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Security Labels that define affected terms<br/>Binding (extensible): Security Labels from the Healthcare Privacy and Security Classification System. [All Security Labels](http://hl7.org/fhir/stu3/valueset-security-labels.html) |
|  - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - agent | 0..* | Not Used | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Contract Term Agent List |
|  - - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - - actor | 1..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Contract Term Agent Subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [Device](http://hl7.org/fhir/stu3/StructureDefinition/Device "Device") |  |
|   |  | Not Used | [Group](http://hl7.org/fhir/stu3/StructureDefinition/Group "Group") |  |
|   |  | Not Used | [Substance](http://hl7.org/fhir/stu3/StructureDefinition/Substance "Substance") |  |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|   |  | Not Used | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|   |  | Not Used | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") |  |
|   |  | Not Used | [CareConnect-RelatedPerson-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-RelatedPerson-1 "CareConnect-RelatedPerson-1") |  |
|   |  | Not Used | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") |  |
|   |  | Not Used | [CareConnect-Contract-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Contract-1 "CareConnect-Contract-1") |  |
|  - - - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - - - role | 0..* | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of the Contract Term Agent<br/>Binding (example): Detailed codes for the contract actor role. [Contract Actor Role Codes](http://hl7.org/fhir/stu3/valueset-contract-actorrole.html) |
|  - - - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Human readable Contract term text |
|  - - valuedItem | 0..* | Not Used | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Contract Term Valued Item List |
|  - - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - - entity[x] | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Contract Term Valued Item Type |
|   |  | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") |  |
|   |  | Not Used | [Resource](http://hl7.org/fhir/stu3/StructureDefinition/Resource "Resource") |  |
|  - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Contract Term Valued Item Number |
|  - - - - use | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known. [IdentifierUse](http://hl7.org/fhir/stu3/valueset-identifier-use.html) |
|  - - - - type | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [Identifier Type Codes](http://hl7.org/fhir/stu3/valueset-identifier-type.html) |
|  - - - - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value |
|  - - - - value | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - - - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - - - - assigner | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - - - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - - - effectiveTime | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Contract Term Valued Item Effective Tiem |
|  - - - quantity | 0..1 | Not Used | [Quantity (SimpleQuantity)](http://hl7.org/fhir/stu3/StructureDefinition/SimpleQuantity "Quantity (SimpleQuantity)") | Contract Term Valued Item Count<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/>Constraint (sqty-1): The comparator is not used on a SimpleQuantity |
|  - - - - value | 0..1 | Not Used | [Decimal](http://hl7.org/fhir/stu3/datatypes.html#decimal "Decimal") | Numerical value (with implicit precision) |
|  - - - - unit | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Unit representation |
|  - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | System that defines coded unit form |
|  - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Coded form of the unit |
|  - - - unitPrice | 0..1 | Not Used | [Money](http://hl7.org/fhir/stu3/datatypes.html#money "Money") | Contract Term Valued Item fee, charge, or cost<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/>Constraint (mny-1): There SHALL be a code if there is a value and it SHALL be an expression of currency. If system is present, it SHALL be ISO 4217 (system = "urn:iso:std:iso:4217" - currency). |
|  - - - - value | 0..1 | Not Used | [Decimal](http://hl7.org/fhir/stu3/datatypes.html#decimal "Decimal") | Numerical value (with implicit precision) |
|  - - - - comparator | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | < : <= : >= : > - how to understand the value<br/>Binding (required): How the Quantity should be understood and represented. [QuantityComparator](http://hl7.org/fhir/stu3/valueset-quantity-comparator.html) |
|  - - - - unit | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Unit representation |
|  - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | System that defines coded unit form |
|  - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Coded form of the unit |
|  - - - factor | 0..1 | Not Used | [Decimal](http://hl7.org/fhir/stu3/datatypes.html#decimal "Decimal") | Contract Term Valued Item Price Scaling Factor |
|  - - - points | 0..1 | Not Used | [Decimal](http://hl7.org/fhir/stu3/datatypes.html#decimal "Decimal") | Contract Term Valued Item Difficulty Scaling Factor |
|  - - - net | 0..1 | Not Used | [Money](http://hl7.org/fhir/stu3/datatypes.html#money "Money") | Total Contract Term Valued Item Value<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/>Constraint (mny-1): There SHALL be a code if there is a value and it SHALL be an expression of currency. If system is present, it SHALL be ISO 4217 (system = "urn:iso:std:iso:4217" - currency). |
|  - - - - value | 0..1 | Not Used | [Decimal](http://hl7.org/fhir/stu3/datatypes.html#decimal "Decimal") | Numerical value (with implicit precision) |
|  - - - - comparator | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | < : <= : >= : > - how to understand the value<br/>Binding (required): How the Quantity should be understood and represented. [QuantityComparator](http://hl7.org/fhir/stu3/valueset-quantity-comparator.html) |
|  - - - - unit | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Unit representation |
|  - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | System that defines coded unit form |
|  - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Coded form of the unit |
|  - - group | 0..* | Not Used | [see Contract.term](http://hl7.org/fhir/STU3/contract.html#Contract.term "see Contract.term") | Nested Contract Term Group |
|  - binding[x] | 0..1 | Not Used | [Attachment](http://hl7.org/fhir/stu3/datatypes.html#attachment "Attachment") | Binding Contract<br/>Constraint (att-1): It the Attachment has data, it SHALL have a contentType |
|   |  | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") |  |
|   |  | Not Used | [DocumentReference](http://hl7.org/fhir/stu3/StructureDefinition/DocumentReference "DocumentReference") |  |
|   |  | Not Used | [QuestionnaireResponse](http://hl7.org/fhir/stu3/StructureDefinition/QuestionnaireResponse "QuestionnaireResponse") |  |
|   |  | Not Used | [CareConnect-Composition-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Composition-1 "CareConnect-Composition-1") |  |
|  - friendly | 0..* | Not Used | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Contract Friendly Language |
|  - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - content[x] | 1..1 | Not Used | [Attachment](http://hl7.org/fhir/stu3/datatypes.html#attachment "Attachment") | Easily comprehended representation of this Contract<br/>Constraint (att-1): It the Attachment has data, it SHALL have a contentType |
|   |  | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") |  |
|   |  | Not Used | [DocumentReference](http://hl7.org/fhir/stu3/StructureDefinition/DocumentReference "DocumentReference") |  |
|   |  | Not Used | [QuestionnaireResponse](http://hl7.org/fhir/stu3/StructureDefinition/QuestionnaireResponse "QuestionnaireResponse") |  |
|   |  | Not Used | [CareConnect-Composition-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Composition-1 "CareConnect-Composition-1") |  |
|  - legal | 0..* | Not Used | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Contract Legal Language |
|  - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - content[x] | 1..1 | Not Used | [Attachment](http://hl7.org/fhir/stu3/datatypes.html#attachment "Attachment") | Contract Legal Text<br/>Constraint (att-1): It the Attachment has data, it SHALL have a contentType |
|   |  | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") |  |
|   |  | Not Used | [DocumentReference](http://hl7.org/fhir/stu3/StructureDefinition/DocumentReference "DocumentReference") |  |
|   |  | Not Used | [QuestionnaireResponse](http://hl7.org/fhir/stu3/StructureDefinition/QuestionnaireResponse "QuestionnaireResponse") |  |
|   |  | Not Used | [CareConnect-Composition-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Composition-1 "CareConnect-Composition-1") |  |
|  - rule | 0..* | Not Used | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Computable Contract Language |
|  - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - content[x] | 1..1 | Not Used | [Attachment](http://hl7.org/fhir/stu3/datatypes.html#attachment "Attachment") | Computable Contract Rules<br/>Constraint (att-1): It the Attachment has data, it SHALL have a contentType |
|   |  | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") |  |
|   |  | Not Used | [DocumentReference](http://hl7.org/fhir/stu3/StructureDefinition/DocumentReference "DocumentReference") |  |


## Mapping for Person concerns Location ##  

The Person concerns List has reference(s) to the Location resource. This means that any exchange of the plan and requested actions details heading data must also include the [Location Details](explore_location.html#mapping-for-location)

## Person concerns example ##
<script src="https://gist.github.com/IOPS-DEV/c835755b9f7c98dd79063e48e17e1441.js"></script>