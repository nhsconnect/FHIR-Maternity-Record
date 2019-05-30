---
title: Individual Requirements Bundle
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_individual_requirement.html
summary: "The FHIR profiles used for the Individual requirements Bundle"
---

## Heading Description ##
The Individual requirements that a woman has, e.g. communication, cultural, cognitive or mobility needs.

- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)
- [CareConnect-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)
- [CareConnect-Flag-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Flag-1)

The following profiles are referenced from the investigation results details list structure:

- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)

## Individual Requirements Structure Details ##

{% include custom/individual_requirements.svg %}

## Mapping Overview ##

|Date/Time|[Observation](explore_individual_requirement.html#mapping-for-individual-needs-person-observation)|effective|
|GP opt Out Indicator|[Flag](explore_individual_requirement.html#mapping-for-individual-requirements-gp-opt-out-flag)|code and value|
|Individual Needs Person Indicator|[Flag](explore_individual_requirement.html#mapping-for-individual-needs-person-indicator-flag)|code and value|
|Accessible Information - Communication Support|[Observation](explore_individual_requirement.html#mapping-for-individual-needs-person-observation)|code and value|
|Accessible Information - Requires Communication Professional||component.code|
|Accessible Information - Requires Specific Contact Method||component.code
|Accessible Information - Requires specific information format||component.code
|Mobility Needs||component.code|
|Individual Requirement Narrative Comment||comment|

## Mapping for Individual Requirements List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3| None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_safeguarding_all.html#mapping-for-safeguarding-details-list)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | Meta | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-List-1'</font> |
|  - identifier | 0..* | Required | Identifier | Business identifier<br/><font color='red'>An identifier for this Observation details list</font> |
|  - - system | 1..1 | Required | Uri | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Mandatory | String | The value that is unique<br/><font color='red'>An identifier for this Observation details list</font> |
|  - status | 1..1 | Mandatory | Code | current : retired : entered-in-error<br/>Binding (required): The current state of the list [ListStatus](http://hl7.org/fhir/stu3/valueset-list-status.html)<br/><font color='red'>The status of the list MUST contain the value 'current'</font> |
|  - mode | 1..1 | Mandatory | Code | working : snapshot : changes<br/>Binding (required): The processing mode that applies to this list [ListMode](http://hl7.org/fhir/stu3/valueset-list-mode.html)<br/><font color='red'>The mode of the list MUST contain the value 'snapshot'</font> |
|  - title | 0..1 | Mandatory | String | Descriptive name for the list<br/><font color='red'>This MUST contain the value 'Observation'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading Investigation Results'</b></font>  |
|  - code | 0..1 | Mandatory | CodeableConcept | What the purpose of this list is<br/>Binding (preferred): What the purpose of a list is [CareConnect-ListCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListCode-1)<br/><font color='red'>The PRSB heading for this list. Note: for Maternity the value stated below is used which is not from the preferred value set </font> |
|  - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system<br/><font color='red'>The SNOMED CT concept for the PRSB heading type</font> |
|  - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value '1078911000000106'</font> |
|  - - - display | 0..1 | Mandatory | String | Representation defined by the system<br/><font color='red'>This MUST contain the value 'Individual requirements'<br/>Mapping to Maternity data item = 'PSRB Heading Individual requirements'</font>  |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color="red">This is the subject of the Observations details List. This MUST use the CareConnect patient profile.</font>See [patient resource reference](explore_observations.html#patient-reference) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - date | 0..1 | Required | dateTime | When the list was prepared<br/><font color="red">This MUST contain a system date to indicate when the list was created or updated</font> |
|  - entry | 0..* | Required | BackboneElement | Entries in the list<br/><font color="red">The entries MUST be as per the diagram for this PRSB headings list with the encounter resource being the focal resource. Multiple Observations with associated resources MAY be present</font> |
|  - - date | 0..1 | Required | dateTime | When item added to list<br/><font color='red'>The SHOULD contain a system time of when the item was added to the list.</font> |
|  - - item | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color="red">A reference to an Observation resource included in the list. This MUST use the CareConnect Observation profile.</font>See [Observation resource](explore_investigation_results.html#mapping-for-investigation-results-observation) for information on how to populate the resource. |
|  - - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL <font color="red">The reference to the included Observation resource.</font> |

## Patient Reference ##

The Plan and requested actions List has a mandated subject reference to the Patient resource. This means that any exchange of the Plan and requested actions heading data must also include the [Patient demographics List.](explore_patient_demographics.html)

## Mapping for Individual Requirements GP Opt Out Flag ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/flag.html)|>|Level 2|[CareConnect-Flag-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Flag-1)|>|Level 3| None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_individual_requirement.html#mapping-for-individual-requirements-gp-opt-out-flag)**|

|  **Name** | **Card.** | Conformance | **Type** | **Description/Constraints** |
| :--- | :--- | --- | :--- | :--- |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color="red">The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Flag-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business identifier |
|  - - system | 1..1 | Required | Uri | The namespace for the identifier value |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - status | 1..1 | Mandatory | Code | active \| inactive \| entered-in-error<br/>Binding (required): Indicates whether this flag is active and needs to be displayed to a user, or whether it is no longer needed or entered in error. ( http://hl7.org/fhir/stu3/valueset-flag-status.html )<br/><font color="red">Status of the Flag</font> |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Coded or textual message to display to user<br/>Binding (example): Detail codes identifying specific flagged issues. ( http://hl7.org/fhir/stu3/valueset-flag-code.html )<br/><font color="red">MUST use a code from the valueSet https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-OptOutReason-1</font> |
|  - - coding | 0..* | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | SNOMED CT representation identifying specific flagged issues |
|  - - - extension (snomedCTDescriptionID) | 0..1 | Required | [Extension](http://hl7.org/fhir/stu3/extensibility.html#Extension "Extension") | The SNOMED CT Description ID for the display<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>URL: https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/>Fixed Value: http://snomed.info/sct |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - text | 0..1 | Optional | String | Plain text representation of the concept |
|  - subject | 1..1 | Mandatory | Reference | Who/What is flag about?<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | CareConnect-Patient-1 |  |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |


## Mapping for Individual Needs Person Indicator Flag ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/flag.html)|>|Level 2|[CareConnect-Flag-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Flag-1)|>|Level 3| None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_individual_requirement.html#mapping-for-individual-needs-person-indicator-flag)**|

|  **Name** | **Card.** | Conformance | **Type** | **Description/Constraints** |
| :--- | :--- | --- | :--- | :--- |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color="red">The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Flag-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business identifier |
|  - - system | 1..1 | Required | Uri | The namespace for the identifier value |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - status | 1..1 | Mandatory | Code | active \| inactive \| entered-in-error<br/>Binding (required): Indicates whether this flag is active and needs to be displayed to a user, or whether it is no longer needed or entered in error. ( http://hl7.org/fhir/stu3/valueset-flag-status.html )<br/><font color="red">Status of the Flag</font> |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Coded or textual message to display to user<br/>Binding (example): Detail codes identifying specific flagged issues. ( http://hl7.org/fhir/stu3/valueset-flag-code.html )<br/><font color="red">MUST use a code from the valueSet https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-IndividualNeedsPerson-1</font> |
|  - - coding | 0..* | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color="red">MUST use https://fhir.hl7.org.uk/STU3/CodeSystem/CareConnect-IndividualNeedsPerson-1</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system <font color="red">MUST use a value from https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-IndividualNeedsPerson-1</font>|
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system |
|  - - text | 0..1 | Optional | String | Plain text representation of the concept |
|  - subject | 1..1 | Mandatory | Reference | Who/What is flag about?<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | CareConnect-Patient-1 |  |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL |

## Mapping for Individual Needs Person Observation ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/observation.html)|>|Level 2|[CareConnect-Observation-1 Profile](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Observation-1)|>|Level 3| None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_individual_requirement.html#mapping-for-individual-needs-person-observation)**|


|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Observation-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business Identifier for observation<br/><font color='red'>An identifier for this Observation</font> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - - assigner | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | registered : preliminary : final : amended +<br/>Binding (required): Codes providing the status of an observation. [ObservationStatus](http://hl7.org/fhir/stu3/valueset-observation-status.html) |
|  - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of observation (code / type)<br/><font color="red">The type of investigation performed</font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system describing a type of observation [CareConnect-ObservationType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ObservationType-1) |
|  - - - extension (snomedCTDescriptionID) | 0..1 | Required | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | The SNOMED CT Description ID for the display.<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color="red">1078911000000106</font> |
|  - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color="red">Individual requirements</font> |
|  - - text | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who and/or what this is about<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|  - comment | 0..1 | Required | String |Comments about result <font color="red">Individual requirements that a person has. These may be communication, cultural, learning or mobility needs related to themselves or their primary carer</font>
|  - component | 0..* | Required | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Component results<br/><font color="red">Component is used to carry multiple individual person needs information.</font> Information MUST inlcude a code and value pair that is selected from the [Individual Needs](explore_individual_requirement.html#individual-needs-person-reference-sets) Reference sets table |
|  - - code | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Type of component observation (code / type)<br/>Binding (example): Codes identifying names of simple observations. [LOINC Codes](http://hl7.org/fhir/stu3/valueset-observation-codes.html)<br/><font color="red">MUST be a code from one of the pre-defined reference sets</font> |
|  - - coding | 0..* | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: code, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system describing a type of observation [CareConnect-ObservationType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ObservationType-1) |
|  - - - extension (snomedCTDescriptionID) | 0..1 | Required | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | The SNOMED CT Description ID for the display.<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system |
|  - value[x] | 0..1 | Required | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Actual component result<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/><font color="red">Specific information on the requirement</font> |


## Individual Needs Person Reference Sets ##

The observation resource supports multiple 'component' entries. The following component entries MAY be used with the Individual Needs person Observation.

|Element Name| Description |Reference Set Name | Reference Set Code |
|Accessible Information - Communication Support|Outlines capability and support required in order to provide accessibility, with regards to disability|Accessible information - requires communication professional simple reference set|999002151000000104 |
|Accessible Information - Requires Communication Professional|Requirement that a communication professional to be present in order to provide accessibility, with regards to disability |Accessible information - requires communication professional simple reference set|999002151000000104|
|Accessible Information - Requires Specific Contact Method|Requirement for a specific contact method in order to provide accessibility, with regards to disability|Accessible information - requires specific contact method simple reference set|999002131000000106|
|Accessible Information - Requires specific information format|Requires information in a specific format in order to provide accessibility, with regards to disability|Accessible information - requires specific information format simple reference set|999002141000000102|
|Mobility Needs|A person/parent/carer/legal guardian personal physical movement between two spaces that achieves participation and a degree of independence|Mobility findings simple reference set |999002551000000108|

## Example of Individual Requirements ##

<script src="https://gist.github.com/IOPS-DEV/b8f4178c9c6ce70bbd46351b307555d3.js"></script>
