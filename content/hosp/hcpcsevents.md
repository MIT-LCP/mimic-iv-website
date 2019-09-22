+++
title = "HCPCS events"
linktitle = "hcpcsevents"
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
`hcpcs_cd` | CHAR(5)
`ticket_id_seq` | INTEGER
`short_description` | TEXT

# Detailed Description

## `subject_id`

Identifier which is unique to a given patient.

## `hadm_id`

Identifier which is unique to a patient hospitalization.

## `hcpcs_cd`

A five character code which uniquely represents the event.
Link this to `code` in D_HCPCS for a longer description of the code.

## `ticket_id_seq`

An assigned order to HCPCS codes for an individual hospitalization. This order sometimes conveys meaning, e.g. sometimes higher priority, but this is not guaranteed across all codes.

## `short_description`

A short textual descriptions of the `hcpcs_cd` listed for the given row.