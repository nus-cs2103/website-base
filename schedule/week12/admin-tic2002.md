{% from "schedule/index.md" import show_week_pagetop with context%}
{% from "common/macros.njk" import embed_topic, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import show_admin_summary with context %}

{{ show_week_pagetop(12, "admin") }}

{% call show_admin_summary() %}
1. Finish up the project coding
1. Prepare the final submission
{% endcall %}

{{ thumb(1) }} Finish up the project coding

* Finish up any remaining coding work.
* Test the product thoroughly.

{{ thumb(2) }} Prepare the final submission

<div class="indented-level2">

{{ embed_topic("../../admin/index-tic2002.mbdf#final-submission-info", "Admin " + icon_embedding + " Project → Final Submission", "week12Admin-finalSubmission", "1") }}
</div>