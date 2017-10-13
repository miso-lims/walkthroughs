<a name="orders"  href="#" id="toplink">top</a>

# 7. Ordering sequencing

Orders are created on the pool to be sequenced, and include the quantity of sequencing
required (counted in lanes/SMRT cells), and the sequencing chemistry
required (on Illumina).

## 7.1 Creating an Order

1. Select the pools you wish to create orders for:
  * If you are still on the bulk pools page from section **6.1** do not navigate away from the page. Continue to step 2. Otherwise, select pools using the following:
  1. On the  _Pools_ page, select the pool you just created.
1. From the toolbar, click _Create Order_:
1. Select the instrument for sequencing: `NextSeq 550`
1. Fill in the new order box:
  - _Sequencing Parameters_: Select `High 2×151` chemistry.
  - _Lane Count_: the number of lanes that should run for this pool. Enter `2`.
1. Click _Save_.
1. Click on the pool you just added an order to.
1. The order will now be visible in the _Requested Orders_ section.
1. The outstanding sequencing required will be visible under _Order Status_.

The language will vary depending on the platform (_i.e._, PacBio containers
will show _SMRTcell Count_ instead of _Lane Count_).

## 7.2  Checking for unfulfilled orders
The _Orders_ page is used to decide what needs to be sequenced.

1. From the navigation menu, choose _Orders_.
1. Verify that the pool you just created is listed in the _Active_ tab.

Columns on this page will disappear if there are no entries (e.g.,
the _Failed_ column will not be shown if there are no failed runs). When enough
lanes have been sequenced, the row will disappear from the _Active_ tab,
but remain in the _All_ tab. Lanes currently being sequenced will be marked as
in-progress and remain on the _Active_ tab until the run transitions to
_Completed_.

A pool can have many orders. Orders for the same platform and chemistry are
summed when displayed on this page.
