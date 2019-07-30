{% from "schedule/index.md" import show_week_pagetop with context%}
{% from "common/macros.njk" import show_admin_sections_to_read, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import topics, policies, faqs, admin_topics_to_read, show_admin_summary with context %}

{{ show_week_pagetop(8, "admin") }}

{% call show_admin_summary() %}
1. Submit post-lecture quiz
1. Submit peer evaluations on TEAMMATES {{ timing_badge("by Saturday") }}
{% endcall %}

<div id="additional">

#### {{ thumb(1) }} Submit post-lecture quiz

* As per usual.

#### {{ thumb(2) }} Submit peer evaluations on TEAMMATES {{ timing_badge("by Saturday", "secondary") }}

* **Peer Evaluation Round 1** will open on TEAMMATES. You will receive the submission link soon. **If you do not submit feedback responses, you will forfeit participation marks that you earned based on feedback ratings received from others**.

</div>

{{ show_admin_sections_to_read(topics, policies, faqs, admin_topics_to_read.week8, is_flat=false ) }}