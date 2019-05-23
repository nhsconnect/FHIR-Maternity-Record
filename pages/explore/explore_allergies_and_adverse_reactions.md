---
title: Allergies and Adverse Reactions List
keywords:  Lists
tags: [fhir,messaging]
sidebar: foundations_sidebar
permalink: explore_allergies_and_adverse_reactions.html
summary: "The FHIR profiles used for the Allergies and Adverse Reactions list"
---

## Heading Description ##
The details of any known allergies, intolerances or adverse reactions.

The following FHIR profiles are used to form the Allergies and reactions list structure:

- [CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)
- [CareConnect-AllergyIntolerance-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-AllergyIntolerance-1)

The following profiles are referenced from the Allergies and reactions list structure:

- [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1)

## Allergies and Adverse Reactions List Structure ##

{% include custom/allergy_adverse.svg %}

## Maternity Data Standard Mapping to FHIR profiles ##

## Mapping Overview ##

|**Data Standard Element**|**FHIR Profile Mapping**|**FHIR Element**|
|Date/Time Recorded|[List](explore_allergy-and-adverse-reactions.html#mapping-for-allergy-and-adverse-reactions-list)|entry.date|
|Date/Time Asserted|[AllergyIntolerance](explore_allergy-and-adverse-reactions.html#mapping-for-allergy-and-adverse-reactions-allergyintolerance)|assertedDate|
|Causative Agent|[AllergyIntolerance](explore_allergy-and-adverse-reactions.html#mapping-for-allergy-and-adverse-reactions-allergyintolerance)|code.coding<br/>code.text|
|Description of Reaction|[AllergyIntolerance](explore_allergy-and-adverse-reactions.html#mapping-for-allergy-and-adverse-reactions-allergyintolerance)|reaction.manifestation.coding<br/>code.text|
|Type of Reaction|[AllergyIntolerance](explore_allergy-and-adverse-reactions.html#mapping-for-allergy-and-adverse-reactions-allergyintolerance)|type|
|Certainty|[AllergyIntolerance](explore_allergy-and-adverse-reactions.html#mapping-for-allergy-and-adverse-reactions-allergyintolerance)|verificationStatus|
|Severity|[AllergyIntolerance](explore_allergy-and-adverse-reactions.html#mapping-for-allergy-and-adverse-reactions-allergyintolerance)|severity|
|Evidence|[AllergyIntolerance](explore_allergy-and-adverse-reactions.html#mapping-for-allergy-and-adverse-reactions-allergyintolerance)|note|
|Date First Experienced|[AllergyIntolerance](explore_allergy-and-adverse-reactions.html#mapping-for-allergy-and-adverse-reactions-allergyintolerance)|onset|
|Comment|[AllergyIntolerance](explore_allergy-and-adverse-reactions.html#mapping-for-allergy-and-adverse-reactions-allergyintolerance)|note|

The following tables detail how to populate the FHIR resources and the mapping to the Maternity data standard.

## Mapping for Allergies and Adverse Reactions List ##

|>|Level 1|[List Resource](http://hl7.org/fhir/stu3/list.html)|>|Level 2|[CareConnect-List-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1)|>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_allergies_and_adverse_reactions_all.html#mapping-for-allergies-and-adverse-reactions-list)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  List | ​ |  |  | Information summarized from a list of other resources<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (lst-2): The deleted flag can only be used if the mode of the list is "changes"<br/>Constraint (lst-1): A list can only have an emptyReason if it is empty |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-List-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | Business identifier<br/><font color='red'>An identifier for this Allergies and adverse reactions list</font><br/> |
|  - - system | 1..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique<br/>Business identifier<br/><font color='red'>An identifier for this Allergies and adverse reactions list</font> |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource<br/><font color='red'>The organization that allocated the identifier</font> |
|  - status | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | current : retired : entered-in-error<br/>Binding (required): The current state of the list [ListStatus](http://hl7.org/fhir/stu3/valueset-list-status.html)<br/><font color='red'>The status of the list MUST contain the value 'current'</font> |
|  - mode | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | working : snapshot : changes<br/>Binding (required): The processing mode that applies to this list [ListMode](http://hl7.org/fhir/stu3/valueset-list-mode.html)<br/><font color='red'>The mode of the list MUST contain the value 'snapshot'</font> |
|  - title | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Descriptive name for the list<br/><font color='red'>This MUST contain the value 'Allergies and adverse reactions'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading Allergies and adverse reactions'</b></font>  |
|  - code | 0..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | What the purpose of this list is<br/>Binding (preferred): What the purpose of a list is [CareConnect-ListCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListCode-1)<br/><font color='red'>The PRSB heading for this list. Note: for Maternity the value stated below is used which is not from the preferred value set </font> |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/><font color='red'>The SNOMED CT concept for the PRSB heading type</font> |
|  - - - system | 0..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 0..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value '886921000000105'</font> |
|  - - - display | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>This MUST contain the value 'Allergies and adverse reactions'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading Allergies and adverse reactions'</b></font>  |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color='red'>This is the subject of the Allergies and adverse reactions List.<br/>This MUST use the CareConnect patient profile. </font>See [patient resource reference](explore_allergies_and_adverse_reactions.html#patient-reference) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - date | 0..1 | Mandatory | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the list was prepared<br/><font color='red'> This MUST contain a system date to indicate when the list was created or updated</font> |
|  - note | 0..* | Optional | [Annotation](http://hl7.org/fhir/stu3/datatypes.html#annotation "Annotation") | Comments about the list |
|   |  | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | <font color='red'>Who authored the comment on the list.</font>  |
|  - - time | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When the annotation was made |
|  - - text | 1..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The annotation - text content |
|  - entry | 0..* | Mandatory | [BackboneElement](http://hl7.org/fhir/stu3/backboneelement.html "BackboneElement") | Entries in the list<br/><font color='red'>The entries MUST be as per the diagram for this PRSB headings list with the AllergyIntolerance resource being the focal resource. Multiple resources MAY be present</font> |
|  - - date | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When item added to list<br/><font color='red'>The SHOULD contain a system time of when the item was added to the list.<br></font><font color='red'><b>Mapping to Maternity data item = 'Date/Time Recorded'</b></font> |
|  - - item | 1..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>A reference to an AllergyIntolerance resource included in the list<br/>This MUST use the CareConnect AllergyIntolerance profile. </font>See [AllergyIntolerance resource](explore_allergies_and_adverse_reactions.html#mapping-for-allergies-and-adverse-reactions) for information on how to populate the resource. |
|  - - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>The reference to the included AllergyIntolerance resource.</font> |

## Patient Reference ##

The Allergies and adverse reactions list has a mandated subject reference to the Patient resource. This means that any exchange of the Allergies and adverse reactions heading data must also include the [Patient demographics List.](explore_patient_demographics.html)

## Mapping for Allergies and Adverse Reactions AllergyIntolerance ##

|>|Level 1|[AllergyIntolerance Resource](http://hl7.org/fhir/stu3/allergyIntolerance.html)|>|Level 2|[CareConnect-AllergyIntolerance-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-AllergyIntolerance-1)|>|Level 3|None|

|**View Used FHIR Elements**|**[View All FHIR Elements](explore_allergies_and_adverse_reactions_all.html#mapping-for-allergies-and-adverse-reactions-allergyintolerance)**|

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  AllergyIntolerance | ​ |  |  | Allergy or Intolerance (generally: Risk of adverse reaction to a substance)<br/>Constraint (dom-2): If the resource is contained in another resource, it SHALL NOT contain nested Resources<br/>Constraint (dom-1): If the resource is contained in another resource, it SHALL NOT contain any narrative<br/>Constraint (dom-4): If a resource is contained in another resource, it SHALL NOT have a meta.versionId or a meta.lastUpdated<br/>Constraint (dom-3): If the resource is contained in another resource, it SHALL be referred to from elsewhere in the resource<br/>Constraint (ait-1): AllergyIntolerance.clinicalStatus SHALL be present if verificationStatus is not entered-in-error.<br/>Constraint (ait-2): AllergyIntolerance.clinicalStatus SHALL NOT be present if verification Status is entered-in-error |
|  - id | 0..1 | Optional | [Id](http://hl7.org/fhir/stu3/datatypes.html#id "Id") | Logical id of this artifact |
|  - meta | 1..1 | Mandatory | [Meta](http://hl7.org/fhir/stu3/resource.html#Meta "Meta") | Metadata about the resource |
|  - - profile | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Profiles this resource claims to conform to<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-AllergyIntolerance-1'</font> |
|  - identifier | 0..* | Required | [Identifier](http://hl7.org/fhir/stu3/datatypes.html#identifier "Identifier") | External ids for this item |
|  - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | The namespace for the identifier value |
|  - - value | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The value that is unique |
|  - - assigner | 0..1 | Required | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Organization that issued id (may be just text)<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Text alternative for the resource |
|  - clinicalStatus | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | active : inactive : resolved<br/>Binding (required): The clinical status of the allergy or intolerance. [AllergyIntoleranceClinicalStatus](http://hl7.org/fhir/stu3/valueset-allergy-clinical-status.html) |
|  - verificationStatus | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | unconfirmed : confirmed<br/>Binding (required): Assertion about certainty associated with a propensity, or potential risk, of a reaction to the identified substance. [CareConnect-AllergyVerificationStatus-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-AllergyVerificationStatus-1)<br/><font color='red'>This required ValueSet has mappings to SNOMED CT</font><br/><font color='red'><b>Mapping to Maternity data item = 'Certainty'.</b></font> |
|  - type | 0..1 | Required | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | allergy : intolerance - Underlying mechanism (if known)<br/>Binding (required): Identification of the underlying physiological mechanism for a Reaction Risk. [AllergyIntoleranceType](http://hl7.org/fhir/stu3/valueset-allergy-intolerance-type.html)<br/><font color='red'><b>Mapping to Maternity data item = 'Type of Reaction'.</b></font> |
|  - code | 0..1 | Mandatory | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Code that identifies the allergy or intolerance<br/>Binding (example): Type of the substance/product, allergy or intolerance condition, or negation/exclusion codes for reporting no known allergies. [AllergyIntolerance Substance/Product, Condition and Negation Codes](http://hl7.org/fhir/stu3/valueset-allergyintolerance-code.html)<br/><font color='red'>Note the example ValueSet is not used for Maternity and the following should be used instead</font><br/><font color='red'>Coded text - SNOMED CT (<105590001 \|SubstanceOR <373873005 \|Pharmaceutical / biologic product\|OR <716186003 \|No known allergy\|OR 196461000000101 \|Transfer-degraded drug allergy\|OR 196471000000108 \|Transfer-degraded non-drug allergy) - <br/>Alternatively one of the following statements: 'No known drug allergies' Or 'Information not available'.    |
|  - - coding | 0..* | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open |
|  - - coding (snomedCT) | 1..1 | Mandatory | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Binding (example): A code from the SNOMED Clinical Terminology UK or a code from the v3 Code System NullFlavor specifying why a valid value is not present. [CareConnect-AllergyCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-AllergyCode-1)<br/><font color='red'>Note the example ValueSet is not used for Maternity and the following should be used instead</font><br/><font color='red'>Coded text - SNOMED CT (<105590001 \|SubstanceOR <373873005 \|Pharmaceutical / biologic product\|OR <716186003 \|No known allergy\|OR 196461000000101 \|Transfer-degraded drug allergy\|OR 196471000000108 \|Transfer-degraded non-drug allergy) - <br/>Alternatively one of the following statements: 'No known drug allergies' Or 'Information not available'.    |
|  - - - system | 0..1 | Required | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 0..1 | Required | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Representation defined by the system<br/><font color='red'>Coded text - SNOMED CT (<105590001 \|SubstanceOR <373873005 \|Pharmaceutical / biologic product\|OR <716186003 \|No known allergy\|OR 196461000000101 \|Transfer-degraded drug allergy\|OR 196471000000108 \|Transfer-degraded non-drug allergy) |
|  - - - display | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Symbol in syntax defined by the system.<br/><font color='red'>This SHOULD be the preferred term for the SNOMED concept</font> |
|  - - text | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept<br/><font color='red'>This element SHOULD only be populated when the Allergy or adverse reaction cannot be coded or when stating  one of the following statements: 'No known drug allergies' Or 'Information not available'.</font> |
|  - patient | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who the sensitivity is for<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | A reference to the Patient resource.  |
|  - - reference | 0..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Literal reference, Relative, internal or absolute URL<br/><font color='red'>This MUST use the CareConnect Patient profile.</font>See [patient resource reference](explore_allergies_and_adverse_reactions.html#patient-reference) for information on how to populate the resource. |
|  - onset[x] | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | When allergy or intolerance was identified.<br/><font color='red'>When the reaction was first experienced. May be a date or partial date (e.g. year) or text (e.g. during childhood).</font><br/><font color='red'><b>Mapping to Maternity data item = 'Date First Experienced'.</b></font>  |
|   |  | Required | [Age](http://hl7.org/fhir/stu3/datatypes.html#age "Age") |  |
|   |  | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") |  |
|  - assertedDate | 1..1 | Mandatory | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Date record was believed accurate<br/><font color='red'><b>Mapping to Maternity data item = 'Date/Time Asserted'.</b></font> |
|  - note | 0..* | Required | [Annotation](http://hl7.org/fhir/stu3/datatypes.html#annotation "Annotation") | Additional text not captured in other fields<br/><font color='red'>Any additional comment or clarification about the allergy or adverse reaction</font><br/><font color='red'>Mapping to Maternity data item = 'Comment'.</b></font><br/><font color='red'>This element is also used to carry text that is the results of investigations that confirmed the certainty of the diagnosis. Examples might include results of skin prick allergy tests.</font><br/><font color='red'><b>Mapping to Maternity data item = 'Evidence'.</b></font> |
|  - - text | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | The annotation - text content |
|  - - manifestation | 1..* | Required | [CodeableConcept](http://hl7.org/fhir/stu3/datatypes.html#codeableconcept "CodeableConcept") | Clinical symptoms/signs associated with the Event<br/>Binding (extensible): Clinical symptoms and/or signs that are observed or associated with an Adverse Reaction Event. [CareConnect-AllergyManifestation-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-AllergyManifestation-1)<br/><font color='red'>A description of the manifestation of the allergic or adverse reaction experienced by the patient. For example, skin rash, swelling at injection site etc.</font><br/><font color='red'><b>Mapping to Maternity data item = 'Description of Reaction'.</b></font>  |
|  - - - coding | 0..* | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open |
|  - - - coding (snomedCT) | 0..1 | Required | [Coding](http://hl7.org/fhir/stu3/datatypes.html#coding "Coding") | Code defined by a terminology system<br/><font color='red'>Anything under ( 404684003 \| clinical finding (finding) \| ) .</font> |
|  - - - - system | 1..1 | Mandatory | [Uri](http://hl7.org/fhir/stu3/datatypes.html#uri "Uri") | Identity of the terminology system<br/><font color='red'>The element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - - code | 1..1 | Mandatory | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | Symbol in syntax defined by the system<br/><font color='red'> A SNOMED concept as specified above</font> |
|  - - - - display | 1..1 | Mandatory | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Representation defined by the system<br/><font color='red'>This SHOULD be the preferred term associated with the concept</font> |
|  - - - text | 0..1 | Required | [String](http://hl7.org/fhir/stu3/datatypes.html#string "String") | Plain text representation of the concept<br/><font color='red'>Free text field to be used if no coded text available. Note: the CareConnect profile currently does not allow non-coded allergies.</font>  |
|  - - onset | 0..1 | Required | [dateTime](http://hl7.org/fhir/stu3/datatypes.html#datetime "dateTime") | Date(/time) when manifestations showed |
|  - - severity | 0..1 | Required | [Code](http://hl7.org/fhir/stu3/datatypes.html#code "Code") | mild : moderate : severe (of event as a whole)<br/>Binding (required): Clinical assessment of the severity of a reaction event as a whole, potentially considering multiple different manifestations. [CareConnect-ReactionEventSeverity-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ReactionEventSeverity-1)<br/><font color='red'>This required ValueSet has mappings to SNOMED CT</font> |


## Allergies and Adverse Reactions Heading Example ##

<script src="https://gist.github.com/IOPS-DEV/28b5a5f2f854ec8393ff9aa808c8ef9c.js"></script>