---
layout: page
category: walkthrough
title: Libraries tutorial
is-detailed: true

---

<div id="toc">
Table of Contents
<ol>
   <li><a href="#logging_in">Logging In</a></li>
   <li><a href="#props1">Propagating aliquots to libraries</a></li>
   <li><a href="#libraries-receipt">Receiving Libraries</a></li>
   <li><a href="#libraries-qc">Adding Library QCs</a></li>
   <li><a href="#props2">Propagating libraries to dilutions</a></li>
   <li><a href="#boxes">Scanning libraries into your outbox</a></li>
   <li><a href="#libraries-to-dilutions">Propagating libraries to dilutions</a></li>
   <li><a href="#libraries-dils-to-pools">Creating Pools</a></li>
   <li><a href="#libraries-orders">Ordering sequencing</a></li>
   <li><a href="#libraries-trouble">Troubleshooting</a></li>
</ol>
</div>

<div id="infobox">
Download the worksheet for this section here: <a href="3-0-libraries-worksheet">Libraries Worksheet</a>.
</div>

{% include logging_in.md detailed=page.is-detailed %}

<a name="props1" href="#" id="toplink">top</a>

# 2. Propagating aliquots to libraries

A _library_ is made from one sample for a single target _platform_ and
has a specific _design_ associated with it that decides the _selection_
and _strategies_ used to make the library. A library may also have _indices_
(primers/sequencing barcodes/molecular IDs) and QC information.

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

{% include libraries-from-samples.md detailed=page.is-detailed %}


## 2.2 Bulk propagate aliquots to libraries from Box page

In this section, you will use the aliquots created already and create libraries.
These libraries can be sorted based on the parent sample's location within the box,
and indices can be added based on the box position.

1. On the _Boxes_ page, find your box and click on its link.
1. Select all the aliquots in your box by either control-clicking all the aliquots
in the box (command-click on a Mac). If the aliquots are all in one row or column,
you can click on the row/column header to select all items in that row or column. 
Use control-click (or command-click) to select more than one row or column.
1. Click the _Propagate_ button at the top left of the box contents table. If the 
top left of the box contents table indicates that more than one type of element is
selected, de-select the non-aliquot tubes and then click _Propagate_.
1. Choose _1_ replicate.
1. Click _Propagate_.
1. From the bulk libraries table, you can now sort the libraries you are creating
based on their parent sample's position within the box. Sorting can be done by 
rows (`A01`, `A02`, `B01`, `B02`, ...) or columns (`A01`, `B01`, `A02`, `B02`, ...).
  * This may be useful when using the Sciclone robot to create libraries and add 
indices at a particular plate location. Once the libraries are sorted based on the
parent sample's location, the indices can be copy-pasted in the order that the 
robot requires.

{% include libraries-receipt.md detailed=page.is-detailed section=3
  platform='Illumina' type='Paired End' kit='any option' %}

{% include libraries-qc.md %}

<a name="boxes" href="#" id="toplink">top</a>

# 5. Scanning libraries into your outbox

Scan the libraries you just created into the outbox for the sequencing team to
use.

{% include outboxes.md %}


{% include libraries-to-dilutions.md detailed=page.is-detailed %}


{% include libraries-dils-to-pools.md detailed=page.is-detailed %}


{% include libraries-orders.md %}


{% include libraries-trouble.md %}

## What if I assign a library to the wrong parent aliquot?
You can delete the library and re-create it. If this is not appropriate because the
library is already included in a sequencer run, please {{ site.miso_admin_contact }}
to get assistance from the MISO team.


< <a href="2-0-samples">Samples tutorial</a> | <a href="index">Home</a> | <a href="4-0-sequencing">Sequencing tutorial</a> >

