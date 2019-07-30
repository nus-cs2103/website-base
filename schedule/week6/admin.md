{% from "schedule/index.md" import show_week_pagetop with context%}
{% from "common/macros.njk" import show_admin_sections_to_read, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import topics, policies, faqs, admin_topics_to_read, show_admin_summary with context %}

{{ show_week_pagetop(6, "admin") }}

{% call show_admin_summary() %}

1. Submit post-lecture quiz
1. [optional] Submit mid-term feedback for the teaching team {{ timing_badge("by Saturday", "secondary") }}
{% endcall %}

<div id="additional">

#### {{ thumb(1) }} Submit post-lecture quiz

* As per usual.

#### {{ thumb(2) }} [optional] Submit mid-term feedback for the teaching team {{ timing_badge("by Saturday", "secondary") }}
* **An anonymous survey to submit feedback about the teaching team** is now open on IVLE. Please take a few minutes to give feedback to your tutors. As usual, you can use the 'anonymous feedback' feature of IVLE to send us feedback any time.

</div>

{{ show_admin_sections_to_read(topics, policies, faqs, admin_topics_to_read.week6, is_flat=false ) }}