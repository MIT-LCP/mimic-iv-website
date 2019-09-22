+++
title = "Dimension table: ICD procedures"
linktitle = "d_icd_procedures"
weight = 1
toc = false

[menu]
  [menu.main]
    parent = "Hosp Tables"

+++

# The D_ICD_PROCEDURES table

**Table source:** Online sources.

**Table purpose:** Definition table for ICD procedures.

**Number of rows:** 82,763

**Links to:**

* PROCEDURES_ICD on `ICD9_CODE`
* PROCEDURES_ICD on `ICD10_CODE`

# Brief summary

This table defines International Classification of Diseases Version 9 (ICD-9) codes for **procedures**. These codes are assigned at the end of the patient's stay and are used by the hospital to bill for care provided. They can further be used to identify if certain procedures have been performed (e.g. surgery).

<!-- # Important considerations -->

# Table columns

Name | Postgres data type
---- | ----
ICD9\_CODE | VARCHAR(10)
SHORT\_TITLE | VARCHAR(50)
LONG\_TITLE | VARCHAR(300)

# Detailed Description

## `ICD9_CODE`, `ICD10_CODE`

`ICD9_CODE` is the International Coding Definitions Version 9 (ICD-9) code, and `ICD10_CODE` is version 10. Each code corresponds to a single procedural concept.

## `SHORT_TITLE`, `LONG_TITLE`

The title fields provide a brief definition for the given procedure code in `ICD9_CODE`.
