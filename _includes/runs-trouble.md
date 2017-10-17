<a name="trouble" href="#" id="toplink">top</a>

# 8. Troubleshooting

1. When instruments break down, how do you log failures into the system?
    * Add a service record as in <a href="#service">7: Adding Service Records to Sequencers</a>

1. How do you assign single lane failures (if possible)?
    * It is possible to add a RunQC which allows you to select one or more lanes, but adding one does not change the Orders count for the pool in that lane (ie. it does not "requeue" the pool). At this time, please go to the Edit Pool page for the pool in the lane and add another Order for the number of lanes and sequencing parameters requested.

1. How you fail flowcells? Or how does MISO detect failed runs?
    * If MISO automatically detects runs from this sequencer, then in most cases MISO will automatically detect failed runs if the run has begun sequencing.
    * If MISO does not automatically detect runs from this sequencer or you note that MISO has not detected that the run has failed, then you must select the `Failed` status on the Edit Run page, and enter a completion date.
    * If the pool contains a single library and you know that the library is of low enough quality that sequencing should not be attempted again, follow the steps to <a href="#lowQuality">mark a library as Low Quality</a>.
