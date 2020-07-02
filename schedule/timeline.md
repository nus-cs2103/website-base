<frontmatter>
title: "Timeline"
header: header.md
footer: footer.md
head: scheduleHead.md
pageNav: 3
</frontmatter>

{% import "common/topics.njk" as topics with context %}
{% from "common/macros.njk" import embed_topic, get_week_start_date with context %}

<div class="website-content">

# Summary of the Module Timeline

{{ embed_topic("../admin/weeklySchedule.md#week-definition", "Admin " + icon_embedding + " Weekly schedule → The " + module_pair + " week", "1") }}
<p/>
{{ embed_topic("../admin/weeklySchedule.md#deadline-definition", "Admin " + icon_embedding + " Weekly schedule → Deadline for weekly tasks", "1") }}

<p/>
<hr>

{% macro show_link(week_num, icon, page) -%}<small><small><a href="week{{ week_num }}/{{ page }}" class="badge badge-light mr-1">%%{{ icon }}%%</a></small></small>{%- endmacro %}


{% for week_num in range(1, 14) %}
{% set start_day = get_week_start_date(week_num, format_normal) %}

<div tags="m--cs2103 m--cs2113">

### <a href="week{{ week_num }}/" class="badge badge-pill badge-dark"><small>**Week {{ week_num }}** <small>- {{ start_day }}</small></small></a> {{ show_link(week_num, icon_book, "topics.html") }}{{ show_link(week_num, icon_project, "project.html") }}{{ show_link(week_num, icon_tutorial, "tutorial.html") }}{{ show_link(week_num, icon_info, "admin.html") }}

</div>
<div tags="m--tic2002">

### <a href="week{{ week_num }}/" class="badge badge-pill badge-dark"><small>**Week {{ week_num }}** <small>- {{ start_day }}</small></small></a> {{ show_link(week_num, icon_book, "topics.html") }}{{ show_link(week_num, icon_todo, "admin-" + (module | lower) + ".html") }}

</div>
<div tags="m--te3201">

### <a href="week{{ week_num }}/" class="badge badge-pill badge-dark"><small>**Week {{ week_num }}** <small>- {{ start_day }}</small></small></a>

</div>
<div class="indented-level2">

<include src="week{{ week_num }}/index.md#summary" optional />
</div>
{{ line_double }}

{% endfor %}

</div>
