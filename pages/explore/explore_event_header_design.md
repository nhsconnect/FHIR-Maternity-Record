---
title: Digital Child Health (TEST) Event Header Design
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_event_header_design.html
summary: "The standard event header information applicable to Digital Child Health (TEST) (DCH) event messages"
---

## Event header information ##
Each event message will carry a standard set of event header information to help identify the patient, publisher, actual event, etc.

This event header information must consist of the following **mandatory** items and their corresponding FHIR profiles and elements:

| DCH Event Header item requirement      | FHIR resource               | FHIR element                                                                |
|----------------------------------------|-----------------------------|-----------------------------------------------------------------------------|
| patient identification data:           | CareConnect-DCH-Patient-1   |                                                                             |
| NHS Number                             | CareConnect-DCH-Patient-1   | identifier using NHS Number slice                                           |
| Date of Birth                          | CareConnect-DCH-Patient-1   | birthDate                                                                   |
| name                                   | CareConnect-DCH-Patient-1   | name                                                                        |
| event type                             | DCH-MessageHeader-1         | event                                                                       |
| type of service originating the event  | DCH-HealthcareService-1     | type 			                                                             |
| service provider originating the event | CareConnect-DCH-Encounter-1 | serviceProvider                                                             |
| IT system holding the event data       | DCH-MessageHeader-1         | source                                                                      |
| location at which the event occurred   | CareConnect-Location-1 | location                                                                    |
| event date time                        | CareConnect-DCH-Encounter-1 | period.start                                                                |
| event publisher                        | DCH-MessageHeader-1         | responsible                                                                 |
| event published date                   | DCH-MessageHeader-1         | timestamp                                                                   |
| a publication reference number         | DCH-MessageHeader-1         | The resource identifier for the MessageHeader, which will use a UUID format |

The remaining resources in the bundle depend on the Digital Child Health (TEST) Event listed under the [Messages](explore.html) section.









