{% from "schedule/index.md" import show_week_pagetop with context%}
{% from "common/macros.njk" import show_admin_sections_to_read, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import topics, policies, faqs, admin_topics_to_read, show_admin_summary with context %}

{{ show_week_pagetop(5, "admin") }}

{% call show_admin_summary() %}

1. Submit post-lecture quiz
1. Practice peer evaluation on TEAMMATES {{ timing_badge("by Saturday", "secondary") }}
{% endcall %}

<div id="additional">

#### {{ thumb(1) }} Submit post-lecture quiz

* As per usual.

#### {{ thumb(2) }} Practice peer evaluation on TEAMMATES {{ timing_badge("by Saturday", "secondary") }}

* **A practice peer evaluation/feedback session** will be set up on TEAMMATES. You should receive the submission link by Thursday noon. This session is for you get get used to the system and also to get to know the evaluation criteria. This round of peer evaluations are not used for grading. Email `{{ module | lower }}@comp.nus.edu.sg` if you did not receive the submission link on time.

</div>

{{ show_admin_sections_to_read(topics, policies, faqs, admin_topics_to_read.week5, is_flat=false ) }}