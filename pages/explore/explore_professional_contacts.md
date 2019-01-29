---
title: Professional Contacts Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_professional_contacts.html
summary: "The FHIR profiles used for the Professional Contacts Event Message Bundle"
---

The following FHIR profiles are used to form the Professional Contacts Event Message Bundle:

- [Maternity-Record-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-Bundle-1)
- [Maternity-Record-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-MessageHeader-1) - where the coding and display elements for the 'event' type are fixed to 'CH027 - Professional Contacts'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [Maternity-Record-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-HealthcareService-1)
- [CareConnect-Maternity-Record-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Patient-1)
- [CareConnect-Maternity-Record-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [Maternity-Record-CareTeam-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-CareTeam-1)
- [CareConnect-Maternity-Record-Practitioner-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Practitioner-1)
- [CareConnect-Maternity-Record-PractitionerRole-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-PractitionerRole-1)
- [Maternity-Record-ProfessionalContact-EpisodeOfCare-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-ProfessionalContact-EpisodeOfCare-1)

### Professional Contacts Event data item mapping to FHIR profiles ###

Depending on the association, the Child Health Event data items are fulfilled by elements within the FHIR resources listed below.

## Professional Contacts Event with team association ##
                                                                                                   
| Maternity-Record Data Item                 | FHIR resource element                                                                            | Mandatory/Required/Optional |
|-------------------------------|--------------------------------------------------------------------------------------------------|-----------------------------|
| Organisation                  | CareConnect-Organization-1.identifier (ODS Code or ODS Site Code)                       | Mandatory                    |
| Team                          | Maternity-Record-CareTeam-1                                                              | Required                   |
| Role                          | Maternity-Record-CareTeam-1.participant.role                                      | Required                   |
| Care Professional Association | Maternity-Record-ProfessionalContact-EpisodeOfCare-1.type                                                                         | Mandatory                   |
| Contact details             | CareConnect-Organization-1.telecom                                                              | Required                    |
| Start date                    | Maternity-Record-ProfessionalContact-EpisodeOfCare-1.period.start                                                                 | Required                   |
| End date                      | Maternity-Record-ProfessionalContact-EpisodeOfCare-1.period.end                                                                   | Required                   |
| Reason                        | Maternity-Record-ProfessionalContact-EpisodeOfCare-1.reason                                                                   | Optional                   |

## Professional Contacts Event with care professional association ##  
                                                                                                
| Maternity-Record Data Item                 | FHIR resource element                                                                            | Mandatory/Required/Optional |
|-------------------------------|--------------------------------------------------------------------------------------------------|-----------------------------|
| Organisation                  | CareConnect-Organization-1.identifier (ODS Code or ODS Site Code)                       | Mandatory                    |
| Name                          | CareConnect-Maternity-Record-Practitioner-1.name                                                              | Required                    |
| Role                          | CareConnect-Maternity-Record-PractitionerRole-1.code (careProfessionalType)                                       | Required                  |
| Care Professional Association | Maternity-Record-ProfessionalContact-EpisodeOfCare-1.type                                                                         | Mandatory                   |
| Contact details              | CareConnect-Maternity-Record-Practitioner-1.telecom                                                           | Required                    |
| Start date                    | Maternity-Record-ProfessionalContact-EpisodeOfCare-1.period.start                                                                 | Required                   |
| End date                      | Maternity-Record-ProfessionalContact-EpisodeOfCare-1.period.end                                                                   | Required                   |
| Reason                        | Maternity-Record-ProfessionalContact-EpisodeOfCare-1.reason                                                                   | Optional                   |