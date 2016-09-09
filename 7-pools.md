---
layout: page
title: Pools and Dilutions
---

# 7. Dilutions, Pools and Orders
A library cannot be directly loaded into a _lane_ in a _sequencing container_
(flowcell/SMRTcell) in MISO. A dilution must be made and then many dilutions
(or just one) can be mixed into a _pool_ for sequencing.

_Orders_ are requests for sequencing pools a certain number of times. They are
used to keep track of sequencing progress for project management and book-keeping. 

## 7.1 Bulk creating Library Dilutions
Dilutions can be made in bulk from libraries.

<img src="pics/flow-dilution.svg"/>

In this exercise, we will create 4 library dilutions from the libraries we
made previously.

1. On the _List Libraries_ page, check all the libraries just created.
  - `PROJ_0001_Br_P_PE_300_EX`
  - `PROJ_0001_Ly_R_PE_300_EX`
  - `PROJ_0002_Br_P_PE_300_EX`
  - `PROJ_0002_Ly_R_PE_300_EX`
1. From the _Bulk actions_ drop down, select _Make dilutions from selected_ and click _Go_.
1. Enter the concentrations of the dilutions (use any number you wish).
1. Click _Save_.

Dilutions are a bit ephemeral in MISO: there is no list for all the dilutions.
To see the dilutions for a library, view the library page. At present,
Dilutions cannot be saved in Boxes.

## 7.2 Pools
Pools are the last step for libraries before sequencing and represent the
entity that is loaded onto the flowcell lane or SMRTcell. A "pool" can have one or more
library dilutions in it. They are equivalent to "worksets" in Geospiza, but are
required for every lane of sequencing.

<img src="pics/flow-pool.svg"/>

Here we will all all of the dilutions we added previously to make a single pool
of 4.

1. On the _List Pools_ page, under the _Illumina_ tab, select _Options_ → _Add Pool_.
1. Enter the _Pool Information_:
  1. _Alias_: A short description of the pool contents. Enter the project name
followed by `_POOL` (e.g. `PROJ_POOL`)
  1. _Description_: A longer free-text description of the pool. 
  1. _Platform Type_: Leave `Illumina` selected.
  1. _Desired Concentration_: Enter a concentration.
  1. _Creation Date_: Select a date.
  1. _Ready to Run_: Whether or not the pool is ready for sequencing. This flag
     is used together with the Order to show the pool is ready to be sequenced.
     Tick this box.
  1. _Volume_: Enter a pool volume.
1. In the _Pooled Elements_ section, use the search box to find the dilutions created previously.
1. For each dilution, press the _+_ button to add the dilution to the pool.
1. Click _Save_.

Only pools marked as ready to run will be visible when making sequencing
containers (which associate flowcell/SMRTcell Runs with pools).

## TODO: fixme
This pool has a low quality library in it and this will be highlighted when
adding it to the flow cell.

## 8.1 Creating an Order
Orders are created on the pool to be sequenced, and include the quantity of sequencing
required (counted in lanes/SMRT cells), and the sequencing chemistry
required (on Illumina).

1. On the Edit Pool page for the pool you just created, scroll down to the
_Orders_ heading.
1. Fill in the new order box:
  - _Partitions_: the number of lanes/cells that should run for this pool. Enter
`2`
  - _Platform_: Select the instrument for sequencing. `Illumina - Illumina HiSeq 2500`
  - _Sequencing Parameters_: Select `v4 2×126` chemistry.
1. Click _Add_. The order will now be visible in the _Orders_ section.

### 8.1.1  Checking for unfulfilled orders
The _List Orders_ page is used to decide what needs to be sequenced.

1. From the navigation menu, choose _List Orders_.
1. Verify that the pool you just created is listed in the _Unfulfilled_ tab.

Columns on this page will disappear if there are no entries (_e.g._,
the _Failed_ column will not be shown if there are no failed runs). When enough
lanes have been sequenced, the row will disappear from the _Unfulfilled_ tab,
but remain in the _All_ tab. Lanes currently being sequenced will be marked as
in-progress and remain on the _Unfulfilled_ tab until the run transitions to
_Completed_.

A pool can have many orders. Orders for the same platform and chemistry are
summed when displayed on this page.


[Back](6-libraries) [Home](index) [Next](8-runs)
