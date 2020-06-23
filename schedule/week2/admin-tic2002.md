{% from "schedule/index.md" import show_week_pagetop with context%}
{% from "common/macros.njk" import embed_topic, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import show_admin_summary with context %}

{{ show_week_pagetop(2, "admin") }}



{% call show_admin_summary() %}
1. Install SourceTree {{ timing_badge("before the lecture") }}
1. Submit weekly exercises
{% endcall %}

{{ thumb(1) }} Install SourceTree {{ timing_badge("before the lecture", "secondary") }}

* See the panel below:

<div class="indented-level2">

{{ embed_topic("../../admin/index-tic2002.mbdf#git-info", "Admin " + icon_embedding + " Tools → Git, SourceTree", "week2Admin-git", "1") }}
</div>

{{ thumb(2) }} Submit weekly exercises

* As usual, submit weekly programming exercise.
