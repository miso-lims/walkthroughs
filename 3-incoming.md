---
layout: page
title: 3. Incoming samples
---

A _Sample_ contains information about the material upon which the sequencing
experiments are to be based. Samples can be used in any number of sequencing
_Experiments_ in the form of a _Library_ that is often processed further into
pooled _Dilutions._

Every received Sample must have an _Identity_. The Identity corresponds to the
individual or organism with whom the sample originated, i.e. the donor. MISO
requires you to assign an external name, which is usually an identifier from
another institution like a Donor ID.

When material is received for sequencing, it can be in many different forms,
called _Sample Classes_ in MISO. Here are the classes of Sample that can be
received:

* Cell line
* Tumour tissue (Primary or Metastatic)
* Reference tissue
* Xenograft tissue
* gDNA (untreated or whole genome amplified)
* cDNA
* whole RNA

Depending on which Sample Class is chosen, more or less fields appear on the
_Create Sample_ page.

In this workshop, we will create six Samples with four different Identities in
the Project you created in the last session.

<img src="pics/flow-tissue-rx.svg"/>

## 3.1 Entering a single Sample

There are two ways of entering Samples into MISO: Single and Bulk. We will start
by entering a single Sample for reference tissue from the Identity `ID1`.

1. On the left hand menu under _Tracking_, click _Samples_.
1. Click the _Add Sample_ button on the right hand side. There are two tabs
across the top. Ensure that _Single_ is selected.
1. In the _Sample Information_ section, enter or select the following:
  1. Project: Select the project you created in the last exercise.
  1. Alias: leave blank. This will be auto-generated based on other
information in this form.
  1. Description: `Reference 1`.
  1. Date of Receipt: Select a date
  1. Scientific Name: `Homo sapiens`.
  1. Sample Type: select `GENOMIC` from the drop down.
  1. QC Status: select `Ready` from the drop down.
1. In the _Identity_ section:
  1. External names : 
    1. Click _Find or Create Identity_.
    1. In the pop-up window, enter external name: project short name `_ID1` 
(_e.g._, `PROJ_ID2`). This is the name given to the donor by the external 
institute that the tissue came from.
    1. Click _Validate External Name(s)_.
    1. From the dropdown, select `First Receipt`.
    1. Click _Select_.
  1. Sex: Select any item from the dropdown.
1. In the _Details_ section, select the _Sample Class_ `Reference Tissue`.
1. In the _Tissue_ section, select or enter the following to create a reference Sample.
  1. Tissue Origin: `Ly (Lymphocyte)`
  1. Tissue Type: `R (Reference or non-tumour, non-diseased tissue sample)`
  1. Tissue Material: Select any from the drop-down.
  1. External Institute Identifier: `BioBankID 1`. This is the Biobank ID or Tube ID.
It may also be left blank.
  1. Lab: Select `BioBank (University Health Network)` from the drop-down.
  1. Times Received: `1`
  1. Tube Number: `1`
1. At the upper right hand side, click _Save_.

Upon saving, a number of fields will be filled in, including the Alias. The
Tissue
Alias will be in the form PROJ\_0001\_Ly\_R\_nn\_1-1: (Project Short
Name)\_(Individual ID)\_(Tissue Origin)\_(Tissue Type)\_(Passage number)\_(Times
Received)\_(Tube Number). Passage number is only required for Xenografts and Cell
lines. For more information about Sample nomenclature, see <a
href="https://wiki.oicr.on.ca/display/MCPHERSON/LIMS+Guidelines#LIMSGuidelines-SampleNomenclature"
target="_new">Sample Nomenclature</a>.

### 3.1.1 Enter a matrix tube barcode

After saving the Sample, you will be able to enter the barcode for the tube.

