---
title: Screening Review List
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_screening_review.html
summary: "The FHIR profiles used for the Screening Review List"
---

## Heading Description ##
The detais of the womans infectious diseases screening.

The following FHIR profiles are used to form the infectious diseases screemning review details list structure:

- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [CareConnect-ProcedureRequest-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-ProcedureRequest-1)
- [CareConnect-Procedure-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Procedure-1)
- [CareConnect-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)

The following profiles are referenced from the infectious diseases screening details list structure:

- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)

## Social Context Details Structure ##

{% include custom/screening_review.svg %}

## Mapping Overview ##


|Date/Time|[ProcedureRequest](explore_screening_review.html#mapping-for-national-antenatal-screening-programme-procedure-request)| authoredOn.DateTime|
|Performing Professional| [Procedure](explore_screening_review.html#mapping-for-national-antenatal-screening-programme-procedure)|performer.actor|
|SDS Job Role Name |[PractitionerRole]|(explore_practitioner_role.html)|code|
|Location|[Procedure](explore_screening_review.html#mapping-for-national-antenatal-screening-programme-procedure)|location |
|Gestational Age| [Observation](explore_screening_review.html#mapping-for-generic-screening-review-data-items-observation)|code + value |
|Screening Offer Status|[ProcedureRequest](explore_screening_review.html#mapping-for-national-antenatal-screening-programme-procedure-request)| code|
|Screening Declined|[Procedure](explore_screening_review.html#mapping-for-national-antenatal-screening-programme-procedure)|noDoneReason|
|Screening Process|[Procedure](explore_screening_review.html#mapping-for-national-antenatal-screening-programme-procedure)|code|
|Date/Time|[Observation](explore_screening_review.html#mapping-for-generic-screening-review-data-items-observation)|effective[x]|
|Screening Outcome - HIV|[Procedure](explore_screening_review.html#mapping-for-national-antenatal-screening-programme-procedure)|outcome|
|Screening Outcome - Syphilis|[Procedure](explore_screening_review.html#mapping-for-national-antenatal-screening-programme-procedure)|outcome|
|Screening Outcome - Hepatitis B|[Procedure](explore_screening_review.html#mapping-for-national-antenatal-screening-programme-procedure)|outcome|
|Comment|[Procedure](explore_screening_review.html#mapping-for-national-antenatal-screening-programme-procedure)|note|
|Outcome - Hepatitis C|[Procedure](explore_screening_review.html#mapping-for-national-antenatal-screening-programme-procedure)|outcome|
|Outcome Chlamydia|[Procedure](explore_screening_review.html#mapping-for-national-antenatal-screening-programme-procedure)|outcome|
|Screening Outcome - Bacteriuria |[Procedure](explore_screening_review.html#mapping-for-national-antenatal-screening-programme-procedure)|outcome|

## Mapping for Screening Review List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2| [CareConnect-List-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_screening_review.html#mapping-for-screening-review-list)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1'</font> |
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
|  - - - code | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value '1013971000000104'</font> |
|  - - - display | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>This MUST contain the value 'Antenatal screening (observable entity)''</font><br/><font color='red'>Mapping to Maternity data item = 'PSRB Heading 'Screening Review'</font>  |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color='red'>This is the subject of the Social Context details List.<br/>This MUST use the CareConnect patient profile. </font>See[patient resource reference](explore_social_context.html#patient-reference) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - date | 0..1 | Mandatory | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the list was prepared<br/><font color='red'> This MUST contain a system date to indicate when the list created or updated</font> |
|  - note | 0..* | Optional | [Annotation](http://hl7.org/fhir/stu3/datatypes.html#annotation "Annotation") | Comments about the list |
|   |  | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | <font color='red'>Who authored the comment on the list.</font>  |
|  - - time | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the annotation was made |
|  - - text | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The annotation - text content |
|  - entry | 0..* | Mandatory | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Entries in the list<br/><font color='red'>The entries MUST be as per the diagram for this PRSB headings list with the List resource being the focal resource. Multiple Lists with associated resources MAY be present</font> |
|  - - date | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When item added to list<br/><font color='red'>The SHOULD contain a system time of when the item was added to the list.</font> |
|  - - item | 1..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>The reference to the included List resource.</font> |

## Mapping for National Antenatal Screening Programme List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2| [CareConnect-List-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_screening_review_all.html#mapping-for-national-antenatal-screening-programme-list)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1'</font> |
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
|  - - - code | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value '1013971000000104'</font> |
|  - - - display | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>This MUST contain the value 'Antenatal screening (observable entity)''</font><br/><font color='red'>Mapping to Maternity data item = 'PSRB Heading 'Screening Review'</font>  |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color='red'>This is the subject of the Social Context details List.<br/>This MUST use the CareConnect patient profile. </font>See[patient resource reference](explore_social_context.html#patient-reference) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - date | 0..1 | Mandatory | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the list was prepared<br/><font color='red'> This MUST contain a system date to indicate when the list created or updated</font> |
|  - note | 0..* | Optional | [Annotation](http://hl7.org/fhir/stu3/datatypes.html#annotation "Annotation") | Comments about the list |
|   |  | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | <font color='red'>Who authored the comment on the list.</font>  |
|  - - time | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the annotation was made |
|  - - text | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The annotation - text content |
|  - entry | 0..* | Mandatory | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Entries in the list<br/><font color='red'>The entries MUST be as per the diagram for this PRSB headings. Multiple resources MAY be present</font> |
|  - - date | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When item added to list<br/><font color='red'>The SHOULD contain a system time of when the item was added to the list.</font> |
|  - - item | 1..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>The reference to the included resources.</font> |

## Patient Reference ##

The screening review details list has a mandated subject reference to the Patient resource. This means that any exchange of the screening review details heading data must also include the [Patient demographics List.](explore_patient_demographics.html)

## Mapping for National Antenatal Screening Programme Procedure Request ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/procedurerequest.html)|>|Level 2| [CareConnect-Procedure-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-ProcedureRequest-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_screening_review_all.html#mapping-for-national-antenatal-screening-programme-procedure-request)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| --- | --- | --- | --- | --- |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | Meta | Metadata about the resource |
|  - identifier | 0..* | Required | Identifier | Identifiers assigned to this order |
|  - - system | 0..1 | Required | Uri | The namespace for the identifier value |
|  - - value | 0..1 | Mandatory | String | The value that is unique |
|  - - assigner | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - - identifier | 0..1 | Required | Identifier | Logical reference, when literal reference is not known |
|  - status | 1..1 | Mandatory | Code | draft : active : suspended : completed : entered-in-error : cancelled<br/>Binding (required): The status of a procedure or diagnostic order. [RequestStatus](http://hl7.org/fhir/stu3/valueset-request-status.html)<br/><font color="red">MUST be set to 'completed'</font> |
|  - intent | 1..1 | Mandatory | Code | proposal : plan : order +<br/>Binding (required): The kind of procedure or diagnostic request [RequestIntent](http://hl7.org/fhir/stu3/valueset-request-intent.html)<br/><font color="red">Must be set to 'order'</font> |
|  - category | 0..* | Required | CodeableConcept | Classification of procedure<br/>Binding (example): Classification of the procedure [Procedure Category Codes (SNOMED CT)](http://hl7.org/fhir/stu3/valueset-procedure-category.html)<br/><font color="red">National Antenatal Screening Programme - Screening Category MUST be from the preferred valueset (SNOMED CT)( https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ScreeningProgramme-1)</font> |
|  - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system |
|  - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Mandatory | String | Representation defined by the system |
|  - - text | 0..1 | Optional | String | Plain text representation of the concept |
|  - code | 1..1 | Mandatory | CodeableConcept | What is being requested/ordered<br/><font color="red">Diabetic Eye Screening Process MUST be from the preferred valueset (SNOMED CT)( https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-DiabeticEyeScreeningTest-1)</font><br/><font color="red">Infectious Diseases Screening Process MUST be from the preferred valueset (SNOMED CT)( https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-InfectiousDiseasesTests -1)</font><br/><font color="red">FA Downs, Edwards and Pataus Process MUST be from the preferred valueset (SNOMED CT)( https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-FADownsPatausTests -1)</font><br/><font color="red">Sickle Cell and Thalassaemia Process MUST be from the preferred valueset (SNOMED CT)( https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-SickleCellThalassaemiaTests -1)</font><br/><font color="red">FA Structural Anomalies Process MUST be from the preferred valueset (SNOMED CT)( https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-FAStructuralAnomaliesTests -1)</font> |
|  - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system |
|  - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Mandatory | String | Representation defined by the system |
|  - - text | 0..1 | Optional | String | Plain text representation of the concept |
|  - subject | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Individual the service is ordered for<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|  - authoredOn | 0..1 | Mandatory | dateTime | Date request signed<br/><font color="red">Date when the screening test was offered</font> |


## Mapping for National Antenatal Screening Programme Procedure ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/procedure.html)|>|Level 2| [CareConnect-Procedure-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Procedure-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_screening_review_all.html#mapping-for-national-antenatal-screening-programme-procedure)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description/Constraints** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Required | Id | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | Meta | Metadata about the resource |
|  - - profile | 0..* | Mandatory | Uri | Profiles this resource claims to conform to<br/><font color="red">https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Procedure-1</font> |
|  - identifier | 0..* | Required | Identifier | External Identifiers for this procedure |
|  - - system | 1..1 | Required | Uri | The namespace for the identifier value |
|  - - value | 1..1 | Mandatory | String | The value that is unique |
|  - - assigner | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Required | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - - display | 0..1 | Required | String | Text alternative for the resource |
|  - status | 1..1 | Mandatory | Code | preparation \| in-progress \| suspended \| aborted \| completed \| entered-in-error \| unknown<br/>Binding (required): A code specifying the state of the procedure. [EventStatus](http://hl7.org/fhir/stu3/valueset-event-status.html)<br/><font color="red">Status MUST be 'completed'</font> |
|  - notDone | 0..1 | Required | Boolean | True if procedure was not performed as scheduled<br/>Default Value: false |
|  - notDoneReason | 0..1 | Required | CodeableConcept | Reason procedure was not performed<br/>Binding (example): A code that identifies the reason a procedure was not performed. [Procedure Not Performed Reason (SNOMED-CT)](http://hl7.org/fhir/stu3/valueset-procedure-not-performed-reason.html)<br/><font color="red">Details of the antenatal screening process declined. SNOMED CT code MUST be used and one of 763031007 \| Antenatal screening for human immunodeficiency virus refused OR TBA \| TBA OR 763030008 \|Antenatal screening for viral hepatitis type B refused </font><br/> |
|  - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system |
|  - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system |
|  - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Mandatory | String | Representation defined by the system |
|  - - text | 0..1 | Optional | String | Plain text representation of the concept |
|  - category | 0..1 | Required | CodeableConcept | Classification of the procedure<br/>Binding (example): A code that classifies a procedure for searching, sorting and display purposes. [Procedure Category Codes (SNOMED CT)](http://hl7.org/fhir/stu3/valueset-procedure-category.html)<br/><font color="red">National Antenatal Screening Programme - Screening Category MUST be from the preferred valueset (SNOMED CT)( https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ScreeningProgramme-1)</font> |
|  - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system |
|  - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system<br/><font color="red">MUST be a code from (SNOMED CT)( https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ScreeningProgramme-1)</font> |
|  - - - display | 0..1 | Mandatory | String | Representation defined by the system |
|  - - text | 0..1 | Optional | String | Plain text representation of the concept |
|  - code | 0..1 | Mandatory | CodeableConcept | Identification of the procedure<br/>Binding (preferred): A code to identify a specific procedure. [Procedure Codes (SNOMED CT)](http://hl7.org/fhir/stu3/valueset-procedure-code.html)<br/><font color="red">Diabetic Eye Screening Process MUST be from the preferred valueset (SNOMED CT)( https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-DiabeticEyeScreeningProcess-1)</font><br/><font color="red">Infectious Diseases Screening Process MUST be from the preferred valueset (SNOMED CT)( https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-InfectiousDiseasesProcess -1)</font><br/><font color="red">FA Downs, Edwards and Pataus Process MUST be from the preferred valueset (SNOMED CT)( https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-FADownsPatausProcess -1)</font><br/><font color="red">Sickle Cell and Thalassaemia Process MUST be from the preferred valueset (SNOMED CT)( https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-SickleCellThalassaemiaProcess -1)</font><br/><font color="red">FA Structural Anomalies Process MUST be from the preferred valueset (SNOMED CT)( https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-FAStructuralAnomaliesProcess -1)</font><br/><font color="red">Values used for screening process MUST be compatible with the values used in screening outcome</font> |
|  - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Mandatory | Coding | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK. [CareConnect-ProcedureCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ProcedureCode-1) |
|  - - extension (snomedCTDescriptionID) | 0..1 | Required | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | The SNOMED CT Description ID for the display<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - system | 1..1 | Mandatory | Uri | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | Code | Symbol in syntax defined by the system<br/><font color="red">134395001</font> |
|  - - - display | 1..1 | Mandatory | String | Representation defined by the system<br/><font color="red">Diabetic retinopathy screening (procedure)</font> |
|  - subject | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who the procedure was performed on<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL |
|  - performed[x] | 0..1 | Mandatory | dateTime | Date/Period the procedure was performed<br/><font color="red">The date/time the screening outcome was recorded</font> |
|  - performer | 0..* | Required | BackboneElement | The people who performed the procedure |
|  - - actor | 1..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | The reference to the practitioner<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Required | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") |  |
|  - location | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Where the procedure happened<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Required | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") |  |
|  - - reference | 0..1 | Required | String | Literal reference, Relative, internal or absolute URL |
|  - outcome | 0..1 | Mandatory | CodeableConcept | The result of procedure<br/><font color="red">Diabetic Eye Screening Outcome MUST be from the preferred valueset (SNOMED CT)( https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-DiabeticEyeScreeningOutcome-1)</font><br/><font color="red">Infectious Diseases Screening Outcome MUST be from the preferred valueset (SNOMED CT)( https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-InfectiousDiseasesOutcome-1)</font><br/><font color="red">FA Downs, Edwards and Pataus Outcome MUST be from the preferred valueset (SNOMED CT)( https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-FADownsPatausOutcome-1)</font><br/><font color="red">Sickle Cell and Thalassaemia Outcome MUST be from the preferred valueset (SNOMED CT)( https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-SickleCellThalassaemiaOutcome-1)</font><br/><font color="red">FA Structural Anomalies Outcome MUST be from the preferred valueset (SNOMED CT)( https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-FAStructuralAnomaliesOutcome-1)</font><br/><font color="red">Values used for screening outcome MUST be compatible with the values used in screening process</font> |
|  - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system |
|  - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system |
|  - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - display | 0..1 | Mandatory | String | Representation defined by the system<br/><font color="red">SNOMED CT \description tat MUST match code</font> |
|  - - text | 0..1 | Optional | String | Plain text representation of the concept<br/><font color="red">Free text field to be used if no coded text available</font> |

## Mapping for Generic Screening Review Data Items Observation ##

|Gestational Age|[Observation](explore_social_context_household.html#mapping-for-social-context-details-list)|
|Family Origins Questionnaire|[Observation](explore_social_context_household.html#mapping-for-social-context-details-list)|

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/observation.html)|>|Level 2| [CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1|>|Level 3|)None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_screening_review_all.html#mapping-for-generic-screening-review-data-items-observation)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business Identifier for observation<br/><font color='red'>An identifier for this Diabetic Screening Gestational Age Observation</font> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - - assigner | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | registered : preliminary : final : amended +<br/>Binding (required): Codes providing the status of an observation. [ObservationStatus](http://hl7.org/fhir/stu3/valueset-observation-status.html) |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of observation (code / type) |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system describing a type of observation [CareConnect-ObservationType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ObservationType-1) |
|  - - - extension (snomedCTDescriptionID) | 0..1 | Required | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | The SNOMED CT Description ID for the display.<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color="red">57036006</font> |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color="red">Fetal gestational age (observable entity)</font> |
|  - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who and/or what this is about<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|  - - identifier | 0..1 | Mandatory | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - effective[x] | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Clinically relevant time/time-period for observation<br/><font color="red">MUST only be used for Sickle Cell and Thalassaemia Family Origins Questionnaire completion date</font><br/> |
|  - value[x] | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Actual result<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/><font color="red">MUST contain gestational age value</font> |

## Mapping for Structural Anomalies Flag ##

|>|Level 1|[Location Resource](http://hl7.org/fhir/stu3/flag.html)|>|Level 2|[CareConnect-Flag-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Flag-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_screening_review_all.html#mapping-for-structural-anomalies-flag)**|

|  **Name** | **Card.** | Conformance | **Type** | **Description/Constraints** |
| :--- | :--- | --- | :--- | :--- |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business identifier |
|  - - - - system | 0..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - - assigner | 0..1 | Required | Reference | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - - reference | 0..1 | Required | Identifier | Logical reference, when literal reference is not known |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Coded or textual message to display to user<br/>Binding (example): Detail codes identifying specific flagged issues. ( http://hl7.org/fhir/stu3/valueset-flag-code.html )<br/><font color="red">Flag to indicate abnormal Antenatal Screening Ultrasound</font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | SNOMED CT representation identifying specific flagged issues |
|  - - - extension (snomedCTDescriptionID) | 0..1 | Optional | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | The SNOMED CT Description ID for the display<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>URL: https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/>Fixed Value: http://snomed.info/sct |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color="red">SNOMED CT code MUST be fixed to 169665005</font> |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color="red">SNOMED CT description must be fixed to Antenatal ultrasound scan abnormal</font> |
|  - - text | 0..1 | Optional | String | Plain text representation of the concept |
|  - subject | 1..1 | Mandatory | Reference | Who/What is flag about?<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | CareConnect-Patient-1 | <font color="red">This is the subject of the Screening Review List.</font><br/><font color="red">This MUST use the CareConnect patient profile</font><br/><font>See [patient resource reference](explore_screening_review.html#patient-reference) for information on how to populate the resource.</font> |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |

## Mapping for Screening Review Practitioner ##

The screening review details has reference(s) to the Practitioner resource. This means that any exchange of the screening review details heading data must also include the [Practitioner Details](explore_practitioner.html#mapping-for-practitioner)

## Mapping for Screening Review Practitioner Role ##

The screening review details has reference(s) to the Practitioner Role resource. This means that any exchange of the screening review details heading data must also include the [Practitioner Role Details](explore_practitioner_role.html#mapping-for-practitioner_role)

## Mapping for Screening Review Organisation ##

The screening review details has reference(s) to the Organization resource. This means that any exchange of the scan details details heading data must also include the [Organization Details](explore_organization.html)

## Mapping for Screening Review Location ##

The Screening Review details has reference(s) to the Location resource. This means that any exchange of the screening review details heading data must also include the [Location Details](explore_location.html#mapping-for-location)

## Screening Review Example ##

<script src="https://gist.github.com/IOPS-DEV/d67ae40be9978094c77f9a6c45b15911.js"></script>

