---
layout: page
category: walkthrough
title: Libraries tutorial

---

<div id="toc">
Table of Contents
<ol>
   <li><a href="#login">Logging In</a></li>
   <li><a href="#props1">Propagating aliquots to libraries</a></li>
   <li><a href="#qcs">Adding Library QCs</a></li>
   <li><a href="#props2">Propagating libraries to dilutions</a></li>
   <li><a href="#boxes">Scanning libraries into your outbox</a></li>
   <li><a href="#pools">Creating Pools</a></li>
   <li><a href="#orders">Ordering sequencing</a></li>
   <li><a href="#trouble">Troubleshooting</a></li>
</ol>
</div>

<div id="infobox">
Download the worksheet for this section here: <a href="3-0-libraries-worksheet">Libraries Worksheet</a>.
</div>


<a name="login"/>

# 1. Logging in

{% include logging_in.md %}

<a name="props1" href="#" id="toplink">top</a>

# 2. Propagating aliquots to libraries

A _library_ is made from one sample for a single target _platform_ and
has a specific _design_ associated with it that decides the _selection_
and _strategies_ used to make the library. A library may also have _indices_
(primers/barcodes/molecular IDs) and QC information.

<img src="pics/flow-library.svg"/>

MISO stores two important pieces of information about how a library was generated:
the _selection_ (e.g., PCR, cDNA) and the _strategy_ (e.g., WGS, WXS,
amplicon). A _design_ captures both a selection and strategy and the list
of allowed designs is limited based on the sample type (_e.g._, a cDNA sample
can only have SM, WT, or MR library designs and these lock the selection and
strategy type accordingly).

## 2.0 Scan aliquots into your inbox

First, we accept the aliquots made by the samples team and put them into your
inbox.

{% include inboxes.md %}


## 2.1 Bulk propagate aliquots into libraries

In this section, you will use the aliquots created already and create
libraries.

1. On the _Samples_ page, enter your project name into the search box.
1. Check the gDNA aliquot samples to turn into libraries. These samples are the
ones that end in `_D_1`:
  - `PROJ_0001_Br_P_nn_1-1_D_1`
  - `PROJ_0001_Ly_R_nn_1-1_D_1`
  - `PROJ_0002_Br_P_nn_1-1_D_1`
  - `PROJ_0002_Ly_R_nn_1-1_D_1`
1. Click the _Propagate_ button at the top left of the table.
1. Choose _1_ replicate.
1. Click _Propagate_.
1. A table will appear. Enter the library information:
  * _Library Name_: Leave blank as this will be filled in automatically after save.
  * _Library Alias_: Leave blank as this will be filled in automatically.
  For more information about Library nomenclature, see
  <a href="https://wiki.oicr.on.ca/display/MCPHERSON/LIMS+Guidelines#LIMSGuidelines-LibraryNomenclature" 
  target="_new">Library Nomenclature</a>.
  * _Matrix Barcode_: As before, usually this would be scanned by the hand
    scanner. In this tutorial, enter matrix barcodes in the form (Short
name)_(Tissue type)(Individual)_Li, e.g. `PROJ_P1_Li`.
  * _Description_: Library (Tissue type)(individual), e.g. `Library P1`
  * _Design_: EX
  * _Platform_: Illumina
  * _Type_: Paired End
  * _Index Kit_: Nextera Dual Index
  * _Index 1_ and _Index 2_: Select any combination of indices you wish.
    Select different indices for each library. Selecting the same index for two
    different libraries will it unwise to pool those two libraries
    together later.
  * _Size (bp)_: 300
  * _Volume_: 100
  * _Kit_: KAPA Hyper Prep
1. Choose _Save_.

Note that for dual-index libraries, only the first index needs to be
specified. The second is optional.

<a name="qcs" href="#" id="toplink">top</a>

# 3. Quality control
There are three way to indicate library quality in MISO: 1)
Enter quantitative QC values under the _Library QC_ section; 2) The overall pre-sequencing quality
flag _QC passed_; and 3) The post-sequencing quality control _Low quality
library_.

## 3.1 Library QC
After measuring the insert size or concentration, this information can be
entered into each library. There is no bulk entry for this information yet, it must
be entered for each library.

