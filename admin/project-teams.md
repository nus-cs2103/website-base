{% macro show_main_text() %}
<div id="main">

<img src="{{baseUrl}}/admin/images/team.png" width="300px"><br>
<small>%%[Picture: The team that was at the top of early Google]%%</small>
<p/>

**When to form teams**:
* CS2103T: Your team will be formed by the CS2101 side.
* CS2103: Your team will be formed at the _start_ of the week 3 tutorial. Please try to arrive on time for that tutorial; if you are not there at the team forming time and others in the class are unaware which team you wanted to be in, we'll have to put you into a team randomly.

**Team size**: The default ==team size is five==.

<div id="teamIdFormat">

**Team ID**: This will be given to you after forming teams. It has the form `TUTORIAL_ID-TEAM_NUMBER` e.g, `W14-2` means you are in tutorial W14 (i.e., Wed 1400-1500), team 2.
</div>

{{ embed_topic("tutorials.md#tutorialTimetable", "Admin " + icon_embedding + " Tutorials → Tutorial IDs", "projectTeams-tutorialIDs", "3") }}

**Team composition**

We allow some freedom in choosing team members, subject to these constraints:

* All team members should be in the same tutorial. ==Delay forming teams until your place in a tutorial is confirmed.== We do not allow changing tutorials to team up with your preferred team mates.  
* Teams of ==single nationality are not allowed==  unless the only language common among all team members is English. e.g. an all-Singaporean team that include both Chinese and Malay students. %%Rationale: to train you to work in multicultural teams, to ensure that English is used for all project communication%%
* No more than one exchange students per team %%Rationale: to increase interaction between exchange students and NUS students.%%
* Same gender teams are highly discouraged unless unavoidable. %%Rationale: to train you for mixed-gender work environments.%%

* Also note that ==**we may modify teams when circumstances call for it**==. There is no avenue for you to object. Staying with your preferred team is not guaranteed.

</div>
{% endmacro %}

{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-teams", show_main_text) }}