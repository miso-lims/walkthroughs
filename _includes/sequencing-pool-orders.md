<a name="sequencing-pool-orders" href="#" id="toplink">top</a>

# 3. Working with pool orders

To fulfill a pool order, a pool containing all of the specified library aliquots must be linked to
the order. If the pool order specifies sequencing requirements, a sequencing order for the same
pool with matching requirements must also be linked.

From the Edit Pool Order page, you can create a pool containing the required aliquots, or link an
existing pool. If the pool order specifies sequencing requirements, there will also be options to
create or link a sequencing order after a pool is linked.

## 3.1 Creating a pool from a pool order

1. On the _Pool Orders_ page, select the _Outstanding_ tab and click the alias for the pool order
   that was created in the libraries tutorial.
1. At the bottom of the _Order Information_ section, click _Create Pool_.
1. A dialog will appear to confirm the aliquots and proportions of the pool. Click _Yes_ to
   continue.
1. The next dialog allows you to enter pool information. Set the alias to the project short name
   followed by `_POOL_2` (e.g. `PROJ_POOL_2`). Leave the other fields at their default values.
1. Click _Save_. The newly created pool will be linked to the pool order and options to create
   or link a sequencing order will appear.

## 3.2 Creating a sequencing order from a pool order

1. Continuing from the Edit Pool Order page, at the bottom of the _Order Information_ section,
   click the _Create Sequencing Order_ button.
1. In the dialog, enter a description for the sequencing order: `MISO tutorial order`.
1. Click _Save_. The pool order will now be marked as _Fulfilled_ and show that a sequencing order
   is linked.
