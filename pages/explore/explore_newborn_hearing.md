---
title: Newborn Hearing Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_newborn_hearing.html
summary: "The FHIR profiles used for the Newborn Hearing Event Message Bundle"
---

- [Maternity-Record-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-Bundle-1)
- [Maternity-Record-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH021 - Newborn Hearing'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [Maternity-Record-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-HealthcareService-1)
- [CareConnect-Maternity-Record-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Patient-1)
- [CareConnect-Maternity-Record-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-Maternity-Record-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Practitioner-1)
- [CareConnect-Maternity-Record-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-PractitionerRole-1) 
- [CareConnect-Maternity-Record-AABRHearingTest-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-AABRHearingTest-Procedure-1)
- [CareConnect-Maternity-Record-AOAEHearingTest-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-AOAEHearingTest-Procedure-1)
- [CareConnect-Maternity-Record-HearingScreeningSummaryOutcome-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-HearingScreeningSummaryOutcome-Observation-1)
- [Maternity-Record-ProfessionalComment-Communication-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-ProfessionalComment-Communication-1) 

### Newborn Hearing Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:
                                                                     
| Maternity-Record Data Item       | FHIR resource element                                       | Mandatory/Required/Optional | Note                                                                  |
|---------------------|-------------------------------------------------------------|-----------------------------|-----------------------------------------------------------------------|
| Date                | CareConnect-Maternity-Record-Encounter-1.period.start                    | Mandatory                   |                                                                       |
| ODS Site Code       | CareConnect-Location-1.identifier                       | Mandatory                   |                                                                       |
| Professional Name   | CareConnect-Maternity-Record-PractitionerRole-1.code (SDS Job Role Name) | Mandatory                   |                                                                       |
| SDS Job Role Name   | CareConnect-Maternity-Record-Practitioner-1.name                         | Mandatory                   |                                                                       |
| Hearing Test Results (AABR) | CareConnect-Maternity-Record-AABRHearingTest-Procedure-1.outcome           | Required         | two occurrences of this resource are required, one for each ear |
| Hearing Test Result (AOAE) | CareConnect-Maternity-Record-AOAEHearingTest-Procedure-1.outcome             | Required          | up to four occurrences of this resource are required, with two for each test performed |
| Summary Outcome     | CareConnect-Maternity-Record-HearingScreeningSummaryOutcome-Observation-1.valueCodeableConcept        | Mandatory                   |                                                                       |
| Comment        		| Maternity-Record-ProfessionalComment-Communication-1   					| Optional                    |  																					  |