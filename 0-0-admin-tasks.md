---
layout: page
category: walkthrough
title: Administration tasks
contact-admin: email gsi@oicr.on.ca or file a JIRA ticket in _GSI Common_

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

{% include admin-groups.md %}

{% include admin-new-inst.md contact=page.contact-admin %}

<a name="subproj" href="#" id="toplink">top</a>

# 5. Configuring sub-projects

Samples in a project can be assigned a sub-project designation. The sub-project
is primarily a label for human use.
If you haven't yet set up a project, continue to the
next section first.

1. On the left hand menu under _Institute Defaults_ section, click _Subprojects_.
1. Click the _Add_ button at the top left of the table.
1. Enter quantity `1` and click `Create`. 
    * Select the main Project from the drop-down
    * Fill in the alias and description.
    * Select the priority from the drop-down. Eventually this will flag high-priority samples in the MISO interface.
    * Select `Human hg19 random` from the Reference Genome dropdown
1. Click _Save_ in the top right corner of the page.

Once a subproject is set up, it can be selected when creating Samples.

<a name="reports" href="#" id="toplink">top</a>

# 6. Creating project and monthly reports

If you require a report, please {{ page.contact-admin }} for assistance.


<a href="index">Home</a> | <a href="1-0-project-coordination">Project Coordination tutorial</a> > 
