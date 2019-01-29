---
title: Physical Examination Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_physical_examination.html
summary: "The FHIR profiles used for the Physical Examination Event Message Bundle"
---

The following FHIR profiles are used to form the Physical Examination Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH024 - Physical Examination'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1)
- [CareConnect-DCH-PhysicalExaminationHips-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PhysicalExaminationHips-Procedure-1)
- [CareConnect-DCH-PhysicalExaminationEyes-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PhysicalExaminationEyes-Procedure-1)
- [CareConnect-DCH-PhysicalExaminationTestes-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PhysicalExaminationTestes-Procedure-1)
- [CareConnect-DCH-PhysicalExaminationHeart-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PhysicalExaminationHeart-Procedure-1)
- [DCH-ProfessionalComment-Communication-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-ProfessionalComment-Communication-1)

### Physical Examination Details Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:
                                                                                                   
| DCH Data Item         | FHIR resource element                                         | Mandatory/Required/Optional | Note                                                                                  |
|-----------------------|---------------------------------------------------------------|-----------------------------|---------------------------------------------------------------------------------------|
| Date/Time             | CareConnect-DCH-Encounter-1.period.start                      | Mandatory                   |                                                                                       |
| ODS Site Code         | CareConnect-Location-1.identifier (ODS Site Code)         	| Mandatory                   |                                                                                       |
| Professional Name     | CareConnect-DCH-Practitioner-1.name                           | Mandatory                   |                                                                                       |
| SDS Job Role Name     | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name)   | Mandatory                   |                                                                                       |
| Outcome Status Hips   | CareConnect-DCH-PhysicalExaminationHips-Procedure-1.outcome   | Mandatory                   |                                                                                       |
| Outcome Status Eyes   | CareConnect-DCH-PhysicalExaminationEyes-Procedure-1.outcome   | Mandatory                   |                                                                                       |
| Outcome Status Testes | CareConnect-DCH-PhysicalExaminationTestes-Procedure-1.outcome | Mandatory                   |                                                                                       |
| Outcome Status Heart  | CareConnect-DCH-PhysicalExaminationHeart-Procedure-1.outcome  | Mandatory                   |                                                                                       |
| Encounter Type        | CareConnect-DCH-Encounter-1.type (childHealthEncounterType)   | Mandatory                   | Represented using code '006 - Physical Examination' OR '009 - 6-8 Week GP Led Review' |
| Comment        		| DCH-ProfessionalComment-Communication-1   					| Optional                    |  																					  |