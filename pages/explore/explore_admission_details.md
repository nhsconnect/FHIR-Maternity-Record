---
title: Admission Details Bundle
keywords:  bundles
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_admission_details.html
summary: "The FHIR profiles used for the Admission Details Bundle"
---

## Heading Description ##
The details of the woman’s admission.

The following FHIR profiles are used to form the Admission details list structure:

- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)
- [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)
- [RelatedPerson](http://hl7.org/fhir/STU3/relatedperson.html)
- [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)
- [CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)
- [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1)

The following profiles are referenced from the Admission details list structure:

- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)

## Admission Details Structure ##

{% include custom/admission_details.svg %}


## Maternity Data Set Mapping to FHIR profiles ##

The following tables detail how to populate the FHIR resources and the mapping to the Maternity data set.

## Mapping for Admission Details List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_admission_details_all.html#mapping-for-admission-details-list)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for XXX Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  List | ​ |  |  | Information summarized from a list of other resources<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (lst-2): The deleted flag can only be used if the mode of the list is "changes"<br/>Constraint (lst-1): A list can only have an emptyReason if it is empty |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | Meta | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-List-1'</font><br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font>  |
|  - implicitRules | 0..1 | Not Used | Uri | A set of rules under which this content was created |
|  - language | 0..1 | Not Used | Code | Language of the resource content<br/>Binding (extensible): A human language. [Common Languages](http://hl7.org/fhir/stu3/valueset-languages.html) |
|  - text | 0..1 | Not Used | Narrative | Text summary of the resource, for human interpretation |
|  - contained | 0..* | Not Used | Resource | Contained, inline Resources |
|  - extension (clinicalSetting) | 0..1 | Not Used | [Extension-CareConnect-ClinicalSetting-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-ClinicalSetting-1 "Extension-CareConnect-ClinicalSetting-1") | **To record the clinical setting of a problem list<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>** |
|  - extension (warningCode) | 0..1 | Not Used | [Extension-CareConnect-ListWarningCode-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-ListWarningCode-1 "Extension-CareConnect-ListWarningCode-1") | **To capture warnings that the list may be incomplete<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>** |
|  - modifierExtension | 0..* | Not Used | Extension | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/>Slicing: Description: Extensions are always sliced by (at least) url, Discriminator: url, Ordering: false, Rules: Open |
|  - identifier | 0..* | Required | Identifier | Business identifier<br/><font color='red'>An identifier for this Admission details list'</font><br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font>  |
|  - - use | 0..1 | Not Used | Code | usual : official : temp : secondary (If known)<br/>Binding (required): Identifies the purpose for this identifier, if known. [IdentifierUse](http://hl7.org/fhir/stu3/valueset-identifier-use.html) |
|  - - type | 0..1 | Not Used | CodeableConcept | Description of identifier<br/>Binding (extensible): A coded type for an identifier that can be used to determine which identifier to use for a specific purpose. [Identifier Type Codes](http://hl7.org/fhir/stu3/valueset-identifier-type.html) |
|  - - - coding | 0..* | Not Used | Coding | Code defined by a terminology system |
|  - - - - system | 0..1 | Not Used | Uri | Identity of the terminology system |
|  - - - - version | 0..1 | Not Used | String | Version of the system - if relevant |
|  - - - - code | 0..1 | Not Used | Code | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Not Used | String | Representation defined by the system |
|  - - - - userSelected | 0..1 | Not Used | Boolean | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Not Used | String | Plain text representation of the concept |
|  - - system | 1..1 | Required | Uri | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from'</font><br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font>  |
|  - - value | 1..1 | Required | String | The value that is unique<br/>Business identifier<br/><font color='red'>An identifier for this Admission details list'</font><br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font>  |
|  - - period | 0..1 | Not Used | Period | <font color='red'>A identifier'</font> |
|  - - - start | 0..1 | Not Used | dateTime | Starting time with inclusive boundary |
|  - - - end | 0..1 | Not Used | dateTime | End time with inclusive boundary, if not ongoing |
|  - - assigner | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Not Used | [CareConnect-Organization-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Organization-1 "CareConnect-Organization-1") |  |
|  - - - reference | 0..1 | Not Used | String | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Not Used | Identifier | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Select | String | Text alternative for the resource<br/><font color='red'>The organization that allcated the identifier'</font><br/><br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font>  |
|  - status | 1..1 | Mandatory | Code | current : retired : entered-in-error<br/>Binding (required): The current state of the list [ListStatus](http://hl7.org/fhir/stu3/valueset-list-status.html)<br/><font color='red'>The status of the list MUST contain the value currentt'</font><br/><br/><font color='red'><b>Mapping to Maternity Data item Not applicable</b></font>  |
|  - mode | 1..1 | Mandatory | Code | working : snapshot : changes<br/>Binding (required): The processing mode that applies to this list [ListMode](http://hl7.org/fhir/stu3/valueset-list-mode.html) |
|  - title | 0..1 | Select | String | Descriptive name for the list |
|  - code | 0..1 | Select | CodeableConcept | What the purpose of this list is<br/>Binding (preferred): What the purpose of a list is [CareConnect-ListCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListCode-1) |
|  - - coding | 0..* | Select | Coding | Code defined by a terminology system |
|  - - - system | 0..1 | Select | Uri | Identity of the terminology system |
|  - - - version | 0..1 | Select | String | Version of the system - if relevant |
|  - - - code | 0..1 | Select | Code | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Select | String | Representation defined by the system |
|  - - - userSelected | 0..1 | Select | Boolean | If this coding was chosen directly by the user |
|  - - text | 0..1 | Select | String | Plain text representation of the concept |
|  - subject | 0..1 | Select | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Select | [Group](http://hl7.org/fhir/STU3/group.html "Group") |  |
|   |  | Select | [Device](http://hl7.org/fhir/stu3/StructureDefinition/Device "Device") |  |
|   |  | Select | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|   |  | Select | [CareConnect-Location-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Location-1 "CareConnect-Location-1") |  |
|  - - reference | 0..1 | Select | String | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Select | Identifier | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Select | String | Text alternative for the resource |
|  - encounter | 0..1 | Select | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Context in which list created<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Select | [CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1 "CareConnect-Encounter-1") |  |
|  - - reference | 0..1 | Select | String | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Select | Identifier | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Select | String | Text alternative for the resource |
|  - date | 0..1 | Select | dateTime | When the list was prepared |
|  - source | 0..1 | Select | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who and/or what defined the list contents (aka Author)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Select | [Device](http://hl7.org/fhir/stu3/StructureDefinition/Device "Device") |  |
|   |  | Select | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|   |  | Select | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") |  |
|  - - reference | 0..1 | Select | String | Literal reference, Relative, internal or absolute URL |
|  - - identifier | 0..1 | Select | Identifier | Logical reference, when literal reference is not known |
|  - - display | 0..1 | Select | String | Text alternative for the resource |
|  - orderedBy | 0..1 | Select | CodeableConcept | What order the list has<br/>Binding (preferred): What order applies to the items in a list [List Order Codes](http://hl7.org/fhir/stu3/valueset-list-order.html) |
|  - - coding | 0..* | Select | Coding | Code defined by a terminology system |
|  - - - system | 0..1 | Select | Uri | Identity of the terminology system |
|  - - - version | 0..1 | Select | String | Version of the system - if relevant |
|  - - - code | 0..1 | Select | Code | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Select | String | Representation defined by the system |
|  - - - userSelected | 0..1 | Select | Boolean | If this coding was chosen directly by the user |
|  - - text | 0..1 | Select | String | Plain text representation of the concept |
|  - note | 0..* | Select | Annotation | Comments about the list |
|  - - author[x] | 0..1 | Select | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Individual responsible for the annotation<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Select | [RelatedPerson](http://hl7.org/fhir/stu3/StructureDefinition/RelatedPerson "RelatedPerson") |  |
|   |  | Select | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") |  |
|   |  | Select | [CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1 "CareConnect-Practitioner-1") |  |
|   |  | Select | String |  |
|  - - time | 0..1 | Select | dateTime | When the annotation was made |
|  - - text | 1..1 | Select | String | The annotation - text content |
|  - entry | 0..* | Select | BackboneElement | Entries in the list |
|  - - modifierExtension | 0..* | Select | Extension | Extensions that cannot be ignored<br/>Constraint (ext-1): Must have either extensions or value[x], not both |
|  - - flag | 0..1 | Select | CodeableConcept | Status/Workflow information about this item<br/>Binding (example): Codes that provide further information about the reason and meaning of the item in the list [Patient Medicine Change Types](http://hl7.org/fhir/stu3/valueset-list-item-flag.html) |
|  - - - coding | 0..* | Select | Coding | Code defined by a terminology system |
|  - - - - system | 0..1 | Select | Uri | Identity of the terminology system |
|  - - - - version | 0..1 | Select | String | Version of the system - if relevant |
|  - - - - code | 0..1 | Select | Code | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Select | String | Representation defined by the system |
|  - - - - userSelected | 0..1 | Select | Boolean | If this coding was chosen directly by the user |
|  - - - text | 0..1 | Select | String | Plain text representation of the concept |
|  - - deleted | 0..1 | Select | Boolean | If this item is actually marked as deleted<br/>Default Value: false |
|  - - date | 0..1 | Select | dateTime | When item added to list |
|  - - item | 1..1 | Select | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Select | [Resource](http://hl7.org/fhir/stu3/StructureDefinition/Resource "Resource") |  |
|  - - - reference | 0..1 | Select | String | Literal reference, Relative, internal or absolute URL |
|  - - - identifier | 0..1 | Select | Identifier | Logical reference, when literal reference is not known |
|  - - - display | 0..1 | Select | String | Text alternative for the resource |
|  - emptyReason | 0..1 | Select | CodeableConcept | Why list is empty<br/>Binding (preferred): If a list is empty, why it is empty [CareConnect-ListEmptyReasonCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListEmptyReasonCode-1) |
|  - - coding | 0..* | Select | Coding | Code defined by a terminology system |
|  - - - system | 0..1 | Select | Uri | Identity of the terminology system |
|  - - - version | 0..1 | Select | String | Version of the system - if relevant |
|  - - - code | 0..1 | Select | Code | Symbol in syntax defined by the system |
|  - - - display | 0..1 | Select | String | Representation defined by the system |
|  - - - userSelected | 0..1 | Select | Boolean | If this coding was chosen directly by the user |
|  - - text | 0..1 | Select | String | Plain text representation of the concept |

## Mapping for Admission Details Encounter ##

|>|Level 1|[Encounter Resource](http://hl7.org/fhir/stu3/encounter.html)|>|Level 2|[CareConnect-Encounter-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Encounter-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_admission_details_all.html#mapping-for-admission-details-encounter)**|

## Mapping for Admission Details RelatedPerson ##

|>|Level 1|[RelatedPerson Resource](http://hl7.org/fhir/stu3/relatedPerson.html)|>|Level 2|None|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_admission_details_all.html#mapping-for-admission-details-relatedperson)**|

## Mapping for Admission Details Practitioner ##

|>|Level 1|[Practitioner Resource](http://hl7.org/fhir/stu3/practitioner.html)|>|Level 2|[CareConnect-Practitioner-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Practitioner-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_admission_details_all.html#mapping-for-admission-details-practitioner)**|

## Mapping for Admission Details PractitionerRole ##

|>|Level 1|[Practitioner Resource](http://hl7.org/fhir/stu3/practitionerRole.html)|>|Level 2|[CareConnect-PractitionerRole-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-PractitionerRole-1)|>|Level 3|None|


|**View Used FHIR Elements**|**[View All FHIR Elements](explore_admission_details_all.html#mapping-for-admission-details-practitionerrole)**|