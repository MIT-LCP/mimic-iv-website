+++
title = "Dimension table: microbiology items"
linktitle = "d_micro"
weight = 1
toc = false

[menu]
  [menu.main]
    parent = "Hosp Tables"

+++


# The d_labitems table

**Table source:** Hospital database.

**Table purpose:** Definition table for all microbiology measurements.

**Number of rows:** 1294

**Links to:** 

* MICROBIOLOGYEVENTS on `ITEMID`

# Table columns

Name | Postgres data type 
---- | ---- 
ITEMID | INT
LABEL | VARCHAR(100)
CATEGORY | VARCHAR(100)

## `ITEMID`

As the primary key of the table, `ITEMID` is unique to each row.

## `LABEL`

The `LABEL` column describes the concept which is represented by the `ITEMID`, e.g. "AMPICILLIN".

## `CATEGORY`

`CATEGORY` categorizes the `ITEMID` into one of four types:

* ANTIBIOTIC
* MICROTEST
* ORGANISM
* SPECIMEN

 "SPECIMEN" describes the sample taken to perform the test, "MICROTEST" describes the type of test performed, "ORGANISM" is the biological organism grown, and "ANTIBIOTIC" is the antibiotic used for evaluating sensitivity of an organism.