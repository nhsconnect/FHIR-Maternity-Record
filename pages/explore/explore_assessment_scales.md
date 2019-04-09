---
title: Assessment Scales List
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_assessment_scales.html
summary: "The FHIR profiles used for the Assessment Scales List structure"
---


## Heading Description ##
Details of the woman’s assessment scales.

The following FHIR profiles are used to form the Assessment scales list structure:

- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)
- [CareConnect-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)
- [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)

The following profiles are referenced from the Assessment scales list structure:

- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)

## Assessment Scales Structure ##

{% include custom/assessment_scales.svg %}

## Maternity Data Standard Mapping to FHIR profiles ##

## Mapping Overview ##

|**Data Standard Element**|**FHIR Profile**|**FHIR target**|
|Date/Time Recorded|[List](explore_assessment_scales.html#mapping-for-assessment-scales-list)|entry.date|
|ODS/ORD Site Code|[Location](explore_assessment_scales.html#mapping-for-assessment-scales-location)|identifier|
|Performing Professional|[Practitioner](explore_assessment_scales.html#mapping-for-assessment-scales-practitioner)|name|
|SDS Job Role Name|[PractitionerRole](explore_assessment_scales.html#mapping-for-assessment-scales-practitionerRole)|code|
|Coded Assessment Tool Type|[Observation](explore_assessment_scales.html#mapping-for-assessment-scales-observation)|code<br/>value<br/>component.code<br/>component.value|
|Comment|[Observation](explore_assessment_scales.html#mapping-for-assessment-scales-observation)|comment|

## Mapping for Assessment Scales List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_assessment_scales_all.html#mapping-for-assessment-scales-list)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  List | ​ |  |  | Information summarized from a list of other resources<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (lst-2): The deleted flag can only be used if the mode of the list is "changes"<br/>Constraint (lst-1): A list can only have an emptyReason if it is empty |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-List-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business identifier<br/><font color='red'>An identifier for this Assessment scales</font><br/> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique<br/>Business identifier<br/><font color='red'>An identifier for this Assessment scales list</font> |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource<br/><font color='red'>The organization that allocated the identifier</font> |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | current : retired : entered-in-error<br/>Binding (required): The current state of the list [ListStatus](http://hl7.org/fhir/stu3/valueset-list-status.html)<br/><font color='red'>The status of the list MUST contain the value 'current'</font> |
|  - mode | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | working : snapshot : changes<br/>Binding (required): The processing mode that applies to this list [ListMode](http://hl7.org/fhir/stu3/valueset-list-mode.html)<br/><font color='red'>The mode of the list MUST contain the value 'snapshot'</font> |
|  - title | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Descriptive name for the list<br/><font color='red'>This MUST contain the value 'Assessment scales'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading Assessment scales'</b></font>  |
|  - code | 0..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | What the purpose of this list is<br/>Binding (preferred): What the purpose of a list is [CareConnect-ListCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListCode-1)<br/><font color='red'>The PRSB heading for this list. Note: for Maternity the value stated below is used which is not from the preferred value set </font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/><font color='red'>The SNOMED CT concept for the PRSB heading type</font> |
|  - - - system | 0..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value '887141000000103'</font> |
|  - - - display | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>This MUST contain the value 'Assessment scales'</font><br/><font color='red'>Mapping to Maternity data item = 'PSRB Heading Assessment scales'</font>  |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color='red'>This is the subject of the Assessment scales List.<br/>This MUST use the CareConnect patient profile. </font>See [patient resource reference](explore_assessment_scales.html#patient-reference) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - date | 0..1 | Mandatory | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the list was prepared<br/><font color='red'> This MUST contain a system date to indicate when the list created or updated</font><font color='red'><b>Mapping to Maternity data item = 'Date/Time Recorded'</b></font> |
|  - note | 0..* | Optional | [Annotation](http://hl7.org/fhir/stu3/datatypes.html#annotation "Annotation") | Comments about the list |
|   |  | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | <font color='red'>Who authored the comment on the list.</font>  |
|  - - time | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the annotation was made |
|  - - text | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The annotation - text content |
|  - entry | 0..* | Mandatory | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Entries in the list<br/><font color='red'>The entries MUST be as per the diagram for this PRSB headings list with the Observation resource being the focal resource. Multiple resources MAY be present</font> |
|  - - date | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When item added to list<br/><font color='red'>The SHOULD contain a system time of when the item was added to the list.</font> |
|  - - item | 1..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>A reference to an Observation resource included in the list<br/>This MUST use the CareConnect Observation profile. </font>See [Observation resource](explore_assessment_scales.html#mapping-for-assessment-scales-observation) for information on how to populate the resource. |
|  - - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>The reference to the included Observation resource.</font> |


## Mapping for Assessment Scales Observation ##

|>|Level 1|[Observation Resource](http://hl7.org/fhir/stu3/observation.html)|>|Level 2|[CareConnect-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_assessment_scales_all.html#mapping-for-assessment-scales-observation)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for  Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  Observation | ​ |  |  | Measurements and simple assertions<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (obs-7): If code is the same as a component code then the value element associated with the code SHALL NOT be present<br/>Constraint (obs-6): dataAbsentReason SHALL only be present if Observation.value[x] is not present |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Observation-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business Identifier for observation<br/><font color='red'>An identifier for this Assessment scales observation</font> |
|  - - - text | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - - assigner | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | registered : preliminary : final : amended +<br/>Binding (required): Codes providing the status of an observation. [ObservationStatus](http://hl7.org/fhir/stu3/valueset-observation-status.html)<br/><font color='red'>MUST contain the value 'final'.</font> |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of observation (code / type)<br/>Binding (example): Codes identifying names of simple observations. [LOINC Codes](http://hl7.org/fhir/stu3/valueset-observation-codes.html)<br/><font color='red'>This example valueSet is not used by Maternity record. The following SNOMED reference is used</font> [Assessment scale observables simple reference set](https://termbrowser.nhs.uk/?perspective=full&conceptId1=999002331000000109&edition=uk-edition&server=https://termbrowser.dataproducts.nhs.uk/sct-browser-api/snomed&langRefset=999001261000000100,999000691000001104)<br/><font color='red'><b>Mapping to Maternity data item = 'Coded Assessment Tool Type'</b></font> |
|  - - coding | 0..* | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system describing a type of observation [CareConnect-ObservationType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ObservationType-1)<br/><font color='red'>This SNOMED valueSet SHOULD be constrained to the valueSet as indicated in the code element above.</font> |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>A SNOMED concept from the valueSet indicated.</font> |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>The display associated with the SNOMED CT concept. This SHOULD be the preferred term</font>  |
|  - context | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Healthcare event during which this observation is made<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This MUST be a reference to  Encounter resource</font> |
|   |  | Required | [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1 "CareConnect-Encounter-1") | <font color='red'>The Encounter where the assesment was carried out.<br/>This MUST use the Encounter resource. </font>See [Encounter resource](explore_assessment_scales.html#mapping-for-assessment-scales-encounter) for information on how to populate the resource. |
|  - - reference | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the Encounter resource included in the Assessment scales list</font> |
|  - effective[x] | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Clinically relevant time/time-period for observation<br/><font color='red'>The date on which the assessment scale was recorded.</font> |
|  - performer | 0..* | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who is responsible for the observation<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>The professional performing the assessment scale. </font> |
|   |  | Mandatory | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") | <font color='red'>The professional performing the Assessment. This MUST use the Practitioner resource.</font>See [Practitioner resource](explore_assessment_scales.html#mapping-for-assessment-scales-practitioner) for information on how to populate the resource." |
|  - - reference | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the Practitioner resource included in the Assessment scales list</font> |
|  - value[x] | 0..1 | Required | [Quantity](http://hl7.org/fhir/stu3/datatypes.html#quantity "Quantity") | Actual result<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/><font color='red'>The value of the assessment scales where one is required to recorded.</font> |
|   |  | Required | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") |  |
|   |  | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") |  |
|   |  | Required | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") |  |
|   |  | Required | [Range](http://hl7.org/fhir/stu3/datatypes.html#range "Range") |  |
|  - comment | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Comments about result<br/><font color='red'>Supporting text may be given regarding the assessment scale as a whole or a subscale. code.text and component.code.text SHOULD be used when the scale cannot be coded using SNOMED, value.string and component.value.string should be used for the values where no suitable data type is available or applicable.</font> |
|  - component | 0..* | Required | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Component results. <font color='red'>Component Assessment scales</font><br/> |
|  - - code | 1..1 | Required | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of component observation (code / type)<br/>Binding (example): Codes identifying names of simple observations. [LOINC Codes](http://hl7.org/fhir/stu3/valueset-observation-codes.html)<br/><font color='red'>This example valueSet is not used by Maternity record. The following SNOMED reference is used </font> [Assessment scale observables simple reference set](https://termbrowser.nhs.uk/?perspective=full&conceptId1=999002331000000109&edition=uk-edition&server=https://termbrowser.dataproducts.nhs.uk/sct-browser-api/snomed&langRefset=999001261000000100,999000691000001104)<br/><font color='red'><b>Mapping to Maternity data item = 'Coded Assessment Tool Type'</b></font |
|  - - coding | 0..* | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system describing a type of observation [CareConnect-ObservationType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ObservationType-1)<br/><font color='red'>This SNOMED valueSet SHOULD be constrained to the valueSet as indicated in the code element above.</font> |
|  - - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Required | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | "Symbol in syntax defined by the system<br/><font color='red'>A SNOMED concept from the valueSet indicated.</font>" |
|  - - - display | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><br/><font color='red'>The display associated with the SNOMED CT concept. This SHOULD be the preferred term</font>  |
|  - value[x] | 0..1 | Required | [Quantity](http://hl7.org/fhir/stu3/datatypes.html#quantity "Quantity") | Actual component result<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/><font color='red'>The value of the assessment scales where one is required to recorded.</font> |
|   |  | Required | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") |  |
|   |  | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") |  |
|   |  | Required | [Range](http://hl7.org/fhir/stu3/datatypes.html#range "Range") |  |



## Mapping for Assessment Scales Encounter ##

|>|Level 1|[Encounter Resource](http://hl7.org/fhir/stu3/encounter.html)|>|Level 2|[CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_assessment_scales_all.html#mapping-for-assessment-scales-encounter)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  Encounter | ​ |  |  | An interaction during which services are provided to the patient<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Encounter-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Identifier(s) by which this encounter is known<br/><font color='red'>An identifier for this Encounter</font> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique<br/><font color='red'>An identifier for this Assessment scales encounter</font> |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | planned : arrived : triaged : in-progress : onleave : finished : cancelled +<br/>Binding (required): Current state of the encounter [EncounterStatus](http://hl7.org/fhir/stu3/valueset-encounter-status.html)<br/><font color='red'>The status of the Encounter MUST contain the value 'finished'</font> |
|  - location | 0..1 | Required | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | List of locations where the patient has been |
|  - - location | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Location the encounter takes place<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>The site code of the unit to which the person was admitted</font> |
|   |  | Mandatory | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") | "<font color='red'>The location<br/>This MUST use the CareConnect Location profile. </font>See [Location resource](explore_assessment_scales.html#mapping-for-assessment-scales-location) for information on how to populate the resource." |
|  - - - reference | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the Location resource included in the Assessment scales list</font>  |


## Patient Reference ##

The Admission details list has a mandated subject reference to the Patient resource. This means that any exchange of the Admission details heading data must also include the [Patient demographics List.](explore_patient_demographics.html)


## Mapping for Assessment Scales Location ##

|>|Level 1|[Location Resource](http://hl7.org/fhir/stu3/location.html)|>|Level 2|[CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_assessment_scales_all.html#mapping-for-assessment-scales-location)**|

## Mapping for Assessment Scales Practitioner ##

|>|Level 1|[Practitioner Resource](http://hl7.org/fhir/stu3/practitioner.html)|>|Level 2|[CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_assessment_scales_all.html#mapping-for-assessment-scales-practitioner)**|

## Mapping for Assessment Scales PracitionerRole ##

|>|Level 1|[PractitionerRole Resource](http://hl7.org/fhir/stu3/practitionerRole.html)|>|Level 2|[CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_assessment_scales_all.html#mapping-for-assessment-scales-practitionerRole)**|