+++
title = "eMAR details"
linktitle = "emar_detail"
weight = 1
toc = false

[menu]
  [menu.main]
    parent = "Hosp Tables"

+++

# The EMAR_DETAIL table

The EMAR_DETAIL table contains information for each medicine administration made in the EMAR table.
Information includes the associated pharmacy order, the dose due, the dose given, and many other parameters associated with the medical administration.

**Table source:** Hospital database.

**Table purpose:** Provide informtion about medical administrations made for patients while in the hospital.

**Number of rows:** 

**Links to:**

* EMAR on `mar_num`

<!--

# Important considerations

-->

# Table columns

Name | Postgres data type
---- | ----
`subject_id` | INTEGER NOT NULL
`mar_num` | SMALLINT NOT NULL
`parent_field_ordinal` | NUMERIC(5, 3)
`administration_types` | VARCHAR(50)
`pharmacy_order_id` | INTEGER
`pharmacy_order_note` | VARCHAR(20)
`Barcode_Type` | VARCHAR(4)
`Reason_for_No_Barcode` | TEXT
`Complete_Dose_Not_Given` | VARCHAR(5)
`Dose_Due` | VARCHAR(50)
`Dose_Due_Unit` | VARCHAR(50)
`Dose_Given` | VARCHAR(255)
`Dose_Given_Unit` | VARCHAR(50)
`will_remainder_of_dose_be_given` | VARCHAR(5)
`Product_Amount_Given` | VARCHAR(30)
`Product_Unit` | VARCHAR(30)
`Product_Code` | VARCHAR(30)
`Product_Description` | VARCHAR(255)
`Product_Description_Other` | VARCHAR(255)
`Prior_Infusion_Rate` | VARCHAR(20)
`Infusion_Rate` | VARCHAR(20)
`Infusion_Rate_Adjustment` | VARCHAR(50)
`Infusion_Rate_Adjustment_Amount` | VARCHAR(30)
`Infusion_Rate_Units` | VARCHAR(30)
`Route` | VARCHAR(5)
`Infusion_Complete` | VARCHAR(255)
`Completion_Interval` | VARCHAR(30)
`New_IV_Bag_Hung` | VARCHAR(1)
`Continued_infusion_in_other_location` | VARCHAR(1)
`Reason_for_Unscheduled_Stop_or_Removal` | TEXT
`Restart_Interval` | VARCHAR(30)
`Side` | VARCHAR(10)
`Site` | VARCHAR(255)
`non_formulary_visual_verification` | VARCHAR(1)

# Detailed Description

## `subject_id`

`subject_id` is a unique identifier which specifies an individual patient. Any rows associated with a single `subject_id` pertain to the same individual.

## `parent_field_ordinal`

parent field delineates multiple adm for the same eMar event, e.g. multiple formulary doses for the full dose.