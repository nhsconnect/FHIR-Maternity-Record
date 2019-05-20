---
title: Pregnancy Episode Details List
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_pregnancy_episode_all.html
summary: "The FHIR profiles used for the Pregnancy episode details List"
---

{% include custom/under.construction.html content="Please check back later for any updates to this page" %}

## Heading Description ##
The details of the pregnancy episode status.

The following FHIR profiles are used to form the Pregnancy episode details List structure:  
- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1) 
- [CareConnect-EpisodeOfCare-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-EpisodeOfCare-1)   
- [CareConnect-Condition-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Condition-1)
- [CareConnect-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)  

The following profiles are referenced from the Patient demographics list structure:  
- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)  

## Pregnancy episode details list Structure ##

{% include custom/pregnancy_episode_details.svg %}  

## Maternity data standard Mapping to FHIR profiles ##  

## Mapping Overview ##

|**Data Standard Element**|**FHIR Resource Mapping**|**FHIR Element**|
|Date/time|[Condition](explore_pregnancy_episode_details_all.html#mapping-for-pregnancy-episode-details-condition)|assertedDate|
|ODS/ORD Site Code|[Location](explore_pregnancy_episode_details_all.html#mapping-for-pregnancy-episode-details-location)|identifier|
|SDS Job Role Name|[PractitionerRole](explore_pregnancy_episode_details_all.html#mapping-for-pregnancy-episode-details-practitionerrole)|code|
|Performing professional|[Practitioner](explore_pregnancy_episode_details_all.html#mapping-for-pregnancy-episode-details-practitioner)|name|
|Condition|[Condition](explore_pregnancy_episode_details_all.html#mapping-for-pregnancy-episode-details-condition)|code|
|Condition onset date|[Condition](explore_pregnancy_episode_details_all.html#mapping-for-pregnancy-episode-details-condition)|onsetDateTime|
|Condition end date|[Condition](explore_pregnancy_episode_details_all.html#mapping-for-pregnancy-episode-details-condition)|abatementDateTime|
|Fetal diagnosis|[Observation](explore_pregnancy_episode_details_all.html#mapping-for-pregnancy-episode-details-observation)|description| 
|Comment|[Condition](explore_pregnancy_episode_details_all.html#mapping-for-pregnancy-episode-details-condition)|note| 


## Mapping for Pregnancy episode details List ##  


|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3|None|  

|**[View Used FHIR Elements](explore_pregnancy_episode_details_all.html#mapping-for-pregnancy-episode-details-list)**|**View All FHIR Elements**| 
