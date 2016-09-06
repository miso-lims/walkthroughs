# Pools and Dilutions
A library cannot be directly loaded into a _lane_ in a _sequencing container_
(flowcell/SMRTcell) in MISO. A dilution must be made and then many dilutions
(or just one) can be mixed into a _pool_ for sequencing.

##Dilutions
Dilutions can be made in bulk from libraries.

<img src="pics/flow-dilution.svg"/>

1. On the _List Libraries_ page, check all the libraries just created.
1. From the _Bulk actions_ drop down, select _Make dilutions from selected_ and click _Go_.
1. Enter the concentrations of the dilutions (use any number you wish).
1. Click _Save_.

Dilutions are a bit ephemeral in MISO: there is no list for all the dilutions.
To see the dilutions for a library, view that library's page.

##Pools

<img src="pics/flow-pool.svg"/>

1. On the _List Pools_ page, under the _Illumina_ tab, select _Options_ → _Add Pool_.
1. Enter the alias as the project name followed by `_POOL` and description for the pool and the target concentration. Illumina will be selected by default for the type.
1. Check _Ready to Run_.
1. Use the search box to find the dilutions created previously.
1. For each dilution, press the _+_ button to add the dilution to the pool.
1. Click _Save_.

Only pools marked as ready to run will be visible when making flow cells.

This pool has a low quality library in it and this will be highlighted when
adding it to the flow cell.

[Back](6-libraries.md) [Home](readme.md) [Next](8-runs.md)
