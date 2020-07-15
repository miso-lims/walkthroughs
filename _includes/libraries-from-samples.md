## 2.1 Bulk propagate {% if include.detailed == true %}aliquots{% else %}samples{% endif %} into libraries

{% if include.detailed == true %}
In this section, you will use the sample aliquots created already to create libraries.

<img src="pics/flow-aliquot.svg"/>
{% else %}
In this section, you will use the sample created already to create a library.

<img src="pics/plain-flow-aliquot.svg"/>
{% endif %}

1. On the _Samples_ page, enter your project's {% if include.detailed == true %}short{% endif %} name into the search box.
{% if include.detailed == true %}
1. Check the 4 gDNA aliquot samples to turn into libraries. These samples are the
ones that end in `_D_1`.
{% else %}
1. Check the sample to turn into a library.
{% endif %}
1. Click the _Propagate_ button at the top left of the table.
1. Note that "Propagate to Library" is the title of the dialog. Choose _1_ replicate.
1. Click _Propagate_.
1. A table will appear. Enter the library information:
  * _Library Name_: Leave blank as this will be filled in automatically after save.
  * _Library Alias_: Leave blank as this will be filled in automatically.
{% if include.detailed == true %}
        For more information about Library nomenclature, see
        <a href="https://wiki.oicr.on.ca/display/MCPHERSON/LIMS+Guidelines#LIMSGuidelines-LibraryNomenclature" 
        target="_new">Library Nomenclature</a>.
    * _Matrix Barcode_: As before, usually this would be scanned by the hand
      scanner. In this tutorial, enter matrix barcodes in the form
      (Short name)_(Tissue type)(Individual)_Li, e.g. `PROJ_P1_Li`.
    * _Description_: Library (Tissue type)(individual), e.g. `Library P1`
    * _Design_: EX
{% else %}
    * _Description_: Library #, e.g. `Library 1`
{% endif %}
    * _Platform_: Illumina
    * _Type_: Paired End
{% if include.detailed == false %}
    * _Selection_: Select any
    * _Strategy_: Select any
{% endif %}
    * _Index Kit_: Nextera DNA Dual Index
    * _Index 1_ and _Index 2_: Select any combination of indices you wish.
      Select different indices for each library. Selecting the same indices for two
      different libraries would make it unwise to pool those two libraries
      together later.
    * _Kit_: {% if include.detailed == true %}KAPA Hyper Prep{% else %}Any kit{% endif %}
    * _Size (bp)_: 300
{% if include.detailed == true %}
    * _Volume_: 100
    * _Vol. Units_: µL
{% endif %}
1. Choose _Save_. Record the Library aliases and barcodes in your worksheet. <img src="pics/blue_pencil.png">

Note that for dual-index libraries, only the first index needs to be 
specified. The second is optional.
