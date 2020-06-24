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
{% from "_module-" + module + "/weeklyTextbookTopics.mbdf" import weekly_textbook_topics with context %}

{#
-1: site not ready, lands in the module intro page
0: site ready but semester hasn't started, lands in the module intro page
14: exam period, lands in the module intro page
15: site no longer used, lands in the module intro page
1..13: site is active, lands in the week's schedule page
#}
{% set current_week = "-1" %}


{% macro show_week_pagetop(week_num, category) %}

{% if module == "TIC2002" %}
  {% set categories = {
    notices: {name: "Summary", file: "index", icon: icon_announcement, pagenav: 4},
    topics: {name: "Topics", file: "topics", icon: icon_book, pagenav: 3},
    admin: {name: "Tasks", file: "admin", icon: icon_todo, pagenav: 4}
  } %}
{% elseif module == "TE3201" %}
  {% set categories = {
    notices: {name: "Summary", file: "index", icon: icon_announcement, pagenav: 1},
    topics_py: {name: "Programming Topics", file: "topics-py", icon: ":fas-code:", pagenav: 4},
    topics: {name: "SE Topics", file: "topics", icon: icon_book, pagenav: 3},
    admin: {name: "Tasks", file: "admin", icon: ":fas-tasks:", pagenav: 4}
  } %}
{% else %}
  {% set categories = {
    notices: {name: "Summary", file: "index", icon: icon_announcement, pagenav: 4},
    topics: {name: "Topics", file: "topics", icon: icon_book, pagenav: 3},
    project: {name: "Project", file: "project", icon: icon_project, pagenav: 4},
    tutorial: {name: "Tutorial", file: "tutorial", icon: icon_tutorial, pagenav: 4},
    admin: {name: "Admin Info", file: "admin", icon: icon_info, pagenav: 4}
  } %}
{% endif %}

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
  <li class="page-item{{ is_active }}"><a class="page-link" href="{{v.file}}.html"><md>{{ v.icon }}</md> {{v.name}}</a></li>
</li>
{% endfor %}
<li class="page-item">&nbsp;&nbsp;&nbsp;</li><li class="page-item{{ next_status }}"><a class="page-link" href="../week{{ (week_num + 1) }}/"><md>**Next Week** :glyphicon-chevron-right:</md></a></li>
</ul>
</nav>

<p/>

# Week {{ week_num }} <small><small>%%[{{ get_week_start_date(week_num | int, format_normal) }}]%% - {{ categories[category].name }}</small></small>

{% endmacro %}


{% macro show_week_summary(week_num) %}

{% if module == "TIC2002" %}
<span id="summary">
<div class="container">
  <div class="row">
  <div class="col-sm border-right">

<md>**{{ icon_book }} Topics Summary:**</md>

{{ topics.show_week_schedule_main(week_num, weekly_textbook_topics, "", is_toc=true, is_flat=true) }}

<panel type="seamless" header="%%Full ToC%%">
  <include src="topics.md#toc" optional />
</panel>

  </div>
  <div class="col-sm">

<md>**{{ icon_todo }} Tasks Summary:**</md>
<include src="admin-{{ module | lower }}.mbdf#summary" optional/>

  </div>
  </div>
</div>
</span>
<br>

{% elseif module == "TE3201" %} {#--------------------------------------------------------------------------------#}

<span id="summary">
<div class="container">
  <div class="row">
  <div class="col-sm" style="border-right: 1px dotted lightgrey">

#### <a href="topics-py.html" class="badge badge-light">:fas-code: Programming Topics</a>
<include src="../programming-topics.mbdf#week{{ week_num  }}-toc" optional />

  </div>
  <div class="col-sm">

#### <a href="topics.html" class="badge badge-light">{{ icon_book }} SE Topics</a>
{{ topics.show_week_schedule_main(week_num, weekly_textbook_topics, "", is_toc=true, is_flat=true) }}

<panel type="seamless" header="%%Full ToC%%">
  <include src="topics.md#toc" optional />
</panel>

  </div>
  </div>
  <div class="row" style="border-top: 1px dotted lightgrey">
  <div class="col-sm">

#### <a href="admin.html" class="badge badge-light mt-2">:fas-tasks: Tasks</a>
<include src="admin-{{ module | lower }}.mbdf#summary" optional/>
  </div>
  </div>
</div>
</span>
<br>

{% else %} {#---------------------------------------------------------------------------------------#}

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
{% endif %}
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

{% if module in ["TIC2002", "TE3201"] %}
<include src="admin-{{ module | lower }}.mbdf" optional />
{% else %}
{{ show_weekly_admin_tasks(week_num) }}
{% endif %}
</div>
{% endmacro %}


{% macro show_week_topics_page(week_num) %}
<div class="website-content">
{{ show_week_pagetop(week_num, "topics") }}

{% if week_num == "1" %}
<box type="info" dismissible>

Topics allocated to the week will appear in this tab.
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


{% macro show_programming_topics_page(week_num) %}
<div class="website-content">
{{ show_week_pagetop(week_num, "topics_py") }}

{% if week_num == "1" %}
<box type="info" dismissible>

Programming topics allocated to the week will appear in this tab.
</box>
{% endif %}
<include src="../programming-topics.mbdf#week{{ week_num }}" optional />
</div>
{% endmacro %}


<!-- ============================= page content ============================================ -->

{% set week_to_show = "1" if current_week in ["-1", "0", "14", "15"] else current_week %}
<include src="week{{ week_to_show }}/index.md" />
