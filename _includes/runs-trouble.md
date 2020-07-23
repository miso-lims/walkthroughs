<a name="runs-trouble" href="#" id="toplink">top</a>

# 9. Troubleshooting

1. When instruments break down, how do you log failures into the system?
    * Add a service record as in <a href="#service-records">8: Adding Service Records to Sequencers</a>

1. How do you assign single lane failures (if possible)?
    * It is possible to add a lane QC which allows you to select one or more lanes and
      set a status to indicate whether the lane should be considered for sequencing order
      fulfillment, and whether the lane should be analysed.

1. How do you fail flowcells? Or how does MISO detect failed runs?
    * If MISO automatically detects runs from this sequencer, then in most cases MISO will
      automatically detect failed runs if the run has begun sequencing.
    * If MISO does not automatically detect runs from this sequencer or you note that MISO
      has not detected that the run has failed, then you must select the `Failed` status on
      the Edit Run page, and enter a completion date.
    * If the pool contains a single library and you know that the library is of low enough
      quality that sequencing should not be attempted again, follow the steps to
      <a href="#runs-qcs">mark a library as Low Quality</a>.
