---
title: Baby Details (person) List
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_baby_details.html
summary: "The FHIR profiles used for the Baby details (person) List"
---
{% include custom/under.construction.html content="Please check back later for any updates to this page" %}

## Heading Description ##
Birth details of the baby.

The following FHIR profiles are used to form the Baby Details (person) details list structure:

- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)
- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)
- [CareConnect-Observation](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)
- [CareConnect-ProcedureRequest-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-ProcedureRequest-1)

The following profiles are referenced from the Baby Details (person) details list structure:

- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)

## Baby Details (Person) Structure ##

{% include custom/baby_details_person.svg %}

## Maternity Data Standards Mapping to FHIR profiles ##

## Mapping Overview ##

|  **Data Standard Element** | **FHIR Profile Mapping** | **FHIR Element** |
| :--- | :--- | :--- |
|  Family Name | [Patient](explore_baby_details.html#mapping-for-baby-details-person-list) | name.family |
|  First Given Name | [Patient](explore_baby_details.html#mapping-for-baby-details-person-list) | name.given |
|  Other given names (s) | [Patient](explore_baby_details.html#mapping-for-baby-details-person-list) | name.given |
|  NHS Number | [Patient](explore_baby_details.html#mapping-for-baby-details-person-list) | identifier.nhsNumber |
|  Local Patient Identifier | [Patient](explore_baby_details.html#mapping-for-baby-details-person-list) | identifer |
|  Phenotypic Sex (Baby) | [Observation](explore_baby_details.html#mapping-for-observation-resource) | code and value |
|  Birth Order | [Patient](explore_baby_details.html#mapping-for-baby-details-person-list) | multipleBirthInteger |
|  Number of Births in confinement | [Observation](explore_baby_details.html#mapping-for-observation-resource) | code and value |
|  Birth Weight | [Observation](explore_baby_details.html#mapping-for-observation-resource) | code and value |
|  Locally calculated birth weight centile | [Observation](explore_baby_details.html#mapping-for-observation-resource) | code and value |
|  Length of Gestation at Birth | [Observation](explore_baby_details.html#mapping-for-observation-resource) | code and value |
|  Still Born Indicator | [Observation](explore_baby_details.html#mapping-for-observation-resource) | code and value |
|  Rhesus Status | [Observation](explore_baby_details.html#mapping-for-observation-resource) | code and value |
|  Suspected Congenital Abnormality Indicator | [Observation](explore_baby_details.html#mapping-for-observation-resource) | code and value |
|  Investigations Requested | [ProcedureRequest](explore_baby_details.html#mapping-for-procedurerequest-resource) | code |

The following tables detail how to populate the FHIR resources and the mapping to the Maternity data standard.

## Mapping for Baby Details (Person) List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_baby_details_all.html#mapping-for-baby-details-person-list)**|

## Patient Reference ##

The Baby Details (Person) list has a mandated subject reference to the Patient resource. This means that any exchange of the Baby Details (Person) heading data must also include the [Patient demographics List.](explore_patient_demographics.html)


## Mapping for Patient Resource (baby) ##

|>|Level 1|[Patient Resource](http://hl7.org/fhir/stu3/patient.html)|>|Level 2|[CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)|>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_baby_details_all.html#mapping-for-patient-resource-baby)**|


## Mapping for ProcedureRequest Resource ##

|>|Level 1|[ProcedureRequest Resource](http://hl7.org/fhir/stu3/procedurerequest.html)|>|Level 2|[CareConnect-ProcedureRequest-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-ProcedureRequest-1)|>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_baby_details_all.html#mapping-for-procedurerequest-resource)**|


## Mapping for Observation Resource ##
The following Observation codes and value data types should be used for the Observations for the Baby Details (Person) structure:

|  **Observation** | **Code** | **Value[x]** |
| :--- | --- | --- |
|  Phenotypic Sex (Baby) | TBC | **CodeableConcept:** <br>A snomed code from ^999002891000000103:Person phenotypic sex findings simple reference set (foundation metadata concept) |
|  Number of Births in confinement | TBC | **Quantity** |
|  Birth Weight | Snomed CT: 364589006 - Birth weight (observable entity) | **Quantity** |
|  Locally calculated birth weight centile | Snomed CT: 301334000 - Birth weight centile (observable entity) | **Quantity** |
|  Length of Gestation at Birth | Snomed CT: 412726003 - Length of gestation at birth (observable entity) | **Quantity** |
|  Still Born Indicator | TBC | **CodeableConcept:** <br>A Snomed code from <302080006:Finding of birth outcome (finding) |
|  Rhesus Status | TBC | **CodeableConcept:** <br>A Snomed code of '165747007 - RhD positive (finding)' or '165746003 - RhD negative (finding)' |
|  Suspected Congenital Abnormality Indicator | Snomed CT: 1097291000000101 - Suspected congenital abnormality (situation) | **Boolean** |

|>|Level 1|[Observation Resource](http://hl7.org/fhir/stu3/observation.html)|>|Level 2|[CareConnect-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_baby_details_all.html#mapping-for-observation-resource)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  Observation | ​ |  |  | Measurements and simple assertions<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (obs-7): If code is the same as a component code then the value element associated with the code SHALL NOT be present<br/>Constraint (obs-6): dataAbsentReason SHALL only be present if Observation.value[x] is not present |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource <br><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1'</font> |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | registered : preliminary : final : amended +<br/>Binding (required): Codes providing the status of an observation. [ObservationStatus](http://hl7.org/fhir/stu3/valueset-observation-status.html) <br> <font color='red'>This MUST contain the value 'final'</font> |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of observation (code / type)<br/>Binding (example): Codes identifying names of simple observations. [LOINC Codes](http://hl7.org/fhir/stu3/valueset-observation-codes.html) <br> <font color ='red'>This MUST contain the value specified for the relevant Observation specifed in the table above</font> |
|  - - coding | 0..* | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system describing a type of observation [CareConnect-ObservationType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ObservationType-1) <br> <font color ='red'>This MUST contain the value specified for the relevant Observation specifed in the table above</font> |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who and/or what this is about<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided <br> <font color ='red'>This MUST reference the Patient that is the subject of the Observation</font> |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|  - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - value[x] | 0..1 | Optional | [Quantity](http://hl7.org/fhir/stu3/datatypes.html#quantity "Quantity") | Actual result<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present <br><font color ='red'>This MUST use the value datatype specified for the relevant Observation specifed in the table above </font> |
|   |  | Optional | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") |  |
|   |  | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") |  |
|   |  | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") |  |
|   |  | Optional | [Range](http://hl7.org/fhir/stu3/datatypes.html#range "Range") |  |
|   |  | Optional | [Ratio](http://hl7.org/fhir/stu3/datatypes.html#ratio "Ratio") |  |
|   |  | Optional | [SampledData](http://hl7.org/fhir/stu3/datatypes.html#sampleddata "SampledData") |  |
|   |  | Optional | [Attachment](http://hl7.org/fhir/stu3/datatypes.html#attachment "Attachment") |  |
|   |  | Optional | [Time](http://hl7.org/fhir/stu3/datatypes.html#time "Time") |  |
|   |  | Optional | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") |  |
|   |  | Optional | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") |  |

## Baby Details (Person) Heading Example ##