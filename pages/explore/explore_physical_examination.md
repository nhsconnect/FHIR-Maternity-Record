---
title: Physical Examination Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_physical_examination.html
summary: "The FHIR profiles used for the Physical Examination Event Message Bundle"
---

The following FHIR profiles are used to form the Physical Examination Event Message Bundle:

- [Maternity-Record-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-Bundle-1)
- [Maternity-Record-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH024 - Physical Examination'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [Maternity-Record-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-HealthcareService-1)
- [CareConnect-Maternity-Record-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Patient-1)
- [CareConnect-Maternity-Record-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-Maternity-Record-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Practitioner-1)
- [CareConnect-Maternity-Record-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-PractitionerRole-1)
- [CareConnect-Maternity-Record-PhysicalExaminationHips-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-PhysicalExaminationHips-Procedure-1)
- [CareConnect-Maternity-Record-PhysicalExaminationEyes-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-PhysicalExaminationEyes-Procedure-1)
- [CareConnect-Maternity-Record-PhysicalExaminationTestes-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-PhysicalExaminationTestes-Procedure-1)
- [CareConnect-Maternity-Record-PhysicalExaminationHeart-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-PhysicalExaminationHeart-Procedure-1)
- [Maternity-Record-ProfessionalComment-Communication-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-ProfessionalComment-Communication-1)

### Physical Examination Details Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:
                                                                                                   
| Maternity-Record Data Item         | FHIR resource element                                         | Mandatory/Required/Optional | Note                                                                                  |
|-----------------------|---------------------------------------------------------------|-----------------------------|---------------------------------------------------------------------------------------|
| Date/Time             | CareConnect-Maternity-Record-Encounter-1.period.start                      | Mandatory                   |                                                                                       |
| ODS Site Code         | CareConnect-Location-1.identifier (ODS Site Code)         	| Mandatory                   |                                                                                       |
| Professional Name     | CareConnect-Maternity-Record-Practitioner-1.name                           | Mandatory                   |                                                                                       |
| SDS Job Role Name     | CareConnect-Maternity-Record-PractitionerRole-1.code (SDS Job Role Name)   | Mandatory                   |                                                                                       |
| Outcome Status Hips   | CareConnect-Maternity-Record-PhysicalExaminationHips-Procedure-1.outcome   | Mandatory                   |                                                                                       |
| Outcome Status Eyes   | CareConnect-Maternity-Record-PhysicalExaminationEyes-Procedure-1.outcome   | Mandatory                   |                                                                                       |
| Outcome Status Testes | CareConnect-Maternity-Record-PhysicalExaminationTestes-Procedure-1.outcome | Mandatory                   |                                                                                       |
| Outcome Status Heart  | CareConnect-Maternity-Record-PhysicalExaminationHeart-Procedure-1.outcome  | Mandatory                   |                                                                                       |
| Encounter Type        | CareConnect-Maternity-Record-Encounter-1.type (childHealthEncounterType)   | Mandatory                   | Represented using code '006 - Physical Examination' OR '009 - 6-8 Week GP Led Review' |
| Comment        		| Maternity-Record-ProfessionalComment-Communication-1   					| Optional                    |  																					  |