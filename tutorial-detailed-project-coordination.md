---
layout: page
category: walkthrough
title: Project Coordinator tasks
project-example: For example, the PCSI project is sequencing pancreatic tumors, references, cell lines and xenografts as part of the International Cancer Genome Consortium, and the FFPER project sequences samples from a bio-bank with a number of different preparations and treatments in order to determine the impact of each on data quality.
is-detailed: true

---

<div id="toc">
Table of Contents
<ol>
    <li><a href="#logging_in">Logging In</a></li>
    <li><a href="#project-new">Creating Projects</a></li>
    <li><a href="#subproj">Configuring sub-projects</a></li>
</ol>
</div>

<div id="infobox">
Download the worksheet for this section here: <a href="worksheet-detailed-project-coordination">Project coordination Worksheet</a>.
</div>

{% include logging_in.md detailed=page.is-detailed %}

{% include project-new.md project-example=page.project-example detailed=page.is-detailed %}

<a name="subproj" href="#" id="toplink">top</a>

# 3. Configuring sub-projects

Samples in a project can be assigned a sub-project designation. The sub-project
is primarily a label for human use.

1. On the left hand menu in the _Institute Defaults_ section, click _Subprojects_.
1. Click the _Add_ button at the top left of the table.
1. Enter quantity `1` and click _Create_.
    * Select the main Project from the drop-down
    * Fill in the alias and description.
    * Select the priority from the drop-down. This will cause high-priority items
      to display priority messages in the MISO interface.
    * Select `Human hg19 random` from the Reference Genome dropdown
1. Click _Save_ in the top right corner of the page.

Once a subproject is set up, it can be selected when creating Samples.


Now that your project has been created, continue to make your first samples.


< <a href="tutorial-detailed-bulk-tables">Working with Tables</a> | <a href="index">Home</a> | <a href="tutorial-detailed-samples">Samples</a> >
