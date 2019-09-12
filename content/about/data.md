+++
date = "2015-09-01T19:33:17-04:00"
title = "MIMIC-IV"
linktitle = "MIMIC-IV"
weight = 1
toc = false

[menu]
  [menu.main]
    parent = "About"

+++

# MIMIC-IV

MIMIC-IV is an update to MIMIC-III, containing hospitalized patients from 2008 - 2018 inclusive. The data is separated into ``modules'' to reflect the non-overlapping nature and distinct origins of the individual modules.

There are currently five modules:

- core - admissions/transfers/stays/services - this is the hospital level patient tracking dataset
- hosp - hospital level data for patients: labs, micro, and electronic medication administration
- icu - ICU level data. These are the event tables, and are identical in structure to MIMIC-III (chartevents, etc)
- ed - data from the emergency department, fairly simple structure
- cxr - metadata linking CXRs to patients

All patients across all datasets are in mimic_core. However, not all ICU patients have ED data, not all ICU patients have CXRs, not all ED patients have hospital data, and so on. Within an individual dataset, there are also incomplete tables as certain electronic systems did not exist in the past. For example, eMAR data is only available from 2015 onward. A metadata table is being created to identify all major instances of this behavior.

# Release notes

This page lists changes implemented in sequential updates to the MIMIC-CXR database. Issues are tracked using a unique issue number, usually of the form #100, #101, etc (this issue number relates to a private 'building' repository).

## Current version

The current version of the database is v0.1. When referencing this version, we recommend using the full title: MIMIC-IV v0.1.

## MIMIC-IV v0.1

MIMIC-IV v0.1 was released on 15 August 2019.