1. From the _Libraries_ page, check the `PROJ_0001_Br_P_PE_300_EX` library. 
1. Click the _Edit_ button at the top left of the table.
1. Enter the following (note that the QC date will be the current date):
  1. _New Qubit_: `5.72`
  1. _New TapeStation_: `300`
1. Click _Save_.


## 3.2 QC passed
_QC Passed_ is a simple pass/fail flag for a library to decide if it is good
enough for sequencing. If not measured, this can be left as "Unknown".

1. From the _Libraries_ page, find the `PROJ_0001_Br_P_PE_300_EX` library using
the search box and click the sample link.
1. Change _QC passed_ from _Unknown_ to _True_.
1. Click _Save_.

## 3.3 Low Quality Sequencing
Libraries can be marked as having low sequencing quality, which will be shown
after the _Run_ exercises.

<a name="boxes" href="#" id="toplink">top</a>

# 4. Scanning libraries into your outbox

Scan the libraries you just created into the outbox for the sequencing team to
use.

{% include outboxes.md %}


<a name="props2" href="#" id="toplink">top</a>

# 5. Propagating libraries to dilutions

A library cannot be directly loaded into a _lane_ in a _sequencing container_
(flowcell/SMRTcell) in MISO. A dilution must be made and then many dilutions
(or just one) can be mixed into a _pool_ for sequencing.

_Orders_ are requests for sequencing pools a certain number of times. They are
used to keep track of sequencing progress for project management and book-keeping.

## 5.1 Bulk creating Library Dilutions
Dilutions can be made in bulk from libraries.

<img src="pics/flow-dilution.svg"/>

In this exercise, we will create 4 library dilutions from the libraries we
made previously.

1. On the _Libraries_ page, check all the libraries just created.
  - `PROJ_0001_Br_P_PE_300_EX`
  - `PROJ_0001_Ly_R_PE_300_EX`
  - `PROJ_0002_Br_P_PE_300_EX`
  - `PROJ_0002_Ly_R_PE_300_EX`
1. From the toolbar, select _Make dilutions_.
1. Enter the idilution information:
  * _Conc._: (use any number you wish)
  * _Creation Date_: (use the current date)
1. Click _Save_.


<a name="pools"  href="#" id="toplink">top</a>

# 6. Creating Pools

Pools are the last step for libraries before sequencing and represent the
entity that is loaded onto the flowcell lane or SMRTcell. A "pool" can have one or more
library dilutions in it. Every lane of sequencing contains only one pool. 

<img src="pics/flow-pool.svg"/>

Here we will all all of the dilutions we added previously to make a single pool
of 4 samples.

1. If you are still on the bulk dilutions page from section **5.1**, click the
_Propagate_ button at the top left of the table. Continue to step 2. Otherwise:
  1. On the _Dilutions_ page, select the dilutions created.
  1. From the toolbar, click _Pool Together_.
1. Enter the pool information:
  1. _Alias_: A short description of the pool contents. Enter the project name
followed by `_POOL` (e.g. `PROJ_POOL`)
  1. _Description_: A longer free-text description of the pool.
  1. _Creation Date_: Select a date.
  1. _Concentration_: Enter a concentration.
  1. _Volume_: Enter a pool volume.
  1. _Ready to Run_: Whether or not the pool is ready for sequencing. This flag
     is used together with the Order to show the pool is ready to be sequenced.
     Make sure this is _True_.
1. Click _Save_.

<a name="orders"  href="#" id="toplink">top</a>

# 7. Ordering sequencing

Orders are created on the pool to be sequenced, and include the quantity of sequencing
required (counted in lanes/SMRT cells), and the sequencing chemistry
required (on Illumina).

1. Under _Tracking_, select _Pools_.
1. Find the pool you just created and click on it.
1. On the Edit Pool page, scroll down to the _Orders_ heading.
1. Click _Add Order_:
1. Fill in the new order box:
  - _Partitions_: the number of lanes/cells that should run for this pool. Enter
`2`
  - _Platform_: Select the instrument for sequencing. `Illumina - Illumina HiSeq 2500`
  - _Sequencing Parameters_: Select `v4 2×126` chemistry.
