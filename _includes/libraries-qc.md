<a name="libraries-qc" href="#" id="toplink">top</a>

# 4. Quality control
There are three way to indicate library quality in MISO: 1)
Enter quantitative QC values under the _Library QC_ section; 2) The overall 
pre-sequencing quality flag _QC passed_; and 3) The post-sequencing quality
control _Low quality library_.

## 4.1 Library QC
After measuring the insert size or concentration, this information can be
entered into each library.

1. Use advanced search to find the library you wish to QC.
   1. On the _Libraries_ page, enter `created:lasthour creator:me` in the
      _Search_ box and hit _Enter_.
   1. Check the boxes for the libraries that you created previously.
1. Click _Add QCs_ at the top left of the table.
1. Enter `1` QC per library and click _Add_.
1. _Date_: enter today's date
1. _Type_: `qPCR`
1. _Result_: `22`
1. Click _Save_.


## 4.2 QC passed
_QC Passed_ is a simple pass/fail flag for a library to decide if it is good
enough for sequencing. If not measured, this can be left as "Unknown".

1. From the _Libraries_ page, find one of your libraries using the search 
box and click the library name or alias link.
1. Change _QC passed_ from _Unknown_ to _True_.
1. Click _Save_.

## 4.3 Low Quality Sequencing
Libraries can be marked as having low sequencing quality, which will be shown
after the _Run_ exercises.

