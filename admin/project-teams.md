{% macro show_main_text() %}
<div id="main">

<img src="{{baseUrl}}/admin/images/team.png" width="300px"><br>
<small>%%[Picture: The team that was at the top of early Google]%%</small>
<p/>

**When to form teams**

* {{ module }}T: Your team will be formed by CS2101 side in week 1.
* {{ module }}: Your team will be formed in week 3 tutorial.

**Team size**: The default ==team size is five==. 

**Team ID**: This will be given to you after forming teams. It has the form `TUTORIAL_ID-TEAM_NUMBER` e.g, `W14-2` means you are in tutorial W14 (i.e., Wed 1400-1500), team 2.

<panel src="../admin/tutorials.md#tutorialTimetable" header="Admin {{ icon_embedding }} Tutorials → Tutorial IDs" class="embedding" minimized /><p/>

**Team composition**

We allow some freedom in choosing team members, subject to these constraints:

* All team members should be in the same tutorial. ==Delay forming teams until your place in a tutorial is confirmed.== We do not allow changing tutorials to team up with your preferred team mates.  
* Teams of ==single nationality are not allowed== %%&nbsp;Rationale: to train you to work in multicultural teams.%% However, we allow same nationality teams if the only language common among all team members is English. e.g. an all-Singaporean team that include both Chinese and Malay students.
* No more than one exchange students per team %%Rationale: to increase interaction between exchange students and NUS students.%%
* Gender balanced teams are encouraged. While all-male teams may be unavoidable at times (due to high male percentage in the cohort), all-female teams are highly discouraged.

* Also note that ==**we may modify teams when circumstances call for it**==. There is no avenue for you to object. Staying with your preferred team is not guaranteed.

</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-teams", show_main_text) }}