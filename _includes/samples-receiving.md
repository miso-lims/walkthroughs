1. On the left hand menu under _Preparation_, click _Samples_.
1. Click the _Create_ button at the top left of the table.
1. Select Sample Class _Tissue_ and Quantity {{ include.quantity }}.
1. Click _Create_.
1. Enter or select the following in the table:
    1. _Sample Name_: leave blank. This will be auto-generated after save.
{% if include.detailed == true %}
    1. _Sample Alias_: leave blank. This will be auto-generated based on other
       information in this form.
    1. _Description_: `Reference 1`.
{% else %}
    1. _Sample Alias_: enter a sample alias like `PRO1_S#_#`. Replace the `#`
       symbol with numbers of your choosing.
    1. _Description_: `Wheat`
{% endif %}
    1. _Date of Receipt_: Select a date
{% if include.detailed == true %}
    1. _Matrix Barcode_: Use the hand-scanner or type a barcode into the pop-up.
       Record the barcode in your worksheet. <img src="pics/blue_pencil.png">
{% endif %}
    1. _Sample Type_: select `GENOMIC` from the drop down.
    1. _Project_: Select the project you created in the last exercise.
    1. _Scientific Name_: {% if include.detailed == true %}`Homo sapiens`{% else %}`Triticum aestivum`{% endif %}.
