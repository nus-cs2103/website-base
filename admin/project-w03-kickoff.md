{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">

<p class="lead" style="color: purple"><md>:far-calendar-check: <include src="project-timeline.md#kickoff-overview" inline /></md></p>

* **Set up a weekly project meeting time/venue with your team members**
  
  We recommend at least one 1-2 hour face-to-face project meeting per week. %%The project meeting time can be used to discuss project related things, but also, can be used as a time for team members to work on the project tasks individually (having all members in the same place will facilitate easier collaboration and more peer-learning).%%
  
* **Familiarize yourself with AB3**: Download the latest released version %%(i.e., the jar file)%% of AB3 from [its upstream repo](https://se-edu.github.io/addressbook-level3/UserGuide.html) and play around with it to familiarize with its current features.

</div>
</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-w03-kickoff", show_main_text) }}