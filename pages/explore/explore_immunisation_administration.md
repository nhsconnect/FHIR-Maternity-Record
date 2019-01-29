---
title: Immunisation Administration Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_immunisation_administration.html
summary: "The FHIR profiles used for the Immunisation Administration Event Message Bundle"
---

The following FHIR profiles are used to form the Immunisation Administration Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH015 - Immunisation Administration'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1)
- [CareConnect-DCH-Immunization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Immunization-1)
- [CareConnect-DCH-Composition-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Composition-1)
- [CareConnect-DCH-AllergyIntolerance-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-AllergyIntolerance-1)

### Immunisation Administration Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| DCH Data Item               | FHIR resource element                                               | Mandatory/Required/Optional |
|-----------------------------|---------------------------------------------------------------------|-----------------------------|
| Date                        | CareConnect-DCH-Immunisation-1.date                                 | Mandatory                   |
| ODS Site code               | CareConnect-Location-1.identifier (ODS Site Code)               | Mandatory                   |
| Professional Name           | CareConnect-DCH-Practitioner-1.name                                 | Mandatory                   |
| SDS Job Role Name           | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name)         | Mandatory                   |
| Name of Immunisation        | CareConnect-DCH-Immunization-1.vaccinationProcedure                 | Mandatory                   |
| Dose sequence               | CareConnect-DCH-Immunization-1.vaccinationProtocol.doseSequence     | Optional                    |
| Outcome Status              | CareConnect-DCH-Immunization-1.explanation                          | Optional                    |
| Vaccine Product             | CareConnect-DCH-Immunization-1.vaccineCode                          | Required                    |
| Vaccine Manufacturer        | CareConnect-DCH-Immunization-1.manufacturer                         | Required                    |
| Batch Number                | CareConnect-DCH-Immunization-1.lotNumber                            | Required                    |
| Site                        | CareConnect-DCH-Immunization-1.site                                 | Required                    |
| Route                       | CareConnect-DCH-Immunization-1.route                                | Required                    |
| Dose Amount                 | CareConnect-DCH-Immunization-1.doseQuantity                         | Optional                    |
| Reported                    | CareConnect-DCH-Immunization-1.primarySource                        | Required                    |
| Information and Advice Given                    | CareConnect-DCH-Composition-1                   | Required                    |
| Allergies and Adverse Reactions                    | CareConnect-DCH-AllergyIntolerance-1         | Required                    |