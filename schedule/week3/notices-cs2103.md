{% from "common/macros.njk" import embed_topic, timing_badge, show_as_tab with context %}
{% from "schedule/index.md" import show_week_pagetop, show_week_summary with context%}
{{ show_week_pagetop(3, "notices") }}

<box type="warning" dismissible>

* We start tutorials this week. The [tutorial time table]({{ module_website }}/admin/tutorials.html#tutorial-timetable) is on the module website.
</box>
<box dismissible>

Rminder about this warning from the previous week:
<include src="../timeline.md#warnings" />
</box>

<panel type="seamless" header="Reminder about deadlines">
<include src="../timeline.md#warnings" />
</panel>

{{ show_week_summary(3) }}
