---
layout: page
title: Libraries
---

# 6. Libraries
A _library_ is made from one sample for a single target _platform_ and
has a specific _design_ associated with it that decides the _selection_
and _strategies_ used to make the library. A library may also have _indices_
(primers) and QC information.

<img src="pics/flow-library.svg"/>

MISO stores two important pieces of information about how a library was generated:
the _selection_ (e.g., PCR, cDNA) and the _strategy_ (e.g., WGS, WXS,
amplicon). A _design_ captures both a selection and strategy and the list
of allowed designs is limited based on the sample type (_e.g._, a cDNA sample
can only have SM, WT, or MR library designs and these lock the selection and
strategy type accordingly).


## 6.1 Bulk propagate aliquots into libraries

In this section, you will use the aliquots you created already and create
libraries.

1. On the _List Samples_ page, enter your project name into the search box.
1. Check the gDNA aliquot samples to turn into libraries. These samples are the
ones that end in `_D_1`:
  - `PROJ_0001_Br_P_nn_1-1_D_1`
  - `PROJ_0001_Ly_R_nn_1-1_D_1`
  - `PROJ_0002_Br_P_nn_1-1_D_1`
  - `PROJ_0002_Ly_R_nn_1-1_D_1`
1. From the _Bulk actions_ drop down, select _Propagate (library) selected_.
1. A table will appear. Enter the library information:
  * _Alias_: The sample alias up to the tissue, library type, insert size,
    library design (_e.g._, `PROJ_0001_Br_P_PE_318_EX`) &#9888; This alias does
    not automatically fill in yet, so it must be entered:
      - `PROJ_0001_Br_P_PE_300_EX`
      - `PROJ_0001_Ly_R_PE_300_EX`
      - `PROJ_0002_Br_P_PE_300_EX`
      - `PROJ_0002_Ly_R_PE_300_EX`
  * _Description_: Library (Tissue type)(individual), e.g. `Library P1`
  * _Matrix Barcode_: As before, usually this would be scanned by the hand
    scanner. In this tutorial, enter matrix barcodes in the form (Short
name)_(Tissue type)(Individual)_Li, e.g. `PROJ_P1_Li`.
  * _Platform_: Illumina
  * _Type_: Paired End
  * _Selection_: PCR
  * _Strategy_: WXS
  * _Index Kit_: Nextera Dual Index
  * _Index 1_ and _Index 2_: Select any combination of indices you wish.
    Select different indices for each library. Selecting the same index for two
    different libraries will make you unable to pool those two libraries
    together later.
  * _Volume_: 100
  * _Kit_: Agilent SureSelect XT2
1. Choose _Save_.

Note that for dual-index libraries, only the first index needs to be
specified. The second is optional.

## 6.1 Quality control
There are three way to indicate library quality in MISO: 1)
Enter quantitative QC values under the _Library QC_ section; 2) The overall pre-sequencing quality
flag _QC passed_; and 3) The post-sequencing quality control _Low quality
library_.

### 6.2.1 Library QC
After measuring the insert size or concentration, this information can be
entered into each library. There is no bulk entry for this information yet, it must
be entered for each library.

1. From the _List Libraries_ page, find the `PROJ_0001_Br_P_PE_300_EX` library using
the search box and click the sample link.
1. On the right side of the _QCs_ heading, select _Options_ → _Add Library QC_.
1. Enter the information in the row:
  1. _QC Date_: Select a date.
  1. _Method_: Choose a QC instrument.
  1. _Results_: Enter the measurement.
  1. _Insert Size_: Enter the measured insert size.
1. Click _Add_.


### 6.2.2 QC passed
_QC Passed_ is a simple pass/fail flag for a library to decide if it is good
enough for sequencing. If not measured, this can be left as "Unknown".

1. From the _List Libraries_ page, find the `PROJ_0001_Br_P_PE_300_EX` library using 
the search box and click the sample link.
1. Change _QC passed_ from _Unknown_ to _True_.
1. Click _Save_.

### 6.2.3 Low Quality Sequencing
Not every library realises its full potential. After sequencing, specific
libraries can be flagged as having low sequencing quality. The
"Low Quality Sequencing" indicator causes any pool containing this library to be
flagged, so that it can be checked before it is sequenced again.

1. From the _List Libraries_ page, find the `PROJ_0002_Ly_R_PE_300_EX` library and click the link.
1. Check _Low Quality Sequencing_.
1. Click _Save_.

In later exercises, this library will be marked as suspect.

**TODO** Was it????

## 6.3 Boxes
Libraries can also be placed in boxes.

1. From the _List Boxes_ page, find the project-specific box you created before,
e.g. `PROJ_OUTBOX`.
1. Select an unused position and enter a library matrix barcode _PROJ_\_P1\_Li,
e.g. `PROJ_P1_Li`.
1. Click _Lookup_ and then _Update position_.
1. Repeat for the remaining libraries:
  - `PROJ_R1_Li`
  - `PROJ_P2_Li`
  - `PROJ_R2_Li`

[Back](5-boxes) [Home](index) [Next](7-pools)
