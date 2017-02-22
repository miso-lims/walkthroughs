
Boxes hold samples, libraries, and pools. They do not track reagents or
primers. Boxes are separated into _uses_ for different kinds of storage
(_e.g._, tissue samples versus extracted DNA), but there is no check
that items in a box match. Each box also has a _size_ that includes the
physical dimensions of the box as well as whether the box is compatible
with the VisionMate scanner. Every _position_ in the box is identified
by a standard row letter + column number format (_e.g._, C05).

---------------------------

In this exercise, we are going to put the things in the box that you made in
the previous exercises. Depending on whether you have been creating samples or
libraries, some of these fields will be different.

First, create a new box:

1. From the navigation panel, choose _Boxes_ and then _Add Box_.
1. On the _Create Box_ page, enter the information:
  1. Alias: A short name for the box. Record this name in your worksheet. <img src="pics/blue_pencil.png">
  1. _Description_: a human description of the box purpose  “gDNA ready for
    library prep for <project>”.
  1. _Use_: The contents of the box. Select an appropriate use for your entities.
  1. _Size_: Select `8 x 12 scannable`.
1. Click _Save_.

Upon clicking save, a graphic of the box will appear.

<img src="pics/5-empty-box.png" id="figure">

You can now fill the box with the tissues, stocks, aliquots, libraries, or
pools you made in previous steps.

1. Click on a position in the displayed _Contents_ grid.
1. Enter a matrix barcode into the box on the right and click _Lookup_.
Normally a hand scanner would be used.
1. Click _Update Position_. 
  * &#9888; The _Save_ button at the top of the page does not work for
    individual positions, only for _Box Information_.
1. Repeat for as many samples/libraries/pools as you want.

The table below the box diagram shows the position and information for the
currently selected sample. If you would like to see all of the samples in the
table, click the _List all Box Contents_ button at the top right of the table.

In the lab, it is possible to use _Options_ > _Scan Box_ to use the plate
scanner and update all positions at once, but that will not be covered in this
tutorial.

## Using Boxes

Boxes can be found either from the Sample or Library page or the _Boxes_ page.

1. On the _Sample_ page, search for one of your sample or library aliases and click on the alias to load the page.
1. The Box and position is listed under _Location_ near the top of the _Sample
Information_ section. Click on the link to go to the Box (e.g. `PROJ_OUTBOX,
A03`).

Boxes can be used to store Samples, Libraries and Pools and one box can store all
three types.

### Removing and discarding tubes

When you have a position selected, you can also either remove the tube from the
box (setting its location to "Unknown") or discard the tube, meaning it has been
used up. Discarding the tube sets the volume of the sample to 0 and marks it as
"discarded",and removes it from its box.

1. Click on one of the positions in the box with a tube. The position, alias,
   and barcode will appear to the right or below the box graphic. 
   Right-click on the alias and pick "Open in new tab" to load the details page.
1. Go back to the Box page in the other tab. Make sure the tube is still selected in
   the Box and click _Discard Tube_. Click "OK" in the pop-up.
1. Go to the other tab with the Details page and click the browser refresh
   button. The _Location_ field will show as blank, _Volume_ will be set to 0.0,
   and the _Discarded_ box will be ticked.

### Moving samples around in boxes

An item can only exist in one box. If assigned to a new box, it will
disappear from the original.

1. In the current tab, go to the _Boxes_ page, find the _TUTORIAL_ box. This box was previously
created by the MISO developers for the tutorial.
1. Choose an empty position and enter one of your barcodes.
1. Click _Lookup_ and _Update Position_.
1. Go back to your own Box and refresh the page. The sample was removed.

