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

**Table source:** Hospital database.

**Table purpose:** Contains demographics for all patients.

**Number of rows:** 288,710

# Table columns

Name | Postgres data type
---- | ----
SUBJECT\_ID | INT
GENDER | VARCHAR(5)
ANCHOR\_AGE | INT
ANCHOR\_YEAR | INT
ANCHOR\_YEAR_SHIFTED | INT
DOB | TIMESTAMP(0)
DOD | TIMESTAMP(0)

# Detailed Description

## `SUBJECT_ID`

`SUBJECT_ID` is a unique identifier which specifies an individual patient. `SUBJECT_ID` is a candidate key for the table, so is unique for each row. Information that is consistent for the lifetime of a patient is stored in this table.

## `GENDER`

`GENDER` is the genotypical sex of the patient.

## `DOD`

`DOD` is the date of death as recorded in the hospital database.
