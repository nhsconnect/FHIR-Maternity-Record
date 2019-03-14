---
title: About this specification.
keywords:  bundles
tags: [fhir]
sidebar: foundations_sidebar
permalink: overview_how_to_use.html
summary: "How to use this specification"
---

## The Approach ##

This specification uses a different approach to profiling and how the constraints the particular business use cases are applied to the FHIR resources. 

## Profiles ##
This implementation has no business specific profiles but uses the CareConnect level two profiles with additional textual constraints and guidance. This additional text will form part of any conformance testing implemented later in development. 

## Format of Textual Constraints and Guidance ##       

Each Resource used in a FHIR message, bundle or other FHIR structure is documented as a table generated from a rendered version of the CareConnect profile being used as the level 2 profile for the resource. The tables are linked to each other in the same structure that would be used in the XML or JSON instance. The table has links to various things such as the FHIR standard, profiles valuesets etc.

## The Format of the Guidance ##

Each guidance page has the following format

1. - A diagram of the FHIR message, Bundle or FHIR Structure to illustrate the resources used and references between the resources.
2. - Text which indicates the FHIR resource used, the level 2 profile used and any level 3 profile (if used). **Note**: in most implementations that use this approach there will never be any level 3 profiles.
3. - Links to allow the ability to switch from the default view, one that shows only the FHIR resource elements that are used in the FHIR resource to a view of all the elements in the FHIR resource. 
4. - A series of tables one for each CareConnect profile used.These are linked to each other following the references as per the diagram and also provide links to the NHS Digital FHIR server and the HL7 FHIR standard. The tables give the constraints and guidance for the resource above what is already enforced in the CareConnect level 2 profile. The table for each resource used in the instance is contained in a section on this page with the heading Mapping for "Resource Name" for example **Mapping for Patient**.

## The Mapping Table Format ##
The table has five columns with the following headings:
1. Name
2. Card
3. Type
4. Conformance
5. Constraints and Mapping

### Name ###
This column contains the resource name and nested below the FHIR resource elements. the nesting is illustrated using hyphens for example

**-** level 1
**- -** level 2
**- - -** level 3 etc etc

The elements are shown as per the NHS Digital FHIR server rendering and may not include every child element.

### Card ###
This is the cardinally of the element from a business perspective and may be tighter than the CareConnect profile. To follow constraint rules it will never be less constrained than the CareConnect profile.

### Conformance ###
This is conformance of FHIR element from the business perspective. It is either mandatory, required or optional these are defined as below:

-  Mandatory - The FHIR element MUST contain a value - Note the business may allow values such as "not known" or " no information" these allows value will be documented in the Constraints and mapping column.
-  Required - The sender MUST include the information or alternative values as defined by the business use case.
-  Optional - This element may be populated or not dependant on the sending system's capability.

**Note**: These are the default behaviours which may vary from use case to use case. Any variation will be documented in the relevant specification.  

### Type ###
This is the type of element as defined by the FHIR standard. The type will link to the releveant page in hte correct version of the FHIR standard.

 