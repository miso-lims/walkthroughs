---
layout: page
title: Propagating Samples
---

# 4. Propagating Samples
Samples in MISO exist for each step in the tissue preparation: from identity,
to tissue, optionally though tissue preparation, to stock, to aliquot. At each
step, the possible options are limited based on the established workflows.
Group IDs may be assigned at any time and are copied when propagating. Different
QC information is available at each step. For instance, STR status is attached
to the stock.

<img src="pics/flow-sample2.svg"/>

For the tissue samples created previously (by bulk and single entry), we will create stocks for library preparation.

1. On the _List Samples_ page, enter your project name in the search box.
1. Check the boxes for the tissue samples (not the received stock). They will
have names that end in two hyphenated numbers, like `DI4S_0001_Ly_R_nn_1-1`.
1. From the _Bulk actions_ dropdown at the bottom, select _Propagate (sample) selected_.
1. A new dropdown will appear. Select _gDNA (stock)_ and click _Go_.
1. Fill out the table:
  * _Description_: Stock #, where # is the individual number (e.g. `Stock 2` for DI4S_0002)
  * _Matrix Barcode_: (Project short name)\_S# (_e.g._, `DI4S_S1`)
  * _Vol._: `300`
1. Click _Save_.

**TODO: assign barcodes**

## 4.1 Bulk Editing
Samples can be edited in bulk. Assume that we have done some quality control
and wish to update the QC status of the samples.

1. On the _List Samples_ page, enter your project name in the search box.
1. Check the boxes for the stock samples (propagated and received).
1. From the _Bulk actions_ dropdown at the bottom, select _Update selected_ and click _Go_.
1. Change the _QC Passed?_ column to `true` for all rows.
1. Change the _QC Detail_ column to `Ready` for all rows.
1. Click _Save_.

## 4.2 Creating Aliquots
Propagate again from the _gDNA (stock)_ samples to _gDNA (aliquot)_. Use _Library_ as the sample purpose.

[Back](3-incoming) [Home](index) [Next](5-boxes)
