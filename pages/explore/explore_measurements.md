---
title: Measurements Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_measurements.html
summary: "The FHIR profiles used for the Measurements Event Message Bundle"
---

The following FHIR profiles are used to form the Measurements Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH018 - Measurements'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1) 
- [CareConnect-DCH-HeadCircumference-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-HeadCircumference-Observation-1)
- [CareConnect-DCH-Weight-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Weight-Observation-1)
- [CareConnect-DCH-Height-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Height-Observation-1)
- [CareConnect-DCH-Length-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Length-Observation-1)
- [CareConnect-DCH-BMICentile-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-BMICentile-Observation-1)
- [CareConnect-DCH-NCMPWithdrawal-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-NCMPWithdrawal-Observation-1)

### Measurement Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below.
                                                                                                   
| DCH Data Item            | FHIR resource element                                         | Mandatory/Required/Optional | Note                               |
|--------------------------|---------------------------------------------------------------|-----------------------------|------------------------------------|
| Date                     | CareConnect-DCH-Encounter-1.period.start                      | Mandatory                   |                                    |
| ODS Site Code            | CareConnect-Location-1.identifier (ODS Site Code)             | Mandatory                   |                                    |
| Professional Name        | CareConnect-DCH-Practitioner-1.name                           | Mandatory                   |                                    |
| SDS Job Role Name        | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name)   | Mandatory                   |                                    |
| Birth Weight             | CareConnect-DCH-Weight-Observation-1.valueQuantity            | Required                    | Observation.code uses SNOMED CT '364589006 - Birth weight' |
| Birth head circumference | CareConnect-DCH-HeadCircumference-Observation-1.valueQuantity | Required                    | Observation.code uses SNOMED CT '169876006 - Birth head circumference'  |
| Head Circumference       | CareConnect-DCH-HeadCircumference-Observation-1.valueQuantity | Required                    | Observation.code uses SNOMED CT '363812007 - Head circumference'  |
| Weight                   | CareConnect-DCH-Weight-Observation-1.valueQuantity            | Required                    | Observation.code uses SNOMED CT '27113001 - Body weight'  |
| Height                   | CareConnect-DCH-Height-Observation-1.valueQuantity            | Required                    |                                    |
| Length                   | CareConnect-DCH-Length-Observation-1.valueQuantity            | Required                    |                                    |
| BMI centile              | CareConnect-DCH-BMICentile-Observation-1.valueQuantity        | Required                    |                                    |
| Encounter Type           | CareConnect-DCH-Encounter-1.type (childHealthEncounterType)   | Mandatory                   |                                    |
| NCMP Withdrawal Reason   | CareConnect-DCH-NCMPWithdrawal-Observation-1.valueCoding      | Required                    |                                    |                                                                                                                                                    