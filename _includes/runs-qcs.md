<a name="runs-qcs" href="#" id="toplink">top</a>

## 6.2 Mark a library as Low Quality

Not every library realises its full potential. After sequencing, specific
libraries can be flagged as having low sequencing quality. The
"Low Quality Sequencing" indicator causes any pool containing this library to be
flagged, so that it can be checked before it is sequenced again.

1. From the _Libraries_ page, find one of your libraries
and click the link.
1. Check _Low Quality Sequencing_.
1. Click _Save_.

Now if the Pool containing that Library is added to a Sequencing Container, it
will be flagged.

1. Go back to your Run page.
1. Find your pool using the lanes table. It will be flagged with a red warning marker.
1. Hover your mouse over the warning marker to see the full warning message.

## 6.3 Setting Per-Lane QCs

Sometimes a particular lane is bad or for other reasons should not be analysed. MISO
allows setting a per-lane QC. Lane QCs indicate whether a lane should be considered
for sequencing order fulfillment, and whether a lane should proceed to analysis.

1. Go to your run page.
1. In the _Lanes_ section, check the first lane.
1. Click _Set QC_ from the toolbar.
1. Pick `{{ site.lane_qc_bad }}`. This indicates that the sequencing order will not be
   fulfilled - more sequencing is required - and that analysis should be skipped.
1. Enter a description of the problem.
1. Click _Set_.