1. On the _Edit Sample_ page for the sample you just created, click the arrow next to
the blue _ID_ box at the top right hand corner.
1. Select _Assign New Barcode_ from the menu.
1. Use the hand-scanner or type a barcode into the pop-up. For this exercise,
enter your Project Short Name and _R1. e.g. `PROJ_R1`. We will use this barcode
later in the Box section.
1. Click _Save_ on the pop-up.

The page will re-load with the 2D barcode at the top right.

## 3.2 Automatically created Samples

1. Click the _My Projects_ tab at the top and select your project from the list.
1. Open the _Samples_ section on the _Edit Project_ page to see your newly
created samples.

(You can also find your samples by searching on the _Samples_ page or by
using the widget on the MISO front page. At the moment, searching on the 
_Samples_ page is quite slow but you are welcome to try using that page to view
your samples. The widget is fast but does not show enough information for the
following exercises.)

You only created a single Sample but at least two are in this list: the
Reference tissue as well as the Identity. The Identity sample was automatically
created because you provided an _External name_ that had not been previously
used in this Project, and has a name in the format (Project short
name)\_(Individual number), e.g. PROJ_0001. Other types of Samples are created automatically depending
on how you propagate them through to libraries. Some of them will be addressed
in the following tutorials.

## 3.3 Bulk create Samples

Next, we will create four more Samples using the much faster bulk method. The
four samples will be the Primary Tumour Tissue for individuals 1-5.

1. On the left hand menu under _Tracking_, click _Samples_.
1. Click the _Add Sample_ button on the right hand side. There are two tabs
across the top. Ensure that _Bulk_ is selected.
1. _Select project_ dropdown: select your project.
1. _Select class_ dropdown: `Primary Tumor Tissue`.
1. _Number of samples_ text box: `4`.
1. Click _Make Table_.

A table will appear with the requested number of samples in table format. We
will fill in the first row and use the quick-fill option to fill in the rest of
the table.

Enter the following values into the **first row only**.

1. Sample Alias: leave blank. Again, this will be automatically generated from
the rest of the table.
1. Select or enter the following fields:
  1. Description: `Primary`.
  1. Date of Receipt: select a date
  1. Sample Type: select `GENOMIC` from the drop-down.
  1. Sex: select any item from the drop-down.
  1. Tissue Origin: select `Br (Breast)` from the drop-down.
  1. Tissue Type: select `P (Primary Tumour)` from the drop-down.
  1. Times Received: 1
  1. Tube Number: 1
  1. Lab: select `BioBank (University Health Network)` from the drop-down.
  1. Ext. Inst. Identifier: `BioBankID`
  1. Material: Select any item from the drop down.
  1. QC Status: Select `Ready` from the drop down.


Now we will fill in the rest of the table. Like in Excel, you can fill down a
column by double-clicking the square at the lower right hand side of a selected
cell. You can also click and drag to only fill in a certain number of cells.

1. Click the _Sample Type_ cell in the first row. A blue square will appear at
the lower right hand side. Double click it to fill in the rest of the table with
the word "Primary".
1. Fill in the columns in the same way for: _Sex_, _Tissue
Origin_, _Tissue Type_, _Times Received_, _Tube Number_, and _Material_.

<table border="1"><tr><td>
<img src="pics/fill-down-1.png"/>
</td><td>
<img src="pics/fill-down-2.png"/>
</td></tr></table>


Some fields cannot be filled down, so enter each of those separately.

1. _Matrix Barcode_: you would normally use a hand-scanner or
copy and paste a list of barcodes from a spreadsheet. In this case, enter the project
short name followed by P and a number. The fill down functionality does not
auto-increment, so these need to be typed. For example:`PROJ_P1`, `PROJ_P2`, `PROJ_P3`, `PROJ_P4`
1. _External Name_:  replace `PROJ` with your own project name.
  - `PROJ_ID1`
  - `PROJ_ID2`
  - `PROJ_ID3`
  - `PROJ_ID4`
  1. Click _Look up Identities_ (above the top left corner of the table).
  1. Select `First Receipt` from the dropdown menu in each cell of the `Identity Alias` column. 
