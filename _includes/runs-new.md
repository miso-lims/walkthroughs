<a name="runs-new" href="#" id="toplink">top</a>

# {{include.section}}. Creating runs from scratch

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

## {{include.section}}.1 Create a Container

1. On the _Sequencing Containers_ page, select the {{include.platform_type}} platform and
   click the _Add Flow Cell_ button near the top left of the table.
1. Select _{{ include.platform }}_ from the dialog.
1. Select _{{ include.flowcell }}_ from the dialog. Only active (non-archived) models are
   available.
1. Enter the name of your project as the serial number.
{% if include.platform_type == 'Oxford Nanopore' %}
1. Select a _Pore Version_.
1. Select a _Received Date_. The _Returned Date_ is the date that the flow cell was returned
to be recycled. This should be left blank for now, and may be filled out later.
{% endif %}
1. Click _Save_ in the upper right corner of the page.

## {{include.section}}.2 Create a Run

1. On the _Sequencer Runs_ page, select the {{ include.platform_type }} platform and click the 
   _Add {{include.platform_type}} Run_ button near the top left corner of the table.
1. Select _{{ include.sequencer }} ({{ include.platform }})_ from the sequencers list. Only
   active (non-retired) sequencers are available.
1. Enter a unique and memorable _Alias_ for your run.
1. Select _Sequencing Parameters_ `{{ include.seq_params }}`, near the top of the Run
   section.
1. In the _Run Path_ field, enter `path` as the file path to the sequencer output.
{% if include.platform_type != 'Oxford Nanopore' %}
1. Check _Paired End_.
{% else %}
1. Enter a _MinKNOW version_.
1. Enter a _Protocol version_.
{% endif %}
1. Select _Status_ `Running`. Note that if MISO does not automatically detect runs
   from this sequencer, all status updates will have to be entered manually.
1. Enter a date into _Start Date_.
1. Click _Save_ in the upper right corner of the page.
1. In the _Flow Cell_ section, click the _Add Flow Cell_ button.
1. Enter the flow cell serial number of the container you have just created and click
   the _Add_ button.
