<a name="uorders" href="#" id="toplink">top</a>

# 2. Checking for unfulfilled orders

There are two types of orders in MISO - pool orders, and sequencing orders.

Pool orders indicate that a set of library aliquots are ready to be pooled and sequenced. Click
_Pool Orders_ in the navigation menu to view pool orders in MISO. This page is divided into three
tabs:

* _Outstanding_: shows pool orders that require work
* _Fulfilled_: shows pool orders that have been completed
* _Draft_: shows pool orders that are not yet finalized

In addition to pooling requirements, a pool order may specify sequencing requirements. Fulfilling a
pool order requires linking a pool to it, as well as a sequencing order if sequencing requirements
are specified. Thus, a pool order can become a sequencing order.

Sequencing Orders indicate that a pool is ready to be sequenced. The _Outstanding Sequencing
Orders_ page is used to decide what needs to be sequenced.

Columns on this page will disappear if there are no entries (_e.g._,
the _Failed_ column will not be shown if there are no failed runs). When enough
lanes have been sequenced, the row will disappear from the _Outstanding Sequencing Orders_ page,
but remain in the _All Sequencing Orders_ page. Lanes currently being sequenced will be marked as
in-progress and remain on the _Outstanding_ page until the run transitions to _Completed_.

A pool can have many sequencing orders. Orders for the same platform and chemistry are
summed when displayed on this page.
