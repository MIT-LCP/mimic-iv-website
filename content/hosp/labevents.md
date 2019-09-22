+++
title = "Labevents"
linktitle = "labevents"
weight = 1
toc = false

[menu]
  [menu.main]
    parent = "Hosp Tables"

+++

# The  table

**Table source:** Hospital database.

**Table purpose:** Store laboratory measurements for all patients.

**Number of rows:** 

**Links to:**

* D_LABITEMS on `itemid`

<!--

# Important considerations

-->

# Table columns

Name | Postgres data type
---- | ----
`subject_id` | INTEGER NOT NULL
`hadm_id` | INTEGER
`stay_id` | INTEGER
`spec_id` | INTEGER NOT NULL
`itemid` | INTEGER NOT NULL
`charttime` | TIMESTAMP NOT NULL
`storetime` | TIMESTAMP
`value` | VARCHAR(200)
`valuenum` | DOUBLE PRECISION
`valueuom` | VARCHAR(20)
`ref_range_lower` | DOUBLE PRECISION
`ref_range_upper` | DOUBLE PRECISION
`flag` | VARCHAR(10)
`priority` | VARCHAR(7)

# Detailed Description

The LABEVENTS table stores the results of all laboratory measurements made for a single patient.
These include hematology measurements, blood gases, chemistry panels, and less common tests such as genetic assays.