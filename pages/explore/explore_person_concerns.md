---
title: Person concerns List
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_person_concerns.html
summary: "The FHIR profiles used for the Person concerns List"
---

## Heading Description ##
Details of the woman’s concerns, expectations and wishes.

{% include custom/under.construction.html content="Please check back later for any updates to this page" %}  

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
|Maternity Care Plan Type|[CarePlan](explore_person_concerns.html#mapping-for-person-concerns-careplan)|category|
|Planned delivery setting|[Location](explore_person_concerns.html#mapping-for-person-concerns-location)|type|
|Reason for change of planned delivery setting|[CarePlan](explore_person_concerns.html#mapping-for-person-concerns-careplan)|activity.detail.reasonCode|
|Advance Statement Date|[Contract](explore_person_concerns.html#mapping-for-person-concerns-contract)|meta.lastUpdated|
|Advance Statement Details|[Contract](explore_person_concerns.html#mapping-for-person-concerns-contract)|text|
|Location of Advance Statement Document||unmapped| 

## Mapping for Person concerns List ##  

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_person_concerns_all.html#mapping-for-person-concerns-list)**| 

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  List | ​ |  |  | Information summarized from a list of other resources<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (lst-2): The deleted flag can only be used if the mode of the list is "changes"<br/>Constraint (lst-1): A list can only have an emptyReason if it is empty |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business identifier<br><font color='red'>An identifier for this Person concerns List</font><br/><br/> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came</font> |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique<br/><font color='red'>A value for the identifier</font> |
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
|  - - - code | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value 'tbc'</font> |
|  - - - display | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>This MUST contain the value 'Person concerns'</font><br/><font color='red'>Mapping to Maternity data item = 'PSRB Heading Person concerns'</font>  |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color='red'>This is the subject of the Person concerns List.<br/>This MUST use the CareConnect patient profile. </font>See [patient resource reference](explore_person_concerns.html#patient-reference) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - date | 0..1 | Mandatory | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the list was prepared<br/><font color='red'> This MUST contain a system date to indicate when the list created or updated</font> |
|  - note | 0..* | Optional | [Annotation](http://hl7.org/fhir/stu3/datatypes.html#annotation "Annotation") | Comments about the list |
|  - - author[x] | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Individual responsible for the annotation<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") |  |
|   |  | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | <font color='red'>Who authored the comment on the list.</font>  |
|  - - time | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the annotation was made |
|  - - text | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The annotation - text content |
|  - entry | 0..* | Mandatory | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Entries in the list<br/><font color='red'>The entries MUST be as per the diagram for this PRSB headings list with the CarePlan resource being the focal resource. </font> |
|  - - date | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When item added to list<br/><font color='red'>The SHOULD contain a system time of when the item was added to the list.</font> |
|  - - item | 1..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>A reference to a CarePlan resource included in the list</font><br/> |
|  - - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/> |

## Patient Reference ##
The Plan and requested actions List has a mandated subject reference to the Patient resource. This means that any exchange of the Plan and requested actions heading data must also include the [Patient demographics List.](explore_patient_demographics.html)  

## Mapping for Person concerns CarePlan ##  

|>|Level 1|[CarePlan Resource](http://hl7.org/fhir/stu3/careplan.html)|>|Level 2|[CareConnect-CarePlan-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-CarePlan-1)|>|Level 3|None|  

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_person_concerns_all.html#mapping-for-person-concerns-careplan)**| 


|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| --- | --- | --- | --- | --- |
|  CarePlan | ​ |  |  | Healthcare plan for patient or group<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource  <br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-CarePlan-1'</font>  |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | External Ids for this plan <br/><font color='red'>An identifier for this Plan and requested actions CarePlan</font><br/> |
|  - - system | 0..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value <br/><font color='red'>The system from which the identifier came</font> |
|  - - value | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique <br/><font color='red'>A value for the identifier for this Plan and requested actions CarePlan</font> |
|  - - assigner | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
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
|  - - - code | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - userSelected | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - title | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Human-friendly name for the CarePlan |
|  - description | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Summary of nature of plan |
|  - subject | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who care plan is for<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  context | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Created in context of<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1 "CareConnect-Encounter-1") |  |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - period | 1..1 | Mandatory | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Time period plan covers<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - start | 1..1 | Mandatory | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary<br><font color='red'><b>Mapping to Digital Maternity data item 'Date/time'</b></font>  |
|  - - end | 0..1 | Optional | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - author | 0..* | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who is responsible for contents of the plan<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Required | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") |  |
|  - - reference | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - goal | 0..* | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Desired outcome of plan<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br><font color='red'><b>Mapping to Digital Maternity data item 'Concern, wishes or goal details'</b></font>  |
|   |  | Required | [Goal](http://hl7.org/fhir/stu3/StructureDefinition/Goal "Goal") |  |
|  - - reference | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - activity | 0..* | Required | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Action to occur as part of plan<br/>Constraint (cpl-3): Provide a reference or detail, not both |
|  - - outcomeCodeableConcept | 0..* | Optional | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Results of the activity<br/>Binding (example): Identifies the results of the activity [Care Plan Activity Outcome](http://hl7.org/fhir/stu3/valueset-care-plan-activity-outcome.html) |
|  - - - coding | 0..* | Optional | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - system | 0..1 | Optional | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - code | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - userSelected | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - outcomeReference | 0..* | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Appointment, Encounter, Procedure, etc.<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [Resource](http://hl7.org/fhir/stu3/StructureDefinition/Resource "Resource") |  |
|  - - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - - - category | 0..1 | Optional | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | diet : drug : encounter : observation : procedure : supply : other<br/>Binding (example): High-level categorization of the type of activity in a care plan. [CarePlanActivityCategory](http://hl7.org/fhir/stu3/valueset-care-plan-activity-category.html) |
|  - - - - coding | 0..* | Optional | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - - system | 0..1 | Optional | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - - code | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - - userSelected | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - - code | 0..1 | Optional | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Detail type of activity<br/>Binding (example): Detailed description of the type of activity; e.g. What lab test, what procedure, what kind of encounter. [Care Plan Activity](http://hl7.org/fhir/stu3/valueset-care-plan-activity.html) |
|  - - - - coding | 0..* | Optional | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - - system | 0..1 | Optional | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - - code | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - - userSelected | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - - reasonCode | 0..* | Required | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Why activity should be done or why activity was prohibited<br/>Binding (example): Identifies why a care plan activity is needed. Can include any health condition codes as well as such concepts as "general wellness", prophylaxis, surgical preparation, etc. [Activity Reason](http://hl7.org/fhir/stu3/valueset-activity-reason.html)<br/><font color='red'><b>Mapping to Digital Maternity data item 'Reason for change of planned delivery setting'</b></font> |
|  - - - - coding | 0..* | Optional | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - - system | 0..1 | Optional | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - - code | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - - userSelected | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - - reasonReference | 0..* | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Condition triggering need for activity<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-Condition-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Condition-1 "CareConnect-Condition-1") |  |
|  - - - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - - - status | 1..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | not-started : scheduled : in-progress : on-hold : completed : cancelled : unknown<br/>Binding (required): Indicates where the activity is at in its overall life cycle. [CarePlanActivityStatus](http://hl7.org/fhir/stu3/valueset-care-plan-activity-status.html) |
|  - - - statusReason | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Reason for current status |
|  - - - prohibited | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | Do NOT do<br/>Default Value: false |
|   |  | Mandatory | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") |  |
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

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_person_concerns_all.html#mapping-for-person-concerns-contract)**| 


|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| --- | --- | --- | --- | --- |
|  Contract | ​ |  |  | Legal Agreement<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource <br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-CarePlan-1' <br><b>The lastUpdated element maps to Digital Maternity data item = 'Advance Statement data'</b></font>  |
|  - text | 0..1 | Required | [Narrative](http://hl7.org/fhir/stu3/narrative.html#Narrative "Narrative") | Text summary of the resource, for human interpretation<br><font color='red'><b>Mapping to Digital Maternity data item = 'Advance statement details'</b></font>  |
|  - identifier | 0..1 | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Contract number<br/><font color='red'>An identifier for this Person concerns Contract</font> |
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


## Mapping for Person concerns Location ##  

The Person concerns List has reference(s) to the Location resource. This means that any exchange of the plan and requested actions details heading data must also include the [Location Details](explore_location.html#mapping-for-location)

