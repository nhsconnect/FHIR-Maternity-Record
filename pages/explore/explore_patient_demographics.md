---
title: Patient Demographics List
keywords:  lists
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_patient_demographics.html
summary: "The FHIR profiles used for the Patient demographics list structure"
---

## Heading Description ##
This heading holds all of the elements for each instance of a patient demographics entry.

The following FHIR profiles are used to form the Patient demographics list structure:

- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)
- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)
- [CareConnect-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)

The following profiles are referenced from the Patient demographics list structure:

- None

## Patient Demographics Structure ##

{% include custom/patient_demographics.svg %}


## Maternity data standard Mapping to FHIR profiles ##

The following tables detail how to populate the FHIR resources and the mapping to the Maternity data standard.

## Mapping for Patient Demographics List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_patient_demographics_all.html#mapping-for-patient-demographics-list)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  List | ​ |  |  | Information summarized from a list of other resources<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (lst-2): The deleted flag can only be used if the mode of the list is "changes"<br/>Constraint (lst-1): A list can only have an emptyReason if it is empty |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-List-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business identifier<br/><font color='red'>An identifier for this Patient demographics list</font><br/> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique<br/>Business identifier<br/><font color='red'>An identifier for this Patient demographics list</font> |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource<br/><font color='red'>The organization that allocated the identifier</font> |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | current : retired : entered-in-error<br/>Binding (required): The current state of the list [ListStatus](http://hl7.org/fhir/stu3/valueset-list-status.html)<br/><font color='red'>The status of the list MUST contain the value 'current'</font> |
|  - mode | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | working : snapshot : changes<br/>Binding (required): The processing mode that applies to this list [ListMode](http://hl7.org/fhir/stu3/valueset-list-mode.html)<br/><font color='red'>The mode of the list MUST contain the value 'snapshot'</font> |
|  - title | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Descriptive name for the list<br/><font color='red'>This MUST contain the value 'Patient demographics'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading patient demographics'</b></font>  |
|  - code | 0..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | What the purpose of this list is<br/>Binding (preferred): What the purpose of a list is [CareConnect-ListCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListCode-1)<br/><font color='red'>The PRSB heading for this list. Note: for Maternity the value stated below is used which is not from the preferred value set </font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/><font color='red'>The SNOMED CT concept for the PRSB heading type</font> |
|  - - - system | 0..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value '886731000000109'</font> |
|  - - - display | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>This MUST contain the value 'Patient demographics'</font><br/><font color='red'>Mapping to Maternity data item = 'PSRB Heading Patient demographics'</font>  |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color='red'>This is the subject of the Admission details List.<br/><br/>This MUST use the CareConnect patient profile. </font>See [patient resource reference](explore_admission_details.html#patient-reference) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - date | 0..1 | Mandatory | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the list was prepared<br/><font color='red'> This MUST contain a system date to indicate when the list created or updated</font> |
|  - note | 0..* | Optional | [Annotation](http://hl7.org/fhir/stu3/datatypes.html#annotation "Annotation") | Comments about the list |
|   |  | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | <font color='red'>Who authored the comment on the list.</font>  |
|  - - time | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the annotation was made |
|  - - text | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The annotation - text content |
|  - entry | 0..* | Mandatory | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Entries in the list<br/><font color='red'>The entries MUST be as per the diagram for this PRSB headings list with the Observation resource being the focal resource.</font> |
|  - - date | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When item added to list<br/><font color='red'>The SHOULD contain a system time of when the item was added to the list.</font> |
|  - - item | 1..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>A reference to an Observation resource included in the list<br/>This MUST use the CareConnect Observation profile. </font><br/>See [Observation resource](explore_patient_demographics.html#mapping-for-patient-demographics-observation) for information on how to populate the resource. |
|  - - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>The reference to the included Observation resource.</font> |

## Mapping for Patient Demographics Patient ##

|>|Level 1|[Patient Resource](http://hl7.org/fhir/stu3/patient.html)|>|Level 2|[CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_patient_demographics_all.html#mapping-for-patient-demographics-patient)**|


|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  Patient | ​ |  |  | Information about an individual or animal receiving health care services<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 1..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Patient-1'</font> |
|  - extension (ethnicCategory) | 0..1 | Required |  | Ethnic category - The ethnicity of the person<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/><font color='red'>An extension to the Patient resource</font><br/>See [Ethnic category extension](explore_patient_demographics.html#mapping-for-patient-demographics-ethnic-category-extension) for information on how to populate this extension to the resource.<br/><font color='red'><b>Mapping to Maternity data item = 'Ethnicity'.</b></font><br/> |
|  - extension (religiousAffiliation) | 0..1 | Required | [Extension-CareConnect-EthnicCategory-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-EthnicCategory-1 "Extension-CareConnect-EthnicCategory-1") | Religious affiliation - The religious affiliation as specified by the person.<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/><font color='red'>An extension to the Patient resource</font><br/>See [Religious affiliation extension](explore_patient_demographics.html#mapping-for-patient-demographics-religious-affiliation-extension) for information on how to populate this extension to the resource.<br/><font color='red'><b>Mapping to Maternity data item = 'Religion'.</b></font><br/> |
|  - extension (birthPlace) | 0..1 | Required | [birthPlace](http://hl7.org/fhir/StructureDefinition/birthPlace "birthPlace") | Birth Place: The registered place of birth of the patient. <br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/><font color='red'>A common extension to the Patient resource</font><br/>See [Birth place extension](explore_patient_demographics.html#mapping-for-patient-demographics-birth-place-extension) for information on how to populate this extension to the resource.<br/><font color='red'><b>Mapping to Maternity data item = 'Place of Birth'.</b> The town and country of birth of the patient</font> <br/><br/> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | An identifier for this patient<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open at End |
|  - identifier (nhsNumber) | 0..1 | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | The patient's NHS number.<br/><font color='red'>The unique identifier for a patient within the NHS in England and Wales.</font><br/><font color='red'><b>Mapping to Maternity data item = 'NHS number'.</b><br/> |
|  - - extension (nhsNumberVerificationStatus) | 1..1 | Mandatory | [Extension-CareConnect-NHSNumberVerificationStatus-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-NHSNumberVerificationStatus-1 "Extension-CareConnect-NHSNumberVerificationStatus-1") | NHS number verification status<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/><font color='red'>An extension to the Patient resource</font><br/>See [NHS number vertification status extension](explore_patient_demographics.html#mapping-for-patient-demographics-nhs-number-vertification-status-extension) for information on how to populate this extension to the resource.<br/> |
|  - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/Id/nhs-number'</font> |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique<br/><font color='red'>The unique identifier for a patient within the NHS in England and Wales.</font> |
|  - name | 1..* | Mandatory | [HumanName](http://hl7.org/fhir/stu3/datatypes.html#humanname "HumanName") | A name associated with the patient<br/>Slicing: Discriminator: use, Ordering: false, Rules: Open at End |
|  - name (official) | 1..1 | Mandatory | [HumanName](http://hl7.org/fhir/stu3/datatypes.html#humanname "HumanName") | A name associated with the patient.<br/><font color='red'>The full name of the patient. This will normally be given by a Personal Demographics Service (PDS) patient trace, or the name of the patient held on the local Patient Administration System (PAS).</font><br/><font color='red'><b>Mapping to Maternity data item = 'Patient name'.</b></font>  |
|  - - use | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | usual : official : temp : nickname : anonymous : old : maiden<br/><font color='red'>The value attribute of the profile element MUST contain the value 'official'</font><br/>Binding (required): The use of a human name [CareConnect-NameUse-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-NameUse-1) |
|  - - text | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text representation of the full name |
|  - - family | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Family name (often called 'Surname') |
|  - - given | 0..* | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Given names (not always 'first'). Includes middle names |
|  - - prefix | 0..* | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Parts that come before the name |
|  - - suffix | 0..* | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Parts that come after the name |
|  - telecom | 0..* | Required | [ContactPoint](http://hl7.org/fhir/stu3/datatypes.html#contactpoint "ContactPoint") | A contact detail for the individual<br/>Constraint (cpt-2): A system is required if a value is provided.<br/><font color='red'>Telephone contact details of the patient. To include, e.g. mobile, work and home number if available and/or the email address of the patient</font><br/><font color='red'><b>Mapping to Maternity data item = 'Patient telephone number' and/or 'Patient email address'</b></font>  |
|  - - system | 1..1 | Required | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | phone : fax : email : pager : url : sms : other<br/>Binding (required): Telecommunications form for contact point [ContactPointSystem](http://hl7.org/fhir/stu3/valueset-contact-point-system.html) |
|  - - value | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The actual contact point details |
|  - - use | 0..1 | Required | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | home : work : temp : old : mobile - purpose of this contact point<br/>Binding (required): Use of contact point [ContactPointUse](http://hl7.org/fhir/stu3/valueset-contact-point-use.html) |
|  - - rank | 0..1 | Required | [positiveInt](http://hl7.org/fhir/stu3/datatypes.html#positiveint "positiveInt") | Specify preferred order of use (1 = highest) |
|  - gender | 0..1 | Required | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | male : female : other : unknown<br/>Binding (required): The gender of a person used for administrative purposes. [CareConnect-AdministrativeGender-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-AdministrativeGender-1)<br/><font color='red'>As the patient wishes to portray themselves.</font><br/><font color='red'><b>Mapping to Maternity data item = 'Gender'</b></font>  |
|  - birthDate | 0..1 | Required | [Date](http://hl7.org/fhir/stu3/datatypes.html#date "Date") | The date of birth for the individual<br/><font color='red'><b>Mapping to Maternity data item ='Date of Birth'</b></font>  |
|  - deceased[x] | 0..1 | Required | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | Indicates if the individual is deceased or not |
|   |  | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | The date and time when the patient died<br/><font color='red'><b>Mapping to Maternity data item = 'Date of Death and Time of Date'</b></font>  |
|  - address | 0..* | Required | [Address](http://hl7.org/fhir/stu3/datatypes.html#address "Address") | Addresses for the individual.<br/><font color='red'>Patient’s usual place of residence.as per PDS five address line + postcode format</font><br/><font color='red'><b>Mapping to Maternity data item ='Patient address'</b></font> |
|  - - use | 0..1 | Required | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | home : work : temp : old - purpose of this address<br/>Binding (required): The use of an address [AddressUse](http://hl7.org/fhir/stu3/valueset-address-use.html) |
|  - - line | 0..* | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Street name, number, direction & P.O. Box etc.<br/><font color='red'>Patient’s usual place of residence.as per PDS five address line format</font> |
|  - - postalCode | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Postal code for area<br/><font color='red'>Patient’s  postcode PDS format</font> |
|  - maritalStatus | 0..1 | Required | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Marital (civil) status of a patient<br/>Binding (required): The domestic partnership status of a person. [CareConnect-MaritalStatus-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-MaritalStatus-1)<br/><font color='red'>An indicator to identify the legal marital status of the person. The FHIR valueSet MUST be used and mapped to NHS Data Dictionary codes</font><br/><font color='red'><b>Mapping to Maternity data item = 'Marital Status'.</b></font>  |
|  - - coding | 1..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>This MUST contain the value https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-MaritalStatus-1</font> |
|  - - - code | 1..1 | Required | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain a code from the above valueSet</font> |
|  - - - display | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>This MUST contain the display assoicated with the code</font> |

## Mapping for Patient Demographics Observation ##

|>|Level 1|[Observation Resource](http://hl7.org/fhir/stu3/observation.html)|>|Level 2|[CareConnect-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_patient_demographics_all.html#mapping-for-patient-demographics-observation)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  Observation | ​ |  |  | Measurements and simple assertions<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (obs-7): If code is the same as a component code then the value element associated with the code SHALL NOT be present<br/>Constraint (obs-6): dataAbsentReason SHALL only be present if Observation.value[x] is not present |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Observation-1'</font> |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | registered : preliminary : final : amended +<br/>Binding (required): Codes providing the status of an observation. [ObservationStatus](http://hl7.org/fhir/stu3/valueset-observation-status.html)<br/><font color='red'>This MUST contain the value 'final'</font> |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of observation (code / type)<br/>Binding (example): Codes identifying names of simple observations. [LOINC Codes](http://hl7.org/fhir/stu3/valueset-observation-codes.html)<br/><font color='red'>The woman’s phenotypic sex. Determines how the woman will be treated clinically.</font> |
|  - - coding | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system describing a type of observation [CareConnect-ObservationType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ObservationType-1)<br/><font color='red'>This uses a SNOMED CT concept to describe this observation as one of patient's sex</font><br/><font color='red'><b>Mapping to Maternity data item = 'Patient sex'.</b></font> |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value '184100006'</font> |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>This MUST contain the value 'Patient sex'</font> |
|   |  | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | The system element MUST contain the identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|   |  |  |  | The code element MUST contain the symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value '248152002'</font> |
|   |  |  |  | The display element MUST contain the representation defined by the system<br/><font color='red'>This MUST contain the value 'Female'</font> |

## Mapping for Patient Demographics Extension Ethnic category ##

|>|Level 1|[Extension](http://hl7.org/fhir/stu3/extension.html)|>|Level 2|[CareConnect-EthnicCategory-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-EthnicCategory-1)|>|Level 3|None|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | --- | :--- | :--- |
|  Extension | ​ |  |  | Ethnic category<br/>Constraint (ele-1): All FHIR elements must have a @value or children<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - id | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | xml:id (or equivalent in JSON) |
|  - url | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identifies The Meaning Of The Extension<br/>Fixed Value = 'https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-EthnicCategory-1' |
|  - valueCodeableConcept | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | 	A code classifying the person's ethnicity<br/><br/>Binding (required): A code classifying the person's ethnicity. [CareConnect-EthnicCategory-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-EthnicCategory-1) |

## Mapping for Patient Demographics Extension Religious Affiliation ##

|>|Level 1|[Extension](http://hl7.org/fhir/stu3/extension.html)|>|Level 2|[CareConnect-ReligiousAffiliation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-ReligiousAffiliation-1)|>|Level 3|None|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | --- | :--- | :--- |
|  Extension | ​ |  |  | Religious affiliation<br/>Constraint (ele-1): All FHIR elements must have a @value or children<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - id | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | xml:id (or equivalent in JSON) |
|  - url | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identifies The Meaning Of The Extension<br/>Fixed Value = 'https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-ReligiousAffiliation-1' |
|  - valueCodeableConcept | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | A code classifying the person's religious affiliation<br/>Binding (required): A code classifying the person's ethnicity.[CareConnect-ReligiousAffiliation-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ReligiousAffiliation-1) |


## Patient Demographics Heading Example ##

<script src="https://gist.github.com/IOPS-DEV/9d51ee5528e59b70da255468c3da5413.js"></script>