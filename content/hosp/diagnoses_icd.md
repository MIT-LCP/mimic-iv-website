+++
title = "ICD diagnoses"
linktitle = "diagnoses_icd"
weight = 1
toc = false

[menu]
  [menu.main]
    parent = "Hosp Tables"

+++

# The DIAGNOSES_ICD table

During routine hospital care, patients are billed by the *hospital* for diagnoses associated with their hospital stay.
This table contains a record of all diagnoses a patient was billed for during their hospital stay using the ICD-9 and ICD-10 ontologies.
Diagnoses are billed on hospital discharge, and are determined by trained persons who read signed clinical notes.

# Table columns

Name | Postgres data type
---- | ----
`subject_id` | INTEGER
`hadm_id` | INTEGER
`seq_num` | INTEGER
`icd9_code` | CHAR(5)
`icd10_code` | CHAR(7)

## `subject_id`

## `hadm_id`

## `seq_num`

The priority assigned to the diagnoses.
The priority can be interpreted as a ranking of which diagnoses are "important", but many caveats to this broad statement exist.
For example, patients who are diagnosed with sepsis must have sepsis as their *2nd* billed condition. The 1st billed condition must be the infectious agent.
There's also less importance placed on ranking low priority diagnoses "correctly" (as there may be no correct ordering of the priority of the 5th - 10th diagnosis codes, for example).

## `icd9_code`, `icd10_code`

As the data overlaps with the transition period between ICD-9 and ICD-10, patients may be billed using ICD-9 or ICD-10 codes depending on their year of admission.
Only one type of code will be present for an individual hospitalization.