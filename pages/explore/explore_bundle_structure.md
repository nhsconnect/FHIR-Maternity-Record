---
title: Bundle Structure
keywords:  messaging, bundles
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_bundle_structure.html
summary: "The structure of the bundle used for Digital Child Health (TEST) (Maternity-Record) event messages"
---

## The Digital Child Health (TEST) Event Message Bundle Structure ##

To enable a standardised structure to carry information regarding event messages within the scope of the Digital Child Health (TEST) Events specification, the Bundle and the Message Header resources combine to make up the initial event message bundle structure:

<img src="images/explore/Maternity-Recordbundlestructure.png" style="width:40%;max-width:40%;">

This is consistent with the [FHIR specification for the Bundle resource](http://hl7.org/fhir/bundle.html#message), which states that 'A message bundle (type = "message") consists of a series of entries, the first of which is a MessageHeader.'  

**MessageHeader focus**

The root class of the MessageHeader is fulfilled using the 'focus' element in the resource. For Digital Child Health (TEST) events this will reference the Encounter resource.

## The Digital Child Health (TEST) Event Message Bundle Structure with Event Header Items ##

The following components are then added to the initial Maternity-Record Event Message Bundle structure in order to fulfill the [event header requirement](explore_event_header_design.html).

<img src="images/explore/Maternity-Recordheaderitems.png" style="width:75%;max-width:75%;">

## The Digital Child Health (TEST) Event Message Bundle Structure with Maternity-Record Data Items ##

Finally, using the [Immunisation Administration event](explore_immunisation_administration.html) as an example, the following components are added to the Maternity-Record Event Message Bundle structure in order to fulfill the data item requirements specific to the event.

<img src="images/explore/Maternity-Recorddataitems.png" style="width:90%;max-width:90%;">









