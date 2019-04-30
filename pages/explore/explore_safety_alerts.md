---
title: Safety Alerts Bundle
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_safety_alerts.html
summary: "The FHIR profiles used for the Safety alerts Bundle"
---

## Heading Description ##
Details of the concern, risk or issues in relation to safeguarding.

## Safety Alerts Structure ##

{% include custom/safety_alerts.svg %}


## Mapping for Safety Alerts List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2| None|>|Level 3|[CareConnect-List-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_safety_alerts_all.html#mapping-for-safety-alerts-list)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-List-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business identifier<br/><font color='red'>An identifier for this Screening Review list</font><br/> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique<br/>Business identifier<br/><font color='red'>An identifier for this Screening Review details list</font> |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource<br/><font color='red'>The organization that allocated the identifier</font> |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | current : retired : entered-in-error<br/>Binding (required): The current state of the list [ListStatus](http://hl7.org/fhir/stu3/valueset-list-status.html)<br/><font color='red'>The status of the list MUST contain the value 'current'</font> |
|  - mode | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | working : snapshot : changes<br/>Binding (required): The processing mode that applies to this list [ListMode](http://hl7.org/fhir/stu3/valueset-list-mode.html)<br/><font color='red'>The mode of the list MUST contain the value 'snapshot'</font> |
|  - title | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Descriptive name for the list<br/><font color='red'>This MUST contain the value 'Social Context'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading Screening Review'</b></font>  |
|  - code | 0..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | What the purpose of this list is<br/>Binding (preferred): What the purpose of a list is [CareConnect-ListCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListCode-1)<br/><font color='red'>The PRSB heading for this list. Note: for Maternity the value stated below is used which is not from the preferred value set </font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/><font color='red'>The SNOMED CT concept for the PRSB heading type</font> |
|  - - - system | 0..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value '886931000000107'</font> |
|  - - - display | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>This MUST contain the value 'Antenatal screening (observable entity)''</font><br/><font color='red'>Mapping to Maternity data item = 'PSRB Heading ' Safety alerts'</font>  |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color='red'>This is the subject of the Social Context details List.<br/>This MUST use the CareConnect patient profile. </font>See[patient resource reference](explore_social_context.html#patient-reference) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - date | 0..1 | Mandatory | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the list was prepared<br/><font color='red'> This MUST contain a system date to indicate when the list created or updated</font> |
|  - note | 0..* | Optional | [Annotation](http://hl7.org/fhir/stu3/datatypes.html#annotation "Annotation") | Comments about the list |
|   |  | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | <font color='red'>Who authored the comment on the list.</font>  |
|  - - time | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the annotation was made |
|  - - text | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The annotation - text content |
|  - entry | 0..* | Mandatory | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Entries in the list<br/><font color='red'>The entries MUST be as per the diagram for this PRSB headings list with the Flag resource being the focal resource.</font> |
|  - - date | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When item added to list<br/><font color='red'>The SHOULD contain a system time of when the item was added to the list.</font> |
|  - - item | 1..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>The reference to the included resources.</font> |

## Patient Reference ##

The Admission details list has a mandated subject reference to the Patient resource. This means that any exchange of the Admission details heading data must also include the [Patient demographics List.](explore_patient_demographics.html)


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_screening_review_all.html#mapping-for-national-antenatal-screening-programme-list)**|

## Mapping for Safety Alerts ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/flag.html)|>|Level 2| None|>|Level 3|[CareConnect-Flag-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Flag-1)|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_safety_alerts_all.html#mapping-for-safety-alerts)**|

|  **Name** | **Card.** | Conformance | **Type** | **Description/Constraints** |
| :--- | :--- | --- | :--- | :--- |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color="red">The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Flag-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business identifier |
|  - - system | 1..1 | Required | Uri | The namespace for the identifier value |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - - period | 0..1 | Mandatory | Period | Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Mandatory | dateTime | Starting time with inclusive boundary<br/><font color="red">The date on which the safety alert was recorded</font> |
|  - - - end | 0..1 | Required | dateTime | End time with inclusive boundary, if not ongoing |
|  - - assigner | 0..1 | Required | Reference | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - - reference | 0..1 | Required | Identifier | Logical reference, when literal reference is not known |
|  - status | 1..1 | Mandatory | Code | active \| inactive \| entered-in-error<br/>Binding (required): Indicates whether this flag is active and needs to be displayed to a user, or whether it is no longer needed or entered in error. ( http://hl7.org/fhir/stu3/valueset-flag-status.html )<br/><font color="red">Status of the safety alert</font> |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Coded or textual message to display to user<br/>Binding (example): Detail codes identifying specific flagged issues. ( http://hl7.org/fhir/stu3/valueset-flag-code.html )<br/><font color="red">Data item maps to one of PRSB 'Risk to Self' OR 'Risk to Other' OR 'Risk from Others'. Not Coded therefore code.text MUST be used. </font> |
|  - - text | 0..1 | Optional | String | Plain text representation of the concept<br/><font color="red">Narative that describes the 'risk' being recorded. MUST prefix 'Risk to Self' OR 'Risk to Other' OR 'Risk from Others' to narrative to indicate type of risk.</font> |
|  - subject | 1..1 | Mandatory | Reference | Who/What is flag about?<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | CareConnect-Patient-1 |  |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - period | 0..1 | Mandatory | Period | Time period when flag is active<br/>Constraint (per-1): If present, start SHALL have a lower value than end<br/><font color="red">The date on which the safety alert was recorded</font> |
|  - - start | 0..1 | Mandatory | dateTime | Starting time with inclusive boundary |
|  - - end | 0..1 | Required | dateTime | End time with inclusive boundary, if not ongoing |
|  - author | 0..1 | Required | Reference | Flag creator<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Required |  CareConnect-Organization-1 | <font color="red">The Site Code of where the safety alert recorded</font> |
|  - - reference | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |

## Safety Alerts Example ##

<script src="https://gist.github.com/IOPS-DEV/3a74996fc648b2e16e24a97231c75611.js"></script>
