<!-- 
{% from "common/macros.njk" import button, embed_topic, show_as_tab, show_as_rounded_tab, step, thumb, timing_badge with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("githubClassroomInfo") %}
<div id="main">

We will use GitHub Classroom to run the basic Java exercises. It will give you additional opportunities to work with Git and GitHub and get familiar with version control.

<div tags="m--cs2113" id="ghclassroom-prerequsites">

## GitHub Classroom Prerequsites

* Before you start the exercises, you will require two things:
   1. The GitHub username you provided us in the pre-module survey
   1. The masked student identifier. Please refer to the module details page on LumiNUS for more information.
  
* Next, you need to _register_ on the Classroom.

  {{ embed_topic("appendixE-gitHub.md#githubclassroom-registering" ,"Admin " + icon_embedding + " **Registering in GitHub Classroom**", "2", indent="1",  status="collapsed") }}

</div>

<div tags="m--cs2113" id="ghclassroom-exercises-list">

## List of exercises

Note: As such the exercises are open until end of Week 6. The suggested deadline will help you to keep up with the weekly activities that counts for participation points.

<iframe src="{{ url_ghclassroom_ex }}" width="800" height="500" ></iframe>

<br>

<div tags="m--cs2113" id="working-with-ghclassroom-assignments">

## Working on the assignments

{{ embed_topic("appendixE-gitHub.md#githubclassroom-accepting-assignment" ,"Admin " + icon_embedding + " **Accepting an assignment**", "2", indent="1",  status="collapsed") }}

{{ embed_topic("appendixE-gitHub.md#githubclassroom-workingon-assignment" ,"Admin " + icon_embedding + " **Working on the assignment**", "2", indent="1",  status="collapsed") }}

</div>


</div>

{% endcall %}
-->