{% from "schedule/index.md" import show_week_pagetop with context%}
{% from "common/macros.njk" import show_admin_sections_to_read, show_as_tab, thumb with context, timing_badge %}
{% from "common/admin.njk" import topics, policies, faqs, admin_topics_to_read, show_admin_summary with context %}

{{ show_week_pagetop(7, "admin") }}

{% call show_admin_summary() %}
1. iP final submission {{ timing_badge('by weekly deadline') }}
{% endcall %}

<div id="additional">

#### {{ thumb(1) }} iP final submission {{ timing_badge('by weekly deadline', 'secondary') }}

See the [{{ show_as_tab('Project', icon_project) }}](project.html) for more details.

</div>

{{ show_admin_sections_to_read(topics, policies, faqs, admin_topics_to_read.week7, is_flat=false ) }}