Since these are all first receipt, you may fill them down after selecting it in the top row. If 
the identities already existed, you would have to select them individually.
1. _Ext. Inst. Identifier_: add a number to each row starting from 2, i.e..
`BioBankID 2`, `BioBankID 3`, `BioBankID 4`, `BioBankID 5`.
1. _Description_:

    Copying and pasting from Excel and Word is supported.

    Go to
[http://pastebin.com/uQXhafqJ](http://pastebin.com/uQXhafqJ) and copy the list of descriptions by selecting it
with your mouse, right clicking and selecting _Copy_. Then click on the first
cell in the top row of _Description_ and press Ctrl+V on your keyboard to
paste.
1. Click _Save_ at the upper right hand corner.

If everything is correct, the _Alias_ will be auto-generated for each row and
the samples will be saved. If you navigate back to your _Edit Project_ page,
there should be nine Samples:

* 4 Identity Samples
* 1 Reference Sample
* 4 Primary Samples

Notice also that because you used the same _External Name_, ending in `ID1`,
for two samples, reference and primary, they have the same Identity.

## 3.4 Receiving Stock DNA/RNA

The process for receiving Stock DNA is very similar to receiving
tissue. Every stock derives from a Tissue, which originated from an
Identity. MISO will create the tissue for you when you enter a Stock. These
samples are known as _ghost samples_, which do not exist at OICR but are in MISO
for sample tracking purposes.

In this section, we will 'receive' a single Stock DNA tube from individual 2
reference tumour.


<img src="pics/flow-stock-rx.svg"/>

1. On the left hand menu under _Tracking_, click _Samples_.
1. Click the _Add Sample_ button on the right hand side. There are two tabs
across the top. Ensure that _Single_ is selected.
1. In the _Sample Information_ section, enter or select the following:
  1. Project: Select the project you created in the last exercise.
  1. Alias: leave blank. This will be auto-generated based on other
information in this form.
  1. Description: `Stock 1`.
  1. Date of receipt: select a date.
  1. Scientific Name: `Homo sapiens`.
  1. Sample Type: select `GENOMIC` from the drop-down.
  1. QC Status: select `Ready` from the drop-down.
  1. Volume (µl): `300`
1. In the _Identity_ section, enter the
  1. External name : project name `_ID2`.
  1. Sex: Select any item from the dropdown.
1. In the _Details_ section, select the _Sample Class_: `gDNA (stock)`.
1. In the _Tissue_ section, select or enter the following to create a reference
Sample.
  1. Tissue Class: `Reference Tissue`
  1. Tissue Origin: `nn (Unknown)`
  1. Tissue Type: `R (Reference or non-tumour, non-diseased tissue sample)`
  1. Tissue Material: Select any from the drop-down.
  1. External Institute Identifier: `BioBankID 6`.
  1. Lab: `BioBank (University Health Network)`.
  1. Times Received: `1`
  1. Tube Number: `1`
1. At the upper right hand side, click _Save_.

Stock aliases are created from their tissue alias by appending _\_D\_S#_ or _\_R\_S#_.
For example, the first DNA stock that derives from a tissue `PROJ_0002_Ly_R_nn_1-1` has
the name `PROJ_0002_Ly_R_nn_1-1_D_S1`.

After saving, go back to your project page and look at the samples that were
automatically created. Although you received Stock DNA, it has created a Tissue
for you as well.

1. Click on the Tissue  with the alias similar to `PROJ_0002_nn_R_nn_1-1`. It
should have a _Sample Description_ that says only "Tissue".

At the top, you will see a grey section with the warning: "This entity does not
exist except for sample tracking purposes!". This message means that the Tissue
does not exist in a freezer at OICR. Eventually these _ghost samples_ will be
hidden from the MISO interface.

[Back](2-projects) [Home](index) [Next](4-samples)
