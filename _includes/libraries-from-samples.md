## 2.1 Bulk propagate {% if include.detailed == true %}aliquots{% else %}samples{% endif %} into libraries

{% if include.detailed == true %}
In this section, you will use the sample aliquots created already to create libraries.

<img src="pics/flow-aliquot.svg"/>
{% else %}
In this section, you will use the samples created already to create libraries.

<img src="pics/plain-flow-aliquot.svg"/>
{% endif %}

1. On the _Samples_ page, enter your project's {% if include.detailed %}short{% endif %} name into the search
   box and press the `Enter` key on your keyboard.
{% if include.detailed %}
1. Check the 4 {{ site.aliquot_class }} samples created previously.
{% else %}
1. Check the 5 samples created previously.
{% endif %}
1. Click the _Propagate_ button at the top left of the table.
1. In the dialog that appears, choose `1` replicate. If necessary, choose to propagate to `Library`.
1. Click _Propagate_.
1. A table will appear. Enter the library information:
    * _Library Name_: Leave blank as this will be filled in automatically after save.
    * _Library Alias_: Leave blank as this will be filled in automatically.
    * _Matrix Barcode_: As before, usually this would be scanned by the hand scanner. In this tutorial, enter matrix
      barcodes in the form `(project {% if include.detailed %}short{% endif %} name)_(row number)_lib`, e.g.
      `PROJ_1_lib`.
    * _SOP_: Choose any value if required.
    * _Thermal Cycler_: Choose any value if required.
{% if include.detailed == true %}
    * _Design_: Select any
{% endif %}
    * _Platform_: `{{ site.platform_type }}`
    * _Type_: `{{ site.library_type }}`
{% if include.detailed == false %}
    * _Selection_: Select any
    * _Strategy_: Select any
{% endif %}
    * _Index Kit_: `{{ site.index_kit }}`
    * _Index 1_ and _Index 2_ (if available): Select any combination of indices
      you wish. Select different indices for each library. Selecting the same
      indices for two different libraries would make it unwise to pool those two
      libraries together later.
    * _Kit_: Select any
    * _Kit Lot_: Enter today's date, e.g. `2021-06-15`
    * _QC Status_: `{{ site.detailed_qc_status_pending }}`
    * _Size (bp)_: `300`
{% if include.detailed == true %}
    * _Volume_: `100`
    * _Vol. Units_: `µL`
{% endif %}
1. Choose _Save_. Record the Library aliases and barcodes in your worksheet.
   <img src="pics/blue_pencil.png">

Note that for dual-index libraries, only the first index needs to be
specified. The second is optional.
