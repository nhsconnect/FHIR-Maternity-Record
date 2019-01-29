---
title: Birth Details Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_birth_details.html
summary: "The FHIR profiles used for the Birth Details Event Message Bundle"
---

The following FHIR profiles are used to form the Birth Details Event Message Bundle:

- [NHSD-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/NHSD-Bundle-1)
- [NHSD-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/NHSD-MessageHeader-1)
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [CareConnect-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-HealthcareService-1)
- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)
- [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)
- [CareConnect-Condition-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Condition-1)
- [CareConnect-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)
- [CareConnect-Procedure-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Procedure-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)

## Birth Details Bundle structure ##

{% include custom/Birth_details.svg %}


## Birth Details Event data item mapping to FHIR profiles ##


## Mapping for Bundle ##

How to populate the Bundle instance to conform to the profiles below:

|**Level 1**|[Bundle Resource](http://hl7.org/fhir/stu3/bundle.html)|**Level 2**| None|**Level 3**|[NHSD-Bundle-1 Profile](http://xxx)|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_birth_details_all.html#mapping-for-bundle)**|


|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Maternity-Record Implementation** |
|  :------ | :------ | ------ | :------ | :------ |
|  Bundle | ​ |  |  | Contains a collection of resources<br/>Constraint (bdl-7): FullUrl must be unique in a bundle, or else entries with the same fullUrl must have different meta.versionId<br/>Constraint (bdl-9): A document must have an identifier with a system and a value<br/>Constraint (bdl-3): Entry.Request Only For Some Types Of Bundles<br/>Constraint (bdl-4): Entry.Response Only For Some Types Of Bundles<br/>Constraint (bdl-1): Total Only When A Search Or History<br/>Constraint (bdl-2): Entry.Search Only When A Search |
|  - id | 0..1 | Mandatory | [Id](http://hl7.org/fhir/stu3/datatypes.html#id) | <font color='red'>Must contain a UUID to identify the instance of a bundle</font> |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta) | <font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/NHSD-Bundle-1'.</font> |
|  - type | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | document : message : transaction : transaction-response : batch : batch-response : history : searchset : collection<br/>Binding (required): Indicates the purpose of a bundle - how it was intended to be used. [See FHIR STU3 for further info](http://hl7.org/fhir/stu3/valueset-bundle-type.html)<br/><font color='red'>The value attribute of the code element MUST contain the fixed value: 'message'.</font> |
|  - entry | 1..* | Mandatory | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html) | Entry in the bundle - will have a resource, or information<br/>Constraint (bdl-8): fullUrl cannot be a version specific reference<br/>Constraint (bdl-5): Must Be A Resource Unless There'S A Request Or Response |
|  - - fullUrl | 0..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | Absolute URL for resource (server address, or UUID/OID). <font color='red'>This MUST be a UUID prefixed by urn:uuid </font>: |
|  - - resource | 1..1 | Mandatory | [Resource](http://hl7.org/fhir/stu3/resource.html) | A resource in the bundle. <font color='red'>This MUST be to the MessageHeader resource profiled as NHSD-MessageHeader-1.</font> See [Mapping for MessageHeader](explore_birth_details.html#mapping-for-messageheader) for further info. |

## Mapping for MessageHeader ##

How to populate the MessageHeader instance to conform to the profiles below:

|**Level 1**|[MessageHeader Resource](http://hl7.org/fhir/stu3/messageHeader.html)|**Level 2**| None|**Level 3**|[NHSD-MessageHeader-1 Profile](http://xxx)|

|**View Used FHIR Elements**|    |**[View All FHIR Elements](explore_birth_details_all.html#mapping-for-messageheader)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Maternity-Record Implementation** |
|  ------ | :------ | ------ | :------ | :------ |
|  MessageHeader | ​ |  |  | A resource that describes a message that is exchanged between systems<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - id | 1..1 | Mandatory | [Id](http://hl7.org/fhir/stu3/datatypes.html#id) | Logical id of this artifact. <font color='red'>This MUST be a UUID.</font> |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta) | Metadata about the resource. <font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/NHSD-MessageHeader-1'</font> |
|  - extension (messageEventType) | 1..1 | Mandatory | [Extension-Maternity-Record-MessageEventType-1](https://fhir.nhs.uk/STU3/StructureDefinition/Extension-Maternity-Record-MessageEventType-1) | <font color='red'>The url attribute of the extension element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/Extension-Maternity-Record-MessageEventType-1' </font>and be populated as specified [here](explore_birth_details.html#mapping-for-extension-Maternity-Record-messageevent-mapping). |
|  - event | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding) | [Code for the event this message represents - Binding (required): The type of Child Health Event.](https://fhir.nhs.uk/STU3/ValueSet/Maternity-Record-ChildHealthEventType-1) |
|  - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | <font color='red'>MUST contain the value: 'https://fhir.nhs.uk/STU3/CodeSystem/Maternity-Record-ChildHealthEventType-1'</font> |
|  - - code | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | <font color='red'>MUST contain the value 'CH005'</font> |
|  - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | <font color='red'>MUST contain the value 'Birth Details'</font> |
|  - timestamp | 1..1 | Mandatory | [Instant](http://hl7.org/fhir/stu3/datatypes.html#instant) | Time that the message was sent |
|  - source | 1..1 | Mandatory | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html) | Message source application identified using an ASID |
|  - - endpoint | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | Actual message source address or id  <font color='red'>Must contain the ASID of the sending system prefixed by urn:nhs:addressing:asid:for example urn:nhs:addressing:asid:477121000325.</font> |
|  - responsible | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html) | Final responsibility for event<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | CareConnect-Organization-1 | The responsible organization carried in the Organizaion resource in the bundle. <font color='red'>This MUST be to the Organization resource profiled as CareConnect-Organization-1"</font> See [mapping for Organization](explore_birth_details.html#mapping-for-organization) for further info. |
|  - - reference | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Literal reference, Relative, internal or absolute URL<font color='red'>MUST contain a UUID prefixed by urn:uuid:</font> |
|  - focus | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html) | The actual content of the message<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | CareConnect-Encounter-1 | The focus resource in the bundle.<font color='red'> This MUST be to the encounter resource profiled as CareConnect-Encounter-1. </font>[See mapping for encounter for further info](explore_birth_details.html#mapping-for-encounter) |
|  - - reference | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Literal reference, Relative, internal or absolute URL.<font color='red'>MUST contain a UUID prefixed by urn:uuid:</font> |


## Mapping for Encounter ##

How to populate the Encounter instance to conform to the profiles below:

|**Level 1**|[Encounter Resource](http://hl7.org/fhir/stu3/encounter.html)|**Level 2**|[CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)|**Level 3**|None|


|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Maternity-Record Implementation** |
|  ------ | ------ | ------ | ------ | ------ |
|  Encounter | ​ |  |  | An interaction during which services are provided to the patient<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta) | <font color='red'>The value attribute of the  profile element MUST contain the value https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Encounter-1</font> |
|  - identifier | 0..1 | Mandatory | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier) | Identifier(s) by which this encounter is known. |
|  - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | The namespace for the identifier value. <font color="red">MUST contain the value 'https://tools.ietf.org/html/rfc4122'.</font> |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | The value that is unique. <font color="red">MUST contain a UUID</font> |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | planned : arrived : triaged : in-progress : onleave : finished : cancelled. Binding (required): Current state of the encounter. [See FHIR STU3 for further info](http://hl7.org/fhir/stu3/valueset-encounter-status.html) <font color='red'>MUST contain the value 'completed'</font> |
|  - type | 0..* | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept) | Code defined by a terminology system<br/>Binding (required): [The type of Child Health encounter]( https://fhir.nhs.uk/STU3/ValueSet/Maternity-Record-ChildHealthEncounterType-1) |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding) | Code defined by a terminology system<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open |
|  - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri) | Identity of the terminology system. <font color='red'>MUST contain the value 'https://fhir.nhs.uk/STU3/ValueSet/Maternity-Record-ChildHealthEncounterType-1'</font> |
|  - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code) | Symbol in syntax defined by the system. <font color='red'>MUST contain the value '003'.</font> |
|  - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Representation defined by the system. <font color='red'>MUST contain the value 'Birth'.</font> |
|  - subject | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html) | The patient present at the encounter<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided. |
|   |  | Mandatory | [CareConnect-Patient-1](http://xxx) | A patient resource in the bundle.<font color='red'>This MUST be to the Patient resource profiled as CareConnect-Patient-1</font> See [Mapping for Patient](explore_birth_details.html#mapping-for-patient) for further info. |
|  - - reference | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Literal reference, Relative, internal or absolute URL <font color='red'>a reference to the Patient resource instance in the message in the format of  a UUID prefixed with 'urn:uuid:'.</font> |
|   | 0.1 | Mandatory | CareConnect-NHSD-Location | A location resource in the bundle.<font color='red'>This MUST be to the Location resource profiled as CareConnect-NHSD-Location-1</font> See [Mapping for Location](explore_birth_details.html#mapping-for-location) for further info. |
|  - - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Literal reference, Relative, internal or absolute URL <font color='red'>a reference to the location resource instance in the message in the format of  a UUID prefixed with 'urn:uuid:'.</font> |
|  - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Text alternative for the resource |
|  - - serviceProvider | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html) | The custodian organization of this Encounter record<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Organization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Organization-1) | An organization resource in the bundle.<font color='red'>This MUST be to the Organization resource profiled as CareConnect-Organization-1</font> [See mapping for Organization for further info](explore_birth_details.html#mapping-for-organization) |
|  - - - reference | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Literal reference, Relative, internal or absolute URL <font color='red'>a reference to the Organization resource instance in the message in the format of  a UUID prefixed with 'urn:uuid:'.</font> |
|  - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string) | Text alternative for the resource |


## Mapping for Patient ##

How to populate the Patient instance to conform to the profiles below:

|**Level 1**|[Patient Resource](http://hl7.org/fhir/stu3/patient.html)|**Level 2**|[CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)|**Level 3**|None|



|**View Used FHIR Elements**|    |**[View All FHIR Elements](explore_birth_details_all.html#mapping-for-patient)**|

|   |  |  |  |  |
| --- | --- | --- | --- | --- |
|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for XXX Implementation** |
|  Patient | ​ |  |  | Information about an individual receiving health care services<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource. <font color="red">The profile element MUST contain the value https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Patient-1</font>  |
|  - identifier | 0..* | Mandatory | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | An identifier for this patient<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open at End |
|  - - identifier (nhsNumber) | 0..1 | Mandatory | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | The patient's NHS number |
|  - - extension <br/>(nhsNumber<br/>VerificationStatus) | 1..1 | Mandatory | [NHSNumberVerificationStatus-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-NHSNumberVerificationStatus-1) | NHS number verification status<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>[See mapping for nhsNumberVerificationStatus for further info](explore_birth_details.html#mapping-for-nhsNumberVerificationStatus)<br/> |
|  - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>Fixed Value: https://fhir.nhs.uk/Id/nhs-number</font> |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique. <font color='red'>MUST contain a valid NHS Number</font><br/><b><font color='red'>Maps to data set item NHS Number</font></b>  |
|  - name | 1..* | Mandatory | [HumanName](http://hl7.org/fhir/stu3/datatypes.html#humanname "HumanName") | A name associated with the patient<br/>Slicing: Discriminator: use, Ordering: false, Rules: Open at End |
|  - name (official) | 1..1 | Mandatory | [HumanName](http://hl7.org/fhir/stu3/datatypes.html#humanname "HumanName") | A name associated with the patient |
|  - - use | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | usual : official :  temp : nickname : anonymous : old : maiden. Binding (required): The use of a human name. [See FHIR STU3 for further info]( https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-NameUse-1 )<font color='red'> MUST contain the value 'official'</font> |
|  - - family | 1..1 | Mandatory | String | Family name (often called 'Surname') |
|  - - given | 0..* | Mandatory | String | Given names (not always 'first'). Includes middle names |
|  - gender | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | male : female : other : unknown Binding (required): The gender of a person used for administrative purposes.[See FHIR STU3 for further info](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-AdministrativeGender-1) |
|  - birthDate | 0..1 | Mandatory | [Date](http://hl7.org/fhir/stu3/datatypes.html#date "Date") | The date of birth for the individual |
|  - - extension (patient-birthTime) | 0..1 | Mandatory | [patient-birthTime](http://hl7.org/fhir/StructureDefinition/patient-birthTime) | The time of day that the Patient was born. This includes the date to ensure that the timezone information can be communicated effectively.<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>[See mapping for patient-birthTime](explore_birth_details.html#patient-birthTime) for further info. |
|  - address | 0..* | Mandatory | [Address](http://hl7.org/fhir/stu3/datatypes.html#address "Address") | Addresses for the individual |
|  - - use | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | home : work : temp : old - purpose of this address<br/>Binding (required): The use of an address [See FHIR STU3 for further info](http://hl7.org/fhir/stu3/valueset-address-use.html) |
|  - - line | 0..* | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Street name, number, direction & P.O. Box etc. |
|  - - city | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Name of city, town etc. |
|  - - postalCode | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Postal code for area |
|  - multipleBirth[x] | 0..1 | Mandatory | Boolean : Integer | Whether patient is part of a multiple birth <font color='red'>Use Boolean datatype and value false for non multiple births. Use Integer datatype with value of number of births for multiple births</font> |







| Maternity-Record Data Item                       | FHIR resource element                                                   | Mandatory/Required/Optional |
|-------------------------------------|-------------------------------------------------------------------------|-----------------------------|
| Location of Birth                   | CareConnect-Maternity-Record-Delivery-Location-1.identifier (ODS Site Code)           | Required                   |
| Delivery Place Type Code            | CareConnect-Maternity-Record-Delivery-Location-1.physicalType                        | Mandatory                   |
| Birth Order                         | CareConnect-Maternity-Record-Patient-1.multipleBirthInteger                     | Mandatory                   |
| Length of Gestation at Birth        | CareConnect-Maternity-Record-LengthOfGestation-Observation-1.valueQuantity           | Mandatory                   |
| Number of Births in confinement     | CareConnect-Maternity-Record-NumberOfBirths-Observation-1.valueQuantity                  | Mandatory                    |
| Problems during Delivery            | CareConnect-Maternity-Record-ProblemDuringDelivery-Condition-1.code                          | Required                    |
| Physical Problems detected at Birth | CareConnect-Maternity-Record-PhysicalProblemAtBirth-Condition-1.code            | Required                    |
| Neonatal Resuscitation Method       | CareConnect-Maternity-Record-NeonatalResuscitationMethod-Procedure-1.code                           | Required                 |
| Date and Time of Birth              | CareConnect-Maternity-Record-Patient-1.birthDate (with patient-BirthTime extension)                           | Mandatory                 |
| Type of Delivery                    | CareConnect-Maternity-Record-FinalDeliveryType-Procedure-1.code   | Mandatory                    |
| Attempted Type of Delivery          | CareConnect-Maternity-Record-AttemptedDeliveryType-Condition-1.code   | Required                    |
| Onset of Spontaneous Respiration    | CareConnect-Maternity-Record-SpontaneousRespirationOnset-Observation-1.component  | Optional                    |
| APGAR Score (1 Minute)              | CareConnect-Maternity-Record-APGARScore-Observation-1.valueQuantity                 | Mandatory                   |
| APGAR Score (5 Minute)              | CareConnect-Maternity-Record-APGARScore-Observation-1.valueQuantity                  | Mandatory                   |
| APGAR Score (10 Minute)             | CareConnect-Maternity-Record-APGARScore-Observation-1.valueQuantity                | Optional                    |
| Put To Breast                       | CareConnect-Maternity-Record-PutToBreastIndicator-Observation-1.code                  | Required                    |
| Identical Twin Indicator	      | CareConnect-Maternity-Record-IdenticalTwinIndicator-Observation-1.code               | Optional                    |

