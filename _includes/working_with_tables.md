<a name="quick-help"/>

# 2. Quick Help

The Quick Help section at the top of the bulk tables page contains instructions for how to interact with multiple table cells at once.

1. In the _Preparation_ menu on the left sidebar, click on **Libraries**.
1. At the top left of the _Libraries_ table, click **Receive**.
1. In the dialog box, enter:{% if include.detailed == true %}
    * Aliquot Class: Select any option.{% endif %}
    * Quantity: **5**
1. Click **Receive**.
1. Click the **Quick Help** header at the top right of the page, under the save button.
    * To close the Quick Help section, click again on the **Quick Help** header.

<a name="copy-paste"/>

# 3. Copy & Paste

If you have a spreadsheet that already has the sample information and you need to enter this into MISO, copy-pasting is often the fastest way to do this.

1. Open the _Quick Help_. Note which key combination your current computer uses to paste.
1. Copy the items from the table below (do not copy the "Sample Type" cell).
1. Click in the first row of the _Sample Type_ column, and use the key combination to paste.

| Sample Type |
|-------------|
|GENOMIC|
|GENOMIC|
|GENOMIC|
|GENOMIC|
|GENOMIC|

<a name="fill-many"/>

# 4. Fill Many

Entering the same data in all rows can be done by using the fill handle. The fill handle is the square that appears at the bottom right corner of the cell you have selected. Enter the data in one cell, then you can fill in multiple cells by:
  * double-clicking the fill handle to fill in all cells below.
  * clicking the fill handle and dragging the mouse up or down through other cells to fill those cells with the initial value.

<a name="fill-down-drag"/>

## 4.1 Fill Many: Drag (fills up or down)

1. Select a project from the dropdown in the _last_ row of the _Project_ column.
    * The cell will have a blue border with a blue square (the fill handle) in the bottom right corner. If you do not
      see the fill handle, click on another cell and then click again on the project cell.
1. Click on the fill handle and hold the mouse button down as you drag up to the top row in the _Project_ column.
   Release the mouse button.
    * The cells will all change to the same project.

<a name="fill-down-click"/>

## 4.2 Fill Many: Double-click (fills down)

1. Clear all of the cells in the _Project_ column by clicking each cell and clicking the **Delete** key on your
   keyboard.
1. Select any project from the dropdown in the _first_ row of the _Project_ column.
    * The cell will have a blue border with a blue square (the fill handle) in the bottom right corner. If you do not
      see the fill handle, click on another cell and then click again on the project cell.
1. Double-click on the fill handle.
    * The cells below it will all change to the same project.

*Note*: multiple columns can be filled down at once.
{% if include.detailed == true %}
You can test this out:
1. Fill in values in the top row for the _Tissue Origin_, _Tissue Type_, _Times Received_, and _Tube Number_ columns.
1. Click the _Tissue Origin_ cell, then press **Shift**, click the _Tube Number_ cell, and release the Shift key.
    * All the cells between _Tissue Origin_ and _Tube Number_ will be selected.
1. Double-click or drag down on the blue square in the bottom right corner of the _Tube Number_ cell.
    * All the cells in all the selected columns will change to contain the values from the first row.
{% endif %}

<a name="fill-down-incrementing"/>

## 4.3 Fill Many: Incrementing (fill down)

If the values in a column need to each be one greater than the value in the row before it, you can fill the column using the incremental fill down.

1. In the first two rows of the _Matrix Barcode_ column, enter the following (substituting _XX_ for your initials):

    |Matrix Barcode|
    |-------------|
    |TEST_XX01|
    |TEST_XX02|

1. In the _Matrix Barcode_ column, click the cell in the first row, then press **Shift**, click the cell in the second row, and release both the mouse button and the Shift key.
    * The top two cells will be surrounded by a border, with the fill handle in the bottom right corner of the lower cell.
1. Double-click on the fill handle, and the cells below will be filled in with an incrementing pattern: 1-2-3-4-5.
    * A copied pattern of 1-2-1-2-1 may briefly be seen, but will be overridden by the incrementing pattern.


# Table Actions

<a name="fill-by-row-column"/>

# 5. Fill Boxes by Row or Column

Samples, libraries, library aliquots, or pools can be bulk-added to a box from within the bulk tables pages. Selecting the **Fill Boxes by Row** option adds the tubes in the displayed order, going from left to right, and top to bottom (see Figure 1). Selecting the **Fill Boxes by Column** option adds the tubes in the displayed order from top to bottom, and left to right (see Figure 2).

<table border="1">
<tr>
<td><img src="pics/by-row.png" alt="Arrows on a box showing the Fill by Row pattern"/></td>
<td><img src="pics/by-column.png" alt="Arrows on a box showing the Fill by Column pattern"/></td>
</tr>
<tr>
<td>Figure 1: The Fill Boxes by Row pattern</td>
<td>Figure 2: The Fill Boxes by Column pattern</td>
</tr>
</table>

