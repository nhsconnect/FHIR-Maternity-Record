---
title: Explore Organization
keywords: role 
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_organization_all.html
summary: "The FHIR profile used for Organization"
---

## Heading Description ##

A generic organization profile created using the CareConnect Level 2 [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1) profile, using the elements required to support its use within the Digital Maternity Messaging Specification.

## Mapping for Organization ##

|>|Level 1|[Organization Resource](http://hl7.org/fhir/stu3/organization.html)|>|Level 2|[CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)|>|Level 3|None|


|**[View Used FHIR Elements](explore_organization.html#mapping-for-organization)**|**View All FHIR Elements**|  


|  **Name** | **Card.** | **Conformance** | **Type** | Description, Constraints and mapping for Implementation |
| :--- | :--- | :--- | :--- | :--- |
|  Organization | ​ |  |  | A grouping of people or organizations with a common purpose<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (org-1): The organization SHALL at least have a name or an id, and possibly more than one |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource <br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1'</font> |
|  - implicitRules | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | A set of rules under which this content was created |
|  - language | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Language of the resource content<br/>Binding (extensible): A human language. [Common Languages](http://hl7.org/fhir/stu3/valueset-languages.html) |
|  - text | 0..1 | Not Used | [Narrative](http://hl7.org/fhir/stu3/narrative.html#Narrative "Narrative") | Text summary of the resource, for human interpretation |
|  - contained | 0..* | Not Used | [Resource](http://hl7.org/fhir/stu3/resource.html "Resource") | Contained, inline Resources |
|  - extension (mainLocation) | 0..1 | Optional | [Extension-CareConnect-MainLocation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-MainLocation-1 "Extension-CareConnect-MainLocation-1") | Main location<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - extension (organization-period) | 0..1 | Optional | [organization-period](http://hl7.org/fhir/StructureDefinition/organization-period "organization-period") | The date range that this organization should be considered available<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>Slicing: Description: Extensions are always sliced by (at least) url, Discriminator: url, Ordering: false, Rules: Open |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Identifies this organization across multiple systems<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open at End |
|  - identifier (odsOrganisationCode) | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Organisation Data Service code |
|  - - use | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known. [IdentifierUse](http://hl7.org/fhir/stu3/valueset-identifier-use.html) |
|  - - type | 0..1 | Optional | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [Identifier Type Codes](http://hl7.org/fhir/stu3/valueset-identifier-type.html) |
|  - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/Id/ods-organization-code'</font> |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - assigner | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - identifier (odsSiteCode) | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | ODS Site code to identify the organisation at site level |
|  - - use | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known. [IdentifierUse](http://hl7.org/fhir/stu3/valueset-identifier-use.html) |
|  - - type | 0..1 | Optional | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [Identifier Type Codes](http://hl7.org/fhir/stu3/valueset-identifier-type.html) |
|  - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/Id/ods-site-code'</font> |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - assigner | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - active | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | Whether the organization's record is still in active use<br/>Default Value: true |
|  - type | 0..* | Optional | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Kind of organization<br/>Binding (example): Used to categorize the organization [OrganizationType](http://hl7.org/fhir/stu3/valueset-organization-type.html) |
|  - - coding | 0..* | Optional | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - system | 0..1 | Optional | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - code | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - userSelected | 0..1 | Optional | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - name | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Name used for the organization |
|  - alias | 0..* | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | A list of alternate names that the organization is known as, or was known as in the past |
|  - telecom | 0..* | Optional | [ContactPoint](http://hl7.org/fhir/stu3/datatypes.html#contactpoint "ContactPoint") | A contact detail for the organization<br/>Constraint (cpt-2): A system is required if a value is provided.<br/>Constraint (org-3): The telecom of an organization can never be of use 'home' |
|  - - system | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | phone : fax : email : pager : url : sms : other<br/>Binding (required): Telecommunications form for contact point [ContactPointSystem](http://hl7.org/fhir/stu3/valueset-contact-point-system.html) |
|  - - value | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The actual contact point details |
|  - - use | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | home : work : temp : old : mobile - purpose of this contact point<br/>Binding (required): Use of contact point [ContactPointUse](http://hl7.org/fhir/stu3/valueset-contact-point-use.html) |
|  - - rank | 0..1 | Optional | [positiveInt](http://hl7.org/fhir/stu3/datatypes.html#positiveint "positiveInt") | Specify preferred order of use (1 = highest) |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Time period when the contact point was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - address | 0..* | Optional | [Address](http://hl7.org/fhir/stu3/datatypes.html#address "Address") | An address for the organization<br/>Constraint (org-2): An address of an organization can never be of use 'home' |
|  - - use | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | home : work : temp : old - purpose of this address<br/>Binding (required): The use of an address [AddressUse](http://hl7.org/fhir/stu3/valueset-address-use.html) |
|  - - type | 0..1 | Optional | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | postal : physical : both<br/>Binding (required): The type of an address (physical / postal) [AddressType](http://hl7.org/fhir/stu3/valueset-address-type.html) |
|  - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text representation of the address |
|  - - line | 0..* | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Street name, number, direction & P.O. Box etc. |
|  - - city | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Name of city, town etc. |
|  - - district | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | District name (aka county) |
|  - - state | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Sub-unit of country (abbreviations ok) |
|  - - postalCode | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Postal code for area |
|  - - country | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Country (e.g. can be ISO 3166 2 or 3 letter code) |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Time period when address was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - partOf | 0..1 | Optional | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | The organization of which this organization forms a part<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Optional | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - reference | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Optional | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - contact | 0..* | Not Used | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Contact for the organization for a certain purpose |
|  - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - purpose | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | The type of contact<br/>Binding (extensible): The purpose for which you would contact a contact party [ContactEntityType](http://hl7.org/fhir/stu3/valueset-contactentity-type.html) |
|  - - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - - name | 0..1 | Not Used | [HumanName](http://hl7.org/fhir/stu3/datatypes.html#humanname "HumanName") | A name associated with the contact |
|  - - - use | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | usual : official : temp : nickname : anonymous : old : maiden<br/>Binding (required): The use of a human name [NameUse](http://hl7.org/fhir/stu3/valueset-name-use.html) |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text representation of the full name |
|  - - - family | 1..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Family name (often called 'Surname') |
|  - - - given | 0..* | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Given names (not always 'first'). Includes middle names |
|  - - - prefix | 0..* | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Parts that come before the name |
|  - - - suffix | 0..* | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Parts that come after the name |
|  - - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Time period when name was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - - telecom | 0..* | Not Used | [ContactPoint](http://hl7.org/fhir/stu3/datatypes.html#contactpoint "ContactPoint") | Contact details (telephone, email, etc.) for a contact<br/>Constraint (cpt-2): A system is required if a value is provided. |
|  - - - system | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | phone : fax : email : pager : url : sms : other<br/>Binding (required): Telecommunications form for contact point [ContactPointSystem](http://hl7.org/fhir/stu3/valueset-contact-point-system.html) |
|  - - - value | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The actual contact point details |
|  - - - use | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | home : work : temp : old : mobile - purpose of this contact point<br/>Binding (required): Use of contact point [ContactPointUse](http://hl7.org/fhir/stu3/valueset-contact-point-use.html) |
|  - - - rank | 0..1 | Not Used | [positiveInt](http://hl7.org/fhir/stu3/datatypes.html#positiveint "positiveInt") | Specify preferred order of use (1 = highest) |
|  - - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Time period when the contact point was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - - address | 0..1 | Not Used | [Address](http://hl7.org/fhir/stu3/datatypes.html#address "Address") | Visiting or postal addresses for the contact |
|  - - - use | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | home : work : temp : old - purpose of this address<br/>Binding (required): The use of an address [AddressUse](http://hl7.org/fhir/stu3/valueset-address-use.html) |
|  - - - type | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | postal : physical : both<br/>Binding (required): The type of an address (physical / postal) [AddressType](http://hl7.org/fhir/stu3/valueset-address-type.html) |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text representation of the address |
|  - - - line | 0..* | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Street name, number, direction & P.O. Box etc. |
|  - - - city | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Name of city, town etc. |
|  - - - district | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | District name (aka county) |
|  - - - state | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Sub-unit of country (abbreviations ok) |
|  - - - postalCode | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Postal code for area |
|  - - - country | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Country (e.g. can be ISO 3166 2 or 3 letter code) |
|  - - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | Time period when address was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Starting time with inclusive boundary |
|  - - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | End time with inclusive boundary, if not ongoing |
|  - endpoint | 0..* | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Technical endpoints providing access to services operated for the organization<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [Endpoint](http://hl7.org/fhir/stu3/StructureDefinition/Endpoint "Endpoint") |  |
|  - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Logical reference, when literal reference is not known |


