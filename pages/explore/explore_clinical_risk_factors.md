---
title: Clinical Risk Factors Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_clinical_risk_factors.html
summary: "The FHIR profiles used for the Clinical Risk Factors Event Message Bundle"
---

The following FHIR profiles are used to form the Clinical Risk Factors Event Message Bundle:

- [Maternity-Record-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-Bundle-1)
- [Maternity-Record-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-MessageHeader-1) - where the coding and display elements for the 'event' type are fixed to 'CH007 - Clinical Risk Factors'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [Maternity-Record-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-HealthcareService-1)
- [CareConnect-Maternity-Record-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Patient-1)
- [CareConnect-Maternity-Record-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-Maternity-Record-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Practitioner-1)
- [CareConnect-Maternity-Record-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-PractitionerRole-1)
- [Maternity-Record-ClinicalRiskFactor-RiskAssessment-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-ClinicalRiskFactor-RiskAssessment-1)

### Clinical Risk Factors Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| Maternity-Record Data Item          | FHIR resource element                                                 | Mandatory/Required/Optional |
|------------------------|-----------------------------------------------------------------------|-----------------------------|
| Date                   | Maternity-Record-ClinicalRiskFactor-RiskAssessment-1.occurrenceDateTime                                            | Mandatory                   |
| ODS Site   Code        | CareConnect-Location-1.identifier (ODS Site Code)                 | Mandatory                   |
| SDS Job   Role Name    | CareConnect-Maternity-Record-PractitionerRole-1.code (SDS Job Role Name) | Mandatory                   |
| Professional   Name    | CareConnect-Maternity-Record-Practitioner-1.name                                   | Mandatory                   |
| Relevant Clinical Risk Factor | Maternity-Record-ClinicalRiskFactor-RiskAssessment-1.prediction.outcome                             | Required                   |
| Clinical Risk Assessment      | Maternity-Record-ClinicalRiskFactor-RiskAssessment-1.method                                           | Required                 |
| Risk Mitigation      | Maternity-Record-ClinicalRiskFactor-RiskAssessment-1.mitigation                                       | Required                  |