---
title: Professional contacts List
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_professional_contacts.html
summary: "The FHIR profiles used for the Professional contacts List"
---

## Heading Description ##
The details of the woman’s professional contacts.

{% include custom/under.construction.html content="Please check back later for any updates to this page" %}  

The following FHIR profiles are used to form the Professional contacts List structure:  
- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)  
- [CareConnect-EpisodeOfCare-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-EpisodeOfCare-1)
- [CareConnect-CareTeam-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-CareTeam-1)  
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)  
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)

The following profiles are referenced from the Patient demographics list structure:  
- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)  

## Professional contacts Structure ##

{% include custom/prof_contacts.svg %}  

## Maternity data standard Mapping to FHIR profiles ##  

## Mapping Overview ##

|**Data Standard Element**|**FHIR Resource Mapping**|**FHIR Element**|
|Organisation|[Organization](explore_professional_contacts.html#mapping-for-professional-contacts-organization)|identifier|
|Team|[CareTeam](explore_professional_contacts.html#mapping-for-professional-contacts-careteam)|name|
|Name|[Practitioner](explore_professional_contacts.html#mapping-for-professional-contacts-practitioner)|name|  
|Role|[PractitionerRole](explore_professional_contacts.html#mapping-for-professional-contacts-practitionerrole)|code|
|CareSetting||unmapped|
|Keyworker|[PractitionerRole](explore_professional_contacts.html#mapping-for-professional-contacts-practitionerrole)|code|
|Care Professional Association|[EpisodeOfCare](explore_professional_contacts.html#mapping-for-professional-contacts-episodeofcare)|type|
|Contact details|[Organization](explore_professional_contacts.html#mapping-for-professional-contacts-organization)/[Practitioner](explore_professional_contacts.html#mapping-for-professional-contacts-practitioner)|telecom| 
|Start date|[CareTeam](explore_professional_contacts.html#mapping-for-professional-contacts-careteam)|period.start| 
|End date|[CareTeam](explore_professional_contacts.html#mapping-for-professional-contacts-careteam)|period.end| 
|Reason|[EpisodeOfCare](explore_professional_contacts.html#mapping-for-professional-contacts-episodeofcare)|reason| 


## Mapping for Professional contacts List ##  


|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3|None|  

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_professional_contacts_all.html#mapping-for-professional-contacts-list)**| 


## Mapping for Professional contacts EpisodeOfCare ##  


|>|Level 1|[EpisodeOfCare Resource](http://hl7.org/fhir/stu3/episodeofcare.html)|>|Level 2|[CareConnect-EpisodeOfCare-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-EpisodeOfCare-1)|>|Level 3|None|  

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_professional_contacts_all.html#mapping-for-professional-contacts-episodeofcare)**| 


## Mapping for Professional contacts CareTeam ##  


|>|Level 1|[CareTeam Resource](http://hl7.org/fhir/stu3/careteam.html)|>|Level 2|[CareConnect-CareTeam-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-CareTeam-1)|>|Level 3|None|  

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_professional_contacts_all.html#mapping-for-professional-contacts-careteam)**| 


## Mapping for Professional contacts Practitioner ## 

The Professional contacts List has reference(s) to the Practitioner resource. This means that any exchange of the Professional contacts List heading data must also include the [Practitioner Details](explore_practitioner.html#mapping-for-practitioner)

## Mapping for Professional contacts PractitionerRole ##  

The Professional contacts List has reference(s) to the Practitioner Role resource. This means that any exchange of the Professional contacts List heading data must also include the [Practitioner Role Details](explore_practitioner_role.html#mapping-for-practitioner_role)  

## Mapping for Professional contacts Organization ##  

The Professional contacts List has reference(s) to the Organization resource. This means that any exchange of the Professional contacts List heading data must also include the [Organization Details](explore_organization.html#mapping-for-organization)


