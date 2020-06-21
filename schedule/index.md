<frontmatter>
title: "Schedule"
header: header.md
footer: footer.md
head: scheduleHead.md
pageNav: 1
</frontmatter>

{% import "common/topics.njk" as topics with context %}
{% from "admin/admin-tasks.mbdf" import show_weekly_admin_tasks with context %}
{% from "common/macros.njk" import get_week_start_date with context %}
{% from "_config.mbdf" import weekly_textbook_topics with context %}

{#
-1: site not ready, lands in the module intro page
0: site ready but semester hasn't started, lands in the module intro page
14: exam period, lands in the module intro page
15: site no longer used, lands in the module intro page
1..13: site is active, lands in the week's schedule page
#}
{% set current_week = "-1" %}


{% macro show_week_pagetop(week_num, category) %}


{% set categories = {
  notices: {name: "Summary", file: "index", icon: icon_announcement, pagenav: 4},
  topics: {name: "Topics", file: "topics", icon: icon_book, pagenav: 3},
  project: {name: "Project", file: "project", icon: icon_project, pagenav: 4},
  tutorial: {name: "Tutorial", file: "tutorial", icon: icon_tutorial, pagenav: 4},
  admin: {name: "Admin Info", file: "admin", icon: icon_info, pagenav: 4}
} %}

<frontmatter>
title: "Week {{ week_num }} - {{ categories[category].name }}"
header: header.md
footer: footer.md
head: scheduleHead.md
pageNav: {{ categories[category].pagenav }}
</frontmatter>

<nav>
<ul class="pagination mt-2">
{%- set previous_status = " disabled" if week_num == 1 else "" -%}
{%- set next_status = " disabled" if week_num == 13 else "" -%}
<li class="page-item{{ previous_status }}"><a class="page-link" href="../week{{ (week_num - 1) }}/"><md>:glyphicon-chevron-left: **Previous Week**</md></a></li>
<li class="page-item">&nbsp;&nbsp;&nbsp;</li>
{% for c,v in categories %}
  {%- set is_active = " active" if categories[category] == v else "" -%}
  <li class="page-item{{ is_active }}"><a class="page-link" href="{{v.file}}.html">{{ v.icon }} {{v.name}}</a></li>
</li>
{% endfor %}
<li class="page-item">&nbsp;&nbsp;&nbsp;</li><li class="page-item{{ next_status }}"><a class="page-link" href="../week{{ (week_num + 1) }}/"><md>**Next Week** :glyphicon-chevron-right:</md></a></li>
</ul>
</nav>

<p/>

# Week {{ week_num }} <small><small>%%[{{ get_week_start_date(week_num | int, format_normal) }}]%% - {{ categories[category].name }}</small></small>

{% endmacro %}


{% macro show_week_summary(week_num) %}

<span id="summary">
<div class="container">
  <div class="row">
  <div class="col-sm border-right border-bottom">

{{ topics.show_week_schedule_main(week_num, weekly_textbook_topics, "", is_toc=true, is_flat=true) }}

<panel type="seamless" header="%%Full ToC%%">
  <include src="topics.md#toc" optional />
</panel>

  </div>
  <div class="col-sm border-bottom">

**Admin:**
<include src="admin.md#summary" optional/>
<include src="project-{{ module | lower }}.mbdf#summary" optional/>

  </div>
  </div>
</div>
</span>
<br>
{% endmacro %}

{% macro show_project_summary(ip_file=false, tp_file=false, milestone=false) %}
<div id="summary" class="lead border-bottom border-left ml-3 mb-3 pl-2" style="color: purple;">

{% if ip_file %}
**iP:**
<include src="../../admin/{{ ip_file }}#summary" />
{% endif %}
{% if tp_file %}
**tP:** {% if milestone %}<span class="border rounded text-success border-success pr-1 pl-1">:fas-tag: **{{ milestone }}**</span>{% endif %}
<include src="../../admin/{{ tp_file }}#summary" />
{% endif %}
</div>

{% endmacro %}


{% macro show_week_index_page(week_num) %}
<div class="website-content">
{{ show_week_pagetop(week_num, "notices") }}

<include src="notices-{{ module | lower }}.mbdf" optional />

{{ show_week_summary(week_num) }}
</div>
{% endmacro %}


{% macro show_week_admin_page(week_num) %}
<div class="website-content">
{{ show_week_pagetop(week_num, "admin") }}

{% if week_num == "1" %}
<box type="info" dismissible>

Admin info relevant to the week will appear in this tab.
</box>
{% endif %}

{{ show_weekly_admin_tasks(week_num) }}
</div>
{% endmacro %}


{% macro show_week_topics_page(week_num) %}
<div class="website-content">
{{ show_week_pagetop(week_num, "topics") }}

{% if week_num == "1" %}
<box type="info" dismissible>

* Topics allocated to the week will appear in this tab.
* If the lecture is in the 2nd half of the week (i.e., Wednesday 12 noon or later), the lecture in week `N` will cover topics allocated to the week `N+1` e.g., **Lecture 1 will cover Week 2 topics**, and so on.
</box>
{% endif %}
{{ topics.show_week_schedule(week_num, weekly_textbook_topics) }}
</div>
{% endmacro %}


{% macro show_week_tutorial_page(week_num) %}
<div class="website-content">
{{ show_week_pagetop(week_num, "tutorial") }}

{% if week_num == "1" %}
<box type="info" dismissible>

Information relevant to the week's tutorial will appear in this tab.
</box>
{% endif %}
<include src="tutorial-{{ module | lower }}.mbdf" optional />
</div>
{% endmacro %}


{% macro show_week_project_page(week_num) %}
<div class="website-content">
{{ show_week_pagetop(week_num, "project") }}

{% if week_num == "1" %}
<box type="info" dismissible>

Project-related information relevant to the week will appear in this tab.
</box>
{% endif %}
<include src="project-{{ module | lower }}.mbdf" optional />
</div>
{% endmacro %}


<!-- ============================= page content ============================================ -->

{% set week_to_show = "1" if current_week in ["-1", "0", "14", "15"] else current_week %}
<include src="week{{ week_to_show }}/index.md" />
