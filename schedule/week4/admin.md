{% from "schedule/index.md" import show_week_pagetop with context%}
{% from "common/macros.njk" import show_admin_sections_to_read, show_as_tab, thumb with context %}
{% from "common/admin.njk" import topics, policies, faqs, admin_topics_to_read, show_admin_summary with context %}

{{ show_week_pagetop(4, "admin") }}

{% call show_admin_summary() %}
1. Accept GitHub invitation from the module organization
1. Practice peer evaluation on TEAMMATES
{% endcall %}

<div id="additional">

#### {{ thumb(1) }} Accept GitHub invitation from the module organization

* We will be adding you all to {{ module | lower }}-{{ semester }} github org. **Please accept the invitation sent by GitHub** as you need to be a member of the org for some of the future module activities. If you did not receive the invitation link, you can use the link [https://github.com/orgs/nus-{{ module | lower }}-{{ semester }}/invitation](https://github.com/orgs/nus-{{ module | lower }}-{{ semester }}/invitation).

#### {{ thumb(2) }} Practice peer evaluation on TEAMMATES

* **A practice peer evaluation/feedback session** will be set up on TEAMMATES. You should receive the submission link by Thursday noon. This session is for you get get used to the system and also to get to know the evaluation criteria. This round of peer evaluations are not used for grading. Email `{{ module | lower }}@comp.nus.edu.sg` if you did not receive the submission link on time.
</div>

{{ show_admin_sections_to_read(topics, policies, faqs, admin_topics_to_read.week4, is_flat=false ) }}