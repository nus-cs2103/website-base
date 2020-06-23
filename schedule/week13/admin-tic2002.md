{% from "schedule/index.md" import show_week_pagetop with context%}
{% from "common/macros.njk" import embed_topic, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import show_admin_summary with context %}

{{ show_week_pagetop(13, "admin") }}

{% call show_admin_summary() %}
1. Submit the project {{ timing_badge("Monday 2359") }}
1. Attend the exam review {{ timing_badge("during lecture", "info") }}
{% endcall %}

{{ thumb(1) }} Submit the project {{ timing_badge("Monday 2359", "secondary") }}

<div class="indented-level2">

{{ embed_topic("../../admin/index-tic2002.mbdf#final-submission-info", "Admin " + icon_embedding + " Project → Final Submission", "week13Admin-finalSubmission", "1") }}
</div>

{{ thumb(1) }} Attend the module recap and exam briefing {{ timing_badge("during lecture", "secondary") }}

* This week's lecture will give a brief recap of the module and brief you about the exam.

