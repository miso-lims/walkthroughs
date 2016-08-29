#Boxes
Boxes hold samples, libraries, and pools. They do not track reagents or
primers. Boxes are separated into _uses_ for different kinds of storage
(_e.g._, tissue samples versus extracted DNA), but there is no check
that items in a box match. Each box also has a _size_ that includes the
physical dimensions of the box as well as whether the box is compatible
with the VisionMate scanner. Every _position_ in the box is identified
by a standard row letter + column number format (_e.g._, C05).

The goal is to create a box for the samples created in the previous step.

1. From the navigation panel, choose _List Boxes_ and then _Add Box_.
1. Enter an alias starting with the project name followed by `_OUTBOX`.
1. Enter the description “gDNA ready for sequencing for <project>”.
1. Select “DNA” for the _Use_ and “8×12” for _Size_.
1. Click _Save_.
1. Click on a position in the displayed _Contents_ grid.
1. Enter a barcode into the box on the right and click _Lookup_.
Normally a hand scanner would be used.
1. Click _Update Position_.
1. Repeat for all the samples.

In the lab, it's also possible to use _Options_ → _Scan Box_.

##Using Boxes
Boxes can be found either from the library/sample/sample page of their
contents or the _List Boxes_ page.

1. On the _List Boxes_ page, choose the _DNA_ tab.
1. Either scroll through the list or use the search box to find the box
you created.
1. In that box, select the `_0002_Br_P_nn_1-1_D_S1` sample and click _Trash Tube_. This will
set the sample's volume to be zero and marked as “emptied”.
1. Go to the _List Pools_ page and search for one of the samples you've
created.
1. Scroll to the location and look for the link to the box.

An item can only exist in one box. If assigned to a new box, it will
disappear from the original.

1. On the _List Boxes_ page, find the _TUTORIAL_ box.
1. Choose an empty position and enter the barcode `_S4` (_e.g._, `DI4S_S4`).
1. Click _Lookup_ and _Update Position_.
1. Return to the _List Boxes_ page and find your project outbox.
1. Verify that the sample was removed from the outbox.

[Back](4-samples.md) [Home](readme.md) [Next](6-libraries.md)
