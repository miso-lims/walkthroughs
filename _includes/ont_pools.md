<a name="pools" href="#" id="toplink">top</a>

# 4. Pooling Libraries

A library cannot be directly loaded into a _flow cell_. A _dilution_ must be made, and
then many dilutions (or just one) can be mixed into a _pool_ for sequencing.

_Orders_ are requests for sequencing pools a certain number of times. They are used to
keep track of sequencing progress for project management and book-keeping.

## 4.1 Creating a Dilution

1. If you are still on the Create Libraries page, click the _Make dilutions_ button in the
toolbar. Otherwise, go to the Libraries page, select the library you created in
the previous exercise, and click the _Make dilutions_ button.
1. Click the _Create_ button in the dialog that pops up.
1. Leave the default values and click _Save_.

## 4.2 Creating a Pool

Here we will create a pool that contains the single dilution that we just created.

1. If you are still on the Create Dilutions from Libraries page, click the _Pool separately_
button in the toolbar. Otherwise, go to the Dilutions page, select the dilution you created
in the previous exercise, and click the _Pool separately_ button.
1. Click the _Create_ button in the dialog that pops up.
1. Enter the pool information:
  * _Volume_: Enter a volume.
1. Leave the remaining fields at their default values and click _Save_.
1. A dialog will pop up, warning you about saving without a barcode. Click _Save_ again.

## 4.3 Creating an Order

1. If you are still on the Create Pools from Dilutions page, click the _Create Orders_
button in the toolbar. Otherwise, go to the Pools page, select the pool you created in the
previous exercise, and click the _Create Orders_ button.
1. Enter the order information:
  * _Platform_: MinION
  * _Sequencing Parameters_: Sequencing Run
  * _Partitions_: 2
1. Click _Save_.
1. Go to the _Active Orders_ page and select the _Oxford Nanopore_ tab. The order you just
created should show up here.

