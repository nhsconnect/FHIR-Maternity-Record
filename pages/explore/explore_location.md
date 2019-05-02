---
title: Location
keywords: role 
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_location.html
summary: "The FHIR profiles used for Practitioner Role"
---

## Heading Description ##

A generic location profile created using the CareConnect Level 2 [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1) profile, using the elements required to support its use within the Digital Maternity Messaging Specfication.

## Mapping for Location ##

|>|Level 1|[Location Resource](http://hl7.org/fhir/stu3/location.html)|>|Level 2|[CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_location_all.html#mapping-for-location)**|

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

