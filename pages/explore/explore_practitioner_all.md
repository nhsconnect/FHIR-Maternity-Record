---
title: Practitioner
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_practitioner_all.html
summary: "The FHIR profiles used for Practitioner"
---

## Heading Description ##

A generic practitioner resource based on the CareConnect L2 [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1) profile, using the elements required to support its use within the Digital Maternity Messaging Specfication.

## Mapping for Practitioner ##

|>|Level 1|[Practitioner Resource](http://hl7.org/fhir/stu3/practitioner.html)|>|Level 2|[CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)|>|Level 3|None|


|**[View Used FHIR Elements](explore_practitioner.html#mapping-for-practitioner)**|**[View All FHIR Elements]**|


|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  Practitioner | ​ |  |  | A person with a formal responsibility in the provisioning of healthcare or related services<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/><font color='red'>The name and designation of the consultant, who has overall responsibility for the person (may not actually see the person)</font> |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1'</font> |
|  - implicitRules | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | **A set of rules under which this content was created** |
|  - language | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | **Language of the resource content<br/>Binding (extensible): A human language. [Common Languages](http://hl7.org/fhir/stu3/valueset-languages.html)** |
|  - text | 0..1 | Not Used | [Narrative](http://hl7.org/fhir/stu3/narrative.html#Narrative "Narrative") | **Text summary of the resource, for human interpretation** |
|  - contained | 0..* | Not Used | [Resource](http://hl7.org/fhir/stu3/resource.html "Resource") | **Contained, inline Resources** |
|  - extension (nhsCommunication) | 0..* | Not Used | [Extension-CareConnect-NHSCommunication-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-NHSCommunication-1 "Extension-CareConnect-NHSCommunication-1") | **NHS communication preferences for a resource<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>** |
|  - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | **Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>Slicing: Description: Extensions are always sliced by (at least) url, Discriminator: url, Ordering: false, Rules: Open** |
|  - identifier | 0..* | Mandatory | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | A identifier for the person as this agent<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open at End |
|  - identifier (sdsUserID) | 0..1 | Mandatory | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | A identifier for the person as this agent<br/><font color='red'>This will be the clinicians SDS identifier (GMC code)</font><br/><font color='red'><b>Mapping to Maternity Data set = 'Responsible Clinician Identifier'.</b></font> |
|  - - use | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known. [IdentifierUse](http://hl7.org/fhir/stu3/valueset-identifier-use.html)<br/><font color='red'>This MUST contain the value 'offical'.</font> |
|  - - type | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [Identifier Type Codes](http://hl7.org/fhir/stu3/valueset-identifier-type.html) |
|  - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/Id/sds-user-id'</font><br/><font color='red'><b>Maternity data set mapping = ' |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique<br/><font color='red'>This MUST contain the person's SDS user id</font> |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | **Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end** |
|  - - assigner | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | **Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided** |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") | **** |
|  - identifier (sdsRoleProfileID) | 0..* | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | **A identifier for the person as this agent** |
|  - - use | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | **usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known. [IdentifierUse](http://hl7.org/fhir/stu3/valueset-identifier-use.html)** |
|  - - type | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | **Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [Identifier Type Codes](http://hl7.org/fhir/stu3/valueset-identifier-type.html)** |
|  - - system | 1..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | **The namespace for the identifier value<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/Id/sds-role-profile-id'</font>** |
|  - - value | 1..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **The value that is unique** |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | **Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end** |
|  - - assigner | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | **Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided** |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") | **** |
|  - active | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | **Whether this practitioner's record is in active use<br/>Default Value: true** |
|  - name | 0..* | Required | [HumanName](http://hl7.org/fhir/stu3/datatypes.html#humanname "HumanName") | The name(s) associated with the practitioner |
|  - - use | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | **usual : official : temp : nickname : anonymous : old : maiden<br/>Binding (required): The use of a human name [NameUse](http://hl7.org/fhir/stu3/valueset-name-use.html)** |
|  - - text | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text representation of the full name<br/><font color='red'><b>Mapping to Maternity Data set = 'Responsible Clinician Name'.</b></font> |
|  - - family | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Family name (often called 'Surname') |
|  - - given | 0..* | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Given names (not always 'first'). Includes middle names |
|  - - prefix | 0..* | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Parts that come before the name |
|  - - suffix | 0..* | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Parts that come after the name |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | **Time period when name was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end** |
|  - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | **Starting time with inclusive boundary** |
|  - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | **End time with inclusive boundary, if not ongoing** |
|  - telecom | 0..* | Not Used | [ContactPoint](http://hl7.org/fhir/stu3/datatypes.html#contactpoint "ContactPoint") | **A contact detail for the practitioner (that apply to all roles)<br/>Constraint (cpt-2): A system is required if a value is provided.** |
|  - - system | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | **phone : fax : email : pager : url : sms : other<br/>Binding (required): Telecommunications form for contact point [ContactPointSystem](http://hl7.org/fhir/stu3/valueset-contact-point-system.html)** |
|  - - value | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **The actual contact point details** |
|  - - use | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | **home : work : temp : old : mobile - purpose of this contact point<br/>Binding (required): Use of contact point [ContactPointUse](http://hl7.org/fhir/stu3/valueset-contact-point-use.html)** |
|  - - rank | 0..1 | Not Used | [positiveInt](http://hl7.org/fhir/stu3/datatypes.html#positiveint "positiveInt") | **Specify preferred order of use (1 = highest)** |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | **Time period when the contact point was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end** |
|  - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | **Starting time with inclusive boundary** |
|  - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | **End time with inclusive boundary, if not ongoing** |
|  - address | 0..* | Not Used | [Address](http://hl7.org/fhir/stu3/datatypes.html#address "Address") | **Address(es) of the practitioner that are not role specific (typically home address)** |
|  - - use | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | **home : work : temp : old - purpose of this address<br/>Binding (required): The use of an address [AddressUse](http://hl7.org/fhir/stu3/valueset-address-use.html)** |
|  - - type | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | **postal : physical : both<br/>Binding (required): The type of an address (physical / postal) [AddressType](http://hl7.org/fhir/stu3/valueset-address-type.html)** |
|  - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Text representation of the address** |
|  - - line | 0..* | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Street name, number, direction & P.O. Box etc.** |
|  - - city | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Name of city, town etc.** |
|  - - district | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **District name (aka county)** |
|  - - state | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Sub-unit of country (abbreviations ok)** |
|  - - postalCode | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Postal code for area** |
|  - - country | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Country (e.g. can be ISO 3166 2 or 3 letter code)** |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | **Time period when address was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end** |
|  - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | **Starting time with inclusive boundary** |
|  - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | **End time with inclusive boundary, if not ongoing** |
|  - gender | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | **male : female : other : unknown<br/>Binding (required): The gender of a person used for administrative purposes. [CareConnect-AdministrativeGender-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-AdministrativeGender-1)** |
|  - birthDate | 0..1 | Not Used | [Date](http://hl7.org/fhir/stu3/datatypes.html#date "Date") | **The date on which the practitioner was born** |
|  - photo | 0..* | Not Used | [Attachment](http://hl7.org/fhir/stu3/datatypes.html#attachment "Attachment") | **Image of the person<br/>Constraint (att-1): It the Attachment has data, it SHALL have a contentType** |
|  - - contentType | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | **Mime type of the content, with charset etc.<br/>Binding (required): The mime type of an attachment. Any valid mime type is allowed. [Mime Type](http://www.rfc-editor.org/bcp/bcp13.txt)** |
|  - - language | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | **Human language of the content (BCP-47)<br/>Binding (extensible): A human language. [Common Languages](http://hl7.org/fhir/stu3/valueset-languages.html)** |
|  - - data | 0..1 | Not Used | [base64Binary](http://hl7.org/fhir/stu3/datatypes.html#base64binary "base64Binary") | **Data inline, base64ed** |
|  - - url | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | **Uri where the data can be found** |
|  - - size | 0..1 | Not Used | [unsignedInt](http://hl7.org/fhir/stu3/datatypes.html#unsignedint "unsignedInt") | **Number of bytes of content (if url provided)** |
|  - - hash | 0..1 | Not Used | [base64Binary](http://hl7.org/fhir/stu3/datatypes.html#base64binary "base64Binary") | **Hash of the data (sha-1, base64ed)** |
|  - - title | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Label to display in place of the data** |
|  - - creation | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | **Date attachment was first created** |
|  - qualification | 0..* | Not Used | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | **Qualifications obtained by training and certification** |
|  - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | **Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both** |
|  - - identifier | 0..* | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | **An identifier for this qualification for the practitioner** |
|  - - - use | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | **usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known. [IdentifierUse](http://hl7.org/fhir/stu3/valueset-identifier-use.html)** |
|  - - - type | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | **Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [Identifier Type Codes](http://hl7.org/fhir/stu3/valueset-identifier-type.html)** |
|  - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | **The namespace for the identifier value** |
|  - - - value | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **The value that is unique** |
|  - - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | **Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end** |
|  - - - assigner | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | **Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided** |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") | **** |
|  - - code | 1..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | **Coded representation of the qualification<br/>Binding (example): Specific qualification the practitioner has to provide a service [v2 table 0360, Version 2.7](http://hl7.org/fhir/STU3/v2/0360/2.7/index.html)** |
|  - - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | **Code defined by a terminology system** |
|  - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | **Identity of the terminology system** |
|  - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Version of the system - if relevant** |
|  - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | **Symbol in syntax defined by the system** |
|  - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Representation defined by the system** |
|  - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | **If this coding was chosen directly by the user** |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Plain text representation of the concept** |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | **Period during which the qualification is valid<br/>Constraint (per-1): If present, start SHALL have a lower value than end** |
|  - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | **Starting time with inclusive boundary** |
|  - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | **End time with inclusive boundary, if not ongoing** |
|  - - issuer | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | **Organization that regulates and issues the qualification<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided** |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") | **** |
|  - - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Literal reference, Relative, internal or absolute URL** |
|  - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | **Logical reference, when literal reference is not known** |

