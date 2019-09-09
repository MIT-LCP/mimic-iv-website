+++
title = "Transfers"
linktitle = "transfers"
weight = 1
toc = false

[menu]
  [menu.main]
    parent = "Core Tables"

+++

# The transfers table

**Table source:** Hospital database.

**Table purpose:** Physical locations for patients throughout their hospital stay.

**Number of rows:** 1,530,887

**Links to:**

* PATIENTS on `SUBJECT_ID`
* ADMISSIONS on `HADM_ID`
* ICUSTAYS on `STAY_ID`

# Important considerations

* The ICUSTAYS table is derived from this table.

# Table columns

Name | Postgres data type
---- | ----
SUBJECT\_ID | INT
HADM\_ID | INT
STAY\_ID | INT
TRANSFER\_ID | INT
EVENTTYPE | VARCHAR(10)
INTIME | TIMESTAMP(0)
CAREUNIT | VARCHAR(255)
OUTTIME | TIMESTAMP(0)
LOS | INT


# Detailed Description

## `SUBJECT_ID`, `HADM_ID`, `STAY_ID`, `TRANSFER_ID`

Identifiers which specify the patient: `SUBJECT_ID` is unique to a patient, `HADM_ID` is unique to a patient hospital stay, `STAY_ID` is unique to a patient stay in a hospital unit, `TRANSFER_ID` is unique to a patient physical location.

## `EVENTTYPE`

`EVENTTYPE` describes what transfer event occurred: 'admit' for an admission, 'transfer' for an intra-hospital transfer and 'discharge' for a discharge from the hospital.

## `CAREUNIT`

`CAREUNIT` contains the care unit in which the patient currently resides. 

The `INTIME` and `OUTTIME` of the transfer event correspond to the `CAREUNIT`.

## `INTIME`, `OUTTIME`

`INTIME` provides the date and time the patient was transferred into the current care unit from the previous care unit. `OUTTIME` provides the date and time the patient was transferred out of the current physical location.

## `LOS`

`LOS` is the length of stay for the patient for the current physical location.
