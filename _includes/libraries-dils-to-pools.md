<a name="libraries-dils-to-pools"  href="#" id="toplink">top</a>

# 7. Creating Pools

Pools are the last step for libraries before sequencing and represent the
entity that is loaded onto the flowcell lane or SMRTcell. A "pool" can have one or more
library dilutions in it. Every lane of sequencing contains only one pool.

{% if include.detailed == true %}
<img src="pics/flow-pool.svg"/>
{% else %}
<img src="pics/plain-flow-pool.svg"/>
{% endif %}

## 7.1 Bulk creating a Pool

Here we will pool all of the dilutions we added previously to make a single pool
of 4 dilutions.

1. Select the dilutions you wish to pool:
  * If you are still on the bulk dilutions page from section **5.1** do not navigate away
    from the page. Otherwise, go to the _Dilutions_ page, and select the dilutions you created.
1. From the toolbar at the top left, click _Pool Together_. Click _Create_ in the dialog.
1. Enter the pool information:
  * _Alias_: A short description of the pool contents. Enter the project short name
    followed by `_POOL` (e.g. `PROJ_POOL`)
  * _Description_: A longer free-text description of the pool.
  * _Creation Date_: Select a date.
  * _Concentration_: Enter a concentration.
  * _Conc. Units_: ng/µL
  * _Volume_: Enter a pool volume.
  * _Vol. Units_: µL
1. Click _Save_.
