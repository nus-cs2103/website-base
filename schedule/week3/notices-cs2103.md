{% from "common/macros.njk" import embed_topic, timing_badge, show_as_tab with context %}
{% from "schedule/index.md" import show_week_pagetop, show_week_summary with context%}
{{ show_week_pagetop(3, "notices") }}

<box type="warning">

* The **deadline to achieve weekly tasks is the midnight before your tutorial**, unless mentioned otherwise. Our scripts that detect your work run at midnight and only the work that's done by midnight will be eligible for marks (for cases where the task is graded).
* We start tutorials this week. The [tutorial time table]({{ module_website }}/admin/tutorials.html#tutorial-timetable) is on the module website.
</box>

{{ show_week_summary(3) }}
