---
layout: page
category: walkthrough
title: Sequencing tutorial
is-detailed: true

---

<div id="toc">
Table of Contents
<ul>
   <li><a href="#logging_in">1. Logging In</a></li>
   <li><a href="#uorders">2. Checking for sequencing Orders</a></li>
   <li><a href="#runs-new">3. Creating Runs from scratch</a></li>
   <li><a href="#runs-auto">4. Working with automatically created runs</a></li>
   <li><a href="#runs-add-pools">5. Adding Pools to Runs</a></li>
   <li><a href="#runs-qcs">5.1 Mark a library as Low Quality</a></li>
   <li><a href="#boxes">6. Scanning libraries into your outbox</a></li>
   <li><a href="#service-records">7. Adding Service Records to Instruments</a></li>
   <li><a href="#runs-trouble">8. Troubleshooting</a></li>
</ul>
</div>

<div id="infobox">
Download the worksheet for this section here: <a href="4-0-sequencing-worksheet">Sequencing Worksheet</a>.
</div>

{% include logging_in.md detailed=page.is-detailed %}

{% include uorders.md %}


## 2.1 Scan libraries into your inbox

First, scan the libraries from the libraries team into your inbox for further
work.

{% include inboxes.md %}

{% include runs-new.md section=3 flowcell=site.flowcell sequencer=site.sequencer
  platform=site.platform platform_type=site.platform_type seq_params=site.seq_params %}

{% include runs-auto.md %}

{% include runs-add-pools.md %}

{% include runs-qcs.md %}

<a name="boxes" href="#" id="toplink">top</a>

# 6. Scanning libraries/pools into your outbox

Lastly, place the libraries/pools in your outbox for storage.

{% include outboxes.md %}

{% include service-records.md %}

{% include runs-trouble.md %}

< <a href="3-0-libraries">Libraries tutorial</a> | <a href="index">Home</a> >
