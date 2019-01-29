---
title: Legal Information Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_legal_information.html
summary: "The FHIR profiles used for the Legal Information Event Message Bundle"
---

The following FHIR profiles are used to form the Legal Information Event Message Bundle:

- [Maternity-Record-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-Bundle-1)
- [Maternity-Record-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-MessageHeader-1) - where the coding and display elements for the 'event' type are fixed to 'CH033 - Legal Information'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [Maternity-Record-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-HealthcareService-1)
- [CareConnect-Maternity-Record-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Patient-1)
- [CareConnect-Maternity-Record-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-Maternity-Record-LookedAfterChildStartDate-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-LookedAfterChildStartDate-Observation-1)
- [CareConnect-Maternity-Record-LookedAfterChildEndDate-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-LookedAfterChildEndDate-Observation-1)
- [CareConnect-Maternity-Record-ChildProtectionPlanStartDate-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-ChildProtectionPlanStartDate-Observation-1)
- [CareConnect-Maternity-Record-ChildProtectionPlanEndDate-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-ChildProtectionPlanEndDate-Observation-1)

### Legal Information Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| Maternity-Record Data Item                    | FHIR Resource element                             | Mandatory/Required/Optional |
|----------------------------------|---------------------------------------------------|-----------------------------|
| Date                             | CareConnect-Maternity-Record-Encounter-1.period.start          | Mandatory                   |
| Looked After Child Start Date    | CareConnect-Maternity-Record-LookedAfterChildStartDate-Observation-1.valueDateTime | Required                    |
| Looked After Child End Date      | CareConnect-Maternity-Record-LookedAfterChildEndDate-Observation-1.valueDateTime   | Required                    |
| Local Authority (LAC)            | CareConnect-Organization-1.name               | Required                    |
| Child Protection Plan Start Date | CareConnect-Maternity-Record-ChildProtectionPlanStartDate-Observation-1.valueDateTime       | Required                    |
| Child Protection Plan End Date   | CareConnect-Maternity-Record-ChildProtectionPlanEndDate-Observation-1.valueDateTime         | Required                    |
| Local Authority (CPP)            | CareConnect-Organization-1.name               | Required                    |