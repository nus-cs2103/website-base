{% from "schedule/index.md" import show_week_pagetop with context%}
{% from "common/macros.njk" import show_admin_sections_to_read, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import topics, policies, faqs, admin_topics_to_read, show_admin_summary with context %}

{{ show_week_pagetop(4, "admin") }}

{% call show_admin_summary() %}
1. Accept GitHub invitation from the module organization
1. Submit post-lecture quiz
{% endcall %}

<div id="additional">

#### {{ thumb(1) }} Accept GitHub invitation from the module organization

* We will be adding you all to {{ module | lower }}-{{ semester }} github org. **Please accept the invitation sent by GitHub** as you need to be a member of the org for some of the future module activities. If you did not receive the invitation link, you can use the link [https://github.com/orgs/nus-{{ module | lower }}-{{ semester }}/invitation](https://github.com/orgs/nus-{{ module | lower }}-{{ semester }}/invitation).

#### {{ thumb(2) }} Submit post-lecture quiz

* As per usual.

</div>

{{ show_admin_sections_to_read(topics, policies, faqs, admin_topics_to_read.week4, is_flat=false ) }}