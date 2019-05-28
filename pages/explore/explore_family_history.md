---
title: Family History Bundle
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_family_history.html
summary: "The FHIR profiles used for the Family history Bundle"
---


## Heading Description ##
Information on illness in family relations relevant to the health or care of the woman.

- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)
- [CareConnect-FamilyMemberHistory-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-FamilyMemberHistory-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)

The following profiles are referenced from the investigation results details list structure:

- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)

## Family History Structure Details ##

{% include custom/family_history.svg %}

## Mapping Overview ##

|Date/Time|[FamilyMemberHistory](explore_family_history.html#mapping-for-family-history-family-member-history)|date|
|ODS/ORD Site Code|[Location](explore_family_history.html#mapping-for-family-history-location)|identifier|
|Family History|[FamilyMemberHistory](explore_family_history.html#mapping-for-family-history-family-member-history)|condition.code|
|Person in the Family||relationship|
|Comment||note|

## Mapping for Family History List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3| None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_safeguarding_all.html#mapping-for-safeguarding-details-list)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | Meta | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-List-1'</font> |
|  - identifier | 0..* | Required | Identifier | Business identifier<br/><font color='red'>An identifier for this Family History details list</font> |
|  - - system | 1..1 | Required | Uri | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Mandatory | String | The value that is unique<br/><font color='red'>An identifier for this Family History details list</font> |
|  - status | 1..1 | Mandatory | Code | current : retired : entered-in-error<br/>Binding (required): The current state of the list [ListStatus](http://hl7.org/fhir/stu3/valueset-list-status.html)<br/><font color='red'>The status of the list MUST contain the value 'current'</font> |
|  - mode | 1..1 | Mandatory | Code | working : snapshot : changes<br/>Binding (required): The processing mode that applies to this list [ListMode](http://hl7.org/fhir/stu3/valueset-list-mode.html)<br/><font color='red'>The mode of the list MUST contain the value 'snapshot'</font> |
|  - title | 0..1 | Mandatory | String | Descriptive name for the list<br/><font color='red'>This MUST contain the value 'Family History'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading GP Practice'</b></font>  |
|  - code | 0..1 | Mandatory | CodeableConcept | What the purpose of this list is<br/>Binding (preferred): What the purpose of a list is [CareConnect-ListCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListCode-1)<br/><font color='red'>The PRSB heading for this list. Note: for Maternity the value stated below is used which is not from the preferred value set </font> |
|  - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system<br/><font color='red'>The SNOMED CT concept for the PRSB heading type</font> |
|  - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value '163051000000102'</font> |
|  - - - display | 0..1 | Mandatory | String | Representation defined by the system<br/><font color='red'>This MUST contain the value 'Family History'<br/>Mapping to Maternity data item = 'PSRB Heading Family History'</font>  |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color="red">This is the subject of the Family History details List. This MUST use the CareConnect patient profile.</font>See [patient resource reference](explore_observation.html#patient-reference) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - date | 0..1 | Required | dateTime | When the list was prepared<br/><font color="red">This MUST contain a system date to indicate when the list was created or updated</font> |
|  - entry | 0..* | Required | BackboneElement | Entries in the list<br/><font color="red">The entries MUST be as per the diagram for this PRSB headings list. MAY contain a 'Family History of Fetus List' and/or 'Family History of Woman List'</font> |
|  - - date | 0..1 | Required | dateTime | When item added to list<br/><font color='red'>The SHOULD contain a system time of when the item was added to the list.</font> |
|  - - item | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color="red">A references to Organization, Practice and Flag resources MAY be included in the list. These MUST use the CareConnect profiles.</font>|
|  - - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL <font color="red">The reference to the included CareConnect resource.</font> |

## Mapping for Family History of Fetus List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3| None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_safeguarding_all.html#mapping-for-safeguarding-details-list)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | Meta | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-List-1'</font> |
|  - identifier | 0..* | Required | Identifier | Business identifier<br/><font color='red'>An identifier for this Family History details list</font> |
|  - - system | 1..1 | Required | Uri | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Mandatory | String | The value that is unique<br/><font color='red'>An identifier for this Family History details list</font> |
|  - status | 1..1 | Mandatory | Code | current : retired : entered-in-error<br/>Binding (required): The current state of the list [ListStatus](http://hl7.org/fhir/stu3/valueset-list-status.html)<br/><font color='red'>The status of the list MUST contain the value 'current'</font> |
|  - mode | 1..1 | Mandatory | Code | working : snapshot : changes<br/>Binding (required): The processing mode that applies to this list [ListMode](http://hl7.org/fhir/stu3/valueset-list-mode.html)<br/><font color='red'>The mode of the list MUST contain the value 'snapshot'</font> |
|  - title | 0..1 | Mandatory | String | Descriptive name for the list<br/><font color='red'>This MUST contain the value 'Family History'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading GP Practice'</b></font>  |
|  - code | 0..1 | Mandatory | CodeableConcept | What the purpose of this list is<br/>Binding (preferred): What the purpose of a list is [CareConnect-ListCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListCode-1)<br/><font color='red'>The PRSB heading for this list. Note: for Maternity the value stated below is used which is not from the preferred value set </font> |
|  - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system<br/><font color='red'>The SNOMED CT concept for the PRSB heading type</font> |
|  - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value '163051000000102'</font> |
|  - - - display | 0..1 | Mandatory | String | Representation defined by the system<br/><font color='red'>This MUST contain the value 'Family History'<br/>Mapping to Maternity data item = 'PSRB Heading Family History'</font>  |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color="red">This is the subject of the Family History details List. This MUST use the CareConnect patient profile.</font>See [patient resource reference](explore_observation.html#patient-reference) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - date | 0..1 | Required | dateTime | When the list was prepared<br/><font color="red">This MUST contain a system date to indicate when the list was created or updated</font> |
|  - entry | 0..* | Required | BackboneElement | Entries in the list<br/><font color="red">The entries MUST be as per the diagram for this PRSB headings list. MUST contain a 'Encounter Resource' and/ MAY inlcude a 'FamilyMemberHistory resource'</font> |
|  - - date | 0..1 | Required | dateTime | When item added to list<br/><font color='red'>The SHOULD contain a system time of when the item was added to the list.</font> |
|  - - item | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color="red">A references to Organization, Practice and Flag resources MAY be included in the list. These MUST use the CareConnect profiles.</font>|
|  - - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL <font color="red">The reference to the included CareConnect resource.</font> |

## Mapping for Family History of Woman List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3| None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_safeguarding_all.html#mapping-for-safeguarding-details-list)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | Meta | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-List-1'</font> |
|  - identifier | 0..* | Required | Identifier | Business identifier<br/><font color='red'>An identifier for this Family History details list</font> |
|  - - system | 1..1 | Required | Uri | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Mandatory | String | The value that is unique<br/><font color='red'>An identifier for this Family History details list</font> |
|  - status | 1..1 | Mandatory | Code | current : retired : entered-in-error<br/>Binding (required): The current state of the list [ListStatus](http://hl7.org/fhir/stu3/valueset-list-status.html)<br/><font color='red'>The status of the list MUST contain the value 'current'</font> |
|  - mode | 1..1 | Mandatory | Code | working : snapshot : changes<br/>Binding (required): The processing mode that applies to this list [ListMode](http://hl7.org/fhir/stu3/valueset-list-mode.html)<br/><font color='red'>The mode of the list MUST contain the value 'snapshot'</font> |
|  - title | 0..1 | Mandatory | String | Descriptive name for the list<br/><font color='red'>This MUST contain the value 'Family History'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading GP Practice'</b></font>  |
|  - code | 0..1 | Mandatory | CodeableConcept | What the purpose of this list is<br/>Binding (preferred): What the purpose of a list is [CareConnect-ListCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListCode-1)<br/><font color='red'>The PRSB heading for this list. Note: for Maternity the value stated below is used which is not from the preferred value set </font> |
|  - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system<br/><font color='red'>The SNOMED CT concept for the PRSB heading type</font> |
|  - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value '163051000000102'</font> |
|  - - - display | 0..1 | Mandatory | String | Representation defined by the system<br/><font color='red'>This MUST contain the value 'Family History'<br/>Mapping to Maternity data item = 'PSRB Heading Family History'</font>  |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color="red">This is the subject of the Family History details List. This MUST use the CareConnect patient profile.</font>See [patient resource reference](explore_observation.html#patient-reference) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - date | 0..1 | Required | dateTime | When the list was prepared<br/><font color="red">This MUST contain a system date to indicate when the list was created or updated</font> |
|  - entry | 0..* | Required | BackboneElement | Entries in the list<br/><font color="red">The entries MUST be as per the diagram for this PRSB headings list. MUST contain a 'Encounter Resource' and/ MAY inlcude a 'FamilyMemberHistory resource'</font> |
|  - - date | 0..1 | Required | dateTime | When item added to list<br/><font color='red'>The SHOULD contain a system time of when the item was added to the list.</font> |
|  - - item | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color="red">A references to Organization, Practice and Flag resources MAY be included in the list. These MUST use the CareConnect profiles.</font>|
|  - - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL <font color="red">The reference to the included CareConnect resource.</font> |

## Mapping for Family History Encounter ##

|>|Level 1|[Encounter Resource](http://hl7.org/fhir/stu3/encounter.html)|>|Level 2|[CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_admission_details_all.html#mapping-for-admission-details-encounter)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
| :--- | :--- | :--- | :--- | :--- |
|  Encounter | ​ |  |  | An interaction during which services are provided to the patient<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Identifier(s) by which this encounter is known<br/><font color='red'>An identifier for this Encounter</font> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique<br/><font color='red'>An identifier for this Encounter</font> |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | planned : arrived : triaged : in-progress : onleave : finished : cancelled +<br/>Binding (required): Current state of the encounter [EncounterStatus](http://hl7.org/fhir/stu3/valueset-encounter-status.html)<br/><font color='red'>The status of the Encounter MUST contain the value 'finished'</font> |
|  - location | 0..1 | Required | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | List of locations where the patient has been |
|  - - location | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Location the encounter takes place<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>The ODS/ORD Site Code of where the Family History was recorded</font> |
|   |  | Mandatory | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") | The location<br/> <font color='red'>This MUST use the CareConnect Location profile. </font>See [Location resource](explore_admission_details.html#mapping-for-admission-details-location) for information on how to populate the resource." |
|  - - - reference | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the Location resource included in the Family History details list</font>  |

## Patient Reference ##

The Plan and requested actions List has a mandated subject reference to the Patient resource. This means that any exchange of the Plan and requested actions heading data must also include the [Patient demographics List.](explore_patient_demographics.html)

## Mapping for Family History Family Member History ##

|>|Level 1|[FamilyMemberHistory Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-FamilyMemberHistory-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-FamilyMemberHistory-1)|>|Level 3| None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_safeguarding_all.html#mapping-for-safeguarding-details-list)**|

|  **Name** | **Card.** | Conformance | **Type** | **Description/Constraints** |
| :--- | :--- | --- | :--- | :--- |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  -meta | 0..1 | Mandatory | Meta | Metadata about the resource |
|  - identifier | 0..* | Required | Identifier | External Id(s) for this record<br/><font color="red">An identifier for this FamilyMemberHistory</font> |
|  - - system | 1..1 | Required | Uri | The namespace for the identifier value<br/><font color="red">The system from which the identifier came from</font> |
|  - - value | 1..1 | Required | String | The value that is unique<br/><font color="red">An identifier for this FamilyMemberHistory</font> |
|  - patient | 1..1 | Mandatory | Reference ( CareConnect-Patient-1 ) | Patient history is about<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - date	 | 0..1 | Mandatory | dateTime | When history was captured/updated <font color="red">The date the Family History was recorded</font> |
|  - relationship | 1..1 | Required | CodeableConcept | Relationship to the subject<br/>Binding (example): The nature of the relationship between the patient and the related person being described in the family member history. ( http://hl7.org/fhir/stu3/v3/FamilyMember/vs.html )<br/><font color="red">The relationship of the person with the condition to the mother</font> |
|  - - - system | 1..1 | Mandatory | Uri | Identity of the terminology system<br/>Fixed Value: http://snomed.info/sct |
|  - - - code | 1..1 | Mandatory | Code | Symbol in syntax defined by the system<br/><font color="red">A SNOMED CT from the Person in the family concept</font> |
|  - - - display | 1..1 | Mandatory | String | Representation defined by the system<br/><font color="red">The display associated with the SNOMED CT concept. This SHOULD be the preferred term</font> |
|  - note | 0..* | Optional | Annotation | General note about related person<br/><font color="red">Any further textual comment.</font> |
|  - - text | 1..1 | Mandatory | String | The annotation - text content |
|  - condition | 0..* | Mandatory | BackboneElement | Condition that the related person had<br/><font color="red">The condition or diagnosis in family relations deemed to be significant to the care or health of the mother.</font> |
|  - - code | 1..1 | Mandatory | CodeableConcept | Condition suffered by relation<br/>Binding (example): Identification of the Condition or diagnosis. ( http://hl7.org/fhir/stu3/valueset-condition-code.html ) |
|  - - - coding (snomedCT) | 0..1 | Required | Coding | Code defined by a terminology system<br/><font color="red"> A concept from the Family history of clinical finding concept</font> |
|  - - - - system | 1..1 | Mandatory | Uri | Identity of the terminology system<br/>Fixed Value: http://snomed.info/sct |
|  - - - - code | 1..1 | Mandatory | Code | Symbol in syntax defined by the system<br/><font color="red">A SNOMED CT from theFamily history of clinical finding as defined above</font> |
|  - - - - display | 1..1 | Mandatory | String | Representation defined by the system<br/><font color="red">he display associated with the SNOMED CT concept. This SHOULD be the preferred term</font> |

## Mapping for Family History Location ##

The Family History details has reference(s) to the Location resource. This means that any exchange of the family history details heading data must also include the [Location Details](explore_location.html#mapping-for-location)

## Example of Family History ##

<script src="https://gist.github.com/IOPS-DEV/75399e2302222fbe4947b17e30180321.js"></script>
