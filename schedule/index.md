<frontmatter>
title: "Full Schedule of Module Activities"
footer: footer.md
</frontmatter>

<link rel="stylesheet" href="{{baseUrl}}/css/main.css">
<link rel="stylesheet" href="{{baseUrl}}/css/schedule.css">

<include src="../common/header.md" />

<div class="website-content">

# Full Schedule of Module Activities

<panel header="### <small>**{{glyphicon_calendar}} Tutorial Timetable**</small>" no-close>
  <include src="overview/tutorialSchedule.md"/>
</panel>
<include src="overview/index.md" name=":exclamation: **Info relevant to all weeks**" dynamic />
<p/>

{% set weeks = [
    {num: "1", day:"Aug 13"},
    {num: "2", day:"Aug 20"},
    {num: "3", day:"Aug 27"}, 
    {num: "4", day:"Sep 3"},
    {num: "5", day: "Sep 10" },
    {num: "6", day: "Sep 17" },
    {num: "7", day: "Oct 1" },
    {num: "8", day: "Oct 8" },
    {num: "9", day: "Oct 15" },
    {num: "10", day: "Oct 22" },
    {num: "11", day: "Oct 29" },
    {num: "12", day: "Nov 5" },
    {num: "13", day: "Nov 12" }
] %}


{% set current_weeks = ["5"] %}


{% macro show_past_week(week) %}
<panel type="seamless" src="week{{ week.num }}/index.md" dynamic no-close>
<span slot="header" class="panel-title week-past"> Week {{ week.num }} [{{ week.day }}]</span>
</panel>
{% endmacro %}


{% macro show_future_week(week) %}
<panel type="seamless" src="week{{ week.num }}/index.md" dynamic no-close>
<span slot="header" class="panel-title week-future"> Week {{ week.num }} [{{ week.day }}]</span>
</panel>
{% endmacro %}


{% macro show_current_week(week) %}
<panel type="seamless" expanded no-close>
<span slot="header" class="panel-title week"> Week {{ week.num }} [{{ week.day }}]</span>
  <include src="week{{ week.num }}/index.md"/>
</panel>
{% endmacro %}


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