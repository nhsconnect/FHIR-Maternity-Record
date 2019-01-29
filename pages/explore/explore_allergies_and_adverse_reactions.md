---
title: Allergies and Adverse Reactions Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_allergies_and_adverse_reactions.html
summary: "The FHIR profiles used for the Allergies and Adverse Reactions Event Message Bundle"
---

The following FHIR profiles are used to form the Allergies and Adverse Reactions Event Message Bundle:

- [Maternity-Record-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-Bundle-1)
- [Maternity-Record-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-MessageHeader-1) - where the coding and display elements for the 'event' type are fixed to 'CH003 - Allergies and Adverse Reactions'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [Maternity-Record-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-HealthcareService-1)
- [CareConnect-Maternity-Record-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Patient-1)
- [CareConnect-Maternity-Record-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-Maternity-Record-AllergyIntolerance-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-AllergyIntolerance-1)


### Allergies and Drug Reactions Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:
                                                                                                   
| Maternity-Record Data Item               | FHIR resource element                                                                                   | Mandatory/Required/Optional |
|-----------------------------|---------------------------------------------------------------------------------------------------------|-----------------------------|
| Date                        | CareConnect-Maternity-Record-AllergyIntolerance-1.assertedDate      | Mandatory                   |
| Causative Agent             | CareConnect-Maternity-Record-AllergyIntolerance-1.code                                                 | Mandatory                   |
| Description of Reaction     | CareConnect-Maternity-Record-AllergyIntolerance-1.reaction.manifestation.description or                                 | Optional                    |
| 	     | CareConnect-Maternity-Record-AllergyIntolerance-1.reaction.manifestation.coding                                 | Optional                    |
| Type Of Reaction            | CareConnect-Maternity-Record-AllergyIntolerance-1.type                                                            | Optional                    |
| Certainty                   | CareConnect-Maternity-Record-AllergyIntolerance-1.verificationStatus                                         | Optional                    |
| Severity                    | CareConnect-Maternity-Record-AllergyIntolerance-1.reaction.manifestation.severity                                          | Optional                    |
| Evidence                    | CareConnect-Maternity-Record-AllergyIntolerance-1.reaction.note															| Optional                    |
| Probability of Recurrence   | CareConnect-Maternity-Record-AllergyIntolerance.reaction.note                                              | Optional                    |
| Date First Experienced      | CareConnect-Maternity-Record-AllergyIntolerance.onset                                                                | Optional                    |