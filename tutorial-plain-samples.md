---
layout: page
category: walkthrough
title: Samples Tutorial
is-detailed: false

---

<div id="toc">
Table of Contents
<ol>
    <li><a href="#logging_in">Logging In</a></li>
    <li><a href="#receipt">Receiving Samples</a></li>
    <li><a href="#qcs">Adding Sample QCs</a></li>
    <li><a href="#boxes">Scanning samples into the outbox</a></li>
    <li><a href="#trouble">Troubleshooting</a></li>
</ol>
</div>

<div id="infobox">
Print the worksheet for this section here: <a href="worksheet-plain-samples">Samples Worksheet</a>.
</div>

{% include logging_in.md detailed=page.is-detailed %}

<a name="receipt" href="#" id="toplink">top</a>

# 2. Receiving samples

A _Sample_ contains information about the material upon which the sequencing
experiments are to be based. Samples can be used in any number of sequencing
_Experiments_ in the form of a _Library_ that is processed further into
single or pooled _Library Aliquots._

## 2.1 Receiving a Sample

Samples are entered into MISO using the bulk entry screen.

{% include samples-receiving.md detailed=page.is-detailed %}
    1. _QC Passed?_: `True`
1. At the upper right hand side, click _Save_.

## 2.2 Entering Bulk Samples

Next we will create four more samples.

{% include samples-receiving-bulk.md detailed=page.is-detailed %}

If you navigate back to your _Edit Project_ page, there should now be five samples.

## 2.3 Receipt Transfers

{% include receipt-transfer.md detailed=page.is-detailed items_exercise="2.2" type="sample"
  type_plural="samples" %}


## 2.4 Scanning Samples into a Box

In this section we will add the Samples you just received into your
inbox for further work.

{% include inboxes.md %}

## 2.5 Bulk Editing

Samples can be edited in bulk. Assume that we wish to update the description of the samples.

1. On the _Samples_ page, enter your project name in the search box and press the `Enter` key on your keyboard.
1. Check the boxes for the samples that you created in exercise 2.2.
1. Click the _Edit_ button at the top left of the table.
1. Change the _Description_ value: any value
1. Click _Save_.

<a name="qcs" href="#" id="toplink">top</a>

# 3. Sample QCs

## 3.1 Adding Sample QCs

{% include bulk-qc.md detailed=page.is-detailed items_section="2.2" type="sample" type_plural="samples" %}

<a name="boxes" href="#" id="toplink">top</a>

# 4. Scanning samples into outboxes

{% include outboxes.md %}

<a name="trouble" href="#" id="toplink">top</a>

# Troubleshooting

{% include samples-trouble.md detailed=page.is-detailed %}


< <a href="tutorial-plain-project-coordination">Project Coordination</a> | <a href="index-plain">Home</a> | <a href="tutorial-plain-libraries">Libraries</a> >
