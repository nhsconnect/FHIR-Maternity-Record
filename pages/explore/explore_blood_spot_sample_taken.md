---
title: Blood Spot Sample Taken Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_blood_spot_sample_taken.html
summary: "The FHIR profiles used for the Blood Spot Sample Taken Event Message Bundle"
---

The following FHIR profiles are used to form the Blood Spot Sample Taken Event Message Bundle:

- [Maternity-Record-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-Bundle-1)
- [Maternity-Record-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH006 - Blood Spot Sample Taken'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [Maternity-Record-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-HealthcareService-1)
- [CareConnect-Maternity-Record-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Patient-1)
- [CareConnect-Maternity-Record-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-Maternity-Record-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Practitioner-1)
- [CareConnect-Maternity-Record-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-PractitionerRole-1)
- [CareConnect-Maternity-Record-NewbornBloodSpotSampleTaken-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-NewbornBloodSpotSampleTaken-Procedure-1)
- [Maternity-Record-NewbornBloodSpotScreening-ProcedureRequest-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-NewbornBloodSpotScreening-ProcedureRequest-1)


### Blood Spot Sample Taken event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below.

| Maternity-Record Data Item     | FHIR resource element                           | Mandatory/Required/Optional |
|-------------------|-------------------------------------------------|-----------------------------|
| Date              | CareConnect-Maternity-Record-NewbornBloodSpotSampleTaken-Procedure-1.performedDateTime        | Mandatory                   |
| ODS Site Code     | CareConnect-Location-1.identifier (ODS Site Code)          | Mandatory                   |
| Professional Name | CareConnect-Maternity-Record-Practitioner-1.name | Mandatory                   |
| SDS Job Role Name | CareConnect-Maternity-Record-PractitionerRole-1.code (SDS Job Role Name)            | Mandatory                   |
| Date              | Maternity-Record-NewbornBloodSpotScreening-ProcedureRequest-1.authoredOn                | Mandatory                   |