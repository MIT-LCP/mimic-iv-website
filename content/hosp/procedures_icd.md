+++
title = "ICD Procedures"
linktitle = "procedures_icd"
weight = 1
toc = false

[menu]
  [menu.main]
    parent = "Hosp Tables"

+++

# The  table

**Table source:** Hospital database.

**Table purpose:** 

**Number of rows:** 

**Links to:**

<!--

# Important considerations

-->

# Table columns

Name | Postgres data type
---- | ----
`subject_id` | INTEGER
`hadm_id` | INTEGER
`seq_num` | INTEGER
`icd9_code` | CHAR(5)
`icd10_code` | CHAR(7)

# Detailed Description

During routine hospital care, patients are billed by the *hospital* for procedures they undergo.
This table contains a record of all procedures a patient was billed for during their hospital stay using the ICD-9 and ICD-10 ontologies.

# Important considerations

* Procedures during the hospital stay can be billed (1) by the hospital or (2) by the provider. This table contains only procedures billed by the hospital.

## `subject_id`

`subject_id` is a unique identifier which specifies an individual patient. Any rows associated with a single `subject_id` pertain to the same individual.

## `hadm_id`

## `seq_num`

The order in which the procedures occurred within the hospital stay.

## `icd9_code`, `icd10_code`

As the data overlaps with the transition period between ICD-9 and ICD-10, patients may be billed using ICD-9 or ICD-10 codes depending on their year of admission.
Only one type of code will be present for an individual hospitalization.