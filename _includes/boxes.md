
Boxes hold samples, libraries, and pools. They do not track reagents or
primers. Boxes are separated into _uses_ for different kinds of storage
(_e.g._, tissue samples versus extracted DNA), but there is no check
that items in a box match. Each box also has a _size_ that includes the
physical dimensions of the box as well as whether the box is compatible
with the VisionMate scanner. Every _position_ in the box is identified
by a standard row letter + column number format (_e.g._, C05).

The goal is to create a box for the samples created in the previous step.

1. From the navigation panel, choose _Boxes_ and then _Add Box_.
1. On the _Create Box_ page, enter the information:
  1. Alias: A short name for the box. Enter your short name followed by
     `_OUTBOX` (e.g. PROJ\_OUTBOX)
  1. _Description_: a human description of the box purpose  “gDNA ready for
    library prep for <project>”.
  1. _Use_: The contents of the box. Select `DNA`.
  1. _Size_: Select `8 x 12 scannable`.
1. Click _Save_.

Upon clicking save, a graphic of the box will appear. You can now load your
samples into the box. All types of samples can be entered in the box, including
the tissues, stocks and aliquots you made in the previous steps.

1. Click on a position in the displayed _Contents_ grid.
1. Enter a matrix barcode into the box on the right and click _Lookup_.
Normally a hand scanner would be used. For this exercise, use this handy
reference list:
  * `PROJ_P1_St`
  * `PROJ_P2_St`
  * `PROJ_R1_St`
  * `PROJ_R2_St`
  * `PROJ_P1_Al`
  * `PROJ_P2_Al`
  * `PROJ_R1_Al`
  * `PROJ_R2_Al`
1. Click _Update Position_. 
  * &#9888; The _Save_ button does not work for individual positions, only for
    _Box Information_.
1. Repeat for all the samples listed above.

The table below the box diagram shows the position and information for the
currently selected sample. If you would like to see all of the samples in the
table, click the _List all Box Contents_ button at the top right of the table.

In the lab, it is possible to use _Options_ > _Scan Box_ to use the plate
scanner and update all positions at once, but that will not be covered in this
tutorial.

## Using Boxes

Boxes can be found either from the Sample or Library page or the _Boxes_ page.

1. On the _Sample_ page, enter your project name.
1. Click on the alias for individual 2 primary stock, i.e.
`PROJ_0002_Br_P_nn_1-1_D_S1`.
1. The Box and position is listed under _Location_ near the top of the _Sample
Information_ section. Click on the link to go to the Box (e.g. `PROJ_OUTBOX,
A03`).

Boxes can be used to store Samples, Libraries and Pools and one box can store all
three types.

### Removing and trashing tubes

When you have a position selected, you can also either remove the tube from the
box (setting its location to "Unknown") or trash the tube, meaning it has been
used up. Trashing the tube sets the volume of the sample to 0 and marks it as
"emptied".

1. From the list below the box, find the location of the
`PROJ_0002_Br_P_nn_1-1_D_S1` sample.
1. Open the sample page in a new tab by clicking on the Sample link (Right click
on the link and select "Open in new tab").
1. Go back to the Box page if necessary. Select the sample you just opened in
the Box and click _Trash Tube_. Click "OK" in the pop-up.
1. Go to the other tab with the _Edit Sample_ page and click the browser refresh
button. The _Location_ field will show as blank, _Volume_ will be set to 0.0,
and the _Emptied_ box will be ticked.

### Moving samples around in boxes

An item can only exist in one box. If assigned to a new box, it will
disappear from the original.

1. In the current tab, go to the _Boxes_ page, find the _TUTORIAL_ box. This box was previously
created by the MISO developers for the tutorial..
1. Choose an empty position and enter your barcode ending in `PROJ_P1_Al` (e.g., `PROJ_P1_Al`).
1. Click _Lookup_ and _Update Position_.
1. Go back to the first tab with your `PROJ_OUTBOX` Box and refresh the
browser, or return to the _Boxes_ page and find your project outbox. The
sample was removed from the outbox.


[Back](4-samples) [Home](index) [Next](6-libraries)
