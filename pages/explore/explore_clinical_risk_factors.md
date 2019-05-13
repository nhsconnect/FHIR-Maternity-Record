---
title: Clinical Risk Factors List
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_clinical_risk_factors.html
summary: "The FHIR profiles used for the Clinical risk factors List"
---
## Heading Description ##
Details of clinical risk factors to the woman, foetus or child after birth’.

The following FHIR profiles are used to form the Clinical risk factors list structure:

- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)
- [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)
- [CareConnect-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-RiskAssessemnt-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-RiskAssessment-1)

The following profiles are referenced from the Clinical risk factors list structure:

- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)

## Clinical Risk Factors Structure ##

{% include custom/clinical_risk_factors.svg %}

## Maternity Data Standard Mapping to FHIR profiles ##

## Mapping Overview ##


|**Data Standard Element**|**FHIR Profile Mapping**|**FHIR Element**|
|Date/Time|[RiskAssessement](explore_clinical_risk_factors.html#mapping-for-clinical-risk-factors-list)|period|
|ODS/ORD Site Code|[Location](explore_clinical_risk_factors.html#mapping-for-clinical-risk-factors-location)|identifier|
|SDS Job Role Name|[PractitionerRole](explore_clinical_risk_factors.html#mapping-for-clinical-risk-factors-practitionerrole)|identifier|
|Professional Name|[Practitioner](explore_clinical_risk_factors.html#mapping-for-clinical-risk-factors-practitioner)|name|
|Relevant Clinical Risk Factor|[Observation](explore_clinical_risk_factors.html#mapping-for-clinical-risk-factors-observation)|code|
|Clinical Risk Assessment|[RiskAssessment](explore_clinical_risk_factors.html#mapping-for-clinical-risk-factors-riskassessment)|method|
|Risk Mitigation|[RiskAssessment](explore_clinical_risk_factors.html#mapping-for-clinical-risk-factors-riskassessment)|mitigation.string|


## Mapping for Clinical Risk Factors List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_clinical_risk_factors_all.html#mapping-for-clinical-risk-factors-list)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  List | ​ |  |  | Information summarized from a list of other resources<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (lst-2): The deleted flag can only be used if the mode of the list is "changes"<br/>Constraint (lst-1): A list can only have an emptyReason if it is empty |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business identifier<br/><font color='red'>An identifier for this Clinical risk factors list</font><br/> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique<br/>Business identifier<br/><font color='red'>An identifier for this Clinical risk factors list</font> |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource<br/><font color='red'>The organization that allocated the identifier</font> |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | current : retired : entered-in-error<br/>Binding (required): The current state of the list [ListStatus](http://hl7.org/fhir/stu3/valueset-list-status.html)<br/><font color='red'>The status of the list MUST contain the value 'current'</font> |
|  - mode | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | working : snapshot : changes<br/>Binding (required): The processing mode that applies to this list [ListMode](http://hl7.org/fhir/stu3/valueset-list-mode.html)<br/><font color='red'>The mode of the list MUST contain the value 'snapshot'</font> |
|  - title | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Descriptive name for the list<br/><font color='red'>This MUST contain the value 'Clinical risk factors'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading Clinical Risk Factors'</b></font>  |
|  - code | 0..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | What the purpose of this list is<br/>Binding (preferred): What the purpose of a list is [CareConnect-ListCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListCode-1)<br/><font color='red'>The PRSB heading for this list. Note: for Maternity the value stated below is used which is not from the preferred value set </font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/><font color='red'>The SNOMED CT concept for the PRSB heading type</font> |
|  - - - system | 0..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value '886831000000103'</font> |
|  - - - display | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>This MUST contain the value 'Clinical risk factors'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading Clinical risk factors'</b></font>  |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color='red'>This is the subject of the Clinical risk factors List.<br/>This MUST use the CareConnect patient profile. </font>See [patient resource reference](explore_clinical_risk_factors.html#patient-reference) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - date | 0..1 | Mandatory | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the list was prepared<br/><font color='red'> This MUST contain a system date to indicate when the list was created or updated</font> |
|  - note | 0..* | Optional | [Annotation](http://hl7.org/fhir/stu3/datatypes.html#annotation "Annotation") | Comments about the list |
|   |  | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | <font color='red'>Who authored the comment on the list.</font>  |
|  - - time | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the annotation was made |
|  - - text | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The annotation - text content |
|  - entry | 0..* | Mandatory | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Entries in the list<br/><font color='red'>The entries MUST be as per the diagram for this PRSB headings list with the Encounter resource being the focal resource. Multiple resources MAY be present</font> |
|  - - date | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When item added to list<br/><font color='red'>This SHOULD contain a system time of when the item was added to the list.</font> |
|  - - item | 1..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>A reference to an Encounter resource included in the list<br/>This MUST use the CareConnect Encounter profile. </font>See [Encounter resource](explore_clinical_risk_factors.html#mapping-for-clinical-risk-factors-encounter) for information on how to populate the resource. |
|  - - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>The reference to the included Encounter resource.</font> |

## Mapping for Clinical Risk Factors Encounter ##

|>|Level 1|[Encounter Resource](http://hl7.org/fhir/stu3/encounter.html)|>|Level 2|[CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)|>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_clinical_risk_factors_all.html#mapping-for-clinical-risk-factors-encounter)**| 

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  Encounter | ​ |  |  | An interaction during which services are provided to the patient<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Identifier(s) by which this encounter is known<br/><font color='red'>An identifier for this Encounter</font> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique<br/><font color='red'>An identifier for this Clinical risk factors encounter</font> |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | planned : arrived : triaged : in-progress : onleave : finished : cancelled +<br/>Binding (required): Current state of the encounter [EncounterStatus](http://hl7.org/fhir/stu3/valueset-encounter-status.html)<br/><font color='red'>The status of the Encounter MUST contain the value 'finished'</font> |
|  - location | 0..1 | Required | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | List of locations where the patient has been |
|  - - location | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Location the encounter takes place<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>Where the risk  assessment took place</font> |
|   |  | Mandatory | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") | <font color='red'>The location<br/>This MUST use the CareConnect Location profile. </font>See [Location resource](explore_clinical_risk_factors.html#mapping-for-clinical-risk-factors-location) for information on how to populate the resource. |
|  - - - reference | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the Location resource included in the Clinical risk factors list</font>  |

## Mapping for Clinical Risk Factors RiskAssessment ##

|>|Level 1|[RiskAssessment Resource](http://hl7.org/fhir/stu3/riskassessment.html)|>|Level 2|[CareConnect-RiskAssessment-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-RiskAssessment-1)|>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_clinical_risk_factors_all.html#mapping-for-clinical-risk-factors-riskassessment)**| 

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| --- | --- | --- | --- | --- |
|  RiskAssessment | ​ |  |  | Potential outcomes for a subject with likelihood<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | Meta | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-RiskAssessment-1'</font> |
|  - identifier | 0..1 | Required | Identifier | Unique identifier for the assessment |
|  - - system | 0..1 | Required | Uri | The namespace for the identifier value |
|  - - value | 0..1 | Required | String | The value that is unique |
|  - status | 1..1 | Mandatory | Code | registered : preliminary : final : amended +<br/>Binding (required): The status of the risk assessment; e.g. preliminary, final, amended, etc. [ObservationStatus](http://hl7.org/fhir/stu3/valueset-observation-status.html)<br/><font color='red'>This SHOULD contain a value of 'final'</font> |
|  - method | 1..1 | Mandatory | CodeableConcept | Evaluation mechanism<br/>Binding (example): The mechanism or algorithm used to make the assessment; e.g. TIMI, PRISM, Cardiff Type 2 diabetes, etc.<br/><font color='red'><b>Mapping to Maternity data item = 'Clinical Risk Assessment'</b></font> |
|  - - coding | 0..* | Required | Coding | Code defined by a terminology system |
|  - - text | 0..1 | Required | String | Plain text representation of the concept<br/><font color='red'>Specific assessments undertaken in relation to the risk</font><br/><font color='red'><b>Mapping to Maternity data item = 'Clinical Risk Assessment'</b></font> |
|  - context | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Where was assessment performed?<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Required | [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1 "CareConnect-Encounter-1") | <font color='red'>This MUST use the CareConnect Encounter profile. </font>See [Encounter resource](explore_clinical_risk_factors.html#mapping-for-clinical-risk-factors-encounter) for information on how to populate the resource. |
|  - - reference | 0..1 | Required | String | Literal reference, Relative, internal or absolute URL |
|  - occurrence[x] | 0..1 | Required | dateTime | When was assessment made?<br/><font color='red'><b>Mapping to Maternity data item = 'Date/Time'</b></font>  |
|  - performer | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who did assessment?<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Required | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") | <font color='red'>This MUST use the CareConnect Practitioner profile. </font>See [Practitioner resource](explore_clinical_risk_factors.html#mapping-for-clinical-risk-factors-practitioner) for information on how to populate the resource. |
|  - - reference | 0..1 | Required | String | Literal reference, Relative, internal or absolute URL |
|  - basis | 0..* | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Information used in assessment<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>Factors that have been shown to be associated with the development of a medical condition being considered as a diagnosis. E.g. being overweight, smoker,  enzyme deficiency.</font><br/><font color='red'><b>Mapping to Maternity data item = 'Relevant Clinical Risk Factor'</b></font> |
|   |  | Required | [Resource](http://hl7.org/fhir/stu3/StructureDefinition/Resource "Resource") | <font color='red'>The coded information used in an assessment<br/>This MUST use the CareConnect  observation profile. </font>See [Observation resource](explore_clinical_risk_factors.html#mapping-for-clinical-risk-factors-observation) for information on how to populate the resource. |
|  - - reference | 0..1 | Required | String | Literal reference, Relative, internal or absolute URL |
|  - mitigation | 0..1 | Required | String | How to reduce risk |


## Patient Reference ##

The Admission details list has a mandated subject reference to the Patient resource. This means that any exchange of the Admission details heading data must also include the [Patient demographics List.](explore_patient_demographics.html)

## Mapping for Clinical Risk Factors Observation ##

|>|Level 1|[Observation Resource](http://hl7.org/fhir/stu3/observation.html)|>|Level 2|[CareConnect-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|>|Level 3|None| 

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_clinical_risk_factors_all.html#mapping-for-clinical-risk-factors-observation)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  Observation | ​ |  |  | Measurements and simple assertions<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (obs-7): If code is the same as a component code then the value element associated with the code SHALL NOT be present<br/>Constraint (obs-6): dataAbsentReason SHALL only be present if Observation.value[x] is not present |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1'</font> |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | registered : preliminary : final : amended +<br/>Binding (required): Codes providing the status of an observation. [ObservationStatus](http://hl7.org/fhir/stu3/valueset-observation-status.html)<br/><font color='red'>This MUST contain the value 'final'</font> |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of observation (code / type)<br/>Binding (example): Codes identifying names of simple observations. [LOINC Codes](http://hl7.org/fhir/stu3/valueset-observation-codes.html)<br/> |
|  - - coding | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system describing a type of observation [CareConnect-ObservationType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ObservationType-1)<br/><font color='red'>This uses a SNOMED CT concept to describe this observation as one related to clinical risk assessment</font><br/><font color='red'><b>Mapping to Maternity data item = 'Relevant Clinical Risk Factor'</b></font> |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain a concept from 999000131000000105 \|Care planning health issues simple reference set (foundation metadata concept)\|   </font> |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>This SHOULD contain the preferred term associated with the code</font> |

## Mapping for Clinical Risk Factors Location ##

The clinical risk factors has reference(s) to the Location resource. This means that any exchange of the clinical risk factors heading data must also include the [Location Details.](explore_location.html#mapping-for-location)

## Mapping for Clinical Risk Factors Practitioner ##

The clinical risk factors has reference(s) to the Practitioner resource. This means that any exchange of the clinical risk factors heading data must also include the [Practitioner Details.](explore_practitioner.html#mapping-for-practitioner)

## Mapping for Clinical Risk Factors PractitionerRole ##

The clinical risk factors has reference(s) to the Practitioner Role resource. This means that any exchange of the clinical risk factors heading data must also include the [Practitioner Role Details.](explore_practitioner_role.html#mapping-for-practitioner_role)


## Clinical Risk Factors Heading Example ##

<script src="https://gist.github.com/IOPS-DEV/04a0e4fa207c2ff6eb9f478e73313d2b.js"></script>
 