#Incoming samples
For our incoming samples, we're going to have 5 of them, numbered 0001
to 0005. Everyone will have a unique project to work under.

 
## Entering the sample Stock

The analyte/template type is entered into LIMS first before entering stocks and aliquots. DNA samples are coded as “_D” and RNA samples are coded as “_R”. The DNA/RNA stocks, aliquots and libraries are parented to the sample template type

1. Log into LIMS, http://miso.gsi.oicr.on.ca/
1. Under Tracking, click List Samples.
1. Check the boxes for the samples.
1. At the bottom of the page, select Propagate (sample) selected, select gDNA (stock) and click Go.
1. Enter the sample name i.e. LIMS ID
  * LIMS ID of a sample is allocated based on specified LIMS nomenclature.
  * It consists of; (Project Name)_(Individual number)_(Tissue Origin)_(TissueType)_(Passage)_(Cumulative Total of Samples Received)-(Piece Number from the Specific Received Sample)_(Type of Analyte)_(Aliquot Number)
  * For example - AAAA_8080_Pa_P_nn_2-1_D_S1is the LIMS ID given to a received DNA sample of the AAAA Project, individual 8080, tissue originating from Pancreas, ofprimary tumour, no specified passage numberand has been received twice-RNA material of the same sample would be coded as: AAAA_8080_Pa_P_nn_2-1_R_S1
1. Enter the required fields as specified i.e. sample barcode (scanned from the matrix tube), concentration, volume and sample description.
1. Click Save



## Entering Sample Aliquot

1. Log into LIMS 
1. Under Tracking, click List samples.
1. Click the check boxes for all the stock tubes.
1. From the Bulk actions drop box at the bottom, select Propagate (sample) selected. Then selectthe appropriate class marked (aliquot). Then click Go.
1. Enter Aliquot name. Aliquot names end with D_1 for DNA or R_1 for RNA, where the _1 represents number of aliquot of a sample. i.e. AAAA_8080_Pa_P_nn_2-1_D_1represents the first DNA aliquot of AAAA_8080.
1. Click Save.

Sample aliquot is now entered in LIMS.
