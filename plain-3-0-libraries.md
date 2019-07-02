---
layout: page
category: walkthrough
title: Libraries tutorial
is-detailed: false

---

<div id="toc">
Table of Contents
<ol>
   <li><a href="#logging_in">Logging In</a></li>
   <li><a href="#props1">Propagating samples to libraries</a></li>
   <li><a href="#libraries-receipt">Receiving Libraries</a></li>
   <li><a href="#libraries-qc">Adding Library QCs</a></li>
   <li><a href="#boxes">Scanning libraries into your outbox</a></li>
   <li><a href="#libraries-to-library-aliquotss">Propagating libraries to library aliquots</a></li>
   <li><a href="#libraries-library-aliquots-to-pools">Creating Pools</a></li>
   <li><a href="#libraries-orders">Ordering sequencing</a></li>
   <li><a href="#libraries-trouble">Troubleshooting</a></li>
</ol>
</div>

{% include logging_in.md detailed=page.is-detailed %}

<a name="props1" href="#" id="toplink">top</a>

# 2. Propagating samples to libraries

A _library_ is made from one sample for a single target _platform_ and
has a specific _design_ associated with it that decides the _selection_
and _strategies_ used to make the library. A library may also have _indices_
(primers/sequencing barcodes/molecular IDs) and QC information.

## 2.0 Scan samples into your inbox

First, we accept the samples made by the samples team and put them into your
inbox.

{% include inboxes.md %}

{% include libraries-from-samples.md detailed=page.is-detailed %}

{% include libraries-receipt.md detailed=page.is-detailed section=3 %}

{% include libraries-qc.md %}

<a name="boxes" href="#" id="toplink">top</a>

# 5. Scanning libraries into your outbox

{% include outboxes.md %}


{% include libraries-to-library-aliquots.md detailed=page.is-detailed %}


{% include libraries-library-aliquots-to-pools.md detailed=page.is-detailed %}


{% include libraries-orders.md %}


{% include libraries-trouble.md %}


< <a href="plain-2-0-samples">Samples tutorial</a> | <a href="plain-index">Home</a> | <a href="plain-4-0-sequencing">Sequencing tutorial</a> >


