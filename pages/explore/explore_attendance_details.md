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

## Attendance Details Structure ##

{% include custom/attendance_details.svg %}

## Maternity Data Standard Mapping to FHIR profiles ##

## Mapping Overview ##

|**Data Standard Element**|**FHIR Profile Mapping**|**FHIR Element**|
|Date/Time|[List](explore_attendance_details.html#mapping-for-attendance_details-list)|period|
|ODS/ORD Site Code|[Location](explore_attendance_details.html#mapping-for-attendance_details-location)|identifier|
|Location Type|[Encounter](explore_attendance_details.html#mapping-for-attendance_details-location)|class|
|Professional Name|[Practitioner](explore_attendance_details.html#mapping-for-attendance_details-practitioner)|name|
|SDS Job Role Name|[PractitionerRole](explore_attendance_details.html#mapping-for-attendance_details-practitionerrole)|identifier|
|Contact type|[Encounter](explore_attendance_details.html#mapping-for-attendance_details-encounter)|type|
|Consultation method|[Communication](explore_attendance_details.html#mapping-for-attendance_details-communication)|medium|
|Care setting|[Location](explore_attendance_details.html#mapping-for-attendance_details-location)|type|
|Service|[EpisodeOfCare](explore_attendance_details.html#mapping-for-attendance_details-episodeofcare)|type|
|Care professional present (name)|[Practitioner](explore_attendance_details.html#mapping-for-attendance_details-practitioner)|name|
|Care professional present (role)|[PractitionerRole](explore_attendance_details.html#mapping-for-attendance_details-practitionerrole)|role|
|Care professionals present type|[Encounter](explore_attendance_details.html#mapping-for-attendance_details-encounter)|participant.type|
|First Given Name|[RelatedPerson](explore_attendance_details.html#mapping-for-attendance_details-relatedperson)|name|
|Family Name|[RelatedPerson](explore_attendance_details.html#mapping-for-attendance_details-relatedperson)|name|
|Relationship of person accompanying patient|[Encounter](explore_attendance_details.html#mapping-for-attendance_details-encounter)|participant.type|
|Outcome of contact|Currently not mapped|Currently not mapped|

  
