---
title: Blood Spot Test Outcome Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_blood_spot_test_outcome.html
summary: "The FHIR profiles used for the Blood Spot Test Outcome Event Message Bundle"
---

The following FHIR profiles are used to form the Blood Spot Test Outcome Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH035 Blood Spot Test Outcome'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [DCH-NewbornBloodSpotScreening-DiagnosticReport-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-NewbornBloodSpotScreening-DiagnosticReport-1)
- [CareConnect-DCH-NewbornBloodSpotScreeningPKU-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NewbornBloodSpotScreeningPKU-Procedure-1)
- [CareConnect-DCH-NewbornBloodSpotScreeningSCD-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NewbornBloodSpotScreeningSCD-Procedure-1)
- [CareConnect-DCH-NewbornBloodSpotScreeningCF-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NewbornBloodSpotScreeningCF-Procedure-1)
- [CareConnect-DCH-NewbornBloodSpotScreeningCHT-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NewbornBloodSpotScreeningCHT-Procedure-1)
- [CareConnect-DCH-NewbornBloodSpotScreeningMCADD-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NewbornBloodSpotScreeningMCADD-Procedure-1)
- [CareConnect-DCH-NewbornBloodSpotScreeningHCU-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NewbornBloodSpotScreeningHCU-Procedure-1)
- [CareConnect-DCH-NewbornBloodSpotScreeningMSUD-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NewbornBloodSpotScreeningMSUD-Procedure-1)
- [CareConnect-DCH-NewbornBloodSpotScreeningGA1-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NewbornBloodSpotScreeningGA1-Procedure-1)
- [CareConnect-DCH-NewbornBloodSpotScreeningIVA-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NewbornBloodSpotScreeningIVA-Procedure-1)
- [DCH-ProfessionalComment-Communication-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-ProfessionalComment-Communication-1) 


### Blood Spot Test Outcome Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below.

| DCH Data Item                                            | FHIR resource element             | Mandatory/Required/Optional |
|----------------------------------------------------------|-----------------------------------|-----------------------------|
| Date                                                     | DCH-NewbornBloodSpotScreening-DiagnosticReport-1.issued     | Mandatory                   |
| Outcome - PHENYLKETONURIA                                | CareConnect-DCH-NewbornBloodSpotScreeningPKU-Procedure-1.outcome | Mandatory                   |
| Outcome - SICKLE CELL DISEASE                            | CareConnect-DCH-NewbornBloodSpotScreeningSCD-Procedure-1.outcome | Mandatory                   |
| Outcome - CYSTIC FIBROSIS                                | CareConnect-DCH-NewbornBloodSpotScreeningCF-Procedure-1.outcome | Mandatory                   |
| Outcome - CONGENITAL HYPOTHYROIDISM                      | CareConnect-DCH-NewbornBloodSpotScreeningCHT-Procedure-1.outcome | Mandatory                   |
| Outcome - MEDIUM CHAIN ACYL-COA DEHYDROGENASE DEFICIENCY | CareConnect-DCH-NewbornBloodSpotScreeningMCADD-Procedure-1.outcome | Mandatory                   |
| Outcome - HOMOCYSTINURIA                                 | CareConnect-DCH-NewbornBloodSpotScreeningHCU-Procedure-1.outcome | Mandatory                   |
| Outcome - MAPLE SYRUP URINE DISEASE                      | CareConnect-DCH-NewbornBloodSpotScreeningMSUD-Procedure-1.outcome | Mandatory                   |
| Outcome - GLUTARIC ACIDURIA TYPE 1                       | CareConnect-DCH-NewbornBloodSpotScreeningGA1-Procedure-1.outcome | Mandatory                   |
| Outcome - ISOVALERIC ACIDAEMIA                            | CareConnect-DCH-NewbornBloodSpotScreeningIVA-Procedure-1.outcome | Mandatory                   |
| Comment        											| DCH-ProfessionalComment-Communication-1   						| Optional                    | 

