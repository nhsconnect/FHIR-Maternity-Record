---
title: Architecture Overview
keywords:  bundle
tags: [fhir,bundles]
sidebar: foundations_sidebar
permalink: explore_overview.html
summary: "Overview of the Architecture Used for the Maternity Record"
---

## Overview ##

The Maternity Record specification is the first use by NHS Digital of PRSB headings in a structured record, previously PRSB headings have only been used in document (composition) based exchanges. The Maternity Record is not document based and makes no use of the Composition resource.
This specification details the structure of the Maternity record to satisfy some overarching business requirements. These are:

- To group, maintain context, query and retrieve the data using PRSB headings in a FHIR based Maternity record at the PRSB heading level
- To group, maintain context, query and retrieve the data at Maternity record level.

## Approach to Profiling ##

Maternity record will only use CareConnect level 2 profiles. There will be no level 3 profiles defined for the initial first of type implementations. If following consultation it is deemed necessary level 3 profiles may created. 


The proposal is to use a FHIR Bundle resource which contains a number of FHIR List resources, one List resource per PRSB Heading.

## Bundle Structure Overview Diagram ##

This diagram illustrates the way the PRSB headings are structured using the FHIR List resource within the FHIR Bundle resource.

<a href="images/explore/maternity_bundle_overview.pdf" target="_blank" style="width: 100%;max-width: 100%;"><b>Click to open in a new window</b></a>

<img src="images/explore/maternity_bundle_overview.png" style="width: auto %;height: auto%;"/>

