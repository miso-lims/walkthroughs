<a name="runs-new" href="#" id="toplink">top</a>

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