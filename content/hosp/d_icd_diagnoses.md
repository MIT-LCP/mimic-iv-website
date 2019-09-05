+++
title = "Dimension table: ICD diagnoses"
linktitle = "d_icd_diagnoses"
weight = 1
toc = false

[menu]
  [menu.main]
    parent = "Hosp Tables"

+++


# The d_icd_diagnoses table

**Table source:** Online sources.

**Table purpose:** Definition table for ICD diagnoses.

**Number of rows:** 108,911

**Links to:**

* DIAGNOSES_ICD ON `ICD9_CODE`
* DIAGNOSES_ICD ON `ICD10_CODE`

# Brief summary

This table defines International Classification of Diseases Version 9 (ICD-9) codes for **diagnoses**. These codes are assigned at the end of the patient's stay and are used by the hospital to bill for care provided.

<!-- # Important considerations -->

# Table columns

Name | Postgres data type
---- | ----
ICD9\_CODE | VARCHAR(10)
ICD10\_CODE | VARCHAR(10)
SHORT\_TITLE | VARCHAR(50)
LONG\_TITLE | VARCHAR(300)

# Detailed Description

## `ICD9_CODE`, `ICD10_CODE`

`ICD9_CODE` is the International Coding Definitions Version 9 (ICD-9) code, and `ICD10_CODE` is version 10. Each code corresponds to a single diagnostic concept.

## `SHORT_TITLE`, `LONG_TITLE`

The title fields provide a brief definition for the given diagnosis code in `ICD9_CODE`.
