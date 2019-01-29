---
title: Medication Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_medication.html
summary: "The FHIR profiles used for the Medication Event Message Bundle"
---

The following FHIR profiles are used to form the Medication Event Message Bundle:

- [Maternity-Record-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-Bundle-1)
- [Maternity-Record-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-MessageHeader-1) - where the coding and display elements for the 'event' type are fixed to 'CH019 - Medication'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [Maternity-Record-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-HealthcareService-1)
- [CareConnect-Maternity-Record-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Patient-1)
- [CareConnect-Maternity-Record-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-Maternity-Record-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Practitioner-1)
- [CareConnect-Maternity-Record-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-PractitionerRole-1)
- [CareConnect-Maternity-Record-Medication-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Medication-1)
- [CareConnect-Maternity-Record-MedicationRequest-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-MedicationRequest-1)
- [Maternity-Record-MedicationAdministration-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-MedicationAdministration-1)
- [CareConnect-Maternity-Record-MedicationStatement-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-MedicationStatement-1)  


### Medication Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below, to reflect medication either administered or prescribed:

**Medication Administered**

| Maternity-Record Data Item               | FHIR Resource element                                                     | Mandatory/Required/Optional |
|-----------------------------|---------------------------------------------------------------------------|-----------------------------|
| Date                        | Maternity-Record-MedicationAdministration-1.effectiveTimeDateTime                      | Mandatory                   |
| Start Date                  | CareConnect-Maternity-Record-MedicationRequest-1.dosageInstruction.timing.repeat.boundsPeriod.start   | Required                    |
| End Date                    | CareConnect-Maternity-Record-MedicationRequest-1.dosageInstruction.timing.repeat.boundsPeriod.end     | Required                    |
| ODS Site Code               | CareConnect-Maternity-Record-Location.identifier (ODS Site Code)                       | Required                    |
| Professional Name           | CareConnect-Maternity-Record-Practitioner-1.name                                       | Required                    |
| SDS Job Role Name           | CareConnect-Maternity-Record-PractitionerRole-1.code (SDS Job Role Name)       | Required                    |
| Medication Name             | CareConnect-Maternity-Record-Medication-1.code	                                | Mandatory                   |
| Form                        | CareConnect-Maternity-Record-Medication-1.form                                 | Required                    |
| Route                       | Maternity-Record-MedicationAdministration-1.dosage.route                             | Required                    |
| Course status               | CareConnect-Maternity-Record-MedicationRequest-1.status                                  | Optional                    |
| Dose directions description | Maternity-Record-MedicationAdministration-1.dosage.text             | Optional                    |
| Dose Direction Duration     | CareConnect-Maternity-Record-MedicationStatement-1.dosage.additionalInstruction                                    | Required                    |
| Additional instruction      | CareConnect-Maternity-Record-MedicationRequest-1.dosageInstruction.additionalInstruction | Optional                    |
| Medical devices             | CareConnect-Maternity-Record-MedicationStatement-1                                                 | Optional                    |
| Indication                  | CareConnect-Maternity-Record-MedicationRequest-1.reasonCode                                  | Required                    |


**Medication Prescribed**

| Maternity-Record Data Item               | FHIR Resource element                                                     | Mandatory/Required/Optional |
|-----------------------------|---------------------------------------------------------------------------|-----------------------------|
| Date                        | CareConnect-Maternity-Record-MedicationRequest-1.authoredOn                     | Mandatory                   |
| Start Date                  | CareConnect-Maternity-Record-MedicationRequest-1.dosageInstruction.timing.repeat.boundsPeriod.start   | Required                    |
| End Date                    | CareConnect-Maternity-Record-MedicationRequest-1.dosageInstruction.timing.repeat.boundsPeriod.end     | Required                    |
| ODS Site Code               | CareConnect-Maternity-Record-Location.identifier (ODS Site Code)                       | Required                    |
| Professional Name           | CareConnect-Maternity-Record-Practitioner-1.name                                       | Required                    |
| SDS Job Role Name           | CareConnect-Maternity-Record-PractitionerRole-1.code (SDS Job Role Name)       | Required                    |
| Medication Name             | CareConnect-Maternity-Record-Medication-1.code	                                | Mandatory                   |
| Form                        | CareConnect-Maternity-Record-Medication-1.form                                 | Required                    |
| Route                       | CareConnect-Maternity-Record-MedicationRequest-1.dosageInstruction.route                             | Required                    |
| Course status               | CareConnect-Maternity-Record-MedicationRequest-1.status                                  | Optional                    |
| Dose directions description | CareConnect-Maternity-Record-MedicationRequest-1.dosageInstruction.text             | Optional                    |
| Dose Direction Duration     | CareConnect-Maternity-Record-MedicationStatement-1.dosage.additionalInstruction                                    | Required                    |
| Additional instruction      | CareConnect-Maternity-Record-MedicationRequest-1.dosageInstruction.additionalInstruction | Optional                    |
| Medical devices             | CareConnect-Maternity-Record-MedicationStatement-1                                                 | Optional                    |
| Indication                  | CareConnect-Maternity-Record-MedicationRequest-1.reasonCode                                  | Required                    |          