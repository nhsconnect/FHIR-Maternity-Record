---
title: Patient Demographics List
keywords:  lists
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_patient_demographics.html
summary: "The FHIR profiles used for the Patient demographics list structure"
---

## Heading Description ##
This heading holds all of the elements for each instance of a patient demographics entry.

The following FHIR profiles are used to form the Patient demographics list structure:

- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)
- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)
- [CareConnect-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)

The following profiles are referenced from the Patient demographics list structure:

- None

## Patient Demographics Structure ##

{% include custom/patient_demographics.svg %}


## Maternity Data Set Mapping to FHIR profiles ##

The following tables detail how to populate the FHIR resources and the mapping to the Maternity data set.

## Mapping for Patient Demographics List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_admission_details_all.html#mapping-for-admission-details-list)**|


|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  List | ​ |  |  | Information summarized from a list of other resources<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (lst-2): The deleted flag can only be used if the mode of the list is "changes"<br/>Constraint (lst-1): A list can only have an emptyReason if it is empty |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | Meta | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-List-1'</font> |
|  - identifier | 0..* | Required | Identifier | Business identifier<br/><font color='red'>An identifier for this Patient demographics list</font><br/> |
|  - - system | 1..1 | Required | Uri | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Mandatory | String | The value that is unique<br/>Business identifier<br/><font color='red'>An identifier for this Patient demographics list</font> |
|  - - - display | 0..1 | Required | String | Text alternative for the resource<br/><font color='red'>The organization that allocated the identifier</font> |
|  - status | 1..1 | Mandatory | Code | current : retired : entered-in-error<br/>Binding (required): The current state of the list [ListStatus](http://hl7.org/fhir/stu3/valueset-list-status.html)<br/><font color='red'>The status of the list MUST contain the value 'current'</font> |
|  - mode | 1..1 | Mandatory | Code | working : snapshot : changes<br/>Binding (required): The processing mode that applies to this list [ListMode](http://hl7.org/fhir/stu3/valueset-list-mode.html)<br/><font color='red'>The mode of the list MUST contain the value 'snapshot'</font> |
|  - title | 0..1 | Mandatory | String | Descriptive name for the list<br/><font color='red'>This MUST contain the value 'Patient demographics'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading patient demographics'</b></font>  |
|  - code | 0..1 | Mandatory | CodeableConcept | What the purpose of this list is<br/>Binding (preferred): What the purpose of a list is [CareConnect-ListCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListCode-1)<br/><font color='red'>The PRSB heading for this list. Note: for Maternity the value stated below is used which is not from the preferred value set </font> |
|  - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system<br/><font color='red'>The SNOMED CT concept for the PRSB heading type</font> |
|  - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value '886731000000109'</font> |
|  - - - display | 0..1 | Mandatory | String | Representation defined by the system<br/><font color='red'>This MUST contain the value 'Patient demographics'</font><br/><font color='red'>Mapping to Maternity data item = 'PSRB Heading Patient demographics'</font>  |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color='red'>This is the subject of the Patient demgraphics List.<br/>This MUST use the CareConnect patient profile. </font>See [patient resource](explore_patient_demographics.html#mapping-for-patient-demopgraphics-patient) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - date | 0..1 | Mandatory | dateTime | When the list was prepared<br/><font color='red'> This MUST contain a system date to indicate when the list created or updated</font> |
|  - note | 0..* | Optional | Annotation | Comments about the list |
|   |  | Required | String | <font color='red'>Who authored the comment on the list.</font>  |
|  - - time | 0..1 | Required | dateTime | When the annotation was made |
|  - - text | 1..1 | Required | String | The annotation - text content |
|  - entry | 0..* | Mandatory | BackboneElement | Entries in the list<br/><font color='red'>The entries MUST be as per the diagram for this PRSB headings list with the Observation resource being the focal resource.</font> |
|  - - date | 0..1 | Required | dateTime | When item added to list<br/><font color='red'>The SHOULD contain a system time of when the item was added to the list.</font> |
|  - - item | 1..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>A reference to an Observation resource included in the list<br/>This MUST use the CareConnect Observation profile. </font>See [Observation resource](explore_patient_demographics.html#mapping-for-observation) for information on how to populate the resource. |
|  - - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL<br/><font color='red'>The reference to the included Observation resource.</font> 

