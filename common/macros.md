{% macro show_priority(level) %}
{% set label_style = {"1": "danger", "2": "warning", "3": "info", "4": "success"} %}
{% set label_open = "<span class='label label-" + label_style[level] + "'>" %}
{% set star = "<span class='glyphicon glyphicon-star' aria-hidden='true'></span>" %}
{% set label_close = "&nbsp;</span>" %}
{% set stars = {"1": label_open + star + label_close, "2": label_open + star + star + label_close, "3": label_open + star + star + star + label_close, "4": label_open + star + star + star + star + label_close} %}{{stars[level] }}
{% endmacro %}

{% macro show_stars(level) %}{{ show_priority(level) | trim }}{% endmacro %}

{% macro show_outcome(id, heading, priority, file) %}
<panel no-close >
<span slot="header" class="panel-title"><md>`{{ id }}` **{{ heading }}**</md> {{ show_stars(priority) }}</span>
  <include src="{{ file }}" />
</panel>
{% endmacro %}

{% macro show_outcome_groups(week_num, outcome_groups) %}
<link rel="stylesheet" href="{{baseUrl}}/css/main.css">
<link rel="stylesheet" href="{{baseUrl}}/css/schedule.css">

<div class="website-content">

## Week {{ week_num }} - Outcomes 

<div id="main">
{% set i = 0 %}
{% for outcome_group in outcome_groups %}
<span class="activity-desc">{{ outcome_group.name }}</span>
<div class="indented">
  {% for outcome in outcome_group.outcomes %}
  {% set i = i + 1 %}
  {{ show_outcome("W" + week_num + "." + i, outcome.heading, outcome.priority, outcome.file) }}
  {% endfor %}
</div>
<p/>
{% endfor %}
</div>
</div>
{% endmacro %}


{% macro show_admin_section_to_read(heading, priority, source) %}
<panel src="{{ source }}" dynamic no-close >
<span slot="header" class="panel-title"><md>%%Admin »%% {{ heading }} {{ show_stars(priority) }}</span>
</panel>
{% endmacro %}

{% macro show_admin_sections_to_read(admin_sections) %}
<span class="activity-desc">Admin info to read:<span>
<div class="indented">
{% for admin_section in admin_sections %}
{{ show_admin_section_to_read(admin_section.heading, admin_section.priority, "../../admin/" + admin_section.source) }}
{% endfor %}
</div>
{% endmacro %}

{% macro show_week_schedule(week_num) %}
<panel type="seamless" popup-url="{{baseUrl}}/schedule/week{{ week_num }}/outcomes.html" expanded no-close>
  <span slot="header" class="panel-title activity-type">{{glyphicon_flag}} Outcomes</span>
  <div class="indented">
  <include src="outcomes.md#main" />
  </div>
</panel>

<panel type="seamless" expanded no-close>
  <span slot="header" class="panel-title activity-type">{{glyphicon_check}} Todo</span>
  <div class="indented">
  <include src="todo.md" />
  </div>
</panel>

<panel type="seamless" expanded no-close>
<span slot="header" class="panel-title activity-type">{{glyphicon_pencil}} Tutorial {{ week_num }}</span>
   <div class="indented">
   <include src="tutorial.md" />
   </div>
</panel>

<panel type="seamless" expanded no-close>
<span slot="header" class="panel-title activity-type">{{glyphicon_blackboard}} Lecture {{ week_num }}</span>
  <div class="indented">
  <include src="lecture.md" />
  </div>
</panel>

{% endmacro %}

