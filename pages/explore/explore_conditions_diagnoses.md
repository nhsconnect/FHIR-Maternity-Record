---
title: Conditions / Diagnoses Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_conditions_diagnoses.html
summary: "The FHIR profiles used for the Conditions / Diagnoses Event Message Bundle"
---

The following FHIR profiles are used to form the Conditions / Diagnoses Event Message Bundle:

- [Maternity-Record-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-Bundle-1)
- [Maternity-Record-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-MessageHeader-1) - where the coding and display elements for the 'event' type are fixed to 'CH008 - Conditions or Diagnoses'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [Maternity-Record-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-HealthcareService-1)
- [CareConnect-Maternity-Record-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Patient-1)
- [CareConnect-Maternity-Record-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-Maternity-Record-Diagnosis-Condition-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Diagnosis-Condition-1)
- [CareConnect-Maternity-Record-Problem-Condition-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Problem-Condition-1)
- [CareConnect-Maternity-Record-FetalDiagnosis-Condition-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-FetalDiagnosis-Condition-1)

### Conditions or Diagnoses Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| Maternity-Record Data Item        | FHIR resource element                                    | Mandatory/Required/Optional | Note                    |
|----------------------|----------------------------------------------------------|-----------------------------|-------------------------|
| Condition            | CareConnect-Maternity-Record-Diagnosis-Condition-1.code or               | Mandatory                   |                         |
|                      | CareConnect-Maternity-Record-Problem-Condition-1.code                 | Mandatory                   |                         |
| Condition category   | CareConnect-Maternity-Record-Diagnosis-Condition-1.category or           | Mandatory                   | fixed value 'diagnosis' |
|                      | CareConnect-Maternity-Record-Problem-Condition-1.category             | Mandatory                   | fixed value 'problem'   |
| Stage of Disease     | CareConnect-Maternity-Record-Diagnosis-Condition-1.stage.summary.coding.text or    | Optional                    |                         |
|      | CareConnect-Maternity-Record-Problem-Condition-1.stage.summary.coding.text     | Optional                    |                         |
| Condition onset date | CareConnect-Maternity-Record-Diagnosis-Condition-1.onsetDateTime or onsetString or | Optional                    |                         |
|  | CareConnect-Maternity-Record-Problem-Condition-1.onsetDateTime or onsetString  | Optional                    |                         |
| Condition end date | CareConnect-Maternity-Record-Diagnosis-Condition-1.abatementDateTime or abatementString  | Optional                    |                         |
|  | CareConnect-Maternity-Record-Problem-Condition-1.abatementDateTime or abatementString | Optional                    |                         |
| Fetal Diagnosis      | CareConnect-Maternity-Record-FetalDiagnosis-Condition-1               | Optional                    |                         |
