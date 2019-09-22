+++
title = "Electronic Medical Administration Record"
linktitle = "emar"
weight = 1
toc = false

[menu]
  [menu.main]
    parent = "Hosp Tables"

+++

# The EMAR table

The EMAR table is used to record administrations of a given medicine to an individual patient.
Records in this table are populated by bedside nursing staff scanning barcodes associated with the medicine and the patient.

**Table source:** Hospital database.

**Table purpose:** Record electronic medical administrations.

**Number of rows:** 

**Links to:**

* EMAR_DETAIL on `mar_num`

<!--

# Important considerations

-->

# Table columns

Name | Postgres data type
---- | ----
`subject_id` | INTEGER NOT NULL
`hadm_id` | INTEGER
`mar_num` | SMALLINT NOT NULL
`poe_order_num` | SMALLINT NOT NULL
`charttime` | TIMESTAMP WITHOUT TIME ZONE NOT NULL
`medication` | TEXT
`scheduletime` | TIMESTAMP WITHOUT TIME ZONE
`storetime` | TIMESTAMP WITHOUT TIME ZONE NOT NULL