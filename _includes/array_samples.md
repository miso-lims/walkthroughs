<a name="array-samples" href="#" id="toplink">top</a>

# 3. Samples

Next, we will create the samples to be run in our array. {% if include.detailed == true %}Only Aliquot Samples can be
added to arrays, so we will receive Aliquots directly in this walkthrough.{% endif %}

## 3.1 Receiving Samples

1. In the left hand menu under _Tracking_, click _Samples_.
1. Click the _Create_ button at the top of the table.
1. In the dialog that appears, select _Sample Class_: gDNA (aliquot), and _Quantity_: 8, and click _Create_.
1. Select or enter the following data for all samples:
    * _Sample Type_: GENOMIC
    * _Project_: select your project
    * _Sci. Name_: Homo sapiens
{% if include.detailed == true %}
    * _Tissue Origin_: Ly (Lymphocyte)
    * _Tissue Type_: P (Primary tumour)
    * _Times Received_: 1
    * _Tube Number_: 1
    * _STR Status_: Not Submitted
    * _QC Status_: Ready
    * _Purpose_: Extra
1. Enter "PROJ_1" for the _External Name_ of the first sample, replacing "PROJ" with your own project's shortname.
1. Enter "PROJ_2", "PROJ_3", etc... for the _External Name_ of each remaining sample, incrementing by 1 each time so
   that they each have a unique _External Name_.
1. Enter the same values into the _Matrix Barcode_ column that you used for the _External Names_.
{% else %}
    * _QC Passed?_: True
1. Enter a _Sample Alias_ in the form "PROJ_S#_#" for each sample. Replace "PROJ" with the short name of your project,
   and replace the "#" symbol with numbers of your choosing.
1. Enter "PROJ_1" for the _Matrix Barcode_ of the first sample, replacing "PROJ" with your own project's shortname.
1. Enter "PROJ_2", "PROJ_3", etc... for the _Matrix Barcode_ of each remaining sample, incrementing by 1 each time so
   that they each have a unique _Matrix Barcode_.
{% endif %}
1. Click _Save_ at the top right.
