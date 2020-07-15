## {{ include.section }} Creating a new project

To create a new project:

1. After logging in, click the _Projects_ link under _Preparation_ in the menu on the left side
of the screen.
1. Click the _Add_ button at the top left corner. The _Create Project_ page will
display with a number of fields that you can fill in.
1. Ignore Project ID and Name, since they are set by MISO once the Project is saved.
1. Enter a unique _Alias_. The alias is a name, chosen by us, that is associated
with a project. The alias must be unique and contain only letters or numbers. It
cannot contain spaces or punctuation. e.g. `DoIt4Science` (be creative!).
{% if include.worksheet %}Record this alias in your worksheet.
<img src="pics/blue_pencil.png">{% endif %}
{% if include.detailed == true %}
1. Enter a _Short Name_ for your project. The short name should be 2-5 letters in
all CAPS and related to the project alias. This short name will be used to
automatically generate sample and library names. e.g. short name: `DI4S`.
{% if include.worksheet %}Record the short name in your worksheet.
<img src="pics/blue_pencil.png">{% endif %}
{% else %}
1. Leave the _Short Name_ field blank.
{% endif %}
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
{% if include.detailed == true %}
1. Select the _Reference Genome_ `Human hg19 random`. This should be the primary
species that will be sequenced in the course of the project. Xenografts count
as human.
{% else %}
1. Leave the _Reference Genome_ as `Unknown`.
{% endif %}
1. Click the _Save_ button at the upper right.
1. MISO will generate an ID and name for the project. The name be 'PRO' followed
   by the ID (e.g. "PRO123"). {% if include.worksheet %}Record this name in your
   worksheet. <img src="pics/blue_pencil.png">{% endif %}
   

Upon save, you will be taken to the _Edit Project_ page, where you can see the
project you just created. Notice that the Project ID and Name now have values.
The Project ID will be an integer, and the Name will begin with PRO. These are
specific to this project and used by MISO to track the project internally.

