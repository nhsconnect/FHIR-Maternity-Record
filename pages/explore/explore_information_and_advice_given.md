---
title: Information and Advice Given Bundle
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_information_and_advice_given.html
summary: "The FHIR profiles used for the Information and advice given Bundle"
---

## Heading Description ##
A record of any information or advice given for the woman, carer or relevant third party.

- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)
- [CareConnect-Communication-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Communication-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)

The following profiles are referenced from the investigation results details list structure:

- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)

## Information and Advice Given Structure Details ##

{% include custom/information_and_advice.svg %}

## Mapping Overview ##

|Date/Time|[Communication](explore_information_and_advice_given.html#mapping-for-investigation-encounter)|sent|
|ODS/ORD Site Code|[Encounter](explore_information_and_advice_given.html#mapping-for-investigation-encounter)|context.[Encounter.location.location]|
|SDS Job Role Name|[PractitionerRole](explore_information_and_advice_given.html#mapping-for-investigation-results-role)|name.[practitionerRole]|
|Professional Name|[Practitioner](explore_information_and_advice_given.html#mapping-for-investigation-results-practitioner)|performer.[practitioner]|
|Information Or Advice Given|[Communication](explore_information_and_advice_given.html#mapping-for-investigation-results-observation)|payload.content|
|Recipient|[Communication](explore_information_and_advice_given.html#mapping-for-investigation-results-observation)|recipient|


## Mapping for Information and Advice Given List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3| None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_safeguarding_all.html#mapping-for-safeguarding-details-list)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | Meta | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-List-1'</font> |
|  - identifier | 0..* | Required | Identifier | Business identifier<br/><font color='red'>An identifier for this Observation details list</font> |
|  - - system | 1..1 | Required | Uri | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Mandatory | String | The value that is unique<br/><font color='red'>An identifier for this Observation details list</font> |
|  - status | 1..1 | Mandatory | Code | current : retired : entered-in-error<br/>Binding (required): The current state of the list [ListStatus](http://hl7.org/fhir/stu3/valueset-list-status.html)<br/><font color='red'>The status of the list MUST contain the value 'current'</font> |
|  - mode | 1..1 | Mandatory | Code | working : snapshot : changes<br/>Binding (required): The processing mode that applies to this list [ListMode](http://hl7.org/fhir/stu3/valueset-list-mode.html)<br/><font color='red'>The mode of the list MUST contain the value 'snapshot'</font> |
|  - title | 0..1 | Mandatory | String | Descriptive name for the list<br/><font color='red'>This MUST contain the value 'Observation'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading Investigation Results'</b></font>  |
|  - code | 0..1 | Mandatory | CodeableConcept | What the purpose of this list is<br/>Binding (preferred): What the purpose of a list is [CareConnect-ListCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListCode-1)<br/><font color='red'>The PRSB heading for this list. Note: for Maternity the value stated below is used which is not from the preferred value set </font> |
|  - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system<br/><font color='red'>The SNOMED CT concept for the PRSB heading type</font> |
|  - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value '1052951000000105'</font> |
|  - - - display | 0..1 | Mandatory | String | Representation defined by the system<br/><font color='red'>This MUST contain the value 'Information and advice given'<br/>Mapping to Maternity data item = 'PSRB Heading Information and advice given'</font>  |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color="red">This is the subject of the Observations details List. This MUST use the CareConnect patient profile.</font>See [patient resource reference](explore_observation.html#patient-reference) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - date | 0..1 | Required | dateTime | When the list was prepared<br/><font color="red">This MUST contain a system date to indicate when the list was created or updated</font> |
|  - entry | 0..* | Required | BackboneElement | Entries in the list<br/><font color="red">The entries MUST be as per the diagram for this PRSB headings list with the encounter resource being the focal resource. Multiple Observations with associated resources MAY be present</font> |
|  - - date | 0..1 | Required | dateTime | When item added to list<br/><font color='red'>The SHOULD contain a system time of when the item was added to the list.</font> |
|  - - item | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color="red">A reference to an Observation resource included in the list. This MUST use the CareConnect Observation profile.</font>See [Observation resource](explore_investigation_results.html#mapping-for-investigation-results-observation) for information on how to populate the resource. |
|  - - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL <font color="red">The reference to the included Observation resource.</font> |

## Patient Reference ##

The Plan and requested actions List has a mandated subject reference to the Patient resource. This means that any exchange of the Plan and requested actions heading data must also include the [Patient demographics List.](explore_patient_demographics.html)

## Mapping for Information and Advice Given Communication ##

|>|Level 1|[Communication Resource](http://hl7.org/fhir/stu3/communication.html)|>|Level 2|[CareConnect-Communication-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Communication-1)|>|Level 3| None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_safeguarding_all.html#mapping-for-safeguarding-details-list)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description/Constraints** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Communication-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Unique identifier |
|  - - system | 0..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/> |
|  - - value | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - status | 1..1 | Mandatory | code | <font color="red">MUST be 'completed'</font> |
|  - recipient | 0..* | Required | [Reference](http://hl7.org/fhir/STU3/references.html "Reference") | Message recipient<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color="red">This MUST be a reference to the RelatedPerson resource</font> |
|   | 0..1 | Required | [CareConnect-RelatedPerson-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-RelatedPerson-1 "CareConnect-RelatedPerson-1") | <font color="red">The relationship of the person accompanying the person who the advice was given to. This MUST use the relatedPerson resource.</font>See [relatedPerson resource] (explore_investigation_results.html#mapping-for-investigation-encounter) for information on how to populate the resource. |
|  - context | 0..1 | Required | [Reference](http://hl7.org/fhir/STU3/references.html "Reference") | Encounter or episode leading to message<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color="red">This MUST be a reference to Encounter resource</font> |
|   | 0..1 | Required | [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1 "CareConnect-Encounter-1") | <font color="red">The Encounter where the information and advice was given out.This MUST use the Encounter resource.</font>See [Encounter resource](explore_investigation_results.html#mapping-for-investigation-encounter) for information on how to populate the resource. |
|  - - reference | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the Encounter resource</font>  |
|  - sent | 0..1 | Mandatory | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When sent<br/><font color="red">The date on which the information and advice was given</font> |
|  - sender | 0..1 | Required | [Reference](http://hl7.org/fhir/STU3/references.html "Reference") | Message sender<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color="red">This MUST be a reference to Practitioner resource</font><br/> |
|   | 0..1 | Required | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1-1 "CareConnect-Practitioner-1") | <font color="red">The Practitioner who gave the information and advice..This MUST use the Practitioner resource.</font>See [Practitioner resource] (explore_investigation_results.html#mapping-for-investigation-encounter) for information on how to populate the resource. |
|  - payload | 0..* | Required | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Message payload<br/><font color="red">The oral or written information or advice given to the patient, carer, other authorised representative, care professional or other third party.</font> |
|  - - content[x] | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Message part content |

## Mapping for Information and Advice Given Encounter ##

|>|Level 1|[Encounter Resource](http://hl7.org/fhir/stu3/encounter.html)|>|Level 2|[CareConnect-Encounter-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)|>|Level 3| None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_safeguarding_all.html#mapping-for-safeguarding-details-list)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | Meta | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Encounter-1'</font> |
|  - identifier | 0..* | Required | Identifier | Identifier(s) by which this encounter is known<br/><font color='red'>An identifier for this Encounter</font> |
|  - - system | 1..1 | Mandatory | Uri | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Mandatory | String | The value that is unique<br/><font color='red'>An identifier for this observation encounter</font> |
|  - status | 1..1 | Mandatory | Code | planned : arrived : triaged : in-progress : onleave : finished : cancelled +<br/>Binding (required): Current state of the encounter [EncounterStatus](http://hl7.org/fhir/stu3/valueset-encounter-status.html) |
|  - period | 0..1 | Mandatory | Period | The start and end time of the encounter<br/>Constraint (per-1): If present, start SHALL have a lower value than end<br/><font color="red">The date on which the observation was recorded</font> |
|  - - start | 0..1 | Mandatory | dateTime | Starting time with inclusive boundary |
|  - - end | 0..1 | Required | dateTime | End time with inclusive boundary, if not ongoing |
|  - location | 0..* | Required | BackboneElement | List of locations where the patient has been |
|  - - location | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Location the encounter takes place<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>Details of where the information and advice was given</font> |
|   |  | Mandatory | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") | This MUST use the CareConnect Location profile. </font>See [Location resource](explore_observation.html#mapping-for-observation-location) for information on how to populate the resource. |
|  - - - reference | 0..1 | Required | String | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the Location resource included in the Communication details</font>  |

## Mapping for Information and Advice Given RelatedPerson ##

The information and advice given details has reference(s) to the related person resource. This means that any exchange of the information and advice given heading data must also include the [Related Person Details](explore_related_person.html#mapping-for-related_person).

## Mapping for Investigation Results Practitioner ##

The investigation results has reference(s) to the Practitioner resource. This means that any exchange of the investigation results heading data must also include the [Practitioner Details](explore_practitioner.html#mapping-for-practitioner)

## Mapping for Investigation Results Role ##

The investigation results has reference(s) to the Practitioner Role resource. This means that any exchange of the investigation results heading data must also include the [Practitioner Role Details](explore_practitioner_role.html#mapping-for-practitioner_role)

## Example of Information and Advice Given ##

<script src="https://gist.github.com/IOPS-DEV/c9e4f5151d7816084ad71d30e380311e.js"></script>
