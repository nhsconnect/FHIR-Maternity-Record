---
title: Blood Spot Card Received Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_blood_spot_card_received.html
summary: "The FHIR profiles used for the Blood Spot Card Received Event Message Bundle"
---

The following FHIR profiles are used to form the Blood Spot Card Received Event Message Bundle:

- [Maternity-Record-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-Bundle-1)
- [Maternity-Record-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH034 Blood Spot Card Received'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [Maternity-Record-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-HealthcareService-1)
- [CareConnect-Maternity-Record-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Patient-1)
- [CareConnect-Maternity-Record-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [Maternity-Record-NewbornBloodSpotScreening-Specimen-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-NewbornBloodSpotScreening-Specimen-1)


### Blood Spot Card Received Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below.

| Maternity-Record Data Item           | FHIR resource element                     | Mandatory/Required/Optional |
|-------------------------|-------------------------------------------|-----------------------------|
| Date                    | Maternity-Record-NewbornBloodSpotScreening-Specimen-1.receivedTime               | Mandatory                    |
| Laboratory Identifier | CareConnect-Organization-1.identifier | Mandatory                    |