<a name="arrays" href="#" id="toplink">top</a>

# 3. Arrays

An Array represents a chip which can have Samples added to it to be run on
an Array Scanner. Arrays can have different layouts depending on the chip model.

{% if include.detailed == true %}
Note: Only Aliquot Samples may be added to an Array.
{% endif %}

# 3.1. Create an Array

1. On the _Arrays_ page, click the _Add_ button
1. Choose an _Array Model_. If there are no options in this list, ask your MISO
administrator to add some Array Models to MISO
1. Enter a unique _Alias_ and _Serial Number_ for your Array
1. Click _Save_. The array must be saved before samples can be added to it
1. Add a Sample to the Array. The user interface is similar to Boxes:
    1. Select an empty position on the array, which will appear as a grey circle
    1. In the _Search_ box to the right, enter the Name, Alias, or Barcode of the
    Sample you wish to add
    1. Press _Enter_ or click the _Lookup_ button
    1. Your Sample should appear in the _Results_ dropdown. Click _Update position_
    to add it to the array
1. Repeat for the other samples

