---
title: Demographic History List
keywords:  bundles
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_demographic_history_all.html
summary: "The FHIR profiles used for the Demographic history list"
---

## Heading Description ##
This heading holds all of the elements for each instance of a patient demographics history as provided by the PDS previous demographic history flag.

The following FHIR profiles are used to form the Demographics history list structure:

- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)
- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)

The following profiles are referenced from the Demographics history list structure:

- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)

## Demographics History Structure ##

{% include custom/demographic_history.svg %}




## Maternity Data Standard Mapping to FHIR profiles ##

The following tables detail how to populate the FHIR resources and the mapping to the Maternity data standard.

## Mapping for Demographic History List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3|None|


|**[View Used FHIR Elements](explore_demographics_history.html#mapping-for-demographic-history-list)**|**View All FHIR Elements**|


## Mapping for Demographic History Patient ##

|>|Level 1|[Patient Resource](http://hl7.org/fhir/stu3/patient.html)|>|Level 2|[CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)|>|Level 3|None|


|**[View Used FHIR Elements](explore_demographics_history.html#mapping-for-demographic-history-patient)**|**[View All FHIR Elements]**|


## Patient Reference ##

The Admission details list has a mandated subject reference to the Patient resource. This means that any exchange of the Admission details heading data must also include the [Patient demographics List.](explore_patient_demographics.html)

## Demographics History Heading Example ##

<script src="https://gist.github.com/IOPS-DEV/9d51ee5528e59b70da255468c3da5413.js"></script>

