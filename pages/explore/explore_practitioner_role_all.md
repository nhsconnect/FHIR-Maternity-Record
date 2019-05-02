---
title: Practitioner Role
keywords: role 
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_practitioner_role_all.html
summary: "The FHIR profiles used for Practitioner Role"
---

## Heading Description ##

A generic practitioner role resource created using the CareConnect Level 2 [PractitionerRole](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1) profile, using the elements required to support its use within the Digital Maternity Messaging Specfication.

## Mapping for Assessment Scales PractitionerRole ##

|>|Level 1|[PractitionerRole Resource](http://hl7.org/fhir/stu3/practitionerRole.html)|>|Level 2|[CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)|>|Level 3|None|


|**[View Used FHIR Elements](explore_practitioner_role.html#mapping-for-practitioner-role)**|**View All FHIR Elements**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  PractitionerRole | ​ |  |  | Roles/organizations the practitioner is associated with<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource |
|  - - versionId | 0..1 | Not Used | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | **Version specific identifier** |
|  - - lastUpdated | 0..1 | Not Used | [Instant](http://hl7.org/fhir/stu3/datatypes.html#instant "Instant") | **When the resource version last changed** |
|  - - profile | 0..* | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Profiles this resource claims to conform to<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1'</font> |
|  - - security | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | **Security Labels applied to this resource<br/>Binding (extensible): Security Labels from the Healthcare Privacy and Security Classification System. [All Security Labels](http://hl7.org/fhir/stu3/valueset-security-labels.html)** |
|  - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | **Identity of the terminology system** |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Version of the system - if relevant** |
|  - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | **Symbol in syntax defined by the system** |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Representation defined by the system** |
|  - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | **If this coding was chosen directly by the user** |
|  - - tag | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | **Tags applied to this resource<br/>Binding (example): Codes that represent various types of tags, commonly workflow-related; e.g. "Needs review by Dr. Jones" [Common Tags](http://hl7.org/fhir/stu3/valueset-common-tags.html)** |
|  - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | **Identity of the terminology system** |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Version of the system - if relevant** |
|  - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | **Symbol in syntax defined by the system** |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Representation defined by the system** |
|  - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | **If this coding was chosen directly by the user** |
|  - implicitRules | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | **A set of rules under which this content was created** |
|  - language | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | **Language of the resource content<br/>Binding (extensible): A human language. [Common Languages](http://hl7.org/fhir/stu3/valueset-languages.html)** |
|  - text | 0..1 | Not Used | [Narrative](http://hl7.org/fhir/stu3/narrative.html#Narrative "Narrative") | **Text summary of the resource, for human interpretation** |
|  - - status | 1..1 | Not Used | Code | **generated : extensions : additional : empty<br/>Binding (required): The status of a resource narrative [NarrativeStatus](http://hl7.org/fhir/stu3/valueset-narrative-status.html)** |
|  - - div | 1..1 | Not Used | [Xhtml](http://hl7.org/fhir/stu3/narrative.html#xhtml "Xhtml") | **Limited xhtml content<br/>Constraint (txt-1): The narrative SHALL contain only the basic html formatting elements and attributes described in chapters 7-11 (except section 4 of chapter 9) and 15 of the HTML 4.0 standard, <a> elements (either name or href), images and internally contained style attributes<br/>Constraint (txt-2): The narrative SHALL have some non-whitespace content** |
|  - contained | 0..* | Not Used | [Resource](http://hl7.org/fhir/stu3/resource.html "Resource") | **Contained, inline Resources** |
|  - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | **Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>Slicing: Description: Extensions are always sliced by (at least) url, Discriminator: url, Ordering: false, Rules: Open** |
|  - identifier | 0..* | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | **Business Identifiers that are specific to a role/location** |
|  - - use | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | **usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known. [IdentifierUse](http://hl7.org/fhir/stu3/valueset-identifier-use.html)** |
|  - - type | 0..1 | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | **Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [Identifier Type Codes](http://hl7.org/fhir/stu3/valueset-identifier-type.html)** |
|  - - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | **Code defined by a terminology system** |
|  - - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | **Identity of the terminology system** |
|  - - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Version of the system - if relevant** |
|  - - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | **Symbol in syntax defined by the system** |
|  - - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Representation defined by the system** |
|  - - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | **If this coding was chosen directly by the user** |
|  - - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Plain text representation of the concept** |
|  - - system | 1..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | **The namespace for the identifier value** |
|  - - value | 1..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **The value that is unique** |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | **Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end** |
|  - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | **Starting time with inclusive boundary** |
|  - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | **End time with inclusive boundary, if not ongoing** |
|  - - assigner | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | **Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided** |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") | **** |
|  - - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Literal reference, Relative, internal or absolute URL** |
|  - - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | **Logical reference, when literal reference is not known** |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Text alternative for the resource** |
|  - active | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | **Whether this practitioner's record is in active use<br/>Default Value: true** |
|  - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | **The period during which the practitioner is authorized to perform in these role(s)<br/>Constraint (per-1): If present, start SHALL have a lower value than end** |
|  - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | **Starting time with inclusive boundary** |
|  - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | **End time with inclusive boundary, if not ongoing** |
|  - practitioner | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | **Practitioner that is able to provide the defined services for the organisation<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided** |
|   |  | Not Used | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") | **** |
|  - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Literal reference, Relative, internal or absolute URL** |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | **Logical reference, when literal reference is not known** |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Text alternative for the resource** |
|  - organization | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | **Organization where the roles are available<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided** |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") | **** |
|  - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Literal reference, Relative, internal or absolute URL** |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | **Logical reference, when literal reference is not known** |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Text alternative for the resource** |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Roles which this practitioner may perform<br/>Slicing: Discriminator: coding.system, Ordering: false, Rules: Open at End<br/>Binding (example): The role a person plays representing an organization [PractitionerRole](http://hl7.org/fhir/stu3/valueset-practitioner-role.html) |
|  - code (sdsJobRoleName) | 0..1 | Required | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Roles which this practitioner may perform<br/>Binding (required): The role a person plays representing an organization [CareConnect-SDSJobRoleName-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-SDSJobRoleName-1)<br/><font color='red'><b>Mapping to Maternity data item='SDS Job Role Name'.</b></font>  |
|  - - coding | 1..1 | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/CodeSystem/CareConnect-SDSJobRoleName-1'</font> |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Version of the system - if relevant** |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Representation defined by the system<br/><font color='red'>The role code of the practitioner</font> |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>The role name of the practitioner</font> |
|  - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | **If this coding was chosen directly by the user** |
|  - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Plain text representation of the concept** |
|  - specialty | 0..* | Not Used | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | **Specific specialty of the practitioner<br/>Binding (preferred): Specific specialty associated with the agency [Practice Setting Code Value Set](http://hl7.org/fhir/stu3/valueset-c80-practice-codes.html)** |
|  - - coding | 0..* | Not Used | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | **Code defined by a terminology system** |
|  - - - system | 0..1 | Not Used | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | **Identity of the terminology system** |
|  - - - version | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Version of the system - if relevant** |
|  - - - code | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | **Symbol in syntax defined by the system** |
|  - - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Representation defined by the system** |
|  - - - userSelected | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | **If this coding was chosen directly by the user** |
|  - - text | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Plain text representation of the concept** |
|  - location | 0..* | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | **The location(s) at which this practitioner provides care<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided** |
|   |  | Not Used | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") | **** |
|  - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Literal reference, Relative, internal or absolute URL** |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | **Logical reference, when literal reference is not known** |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Text alternative for the resource** |
|  - healthcareService | 0..* | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | **The list of healthcare services that this worker provides for this role's Organization/Location(s)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided** |
|   |  | Not Used | [HealthcareService](http://hl7.org/fhir/stu3/StructureDefinition/HealthcareService "HealthcareService") | **** |
|  - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Literal reference, Relative, internal or absolute URL** |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | **Logical reference, when literal reference is not known** |
|  - - display | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Text alternative for the resource** |
|  - telecom | 0..* | Not Used | [ContactPoint](http://hl7.org/fhir/stu3/datatypes.html#contactpoint "ContactPoint") | **Contact details that are specific to the role/location/service<br/>Constraint (cpt-2): A system is required if a value is provided.** |
|  - - system | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | **phone : fax : email : pager : url : sms : other<br/>Binding (required): Telecommunications form for contact point [ContactPointSystem](http://hl7.org/fhir/stu3/valueset-contact-point-system.html)** |
|  - - value | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **The actual contact point details** |
|  - - use | 0..1 | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | **home : work : temp : old : mobile - purpose of this contact point<br/>Binding (required): Use of contact point [ContactPointUse](http://hl7.org/fhir/stu3/valueset-contact-point-use.html)** |
|  - - rank | 0..1 | Not Used | [positiveInt](http://hl7.org/fhir/stu3/datatypes.html#positiveint "positiveInt") | **Specify preferred order of use (1 = highest)** |
|  - - period | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | **Time period when the contact point was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end** |
|  - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | **Starting time with inclusive boundary** |
|  - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | **End time with inclusive boundary, if not ongoing** |
|  - availableTime | 0..* | Not Used | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | **Times the Service Site is available** |
|  - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | **Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both** |
|  - - daysOfWeek | 0..* | Not Used | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | **mon : tue : wed : thu : fri : sat : sun<br/>Binding (required): The days of the week. [DaysOfWeek](http://hl7.org/fhir/stu3/valueset-days-of-week.html)** |
|  - - allDay | 0..1 | Not Used | [Boolean](http://hl7.org/fhir/stu3/datatypes.html#boolean "Boolean") | **Always available? e.g. 24 hour service** |
|  - - availableStartTime | 0..1 | Not Used | [Time](http://hl7.org/fhir/stu3/datatypes.html#time "Time") | **Opening time of day (ignored if allDay = true)** |
|  - - availableEndTime | 0..1 | Not Used | [Time](http://hl7.org/fhir/stu3/datatypes.html#time "Time") | **Closing time of day (ignored if allDay = true)** |
|  - notAvailable | 0..* | Not Used | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | **Not available during this time due to provided reason** |
|  - - modifierExtension | 0..* | Not Used | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | **Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both** |
|  - - description | 1..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Reason presented to the user explaining why time not available** |
|  - - during | 0..1 | Not Used | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") | **Service not availablefrom this date<br/>Constraint (per-1): If present, start SHALL have a lower value than end** |
|  - - - start | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | **Starting time with inclusive boundary** |
|  - - - end | 0..1 | Not Used | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | **End time with inclusive boundary, if not ongoing** |
|  - availabilityExceptions | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Description of availability exceptions** |
|  - endpoint | 0..* | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | **Technical endpoints providing access to services operated for the practitioner with this role<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided** |
|   |  | Not Used | [Endpoint](http://hl7.org/fhir/stu3/StructureDefinition/Endpoint "Endpoint") | **** |
|  - - reference | 0..1 | Not Used | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | **Literal reference, Relative, internal or absolute URL** |
|  - - identifier | 0..1 | Not Used | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | **Logical reference, when literal reference is not known** |

