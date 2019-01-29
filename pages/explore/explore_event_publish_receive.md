---
title: Event Publishing and Receiving Requirements
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_event_publish_receive.html
summary: "Capabilities to be supported via publish and receiving requirements"
---

## Background ##
The Digital Child Health (TEST) event messages are subject to supporting the following event publishing and receiving requirements:

## Publishing Events ##

| **TBC1**    | A supplier system MUST comply to the binding strengths set out within the FHIR specification                                                                                                                                                                                                                                          |
|         | **Required:** To be conformant, the concept in this element SHALL be from the specified value set.                                                                                                                                                                                                                                        |
|         | **Extensible:** To be conformant, the concept in this element SHALL be from the specified value set if any of the codes within the value set can apply to the concept being communicated. If the value set does not cover the concept (based on human review), alternate coding’s (or, data type allowing, text) may be included instead. |
|         | **Preferred:** Instances are encouraged to draw from the specified codes for interoperability purposes but are not required to do so to be considered conformant.                                                                                                                                                                         |
|         | **Example:** Instances are not expected or even encouraged to draw from the specified value set. The value set merely provides examples of the types of concepts intended to be included.                                                                                                                                                 |
| **DCH-370** | A supplier system SHOULD send together via FHIR, any events that have occurred during the same intervention/encounter.                                                                                                                                                                                                                |
|         | All events produced during the same intervention/encounter MUST be linked to allow the events to be reformed in the subscribing supplier system. This SHOULD be done via using the "logical identifier" to ensure that there is a link when a subscribing system receives the events.                                                 |
|         | <img src="images/explore/encounter.PNG" style="width:50%;max-width: 50%;">                                                                                                                                                                                                                                                                                                                                     |
|         | For example, a **sender** creates an Immunisation bundle:                                                                                                                                                                                                                                                                                  |
|         | Sender MUST construct a DCH Immunisation bundle as a” new” message                                                                                                                                                                                                                                                                    |
|         | Sender MUST record that the Immunisation bundle has been sent                                                                                                                                                                                                                                                                         |
|         | A **sender** creates a DCH Professional Comment bundle                                                                                                                                                                                                                                                                                        |
|         | Sender MUST construct a DCH Professional Comment  bundle as a “new” message – ensuring that the same Encounter “logical” identifiers are the same as the corresponding immunisation bundle                                                                                                                                             |
|         | Sender MUST record that the Professional Comment bundle has been sent                                                                                                                                                                                                                                                                 |
| **TBC2**   | A supplier system MUST conform to the definitions of Mandatory, Required and Optional as set out in the [Healthy Child Events Specification](https://theprsb.org/standards/healthychildrecord/)                                                                                                                                           |
|         | Each event message will detail the information requirements applicable to each data item requirement, these are described as:                                                                                                                                                                                                         |
|         | **Mandatory:** should always be included in the electronic communication. Where there is no information then the message will contain appropriate coded text to identify this.                                                                                                                                                            |
|         | **Required:** where information should be recorded (and communicated) if available.                                                                                                                                                                                                                                                       |
|         | **Optional:** where local decisions can be made about whether to communicate the information                                                                                                                                                                                                                                              |
| **TBC3**   | If a data item is marked as MANDATORY or REQUIRED, it MUST not be ‘downgraded’ to OPTIONAL by local agreement. However, it COULD by local agreement be upgraded from OPTIONAL to either REQUIRED or MANDATORY.                                                                                                                        |

## Receiving Events ##

| **DCH-374** | A supplier system MUST ensure that it uses the 'logical' identifier within FHIR to link data across message bundles to make sure the information is entered into the correct part of the record. |
|         | <img src="images/explore/encounter.PNG" style="width:50%;max-width: 50%;">                                                                                                                                                                                     
|         | A **receiver** receives the immunisation bundle:                                                                                                                                                      |
|         | Receiver MUST process the immunisation bundle (keeping all the “header data”)                                                                                                                    |
|         | Receiver MUST store the encounter “logical” identifier                                                                                                                                           |
|         | Receiver MUST try to match the encounter “logical” identifier to any known professional comments encounter “logical” identifier (and link the records if found)                                  |
|         | A **receiver** receives the professional comment bundle:                                                                                                                                              |
|         | Receiver MUST process the professional comment bundle (keeping all the “header data”)                                                                                                            |
|         | Receiver MUST store the encounter “logical” identifier                                                                                                                                           |
|         | Receiver MUST try to match the encounter “logical” identifier to any known immunisation encounter “logical” identifier (and link the records if found)                                           |

