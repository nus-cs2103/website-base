{% from "common/macros.njk" import embed_topic, show_admin_sections_to_read, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import policies, show_admin_summary, topics with context %}

{% call show_admin_summary() %}
1. Submit the project
{% endcall %}

<span id="week13-project">

#### {{ thumb(1) }} Submit the project

{{ embed_topic("../../admin/index-tee3201-fragment.md#final-submission-info", "Admin " + icon_embedding + " Project → Final Submission", "1", indent="2") }}
</span>
