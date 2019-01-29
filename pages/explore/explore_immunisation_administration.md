---
title: Immunisation Administration Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_immunisation_administration.html
summary: "The FHIR profiles used for the Immunisation Administration Event Message Bundle"
---

The following FHIR profiles are used to form the Immunisation Administration Event Message Bundle:

- [Maternity-Record-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-Bundle-1)
- [Maternity-Record-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH015 - Immunisation Administration'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [Maternity-Record-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-HealthcareService-1)
- [CareConnect-Maternity-Record-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Patient-1)
- [CareConnect-Maternity-Record-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-Maternity-Record-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Practitioner-1)
- [CareConnect-Maternity-Record-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-PractitionerRole-1)
- [CareConnect-Maternity-Record-Immunization-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Immunization-1)
- [CareConnect-Maternity-Record-Composition-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Composition-1)
- [CareConnect-Maternity-Record-AllergyIntolerance-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-AllergyIntolerance-1)

### Immunisation Administration Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| Maternity-Record Data Item               | FHIR resource element                                               | Mandatory/Required/Optional |
|-----------------------------|---------------------------------------------------------------------|-----------------------------|
| Date                        | CareConnect-Maternity-Record-Immunisation-1.date                                 | Mandatory                   |
| ODS Site code               | CareConnect-Location-1.identifier (ODS Site Code)               | Mandatory                   |
| Professional Name           | CareConnect-Maternity-Record-Practitioner-1.name                                 | Mandatory                   |
| SDS Job Role Name           | CareConnect-Maternity-Record-PractitionerRole-1.code (SDS Job Role Name)         | Mandatory                   |
| Name of Immunisation        | CareConnect-Maternity-Record-Immunization-1.vaccinationProcedure                 | Mandatory                   |
| Dose sequence               | CareConnect-Maternity-Record-Immunization-1.vaccinationProtocol.doseSequence     | Optional                    |
| Outcome Status              | CareConnect-Maternity-Record-Immunization-1.explanation                          | Optional                    |
| Vaccine Product             | CareConnect-Maternity-Record-Immunization-1.vaccineCode                          | Required                    |
| Vaccine Manufacturer        | CareConnect-Maternity-Record-Immunization-1.manufacturer                         | Required                    |
| Batch Number                | CareConnect-Maternity-Record-Immunization-1.lotNumber                            | Required                    |
| Site                        | CareConnect-Maternity-Record-Immunization-1.site                                 | Required                    |
| Route                       | CareConnect-Maternity-Record-Immunization-1.route                                | Required                    |
| Dose Amount                 | CareConnect-Maternity-Record-Immunization-1.doseQuantity                         | Optional                    |
| Reported                    | CareConnect-Maternity-Record-Immunization-1.primarySource                        | Required                    |
| Information and Advice Given                    | CareConnect-Maternity-Record-Composition-1                   | Required                    |
| Allergies and Adverse Reactions                    | CareConnect-Maternity-Record-AllergyIntolerance-1         | Required                    |