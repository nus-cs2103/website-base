{% from "schedule/index.md" import show_week_pagetop with context%}
{% from "common/macros.njk" import embed_topic, show_admin_sections_to_read, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import topics, policies, faqs, admin_topics_to_read, show_admin_summary with context %}

{{ show_week_pagetop(13, "admin") }}

{% call show_admin_summary() %}

1. Submit Final Peer Evaluation on TEAMMATES {{ timing_badge("by Thursday 2359") }}
{% endcall %}

<div id="additional">

#### {{ thumb(1) }} Submit Final Peer Evaluation on TEAMMATES {{ timing_badge("by Thursday 2359", "secondary") }}

* Submission will open on Tuesday morning (after the final submission deadline).

{{ embed_topic("../../admin/peerEvaluations.md#finalPeerEvaluations", "Admin " + icon_embedding + " Peer Evaluations → Session: Final Peer Evaluation", "1", indent="2", status="expanded") }}

</div>
