+++
title = "Admissions"
linktitle = "admissions"
weight = 1
toc = false

[menu]
  [menu.main]
    parent = "Core Tables"

+++

# The admissions table

**Table source:** Hospital database.

**Table purpose:** Define a patient's hospital admission, HADM\_ID.

**Number of rows:** 346,380

**Links to:**

* PATIENTS on `SUBJECT_ID`

# Brief summary

The ADMISSIONS table gives information regarding a patient's admission to the hospital. Since each unique hospital visit for a patient is assigned a unique `HADM_ID`, the ADMISSIONS table can be considered as a definition table for `HADM_ID`. Information available includes timing information for admission and discharge, demographic information, the source of the admission, and so on.

# Important considerations

* The data is sourced from the admission, discharge and transfer database from the hospital (often referred to as 'ADT' data).
* Organ donor accounts are sometimes created for patients who died in the hospital. These are distinct hospital admissions with very short, sometimes negative lengths of stay. Furthermore, their `DEATHTIME` is frequently the same as the earlier patient admission's `DEATHTIME`.
* All text data, except for that in the `INSURANCE` column, is stored in upper case.

# Table columns

Name | Postgres data type
---- | ----
SUBJECT\_ID | INT
HADM\_ID | INT
ADMITTIME | TIMESTAMP(0)
DISCHTIME | TIMESTAMP(0)
DEATHTIME | TIMESTAMP(0)
ADMISSION\_TYPE | VARCHAR(40)
ADMISSION\_LOCATION | VARCHAR(60)
DISCHARGE\_LOCATION | VARCHAR(60)
INSURANCE | VARCHAR(255)
LANGUAGE | VARCHAR(10)
ETHNICITY | VARCHAR(80)
EDREGTIME | TIMESTAMP(0)
EDOUTTIME | TIMESTAMP(0)
HOSPITAL\_EXPIRE_FLAG | SMALLINT

# Detailed description

The `ADMISSIONS` table defines all `HADM_ID` present in the database, covering an admission period between 1 January 2008 and 31 December 2018.

## `SUBJECT_ID`, `HADM_ID`

Each row of this table contains a unique `HADM_ID`, which represents a single patient's admission to the hospital. `HADM_ID` ranges from 2000000 - 2999999. It is possible for this table to have duplicate `SUBJECT_ID`, indicating that a single patient had multiple admissions to the hospital. The ADMISSIONS table can be linked to the PATIENTS table using `SUBJECT_ID`.

## `ADMITTIME`, `DISCHTIME`, `DEATHTIME`

`ADMITTIME` provides the date and time the patient was admitted to the hospital, while `DISCHTIME` provides the date and time the patient was discharged from the hospital. If applicable, `DEATHTIME` provides the time of in-hospital death for the patient. Note that `DEATHTIME` is only present if the patient died in-hospital, and is almost always the same as the patient's `DISCHTIME`. However, there can be some discrepancies due to typographical errors.

## `ADMISSION_TYPE`

`ADMISSION_TYPE` describes the type of the admission.

## `ADMISSION_LOCATION`

`ADMISSION_LOCATION` provides information about the previous location of the patient prior to arriving at the hospital.

## `INSURANCE`, `LANGUAGE`, `ETHNICITY`

The `INSURANCE`, `LANGUAGE`, `ETHNICITY` columns describe patient demographics. These columns occur in the ADMISSIONS table as they are originally sourced from the admission, discharge, and transfers (ADT) data from the hospital database.

## `EDREGTIME`, `EDOUTTIME`

Time that the patient was registered and discharged from the emergency department.

## `HOSPITAL_EXPIRE_FLAG`

This indicates whether the patient died within the given hospitalization. `1` indicates death in the hospital, and `0` indicates survival to hospital discharge.
