---
layout: page
category: walkthrough
title: Administration tasks

---

<div id="toc">
Table of Contents
<ol>
    <li><a href="#login">Logging In</a></li>
    <li><a href="#proj">Creating Projects</a></li>
    <li><a href="#users">Adding Users</a></li>
    <li><a href="#perms">Creating groups and adding users to them</a></li>
    <li><a href="#inst">Adding new instruments</a></li>
    <li><a href="#reports">Creating project and monthly reports</a></li>
</ol>
</div>

<div id="infobox">
Download the worksheet for this section here: <a href="1-0-admin-tasks-worksheet">Admin tasks Worksheet</a>. 
</div>


<a name="login"/>

# 1. Logging in

{% include logging_in.md %}


<a name="proj"/>

# 2. Creating projects

A _Project_ contains information about a set of _Studies_ that may comprise many
different _Samples_, _Experiments_ and _Runs_. Samples are attached to Projects and
they are often processed into _Libraries_ and then _Dilutions_, which are then 
_Pooled_ and sequenced. Projects also have Overviews, which hold information about 
a Project proposal. In this part of this workshop, we will create projects, set 
permissions, and familiarize ourselves with the project overview page.

Projects represent a sequencing effort toward a particular goal, usually led by
a particular group or principal investigator. For example, the PCSI project is
sequencing pancreatic tumors, references, cell lines and xenografts as part of
the International Cancer Genome Consortium, and the FFPER project sequences
samples from a bio-bank with a number of different preparations and treatments
in order to determine the impact of each on data quality.

In this workshop, you will make your own project where you will create samples,
libraries and other entities.

Most pages have a "Quick Help" tab at the top right under the Save
button where you can find basic information about the current page.


## 2.1 Create a new project

To create a new project:

1. After logging in, click the _My Projects_ tab at the top of the MISO
dashboard. 
1. Select the _Add Project_ button at the top right corner. 

The _Create Project_ page will display with a number of fields that you can fill in.

1. Ignore Project ID and Name, since they are set by MISO once the Project is saved.
1. Enter a unique _Alias_. The alias is a name, chosen by us, that is associated
with a project. The aliases must be a unique and contain only letters or
numbers. It cannot contain spaces or punctuation. e.g. `DoIt4Science` (be creative!).
Record this alias in your worksheet. <img src="pics/blue_pencil.png">
1. Enter a _Short Name_ for your project. The short name should be 2-5 letters in
all CAPS and related to the project alias. This short name will be used to
automatically generate sample and library names. e.g. short name: `DI4S`.
Record the short name in your worksheet. <img src="pics/blue_pencil.png">
1. In the _Description_ field, enter `MISO training workshop [Date]`
1. Choose the amount of _Progress_ that your project has accomplished:
  * Unknown : I was told to enter this data and I does what they tells me.
  * Active : We are receiving/have received samples and are actively working on
    this project.
  * Inactive : Project is not yet done, but waiting for external collaborators,
    REB approval, papers to be published, etc.
  * Cancelled : Project was scrapped because we did not get funding/samples/REB
    approval.
  * Proposed : Project Initiation form has been received and is awaiting go-ahead
    by Genomics leadership.
  * Pending : We are waiting for the project to start.
  * Approved : Project has been approved by Genomics leadership.

1. Select the _Reference Genome_ `Human hg19 random`. This should be the primary
species that will be sequenced in the course of the project. Xenografts count
as human.
1. In the _Permissions_ section, select `your name` from the _Owner_ drop-down.
1. Make sure that _Allow all internal users access?_ is selected.

<img alt="Create Project DI4S" src="pics/create-di4s.png" id="figure"/>

1. Click the _Save_ button at the upper right. 

Upon save, you will be taken to the _Edit Project_ page, where you can see the
project you just created. Notice that the Project ID and Name now have values.
The Project ID will be an integer, and the Name will begin with PRO. These are
specific to this project and used by MISO to track the project internally.

### 2.1.1 Add a Study

In order to make sure MISO is SRA-compliant, you must add a _Study_ to your Project. Studies are legacy objects that are not really used in the current system, but need to be added anyway.

1. Click on the _Studies_ section to expand the section.
1. Hover over the _Options_ menu at the top right of the Studies table, and
   click _Add new Study_.
1. Much like creating a Project, enter:
  1. Alias (letters and numbers only): this can have any name, but make sure
it is recognizable as belonging to your Project.
  1. Description: any free-text description
  1. Select a Study Type from the drop-down menu : Unless you are certain of the
sequencing type, select `Other`.
1. Click the _Save_ button at the upper right.


## 2.2 My Projects tab

1. Click again on the _My Projects_ tab. 

You will see a list of all of the projects you have access to in MISO.

1. Find the project you just created in the list. You can sort any column in the
table by clicking the column header. You can also search for your project by
any of the displayed columns and the table will filter as you type. 
1. Click on the link in the Project Name, Short Name or Alias (they all go to the
same page).


## 2.3 Edit Project page

The _Edit Project_ page is used for viewing basic information about a project as
well as all of the entities associated with that project, such as the samples,
libraries, pools, and runs.

