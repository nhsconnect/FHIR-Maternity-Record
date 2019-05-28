---
title: Pregnancy Outcome List
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_pregnancy_outcome.html
summary: "The FHIR profiles used for the Pregnancy outcome List"
---

## Heading Description ##  
Details of a pregnancy outcome and birth

The following FHIR profiles are used to form the Plan and requested actions List structure:  
- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)  
- [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)  
- [CareConnect-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)
- [CareConnect-Condition-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Condition-1)  
- [CareConnect-Procedure-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Procedure-1)  
- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1) (Baby Patient)
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)  
- [CareConnect-RelatedPerson-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-RelatedPerson-1)  
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)  
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)  

The following profiles are referenced from the Patient demographics list structure:  
- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)  

## Pregnancy outcome Structure ##  

{% include custom/pregnancy_outcome.svg %}  

## Maternity data standard Mapping to FHIR profiles ##  

## Mapping Overview ##

|**Data Standard Element**|**FHIR Resource Mapping**|**FHIR Element**|
|Date/time|[Procedure](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-procedure)|performedDateTime|
|ODS/ORD Site Code|[Location](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-location)|identifier|  
|Professional Name|[Practitioner](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-practitioner)|name|
|SDS Job Role Name|[PractitionerRole](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-practitionerrole)|code|
|Pregnancy outcome|[Observation](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-outcome)|code/valueCodeableConcept|
|Date and time of Established Labour|[Observation](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-observation)|effectiveDateTime|
|Labour onset method|[Observation](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-observation)|code/value[x]|
|Date and time Fully Dilated|[Observation](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-observation)|effectiveDateTime| 
|Duration of 1st Stage|[Observation](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-observation)|code/valueQuantity| 
|Onset of 2nd Stage of Labour|[Observation](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-observation)|effectivePeriod.start| 
|Date and time pushing commenced|[Observation](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-observation)|effectivePeriod.start| 
|Location of birth|[Location](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-location)/[Organization](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-organization)|name|  
|Delivery place type|[Location](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-location)|type|  
|Delivery place type comment|[Location](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-location)|type.coding.text|  
|Birth attendants|[RelatedPerson](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-relatedperson)|name|  
|Date and Time of Rupture of Membranes|[Observation](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-observation)|code/valueDateTime| 
|Duration of Rupture of Membranes|[Observation](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-observation)|unmapped| 
|Pain relief|[Procedure](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-procedure)|code| 
|Anaesthesia Type|[Procedure](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-procedure)|code| 
|Delivery decision Date/Time||unmapped| 
|Delivery decision made by|[Practitioner](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-practitioner)|name| 
|Reason for Delivery decision||unmapped| 
|Head delivered||unmapped| 
|Delivery date/time|[Observation](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-observation)|code/valueDateTime| 
|Duration of second stage|[Observation](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-observation)|code/valueQuantity| 
|Attempted type of delivery|[Condition](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-condition)|code|  
|Type of delivery|[Procedure](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-procedure)|code| 
|Length of labour|[Observation](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-observation)|code/valueQuantity| 
|Delayed cord clamping duration||unmapped| 
|Delayed cord clamping details||unmapped| 
|Cord clamping delayed reason||unmapped| 
|Cord milked indicator||unmapped| 
|Placenta delivery method|[Procedure](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-procedure)|unmapped| 
|End of third stage|[Observation](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-observation)|unmapped| 
|Third stage duration|[Observation](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-observation)|code/valueQuantity| 
|Genital tract trauma|[Condition](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-condition)|code|  
|Examination of placenta and membranes||unmapped| 
|Placenta disposal method|[Procedure](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-procedure)|unmapped| 
|Placenta sent for histology|[Procedure](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-procedure)|unmapped| 
|Total blood loss|[Observation](explore_pregnancy_outcome.html#mapping-for-pregnancy-outcome-observation)|code/valueQuantity| 


## Mapping for Pregnancy outcome List ##  

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3|None|  

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_pregnancy_outcome_all.html#mapping-for-pregnancy-outcome-list)**| 

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  List |  |  |  | Information summarized from a list of other resources<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (lst-2): The deleted flag can only be used if the mode of the list is "changes"<br/>Constraint (lst-1): A list can only have an emptyReason if it is empty |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business identifier<br><font color='red'>An identifier for this Pregnancy outcome List</font><br/><br/> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came</font> |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique<br/><font color='red'>A value for the identifier</font> |
|  - - assigner | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource<br/> |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | current : retired : entered-in-error<br/>Binding (required): The current state of the list [ListStatus](http://hl7.org/fhir/stu3/valueset-list-status.html)<br/><font color='red'>The status of the list MUST contain the value 'current'</font> |
|  - mode | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | working : snapshot : changes<br/>Binding (required): The processing mode that applies to this list [ListMode](http://hl7.org/fhir/stu3/valueset-list-mode.html)<br/><font color='red'>The mode of the list MUST contain the value 'snapshot'</font> |
|  - title | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Descriptive name for the list<br/><font color='red'>This MUST contain the value 'Pregnancy outcome'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading Pregnancy outcome'</b></font>  |
|  - code | 0..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | What the purpose of this list is<br/>Binding (preferred): What the purpose of a list is [CareConnect-ListCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListCode-1)<br/><font color='red'>The PRSB heading for this list. Note: for Maternity the value stated below is used which is not from the preferred value set </font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/><font color='red'>The SNOMED CT concept for the PRSB heading type</font> |
|  - - - system | 0..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value 'tbc'</font> |
|  - - - display | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>This MUST contain the value 'Pregnancy outcome'</font><br/><font color='red'><b>Mapping to Maternity data item = 'Pregnancy outcome'</b></font>  |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color='red'>This is the subject of the Pregnancy outcome List.<br/>This MUST use the CareConnect patient profile. </font>See [patient resource reference](explore_pregnancy_outcome.html#patient-reference) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - date | 0..1 | Mandatory | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the list was prepared<br/><font color='red'> This MUST contain a system date to indicate when the list was created or updated</font> |
|  - note | 0..* | Optional | [Annotation](http://hl7.org/fhir/stu3/datatypes.html#annotation "Annotation") | Comments about the list |
|  - - author[x] | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Individual responsible for the annotation<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") |  |
|   |  | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | <font color='red'>Who authored the comment on the list.</font>  |
|  - - time | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the annotation was made |
|  - - text | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The annotation - text content |
|  - entry | 0..* | Mandatory | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Entries in the list<br/><font color='red'>The entries MUST be as per the diagram for this PRSB headings list with the Encounter, Condition, Observation and Procedure resources being the focal resources. </font> |
|  - - date | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When item added to list<br/><font color='red'>The SHOULD contain a system time of when the item was added to the list.</font> |
|  - - item | 1..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>A reference to the Encounter, Condition, Observation and Procedure resources included in the list</font><br/> |
|  - - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/> |

## Patient Reference ##  

The Pregnancy outcome List has a mandated subject reference to the Patient resource. This means that any exchange of the Plan and requested actions heading data must also include the [Patient demographics List.](explore_patient_demographics.html)  



## Mapping for Pregnancy outcome Encounter ##  

|>|Level 1|[Encounter Resource](http://hl7.org/fhir/stu3/encounter.html)|>|Level 2|[CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)|>|Level 3|None|  

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_pregnancy_outcome_all.html#mapping-for-pregnancy-outcome-encounter)**|  


|  **Name** | **Card.** | **Conformance** | **Type** | Description, Constraints and mapping for Implementation |
| :--- | :--- | :--- | :--- | :--- |
|  Encounter | ​ |  |  | An interaction during which services are provided to the patient<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Identifier(s) by which this encounter is known <br/><font color='red'>An identifier for this Encounter</font> |
|  - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came</font>  |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique <br/><font color='red'>A value for the identifier </font> |
|  - - assigner | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | planned : arrived : triaged : in-progress : onleave : finished : cancelled +<br/>Binding (required): Current state of the encounter [EncounterStatus](http://hl7.org/fhir/stu3/valueset-encounter-status.html) |
|  - subject | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | The patient ro group present at the encounter<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|  - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - participant | 0..1 | Required | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | List of participants involved in the encounter  |
|  - - type | 0..* | Optional | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Role of participant in encounter<br/>Binding (extensible): Role of participant in encounter [ParticipantType](http://hl7.org/fhir/stu3/valueset-encounter-participant-type.html) |
|  - - - coding | 0..* | Optional | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - system | 0..1 | Optional | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - code | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - userSelected | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - period | 0..1 | Optional | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Period of time during the encounter that the participant participated<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Optional | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - end | 0..1 | Optional | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - - individual | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Persons involved in the encounter other than the patient<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [RelatedPerson](http://hl7.org/fhir/stu3/StructureDefinition/RelatedPerson "RelatedPerson") |  |
|   |  | Optional | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") |  |
|  - - - reference | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - period | 0..1 | Optional | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | The start and end time of the encounter<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - start | 0..1 | Optional | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - end | 0..1 | Optional | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - location | 1..* | Mandatory | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | List of locations where the patient has been |
|  - - location | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Location the encounter takes place<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") |  |
|  - - - reference | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - - status | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | planned : active : reserved : completed<br/>Binding (required): The status of the location. [EncounterLocationStatus](http://hl7.org/fhir/stu3/valueset-encounter-location-status.html) |
|  - - period | 0..1 | Optional | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Time period during which the patient was present at the location<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Optional | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - end | 0..1 | Optional | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
 


## Mapping for Pregnancy outcome Observation ##  

The following combination of Observation codes, value datatypes and other elements should be used for the Observations for the Pregnancy outcome structure:

|  **Observation** | **Code** | **Value[x]** | **Conformance** |
| :--- | --- | --- |
|  Pregnancy outcome | SNOMED CT: 267013003 - Past pregnancy outcome | **CodeableConcept:** <br>A code from NHS Data Dictionary - PREGNANCY OUTCOME CODE | Mandatory |
|  Labour onset method | tbc | **CodeableConcept:** <br>A code from a SNOMED valueset tbc | Mandatory |
|  Date and time of rupture of membrane | Snomed CT: 289251005 - Time rupture of membranes detected | **valueDateTime** | Required |
|  Delivery date/time | Snomed CT: 397836004 - Time of delivery | **valueDateTime** | Mandatory |
|  Duration of second stage | Snomed CT: 169822006 - Duration of second stage of labour | **valueQuantity** | Required |
|  Length of labour | SNOMED CT: 289248003 - Duration of labour | **valueQuantity** | Required |
|  Third stage duration | SNOMED CT: 169823002 - Duration of third stage of labour | **valueQuantity** | Required |
|  Total blood loss | Snomed CT: 250771004 - Actual blood loss | **valueQuantity** | Mandatory |

|  **Observation** | **Code** | **Element** | **Conformance** |
| :--- | --- | --- |
|  Date and time of established labour | SNOMED CT: 20236002 - Labour established | **effectiveDateTime** | Required |
|  Date and time Fully Dilated | SNOMED CT: 62472004 - Cervix fully dilated | **effectiveDateTime** | Required |
|  Onset of 2nd stage of labour | SNOMED CT: 249160009 - Onset of second stage of labour | **effectivePeriod.start** | Required |
|  Date and time pushing commenced | SNOMED CT: 249163006 - Onset of pushing (in labor) | **effectivePeriod.start** | Required |

|>|Level 1|[Observation Resource](http://hl7.org/fhir/stu3/observation.html)|>|Level 2|[CareConnect-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|>|Level 3|None|  

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_pregnancy_outcome_all.html#mapping-for-pregnancy-outcome-observation)**| 



|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  Observation | ​ |  |  | Measurements and simple assertions<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (obs-7): If code is the same as a component code then the value element associated with the code SHALL NOT be present<br/>Constraint (obs-6): dataAbsentReason SHALL only be present if Observation.value[x] is not present |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business Identifier for observation <br><font color='red'>An identifier for this Pregnancy outcome Observation</font> |
|  - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came</font> |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique <font color='red'>The value for the identifier</font><br/> |
|  - - assigner | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | registered : preliminary : final : amended +<br/>Binding (required): Codes providing the status of an observation. [ObservationStatus](http://hl7.org/fhir/stu3/valueset-observation-status.html)<br/><font color='red'>This MUST contain the value 'final'</font> |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of observation (code / type)<br/>Binding (example): Codes identifying names of simple observations. [LOINC Codes](http://hl7.org/fhir/stu3/valueset-observation-codes.html)<br/><br/> |
|  - - coding | 0..1 | Optional | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Optional | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system describing a type of observation [CareConnect-ObservationType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ObservationType-1)<br/> |
|  - - - extension (snomedCTDescriptionID) | 0..1 | Optional | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | The SNOMED CT Description ID for the display.<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>CodeSystem tbc</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>tbc </font> |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>tbc</font> |
|  - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - subject | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who and/or what this is about<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|  - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - context | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Healthcare event during which this observation is made<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1 "CareConnect-Encounter-1") |  |
|  - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - effective[x] | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Clinically relevant time/time-period for observation<br/> |
|   |  | Required | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") |  |
|  - issued | 0..1 | Optional | [Instant](http://hl7.org/fhir/stu3/datatypes.html#instant "Instant") | Date/Time this was made available |
|  - performer | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who is responsible for the observation<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Required | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") |  |
|  - - reference | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - value[x] | 0..1 | Required | [Quantity](http://hl7.org/fhir/stu3/datatypes.html#quantity "Quantity") | Actual result<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present |
|  - value[x] |  | Required | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | The system element MUST contain the identity of the terminology system <br/> |
|  - value[x] |  | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") |  |
|  - value[x] |  | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") |  |
|  - value[x] |  | Optional | [Time](http://hl7.org/fhir/stu3/datatypes.html#time "Time") |  |
|  - value[x] |  | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") |  |
|  - value[x] |  | Required | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") |  |
|  - comment | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Comments about result |
|  - bodySite | 0..1 | Optional | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Observed body part<br/>Binding (example): Codes describing anatomical locations. May include laterality. [SNOMED CT Body Structures](http://hl7.org/fhir/stu3/valueset-body-site.html) |
|  - - coding | 0..* | Optional | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Optional | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - extension (snomedCTDescriptionID) | 0..1 | Optional | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | The SNOMED CT Description ID for the display.<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - userSelected | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - method | 0..1 | Optional | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | How it was done<br/>Binding (example): Methods for simple observations. [Observation Methods](http://hl7.org/fhir/stu3/valueset-observation-methods.html) |
|  - - coding | 0..* | Optional | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Optional | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (preferred): A code from SNOMED Clinical Terminology UK [CareConnect-ObservationMethod-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ObservationMethod-1) |
|  - - - extension (snomedCTDescriptionID) | 0..1 | Optional | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | The SNOMED CT Description ID for the display.<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - userSelected | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |


## Mapping for Pregnancy outcome Procedure ##  

The following combination of Procedure codes and other elements should be used for the Procedures for the Pregnancy outcome structure:

|  **Procedure** | **Code** | **Element** | **Conformance** |
| :--- | --- | --- |
|  Performed date/time | SNOMED CT: 223493006 - Documenting observations | **performedDateTime** | Mandatory |
|  Pain relief | A code from NHS Data Dictionary - PAIN RELIEF TYPE IN LABOUR AND DELIVERY | | Required |
|  Anaesthesia type | A code from NHS Data Dictionary - ANAESTHESIA TYPE IN LABOUR AND DELIVERY | | Required |
|  Type of delivery | A code from NHS Data Dictionary - NHS Data Dictionary - DELIVERY METHOD | | Mandatory |
|  Placenta delivery method | Snomed CT: 236994008 - Placental delivery procedure | | Mandatory |

|>|Level 1|[Procedure Resource](http://hl7.org/fhir/stu3/procedure.html)|>|Level 2|[CareConnect-Procedure-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Procedure-1)|>|Level 3|None|  

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_pregnancy_outcome_all.html#mapping-for-pregnancy-outcome-procedure)**| 


|  **Name** | **Card.** | **Conformance** | **Type** | **Description/Constraints** |
| :--- | :--- | :--- | :--- | :--- |
|  Procedure | ​ |  |  | An action that is being or was performed on a patient<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (pro-1): Reason not done is only permitted if notDone indicator is true |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Required | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource |
|  - - profile | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Profiles this resource claims to conform to <br><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Procedure-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | External Identifiers for this procedure <br><br/><font color='red'>An identifier for this Procedure</font> |
|  - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value <font color='red'>The system from which the identifier came</font> |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique <font color='red'>A value for the identifier</font> |
|  - - assigner | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - partOf | 0..* | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Part of referenced event<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Required | [CareConnect-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1 "CareConnect-Observation-1") |  |
|  - - reference | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | preparation | in-progress | suspended | aborted | completed | entered-in-error | unknown<br/>Binding (required): A code specifying the state of the procedure. [EventStatus](http://hl7.org/fhir/stu3/valueset-event-status.html) |
|  - notDone | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | True if procedure was not performed as scheduled<br/>Default Value: false |
|  - notDoneReason | 0..1 | Optional | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Reason procedure was not performed<br/>Binding (example): A code that identifies the reason a procedure was not performed. [Procedure Not Performed Reason (SNOMED-CT)](http://hl7.org/fhir/stu3/valueset-procedure-not-performed-reason.html) |
|  - - coding | 0..* | Optional | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - system | 0..1 | Optional | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - code | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - userSelected | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - category | 0..1 | Optional | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Classification of the procedure<br/>Binding (example): A code that classifies a procedure for searching, sorting and display purposes. [Procedure Category Codes (SNOMED CT)](http://hl7.org/fhir/stu3/valueset-procedure-category.html) |
|  - - coding | 0..* | Optional | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - system | 0..1 | Optional | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - code | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - userSelected | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - code | 0..1 | Required | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Identification of the procedure<br/>Binding (preferred): A code to identify a specific procedure. [Procedure Codes (SNOMED CT)](http://hl7.org/fhir/stu3/valueset-procedure-code.html) <br/> |
|  - - coding | 0..* | Optional | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK. [CareConnect-ProcedureCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ProcedureCode-1)<br/> |
|  - - extension (snomedCTDescriptionID) | 0..1 | Optional | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | The SNOMED CT Description ID for the display<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - userSelected | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - subject | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who the procedure was performed on<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|  - - reference | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - context | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Encounter or episode associated with the procedure<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1 "CareConnect-Encounter-1") |  |
|  - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - performed[x] | 1..1 | Mandatory | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Date/Period the procedure was performed<br><font color='red'><b>Mapping to Digital Maternity data item='Date/time'</b></font> |
|   |  | Optional | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") |  |
|  - performer | 0..1 | Required | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | The people who performed the procedure |
|  - - role | 0..1 | Optional | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | The role the actor was in<br/>Binding (example): A code that identifies the role of a performer of the procedure. [Procedure Performer Role Codes](http://hl7.org/fhir/stu3/valueset-performer-role.html) |
|  - - - coding | 0..* | Optional | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - system | 0..1 | Optional | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - code | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - userSelected | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - actor | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | The reference to the practitioner<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/> |
|   |  | Optional | [Device](http://hl7.org/fhir/stu3/StructureDefinition/Device "Device") |  |
|   |  | Required | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") |  |
|  - - - reference | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - - onBehalfOf | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization the device or practitioner was acting for<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/> |
|   |  | Optional | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - location | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Where the procedure happened<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Required | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") |  |
|  - - reference | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - bodySite | 0..* | Optional | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Target body sites<br/>Binding (example): Codes describing anatomical locations. May include laterality. [SNOMED CT Body Structures](http://hl7.org/fhir/stu3/valueset-body-site.html)<br/> |
|  - - coding (snomedCT) | 1..1 | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK. [CareConnect-BodySite-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-BodySite-1) |
|  - - extension (snomedCTDescriptionID) | 0..1 | Optional | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | The SNOMED CT Description ID for the display<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - userSelected | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - outcome | 0..1 | Optional | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | The result of procedure<br/>Binding (example): An outcome of a procedure - whether it was resolved or otherwise. [Procedure Outcome Codes (SNOMED CT)](http://hl7.org/fhir/stu3/valueset-procedure-outcome.html) |
|  - - coding | 0..* | Optional | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - system | 0..1 | Optional | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - code | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - userSelected | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |


## Mapping for Pregnancy outcome Condition ##  

The following combination of Condition codes and other elements should be used for the Conditions for the Pregnancy outcome structure:

|  **Condition** | **Code** | **Element** | **Conformance** |
| :--- | --- | --- |
|  Attempted type of delivery | SNOMED CT: Valueset tbc | | Required |
|  Genital tract trauma | A code from NHS Data Dictionary - TRAUMATIC LESION OF GENITAL TRACT TYPE CODE | | Required |  

|>|Level 1|[Condition Resource](http://hl7.org/fhir/stu3/condition.html)|>|Level 2|[CareConnect-Condition-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Condition-1)|>|Level 3|None|  

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_pregnancy_outcome_all.html#mapping-for-pregnancy-outcome-condition)**|  


|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| --- | --- | --- | --- | --- |
|  Condition | ​ |  |  | Detailed information about conditions, problems or diagnoses<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (con-4): If condition is abated, then clinicalStatus must be either inactive, resolved, or remission<br/>Constraint (con-3): Condition.clinicalStatus SHALL be present if verificationStatus is not entered-in-error |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource <br><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Condition-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | External Ids for this condition <br><font color='red'>An identifier for this Pregnancy outcome Condition </font> |
|  - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value <br><font color='red'>The system from which the identifier came </font> |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique <br><font color='red'>A value for the identifier </font> |
|  - - assigner | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - clinicalStatus | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | active : recurrence : inactive : remission : resolved<br/>Binding (required): The clinical status of the condition or diagnosis. [Condition Clinical Status Codes](http://hl7.org/fhir/stu3/valueset-condition-clinical.html) |
|  - category | 0..* | Optional | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | problem-list-item : encounter-diagnosis : presenting-complaint<br/>Binding (extensible): A category assigned to the condition. [CareConnect-ConditionCategory-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ConditionCategory-1) |
|  - - coding | 0..* | Optional | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - system | 1..1 | Optional | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - code | 0..1 | Required | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Identification of the condition, problem or diagnosis<br/>Binding (example): Identification of the condition or diagnosis. [Condition/Problem/Diagnosis Codes](http://hl7.org/fhir/stu3/valueset-condition-code.html)<br/> |
|  - - coding | 0..* | Optional | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Optional | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (required): A code from the SNOMED Clinical Terminology UK [CareConnect-ConditionCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ConditionCode-1) |
|  - - - extension (snomedCTDescriptionID) | 0..1 | Optional | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | Optional Extensions Element<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - userSelected | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - bodySite | 0..* | Optional | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Anatomical location, if relevant<br/>Binding (example): Codes describing anatomical locations. May include laterality. [SNOMED CT Body Structures](http://hl7.org/fhir/stu3/valueset-body-site.html) |
|  - - coding | 0..* | Optional | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Optional | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (required): A code from SNOMED Clinical Terminology UK [CareConnect-BodySite-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-BodySite-1) |
|  - - - extension (snomedCTDescriptionID) | 0..1 | Optional | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | Optional Extensions Element<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - userSelected | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - subject | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who has the condition?<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|  - - reference | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - context | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Encounter or episode when condition first asserted<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1 "CareConnect-Encounter-1") |  |
|  - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - onset[x] | 0..1 | Optional | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Estimated or actual date, date-time, or age <br/> |
|  - abatement[x] | 0..1 | Optional | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | If/when in resolution/remission  |
|  - assertedDate | 0..1 | Optional | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Date record was believed accurate |
|  - asserter | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Person who asserts this condition<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") |  |
|  - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - note | 0..* | Optional | [Annotation](http://hl7.org/fhir/stu3/datatypes.html#annotation "Annotation") | Additional information about the Condition |
|  - - author[x] | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Individual responsible for the annotation<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [RelatedPerson](http://hl7.org/fhir/stu3/StructureDefinition/RelatedPerson "RelatedPerson") |  |
|   |  | Optional | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") |  |
|   |  | Optional | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|   |  | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") |  |
|  - - time | 0..1 | Optional | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the annotation was made |
|  - - text | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The annotation - text content |


## Mapping for Pregnancy outcome Baby Patient ##  

|>|Level 1|[Patient Resource](http://hl7.org/fhir/stu3/patient.html)|>|Level 2|[CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)|>|Level 3|None|  

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_pregnancy_outcome_all.html#mapping-for-pregnancy-outcome-baby-patient)**| 

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  Patient | ​ |  |  | Information about an individual or animal receiving health care services<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource <br><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1'</font> |
|  - identifier | 0..* | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | An identifier for this patient<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open at End<br> <font color='red'>An identifier for this Pregnancy outcome Baby Patient</font> |
|  - - use | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known. [IdentifierUse](http://hl7.org/fhir/stu3/valueset-identifier-use.html) |
|  - - type | 0..1 | Optional | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [Identifier Type Codes](http://hl7.org/fhir/stu3/valueset-identifier-type.html) |
|  - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'></font> |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - - period | 0..1 | Optional | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - assigner | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - active | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | Whether this patient's record is in active use<br/>Default Value: true |
|  - name | 1..* | Mandatory | [HumanName](http://hl7.org/fhir/stu3/datatypes.html#humanname "HumanName") | A name associated with the patient<br/>Slicing: Discriminator: use, Ordering: false, Rules: Open at End |
|  - name (official) | 1..1 | Mandatory | [HumanName](http://hl7.org/fhir/stu3/datatypes.html#humanname "HumanName") | A name associated with the patient |
|  - - use | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | usual : official : temp : nickname : anonymous : old : maiden<br/><font color='red'>The value attribute MUST contain the value 'official'</font><br/>Binding (required): The use of a human name [CareConnect-NameUse-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-NameUse-1) |
|  - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text representation of the full name |
|  - - family | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Family name (often called 'Surname') |
|  - - given | 0..* | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Given names (not always 'first'). Includes middle names |
|  - - prefix | 0..* | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Parts that come before the name |
|  - - suffix | 0..* | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Parts that come after the name |
|  - - period | 0..1 | Optional | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Time period when name was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Optional | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - end | 0..1 | Optional | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - name (other) | 0..* | Optional | [HumanName](http://hl7.org/fhir/stu3/datatypes.html#humanname "HumanName") | A name associated with the patient |
|  - - use | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | usual : official : temp : nickname : anonymous : old : maiden<br/>Binding (required): The use of a human name [CareConnect-NameUse-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-NameUse-1) |
|  - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text representation of the full name |
|  - - family | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Family name (often called 'Surname') |
|  - - given | 0..* | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Given names (not always 'first'). Includes middle names |
|  - - prefix | 0..* | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Parts that come before the name |
|  - - suffix | 0..* | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Parts that come after the name |
|  - - period | 0..1 | Optional | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Time period when name was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Optional | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - end | 0..1 | Optional | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - gender | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | male : female : other : unknown<br/>Binding (required): The gender of a person used for administrative purposes. [CareConnect-AdministrativeGender-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-AdministrativeGender-1) |
|  - deceased[x] | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | Indicates if the individual is deceased or not |
|   |  | Optional | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") |  |
|  - multipleBirth[x] | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | Whether patient is part of a multiple birth |
|   |  | Optional | [Integer](http://hl7.org/fhir/stu3/datatypes.html#integer "Integer") |  |





## Mapping for Pregnancy outcome Practitioner ## 

The Pregnancy outcome List has reference(s) to the Practitioner resource. This means that any exchange of the Pregnancy outcome List heading data must also include the [Practitioner Details](explore_practitioner.html#mapping-for-practitioner)

## Mapping for Pregnancy outcome PractitionerRole ##  

The Pregnancy outcome List has reference(s) to the PractitionerRole resource. This means that any exchange of the Pregnancy outcome List heading data must also include the [PractitionerRole Details](explore_practitioner_role.html#mapping-for-practitioner_role)  

## Mapping for Pregnancy outcome RelatedPerson ##  

The Pregnancy outcome List has reference(s) to the related person resource. This means that any exchange of the Pregnancy outcome List heading data must also include the [Related Person Details](explore_related_person.html#mapping-for-related_person)  

## Mapping for Pregnancy outcome Location ##  

The Pregnancy outcome List has reference(s) to the Location resource. This means that any exchange of the Pregnancy outcome List heading data must also include the [Location Details](explore_location.html#mapping-for-location)  

## Mapping for Pregnancy outcome Organization ##  

The Pregnancy outcome List has reference(s) to the Organization resource. This means that any exchange of the Pregnancy outcome List heading data must also include the [Organization Details](explore_organization.html#mapping-for-organization)
