+++
title = "CXR Record List"
linktitle = "cxr_record_list"
weight = 1
toc = false

[menu]
  [menu.main]
    parent = "CXR Tables"

+++

# CXR Record List

This table lists all records in the MIMIC-CXR database.
Each DICOM file, corresponding to a single chest x-ray, is assigned a unique `dicom_id`.
This table links those IDs to a `study_id` for the radiology report and a `subject_id` for the patient.

**Table source:** Hospital database.

**Table purpose:** Provides a link between `subject_id`, `study_id`, and `dicom_id`.

**Number of rows:** 

**Links to:**

* CORE.PATIENTS on `subject_id`

<!-- # Important considerations -->

# Table columns

Name | Postgres data type
---- | ----
`subject_id`   | INTEGER NOT NULL
`study_id`     | INTEGER NOT NULL
`dicom_id`     | TEXT NOT NULL

## `subject_id`

## `study_id`

A unique identifier for the radiology report written for the given chest x-ray.

## `dicom_id`

A unique identifier for the chest x-ray.