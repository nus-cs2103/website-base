{% from "schedule/index.md" import all_outcomes with context %}
{% from "common/tutorial.njk" import  show_week_evidences with context %}
{{ show_week_evidences("5", all_outcomes) }}