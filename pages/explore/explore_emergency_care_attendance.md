---
title: Emergency Care Attendance Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_emergency_care_attendance.html
summary: "The FHIR profiles used for the Emergency Care Attendance Event Message Bundle"
---

The following FHIR profiles are used to form the Emergency Care Attendance Event Message Bundle:

- [Maternity-Record-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-Bundle-1)
- [Maternity-Record-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH011 - Emergency Care Attendance'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [Maternity-Record-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-HealthcareService-1)
- [CareConnect-Maternity-Record-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Patient-1)
- [CareConnect-Maternity-Record-Emergency-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Emergency-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-Maternity-Record-EmergencyCare-Procedure-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-EmergencyCare-Procedure-1)
- [Maternity-Record-RelatedPerson-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-RelatedPerson-1)

### Emergency Care Attendance Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| Maternity-Record Data Item                 | FHIR resource element                                                      | Mandatory/Required/Optional |
|-------------------------------|----------------------------------------------------------------------------|-----------------------------|
| Date and Time of attendance   | CareConnect-Maternity-Record-Emergency-Encounter-1.period.start                         | Mandatory                   |
| Date and Time of discharge    | CareConnect-Maternity-Record-Emergency-Encounter-1.period.end                           | Mandatory                   |
| ODS Site Code                 | CareConnect-Location-1.identifier (ODS Site Code)                      | Mandatory                   |
| Accompanied by (Name)         | Maternity-Record-RelatedPerson-1.name                                                   | Required                    |
| Accompanied by (Relationship) | Maternity-Record-RelatedPerson-1.relationship                                           | Required                    |
| Referral Source               | CareConnect-Maternity-Record-Emergency-Encounter-1.hospitalization.admitSource          | Required                    |
| Presenting Complaint          | CareConnect-Maternity-Record-Emergency-Encounter-1.reason                               | Mandatory                   |
| Procedure                     | CareConnect-Maternity-Record-EmergencyCare-Procedure-1.code                | Required                    |
| Discharge destination         | CareConnect-Maternity-Record-Emergency-Encounter-1.hospitalization.dischargeDisposition                 | Mandatory                   |
| Discharge status              | CareConnect-Maternity-Record-Emergency-Encounter-1.emergencyDischargeStatus | Mandatory                   |