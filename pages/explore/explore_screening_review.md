---
title: Screening Review Bundle
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_screening_review.html
summary: "The FHIR profiles used for the Screening Review Bundle"
---

## Heading Description ##

## Social Context Details Structure ##

{% include custom/screening_review.svg %}

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2| None|>|Level 3|[CareConnect-List-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_screening_review.html#mapping-for-screening-review-list)**|

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

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2| None|>|Level 3|[CareConnect-List-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_screening_review.html#mapping-for-screening-review-list)**|

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

## Mapping for National Antenatal Screening Programme Procedure Request ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/procedurerequest.html)|>|Level 2| None|>|Level 3|[CareConnect-Procedure-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-ProcedureRequest-1)|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_screening_review_all.html#mapping-for-diabetic-eye-screening-observation)**|

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

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/procedure.html)|>|Level 2| None|>|Level 3|[CareConnect-Procedure-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Procedure-1)|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_screening_review_all.html#mapping-for-diabetic-eye-screening-observation)**|

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

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/observation.html)|>|Level 2| None|>|Level 3|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_screening_review_all.html#mapping-for-diabetic-eye-screening-gestational-age-observation)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Observation-1'</font> |
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


## Mapping for Screening Practitioner ##

|>|Level 1|[Practitioner Resource](http://hl7.org/fhir/stu3/practitioner.html)|>|Level 2|[CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_screening_review_all.html#mapping-for-diabetic-eye-screening-practitioner)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Practitioner-1'</font> |
|  - identifier | 0..* | Mandatory | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | A identifier for the person as this agent<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open at End |
|  - identifier (sdsUserID) | 0..1 | Mandatory | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | A identifier for the person as this agent<br/><font color='red'>This will be the clinicians SDS identifier (GMC code)</font><br/><font color='red'><b>Mapping to Maternity Data set = 'Responsible Clinician Identifier'.</b></font> |
|  - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/Id/sds-user-id'</font> |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique<br/><font color='red'>This MUST contain the person's SDS user id</font> |
|  - name | 0..* | Required | [HumanName](http://hl7.org/fhir/stu3/datatypes.html#humanname "HumanName") | The name(s) associated with the practitioner |
|  - - text | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text representation of the full name<br/><font color='red'><b>Mapping to Maternity Data set = 'Responsible Clinician Name'.</b></font> |
|  - - family | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Family name (often called 'Surname') |
|  - - given | 0..* | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Given names (not always 'first'). Includes middle names |
|  - - prefix | 0..* | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Parts that come before the name |
|  - - suffix | 0..* | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Parts that come after the name |

## Mapping for Screening Practitioner Role ##

|>|Level 1|[PractitionerRole Resource](http://hl7.org/fhir/stu3/practitionerrole.html)|>|Level 2|[CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_screening_review_all.html#mapping-for-diabetic-eye-screening-practitioner-role)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | Meta | Metadata about the resource<br/> |
|  - - profile | 0..* | Mandatory | Uri | Profiles this resource claims to conform to<br/><font color="red">The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1'</font> |
|  - identifier | 0..* | Mandatory | Identifier | Business Identifiers that are specific to a role/location |
|  - active | 0..1 | Required | Boolean | Whether this practitioner's record is in active use<br/>Default Value: true |
|  - period | 0..1 | Required | Period | The period during which the practitioner is authorized to perform in these role(s)<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - start | 0..1 | Required | dateTime | Starting time with inclusive boundary |
|  - - end | 0..1 | Required | dateTime | End time with inclusive boundary, if not ongoing |
|  - practitioner | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Practitioner that is able to provide the defined services for the organisation<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") | <font color='red'>The responsible clinician who performs the role.<br/>This MUST use the CareConnect Practitioner profile. </font>See [Practitioner resource](explore_screening_review.html#mapping-for-diabetic-eye-screening-practitioner) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL |
|  - code | 0..* | Required | CodeableConcept | Roles which this practitioner may perform<br/>Slicing: Discriminator: coding.system, Ordering: false, Rules: Open at End<br/>Binding (example): The role a person plays representing an organization [PractitionerRole](http://hl7.org/fhir/stu3/valueset-practitioner-role.html) |
|  - code (sdsJobRoleName) | 0..1 | Required | CodeableConcept | Roles which this practitioner may perform<br/>Binding (required): The role a person plays representing an organization [CareConnect-SDSJobRoleName-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-SDSJobRoleName-1) |
|  - - coding | 1..1 | Mandatory | Coding | Code defined by a terminology system |
|  - - - system | 1..1 | Mandatory | Uri | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/CodeSystem/CareConnect-SDSJobRoleName-1'</font> |
|  - - - code | 1..1 | Mandatory | Code | Symbol in syntax defined by the system |
|  - - - display | 1..1 | Mandatory | String | Representation defined by the system |
|  - - text | 0..1 | Optional | String | Plain text representation of the concept |
|  - location | 0..* | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | The location(s) at which this practitioner provides care<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") | <font color='red'>The location where the clinician performed the vaccination.<br/>This MUST use the CareConnect Location profile. </font>See [Location resource](explore_vaccination_details.html#mapping-for-vaccination-details-location) for information on how to populate the resource. |
|  - - reference | 0..1 | Not Used | String | Literal reference, Relative, internal or absolute URL |

## Mapping for Diabetic Eye Screening Location ##

|>|Level 1|[Location Resource](http://hl7.org/fhir/stu3/location.html)|>|Level 2|[CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_screening_review_all.html#mapping-for-diabetic-eye-screening-location)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  Location | ​ |  |  | Details and position information for a physical place<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 1..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Location-1'</font> |
|  - identifier (odsSiteCode) | 0..1 | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | ODS Site code to identify the organisation at site level<br/><font color='red'>Site code of the unit to which the person was admitted</font> <br/><font color='red'><b>Maternity Data set mapping = 'ODS/ORD Site Code'</b></font> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | ODS Code<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/Id/ods-site-code'</font> |
|  - - value | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The ODS Site code name, to reflect the code used |
|  - type | 0..1 | Required | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of function performed<br/>Binding (extensible): Indicates the type of function performed at the location. [ServiceDeliveryLocationRoleType](http://hl7.org/fhir/stu3/v3/ServiceDeliveryLocationRoleType/vs.html )<br/><font color='red'><b>Maternity Date set mapping = 'Specialty admitted to'</b></font><br/><font color='red'>Note this valueset is defined as extensible and therefore if the code exists in this valueSet then that code MUST be used.</font> <br/> <font color='red'>Alternatively if the code does not exist in this valueSet then a code from the</font> [Activity Treatment Function Code](https://www.datadictionary.nhs.uk/data_dictionary/data_field_notes/a/act/activity_treatment_function_code_de.asp?shownav=1?query=%22ACTIVITY+TREATMENT+FUNCTION+CODE%22&rank=100&shownav=1) <font color='red'>valueSet MUST be used</font><br/>  |
|  - - coding | 0..* | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - system | 0..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>MUST contain the value 'http://hl7.org/fhir/stu3/v3/ServiceDeliveryLocationRoleType'</font> |
|  - - - code | 0..1 | Required | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the code which describes the speciality of the location.</font> |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>This MUST contain the display associated with the code</font> |
|  - physicalType | 0..1 | Required | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Physical form of the location<br/>Binding (example): Physical form of the location [LocationType](http://hl7.org/fhir/stu3/valueset-location-physical-type.html) |
|  - - text | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept<br/><font color='red'>This is the physical location of the person. E.g hospital ward, bed, theatre. For ambulatory care, eg, health centre, clinic, resource centre, person’s home maximum 150 characters</font><br/><font color='red'><b>Maternity Date set mapping = 'Patient Location'</b></font> |