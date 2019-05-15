---
title: Baby Details (person) List
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_baby_details_all.html
summary: "The FHIR profiles used for the Baby details (person) List"
---
{% include custom/under.construction.html content="Please check back later for any updates to this page" %}

## Heading Description ##
Birth details of the baby.

The following FHIR profiles are used to form the Baby Details (person) details list structure:

- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)
- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)
- [CareConnect-Observation](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)
- [CareConnect-ProcedureRequest-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-ProcedureRequest-1)

The following profiles are referenced from the Baby Details (person) details list structure:

- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)

## Baby Details (Person) Structure ##

{% include custom/baby_details_person.svg %}

## Maternity Data Standards Mapping to FHIR profiles ##

## Mapping Overview ##

## Mapping for Baby Details (Person) List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_baby_details.html#mapping-for-baby-details-person-list)**|

## Patient Reference ##

The Baby Details (Person) list has a mandated subject reference to the Patient resource. This means that any exchange of the Baby Details (Person) heading data must also include the [Patient demographics List.](explore_patient_demographics.html)


## Mapping for Patient Resource (baby) ##

|>|Level 1|[Patient Resource](http://hl7.org/fhir/stu3/patient.html)|>|Level 2|[CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)|>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_baby_details.html#mapping-for-patient-resource-baby)**|


## Mapping for ProcedureRequest Resource ##

|>|Level 1|[ProcedureRequest Resource](http://hl7.org/fhir/stu3/procedurerequest.html)|>|Level 2|[CareConnect-ProcedureRequest-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-ProcedureRequest-1)|>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_baby_details.html#mapping-for-procedurerequest-resource)**|


## Mapping for Observation Resource ##

|>|Level 1|[Observation Resource](http://hl7.org/fhir/stu3/observation.html)|>|Level 2|[CareConnect-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_baby_details.html#mapping-for-observation-resource)**|