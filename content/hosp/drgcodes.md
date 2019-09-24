+++
title = "DRG Codes"
linktitle = "drgcodes"
weight = 1
toc = false

[menu]
  [menu.main]
    parent = "Hosp Tables"

+++

# The DRGCODES table

**Table source:** Hospital database.

**Table purpose:** Stores diagnosis related groups: codes which identify the primary reason for a patients hospitalization, which are subsequently used for reimbursement.

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
`drg_type` | VARCHAR(4)
`description` | VARCHAR(195)
`drg_severity` | SMALLINT
`drg_mortality` | SMALLINT

# Detailed Description

Diagnosis related groups (DRGs) are used by the hospital to obtain reimbursement for a patient's hospital stay.
The codes correspond to the primary reason for a patient's stay at the hospital.

## `subject_id`

`subject_id` is a unique identifier which specifies an individual patient. Any rows associated with a single `subject_id` pertain to the same individual.

## `hadm_id`

## `drg_type`

The specific DRG ontology used for the code.

## `description`

A coded description for the given DRG code.

## `drg_severity`, `drg_mortality`

Some DRG ontologies further qualify the patient severity of illness and likelihood of mortality, which are recorded here.