{% from "schedule/index.md" import show_week_pagetop with context%}
{{ show_week_pagetop(4, "admin") }}

<panel type="seamless" header="%%{{ icon_info }} TLDR%%" >
<span id="summary">

**Admin:**
1. Accept GitHub invitation from the module organization
1. Practice peer evaluation on TEAMMATES
</span>
</panel>
<p/>

<div id="additional">

* We will be adding you all to {{ module | lower }}-{{ semester }} github org. **Please accept the invitation sent by GitHub** as you need to be a member of the org for some of the future module activities. If you did not receive the invitation link, you can use the link [https://github.com/orgs/nus-{{ module | lower }}-{{ semester }}/invitation](https://github.com/orgs/nus-{{ module | lower }}-{{ semester }}/invitation).

* **A practice peer evaluation/feedback session** will be set up on TEAMMATES. You should receive the submission link by Thursday noon. This session is for you get get used to the system and also to get to know the evaluation criteria. This round of peer evaluations are not used for grading. Email `{{ module | lower }}@comp.nus.edu.sg` if you did not receive the submission link on time.
</div>

{% import "common/macros.njk" as macros with context %}
{% from "common/admin.njk" import topics, policies, faqs, admin_topics_to_read with context %}

{{ macros.show_admin_sections_to_read(topics, policies, faqs, admin_topics_to_read.week4, is_flat=false ) }}