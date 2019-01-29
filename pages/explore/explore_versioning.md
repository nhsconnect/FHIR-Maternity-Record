---
title: Event Versioning Approach
keywords:  messaging, versioning
tags: [fhir,versioning]
sidebar: foundations_sidebar
permalink: explore_event_versioning.html
summary: "How to manage versions of event definitions and event instances"
---

## Background ##

When thinking about managing versions in a publish/subscribe solution, there are two main aspects to consider:

- Managing changes to an event instance (e.g. publishing an update to a previously published event)
- Managing changes to the definition of events (e.g. handling changes to the fields sent in events)

This page covers the approach to be taken for both of these areas.

## Versioning of Event Instances ##

An event is packaged up as a FHIR bundle, which has the standard FHIR versioning information within it's ["meta" element](https://www.hl7.org/fhir/resource.html#Meta). This includes attributes for the versionId and lastUpdated.

- The publisher of an event MUST therefore:
	- Populate the meta.versionId attribute with a unique ID for the version of the event. Note: This can be any ID value, so may not be a sequential version number.
	- Populate the meta.lastUpdated attribute with the date/time stamp of this version of the event.

These two attributes allow receivers of events to be ensure updates to an event are processed in the correct order - specifically, the receiver MUST:

- Check the lastUpdated attribute for each new updated event received, and only process the new version if it is a later date/time than the last one processed.

Event receivers SHOULD also check that updated events with different content also have a new versionId, and generate an error if two different events are received with the same versionId

## Versioning of Event Definitions ##

When updating the national definitions (profiles) for events, we will follow the following general principles:

- Avoid breaking changes wherever possible
- Ensure breaking changes are a new major version of the event definition (using Semantic Versioning as per the general [policy for FHIR versioning](https://developer.nhs.uk/apis/fhir-policy/versioning.html))
- Because minor/patch versions of an event are non-breaking, all subscribers will be able to process different minor versions safely

However, there may also be occasions when a breaking change to an event definition is unavoidable. In those cases:

NHS Digital will publish details of the new major version as a new profile (with the major version numer in the profile ID), at which point:

- All subscribers SHOULD support new major versions within 6 months of publication
- Publishers SHOULD NOT publish any events in the new major version until 6 months after publication

The National Event Management Service:

- Will not transform any events between versions
- Will send the event to the subscriber regardless of whether they are able to support the new version (they may want to queue it and process it later)

Publishers MUST declare the event definition profile URL in the meta.profile attribute of all events they publish

When a subscriber receives an event:

- They MUST use the meta.profile element to establish the major version of the event received to establish whether they are able to process this event version
- They should then provide suitable functionality (to be determined in the design of the local system) to deal with events that are in a new format they they do not yet support - for example, they MAY:
	- Store the full resource received for later retrospective processing
	- Provide a message to the user that an event has occurred that can't be processed fully
	- Apply a standard rendering of the event so the user can see the event details even if it can't be fully parsed


