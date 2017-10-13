---
layout: page
category: walkthrough
title: Administration tasks
contact-admin: contact your MISO administrator

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
Contact your MISO administrator to gain admin status.

<a name="users" href="#" id="toplink">top</a>

# 2. Adding Users

The method of adding users varies by MISO installation. 

If you were able to log in at the beginning of this tutorial using a user name and/or password
you chose, you can add new users.

1. On the left hand menu under the _User Administration_ section, click _Users_.
1. Click the _Add_ button at the top left of the table.
1. Enter the new user's login name (all one word), email, and a password.
1. Click _Save_ in the top right corner.

If you were able to log in at the beginning of this tutorial using a user name and password 
that you use for other services at your institute, users cannot be manually added by administrators.
Users must be added by IT; once added, users can log in to MISO using their existing credentials 
(LDAP or Active Directory).

OICR uses Active Directory authentication for MISO. Users must be added by IT; once added,
they can then log in to MISO using their email credentials.
  * IT must add users to the `ROLE_INTERNAL` group, and admins must additionally be added
to the `ROLE_ADMIN` group.

{% include admin-groups.md %}

{% include admin-new-inst.md contact=page.contact-admin %}

{% include admin-reports.md contact=page.contact-admin %}


<a href="plain-index">Home</a> | <a href="plain-1-0-project-coordination">Project Coordination tutorial</a> >

