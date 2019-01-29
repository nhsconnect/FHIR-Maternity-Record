---
title: Professional Contacts Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_professional_contacts.html
summary: "The FHIR profiles used for the Professional Contacts Event Message Bundle"
---

The following FHIR profiles are used to form the Professional Contacts Event Message Bundle:

- [DCH-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-Bundle-1)
- [DCH-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-MessageHeader-1) - where the coding and display elements for the 'event' type are fixed to 'CH027 - Professional Contacts'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [DCH-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-HealthcareService-1)
- [CareConnect-DCH-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Patient-1)
- [CareConnect-DCH-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [DCH-CareTeam-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-CareTeam-1)
- [CareConnect-DCH-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-Practitioner-1)
- [CareConnect-DCH-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-DCH-PractitionerRole-1)
- [DCH-ProfessionalContact-EpisodeOfCare-1](https://fhir.nhs.uk/STU3/StructureDefinition/DCH-ProfessionalContact-EpisodeOfCare-1)

### Professional Contacts Event data item mapping to FHIR profiles ###

Depending on the association, the Child Health Event data items are fulfilled by elements within the FHIR resources listed below.

## Professional Contacts Event with team association ##
                                                                                                   
| DCH Data Item                 | FHIR resource element                                                                            | Mandatory/Required/Optional |
|-------------------------------|--------------------------------------------------------------------------------------------------|-----------------------------|
| Organisation                  | CareConnect-Organization-1.identifier (ODS Code or ODS Site Code)                       | Mandatory                    |
| Team                          | DCH-CareTeam-1                                                              | Required                   |
| Role                          | DCH-CareTeam-1.participant.role                                      | Required                   |
| Care Professional Association | DCH-ProfessionalContact-EpisodeOfCare-1.type                                                                         | Mandatory                   |
| Contact details             | CareConnect-Organization-1.telecom                                                              | Required                    |
| Start date                    | DCH-ProfessionalContact-EpisodeOfCare-1.period.start                                                                 | Required                   |
| End date                      | DCH-ProfessionalContact-EpisodeOfCare-1.period.end                                                                   | Required                   |
| Reason                        | DCH-ProfessionalContact-EpisodeOfCare-1.reason                                                                   | Optional                   |

## Professional Contacts Event with care professional association ##  
                                                                                                
| DCH Data Item                 | FHIR resource element                                                                            | Mandatory/Required/Optional |
|-------------------------------|--------------------------------------------------------------------------------------------------|-----------------------------|
| Organisation                  | CareConnect-Organization-1.identifier (ODS Code or ODS Site Code)                       | Mandatory                    |
| Name                          | CareConnect-DCH-Practitioner-1.name                                                              | Required                    |
| Role                          | CareConnect-DCH-PractitionerRole-1.code (careProfessionalType)                                       | Required                  |
| Care Professional Association | DCH-ProfessionalContact-EpisodeOfCare-1.type                                                                         | Mandatory                   |
| Contact details              | CareConnect-DCH-Practitioner-1.telecom                                                           | Required                    |
| Start date                    | DCH-ProfessionalContact-EpisodeOfCare-1.period.start                                                                 | Required                   |
| End date                      | DCH-ProfessionalContact-EpisodeOfCare-1.period.end                                                                   | Required                   |
| Reason                        | DCH-ProfessionalContact-EpisodeOfCare-1.reason                                                                   | Optional                   |