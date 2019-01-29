---
title: CareConnect FHIR Profiles
keywords:  messaging, bundles
tags: [fhir,messaging]
toc: false
sidebar: overview_sidebar
permalink: support_careconnect.html
summary: "Clarification on the application of CareConnect STU3 FHIR profiles for Digital Child Health (TEST) (DCH) event messages"
---

## Background ##
FHIR Messaging components specified within this site have been developed by NHS Digital and where applicable, use CareConnect profiles created in collaboration with the [INTEROPen](http://interopen.org) community. 

The INTEROPen vision is to create a library of nationally defined HL7® FHIR® resources and interaction patterns that implementers can adopt to simplify integration and interoperability within UK health and social care.

## Application of CareConnect STU3 FHIR profiles for Digital Child Health (TEST) ##

This Beta specification release includes FHIR profiles derived from the following CareConnect STU3 FHIR profiles and their supporting artefacts, which have been published following INTEROPen curation on the [HL7-UK github repository](https://github.com/HL7-UK/CareConnect-profiles-STU3/):

- [CareConnect-AllergyIntolerance-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-AllergyIntolerance-1)
- [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)
- [CareConnect-Immunization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Immunization-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)
- [CareConnect-Medication-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Medication-1)
- [CareConnect-MedicationRequest-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-MedicationRequest-1)
- [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1)
- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)

This Beta specification release also includes FHIR profiles derived from the following **draft** CareConnect STU3 FHIR profiles and their supporting artefacts. These have been developed by NHS Digital as part of an exercise to uplift the CareConnect DSTU2 FHIR Profiles published by INTEROPen to an STU3 equivalent, within a [feature branch](https://github.com/nhsconnect/CareConnect-profiles/tree/feature/stu3) on the [NHSConnect CareConnect profiles github repository](https://github.com/nhsconnect/CareConnect-profiles):

 - CareConnect-Condition-1
 - CareConnect-FamilyMemberHistory-1
 - CareConnect-Observation-1
 - CareConnect-Procedure-1 

Derived FHIR profiles have been developed with reference to the INTEROPen document ['Deriving-CareConnect-Profiles'](https://docs.google.com/document/d/1Fe6_w78BiNKwAnmsJi0-oQe7TRc2VpFqUQGpdpbkn7s/edit#heading=h.v4n7w91x36ud).


