---
title: Admission Details Bundle
keywords:  bundles
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_admission_details.html
summary: "The FHIR profiles used for the Admission Details Bundle"
---

## Heading Description ##
The details of the woman’s admission.

The following FHIR profiles are used to form the Admission details list structure:

- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)
- [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)
- [RelatedPerson](http://hl7.org/fhir/STU3/relatedperson.html)
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)

The following profiles are referenced from the Admission details list structure:

- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)

## Admission Details Structure ##

{% include custom/admission_details.svg %}


## Maternity Data Set Mapping to FHIR profiles ##

The following tables detail how to populate the FHIR resources and the mapping to the Maternity data set.

## Mapping for Admission Details List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_admission_details_all.html#mapping-for-admission-details-list)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for XXX Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  List | ​ |  |  | Information summarized from a list of other resources<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (lst-2): The deleted flag can only be used if the mode of the list is "changes"<br/>Constraint (lst-1): A list can only have an emptyReason if it is empty |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | Meta | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-List-1'</font><br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font>  |
|  - identifier | 0..* | Required | Identifier | Business identifier<br/><font color='red'>An identifier for this Admission details list</font><br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font>  |
|  - - system | 1..1 | Required | Uri | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font><br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font>  |
|  - - value | 1..1 | Required | String | The value that is unique<br/>Business identifier<br/><font color='red'>An identifier for this Admission details list</font><br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font>  |
|  - - assigner | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - - display | 0..1 | Required | String | Text alternative for the resource<br/><font color='red'>The organization that allcated the identifier</font><br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font>  |
|  - status | 1..1 | Mandatory | Code | current : retired : entered-in-error<br/>Binding (required): The current state of the list [ListStatus](http://hl7.org/fhir/stu3/valueset-list-status.html)<br/><font color='red'>The status of the list MUST contain the value 'current''</font><br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font>  |
|  - mode | 1..1 | Mandatory | Code | working : snapshot : changes<br/>Binding (required): The processing mode that applies to this list [ListMode](http://hl7.org/fhir/stu3/valueset-list-mode.html)<br/><font color='red'>The mode of the list MUST contain the value 'snapshot'</font><br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font>  |
|  - title | 0..1 | Mandatory | String | Descriptive name for the list<br/><font color='red'>This MUST contain the value 'Admission details'</font><br/><font color='red'><b>Mapping to Maternity Data item = 'PSRB Heading Admission details'</b></font>  |
|  - code | 0..1 | Mandatory | CodeableConcept | What the purpose of this list is<br/>Binding (preferred): What the purpose of a list is [CareConnect-ListCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListCode-1) |
|  - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system |
|  - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system<br/><font='red'>This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system<br/><font='red'>This MUST contain the value '886781000000108'</font><br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font>  |
|  - - - display | 0..1 | Mandatory | String | Representation defined by the system<br/><font color='red'>This MUST contain the value 'Admission details'</font><br/><br/><font color='red'><b>Mapping to Maternity Data item = 'PSRB Heading Admission details'</b></font>  |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | This is the subject of the Admission details List.<br/>This MUST use the CareConnect patient profile. See [patient resource](explore_admission_details.html#mapping-for-admission-details-encounter) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographic list within the FHIR Bundle. Note the Patient demopgraphic list is mandatory in the FHIR bundle</font/>  |
|  - date | 0..1 | Mandatory | dateTime | When the list was prepared<br/><font color='red'> This MUST contain a system date to indicate when the list created or updated</font/><br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font>  |
|  - note | 0..* | Optional | Annotation | Comments about the list<br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font>  |
|   |  | Required | String | <font color='red'>Who authored the comment on the list.</font> <br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font>  |
|  - - time | 0..1 | Required | dateTime | When the annotation was made<br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font>  |
|  - - text | 1..1 | Required | String | The annotation - text content<br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font>  |
|  - entry | 0..* | Mandatory | BackboneElement | Entries in the list<br/><font color='red'>The entries MUST be as per the diagram for this PRSB headings list with the ecounter resource being the focal resource. Multiple Encounters with associated resources MAY be present</font><br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font>  |
|  - - date | 0..1 | Required | dateTime | When item added to list<br/><font color='red'>The SHOULD contain a system time of when the item was added to the list.</font><br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font>  |
|  - - item | 1..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>A reference to an Encounter resource included in the list</font><br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font> " |
|  - - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL<br/><font color='red'>The reference to the included Encounter resource.</font><br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font> " |

## Mapping for Admission Details Encounter ##

|>|Level 1|[Encounter Resource](http://hl7.org/fhir/stu3/encounter.html)|>|Level 2|[CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_admission_details_all.html#mapping-for-admission-details-encounter)**|

## Mapping for Admission Details RelatedPerson ##

|>|Level 1|[RelatedPerson Resource](http://hl7.org/fhir/stu3/relatedPerson.html)|>|Level 2|None|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_admission_details_all.html#mapping-for-admission-details-relatedperson)**|

## Mapping for Admission Details Practitioner ##

|>|Level 1|[Practitioner Resource](http://hl7.org/fhir/stu3/practitioner.html)|>|Level 2|[CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_admission_details_all.html#mapping-for-admission-details-practitioner)**|

## Mapping for Admission Details PractitionerRole ##

|>|Level 1|[Practitioner Resource](http://hl7.org/fhir/stu3/practitionerRole.html)|>|Level 2|[CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_admission_details_all.html#mapping-for-admission-details-practitionerrole)**|