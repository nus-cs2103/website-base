{% from "common/macros.njk" import embed_topic, timing_badge, show_as_tab with context %}
{% from "schedule/index.md" import show_week_pagetop, show_week_summary with context%}
{{ show_week_pagetop(7, "notices") }}

{{ show_week_summary(7) }}


