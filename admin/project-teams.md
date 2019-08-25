{% macro show_main_text() %}
<div id="main">

<img src="{{baseUrl}}/admin/images/team.png" width="300px"><br>
<small>%%[Picture: The team that was at the top of early Google]%%</small>
<p/>

**When to form teams**:
* CS2103T: Your team will be formed by the CS2101 side.
* CS2103: Your team will be formed at the _start_ of the week 3 tutorial. Please try to arrive on time for that tutorial; if you are not there at the team forming time and others in the class are unaware which team you wanted to be in, we'll have to put you into a team randomly.

**Team size**: The default ==team size is five==.

**Team composition**

We allow some freedom in choosing team members, subject to these constraints:

* All team members should be in the same tutorial. ==Delay forming teams until your place in a tutorial is confirmed.== We do not allow changing tutorials to team up with your preferred team mates.  
* Teams of ==single nationality are not allowed==  unless the only language common among all team members is English. e.g. an all-Singaporean team that include both Chinese and Malay students. %%Rationale: to train you to work in multicultural teams, to ensure that English is used for all project communication%%
* No more than one exchange students per team %%Rationale: to increase interaction between exchange students and NUS students.%%
* Same gender teams are discouraged but allowed. %%Rationale: to train you for mixed-gender work environments.%%

* Also note that ==**we may modify teams when circumstances call for it**==. There is no avenue for you to object. Staying with your preferred team is not guaranteed.

</div>
<div id="teamIdFormat">

**Team ID**: This will be given to you after forming teams. It has the form `TUTORIAL_ID-TEAM_NUMBER` e.g, `CS2103-W14-2` means you are in tutorial `CS2103-W14` (i.e., in module `CS2103`, on `Wednesday`, at `1400-1500`), team `2`.

{{ embed_topic("tutorials.md#tutorialTimetable", "Admin " + icon_embedding + " Tutorials → Tutorial IDs", "projectTeams-tutorialIDs", "3") }}
</div>
<div id="teamCommunication">

* **We recommend at least one 1-2 hour ==face-to-face== project meeting per week**, in addition to any online meetings. %%Reason: you need to know how to run both types of project meetings%%. The project meeting time can be used to discuss project related things, but also, can be used as a time for team members to work on the project tasks individually (having all members in the same place will facilitate easier collaboration and more peer-learning).

* After the team has been finalized (latest by week 3 tutorial), decide on a 1-2 hour time slot and a venue that all commit to. **All members are expected to honor this commitment** (not doing so could lower the peer evaluation ratings you receive, which in turn will be factored into your grade).<br>
  {{ icon_tip }} The best time to have the weekly project meeting is, after the previous week's lecture but before the deadline for weekly tasks.

* You can also create private slack channels within the [module's slack team]({{slack_team}}). These channels will not be visible to others (even instructors).
</div>
{% endmacro %}

{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-teams", show_main_text) }}