Once you create different entities for your project like _Samples, Libraries,
Library Dilutions, Pools_ and _Runs_, you can view and search them on this page.
Each section can be expanded by clicking on its name or the arrow next to it.
The tables under each section can be sorted by the column header or searched
using the field in the upper right. The _Options_ menu above the search bar
contains actions you can perform on the entities in the project.



### 2.3.1 Add a project overview

_Project Overviews_ specify the origin of a specific set of samples
that are part of the project. For example, if you are receiving some samples
from a clinician and other samples from a hospital, you can enter the expected
numbers of samples from each and indicate how many of them passed quality
control and what stage of preparation has been completed. Project overviews are
optional and only used to indicate overall progress on the _My Projects_ page.

1. Click _Add Overview_ at the right side under the Project Information. 
1. In the pop-up, enter a principal investigator (`You Yourname`!)
1. In _No. proposed samples_, enter `5`. 
1. Click the _Add Overview_ button.

The _Edit Project_ page will reload and now there will be a table with your name
under the _Project Information_ section. You can fill in other values if you wish, or
leave them blank for now. You can also select the checkboxes below the table to
show that certain stages have been completed. Remember to press the _Save_
button after you are finished editing.


### 2.3.2 Add Project Files

In the _Project Files_ section, you can add attach any necessary documents to the
project (e.g. Project Information form, REB).

1. Click the _Project Files_ section on the Edit Project page.
1. Find a document or image that is appropriate for your study 

Now that your project has been created, continue to make your first samples.


<a name="users"/>

# 3. Adding Users

OICR uses Active Directory authentication for MISO. Users must be added by IT; once added,
they can then log in to MISO using their email credentials.

1. Please email helpdesk@oicr.on.ca and CC Morgan Taschuk to request that the user be added to MISO LIMS by 
making them part of the following Active Directory groups:
    * If the person is to be added as an admin: `MISO_ROLE_ADMIN` and `MISO_ROLE_INTERNAL` groups.
    * If the person is not to be given admin access: `MISO_ROLE_INTERNAL` group.

<a name="perms"/>

# 4. Creating groups and adding users to them

_Groups_ permit fine-grained control over who has view and/or edit access to an
item in MISO. There is a default group in MISO for "all internal users".
There are also groups for Watchers, but these features are not yet fully functional. 

## 4.1 Create a Group

To create a new group:

1. Select the _Groups_ link in the left-hand menu.
1. Select the _Add Group_ link near the top right corner.

The _Edit Group_ page will display a number of fields that you can fill in.
1. Enter a unique _Name_. The name must contain only letters or numbers. It
   cannot contain spaces or punctuation.
1. Enter a _Description_ of your group.
1. Select your user as the only member of your group.
1. Click the _Save_ button at the upper right.

## 4.2 Update your project's permissions 

Return to your new project's page and update the permissions:
1. Click the _Permissions_ section divider to expand it.
1. Click the _Allow all internal users access?_ box to deselect it.
1. Select your new group in both the _Groups (read)_ and _Groups (write)_
   sections.
1. Click the _Save_ button at the upper right.
1. Click the _My Projects_ tab at the top of the page.
1. Partner with someone else who has completed these steps and compare the
   projects on your pages. You should be unable to view the other person's
project.

Return to your new project's page and update the permissions once more:
1. Click the _Permissions_ section divider to expand it.
1. Click the _Allow all itnernal users access?_ box to select it.
1. Click the _Save_ button at the upper right.

<a name="inst"/>

# 5. Adding new instruments

New sequencing machines must be added to MISO so that MISO can be made aware of the
runs that use them.

## 5.1 Add a new model of sequencer

If MISO does not yet have this type of sequencer in the database, you will need 
to contact your MISO administrator to put the new model into MISO before you can 
add a new sequencer of that model.

1. Please email gsi@oicr.on.ca or file a JIRA ticket in _GSI Common_ to add the new sequencer 
model to MISO. Include the following information:
    * Sequencer manufacturer (Platform)
    * Model
    * Standard read lengths you anticipate using for sequencing (_e.g._ 1.250, 2x126)

## 5.1 Add a new sequencer 

1. Click the _My Account_ tab at the top of the page.
1. Click _Configure_ in the _Sequencing Machines_ section.
1. Click the _Add Sequencer_ link in the top right corner.
1. Fill in the fields of the new row that is inserted at the top of the table:
    * _Name_: enter the serial number (case-sensitive)
    * _Platform_: select a platform from the dropdown menu
    * _Hostname_: enter `localhost`
1. Click _Add_ to save the new sequencer.

## 5.2 Set up MISO to be aware of aware of the sequencer's output

1. Please email gsi@oicr.on.ca or file a JIRA ticket in _GSI Common_. Give the name of the new 
sequencing machine and indicate that you would like GSI to add the 
sequencing machine's output folder to the notification server properties file.


<a name="reports"/>

# 6. Creating project and monthly reports

MISO has some basic reporting capabilities. However, it also seems to contain
dragons which periodically kill all of MISO when they are disturbed. If you require a report, 
please email gsi@oicr.on.ca for assistance.


<a href="index">Home</a> | <a href="2-0-samples">Samples tutorial</a> > 
