<a name="libraries-library-aliquots-to-pools"  href="#" id="toplink">top</a>

# 8. Creating Pools

Pools are the last step for libraries before sequencing and represent the
entity that is loaded onto the flowcell lane or SMRTcell. A "pool" can have one or more
library aliquots in it. Every lane of sequencing contains only one pool.

{% if include.detailed == true %}
<img src="pics/flow-pool.svg"/>
{% else %}
<img src="pics/plain-flow-pool.svg"/>
{% endif %}

## 8.1 Bulk creating a Pool

Here we will pool all of the aliquots we added previously to make a single pool
of 4 aliquots.

1. On the _Library Aliquots_ page, check the four library aliquots you created.
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
1. Click _Save_. Record the Pool alias in your worksheet. <img src="pics/blue_pencil.png">
