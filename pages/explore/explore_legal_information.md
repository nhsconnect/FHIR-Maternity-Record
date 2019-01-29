---
title: Legal Information Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_legal_information.html
summary: "The FHIR profiles used for the Legal Information Event Message Bundle"
---

The following FHIR profiles are used to form the Legal Information Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display elements for the 'event' type are fixed to 'CH033 - Legal Information'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-DCH-LookedAfterChildStartDate-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-LookedAfterChildStartDate-Observation-1)
- [CareConnect-DCH-LookedAfterChildEndDate-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-LookedAfterChildEndDate-Observation-1)
- [CareConnect-DCH-ChildProtectionPlanStartDate-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-ChildProtectionPlanStartDate-Observation-1)
- [CareConnect-DCH-ChildProtectionPlanEndDate-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-ChildProtectionPlanEndDate-Observation-1)

### Legal Information Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item                    | FHIR Resource element                             | Mandatory/Required/Optional |
|----------------------------------|---------------------------------------------------|-----------------------------|
| Date                             | CareConnect-DCH-Encounter-1.period.start          | Mandatory                   |
| Looked After Child Start Date    | CareConnect-DCH-LookedAfterChildStartDate-Observation-1.valueDateTime | Required                    |
| Looked After Child End Date      | CareConnect-DCH-LookedAfterChildEndDate-Observation-1.valueDateTime   | Required                    |
| Local Authority (LAC)            | CareConnect-Organization-1.name               | Required                    |
| Child Protection Plan Start Date | CareConnect-DCH-ChildProtectionPlanStartDate-Observation-1.valueDateTime       | Required                    |
| Child Protection Plan End Date   | CareConnect-DCH-ChildProtectionPlanEndDate-Observation-1.valueDateTime         | Required                    |
| Local Authority (CPP)            | CareConnect-Organization-1.name               | Required                    |