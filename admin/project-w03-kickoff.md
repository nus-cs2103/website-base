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

* After forming teams, **set up a weekly project meeting time/venue (and communication channels) with your team members**:

<div class="indented-level2">

{{ embed_topic("project-teams.md#teamCommunication", "Admin " + icon_embedding + " **Teams → Communication**", "-", "2") }}
</div>

</div>
</div>
{% endmacro %}

{{ show_admin_page("project-w03-kickoff", show_main_text) }}