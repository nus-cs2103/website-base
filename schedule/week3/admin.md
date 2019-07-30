{% from "schedule/index.md" import show_week_pagetop with context%}
{% from "common/macros.njk" import show_admin_sections_to_read, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import topics, policies, faqs, admin_topics_to_read, show_admin_summary with context %}

{{ show_week_pagetop(3, "admin") }}

{% call show_admin_summary() %}
1. Submit post-lecture quiz
1. CS2103 students: Form teams during the tutorial
{% endcall %}

<div id="additional">

#### {{ thumb(1) }} Submit post-lecture quiz

* **Post-lecture quiz**: As usual, read weekly topics allocated for this week. Submit the post-lecture quiz to test your knowledge of those topics. The quiz link will be emailed to you on the previous week's Friday.

#### {{ thumb(1) }} CS2103 students: Form teams during the tutorial

* See the [{{ show_as_tab("Tutorial", icon_tutorial) }}](tutorial-{{ module | lower }}.html) tab for more info.

</div>

{{ show_admin_sections_to_read(topics, policies, faqs, admin_topics_to_read.week3, is_flat=false ) }}