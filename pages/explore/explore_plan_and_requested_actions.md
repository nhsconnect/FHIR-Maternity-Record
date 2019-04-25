---
title: Plan and Requested Actions List
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_plan_and_requested_actions.html
summary: "The FHIR profiles used for the Plan and requested actions Bundle"
---

## Heading Description ##
This heading gives details of planned investigations, procedures and treatment for a woman’s identified conditions and priorities.  


{% include custom/under.construction.html content="Please check back later for any updates to this page" %}

The following FHIR profiles are used to form the Plan and requested actions list structure:  
- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)  
- [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)  
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-CarePlan-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-CarePlan-1)
- [CareConnect-RelatedPerson-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-RelatedPerson-1)  
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)

The following profiles are referenced from the Patient demographics list structure:  
- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)

## Plan and Requested Actions Structure ##

{% include custom/plan_req_actions.svg %}  

## Maternity data standard Mapping to FHIR profiles ##  

## Mapping Overview ##

|**Data Standard Element**|**FHIR Resource Mapping**|**FHIR Element**|
|Date/time|[Encounter](explore_plan_and_requested_actions.html#mapping-for-plan-and-requested-actions-encounter)|period.start|
|ODS/ORD Site Code|[Location](explore_plan_and_requested_actions.html#mapping-for-plan-and-requested-actions-location)|identifier|
|SDS Job Role Name|[Practitioner](explore_plan_and_requested_actions.html#mapping-for-plan-and-requested-actions-practitioner)|code|
|Professional Name|[Practitioner](explore_plan_and_requested_actions.html#mapping-for-plan-and-requested-actions-practitioner)|name|
|Status (of professional plan)|[CarePlan](explore_plan_and_requested_actions.html#mapping-for-plan-and-requested-actions-careplan)|status (values may require discussion)|
|Type (of professional plan)|[CarePlan](explore_plan_and_requested_actions.html#mapping-for-plan-and-requested-actions-careplan)|category (values tbc)|
|Plan due date|[CarePlan](explore_plan_and_requested_actions.html#mapping-for-plan-and-requested-actions-careplan)|period.start|
|Plan details|[CarePlan](explore_plan_and_requested_actions.html#mapping-for-plan-and-requested-actions-careplan)|description| 
|Date Plan agreed|[CarePlan](explore_plan_and_requested_actions.html#mapping-for-plan-and-requested-actions-careplan)|activity.detail.scheduledPeriod.start| 
|Actions|[CarePlan](explore_plan_and_requested_actions.html#mapping-for-plan-and-requested-actions-careplan)|description| 
|Recipient|[RelatedPerson](explore_plan_and_requested_actions.html#mapping-for-plan-and-requested-actions-relatedperson)|relationship| 
 

## Mapping for Plan and Requested Actions List ##  

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_plan_and_requested_actions_all.html#mapping-for-plan-and-requested-actions-list)**| 


## Patient Reference ##

The Plan and requested actions list has a mandated subject reference to the Patient resource. This means that any exchange of the Plan and requested actions heading data must also include the [Patient demographics List.](explore_patient_demographics.html)


## Mapping for Plan and Requested Actions Encounter ##  

## Mapping for Plan and Requested Actions Location ##  

## Mapping for Plan and Requested Actions CarePlan ##  

## Mapping for Plan and Requested Actions Practitioner ##  

## Mapping for Plan and Requested Actions PractitionerRole ##  

## Mapping for Plan and Requested Actions RelatedPerson ##  


