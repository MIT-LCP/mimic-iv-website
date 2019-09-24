+++
title = "Patients"
linktitle = "patients"
weight = 1
toc = false

[menu]
  [menu.main]
    parent = "Core Tables"

+++

# The patients table

Information that is consistent for the lifetime of a patient is stored in this table.

**Table source:** Hospital database.

**Table purpose:** Contains demographics for all patients.

**Number of rows:** 288,710

# Table columns

Name | Postgres data type
---- | ----
subject_id | INT
GENDER | VARCHAR(5)
ANCHOR\_AGE | INT
ANCHOR\_YEAR | INT
ANCHOR\_YEAR_SHIFTED | INT
DOB | TIMESTAMP(0)
DOD | TIMESTAMP(0)

# Detailed Description

## `subject_id`

`subject_id` is a unique identifier which specifies an individual patient. Any rows associated with a single `subject_id` pertain to the same individual. As `subject_id` is the primary key for the table, it is unique for each row. 

## `GENDER`

`GENDER` is the genotypical sex of the patient.

## `DOD`

`DOD` is the date of death as recorded in the hospital database.
