{% from "schedule/index.md" import show_week_pagetop with context%}
{% import "common/macros.njk" as macros with context %}
{% from "common/admin.njk" import topics, policies, faqs, admin_topics_to_read, show_admin_summary with context %}

{{ show_week_pagetop(3, "admin") }}

{% call show_admin_summary() %}
1. Submit post-lecture quiz
1. CS2103 students: Form teams during the tutorial
{% endcall %}

<div id="additional">

#####

* **Post-lecture quiz**: As usual, read weekly topics allocated for this week. Submit the post-lecture quiz to test your knowledge of those topics. The quiz link will be emailed to you on the previous week's Friday.


</div>

{{ macros.show_admin_sections_to_read(topics, policies, faqs, admin_topics_to_read.week3, is_flat=false ) }}