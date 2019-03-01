<a name="box-data" href="#">top</a>

# 2. Creating Some Test Data

We are going to need some items to play with, so we will create a few pools:

1. Go to the _Dilutions_ page.
1. Select any five dilutions from the list.
1. Click _Pool Separately_ in the toolbar. Click _Create_ in the dialog.
1. Enter the following attributes for the pools. Replace 'XX' with your own initials:
    
    | Alias | Matrix Barcode | Volume | Vol. Units |
    | XX_POOL_1 | XX_A01 | 5 | µL |
    | XX_POOL_2 | XX_A02 | 5 | µL |
    | XX_POOL_3 | XX_A03 | 5 | µL |
    | XX_POOL_4 | XX_A04 | 5 | µL |
    | XX_POOL_5 | XX_A05 | 5 | µL |
    
1. Click _Save_ at the top right.

<a name="box-new" href="#">top</a>

# 3. Create a Box

Create a box to use for the rest of this walkthrough:

1. Go to the _Boxes_ page.
1. Click _Add_ in the toolbar. In the dialog, set _Quantity_ to `1` and click _Create_.
1. Fill out the box information as follows.
    * _Alias_: `XX Test Box` (replace `XX` with your own initials)
    * _Box Use_: Sequencing
    * _Box Size_: 8 x 12 scannable
1. Click _Save_ at the top right.

<a name="box-selecting" href="#">top</a>

# 4. Selecting Positions

<img src="pics/box-selecting.png" id="figure">

1. On the Edit Box page, scroll down to the Contents section. You will see a diagram
   containing many circles. Each circle represents a position in the box. These are
   labelled with row letters and column numbers.
1. Hover your mouse over one of the circles. It will display a tooltip showing the
   position name and what it contains. e.g. "B03: EMPTY"
1. Click on any of the circles. It will be highlighted to indicate that it is selected.
   Additional controls for manipulating this position will appear on the page.
1. Hold the Ctrl key on your keyboard (or Command on a Mac) and click another position.
   Now two positions are selected, and the additional controls will change to reflect
   this.
1. Click one of the row labels - the letters on the left of the diagram. The entire
   row will be selected.
1. Hold the Ctrl/Command key on your keyboard and click another row label. Now both
   rows are selected.
1. Click one of the column labels - the numbers at the top of the diagram. The entire
   column will be selected.
1. Below the diagram, click the _Select All_ button. All positions will be selected.
1. click the _Select Odd Columns_ button. Columns 1, 3, 5, 7, 9, and 11 will be selected.
   This (and the _Select Even Columns_ option) can be especially useful when a robot is
   working on your samples and may do something such as creating libraries in the
   even-numbered columns from samples in the odd-numbered columns.

<a name="box-add-single" href="#">top</a>

# 5. Adding individual items

1. Select any single empty position in your box.
1. In the _Search_ box, type the barcode of your first pool - `XX-A01` and click _Lookup_.
1. The name and alias of the pool will appear in the _Results_ dropdown. Click _Update
   Position_ to confirm and save the pool in the selected box position. The diagram is
   updated to show the selected position filled.

<a name="box-replace-single" href="#">top</a>

# 6. Replacing items

You can add an item to a position that already has an item. this will cause the existing
item to be replaced. The existing item is removed from the box and its location is then
unknown.

1. Select the position where you have already added your pool.
1. In the _Search_ box, type the barcode of your last pool - `XX-A05` and click _Lookup_.
1. The name and alias of the pool will appear in the _Results_ dropdown. Click _Update
   Position_.
1. A dialog will warn you about replacing the current item. Click _Replace_.

<a name="box-add-multiple" href="#">top</a>

# 7. Adding multiple items

1. Select any single empty position in your box.
1. Hold the Ctrl/Command key and click 3 more empty positions. You should now have 4
   positions selected.
1. In the _Position Search_ list, fill in the barcodes for your remaining pools -
   `XX-A01`, `XX-A02`, `XX-A03`, and `XX-A04`
1. Click _Update_. The diagram is updated to show the new pools you've added.

<a name="box-remove-single" href="#">top</a>

# 8. Removing an item

1. Select any single position containing one of your pools.
1. Click the _Remove Item_ button. A warning appears, telling you that the item's
   position will be unknown. Click _Remove_ to confirm.

<a name="box-remove-multiple" href="#">top</a>

# 9. Removing multiple items

1. Select the rest of the positions you've added pools to.
1. Click the _Remove Selected_ button. Click _Remove_ again in the warning dialog.
   The box should now be empty.

<a name="box-fill-pattern" href="#">top</a>

# 10. Filling the box by barcode pattern

The "Fill by Barcode Pattern" feature allows you to assign barcodes which indicate the
box position that items should be stored in. In most cases, these will not be real
barcodes, but will be fake ones assigned just for this purpose. This may be useful when
creating items that are stored in plates, which will not usually have a barcode for
each position.

1. Ensure that your box is empty. If there are any items remaining in it, remove them
   as detailed in the previous exercise.
1. From the _Options_ menu in the _Contents_ bar, click _Fill by Barcode Pattern_.
1. In the dialog, enter _Prefix_ `XX_`, replacing `XX` with your own initials.
1. Select Standard suffixes. This means that the barcode pattern contains the name of
   the position where the item should be stored. e.g. the item with barcode `XX_A01`
   should be stored in position `A01`.
1. Click _Fill_. Your pools are all added to the box in the positions specified in
   their barcodes.

<a name="box-export" href="#">top</a>

# 11. Exporting to Excel

You can easily export a spreadsheet detailing a box and its contents:

1. From the _Options_ menu in the _Contents_ bar, select _Export Box to Excel_.
1. Open the downloaded file. It contains some box information at the top, followed by
   information about its contents below.
1. Close the spreadsheet when you are done having a look.

<a name="box-discard-single" href="#">top</a>

# 12. Discarding an item

When you discard an item in MISO, several things happen:

* the item is removed from its box
* the item's volume is set to 0
* the item is marked as discarded

You can discard items from the Edit Box page:

1. In the _Contents_ diagram, select the item stored in position A01.
1. Right-click on the item's name or alias and choose _Open Link in New Tab_.
1. Select the new tab and note the Pool's volume. Note also that the discarded checkbox
   is not checked.
1. Return to the other tab and click _Discard Item_. In the dialog, click _Discard_
   again to confirm. The item is removed from the box.
1. Return again to the other tab and refresh the page. The pool's volume is now set to 0
   and it is marked as discarded.

<a name="box-discard-multiple" href="#">top</a>

# 13. Discarding multiple items

1. In the _Contents_ diagram, select the items in positions A02 and A03.
1. Click _Discard Selected_. In the dialog, click _Discard_ again to confirm. Both
   items are discarded at once and disappear from the box.

<a name="box-discard-all" href="#">top</a>

# 14. Discarding all items

To discard all remaining items in the box:

1. From the _Options_ menu in the _Contents_ bar, select _Discard All Contents_. In the
   dialog, click _Discard_ to confirm. All remaining items are discarded at once and
   disappear from the box.

