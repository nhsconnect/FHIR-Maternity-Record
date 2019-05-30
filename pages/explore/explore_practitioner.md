---
title: Practitioner
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_practitioner.html
summary: "The FHIR profiles used for Practitioner"
---

## Heading Description ##

A generic practitioner resource based on the CareConnect L2 [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1) profile, using the elements required to support its use within the Digital Maternity Messaging Specfication.

## Mapping for Practitioner ##

|>|Level 1|[Practitioner Resource](http://hl7.org/fhir/stu3/practitioner.html)|>|Level 2|[CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_practitioner_all.html#mapping-for-practitioner)**|

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



