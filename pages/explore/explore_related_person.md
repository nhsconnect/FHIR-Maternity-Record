---
title: Related Person
keywords: role 
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_related_person.html
summary: "The FHIR profiles used for Practitioner Role"
---

## Heading Description ##


A generic related person profile created using the CareConnect Level 2 [CareConnect-RelatedPerson-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-RelatedPerson-1) profile, using the elements required to support its use within the Digital Maternity Messaging Specfication.


## Mapping for Related Person ##

|>|Level 1|[RelatedPerson Resource](http://hl7.org/fhir/stu3/relatedPerson.html)|>|Level 2|[CareConnect-RelatedPerson](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-RelatedPerson-1)|>|Level 3|None|

|**[View Used FHIR Elements]**|**[View All FHIR Elements](explore_related_person_all.html#mapping-for-related-person)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| --- | --- | --- | --- | --- |
|  RelatedPerson | ​ |  |  | An person that is related to a patient, but who is not a direct target of care<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-RelatedPerson-1'</font> |
|  - patient | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | The patient this person is related to<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|  - - reference | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>This must use the CareConnect Patient profile.</font>See [patient resource reference](explore_allergies_and_adverse_reactions.html#patient-reference) for information on how to populate the resource. |
|  - relationship | 0..1 | Optional | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | The nature of the relationship<br/>Binding (preferred): The nature of the relationship between a patient and the related person [PatientRelationshipType](http://hl7.org/fhir/stu3/valueset-relatedperson-relationshiptype.html) |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system |
|  - - - system | 0..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>This SHOULD contain the value 'http://hl7.org/fhir/stu3/valueset-relatedperson-relationshiptype' if the preferred codeSystem is used.</font>  |
|  - - - code | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>This SHOULD contain a value from the preferred codeSystem</font> |
|  - - - display | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>This MUST contain the display associated with the code.</font> |
|  - name | 0..* | Required | [HumanName](http://hl7.org/fhir/stu3/datatypes.html#humanname "HumanName") | A name associated with the person<br/><font color='red'>Maximum 150 Characters a structured name may be sent if available.</font> |
|  - - text | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text representation of the full name<br/><font color='red'><b>Mapping to Maternity Data item = 'Person accompanying patient'</b></font> |
|  - - family | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Family name (often called 'Surname') |
|  - - given | 0..* | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Given names (not always 'first'). Includes middle names |
|  - - prefix | 0..* | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Parts that come before the name |
|  - - suffix | 0..* | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Parts that come after the name |

