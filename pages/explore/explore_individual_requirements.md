---
title: Individual Requirements Event Message Bundle
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_individual_requirements.html
summary: "The FHIR profiles used for the Individual Requirements Event Message Bundle"
---

The following FHIR profiles are used to form the Individual Requirements Event Message Bundle:

- [Maternity-Record-Bundle-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-Bundle-1)
- [Maternity-Record-MessageHeader-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-MessageHeader-1) - where the coding and display for the event element is fixed to 'CH016 - Individual Requirements'
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [Maternity-Record-HealthcareService-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-HealthcareService-1)
- [CareConnect-Maternity-Record-Patient-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Patient-1)
- [CareConnect-Maternity-Record-Encounter-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Maternity-Record-Encounter-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [Maternity-Record-IndividualRequirements-QuestionnaireResponse-1](https://fhir.nhs.uk/STU3/StructureDefinition/Maternity-Record-IndividualRequirements-QuestionnaireResponse-1)


### Individual Requirements Event data item mapping to FHIR profiles ###

The Child Health Event data items are fulfilled by elements within the FHIR resources listed below:

| Maternity-Record Data Item                                                 | FHIR Resource element                                                    | Mandatory/Required/Optional |
|---------------------------------------------------------------|--------------------------------------------------------------------------|-----------------------------|
| GP Opt Out Indicator                                          | Maternity-Record-IndividualRequirements-QuestionnaireResponse-1.gPOptOutIndicator     | Required                    |
| Individual Needs Person Indicator                             | Maternity-Record-IndividualRequirements-QuestionnaireResponse-1.individualNeedsPersonIndicator | Mandatory                   |
| Accessible Information - Communication Support                | Maternity-Record-IndividualRequirements-QuestionnaireResponse-1.communicationSupport                    | Required                    |
| Accessible Information - Requires Communication Professional  | Maternity-Record-IndividualRequirements-QuestionnaireResponse-1.communicationProfessional               | Required                    |
| Accessible Information - Requires Specific Contact Method     | Maternity-Record-IndividualRequirements-QuestionnaireResponse-1.specificContactMethod                           | Required                    |
| Accessible Information - Requires specific information format | Maternity-Record-IndividualRequirements-QuestionnaireResponse-1.specificInformationFormat                       | Required                    |
| Mobility Needs                                                | Maternity-Record-IndividualRequirements-QuestionnaireResponse-1.mobilityNeeds                         | Required                    |
| Cognitive                                                     | Maternity-Record-IndividualRequirements-QuestionnaireResponse-1.cognitive                        | Required                    |