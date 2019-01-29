---
title: Safety Alerts Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_safety_alerts.html
summary: "The FHIR profiles used for the Safety Alerts Event Message Bundle"
---

The following FHIR profiles are used to form the Safety Alerts Event Message Bundle:

- [Maternity-Record-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-Bundle-1)
- [Maternity-Record-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH029 - Safety Alerts'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [Maternity-Record-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-HealthcareService-1)
- [CareConnect-Maternity-Record-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Patient-1)
- [CareConnect-Maternity-Record-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-Maternity-Record-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Practitioner-1)
- [CareConnect-Maternity-Record-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-PractitionerRole-1) 
- [CareConnect-Maternity-Record-SafeguardingRisk-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-SafeguardingRisk-Observation-1)

### Safety Alerts Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| Maternity-Record Data Item     | FHIR Resource element                                       | Mandatory/Required/Optional | Note                                                                 |
|-------------------|-------------------------------------------------------------|-----------------------------|----------------------------------------------------------------------|
| Date              | CareConnect-Maternity-Record-Encounter-1.period.start                    | Mandatory                   |                                                                      |
| ODS Site Code     | CareConnect-Location-1.identifier (ODS Site Code)       | Mandatory                   |                                                                      |
| SDS Job Role Name | CareConnect-Maternity-Record-PractitionerRole-1.code (SDS Job Role Name) | Mandatory                   |                                                                      |
| Professional Name | CareConnect-Maternity-Record-Practitioner-1.name                         | Mandatory                   |                                                                      |
| Risk to self      | CareConnect-Maternity-Record-SafeguardingRisk-Observation-1.valueString  | Required                    | Represented using SNOMED CT code '886941000000103 Risk to self'      |
| Risk to others    | CareConnect-Maternity-Record-SafeguardingRisk-Observation-1.valueString  | Required                    | Represented using SNOMED CT code '886951000000100 Risk to others'    |
| Risk from others  | CareConnect-Maternity-Record-SafeguardingRisk-Observation-1.valueString  | Required                    | Represented using SNOMED CT code '1064461000000103 Risk from others' |