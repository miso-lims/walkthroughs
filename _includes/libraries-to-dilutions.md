<a name="props2" href="#" id="toplink">top</a>

# 6. Propagating libraries to dilutions

A library cannot be directly loaded into a _lane_ in a _sequencing container_
(flowcell/SMRTcell) in MISO. A dilution must be made and then many dilutions
(or just one) can be mixed into a _pool_ for sequencing.

_Orders_ are requests for sequencing pools a certain number of times. They are
used to keep track of sequencing progress for project management and book-keeping.

## 6.1 Bulk creating Library Dilutions
Dilutions can be made in bulk from libraries.

{% if include.detailed == true %}
<img src="pics/flow-dilution.svg"/>
{% else %}
<img srg="pics/plain-flow-dilution.svg"/>
{% endif %}

In this exercise, we will create 4 library dilutions from the libraries we
made previously.

1. On the _Libraries_ page, check all the libraries just created.
1. From the toolbar, select _Make dilutions_.
  * Note that the _Make dilutions_ option is also available after bulk creating
or bulk editing libraries.
1. Enter the dilution information:
  * _Conc._: (use any number you wish)
  * _Creation Date_: (use the current date)
{% if include.detailed == true %}
  * _Targeted Sequencing_: select any targeted sequencing value
{% endif %}
1. Click _Save_.

