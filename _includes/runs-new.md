<a name="nruns" href="#" id="toplink">top</a>

# 3. Creating runs from scratch

MISO supports runs from Illumina, PacBio, Oxford Nanopore, and other sequencers, so 
the terms used for instrument runs and associated libraries are intentionally 
different from those used by the vendor. A MISO _Run_ represents a sequencing run 
where the sequencer has been loaded and sequencing has begun. The run scanner can be
configured to detect new Illumina and PacBio runs and automatically create
corresponding runs in MISO, while runs for other platforms must be created manually.
A _Sequencing Container_ is the link between the library information and the
instrument Run, and contains one or more lanes. Each Illumina lane, PacBio SMRT 
cell, or Oxford Nanopore flow cell is loaded with exactly one _Pool_.  Runs and
Containers can be associated as soon as the Run and Container have both been created.

## 3.1 Create a Container

1. On the _Sequencing Containers_ page, select the Illumina platform and click the
   _Create Flowcell_ button near the top left of the table.
1. Select _{{ site.flowcell }}_ from the dialog. Only active (non-archived) models are
   available.
1. Enter the name of your project as the serial number.
1. Click _Save_ in the upper right corner of the page.

## 3.2 Create a Run

1. On the _Sequencer Runs_ page, select the Illumina platform and click the 
   _Add Illumina Run_ button near the top left corner of the table.
1. Select _{{ site.sequencer }} ({{ site.platform }})_ from the sequencers list. Only
   active (non-retired) sequencers are available.
1. Enter a unique and memorable _Alias_ for your run.
1. Select _Sequencing Parameters_ `{{ site.seq_params }}`, near the top of the Run
   section.
1. In the _Run Path_ field, enter `path` as the file path to the sequencer output.
1. Check _Paired End_.
1. Select _Status_ `Running`. Note that if MISO does not automatically detect runs
   from this sequencer, all status updates will have to be entered manually.
1. Enter a date into _Start Date_.
1. Click _Save_ in the upper right corner of the page.
1. In the _Flow Cell_ section, click the _Add Flow Cell_ button.
1. Enter the flow cell serial number of the container you have just created and click
   the _Add_ button.

<a name="aruns" href="#" id="toplink">top</a>

# 4. Working with automatically created runs

About five minutes after an instrument begins imaging, MISO will detect it
and create a _Run_. As sequencing continues, MISO will pull back information
about the quality of the run similar to the on-instrument applications like SAV.
This includes statistics like percent pass filter, the percent of bases with
Qscores over 30, and cluster density.

1. From the _Sequencer Runs_ page, find the run assigned to you for this tutorial.
Click on the run alias to go to the run page.
1. Scroll down to the _Metrics_ section and examine the sequencing metrics for
this run.

<a href="pics/metrics.png"><img style="width:100%;" src="pics/metrics.png"/></a>


<a name="pools" href="#" id="toplink">top</a>

# 5. Adding pools to runs

The Run (representing an instrument run) is associated with Pools using a
_Sequencing Container_.

<img src="pics/flow-cell.svg"/>

## 5.1 Add a pool to a run

1. On the page of the Run assigned to you, scroll down to the _Lanes_ section.
1. Check the first the lane.
1. Click _Assign Pool_ from the toolbar.
1. Search for the pool you previously created. Try _Outstanding Orders (Matched Chemistry)_.
1. Click the pool from the list.

Now check on the Order.

1. Click on the _Orders_ page and verify that the _Remaining_ column now
shows 1 for the pool you added to the run.

<a name="lowQuality" href="#" id="toplink">top</a>

## 5.1 Mark a library as Low Quality
Not every library realises its full potential. After sequencing, specific
libraries can be flagged as having low sequencing quality. The
"Low Quality Sequencing" indicator causes any pool containing this library to be
flagged, so that it can be checked before it is sequenced again.

1. From the _Libraries_ page, find one of your libraries
and click the link.
1. Check _Low Quality Sequencing_.
1. Click _Save_.

Now if the Pool containing that Library is added to a Sequencing Container, it
will be flagged.

1. Go back to your Run page.
1. Find your pool using the lanes table. It will be flagged red.

## 5.2 Setting Per-Lane QCs
Sometimes a particular lane is bad. MISO allows setting a per-lane QC. This does 
_not_ prevent analysis. Contact {{ site.miso_admin }} when a lane should not be analysed.

1. Go to your run page.
1. Check the first run.
1. Click _Set QC_ from the toolbar.
1. Pick _Failed: Other problem_.
1. Enter a description of the problem.
1. Click _Set_.

<a name="boxes" href="#" id="toplink">top</a>

# 6. Scanning libraries/pools into your outbox

Lastly, place the libraries/pools in your outbox for storage.

{% include outboxes.md %}


<a name="service" href="#" id="toplink">top</a>

# 7. Adding Service Records to Instruments

Each instrument can have one or more associated service records.

1. Select _Instruments_.
1. Choose an individual instrument.
1. Use the blue arrow to expand the _Service Records_ section.
1. From _Options_, choose _Add Service Record_.
1. Fill in the form as follows:
  * _Title_: a short description of the work (_e.g._, `Remove gremlin from sequencer`)
  * _Description_: a long description of the work (_e.g._, `A gremlin was found outside of the terrible 80s movie. It had developed a taste for polymerase.`)
  * _Serviced By_: your name
  * _Service Date_: the current date
1. Click _Save_.

After saving, it is also possible to attach files to the record. Look under the _Attachments_ heading.
