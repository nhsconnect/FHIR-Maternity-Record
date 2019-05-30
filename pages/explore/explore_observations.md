---
title: Observations Bundle
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_observations.html
summary: "The FHIR profiles used for the Observations Bundle"
---

## Heading Description ##
The record of physiological observations, e.g., weight, height, heart rate, blood pressure, temperature, pulse, respiratory rate and oxygen saturation. Use of National Early Warning Score (NEWS) scores where appropriate. 

The following FHIR profiles are used to form the https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Medication-1 details list structure:

- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [CareConnect-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)


The following profiles are referenced from the https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Medication-1 details list structure:

- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)

## Observation Structure Details ##

{% include custom/observations.svg %}

## Mapping Overview ##

|**Data Standard Element**|**FHIR Profile**|**FHIR target**|
|Date| [Encounter](explore_observations.html#mapping-for-observation-encounter)| location|
|ODS/ORD Site Code| [Encounter](explore_observations.html#mapping-for-observation-encounter) |location
|Professional Name| [Observation] Used by all Observation Instances | performer |
|SDS Job Role Name | [PractitionerRole](explore_observations.html#mapping-for-plan-and-requested-actions-practitionerrole) |code
|Weight| [Observation](explore_observations.html#mapping-for-weight-observation) | valuevalue.Quantity |
|Height /Length|[Observation](explore_observations.html#mapping-for-length-observation) | valuevalue.Quantity |
|BMI|[Observation](explore_observations.html#mapping-for-bmi-observation) | valuevalue.Quantity |
|Systolic Blood Pressure |[Observation](explore_observations.html#mapping-for-blood-pressure-observation-details) | component.value.valueQuantity |
|Diastolic Blood Pressure | [Observation]| component.value.valueQuantity |
|Heart Rate (bpm)|[Observation](explore_observations.html#mapping-for-heart-rate-observation) | valuevalue.Quantity |
|Temperature| [Observation](explore_observations.html#mapping-for-body-temperature-observation)| valuevalue.Quantity |
|Respiration rate| [Observation](explore_observations.html#mapping-for-respiratory-observation)| valuevalue.Quantity |
|Oxygen Saturation|[Observation](explore_observations.html#mapping-for-oxygen-saturation) | valuevalue.Quantity |

## Mapping for Observation List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_referral_details_all.html#mapping-for-referral)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | Meta | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-List-1'</font> |
|  - identifier | 0..* | Required | Identifier | Business identifier<br/><font color='red'>An identifier for this Observtion details list</font> |
|  - - system | 1..1 | Required | Uri | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Mandatory | String | The value that is unique<br/><font color='red'>An identifier for this Observation details list</font> |
|  - status | 1..1 | Mandatory | Code | current : retired : entered-in-error<br/>Binding (required): The current state of the list [ListStatus](http://hl7.org/fhir/stu3/valueset-list-status.html)<br/><font color='red'>The status of the list MUST contain the value 'current'</font> |
|  - mode | 1..1 | Mandatory | Code | working : snapshot : changes<br/>Binding (required): The processing mode that applies to this list [ListMode](http://hl7.org/fhir/stu3/valueset-list-mode.html)<br/><font color='red'>The mode of the list MUST contain the value 'snapshot'</font> |
|  - title | 0..1 | Mandatory | String | Descriptive name for the list<br/><font color='red'>This MUST contain the value 'Referralt'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading Observations'</b></font>  |
|  - code | 0..1 | Mandatory | CodeableConcept | What the purpose of this list is<br/>Binding (preferred): What the purpose of a list is [CareConnect-ListCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListCode-1)<br/><font color='red'>The PRSB heading for this list. Note: for Maternity the value stated below is used which is not from the preferred value set </font> |
|  - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system<br/><font color='red'>The SNOMED CT concept for the PRSB heading type</font> |
|  - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value 'Observations'</font> |
|  - - - display | 0..1 | Mandatory | String | Representation defined by the system<br/><font color='red'>Mapping to Maternity data item = 'PSRB Heading Referral'</font>  |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color="red">This is the subject of the Observations details List. This MUST use the CareConnect patient profile.</font>See [patient resource reference](explore_referral_details.html#patient-reference) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - date | 0..1 | Required | dateTime | When the list was prepared<br/><font color="red">This MUST contain a system date to indicate when the list was created or updated</font> |
|  - entry | 0..* | Required | BackboneElement | Entries in the list<br/><font color="red">The entries MUST be as per the diagram for this PRSB headings list with the encounter resource being the focal resource. Multiple Observations with associated resources MAY be present</font> |
|  - - date | 0..1 | Required | dateTime | When item added to list<br/><font color='red'>The SHOULD contain a system time of when the item was added to the list.</font> |
|  - - item | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color="red">A reference to an Observation resource included in the list This MUST use the CareConnect Observation profile. |
|  - - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL |

## Patient Reference ##

The Plan and requested actions List has a mandated subject reference to the Patient resource. This means that any exchange of the Plan and requested actions heading data must also include the [Patient demographics List.](explore_patient_demographics.html)

## Mapping for Weight Observation ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/Observation.html)|>|Level 2|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|>|Level 3|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_observations_all.html#mapping-for-blood-pressure-observation-details)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  Observation | ​ |  |  | Measurements and simple assertions<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (obs-7): If code is the same as a component code then the value element associated with the code SHALL NOT be present<br/>Constraint (obs-6): dataAbsentReason SHALL only be present if Observation.value[x] is not present |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Observation-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business Identifier for observation<br/><font color='red'>An identifier for this Observation</font> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - - assigner | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | registered : preliminary : final : amended +<br/>Binding (required): Codes providing the status of an observation. [ObservationStatus](http://hl7.org/fhir/stu3/valueset-observation-status.html) |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of observation (code / type)<br/><font color="red">Weight Observation</font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system describing a type of observation [CareConnect-ObservationType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ObservationType-1) |
|  - - - extension (snomedCTDescriptionID) | 0..1 | Required | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | The SNOMED CT Description ID for the display.<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color="red">SNOMED CT code 27113001</font> |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color="red">MUST be 'Body weight'</font> |
|  - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who and/or what this is about<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|  - - identifier | 0..1 | Mandatory | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - effective[x] | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Clinically relevant time/time-period for observation<br/><font color="red">The date/time the obsrvation was recorded</font><br/> |
|  - performer | 0..* | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who is responsible for the observation<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") | <font color="red">The Site Code of where the obsrvation was recorded</font> |
|   |  | Mandatory | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") | <font color="red">Name of Professional recording the observation</font> |
|  - valueQuantity | 0..1 | Required | Quantity | Actual result<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/>Binding (required): Common UCUM units for recording Vital Signs ( http://hl7.org/fhir/stu3/valueset-ucum-vitals-common.html ) |
|  - - value | 1..1 | Mandatory | Decimal | Numerical value (with implicit precision) |
|  - - unit | 1..1 | Mandatory | String | Unit representation |
|  - - system | 1..1 | Mandatory | Uri | System that defines coded unit form<br/>Fixed Value: http://unitsofmeasure.org |
|  - - code | 1..1 | Mandatory | Code | Coded form of the unit<br/>Fixed Value: g |

## Mapping for Length Observation ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/Observation.html)|>|Level 2|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|>|Level 3|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_observations_all.html#mapping-for-blood-pressure-observation-details)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  Observation | ​ |  |  | Measurements and simple assertions<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (obs-7): If code is the same as a component code then the value element associated with the code SHALL NOT be present<br/>Constraint (obs-6): dataAbsentReason SHALL only be present if Observation.value[x] is not present |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Observation-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business Identifier for observation<br/><font color='red'>An identifier for this Observation</font> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - - assigner | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | registered : preliminary : final : amended +<br/>Binding (required): Codes providing the status of an observation. [ObservationStatus](http://hl7.org/fhir/stu3/valueset-observation-status.html) |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of observation (code / type)<br/><font color="red">Weight Observation</font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system describing a type of observation [CareConnect-ObservationType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ObservationType-1) |
|  - - - extension (snomedCTDescriptionID) | 0..1 | Required | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | The SNOMED CT Description ID for the display.<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color="red">SNOMED CT code 50373000</font> |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color="red">MUST be 'Body height measure')</font> |
|  - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who and/or what this is about<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|  - - identifier | 0..1 | Mandatory | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - effective[x] | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Clinically relevant time/time-period for observation<br/><font color="red">The date/time the obsrvation was recorded</font><br/> |
|  - performer | 0..* | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who is responsible for the observation<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") | <font color="red">The Site Code of where the obsrvation was recorded</font> |
|   |  | Mandatory | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") | <font color="red">Name of Professional recording the observation</font> |
|  - valueQuantity | 0..1 | Required | Quantity | Actual result<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/>Binding (required): Common UCUM units for recording Vital Signs ( http://hl7.org/fhir/stu3/valueset-ucum-vitals-common.html ) |
|  - - value | 1..1 | Mandatory | Decimal | Numerical value (with implicit precision) |
|  - - unit | 1..1 | Mandatory | String | Unit representation |
|  - - system | 1..1 | Mandatory | Uri | System that defines coded unit form<br/>Fixed Value: http://unitsofmeasure.org |
|  - - code | 1..1 | Mandatory | Code | Coded form of the unit<br/>Fixed Value: cm |

## Mapping for BMI Observation ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/Observation.html)|>|Level 2|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|>|Level 3|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_observations_all.html#mapping-for-blood-pressure-observation-details)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  Observation | ​ |  |  | Measurements and simple assertions<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (obs-7): If code is the same as a component code then the value element associated with the code SHALL NOT be present<br/>Constraint (obs-6): dataAbsentReason SHALL only be present if Observation.value[x] is not present |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Observation-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business Identifier for observation<br/><font color='red'>An identifier for this Observation</font> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - - assigner | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | registered : preliminary : final : amended +<br/>Binding (required): Codes providing the status of an observation. [ObservationStatus](http://hl7.org/fhir/stu3/valueset-observation-status.html) |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of observation (code / type)<br/><font color="red">Weight Observation</font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system describing a type of observation [CareConnect-ObservationType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ObservationType-1) |
|  - - - extension (snomedCTDescriptionID) | 0..1 | Required | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | The SNOMED CT Description ID for the display.<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color="red">SNOMED CT code 60621009</font> |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color="red">MUST be 'Body mass index')</font> |
|  - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who and/or what this is about<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|  - - identifier | 0..1 | Mandatory | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - effective[x] | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Clinically relevant time/time-period for observation<br/><font color="red">The date/time the obsrvation was recorded</font><br/> |
|  - performer | 0..* | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who is responsible for the observation<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") | <font color="red">The Site Code of where the obsrvation was recorded</font> |
|   |  | Mandatory | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") | <font color="red">Name of Professional recording the observation</font> |
|  - valueQuantity | 0..1 | Required | Quantity | Actual result<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/>Binding (required): Common UCUM units for recording Vital Signs ( http://hl7.org/fhir/stu3/valueset-ucum-vitals-common.html ) |
|  - - value | 1..1 | Mandatory | Decimal | Numerical value (with implicit precision) |
|  - - unit | 1..1 | Mandatory | String | Unit representation |
|  - - system | 1..1 | Mandatory | Uri | System that defines coded unit form<br/>Fixed Value: http://unitsofmeasure.org |
|  - - code | 1..1 | Mandatory | Code | Coded form of the unit<br/>Fixed Value: cm |

## Mapping for Blood Pressure Observation Details ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/Observation.html)|>|Level 2|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|>|Level 3|[CareConnect-BloodPressure-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-BloodPressure-Observation-1)|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_observations_all.html#mapping-for-blood-pressure-observation-details)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-BloodPressure-Observation-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business Identifier for observation<br/><font color='red'>An identifier for this Observation</font> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - - assigner | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | registered : preliminary : final : amended +<br/>Binding (required): Codes providing the status of an observation. [ObservationStatus](http://hl7.org/fhir/stu3/valueset-observation-status.html) |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of observation (code / type)<br/><font color="red">Type of Observation performed</font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system describing a type of observation [CareConnect-ObservationType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ObservationType-1) |
|  - - - extension (snomedCTDescriptionID) | 0..1 | Required | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | The SNOMED CT Description ID for the display.<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color="red">MUSt contain code '75367002'</font> |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color="red">MUST be 'Blood pressure'</font> |
|  - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who and/or what this is about<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|  - - identifier | 0..1 | Mandatory | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - effective[x] | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Clinically relevant time/time-period for observation<br/><font color="red">The date on which the observation was recorded</font><br/> |
|  - performer | 0..* | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who is responsible for the observation<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color="red">Name of the professional performing the observation</font> |
|   |  | Required | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") | <font color="red">Name of Professional recording the observation</font> |
|  - component | 0..* | Required | BackboneElement | Used when reporting systolic and diastolic blood pressure.<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - code | 1..1 | Mandatory | CodeableConcept | Type of component observation (code / type)<br/>Slice discriminator: Code<br/>Binding (extensible): Codes identifying names of simple observations. ( http://hl7.org/fhir/stu3/valueset-observation-vitalsignresult.html ) |
|  - - - - system | 1..1 | Mandatory | Uri | Identity of the terminology system<br/>Fixed Value: <http://loinc.org> |
|  - - - - code | 1..1 | Mandatory | Code | Symbol in syntax defined by the system<br/>Binding (extensible): http://hl7.org/fhir/stu3/valueset-observation-vitalsignresult.html |
|  - component (systolicComponent) | 0..* | Required | BackboneElement | Component results |
|  - - code | 1..1 | Mandatory | CodeableConcept | Type of component observation (code / type)<br/>Binding (extensible): This value set indicates the allowed vital sign result types. (http://hl7.org/fhir/stu3/valueset-observation-vitalsignresult.html ) |
|  - - - coding | 0..* | Required | Coding | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - - coding (loinc) | 1..1 | Mandatory | Coding | Systolic Blood Pressure |
|  - - - - system | 1..1 | Mandatory | Uri | Identity of the terminology system<br/>Fixed Value: http://loinc.org |
|  - - - coding (snomedCT) | 1..1 | Mandatory | Coding | Systolic Blood Pressure |
|  - - - - system | 1..1 | Mandatory | Uri | Identity of the terminology system<br/>Fixed Value: http://snomed.info/sct |
|  - - - - code | 1..1 | Mandatory | Code | Symbol in syntax defined by the system<br/>Fixed Value: 72313002 |
|  - - - - display | 1..1 | Mandatory | String | Representation defined by the system<br/>Fixed Value: Systolic arterial pressure |
|  - - - value | 1..1 | Mandatory | Decimal | Numerical value (with implicit precision) |
|  - - - unit | 1..1 | Mandatory | String | Unit representation |
|  - - - system | 1..1 | Mandatory | Uri | System that defines coded unit form<br/>Fixed Value: http://unitsofmeasure.org |
|  - - - code | 1..1 | Mandatory | Code | Coded responses from the common UCUM units for vital signs value set.<br/>Fixed Value: mm[Hg] |
|  - - component (diastolicComponent) | 0..* | Required | BackboneElement | Component results |
|  - - code | 1..1 | Mandatory | CodeableConcept | Type of component observation (code / type)<br/>Binding (example): Codes identifying names of simple observations. ( http://hl7.org/fhir/stu3/valueset-observation-codes.html ) |
|  - - - coding | 0..* | Required | Coding | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - - coding (loinc) | 1..1 | Mandatory | Coding | Diastolic Blood Pressure |
|  - - - - system | 1..1 | Mandatory | Uri | Identity of the terminology system<br/>Fixed Value: http://loinc.org |
|  - - - - code | 1..1 | Mandatory | Code | Symbol in syntax defined by the system<br/>Fixed Value: 8462-4 |
|  - - - coding (snomedCT) | 1..1 | Mandatory | Coding | Diastolic Blood Pressure |
|  - - - - system | 1..1 | Mandatory | Uri | Identity of the terminology system<br/>Fixed Value: http://snomed.info/sct |
|  - - - - code | 1..1 | Mandatory | Code | Symbol in syntax defined by the system<br/>Fixed Value: 1091811000000102 |
|  - - - - display | 1..1 | Mandatory | String | Representation defined by the system<br/>Fixed Value: Diastolic arterial pressure |
|  - - - value | 1..1 | Mandatory | Decimal | Numerical value (with implicit precision) |
|  - - - unit | 1..1 | Mandatory | String | Unit representation |
|  - - - system | 1..1 | Mandatory | Uri | System that defines coded unit form<br/>Fixed Value: http://unitsofmeasure.org |
|  - - - code | 1..1 | Mandatory | Code | Coded responses from the common UCUM units for vital signs value set.<br/>Fixed Value: mm[Hg] |


## Mapping for Heart Rate Observation ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/Observation.html)|>|Level 2|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|>|Level 3|[CareConnect-BloodPressure-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-HeartRate-Observation-1)|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_observations_all.html#mapping-for-heart-rate-observation-details)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-HeartRate-Observation-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business Identifier for observation<br/><font color='red'>An identifier for this Observation</font> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - - assigner | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | registered : preliminary : final : amended +<br/>Binding (required): Codes providing the status of an observation. [ObservationStatus](http://hl7.org/fhir/stu3/valueset-observation-status.html) |
|  - code | 1..1 | Mandatory | CodeableConcept | Type of observation (code / type)<br/>Binding (extensible): This value set indicates the allowed vital sign result types. (http://hl7.org/fhir/stu3/valueset-observation-vitalsignresult.html ) |
|   - -coding | 1..* | Mandatory | Coding | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (loinc) | 1..1 | Mandatory | Coding | Code defined by a terminology system<br/>Binding (extensible): This value set indicates the allowed vital sign result types (http://hl7.org/fhir/stu3/valueset-observation-vitalsignresult.html ) |
|  - - - system | 1..1 | Mandatory | Uri | Identity of the terminology system<br/>Fixed Value: http://loinc.org |
|  - - - code | 1..1 | Mandatory | Code | Symbol in syntax defined by the system<br/>Fixed Value: 8867-4 |
|  - - coding (snomedCT) | 1..1 | Mandatory | Coding | Code defined by a terminology system |
|  - - - system | 1..1 | Mandatory | Uri | Identity of the terminology system<br/>Fixed Value: http://snomed.info/sct |
|  - - - code | 1..1 | Mandatory | Code | Symbol in syntax defined by the system<br/>Fixed Value: 75367002 |
|  - - - display | 0..1 | Required | Representation defined by the system<br/>Fixed Value: Blood pressure|
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who and/or what this is about<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|  - - identifier | 0..1 | Mandatory | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - effective[x] | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Clinically relevant time/time-period for observation<br/><font color="red">The date on which the observation was recorded</font><br/> |
|  - performer | 0..* | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who is responsible for the observation<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color="red">Name of the professional performing the observation</font> |
|   |  | Required | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") | <font color="red">Name of Professional recording the observation</font> |
|  - valueQuantity | 0..1 | Required | Quantity | Actual result<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/>Binding (required): Common UCUM units for recording Vital Signs ( http://hl7.org/fhir/stu3/valueset-ucum-vitals-common.html ) |
|  - - value | 1..1 | Mandatory | Decimal | Numerical value (with implicit precision) |
|  - - unit | 1..1 | Mandatory | String | Unit representation |
|  - - system | 1..1 | Mandatory | Uri | System that defines coded unit form<br/>Fixed Value: http://unitsofmeasure.org |
|  - - code | 1..1 | Mandatory | Code | Coded responses from the common UCUM units for vital signs value set.<br/>Fixed Value: /min |

## Mapping for Body Temperature Observation ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/Observation.html)|>|Level 2|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|>|Level 3|[CareConnect-BodyTemperature-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-BodyTemperature-Observation-1)|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_observations_all.html#mapping-for-heart-rate-observation-details)**|


|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-BodyTemperature-Observation-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business Identifier for observation<br/><font color='red'>An identifier for this Observation</font> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - - assigner | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | registered : preliminary : final : amended +<br/>Binding (required): Codes providing the status of an observation. [ObservationStatus](http://hl7.org/fhir/stu3/valueset-observation-status.html) |
|  - code | 1..1 | Mandatory | CodeableConcept | Type of observation (code / type)<br/>Binding (extensible): This value set indicates the allowed vital sign result types. (http://hl7.org/fhir/stu3/valueset-observation-vitalsignresult.html ) |
|   - -coding | 1..* | Mandatory | Coding | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (loinc) | 1..1 | Mandatory | Coding | Code defined by a terminology system<br/>Binding (extensible): This value set indicates the allowed vital sign result types (http://hl7.org/fhir/stu3/valueset-observation-vitalsignresult.html ) |
|  - - - system | 1..1 | Mandatory | Uri | Identity of the terminology system<br/>Fixed Value: http://loinc.org |
|  - - - code | 1..1 | Mandatory | Code | Symbol in syntax defined by the system<br/>Fixed Value: 8310-5 |
|  - - - display | 0..1 | Required | String | Representation defined by the system<br/>Fixed Value: Core body temperature |
|  - - coding (snomedCT) | 1..1 | Mandatory | Coding | Code defined by a terminology system |
|  - - - system | 1..1 | Mandatory | Uri | Identity of the terminology system<br/>Fixed Value: http://snomed.info/sct |
|  - - - code | 1..1 | Mandatory | Code | Symbol in syntax defined by the system<br/>Fixed Value: 276885007 |
|  - - - display | 1..1 | Required | String | Representation defined by the system<br/>Fixed Value: Blood pressure |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who and/or what this is about<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|  - - identifier | 0..1 | Mandatory | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - effective[x] | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Clinically relevant time/time-period for observation<br/><font color="red">The date on which the observation was recorded</font><br/> |
|  - performer | 0..* | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who is responsible for the observation<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color="red">Name of the professional performing the observation</font> |
|   |  | Required | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") | <font color="red">Name of Professional recording the observation</font> |
|  - valueQuantity | 0..1 | Required | Quantity | Actual result<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/>Binding (required): Common UCUM units for recording Vital Signs ( http://hl7.org/fhir/stu3/valueset-ucum-vitals-common.html ) |
|  - - value | 1..1 | Mandatory | Decimal | Numerical value (with implicit precision) |
|  - - unit | 1..1 | Mandatory | String | Unit representation |
|  - - system | 1..1 | Mandatory | Uri | System that defines coded unit form<br/>Fixed Value: http://unitsofmeasure.org |
|  - - code | 1..1 | Mandatory | Code | Coded responses from the common UCUM units for vital signs value set.<br/>Fixed Value: Cel<br/>Binding (required): UCUM units for recording Body Temperature ( [http://hl7.org/fhir/stu3/valueset-ucum-bodytemp.html](http://hl7.org/fhir/stu3/valueset-ucum-bodytemp.html) ) |

## Mapping for Oxygen Saturation ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/Observation.html)|>|Level 2|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|>|Level 3|[CareConnect-OxygenSaturation-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-OxygenSaturation-Observation-1)|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_observations_all.html#mapping-for-heart-rate-observation-details)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-OxygenSaturation-Observation-1'<br/>'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business Identifier for observation<br/><font color='red'>An identifier for this Observation</font> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - - assigner | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | registered : preliminary : final : amended +<br/>Binding (required): Codes providing the status of an observation. [ObservationStatus](http://hl7.org/fhir/stu3/valueset-observation-status.html) |
|  - code | 1..1 | Mandatory | CodeableConcept | Type of observation (code / type)<br/>Binding (extensible): This value set indicates the allowed vital sign result types. (http://hl7.org/fhir/stu3/valueset-observation-vitalsignresult.html ) |
|   - -coding | 1..* | Mandatory | Coding | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (loinc) | 1..1 | Mandatory | Coding | Code defined by a terminology system<br/>Binding (extensible): This value set indicates the allowed vital sign result types (http://hl7.org/fhir/stu3/valueset-observation-vitalsignresult.html ) |
|  - - - system | 1..1 | Mandatory | Uri | Identity of the terminology system<br/>Fixed Value: http://loinc.org |
|  - - - code | 1..1 | Mandatory | Code | Symbol in syntax defined by the system<br/>Fixed Value: 59408-5 |
|  - - - display | 0..1 | Not Used | String | Representation defined by the system<br/>Fixed Value: Core body temperature |
|  - - coding (snomedCT) | 1..1 | Mandatory | Coding | Code defined by a terminology system |
|  - - - system | 1..1 | Mandatory | Uri | Identity of the terminology system<br/>Fixed Value: http://snomed.info/sct |
|  - - - code | 1..1 | Mandatory | Code | Symbol in syntax defined by the system<br/>Fixed Value: 103228002 |
|  - - - display | 1..1 | Required | String | Representation defined by the system<br/>Fixed Value: Blood oxygen saturation |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who and/or what this is about<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|  - - identifier | 0..1 | Mandatory | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - effective[x] | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Clinically relevant time/time-period for observation<br/><font color="red">The date on which the observation was recorded</font><br/> |
|  - performer | 0..* | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who is responsible for the observation<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color="red">Name of the professional performing the observation</font> |
|   |  | Required | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") | <font color="red">Name of Professional recording the observation</font> |
|  - valueQuantity | 0..1 | Required | Quantity | Actual result<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/>Binding (required): Common UCUM units for recording Vital Signs ( http://hl7.org/fhir/stu3/valueset-ucum-vitals-common.html ) |
|  - - value | 1..1 | Mandatory | Decimal | Numerical value (with implicit precision) |
|  - - unit | 1..1 | Mandatory | String | Unit representation |
|  - - system | 1..1 | Mandatory | Uri | System that defines coded unit form<br/>Fixed Value: http://unitsofmeasure.org |
|  - - code | 1..1 | Mandatory | Code | Coded form of the unit<br/>Fixed Value: % |

## Mapping for Respiratory Observation ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/Observation.html)|>|Level 2|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-RespiratoryRate-Observation-1)|>|Level 3|[CareConnect-BloodPressure-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-RespiratoryRate-Observation-1)|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_observations_all.html#mapping-for-heart-rate-observation-details)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-RespiratoryRate-Observation-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business Identifier for observation<br/><font color='red'>An identifier for this Observation</font> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - - assigner | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | registered : preliminary : final : amended +<br/>Binding (required): Codes providing the status of an observation. [ObservationStatus](http://hl7.org/fhir/stu3/valueset-observation-status.html) |
|  - code | 1..1 | Mandatory | CodeableConcept | Type of observation (code / type)<br/>Binding (extensible): This value set indicates the allowed vital sign result types. (http://hl7.org/fhir/stu3/valueset-observation-vitalsignresult.html ) |
|   - -coding | 1..* | Mandatory | Coding | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (loinc) | 1..1 | Mandatory | Coding | Code defined by a terminology system<br/>Binding (extensible): This value set indicates the allowed vital sign result types (http://hl7.org/fhir/stu3/valueset-observation-vitalsignresult.html ) |
|  - - - system | 1..1 | Mandatory | Uri | Identity of the terminology system<br/>Fixed Value: http://loinc.org |
|  - - - code | 1..1 | Mandatory | Code | Symbol in syntax defined by the system<br/>Fixed Value: 9279-1 |
|  - - - display | 0..1 | Not Used | String | Representation defined by the system<br/>Fixed Value: Core body temperature |
|  - - coding (snomedCT) | 1..1 | Mandatory | Coding | Code defined by a terminology system |
|  - - - system | 1..1 | Mandatory | Uri | Identity of the terminology system<br/>Fixed Value: http://snomed.info/sct |
|  - - - code | 1..1 | Mandatory | Code | Symbol in syntax defined by the system<br/>Fixed Value: 86290005 |
|  - - - display | 1..1 | Required | String | Representation defined by the system<br/>Fixed Value: Respiratory rate |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who and/or what this is about<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|  - - identifier | 0..1 | Mandatory | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - effective[x] | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Clinically relevant time/time-period for observation<br/><font color="red">The date on which the observation was recorded</font><br/> |
|  - performer | 0..* | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who is responsible for the observation<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color="red">Name of the professional performing the observation</font> |
|   |  | Required | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") | <font color="red">Name of Professional recording the observation</font> |
|  - valueQuantity | 0..1 | Required | Quantity | Actual result<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/>Binding (required): Common UCUM units for recording Vital Signs ( http://hl7.org/fhir/stu3/valueset-ucum-vitals-common.html ) |
|  - - value | 1..1 | Mandatory | Decimal | Numerical value (with implicit precision) |
|  - - unit | 1..1 | Mandatory | String | Unit representation |
|  - - system | 1..1 | Mandatory | Uri | System that defines coded unit form<br/>Fixed Value: http://unitsofmeasure.org |
|  - - code | 1..1 | Mandatory | Code | Coded responses from the common UCUM units for vital signs value set.<br/>Fixed Value: /min<br/>Binding (required): UCUM units for recording Body Temperature ( [http://hl7.org/fhir/stu3/valueset-ucum-bodytemp.html](http://hl7.org/fhir/stu3/valueset-ucum-bodytemp.html) ) |


## Mapping for Observation Encounter ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/encounter.html)|>|Level 2|[CareConnect-Encounter-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)|>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_observations_all.html#mapping-for-observation-encounter)**|

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
|  - - location | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Location the encounter takes place<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>Where the observation took place</font> |
|   |  | Mandatory | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") | This MUST use the CareConnect Location profile. </font>See [Location resource](explore_observations.html#mapping-for-observation-location) for information on how to populate the resource. |
|  - - - reference | 0..1 | Required | String | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the Location resource included in the observation details list</font>  |

## Mapping for Plan and Requested Actions Practitioner ## 

The plan and requested actions details has reference(s) to the Practitioner resource. This means that any exchange of the plan and requested actions details heading data must also include the [Practitioner Details](explore_practitioner.html#mapping-for-practitioner)

## Mapping for Plan and Requested Actions PractitionerRole ##  

The plan and requested actions details has reference(s) to the Practitioner Role resource. This means that any exchange of the plan and requested actions details heading data must also include the [Practitioner Role Details](explore_practitioner_role.html#mapping-for-practitioner_role)

## Mapping for Observation Location ##

The observations details has reference(s) to the Location resource. This means that any exchange of the observations details heading data must also include the [Location Details](explore_location.html#mapping-for-location)

## Example of Observation ##

<script src="https://gist.github.com/IOPS-DEV/e52540c784cd9e23625f696dd56b3621.js"></script>
