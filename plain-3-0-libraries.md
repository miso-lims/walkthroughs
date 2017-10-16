---
layout: page
category: walkthrough
title: Libraries tutorial
is-detailed: false
section: **2.1**
miso-url: YOUR MISO SITE ADDRESS

---

<div id="toc">
Table of Contents
<ol>
   <li><a href="#login">Logging In</a></li>
   <li><a href="#props1">Propagating samples to libraries</a></li>
   <li><a href="#qcs">Adding Library QCs</a></li>
   <li><a href="#props2">Propagating libraries to dilutions</a></li>
   <li><a href="#boxes">Scanning libraries into your outbox</a></li>
   <li><a href="#pools">Creating Pools</a></li>
   <li><a href="#orders">Ordering sequencing</a></li>
   <li><a href="#trouble">Troubleshooting</a></li>
</ol>
</div>

<a name="login"/>

# 1. Logging in

{% include logging_in.md detailed=page.is-detailed misoUrl=page.miso-url %}

<a name="props1" href="#" id="toplink">top</a>

# 2. Propagating samples to libraries

A _library_ is made from one sample for a single target _platform_ and
has a specific _design_ associated with it that decides the _selection_
and _strategies_ used to make the library. A library may also have _indices_
(primers/sequencing barcodes/molecular IDs) and QC information.
can aliquots into your inbox

## 2.0 Scan samples into your inbox

First, we accept the samples made by the samples team and put them into your
inbox.

{% include inboxes.md %}

{% include libraries-from-samples.md detailed=page.is-detailed %}

{% include libraries-qc.md detailed=page.is-detailed section=page.section %}

<a name="boxes" href="#" id="toplink">top</a>

# 4. Scanning libraries into your outbox

Scan the libraries you just created into the outbox for the sequencing team to
use.

{% include outboxes.md %}


{% include libraries-to-dilutions.md detailed=page.is-detailed %}


{% include libraries-dils-to-pools.md %}


{% include libraries-orders.md %}


{% include libraries-trouble.md %}


< <a href="plain-2-0-samples">Samples tutorial</a> | <a href="plain-index">Home</a> | <a href="plain-4-0-sequencing">Sequencing tutorial</a> >