1. Click _Save_. The order will now be visible in the _Orders_ section.

### 7.1  Checking for unfulfilled orders
The _Orders_ page is used to decide what needs to be sequenced.

1. From the navigation menu, choose _Orders_.
1. Verify that the pool you just created is listed in the _Unfulfilled_ tab.

Columns on this page will disappear if there are no entries (_e.g._,
the _Failed_ column will not be shown if there are no failed runs). When enough
lanes have been sequenced, the row will disappear from the _Unfulfilled_ tab,
but remain in the _All_ tab. Lanes currently being sequenced will be marked as
in-progress and remain on the _Unfulfilled_ tab until the run transitions to
_Completed_.

A pool can have many orders. Orders for the same platform and chemistry are
summed when displayed on this page.

<a name="trouble" href="#" id="toplink">top</a>

# Troubleshooting

## How do I correct an index on a library?
The index can be changed on either the individual library page or the bulk edit page.

1. From _Tracking_, _Library_, select the library that needs to be changed.
1. If necessary, change _Index Family_. If selected, the indices will be erased.
1. Select the correct index under _Indices_. If the index family supports dual barcoding, another drop down will appear.

## What if I assign a library to the wrong parent aliquot?
Please email gsi@oicr.on.ca or file a JIRA ticket in GSI Common to get assistance from the MISO team.

## What if I forget to put a library dilution in a pool?
If the library dilution has not been created:

1. From _Tracking_, _Library_, select the library that needs to be added.
1. In the _Library Dilution_ section, hover over _Options_ and select _Add Library Dilution_.
1. Fill out the new row in the table, then click _Add_.

Once the dilution exists:

1. From _Tracking_, _Pool_, select the pool that needs the additional library dilution.
1. In the _Pool Elements_ section, find the second table, labelled _Select poolable elements_.
1. Enter the library name, library alias, or dilution name in the _Search_ box.
1. Find the correct dilution in the list and click the plus button beside it.

## How do I change the targeted sequencing type on a library?
Targeted sequencing is connected to the dilution since the same library can be used for multiple targeted sequencing panels.

1. From _Tracking_, _Library_, select the library that needs to be changed.
1. In the _Library Dilution_ section, under the _Edit_ column, click the pencil beside the dilution that needs to be changed.
1. Select a new _Targeted Sequencing_ from the list.
1. Under the _Edit_ column, click _Save_.

## How can I add a new targeted sequencing type, kit, or anything else in drop-down menus?
For targeted sequencing and indices, please email gsi@oicr.on.ca or file a JIRA ticket in GSI Common to get assistance from the MISO team.

Kits can be added easily:

1. From _Tracking_, _Kits_, select the type of kit you want to add.
1. Click _Create Kit Descriptor_.
1. Fill in the form. The _Stock Level_ is not currently used, so leave it at zero.
1. Carefully select the _Kit Type_ and _Platform_. This will determine what the kit can be used for.
1. Click _Save_.

## How do I make bulk orders?
Alas, this is not possible yet.

## How are matrix tube barcodes assigned to tubes?
Barcodes can be assigned on an individual edit page or in bulk.

To change a single library:

1. From _Tracking_, _Library_, select the library that needs to be changed.
1. In the top right, you will see a box labelled _Barcode_.
1. Hover over the down arrow and select _Update Barcode_.
1. Scan the barcode.
1. Click _Save_.

To change many libraries:

1. From _Tracking_, _Library_, check the box beside each library that needs to be changed.
1. From the toolbar, click _Edit_.
1. Select the cell in the _Matrix Barcode_ column for the library and scan the barcode.
1. Repeat for all the libraries.
1. Click _Save_.

## What is the importance of selecting a study since it prevents the sequencing stage from adding pools to the lane containers?
The study is important for submitting to the ERA. Although we are not using
that feature of MISO, it's required that all projects have at least one study
and that it is required when adding a pool to a lane.

< <a href="2-0-samples">Samples tutorial</a> | <a href="index">Home</a> | <a href="4-0-sequencing">Sequencing tutorial</a> >

