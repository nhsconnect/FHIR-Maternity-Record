---
title: Vaccinations List
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_vaccinations_all.html
summary: "The FHIR profiles used for the Vaccinations List"
---

## Heading Description ##
The details of a women’s vaccinations.

## Vaccinations Details Structure ##

{% include custom/vaccinations.svg %}

## Maternity Data Standards Mapping to FHIR profiles ##

## Mapping Overview ##

|**Data Standard Element**|**FHIR Profile**|**FHIR target**|
|Date and Time of vaccinations|[Encounter](explore_vaccinations_details.html#mapping-for-vaccinations-details-encounter)|period.start|
|ODS/ORD Site Code|[Location](explore_vaccinations_details.html#mapping-for-vaccinations-details-location)|identifier|
|Performing Professional|[Practitioner](explore_vaccinations_details.html#mapping-for-vaccinations-details-practitioner)|identifier and name|
|SDS Job Role Name| [PractitionerRole](explore_vaccinations.html#mapping-for-vaccination-practitioner-role)|code|
|Reported Date|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|date|
|Primary Source|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|primarySource|
|Report Origin|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|reportOrigin|
|Vaccination Procedure|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|extension.vaccinationProcedure|
|Vaccination Situation (Not Given Outcome)|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|explanation.reasonNotGiven|
|Not Given flag|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|notGiven|
|Dose sequence|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|vaccinationProtocol.doseSequence|
|Vaccine Product|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|vaccineCode.coding.code|
|Vaccine Manufacturer|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|manufacturer|
|Batch Number|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|lotNumber|
|Site of Vaccination|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|site|
|Route of Vaccination|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|route|
|Dose Amount|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|doseQuantity|
|Indication|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|reason|


## Mapping for Vaccination Details List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2| None|>|Level 3|[CareConnect-List-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|


|**[View Used FHIR Elements](explore_vaccinations.html#mapping-for-vaccination-details-list)**|**View All FHIR Elements**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  List | ​ |  |  | Information summarized from a list of other resources<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (lst-2): The deleted flag can only be used if the mode of the list is "changes"<br/>Constraint (lst-1): A list can only have an emptyReason if it is empty |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1'</font> |
|  - implicitRules | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | A set of rules under which this content was created |
|  - language | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Language of the resource content<br/>Binding (extensible): A human language. [Common Languages](http://hl7.org/fhir/stu3/valueset-languages.html) |
|  - text | 0..1 | Not Used | [Narrative](http://hl7.org/fhir/stu3/narrative.html#Narrative "Narrative") | Text summary of the resource, for human interpretation |
|  - contained | 0..* | Not Used | [Resource](http://hl7.org/fhir/stu3/resource.html "Resource") | Contained, inline Resources |
|  - extension (clinicalSetting) | 0..1 | Not Used | [Extension-CareConnect-ClinicalSetting-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-ClinicalSetting-1 "Extension-CareConnect-ClinicalSetting-1") | **To record the clinical setting of a problem list<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>** |
|  - extension (warningCode) | 0..1 | Not Used | [Extension-CareConnect-ListWarningCode-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-ListWarningCode-1 "Extension-CareConnect-ListWarningCode-1") | **To capture warnings that the list may be incomplete<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>** |
|  - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>Slicing: Description: Extensions are always sliced by (at least) url, Discriminator: url, Ordering: false, Rules: Open |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business identifier<br/><font color='red'>An identifier for this vaccination details list</font><br/> |
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
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique<br/>Business identifier<br/><font color='red'>An identifier for this vaccination details list</font> |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | <font color='red'>A identifier'</font> |
|  - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - - assigner | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource<br/><font color='red'>The organization that allocated the identifier</font> |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | current : retired : entered-in-error<br/>Binding (required): The current state of the list [ListStatus](http://hl7.org/fhir/stu3/valueset-list-status.html)<br/><font color='red'>The status of the list MUST contain the value 'current'</font> |
|  - mode | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | working : snapshot : changes<br/>Binding (required): The processing mode that applies to this list [ListMode](http://hl7.org/fhir/stu3/valueset-list-mode.html)<br/><font color='red'>The mode of the list MUST contain the value 'snapshot'</font> |
|  - title | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Descriptive name for the list<br/><font color='red'>This MUST contain the value 'Admission details'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading Immunisation details'</b></font>  |
|  - code | 0..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | What the purpose of this list is<br/>Binding (preferred): What the purpose of a list is [CareConnect-ListCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListCode-1)<br/><font color='red'>The PRSB heading for this list. Note: for Maternity the value stated below is used which is not from the preferred value set </font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/><font color='red'>The SNOMED CT concept for the PRSB heading type</font> |
|  - - - system | 0..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant<br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font>  |
|  - - - code | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value '1102181000000102'</font> |
|  - - - display | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>This MUST contain the value 'Immunisations'</font><br/><font color='red'>Mapping to Maternity data item = 'PSRB Heading Immunisation details'</font>  |
|  - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Not Used | [Group](http://hl7.org/fhir/STU3/group.html "Group") |  |
|   |  | Not Used | [Device](http://hl7.org/fhir/stu3/StructureDefinition/Device "Device") |  |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color='red'>This is the subject of the vaccination details List.<br/>This MUST use the CareConnect patient profile. </font>See[patient resource reference](explore_admission_details.html#patient-reference) for information on how to populate the resource. |
|   |  | Not Used | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") |  |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - encounter | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Context in which list created<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>A reference to the encounter resource within the Admission details list. </font/> <br/> |
|   |  | Not Used | [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1 "CareConnect-Encounter-1") | This is the context of the Admission details List.<br/>This MUST use the CareConnect encounter profile. See [encounter resource](explore_admission_details.html#mapping-for-admission-details-encounter) for information on how to populate the resource. |
|  - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - date | 0..1 | Mandatory | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the list was prepared<br/><font color='red'> This MUST contain a system date to indicate when the list was created or updated</font> |
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
|  - - item | 1..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>A reference to an Encounter resource included in the list<br/>This MUST use the CareConnect Encounter profile. </font>See [Encounter resource](explore_vaccinations_details.html#mapping-for-vaccination-details-encounter) for information on how to populate the resource. |
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

## Patient Reference ##

The vaccination details list has a mandated subject reference to the Patient resource. This means that any exchange of the vaccination details heading data must also include the [Patient demographics List.](explore_patient_demographics.html)

## Mapping for Vaccinations ##

|>|Level 1|[Immunization Resource](http://hl7.org/fhir/stu3/immunization.html)|>|Level 2| None|>|Level 3|[CareConnect-Immunization-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Immunization-1)|


|**[View Used FHIR Elements](explore_vaccinations_all.html#mapping-for-immunization)**|**View All FHIR Elements**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | --- |
|  Immunization | ​ |  |  | Immunization event information<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (imm-2): If immunization was administered (notGiven=false) then explanation.reasonNotGiven SHALL be absent.<br/>Constraint (imm-1): If immunization was not administered (notGiven=true) then there SHALL be no reaction nor explanation.reason present |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | Meta | Metadata about the resource |
|  - - profile | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Profiles this resource claims to conform to<br/><font color="red">The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-AllergyIntolerance-1'</font> |
|  - implicitRules | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | A set of rules under which this content was created |
|  - language | 0..1 | Not Used | Code | Language of the resource content<br/>Binding (extensible): A human language. [Common Languages](http://hl7.org/fhir/stu3/valueset-languages.html) |
|  - text | 0..1 | Not Used | Narrative | Text summary of the resource, for human interpretation |
|  - contained | 0..* | Not Used | Resource | Contained, inline Resources |
|  - extension (parentPresent) | 0..1 | Not Used | [Extension-CareConnect-ParentPresent-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-ParentPresent-1 "Extension-CareConnect-ParentPresent-1") | Was a parent present at the Immunization<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - extension (recordedDate) | 0..1 | Not Used | [Extension-CareConnect-DateRecorded-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-DateRecorded-1 "Extension-CareConnect-DateRecorded-1") | The date that the Vaccination was recorded<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - extension (vaccinationProcedure) | 0..1 | Required | [Extension-CareConnect-VaccinationProcedure-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-VaccinationProcedure-1 "Extension-CareConnect-VaccinationProcedure-1") | An extension to hold an immunization procedure code<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/><font color="red">Only use SNOMED CT coding or free text where no SNOMED CT code is available.</font><br/> |
|  - modifierExtension | 0..* | Not Used | Extension | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>Slicing: Description: Extensions are always sliced by (at least) url, Discriminator: url, Ordering: false, Rules: Open |
|  - identifier | 0..* | Required | Identifier | Business identifier |
|  - - use | 0..1 | Not Used | Code | usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known. [IdentifierUse](http://hl7.org/fhir/stu3/valueset-identifier-use.html) |
|  - - type | 0..1 | Not Used | CodeableConcept | Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [Identifier Type Codes](http://hl7.org/fhir/stu3/valueset-identifier-type.html) |
|  - - - coding | 0..* | Not Used | Coding | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | Uri | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | Code | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | String | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | String | Plain text representation of the concept |
|  - - system | 1..1 | Mandatory | Uri | The namespace for the identifier value |
|  - - value | 1..1 | Mandatory | String | The value that is unique |
|  - - period | 0..1 | Not Used | Period | Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | dateTime | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | dateTime | End time with inclusive boundary, if not ongoing |
|  - - assigner | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  |  | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - - reference | 0..1 | Not Used | String | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Required | String | Text alternative for the resource |
|  - status | 1..1 | Mandatory | Code | Completed<br/>Binding (required): A set of codes indicating the current status of an Immunization [Immunization Status Codes](http://hl7.org/fhir/stu3/valueset-immunization-status.html)<br/><font color='red'>The status of the list MUST contain the value 'Completed'</font> |
|  - notGiven | 1..1 | Mandatory | Boolean | Flag for whether immunization was given<br/><font color="red">true = not given</font><br/><font color="red">false = given</font> |
|  - vaccineCode | 1..1 | Optional | CodeableConcept | Vaccine product administered<br/>Binding (extensible): The code for vaccine product administered [CareConnect-VaccineCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-VaccineCode-1) |
|  - - coding | 0..* | Optional | Coding | Code defined by a terminology system |
|  - - - system | 0..1 | Optional | Uri | Identity of the terminology system |
|  - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - code | 0..1 | Optional | Code | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Optional | String | Representation defined by the system |
|  - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - text | 0..1 | Optional | String | Plain text representation of the concept |
|  - patient | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who was immunized<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  |  | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color='red'>This is the subject of the Immunisation details List.<br/>This MUST use the CareConnect patient profile. </font>See[patient resource reference](explore_admission_details.html#patient-reference) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL<br/><br/><font color='red'>This must use the CareConnect Patient profile.</font>See [patient resource reference](explore_allergies_and_adverse_reactions.html#patient-reference) for information on how to populate the resource |
|  - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - encounter | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Encounter administered as part of<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the vaccination encounter.</font> |
|   |  |  | [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1 "CareConnect-Encounter-1") | This is the context of the vaccination details List.<br/>This MUST use the CareConnect encounter profile. See [encounter resource](explore_admission_details.html#mapping-for-admission-details-encounter) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the encounter resource included in the vaccination list within the FHIR Bundle.</font>  |
|  - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - date | 0..1 | Mandatory | dateTime | Vaccination administration date<br/><font color="red">The date/time on which the immunisation intervention was carried out or was meant to be administered</font> |
|  - primarySource | 1..1 | Mandatory | Boolean | Indicates context the data was recorded in<br/>Default Value: true<br/><font color="red">false if reported</font> |
|  - reportOrigin | 0..1 | Required | CodeableConcept | Indicates the source of a secondarily reported record<br/>Binding (example): The source of the data for a record which is not from a primary source. [Immunization Origin Codes](http://hl7.org/fhir/stu3/valueset-immunization-origin.html) |
|  - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system |
|  - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system |
|  - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Mandatory | String | Representation defined by the system |
|  - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - text | 0..1 | Not Used | String | Plain text representation of the concept |
|  - location | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Where vaccination occurred<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  |  | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") | <font color='red'>This is the location where the vaccination took place. This MUST use the CareConnect location profile.</font> |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - manufacturer | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Vaccine manufacturer<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  |  | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - lotNumber | 0..1 | Optional | String | Vaccine lot number<br/><font color="red">The batch number of the vaccine product</font> |
|  - expirationDate | 0..1 | Not Used | Date | Vaccine expiration date |
|  - site | 0..1 | Optional | CodeableConcept | Body site vaccine was administered<br/>Binding (examle): The site at which the vaccine was administered [Codes for Immunization Site of Administration](http://hl7.org/fhir/stu3/valueset-immunization-site.html)<br/><font color="red">The immunization site does not use the preferred value set but uses SNOMED CT concepts instead Mapping to Maternity data item = 'site'.<br/><br/> |
|  - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Optional | Coding | Code defined by a terminology system<br/><font color="red">The immunization site does not use the preferred value set but uses SNOMED CT concepts instead Mapping to Maternity data item = 'site'. |
|  - - - extension (snomedCTDescriptionID) | 0..1 | Optional | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | The SNOMED CT Description ID for the display<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - system | 1..1 | Mandatory | Uri | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - code | 1..1 | Mandatory | Code | Symbol in syntax defined by the system<br/><font color="r3ed">A SNOMED CT code</font> |
|  - - - display | 1..1 | Mandatory | String | Representation defined by the system<br/><font color="red">The display associated with the SNOMED CT concept. This SHOULD be the preferred term</font> |
|  - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - text | 0..1 | Optional | String | Plain text representation of the concept<br/>This element SHOULD only be populated when the Immunisation cannot be coded or when stating one of the following statements: 'No known site' Or 'Information not available'. |
|  - route | 0..1 | Optional | CodeableConcept | How vaccine entered body<br/>Binding (example): The route by which the vaccine was administered [Immunization Route Codes](http://hl7.org/fhir/stu3/valueset-immunization-route.html)<br/><font color="red">Note the example valueSet is not used for Maternity and the following should be used instead<br/>Coded text - SNOMED CT (<284009009  |Route of administration value (qualifier value))</font> |
|  - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Optional | Coding | Code defined by a terminology system<br/>Binding (example): A code from the SNOMED Clinical Terminology UK coding system that describes the e-Prescribing route of administration. [CareConnect-MedicationDosageRoute-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-MedicationDosageRoute-1)<br/><font color="red">Note the example valueSet is not used for Maternity and the following should be used instead<br/>Coded text - SNOMED CT (<284009009  |Route of administration value (qualifier value))</font> |
|  - - - extension (snomedCTDescriptionID) | 0..1 | Optional | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | The SNOMED CT Description ID for the display<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - system | 1..1 | Mandatory | Uri | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - code | 1..1 | Mandatory | Code | Symbol in syntax defined by the system<br/><font color="red">Coded text - SNOMED CT (<284009009  |Route of administration value (qualifier value))</font> |
|  - - - display | 1..1 | Mandatory | String | Representation defined by the system<br/><font color="red">This SHOULD be the preferred term for the SNOMED concept</font> |
|  - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - text | 0..1 | Optional | String | Plain text representation of the concept<br/><font color="red">This element SHOULD only be populated when the Immunisation cannot be coded or when stating one of the following statements: 'No known route' Or 'Information not available'.</font> |
|  - doseQuantity | 0..1 | Optional | [Quantity (SimpleQuantity )](http://hl7.org/fhir/stu3/StructureDefinition/SimpleQuantity "Quantity (SimpleQuantity )") | Amount of vaccine administered<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/>Constraint (sqty-1): The comparator is not used on a SimpleQuantity<br/><font color="red">Amount of vaccine administered</font> |
|  - - value | 0..1 | Required | Decimal | Numerical value (with implicit precision) |
|  - - unit | 0..1 | Required | String | Unit representation |
|  - - system | 0..1 | Required | Uri | System that defines coded unit form |
|  - - code | 0..1 | Required | Code | Coded form of the unit |
|  - practitioner | 0..* | Mandatory | BackboneElement | Who performed event |
|  - - modifierExtension | 0..* | Not Used | Extension | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - role | 0..1 | Mandatory | CodeableConcept | What type of performance was done<br/>Binding (extensible): The role a practitioner plays in the immunization event [Immunization Role Codes](http://hl7.org/fhir/stu3/valueset-immunization-role.html) |
|  - - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system |
|  - - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Mandatory | String | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Optional | String | Plain text representation of the concept |
|  - - actor | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Individual who was performing<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color="red">This MUST be a reference to the Practitioner resource</font> |
|   |  | Required | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") | <font color='red'>The responsible clinician for the encounter.<br/>This MUST use the CareConnect Practitioner profile. </font>See [Practitioner resource](explore_vaccination_details.html#mapping-for-vaccination-details-encounter) for information on how to populate the resource. |
|  - - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL<br/>A reference to the Practitioner resource included in the Immunisation details list |
|  - - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - note | 0..* | Optional | Annotation | Vaccination notes |
|  - - author[x] | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Individual responsible for the annotation<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  |  | [RelatedPerson](http://hl7.org/fhir/stu3/StructureDefinition/RelatedPerson "RelatedPerson") |  |
|   |  |  | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") |  |
|   |  |  | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|   |  |  | String |  |
|  - - time | 0..1 | Not Used | dateTime | When the annotation was made |
|  - - text | 1..1 | Not Used | String | The annotation - text content |
|  - explanation | 0..1 | Optional | BackboneElement | Administration/non-administration reasons<br/><font color="red">The clinical indication or reason for administering or recording an historical vaccination. </font> |
|  - - modifierExtension | 0..* | Not Used | Extension | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - reason | 0..* | Optional | CodeableConcept | Why immunization occurred<br/>Binding (example): The reason why a vaccine was administered [CareConnect-ImmunizationExplanationReason-2 ](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ImmunizationExplanationReason-2) |
|  - - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system |
|  - - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system<br/><font color="red">This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Mandatory | String | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | String | Plain text representation of the concept |
|  - - reasonNotGiven | 0..1 | Required | CodeableConcept | Why immunization did not occur<br/>Binding (example): The reason why a vaccine was not administered [Immunization Reasons for Not Immunizing Codes](http://hl7.org/fhir/stu3/valueset-no-immunization-reason.html)<br/><font color="red">Where a vaccine is not administered a PROCEDURE WITH EXPLICIT CONTEXT (SNOMED CT). Codes TBA |
|  - - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system |
|  - - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Mandatory | String | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Optional | String | Plain text representation of the concept |
|  - reaction | 0..* | Not Used | BackboneElement | Details of a reaction that follows immunization |
|  - - modifierExtension | 0..* | Not Used | Extension | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - date | 0..1 | Not Used | dateTime | When reaction started |
|  - - detail | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Additional information on reaction<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  |  | [CareConnect-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1 "CareConnect-Observation-1") |  |
|  - - - reference | 0..1 | Not Used | String | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - - reported | 0..1 | Not Used | Boolean | Indicates self-reported reaction |
|  - vaccinationProtocol | 0..* | Mandatory | BackboneElement | What protocol was followed |
|  - - modifierExtension | 0..* | Not Used | Extension | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - doseSequence | 1..1 | Required | positiveInt | Dose number within series<br/><font color="red">Nominal position in a series of vaccines</font> |
|  - - description | 0..1 | Not Used | String | Details of vaccine protocol |
|  - - authority | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who is responsible for protocol<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  |  | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - - reference | 0..1 | Not Used | String | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - - series | 0..1 | Not Used | String | Name of vaccine series |
|  - - seriesDoses | 0..1 | Not Used | positiveInt | Recommended number of doses for immunity |
|  - - targetDisease | 1..* | Not Used | CodeableConcept | Disease immunized against<br/>Binding (example): The disease target of the vaccination protocol [Vaccination Protocol Dose Target Codes](http://hl7.org/fhir/stu3/valueset-vaccination-protocol-dose-target.html) |
|  - - - coding | 0..* | Not Used | Coding | Code defined by a terminology system<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open |
|  - - - coding (snomedCT) | 0..1 | Not Used | Coding | Code defined by a terminology system |
|  - - - - extension (snomedCTDescriptionID) | 0..1 | Not Used | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | The SNOMED CT Description ID for the display<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - - system | 1..1 | Not Used | Uri | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - - code | 1..1 | Not Used | Code | Symbol in syntax defined by the system |
|  - - - - display | 1..1 | Not Used | String | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | String | Plain text representation of the concept |
|  - - doseStatus | 1..1 | Not Used | CodeableConcept | Indicates if dose counts towards immunity<br/>Binding (example): The status of the vaccination protocol (i.e. should this count) [Vaccination Protocol Dose Status codes](http://hl7.org/fhir/stu3/valueset-vaccination-protocol-dose-status.html) |
|  - - - coding | 0..* | Not Used | Coding | Code defined by a terminology system |
|  - - - - system | 1..1 | Not Used | Uri | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - - code | 1..1 | Not Used | Code | Symbol in syntax defined by the system |
|  - - - - display | 1..1 | Not Used | String | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | String | Plain text representation of the concept |
|  - - doseStatusReason | 0..1 | Not Used | CodeableConcept | Why dose does (not) count<br/>Binding (example): The reason for the determining if a vaccination should count or why vaccination should not count. [Vaccination Protocol Dose Status Reason codes](http://hl7.org/fhir/stu3/valueset-vaccination-protocol-dose-status-reason.html) |
|  - - - coding | 0..* | Not Used | Coding | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | Uri | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | Code | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | String | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | String | Plain text representation of the concept |


## Mapping for Vaccination Encounter ##

|>|Level 1|[Encounter Resource](http://hl7.org/fhir/stu3/encounter.html)|>|Level 2|[CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)|>|Level 3|None|


|**[View Used FHIR Elements*](explore_vaccinations.html#mapping-for-vaccination-encounter)**|**View All FHIR Elements**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  Encounter | ​ |  |  | An interaction during which services are provided to the patient<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1'</font> |
|  - implicitRules | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | A set of rules under which this content was created |
|  - language | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Language of the resource content<br/>Binding (extensible): A human language. [Common Languages](http://hl7.org/fhir/stu3/valueset-languages.html) |
|  - text | 0..1 | Not Used | [Narrative](http://hl7.org/fhir/stu3/narrative.html#Narrative "Narrative") | Text summary of the resource, for human interpretation |
|  - contained | 0..* | Not Used | [Resource](http://hl7.org/fhir/stu3/resource.html "Resource") | Contained, inline Resources |
|  - extension (encounterTransport) | 0..1 | Not Used | [Extension-CareConnect-EncounterTransport-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-EncounterTransport-1 "Extension-CareConnect-EncounterTransport-1") | Encounter transport<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - extension (outcomeOfAttendance) | 0..1 | Not Used | [Extension-CareConnect-OutcomeOfAttendance-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-OutcomeOfAttendance-1 "Extension-CareConnect-OutcomeOfAttendance-1") | An extension to the Encounter resource to record the outcome of an Out-Patient attendance.<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
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
|  - - value | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique<br/><font color='red'>An identifier for this Vaccination encounter</font> |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - - assigner | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | planned : arrived : triaged : in-progress : onleave : finished : cancelled +<br/>Binding (required): Current state of the encounter [EncounterStatus](http://hl7.org/fhir/stu3/valueset-encounter-status.html)<br/><font color='red'>The status of the Encounter MUST contain the value 'finished'</font> |
|  - statusHistory | 0..* | Not Used | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | List of past encounter statuses |
|  - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - status | 1..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | planned : arrived : triaged : in-progress : onleave : finished : cancelled +<br/>Binding (required): Current state of the encounter [EncounterStatus](http://hl7.org/fhir/stu3/valueset-encounter-status.html) |
|  - - period | 1..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | The time that the episode was in the specified status<br/>Constraint (per-1): If present, start SHALL have a lower value than end<br/><font color='red'><b>Mapping to Maternity data item ='Date/Time'</b></font>  |
|  - - - start | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - end | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - class | 0..1 | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Classification of the encounter<br/>Binding (extensible): Classification of the encounter [ActEncounterCode](http://hl7.org/fhir/stu3/v3/ActEncounterCode/vs.html) |
|  - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - classHistory | 0..* | Not Used | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | List of past encounter classes |
|  - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - class | 1..1 | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Classification of the encounter<br/>Binding (extensible): Classification of the encounter [ActEncounterCode](http://hl7.org/fhir/stu3/v3/ActEncounterCode/vs.html) |
|  - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - period | 1..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | The time that the episode was in the specified class<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - type | 0..* | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Specific type of encounter<br/>Binding (example): The type of encounter [EncounterType](http://hl7.org/fhir/stu3/valueset-encounter-type.html)<br/> |
|  - - coding | 0..1 | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system that describes an encounter between a care professional and the patient (or patient's record). [CareConnect-EncounterType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-EncounterType-1) |
|  - - - extension (snomedCTDescriptionID) | 0..1 | Not Used | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | The SNOMED CT Description ID for the display<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - system | 1..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/> |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - code | 1..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 1..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
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
|  - subject | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | The patient ro group present at the encounter<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
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
|  - participant | 0..* | Not Used | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | List of participants involved in the encounter |
|  - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - type | 0..2 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Role of participant in encounter<br/>Binding (extensible): Role of participant in encounter [ParticipantType](http://hl7.org/fhir/stu3/valueset-encounter-participant-type.html)<br/><font color='red'>There will be up to two instances of this element, the first carries a reference to the responsible clinical using the Practitioner resource and the second a reference to the person accompanying the patient using the relatedPerson resource</font> |
|  - - - coding | 1..1 | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/><font color='red'>There will be one instance of the coding for each instance of type</font> |
|  - - - - system | 1..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://hl7.org/fhir/ValueSet/encounter-participant-type'</font> |
|  - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - code | 1..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>The Responsible Clinician will use a code of 'CON'</font><br/><font color='red'>The Person accompanying patient will use a code of 'ESC'</font>  |
|  - - - - display | 1..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | <font color='red'>The Responsible Clinician will use a display of 'consultant'</font><br/><font color='red'>The Person accompanying patient will use a code of 'escort'</font>  |
|  - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Period of time during the encounter that the participant participated<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - - individual | 1..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Persons involved in the encounter other than the patient<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This MUST be a reference to either the Practitioner or RelatedPerson resource</font> |
|   |  | Not Used | [RelatedPerson](http://hl7.org/fhir/stu3/StructureDefinition/RelatedPerson "RelatedPerson") | <font color='red'>The person accompanying the patient.<br/>This MUST use the RelatedPerson resource. </font>See [RelatedPerson resource](explore_admission_details.html#mapping-for-admission-details-relatedperson) for information on how to populate the resource. |
|   |  | Not Used | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") | <font color='red'>The responsible clinician for the encounter.<br/>This MUST use the CareConnect Practitioner profile. </font>See [Practitioner resource](explore_admission_details.html#mapping-for-admission-details-encounter) for information on how to populate the resource. |
|  - - - reference | 1..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the RelatedPerson resource or the Practitioner resource included in the Assessment scales list</font>  |
|  - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - appointment | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | The appointment that scheduled this encounter<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [Appointment](http://hl7.org/fhir/stu3/StructureDefinition/Appointment "Appointment") |  |
|  - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | The start and end time of the encounter<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary<br/><font color='red'>The date and time of admission</font><br/><font color='red'><b>Mapping to Maternity data item = 'Date and Time of admission'.</b></font> |
|  - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - length | 0..1 | Not Used | [Duration](http://hl7.org/fhir/stu3/datatypes.html#duration "Duration") | Quantity of time the encounter lasted (less time absent)<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/>Constraint (drt-1): There SHALL be a code if there is a value and it SHALL be an expression of time. If system is present, it SHALL be UCUM. |
|  - - value | 0..1 | Not Used | [Decimal](http://hl7.org/fhir/stu3/datatypes.html#decimal "Decimal") | Numerical value (with implicit precision) |
|  - - comparator | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | < : <= : >= : > - how to understand the value<br/>Binding (required): How the Quantity should be understood and represented. [QuantityComparator](http://hl7.org/fhir/stu3/valueset-quantity-comparator.html) |
|  - - unit | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Unit representation |
|  - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | System that defines coded unit form |
|  - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Coded form of the unit |
|  - reason | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Reason the encounter takes place (code)<br/>Binding (preferred): Reason why the encounter takes place. [Encounter Reason Codes](http://hl7.org/fhir/stu3/valueset-encounter-reason.html)<br/><font color='red'>The Assessment scales encounter does not use the preferred value set but uses SNOMED CT concepts instead</font> |
|  - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/><font color='red'>A concept from the Care planning health issues simple reference set</font><br/>[See here for further information](https://termbrowser.nhs.uk/?perspective=full&conceptId1=999000131000000105&edition=uk-edition&server=https://termbrowser.dataproducts.nhs.uk/sct-browser-api/snomed&langRefset=999001261000000100,999000691000001104)<br/><font color='red'>Note this reference set MAY be extnded as required by the sending system</font> |
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
|  - - role | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Role that this diagnosis has within the encounter (e.g. admission, billing, discharge …)<br/>Binding (preferred): The type of diagnosis this condition represents [DiagnosisRole](http://hl7.org/fhir/stu3/valueset-diagnosis-role.html) |
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
|  - hospitalization | 0..1 | Not Used | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Details about the admission to a healthcare service |
|  - - extension (admissionMethod) | 0..1 | Not Used | [Extension-CareConnect-AdmissionMethod-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-AdmissionMethod-1 "Extension-CareConnect-AdmissionMethod-1") | An extension to the Encounter resource to record how a Patient was admitted to hospital.<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/><font color='red'>An extension to the Encounter  resource</font><br/>See [Admission method extension](explore_admission_details.html#mapping-for-admission-details-admission-method-extension) for information on how to populate this extension to the resource.<br/><font color='red'><b>Mapping to Maternity data item = 'Reason for Admission'.</b></font>  |
|  - - extension (dischargeMethod) | 0..1 | Not Used | [Extension-CareConnect-DischargeMethod-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-DischargeMethod-1 "Extension-CareConnect-DischargeMethod-1") | An extension to the Encounter resource to record the method of discharge from hospital.<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - preAdmissionIdentifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Pre-admission identifier |
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
|  - - origin | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | The location from which the patient came before admission<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") |  |
|  - - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - - admitSource | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | From where patient was admitted (physician referral, transfer)<br/>Binding (preferred): The source of admission to a Hospital Provider Spell or a Nursing Episode when the Patient is in a Hospital Site or a Care Home. [CareConnect-SourceOfAdmission-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-SourceOfAdmission-1)<br/><font color='red'><b>Maternity Data set mapping = 'Source of Admission'</b></font> |
|  - - - coding | 0..1 | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - system | 1..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - code | 1..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value 'https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-SourceOfAdmission-1'</font> |
|  - - - - display | 1..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>This MUST contain a code from the stated ValueSet</font>  |
|  - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept<br/> |
|  - - reAdmission | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | The type of hospital re-admission that has occurred (if any). If the value is absent, then this is not identified as a readmission<br/>Binding (example): The reason for re-admission of this hospitalization encounter. [v2 Re-Admission Indicator](http://hl7.org/fhir/ValueSet/v2-0092) |
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
|  - - location | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Location the encounter takes place<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>The site code of the location where teh vaccination was administered.</font> |
|   |  | Mandatory | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") | "<font color='red'>The location<br/>This MUST use the CareConnect Location profile. </font>See [Location resource](explore_assessment_scales.html#mapping-for-assessment-scales-location) for information on how to populate the resource." |
|  - - - reference | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the Location resource included in the Vaccination list</font>  |
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

## Mapping for Vaccination Practitioner ##

The vaccination details has reference(s) to the Practitioner resource. This means that any exchange of the vaccination details heading data must also include the [[Practitioner Details](explore_practitioner.html#mapping-for-practitioner)

## Mapping for Vaccination Practitioner Role ##

The vaccination details has reference(s) to the Practitioner Role resource. This means that any exchange of the vaccination details heading data must also include the [[Practitioner Role Details](explore_practitioner_role.html#mapping-for-practitioner_role)

## Mapping for Vaccination Location ##

The vaccination details has reference(s) to the Location resource. This means that any exchange of the vaccination details heading data must also include the [[Location Details](explore_location.html#mapping-for-location)

## Vaccination Details Heading Example ##