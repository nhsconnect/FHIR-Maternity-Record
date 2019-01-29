---
title: Blood Spot Test Outcome Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_blood_spot_test_outcome.html
summary: "The FHIR profiles used for the Blood Spot Test Outcome Event Message Bundle"
---

The following FHIR profiles are used to form the Blood Spot Test Outcome Event Message Bundle:

- [Maternity-Record-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-Bundle-1)
- [Maternity-Record-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH035 Blood Spot Test Outcome'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [Maternity-Record-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-HealthcareService-1)
- [CareConnect-Maternity-Record-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Patient-1)
- [CareConnect-Maternity-Record-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [Maternity-Record-NewbornBloodSpotScreening-DiagnosticReport-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-NewbornBloodSpotScreening-DiagnosticReport-1)
- [CareConnect-Maternity-Record-NewbornBloodSpotScreeningPKU-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-NewbornBloodSpotScreeningPKU-Procedure-1)
- [CareConnect-Maternity-Record-NewbornBloodSpotScreeningSCD-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-NewbornBloodSpotScreeningSCD-Procedure-1)
- [CareConnect-Maternity-Record-NewbornBloodSpotScreeningCF-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-NewbornBloodSpotScreeningCF-Procedure-1)
- [CareConnect-Maternity-Record-NewbornBloodSpotScreeningCHT-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-NewbornBloodSpotScreeningCHT-Procedure-1)
- [CareConnect-Maternity-Record-NewbornBloodSpotScreeningMCADD-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-NewbornBloodSpotScreeningMCADD-Procedure-1)
- [CareConnect-Maternity-Record-NewbornBloodSpotScreeningHCU-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-NewbornBloodSpotScreeningHCU-Procedure-1)
- [CareConnect-Maternity-Record-NewbornBloodSpotScreeningMSUD-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-NewbornBloodSpotScreeningMSUD-Procedure-1)
- [CareConnect-Maternity-Record-NewbornBloodSpotScreeningGA1-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-NewbornBloodSpotScreeningGA1-Procedure-1)
- [CareConnect-Maternity-Record-NewbornBloodSpotScreeningIVA-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-NewbornBloodSpotScreeningIVA-Procedure-1)
- [Maternity-Record-ProfessionalComment-Communication-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-ProfessionalComment-Communication-1) 


### Blood Spot Test Outcome Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below.

| Maternity-Record Data Item                                            | FHIR resource element             | Mandatory/Required/Optional |
|----------------------------------------------------------|-----------------------------------|-----------------------------|
| Date                                                     | Maternity-Record-NewbornBloodSpotScreening-DiagnosticReport-1.issued     | Mandatory                   |
| Outcome - PHENYLKETONURIA                                | CareConnect-Maternity-Record-NewbornBloodSpotScreeningPKU-Procedure-1.outcome | Mandatory                   |
| Outcome - SICKLE CELL DISEASE                            | CareConnect-Maternity-Record-NewbornBloodSpotScreeningSCD-Procedure-1.outcome | Mandatory                   |
| Outcome - CYSTIC FIBROSIS                                | CareConnect-Maternity-Record-NewbornBloodSpotScreeningCF-Procedure-1.outcome | Mandatory                   |
| Outcome - CONGENITAL HYPOTHYROIDISM                      | CareConnect-Maternity-Record-NewbornBloodSpotScreeningCHT-Procedure-1.outcome | Mandatory                   |
| Outcome - MEDIUM CHAIN ACYL-COA DEHYDROGENASE DEFICIENCY | CareConnect-Maternity-Record-NewbornBloodSpotScreeningMCADD-Procedure-1.outcome | Mandatory                   |
| Outcome - HOMOCYSTINURIA                                 | CareConnect-Maternity-Record-NewbornBloodSpotScreeningHCU-Procedure-1.outcome | Mandatory                   |
| Outcome - MAPLE SYRUP URINE DISEASE                      | CareConnect-Maternity-Record-NewbornBloodSpotScreeningMSUD-Procedure-1.outcome | Mandatory                   |
| Outcome - GLUTARIC ACIDURIA TYPE 1                       | CareConnect-Maternity-Record-NewbornBloodSpotScreeningGA1-Procedure-1.outcome | Mandatory                   |
| Outcome - ISOVALERIC ACIDAEMIA                            | CareConnect-Maternity-Record-NewbornBloodSpotScreeningIVA-Procedure-1.outcome | Mandatory                   |
| Comment        											| Maternity-Record-ProfessionalComment-Communication-1   						| Optional                    | 

