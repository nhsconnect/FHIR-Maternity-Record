---
title: Attendance Details List
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_attendance_details.html
summary: "The FHIR profiles used for the Attendance details List"
---

## Heading Description ##
The details of the woman’s contact with services.

The following FHIR profiles are used to form the Attendance details list structure:

- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)
- [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)
- [CareConnect-Communication-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Commmunication-1)
- [CareConnect-EpisodeOfCare-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-EpisodeOfCare-1)
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)

The following profiles are referenced from the Attendance details list structure:

- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)

## Assessment Scales Structure ##

{% include custom/attendance_details.svg %}

## Maternity Data Standard Mapping to FHIR profiles ##

## Mapping Overview ##

|**Data Standard Element**|**FHIR Profile Mapping**|**FHIR Element**|
|Date/Time|[List](explore_attendance_details.html#mapping-for-attendance_details-list)|encounter.period|
|ODS/ORD Site Code|[Location](explore_attendance_details.html#mapping-for-attendance_details-location)|location.identifier|
|Location Type|[Location](explore_attendance_details.html#mapping-for-attendance_details-location)|type|
|Professional Name|[Practitioner](explore_attendance_details.html#mapping-for-attendance_details-practitioner)|practitioner.name|
|SDS Job Role Name|[PractitionerRole](explore_attendance_details.html#mapping-for-attendance_details-practitionerrole)|encounter.period|

|Contact type|[](explore_attendance_details.html#mapping-for-attendance_details-list)|encounter.period|
|Date/Time|[List](explore_attendance_details.html#mapping-for-attendance_details-list)|encounter.period|
|SDS  |[List](explore_attendance_details.html#mapping-for-attendance_details-list)|encounter.period|