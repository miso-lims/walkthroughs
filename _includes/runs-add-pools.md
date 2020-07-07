<a name="runs-add-pools" href="#" id="toplink">top</a>

# 6. Adding pools to runs
 
The Run (representing an instrument run) is associated with Pools using a
_Sequencing Container_.

{% if include.detailed == true %}
<img src="pics/flow-cell.svg"/>
{% else %}
<img src="pics/plain-flow-cell.svg"/>
{% endif %}
 
## 6.1 Add a pool to a run
 
1. On the page of the run you created in exercise 4.2, scroll down to the
   _Lanes_ section.
1. Check the first the lane.
1. Click _Assign Pool_ from the toolbar.
1. Search for the pool created by the libraries team that you scanned into
   your inbox in exercise 2.1. Try _Outstanding Orders (Matched Chemistry)_.
1. Click the pool from the list.

Now check on the sequencing order.
 
1. Click on the _Outstanding Sequencing Orders_ page and verify that the _Remaining_ column now
shows 1 for the pool you added to the run.
