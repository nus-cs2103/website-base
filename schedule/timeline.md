<frontmatter>
title: "Timeline"
header: header.md
footer: footer.md
head: scheduleHead.md
pageNav: 3
</frontmatter>

{% import "common/topics.njk" as topics with context %}
{% from "schedule/index.md" import all_topics, weeks with context %}


# Summary of the Module Timeline

<box type="warning" dismissible>
<span id="warnings">

* Please try to **follow instructions closely**. If you deviate, our grading scripts will not be able to detect your work.
* The deadline to complete tasks allocated to the week is the **<tooltip content="e.g., if your tutorial is on Thursday, the deadline is Wednesday 23.59">midnight before your tutorial day</tooltip>**, unless stated otherwise. Our scripts that detect your work run at midnight and only the work that's done by midnight will be eligible for marks (for cases where the task is graded).
* You may have to **go through the weekly topics before attempting weekly project tasks** as the knowledge from those topics may be needed to complete the iP tasks.

</span>
</box>

{% macro show_links(week_num) -%}
<small><small><a href="week{{ week_num }}/project.html" class="badge badge-light">%%{{ icon_book }}%%</a></small></small><small><small><a href="week{{ week_num }}/topics.html" class="badge badge-light">%%{{ icon_project }}%%</a></small></small><small><small><a href="week{{ week_num }}/tutorial-{{ module | lower }}.html" class="badge badge-light">%%{{ icon_tutorial }}%%</a></small></small><small><small><a href="week{{ week_num }}/admin.html" class="badge badge-light">%%{{ icon_info }}%%</a></small></small>
{%- endmacro %}
{% for week_num in range(1, 14) %}

### <a href="week{{ week_num }}/" class="badge badge-pill badge-dark"><small>**Week {{ week_num }}** <small>- {{ weeks[week_num-1].day }}</small></small></a> {{ show_links(week_num) }}

<include src="week{{ week_num }}/notices-{{ module }}.md#summary" optional />
{% endfor %}



