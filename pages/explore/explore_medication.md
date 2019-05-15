---
title: Medication and Medical Devices Bundle
keywords:  list
tags: [fhir]
sidebar: foundations_sidebar
permalink: explore_medication.html
summary: "The FHIR profiles used for the Medication and medical devices Bundle"
---

## Heading Description ##
The details of and instructions for medications and medical equipment the woman is using or has been using but discontinued.

## Medications and Medical Devices Details Structure ##

{% include custom/medicationstatement.svg %}

## Mapping for Medication Statement List ##

|  **Name** | **Card.** | **Conformance** | **Type** | **Description, Constraints and mapping for Digital Maternity Implementation** |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | Meta | Metadata about the resource<br/><font color='red'>The value attribute of the profile element MUST contain the value 'https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-List-1'</font> |
|  - identifier | 0..* | Required | Identifier | Business identifier<br/><font color='red'>An identifier for this Medication Statement details list</font> |
|  - - system | 1..1 | Required | Uri | The namespace for the identifier value<br/><font color='red'>The system from which the identifier came from</font> |
|  - - value | 1..1 | Mandatory | String | The value that is unique<br/><font color='red'>An identifier for this Medication Statement details list</font> |
|  - status | 1..1 | Mandatory | Code | current : retired : entered-in-error<br/>Binding (required): The current state of the list [ListStatus](http://hl7.org/fhir/stu3/valueset-list-status.html)<br/><font color='red'>The status of the list MUST contain the value 'current'</font> |
|  - mode | 1..1 | Mandatory | Code | working : snapshot : changes<br/>Binding (required): The processing mode that applies to this list [ListMode](http://hl7.org/fhir/stu3/valueset-list-mode.html)<br/><font color='red'>The mode of the list MUST contain the value 'snapshot'</font> |
|  - title | 0..1 | Mandatory | String | Descriptive name for the list<br/><font color='red'>This MUST contain the value 'Observation'</font><br/><font color='red'><b>Mapping to Maternity data item = 'PSRB Heading Medications and Medical Devices'</b></font>  |
|  - code | 0..1 | Mandatory | CodeableConcept | What the purpose of this list is<br/>Binding (preferred): What the purpose of a list is [CareConnect-ListCode-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ListCode-1)<br/><font color='red'>The PRSB heading for this list. Note: for Maternity the value stated below is used which is not from the preferred value set </font> |
|  - - coding | 0..* | Mandatory | Coding | Code defined by a terminology system<br/><font color='red'>The SNOMED CT concept for the PRSB heading type</font> |
|  - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system<br/><font color='red'>This MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system<br/><font color='red'>This MUST contain the value '933361000000108''</font> |
|  - - - display | 0..1 | Mandatory | String | Representation defined by the system<br/><font color='red'>Mapping to Maternity data item = 'PSRB Heading Medications and medical devices'</font>  |
|  - subject | 0..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | If all resources have the same subject<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color='red'>This is a reference to the Patient who is the subject of the list.</font> |
|   |  | Mandatory | [CareConnect-Patient-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Patient-1 "CareConnect-Patient-1") | <font color="red">This is the subject of the Observations details List. This MUST use the CareConnect patient profile.</font>See [patient resource reference](explore_observation.html#patient-reference) for information on how to populate the resource. |
|  - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL<br/><font color='red'>A reference to the patient resource included in the Patient demographics list within the FHIR Bundle. Note the Patient demographics list is mandatory in the FHIR bundle</font>  |
|  - date | 0..1 | Required | dateTime | When the list was prepared<br/><font color="red">This MUST contain a system date to indicate when the list was created or updated</font> |
|  - entry | 0..* | Required | BackboneElement | Entries in the list<br/><font color="red">The entries MUST be as per the diagram for this PRSB headings list with the medicationStatement resource being the focal resource. Multiple resources MAY be present</font> |
|  - - date | 0..1 | Required | dateTime | When item added to list<br/><font color='red'>The SHOULD contain a system time of when the item was added to the list.</font> |
|  - - item | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Actual entry<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided<br/><font color="red">A reference to an MedicationStatement resource included in the list This MUST use the CareConnect MedicationStatement profile. |
|  - - - reference | 0..1 | Mandatory | String | Literal reference, Relative, internal or absolute URL |

## Mapping for Medication Statement (Cluster) ##

|  **Name** | **Card.** | **Conformance** | **Type** | Description, Constraints and mapping for Digotal Maternity Implementation |
| :--- | :--- | :--- | :--- | :--- |
|  - id | 0..1 | Optional | Id | Logical id of this artifact |
|  - meta | 0..1 | Mandatory | Meta | Metadata about the resource |
|  - extension (changeSummary) | 0..* | Optional | [Extension-CareConnect-MedicationChangeSummary-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/Extension-CareConnect-MedicationChangeSummary-1 "Extension-CareConnect-MedicationChangeSummary-1") | Optional Extensions Element<br/> |
|   - - extension (status) | 0..1 | Optional | Extension | The change status of a medication<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/><font color="red">The nature of any change made to the medication</font> |
|  - - - url | 1..1 | Mandatory | Uri | Identifies The Meaning Of The Extension<br/>Fixed Value: status |
|  - - - valueCode | 0..1 | Optional | Code | The change status of a medication.<br/>Binding (required): A ValueSet to identify the change status of a medication. (https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-MedicationChangeStatus-1 ) |
|  - - extension (indicationForChange) | 0..1 | Optional | Extension | Additional Content defined by implementations<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/><font color="red">Reason for change in medication, e.g. sub-therapeutic dose, patient intolerant.</font> |
|  - - - url | 1..1 | Mandatory | Uri | Identifies The Meaning Of The Extension<br/>Fixed Value: indicationForChange |
|  - - - valueCodeableConcept | 0..1 | Optional | CodeableConcept | Value of extension |
|  - - extension (dateChanged) | 0..1 | Optional | Extension | Additional Content defined by implementations<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/><font color="red">The date of the latest change - addition, or amendment</font> |
|  - - - url | 1..1 | Mandatory | Uri | Identifies The Meaning Of The Extension<br/>Fixed Value: dateChanged |
|  - - - valueDateTime | 0..1 | Optional | dateTime | Value of extension |
|  - - extension (detailsOfAmendment) | 0..1 | Optional | Extension | Additional Content defined by implementations<br/>Constraint (ext-1): Must have either extensions or value[x], not both<br/><font color="red">Where a change is made to the medication i.e. one drug stopped and another started or e.g. dose, frequency or route is changed.</font> |
|  - - - url | 1..1 | Mandatory | Uri | Identifies The Meaning Of The Extension<br/>Fixed Value: detailsOfAmendment |
|  - - - valueString | 0..1 | Optional | String | Value of extension |
|  - identifier | 0..* | Required | Identifier | External identifier |
|  - - system | 1..1 | Mandatory | Uri | The namespace for the identifier value |
|  - - value | 1..1 | Required | String | The value that is unique |
|  - status | 1..1 | Mandatory | Code | active : completed : entered-in-error : intended : stopped : on-hold<br/>Binding (required): A coded concept indicating the current status of a MedicationStatement. [MedicationStatementStatus](http://hl7.org/fhir/stu3/valueset-medication-statement-status.html) |
|  - medicationReference | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | What medication was taken<br/> |
|   | 0..1 | Mandatory | [Period](http://hl7.org/fhir/stu3/datatypes.html#period "Period") |  |
|  - subject | 1..1 | Mandatory | [Reference](http://hl7.org/fhir/stu3/references.html "Reference") | Who is/was taking the medication<br/>Constraint (ref-1): SHALL have a contained resource if a local reference is provided |
|  - taken | 1..1 | Mandatory | Code | y : n : unk : na<br/>Binding (required): A coded concept identifying level of certainty if patient has taken or has not taken the medication [MedicationStatementTaken](http://hl7.org/fhir/stu3/valueset-medication-statement-taken.html) |
|  - dosage | 0..* | Optional | Dosage | Details of how medication is/was taken or should be taken |
|  - - text | 0..1 | Optional | String | Free text dosage instructions e.g. SIG<br/><font color="red">A plain text description of medication single dose amount, as described in the AoMRC medication headings.  Comment: e.g. "30 mg" or "2 tabs". UK Secondary care clinicians and systems normally minimally structure their dose directions, separating Dose amount and Dose timing (often referred to as Dose and Frequency). This format is not normally used in GP systems, which will always import Dose and Frequency descriptions concatenated into the single Dose directions description.</font> |
|  - - additionalInstruction | 0..* | Optional | CodeableConcept | Supplemental instruction - e.g. "with meals"<br/>Binding (example): A coded concept identifying additional instructions such as "take with water" or "avoid operating heavy machinery". [SNOMED CT Additional Dosage Instructions](http://hl7.org/fhir/stu3/valueset-additional-instruction-codes.html) |
|  - - patientInstruction | 0..1 | Optional | String | Patient or consumer oriented instructions |
|  - - timing | 0..1 | Optional | Timing | When medication should be administered |
|  - - - - duration | 0..1 | Optional | Decimal | How long when it happens |
|  - - - code | 0..1 | Optional | CodeableConcept | BID : TID : QID : AM : PM : QD : QOD : Q4H : Q6H +<br/>Binding (preferred): Code for a known / defined timing pattern. [TimingAbbreviation](http://hl7.org/fhir/stu3/valueset-timing-abbreviation.html) |
|  - - - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system |
|  - - - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system |
|  - - - - - display | 0..1 | Mandatory | String | Representation defined by the system |
|  - - - - text | 0..1 | Optional | String | Plain text representation of the concept |
|  - - site | 0..1 | Optional | CodeableConcept | Body site to administer to<br/>Binding (example): A coded concept describing the site location the medicine enters into or onto the body. [SNOMED CT Anatomical Structure for Administration Site Codes](http://hl7.org/fhir/stu3/valueset-approach-site-codes.html)<br/><font color="red">The anatomical site at which the medication is to be administered. Comment: e.g. "Left eye"</font> |
|  - - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system |
|  - - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Mandatory | String | Representation defined by the system |
|  - - - text | 0..1 | Optional | String | Plain text representation of the concept |
|  - - route | 0..1 | Optional | CodeableConcept | How drug should enter body<br/>Binding (example): A coded concept describing the route or physiological path of administration of a therapeutic agent into or onto the body of a subject. [SNOMED CT Route Codes](http://hl7.org/fhir/stu3/valueset-route-codes.html)<br/><font color="red">Medication administration description (oral, IM, IV, etc.): may include method of administration (e.g., by infusion, via nebuliser, via NG tube) .</font> |
|  - - - coding | 0..* | Required | Coding | Code defined by a terminology system<br/>Slicing: Discriminator: system, Ordering: false, Rules: Open |
|  - - - coding (snomedCT) | 0..1 | Required | Coding | Code defined by a terminology system<br/>Binding (example): A code from the SNOMED Clinical Terminology UK coding system that describes the e-Prescribing route of administration. [CareConnect-MedicationDosageRoute-1](https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-MedicationDosageRoute-1) |
|  - - - - system | 1..1 | Mandatory | Uri | Identity of the terminology system<br/><font color='red'>The value attribute of the profile element MUST contain the value 'http://snomed.info/sct'</font> |
|  - - - - code | 1..1 | Mandatory | Code | Symbol in syntax defined by the system |
|  - - - - display | 1..1 | Mandatory | String | Representation defined by the system |
|  - - - text | 0..1 | Optional | String | Plain text representation of the concept |
|  - - method | 0..1 | Optional | CodeableConcept | Technique for administering medication<br/>Binding (example): A coded concept describing the technique by which the medicine is administered. [SNOMED CT Administration Method Codes](http://hl7.org/fhir/stu3/valueset-administration-method-codes.html) |
|  - - - coding | 0..* | Required | Coding | Code defined by a terminology system |
|  - - - - system | 0..1 | Mandatory | Uri | Identity of the terminology system |
|  - - - - code | 0..1 | Mandatory | Code | Symbol in syntax defined by the system |
|  - - - - display | 0..1 | Mandatory | String | Representation defined by the system |
|  - - - text | 0..1 | Optional | String | Plain text representation of the concept |

## Mapping for Medications and Medical Devices Practitioner ##

The medications and medical devices  details has reference(s) to the Practitioner resource. This means that any exchange of the medications and medical devices details heading data must also include the [Practitioner Details](explore_practitioner.html#mapping-for-practitioner)

## Mapping for Medications and Medical Devices Practitioner Role ##

The medications and medical devices  details has reference(s) to the Practitioner Role resource. This means that any exchange of the medications and medical devices  details heading data must also include the [Practitioner Role Details](explore_practitioner_role.html#mapping-for-practitioner_role)

## Mapping for Medications and Medical Devices Organisation ##

The medications and medical devices  details has reference(s) to the Practitioner Role resource. This means that any exchange of the medications and medical devices  details heading data must also include the [Practitioner Role Details](explore_organisation_role.html#mapping-for-practitioner_role)