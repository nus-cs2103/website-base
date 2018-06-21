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

{% macro show_outcome_groups(outcome_groups) %}
{% for outcome_group in outcome_groups %}
<span class="activity-desc">{{ outcome_group.name }}</span>
<div class="indented">
  {% for outcome in outcome_group.outcomes %}
  {{ show_outcome(outcome.id, outcome.heading, outcome.priority, outcome.file) }}
  {% endfor %}
</div>
<p/>
{% endfor %}
{% endmacro %}


{% macro show_admin_section_to_read(heading, priority, source) %}
<panel src="{{ source }}" dynamic no-close >
<span slot="header" class="panel-title"><md>%%Admin »%% {{ heading }} {{ show_stars(priority) }}</span>
</panel>
{% endmacro %}
