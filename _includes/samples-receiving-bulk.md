1. On the left hand menu under _Preparation_, click _Samples_.
1. Click the _Create_ button at the top left of the table.
1. Choose {% if include.detailed %}Sample Class _Tissue_ and{% endif %} Quantity _4_.
1. Click _Create_.

A table will appear with the requested number of samples in table format. We
will fill in the first row and use the quick-fill option to fill in the rest of
the table.

1. Select or enter the following data in the **first row only**:
    * _Name_: leave blank. This will be automatically generated after save.
{% if include.detailed %}
    * _Alias_: leave blank. Again, this will be automatically generated from the rest of the table.
{% else %}
    * _Alias_: `{{ site.plain_sample2_alias }}`
{% endif %}
    * _Date of Receipt_: Select today's date.
    * _Time of Receipt_: `9:00 am`
    * _Received From_: Select any lab.
    * _Received By_: Select any group.
    * _Sample Type_: Select `GENOMIC` from the drop-down.
    * _Project_: Select your project's {% if include.detailed %}short{% endif %} name from the drop-down.
{% if include.detailed %}
    * _Subproject_: Select the subproject you created.
{% endif %}
    * _Sci. Name_: Select any item from the dropdown.
{% if include.detailed %}
    * _Donor Sex_: Select any item from the drop-down.
    * _Tissue Origin_: `Br (Breast)`
    * _Tissue Type_: `P (Primary Tumour)`
    * _Times Received_: `1`
    * _Tube Number_: `1`
    * _Secondary ID_: `BioBankID 1`.
    * _Material_: Select any item from the drop down.
    * _QC Status_: `Ready`
{% else %}
    * _QC Passed?_: `True`
{% endif %}

Now we will fill in the rest of the table. Like in Excel, you can fill down a
column by double-clicking the square in the lower right hand corner of a selected
cell. You can also click and drag to only fill in a certain number of cells.

<table border="1"><tr><td>
<img src="pics/fill-down-1.png"/>
</td><td>
<img src="pics/fill-down-2.png"/>
</td></tr></table>

Copy and pasting from Excel and Word is supported. Press Ctrl+V (Windows & Linux) or
Command+V (Mac) on your keyboard to paste into the selected cell(s).

1. Click the _Date of Receipt_ cell in the first row. A blue square will appear at
   the lower right hand corner of the cell. Double click it to fill in the rest of the
   column with the same date.
1. Fill in the columns in the same way for: _Time of Receipt_, _Received From_, _Received By_, _Sample Type_, _Project_,
   _Sci. Name_, {% if include.detailed %} _Subproject_, _Donor Sex_, _Tissue Origin_, _Tissue Type_, _Times Received_,
   _Tube Number_, _Material_, and _QC Status_ {% else %} _QC Passed?_{% endif %}.
1. Copy text from another program and paste it into the _Description_ cell.

1. _Matrix Barcode_: you would normally use a hand-scanner or copy and paste a list of
barcodes from a spreadsheet. For each sample, select a barcode and scan or type it in. If
you were not given barcodes to use, enter the following instead, replacing `PROJ` with your
project's {% if include.detailed %}short{% endif %} name.
    - `PROJ-201`
    - `PROJ-202`
    - `PROJ-203`
    - `PROJ-204`
{% if include.detailed %}
1. _External Name_:  Again, this is the name of the *individual*, whether internal or external.
Here's a suggested list. Replace `PROJ` with your own project short name.
    - `PROJ_ID1`
    - `PROJ_ID2`
    - `PROJ_ID3`
    - `PROJ_ID4`
1. Because you've already created an Identity with the external name `PROJ_ID1`, it is found as a match
to the external name you entered for the top row. In the `Identity Alias` dropdown menu for the first row,
select the existing Identity.
1. Select `First Receipt` from the dropdown menu in each remaining cell of the `Identity Alias` column.
{% endif %}

If you have a label with an incrementing number (_e.g._, `1`, `2`), enter two rows, select them, then double click the
blue square.

{% if include.detailed %}
1. _Secondary ID_: enter `BioBankID 2` in the second row. Select the _Secondary Identifier_ fields for rows 1 and 2,
   then double click the blue square to fill down rows 3 and 4.
{% else %}
1. _Alias_: enter `{{ site.plain_sample3_alias }}` in the second row. Select the _Alias_ fields for rows 1 and 2, then
   double-click the blue square to fill down rows 3 and 4.
{% endif %}
1. Click _Save_ at the upper right hand corner.


If everything is correct, the {% if include.detailed %} _Sample Alias_ and {% endif %} _Sample Name_ will be
auto-generated for each row and the samples will be saved.

Record the {% if include.detailed %}external name, sample class, alias,{% else %}alias{% endif %} and barcode of each
sample in your worksheet. <img src="pics/blue_pencil.png">
