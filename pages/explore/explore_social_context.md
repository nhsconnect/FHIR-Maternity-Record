---
title: Social Context Bundle
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_social_context_person.html
summary: "The FHIR profiles used for the Social context Bundle"
---

## Heading Description ##
The social setting in which the woman lives, such as their household, occupational history, and lifestyle factors.

|**Data Standard Element**|**FHIR Profile**|**FHIR target**|
|Date/Time|[Observation](explore_social_context_person.html#mapping-for-social-context-details-list)|
|Stage of Conception|[Observation](explore_social_context_person.html#mapping-for-social-context-details-list)|
|Social Circumstances|[Observation](explore_social_context_person.html#social-context-observation-data-item---social-circumstances)|
|Lifestyle|[Observation](explore_social_context_person.html#social-context-observation-data-item---lifestyle)|
|Smoking Status|[Observation](explore_social_context_person.html#social-context-observation-data-item---smoking-details)|
|Smoking Status- details|[Observation](explore_social_context_person.html#social-context-observation-data-item---smoking-details)|
|Type of Nicotine Replacement used|[Observation](explore_social_context_person.html#social-context-observation-data-item---smoking-details)|
|CO Screning Status|[Observation](explore_social_context_person.html#social-context-observation-data-item---co-screening-status)|
|CO Screening Result|[Observation](explore_social_context_person.html#social-context-observation-data-item---co-screening-result)|
|Date stopped smoking|[Observation](explore_social_context_person.html#social-context-observation-data-item---smoking-details)|
|Drug/substance use|[Observation](explore_social_context_person.html#social-context-observation-data-item---drug-substance-use)|
|Drug/substance use - details|[Observation](explore_social_context_person.html#social-context-observation-data-item---drug-substance-use)|
|Date stopped|[Observation](explore_social_context_person.html#social-context-observation-data-item---drug-substance-use)|
|Alcohol use|[Observation](explore_social_context_person.html#social-context-observation-data-item---alcohol-use)|
|Alcohol use - details|[Observation](explore_social_context_person.html#social-context-observation-data-item---alcohol-use)|
|Alcohol drinking status|[Observation](explore_social_context_person.html#social-context-observation-data-item---alcohol-drinking-status)|
|Date stopped usual pattern of drinking|[Observation](explore_social_context_person.html#social-context-observation-data-item---alcohol-use)|
|Education Level|[Observation](explore_social_context_person.html#social-context-observation-data-item---education)|
|Number of years in Education|[Observation](explore_social_context_person.html#social-context-observation-data-item---education)|
|Employment status|[Observation](explore_social_context_person.html#social-context-observation-data-item---employment-status)|
|Occupation|[Observation](explore_social_context_person.html#social-context-observation-data-item---occupation)|
|Asylum Status|[Observation](explore_social_context_person.html#social-context-observation-data-item---asylum-status)|


## Social Context Details Structure ##

{% include custom/Social_Context.svg %}

## Mapping for Social Context Details List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2| None|>|Level 3|[CareConnect-List-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_social_context_person.html#mapping-for-social-context-details-list)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business identifier<br/><font color='red'>An identifier for this Social Context details list</font><br/> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique<br/>Business identifier<br/><font color='red'>An identifier for this Social Context details list</font> |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource<br/><font color='red'>The organization that allocated the identifier</font> |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | current : retired : entered-in-error<br/>Binding (required): The current state of the list [ListStatus](http://hl7.org/fhir/stu3/valueset-list-status.html)<br/><font color='red'>The status of the list MUST contain the value 'current'</font> |
|  - mode | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | working : snapshot : changes<br/>Binding (required): The processing mode that applies to this list [ListMode](http://hl7.org/fhir/stu3/valueset-list-mode.html)<br/><font color='red'>The mode of the list MUST contain the value 'snapshot'</font> |
|  - title | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Descriptive name for the list<br/><font color='red'>This MUST contain the value 'Social Context'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading Social Context'</b></font>  |
|  - code | 0..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | What the purpose of this list is<br/>Binding (preferred): What the purpose of a list is [CareConnect-ListCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListCode-1)<br/><font color='red'>The PRSB heading for this list. Note: for Maternity the value stated below is used which is not from the preferred value set </font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/><font color='red'>The SNOMED CT concept for the PRSB heading type</font> |
|  - - - system | 0..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value '163011000000101'</font> |
|  - - - display | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>This MUST contain the value 'Social Context''</font><br/><font color='red'>Mapping to Maternity data item = 'PSRB Heading Social Context details'</font>  |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color='red'>This is the subject of the Social Context details List.<br/>This MUST use the CareConnect patient profile. </font>See[patient resource reference](explore_social_context_person.html#patient-reference) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - date | 0..1 | Mandatory | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the list was prepared<br/><font color='red'> This MUST contain a system date to indicate when the list created or updated</font> |
|  - note | 0..* | Optional | [Annotation](http://hl7.org/fhir/stu3/datatypes.html#annotation "Annotation") | Comments about the list |
|   |  | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | <font color='red'>Who authored the comment on the list.</font>  |
|  - - time | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the annotation was made |
|  - - text | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The annotation - text content |
|  - entry | 0..* | Mandatory | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Entries in the list<br/><font color='red'>The entries MUST be as per the diagram for this PRSB headings list with the encounter resource being the focal resource. Multiple Encounters with associated resources MAY be present</font> |
|  - - date | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When item added to list<br/><font color='red'>The SHOULD contain a system time of when the item was added to the list.</font> |
|  - - item | 1..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>The reference to the included Encounter resource.</font> |

## Mappings for Social Context Person List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2| None|>|Level 3|[CareConnect-List-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_social_context_all.html#mappings-for-social-context-person-list)**|


|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business identifier<br/><font color='red'>An identifier for this Social Context details list</font><br/> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique<br/>Business identifier<br/><font color='red'>An identifier for this Social Context details list</font> |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource<br/><font color='red'>The organization that allocated the identifier</font> |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | current : retired : entered-in-error<br/>Binding (required): The current state of the list [ListStatus](http://hl7.org/fhir/stu3/valueset-list-status.html)<br/><font color='red'>The status of the list MUST contain the value 'current'</font> |
|  - mode | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | working : snapshot : changes<br/>Binding (required): The processing mode that applies to this list [ListMode](http://hl7.org/fhir/stu3/valueset-list-mode.html)<br/><font color='red'>The mode of the list MUST contain the value 'snapshot'</font> |
|  - title | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Descriptive name for the list<br/><font color='red'>This MUST contain the value 'Social Context'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading Social Context'</b></font>  |
|  - code | 0..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | What the purpose of this list is<br/>Binding (preferred): What the purpose of a list is [CareConnect-ListCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListCode-1)<br/><font color='red'>The PRSB heading for this list. Note: for Maternity the value stated below is used which is not from the preferred value set </font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/><font color='red'>The SNOMED CT concept for the PRSB heading type</font> |
|  - - - system | 0..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value '163041000000100'</font> |
|  - - - display | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>This MUST contain the value 'Lifestyle - care record element (record artifact)''</font><br/><font color='red'>Mapping to Maternity data item = 'PSRB Heading Social Context Person Details'</font>  |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color='red'>This is the subject of the Social Context details List.<br/>This MUST use the CareConnect patient profile. </font>See[patient resource reference](explore_social_context_person.html#patient-reference) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - date | 0..1 | Mandatory | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the list was prepared<br/><font color='red'> This MUST contain a system date to indicate when the list created or updated</font> |
|  - note | 0..* | Optional | [Annotation](http://hl7.org/fhir/stu3/datatypes.html#annotation "Annotation") | Comments about the list |
|   |  | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | <font color='red'>Who authored the comment on the list.</font>  |
|  - - time | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the annotation was made |
|  - - text | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The annotation - text content |
|  - entry | 0..* | Mandatory | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Entries in the list<br/><font color='red'>The entries MUST be as per the diagram for this PRSB headings list with the Observation resource being the focal resource. Multiple Observations with associated resources MAY be present</font> |
|  - - date | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When item added to list<br/><font color='red'>The SHOULD contain a system time of when the item was added to the list.</font> |
|  - - item | 1..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>The reference to the included Encounter resource.</font> |

## Patient Reference ##

The social context (person) list has a mandated subject reference to the Patient resource. This means that any exchange of the spcial context (person) heading data must also include the [Patient demographics List.](explore_patient_demographics.html)

## Generic Mappings for Social Context Person Observation ##

|>|Level 1|[Observation Resource](http://hl7.org/fhir/stu3/observation.html)|>|Level 2| None|>|Level 3|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_social_context_all.html#generic-mappings-for-social-context-person-observation)**|


|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color="red">The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1'</font> |
|  - identifier | 0..* | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business Identifier for observation |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | registered : preliminary : final : amended +<br/>Binding (required): Codes providing the status of an observation. [ObservationStatus](http://hl7.org/fhir/stu3/valueset-observation-status.html) |
|  - category | 0..* | Required | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Classification of type of observation<br/>Binding (preferred): Codes for high level observation categories. [Observation Category Codes](http://hl7.org/fhir/stu3/valueset-observation-category.html)<br/><font color="red">Stage of Conception</font><br/><font color="red">Field to indicate what stage of the conception process the social context fields are being recorded for</font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - system | 0..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color="red">This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color="red">A concept from SNOMED CT Termonology</font> |
|  - - - display | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color="red">A SNOMED CT description that MUST match the concept code used</font> |
|SPECIFIC MAPPING SECTION (CODE)- START|||||
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who and/or what this is about<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - effective[x] | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Clinically relevant time/time-period for observation<br/><font color="red">Date and time the social context (person) information was recorded</font> |
|   |  | Mandatory | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") |  |
|SPECIFIC MAPPING SECTION (VALUE) - START|||||
|  - comment | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Comments about result |

## Data Item Specific Mappings ##

The following sections contain mappings for social context person data items. These should be used to create a data item specific observation entry. Each data item within social context is made up of an individual observation. The diagram below provides a basic visual indication of this process.

<img src="images/social_context_2.png" style="width:80%;max-width: 80%;">

## Social Context Observation Data Item - Social Circumstances ##

|>|Level 1|[Observation Resource](http://hl7.org/fhir/stu3/observation.html)|>|Level 2| None|>|Level 3|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_social_context_all.html#social-context-observation-data-item---social-circumstances)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of observation (code / type)<br/>Binding (example): Codes identifying names of simple observations. [LOINC Codes](http://hl7.org/fhir/stu3/valueset-observation-codes.html)<br/><font color="red">A SNOMED concept that represents the PRSB maternity data item 'Social Circumstances'</font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system describing a type of observation [CareConnect-ObservationType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ObservationType-1) |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color="red">TBA</font><br/> |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color="red">TBA</font> |
|  - value[x] | 0..1 | Required | [Quantity](http://hl7.org/fhir/stu3/datatypes.html#quantity "Quantity") | Actual result<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present |
|   |  | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") |  |

## Social Context Observation Data Item - Lifestyle ##

|>|Level 1|[Observation Resource](http://hl7.org/fhir/stu3/observation.html)|>|Level 2| None|>|Level 3|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_social_context_all.html#social-context-observation-data-item---lifestyle)**|


|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - **code** | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of observation (code / type)<br/>Binding (example): Codes identifying names of simple observations. [LOINC Codes](http://hl7.org/fhir/stu3/valueset-observation-codes.html)<br/><font color="red">A SNOMED concept that represents the PRSB maternity data item 'Social Circumstances'</font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system describing a type of observation [CareConnect-ObservationType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ObservationType-1) |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color="red">TBA</font><br/> |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color="red">TBA</font> |
|  - value[x] | 0..1 | Required | [Quantity](http://hl7.org/fhir/stu3/datatypes.html#quantity "Quantity") | Actual result<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present |
|   |  | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") |  |

## Social Context Observation Data Item - Smoking Details ##

## Multiple Data Items in this Observation ##

|Smoking Status|[Observation](explore_social_context_person.html#mapping-for-social-context-details-list)|
|Smoking Status- details|[Observation](explore_social_context_person.html#mapping-for-social-context-details-list)|
|Type of Nicotine Replacement used|[Observation](explore_social_context_person.html#mapping-for-social-context-details-list)|
|Date stopped smoking|[Observation](explore_social_context_person.html#social-context-observation-data-item---smoking-details)|

|>|Level 1|[Observation Resource](http://hl7.org/fhir/stu3/observation.html)|>|Level 2| None|>|Level 3|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_social_context_all.html#social-context-observation-data-item---smoking-details)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of observation (code / type)<br/>Binding (example): Codes identifying names of simple observations. [LOINC Codes](http://hl7.org/fhir/stu3/valueset-observation-codes.html)<br/><font color="red"><font color="red">A SNOMED CT concept from the Smoking simple reference set </font></font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system describing a type of observation [CareConnect-ObservationType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ObservationType-1) |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color="red">A code from the SNOMEd reference set '999000891000000102'</font> |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color="red">A description from the simple reference set that matches the given SNOMED CT code</font> |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - effective[x] | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Clinically relevant time/time-period for observation<br/><font color="red">Date stopped smoking</font> |
|  - comment | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Comments about result<br/><font color="red">Smoking status details</font> |
|  - component | 0..* | Required | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Component results<br/><font color="red">The type of nicotine replacement product used if applicable</font> |
|  - - code | 1..1 | Required | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of component observation (code / type)<br/>Binding (example): Codes identifying names of simple observations. [LOINC Codes](http://hl7.org/fhir/stu3/valueset-observation-codes.html) |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system describing a type of observation [CareConnect-ObservationType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ObservationType-1) |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |


## Social Context Observation Data Item - CO Screening Status ##

|>|Level 1|[Observation Resource](http://hl7.org/fhir/stu3/observation.html)|>|Level 2| None|>|Level 3|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_social_context_all.html#social-context-observation-data-item---co-screening-status)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of observation (code / type)<br/><font color="red">A code to describe the CO Screening Status</font> |
|  - - coding | 0..* | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | <font color="red">Where a clinical coding terminology is available this MUST be used'</font> |
|  - - coding (snomedCT) | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system describing a type of observation [CareConnect-ObservationType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ObservationType-1) |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color="red">Code for CO Screening Satus from a suitable Terminology</font><br/> |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color="red">A description to match with the code provided by the terminology system used</font> |
|  - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept<br/><font color="red">Where a termonology is unavailable, a text narrative MAY be used as an alternative</font> |
|  - value[x] | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Actual result<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present |

## Social Context Observation Data Item - CO Screening Result ##

|>|Level 1|[Observation Resource](http://hl7.org/fhir/stu3/observation.html)|>|Level 2| None|>|Level 3|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_social_context_all.html#social-context-observation-data-item---co-screening-result)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of observation (code / type)<br/><font color="red">A code to describe the CO Screening Result</font> |
|  - - coding | 0..* | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | <font color="red">Where a clinical coding terminology is available this MUST be used'</font> |
|  - - coding (snomedCT) | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system describing a type of observation [CareConnect-ObservationType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ObservationType-1) |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color="red">Code for CO Screening Result from a suitable Terminology</font><br/> |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color="red">A description to match with the code provided by the terminology system used</font> |
|  - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept<br/><font color="red">Where a termonology is unavailable, a text narrative MAY be used as an alternative</font> |
|  - value[x] | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Actual result<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present |


## Social Context Observation Data Item - Drug Substance Use ##

## Multiple Data Items in this Observation ##

|Drug/substance use|[Observation](explore_social_context_person.html#mapping-for-social-context-details-list)|
|Drug/substance use - details|[Observation](explore_social_context_person.html#mapping-for-social-context-details-list)|
|Date stopped|[Observation](explore_social_context_person.html#mapping-for-social-context-details-list)|

|>|Level 1|[Observation Resource](http://hl7.org/fhir/stu3/observation.html)|>|Level 2| None|>|Level 3|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_social_context_all.html#social-context-observation-data-item---drug-substance-use)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maernity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of observation (code / type)<br/><font color="red">Drug / Substance usage details</font> |
|  - - coding | 0..* | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system describing a type of observation [CareConnect-ObservationType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ObservationType-1) |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color="red">Coded text - SNOMED CT 361055000 \| Misuses drugs OR 371422002 \| History of substance abuse OR 228368007 \| Has never misused drugs OR 783241000000102 \| Declined to give substance misuse history</font> |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color="red">This SHOULD be the preferred term for the SNOMED concept</font> |
|  - effective[x] | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Clinically relevant time/time-period for observation<br/><font color="red">The date the person stopped using the drug/substance</font> |
|  - component | 0..* | Optional | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Component results<br/><font color="red">Detailed history of drug/substance use</font> |
|  - - text | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |



## Social Context Observation Data Item - Alcohol Use ##

## Multiple Data Items in Observation ##

|Alcohol use|[Observation](explore_social_context_person.html#social-context-observation-data-item---alcohol-use)|
|Alcohol use - details|[Observation](explore_social_context_person.html#social-context-observation-data-item---alcohol-use)|
|Date stopped usual pattern of drinking|[Observation](explore_social_context_person.html#social-context-observation-data-item---alcohol-use)|

|>|Level 1|[Observation Resource](http://hl7.org/fhir/stu3/observation.html)|>|Level 2| None|>|Level 3|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_social_context_all.html#social-context-observation-data-item---alcohol-use)**|


|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maernity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of observation (code / type)<br/><font color="red">Alcohol usage details</font> |
|  - - coding | 0..* | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system describing a type of observation [CareConnect-ObservationType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ObservationType-1) |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color="red">Coded text - SNOMED CT 219006 \| Current drinker of alcohol (finding) OR 105542008 \| current non-drinker of alcohol OR 228274009 \| Lifetime non-drinker OR 1104551000000109 \| Declined to provide information about alcholol use OR 371434005 \| History of alcohol abuse</font> |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color="red">This SHOULD be the preferred term for the SNOMED concept</font> |
|  - effective[x] | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Clinically relevant time/time-period for observation<br/><font color="red">The date the person stopped usual pattern of drinking</font> |
|  - component | 0..* | Optional | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Component results<br/><font color="red">Detailed history of alcohol e use</font> |
|  - - text | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |


## Social Context Observation Data Item - Alcohol Drinking Status ##

|>|Level 1|[Observation Resource](http://hl7.org/fhir/stu3/observation.html)|>|Level 2| None|>|Level 3|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_social_context_all.html#social-context-observation-data-item---alcohol-drinking-status)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maernity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of observation (code / type)<br/><font color="red">Alcohol Status details</font> |
|  - - coding | 0..* | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system describing a type of observation [CareConnect-ObservationType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ObservationType-1) |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color="red">Coded text - SNOMED CT 777651000000101 \| Higher risk alcohol drinking (finding) OR 66590003 \| Alcohol dependence (disorder) OR 105542008 \| Current non-drinker of alcohol (finding) OR 160580001 \|Alcohol consumption unknown (finding) OR 160593006 \| Alcohol intake within recommended sensible limits (finding)</font> |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color="red">This SHOULD be the preferred term for the SNOMED concept</font> |
|  - effective[x] | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Clinically relevant time/time-period for observation<br/><font color="red">The date the person stopped usual pattern of drinking</font> |
|  - component | 0..* | Not Used | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Component results<br/><font color="red">Detailed history of alcohol e use</font> |
|  - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |


## Social Context Observation Data Item - Education ##

## Multiple Data Items in Observation ##

|Education Level|[Observation](explore_social_context_person.html#mapping-for-social-context-details-list)|
|Number of years in Education|[Observation](explore_social_context_person.html#mapping-for-social-context-details-list)|

|>|Level 1|[Observation Resource](http://hl7.org/fhir/stu3/observation.html)|>|Level 2| None|>|Level 3|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_social_context_all.html#social-context-observation-data-item---education)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maernity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of observation (code / type)<br/><font color="red">Education Details</font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>Codesystem TBA</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color="red">Codes TBA</font> |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color="red">TBA</font> |
|  - - text | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - value[x] | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Actual result<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/><font color="red">The number of years that the person spent in education</font> |

## Social Context Observation Data Item - Employment Status ##

|>|Level 1|[Observation Resource](http://hl7.org/fhir/stu3/observation.html)|>|Level 2| None|>|Level 3|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_social_context_all.html#social-context-observation-data-item---employment-status)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maernity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of observation (code / type)<br/><font color="red">Employment Status</font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>Codesystem TBA</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color="red">Codes TBA</font> |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color="red">TBA</font> |
|  - - text | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |


## Social Context Observation Data Item - Occupation ##

|>|Level 1|[Observation Resource](http://hl7.org/fhir/stu3/observation.html)|>|Level 2| None|>|Level 3|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_social_context_all.html#social-context-observation-data-item---occupation)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maernity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of observation (code / type)<br/><font color="red">Occupation</font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>Codesystem TBA</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color="red">Codes TBA</font> |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color="red">TBA</font> |
|  - - text | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |

## Social Context Observation Data Item - Asylum Status ##

|>|Level 1|[Observation Resource](http://hl7.org/fhir/stu3/observation.html)|>|Level 2| None|>|Level 3|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_social_context_person.html#social-context-observation-data-item---asylum-status)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maernity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of observation (code / type)<br/><font color="red">Asylum Status</font> |
|  - - coding | 0..* | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system describing a type of observation [CareConnect-ObservationType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ObservationType-1) |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color="red">Coded text - SNOMED CT 390790000 \| Asylum seeker (person) OR 446654005 \| Refugee (person) OR 729851000000109 \| Asylum seeker with discretionary leave to remain (person) OR 729851000000109 \|Asylum seeker with discretionary leave to remain (person) OR 160702009 \| Illegal migrant (finding)(TBA) OR 224619008 \| Migrant (person)(TBA)</font> |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color="red">This SHOULD be the preferred term for the SNOMED concept</font> |
|  - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |

## Social Context Observation Data Item - Social Risk Factors ##

|>|Level 1|[Observation Resource](http://hl7.org/fhir/stu3/observation.html)|>|Level 2| None|>|Level 3|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_social_context_person.html#social-context-observation-data-item---social-risk-factors)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maernity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of observation (code / type)<br/><font color="red">Social Risk Factors</font> |
|  - - coding | 0..* | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system describing a type of observation [CareConnect-ObservationType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ObservationType-1) |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color="red">TBA</font> |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color="red">This SHOULD be the preferred term for the SNOMED concept</font> |
|  - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |


## Patient Reference ##

The social context person details list has a mandated subject reference to the Patient resource. This means that any exchange of the social context person details heading data must also include the [Patient demographics List.](explore_patient_demographics.html)


## Social Context Person Observation Details Heading Example ##

<script src="https://gist.github.com/IOPS-DEV/89bf5d2e8ab396d94c5d6647d1f86e1a.js"></script>

