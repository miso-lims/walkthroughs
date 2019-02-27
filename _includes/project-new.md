<a name="proj" href="#" id="toplink">top</a>

# 2. Creating projects

A _Project_ contains information about a set of _Studies_ that may comprise many
different _Samples_, _Experiments_ and _Runs_. Samples are attached to Projects and
they are often processed into _Libraries_ and then _Dilutions_, which are then
_Pooled_ and sequenced. This part of the workshop details creating a new project.

Projects represent a sequencing effort toward a particular goal, usually led by
a particular group or principal investigator. {{ include.project-example }}

In this workshop, you will make your own project where you will create samples,
libraries and other entities.

Most pages have a "Quick Help" tab at the top right under the Save
button where you can find basic information about the current page.


{% include project-create.md detailed=include.detailed section=2.1 worksheet=true %}

### 2.1.1 Add a Study (optional)

If you plan to upload your project data to the ENA, you must add a _Study_ to 
your Project.

1. Click on the _Studies_ header to expand the section.
1. Click the _Add_ button at the top left of the table.
1. Much like creating a Project, enter:
  1. Alias (letters and numbers only): this can have any name, but make sure
     it is recognizable as belonging to your Project.
  1. Description: any free-text description
  1. Select a Study Type from the drop-down menu. Unless you are certain of the
     sequencing type, select `Other`.
1. Click the _Save_ button at the upper right.


## 2.2 My Projects tab

1. Click again on the _My Projects_ tab. You will see a list of all of the projects
in MISO.

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
The tables under each section can be sorted by clicking the column header or
searched using the field in the upper right.



### 2.3.1 Add Project Files

In the _Project Files_ section, you can add attach any necessary documents to the
project (e.g. Project Information form, REB).

1. On the Edit Project page, click the _Project Files_ header to expand the section.
1. Click the _Upload_ button at the top left of the table.
1. In the dialog, click the _Browse..._ button.
1. Select a document or image that is appropriate for your study
1. Choose a category for the attachment
1. Click the _Upload_ button
