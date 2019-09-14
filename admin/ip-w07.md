{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/macros.njk" import embed_topic, thumb, timing_badge with context %}

{% macro show_main_text() %}
<div id="main">

{% call show_project_summary_lead()%}
1. Do any final clean-ups
1. Submit the final version {{ timing_badge('by Monday 2359') }}
{% endcall %}
<div id="body">

#### {{ thumb(1) }} Do any final clean-ups

* Finish leftover increments from the previous weeks, if any
* Do any code cleanups, if necessary
* Update the User Guide, if necessary

#### {{ thumb(2) }} Submit the final version {{ timing_badge('by Monday 2359', "secondary") }}

* Submission is to be done via GitHub releases. If there were any changes to the code since the last release, do a new release.

</div>
</div>
{% endmacro %}

{{ show_admin_page("ip-w06", show_main_text) }}