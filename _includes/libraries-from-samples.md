## 2.1 Bulk propagate {% if detailed == true %}aliquots{% else %}samples{% endif %} into libraries

In this section, you will use the {% if detailed == true %}aliquots{% else %}samples{% endif %} 
created already to create libraries.

{% if detailed == true %}
<img src="pics/flow-aliquot.svg"/>
{% else %}
<img src="pics/plain-flow-aliquot.svg"/>
{% endif %}

1. On the _Samples_ page, enter your project name into the search box.
{% if detailed == true %}
1. Check the gDNA aliquot samples to turn into libraries. These samples are the
ones that end in `_D_1`:
  - `PROJ_0001_Br_P_nn_1-1_D_1`
  - `PROJ_0001_Ly_R_nn_1-1_D_1`
  - `PROJ_0002_Br_P_nn_1-1_D_1`
  - `PROJ_0002_Ly_R_nn_1-1_D_1`
{% else %}
1. Check the samples to turn into libraries.
{% endif %}
1. Click the _Propagate_ button at the top left of the table.
1. Note that "Propagate to libraries" is the title of the box. Choose _1_ replicate.
1. Click _Propagate_.
1. A table will appear. Enter the library information:
  * _Library Name_: Leave blank as this will be filled in automatically after save.
  * _Library Alias_: Leave blank as this will be filled in automatically.
{% if detailed == true %}
  For more information about Library nomenclature, see
  <a href="https://wiki.oicr.on.ca/display/MCPHERSON/LIMS+Guidelines#LIMSGuidelines-LibraryNomenclature" 
  target="_new">Library Nomenclature</a>.
  * _Matrix Barcode_: As before, usually this would be scanned by the hand
    scanner. In this tutorial, enter matrix barcodes in the form (Short
name)_(Tissue type)(Individual)_Li, e.g. `PROJ_P1_Li`.
  * _Description_: Library (Tissue type)(individual), e.g. `Library P1`
  * _Design_: EX
{% else %}
  * _Description_: Library #, e.g. `Library 1`
{% endif %}
  * _Platform_: Illumina
  * _Type_: Paired End
  * _Index Kit_: Nextera DNA Dual Index
  * _Index 1_ and _Index 2_: Select any combination of indices you wish.
    Select different indices for each library. Selecting the same index for two
    different libraries will it unwise to pool those two libraries
    together later.
  * _Kit_: {% if detailed == true %}KAPA Hyper Prep{% else %}Any kit{% endif %}
  * _Size (bp)_: 300
{% if detailed == true %}
  * _Volume_: 100
{% endif %}
1. Choose _Save_.

Note that for dual-index libraries, only the first index needs to be 
specified. The second is optional.
