<a name="pool-orders" href="#" id="toplink">top</a>

# 7. Creating pool orders

A pool order indicates that a set of library aliquots is ready to be pooled and sequenced. If you
hand off library aliquots to another person or team to create the pool, you should create a pool
order to pass on the requirements.

## 7.1 Creating a pool order

1. On the _Library Aliquots_ list page, check the {% if include.detailed == true %}five{% else %}six{% endif %} aliquots
   you just created.
1. From the toolbar, select _Create Order_.
1. Enter the order information:
   * _Alias_: Enter the project {% if include.detailed == true %}short{% endif %} name followed by ` Order 1` (e.g.
     `PROJ Order 1`)
   * _Purpose_: `Production`
   * _Specify sequencing requirements?_: Yes
   * _Platform_: `{{ site.platform_type }}`
   * _Instrument Model_: `{{ site.platform }}`
   * _Container Model_: `{{ site.flowcell }}`
   * _Sequencing Parameters_: `{{ site.seq_params }}`
   * _Partitions required_: 1
   * _Draft_: No
1. Click _Save_. Record the order alias in your worksheet. <img src="pics/blue_pencil.png">
