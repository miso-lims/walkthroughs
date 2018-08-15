<a name="admin-new-inst" href="#" id="toplink">top</a>

# 4. Adding new instruments

New sequencing machines must be added to MISO so that MISO can be made aware of the
runs that use them.

## 4.1 Add a new model of sequencer

If MISO does not yet have this type of sequencer in the database, you will need
to contact {{ site.miso_admin_contact }} to put the new model into MISO before you can 
add a new sequencer of that model.

1. Please {{ site.miso_admin_contact }}  to add the new sequencer 
model to MISO. Include the following information:
    * Sequencer manufacturer (Platform)
    * Model
    * Standard read lengths you anticipate using for sequencing (_e.g._ 1x250, 2x126)

## 4.1 Add a new sequencer 

1. Click the _Home_ tab at the top of the page.
1. Click _Instruments_ in the _Tracking_ section.
1. Click the _Add_ link in the top left corner.
1. Fill in the fields of the new row that is inserted at the top of the table:
    * _Instrument Name_: enter the instrument name (case-sensitive)
    * _Platform_: select a platform from the dropdown menu
    * _Serial Number_: enter the serial number (case-sensitive)
    * _Hostname_: enter `localhost`
1. Click _Add_ to save the new sequencer.

## 4.2 Set up MISO to be aware of aware of the sequencer's output

1. Please {{ site.miso_admin_contact }}. Give the name of the new 
sequencing machine and indicate that you would like them to add the 
sequencing machine's output folder to the notification server properties file.

