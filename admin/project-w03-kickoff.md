{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/macros.njk" import embed_topic, thumb, timing_badge with context %}

{% macro show_main_text() %}
<div id="main">

{% call show_project_summary_lead()%}
2. Get familiar with AB3 features
1. Set up a project meeting time {{ timing_badge("by the end of the tutorial", "info") }}
{% endcall %}

<div id="body">

#### {{ thumb(1) }} Get familiar with AB3 features

* **Familiarize yourself with AB3**: Download the latest released version %%(i.e., the jar file)%% of AB3 from [its upstream repo](https://se-edu.github.io/addressbook-level3/UserGuide.html) and play around with it to familiarize with its current features.

#### {{ thumb(2) }} Set up a project meeting time {{ timing_badge("by the end of the tutorial", "secondary") }}

* After forming teams, **set up a weekly project meeting time/venue with your team members**:

  * **We recommend at least one 1-2 hour ==face-to-face== project meeting per week**, in addition to any online meetings. %%Reason: you need to know how to run both types of project meetings%%. The project meeting time can be used to discuss project related things, but also, can be used as a time for team members to work on the project tasks individually (having all members in the same place will facilitate easier collaboration and more peer-learning).

  * After the team has been finalized (latest by week 3 tutorial), decide on a 1-2 hour time slot and a venue that all commit to. **All members are expected to honor this commitment** (not doing so could lower the peer evaluation ratings you receive, which in turn will be factored into your grade).<br>
    {{ icon_tip }} The best time to have the weekly project meeting is, after the previous week's lecture but before the deadline for weekly tasks.

</div>
</div>
{% endmacro %}

{{ show_admin_page("project-w03-kickoff", show_main_text) }}