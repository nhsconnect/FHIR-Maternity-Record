---
title: Vaccinations Bundle
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_vaccinations.html
summary: "The FHIR profiles used for the Vaccinations Bundle"
---

## Heading Description ##
The details of a women’s vaccinations.

## Vaccinations Details Structure ##

{% include custom/vaccinations.svg %}

## Maternity Data Standards Mapping to FHIR profiles ##

## Mapping Overview ##

|**Data Standard Element**|**FHIR Profile**|**FHIR target**|
|Date and Time of vaccinations|[Encounter](explore_vaccinations_details.html#mapping-for-vaccinations-details-encounter)|period.start|
|ODS/ORD Site Code|[Location](explore_vaccinations_details.html#mapping-for-vaccinations-details-location)|identifier|
|Performing Professional|[Practitioner](explore_vaccinations_details.html#mapping-for-vaccinations-details-practitioner)|identifier and name|
|SDS Job Role Name| [PractitionerRole](explore_vaccinations.html#mapping-for-vaccination-practitioner-role)|code|
|Reported Date|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|date|
|Primary Source|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|primarySource|
|Report Origin|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|reportOrigin|
|Vaccination Procedure|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|extension.vaccinationProcedure|
|Vaccination Situation (Not Given Outcome)|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|explanation.reasonNotGiven|
|Not Given flag|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|notGiven|
|Dose sequence|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|vaccinationProtocol.doseSequence|
|Vaccine Product|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|vaccineCode.coding.code|
|Vaccine Manufacturer|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|manufacturer|
|Batch Number|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|lotNumber|
|Site of Vaccination|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|site|
|Route of Vaccination|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|route|
|Dose Amount|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|doseQuantity|
|Indication|[Immunization](explore_vaccinations.html#mapping-for-vaccinations)|reason|


## Mapping for Vaccination Details List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2| None|>|Level 3|[CareConnect-List-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_vaccinations_all.html#mapping-for-vaccination-details-list)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business identifier<br/><font color='red'>An identifier for this vaccination details list</font><br/> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique<br/>Business identifier<br/><font color='red'>An identifier for this vaccination details list</font> |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource<br/><font color='red'>The organization that allocated the identifier</font> |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | current : retired : entered-in-error<br/>Binding (required): The current state of the list [ListStatus](http://hl7.org/fhir/stu3/valueset-list-status.html)<br/><font color='red'>The status of the list MUST contain the value 'current'</font> |
|  - mode | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | working : snapshot : changes<br/>Binding (required): The processing mode that applies to this list [ListMode](http://hl7.org/fhir/stu3/valueset-list-mode.html)<br/><font color='red'>The mode of the list MUST contain the value 'snapshot'</font> |
|  - title | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Descriptive name for the list<br/><font color='red'>This MUST contain the value 'Admission details'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading Immunisation details'</b></font>  |
|  - code | 0..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | What the purpose of this list is<br/>Binding (preferred): What the purpose of a list is [CareConnect-ListCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListCode-1)<br/><font color='red'>The PRSB heading for this list. Note: for Maternity the value stated below is used which is not from the preferred value set </font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/><font color='red'>The SNOMED CT concept for the PRSB heading type</font> |
|  - - - system | 0..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value '1102181000000102'</font> |
|  - - - display | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>This MUST contain the value 'Immunisations'</font><br/><font color='red'>Mapping to Maternity data item = 'PSRB Heading Immunisation details'</font>  |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color='red'>This is the subject of the vaccination details List.<br/>This MUST use the CareConnect patient profile. </font>See[patient resource reference](explore_vaccinations.html#patient-reference) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - date | 0..1 | Mandatory | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the list was prepared<br/><font color='red'> This MUST contain a system date to indicate when the list was created or updated</font> |
|  - note | 0..* | Optional | [Annotation](http://hl7.org/fhir/stu3/datatypes.html#annotation "Annotation") | Comments about the list |
|   |  | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | <font color='red'>Who authored the comment on the list.</font>  |
|  - - time | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the annotation was made |
|  - - text | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The annotation - text content |
|  - entry | 0..* | Mandatory | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Entries in the list<br/><font color='red'>The entries MUST be as per the diagram for this PRSB headings list with the encounter resource being the focal resource. Multiple Encounters with associated resources MAY be present</font> |
|  - - date | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When item added to list<br/><font color='red'>The SHOULD contain a system time of when the item was added to the list.</font> |
|  - - item | 1..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>A reference to an Encounter resource included in the list<br/>This MUST use the CareConnect Encounter profile. </font>See [Encounter resource](explore_vaccinations_details.html#mapping-for-vaccinations-details-encounter) for information on how to populate the resource. |
|  - - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>The reference to the included Encounter resource.</font> |

## Patient Reference ##

The Admission details list has a mandated subject reference to the Patient resource. This means that any exchange of the Admission details heading data must also include the [Patient demographics List.](explore_patient_demographics.html)

## Mapping for Vaccinations ##

|>|Level 1|[Immunization Resource](http://hl7.org/fhir/stu3/immunization.html)|>|Level 2| None|>|Level 3|[CareConnect-Immunization-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Immunization-1)|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_vaccinations_all.html#mapping-for-vaccinations)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | --- |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | Meta | Metadata about the resource |
|  - - profile | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Profiles this resource claims to conform to<br/><font color="red">The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-AllergyIntolerance-1'</font> |
|  - extension (vaccinationProcedure) | 0..1 | Required | [Extension-CareConnect-VaccinationProcedure-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-VaccinationProcedure-1 "Extension-CareConnect-VaccinationProcedure-1") | An extension to hold an immunization procedure code<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/><font color="red">Only use SNOMED CT coding or free text where no SNOMED CT code is available.</font><br/> |
|  - identifier | 0..* | Required | Identifier | Business identifier |
|  - - system | 1..1 | Mandatory | Uri | The namespace for the identifier value |
|  - - value | 1..1 | Mandatory | String | The value that is unique |
|  - - assigner | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - - display | 0..1 | Required | String | Text alternative for the resource |
|  - status | 1..1 | Mandatory | Code | Completed<br/>Binding (required): A set of codes indicating the current status of an Immunization [Immunization Status Codes](http://hl7.org/fhir/stu3/valueset-immunization-status.html)<br/><font color='red'>The status of the list MUST contain the value 'Completed'</font> |
|  - notGiven | 1..1 | Mandatory | Boolean | Flag for whether immunization was given<br/><font color="red">true = not given</font><br/><font color="red">false = given</font> |
|  - vaccineCode | 1..1 | Optional | CodeableConcept | Vaccine product administered<br/>Binding (extensible): The code for vaccine product administered [CareConnect-VaccineCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-VaccineCode-1) |
|  - - coding | 0..* | Optional | Coding | Code defined by a terminology system |
|  - - - system | 0..1 | Optional | Uri | Identity of the terminology system |
|  - - - code | 0..1 | Optional | Code | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Optional | String | Representation defined by the system |
|  - - text | 0..1 | Optional | String | Plain text representation of the concept |
|  - patient | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who was immunized<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL<br/><br/><font color='red'>This must use the CareConnect Patient profile.</font>See [patient resource reference](explore_vaccinations.html#patient-reference) for information on how to populate the resource |
|  - encounter | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Encounter administered as part of<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the vaccination encounter.</font> |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the encounter resource included in the vaccination list within the FHIR Bundle.</font>  |
|  - date | 0..1 | Mandatory | dateTime | Vaccination administration date<br/><font color="red">The date/time on which the immunisation intervention was carried out or was meant to be administered</font> |
|  - primarySource | 1..1 | Mandatory | Boolean | Indicates context the data was recorded in<br/>Default Value: true<br/><font color="red">false if reported</font> |
|  - reportOrigin | 0..1 | Required | CodeableConcept | Indicates the source of a secondarily reported record<br/>Binding (example): The source of the data for a record which is not from a primary source. [Immunization Origin Codes](http://hl7.org/fhir/stu3/valueset-immunization-origin.html) |
|  - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system |
|  - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system |
|  - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Mandatory | String | Representation defined by the system |
|  - location | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Where vaccination occurred<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL |
|  - manufacturer | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Vaccine manufacturer<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL |
|  - lotNumber | 0..1 | Optional | String | Vaccine lot number<br/><font color="red">The batch number of the vaccine product</font> |
|  - site | 0..1 | Optional | CodeableConcept | Body site vaccine was administered<br/>Binding (examle): The site at which the vaccine was administered [Codes for Immunization Site of Administration](http://hl7.org/fhir/stu3/valueset-immunization-site.html)<br/><font color="red">The immunization site does not use the preferred value set but uses SNOMED CT concepts instead Mapping to Maternity data item = 'site'.<br/><br/> |
|  - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Optional | Coding | Code defined by a terminology system<br/><font color="red">The immunization site does not use the preferred value set but uses SNOMED CT concepts instead Mapping to Maternity data item = 'site'. |
|  - - - extension (snomedCTDescriptionID) | 0..1 | Optional | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | The SNOMED CT Description ID for the display<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - system | 1..1 | Mandatory | Uri | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | Code | Symbol in syntax defined by the system<br/><font color="red">A SNOMED CT code</font> |
|  - - - display | 1..1 | Mandatory | String | Representation defined by the system<br/><font color="red">The display associated with the SNOMED CT concept. This SHOULD be the preferred term</font> |
|  - - text | 0..1 | Optional | String | Plain text representation of the concept<br/>This element SHOULD only be populated when the Immunisation cannot be coded or when stating one of the following statements: 'No known site' Or 'Information not available'. |
|  - route | 0..1 | Optional | CodeableConcept | How vaccine entered body<br/>Binding (example): The route by which the vaccine was administered [Immunization Route Codes](http://hl7.org/fhir/stu3/valueset-immunization-route.html)<br/><font color="red">Note the example valueSet is not used for Maternity and the following should be used instead<br/>Coded text - SNOMED CT (<284009009  |Route of administration value (qualifier value))</font> |
|  - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Optional | Coding | Code defined by a terminology system<br/>Binding (example): A code from the SNOMED Clinical Terminology UK coding system that describes the e-Prescribing route of administration. [CareConnect-MedicationDosageRoute-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-MedicationDosageRoute-1)<br/><font color="red">Note the example valueSet is not used for Maternity and the following should be used instead<br/>Coded text - SNOMED CT (<284009009  |Route of administration value (qualifier value))</font> |
|  - - - extension (snomedCTDescriptionID) | 0..1 | Optional | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | The SNOMED CT Description ID for the display<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - system | 1..1 | Mandatory | Uri | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | Code | Symbol in syntax defined by the system<br/><font color="red">Coded text - SNOMED CT (<284009009  |Route of administration value (qualifier value))</font> |
|  - - - display | 1..1 | Mandatory | String | Representation defined by the system<br/><font color="red">This SHOULD be the preferred term for the SNOMED concept</font> |
|  - - text | 0..1 | Optional | String | Plain text representation of the concept<br/><font color="red">This element SHOULD only be populated when the Immunisation cannot be coded or when stating one of the following statements: 'No known route' Or 'Information not available'.</font> |
|  - doseQuantity | 0..1 | Optional | [Quantity (SimpleQuantity )](http://hl7.org/fhir/stu3/StructureDefinition/SimpleQuantity "Quantity (SimpleQuantity )") | Amount of vaccine administered<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/>Constraint (sqty-1): The comparator is not used on a SimpleQuantity<br/><font color="red">Amount of vaccine administered</font> |
|  - - value | 0..1 | Required | Decimal | Numerical value (with implicit precision) |
|  - - unit | 0..1 | Required | String | Unit representation |
|  - - system | 0..1 | Required | Uri | System that defines coded unit form |
|  - - code | 0..1 | Required | Code | Coded form of the unit |
|  - practitioner | 0..* | Mandatory | BackboneElement | Who performed event |
|  - - role | 0..1 | Mandatory | CodeableConcept | What type of performance was done<br/>Binding (extensible): The role a practitioner plays in the immunization event [Immunization Role Codes](http://hl7.org/fhir/stu3/valueset-immunization-role.html) |
|  - - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system |
|  - - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system |
|  - - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Mandatory | String | Representation defined by the system |
|  - - - text | 0..1 | Optional | String | Plain text representation of the concept |
|  - - actor | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Individual who was performing<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color="red">This MUST be a reference to the Practitioner resource</font> |
|   |  | Required | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") | <font color='red'>The responsible clinician for the encounter.<br/>This MUST use the CareConnect Practitioner profile. </font>See [Practitioner resource](explore_vaccination_details.html#mapping-for-vaccination-details-encounter) for information on how to populate the resource. |
|  - - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL<br/>A reference to the Practitioner resource included in the Immunisation details list |
|  - note | 0..* | Optional | Annotation | Vaccination notes |
|  - explanation | 0..1 | Optional | BackboneElement | Administration/non-administration reasons<br/><font color="red">The clinical indication or reason for administering or recording an historical vaccination. </font> |
|  - - reason | 0..* | Optional | CodeableConcept | Why immunization occurred<br/>Binding (example): The reason why a vaccine was administered [CareConnect-ImmunizationExplanationReason-2 ](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ImmunizationExplanationReason-2) |
|  - - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system |
|  - - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system<br/><font color="red">This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Mandatory | String | Representation defined by the system |
|  - - reasonNotGiven | 0..1 | Required | CodeableConcept | Why immunization did not occur<br/>Binding (example): The reason why a vaccine was not administered [Immunization Reasons for Not Immunizing Codes](http://hl7.org/fhir/stu3/valueset-no-immunization-reason.html)<br/><font color="red">Where a vaccine is not administered a PROCEDURE WITH EXPLICIT CONTEXT (SNOMED CT). Codes TBA |
|  - - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system |
|  - - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system |
|  - - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Mandatory | String | Representation defined by the system |
|  - - - text | 0..1 | Optional | String | Plain text representation of the concept |
|  - vaccinationProtocol | 0..* | Mandatory | BackboneElement | What protocol was followed |
|  - - doseSequence | 1..1 | Required | positiveInt | Dose number within series<br/><font color="red">Nominal position in a series of vaccines</font> |


## Mapping for Vaccination Encounter ##

|>|Level 1|[Encounter Resource](http://hl7.org/fhir/stu3/encounter.html)|>|Level 2|[CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_vaccinations_all.html#mapping-for-vaccination-encounter)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  Encounter | ​ |  |  | An interaction during which services are provided to the patient<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Identifier(s) by which this encounter is known<br/><font color='red'>An identifier for this Encounter</font> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique<br/><font color='red'>An identifier for this Vaccination encounter</font> |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | planned : arrived : triaged : in-progress : onleave : finished : cancelled +<br/>Binding (required): Current state of the encounter [EncounterStatus](http://hl7.org/fhir/stu3/valueset-encounter-status.html)<br/><font color='red'>The status of the Encounter MUST contain the value 'finished'</font> |
|  - - - start | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - end | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - location | 0..1 | Required | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | List of locations where the patient has been |
|  - - location | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Location the encounter takes place<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>The site code of the location where teh vaccination was administered.</font> |
|   |  | Mandatory | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") | "<font color='red'>The location<br/>This MUST use the CareConnect Location profile. </font>See [Location resource](explore_vaccinations.html#mapping-for-vaccination-location) for information on how to populate the resource." |
|  - - - reference | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the Location resource included in the Vaccination list</font>  |

## Mapping for Vaccination Practitioner ##

|>|Level 1|[Practitioner Resource](http://hl7.org/fhir/stu3/practitioner.html)|>|Level 2|[CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_vaccinations_all.html#mapping-for-vaccination-practitioner)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  Practitioner | ​ |  |  | A person with a formal responsibility in the provisioning of healthcare or related services<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/><font color='red'>The name and designation of the consultant, who has overall responsibility for the person (may not actually see the person)</font> |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1'</font> |
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

## Mapping for Vaccination Practitioner Role ##


|>|Level 1|[PractitionerRole Resource](http://hl7.org/fhir/stu3/practitionerrole.html)|>|Level 2|[CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_vaccinations_all.html#mapping-for-vaccination-practitioner-role)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | Meta | Metadata about the resource<br/> |
|  - - profile | 0..* | Mandatory | Uri | Profiles this resource claims to conform to<br/><font color="red">The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1'</font> |
|  - identifier | 0..* | Mandatory | Identifier | Business Identifiers that are specific to a role/location |
|  - active | 0..1 | Required | Boolean | Whether this practitioner's record is in active use<br/>Default Value: true |
|  - period | 0..1 | Required | Period | The period during which the practitioner is authorized to perform in these role(s)<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - start | 0..1 | Required | dateTime | Starting time with inclusive boundary |
|  - - end | 0..1 | Required | dateTime | End time with inclusive boundary, if not ongoing |
|  - practitioner | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Practitioner that is able to provide the defined services for the organisation<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") | <font color='red'>The responsible clinician who performs the role.<br/>This MUST use the CareConnect Practitioner profile. </font>See [Practitioner resource](explore_vaccination_details.html#mapping-for-vaccination-details-encounter) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL |
|  - code | 0..* | Required | CodeableConcept | Roles which this practitioner may perform<br/>Slicing: Discriminator: coding.system, Ordering: false, Rules: Open at End<br/>Binding (example): The role a person plays representing an organization [PractitionerRole](http://hl7.org/fhir/stu3/valueset-practitioner-role.html) |
|  - code (sdsJobRoleName) | 0..1 | Required | CodeableConcept | Roles which this practitioner may perform<br/>Binding (required): The role a person plays representing an organization [CareConnect-SDSJobRoleName-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-SDSJobRoleName-1) |
|  - - coding | 1..1 | Mandatory | Coding | Code defined by a terminology system |
|  - - - system | 1..1 | Mandatory | Uri | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/CodeSystem/CareConnect-SDSJobRoleName-1'</font> |
|  - - - code | 1..1 | Mandatory | Code | Symbol in syntax defined by the system |
|  - - - display | 1..1 | Mandatory | String | Representation defined by the system |
|  - - text | 0..1 | Optional | String | Plain text representation of the concept |
|  - location | 0..* | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | The location(s) at which this practitioner provides care<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") | <font color='red'>The location where the clinician performed the vaccination.<br/>This MUST use the CareConnect Location profile. </font>See [Location resource](explore_vaccination_details.html#mapping-for-vaccination-details-location) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL |

## Mapping for Vaccination Location ##

|>|Level 1|[Location Resource](http://hl7.org/fhir/stu3/location.html)|>|Level 2|[CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_vaccinations_all.html#mapping-for-vaccination-location)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  Location | ​ |  |  | Details and position information for a physical place<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 1..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1'</font> |
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

## Vaccination Details Heading Example ##

<script src="https://gist.github.com/IOPS-DEV/f935da40d3c074aa95caa6f86c40c2d7.js"></script>
