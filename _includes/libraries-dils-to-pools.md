<a name="pools"  href="#" id="toplink">top</a>

# 6. Creating Pools

Pools are the last step for libraries before sequencing and represent the
entity that is loaded onto the flowcell lane or SMRTcell. A "pool" can have one or more
library dilutions in it. Every lane of sequencing contains only one pool.

{% if detailed == true %}
<img src="pics/flow-pool.svg"/>
{% else %}
<img src="pics/plain-flow-pool.svg"/>
{% endif %}

## 6.1 Bulk creating a Pool

Here we will pool all of the dilutions we added previously to make a single pool
of 4 dilutions.

1. Select the dilutions you wish to pool:
  * If you are still on the bulk dilutions page from section **5.1** do not navigate away from the page. Continue to step 2. Otherwise, select dilutions using the following:
  1. On the _Dilutions_ page, select the dilutions created.
1. From the toolbar at the top left, click _Pool Together_.
1. Enter the pool information:
  * _Alias_: A short description of the pool contents. Enter the project name
followed by `_POOL` (e.g. `PROJ_POOL`)
  * _Description_: A longer free-text description of the pool.
  * _Creation Date_: Select a date.
  * _Concentration_: Enter a concentration.
  * _Volume_: Enter a pool volume.
  * _Ready to Run_: Whether or not the pool is ready for sequencing. This flag
     is used together with the Order to show the pool is ready to be sequenced.
     Make sure this is _True_.
1. Click _Save_.
