<frontmatter>
title: "Timeline"
header: header.md
footer: footer.md
head: scheduleHead.md
pageNav: 3
</frontmatter>

{% import "common/topics.njk" as topics with context %}
{% from "common/macros.njk" import get_week_start_date with context %}

<div class="website-content">

# Summary of the Module Timeline

<box type="warning" dismissible>
<span id="warnings">

* Please try to **follow instructions closely**. If you deviate, our grading scripts will not be able to detect your work.
* The deadline to complete tasks allocated to the week is the **<tooltip content="e.g., if your tutorial is on Thursday, the deadline is Wednesday 23.59">midnight before your tutorial day</tooltip>**, unless stated otherwise. Our scripts that detect your work run at midnight and only the work that's done by midnight will be eligible for marks (for cases where the task is graded).
* You may have to **go through the weekly topics<span tags="m--cs2113"> (and do the weekly programming exercises)</span> before attempting weekly project tasks** as the knowledge from those topics may be needed to complete the project tasks.

</span>
</box>

{% macro show_link(week_num, icon, page) -%}<small><small><a href="week{{ week_num }}/{{ page }}" class="badge badge-light mr-1">%%{{ icon }}%%</a></small></small>{%- endmacro %}


{% for week_num in range(1, 14) %}
{% set start_day = get_week_start_date(week_num, format_normal) %}

<div tags="m--cs2103 m--cs2113">

### <a href="week{{ week_num }}/" class="badge badge-pill badge-dark"><small>**Week {{ week_num }}** <small>- {{ start_day }}</small></small></a> {{ show_link(week_num, icon_book, "topics.html") }}{{ show_link(week_num, icon_project, "project.html") }}{{ show_link(week_num, icon_tutorial, "tutorial.html") }}{{ show_link(week_num, icon_info, "admin.html") }}

</div>
<div tags="m--tic2002">

### <a href="week{{ week_num }}/" class="badge badge-pill badge-dark"><small>**Week {{ week_num }}** <small>- {{ weeks[week_num-1].day }}</small></small></a> {{ show_link(week_num, icon_book, "topics.html") }}{{ show_link(week_num, icon_todo, "admin-" + (module | lower) + ".html") }}

</div>

<include src="week{{ week_num }}/index.md#summary" optional />
{% endfor %}

</div>
