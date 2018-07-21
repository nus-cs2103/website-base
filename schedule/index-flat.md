<frontmatter>
title: "Full Schedule of Module Activities (flat version)"
footer: footer.md
</frontmatter>

{% import "common/outcomes.njk" as outcomes with context %}
{% from "schedule/index.md" import weeks, current_weeks, all_outcomes %}

{% macro show_week_outcomes(week_num, path="") %}
### {{ icon_outcome }} Outcomes
<div class="indented">
{{ outcomes.show_week_schedule_main(week_num, all_outcomes, path) }}
</div>
{% endmacro %}


{% macro show_week_todos(week_num, path="") %}
### {{ icon_todo }} Todo
<div class="indented">
<include src="{{ path }}todo.md" />
</div>
{% endmacro %}


{% macro show_week_tutorial(week_num, path="") %}
### {{ icon_tutorial }} Tutorial {{ week_num }}
<div class="indented">
<include src="{{ path }}tutorial.md" />
</div>
{% endmacro %}


{% macro show_week_lecture(week_num, path="") %}
### {{ icon_lecture }} Lecture {{ week_num }}
<div class="indented">
<include src="{{ path }}lecture.md" />
</div>
{% endmacro %}


{% macro show_week_schedule(week_num, path="") %}
{{ show_week_todos(week_num, path) }}

{# omit outcomes if it is the first week #}
{% if week_num != "1" %}
  {{ show_week_outcomes(week_num, path) }}
{% endif %}

{{ show_week_tutorial(week_num, path) }}
{{ show_week_lecture(week_num, path) }}

{% endmacro %}


{% macro show_past_week(week) %}
<panel type="seamless" src="week{{ week.num }}/index.md" no-close>
<span slot="header" class="card-title week-past"> Week {{ week.num }} [{{ week.day }}]</span>
</panel>
{% endmacro %}


{% macro show_future_week(week) %}
<panel type="seamless" src="week{{ week.num }}/index.md" no-close>
<span slot="header" class="card-title week-future"> Week {{ week.num }} [{{ week.day }}]</span>
</panel>
{% endmacro %}


{% macro show_current_week(week) %}

## Week {{ week.num }} [{{ week.day }}]
<div class="indented">
{{ show_week_schedule(week.num, "week" + week.num + "/") }}
</div>
<hr>
{% endmacro %}

<!-- ============================= page content ============================================ -->

<link rel="stylesheet" href="{{baseUrl}}/css/main.css">
<link rel="stylesheet" href="{{baseUrl}}/css/schedule.css">

<include src="../common/header-flat.md" />

<div class="website-content" id="main">

# Full Schedule of Module Activities

<panel src="overview/index.md" header=":exclamation: **Info relevant to all weeks**"  />
<panel src="../admin/tutorials.md#tutorialTimetable" header="**{{glyphicon_calendar}} Tutorial Timetable**" />

<p/>

{% for week in weeks %}
{% set current_week_num = current_weeks[0] | int %}
{% set week_num = week.num | int %}
{% if week.num in current_weeks %}
  {{ show_current_week(week) }}
{% elseif week_num < current_week_num %}
  {{ show_past_week(week) }}
{% else %}
  {{ show_future_week(week) }}
{% endif %}
{% endfor %}


</div>