1. Return to your _Create Libraries_ bulk table.
1. In the top row of the _Box Search_ column, enter the alias of the box you created in the Working with Boxes tutorial
   (it should be `XX Test Box`, with `XX` being your initials).
   Once the top row of the _Box Alias_ column displays a box alias value, [fill down](#fill-down-drag) the _Box Alias_
   column.
1. Click **Fill Boxes by Row**.
    * The _Position_ column will be filled in. Note the pattern of the positions.
1. Delete the value in the top row of the _Position_ column. Fill down the rest of the _Position_ column so that all cells are empty.
1. Click **Fill Boxes by Column**.
    * The _Position_ column values will change. Note the new pattern of the positions.

<a name="check-qcs"/>

# 6. Check QCs (Libraries only)

The _Check QCs_ feature can be used to automatically update the _QC Passed?_ column values based on the values in the _Size (bp)_, _Volume_, or _Conc._ columns.

1. Return to your _Create Libraries_ bulk table.
1. Ensure all _QC Passed?_ cells are set to **Unknown**.
1. In the top row, enter the following values:
    * _Size (bp)_: **300**
    * _Volume_: **10**
    * _Conc._: **2**
1. In the second row, enter the following values:
    * _Size (bp)_: **301**
    * _Volume_: **11**
    * _Conc._: **3**
1. Use the [incrementing fill](#fill-down-incrementing) to fill in the _Size (bp)_, _Volume_, and _Conc._ columns.
    * Note that the _Vol. Units_ column does not contain numbers and so cannot be incrementally filled down.
1. Click **Check QCs**.
1. In the _Size_ section, select **=** from the dropdown menu and enter **303** into the input field.
1. Leave the _Volume_ and _Concentration_ sections set to **ignore**.
1. Click **Check**.
    * Note that the _QC Passed?_ values have changed.
1. Click **Check QCs**.
1. In the _Volume_ section, select **>** from the dropdown menu and enter **10** into the input field.
1. In the _Concentration_ section, select **<=** from the dropdown menu and enter **4** into the input field.
1. Leave the _Size_ section set to **ignore**.
1. Click **Check**.
    * Note that the _QC Passed?_ values have changed.

<a name="export"/>

# 7. Export

The current state of the bulk table data can be exported at any time. Exports can be saved as Microsoft Excel, Open Document Format, or Comma-delimited Data (CSV) files.

1. Return to your _Create Libraries_ bulk table.
1. Click **Export Data** at the top of the table.
1. Select **Microsoft Excel** format.
1. Click **Export**.
    * The spreadsheet will begin downloading.

<a name="import"/>

# 8. Import

A spreadsheet can be uploaded to a bulk table page, and any matching data from the spreadsheet will be entered in the table.
  * In order to match, the spreadsheet column header must exactly match the bulk table column header.
  * Spreadsheet upload will fail if:
      * the spreadsheet contains columns whose headers don't match any headers in the bulk table
      * the spreadsheet contains more rows than the bulk table does
  * If the spreadsheet cells contain invalid data, the data will still be entered in the table.
  * If the spreadsheet contains fewer columns than the table does, the table data for columns not in the spreadsheet will remain unchanged.

1. Open the spreadsheet you downloaded in the [Export](#export) section.
1. Delete all columns to the right of the _Sci. Name_ column.
1. Enter text into some or all of the remaining cells.
1. Save the spreadsheet.
1. Return to your _Create Libraries_ bulk table.
1. Click **Import**.
1. Choose the spreadsheet you edited, and click **Import**.
    * The cell values of the columns from the spreadsheet will change.
    * The cell values of the columns not present in the spreadsheet will be unaffected by the import.

# Miscellaneous

<a name="cell-colours"/>

# 9. Cell Colours

Some of the cells in a table can have different colours, each of which indicates a specific meaning:
  * Red: cell needs to be filled with valid data (empty cell is invalid).{% if include.detailed == true %}
  * Yellow (_Sample/Library Alias_ only): this alias is non-standard, and whatever is entered here will be saved
    (validation will be skipped).
  * Purple (_Identity Alias_ only): This cell is automatically filled in, but there are other items in the dropdown that
    you may wish to select instead.{% endif %}

<a name="read-only"/>

# 10. Read-Only Cells

Read-only cells cannot be edited directly. They contain lighter text than cells you can interact
with. For instance, the _Sample Class_ cells will be read-only. The _Sample Name_, _Library Name_,
_Library Aliquot Name_, and _Pool Name_ columns will all be automatically filled in after the item
is created.

Sometimes, a read-only cell becomes editable once another cell has been changed.
1. Return to your _Create Libraries_ bulk table.
1. Click the dropdown arrow in the _Index 1_ column for row 1.
    * Nothing happens, as this cell is read-only.
1. Select the following options in row 1:
    * _Platform_: `{{ site.platform_type }}`
    * _Index Kit_: `{{ site.index_kit }}`
1. Click the dropdown arrow in the _Index 1_ column for row 1 again.
    * The cell is no longer read-only, so the dropdown opens and there are options to choose from.

<a name="dependent-cells"/>

# 11. Dependent Cells

Some cells change (dropdown items, required vs optional, read-only vs editable) according to the value of other cells. For instance, on the bulk _Create Libraries_ and _Edit Libraries_ pages:{% if include.detailed == true %}
  * Selecting a _Template_ (if available) will lock in values for some or all of _Design_, _Code_, _Platform_, _Type_, _Index Kit_, and _Kit_.
  * Selecting a _Design_ will lock in values for some or all of _Code_, _Selection_, _Strategy_. {% endif %}
  * Changing _Platform_ will affect the dropdown items for _Type_, _Index Kit_, and _Kit_.
  * Changing _Index Kit_ will affect the dropdown items for _Index 1_ and _Index 2_.
