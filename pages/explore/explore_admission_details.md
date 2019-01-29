---
title: Admission Details Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_admission_details.html
summary: "The FHIR profiles used for the Admission Details Event Message Bundle"
---

The following FHIR profiles are used to form the Admission Details Event Message Bundle:

- [Maternity-Record-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-Bundle-1)
- [Maternity-Record-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH002 - Admission Details'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [Maternity-Record-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-HealthcareService-1)
- [CareConnect-Maternity-Record-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Patient-1)
- [CareConnect-Maternity-Record-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-Maternity-Record-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Practitioner-1)
- [CareConnect-Maternity-Record-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-PractitionerRole-1)
- [Maternity-Record-RelatedPerson-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-RelatedPerson-1) 


### Admission Details Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| Maternity-Record Data Item               | FHIR resource element                                   | Mandatory/Required/Optional |
|-----------------------------|---------------------------------------------------------|-----------------------------|
| Date                        | CareConnect-Maternity-Record-Encounter-1.period.start                | Mandatory                   |
| ODS Site Code               | CareConnect-Location-1.identifier (ODS Site Code)   | Mandatory                   |
| Name of Location            | CareConnect-Location-1.name   | Required                   |
| Responsible Consultant      | CareConnect-Maternity-Record-Practitioner-1                          | Required                    |
| Patient Location            | CareConnect-Location-1.type.text    | Required                   |
| Reason for Admission        | CareConnect-Maternity-Record-Encounter-1.reason.text                      | Required                    |
| Admission Method            | CareConnect-Maternity-Record-Encounter-1.hospitalization.admissionMethod | Required                    |
| Speciality                  | Maternity-Record-HealthcareService-1.serviceType.specialty or          | Required                    |
|      						  | CareConnect-Maternity-Record-PractitionerRole-1.specialty         | Required                    |
| Source of Admission         | CareConnect-Maternity-Record-Encounter-1.hospitalization.admitSource        | Required                    |
| Person accompanying patient | Maternity-Record-RelatedPerson-1                                     | Required                    |



