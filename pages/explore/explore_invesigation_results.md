---
title: Investigation Results Bundle
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_investigation_results.html
summary: "The FHIR profiles used for the Investigation results Bundle"
---

## Heading Description ##
The details of the investigation results.

- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)
- [CareConnect-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)

The following profiles are referenced from the investigation results details list structure:

- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)

## Investigation Results Structure Details ##

{% include custom/investigation_results.svg %}

## Mapping Overview ##

|Date/Time|[Encounter](explore_investigation_results.html#mapping-for-investigation-encounter)|period.start|
|ODS/ORD Site Code|[Encounter](explore_investigation_results.html#mapping-for-investigation-encounter)|location.[Location.identifier]|
|SDS Job Role Name|[Observation](explore_investigation_results.html#mapping-for-investigation-results-role)|name.[practitionerRole]|
|Professional Name|[Observation](explore_investigation_results.html#mapping-for-investigation-results-practitioner)|performer.[practitioner]|
|Investigation|[Observation](explore_investigation_results.html#mapping-for-investigation-results-observation)|code|
|Investigation Results|[Observation](explore_investigation_results.html#mapping-for-investigation-results-observation)|value|


## Mapping for Investigation Results List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3| None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_safeguarding_all.html#mapping-for-safeguarding-details-list)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | Meta | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1'</font> |
|  - identifier | 0..* | Required | Identifier | Business identifier<br/><font color='red'>An identifier for this Observation details list</font> |
|  - - system | 1..1 | Required | Uri | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Mandatory | String | The value that is unique<br/><font color='red'>An identifier for this Observation details list</font> |
|  - status | 1..1 | Mandatory | Code | current : retired : entered-in-error<br/>Binding (required): The current state of the list [ListStatus](http://hl7.org/fhir/stu3/valueset-list-status.html)<br/><font color='red'>The status of the list MUST contain the value 'current'</font> |
|  - mode | 1..1 | Mandatory | Code | working : snapshot : changes<br/>Binding (required): The processing mode that applies to this list [ListMode](http://hl7.org/fhir/stu3/valueset-list-mode.html)<br/><font color='red'>The mode of the list MUST contain the value 'snapshot'</font> |
|  - title | 0..1 | Mandatory | String | Descriptive name for the list<br/><font color='red'>This MUST contain the value 'Observation'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading Investigation Results'</b></font>  |
|  - code | 0..1 | Mandatory | CodeableConcept | What the purpose of this list is<br/>Binding (preferred): What the purpose of a list is [CareConnect-ListCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListCode-1)<br/><font color='red'>The PRSB heading for this list. Note: for Maternity the value stated below is used which is not from the preferred value set </font> |
|  - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system<br/><font color='red'>The SNOMED CT concept for the PRSB heading type</font> |
|  - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value '1082101000000102'</font> |
|  - - - display | 0..1 | Mandatory | String | Representation defined by the system<br/><font color='red'>Mapping to Maternity data item = 'PSRB Heading Investigation results'</font>  |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color="red">This is the subject of the Observations details List. This MUST use the CareConnect patient profile.</font>See [patient resource reference](explore_observations.html#patient-reference) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - date | 0..1 | Required | dateTime | When the list was prepared<br/><font color="red">This MUST contain a system date to indicate when the list was created or updated</font> |
|  - entry | 0..* | Required | BackboneElement | Entries in the list<br/><font color="red">The entries MUST be as per the diagram for this PRSB headings list with the encounter resource being the focal resource. Multiple Observations with associated resources MAY be present</font> |
|  - - date | 0..1 | Required | dateTime | When item added to list<br/><font color='red'>The SHOULD contain a system time of when the item was added to the list.</font> |
|  - - item | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color="red">A reference to an Observation resource included in the list. This MUST use the CareConnect Observation profile.</font>See [Observation resource](explore_investigation_results.html#mapping-for-investigation-results-observation) for information on how to populate the resource. |
|  - - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL <font color="red">The reference to the included Observation resource.</font> |

## Patient Reference ##

The Plan and requested actions List has a mandated subject reference to the Patient resource. This means that any exchange of the Plan and requested actions heading data must also include the [Patient demographics List.](explore_patient_demographics.html)

## Mapping for Investigation results Observation ##

|>|Level 1|[Observation Resource](http://hl7.org/fhir/stu3/observation.html)|>|Level 2|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|>|Level 3| None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_safeguarding_all.html#mapping-for-safeguarding-details-list)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource|
|  - - profile | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Profiles this resource claims to conform to<br/><font color="red">The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business Identifier for observation<br/><font color='red'>An identifier for this Observation</font> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - - assigner | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | registered : preliminary : final : amended +<br/>Binding (required): Codes providing the status of an observation. [ObservationStatus](http://hl7.org/fhir/stu3/valueset-observation-status.html) |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of observation (code / type)<br/><font color="red">The type of investigation performed</font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system describing a type of observation [CareConnect-ObservationType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ObservationType-1) |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color="red"><71388002</font> |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color="red">Procedure (procedure)</font> |
|  - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color="red">This is the subject of the Observations details List. This MUST use the CareConnect patient profile.</font>See [patient resource reference](explore_observations.html#patient-reference) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - context | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Healthcare event during which this observation is made<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color="red">This MUST be a reference to Encounter resource</font> |
|   |  | Required | [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1 "CareConnect-Encounter-1") | <font color="red">The Encounter where the assessment was carried out.This MUST use the Encounter resource.</font>See [Encounter resource](explore_investigation_results.html#mapping-for-investigation-encounter) for information on how to populate the resource. |
|  - performer | 0..* | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who is responsible for the observation<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Required | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") | <font color="red">Name of Professional recording the observation</font> |
|  - value[x] | 0..1 | Required | Quantity | Actual result<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/>Binding (required): Common UCUM units for recording Vital Signs ( http://hl7.org/fhir/stu3/valueset-ucum-vitals-common.html )<br/><font color="red">For each investigation, the result of the investigation (this includes the result value, with unit of observation and reference interval where applicable and date)</font> |
|   |  | Required | CodeableConcept |  |
|   |  | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") |  |
|   |  | Required | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") |  |
|   |  | Required | [Range](http://hl7.org/fhir/stu3/datatypes.html#range "Range") |  |
|   |  | Required | [Ratio](http://hl7.org/fhir/stu3/datatypes.html#ratio "Ratio") |  |
|   |  | Required | [SampledData](http://hl7.org/fhir/stu3/datatypes.html#sampleddata "SampledData") |  |
|   |  | Required | [Attachment](http://hl7.org/fhir/stu3/datatypes.html#attachment "Attachment") |  |
|   |  | Required | [Time](http://hl7.org/fhir/stu3/datatypes.html#time "Time") |  |
|   |  | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") |  |
|   |  | Required | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") |  |


## Mapping for Investigation Encounter ##

|>|Level 1|[Encounter Resource](http://hl7.org/fhir/stu3/encounter.html)|>|Level 2|[CareConnect-Encounter-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)|>|Level 3| None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_safeguarding_all.html#mapping-for-safeguarding-details-list)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | Meta | Metadata about the resource |
|  - - profile | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Profiles this resource claims to conform to<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1'</font>|
|  - identifier | 0..* | Required | Identifier | Identifier(s) by which this encounter is known<br/><font color='red'>An identifier for this Encounter</font> |
|  - - system | 1..1 | Mandatory | Uri | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Mandatory | String | The value that is unique<br/><font color='red'>An identifier for this observation encounter</font> |
|  - status | 1..1 | Mandatory | Code | planned : arrived : triaged : in-progress : onleave : finished : cancelled +<br/>Binding (required): Current state of the encounter [EncounterStatus](http://hl7.org/fhir/stu3/valueset-encounter-status.html) |
|  - period | 0..1 | Mandatory | Period | The start and end time of the encounter<br/>Constraint (per-1): If present, start SHALL have a lower value than end<br/><font color="red">The date on which the observation was recorded</font> |
|  - - start | 0..1 | Mandatory | dateTime | Starting time with inclusive boundary |
|  - - end | 0..1 | Required | dateTime | End time with inclusive boundary, if not ongoing |
|  - location | 0..* | Required | BackboneElement | List of locations where the patient has been |
|  - - location | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Location the encounter takes place<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>Where the observation took place</font> |
|   |  | Mandatory | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") | <font color="red">This MUST use the CareConnect Location profile. </font>See [Location resource](explore_observations.html#mapping-for-observation-location) for information on how to populate the resource. |
|  - - - reference | 0..1 | Required | String | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the Location resource included in the observation details list</font>  |

## Mapping for Investigation Results Practitioner ##

The investigation results has reference(s) to the Practitioner resource. This means that any exchange of the investigation results heading data must also include the [Practitioner Details](explore_practitioner.html#mapping-for-practitioner)

## Mapping for Investigation Results Role ##

The investigation results has reference(s) to the Practitioner Role resource. This means that any exchange of the investigation results heading data must also include the [Practitioner Role Details](explore_practitioner_role.html#mapping-for-practitioner_role)


## Mapping for Investigation Results Location ##

The investigation results details has reference(s) to the Location resource. This means that any exchange of the investigation results details heading data must also include the [Location Details](explore_location.html#mapping-for-location)

## Example of Investigation Result ##

<script src="https://gist.github.com/IOPS-DEV/2352b840abe6fe3102405bb685b0d454.js"></script>