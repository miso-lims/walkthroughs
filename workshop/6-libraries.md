#Libraries
A _library_ is made from one sample for a single target _platform_ and
has a specific _design_ associated with it that decides the _selection_
and _strategies_ used to make the library. A library may also have _tag
barcodes_ (primers) and QC information.

<img src="pics/flow-library.svg"/>

1. On the _List Samples_ page, enter your project name into the search box.
1. Check the gDNA aliquot samples to turn into libraries.
1. From the _Bulk actions_ drop down, select _Propagate (library) selected_.
1. A table will appear. Enter the library information:
  * _Description_: Library #, where # is the sample number
  * _Platform_: Illumina
  * _Type_: Paired End
  * _Selection_: PCR
  * _Strategy_: WGS
  * _Barcode Kit_: Nextera Dual Index
  * _Index 1_ and _Index 2_: Select any indices you wish
  * _Volume_: 100
  * _Kit_: Agilent SureSelect XT2
1. Choose _Save_.

Note that for dual-index barcodes, only the first barcode needs to be
specified. The second is optional.

##Design
MISO has two important pieces of information about how a library was generated:
the _selection_ (_e.g._, PCR, cDNA) and the _strategy_ (_e.g._, WGS, WXS,
amplicon). For libraries made though a workflow, the reasonable set of options
is much smaller. A _design_ captures both a selection and strategy and the list
of allowed designs is limited based on the sample type (_e.g._, a cDNA sample
can only have SM, WT, or MR library designs and these lock the selection and
strategy type accordingly).

If the design is selected and the _alias_ field is left blank, a name will be
automatically generated with the correct suffix.

##Quality control
There are three pieces of quality control information for a library in MISO:

1. The quantitative QC values (library QC)
1. The overall pre-sequencing quality control (QC passed)
1. The post-sequencing quality control (low quality library)

###Library QC
After measuring the insert size or concentration, this information can be
entered. There is no bulk entry for this information, it must be entered per
library at this time.

1. From the _List Libraries_ page, find the 0001 library using the search box and click the link.
1. Beside the _QCs_ heading, select _Options_ → _Add Library QC_.
1. Enter the insert size or concentration and the instrument used to perform the measurement.
1. Click _Add_.

###QC passed
The QC passed is a simple pass/fail for a library to decide if it is good
enough for sequencing.

1. From the _List Libraries_ page, find 0001 library and click the link.
1. Change _QC passed_ from _Unknown_ to _True_.
1. Click _Save_.

###Low Quality Library
Not every library realises its full potential. After sequencing, sometimes
problems are discovered in libraries that need to be sequenced again. The
“low-quality library” indicator causes any pool containing this library to be
flagged, in case it will be sequenced again.

1. From the _List Libraries_ page, find the 0004 library and click the link.
1. Check _Low quality library_.
1. Click _Save_.

In later exercises, this library will be marked as suspect.

## Boxes
Libraries can also be placed in boxes.

1. From the _List Boxes_ page, find the project-specific box created before.
1. Select an unused position and enter a matrix barcode from the table above.
1. Click _Lookup_ and then _Update position_.
1. Repeat for the remaining libraries.
