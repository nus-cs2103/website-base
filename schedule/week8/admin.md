{% from "schedule/index.md" import show_week_pagetop with context%}
{% from "common/macros.njk" import embed_topic, show_admin_sections_to_read, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import topics, policies, faqs, admin_topics_to_read, show_admin_summary with context %}

{{ show_week_pagetop(8, "admin") }}

{% call show_admin_summary() %}
1. Submit post-lecture quiz
1. Submit Midterm Peer Evaluations on TEAMMATES {{ timing_badge("by Saturday") }}
{% endcall %}

<div id="additional">

#### {{ thumb(1) }} Submit post-lecture quiz

* As per usual.

#### {{ thumb(2) }} Submit Midterm Peer Evaluations on TEAMMATES {{ timing_badge("by Saturday", "secondary") }}

* **Peer Evaluation Round 1** will open on TEAMMATES. You will receive the submission link soon.

{{ embed_topic("../../admin/peerEvaluations.md#midtermPeerEvaluations", "Admin " + icon_embedding + " Peer Evaluations → Session: Midterm Peer Evaluation", "1", indent="2", status="expanded") }}

</div>
