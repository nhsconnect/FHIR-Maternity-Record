---
title: Discharge Details Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_discharge_details.html
summary: "The FHIR profiles used for the Discharge Details Event Message Bundle"
---

The following FHIR profiles are used to form the Discharge Details Event Message Bundle:

- [Maternity-Record-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-Bundle-1)
- [Maternity-Record-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH009 - Discharge Details'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [Maternity-Record-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-HealthcareService-1)
- [CareConnect-Maternity-Record-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Patient-1)
- [CareConnect-Maternity-Record-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-Maternity-Record-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Practitioner-1)
- [CareConnect-Maternity-Record-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-PractitionerRole-1) 


### Discharge Details Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| Maternity-Record Data Item                     | FHIR resource element                                            | Mandatory/Required/Optional | Note                                                                                  |
|-----------------------------------|------------------------------------------------------------------|-----------------------------|---------------------------------------------------------------------------------------|
| Date and Time of Discharge        | CareConnect-Maternity-Record-Encounter-1.period.end                           | Mandatory                   |                                                                                       |
| ODS Site Code                     | CareConnect-Location-1.identifier (ODS Site Code)            | Mandatory                   |                                                                                       |
| Name of Location                  | CareConnect-Location-1.name                                  | Required                    |                                                                                       |
| Discharging Consultant            | CareConnect-Maternity-Record-Practitioner-1                                   | Required                    |                                                                                       |
| Discharging Speciality/Department | Maternity-Record-HealthcareService-1.specialty or                             | Required                    |                                                                                       |
|                                   | CareConnect-Maternity-Record-PractitionerRole-1.specialty                     | Required                    |                                                                                       |
| Discharge method                  | CareConnect-Maternity-Record-Encounter-1.hospitalization.dischargeMethod      | Required                    |                                                                                       |
| Discharge destination             | CareConnect-Maternity-Record-Encounter-1.hospitalization.dischargeDisposition | Required                    |                                                                                       |
| Discharge address                 | CareConnect-Location-1.address                               | Required                    |                                                                                       |
| Encounter Type                    | CareConnect-Maternity-Record-Encounter-1.type (childHealthEncounterType)      | Required                    | Represented using code '001 - Birth Discharge' OR '002 - Maternity Discharge' only |
