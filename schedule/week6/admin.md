{% from "schedule/index.md" import show_week_pagetop with context%}
{% from "common/macros.njk" import show_admin_sections_to_read, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import topics, policies, faqs, admin_topics_to_read, show_admin_summary with context %}

{{ show_week_pagetop(6, "admin") }}

{% call show_admin_summary() %}

1. Submit post-lecture quiz
1. [optional] Submit mid-term feedback for the teaching team {{ timing_badge("by Sunday", "secondary") }}
{% endcall %}

<div id="additional">

#### {{ thumb(1) }} Submit post-lecture quiz

* As per usual.

#### {{ thumb(2) }} [optional] Submit mid-term feedback for the teaching team {{ timing_badge("by Sunday", "secondary") }}
* **An anonymous survey to submit feedback about the teaching team** will open on LumiNUS around Monday. You will receive an email when it opens. Please take a few minutes to give feedback to your tutors.

</div>

{{ show_admin_sections_to_read(topics, policies, faqs, admin_topics_to_read.week6, is_flat=false ) }}