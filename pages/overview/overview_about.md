---
title: About this specification.
keywords:  bundles
tags: [fhir]
sidebar: foundations_sidebar
permalink: overview_about.html
summary: "How to use this specification"
---

# The Approach #

This specification uses a different approach to profiling and how the constraints the particular business use cases are applied to the FHIR resources. 

# Profiles #
This implementation has no business specific profiles but uses the CareConnect level two profiles and additional textual constraints and guidance. This additional text will form part of any conformance testing implemented later in development. 

# Format of Textual Constraints and Guidance #       

Each Resource used in a FHIR message, bundle or other FHIR structure is documented as a table generated from a rendered version of the CareConnect profile being use for the resource. The tables are linked to each other in the same structure that would be used in the XML or JSON instance. The table has links to various things such as the FHIR standard, profiles valuesets etc.

# The Resource Tables Explained #
The table for each resource used in the instance is contained in a section with the heading Mapping for "Resource Name" for example ## Mapping for Patient ##
