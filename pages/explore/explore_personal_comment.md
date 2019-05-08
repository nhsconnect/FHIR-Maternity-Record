---
title: Personal Comment List
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_personal_comment.html
summary: "The FHIR profiles used for the Personal comment List"
---

## Heading Description ##
This heading gives details of any comment recorded by the woman or her representative.  

{% include custom/under.construction.html content="Please check back later for any updates to this page" %}

The following FHIR profiles are used to form the Personal comment List structure:  
- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)
- [CareConnect-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)

The following profiles are referenced from the Patient demographics list structure:  
- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)

## Personal Comment Structure ##

{% include custom/personal_comment.svg %}  

## Maternity data standard Mapping to FHIR profiles ##  

## Mapping Overview ##

|**Data Standard Element**|**FHIR Resource Mapping**|**FHIR Element**|
|Date/time|[Observation](explore_personal_comment.html#mapping-for-personal-comment-observation)|effectiveDateTime|
|Name|[Practitioner](explore_personal_comment.html#mapping-for-personal-comment-practitioner)|name|
|Details|[Observation](explore_personal_comment.html#mapping-for-personal-comment-observation)|valueString|
|Relationship status|[PractitionerRole](explore_personal_comment.html#mapping-for-personal-comment-practitionerrole)|code|

The following tables detail how to populate the FHIR resources and the mapping to the Maternity data standard.

## Mapping for Personal comment List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_personal_comment_all.html#mapping-for-personal-comment-list)**| 


## Patient Reference ##

The Personal contacts List has a mandated subject reference to the Patient resource. This means that any exchange of the Personal contacts heading data must also include the [Patient demographics List.](explore_patient_demographics.html)


## Mapping for Personal comment Observation ##  

|>|Level 1|[Observation Resource](http://hl7.org/fhir/stu3/observation.html)|>|Level 2|[CareConnect-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)||>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_personal_comment_all.html#mapping-for-personal-comment-observation)**| 

## Mapping for Personal comment Practitioner ## 

The plan and requested actions details has reference(s) to the Practitioner resource. This means that any exchange of the plan and requested actions details heading data must also include the [Practitioner Details](explore_practitioner.html#mapping-for-practitioner)

## Mapping for Personal comment PractitionerRole ##  

The plan and requested actions details has reference(s) to the Practitioner Role resource. This means that any exchange of the plan and requested actions details heading data must also include the [Practitioner Role Details](explore_practitioner_role.html#mapping-for-practitioner_role)
