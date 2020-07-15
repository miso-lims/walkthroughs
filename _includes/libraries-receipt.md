<a name="receipt"  href="#" id="toplink">top</a>

# {{include.section}}. Receiving Libraries

Propagating libraries from samples is only possible if there are existing samples to propagate from,
and only makes sense if the libraries were prepared in-house. Libraries may also be received without
the samples. The sample information is still required, but it can all be entered in one step.

{% if include.detailed == true %}
When a library is entered in this way, the automatically-created sample hierarchy will include an
Identity, Tissue, Stock, and Aliquot. Existing Identities and Tissues may be included in the hierarchy
if they match the data entered.
{% endif %}

## {{include.section}}.1 Entering received Libraries

1. On the left hand menu under _Preparation_, click _Libraries_.
1. Click the _Receive_ button at the top of the table.
{% if include.detailed == true %}
1. In the dialog, select _Aliquot Class_: gDNA (aliquot), and _Quantity_: 1, and click _Receive_
{% else %}
1. In the dialog, select _Quantity_: 1, and click _Receive_
{% endif %}
1. Select or enter the following data:
{% if include.detailed == false %}
    * _Sample Alias_: enter a sample alias like `PRO1_S#_#`. Replace `PRO1` with
      your project's name, and replace the `#` symbol with numbers of your choosing.
{% endif %}
    * _Sample Type_: select `GENOMIC` from the drop-down.
    * _Project_: Select your project from the drop-down.
{% if include.detailed == true %}
    * _Subproject_: Select the subproject you created.
{% endif %}
    * _Sci. Name_: Homo sapiens{% if include.detailed == true %}
    * _External Name_: Enter `PROJ_ID10`, replacing the `PROJ` with your own project short name. The
      _Identity Alias_ column should change to show `First Receipt (PROJ)`.
    * _Donor Sex_: select any option from the drop-down.
    * _Tissue Origin_: select Pa (Pancreas) from the drop-down.
    * _Tissue Type_: select P (Primary tumour) from the drop-down.
    * _Times Received_: 1
    * _Tube Number_: 1{% endif %}
    * _Date of receipt_: select today's date
    * _Received From_: Select any lab.
    * _Received By_: Select any group.
{% if include.detailed == true %}
    * _Design_: select WG from the drop-down
{% endif %}
    * _Platform_: select {{include.platform}} from the drop-down
    * _Type_: select {{include.type}} from the drop-down
{% if include.detailed == false %}
    * _Selection_: PCR
    * _Strategy_: WGS
{% endif %}
    * _Index Kit_: select No indices from the drop-down
    * _Kit_: select {{include.kit}} from the drop-down
    * _Size (bp)_: 430
1. Click _Save_ at the top right. Record the Library alias and barcode in your worksheet. <img src="pics/blue_pencil.png">


