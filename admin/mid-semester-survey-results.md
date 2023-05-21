<frontmatter>
title: "Admin: Mid-Semester Survey Followup"
pageNav: 3
</frontmatter>

{% if current_week in ["6", "7", "8", "9", "10", "11", "12", "13"] and course in ['CS2103', 'TIC2002', 'TEE3201'] %}

<include src="../_course-{{ course }}/mid-semester-survey-results.md" />

{% else %}
<br>
This page is available during weeks 7-13 only!
{% endif %}
