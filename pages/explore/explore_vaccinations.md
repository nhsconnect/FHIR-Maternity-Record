---
title: Vaccinations Bundle
keywords:  bundles
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_vaccinations.html
summary: "The FHIR profiles used for the Vaccinations Bundle"
---

## Heading Description ##
The details of a women’s immunisations.

## Vaccinations Details Structure ##

{% include custom/vaccinations.svg %}

## Maternity Data Standards Mapping to FHIR profiles ##

## Mapping Overview ##

|**Data Standard Element**|**FHIR Profile**|**FHIR target**|
|Date and Time of vaccinations|[Encounter](explore_vaccinations_details.html#mapping-for-vaccinations-details-encounter)|period.start|
|ODS/ORD Site Code|[Location](explore_vaccinations_details.html#mapping-for-vaccinations-details-location)|identifier|
|Professional Name|[Practitioner](explore_vaccinations_details.html#mapping-for-vaccinations-details-practitioner)|identifier and name|
|SDS Job Role Name|
|Encounter Type|[Encounter]
|Name of Immunisation|
|Dose sequence| 
|Outcome Status|
|Vaccine Product| 
|Vaccine Manufacturer| 
|Batch Number|
|Site|
|Route| 
|Dose Amount|
|Reported|

## Mapping for Immunisation Details List ##

|>|Level 1|[Bundle Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2| None|>|Level 3|[CareConnect-List-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_vaccinations_all.html#mapping-for-bundle)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  List | ​ |  |  | Information summarized from a list of other resources<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (lst-2): The deleted flag can only be used if the mode of the list is "changes"<br/>Constraint (lst-1): A list can only have an emptyReason if it is empty |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-List-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business identifier<br/><font color='red'>An identifier for this Immunisation details list</font><br/> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique<br/>Business identifier<br/><font color='red'>An identifier for this Immunisation details list</font> |
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
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color='red'>This is the subject of the Immunisation details List.<br/>This MUST use the CareConnect patient profile. </font>See[patient resource reference](explore_admission_details.html#patient-reference) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - date | 0..1 | Mandatory | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the list was prepared<br/><font color='red'> This MUST contain a system date to indicate when the list created or updated</font> |
|  - note | 0..* | Optional | [Annotation](http://hl7.org/fhir/stu3/datatypes.html#annotation "Annotation") | Comments about the list |
|   |  | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | <font color='red'>Who authored the comment on the list.</font>  |
|  - - time | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the annotation was made |
|  - - text | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The annotation - text content |
|  - entry | 0..* | Mandatory | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Entries in the list<br/><font color='red'>The entries MUST be as per the diagram for this PRSB headings list with the encounter resource being the focal resource. Multiple Encounters with associated resources MAY be present</font> |
|  - - date | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When item added to list<br/><font color='red'>The SHOULD contain a system time of when the item was added to the list.</font> |
|  - - item | 1..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>A reference to an Encounter resource included in the list<br/>This MUST use the CareConnect Encounter profile. </font>See [Encounter resource](explore_admission_details.html#mapping-for-admission-details-encounter) for information on how to populate the resource. |
|  - - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>The reference to the included Encounter resource.</font> |

## Patient Reference ##

The Admission details list has a mandated subject reference to the Patient resource. This means that any exchange of the Admission details heading data must also include the [Patient demographics List.](explore_patient_demographics.html)

## Mapping for Immunisations ##

|>|Level 1|[Bundle Resource](http://hl7.org/fhir/stu3/immunization.html)|>|Level 2| None|>|Level 3|[CareConnect-Immunization-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Immunization-1)|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_vaccinations_all.html#mapping-for-bundle)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | --- |
|  - id | 0..1 | Optional | Id | **Logical id of this artifact** |
|  - meta | 0..1 | Mandatory | Meta | **Metadata about the resource** |
|  - - profile | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | **Profiles this resource claims to conform to<br/><font color="red">The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-AllergyIntolerance-1'</font>** |
|  - identifier | 0..* | Required | Identifier | **Business identifier** |
|  - - system | 1..1 | Mandatory | Uri | **The namespace for the identifier value** |
|  - - value | 1..1 | Mandatory | String | **The value that is unique** |
|  - - assigner | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | **Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided** |
|  - - - display | 0..1 | Required | String | **Text alternative for the resource** |
|  - status | 1..1 | Mandatory | Code | **Completed<br/>Binding (required): A set of codes indicating the current status of an Immunization [Immunization Status Codes](http://hl7.org/fhir/stu3/valueset-immunization-status.html)<br/><font color='red'>The status of the list MUST contain the value 'Completed'</font>** |
|  - vaccineCode | 1..1 | Optional | CodeableConcept | **Vaccine product administered<br/>Binding (extensible): The code for vaccine product administered [CareConnect-VaccineCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-VaccineCode-1)** |
|  - - coding | 0..* | Optional | Coding | **Code defined by a terminology system** |
|  - - - system | 0..1 | Optional | Uri | **Identity of the terminology system** |
|  - - - code | 0..1 | Optional | Code | **Symbol in syntax defined by the system** |
|  - - - display | 0..1 | Optional | String | **Representation defined by the system** |
|  - - text | 0..1 | Optional | String | **Plain text representation of the concept** |
|  - patient | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | **Who was immunized<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided** |
|  - - reference | 0..1 | Mandatory | String | **Literal reference, Relative, internal or absolute URL<br/><br/><font color='red'>This must use the CareConnect Patient profile.</font>See [patient resource reference](explore_allergies_and_adverse_reactions.html#patient-reference) for information on how to populate the resource** |
|  - encounter | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | **Encounter administered as part of<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided** |
|  - - reference | 0..1 | Mandatory | String | **Literal reference, Relative, internal or absolute URL** |
|  - date | 0..1 | Mandatory | dateTime | **Vaccination administration date<br/><font color="red">The date/time on which the immunisation intervention was carried out or was meant to be administered</font>** |
|  - primarySource | 1..1 | Mandatory | Boolean | **Indicates context the data was recorded in<br/>Default Value: true** |
|  - manufacturer | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | **Vaccine manufacturer<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided** |
|  - - reference | 0..1 | Mandatory | String | **Literal reference, Relative, internal or absolute URL** |
|  - lotNumber | 0..1 | Optional | String | **Vaccine lot number<br/><font color="red">The batch number of the vaccine product</font>** |
|  - site | 0..1 | Optional | CodeableConcept | **Body site vaccine was administered<br/>Binding (examle): The site at which the vaccine was administered [Codes for Immunization Site of Administration](http://hl7.org/fhir/stu3/valueset-immunization-site.html)<br/><font color="red">The immunization site does not use the preferred value set but uses SNOMED CT concepts instead Mapping to Maternity data item = 'site'.<br/><br/>** |
|  - - coding | 0..* | Mandatory | Coding | **Code defined by a terminology system<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open** |
|  - - coding (snomedCT) | 0..1 | Optional | Coding | **Code defined by a terminology system<br/><font color="red">The immunization site does not use the preferred value set but uses SNOMED CT concepts instead Mapping to Maternity data item = 'site'.** |
|  - - - extension (snomedCTDescriptionID) | 0..1 | Optional | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | **The SNOMED CT Description ID for the display<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>** |
|  - - - system | 1..1 | Mandatory | Uri | **Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font>** |
|  - - - code | 1..1 | Mandatory | Code | **Symbol in syntax defined by the system<br/><font color="r3ed">A SNOMED CT code</font>** |
|  - - - display | 1..1 | Mandatory | String | **Representation defined by the system<br/><font color="red">The display associated with the SNOMED CT concept. This SHOULD be the preferred term</font>** |
|  - - text | 0..1 | Optional | String | **Plain text representation of the concept<br/>This element SHOULD only be populated when the Immunisation cannot be coded or when stating one of the following statements: 'No known site' Or 'Information not available'.** |
|  - route | 0..1 | Optional | CodeableConcept | **How vaccine entered body<br/>Binding (example): The route by which the vaccine was administered [Immunization Route Codes](http://hl7.org/fhir/stu3/valueset-immunization-route.html)<br/><font color="red">Note the example valueSet is not used for Maternity and the following should be used instead<br/>Coded text - SNOMED CT (<284009009  |Route of administration value (qualifier value))</font>** |
|  - - coding | 0..* | Mandatory | Coding | **Code defined by a terminology system<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open** |
|  - - coding (snomedCT) | 0..1 | Optional | Coding | **Code defined by a terminology system<br/>Binding (example): A code from the SNOMED Clinical Terminology UK coding system that describes the e-Prescribing route of administration. [CareConnect-MedicationDosageRoute-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-MedicationDosageRoute-1)<br/><font color="red">Note the example valueSet is not used for Maternity and the following should be used instead<br/>Coded text - SNOMED CT (<284009009  |Route of administration value (qualifier value))</font>** |
|  - - - extension (snomedCTDescriptionID) | 0..1 | Optional | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | **The SNOMED CT Description ID for the display<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>** |
|  - - - system | 1..1 | Mandatory | Uri | **Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font>** |
|  - - - code | 1..1 | Mandatory | Code | **Symbol in syntax defined by the system<br/><font color="red">Coded text - SNOMED CT (<284009009  |Route of administration value (qualifier value))</font>** |
|  - - - display | 1..1 | Mandatory | String | **Representation defined by the system<br/><font color="red">This SHOULD be the preferred term for the SNOMED concept</font>** |
|  - - text | 0..1 | Optional | String | **Plain text representation of the concept<br/><font color="red">This element SHOULD only be populated when the Immunisation cannot be coded or when stating one of the following statements: 'No known route' Or 'Information not available'.</font>** |
|  - doseQuantity | 0..1 | Optional | [Quantity (SimpleQuantity )](http://hl7.org/fhir/stu3/StructureDefinition/SimpleQuantity "Quantity (SimpleQuantity )") | **Amount of vaccine administered<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/>Constraint (sqty-1): The comparator is not used on a SimpleQuantity<br/><font color="red">Amount of vaccine administered</font>** |
|  - - value | 0..1 | Required | Decimal | **Numerical value (with implicit precision)** |
|  - - unit | 0..1 | Required | String | **Unit representation** |
|  - - system | 0..1 | Required | Uri | **System that defines coded unit form** |
|  - - code | 0..1 | Required | Code | **Coded form of the unit** |
|  - practitioner | 0..* | Mandatory | BackboneElement | **Who performed event** |
|  - - role | 0..1 | Mandatory | CodeableConcept | **What type of performance was done<br/>Binding (extensible): The role a practitioner plays in the immunization event [Immunization Role Codes](http://hl7.org/fhir/stu3/valueset-immunization-role.html)** |
|  - - - coding | 0..* | Mandatory | Coding | **Code defined by a terminology system** |
|  - - - - system | 0..1 | Mandatory | Uri | **Identity of the terminology system** |
|  - - - - code | 0..1 | Mandatory | Code | **Symbol in syntax defined by the system** |
|  - - - - display | 0..1 | Mandatory | String | **Representation defined by the system** |
|  - - - text | 0..1 | Optional | String | **Plain text representation of the concept** |
|  - - actor | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | **Individual who was performing<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color="red">This MUST be a reference to the Practitioner resource</font>** |
|   |  | Required | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") | **<font color='red'>The responsible clinician for the encounter.<br/>This MUST use the CareConnect Practitioner profile. </font>See [Practitioner resource](explore_admission_details.html#mapping-for-admission-details-encounter) for information on how to populate the resource.** |
|  - - - reference | 0..1 | Mandatory | String | **Literal reference, Relative, internal or absolute URL<br/>A reference to the Practitioner resource included in the Immunisation details list** |
|  - note | 0..* | Optional | Annotation | **Vaccination notes<br/><font color="red">Where a flag to indicate the information was reported to a healthcare professional is available, this MAY be recorded as a note.</font>** |
