---
title: Clinical Risk Factors List
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_clinical_risk_factors.html
summary: "The FHIR profiles used for the Clinical risk factors List"
---
## Heading Description ##
Details of clinical risk factors to the woman, foetus or child after birth’.

{% include custom/under.construction.html content="Please check back later for any updates to this page" %}

The following FHIR profiles are used to form the Attendance details list structure:

- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)
- [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-RiskAssessemnt-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-RiskAssessment-1)

The following profiles are referenced from the Attendance details list structure:

- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)

## Clinical Risk Factors Structure ##

{% include custom/clinical_risk_factors.svg %}

## Maternity Data Standard Mapping to FHIR profiles ##

## Mapping Overview ##


|**Data Standard Element**|**FHIR Profile Mapping**|**FHIR Element**|
|Date/Time|[List](explore_attendance_details.html#mapping-for-attendance-details-list)|period|
|ODS/ORD Site Code|[Location](explore_attendance_details.html#mapping-for-attendance-details-location)|identifier|
|Location Type|[Encounter](explore_attendance_details.html#mapping-for-attendance-details-location)|class|
|Professional Name|[Practitioner](explore_attendance_details.html#mapping-for-attendance-details-practitioner)|name|
|SDS Job Role Name|[PractitionerRole](explore_attendance_details.html#mapping-for-attendance-details-practitionerrole)|identifier|
|Contact type|[Encounter](explore_attendance_details.html#mapping-for-attendance-details-encounter)|type|
|Consultation method|[Communication](explore_attendance_details.html#mapping-for-attendance-details-communication)|medium|
|Care setting|[Location](explore_attendance_details.html#mapping-for-attendance-details-location)|type|
|Service|[EpisodeOfCare](explore_attendance_details.html#mapping-for-attendance-details-episodeofcare)|type|
|Care professional present (name)|[Practitioner](explore_attendance_details.html#mapping-for-attendance-details-practitioner)|name|
|Care professional present (role)|[PractitionerRole](explore_attendance_details.html#mapping-for-attendance-details-practitionerrole)|role|
|Care professionals present type|[Encounter](explore_attendance_details.html#mapping-for-attendance-details-encounter)|participant.type|
|First Given Name|[RelatedPerson](explore_attendance_details.html#mapping-for-attendance-details-relatedperson)|name|
|Family Name|[RelatedPerson](explore_attendance_details.html#mapping-for-attendance-details-relatedperson)|name|
|Relationship of person accompanying patient|[Encounter](explore_attendance_details.html#mapping-for-attendance-details-encounter)|participant.type|
|Outcome of contact|OutcomeOfAttendance extension |Currently not mapped due to "required" valueSet issues|


## Mapping for Clinical Risk Factors List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_clinical_risk_factors_all.html#mapping-for-clinical-risk_factors-list)**|



## Mapping for Clinical Risk Factors Encounter ##

|>|Level 1|[Encounter Resource](http://hl7.org/fhir/stu3/encounter.html)|>|Level 2|[CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)|>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_clinical_risk_factors_all.html#mapping-for-clinical-risks-factors-encounter)**| 

## Patient Reference ##

The Admission details list has a mandated subject reference to the Patient resource. This means that any exchange of the Admission details heading data must also include the [Patient demographics List.](explore_patient_demographics.html)



## Mapping for Clinical Risk Factors Practitioner ##

|>|Level 1|[Practitioner Resource](http://hl7.org/fhir/stu3/practitioner.html)|>|Level 2|[CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)|>|Level 3|None| 

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_clinical_risks_factors_all.html#mapping-for-clinical-risk-factors-practitioner)**|

## Mapping for Clinical Risk Factors PractitionerRole ##

|>|Level 1|[PractitionerRole Resource](http://hl7.org/fhir/stu3/practitionerrole.html)|>|Level 2|[CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)|>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_attendance_details_all.html#mapping-for-clinical-risk-factors-practitionerrole)**| 


## Mapping for Clinical Risk Factors Location ##

|>|Level 1|[Location Resource](http://hl7.org/fhir/stu3/location.html)|>|Level 2|[CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)|>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_clinical_risk_factors_all.html#mapping-for-clinical-risk-factors-location)**| 

## Clinical Risk Factors Heading Example ##

<script src="https://gist.github.com/IOPS-DEV/60.js"></script>
 