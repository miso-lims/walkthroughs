<a name="libraries-trouble" href="#" id="toplink">top</a>

# Troubleshooting

## How do I correct an index on a library?
The index can be changed on either the individual library page or the bulk edit page.

1. From the _Libraries_ page, click the name or alias of the library that needs to be changed.
1. If necessary, change _Index Family_. If selected, the indices will be erased.
1. Select the correct index under _Indices_. If the index family supports dual barcoding, another drop down will appear.


## What if I forget to put a library aliquot in a pool?
If the library aliquot has not been created:

1. From the _Libraries_ page, check the library that needs to be added.
1. From the toolbar, click _Make aliquots_.
1. Fill out the new row in the table, then click _Save_.

Once the library aliquot exists:

1. From the _Pools_ page, select the pool that needs the additional library aliquot.
1. In the _Available Library Aliquots_ section, enter the library name, library alias, or library
   aliquot name in the _Search_ box.
1. Find the correct aliquot in the list and check it.
1. Click _Add_ on the toolbar.

## How do I make bulk sequencing orders?
Making sequencing orders in bulk can be done from the _Pools_ page:

1. Select all the pools needing sequencing.
1. Click _Create Orders_ and enter the order information for each pool.

## How do I change the targeted sequencing type on a library?
Targeted sequencing is connected to the library aliquot since the same library can be used for
multiple targeted sequencing panels.

1. From the _Library Aliquots_ page, check the library aliquots that need to be changed.
1. From the toolbar, click _Edit_.
1. Select a new _Targeted Sequencing_ from the list.
1. Click _Save_.

## How can I add a new targeted sequencing type, kit, or anything else in drop-down menus?
For targeted sequencing and indices, please {{ site.miso_admin_contact }} to get assistance from the MISO team.

Kits can be added easily:

1. From the _Kits_ page, located in the _Misc_ menu, select the type of kit you want to add.
1. Click _Add_.
1. Fill in the form. The _Stock Level_ is not currently used, so leave it at zero.
1. Carefully select the _Kit Type_ and _Platform_. This will determine what the kit can be used for.
1. Click _Save_.

## How are matrix tube barcodes assigned to tubes?
Barcodes can be assigned on an individual edit page or in bulk.

To change a single library:

1. From _Libraries_ page, click the name or alias of the library that needs to be changed.
1. Clear the field labelled _Matrix Barcode_.
1. Scan the new barcode.
1. Click _Save_.

To change many libraries:

1. From _Libraries_ page, check the box beside each library that needs to be changed.
1. From the toolbar, click _Edit_.
1. Select the cell in the _Matrix Barcode_ column for the library and scan the barcode.
1. Repeat for all the libraries.
1. Click _Save_.

## How can I delete a library?
Libraries can be deleted from the Libraries list page by selecting the libraries and clicking _Delete_. A
library cannot be deleted if it has any aliquots. Only the library's creator or an admin can delete a library.
Deleted items are listed on the Deletions list page. Deleting a library is permanent and cannot be undone.

## How can I delete a library aliquot?
Library aliquots can be deleted from the Library Aliquots list page by selecting the aliquots and clicking
_Delete_. A library aliquot cannot be deleted if it has been added to any pools. Only the aliquot's creator or
an admin can delete an aliquot. Deleted items are listed on the Deletions list page. Deleting a library aliquot
is permanent and cannot be undone.

## How can I delete a pool?
Pools can be deleted from the Pools list page by selecting the pools and clicking _Delete_. A pool cannot
be deleted if it has been added to any partitions. Any associated sequencing orders will be deleted along with a pool.
Only the pool's creator or an admin can delete a pool. Deleted items are listed on the Deletions list page.
Deleting a pool is permanent and cannot be undone.

## How can I delete a sequencing order?
Sequencing orders can be deleted from the Edit Pool page by selecting the orders and clicking _Delete_. Deleted items
are listed on the Deletions list page.  Deleting a sequencing order is permanent and cannot be undone.
