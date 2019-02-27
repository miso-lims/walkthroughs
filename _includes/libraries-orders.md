<a name="libraries-orders"  href="#" id="toplink">top</a>

# 8. Ordering sequencing

Orders are created on the pool to be sequenced, and include the quantity of sequencing
required (counted in lanes/SMRT cells), and the sequencing chemistry
required (on Illumina).

## 8.1 Creating an Order

1. From the navigation menu, select _Pools_.
1. On the  _Pools_ page, select the pool you just created.
1. From the toolbar, click _Create Orders_.
1. Enter the order information:
  - _Instrument Model_: Select the instrument for sequencing: `{{ site.platform }}`.
  - _Sequencing Parameters_: Select `{{ site.seq_params }}` chemistry.
  - _Partitions_: the number of lanes that should run for this pool. Enter `2`.
1. Click _Save_.
1. From the navigation menu, select _Pools_ again.
1. Click on the pool you just added an order to.
1. The order will now be visible in the _Requested Orders_ section.
1. The outstanding sequencing required will be visible under _Order Status_.

The language will vary depending on the platform (_i.e._, PacBio containers
will show _SMRTcell Count_ instead of _Lane Count_).

## 8.2  Checking for unfulfilled orders
The _Active Orders_ page is used to decide what needs to be sequenced.

1. From the navigation menu, choose _Active Orders_.
1. Verify that the pool you just created is listed.

When enough lanes have been sequenced, the row will disappear from the _Active Orders_
page, but remain on the _All Orders_ page. Lanes currently being sequenced will be
marked as in-progress and remain on the _Active Orders_ page until the run transitions
to _Completed_. Columns on the _All Orders_ page will disappear if there are no entries
(e.g., the _Failed_ column will not be shown if there are no failed runs).

A pool can have many orders. Orders for the same platform and chemistry are
summed when displayed on the Order pages.
