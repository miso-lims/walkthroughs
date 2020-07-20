1. On the left hand menu under _Preparation_, click _Samples_.
1. Click the _Create_ button at the top left of the table.
1. Select {% if include.detailed == true %}Sample Class _Tissue_ and{% endif %} Quantity {{ include.quantity }}.
1. Click _Create_.
1. Enter or select the following in the table:
    1. _Sample Name_: leave blank. This will be auto-generated after save.
{% if include.detailed == true %}
    1. _Sample Alias_: leave blank. This will be auto-generated based on other
       information in this form.
    1. _Description_: `Reference 1`.
{% else %}
    1. _Sample Alias_: enter a sample alias like `{{ site.plain_sample1_alias }}`. Replace `PRO1` with
       your project's name, and replace the `#` symbol with numbers of your
       choosing. Record the alias on your worksheet. <img src="pics/blue_pencil.png">
    1. _Description_: `Wheat`
{% endif %}
    1. _Date of Receipt_: Select a date
    1. _Received From_: Select any lab
    1. _Received By_: Select any group. If there are no options in the dropdown,
       ask your MISO administrator to add you to an appropriate group.
    1. _Matrix Barcode_: Use the hand-scanner or type a barcode into the pop-up.
       If you weren't given any barcodes to use, enter one like `PROJ-101`,
       replacing `PROJ` with your project's {% if include.detailed == true %}short{% endif %}
       name. Record the barcode on your worksheet. <img src="pics/blue_pencil.png">
    1. _Sample Type_: select `GENOMIC` from the drop down.
    1. _Project_: Select the {% if include.detailed == true %}short{% endif %}
       name of the project you created in the last exercise.
{% if include.detailed == true %}
    1. _Subproject_: Select the subproject you created. If the subproject does not
       appear in the dropdown, you may need to refresh the page and re-enter the above
       information. It can sometimes take a few minutes for the new subproject option
       to become available.
{% endif %}
    1. _Scientific Name_: Select any option from the dropdown.
