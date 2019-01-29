---
title: Medication Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_medication.html
summary: "The FHIR profiles used for the Medication Event Message Bundle"
---

The following FHIR profiles are used to form the Medication Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display elements for the 'event' type are fixed to 'CH019 - Medication'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1)
- [CareConnect-DCH-Medication-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Medication-1)
- [CareConnect-DCH-MedicationRequest-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-MedicationRequest-1)
- [DCH-MedicationAdministration-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MedicationAdministration-1)
- [CareConnect-DCH-MedicationStatement-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-MedicationStatement-1)  


### Medication Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below, to reflect medication either administered or prescribed:

**Medication Administered**

| DCH Data Item               | FHIR Resource element                                                     | Mandatory/Required/Optional |
|-----------------------------|---------------------------------------------------------------------------|-----------------------------|
| Date                        | DCH-MedicationAdministration-1.effectiveTimeDateTime                      | Mandatory                   |
| Start Date                  | CareConnect-DCH-MedicationRequest-1.dosageInstruction.timing.repeat.boundsPeriod.start   | Required                    |
| End Date                    | CareConnect-DCH-MedicationRequest-1.dosageInstruction.timing.repeat.boundsPeriod.end     | Required                    |
| ODS Site Code               | CareConnect-DCH-Location.identifier (ODS Site Code)                       | Required                    |
| Professional Name           | CareConnect-DCH-Practitioner-1.name                                       | Required                    |
| SDS Job Role Name           | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name)       | Required                    |
| Medication Name             | CareConnect-DCH-Medication-1.code	                                | Mandatory                   |
| Form                        | CareConnect-DCH-Medication-1.form                                 | Required                    |
| Route                       | DCH-MedicationAdministration-1.dosage.route                             | Required                    |
| Course status               | CareConnect-DCH-MedicationRequest-1.status                                  | Optional                    |
| Dose directions description | DCH-MedicationAdministration-1.dosage.text             | Optional                    |
| Dose Direction Duration     | CareConnect-DCH-MedicationStatement-1.dosage.additionalInstruction                                    | Required                    |
| Additional instruction      | CareConnect-DCH-MedicationRequest-1.dosageInstruction.additionalInstruction | Optional                    |
| Medical devices             | CareConnect-DCH-MedicationStatement-1                                                 | Optional                    |
| Indication                  | CareConnect-DCH-MedicationRequest-1.reasonCode                                  | Required                    |


**Medication Prescribed**

| DCH Data Item               | FHIR Resource element                                                     | Mandatory/Required/Optional |
|-----------------------------|---------------------------------------------------------------------------|-----------------------------|
| Date                        | CareConnect-DCH-MedicationRequest-1.authoredOn                     | Mandatory                   |
| Start Date                  | CareConnect-DCH-MedicationRequest-1.dosageInstruction.timing.repeat.boundsPeriod.start   | Required                    |
| End Date                    | CareConnect-DCH-MedicationRequest-1.dosageInstruction.timing.repeat.boundsPeriod.end     | Required                    |
| ODS Site Code               | CareConnect-DCH-Location.identifier (ODS Site Code)                       | Required                    |
| Professional Name           | CareConnect-DCH-Practitioner-1.name                                       | Required                    |
| SDS Job Role Name           | CareConnect-DCH-PractitionerRole-1.code (SDS Job Role Name)       | Required                    |
| Medication Name             | CareConnect-DCH-Medication-1.code	                                | Mandatory                   |
| Form                        | CareConnect-DCH-Medication-1.form                                 | Required                    |
| Route                       | CareConnect-DCH-MedicationRequest-1.dosageInstruction.route                             | Required                    |
| Course status               | CareConnect-DCH-MedicationRequest-1.status                                  | Optional                    |
| Dose directions description | CareConnect-DCH-MedicationRequest-1.dosageInstruction.text             | Optional                    |
| Dose Direction Duration     | CareConnect-DCH-MedicationStatement-1.dosage.additionalInstruction                                    | Required                    |
| Additional instruction      | CareConnect-DCH-MedicationRequest-1.dosageInstruction.additionalInstruction | Optional                    |
| Medical devices             | CareConnect-DCH-MedicationStatement-1                                                 | Optional                    |
| Indication                  | CareConnect-DCH-MedicationRequest-1.reasonCode                                  | Required                    |          