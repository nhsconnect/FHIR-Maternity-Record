---
title: Practitioner Role
keywords: role 
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_practitioner_role.html
summary: "The FHIR profiles used for Practitioner Role"
---

## Heading Description ##

A generic practitioner role resource created using the CareConnect Level 2 [PractitionerRole](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1) profile, using the elements required to support its use within the Digital Maternity Messaging Specfication.

## Mapping for Practitioner Role ##


|>|Level 1|[PractitionerRole Resource](http://hl7.org/fhir/stu3/practitionerrole.html)|>|Level 2|[CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_practitioner_role_all.html#mapping-for-practitioner-role)**|

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
|   |  | Mandatory | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") | <font color='red'>The responsible clinician who performs the role.<br/>This MUST use the CareConnect Practitioner profile. </font>See [Practitioner resource](explore_practitioner_all.html#mapping-for-practitioner) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL |
|  - code | 0..* | Required | CodeableConcept | Roles which this practitioner may perform<br/>Slicing: Discriminator: coding.system, Ordering: false, Rules: Open at End<br/>Binding (example): The role a person plays representing an organization [PractitionerRole](http://hl7.org/fhir/stu3/valueset-practitioner-role.html) |
|  - code (sdsJobRoleName) | 0..1 | Required | CodeableConcept | Roles which this practitioner may perform<br/>Binding (required): The role a person plays representing an organization [CareConnect-SDSJobRoleName-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-SDSJobRoleName-1) |
|  - - coding | 1..1 | Mandatory | Coding | Code defined by a terminology system |
|  - - - system | 1..1 | Mandatory | Uri | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/CodeSystem/CareConnect-SDSJobRoleName-1'</font> |
|  - - - code | 1..1 | Mandatory | Code | Symbol in syntax defined by the system |
|  - - - display | 1..1 | Mandatory | String | Representation defined by the system |
|  - - text | 0..1 | Optional | String | Plain text representation of the concept |
|  - location | 0..* | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | The location(s) at which this practitioner provides care<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") | <font color='red'>The location where the clinician performed the vaccination.<br/>This MUST use the CareConnect Location profile. </font>See [Location resource](explore_location_all.html#mapping-for-location) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL |
