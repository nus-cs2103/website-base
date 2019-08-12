{% from "common/macros.njk" import embed_topic, timing_badge, show_as_tab with context %}
{% from "schedule/index.md" import show_week_pagetop, show_week_summary with context%}
{{ show_week_pagetop(1, "notices") }}

<box type="info" dismissible>

A summary of the week, and announcements relevant to that week, will appear in this tab. Refer to the respective tabs (i.e., [{{ show_as_tab('Topics', icon_book) }}](topics.html), [{{ show_as_tab('Project', icon_project) }}](project.html), ... given at the top of this page) for more details.

A **[full timeline](../timeline.html)** is available too.
</box>

{{ show_week_summary(1) }}



