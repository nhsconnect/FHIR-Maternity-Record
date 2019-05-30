---
title: Attendance Details List
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_attendance_details.html
summary: "The FHIR profiles used for the Attendance details List"
---

## Heading Description ##
The details of the woman’s contact with services.

The following FHIR profiles are used to form the Attendance details list structure:

- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)
- [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)
- [CareConnect-Communication-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Communication-1)
- [CareConnect-EpisodeOfCare-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-EpisodeOfCare-1)
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)

The following profiles are referenced from the Attendance details list structure:

- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)

## Attendance Details Structure ##

{% include custom/attendance_details.svg %}

## Maternity Data Standard Mapping to FHIR profiles ##

## Mapping Overview ##

|**Data Standard Element**|**FHIR Profile Mapping**|**FHIR Element**|
|Date/Time|[List](explore_attendance_details.html#mapping-for-attendance-details-list)|period|
|ODS/ORD Site Code|[Location](explore_attendance_details.html#mapping-for-attendance-details-location)|identifier|
|Location Type|[Encounter](explore_attendance_details.html#mapping-for-attendance-details-location)|class|
|Professional Name|[Practitioner](explore_attendance_details.html#mapping-for-attendance-details-practitioner)|name|
|SDS Job Role Name|[PractitionerRole](explore_attendance_details.html#mapping-for-attendance-details-practitionerrole)|identifier|
|Contact type|[Encounter](explore_attendance_details.html#mapping-for-attendance-details-encounter)|type|
|Consultation method|[Communication](explore_attendance_details.html#mapping-for-attendance-details-communication)|medium|
|Care setting|[Location](explore_attendance_details.html#mapping-for-attendance-details-location)|type|
|Service|[EpisodeOfCare](explore_attendance_details.html#mapping-for-attendance-details-episodeofcare)|type|
|Care professional present (name)|[Practitioner](explore_attendance_details.html#mapping-for-attendance-details-practitioner)|name|
|Care professional present (role)|[PractitionerRole](explore_attendance_details.html#mapping-for-attendance-details-practitionerrole)|role|
|Care professionals present type|[Encounter](explore_attendance_details.html#mapping-for-attendance-details-encounter)|participant.type|
|First Given Name|[RelatedPerson](explore_attendance_details.html#mapping-for-attendance-details-relatedperson)|name|
|Family Name|[RelatedPerson](explore_attendance_details.html#mapping-for-attendance-details-relatedperson)|name|
|Relationship of person accompanying patient|[Encounter](explore_attendance_details.html#mapping-for-attendance-details-encounter)|participant.type|
|Outcome of contact|OutcomeOfAttendance extension |Currently not mapped due to "required" ValueSet issues|

## Mapping for Attendance Details List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_attendance_details_all.html#mapping-for-attendance-details-list)**|


|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  List | ​ |  |  | Information summarized from a list of other resources<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (lst-2): The deleted flag can only be used if the mode of the list is "changes"<br/>Constraint (lst-1): A list can only have an emptyReason if it is empty |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business identifier<br/><font color='red'>An identifier for this Attendance details list</font><br/> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique<br/>Business identifier<br/><font color='red'>An identifier for this Attendance details list</font> |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource<br/><font color='red'>The organization that allocated the identifier</font> |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | current : retired : entered-in-error<br/>Binding (required): The current state of the list [ListStatus](http://hl7.org/fhir/stu3/valueset-list-status.html)<br/><font color='red'>The status of the list MUST contain the value 'current'</font> |
|  - mode | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | working : snapshot : changes<br/>Binding (required): The processing mode that applies to this list [ListMode](http://hl7.org/fhir/stu3/valueset-list-mode.html)<br/><font color='red'>The mode of the list MUST contain the value 'snapshot'</font> |
|  - title | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Descriptive name for the list<br/><font color='red'>This MUST contain the value 'Attendance details'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading Attendance details'</b></font>  |
|  - code | 0..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | What the purpose of this list is<br/>Binding (preferred): What the purpose of a list is [CareConnect-ListCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListCode-1)<br/><font color='red'>The PRSB heading for this list. Note: for Maternity the value stated below is used which is not from the preferred value set </font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/><font color='red'>The SNOMED CT concept for the PRSB heading type</font> |
|  - - - system | 0..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value '1077881000000105'</font> |
|  - - - display | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>This MUST contain the value 'Attendance details'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading Attendance details'</b></font>  |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color='red'>This is the subject of the Attendance details List.<br/>This MUST use the CareConnect patient profile. </font>See [patient resource reference](explore_attendance_details.html#patient-reference) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - date | 0..1 | Mandatory | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the list was prepared<br/><font color='red'> This MUST contain a system date to indicate when the list was created or updated</font> |
|  - note | 0..* | Optional | [Annotation](http://hl7.org/fhir/stu3/datatypes.html#annotation "Annotation") | Comments about the list |
|   |  | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | <font color='red'>Who authored the comment on the list.</font>  |
|  - - time | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the annotation was made |
|  - - text | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The annotation - text content |
|  - entry | 0..* | Mandatory | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Entries in the list<br/><font color='red'>The entries MUST be as per the diagram for this PRSB headings list with the encounter resource being the focal resource. Multiple Encounters with associated resources MAY be present</font> |
|  - - date | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When item added to list<br/><font color='red'>This SHOULD contain a system time of when the item was added to the list.</font> |
|  - - item | 1..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>A reference to an Encounter resource included in the list<br/>This MUST use the CareConnect Encounter profile. </font>See [Encounter resource](explore_attendance_details.html#mapping-for-attendance-details-encounter) for information on how to populate the resource. |
|  - - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>The reference to the included Encounter resource.</font> |


## Mapping for Attendance Details Encounter ##

|>|Level 1|[Encounter Resource](http://hl7.org/fhir/stu3/encounter.html)|>|Level 2|[CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)|>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_attendance_details_all.html#mapping-for-attendance-details-encounter)**|  

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  Encounter | ​ |  |  | An interaction during which services are provided to the patient<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1'</font> |
|  - extension (outcomeOfAttendance)| 0..1 | Required | [Extension-CareConnect-OutcomeOfAttendance-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-OutcomeOfAttendance-1 "Extension-CareConnect-OutcomeOfAttendance-1") | An extension to the Encounter resource to record the outcome of an Out-Patient attendance.<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/><font color='red'>This item is currently not mapped due to issues with the required ValueSet</font><br/> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Identifier(s) by which this encounter is known<br/><font color='red'>An identifier for this Encounter</font> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique<br/><font color='red'>An identifier for this Attendance details encounter</font> |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | planned : arrived : triaged : in-progress : onleave : finished : cancelled +<br/>Binding (required): Current state of the encounter [EncounterStatus](http://hl7.org/fhir/stu3/valueset-encounter-status.html)<br/><font color='red'>The status of the Encounter MUST contain the value 'finished'</font> |
|  - class | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Classification of the encounter<br/>Binding (extensible): Classification of the encounter [ActEncounterCode](http://hl7.org/fhir/stu3/v3/ActEncounterCode/vs.html) |
|  - - system | 0..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - code | 0..1 | Required | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - type | 0..1 | Required | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Specific type of encounter<br/>Binding (example): The type of encounter [EncounterType](http://hl7.org/fhir/stu3/valueset-encounter-type.html)<br/> |
|  - - coding | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | <font color='red'>The example MUST not be used the following ValueSet MUST be used instead</font> [Care Contact Type](https://www.datadictionary.nhs.uk/data_dictionary/attributes/c/card/care_contact_type_de.asp?shownav=1) |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/> |
|  - - - code | 1..1 | Required | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - participant | 0..* | Required | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | List of participants involved in the encounter<br/><font color='red'><b>Mapping to Maternity data item = 'Care professionals present' , 'Person accompanying patient' and 'Professional performing the contact'</b></font> |
|  - - type | 0..* | Required | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Role of participant in encounter<br/>Binding (extensible): Role of participant in encounter [ParticipantType](http://hl7.org/fhir/stu3/valueset-encounter-participant-type.html)<br/><font color='red'>There will be several instances of this element. The first use case is for Care professionals present and performing professional which will use a reference to  the Practitioner resource and the second use case is for Person accompanying patient and this will use a reference to  the RelatedPerson resource</font><br/><font color='red'><b>Mapping to Maternity data item ='Care professionals present type' , 'Professional performing the contact' and 'Relationship of Person accompanying patient'</b></font> |
|  - - - coding | 1..1 | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/><font color='red'>There will be one instance of the coding for each instance of type</font> |
|  - - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | 	
Identity of the terminology system  |
|  - - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system <font color='red'>The Care professionals present will use the most appropriate code the performing professional will use a code of 'PPRF'.</font><br/><font color='red'>The Person accompanying patient will use a code of 'ESC'</font>  |
|  - - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Code defined by a terminology system<br/><font color='red'>The Care professional will use the display of 'primary performer'</font><br/><font color='red'>The Person accompanying patient will use a display of 'escort'</font>  |
|  - - individual | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Persons involved in the encounter other than the patient<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This MUST be a reference to either the Practitioner or RelatedPerson resource</font> |
|   |  | Required | [RelatedPerson](http://hl7.org/fhir/stu3/StructureDefinition/RelatedPerson "RelatedPerson") | <font color='red'>The person accompanying the patient.<br/>This MUST use the RelatedPerson resource. </font>See [RelatedPerson resource](explore_attendance_details.html#mapping-for-attendance-details-relatedperson) for information on how to populate the resource. |
|   |  | Required | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") | <font color='red'>Care Professionals present during the encounter.<br/>This MUST use the CareConnect Practitioner profile. </font>See [Practitioner resource](explore_attendance_details.html#mapping-for-attendance-details-practitioner) for information on how to populate the resource. |
|  - - - reference | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the RelatedPerson resource or the Practitioner resource included in the Attendance details list</font>  |
|  - location | 0..1 | Required | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | List of locations where the patient has been |
|  - - location | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Location the encounter takes place<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>The site code of the unit to which the person was admitted</font> |
|   |  | Mandatory | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") | <font color='red'>The location<br/>This MUST use the CareConnect Location profile. </font>See [Location resource](explore_attendance_details.html#mapping-for-attendance-details-location) for information on how to populate the resource." |
|  - - - reference | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the Location resource included in the Attendance details list</font>  |

## Patient Reference ##

The Admission details list has a mandated subject reference to the Patient resource. This means that any exchange of the Admission details heading data must also include the [Patient demographics List.](explore_patient_demographics.html)


## Mapping for Attendance Details Communication ##

|>|Level 1|[Communication Resource](http://hl7.org/fhir/stu3/communication.html)|>|Level 2|[CareConnect-Communication-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Communication -1)|>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_attendance_details_all.html#mapping-for-attendance-details-communication)**|  

|  **Name** | **Card.** | **Conformance** | **Type** | **Description/Constraints** |
| :--- | :--- | :--- | :--- | :--- |
|  Communication | ​ |  |  | A record of information transmitted from a sender to a receiver<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (com-1): Not Done Reason can only be specified if NotDone is "true" |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 1..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Communication-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Unique identifier |
|  - - system | 0..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value |
|  - - value | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - medium | 0..* | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | A channel of communication<br/>Binding (example): Codes for communication mediums such as phone, fax, email, in person, etc. [Participation-Mode](http://hl7.org/fhir/stu3/v3/ParticipationMode/vs.html)<br/><font color='red'>This example ValueSet MUST not be used the follow ValueSet from NHS Data Dictionary should be used instead </font>[CONSULTATION MEDIUM USED](https://www.datadictionary.nhs.uk/data_dictionary/attributes/c/cons/consultation_medium_used_de.asp?shownav=1?query=%22CONSULTATION+MEDIUM+USED&rank=100&shownav=1) <br/><font color='red'><b>Mapping to Maternity data item = 'Consultation method'</b></font> |
|  - - coding | 0..* | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - system | 0..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'https://www.datadictionary.nhs.uk'</font> |
|  - - - code | 0..1 | Required | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>The code MUST be  from the stated ValueSet</font> |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>The display MUST be the text associated with the code</font> |

## Mapping for Attendance Details EpisodeOfCare ##

|>|Level 1|[EpisodeOfCare Resource](http://hl7.org/fhir/stu3/episodeofcare.html)|>|Level 2|[CareConnect-EpisodeOfCare-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-EpisodeOfCare-1)|>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_attendance_details_all.html#mapping-for-attendance-details-episodeofcare)**|  

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| --- | --- | --- | --- | --- |
|  EpisodeOfCare | ​ |  |  | An association of a Patient with an Organization and Healthcare Provider(s) for a period of time that the Organization assumes some level of responsibility<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 1..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-EpisodeOfCare-1'</font>"<br/> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business Identifier(s) relevant for this EpisodeOfCare |
|  - - system | 0..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value |
|  - - value | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | planned : waitlist : active : onhold : finished : cancelled : entered-in-error<br/>Binding (required): The status of the episode of care. [EpisodeOfCareStatus](http://hl7.org/fhir/stu3/valueset-episode-of-care-status.html)<br/><font color='red'>This MUST contain the value 'finished'</font> |
|  - type | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type/class - e.g. specialist referral, disease management<br/>Binding (example): The type of the episode of care [EpisodeOfCareType](http://hl7.org/fhir/stu3/valueset-episodeofcare-type.html)<br/><font color='red'>This example ValueSet MUST NOT be used.</font> The Data Dictionary [SERVICE](https://www.datadictionary.nhs.uk/data_dictionary/attributes/s/ser/service_or_team_type_referred_to_for_community_care_de.asp?shownav=1) ValueSet should be used instead.  <br/><font color='red'><b>Mapping to Maternity data item = 'Service'</b></font> |
|  - - coding | 0..* | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - system | 0..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - code | 0..1 | Required | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - patient | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | The patient who is the focus of this episode of care<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the EpisodeOfCare.</font> |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color='red'>This is the subject of the Episode of Care. This MUST use the CareConnect patient profile.</font> <br/>See [patient resource ](https://nhsconnect.github.io/FHIR-Maternity-Record/explore_attendance_details.html#patient-reference) reference for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle.</font> |


## Mapping for Attendance Details Location ##

The attendance details scales details has reference(s) to the Location resource. This means that any exchange of the attendance details heading data must also include the [Location Details.](explore_location.html#mapping-for-location)

## Mapping for Attendance Details Practitioner ##

The attendance details has reference(s) to the Practitioner resource. This means that any exchange of the attendance details heading data must also include the [Practitioner Details.](explore_practitioner.html#mapping-for-practitioner)

## Mapping for Attendance Details PractitionerRole ##

The attendance details has reference(s) to the Practitioner Role resource. This means that any exchange of the attendance details heading data must also include the [Practitioner Role Details.](explore_practitioner_role.html#mapping-for-practitioner_role)


## Attendance Details Heading Example ##

<script src="https://gist.github.com/IOPS-DEV/6017a8a572e62dc45106b60311425ab4.js"></script>