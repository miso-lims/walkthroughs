---
layout: page
category: walkthrough
title: Administration tasks

---

<div id="toc">
Table of Contents
<ol>
    <li><a href="#login">Logging In</a></li>
    <li><a href="#users">Adding Users</a></li>
    <li><a href="#perms">Creating groups and adding users to them</a></li>
    <li><a href="#inst">Adding new instruments</a></li>
    <li><a href="#subproj">Configuring subprojects</a></li>
    <li><a href="#reports">Creating project and monthly reports</a></li>
</ol>
</div>

<a name="login"/>

# 1. Logging in

{% include logging_in.md %}


In order to perform the tasks in this section you must be a MISO admin.
Email IT, CC Morgan Taschuk and request to be added to the `MISO_ROLE_ADMIN`
Active Directory group.

<a name="users" href="#" id="toplink">top</a>

# 2. Adding Users

OICR uses Active Directory authentication for MISO. Users must be added by IT; once added,
they can then log in to MISO using their email credentials.

1. Please email ithelpdesk@oicr.on.ca and CC Morgan Taschuk to request that the user be added to MISO LIMS by 
making them part of the following Active Directory groups:
    * If the person is to be added as an admin: `MISO_ROLE_ADMIN` and `MISO_ROLE_INTERNAL` groups.
    * If the person is not to be given admin access: `MISO_ROLE_INTERNAL` group.

<a name="perms" href="#" id="toplink">top</a>

# 3. Creating groups and adding users to them

_Groups_ permit fine-grained control over who has view and/or edit access to an
item in MISO. There is a default group in MISO for "all internal users".
There are also groups for Watchers, but these features are not yet fully functional. 

## 3.1 Create a Group

To create a new group:

1. Select the _Groups_ link in the left-hand menu.
1. Select the _Add Group_ link near the top right corner.

The _Edit Group_ page will display a number of fields that you can fill in.
1. Enter a unique _Name_. The name must contain only letters or numbers. It
   cannot contain spaces or punctuation.
1. Enter a _Description_ of your group.
1. Select your user as the only member of your group.
1. Click the _Save_ button at the upper right.

<a name="inst" href="#" id="toplink">top</a>

# 4. Adding new instruments

New sequencing machines must be added to MISO so that MISO can be made aware of the
runs that use them.

## 4.1 Add a new model of sequencer

If MISO does not yet have this type of sequencer in the database, you will need 
to contact your MISO administrator to put the new model into MISO before you can 
add a new sequencer of that model.

1. Please email gsi@oicr.on.ca or file a JIRA ticket in _GSI Common_ to add the new sequencer 
model to MISO. Include the following information:
    * Sequencer manufacturer (Platform)
    * Model
    * Standard read lengths you anticipate using for sequencing (_e.g._ 1x250, 2x126)

## 4.1 Add a new sequencer 

1. Click the _My Account_ tab at the top of the page.
1. Click _Configure_ in the _Sequencing Machines_ section.
1. Click the _Add Sequencer_ link in the top right corner.
1. Fill in the fields of the new row that is inserted at the top of the table:
    * _Name_: enter the serial number (case-sensitive)
    * _Platform_: select a platform from the dropdown menu
    * _Hostname_: enter `localhost`
1. Click _Add_ to save the new sequencer.

## 4.2 Set up MISO to be aware of aware of the sequencer's output

1. Please email gsi@oicr.on.ca or file a JIRA ticket in _GSI Common_. Give the name of the new 
sequencing machine and indicate that you would like GSI to add the 
sequencing machine's output folder to the notification server properties file.

<a name="subproj" href="#" id="toplink">top</a>

# 5. Configuring sub-projects

Samples in a project can be assigned a sub-project designation. The sub-project
is primarily a label for human use.
If you haven't yet set up a project, continue to the
next section first.

1. Click on the _My Account_ tab at the top of the page.
1. In the _Institute Defaults_ section, click on _Subprojects_.
1. Click on the _New Subproject_ button. 
    * Select the main Project from the drop-down
    * Fill in the alias and description.
    * Select the priority from the drop-down. Eventually this will flag high-priority samples in the MISO interface.
    * Select `Human hg19 random` from the Reference Genome dropdown
1. Click _Add_.

Once a subproject is set up, it can be selected when creating Samples.

<a name="reports" href="#" id="toplink">top</a>

# 6. Creating project and monthly reports

MISO has some basic reporting capabilities. However, it also seems to contain
dragons which periodically kill all of MISO when they are disturbed. If you require a report, 
please email gsi@oicr.on.ca for assistance.


<a href="index">Home</a> | <a href="1-0-project-coordination">Project Coordination tutorial</a> > 
