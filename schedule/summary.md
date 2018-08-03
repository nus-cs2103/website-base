{% import "common/outcomes.njk" as outcomes with context %}
{% from "common/macros.njk" import  show_stars, show_priority_style with context %}
{% import "se-book-adapted/config.njk" as config with context %}

{% from "schedule/index.md" import all_outcomes %}


{% macro show_unit(unit) -%}
{% set chapter = unit.location[0] %}
{% set path_as_array = unit.location.slice(1,4) %}
{% set path = path_as_array.join("/") %}
{% set full_path = unit.location.join("/") %}
{% if not unit.priority %}
  {% set priority = config.get_priority(chapter, path_as_array) %}
{% else %}
  {% set priority = unit.priority %}
{% endif %}
<span class="bg-light text-{{ show_priority_style(priority) }}">{{ unit.location | join("/") }} {{ show_stars(priority) }}</span>
{%- endmacro %}

{% macro show_item(item) -%}
{% if item.week %}
<br><big><md>**Week {{ item.week }}**</md></big>
{% elif item.name %}
<br>{{ fas_circle }} **{{ item.name }}**
{% elif item.heading %}
<br>&nbsp;&nbsp;&nbsp;{{ far_circle }} {{ item.heading }} {{ show_stars(item.priority) if item.priority }} :<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
{% elif item.location %}
{{ show_unit(item) | trim }}
{% endif %}
{%- endmacro %}


{% for item in all_outcomes %}&nbsp;{{ show_item(item) | trim }}{% endfor %}
