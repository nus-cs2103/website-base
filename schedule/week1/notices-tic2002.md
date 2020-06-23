{% from "common/macros.njk" import embed_topic, timing_badge, show_as_tab with context %}
{% from "schedule/index.md" import show_week_pagetop, show_week_summary with context%}
{{ show_week_pagetop(1, "notices") }}

<box type="info" dismissible>

A summary of the week, and announcements relevant to that week, will appear in this tab.<br>Click on the [{{ show_as_tab("Topics", icon_book) }}](topics.html) and the [{{ show_as_tab("Tasks", icon_todo) }}](admin-{{ module | lower }}.html) tabs (shown at the top of this page) to see more details of each category.
</box>

<panel type="warning" expanded no-close>
<span slot="header">

Admin {{ icon_embedding }} Policies → Deadlines
</span>
<include src="../../admin/index-tic2002.md#deadlines-info" />
</panel>
<p/>

{{ show_week_summary(1) }}