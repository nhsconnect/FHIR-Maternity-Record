---
title: Admission Details Bundle
keywords:  bundles
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_admission_details_all.html
summary: "The FHIR profiles used for the Admission Details Bundle"
---

## Heading Description ##
The details of the woman’s admission.

The following FHIR profiles are used to form the Admission details list structure:

- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)
- [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)
- [RelatedPerson](http://hl7.org/fhir/STU3/relatedperson.html)
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)

The following profiles are referenced from the Admission details list structure:

- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)

## Admission Details Structure ##

{% include custom/admission_details.svg %}


## Maternity Data Set Mapping to FHIR profiles ##

The following tables detail how to populate the FHIR resources and the mapping to the Maternity data set.

## Mapping for Admission Details List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3|None|


|**[View Used FHIR Elements](explore_admission_details.html#mapping-for-admission-details-list)**|**[View All FHIR Elements]**|


|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  List | ​ |  |  | Information summarized from a list of other resources<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (lst-2): The deleted flag can only be used if the mode of the list is "changes"<br/>Constraint (lst-1): A list can only have an emptyReason if it is empty |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | Meta | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-List-1'</font> |
|  - implicitRules | 0..1 | Not Used | Uri | A set of rules under which this content was created |
|  - language | 0..1 | Not Used | Code | Language of the resource content<br/>Binding (extensible): A human language. [Common Languages](http://hl7.org/fhir/stu3/valueset-languages.html) |
|  - text | 0..1 | Not Used | Narrative | Text summary of the resource, for human interpretation |
|  - contained | 0..* | Not Used | Resource | Contained, inline Resources |
|  - extension (clinicalSetting) | 0..1 | Not Used | [Extension-CareConnect-ClinicalSetting-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-ClinicalSetting-1 "Extension-CareConnect-ClinicalSetting-1") | **To record the clinical setting of a problem list<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>** |
|  - extension (warningCode) | 0..1 | Not Used | [Extension-CareConnect-ListWarningCode-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-ListWarningCode-1 "Extension-CareConnect-ListWarningCode-1") | **To capture warnings that the list may be incomplete<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>** |
|  - modifierExtension | 0..* | Not Used | Extension | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>Slicing: Description: Extensions are always sliced by (at least) url, Discriminator: url, Ordering: false, Rules: Open |
|  - identifier | 0..* | Required | Identifier | Business identifier<br/><font color='red'>An identifier for this Admission details list</font><br/> |
|  - - use | 0..1 | Not Used | Code | usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known. [IdentifierUse](http://hl7.org/fhir/stu3/valueset-identifier-use.html) |
|  - - type | 0..1 | Not Used | CodeableConcept | Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [Identifier Type Codes](http://hl7.org/fhir/stu3/valueset-identifier-type.html) |
|  - - - coding | 0..* | Not Used | Coding | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | Uri | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | Code | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | String | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | String | Plain text representation of the concept |
|  - - system | 1..1 | Required | Uri | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Mandatory | String | The value that is unique<br/>Business identifier<br/><font color='red'>An identifier for this Admission details list</font> |
|  - - period | 0..1 | Not Used | Period | <font color='red'>A identifier'</font> |
|  - - - start | 0..1 | Not Used | dateTime | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | dateTime | End time with inclusive boundary, if not ongoing |
|  - - assigner | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - - reference | 0..1 | Not Used | String | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Required | String | Text alternative for the resource<br/><font color='red'>The organization that allocated the identifier</font> |
|  - status | 1..1 | Mandatory | Code | current : retired : entered-in-error<br/>Binding (required): The current state of the list [ListStatus](http://hl7.org/fhir/stu3/valueset-list-status.html)<br/><font color='red'>The status of the list MUST contain the value 'current'</font> |
|  - mode | 1..1 | Mandatory | Code | working : snapshot : changes<br/>Binding (required): The processing mode that applies to this list [ListMode](http://hl7.org/fhir/stu3/valueset-list-mode.html)<br/><font color='red'>The mode of the list MUST contain the value 'snapshot'</font> |
|  - title | 0..1 | Mandatory | String | Descriptive name for the list<br/><font color='red'>This MUST contain the value 'Admission details'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading Admission details'</b></font>  |
|  - code | 0..1 | Mandatory | CodeableConcept | What the purpose of this list is<br/>Binding (preferred): What the purpose of a list is [CareConnect-ListCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListCode-1)<br/><font color='red'>The PRSB heading for this list. Note: for Maternity the value stated below is used which is not from the preferred value set </font> |
|  - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system<br/><font color='red'>The SNOMED CT concept for the PRSB heading type</font> |
|  - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - version | 0..1 | Not Used | String | Version of the system - if relevant<br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font>  |
|  - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value '886781000000108'</font> |
|  - - - display | 0..1 | Mandatory | String | Representation defined by the system<br/><font color='red'>This MUST contain the value 'Admission details'</font><br/><font color='red'>Mapping to Maternity data item = 'PSRB Heading Admission details'</font>  |
|  - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - text | 0..1 | Not Used | String | Plain text representation of the concept |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Not Used | [Group](http://hl7.org/fhir/STU3/group.html "Group") |  |
|   |  | Not Used | [Device](http://hl7.org/fhir/stu3/StructureDefinition/Device "Device") |  |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color='red'>This is the subject of the Admission details List.<br/>This MUST use the CareConnect patient profile. </font>See [patient resource](explore_admission_details.html#mapping-for-admission-details-patient) for information on how to populate the resource. |
|   |  | Not Used | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") |  |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - encounter | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Context in which list created<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>A reference to the encounter resource within the Admission details list. </font/> <br/> |
|   |  | Not Used | [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1 "CareConnect-Encounter-1") | This is the context of the Admission details List.<br/>This MUST use the CareConnect encounter profile. See [encounter resource](explore_admission_details.html#mapping-for-admission-details-encounter) for information on how to populate the resource. |
|  - - reference | 0..1 | Not Used | String | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - date | 0..1 | Mandatory | dateTime | When the list was prepared<br/><font color='red'> This MUST contain a system date to indicate when the list created or updated</font> |
|  - source | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who and/or what defined the list contents (aka Author)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [Device](http://hl7.org/fhir/stu3/StructureDefinition/Device "Device") |  |
|   |  | Not Used | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|   |  | Not Used | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") |  |
|  - - reference | 0..1 | Not Used | String | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - orderedBy | 0..1 | Not Used | CodeableConcept | What order the list has<br/>Binding (preferred): What order applies to the items in a list [List Order Codes](http://hl7.org/fhir/stu3/valueset-list-order.html) |
|  - - coding | 0..* | Not Used | Coding | Code defined by a terminology system |
|  - - - system | 0..1 | Not Used | Uri | Identity of the terminology system |
|  - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - code | 0..1 | Not Used | Code | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Not Used | String | Representation defined by the system |
|  - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - text | 0..1 | Not Used | String | Plain text representation of the concept |
|  - note | 0..* | Optional | Annotation | Comments about the list |
|  - - author[x] | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Individual responsible for the annotation<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [RelatedPerson](http://hl7.org/fhir/stu3/StructureDefinition/RelatedPerson "RelatedPerson") |  |
|   |  | Not Used | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|   |  | Not Used | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") |  |
|   |  | Required | String | <font color='red'>Who authored the comment on the list.</font>  |
|  - - time | 0..1 | Required | dateTime | When the annotation was made |
|  - - text | 1..1 | Required | String | The annotation - text content |
|  - entry | 0..* | Mandatory | BackboneElement | Entries in the list<br/><font color='red'>The entries MUST be as per the diagram for this PRSB headings list with the encounter resource being the focal resource. Multiple Encounters with associated resources MAY be present</font> |
|  - - modifierExtension | 0..* | Not Used | Extension | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - flag | 0..1 | Not Used | CodeableConcept | Status/Workflow information about this item<br/>Binding (example): Codes that provide further information about the reason and meaning of the item in the list [Patient Medicine Change Types](http://hl7.org/fhir/stu3/valueset-list-item-flag.html) |
|  - - - coding | 0..* | Not Used | Coding | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | Uri | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | Code | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | String | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | String | Plain text representation of the concept |
|  - - deleted | 0..1 | Not Used | Boolean | If this item is actually marked as deleted<br/>Default Value: false |
|  - - date | 0..1 | Required | dateTime | When item added to list<br/><font color='red'>The SHOULD contain a system time of when the item was added to the list.</font> |
|  - - item | 1..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>A reference to an Encounter resource included in the list<br/>This MUST use the CareConnect Encounter profile. </font>See [Encounter resource](explore_admission_details.html#mapping-for-admission-details-encounter) for information on how to populate the resource. |
|   |  | Not Used | [Resource](http://hl7.org/fhir/stu3/StructureDefinition/Resource "Resource") |  |
|  - - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL<br/><font color='red'>The reference to the included Encounter resource.</font> |
|  - - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - emptyReason | 0..1 | Not Used | CodeableConcept | Why list is empty<br/>Binding (preferred): If a list is empty, why it is empty [CareConnect-ListEmptyReasonCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListEmptyReasonCode-1) |
|  - - coding | 0..* | Not Used | Coding | Code defined by a terminology system |
|  - - - system | 0..1 | Not Used | Uri | Identity of the terminology system |
|  - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - code | 0..1 | Not Used | Code | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Not Used | String | Representation defined by the system |
|  - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - text | 0..1 | Not Used | String | Plain text representation of the concept |


## Mapping for Admission Details Encounter ##

|>|Level 1|[Encounter Resource](http://hl7.org/fhir/stu3/encounter.html)|>|Level 2|[CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)|>|Level 3|None|


|**[View Used FHIR Elements](explore_admission_details.html#mapping-for-admission-details-encounter)**|**[View All FHIR Elements]**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  Encounter | ​ |  |  | An interaction during which services are provided to the patient<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | Meta | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Encounter-1'</font> |
|  - implicitRules | 0..1 | Not Used | Uri | A set of rules under which this content was created |
|  - language | 0..1 | Not Used | Code | Language of the resource content<br/>Binding (extensible): A human language. [Common Languages](http://hl7.org/fhir/stu3/valueset-languages.html) |
|  - text | 0..1 | Not Used | Narrative | Text summary of the resource, for human interpretation |
|  - contained | 0..* | Not Used | Resource | Contained, inline Resources |
|  - extension (encounterTransport) | 0..1 | Not Used | [Extension-CareConnect-EncounterTransport-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-EncounterTransport-1 "Extension-CareConnect-EncounterTransport-1") | Encounter transport<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - extension (outcomeOfAttendance) | 0..1 | Not Used | [Extension-CareConnect-OutcomeOfAttendance-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-OutcomeOfAttendance-1 "Extension-CareConnect-OutcomeOfAttendance-1") | An extension to the Encounter resource to record the outcome of an Out-Patient attendance.<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - extension (emergencyCareDischargeStatus) | 0..1 | Not Used | [Extension-CareConnect-EmergencyCareDischargeStatus-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-EmergencyCareDischargeStatus-1 "Extension-CareConnect-EmergencyCareDischargeStatus-1") | An extension to the Encounter resource which is used indicate the status of the Patient on discharge from an Emergency Care Department.<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - modifierExtension | 0..* | Not Used | Extension | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>Slicing: Description: Extensions are always sliced by (at least) url, Discriminator: url, Ordering: false, Rules: Open |
|  - identifier | 0..* | Required | Identifier | Identifier(s) by which this encounter is known<br/><font color='red'>An identifier for this Encounter</font> |
|  - - use | 0..1 | Not Used | Code | usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known. [IdentifierUse](http://hl7.org/fhir/stu3/valueset-identifier-use.html) |
|  - - type | 0..1 | Not Used | CodeableConcept | Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [Identifier Type Codes](http://hl7.org/fhir/stu3/valueset-identifier-type.html) |
|  - - - coding | 0..* | Not Used | Coding | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | Uri | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | Code | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | String | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | String | Plain text representation of the concept |
|  - - system | 1..1 | Required | Uri | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Required | String | The value that is unique<br/><font color='red'>An identifier for this Admission details list</font> |
|  - - period | 0..1 | Not Used | Period | Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | dateTime | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | dateTime | End time with inclusive boundary, if not ongoing |
|  - - assigner | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - - reference | 0..1 | Not Used | String | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - status | 1..1 | Mandatory | Code | planned : arrived : triaged : in-progress : onleave : finished : cancelled +<br/>Binding (required): Current state of the encounter [EncounterStatus](http://hl7.org/fhir/stu3/valueset-encounter-status.html)<br/><font color='red'>The status of the Encounter MUST contain the value 'finished'</font> |
|  - statusHistory | 0..* | Not Used | BackboneElement | List of past encounter statuses |
|  - - modifierExtension | 0..* | Not Used | Extension | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - status | 1..1 | Not Used | Code | planned : arrived : triaged : in-progress : onleave : finished : cancelled +<br/>Binding (required): Current state of the encounter [EncounterStatus](http://hl7.org/fhir/stu3/valueset-encounter-status.html) |
|  - - period | 1..1 | Not Used | Period | The time that the episode was in the specified status<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | dateTime | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | dateTime | End time with inclusive boundary, if not ongoing |
|  - class | 0..1 | Not Used | Coding | Classification of the encounter<br/>Binding (extensible): Classification of the encounter [ActEncounterCode](http://hl7.org/fhir/stu3/v3/ActEncounterCode/vs.html) |
|  - - system | 0..1 | Not Used | Uri | Identity of the terminology system |
|  - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - code | 0..1 | Not Used | Code | Symbol in syntax defined by the system |
|  - - display | 0..1 | Not Used | String | Representation defined by the system |
|  - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - classHistory | 0..* | Not Used | BackboneElement | List of past encounter classes |
|  - - modifierExtension | 0..* | Not Used | Extension | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - class | 1..1 | Not Used | Coding | Classification of the encounter<br/>Binding (extensible): Classification of the encounter [ActEncounterCode](http://hl7.org/fhir/stu3/v3/ActEncounterCode/vs.html) |
|  - - - system | 0..1 | Not Used | Uri | Identity of the terminology system |
|  - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - code | 0..1 | Not Used | Code | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Not Used | String | Representation defined by the system |
|  - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - period | 1..1 | Not Used | Period | The time that the episode was in the specified class<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | dateTime | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | dateTime | End time with inclusive boundary, if not ongoing |
|  - type | 0..* | Not Used | CodeableConcept | Specific type of encounter<br/>Binding (example): The type of encounter [EncounterType](http://hl7.org/fhir/stu3/valueset-encounter-type.html)<br/> |
|  - - coding | 0..1 | Not Used | Coding | Code defined by a terminology system<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..* | Not Used | Coding | Code defined by a terminology system<br/>Binding (extensible): A code from the SNOMED Clinical Terminology UK coding system that describes an encounter between a care professional and the patient (or patient's record). [CareConnect-EncounterType-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-EncounterType-1) |
|  - - - extension (snomedCTDescriptionID) | 0..1 | Not Used | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | The SNOMED CT Description ID for the display<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - system | 1..1 | Not Used | Uri | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - code | 1..1 | Not Used | Code | Symbol in syntax defined by the system |
|  - - - display | 1..1 | Not Used | String | Representation defined by the system |
|  - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - text | 0..1 | Not Used | String | Plain text representation of the concept |
|  - priority | 0..1 | Not Used | CodeableConcept | Indicates the urgency of the encounter<br/>Binding (example): Indicates the urgency of the encounter. [v3 Code System ActPriority](http://hl7.org/fhir/stu3/v3/ActPriority/vs.html) |
|  - - coding | 0..* | Not Used | Coding | Code defined by a terminology system |
|  - - - system | 0..1 | Not Used | Uri | Identity of the terminology system |
|  - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - code | 0..1 | Not Used | Code | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Not Used | String | Representation defined by the system |
|  - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - text | 0..1 | Not Used | String | Plain text representation of the concept |
|  - subject | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | The patient ro group present at the encounter<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [Group](http://hl7.org/fhir/STU3/group.html "Group") |  |
|   |  | Not Used | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|  - - reference | 0..1 | Not Used | String | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - episodeOfCare | 0..* | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Episode(s) of care that this encounter should be recorded against<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [EpisodeOfCare](http://hl7.org/fhir/stu3/StructureDefinition/EpisodeOfCare "EpisodeOfCare") |  |
|  - - reference | 0..1 | Not Used | String | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - incomingReferral | 0..* | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | The ReferralRequest that initiated this encounter<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [ReferralRequest](http://hl7.org/fhir/stu3/StructureDefinition/ReferralRequest "ReferralRequest") |  |
|  - - reference | 0..1 | Not Used | String | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - participant | 0..* | Required | BackboneElement | List of participants involved in the encounter |
|  - - modifierExtension | 0..* | Not Used | Extension | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - type | 0..2 | Required | CodeableConcept | Role of participant in encounter<br/>Binding (extensible): Role of participant in encounter [ParticipantType](http://hl7.org/fhir/stu3/valueset-encounter-participant-type.html)<br/><font color='red'>There will be up to two instances of this element, the first carries a reference to the responsible clinical using the Practitioner resource and the second a reference to the person accompanying the patient using the relatedPerson resource</font> |
|  - - - coding | 1..1 | Mandatory | Coding | Code defined by a terminology system<br/><font color='red'>There will be one instance of the coding for each instance of type</font> |
|  - - - - system | 1..1 | Mandatory | Uri | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://hl7.org/fhir/ValueSet/encounter-participant-type'</font> |
|  - - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - - code | 1..1 | Mandatory | Code | Symbol in syntax defined by the system<br/><font color='red'>The Responsible Clinician will use a code of 'CON'</font><br/><font color='red'>The Person accompanying patient will use a code of 'ESC'</font>  |
|  - - - - display | 1..1 | Mandatory | String | <font color='red'>The Responsible Clinician will use a display of 'consultant'</font><br/><font color='red'>The Person accompanying patient will use a code of 'escort'</font>  |
|  - - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | String | Plain text representation of the concept |
|  - - period | 0..1 | Not Used | Period | Period of time during the encounter that the participant participated<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | dateTime | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | dateTime | End time with inclusive boundary, if not ongoing |
|  - - individual | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Persons involved in the encounter other than the patient<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This MUST be a reference to either the Practitioner or RelatedPerson resource</font> |
|   |  | Required | [RelatedPerson](http://hl7.org/fhir/stu3/StructureDefinition/RelatedPerson "RelatedPerson") | <font color='red'>The person accompanying the patient.<br/>This MUST use the RelatedPerson resource. </font>See [RelatedPerson resource](explore_admission_details.html#mapping-for-admission-details-relatedperson) for information on how to populate the resource. |
|   |  | Required | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") | <font color='red'>The responsible clinician for the encounter.<br/>This MUST use the CareConnect Practitioner profile. </font>See [Practitioner resource](explore_admission_details.html#mapping-for-admission-details-encounter) for information on how to populate the resource. |
|  - - - reference | 1..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the RelatedPerson resource or the Practitioner resource included in the Admission details list</font>  |
|  - - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - appointment | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | The appointment that scheduled this encounter<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [Appointment](http://hl7.org/fhir/stu3/StructureDefinition/Appointment "Appointment") |  |
|  - - reference | 0..1 | Not Used | String | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - period | 0..1 | Required | Period | The start and end time of the encounter<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - start | 0..1 | Required | dateTime | Starting time with inclusive boundary<br/><font color='red'>The date and time of admission</font><br/><font color='red'><b>Mapping to Maternity data item = 'Date and Time of admission'.</b></font> |
|  - - end | 0..1 | Not Used | dateTime | End time with inclusive boundary, if not ongoing |
|  - length | 0..1 | Not Used | Duration | Quantity of time the encounter lasted (less time absent)<br/>Constraint (qty-3): If a code for the unit is present, the system SHALL also be present<br/>Constraint (drt-1): There SHALL be a code if there is a value and it SHALL be an expression of time. If system is present, it SHALL be UCUM. |
|  - - value | 0..1 | Not Used | Decimal | Numerical value (with implicit precision) |
|  - - comparator | 0..1 | Not Used | Code | < : <= : >= : > - how to understand the value<br/>Binding (required): How the Quantity should be understood and represented. [QuantityComparator](http://hl7.org/fhir/stu3/valueset-quantity-comparator.html) |
|  - - unit | 0..1 | Not Used | String | Unit representation |
|  - - system | 0..1 | Not Used | Uri | System that defines coded unit form |
|  - - code | 0..1 | Not Used | Code | Coded form of the unit |
|  - reason | 0..1 | Required | CodeableConcept | Reason the encounter takes place (code)<br/>Binding (preferred): Reason why the encounter takes place. [Encounter Reason Codes](http://hl7.org/fhir/stu3/valueset-encounter-reason.html)<br/><font color='red'>The Admission details encounter does not use the preferred value set but uses SNOMED CT concepts instead</font> |
|  - - coding | 0..* | Not Used | Coding | Code defined by a terminology system<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 0..1 | Required | Coding | Code defined by a terminology system<br/><font color='red'>A concept from the Care planning health issues simple reference set</font><br/>[See here for further information](https://termbrowser.nhs.uk/?perspective=full&conceptId1=999000131000000105&edition=uk-edition&server=https://termbrowser.dataproducts.nhs.uk/sct-browser-api/snomed&langRefset=999001261000000100,999000691000001104)<br/><font color='red'>Note this reference set MAY be extnded as required by the sending system</font> |
|  - - - extension (snomedCTDescriptionID) | 0..1 | Not Used | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | The SNOMED CT Description ID for the display<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - system | 1..1 | Required | Uri | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - code | 1..1 | Required | Code | Symbol in syntax defined by the system<br/><font color='red'>A SNOMED CT from the Care planning health issues simple reference set as defined above</font>  |
|  - - - display | 1..1 | Required | String | Representation defined by the system<br/><font color='red'>The display associated with the SNOMED CT concept. This SHOULD be the preferred term</font> |
|  - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - text | 0..1 | Required | String | Plain text representation of the concept<br/><font color='red'>This MAY be used where a suitable coded concept is not available to the sending system</font> |
|  - diagnosis | 0..* | Not Used | BackboneElement | The list of diagnosis relevant to this encounter |
|  - - modifierExtension | 0..* | Not Used | Extension | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - condition | 1..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Reason the encounter takes place (resource)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Procedure-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Procedure-1 "CareConnect-Procedure-1") |  |
|   |  | Not Used | [CareConnect-Condition-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Condition-1 "CareConnect-Condition-1") |  |
|  - - - reference | 0..1 | Not Used | String | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - - role | 0..1 | Not Used | CodeableConcept | Role that this diagnosis has within the encounter (e.g. admission, billing, discharge …)<br/>Binding (preferred): The type of diagnosis this condition represents [DiagnosisRole](http://hl7.org/fhir/stu3/valueset-diagnosis-role.html) |
|  - - - coding | 0..* | Not Used | Coding | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | Uri | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | Code | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | String | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | String | Plain text representation of the concept |
|  - - rank | 0..1 | Not Used | positiveInt | Ranking of the diagnosis (for each role type) |
|  - account | 0..* | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | The set of accounts that may be used for billing for this Encounter<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [Account](http://hl7.org/fhir/stu3/StructureDefinition/Account "Account") |  |
|  - - reference | 0..1 | Not Used | String | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - hospitalization | 0..1 | Required | BackboneElement | Details about the admission to a healthcare service |
|  - - extension (admissionMethod) | 0..1 | Required | [Extension-CareConnect-AdmissionMethod-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-AdmissionMethod-1 "Extension-CareConnect-AdmissionMethod-1") | An extension to the Encounter resource to record how a Patient was admitted to hospital.<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/><font color='red'>An extension to the Encounter  resource</font><br/>See [Admission method extension](explore_admission_details.html#mapping-for-admission-details-admission-method-extension) for information on how to populate this extension to the resource.<br/><font color='red'><b>Mapping to Maternity data item = 'Reason for Admission'.</b></font>  |
|  - - extension (dischargeMethod) | 0..1 | Not Used | [Extension-CareConnect-DischargeMethod-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-DischargeMethod-1 "Extension-CareConnect-DischargeMethod-1") | An extension to the Encounter resource to record the method of discharge from hospital.<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - modifierExtension | 0..* | Not Used | Extension | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - preAdmissionIdentifier | 0..1 | Not Used | Identifier | Pre-admission identifier |
|  - - - use | 0..1 | Not Used | Code | usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known . [IdentifierUse](http://hl7.org/fhir/stu3/valueset-identifier-use.html) |
|  - - - type | 0..1 | Not Used | CodeableConcept | Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [Identifier Type Codes](http://hl7.org/fhir/stu3/valueset-identifier-type.html) |
|  - - - - coding | 0..* | Not Used | Coding | Code defined by a terminology system |
|  - - - - - system | 0..1 | Not Used | Uri | Identity of the terminology system |
|  - - - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - - - code | 0..1 | Not Used | Code | Symbol in syntax defined by the system |
|  - - - - - display | 0..1 | Not Used | String | Representation defined by the system |
|  - - - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - - - text | 0..1 | Not Used | String | Plain text representation of the concept |
|  - - - system | 1..1 | Not Used | Uri | The namespace for the identifier value |
|  - - - value | 1..1 | Not Used | String | The value that is unique |
|  - - - period | 0..1 | Not Used | Period | Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - - start | 0..1 | Not Used | dateTime | Starting time with inclusive boundary |
|  - - - - end | 0..1 | Not Used | dateTime | End time with inclusive boundary, if not ongoing |
|  - - - assigner | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - - - reference | 0..1 | Not Used | String | Literal reference, Relative, internal or absolute URL |
|  - - - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - - origin | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | The location from which the patient came before admission<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") |  |
|  - - - reference | 0..1 | Not Used | String | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - - admitSource | 0..1 | Required | CodeableConcept | From where patient was admitted (physician referral, transfer)<br/>Binding (preferred): The source of admission to a Hospital Provider Spell or a Nursing Episode when the Patient is in a Hospital Site or a Care Home. [CareConnect-SourceOfAdmission-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-SourceOfAdmission-1)<br/><font color='red'><b>Maternity Data set mapping = 'Source of Admission'</b></font> |
|  - - - coding | 0..1 | Required | Coding | Code defined by a terminology system |
|  - - - - system | 1..1 | Mandatory | Uri | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - - code | 1..1 | Mandatory | Code | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value 'https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-SourceOfAdmission-1'</font> |
|  - - - - display | 1..1 | Mandatory | String | Representation defined by the system<br/><font color='red'>This MUST contain a code from the stated ValueSet</font>  |
|  - - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | String | Plain text representation of the concept<br/> |
|  - - reAdmission | 0..1 | Not Used | CodeableConcept | The type of hospital re-admission that has occurred (if any). If the value is absent, then this is not identified as a readmission<br/>Binding (example): The reason for re-admission of this hospitalization encounter. [v2 Re-Admission Indicator](http://hl7.org/fhir/ValueSet/v2-0092) |
|  - - - coding | 0..* | Not Used | Coding | Code defined by a terminology system<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open |
|  - - - coding (snomedCT) | 0..1 | Not Used | Coding | Code defined by a terminology system |
|  - - - - extension (snomedCTDescriptionID) | 0..1 | Not Used | [Extension-coding-sctdescid](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-coding-sctdescid "Extension-coding-sctdescid") | The SNOMED CT Description ID for the display<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/> |
|  - - - - system | 1..1 | Not Used | Uri | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - - code | 1..1 | Not Used | Code | Symbol in syntax defined by the system |
|  - - - - display | 1..1 | Not Used | String | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | String | Plain text representation of the concept |
|  - - dietPreference | 0..* | Not Used | CodeableConcept | Diet preferences reported by the patient<br/>Binding (extensible): Medical, cultural or ethical food preferences to help with catering requirements. [Diet](http://hl7.org/fhir/stu3/valueset-encounter-diet.html) |
|  - - - coding | 0..* | Not Used | Coding | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | Uri | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | Code | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | String | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | String | Plain text representation of the concept |
|  - - specialCourtesy | 0..* | Not Used | CodeableConcept | Special courtesies (VIP, board member)<br/>Binding (preferred): Special courtesies [SpecialCourtesy](http://hl7.org/fhir/stu3/valueset-encounter-special-courtesy.html) |
|  - - - coding | 0..* | Not Used | Coding | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | Uri | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | Code | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | String | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | String | Plain text representation of the concept |
|  - - specialArrangement | 0..* | Not Used | CodeableConcept | Wheelchair, translator, stretcher, etc.<br/>Binding (preferred): Special arrangements [SpecialArrangements](http://hl7.org/fhir/stu3/valueset-encounter-special-arrangements.html) |
|  - - - coding | 0..* | Not Used | Coding | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | Uri | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | Code | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | String | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | String | Plain text representation of the concept |
|  - - destination | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Location to which the patient is discharged<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") |  |
|  - - - reference | 0..1 | Not Used | String | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - - dischargeDisposition | 0..1 | Not Used | CodeableConcept | Category or kind of location after discharge<br/>Binding (example): The destination of a Patient on completion of a Hospital Provider Spell, or a note that the Patient died or was a still birth. [CareConnect-DischargeDestination-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-DischargeDestination-1) |
|  - - - coding | 0..* | Not Used | Coding | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | Uri | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | Code | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | String | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | String | Plain text representation of the concept |
|  - location | 0..1 | Required | BackboneElement | List of locations where the patient has been |
|  - - modifierExtension | 0..* | Not Used | Extension | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - location | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Location the encounter takes place<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>The site code of the unit to which the person was admitted</font> |
|   |  | Mandatory | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") | "<font color='red'>The location<br/>This MUST use the CareConnect Location profile. </font>See [Location resource](explore_admission_details.html#mapping-for-admission-details-location) for information on how to populate the resource." |
|  - - - reference | 1..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the Location resource included in the Admission details list</font>  |
|  - - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - - status | 0..1 | Not Used | Code | planned : active : reserved : completed<br/>Binding (required): The status of the location. [EncounterLocationStatus](http://hl7.org/fhir/stu3/valueset-encounter-location-status.html) |
|  - - period | 0..1 | Not Used | Period | Time period during which the patient was present at the location<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | dateTime | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | dateTime | End time with inclusive boundary, if not ongoing |
|  - serviceProvider | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | The custodian organization of this Encounter record<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - reference | 0..1 | Not Used | String | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - partOf | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Another Encounter this encounter is part of<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1 "CareConnect-Encounter-1") |  |
|  - - reference | 0..1 | Not Used | String | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | String | Text alternative for the resource |

## Mapping for Admission Details RelatedPerson ##

|>|Level 1|[RelatedPerson Resource](http://hl7.org/fhir/stu3/relatedPerson.html)|>|Level 2|None|>|Level 3|None|


|**[View Used FHIR Elements](explore_admission_details.html#mapping-for-admission-details-relatedperson)**|**[View All FHIR Elements]**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| --- | --- | --- | --- | --- |
|  RelatedPerson | ​ |  |  | An person that is related to a patient, but who is not a direct target of care<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | Meta | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-RelatedPerson-1'</font> |
|  - implicitRules | 0..1 | Not Used | Uri | A set of rules under which this content was created |
|  - language | 0..1 | Not Used | Code | Language of the resource content<br/>Binding (extensible): A human language. [Common Languages](http://hl7.org/fhir/stu3/valueset-languages.html) |
|  - text | 0..1 | Not Used | Narrative | Text summary of the resource, for human interpretation |
|  - contained | 0..* | Not Used | Resource | Contained, inline Resources |
|  - modifierExtension | 0..* | Not Used | Extension | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>Slicing: Description: Extensions are always sliced by (at least) url, Discriminator: url, Ordering: false, Rules: Open |
|  - identifier | 0..* | Not Used | Identifier | A human identifier for this person |
|  - - use | 0..1 | Not Used | Code | usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known. [IdentifierUse](http://hl7.org/fhir/stu3/valueset-identifier-use.html) |
|  - - type | 0..1 | Not Used | CodeableConcept | Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [Identifier Type Codes](http://hl7.org/fhir/stu3/valueset-identifier-type.html) |
|  - - - coding | 0..* | Not Used | Coding | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | Uri | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | Code | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | String | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | String | Plain text representation of the concept |
|  - - system | 0..1 | Not Used | Uri | The namespace for the identifier value |
|  - - value | 0..1 | Not Used | String | The value that is unique |
|  - - period | 0..1 | Not Used | Period | Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | dateTime | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | dateTime | End time with inclusive boundary, if not ongoing |
|  - - assigner | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - - reference | 0..1 | Not Used | String | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - active | 0..1 | Not Used | Boolean | Whether this related person's record is in active use<br/>Default Value: true |
|  - patient | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | The patient this person is related to<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - relationship | 0..1 | Optional | CodeableConcept | The nature of the relationship<br/>Binding (preferred): The nature of the relationship between a patient and the related person [PatientRelationshipType](http://hl7.org/fhir/stu3/valueset-relatedperson-relationshiptype.html) |
|  - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system |
|  - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system<br/><font color='red'>This SHOULD contain the value 'http://hl7.org/fhir/stu3/valueset-relatedperson-relationshiptype' if the preferred codeSystem is used.</font>  |
|  - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system<br/><font color='red'>This SHOULD contain a value from the preferred codeSystem</font> |
|  - - - display | 0..1 | Mandatory | String | Representation defined by the system<br/><font color='red'>This MUST contain the display associated with the code.</font> |
|  - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - text | 0..1 | Not Used | String | Plain text representation of the concept |
|  - name | 0..* | Required | HumanName | A name associated with the person<br/><font color='red'>Maximum 150 Characters a structured name may be sent if available.</font> |
|  - - use | 0..1 | Not Used | Code | usual : official : temp : nickname : anonymous : old : maiden<br/>Binding (required): The use of a human name [NameUse](http://hl7.org/fhir/stu3/valueset-name-use.html) |
|  - - text | 0..1 | Required | String | Text representation of the full name<br/><font color='red'><b>Mapping to Maternity Data item = 'Person accompanying patient'</b></font> |
|  - - family | 0..1 | Optional | String | Family name (often called 'Surname') |
|  - - given | 0..* | Optional | String | Given names (not always 'first'). Includes middle names |
|  - - prefix | 0..* | Optional | String | Parts that come before the name |
|  - - suffix | 0..* | Optional | String | Parts that come after the name |
|  - - period | 0..1 | Not Used | Period | Time period when name was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | dateTime | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | dateTime | End time with inclusive boundary, if not ongoing |
|  - telecom | 0..* | Not Used | ContactPoint | A contact detail for the person<br/>Constraint (cpt-2): A system is required if a value is provided. |
|  - - system | 0..1 | Not Used | Code | phone : fax : email : pager : url : sms : other<br/>Binding (required): Telecommunications form for contact point [ContactPointSystem](http://hl7.org/fhir/stu3/valueset-contact-point-system.html) |
|  - - value | 0..1 | Not Used | String | The actual contact point details |
|  - - use | 0..1 | Not Used | Code | home : work : temp : old : mobile - purpose of this contact point<br/>Binding (required): Use of contact point [ContactPointUse](http://hl7.org/fhir/stu3/valueset-contact-point-use.html) |
|  - - rank | 0..1 | Not Used | positiveInt | Specify preferred order of use (1 = highest) |
|  - - period | 0..1 | Not Used | Period | Time period when the contact point was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | dateTime | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | dateTime | End time with inclusive boundary, if not ongoing |
|  - gender | 0..1 | Not Used | Code | male : female : other : unknown<br/>Binding (required): The gender of a person used for administrative purposes. [AdministrativeGender](http://hl7.org/fhir/stu3/valueset-administrative-gender.html) |
|  - birthDate | 0..1 | Not Used | Date | The date on which the related person was born |
|  - address | 0..* | Not Used | Address | Address where the related person can be contacted or visited |
|  - - use | 0..1 | Not Used | Code | home : work : temp : old - purpose of this address<br/>Binding (required): The use of an address [AddressUse](http://hl7.org/fhir/stu3/valueset-address-use.html) |
|  - - type | 0..1 | Not Used | Code | postal : physical : both<br/>Binding (required): The type of an address (physical / postal) [AddressType](http://hl7.org/fhir/stu3/valueset-address-type.html) |
|  - - text | 0..1 | Not Used | String | Text representation of the address |
|  - - line | 0..* | Not Used | String | Street name, number, direction & P.O. Box etc. |
|  - - city | 0..1 | Not Used | String | Name of city, town etc. |
|  - - district | 0..1 | Not Used | String | District name (aka county) |
|  - - state | 0..1 | Not Used | String | Sub-unit of country (abbreviations ok) |
|  - - postalCode | 0..1 | Not Used | String | Postal code for area |
|  - - country | 0..1 | Not Used | String | Country (e.g. can be ISO 3166 2 or 3 letter code) |
|  - - period | 0..1 | Not Used | Period | Time period when address was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | dateTime | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | dateTime | End time with inclusive boundary, if not ongoing |
|  - photo | 0..* | Not Used | Attachment | Image of the person<br/>Constraint (att-1): It the Attachment has data, it SHALL have a contentType |
|  - - contentType | 0..1 | Not Used | Code | Mime type of the content, with charset etc.<br/>Binding (required): The mime type of an attachment. Any valid mime type is allowed. [Mime Type]( http://www.rfc-editor.org/bcp/bcp13.txt ) |
|  - - language | 0..1 | Not Used | Code | Human language of the content (BCP-47)<br/>Binding (extensible): A human language. ( http://hl7.org/fhir/stu3/valueset-languages.html ) |
|  - - data | 0..1 | Not Used | base64Binary | Data inline, base64ed |
|  - - url | 0..1 | Not Used | Uri | Uri where the data can be found |
|  - - size | 0..1 | Not Used | unsignedInt | Number of bytes of content (if url provided) |
|  - - hash | 0..1 | Not Used | base64Binary | Hash of the data (sha-1, base64ed) |
|  - - title | 0..1 | Not Used | String | Label to display in place of the data |
|  - - creation | 0..1 | Not Used | dateTime | Date attachment was first created |
|  - period | 0..1 | Not Used | Period | Period of time that this relationship is considered valid<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - start | 0..1 | Not Used | dateTime | Starting time with inclusive boundary |
|  - - end | 0..1 | Not Used | dateTime | End time with inclusive boundary, if not ongoing |


## Mapping for Admission Details Practitioner ##

|>|Level 1|[Practitioner Resource](http://hl7.org/fhir/stu3/practitioner.html)|>|Level 2|[CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)|>|Level 3|None|


|**[View Used FHIR Elements](explore_admission_details.html#mapping-for-admission-details-practitioner)**|**[View All FHIR Elements]**|


|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  Practitioner | ​ |  |  | A person with a formal responsibility in the provisioning of healthcare or related services<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/><font color='red'>The name and designation of the consultant, who has overall responsibility for the person (may not actually see the person)</font> |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | Meta | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Practitioner-1'</font> |
|  - implicitRules | 0..1 | Not Used | Uri | **A set of rules under which this content was created** |
|  - language | 0..1 | Not Used | Code | **Language of the resource content<br/>Binding (extensible): A human language. [Common Languages](http://hl7.org/fhir/stu3/valueset-languages.html)** |
|  - text | 0..1 | Not Used | Narrative | **Text summary of the resource, for human interpretation** |
|  - contained | 0..* | Not Used | Resource | **Contained, inline Resources** |
|  - extension (nhsCommunication) | 0..* | Not Used | [Extension-CareConnect-NHSCommunication-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-NHSCommunication-1 "Extension-CareConnect-NHSCommunication-1") | **NHS communication preferences for a resource<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>** |
|  - modifierExtension | 0..* | Not Used | Extension | **Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>Slicing: Description: Extensions are always sliced by (at least) url, Discriminator: url, Ordering: false, Rules: Open** |
|  - identifier | 0..* | Mandatory | Identifier | A identifier for the person as this agent<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open at End |
|  - identifier (sdsUserID) | 0..1 | Mandatory | Identifier | A identifier for the person as this agent<br/><font color='red'>This will be the clinicians SDS identifier (GMC code)</font><br/><font color='red'><b>Mapping to Maternity Data set = 'Responsible Clinician Identifier'.</b></font> |
|  - - use | 0..1 | Not Used | Code | usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known. [IdentifierUse](http://hl7.org/fhir/stu3/valueset-identifier-use.html)<br/><font color='red'>This MUST contain the value 'offical'.</font> |
|  - - type | 0..1 | Not Used | CodeableConcept | Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [Identifier Type Codes](http://hl7.org/fhir/stu3/valueset-identifier-type.html) |
|  - - system | 1..1 | Mandatory | Uri | The namespace for the identifier value<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/Id/sds-user-id'</font><br/><font color='red'><b>Maternity data set mapping = ' |
|  - - value | 1..1 | Mandatory | String | The value that is unique<br/><font color='red'>This MUST contain the person's SDS user id</font> |
|  - - period | 0..1 | Not Used | Period | **Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end** |
|  - - assigner | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | **Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided** |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") | **** |
|  - identifier (sdsRoleProfileID) | 0..* | Not Used | Identifier | **A identifier for the person as this agent** |
|  - - use | 0..1 | Not Used | Code | **usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known. [IdentifierUse](http://hl7.org/fhir/stu3/valueset-identifier-use.html)** |
|  - - type | 0..1 | Not Used | CodeableConcept | **Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [Identifier Type Codes](http://hl7.org/fhir/stu3/valueset-identifier-type.html)** |
|  - - system | 1..1 | Not Used | Uri | **The namespace for the identifier value<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/Id/sds-role-profile-id'</font>** |
|  - - value | 1..1 | Not Used | String | **The value that is unique** |
|  - - period | 0..1 | Not Used | Period | **Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end** |
|  - - assigner | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | **Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided** |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") | **** |
|  - active | 0..1 | Not Used | Boolean | **Whether this practitioner's record is in active use<br/>Default Value: true** |
|  - name | 0..* | Required | HumanName | The name(s) associated with the practitioner |
|  - - use | 0..1 | Not Used | Code | **usual : official : temp : nickname : anonymous : old : maiden<br/>Binding (required): The use of a human name [NameUse](http://hl7.org/fhir/stu3/valueset-name-use.html)** |
|  - - text | 0..1 | Required | String | Text representation of the full name<br/><font color='red'><b>Mapping to Maternity Data set = 'Responsible Clinician Name'.</b></font> |
|  - - family | 0..1 | Optional | String | Family name (often called 'Surname') |
|  - - given | 0..* | Optional | String | Given names (not always 'first'). Includes middle names |
|  - - prefix | 0..* | Optional | String | Parts that come before the name |
|  - - suffix | 0..* | Optional | String | Parts that come after the name |
|  - - period | 0..1 | Not Used | Period | **Time period when name was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end** |
|  - - - start | 0..1 | Not Used | dateTime | **Starting time with inclusive boundary** |
|  - - - end | 0..1 | Not Used | dateTime | **End time with inclusive boundary, if not ongoing** |
|  - telecom | 0..* | Not Used | ContactPoint | **A contact detail for the practitioner (that apply to all roles)<br/>Constraint (cpt-2): A system is required if a value is provided.** |
|  - - system | 0..1 | Not Used | Code | **phone : fax : email : pager : url : sms : other<br/>Binding (required): Telecommunications form for contact point [ContactPointSystem](http://hl7.org/fhir/stu3/valueset-contact-point-system.html)** |
|  - - value | 0..1 | Not Used | String | **The actual contact point details** |
|  - - use | 0..1 | Not Used | Code | **home : work : temp : old : mobile - purpose of this contact point<br/>Binding (required): Use of contact point [ContactPointUse](http://hl7.org/fhir/stu3/valueset-contact-point-use.html)** |
|  - - rank | 0..1 | Not Used | positiveInt | **Specify preferred order of use (1 = highest)** |
|  - - period | 0..1 | Not Used | Period | **Time period when the contact point was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end** |
|  - - - start | 0..1 | Not Used | dateTime | **Starting time with inclusive boundary** |
|  - - - end | 0..1 | Not Used | dateTime | **End time with inclusive boundary, if not ongoing** |
|  - address | 0..* | Not Used | Address | **Address(es) of the practitioner that are not role specific (typically home address)** |
|  - - use | 0..1 | Not Used | Code | **home : work : temp : old - purpose of this address<br/>Binding (required): The use of an address [AddressUse](http://hl7.org/fhir/stu3/valueset-address-use.html)** |
|  - - type | 0..1 | Not Used | Code | **postal : physical : both<br/>Binding (required): The type of an address (physical / postal) [AddressType](http://hl7.org/fhir/stu3/valueset-address-type.html)** |
|  - - text | 0..1 | Not Used | String | **Text representation of the address** |
|  - - line | 0..* | Not Used | String | **Street name, number, direction & P.O. Box etc.** |
|  - - city | 0..1 | Not Used | String | **Name of city, town etc.** |
|  - - district | 0..1 | Not Used | String | **District name (aka county)** |
|  - - state | 0..1 | Not Used | String | **Sub-unit of country (abbreviations ok)** |
|  - - postalCode | 0..1 | Not Used | String | **Postal code for area** |
|  - - country | 0..1 | Not Used | String | **Country (e.g. can be ISO 3166 2 or 3 letter code)** |
|  - - period | 0..1 | Not Used | Period | **Time period when address was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end** |
|  - - - start | 0..1 | Not Used | dateTime | **Starting time with inclusive boundary** |
|  - - - end | 0..1 | Not Used | dateTime | **End time with inclusive boundary, if not ongoing** |
|  - gender | 0..1 | Not Used | Code | **male : female : other : unknown<br/>Binding (required): The gender of a person used for administrative purposes. [CareConnect-AdministrativeGender-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-AdministrativeGender-1)** |
|  - birthDate | 0..1 | Not Used | Date | **The date on which the practitioner was born** |
|  - photo | 0..* | Not Used | Attachment | **Image of the person<br/>Constraint (att-1): It the Attachment has data, it SHALL have a contentType** |
|  - - contentType | 0..1 | Not Used | Code | **Mime type of the content, with charset etc.<br/>Binding (required): The mime type of an attachment. Any valid mime type is allowed. [Mime Type](http://www.rfc-editor.org/bcp/bcp13.txt)** |
|  - - language | 0..1 | Not Used | Code | **Human language of the content (BCP-47)<br/>Binding (extensible): A human language. [Common Languages](http://hl7.org/fhir/stu3/valueset-languages.html)** |
|  - - data | 0..1 | Not Used | base64Binary | **Data inline, base64ed** |
|  - - url | 0..1 | Not Used | Uri | **Uri where the data can be found** |
|  - - size | 0..1 | Not Used | unsignedInt | **Number of bytes of content (if url provided)** |
|  - - hash | 0..1 | Not Used | base64Binary | **Hash of the data (sha-1, base64ed)** |
|  - - title | 0..1 | Not Used | String | **Label to display in place of the data** |
|  - - creation | 0..1 | Not Used | dateTime | **Date attachment was first created** |
|  - qualification | 0..* | Not Used | BackboneElement | **Qualifications obtained by training and certification** |
|  - - modifierExtension | 0..* | Not Used | Extension | **Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both** |
|  - - identifier | 0..* | Not Used | Identifier | **An identifier for this qualification for the practitioner** |
|  - - - use | 0..1 | Not Used | Code | **usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known. [IdentifierUse](http://hl7.org/fhir/stu3/valueset-identifier-use.html)** |
|  - - - type | 0..1 | Not Used | CodeableConcept | **Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [Identifier Type Codes](http://hl7.org/fhir/stu3/valueset-identifier-type.html)** |
|  - - - system | 0..1 | Not Used | Uri | **The namespace for the identifier value** |
|  - - - value | 0..1 | Not Used | String | **The value that is unique** |
|  - - - period | 0..1 | Not Used | Period | **Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end** |
|  - - - assigner | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | **Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided** |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") | **** |
|  - - code | 1..1 | Not Used | CodeableConcept | **Coded representation of the qualification<br/>Binding (example): Specific qualification the practitioner has to provide a service [v2 table 0360, Version 2.7](http://hl7.org/fhir/ValueSet/v2-2.7-0360)** |
|  - - - coding | 0..* | Not Used | Coding | **Code defined by a terminology system** |
|  - - - - system | 0..1 | Not Used | Uri | **Identity of the terminology system** |
|  - - - - version | 0..1 | Not Used | String | **Version of the system - if relevant** |
|  - - - - code | 0..1 | Not Used | Code | **Symbol in syntax defined by the system** |
|  - - - - display | 0..1 | Not Used | String | **Representation defined by the system** |
|  - - - - userSelected | 0..1 | Not Used | Boolean | **If this coding was chosen directly by the user** |
|  - - - text | 0..1 | Not Used | String | **Plain text representation of the concept** |
|  - - period | 0..1 | Not Used | Period | **Period during which the qualification is valid<br/>Constraint (per-1): If present, start SHALL have a lower value than end** |
|  - - - start | 0..1 | Not Used | dateTime | **Starting time with inclusive boundary** |
|  - - - end | 0..1 | Not Used | dateTime | **End time with inclusive boundary, if not ongoing** |
|  - - issuer | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | **Organization that regulates and issues the qualification<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided** |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") | **** |
|  - - - reference | 0..1 | Not Used | String | **Literal reference, Relative, internal or absolute URL** |
|  - - - identifier | 0..1 | Not Used | Identifier | **Logical reference, when literal reference is not known** |


## Mapping for Admission Details Location ##

|>|Level 1|[Location Resource](http://hl7.org/fhir/stu3/location.html)|>|Level 2|[CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)|>|Level 3|None|


|**[View Used FHIR Elements](explore_admission_details.html#mapping-for-admission-details-location)**|**[View All FHIR Elements]**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  Location | ​ |  |  | Details and position information for a physical place<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  - meta | 1..1 | Mandatory | Meta | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-Location-1'</font> |
|  - implicitRules | 0..1 | Not Used | Uri | **A set of rules under which this content was created** |
|  - language | 0..1 | Not Used | Code | **Language of the resource content<br/>Binding (extensible): A human language. [Common Languages](http://hl7.org/fhir/stu3/valueset-languages.html)** |
|  - text | 0..1 | Not Used | Narrative | **Text summary of the resource, for human interpretation** |
|  - contained | 0..* | Not Used | Resource | **Contained, inline Resources** |
|  - modifierExtension | 0..* | Not Used | Extension | **Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>Slicing: Description: Extensions are always sliced by (at least) url, Discriminator: url, Ordering: false, Rules: Open** |
|  - identifier | 0..* | Not Used | Identifier | Unique code or number identifying the location to its users<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open at End |
|  - identifier (odsSiteCode) | 0..1 | Required | Identifier | ODS Site code to identify the organisation at site level<br/><font color='red'>Site code of the unit to which the person was admitted</font> <br/><font color='red'><b>Maternity Data set mapping = 'ODS/ORD Site Code'</b></font> |
|  - - use | 0..1 | Not Used | Code | usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known. [IdentifierUse](http://hl7.org/fhir/stu3/valueset-identifier-use.html) |
|  - - type | 0..1 | Not Used | CodeableConcept | Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [Identifier Type Codes](http://hl7.org/fhir/stu3/valueset-identifier-type.html) |
|  - - system | 1..1 | Required | Uri | ODS Code<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/Id/ods-site-code'</font> |
|  - - value | 1..1 | Required | String | The ODS Site code name, to reflect the code used |
|  - - period | 0..1 | Not Used | Period | Time period when id is/was valid for use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - assigner | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - status | 0..1 | Not Used | Code | active : suspended : inactive<br/>Binding (required): Indicates whether the location is still in use. [LocationStatus](http://hl7.org/fhir/stu3/valueset-location-status.html) |
|  - operationalStatus | 0..1 | Not Used | Coding | The Operational status of the location (typically only for a bed/room)<br/>Binding (preferred): The operational status if the location (where typically a bed/room) [v2 Bed Status](http://hl7.org/fhir/ValueSet/v2-0116) |
|  - - system | 0..1 | Not Used | Uri | Identity of the terminology system |
|  - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - code | 0..1 | Not Used | Code | Symbol in syntax defined by the system |
|  - - display | 0..1 | Not Used | String | Representation defined by the system |
|  - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - name | 0..1 | Not Used | String | Name of the location as used by humans |
|  - alias | 0..* | Not Used | String | A list of alternate names that the location is known as, or was known as in the past |
|  - description | 0..1 | Not Used | String | Additional details about the location that could be displayed as further information to identify the location beyond its name<br/><font color='red'>This is the physical location of the person. E.g hospital ward, bed, theatre. For ambulatory care, eg, health centre, clinic, resource centre, person’s home maximum 150 characters</font><br/><font color='red'><b>Maternity Date set mapping = 'Patient Location'</b></font> |
|  - mode | 0..1 | Not Used | Code | instance : kind<br/>Binding (required): Indicates whether a resource instance represents a specific location or a class of locations. [LocationMode](http://hl7.org/fhir/stu3/valueset-location-mode.html) |
|  - type | 0..1 | Required | CodeableConcept | Type of function performed<br/>Binding (extensible): Indicates the type of function performed at the location. [ServiceDeliveryLocationRoleType](http://hl7.org/fhir/stu3/v3/ServiceDeliveryLocationRoleType/vs.html )<br/><font color='red'><b>Maternity Date set mapping = 'Specialty admitted to'</b></font><br/><font color='red'>Note this valueset is defined as extensible and therefore if the code exists in this valueSet then that code MUST be used.</font> <br/> <font color='red'>Alternatively if the code does not exist in this valueSet then a code from the</font> [Activity Treatment Function Code](https://www.datadictionary.nhs.uk/data_dictionary/data_field_notes/a/act/activity_treatment_function_code_de.asp?shownav=1?query=%22ACTIVITY+TREATMENT+FUNCTION+CODE%22&rank=100&shownav=1) <font color='red'>valueSet MUST be used</font><br/>  |
|  - - coding | 0..* | Required | Coding | Code defined by a terminology system |
|  - - - system | 0..1 | Required | Uri | Identity of the terminology system<br/><font color='red'>MUST contain the value 'http://hl7.org/fhir/stu3/v3/ServiceDeliveryLocationRoleType'</font> |
|  - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - code | 0..1 | Required | Code | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the code which describes the speciality of the location.</font> |
|  - - - display | 0..1 | Required | String | Representation defined by the system<br/><font color='red'>This MUST contain the display associated with the code</font> |
|  - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - text | 1..1 | Not Used | String | Plain text representation of the concept<br/> |
|  - telecom | 0..* | Not Used | ContactPoint | Contact details of the location<br/>Constraint (cpt-2): A system is required if a value is provided. |
|  - - system | 0..1 | Not Used | Code | phone : fax : email : pager : url : sms : other<br/>Binding (required): Telecommunications form for contact point [ContactPointSystem](http://hl7.org/fhir/stu3/valueset-contact-point-system.html) |
|  - - value | 0..1 | Not Used | String | The actual contact point details |
|  - - use | 0..1 | Not Used | Code | home : work : temp : old : mobile - purpose of this contact point<br/>Binding (required): Use of contact point [ContactPointUse](http://hl7.org/fhir/stu3/valueset-contact-point-use.html) |
|  - - rank | 0..1 | Not Used | positiveInt | Specify preferred order of use (1 = highest) |
|  - - period | 0..1 | Not Used | Period | Time period when the contact point was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | dateTime | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | dateTime | End time with inclusive boundary, if not ongoing |
|  - address | 0..1 | Not Used | Address | Physical location |
|  - - use | 0..1 | Not Used | Code | home : work : temp : old - purpose of this address<br/>Binding (required): The use of an address [AddressUse](http://hl7.org/fhir/stu3/valueset-address-use.html) |
|  - - type | 0..1 | Not Used | Code | postal : physical : both<br/>Binding (required): The type of an address (physical / postal) [AddressType](http://hl7.org/fhir/stu3/valueset-address-type.html) |
|  - - text | 0..1 | Not Used | String | Text representation of the address |
|  - - line | 0..* | Not Used | String | Street name, number, direction & P.O. Box etc. |
|  - - city | 0..1 | Not Used | String | Name of city, town etc. |
|  - - district | 0..1 | Not Used | String | District name (aka county) |
|  - - state | 0..1 | Not Used | String | Sub-unit of country (abbreviations ok) |
|  - - postalCode | 0..1 | Not Used | String | Postal code for area |
|  - - country | 0..1 | Not Used | String | Country (e.g. can be ISO 3166 2 or 3 letter code) |
|  - - period | 0..1 | Not Used | Period | Time period when address was/is in use<br/>Constraint (per-1): If present, start SHALL have a lower value than end |
|  - - - start | 0..1 | Not Used | dateTime | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | dateTime | End time with inclusive boundary, if not ongoing |
|  - physicalType | 0..1 | Required | CodeableConcept | Physical form of the location<br/>Binding (example): Physical form of the location [LocationType](http://hl7.org/fhir/stu3/valueset-location-physical-type.html) |
|  - - coding | 0..1 | Not Used | Coding | Code defined by a terminology system |
|  - - - system | 0..1 | Not Used | Uri | Identity of the terminology system |
|  - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - code | 0..1 | Not Used | Code | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Not Used | String | Representation defined by the system |
|  - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - text | 0..1 | Required | String | Plain text representation of the concept<br/><font color='red'>This is the physical location of the person. E.g hospital ward, bed, theatre. For ambulatory care, eg, health centre, clinic, resource centre, person’s home maximum 150 characters</font><br/><font color='red'><b>Maternity Date set mapping = 'Patient Location'</b></font> |
|  - position | 0..1 | Not Used | BackboneElement | The absolute geographic location |
|  - - modifierExtension | 0..* | Not Used | Extension | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - longitude | 1..1 | Not Used | Decimal | Longitude with WGS84 datum |
|  - - latitude | 1..1 | Not Used | Decimal | Latitude with WGS84 datum |
|  - - altitude | 0..1 | Not Used | Decimal | Altitude with WGS84 datum |
|  - managingOrganization | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization responsible for provisioning and upkeep<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - reference | 0..1 | Not Used | String | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - partOf | 0..1 | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Another Location this one is physically part of<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") |  |
|  - - reference | 0..1 | Not Used | String | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | String | Text alternative for the resource |
|  - endpoint | 0..* | Not Used | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Technical endpoints providing access to services operated for the location<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [Endpoint](http://hl7.org/fhir/stu3/StructureDefinition/Endpoint "Endpoint") |  |
|  - - reference | 0..1 | Not Used | String | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Not Used | String | Text alternative for the resource |


## Mapping for Admission Details Admission Method Extension ##

|>|Level 1|[Extension](http://hl7.org/fhir/STU3/extensibility.html#Extension)|>|Level 2|[Extension-CareConnect-AdmissionMethod-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-AdmissionMethod-1)|>|Level 3|None|


|**[View Used FHIR Elements](explore_admission_details.html#mapping-for-admission-details-location)**|**View All FHIR Elements**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | --- | :--- | :--- |
|  Extension | ​ |  |  | An extension to the Encounter resource to record how a Patient was admitted to hospital.<br/>Constraint (ele-1): All FHIR elements must have a @value or children<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - id | 0..1 | Optional | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | xml:id (or equivalent in JSON) |
|  - url | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identifies The Meaning Of The Extension Fixed Value = 'https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-AdmissionMethod-1' |
|  - valueCodeableConcept | 1..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | The method of admission to a Hospital Provider Spell.<br/>Binding (required): The method of admission to a Hospital Provider Spell. <br/>[Admission Method](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-AdmissionMethod-1 ) |

## Admission Details Heading Example ##

<script src="https://gist.github.com/IOPS-DEV/9d51ee5528e59b70da255468c3da5413.js"></script>