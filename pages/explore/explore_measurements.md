---
title: Measurements Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_measurements.html
summary: "The FHIR profiles used for the Measurements Event Message Bundle"
---

The following FHIR profiles are used to form the Measurements Event Message Bundle:

- [Maternity-Record-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-Bundle-1)
- [Maternity-Record-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH018 - Measurements'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [Maternity-Record-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-HealthcareService-1)
- [CareConnect-Maternity-Record-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Patient-1)
- [CareConnect-Maternity-Record-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-Maternity-Record-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Practitioner-1)
- [CareConnect-Maternity-Record-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-PractitionerRole-1) 
- [CareConnect-Maternity-Record-HeadCircumference-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-HeadCircumference-Observation-1)
- [CareConnect-Maternity-Record-Weight-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Weight-Observation-1)
- [CareConnect-Maternity-Record-Height-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Height-Observation-1)
- [CareConnect-Maternity-Record-Length-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Length-Observation-1)
- [CareConnect-Maternity-Record-BMICentile-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-BMICentile-Observation-1)
- [CareConnect-Maternity-Record-NCMPWithdrawal-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-NCMPWithdrawal-Observation-1)

### Measurement Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below.
                                                                                                   
| Maternity-Record Data Item            | FHIR resource element                                         | Mandatory/Required/Optional | Note                               |
|--------------------------|---------------------------------------------------------------|-----------------------------|------------------------------------|
| Date                     | CareConnect-Maternity-Record-Encounter-1.period.start                      | Mandatory                   |                                    |
| ODS Site Code            | CareConnect-Location-1.identifier (ODS Site Code)             | Mandatory                   |                                    |
| Professional Name        | CareConnect-Maternity-Record-Practitioner-1.name                           | Mandatory                   |                                    |
| SDS Job Role Name        | CareConnect-Maternity-Record-PractitionerRole-1.code (SDS Job Role Name)   | Mandatory                   |                                    |
| Birth Weight             | CareConnect-Maternity-Record-Weight-Observation-1.valueQuantity            | Required                    | Observation.code uses SNOMED CT '364589006 - Birth weight' |
| Birth head circumference | CareConnect-Maternity-Record-HeadCircumference-Observation-1.valueQuantity | Required                    | Observation.code uses SNOMED CT '169876006 - Birth head circumference'  |
| Head Circumference       | CareConnect-Maternity-Record-HeadCircumference-Observation-1.valueQuantity | Required                    | Observation.code uses SNOMED CT '363812007 - Head circumference'  |
| Weight                   | CareConnect-Maternity-Record-Weight-Observation-1.valueQuantity            | Required                    | Observation.code uses SNOMED CT '27113001 - Body weight'  |
| Height                   | CareConnect-Maternity-Record-Height-Observation-1.valueQuantity            | Required                    |                                    |
| Length                   | CareConnect-Maternity-Record-Length-Observation-1.valueQuantity            | Required                    |                                    |
| BMI centile              | CareConnect-Maternity-Record-BMICentile-Observation-1.valueQuantity        | Required                    |                                    |
| Encounter Type           | CareConnect-Maternity-Record-Encounter-1.type (childHealthEncounterType)   | Mandatory                   |                                    |
| NCMP Withdrawal Reason   | CareConnect-Maternity-Record-NCMPWithdrawal-Observation-1.valueCoding      | Required                    |                                    |                                                                                                                                                    