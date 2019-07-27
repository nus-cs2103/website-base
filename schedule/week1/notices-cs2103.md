{% from "common/macros.njk" import embed_topic, timing_badge, show_as_tab with context %}
{% from "schedule/index.md" import show_week_pagetop, show_week_summary with context%}
{{ show_week_pagetop(1, "notices") }}

<box type="info" dismissible>

A summary of the week, and announcements relevant to that week, will appear in this tab.
</box>

{{ show_week_summary(1) }}



