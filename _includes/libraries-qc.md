<a name="libraries-qc" href="#" id="toplink">top</a>

# 4. Quality control

There are three ways to indicate library quality in MISO: 1)
Enter quantitative QC values under the _Library QC_ section; 2) The overall
pre-sequencing quality field _QC Status_; and 3) The post-sequencing quality
control flag _Low quality library_.

## 4.1 Library QC

After measuring the insert size or concentration, this information can be
entered into each library.

{% include bulk-qc.md detailed=include.detailed items_section="2.1" type="library" type_plural="libraries" %}

## 4.2 QC status

_QC Status_ describes the quality of a library and may be used to indicate
whether it is good enough for sequencing.

1. From the _Libraries_ page, find one of your libraries using the search
box and click the library name or alias link.
1. Change _QC passed_ from `{{ site.detailed_qc_status_pending }}` to
   `{{ site.detailed_qc_status_good }}`.
1. Click _Save_.

## 4.3 Low Quality Sequencing

Libraries can be marked as having low sequencing quality, which will be shown
after the _Run_ exercises.
