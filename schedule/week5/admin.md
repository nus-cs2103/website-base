{% from "schedule/index.md" import show_week_pagetop with context%}
{% from "common/macros.njk" import show_admin_sections_to_read, show_as_tab, thumb with context, timing_badge %}
{% from "common/admin.njk" import topics, policies, faqs, admin_topics_to_read, show_admin_summary with context %}

{{ show_week_pagetop(5, "admin") }}

{% call show_admin_summary() %}

{% endcall %}

<div id="additional"></div>

{{ show_admin_sections_to_read(topics, policies, faqs, admin_topics_to_read.week5, is_flat=false ) }}