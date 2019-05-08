---
title: Referral Details Bundle
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_referral_details.html
summary: "The FHIR profiles used for the Referral details Bundle"
---

## Heading Description ##
The details of the individual or team who referred the woman.

## Referral Structure Details ##

{% include custom/referral_request.svg %}

## Mapping for Referral List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2| None|>|Level 3|[CareConnect-List-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_referral_details_all.html#mapping-for-referral-list)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | Meta | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-List-1'</font> |
|  - identifier | 0..* | Required | Identifier | Business identifier<br/><font color='red'>An identifier for this Social Context details list</font> |
|  - - system | 1..1 | Required | Uri | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - period | 0..1 | Mandatory | Period | Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - status | 1..1 | Mandatory | Code | current : retired : entered-in-error<br/>Binding (required): The current state of the list [ListStatus](http://hl7.org/fhir/stu3/valueset-list-status.html)<br/><font color='red'>The status of the list MUST contain the value 'current'</font> |
|  - mode | 1..1 | Mandatory | Code | working : snapshot : changes<br/>Binding (required): The processing mode that applies to this list [ListMode](http://hl7.org/fhir/stu3/valueset-list-mode.html)<br/><font color='red'>The mode of the list MUST contain the value 'snapshot'</font> |
|  - title | 0..1 | Mandatory | String | Descriptive name for the list<br/><font color='red'>This MUST contain the value 'Referralt'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading Referral'</b></font>  |
|  - code | 0..1 | Mandatory | CodeableConcept | What the purpose of this list is<br/>Binding (preferred): What the purpose of a list is [CareConnect-ListCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListCode-1)<br/><font color='red'>The PRSB heading for this list. Note: for Maternity the value stated below is used which is not from the preferred value set </font> |
|  - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system<br/><font color='red'>The SNOMED CT concept for the PRSB heading type</font> |
|  - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value '3457005'</font> |
|  - - - display | 0..1 | Mandatory | String | Representation defined by the system<br/><font color='red'>Mapping to Maternity data item = 'PSRB Heading Referral'</font>  |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color="red">This is the subject of the Admission details List. This MUST use the CareConnect patient profile.</font>See [patient resource reference](explore_referral.html#patient-reference) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - date | 0..1 | Required | dateTime | When the list was prepared<br/><font color="red">This MUST contain a system date to indicate when the list was created or updated</font> |
|  - entry | 0..* | Required | BackboneElement | Entries in the list<br/><font color="red">The entries MUST be as per the diagram for this PRSB headings list with the encounter resource being the focal resource. Multiple Observations with associated resources MAY be present</font> |
|  - - date | 0..1 | Required | dateTime | When item added to list<br/><font color='red'>The SHOULD contain a system time of when the item was added to the list.</font> |
|  - - item | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color="red">A reference to an Encounter resource included in the list This MUST use the CareConnect Observation profile. |
|  - - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL |

## Patient Reference ##

The Plan and requested actions List has a mandated subject reference to the Patient resource. This means that any exchange of the Plan and requested actions heading data must also include the [Patient demographics List.](explore_patient_demographics.html)

## Mapping for Referral ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/referralrequest.html)|>|Level 2| None|>|Level 3|[CareConnect-ReferralRequest-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-ReferralRequest-1)|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_referral_details_all.html#mapping-for-referral)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| --- | --- | --- | --- | --- |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-ReferralRequest-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business identifier<br/><font color='red'>An identifier for this Referral Request</font> |
|  - - system | 0..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value |
|  - - value | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - type | 0..1 | Required | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Referral/Transition of care request type<br/>Binding (example): Codes for types of referral; e.g. consult, transfer, temporary transfer. (http://hl7.org/fhir/stu3/valueset-referral-type.html )<br/><font color="red">A classification which identifies the source of referral</font> |
|  - priority | 0..1 | Required | Code | Urgency of referral / transfer of care request<br/>Binding (required): Codes indicating the relative priority of the referral. ( http://hl7.org/fhir/stu3/valueset-request-priority.html )<br/><font color="red">This is the priority of a request for services</font> |
|  - subject | 1..1 | Mandatory | Reference | Patient referred to care or transfer<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - authoredOn | 0..1 | Mandatory | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Date of creation/activation<br/><font color="red">The date the Referral was made</font> |
|  - - onBehalfOf | 0..1 | Required | Reference | Organization agent is acting for<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Required | CareConnect-Organization-1 |  |
|  - specialty | 0..1 | Mandatory | CodeableConcept | The clinical specialty (discipline) that the referral is requested for<br/>Binding (example): Codes indicating the types of capability the referred to service provider must have. (http://hl7.org/fhir/stu3/valueset-practitioner-specialty.html ) |
|  - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system |
|  - - - system | 0..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - code | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - reasonCode | 0..* | Mandatory | CodeableConcept | Reason for referral / transfer of care request<br/>Binding (example): Codes indicating why the referral is being requested. ( http://hl7.org/fhir/stu3/valueset-clinical-findings.html )<br/><font color="red">Reason for Referral</font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - system | 0..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - code | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - note | 0..* | Optional | [Annotation](http://hl7.org/fhir/stu3/datatypes.html#annotation "Annotation") | Comments made about referral request<br/><font color="red">Comment related to referral</font> |
|  - - author[x] | 0..1 | Required | String | Individual responsible for the annotation<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | CareConnect-Patient-1 |  |
|   |  | Optional | CareConnect-RelatedPerson-1 |  |
|   |  | Optional | CareConnect-Practitioner-1 |  |

## Mapping for Plan and Requested Actions Practitioner ## 

The plan and requested actions details has reference(s) to the Practitioner resource. This means that any exchange of the plan and requested actions details heading data must also include the [Practitioner Details](explore_practitioner.html#mapping-for-practitioner)

## Mapping for Plan and Requested Actions PractitionerRole ##  

The plan and requested actions details has reference(s) to the Practitioner Role resource. This means that any exchange of the plan and requested actions details heading data must also include the [Practitioner Role Details](explore_practitioner_role.html#mapping-for-practitioner_role)

## Referral Example ##

<script src="https://gist.github.com/IOPS-DEV/bda39816eded889855782144de5bc3aa.js"></script>